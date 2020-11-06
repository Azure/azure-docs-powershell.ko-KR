---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlElasticPool.md
ms.openlocfilehash: 563cddc1723f0706eb5cdde691e9ab960e871989
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531591"
---
# <span data-ttu-id="8cf02-101">Set-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="8cf02-101">Set-AzureRmSqlElasticPool</span></span>

## <span data-ttu-id="8cf02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8cf02-102">SYNOPSIS</span></span>
<span data-ttu-id="8cf02-103">Azure SQL 데이터베이스에서 탄력적 데이터베이스 풀의 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cf02-103">Modifies properties of an elastic database pool in Azure SQL Database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8cf02-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8cf02-104">SYNTAX</span></span>

```
Set-AzureRmSqlElasticPool [-ElasticPoolName] <String> [-Edition <DatabaseEdition>] [-Dtu <Int32>]
 [-StorageMB <Int32>] [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8cf02-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8cf02-105">DESCRIPTION</span></span>
<span data-ttu-id="8cf02-106">**AzureRmSqlElasticPool** Cmdlet은 Azure SQL Database의 탄력적 풀에 대 한 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cf02-106">The **Set-AzureRmSqlElasticPool** cmdlet sets properties for an elastic pool in Azure SQL Database.</span></span> <span data-ttu-id="8cf02-107">이 cmdlet은 풀 당 eDTUs ( *Dtu* ), 풀 당 저장소 최대 크기 ( *storagemb* ), 데이터베이스당 최대 eDTUs ( *DatabaseDtuMax* ), 데이터베이스당 최소 eDTUs ( *DatqabaseDtuMin* )을 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8cf02-107">This cmdlet can modify the eDTUs per pool ( *Dtu* ), storage max size per pool ( *StorageMB* ), maximum eDTUs per database ( *DatabaseDtuMax* ), and minimum eDTUs per database ( *DatqabaseDtuMin* ).</span></span>

<span data-ttu-id="8cf02-108">여러 매개 변수 ( *-Dtu,-DatabaseDtuMin 및-DatabaseDtuMax* )에는 해당 매개 변수에 대 한 유효한 값 목록에서 값을 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cf02-108">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="8cf02-109">예를 들어 표준 100 eDTU 풀에 대 한-DatabaseDtuMax은 10, 20, 50 또는 100 으로만 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8cf02-109">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="8cf02-110">유효한 값에 대 한 자세한 내용은 [탄력적 풀](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)의 특정 크기 풀에 대 한 표를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8cf02-110">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="8cf02-111">예제의</span><span class="sxs-lookup"><span data-stu-id="8cf02-111">EXAMPLES</span></span>

### <span data-ttu-id="8cf02-112">예제 1: 탄력적 풀의 속성 수정</span><span class="sxs-lookup"><span data-stu-id="8cf02-112">Example 1: Modify properties for an elastic pool</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Dtu 1000 -DatabaseDtuMax 100 -DatabaseDtuMin 20
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/Server01/elasticPools/ElasticPool01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
ElasticPoolName   : ElasticPool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Standard
Dtu               : 200
DatabaseDtuMax    : 100
DatabaseDtuMin    : 20
StorageMB         : 204800
Tags              :
```

<span data-ttu-id="8cf02-113">이 명령은 elasticpool01 이라는 탄력적 풀의 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cf02-113">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="8cf02-114">명령은 탄력적 풀에 대 한 Dtu 수를 1000로 설정 하 고 최소 및 최대 Dtu를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cf02-114">The command sets the number of DTUs for the elastic pool to 1000 and sets the minimum and maximum DTUs.</span></span>

### <span data-ttu-id="8cf02-115">예제 2: 탄력적 풀의 저장소 최대 크기 수정</span><span class="sxs-lookup"><span data-stu-id="8cf02-115">Example 2: Modify the storage max size of an elastic pool</span></span>
```
PS C:\>Set-AzureRmSqlDatabaseElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -StorageMB 2097152
ResourceId        : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/resourcegroup01/providers/Microsoft.Sql/servers/Server01/elasticPools/ElasticPool01
ResourceGroupName : ResourceGroup01
ServerName        : Server01
ElasticPoolName   : ElasticPool01
Location          : Central US
CreationDate      : 8/26/2015 10:00:17 PM
State             : Ready
Edition           : Premium
Dtu               : 200
DatabaseDtuMax    : 100
DatabaseDtuMin    : 20
StorageMB         : 2097152
Tags              :
```

<span data-ttu-id="8cf02-116">이 명령은 elasticpool01 이라는 탄력적 풀의 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cf02-116">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="8cf02-117">명령은 탄력적 풀의 최대 저장소를 2TB로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cf02-117">The command sets the max storage for an elastic pool to 2 TB.</span></span>

