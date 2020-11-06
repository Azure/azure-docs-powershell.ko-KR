---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlElasticPool.md
ms.openlocfilehash: 3d93b0d82a2769acce620ce97141be68c003c281
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531611"
---
# <span data-ttu-id="a82e8-101">New-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="a82e8-101">New-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="a82e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a82e8-102">SYNOPSIS</span></span>
<span data-ttu-id="a82e8-103">SQL 데이터베이스에 대 한 탄력적 데이터베이스 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a82e8-103">Creates an elastic database pool for a SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a82e8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a82e8-104">SYNTAX</span></span>

```
New-AzureRmSqlElasticPool -ElasticPoolName <String> [-Edition <DatabaseEdition>] [-Dtu <Int32>]
 [-StorageMB <Int32>] [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a82e8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a82e8-105">DESCRIPTION</span></span>
<span data-ttu-id="a82e8-106">**AzureRmSqlElasticPool** Cmdlet은 Azure SQL 데이터베이스에 대 한 탄력적 데이터베이스 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a82e8-106">The **New-AzureRmSqlElasticPool** cmdlet creates an elastic database pool for an Azure SQL Database.</span></span>

<span data-ttu-id="a82e8-107">여러 매개 변수 ( *-Dtu,-DatabaseDtuMin 및-DatabaseDtuMax* )에는 해당 매개 변수에 대 한 유효한 값 목록에서 값을 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a82e8-107">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="a82e8-108">예를 들어 표준 100 eDTU 풀에 대 한-DatabaseDtuMax은 10, 20, 50 또는 100 으로만 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a82e8-108">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="a82e8-109">유효한 값에 대 한 자세한 내용은 [탄력적 풀](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)의 특정 크기 풀에 대 한 표를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a82e8-109">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

## <span data-ttu-id="a82e8-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a82e8-110">EXAMPLES</span></span>

### <span data-ttu-id="a82e8-111">예제 1: 탄력적 풀 만들기</span><span class="sxs-lookup"><span data-stu-id="a82e8-111">Example 1: Create an elastic pool</span></span>
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

<span data-ttu-id="a82e8-112">이 명령은 ElasticPool01 이라는 표준 서비스 계층에 탄력적 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a82e8-112">This command creates an elastic pool in the Standard service tier named ElasticPool01.</span></span> <span data-ttu-id="a82e8-113">Server01 라는 서버는 ResourceGroup01 이라는 Azure 리소스 그룹에 할당 되 고,의 탄력적 풀을 호스팅합니다.</span><span class="sxs-lookup"><span data-stu-id="a82e8-113">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="a82e8-114">명령은 풀의 DTU 속성 값과 풀의 데이터베이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a82e8-114">The command specifies DTU property values for the pool and the databases in the pool.</span></span>

## <span data-ttu-id="a82e8-115">변수</span><span class="sxs-lookup"><span data-stu-id="a82e8-115">PARAMETERS</span></span>

### <span data-ttu-id="a82e8-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a82e8-116">-AsJob</span></span>
<span data-ttu-id="a82e8-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="a82e8-117">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a82e8-118">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="a82e8-118">-DatabaseDtuMax</span></span>
<span data-ttu-id="a82e8-119">풀의 단일 데이터베이스가 소비할 수 있는 최대 Dtu (데이터베이스 처리량 단위) 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a82e8-119">Specifies the maximum number of Database Throughput Units (DTUs) that any single database in the pool can consume.</span></span>
<span data-ttu-id="a82e8-120">여러 버전의 기본값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a82e8-120">The default values for the different editions are as follows:</span></span>

- <span data-ttu-id="a82e8-121">기본적.</span><span class="sxs-lookup"><span data-stu-id="a82e8-121">Basic.</span></span> <span data-ttu-id="a82e8-122">5 Dtu</span><span class="sxs-lookup"><span data-stu-id="a82e8-122">5 DTUs</span></span>
- <span data-ttu-id="a82e8-123">표준이.</span><span class="sxs-lookup"><span data-stu-id="a82e8-123">Standard.</span></span> <span data-ttu-id="a82e8-124">100 Dtu</span><span class="sxs-lookup"><span data-stu-id="a82e8-124">100 DTUs</span></span>
- <span data-ttu-id="a82e8-125">Premium.</span><span class="sxs-lookup"><span data-stu-id="a82e8-125">Premium.</span></span> <span data-ttu-id="a82e8-126">125 Dtu</span><span class="sxs-lookup"><span data-stu-id="a82e8-126">125 DTUs</span></span>

<span data-ttu-id="a82e8-127">유효한 값에 대 한 자세한 내용은 [탄력적 풀](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool) 의 특정 크기 풀에 대 한 표를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a82e8-127">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span></span> 


```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a82e8-128">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="a82e8-128">-DatabaseDtuMin</span></span>
<span data-ttu-id="a82e8-129">탄력적 풀이 풀의 모든 데이터베이스에 대해 보장 하는 최소 Dtu 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a82e8-129">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="a82e8-130">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="a82e8-130">The default value is zero (0).</span></span>

