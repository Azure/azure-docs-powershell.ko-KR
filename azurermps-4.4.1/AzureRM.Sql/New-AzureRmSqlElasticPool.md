---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlElasticPool.md
ms.openlocfilehash: 454aac300aa3b34cbc435df455100d64c5d0abdd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711858"
---
# <span data-ttu-id="808f1-101">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="808f1-101">New-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="808f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="808f1-102">SYNOPSIS</span></span>
<span data-ttu-id="808f1-103">SQL 데이터베이스에 대 한 탄력적 데이터베이스 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="808f1-103">Creates an elastic database pool for a SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="808f1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="808f1-104">SYNTAX</span></span>

```
New-AzureRmSqlElasticPool -ElasticPoolName <String> [-Edition <DatabaseEdition>] [-Dtu <Int32>]
 [-StorageMB <Int32>] [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="808f1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="808f1-105">DESCRIPTION</span></span>
<span data-ttu-id="808f1-106">**AzureRmSqlElasticPool** Cmdlet은 Azure SQL 데이터베이스에 대 한 탄력적 데이터베이스 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="808f1-106">The **New-AzureRmSqlElasticPool** cmdlet creates an elastic database pool for an Azure SQL Database.</span></span>

<span data-ttu-id="808f1-107">여러 매개 변수 ( *-Dtu,-DatabaseDtuMin 및-DatabaseDtuMax* )에는 해당 매개 변수에 대 한 유효한 값 목록에서 값을 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="808f1-107">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="808f1-108">예를 들어 표준 100 eDTU 풀에 대 한-DatabaseDtuMax은 10, 20, 50 또는 100 으로만 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="808f1-108">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="808f1-109">유효한 값에 대 한 자세한 내용은 [탄력적 풀](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)의 특정 크기 풀에 대 한 표를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="808f1-109">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

## <span data-ttu-id="808f1-110">예제의</span><span class="sxs-lookup"><span data-stu-id="808f1-110">EXAMPLES</span></span>

### <span data-ttu-id="808f1-111">예제 1: 탄력적 풀 만들기</span><span class="sxs-lookup"><span data-stu-id="808f1-111">Example 1: Create an elastic pool</span></span>
```
PS C:\>New-AzureRmSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Edition "Standard" -Dtu 400 -DatabaseDtuMin 10 -DatabaseDtuMax 100
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/server01/elasticPools/elasticpool01
ResourceGroupName : resourcegroup01
ServerName        : server01
ElasticPoolName   : elasticpool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 400
DatabaseDtuMax    : 100
DatabaseDtuMin    : 10
StorageMB         : 409600
Tags              :
```

<span data-ttu-id="808f1-112">이 명령은 ElasticPool01 이라는 표준 서비스 계층에 탄력적 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="808f1-112">This command creates an elastic pool in the Standard service tier named ElasticPool01.</span></span> <span data-ttu-id="808f1-113">Server01 라는 서버는 ResourceGroup01 이라는 Azure 리소스 그룹에 할당 되 고,의 탄력적 풀을 호스팅합니다.</span><span class="sxs-lookup"><span data-stu-id="808f1-113">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="808f1-114">명령은 풀의 DTU 속성 값과 풀의 데이터베이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="808f1-114">The command specifies DTU property values for the pool and the databases in the pool.</span></span>

## <span data-ttu-id="808f1-115">변수</span><span class="sxs-lookup"><span data-stu-id="808f1-115">PARAMETERS</span></span>

### <span data-ttu-id="808f1-116">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="808f1-116">-DatabaseDtuMax</span></span>
<span data-ttu-id="808f1-117">풀의 단일 데이터베이스가 소비할 수 있는 최대 Dtu (데이터베이스 처리량 단위) 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="808f1-117">Specifies the maximum number of Database Throughput Units (DTUs) that any single database in the pool can consume.</span></span>
<span data-ttu-id="808f1-118">여러 버전의 기본값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="808f1-118">The default values for the different editions are as follows:</span></span>

- <span data-ttu-id="808f1-119">기본적.</span><span class="sxs-lookup"><span data-stu-id="808f1-119">Basic.</span></span> <span data-ttu-id="808f1-120">5 Dtu</span><span class="sxs-lookup"><span data-stu-id="808f1-120">5 DTUs</span></span>
- <span data-ttu-id="808f1-121">표준이.</span><span class="sxs-lookup"><span data-stu-id="808f1-121">Standard.</span></span> <span data-ttu-id="808f1-122">100 Dtu</span><span class="sxs-lookup"><span data-stu-id="808f1-122">100 DTUs</span></span>
- <span data-ttu-id="808f1-123">Premium.</span><span class="sxs-lookup"><span data-stu-id="808f1-123">Premium.</span></span> <span data-ttu-id="808f1-124">125 Dtu</span><span class="sxs-lookup"><span data-stu-id="808f1-124">125 DTUs</span></span>

<span data-ttu-id="808f1-125">유효한 값에 대 한 자세한 내용은 [탄력적 풀](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool) 의 특정 크기 풀에 대 한 표를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="808f1-125">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span></span> 


```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="808f1-126">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="808f1-126">-DatabaseDtuMin</span></span>
<span data-ttu-id="808f1-127">탄력적 풀이 풀의 모든 데이터베이스에 대해 보장 하는 최소 Dtu 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="808f1-127">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="808f1-128">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="808f1-128">The default value is zero (0).</span></span>

