---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 009899E5-83BF-4A3F-877E-70C16D5CD1AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlelasticpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlElasticPool.md
ms.openlocfilehash: 8fbc0d1e1ac32906c081c5a9714c8420e0f1292e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698892"
---
# <span data-ttu-id="9a110-101">New-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="9a110-101">New-AzSqlElasticPool</span></span>

## <span data-ttu-id="9a110-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a110-102">SYNOPSIS</span></span>
<span data-ttu-id="9a110-103">SQL 데이터베이스에 대 한 탄력적 데이터베이스 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9a110-103">Creates an elastic database pool for a SQL Database.</span></span>

## <span data-ttu-id="9a110-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9a110-104">SYNTAX</span></span>

### <span data-ttu-id="9a110-105">DtuBasedPool (기본값)</span><span class="sxs-lookup"><span data-stu-id="9a110-105">DtuBasedPool (Default)</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> [-Edition <String>] [-Dtu <Int32>] [-StorageMB <Int32>]
 [-DatabaseDtuMin <Int32>] [-DatabaseDtuMax <Int32>] [-Tags <Hashtable>] [-ZoneRedundant]
 [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a110-106">VcoreBasedPool</span><span class="sxs-lookup"><span data-stu-id="9a110-106">VcoreBasedPool</span></span>
```
New-AzSqlElasticPool [-ElasticPoolName] <String> -Edition <String> [-StorageMB <Int32>] -VCore <Int32>
 -ComputeGeneration <String> [-DatabaseVCoreMin <Double>] [-DatabaseVCoreMax <Double>] [-Tags <Hashtable>]
 [-ZoneRedundant] [-LicenseType <String>] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a110-107">설명은</span><span class="sxs-lookup"><span data-stu-id="9a110-107">DESCRIPTION</span></span>
<span data-ttu-id="9a110-108">**AzSqlElasticPool** Cmdlet은 Azure SQL 데이터베이스에 대 한 탄력적 데이터베이스 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9a110-108">The **New-AzSqlElasticPool** cmdlet creates an elastic database pool for an Azure SQL Database.</span></span>
<span data-ttu-id="9a110-109">여러 매개 변수 ( *-Dtu,-DatabaseDtuMin 및-DatabaseDtuMax* )에는 해당 매개 변수에 대 한 유효한 값 목록에서 값을 설정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a110-109">Several parameters ( *-Dtu, -DatabaseDtuMin, and -DatabaseDtuMax* ) require the value being set is from the list of valid values for that parameter.</span></span> <span data-ttu-id="9a110-110">예를 들어 표준 100 eDTU 풀에 대 한-DatabaseDtuMax은 10, 20, 50 또는 100 으로만 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9a110-110">For example, -DatabaseDtuMax for a Standard 100 eDTU pool can only be set to 10, 20, 50, or 100.</span></span>  <span data-ttu-id="9a110-111">유효한 값에 대 한 자세한 내용은 [탄력적 풀](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)의 특정 크기 풀에 대 한 표를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9a110-111">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

## <span data-ttu-id="9a110-112">예제의</span><span class="sxs-lookup"><span data-stu-id="9a110-112">EXAMPLES</span></span>

### <span data-ttu-id="9a110-113">예제 1: 탄력적 풀 만들기</span><span class="sxs-lookup"><span data-stu-id="9a110-113">Example 1: Create an elastic pool</span></span>
```
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

<span data-ttu-id="9a110-114">이 명령은 ElasticPool01 이라는 표준 서비스 계층에 탄력적 풀을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9a110-114">This command creates an elastic pool in the Standard service tier named ElasticPool01.</span></span> <span data-ttu-id="9a110-115">Server01 라는 서버는 ResourceGroup01 이라는 Azure 리소스 그룹에 할당 되 고,의 탄력적 풀을 호스팅합니다.</span><span class="sxs-lookup"><span data-stu-id="9a110-115">The server named server01, assigned to an Azure resource group named ResourceGroup01, hosts the elastic pool in.</span></span> <span data-ttu-id="9a110-116">명령은 풀의 DTU 속성 값과 풀의 데이터베이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a110-116">The command specifies DTU property values for the pool and the databases in the pool.</span></span>

## <span data-ttu-id="9a110-117">변수</span><span class="sxs-lookup"><span data-stu-id="9a110-117">PARAMETERS</span></span>

### <span data-ttu-id="9a110-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9a110-118">-AsJob</span></span>
<span data-ttu-id="9a110-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="9a110-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9a110-120">-가 며 Egeneration</span><span class="sxs-lookup"><span data-stu-id="9a110-120">-ComputeGeneration</span></span>
<span data-ttu-id="9a110-121">할당할 계산 생성입니다.</span><span class="sxs-lookup"><span data-stu-id="9a110-121">The compute generation to assign.</span></span>

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

### <span data-ttu-id="9a110-122">-DatabaseDtuMax</span><span class="sxs-lookup"><span data-stu-id="9a110-122">-DatabaseDtuMax</span></span>
<span data-ttu-id="9a110-123">풀의 단일 데이터베이스가 소비할 수 있는 최대 Dtu (데이터베이스 처리량 단위) 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a110-123">Specifies the maximum number of Database Throughput Units (DTUs) that any single database in the pool can consume.</span></span>
<span data-ttu-id="9a110-124">여러 버전의 기본값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9a110-124">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="9a110-125">기본적.</span><span class="sxs-lookup"><span data-stu-id="9a110-125">Basic.</span></span> <span data-ttu-id="9a110-126">5 Dtu</span><span class="sxs-lookup"><span data-stu-id="9a110-126">5 DTUs</span></span>
- <span data-ttu-id="9a110-127">표준이.</span><span class="sxs-lookup"><span data-stu-id="9a110-127">Standard.</span></span> <span data-ttu-id="9a110-128">100 Dtu</span><span class="sxs-lookup"><span data-stu-id="9a110-128">100 DTUs</span></span>
- <span data-ttu-id="9a110-129">Premium.</span><span class="sxs-lookup"><span data-stu-id="9a110-129">Premium.</span></span> <span data-ttu-id="9a110-130">125 Dtu 유효한 값에 대 한 자세한 내용은 [탄력적 풀](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool) 의 특정 크기 풀에 대 한 표를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9a110-130">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)</span></span>

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

### <span data-ttu-id="9a110-131">-DatabaseDtuMin</span><span class="sxs-lookup"><span data-stu-id="9a110-131">-DatabaseDtuMin</span></span>
<span data-ttu-id="9a110-132">탄력적 풀이 풀의 모든 데이터베이스에 대해 보장 하는 최소 Dtu 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a110-132">Specifies the minimum number of DTUs that the elastic pool guarantees to all the databases in the pool.</span></span>
<span data-ttu-id="9a110-133">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="9a110-133">The default value is zero (0).</span></span>
<span data-ttu-id="9a110-134">유효한 값에 대 한 자세한 내용은 [탄력적 풀](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)의 특정 크기 풀에 대 한 표를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9a110-134">For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="9a110-135">-DatabaseVCoreMax</span><span class="sxs-lookup"><span data-stu-id="9a110-135">-DatabaseVCoreMax</span></span>
<span data-ttu-id="9a110-136">모든 SqlAzure 데이터베이스가 풀에서 사용할 수 있는 maxmium VCore 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="9a110-136">The maxmium VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="9a110-137">-DatabaseVCoreMin</span><span class="sxs-lookup"><span data-stu-id="9a110-137">-DatabaseVCoreMin</span></span>
<span data-ttu-id="9a110-138">풀에서 사용할 수 있는 모든 SqlAzure 데이터베이스의 최소 VCore 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="9a110-138">The minimum VCore number any SqlAzure Database can consume in the pool.</span></span>

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

### <span data-ttu-id="9a110-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a110-139">-DefaultProfile</span></span>
<span data-ttu-id="9a110-140">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9a110-140">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9a110-141">-Dtu</span><span class="sxs-lookup"><span data-stu-id="9a110-141">-Dtu</span></span>
<span data-ttu-id="9a110-142">탄력적 풀에 대 한 총 공유 Dtu 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a110-142">Specifies the total number of shared DTUs for the elastic pool.</span></span>
<span data-ttu-id="9a110-143">여러 버전의 기본값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9a110-143">The default values for the different editions are as follows:</span></span>
- <span data-ttu-id="9a110-144">기본적.</span><span class="sxs-lookup"><span data-stu-id="9a110-144">Basic.</span></span>
<span data-ttu-id="9a110-145">100 Dtu</span><span class="sxs-lookup"><span data-stu-id="9a110-145">100 DTUs</span></span>
- <span data-ttu-id="9a110-146">표준이.</span><span class="sxs-lookup"><span data-stu-id="9a110-146">Standard.</span></span>
<span data-ttu-id="9a110-147">100 Dtu</span><span class="sxs-lookup"><span data-stu-id="9a110-147">100 DTUs</span></span>
- <span data-ttu-id="9a110-148">Premium.</span><span class="sxs-lookup"><span data-stu-id="9a110-148">Premium.</span></span>
<span data-ttu-id="9a110-149">125 Dtu 유효한 값에 대 한 자세한 내용은 [탄력적 풀](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool)의 특정 크기 풀에 대 한 표를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9a110-149">125 DTUs For details about which values are valid, see the table for your specific size pool in [elastic pools](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool).</span></span>

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

### <span data-ttu-id="9a110-150">-에디션</span><span class="sxs-lookup"><span data-stu-id="9a110-150">-Edition</span></span>
<span data-ttu-id="9a110-151">탄력적 풀에 사용 되는 Azure SQL 데이터베이스의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a110-151">Specifies the edition of the Azure SQL Database used for the elastic pool.</span></span>
<span data-ttu-id="9a110-152">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9a110-152">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="9a110-153">않아야</span><span class="sxs-lookup"><span data-stu-id="9a110-153">None</span></span>
- <span data-ttu-id="9a110-154">기본적</span><span class="sxs-lookup"><span data-stu-id="9a110-154">Basic</span></span>
- <span data-ttu-id="9a110-155">표준이</span><span class="sxs-lookup"><span data-stu-id="9a110-155">Standard</span></span>
- <span data-ttu-id="9a110-156">Premium</span><span class="sxs-lookup"><span data-stu-id="9a110-156">Premium</span></span>
- <span data-ttu-id="9a110-157">웨어하우스</span><span class="sxs-lookup"><span data-stu-id="9a110-157">DataWarehouse</span></span>
- <span data-ttu-id="9a110-158">비우거나</span><span class="sxs-lookup"><span data-stu-id="9a110-158">Free</span></span>
- <span data-ttu-id="9a110-159">늘이고</span><span class="sxs-lookup"><span data-stu-id="9a110-159">Stretch</span></span>
- <span data-ttu-id="9a110-160">일반 목적</span><span class="sxs-lookup"><span data-stu-id="9a110-160">GeneralPurpose</span></span>
- <span data-ttu-id="9a110-161">BusinessCritical</span><span class="sxs-lookup"><span data-stu-id="9a110-161">BusinessCritical</span></span>

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

### <span data-ttu-id="9a110-162">-ElasticPoolName</span><span class="sxs-lookup"><span data-stu-id="9a110-162">-ElasticPoolName</span></span>
<span data-ttu-id="9a110-163">이 cmdlet이 만드는 탄력적 풀의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a110-163">Specifies the name of the elastic pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="9a110-164">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="9a110-164">-LicenseType</span></span>
<span data-ttu-id="9a110-165">Azure Sql 데이터베이스에 대 한 라이선스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="9a110-165">The license type for the Azure Sql database.</span></span>

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

### <span data-ttu-id="9a110-166">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a110-166">-ResourceGroupName</span></span>
<span data-ttu-id="9a110-167">이 cmdlet이 탄력적 풀을 할당 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a110-167">Specifies the name of the resource group to which this cmdlet assigns the elastic pool.</span></span>

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

### <span data-ttu-id="9a110-168">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9a110-168">-ServerName</span></span>
<span data-ttu-id="9a110-169">탄력적 풀을 호스팅하는 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a110-169">Specifies the name of the server that hosts the elastic pool.</span></span>

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

### <span data-ttu-id="9a110-170">-StorageMB</span><span class="sxs-lookup"><span data-stu-id="9a110-170">-StorageMB</span></span>
<span data-ttu-id="9a110-171">탄력적 풀의 저장소 용량 한도 (mb)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a110-171">Specifies the storage limit, in megabytes, for the elastic pool.</span></span> <span data-ttu-id="9a110-172">이 매개 변수를 지정 하지 않으면이 cmdlet은 *Dtu* 매개 변수의 값에 따라 달라 지는 값을 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a110-172">If you do not specify this parameter, this cmdlet calculates a value that depends on the value of the *Dtu* parameter.</span></span>
<span data-ttu-id="9a110-173">가능 값에 대 한 [eDTU 및 저장소 제한을](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9a110-173">See [eDTU and storage limits](/azure/sql-database/sql-database-elastic-pool#edtu-and-storage-limits-for-elastic-pools) for possible values.</span></span>

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

### <span data-ttu-id="9a110-174">태그</span><span class="sxs-lookup"><span data-stu-id="9a110-174">-Tags</span></span>
<span data-ttu-id="9a110-175">이 cmdlet이 탄력적 풀과 연결 하는 해시 테이블 형식으로 키-값 쌍의 사전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a110-175">Specifies a dictionary of Key-value pairs in the form of a hash table that this cmdlet associates with the elastic pool.</span></span> <span data-ttu-id="9a110-176">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="9a110-176">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="9a110-177">-VCore</span><span class="sxs-lookup"><span data-stu-id="9a110-177">-VCore</span></span>
<span data-ttu-id="9a110-178">Sql Azure 탄력적 풀의 총 공유 수입니다.</span><span class="sxs-lookup"><span data-stu-id="9a110-178">The total shared number of Vcores for the Sql Azure Elastic Pool.</span></span>

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

### <span data-ttu-id="9a110-179">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="9a110-179">-ZoneRedundant</span></span>
<span data-ttu-id="9a110-180">Azure Sql 탄력적 풀에 연결 되는 영역 중복성</span><span class="sxs-lookup"><span data-stu-id="9a110-180">The zone redundancy to associate with the Azure Sql Elastic Pool</span></span>

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

### <span data-ttu-id="9a110-181">-확인</span><span class="sxs-lookup"><span data-stu-id="9a110-181">-Confirm</span></span>
<span data-ttu-id="9a110-182">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a110-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a110-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a110-183">-WhatIf</span></span>
<span data-ttu-id="9a110-184">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9a110-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a110-185">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9a110-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a110-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a110-186">CommonParameters</span></span>
<span data-ttu-id="9a110-187">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a110-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a110-188">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9a110-188">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a110-189">입력</span><span class="sxs-lookup"><span data-stu-id="9a110-189">INPUTS</span></span>

### <span data-ttu-id="9a110-190">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9a110-190">System.String</span></span>

## <span data-ttu-id="9a110-191">출력</span><span class="sxs-lookup"><span data-stu-id="9a110-191">OUTPUTS</span></span>

### <span data-ttu-id="9a110-192">ElasticPool. AzureSqlElasticPoolModel에 대 한</span><span class="sxs-lookup"><span data-stu-id="9a110-192">Microsoft.Azure.Commands.Sql.ElasticPool.Model.AzureSqlElasticPoolModel</span></span>

## <span data-ttu-id="9a110-193">상속자</span><span class="sxs-lookup"><span data-stu-id="9a110-193">NOTES</span></span>

## <span data-ttu-id="9a110-194">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9a110-194">RELATED LINKS</span></span>

[<span data-ttu-id="9a110-195">Get-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="9a110-195">Get-AzSqlElasticPool</span></span>](./Get-AzSqlElasticPool.md)

[<span data-ttu-id="9a110-196">Get-AzSqlElasticPoolActivity</span><span class="sxs-lookup"><span data-stu-id="9a110-196">Get-AzSqlElasticPoolActivity</span></span>](./Get-AzSqlElasticPoolActivity.md)

[<span data-ttu-id="9a110-197">Get-AzSqlElasticPoolDatabase</span><span class="sxs-lookup"><span data-stu-id="9a110-197">Get-AzSqlElasticPoolDatabase</span></span>](./Get-AzSqlElasticPoolDatabase.md)

[<span data-ttu-id="9a110-198">제거-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="9a110-198">Remove-AzSqlElasticPool</span></span>](./Remove-AzSqlElasticPool.md)

[<span data-ttu-id="9a110-199">Set-AzSqlElasticPool</span><span class="sxs-lookup"><span data-stu-id="9a110-199">Set-AzSqlElasticPool</span></span>](./Set-AzSqlElasticPool.md)

[<span data-ttu-id="9a110-200">SQL 데이터베이스 설명서</span><span class="sxs-lookup"><span data-stu-id="9a110-200">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
