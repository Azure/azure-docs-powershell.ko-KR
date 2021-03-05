---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
ms.openlocfilehash: d625e28b0007a9dc99434f0257a910ea804e3644
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970208"
---
# <span data-ttu-id="d2600-101">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="d2600-101">New-AzSqlElasticPool</span></span>

## <span data-ttu-id="d2600-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2600-102">SYNOPSIS</span></span>
<span data-ttu-id="d2600-103">데이터베이스의 탄력적 데이터베이스 풀을 SQL 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d2600-103">Creates an elastic database pool for a SQL Database.</span></span>

## <span data-ttu-id="d2600-104">구문</span><span class="sxs-lookup"><span data-stu-id="d2600-104">SYNTAX</span></span>

### <span data-ttu-id="d2600-105">DtuBasedPool(기본값)</span><span class="sxs-lookup"><span data-stu-id="d2600-105">DtuBasedPool (Default)</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-MaintenanceConfigurationId <String>] [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d2600-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="d2600-106">VcoreBasedPool</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> -Edition <String> [-StorageMB <Int32>] -VCore <Int32>
 -ComputeGeneration <String> [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-MaintenanceConfigurationId <String>] [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2600-107">설명</span><span class="sxs-lookup"><span data-stu-id="d2600-107">DESCRIPTION</span></span>
<span data-ttu-id="d2600-108">**New-AzSqlElasticPool** cmdlet은 Azure SQL 데이터베이스 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d2600-108">The **New-AzSqlElasticPool** cmdlet creates an elastic database pool for an Azure SQL Database.</span></span>
<span data-ttu-id="d2600-109">여러 매개 *변수(-Dtu, -DatabaseDtuMin 및 -DatabaseDtuMax)에는* 설정되는 값이 해당 매개 변수에 대한 유효한 값 목록에서 설정되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2600-109">Several parameters (*-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax*) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="d2600-110">예를 들어 표준 100 eDTU 풀의 -DatabaseDtuMax는 10, 20, 50 또는 100으로만 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d2600-110">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="d2600-111">유효한 값에 대한 자세한 내용은 탄력적 풀의 특정 크기 풀에 대한 [표를 참조합니다.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="d2600-111">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="d2600-112">예제</span><span class="sxs-lookup"><span data-stu-id="d2600-112">EXAMPLES</span></span>

### <span data-ttu-id="d2600-113">예제 1: DTU 탄력적 풀 만들기</span><span class="sxs-lookup"><span data-stu-id="d2600-113">Example 1: Create a DTU elastic pool</span></span>

```powershell
PS C:\>New-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Edition "Standard" -Dtu 400 -DatabaseDtuMin 10 -DatabaseDtuMax 100
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

<span data-ttu-id="d2600-114">이 명령은 ElasticPool01이라는 표준 서비스 계층에 탄력적 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d2600-114">This command creates an elastic pool in the Standard service tier named ElasticPool01.</span></span> <span data-ttu-id="d2600-115">ResourceGroup01이라는 Azure 리소스 그룹에 할당된 server01이라는 서버는 탄력적 풀을 호스트합니다.</span><span class="sxs-lookup"><span data-stu-id="d2600-115">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="d2600-116">명령은 풀 및 풀의 데이터베이스에 대한 DTU 속성 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d2600-116">The command specifies DTU property values for the pool and the databases in the pool.</span></span>

### <span data-ttu-id="d2600-117">예제 2: vCore 탄력적 풀 만들기</span><span class="sxs-lookup"><span data-stu-id="d2600-117">Example 2: Create a vCore elastic pool</span></span>

```powershell
PS C:\> New-AzSqlElasticPool -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ElasticPoolName "ElasticPool01" -Edition "GeneralPurpose" -vCore 2 -ComputeGeneration Gen5
ResourceId          : /subscriptions/00000000-0000-0000-0000-000000000001/resourceGroups/ResourceGroup01/providers/Microsoft.Sql/servers/server01/elasticPools/ElasticPool01
ResourceGroupName   : ResourceGroup01
ServerName          : Server01
ElasticPoolName     : ElasticPool01
Location            : Central US
CreationDate        : 8/29/2019 2:16:40 AM
State               : Ready
Edition             : GeneralPurpose
SkuName             : GP_Gen5
Dtu                 : 2
DatabaseDtuMax      : 2
DatabaseDtuMin      : 0
Capacity            : 2
DatabaseCapacityMin : 0
DatabaseCapacityMax : 2
Family              : Gen5
MaxSizeBytes        : 34359738368
StorageMB           : 32768
Tags                :
```

<span data-ttu-id="d2600-118">이 명령은 ElasticPool01이라는 GengeralPurpose 서비스 계층에 탄력적 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d2600-118">This command creates an elastic pool in the GengeralPurpose service tier named ElasticPool01.</span></span> <span data-ttu-id="d2600-119">ResourceGroup01이라는 Azure 리소스 그룹에 할당된 server01이라는 서버는 탄력적 풀을 호스트합니다.</span><span class="sxs-lookup"><span data-stu-id="d2600-119">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="d2600-120">명령은 풀 및 풀의 데이터베이스에 대한 vCore 속성 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d2600-120">The command specifies the vCore property values for the pool and the databases in the pool.</span></span>

### <span data-ttu-id="d2600-121">예제 3</span><span class="sxs-lookup"><span data-stu-id="d2600-121">Example 3</span></span>

<span data-ttu-id="d2600-122">데이터베이스의 탄력적 데이터베이스 풀을 SQL 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d2600-122">Creates an elastic database pool for a SQL Database.</span></span> <span data-ttu-id="d2600-123">(자동 재생)</span><span class="sxs-lookup"><span data-stu-id="d2600-123">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlElasticPool -ComputeGeneration Gen5 -Edition 'GeneralPurpose' -ElasticPoolName 'ElasticPool01' -ResourceGroupName 'ResourceGroup01' -ServerName 'Server01' -StorageMB 2097152 -VCore 2
```

## <span data-ttu-id="d2600-124">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d2600-124">PARAMETERS</span></span>

### <span data-ttu-id="d2600-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d2600-125">-AsJob</span></span>
<span data-ttu-id="d2600-126">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d2600-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d2600-127">-ComputeGeneration</span><span class="sxs-lookup"><span data-stu-id="d2600-127">-ComputeGeneration</span></span>
<span data-ttu-id="d2600-128">할당할 계산 생성입니다.</span><span class="sxs-lookup"><span data-stu-id="d2600-128">The compute generation to assign.</span></span>

```yaml
Type: System.String
Parameter Sets: VcoreBasedPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2600-129">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="d2600-129">-DatabaseDtuMax</span></span>
<span data-ttu-id="d2600-130">풀의 단일 데이터베이스가 사용할 수 있는 DTUS(Database Throughput Units)의 최대 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d2600-130">Specifies the maximum number of Database Throughput Units (DTUs) that any single database in the pool can consume.</span></span>
<span data-ttu-id="d2600-131">다른 버전에 대한 기본값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d2600-131">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="d2600-132">기본.</span><span class="sxs-lookup"><span data-stu-id="d2600-132">Basic.</span></span> <span data-ttu-id="d2600-133">5DUS</span><span class="sxs-lookup"><span data-stu-id="d2600-133">5 DTUs</span></span>
- <span data-ttu-id="d2600-134">표준입니다.</span><span class="sxs-lookup"><span data-stu-id="d2600-134">Standard.</span></span> <span data-ttu-id="d2600-135">100 DUS</span><span class="sxs-lookup"><span data-stu-id="d2600-135">100 DTUs</span></span>
- <span data-ttu-id="d2600-136">프리미엄입니다.</span><span class="sxs-lookup"><span data-stu-id="d2600-136">Premium.</span></span> <span data-ttu-id="d2600-137">125 DTUS 유효한 값에 대한 자세한 내용은 탄력적 풀의 특정 크기 풀에 대한 [표를 참조합니다.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="d2600-137">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span></span>

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

### <span data-ttu-id="d2600-138">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="d2600-138">-DatabaseDtuMin</span></span>
<span data-ttu-id="d2600-139">탄력적 풀이 풀의 모든 데이터베이스에 보장하는 최소 DUS 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d2600-139">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="d2600-140">기본값은 0(0)입니다.</span><span class="sxs-lookup"><span data-stu-id="d2600-140">The default value is zero (0).</span></span>
<span data-ttu-id="d2600-141">유효한 값에 대한 자세한 내용은 탄력적 풀의 특정 크기 풀에 대한 [표를 참조합니다.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="d2600-141">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="d2600-142">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="d2600-142">-DatabaseVCoreMax</span></span>
<span data-ttu-id="d2600-143">풀에서 사용할 수 있는 SqlAzure Database의 최대 VCore 수입니다.</span><span class="sxs-lookup"><span data-stu-id="d2600-143">The maximum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="d2600-144">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="d2600-144">-DatabaseVCoreMin</span></span>
<span data-ttu-id="d2600-145">풀에서 사용할 수 있는 SqlAzure 데이터베이스의 최소 VCore 수입니다.</span><span class="sxs-lookup"><span data-stu-id="d2600-145">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="d2600-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2600-146">-DefaultProfile</span></span>
<span data-ttu-id="d2600-147">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d2600-147">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d2600-148">-Dtu</span><span class="sxs-lookup"><span data-stu-id="d2600-148">-Dtu</span></span>
<span data-ttu-id="d2600-149">탄력적 풀에 대한 공유 DUS의 총 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d2600-149">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="d2600-150">다른 버전에 대한 기본값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d2600-150">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="d2600-151">기본.</span><span class="sxs-lookup"><span data-stu-id="d2600-151">Basic.</span></span>
<span data-ttu-id="d2600-152">100 DUS</span><span class="sxs-lookup"><span data-stu-id="d2600-152">100 DTUs</span></span>
- <span data-ttu-id="d2600-153">표준입니다.</span><span class="sxs-lookup"><span data-stu-id="d2600-153">Standard.</span></span>
<span data-ttu-id="d2600-154">100 DUS</span><span class="sxs-lookup"><span data-stu-id="d2600-154">100 DTUs</span></span>
- <span data-ttu-id="d2600-155">프리미엄입니다.</span><span class="sxs-lookup"><span data-stu-id="d2600-155">Premium.</span></span>
<span data-ttu-id="d2600-156">125 DTUS 유효한 값에 대한 자세한 내용은 탄력적 풀의 특정 크기 풀에 대한 [표를 참조합니다.](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span><span class="sxs-lookup"><span data-stu-id="d2600-156">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="d2600-157">-Edition</span><span class="sxs-lookup"><span data-stu-id="d2600-157">-Edition</span></span>
<span data-ttu-id="d2600-158">탄력적 풀에 사용되는 Azure SQL 데이터베이스의 에디션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d2600-158">Specifies the edition of the Azure SQL Database used for the elastic pool.</span></span>
<span data-ttu-id="d2600-159">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="d2600-159">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d2600-160">없음</span><span class="sxs-lookup"><span data-stu-id="d2600-160">None</span></span>
- <span data-ttu-id="d2600-161">기본</span><span class="sxs-lookup"><span data-stu-id="d2600-161">Basic</span></span>
- <span data-ttu-id="d2600-162">표준</span><span class="sxs-lookup"><span data-stu-id="d2600-162">Standard</span></span>
- <span data-ttu-id="d2600-163">프리미엄</span><span class="sxs-lookup"><span data-stu-id="d2600-163">Premium</span></span>
- <span data-ttu-id="d2600-164">DataWarehouse</span><span class="sxs-lookup"><span data-stu-id="d2600-164">DataWarehouse</span></span>
- <span data-ttu-id="d2600-165">무료</span><span class="sxs-lookup"><span data-stu-id="d2600-165">Free</span></span>
- <span data-ttu-id="d2600-166">스트레치</span><span class="sxs-lookup"><span data-stu-id="d2600-166">Stretch</span></span>
- <span data-ttu-id="d2600-167">GeneralPurpose</span><span class="sxs-lookup"><span data-stu-id="d2600-167">GeneralPurpose</span></span>
- <span data-ttu-id="d2600-168">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="d2600-168">BusinessCritical</span></span>

```yaml
Type: System.String
Parameter Sets: DtuBasedPool
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: VcoreBasedPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2600-169">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="d2600-169">-ElasticPoolName</span></span>
<span data-ttu-id="d2600-170">이 cmdlet이 만드는 탄력적 풀의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d2600-170">Specifies the name of the elastic pool that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2600-171">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="d2600-171">-LicenseType</span></span>
<span data-ttu-id="d2600-172">Azure Sql 데이터베이스에 대한 라이선스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="d2600-172">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="d2600-173">-MaintenanceConfigurationId</span><span class="sxs-lookup"><span data-stu-id="d2600-173">-MaintenanceConfigurationId</span></span>
<span data-ttu-id="d2600-174">탄력적 풀에 대한 SQL 구성 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d2600-174">The Maintenance configuration id for the SQL Elastic Pool.</span></span>

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

### <span data-ttu-id="d2600-175">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2600-175">-ResourceGroupName</span></span>
<span data-ttu-id="d2600-176">이 cmdlet에서 탄력적 풀을 할당하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d2600-176">Specifies the name of the resource group to which this cmdlet assigns the elastic pool.</span></span>

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

### <span data-ttu-id="d2600-177">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d2600-177">-ServerName</span></span>
<span data-ttu-id="d2600-178">탄력적 풀을 호스트하는 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d2600-178">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="d2600-179">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="d2600-179">-StorageMB</span></span>
<span data-ttu-id="d2600-180">탄력적 풀에 대한 저장소 제한(메가바이트)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d2600-180">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="d2600-181">이 매개 변수를 지정하지 않으면 이 cmdlet은 *Dtu* 매개 변수의 값에 따라 달라지는 값을 계산합니다.</span><span class="sxs-lookup"><span data-stu-id="d2600-181">If you do not specify this parameter, this cmdlet calculates a value that depends on the value of the *Dtu* parameter.</span></span>
<span data-ttu-id="d2600-182">가능한 [값에 대한 eDTU](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) 및 저장소 제한을 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d2600-182">See [eDTU and storage limits](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) for possible values.</span></span>

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

### <span data-ttu-id="d2600-183">-Tags</span><span class="sxs-lookup"><span data-stu-id="d2600-183">-Tags</span></span>
<span data-ttu-id="d2600-184">이 cmdlet이 탄력적 풀과 연결되는 해시 테이블의 형태로 Key-value 쌍의 사전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d2600-184">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the elastic pool.</span></span> <span data-ttu-id="d2600-185">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="d2600-185">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="d2600-186">-VCore</span><span class="sxs-lookup"><span data-stu-id="d2600-186">-VCore</span></span>
<span data-ttu-id="d2600-187">Sql Azure Elastic Pool에 대한 총 공유 Vcores 수입니다.</span><span class="sxs-lookup"><span data-stu-id="d2600-187">The total shared number of Vcores for the Sql Azure Elastic Pool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: VcoreBasedPool
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2600-188">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="d2600-188">-ZoneRedundant</span></span>
<span data-ttu-id="d2600-189">Azure Sql Elastic Pool과 연결되는 영역 중복성</span><span class="sxs-lookup"><span data-stu-id="d2600-189">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="d2600-190">-확인</span><span class="sxs-lookup"><span data-stu-id="d2600-190">-Confirm</span></span>
<span data-ttu-id="d2600-191">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d2600-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2600-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2600-192">-WhatIf</span></span>
<span data-ttu-id="d2600-193">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d2600-193">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2600-194">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d2600-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2600-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2600-195">CommonParameters</span></span>
<span data-ttu-id="d2600-196">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d2600-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2600-197">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d2600-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2600-198">입력</span><span class="sxs-lookup"><span data-stu-id="d2600-198">INPUTS</span></span>

### <span data-ttu-id="d2600-199">System.String</span><span class="sxs-lookup"><span data-stu-id="d2600-199">System.String</span></span>

## <span data-ttu-id="d2600-200">출력</span><span class="sxs-lookup"><span data-stu-id="d2600-200">OUTPUTS</span></span>

### <span data-ttu-id="d2600-201">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span><span class="sxs-lookup"><span data-stu-id="d2600-201">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="d2600-202">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d2600-202">NOTES</span></span>

## <span data-ttu-id="d2600-203">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d2600-203">RELATED LINKS</span></span>

[<span data-ttu-id="d2600-204">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="d2600-204">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="d2600-205">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="d2600-205">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="d2600-206">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="d2600-206">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="d2600-207">Remove-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="d2600-207">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="d2600-208">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="d2600-208">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="d2600-209">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="d2600-209">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