## <span data-ttu-id="8cf02-118">변수</span><span class="sxs-lookup"><span data-stu-id="8cf02-118">PARAMETERS</span></span>

### <span data-ttu-id="8cf02-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8cf02-119">-AsJob</span></span>
<span data-ttu-id="8cf02-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="8cf02-120">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="8cf02-121">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="8cf02-121">-DatabaseDtuMax</span></span>
<span data-ttu-id="8cf02-122">풀의 단일 데이터베이스가 소비할 수 있는 최대 Dtu 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cf02-122">Specifies the maximum number of DTUs that any single database in the pool can consume.</span></span> 

<span data-ttu-id="8cf02-123">유효한 값에 대 한 자세한 내용은 [탄력적 풀](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)의 특정 크기 풀에 대 한 표를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8cf02-123">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

<span data-ttu-id="8cf02-124">여러 버전의 기본값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="8cf02-124">The default values for different editions are as follows:</span></span>

- <span data-ttu-id="8cf02-125">기본적.</span><span class="sxs-lookup"><span data-stu-id="8cf02-125">Basic.</span></span>  <span data-ttu-id="8cf02-126">5 Dtu</span><span class="sxs-lookup"><span data-stu-id="8cf02-126">5 DTUs</span></span>
- <span data-ttu-id="8cf02-127">표준이.</span><span class="sxs-lookup"><span data-stu-id="8cf02-127">Standard.</span></span> <span data-ttu-id="8cf02-128">100 Dtu</span><span class="sxs-lookup"><span data-stu-id="8cf02-128">100 DTUs</span></span>
- <span data-ttu-id="8cf02-129">Premium.</span><span class="sxs-lookup"><span data-stu-id="8cf02-129">Premium.</span></span> <span data-ttu-id="8cf02-130">125 Dtu</span><span class="sxs-lookup"><span data-stu-id="8cf02-130">125 DTUs</span></span>


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

### <span data-ttu-id="8cf02-131">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="8cf02-131">-DatabaseDtuMin</span></span>
<span data-ttu-id="8cf02-132">탄력적 풀이 풀의 모든 데이터베이스에 대해 보장 하는 최소 Dtu 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cf02-132">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>

<span data-ttu-id="8cf02-133">유효한 값에 대 한 자세한 내용은 [탄력적 풀](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)의 특정 크기 풀에 대 한 표를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8cf02-133">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

<span data-ttu-id="8cf02-134">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="8cf02-134">The default value is zero (0).</span></span>

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

### <span data-ttu-id="8cf02-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cf02-135">-DefaultProfile</span></span>
<span data-ttu-id="8cf02-136">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8cf02-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8cf02-137">-Dtu</span><span class="sxs-lookup"><span data-stu-id="8cf02-137">-Dtu</span></span>
<span data-ttu-id="8cf02-138">탄력적 풀에 대 한 총 공유 Dtu 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cf02-138">Specifies the total number of shared DTUs for the elastic pool.</span></span> 

<span data-ttu-id="8cf02-139">유효한 값에 대 한 자세한 내용은 [탄력적 풀](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)의 특정 크기 풀에 대 한 표를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8cf02-139">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span> 

<span data-ttu-id="8cf02-140">여러 버전의 기본값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="8cf02-140">The default values for different editions are as follows:</span></span>

- <span data-ttu-id="8cf02-141">기본적.</span><span class="sxs-lookup"><span data-stu-id="8cf02-141">Basic.</span></span> <span data-ttu-id="8cf02-142">100 Dtu</span><span class="sxs-lookup"><span data-stu-id="8cf02-142">100 DTUs</span></span>
- <span data-ttu-id="8cf02-143">표준이.</span><span class="sxs-lookup"><span data-stu-id="8cf02-143">Standard.</span></span> <span data-ttu-id="8cf02-144">100 Dtu</span><span class="sxs-lookup"><span data-stu-id="8cf02-144">100 DTUs</span></span>
- <span data-ttu-id="8cf02-145">Premium.</span><span class="sxs-lookup"><span data-stu-id="8cf02-145">Premium.</span></span> <span data-ttu-id="8cf02-146">125 Dtu</span><span class="sxs-lookup"><span data-stu-id="8cf02-146">125 DTUs</span></span>

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