<span data-ttu-id="a82e8-131">유효한 값에 대 한 자세한 내용은 [탄력적 풀](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)의 특정 크기 풀에 대 한 표를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a82e8-131">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a82e8-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a82e8-132">-DefaultProfile</span></span>
<span data-ttu-id="a82e8-133">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a82e8-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a82e8-134">-Dtu</span><span class="sxs-lookup"><span data-stu-id="a82e8-134">-Dtu</span></span>
<span data-ttu-id="a82e8-135">탄력적 풀에 대 한 총 공유 Dtu 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a82e8-135">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="a82e8-136">여러 버전의 기본값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a82e8-136">The default values for the different editions are as follows:</span></span>

- <span data-ttu-id="a82e8-137">기본적.</span><span class="sxs-lookup"><span data-stu-id="a82e8-137">Basic.</span></span>
<span data-ttu-id="a82e8-138">100 Dtu</span><span class="sxs-lookup"><span data-stu-id="a82e8-138">100 DTUs</span></span>
- <span data-ttu-id="a82e8-139">표준이.</span><span class="sxs-lookup"><span data-stu-id="a82e8-139">Standard.</span></span>
<span data-ttu-id="a82e8-140">100 Dtu</span><span class="sxs-lookup"><span data-stu-id="a82e8-140">100 DTUs</span></span>
- <span data-ttu-id="a82e8-141">Premium.</span><span class="sxs-lookup"><span data-stu-id="a82e8-141">Premium.</span></span>
<span data-ttu-id="a82e8-142">125 Dtu</span><span class="sxs-lookup"><span data-stu-id="a82e8-142">125 DTUs</span></span>

<span data-ttu-id="a82e8-143">유효한 값에 대 한 자세한 내용은 [탄력적 풀](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)의 특정 크기 풀에 대 한 표를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a82e8-143">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a82e8-144">-에디션</span><span class="sxs-lookup"><span data-stu-id="a82e8-144">-Edition</span></span>
<span data-ttu-id="a82e8-145">탄력적 풀에 사용 되는 Azure SQL 데이터베이스의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a82e8-145">Specifies the edition of the Azure SQL Database used for the elastic pool.</span></span>
<span data-ttu-id="a82e8-146">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a82e8-146">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a82e8-147">Premium</span><span class="sxs-lookup"><span data-stu-id="a82e8-147">Premium</span></span>
- <span data-ttu-id="a82e8-148">기본적</span><span class="sxs-lookup"><span data-stu-id="a82e8-148">Basic</span></span>
- <span data-ttu-id="a82e8-149">표준이</span><span class="sxs-lookup"><span data-stu-id="a82e8-149">Standard</span></span>
- <span data-ttu-id="a82e8-150">웨어하우스</span><span class="sxs-lookup"><span data-stu-id="a82e8-150">DataWarehouse</span></span>
- <span data-ttu-id="a82e8-151">늘이고</span><span class="sxs-lookup"><span data-stu-id="a82e8-151">Stretch</span></span>