<span data-ttu-id="808f1-129">유효한 값에 대 한 자세한 내용은 [탄력적 풀](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)의 특정 크기 풀에 대 한 표를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="808f1-129">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="808f1-130">-Dtu</span><span class="sxs-lookup"><span data-stu-id="808f1-130">-Dtu</span></span>
<span data-ttu-id="808f1-131">탄력적 풀에 대 한 총 공유 Dtu 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="808f1-131">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="808f1-132">여러 버전의 기본값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="808f1-132">The default values for the different editions are as follows:</span></span>

- <span data-ttu-id="808f1-133">기본적.</span><span class="sxs-lookup"><span data-stu-id="808f1-133">Basic.</span></span>
<span data-ttu-id="808f1-134">100 Dtu</span><span class="sxs-lookup"><span data-stu-id="808f1-134">100 DTUs</span></span>
- <span data-ttu-id="808f1-135">표준이.</span><span class="sxs-lookup"><span data-stu-id="808f1-135">Standard.</span></span>
<span data-ttu-id="808f1-136">100 Dtu</span><span class="sxs-lookup"><span data-stu-id="808f1-136">100 DTUs</span></span>
- <span data-ttu-id="808f1-137">Premium.</span><span class="sxs-lookup"><span data-stu-id="808f1-137">Premium.</span></span>
<span data-ttu-id="808f1-138">125 Dtu</span><span class="sxs-lookup"><span data-stu-id="808f1-138">125 DTUs</span></span>

