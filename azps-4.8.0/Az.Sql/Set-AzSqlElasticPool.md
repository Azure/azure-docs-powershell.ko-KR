---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
ms.openlocfilehash: cb76e0ff789f89079772d7f718c3f16c9c01d707
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213876"
---
# <span data-ttu-id="392c9-101">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="392c9-101">Set-AzSqlElasticPool</span></span>

## <span data-ttu-id="392c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="392c9-102">SYNOPSIS</span></span>
<span data-ttu-id="392c9-103">Azure SQL 데이터베이스에서 탄력적 데이터베이스 풀의 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="392c9-103">Modifies properties of an elastic database pool in Azure SQL Database.</span></span>

## <span data-ttu-id="392c9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="392c9-104">SYNTAX</span></span>

### <span data-ttu-id="392c9-105">DtuBasedPool (기본값)</span><span class="sxs-lookup"><span data-stu-id="392c9-105">DtuBasedPool (Default)</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="392c9-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="392c9-106">VcoreBasedPool</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-StorageMB <Int32>] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="392c9-107">설명은</span><span class="sxs-lookup"><span data-stu-id="392c9-107">DESCRIPTION</span></span>
<span data-ttu-id="392c9-108">**AzSqlElasticPool** Cmdlet은 Azure SQL Database의 탄력적 풀에 대 한 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="392c9-108">The **Set-AzSqlElasticPool** cmdlet sets properties for an elastic pool in Azure SQL Database.</span></span> <span data-ttu-id="392c9-109">이 cmdlet은 *Dtu* (eDTUs), 풀 당 저장소 최대 크기 ( *storagemb* ), 데이터베이스당 최대 eDTUs ( *DatabaseDtuMax* ), 데이터베이스당 최소 eDTUs ( *databasedtumin* )를 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="392c9-109">This cmdlet can modify the eDTUs per pool ( *Dtu* ), storage max size per pool ( *StorageMB* ), maximum eDTUs per database ( *DatabaseDtuMax* ), and minimum eDTUs per database ( *DatabaseDtuMin* ).</span></span>
<span data-ttu-id="392c9-110">여러 매개 변수 ( *-Dtu,-DatabaseDtuMin 및-DatabaseDtuMax* )에는 해당 매개 변수에 대 한 유효한 값 목록에서 값을 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="392c9-110">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="392c9-111">예를 들어 표준 100 eDTU 풀에 대 한-DatabaseDtuMax은 10, 20, 50 또는 100 으로만 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="392c9-111">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="392c9-112">유효한 값에 대 한 자세한 내용은 [탄력적 풀](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)의 특정 크기 풀에 대 한 표를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="392c9-112">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="392c9-113">예제의</span><span class="sxs-lookup"><span data-stu-id="392c9-113">EXAMPLES</span></span>

### <span data-ttu-id="392c9-114">예제 1: 탄력적 풀의 속성 수정</span><span class="sxs-lookup"><span data-stu-id="392c9-114">Example 1: Modify properties for an elastic pool</span></span>
```powershell
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

<span data-ttu-id="392c9-115">이 명령은 elasticpool01 이라는 탄력적 풀의 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="392c9-115">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="392c9-116">명령은 탄력적 풀에 대 한 Dtu 수를 1000로 설정 하 고 최소 및 최대 Dtu를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="392c9-116">The command sets the number of DTUs for the elastic pool to 1000 and sets the minimum and maximum DTUs.</span></span>

### <span data-ttu-id="392c9-117">예제 2: 탄력적 풀의 저장소 최대 크기 수정</span><span class="sxs-lookup"><span data-stu-id="392c9-117">Example 2: Modify the storage max size of an elastic pool</span></span>
```powershell
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

<span data-ttu-id="392c9-118">이 명령은 elasticpool01 이라는 탄력적 풀의 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="392c9-118">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="392c9-119">명령은 탄력적 풀의 최대 저장소를 2TB로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="392c9-119">The command sets the max storage for an elastic pool to 2 TB.</span></span>

### <span data-ttu-id="392c9-120">예제 3</span><span class="sxs-lookup"><span data-stu-id="392c9-120">Example 3</span></span>