```yaml
Type: DatabaseEdition
Parameter Sets: (All)
Aliases:
Accepted values: None, Premium, Basic, Standard, DataWarehouse, Stretch, Free, PremiumRS

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a82e8-152">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="a82e8-152">-ElasticPoolName</span></span>
<span data-ttu-id="a82e8-153">이 cmdlet이 만드는 탄력적 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a82e8-153">Specifies the name of the elastic pool that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a82e8-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a82e8-154">-ResourceGroupName</span></span>
<span data-ttu-id="a82e8-155">이 cmdlet이 탄력적 풀을 할당 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a82e8-155">Specifies the name of the resource group to which this cmdlet assigns the elastic pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a82e8-156">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a82e8-156">-ServerName</span></span>
<span data-ttu-id="a82e8-157">탄력적 풀을 호스팅하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a82e8-157">Specifies the name of the server that hosts the elastic pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a82e8-158">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="a82e8-158">-StorageMB</span></span>
<span data-ttu-id="a82e8-159">탄력적 풀의 저장소 용량 한도 (mb)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a82e8-159">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="a82e8-160">이 매개 변수를 지정 하지 않으면이 cmdlet은 *Dtu* 매개 변수의 값에 따라 달라 지는 값을 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="a82e8-160">If you do not specify this parameter, this cmdlet calculates a value that depends on the value of the *Dtu* parameter.</span></span>

<span data-ttu-id="a82e8-161">가능 값에 대 한 [eDTU 및 저장소 제한을](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a82e8-161">See [eDTU and storage limits](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) for possible values.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a82e8-162">태그</span><span class="sxs-lookup"><span data-stu-id="a82e8-162">-Tags</span></span>
<span data-ttu-id="a82e8-163">이 cmdlet이 탄력적 풀과 연결 하는 해시 테이블 형식으로 키-값 쌍의 사전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a82e8-163">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the elastic pool.</span></span> <span data-ttu-id="a82e8-164">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="a82e8-164">For example:</span></span>

<span data-ttu-id="a82e8-165">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="a82e8-165">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a82e8-166">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="a82e8-166">-ZoneRedundant</span></span>
<span data-ttu-id="a82e8-167">Azure Sql 탄력적 풀에 연결 되는 영역 중복성</span><span class="sxs-lookup"><span data-stu-id="a82e8-167">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a82e8-168">-확인</span><span class="sxs-lookup"><span data-stu-id="a82e8-168">-Confirm</span></span>
<span data-ttu-id="a82e8-169">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a82e8-169">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a82e8-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a82e8-170">-WhatIf</span></span>
<span data-ttu-id="a82e8-171">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a82e8-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a82e8-172">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a82e8-172">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a82e8-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a82e8-173">CommonParameters</span></span>
<span data-ttu-id="a82e8-174">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a82e8-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a82e8-175">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a82e8-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a82e8-176">입력</span><span class="sxs-lookup"><span data-stu-id="a82e8-176">INPUTS</span></span>

### <span data-ttu-id="a82e8-177">않아야</span><span class="sxs-lookup"><span data-stu-id="a82e8-177">None</span></span>
<span data-ttu-id="a82e8-178">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a82e8-178">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a82e8-179">출력</span><span class="sxs-lookup"><span data-stu-id="a82e8-179">OUTPUTS</span></span>

### <span data-ttu-id="a82e8-180">ElasticPool. AzureSqlElasticPoolModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="a82e8-180">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="a82e8-181">상속자</span><span class="sxs-lookup"><span data-stu-id="a82e8-181">NOTES</span></span>

## <span data-ttu-id="a82e8-182">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a82e8-182">RELATED LINKS</span></span>

[<span data-ttu-id="a82e8-183">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="a82e8-183">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="a82e8-184">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="a82e8-184">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="a82e8-185">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="a82e8-185">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="a82e8-186">제거-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="a82e8-186">Remove-AzureRmSqlElasticPool</span></span>](./Remove-AzureRmSqlElasticPool.md)

[<span data-ttu-id="a82e8-187">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="a82e8-187">Set-AzureRmSqlElasticPool</span></span>](./Set-AzureRmSqlElasticPool.md)

[<span data-ttu-id="a82e8-188">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="a82e8-188">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
