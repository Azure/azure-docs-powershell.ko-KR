---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
ms.openlocfilehash: d78ca6ef2e342982dc6f5e53e8fff4de606dd5ab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873747"
---
# <span data-ttu-id="fec29-101">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="fec29-101">Set-AzSqlElasticPool</span></span>

## <span data-ttu-id="fec29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fec29-102">SYNOPSIS</span></span>
<span data-ttu-id="fec29-103">Azure SQL 데이터베이스에서 탄력적 데이터베이스 풀의 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fec29-103">Modifies properties of an elastic database pool in Azure SQL Database.</span></span>

## <span data-ttu-id="fec29-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fec29-104">SYNTAX</span></span>

### <span data-ttu-id="fec29-105">DtuBasedPool (기본값)</span><span class="sxs-lookup"><span data-stu-id="fec29-105">DtuBasedPool (Default)</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fec29-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="fec29-106">VcoreBasedPool</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-StorageMB <Int32>] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fec29-107">설명은</span><span class="sxs-lookup"><span data-stu-id="fec29-107">DESCRIPTION</span></span>
<span data-ttu-id="fec29-108">**AzSqlElasticPool** Cmdlet은 Azure SQL Database의 탄력적 풀에 대 한 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fec29-108">The **Set-AzSqlElasticPool** cmdlet sets properties for an elastic pool in Azure SQL Database.</span></span> <span data-ttu-id="fec29-109">이 cmdlet은 *Dtu* (eDTUs), 풀 당 저장소 최대 크기 ( *storagemb* ), 데이터베이스당 최대 eDTUs ( *DatabaseDtuMax* ), 데이터베이스당 최소 eDTUs ( *databasedtumin* )를 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fec29-109">This cmdlet can modify the eDTUs per pool ( *Dtu* ), storage max size per pool ( *StorageMB* ), maximum eDTUs per database ( *DatabaseDtuMax* ), and minimum eDTUs per database ( *DatabaseDtuMin* ).</span></span>
<span data-ttu-id="fec29-110">여러 매개 변수 ( *-Dtu,-DatabaseDtuMin 및-DatabaseDtuMax* )에는 해당 매개 변수에 대 한 유효한 값 목록에서 값을 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fec29-110">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="fec29-111">예를 들어 표준 100 eDTU 풀에 대 한-DatabaseDtuMax은 10, 20, 50 또는 100 으로만 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fec29-111">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="fec29-112">유효한 값에 대 한 자세한 내용은 [탄력적 풀](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)의 특정 크기 풀에 대 한 표를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fec29-112">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="fec29-113">예제의</span><span class="sxs-lookup"><span data-stu-id="fec29-113">EXAMPLES</span></span>

### <span data-ttu-id="fec29-114">예제 1: 탄력적 풀의 속성 수정</span><span class="sxs-lookup"><span data-stu-id="fec29-114">Example 1: Modify properties for an elastic pool</span></span>
```
PS C:\>Set-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Dtu 1000 -DatabaseDtuMax 100 -DatabaseDtuMin 20
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

<span data-ttu-id="fec29-115">이 명령은 elasticpool01 이라는 탄력적 풀의 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fec29-115">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="fec29-116">명령은 탄력적 풀에 대 한 Dtu 수를 1000로 설정 하 고 최소 및 최대 Dtu를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fec29-116">The command sets the number of DTUs for the elastic pool to 1000 and sets the minimum and maximum DTUs.</span></span>

### <span data-ttu-id="fec29-117">예제 2: 탄력적 풀의 저장소 최대 크기 수정</span><span class="sxs-lookup"><span data-stu-id="fec29-117">Example 2: Modify the storage max size of an elastic pool</span></span>
```
PS C:\>Set-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -StorageMB 2097152
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

<span data-ttu-id="fec29-118">이 명령은 elasticpool01 이라는 탄력적 풀의 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fec29-118">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="fec29-119">명령은 탄력적 풀의 최대 저장소를 2TB로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fec29-119">The command sets the max storage for an elastic pool to 2 TB.</span></span>

## <span data-ttu-id="fec29-120">변수</span><span class="sxs-lookup"><span data-stu-id="fec29-120">PARAMETERS</span></span>