### <span data-ttu-id="8cf02-147">-에디션</span><span class="sxs-lookup"><span data-stu-id="8cf02-147">-Edition</span></span>
<span data-ttu-id="8cf02-148">탄력적 풀에 대 한 Azure SQL 데이터베이스의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cf02-148">Specifies the edition of the Azure SQL Database for the elastic pool.</span></span> <span data-ttu-id="8cf02-149">에디션을 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="8cf02-149">You cannot change the edition.</span></span> <span data-ttu-id="8cf02-150">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="8cf02-150">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="8cf02-151">않아야</span><span class="sxs-lookup"><span data-stu-id="8cf02-151">None</span></span>
- <span data-ttu-id="8cf02-152">기본적</span><span class="sxs-lookup"><span data-stu-id="8cf02-152">Basic</span></span>
- <span data-ttu-id="8cf02-153">표준이</span><span class="sxs-lookup"><span data-stu-id="8cf02-153">Standard</span></span>
- <span data-ttu-id="8cf02-154">Premium</span><span class="sxs-lookup"><span data-stu-id="8cf02-154">Premium</span></span>
- <span data-ttu-id="8cf02-155">웨어하우스</span><span class="sxs-lookup"><span data-stu-id="8cf02-155">DataWarehouse</span></span>

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

### <span data-ttu-id="8cf02-156">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="8cf02-156">-ElasticPoolName</span></span>
<span data-ttu-id="8cf02-157">탄력적 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cf02-157">Specifies the name of the elastic pool.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cf02-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cf02-158">-ResourceGroupName</span></span>
<span data-ttu-id="8cf02-159">탄력적 풀이 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cf02-159">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="8cf02-160">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8cf02-160">-ServerName</span></span>
<span data-ttu-id="8cf02-161">탄력적 풀을 호스팅하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cf02-161">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="8cf02-162">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="8cf02-162">-StorageMB</span></span>
<span data-ttu-id="8cf02-163">탄력적 풀의 저장소 용량 한도 (mb)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cf02-163">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="8cf02-164">자세한 내용은 New-AzureRmSqlElasticPool cmdlet을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8cf02-164">For more information, see the New-AzureRmSqlElasticPool cmdlet.</span></span>

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

### <span data-ttu-id="8cf02-165">태그</span><span class="sxs-lookup"><span data-stu-id="8cf02-165">-Tags</span></span>
<span data-ttu-id="8cf02-166">이 cmdlet이 해시 테이블 형식으로 탄력적 풀에 연결 하는 키-값 쌍의 사전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cf02-166">Specifies a dictionary of Key-value pairs that this cmdlet associates with the elastic pool in the form of a hash table.</span></span> <span data-ttu-id="8cf02-167">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="8cf02-167">For example:</span></span>

`@{key0="value0";"key 1"=$null;key2="value2"}`

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

### <span data-ttu-id="8cf02-168">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="8cf02-168">-ZoneRedundant</span></span>
<span data-ttu-id="8cf02-169">Azure Sql 탄력적 풀에 연결 되는 영역 중복성</span><span class="sxs-lookup"><span data-stu-id="8cf02-169">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="8cf02-170">-확인</span><span class="sxs-lookup"><span data-stu-id="8cf02-170">-Confirm</span></span>
<span data-ttu-id="8cf02-171">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cf02-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cf02-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cf02-172">-WhatIf</span></span>
<span data-ttu-id="8cf02-173">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8cf02-173">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cf02-174">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8cf02-174">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cf02-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cf02-175">CommonParameters</span></span>
<span data-ttu-id="8cf02-176">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cf02-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cf02-177">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cf02-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cf02-178">입력</span><span class="sxs-lookup"><span data-stu-id="8cf02-178">INPUTS</span></span>

### <span data-ttu-id="8cf02-179">않아야</span><span class="sxs-lookup"><span data-stu-id="8cf02-179">None</span></span>
<span data-ttu-id="8cf02-180">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8cf02-180">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8cf02-181">출력</span><span class="sxs-lookup"><span data-stu-id="8cf02-181">OUTPUTS</span></span>

### <span data-ttu-id="8cf02-182">ElasticPool. AzureSqlElasticPoolModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="8cf02-182">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="8cf02-183">상속자</span><span class="sxs-lookup"><span data-stu-id="8cf02-183">NOTES</span></span>

## <span data-ttu-id="8cf02-184">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8cf02-184">RELATED LINKS</span></span>

[<span data-ttu-id="8cf02-185">Get-AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="8cf02-185">Get-AzureRmSqlElasticPool</span></span>](./Get-AzureRmSqlElasticPool.md)

[<span data-ttu-id="8cf02-186">Get-AzureRmSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="8cf02-186">Get-AzureRmSqlElasticPoolActivity</span></span>](./Get-AzureRmSqlElasticPoolActivity.md)

[<span data-ttu-id="8cf02-187">Get-AzureRmSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="8cf02-187">Get-AzureRmSqlElasticPoolDatabase</span></span>](./Get-AzureRmSqlElasticPoolDatabase.md)

[<span data-ttu-id="8cf02-188">새로운 AzureRmSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="8cf02-188">New-AzureRmSqlElasticPool</span></span>](./New-AzureRmSqlElasticPool.md)

[<span data-ttu-id="8cf02-189">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="8cf02-189">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
