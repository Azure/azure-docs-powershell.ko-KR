---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/set-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
ms.openlocfilehash: 5cb3723e95acbc05b5fffce55a1f768c8a3b7fba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186556"
---
# <span data-ttu-id="1bead-101">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="1bead-101">Set-AzRedisCache</span></span>

## <span data-ttu-id="1bead-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1bead-102">SYNOPSIS</span></span>
<span data-ttu-id="1bead-103">Redis Cache를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="1bead-103">Modifies a Redis Cache.</span></span>

## <span data-ttu-id="1bead-104">구문</span><span class="sxs-lookup"><span data-stu-id="1bead-104">SYNTAX</span></span>

```
Set-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-MinimumTlsVersion <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1bead-105">설명</span><span class="sxs-lookup"><span data-stu-id="1bead-105">DESCRIPTION</span></span>
<span data-ttu-id="1bead-106">**Set-AzRedisCache** cmdlet은 Azure Redis Cache를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="1bead-106">The **Set-AzRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="1bead-107">예제</span><span class="sxs-lookup"><span data-stu-id="1bead-107">EXAMPLES</span></span>

### <span data-ttu-id="1bead-108">예제 1: Redis Cache 수정</span><span class="sxs-lookup"><span data-stu-id="1bead-108">Example 1: Modify a Redis Cache</span></span>
```
PS C:\>Set-AzRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"}

          PrimaryKey         : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          SecondaryKey       : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          ResourceGroupName  : mygroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/mygroup/providers/Microsoft.Cache/Redis/myCache
          Location           : North Central US
          Name               : MyCache
          Type               : Microsoft.Cache/Redis
          HostName           : mycache.redis.cache.windows.net
          Port               : 6379
          ProvisioningState  : creating
          SslPort            : 6380
          RedisConfiguration : {[maxmemory-policy, allkeys-random]}
          EnableNonSslPort   : False
          RedisVersion       : 2.8
          Size               : 250MB
          Sku                : Standard
          Tag                : {}
          Zone               : []