### <span data-ttu-id="fec29-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fec29-121">-AsJob</span></span>
<span data-ttu-id="fec29-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="fec29-122">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fec29-123">-가 며 Egeneration</span><span class="sxs-lookup"><span data-stu-id="fec29-123">-ComputeGeneration</span></span>
<span data-ttu-id="fec29-124">할당할 계산 생성입니다.</span><span class="sxs-lookup"><span data-stu-id="fec29-124">The compute generation to assign.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedPool
Aliases: Family

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fec29-125">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="fec29-125">-DatabaseDtuMax</span></span>
<span data-ttu-id="fec29-126">풀의 단일 데이터베이스가 소비할 수 있는 최대 Dtu 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fec29-126">Specifies the maximum number of DTUs that any single database in the pool can consume.</span></span>
<span data-ttu-id="fec29-127">유효한 값에 대 한 자세한 내용은 [탄력적 풀](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)의 특정 크기 풀에 대 한 표를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fec29-127">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="fec29-128">여러 버전의 기본값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="fec29-128">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="fec29-129">기본적.</span><span class="sxs-lookup"><span data-stu-id="fec29-129">Basic.</span></span>  <span data-ttu-id="fec29-130">5 Dtu</span><span class="sxs-lookup"><span data-stu-id="fec29-130">5 DTUs</span></span>
- <span data-ttu-id="fec29-131">표준이.</span><span class="sxs-lookup"><span data-stu-id="fec29-131">Standard.</span></span> <span data-ttu-id="fec29-132">100 Dtu</span><span class="sxs-lookup"><span data-stu-id="fec29-132">100 DTUs</span></span>
- <span data-ttu-id="fec29-133">Premium.</span><span class="sxs-lookup"><span data-stu-id="fec29-133">Premium.</span></span> <span data-ttu-id="fec29-134">125 Dtu</span><span class="sxs-lookup"><span data-stu-id="fec29-134">125 DTUs</span></span>

```yaml
Type: System.Int32
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fec29-135">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="fec29-135">-DatabaseDtuMin</span></span>
<span data-ttu-id="fec29-136">탄력적 풀이 풀의 모든 데이터베이스에 대해 보장 하는 최소 Dtu 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fec29-136">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="fec29-137">유효한 값에 대 한 자세한 내용은 [탄력적 풀](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)의 특정 크기 풀에 대 한 표를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fec29-137">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="fec29-138">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="fec29-138">The default value is zero (0).</span></span>

```yaml
Type: System.Int32
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fec29-139">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="fec29-139">-DatabaseVCoreMax</span></span>
<span data-ttu-id="fec29-140">풀에서 사용할 수 있는 모든 SqlAzure 데이터베이스의 최대 VCore 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="fec29-140">The maximum VCore number any SqlAzure Database can consume in the pool.</span></span>

```yaml
Type: System.Double
Parameter Sets: VcoreBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fec29-141">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="fec29-141">-DatabaseVCoreMin</span></span>
<span data-ttu-id="fec29-142">풀에서 사용할 수 있는 모든 SqlAzure 데이터베이스의 최소 VCore 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="fec29-142">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

```yaml
Type: System.Double
Parameter Sets: VcoreBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fec29-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fec29-143">-DefaultProfile</span></span>
<span data-ttu-id="fec29-144">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="fec29-144">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fec29-145">-Dtu</span><span class="sxs-lookup"><span data-stu-id="fec29-145">-Dtu</span></span>
<span data-ttu-id="fec29-146">탄력적 풀에 대 한 총 공유 Dtu 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fec29-146">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="fec29-147">유효한 값에 대 한 자세한 내용은 [탄력적 풀](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)의 특정 크기 풀에 대 한 표를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fec29-147">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="fec29-148">여러 버전의 기본값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="fec29-148">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="fec29-149">기본적.</span><span class="sxs-lookup"><span data-stu-id="fec29-149">Basic.</span></span> <span data-ttu-id="fec29-150">100 Dtu</span><span class="sxs-lookup"><span data-stu-id="fec29-150">100 DTUs</span></span>
- <span data-ttu-id="fec29-151">표준이.</span><span class="sxs-lookup"><span data-stu-id="fec29-151">Standard.</span></span> <span data-ttu-id="fec29-152">100 Dtu</span><span class="sxs-lookup"><span data-stu-id="fec29-152">100 DTUs</span></span>
- <span data-ttu-id="fec29-153">Premium.</span><span class="sxs-lookup"><span data-stu-id="fec29-153">Premium.</span></span> <span data-ttu-id="fec29-154">125 Dtu</span><span class="sxs-lookup"><span data-stu-id="fec29-154">125 DTUs</span></span>

