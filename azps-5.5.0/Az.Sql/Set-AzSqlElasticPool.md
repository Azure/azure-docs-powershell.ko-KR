---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 555D58AB-1361-4BB1-ACD0-905C3C6F4F7E
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlElasticPool.md
ms.openlocfilehash: a420a7edf1d5fb7133087c5ecb9fcf605cbdddf9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176756"
---
# <span data-ttu-id="0b3ff-101">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="0b3ff-101">Set-AzSqlElasticPool</span></span>

## <span data-ttu-id="0b3ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b3ff-102">SYNOPSIS</span></span>
<span data-ttu-id="0b3ff-103">Azure SQL Database에서 탄력적 데이터베이스 풀의 속성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="0b3ff-103">Modifies properties of an elastic database pool in Azure SQL Database.</span></span>

## <span data-ttu-id="0b3ff-104">구문</span><span class="sxs-lookup"><span data-stu-id="0b3ff-104">SYNTAX</span></span>

### <span data-ttu-id="0b3ff-105">DtuBasedPool(기본값)</span><span class="sxs-lookup"><span data-stu-id="0b3ff-105">DtuBasedPool (Default)</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-MaintenanceConfigurationId <String>] [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0b3ff-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="0b3ff-106">VcoreBasedPool</span></span>
```
Set-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-StorageMB <Int32>] [-VCore <Int32>]
 [-ComputeGeneration <String>] [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-MaintenanceConfigurationId <String>] [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b3ff-107">설명</span><span class="sxs-lookup"><span data-stu-id="0b3ff-107">DESCRIPTION</span></span>
<span data-ttu-id="0b3ff-108">**Set-AzSqlElasticPool** cmdlet은 Azure SQL Database의 탄력적 풀에 대한 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="0b3ff-108">The **Set-AzSqlElasticPool** cmdlet sets properties for an elastic pool in Azure SQL Database.</span></span> <span data-ttu-id="0b3ff-109">이 cmdlet은 풀당 *eDTU(Dtu),* 풀당 저장소 최대 *크기(StorageMB),* 데이터베이스당 최대 *eDTU(DatabaseDtuMax)* 및 데이터베이스당 최소 eDTU(DatabaseDtuMin)를 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0b3ff-109">This cmdlet can modify the eDTUs per pool (*Dtu*), storage max size per pool (*StorageMB*), maximum eDTUs per database (*DatabaseDtuMax*), and minimum eDTUs per database (*DatabaseDtuMin*).</span></span>
<span data-ttu-id="0b3ff-110">여러 매개 *변수(-Dtu, -DatabaseDtuMin 및 -DatabaseDtuMax)에는* 해당 매개 변수에 대한 유효한 값 목록에서 설정되는 값이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="0b3ff-110">Several parameters (*-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax*) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="0b3ff-111">예를 들어 표준 100 eDTU 풀에 대한 -DatabaseDtuMax는 10, 20, 50 또는 100으로만 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0b3ff-111">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="0b3ff-112">유효한 값에 대한 자세한 내용은 탄력적 풀의 특정 크기 풀에 대한 [테이블을 참조합니다.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="0b3ff-112">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="0b3ff-113">예제</span><span class="sxs-lookup"><span data-stu-id="0b3ff-113">EXAMPLES</span></span>

### <span data-ttu-id="0b3ff-114">예제 1: 탄력적 풀에 대한 속성 수정</span><span class="sxs-lookup"><span data-stu-id="0b3ff-114">Example 1: Modify properties for an elastic pool</span></span>
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

<span data-ttu-id="0b3ff-115">이 명령은 elasticpool01이라는 탄력적 풀에 대한 속성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="0b3ff-115">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="0b3ff-116">이 명령은 탄력적 풀의 D2 수를 1000으로 설정하고 최소 및 최대 D2를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="0b3ff-116">The command sets the number of DTUs for the elastic pool to 1000 and sets the minimum and maximum DTUs.</span></span>

### <span data-ttu-id="0b3ff-117">예제 2: 탄력적 풀의 저장소 최대 크기 수정</span><span class="sxs-lookup"><span data-stu-id="0b3ff-117">Example 2: Modify the storage max size of an elastic pool</span></span>
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

<span data-ttu-id="0b3ff-118">이 명령은 elasticpool01이라는 탄력적 풀에 대한 속성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="0b3ff-118">This command modifies properties for an elastic pool named elasticpool01.</span></span> <span data-ttu-id="0b3ff-119">이 명령은 탄력적 풀의 최대 저장소를 2 TB로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="0b3ff-119">The command sets the max storage for an elastic pool to 2 TB.</span></span>

### <span data-ttu-id="0b3ff-120">예제 3</span><span class="sxs-lookup"><span data-stu-id="0b3ff-120">Example 3</span></span>

<span data-ttu-id="0b3ff-121">Azure SQL Database에서 탄력적 데이터베이스 풀의 속성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="0b3ff-121">Modifies properties of an elastic database pool in Azure SQL Database.</span></span> <span data-ttu-id="0b3ff-122">(자동Generated)</span><span class="sxs-lookup"><span data-stu-id="0b3ff-122">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlElasticPool -Dtu 1000 -Edition 'GeneralPurpose' -ElasticPoolName 'ElasticPool01' -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01'
```