<span data-ttu-id="392c9-121">Azure SQL 데이터베이스에서 탄력적 데이터베이스 풀의 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="392c9-121">Modifies properties of an elastic database pool in Azure SQL Database.</span></span> <span data-ttu-id="392c9-122">생성</span><span class="sxs-lookup"><span data-stu-id="392c9-122">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticPool -Dtu 1000 -Edition 'GeneralPurpose' -ElasticPoolName 'ElasticPool01' -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01'
```

## <span data-ttu-id="392c9-123">변수</span><span class="sxs-lookup"><span data-stu-id="392c9-123">PARAMETERS</span></span>

### <span data-ttu-id="392c9-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="392c9-124">-AsJob</span></span>
<span data-ttu-id="392c9-125">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="392c9-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="392c9-126">-가 며 Egeneration</span><span class="sxs-lookup"><span data-stu-id="392c9-126">-ComputeGeneration</span></span>
<span data-ttu-id="392c9-127">할당할 계산 생성입니다.</span><span class="sxs-lookup"><span data-stu-id="392c9-127">The compute generation to assign.</span></span>

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

### <span data-ttu-id="392c9-128">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="392c9-128">-DatabaseDtuMax</span></span>
<span data-ttu-id="392c9-129">풀의 단일 데이터베이스가 소비할 수 있는 최대 Dtu 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="392c9-129">Specifies the maximum number of DTUs that any single database in the pool can consume.</span></span>
<span data-ttu-id="392c9-130">유효한 값에 대 한 자세한 내용은 [탄력적 풀](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)의 특정 크기 풀에 대 한 표를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="392c9-130">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="392c9-131">여러 버전의 기본값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="392c9-131">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="392c9-132">기본적.</span><span class="sxs-lookup"><span data-stu-id="392c9-132">Basic.</span></span>  <span data-ttu-id="392c9-133">5 Dtu</span><span class="sxs-lookup"><span data-stu-id="392c9-133">5 DTUs</span></span>
- <span data-ttu-id="392c9-134">표준이.</span><span class="sxs-lookup"><span data-stu-id="392c9-134">Standard.</span></span> <span data-ttu-id="392c9-135">100 Dtu</span><span class="sxs-lookup"><span data-stu-id="392c9-135">100 DTUs</span></span>
- <span data-ttu-id="392c9-136">Premium.</span><span class="sxs-lookup"><span data-stu-id="392c9-136">Premium.</span></span> <span data-ttu-id="392c9-137">125 Dtu</span><span class="sxs-lookup"><span data-stu-id="392c9-137">125 DTUs</span></span>

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

### <span data-ttu-id="392c9-138">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="392c9-138">-DatabaseDtuMin</span></span>
<span data-ttu-id="392c9-139">탄력적 풀이 풀의 모든 데이터베이스에 대해 보장 하는 최소 Dtu 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="392c9-139">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="392c9-140">유효한 값에 대 한 자세한 내용은 [탄력적 풀](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)의 특정 크기 풀에 대 한 표를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="392c9-140">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="392c9-141">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="392c9-141">The default value is zero (0).</span></span>

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

### <span data-ttu-id="392c9-142">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="392c9-142">-DatabaseVCoreMax</span></span>
<span data-ttu-id="392c9-143">풀에서 사용할 수 있는 모든 SqlAzure 데이터베이스의 최대 VCore 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="392c9-143">The maximum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="392c9-144">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="392c9-144">-DatabaseVCoreMin</span></span>
<span data-ttu-id="392c9-145">풀에서 사용할 수 있는 모든 SqlAzure 데이터베이스의 최소 VCore 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="392c9-145">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="392c9-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="392c9-146">-DefaultProfile</span></span>
<span data-ttu-id="392c9-147">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="392c9-147">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="392c9-148">-Dtu</span><span class="sxs-lookup"><span data-stu-id="392c9-148">-Dtu</span></span>
<span data-ttu-id="392c9-149">탄력적 풀에 대 한 총 공유 Dtu 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="392c9-149">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="392c9-150">유효한 값에 대 한 자세한 내용은 [탄력적 풀](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)의 특정 크기 풀에 대 한 표를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="392c9-150">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="392c9-151">여러 버전의 기본값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="392c9-151">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="392c9-152">기본적.</span><span class="sxs-lookup"><span data-stu-id="392c9-152">Basic.</span></span> <span data-ttu-id="392c9-153">100 Dtu</span><span class="sxs-lookup"><span data-stu-id="392c9-153">100 DTUs</span></span>
- <span data-ttu-id="392c9-154">표준이.</span><span class="sxs-lookup"><span data-stu-id="392c9-154">Standard.</span></span> <span data-ttu-id="392c9-155">100 Dtu</span><span class="sxs-lookup"><span data-stu-id="392c9-155">100 DTUs</span></span>
- <span data-ttu-id="392c9-156">Premium.</span><span class="sxs-lookup"><span data-stu-id="392c9-156">Premium.</span></span> <span data-ttu-id="392c9-157">125 Dtu</span><span class="sxs-lookup"><span data-stu-id="392c9-157">125 DTUs</span></span>

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

### <span data-ttu-id="392c9-158">-에디션</span><span class="sxs-lookup"><span data-stu-id="392c9-158">-Edition</span></span>
<span data-ttu-id="392c9-159">탄력적 풀에 대 한 Azure SQL 데이터베이스의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="392c9-159">Specifies the edition of the Azure SQL Database for the elastic pool.</span></span> <span data-ttu-id="392c9-160">에디션을 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="392c9-160">You cannot change the edition.</span></span> <span data-ttu-id="392c9-161">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="392c9-161">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="392c9-162">않아야</span><span class="sxs-lookup"><span data-stu-id="392c9-162">None</span></span>
- <span data-ttu-id="392c9-163">기본적</span><span class="sxs-lookup"><span data-stu-id="392c9-163">Basic</span></span>
- <span data-ttu-id="392c9-164">표준이</span><span class="sxs-lookup"><span data-stu-id="392c9-164">Standard</span></span>
- <span data-ttu-id="392c9-165">Premium</span><span class="sxs-lookup"><span data-stu-id="392c9-165">Premium</span></span>
- <span data-ttu-id="392c9-166">웨어하우스</span><span class="sxs-lookup"><span data-stu-id="392c9-166">DataWarehouse</span></span>
- <span data-ttu-id="392c9-167">비우거나</span><span class="sxs-lookup"><span data-stu-id="392c9-167">Free</span></span>
- <span data-ttu-id="392c9-168">늘이고</span><span class="sxs-lookup"><span data-stu-id="392c9-168">Stretch</span></span>
- <span data-ttu-id="392c9-169">일반 목적</span><span class="sxs-lookup"><span data-stu-id="392c9-169">GeneralPurpose</span></span>
- <span data-ttu-id="392c9-170">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="392c9-170">BusinessCritical</span></span>

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

### <span data-ttu-id="392c9-171">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="392c9-171">-ElasticPoolName</span></span>
<span data-ttu-id="392c9-172">탄력적 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="392c9-172">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="392c9-173">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="392c9-173">-LicenseType</span></span>
<span data-ttu-id="392c9-174">Azure Sql 데이터베이스에 대 한 라이선스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="392c9-174">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="392c9-175">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="392c9-175">-ResourceGroupName</span></span>
<span data-ttu-id="392c9-176">탄력적 풀이 할당 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="392c9-176">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="392c9-177">-ServerName</span><span class="sxs-lookup"><span data-stu-id="392c9-177">-ServerName</span></span>
<span data-ttu-id="392c9-178">탄력적 풀을 호스팅하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="392c9-178">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="392c9-179">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="392c9-179">-StorageMB</span></span>
<span data-ttu-id="392c9-180">탄력적 풀의 저장소 용량 한도 (mb)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="392c9-180">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="392c9-181">자세한 내용은 New-AzSqlElasticPool cmdlet을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="392c9-181">For more information, see the New-AzSqlElasticPool cmdlet.</span></span>

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

### <span data-ttu-id="392c9-182">태그</span><span class="sxs-lookup"><span data-stu-id="392c9-182">-Tags</span></span>
<span data-ttu-id="392c9-183">이 cmdlet이 해시 테이블 형식으로 탄력적 풀에 연결 하는 키-값 쌍의 사전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="392c9-183">Specifies a dictionary of Key-value pairs that this cmdlet associates with the elastic pool in the form of a hash table.</span></span> <span data-ttu-id="392c9-184">예를 들어: `@{key0="value0";"key 1"=$null;key2="value2"}`</span><span class="sxs-lookup"><span data-stu-id="392c9-184">For example: `@{key0="value0";"key 1"=$null;key2="value2"}`</span></span>

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

### <span data-ttu-id="392c9-185">-VCore</span><span class="sxs-lookup"><span data-stu-id="392c9-185">-VCore</span></span>
<span data-ttu-id="392c9-186">Sql Azure 탄력적 풀의 총 공유 수입니다.</span><span class="sxs-lookup"><span data-stu-id="392c9-186">The total shared number of Vcore for the Sql Azure Elastic Pool.</span></span>

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

### <span data-ttu-id="392c9-187">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="392c9-187">-ZoneRedundant</span></span>
<span data-ttu-id="392c9-188">Azure Sql 탄력적 풀에 연결 되는 영역 중복성</span><span class="sxs-lookup"><span data-stu-id="392c9-188">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="392c9-189">-확인</span><span class="sxs-lookup"><span data-stu-id="392c9-189">-Confirm</span></span>
<span data-ttu-id="392c9-190">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="392c9-190">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="392c9-191">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="392c9-191">-WhatIf</span></span>
<span data-ttu-id="392c9-192">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="392c9-192">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="392c9-193">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="392c9-193">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="392c9-194">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="392c9-194">CommonParameters</span></span>
<span data-ttu-id="392c9-195">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="392c9-195">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="392c9-196">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="392c9-196">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="392c9-197">입력</span><span class="sxs-lookup"><span data-stu-id="392c9-197">INPUTS</span></span>

### <span data-ttu-id="392c9-198">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="392c9-198">System.String</span></span>

## <span data-ttu-id="392c9-199">출력</span><span class="sxs-lookup"><span data-stu-id="392c9-199">OUTPUTS</span></span>

### <span data-ttu-id="392c9-200">ElasticPool. AzureSqlElasticPoolModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="392c9-200">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="392c9-201">상속자</span><span class="sxs-lookup"><span data-stu-id="392c9-201">NOTES</span></span>

## <span data-ttu-id="392c9-202">관련 링크</span><span class="sxs-lookup"><span data-stu-id="392c9-202">RELATED LINKS</span></span>

[<span data-ttu-id="392c9-203">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="392c9-203">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="392c9-204">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="392c9-204">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="392c9-205">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="392c9-205">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="392c9-206">새로운 AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="392c9-206">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="392c9-207">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="392c9-207">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