```yaml
Type: System.Int32
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fec29-155">-에디션</span><span class="sxs-lookup"><span data-stu-id="fec29-155">-Edition</span></span>
<span data-ttu-id="fec29-156">탄력적 풀에 대 한 Azure SQL 데이터베이스의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fec29-156">Specifies the edition of the Azure SQL Database for the elastic pool.</span></span> <span data-ttu-id="fec29-157">에디션을 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="fec29-157">You cannot change the edition.</span></span> <span data-ttu-id="fec29-158">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="fec29-158">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="fec29-159">않아야</span><span class="sxs-lookup"><span data-stu-id="fec29-159">None</span></span>
- <span data-ttu-id="fec29-160">기본적</span><span class="sxs-lookup"><span data-stu-id="fec29-160">Basic</span></span>
- <span data-ttu-id="fec29-161">표준이</span><span class="sxs-lookup"><span data-stu-id="fec29-161">Standard</span></span>
- <span data-ttu-id="fec29-162">Premium</span><span class="sxs-lookup"><span data-stu-id="fec29-162">Premium</span></span>
- <span data-ttu-id="fec29-163">웨어하우스</span><span class="sxs-lookup"><span data-stu-id="fec29-163">DataWarehouse</span></span>
- <span data-ttu-id="fec29-164">비우거나</span><span class="sxs-lookup"><span data-stu-id="fec29-164">Free</span></span>
- <span data-ttu-id="fec29-165">늘이고</span><span class="sxs-lookup"><span data-stu-id="fec29-165">Stretch</span></span>
- <span data-ttu-id="fec29-166">일반 목적</span><span class="sxs-lookup"><span data-stu-id="fec29-166">GeneralPurpose</span></span>
- <span data-ttu-id="fec29-167">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="fec29-167">BusinessCritical</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fec29-168">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="fec29-168">-ElasticPoolName</span></span>
<span data-ttu-id="fec29-169">탄력적 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fec29-169">Specifies the name of the elastic pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fec29-170">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="fec29-170">-LicenseType</span></span>
<span data-ttu-id="fec29-171">Azure Sql 데이터베이스에 대 한 라이선스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="fec29-171">The license type for the Azure Sql database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fec29-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fec29-172">-ResourceGroupName</span></span>
<span data-ttu-id="fec29-173">탄력적 풀이 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fec29-173">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="fec29-174">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fec29-174">-ServerName</span></span>
<span data-ttu-id="fec29-175">탄력적 풀을 호스팅하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fec29-175">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="fec29-176">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="fec29-176">-StorageMB</span></span>
<span data-ttu-id="fec29-177">탄력적 풀의 저장소 용량 한도 (mb)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fec29-177">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="fec29-178">자세한 내용은 New-AzSqlElasticPool cmdlet을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fec29-178">For more information, see the New-AzSqlElasticPool cmdlet.</span></span>

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

### <span data-ttu-id="fec29-179">태그</span><span class="sxs-lookup"><span data-stu-id="fec29-179">-Tags</span></span>
<span data-ttu-id="fec29-180">이 cmdlet이 해시 테이블 형식으로 탄력적 풀에 연결 하는 키-값 쌍의 사전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fec29-180">Specifies a dictionary of Key-value pairs that this cmdlet associates with the elastic pool in the form of a hash table.</span></span> <span data-ttu-id="fec29-181">예를 들어: `@{key0="value0";"key 1"=$null;key2="value2"}`</span><span class="sxs-lookup"><span data-stu-id="fec29-181">For example: `@{key0="value0";"key 1"=$null;key2="value2"}`</span></span>

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

### <span data-ttu-id="fec29-182">-VCore</span><span class="sxs-lookup"><span data-stu-id="fec29-182">-VCore</span></span>
<span data-ttu-id="fec29-183">Sql Azure 탄력적 풀의 총 공유 수입니다.</span><span class="sxs-lookup"><span data-stu-id="fec29-183">The total shared number of Vcore for the Sql Azure Elastic Pool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fec29-184">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="fec29-184">-ZoneRedundant</span></span>
<span data-ttu-id="fec29-185">Azure Sql 탄력적 풀에 연결 되는 영역 중복성</span><span class="sxs-lookup"><span data-stu-id="fec29-185">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fec29-186">-확인</span><span class="sxs-lookup"><span data-stu-id="fec29-186">-Confirm</span></span>
<span data-ttu-id="fec29-187">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fec29-187">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fec29-188">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fec29-188">-WhatIf</span></span>
<span data-ttu-id="fec29-189">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fec29-189">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fec29-190">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fec29-190">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fec29-191">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fec29-191">CommonParameters</span></span>
<span data-ttu-id="fec29-192">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fec29-192">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fec29-193">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fec29-193">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fec29-194">입력</span><span class="sxs-lookup"><span data-stu-id="fec29-194">INPUTS</span></span>

### <span data-ttu-id="fec29-195">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fec29-195">System.String</span></span>

## <span data-ttu-id="fec29-196">출력</span><span class="sxs-lookup"><span data-stu-id="fec29-196">OUTPUTS</span></span>

### <span data-ttu-id="fec29-197">ElasticPool. AzureSqlElasticPoolModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="fec29-197">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="fec29-198">상속자</span><span class="sxs-lookup"><span data-stu-id="fec29-198">NOTES</span></span>

## <span data-ttu-id="fec29-199">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fec29-199">RELATED LINKS</span></span>

[<span data-ttu-id="fec29-200">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="fec29-200">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="fec29-201">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="fec29-201">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="fec29-202">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="fec29-202">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="fec29-203">새로운 AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="fec29-203">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="fec29-204">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="fec29-204">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