```

<span data-ttu-id="1bead-109">이 명령은 MyCache라는 Redis Cache에 대한 maxmemory-policy를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1bead-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="1bead-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1bead-110">PARAMETERS</span></span>

### <span data-ttu-id="1bead-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bead-111">-DefaultProfile</span></span>
<span data-ttu-id="1bead-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1bead-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1bead-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="1bead-113">-EnableNonSslPort</span></span>
<span data-ttu-id="1bead-114">비 SSL 포트를 사용하도록 설정되어 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1bead-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="1bead-115">기본값은 $False(비 SSL 포트를 사용하지 않도록 설정)입니다.</span><span class="sxs-lookup"><span data-stu-id="1bead-115">The default value is $False (the non-SSL port is disabled).</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bead-116">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="1bead-116">-MinimumTlsVersion</span></span>
<span data-ttu-id="1bead-117">클라이언트가 캐시에 연결하는 데 필요한 TLS 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1bead-117">Specify the TLS version required by clients to connect to cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bead-118">-Name</span><span class="sxs-lookup"><span data-stu-id="1bead-118">-Name</span></span>
<span data-ttu-id="1bead-119">업데이트할 Redis Cache의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1bead-119">Specifies the name of the Redis Cache to update.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bead-120">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="1bead-120">-RedisConfiguration</span></span>
<span data-ttu-id="1bead-121">Redis 구성 설정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1bead-121">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="1bead-122">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="1bead-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1bead-123">rdb-backup을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1bead-123">rdb-backup-enabled.</span></span>
<span data-ttu-id="1bead-124">Redis 데이터 지속성 사용으로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1bead-124">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="1bead-125">프리미엄 계층만 해당됩니다.</span><span class="sxs-lookup"><span data-stu-id="1bead-125">Premium tier only.</span></span>
- <span data-ttu-id="1bead-126">rdb-storage-connection-string.</span><span class="sxs-lookup"><span data-stu-id="1bead-126">rdb-storage-connection-string.</span></span>
<span data-ttu-id="1bead-127">Redis 데이터 지속성에 대한 Storage 계정에 대한 연결 문자열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1bead-127">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="1bead-128">프리미엄 계층만 해당됩니다.</span><span class="sxs-lookup"><span data-stu-id="1bead-128">Premium tier only.</span></span>
- <span data-ttu-id="1bead-129">rdb-backup-frequency.</span><span class="sxs-lookup"><span data-stu-id="1bead-129">rdb-backup-frequency.</span></span>
<span data-ttu-id="1bead-130">Redis 데이터 지속성에 대한 백업 빈도를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1bead-130">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="1bead-131">프리미엄 계층만 해당됩니다.</span><span class="sxs-lookup"><span data-stu-id="1bead-131">Premium tier only.</span></span> 
- <span data-ttu-id="1bead-132">maxmemory-reserved.</span><span class="sxs-lookup"><span data-stu-id="1bead-132">maxmemory-reserved.</span></span>
<span data-ttu-id="1bead-133">비 캐시 프로세스에 대해 예약된 메모리를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="1bead-133">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="1bead-134">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="1bead-134">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="1bead-135">maxmemory-policy.</span><span class="sxs-lookup"><span data-stu-id="1bead-135">maxmemory-policy.</span></span>
<span data-ttu-id="1bead-136">캐시에 대한 삭제 정책을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="1bead-136">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="1bead-137">모든 가격 책정 계층.</span><span class="sxs-lookup"><span data-stu-id="1bead-137">All pricing tiers.</span></span> 
- <span data-ttu-id="1bead-138">notify-keyspace-events.</span><span class="sxs-lookup"><span data-stu-id="1bead-138">notify-keyspace-events.</span></span>
<span data-ttu-id="1bead-139">키스페이스 알림을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="1bead-139">Configures keyspace notifications.</span></span>
<span data-ttu-id="1bead-140">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="1bead-140">Standard and premium tiers.</span></span> 
- <span data-ttu-id="1bead-141">hash-max-ziplist-entries.</span><span class="sxs-lookup"><span data-stu-id="1bead-141">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="1bead-142">작은 집계 데이터 형식에 대한 메모리 최적화를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="1bead-142">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="1bead-143">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="1bead-143">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="1bead-144">hash-max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="1bead-144">hash-max-ziplist-value.</span></span>
<span data-ttu-id="1bead-145">작은 집계 데이터 형식에 대한 메모리 최적화를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="1bead-145">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="1bead-146">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="1bead-146">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="1bead-147">set-max-intset-entries.</span><span class="sxs-lookup"><span data-stu-id="1bead-147">set-max-intset-entries.</span></span>
<span data-ttu-id="1bead-148">작은 집계 데이터 형식에 대한 메모리 최적화를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="1bead-148">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="1bead-149">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="1bead-149">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="1bead-150">zset-max-ziplist-entries.</span><span class="sxs-lookup"><span data-stu-id="1bead-150">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="1bead-151">작은 집계 데이터 형식에 대한 메모리 최적화를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="1bead-151">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="1bead-152">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="1bead-152">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="1bead-153">zset-max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="1bead-153">zset-max-ziplist-value.</span></span>
<span data-ttu-id="1bead-154">작은 집계 데이터 형식에 대한 메모리 최적화를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="1bead-154">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="1bead-155">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="1bead-155">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="1bead-156">데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1bead-156">databases.</span></span>
<span data-ttu-id="1bead-157">데이터베이스 수를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="1bead-157">Configures the number of databases.</span></span>
<span data-ttu-id="1bead-158">이 속성은 캐시를 만들 때만 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1bead-158">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="1bead-159">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="1bead-159">Standard and Premium tiers.</span></span>
<span data-ttu-id="1bead-160">자세한 내용은 Azure PowerShell을 사용하여 Azure Redis Cache http://go.microsoft.com/fwlink/?LinkId=800051 http://go.microsoft.com/fwlink/?LinkId=800051) 관리(.</span><span class="sxs-lookup"><span data-stu-id="1bead-160">For more information, see Manage Azure Redis Cache with Azure PowerShellhttp://go.microsoft.com/fwlink/?LinkId=800051 (http://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bead-161">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bead-161">-ResourceGroupName</span></span>
<span data-ttu-id="1bead-162">Redis Cache를 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1bead-162">Specifies the name of the resource group that contains the Redis Cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bead-163">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="1bead-163">-ShardCount</span></span>
<span data-ttu-id="1bead-164">프리미엄 클러스터 캐시에 만들 수 있는 Shard 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1bead-164">Specifies the number of shards to create on a Premium cluster cache.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bead-165">-Size</span><span class="sxs-lookup"><span data-stu-id="1bead-165">-Size</span></span>
<span data-ttu-id="1bead-166">Redis Cache의 크기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1bead-166">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="1bead-167">유효한 값은</span><span class="sxs-lookup"><span data-stu-id="1bead-167">Valid values are:</span></span> 
- <span data-ttu-id="1bead-168">P1</span><span class="sxs-lookup"><span data-stu-id="1bead-168">P1</span></span>
- <span data-ttu-id="1bead-169">P2</span><span class="sxs-lookup"><span data-stu-id="1bead-169">P2</span></span>
- <span data-ttu-id="1bead-170">P3</span><span class="sxs-lookup"><span data-stu-id="1bead-170">P3</span></span>
- <span data-ttu-id="1bead-171">P4</span><span class="sxs-lookup"><span data-stu-id="1bead-171">P4</span></span>
- <span data-ttu-id="1bead-172">P5</span><span class="sxs-lookup"><span data-stu-id="1bead-172">P5</span></span>
- <span data-ttu-id="1bead-173">C0</span><span class="sxs-lookup"><span data-stu-id="1bead-173">C0</span></span>
- <span data-ttu-id="1bead-174">C1</span><span class="sxs-lookup"><span data-stu-id="1bead-174">C1</span></span>
- <span data-ttu-id="1bead-175">C2</span><span class="sxs-lookup"><span data-stu-id="1bead-175">C2</span></span>
- <span data-ttu-id="1bead-176">C3</span><span class="sxs-lookup"><span data-stu-id="1bead-176">C3</span></span>
- <span data-ttu-id="1bead-177">C4</span><span class="sxs-lookup"><span data-stu-id="1bead-177">C4</span></span>
- <span data-ttu-id="1bead-178">C5</span><span class="sxs-lookup"><span data-stu-id="1bead-178">C5</span></span>
- <span data-ttu-id="1bead-179">C6</span><span class="sxs-lookup"><span data-stu-id="1bead-179">C6</span></span>
- <span data-ttu-id="1bead-180">250MB</span><span class="sxs-lookup"><span data-stu-id="1bead-180">250MB</span></span>
- <span data-ttu-id="1bead-181">1GB</span><span class="sxs-lookup"><span data-stu-id="1bead-181">1GB</span></span>
- <span data-ttu-id="1bead-182">2.5GB</span><span class="sxs-lookup"><span data-stu-id="1bead-182">2.5GB</span></span>
- <span data-ttu-id="1bead-183">6GB</span><span class="sxs-lookup"><span data-stu-id="1bead-183">6GB</span></span>
- <span data-ttu-id="1bead-184">13GB</span><span class="sxs-lookup"><span data-stu-id="1bead-184">13GB</span></span>
- <span data-ttu-id="1bead-185">26GB</span><span class="sxs-lookup"><span data-stu-id="1bead-185">26GB</span></span>
- <span data-ttu-id="1bead-186">53GB</span><span class="sxs-lookup"><span data-stu-id="1bead-186">53GB</span></span>
- <span data-ttu-id="1bead-187">120GB 기본값은 1GB 또는 C1입니다.</span><span class="sxs-lookup"><span data-stu-id="1bead-187">120GB The default value is 1GB or C1.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bead-188">-Sku</span><span class="sxs-lookup"><span data-stu-id="1bead-188">-Sku</span></span>
<span data-ttu-id="1bead-189">만들 Redis Cache의 SKU를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1bead-189">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="1bead-190">유효한 값은</span><span class="sxs-lookup"><span data-stu-id="1bead-190">Valid values are:</span></span> 
- <span data-ttu-id="1bead-191">기본</span><span class="sxs-lookup"><span data-stu-id="1bead-191">Basic</span></span>
- <span data-ttu-id="1bead-192">표준</span><span class="sxs-lookup"><span data-stu-id="1bead-192">Standard</span></span>
- <span data-ttu-id="1bead-193">Premium 기본값은 Standard입니다.</span><span class="sxs-lookup"><span data-stu-id="1bead-193">Premium The default value is Standard.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bead-194">-Tag</span><span class="sxs-lookup"><span data-stu-id="1bead-194">-Tag</span></span>
<span data-ttu-id="1bead-195">태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="1bead-195">A hash table which represents tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bead-196">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="1bead-196">-TenantSettings</span></span>
<span data-ttu-id="1bead-197">이 매개 변수는 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1bead-197">This parameter has been deprecated.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bead-198">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1bead-198">-Confirm</span></span>
<span data-ttu-id="1bead-199">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1bead-199">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bead-200">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bead-200">-WhatIf</span></span>
<span data-ttu-id="1bead-201">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1bead-201">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1bead-202">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1bead-202">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bead-203">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bead-203">CommonParameters</span></span>
<span data-ttu-id="1bead-204">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1bead-204">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bead-205">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1bead-205">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bead-206">입력</span><span class="sxs-lookup"><span data-stu-id="1bead-206">INPUTS</span></span>

### <span data-ttu-id="1bead-207">System.String</span><span class="sxs-lookup"><span data-stu-id="1bead-207">System.String</span></span>

### <span data-ttu-id="1bead-208">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="1bead-208">System.Collections.Hashtable</span></span>

### <span data-ttu-id="1bead-209">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1bead-209">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="1bead-210">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1bead-210">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="1bead-211">출력</span><span class="sxs-lookup"><span data-stu-id="1bead-211">OUTPUTS</span></span>

### <span data-ttu-id="1bead-212">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="1bead-212">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="1bead-213">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1bead-213">NOTES</span></span>

## <span data-ttu-id="1bead-214">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1bead-214">RELATED LINKS</span></span>

[<span data-ttu-id="1bead-215">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="1bead-215">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="1bead-216">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="1bead-216">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="1bead-217">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="1bead-217">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)