<span data-ttu-id="808f1-139">유효한 값에 대 한 자세한 내용은 [탄력적 풀](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)의 특정 크기 풀에 대 한 표를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="808f1-139">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="808f1-140">-에디션</span><span class="sxs-lookup"><span data-stu-id="808f1-140">-Edition</span></span>
<span data-ttu-id="808f1-141">탄력적 풀에 사용 되는 Azure SQL 데이터베이스의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="808f1-141">Specifies the edition of the Azure SQL Database used for the elastic pool.</span></span>
<span data-ttu-id="808f1-142">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="808f1-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="808f1-143">Premium</span><span class="sxs-lookup"><span data-stu-id="808f1-143">Premium</span></span>
- <span data-ttu-id="808f1-144">기본적</span><span class="sxs-lookup"><span data-stu-id="808f1-144">Basic</span></span>
- <span data-ttu-id="808f1-145">표준이</span><span class="sxs-lookup"><span data-stu-id="808f1-145">Standard</span></span>
- <span data-ttu-id="808f1-146">웨어하우스</span><span class="sxs-lookup"><span data-stu-id="808f1-146">DataWarehouse</span></span>
- <span data-ttu-id="808f1-147">늘이고</span><span class="sxs-lookup"><span data-stu-id="808f1-147">Stretch</span></span>
- <span data-ttu-id="808f1-148">비우거나</span><span class="sxs-lookup"><span data-stu-id="808f1-148">Free</span></span>
- <span data-ttu-id="808f1-149">PremiumRS</span><span class="sxs-lookup"><span data-stu-id="808f1-149">PremiumRS</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Database.Model.DatabaseEdition
Parameter Sets: (All)
Aliases: 
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="808f1-150">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="808f1-150">-ElasticPoolName</span></span>
<span data-ttu-id="808f1-151">이 cmdlet이 만드는 탄력적 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="808f1-151">Specifies the name of the elastic pool that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="808f1-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="808f1-152">-ResourceGroupName</span></span>
<span data-ttu-id="808f1-153">이 cmdlet이 탄력적 풀을 할당 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="808f1-153">Specifies the name of the resource group to which this cmdlet assigns the elastic pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="808f1-154">-ServerName</span><span class="sxs-lookup"><span data-stu-id="808f1-154">-ServerName</span></span>
<span data-ttu-id="808f1-155">탄력적 풀을 호스팅하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="808f1-155">Specifies the name of the server that hosts the elastic pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="808f1-156">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="808f1-156">-StorageMB</span></span>
<span data-ttu-id="808f1-157">탄력적 풀의 저장소 용량 한도 (mb)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="808f1-157">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="808f1-158">이 매개 변수를 지정 하지 않으면이 cmdlet은 *Dtu* 매개 변수의 값에 따라 달라 지는 값을 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="808f1-158">If you do not specify this parameter, this cmdlet calculates a value that depends on the value of the *Dtu* parameter.</span></span>

<span data-ttu-id="808f1-159">가능 값에 대 한 [eDTU 및 저장소 제한을](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="808f1-159">See [eDTU and storage limits](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) for possible values.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="808f1-160">태그</span><span class="sxs-lookup"><span data-stu-id="808f1-160">-Tags</span></span>
<span data-ttu-id="808f1-161">이 cmdlet이 탄력적 풀과 연결 하는 해시 테이블 형식으로 키-값 쌍의 사전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="808f1-161">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the elastic pool.</span></span> <span data-ttu-id="808f1-162">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="808f1-162">For example:</span></span>

<span data-ttu-id="808f1-163">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="808f1-163">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="808f1-164">-확인</span><span class="sxs-lookup"><span data-stu-id="808f1-164">-Confirm</span></span>
<span data-ttu-id="808f1-165">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="808f1-165">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="808f1-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="808f1-166">-WhatIf</span></span>
<span data-ttu-id="808f1-167">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="808f1-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="808f1-168">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="808f1-168">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="808f1-169">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="808f1-169">-DefaultProfile</span></span>
<span data-ttu-id="808f1-170">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="808f1-170">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="808f1-171">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="808f1-171">CommonParameters</span></span>
<span data-ttu-id="808f1-172">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="808f1-172">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="808f1-173">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="808f1-173">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="808f1-174">입력</span><span class="sxs-lookup"><span data-stu-id="808f1-174">INPUTS</span></span>

## <span data-ttu-id="808f1-175">출력</span><span class="sxs-lookup"><span data-stu-id="808f1-175">OUTPUTS</span></span>

### <span data-ttu-id="808f1-176">ElasticPool. AzureSqlElasticPoolModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="808f1-176">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="808f1-177">상속자</span><span class="sxs-lookup"><span data-stu-id="808f1-177">NOTES</span></span>

## <span data-ttu-id="808f1-178">관련 링크</span><span class="sxs-lookup"><span data-stu-id="808f1-178">RELATED LINKS</span></span>

[<span data-ttu-id="808f1-179">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="808f1-179">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="808f1-180">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="808f1-180">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="808f1-181">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="808f1-181">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="808f1-182">제거-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="808f1-182">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="808f1-183">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="808f1-183">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)

[<span data-ttu-id="808f1-184">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="808f1-184">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