## <span data-ttu-id="0b3ff-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0b3ff-123">PARAMETERS</span></span>

### <span data-ttu-id="0b3ff-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0b3ff-124">-AsJob</span></span>
<span data-ttu-id="0b3ff-125">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="0b3ff-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0b3ff-126">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="0b3ff-126">-ComputeGeneration</span></span>
<span data-ttu-id="0b3ff-127">할당할 계산 생성입니다.</span><span class="sxs-lookup"><span data-stu-id="0b3ff-127">The compute generation to assign.</span></span>

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

### <span data-ttu-id="0b3ff-128">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="0b3ff-128">-DatabaseDtuMax</span></span>
<span data-ttu-id="0b3ff-129">풀의 단일 데이터베이스가 사용할 수 있는 최대 D2 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0b3ff-129">Specifies the maximum number of DTUs that any single database in the pool can consume.</span></span>
<span data-ttu-id="0b3ff-130">유효한 값에 대한 자세한 내용은 탄력적 풀의 특정 크기 풀에 대한 [테이블을 참조합니다.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="0b3ff-130">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="0b3ff-131">다른 버전에 대한 기본값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0b3ff-131">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="0b3ff-132">기본.</span><span class="sxs-lookup"><span data-stu-id="0b3ff-132">Basic.</span></span>  <span data-ttu-id="0b3ff-133">5DUS</span><span class="sxs-lookup"><span data-stu-id="0b3ff-133">5 DTUs</span></span>
- <span data-ttu-id="0b3ff-134">표준.</span><span class="sxs-lookup"><span data-stu-id="0b3ff-134">Standard.</span></span> <span data-ttu-id="0b3ff-135">100 D2</span><span class="sxs-lookup"><span data-stu-id="0b3ff-135">100 DTUs</span></span>
- <span data-ttu-id="0b3ff-136">프리미엄.</span><span class="sxs-lookup"><span data-stu-id="0b3ff-136">Premium.</span></span> <span data-ttu-id="0b3ff-137">125DUS</span><span class="sxs-lookup"><span data-stu-id="0b3ff-137">125 DTUs</span></span>

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

### <span data-ttu-id="0b3ff-138">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="0b3ff-138">-DatabaseDtuMin</span></span>
<span data-ttu-id="0b3ff-139">탄력적 풀이 풀의 모든 데이터베이스에 보장하는 최소 D2 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0b3ff-139">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="0b3ff-140">유효한 값에 대한 자세한 내용은 탄력적 풀의 특정 크기 풀에 대한 [테이블을 참조합니다.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="0b3ff-140">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="0b3ff-141">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="0b3ff-141">The default value is zero (0).</span></span>

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

### <span data-ttu-id="0b3ff-142">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="0b3ff-142">-DatabaseVCoreMax</span></span>
<span data-ttu-id="0b3ff-143">SqlAzure 데이터베이스가 풀에서 사용할 수 있는 최대 VCore 수입니다.</span><span class="sxs-lookup"><span data-stu-id="0b3ff-143">The maximum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="0b3ff-144">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="0b3ff-144">-DatabaseVCoreMin</span></span>
<span data-ttu-id="0b3ff-145">SqlAzure 데이터베이스가 풀에서 사용할 수 있는 최소 VCore 수입니다.</span><span class="sxs-lookup"><span data-stu-id="0b3ff-145">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="0b3ff-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b3ff-146">-DefaultProfile</span></span>
<span data-ttu-id="0b3ff-147">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0b3ff-147">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0b3ff-148">-Dtu</span><span class="sxs-lookup"><span data-stu-id="0b3ff-148">-Dtu</span></span>
<span data-ttu-id="0b3ff-149">탄력적 풀에 대한 공유 D2의 총 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0b3ff-149">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="0b3ff-150">유효한 값에 대한 자세한 내용은 탄력적 풀의 특정 크기 풀에 대한 [테이블을 참조합니다.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="0b3ff-150">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>
<span data-ttu-id="0b3ff-151">다른 버전에 대한 기본값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0b3ff-151">The default values for different editions are as follows:</span></span>
- <span data-ttu-id="0b3ff-152">기본.</span><span class="sxs-lookup"><span data-stu-id="0b3ff-152">Basic.</span></span> <span data-ttu-id="0b3ff-153">100 D2</span><span class="sxs-lookup"><span data-stu-id="0b3ff-153">100 DTUs</span></span>
- <span data-ttu-id="0b3ff-154">표준.</span><span class="sxs-lookup"><span data-stu-id="0b3ff-154">Standard.</span></span> <span data-ttu-id="0b3ff-155">100 D2</span><span class="sxs-lookup"><span data-stu-id="0b3ff-155">100 DTUs</span></span>
- <span data-ttu-id="0b3ff-156">프리미엄.</span><span class="sxs-lookup"><span data-stu-id="0b3ff-156">Premium.</span></span> <span data-ttu-id="0b3ff-157">125DUS</span><span class="sxs-lookup"><span data-stu-id="0b3ff-157">125 DTUs</span></span>

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

### <span data-ttu-id="0b3ff-158">-Edition</span><span class="sxs-lookup"><span data-stu-id="0b3ff-158">-Edition</span></span>
<span data-ttu-id="0b3ff-159">탄력적 풀에 대한 Azure SQL 데이터베이스의 에디션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0b3ff-159">Specifies the edition of the Azure SQL Database for the elastic pool.</span></span> <span data-ttu-id="0b3ff-160">버전은 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0b3ff-160">You cannot change the edition.</span></span> <span data-ttu-id="0b3ff-161">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="0b3ff-161">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0b3ff-162">없음</span><span class="sxs-lookup"><span data-stu-id="0b3ff-162">None</span></span>
- <span data-ttu-id="0b3ff-163">기본</span><span class="sxs-lookup"><span data-stu-id="0b3ff-163">Basic</span></span>
- <span data-ttu-id="0b3ff-164">표준</span><span class="sxs-lookup"><span data-stu-id="0b3ff-164">Standard</span></span>
- <span data-ttu-id="0b3ff-165">프리미엄</span><span class="sxs-lookup"><span data-stu-id="0b3ff-165">Premium</span></span>
- <span data-ttu-id="0b3ff-166">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="0b3ff-166">DataWarehouse</span></span>
- <span data-ttu-id="0b3ff-167">무료</span><span class="sxs-lookup"><span data-stu-id="0b3ff-167">Free</span></span>
- <span data-ttu-id="0b3ff-168">Stretch</span><span class="sxs-lookup"><span data-stu-id="0b3ff-168">Stretch</span></span>
- <span data-ttu-id="0b3ff-169">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="0b3ff-169">GeneralPurpose</span></span>
- <span data-ttu-id="0b3ff-170">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="0b3ff-170">BusinessCritical</span></span>

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

### <span data-ttu-id="0b3ff-171">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="0b3ff-171">-ElasticPoolName</span></span>
<span data-ttu-id="0b3ff-172">탄력적 풀의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0b3ff-172">Specifies the name of the elastic pool.</span></span>

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

### <span data-ttu-id="0b3ff-173">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="0b3ff-173">-LicenseType</span></span>
<span data-ttu-id="0b3ff-174">Azure Sql 데이터베이스에 대한 라이선스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="0b3ff-174">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="0b3ff-175">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="0b3ff-175">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="0b3ff-176">탄력적 풀에 대한 유지 관리 SQL ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0b3ff-176">The Maintenance configuration id for the SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="0b3ff-177">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b3ff-177">-ResourceGroupName</span></span>
<span data-ttu-id="0b3ff-178">탄력적 풀이 할당된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0b3ff-178">Specifies the name of the resource group to which the elastic pool is assigned.</span></span>

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

### <span data-ttu-id="0b3ff-179">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0b3ff-179">-ServerName</span></span>
<span data-ttu-id="0b3ff-180">탄력적 풀을 호스트하는 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0b3ff-180">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="0b3ff-181">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="0b3ff-181">-StorageMB</span></span>
<span data-ttu-id="0b3ff-182">탄력적 풀에 대한 저장소 제한(메가바이트)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0b3ff-182">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="0b3ff-183">자세한 내용은 다음 cmdlet을 New-AzSqlElasticPool 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0b3ff-183">For more information, see the New-AzSqlElasticPool cmdlet.</span></span>

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

### <span data-ttu-id="0b3ff-184">-Tags</span><span class="sxs-lookup"><span data-stu-id="0b3ff-184">-Tags</span></span>
<span data-ttu-id="0b3ff-185">이 cmdlet이 해시 테이블의 형태로 탄력적 풀과 연결되는 키-값 쌍의 사전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0b3ff-185">Specifies a dictionary of Key-value pairs that this cmdlet associates with the elastic pool in the form of a hash table.</span></span> <span data-ttu-id="0b3ff-186">예를 들어: `@{key0="value0";"key 1"=$null;key2="value2"}`</span><span class="sxs-lookup"><span data-stu-id="0b3ff-186">For example: `@{key0="value0";"key 1"=$null;key2="value2"}`</span></span>

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

### <span data-ttu-id="0b3ff-187">-VCore</span><span class="sxs-lookup"><span data-stu-id="0b3ff-187">-VCore</span></span>
<span data-ttu-id="0b3ff-188">Sql Azure 탄력적 풀에 대한 총 공유 Vcore 수입니다.</span><span class="sxs-lookup"><span data-stu-id="0b3ff-188">The total shared number of Vcore for the Sql Azure Elastic Pool.</span></span>

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

### <span data-ttu-id="0b3ff-189">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="0b3ff-189">-ZoneRedundant</span></span>
<span data-ttu-id="0b3ff-190">Azure Sql 탄력적 풀과 연결하기 위해 영역 중복</span><span class="sxs-lookup"><span data-stu-id="0b3ff-190">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="0b3ff-191">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0b3ff-191">-Confirm</span></span>
<span data-ttu-id="0b3ff-192">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0b3ff-192">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b3ff-193">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b3ff-193">-WhatIf</span></span>
<span data-ttu-id="0b3ff-194">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="0b3ff-194">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b3ff-195">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0b3ff-195">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b3ff-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b3ff-196">CommonParameters</span></span>
<span data-ttu-id="0b3ff-197">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0b3ff-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b3ff-198">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0b3ff-198">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b3ff-199">입력</span><span class="sxs-lookup"><span data-stu-id="0b3ff-199">INPUTS</span></span>

### <span data-ttu-id="0b3ff-200">System.String</span><span class="sxs-lookup"><span data-stu-id="0b3ff-200">System.String</span></span>

## <span data-ttu-id="0b3ff-201">출력</span><span class="sxs-lookup"><span data-stu-id="0b3ff-201">OUTPUTS</span></span>

### <span data-ttu-id="0b3ff-202">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="0b3ff-202">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="0b3ff-203">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0b3ff-203">NOTES</span></span>

## <span data-ttu-id="0b3ff-204">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0b3ff-204">RELATED LINKS</span></span>

[<span data-ttu-id="0b3ff-205">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="0b3ff-205">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="0b3ff-206">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="0b3ff-206">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="0b3ff-207">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="0b3ff-207">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="0b3ff-208">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="0b3ff-208">New-AzSqlElasticPool</span></span>](./New-AzSqlElasticPool.md)

[<span data-ttu-id="0b3ff-209">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="0b3ff-209">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
