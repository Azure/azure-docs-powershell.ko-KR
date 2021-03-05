---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/powershell/module/az.rediscache/set-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
ms.openlocfilehash: 809939a4e218005c9b4c41846e0885dfca553964
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000912"
---
# <span data-ttu-id="03e2c-101">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="03e2c-101">Set-AzRedisCache</span></span>

## <span data-ttu-id="03e2c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03e2c-102">SYNOPSIS</span></span>
<span data-ttu-id="03e2c-103">Redis Cache를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="03e2c-103">Modifies a Redis Cache.</span></span>

## <span data-ttu-id="03e2c-104">구문</span><span class="sxs-lookup"><span data-stu-id="03e2c-104">SYNTAX</span></span>

```
Set-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-MinimumTlsVersion <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="03e2c-105">설명</span><span class="sxs-lookup"><span data-stu-id="03e2c-105">DESCRIPTION</span></span>
<span data-ttu-id="03e2c-106">**Set-AzRedisCache** cmdlet은 Azure Redis Cache를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="03e2c-106">The **Set-AzRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="03e2c-107">예제</span><span class="sxs-lookup"><span data-stu-id="03e2c-107">EXAMPLES</span></span>

### <span data-ttu-id="03e2c-108">예제 1: Redis Cache 수정</span><span class="sxs-lookup"><span data-stu-id="03e2c-108">Example 1: Modify a Redis Cache</span></span>
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

<span data-ttu-id="03e2c-109">이 명령은 MyCache라는 Redis Cache에 대한 maxmemory-policy를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="03e2c-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="03e2c-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="03e2c-110">PARAMETERS</span></span>

### <span data-ttu-id="03e2c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03e2c-111">-DefaultProfile</span></span>
<span data-ttu-id="03e2c-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="03e2c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="03e2c-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="03e2c-113">-EnableNonSslPort</span></span>
<span data-ttu-id="03e2c-114">비 SSL 포트를 사용하도록 설정되어 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="03e2c-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="03e2c-115">기본값은 $False(비 SSL 포트를 사용하지 않도록 설정)입니다.</span><span class="sxs-lookup"><span data-stu-id="03e2c-115">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="03e2c-116">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="03e2c-116">-MinimumTlsVersion</span></span>
<span data-ttu-id="03e2c-117">캐시에 연결하는 데 필요한 TLS 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="03e2c-117">Specify the TLS version required by clients to connect to cache.</span></span>

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

### <span data-ttu-id="03e2c-118">-Name</span><span class="sxs-lookup"><span data-stu-id="03e2c-118">-Name</span></span>
<span data-ttu-id="03e2c-119">업데이트할 Redis Cache의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="03e2c-119">Specifies the name of the Redis Cache to update.</span></span>

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

### <span data-ttu-id="03e2c-120">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="03e2c-120">-RedisConfiguration</span></span>
<span data-ttu-id="03e2c-121">Redis 구성 설정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="03e2c-121">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="03e2c-122">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="03e2c-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="03e2c-123">rdb-backup을 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="03e2c-123">rdb-backup-enabled.</span></span>
<span data-ttu-id="03e2c-124">Redis 데이터 지속성이 사용하도록 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="03e2c-124">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="03e2c-125">프리미엄 계층만 해당합니다.</span><span class="sxs-lookup"><span data-stu-id="03e2c-125">Premium tier only.</span></span>
- <span data-ttu-id="03e2c-126">rdb-storage-connection-string.</span><span class="sxs-lookup"><span data-stu-id="03e2c-126">rdb-storage-connection-string.</span></span>
<span data-ttu-id="03e2c-127">Redis 데이터 지속성에 대한 Storage 계정에 대한 연결 문자열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="03e2c-127">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="03e2c-128">프리미엄 계층만 해당합니다.</span><span class="sxs-lookup"><span data-stu-id="03e2c-128">Premium tier only.</span></span>
- <span data-ttu-id="03e2c-129">rdb-backup-frequency.</span><span class="sxs-lookup"><span data-stu-id="03e2c-129">rdb-backup-frequency.</span></span>
<span data-ttu-id="03e2c-130">Redis 데이터 지속성에 대한 백업 빈도를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="03e2c-130">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="03e2c-131">프리미엄 계층만 해당합니다.</span><span class="sxs-lookup"><span data-stu-id="03e2c-131">Premium tier only.</span></span> 
- <span data-ttu-id="03e2c-132">maxmemory-reserved.</span><span class="sxs-lookup"><span data-stu-id="03e2c-132">maxmemory-reserved.</span></span>
<span data-ttu-id="03e2c-133">캐시가 아닌 프로세스에 대해 예약된 메모리를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="03e2c-133">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="03e2c-134">표준 및 프리미엄 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="03e2c-134">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="03e2c-135">maxmemory-policy.</span><span class="sxs-lookup"><span data-stu-id="03e2c-135">maxmemory-policy.</span></span>
<span data-ttu-id="03e2c-136">캐시에 대한 삭제 정책을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="03e2c-136">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="03e2c-137">모든 가격 책정 계층.</span><span class="sxs-lookup"><span data-stu-id="03e2c-137">All pricing tiers.</span></span> 
- <span data-ttu-id="03e2c-138">notify-keyspace-events.</span><span class="sxs-lookup"><span data-stu-id="03e2c-138">notify-keyspace-events.</span></span>
<span data-ttu-id="03e2c-139">키스페이스 알림을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="03e2c-139">Configures keyspace notifications.</span></span>
<span data-ttu-id="03e2c-140">표준 및 프리미엄 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="03e2c-140">Standard and premium tiers.</span></span> 
- <span data-ttu-id="03e2c-141">hash-max-ziplist-entries.</span><span class="sxs-lookup"><span data-stu-id="03e2c-141">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="03e2c-142">작은 집계 데이터 형식에 대한 메모리 최적화를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="03e2c-142">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="03e2c-143">표준 및 프리미엄 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="03e2c-143">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="03e2c-144">해시-max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="03e2c-144">hash-max-ziplist-value.</span></span>
<span data-ttu-id="03e2c-145">작은 집계 데이터 형식에 대한 메모리 최적화를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="03e2c-145">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="03e2c-146">표준 및 프리미엄 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="03e2c-146">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="03e2c-147">set-max-intset-entries.</span><span class="sxs-lookup"><span data-stu-id="03e2c-147">set-max-intset-entries.</span></span>
<span data-ttu-id="03e2c-148">작은 집계 데이터 형식에 대한 메모리 최적화를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="03e2c-148">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="03e2c-149">표준 및 프리미엄 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="03e2c-149">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="03e2c-150">zset-max-ziplist-entries.</span><span class="sxs-lookup"><span data-stu-id="03e2c-150">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="03e2c-151">작은 집계 데이터 형식에 대한 메모리 최적화를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="03e2c-151">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="03e2c-152">표준 및 프리미엄 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="03e2c-152">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="03e2c-153">zset-max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="03e2c-153">zset-max-ziplist-value.</span></span>
<span data-ttu-id="03e2c-154">작은 집계 데이터 형식에 대한 메모리 최적화를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="03e2c-154">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="03e2c-155">표준 및 프리미엄 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="03e2c-155">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="03e2c-156">데이터베이스.</span><span class="sxs-lookup"><span data-stu-id="03e2c-156">databases.</span></span>
<span data-ttu-id="03e2c-157">데이터베이스 수를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="03e2c-157">Configures the number of databases.</span></span>
<span data-ttu-id="03e2c-158">이 속성은 캐시를 만들 때만 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03e2c-158">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="03e2c-159">표준 및 프리미엄 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="03e2c-159">Standard and Premium tiers.</span></span>
<span data-ttu-id="03e2c-160">자세한 내용은 Azure PowerShell을 사용하여 Azure Redis Cache 관리를 http://go.microsoft.com/fwlink/?LinkId=800051 http://go.microsoft.com/fwlink/?LinkId=800051) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="03e2c-160">For more information, see Manage Azure Redis Cache with Azure PowerShellhttp://go.microsoft.com/fwlink/?LinkId=800051 (http://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="03e2c-161">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03e2c-161">-ResourceGroupName</span></span>
<span data-ttu-id="03e2c-162">Redis Cache를 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="03e2c-162">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="03e2c-163">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="03e2c-163">-ShardCount</span></span>
<span data-ttu-id="03e2c-164">Premium 클러스터 캐시에서 만들 수 있는 샤드 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="03e2c-164">Specifies the number of shards to create on a Premium cluster cache.</span></span>

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

### <span data-ttu-id="03e2c-165">-Size</span><span class="sxs-lookup"><span data-stu-id="03e2c-165">-Size</span></span>
<span data-ttu-id="03e2c-166">Redis Cache의 크기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="03e2c-166">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="03e2c-167">유효한 값은:</span><span class="sxs-lookup"><span data-stu-id="03e2c-167">Valid values are:</span></span> 
- <span data-ttu-id="03e2c-168">P1</span><span class="sxs-lookup"><span data-stu-id="03e2c-168">P1</span></span>
- <span data-ttu-id="03e2c-169">P2</span><span class="sxs-lookup"><span data-stu-id="03e2c-169">P2</span></span>
- <span data-ttu-id="03e2c-170">P3</span><span class="sxs-lookup"><span data-stu-id="03e2c-170">P3</span></span>
- <span data-ttu-id="03e2c-171">P4</span><span class="sxs-lookup"><span data-stu-id="03e2c-171">P4</span></span>
- <span data-ttu-id="03e2c-172">P5</span><span class="sxs-lookup"><span data-stu-id="03e2c-172">P5</span></span>
- <span data-ttu-id="03e2c-173">C0</span><span class="sxs-lookup"><span data-stu-id="03e2c-173">C0</span></span>
- <span data-ttu-id="03e2c-174">C1</span><span class="sxs-lookup"><span data-stu-id="03e2c-174">C1</span></span>
- <span data-ttu-id="03e2c-175">C2</span><span class="sxs-lookup"><span data-stu-id="03e2c-175">C2</span></span>
- <span data-ttu-id="03e2c-176">C3</span><span class="sxs-lookup"><span data-stu-id="03e2c-176">C3</span></span>
- <span data-ttu-id="03e2c-177">C4</span><span class="sxs-lookup"><span data-stu-id="03e2c-177">C4</span></span>
- <span data-ttu-id="03e2c-178">C5</span><span class="sxs-lookup"><span data-stu-id="03e2c-178">C5</span></span>
- <span data-ttu-id="03e2c-179">C6</span><span class="sxs-lookup"><span data-stu-id="03e2c-179">C6</span></span>
- <span data-ttu-id="03e2c-180">250MB</span><span class="sxs-lookup"><span data-stu-id="03e2c-180">250MB</span></span>
- <span data-ttu-id="03e2c-181">1GB</span><span class="sxs-lookup"><span data-stu-id="03e2c-181">1GB</span></span>
- <span data-ttu-id="03e2c-182">2.5GB</span><span class="sxs-lookup"><span data-stu-id="03e2c-182">2.5GB</span></span>
- <span data-ttu-id="03e2c-183">6GB</span><span class="sxs-lookup"><span data-stu-id="03e2c-183">6GB</span></span>
- <span data-ttu-id="03e2c-184">13GB</span><span class="sxs-lookup"><span data-stu-id="03e2c-184">13GB</span></span>
- <span data-ttu-id="03e2c-185">26GB</span><span class="sxs-lookup"><span data-stu-id="03e2c-185">26GB</span></span>
- <span data-ttu-id="03e2c-186">53GB</span><span class="sxs-lookup"><span data-stu-id="03e2c-186">53GB</span></span>
- <span data-ttu-id="03e2c-187">120GB 기본값은 1GB 또는 C1입니다.</span><span class="sxs-lookup"><span data-stu-id="03e2c-187">120GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="03e2c-188">-Sku</span><span class="sxs-lookup"><span data-stu-id="03e2c-188">-Sku</span></span>
<span data-ttu-id="03e2c-189">만들 Redis Cache의 SKU를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="03e2c-189">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="03e2c-190">유효한 값은:</span><span class="sxs-lookup"><span data-stu-id="03e2c-190">Valid values are:</span></span> 
- <span data-ttu-id="03e2c-191">기본</span><span class="sxs-lookup"><span data-stu-id="03e2c-191">Basic</span></span>
- <span data-ttu-id="03e2c-192">표준</span><span class="sxs-lookup"><span data-stu-id="03e2c-192">Standard</span></span>
- <span data-ttu-id="03e2c-193">Premium 기본값은 Standard입니다.</span><span class="sxs-lookup"><span data-stu-id="03e2c-193">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="03e2c-194">-Tag</span><span class="sxs-lookup"><span data-stu-id="03e2c-194">-Tag</span></span>
<span data-ttu-id="03e2c-195">태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="03e2c-195">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="03e2c-196">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="03e2c-196">-TenantSettings</span></span>
<span data-ttu-id="03e2c-197">이 매개 변수는 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03e2c-197">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="03e2c-198">-확인</span><span class="sxs-lookup"><span data-stu-id="03e2c-198">-Confirm</span></span>
<span data-ttu-id="03e2c-199">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="03e2c-199">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="03e2c-200">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="03e2c-200">-WhatIf</span></span>
<span data-ttu-id="03e2c-201">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="03e2c-201">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="03e2c-202">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="03e2c-202">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="03e2c-203">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03e2c-203">CommonParameters</span></span>
<span data-ttu-id="03e2c-204">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="03e2c-204">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03e2c-205">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="03e2c-205">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03e2c-206">입력</span><span class="sxs-lookup"><span data-stu-id="03e2c-206">INPUTS</span></span>

### <span data-ttu-id="03e2c-207">System.String</span><span class="sxs-lookup"><span data-stu-id="03e2c-207">System.String</span></span>

### <span data-ttu-id="03e2c-208">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="03e2c-208">System.Collections.Hashtable</span></span>

### <span data-ttu-id="03e2c-209">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="03e2c-209">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="03e2c-210">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="03e2c-210">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="03e2c-211">출력</span><span class="sxs-lookup"><span data-stu-id="03e2c-211">OUTPUTS</span></span>

### <span data-ttu-id="03e2c-212">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="03e2c-212">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="03e2c-213">참고 사항</span><span class="sxs-lookup"><span data-stu-id="03e2c-213">NOTES</span></span>

## <span data-ttu-id="03e2c-214">관련 링크</span><span class="sxs-lookup"><span data-stu-id="03e2c-214">RELATED LINKS</span></span>

[<span data-ttu-id="03e2c-215">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="03e2c-215">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="03e2c-216">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="03e2c-216">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="03e2c-217">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="03e2c-217">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)


