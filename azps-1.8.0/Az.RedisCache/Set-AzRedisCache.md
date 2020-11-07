---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/set-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
ms.openlocfilehash: 637a1e634b0f8b6f890519bf4865378f50774e39
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699525"
---
# <span data-ttu-id="04fac-101">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="04fac-101">Set-AzRedisCache</span></span>

## <span data-ttu-id="04fac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04fac-102">SYNOPSIS</span></span>
<span data-ttu-id="04fac-103">Redis 캐시를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04fac-103">Modifies a Redis Cache.</span></span>

## <span data-ttu-id="04fac-104">구문과</span><span class="sxs-lookup"><span data-stu-id="04fac-104">SYNTAX</span></span>

```
Set-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="04fac-105">설명은</span><span class="sxs-lookup"><span data-stu-id="04fac-105">DESCRIPTION</span></span>
<span data-ttu-id="04fac-106">**Set-AzRedisCache** Cmdlet은 Azure Redis Cache를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04fac-106">The **Set-AzRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="04fac-107">예제의</span><span class="sxs-lookup"><span data-stu-id="04fac-107">EXAMPLES</span></span>

### <span data-ttu-id="04fac-108">예제 1: Redis 캐시 수정</span><span class="sxs-lookup"><span data-stu-id="04fac-108">Example 1: Modify a Redis Cache</span></span>
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

<span data-ttu-id="04fac-109">이 명령은 MyCache 라는 Redis Cache에 대 한 maxmemory 정책을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="04fac-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="04fac-110">변수</span><span class="sxs-lookup"><span data-stu-id="04fac-110">PARAMETERS</span></span>

### <span data-ttu-id="04fac-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04fac-111">-DefaultProfile</span></span>
<span data-ttu-id="04fac-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="04fac-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04fac-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="04fac-113">-EnableNonSslPort</span></span>
<span data-ttu-id="04fac-114">비 SSL 포트를 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="04fac-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="04fac-115">기본값은 $False (비 SSL 포트를 사용할 수 없음)입니다.</span><span class="sxs-lookup"><span data-stu-id="04fac-115">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="04fac-116">-이름</span><span class="sxs-lookup"><span data-stu-id="04fac-116">-Name</span></span>
<span data-ttu-id="04fac-117">업데이트할 Redis 캐시의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04fac-117">Specifies the name of the Redis Cache to update.</span></span>

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

### <span data-ttu-id="04fac-118">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="04fac-118">-RedisConfiguration</span></span>
<span data-ttu-id="04fac-119">Redis 구성 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04fac-119">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="04fac-120">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="04fac-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="04fac-121">rdb-백업-사용 가능.</span><span class="sxs-lookup"><span data-stu-id="04fac-121">rdb-backup-enabled.</span></span>
<span data-ttu-id="04fac-122">Redis 데이터 지 속성을 사용 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04fac-122">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="04fac-123">프리미엄 계층만.</span><span class="sxs-lookup"><span data-stu-id="04fac-123">Premium tier only.</span></span>
- <span data-ttu-id="04fac-124">rdb-저장소-연결 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="04fac-124">rdb-storage-connection-string.</span></span>
<span data-ttu-id="04fac-125">Redis 데이터 지 속성에 대 한 저장소 계정에 대 한 연결 문자열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04fac-125">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="04fac-126">프리미엄 계층만.</span><span class="sxs-lookup"><span data-stu-id="04fac-126">Premium tier only.</span></span>
- <span data-ttu-id="04fac-127">rdb-백업-빈도</span><span class="sxs-lookup"><span data-stu-id="04fac-127">rdb-backup-frequency.</span></span>
<span data-ttu-id="04fac-128">Redis 데이터 지 속성에 대 한 백업 빈도를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04fac-128">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="04fac-129">프리미엄 계층만.</span><span class="sxs-lookup"><span data-stu-id="04fac-129">Premium tier only.</span></span> 
- <span data-ttu-id="04fac-130">maxmemory-예약 됨.</span><span class="sxs-lookup"><span data-stu-id="04fac-130">maxmemory-reserved.</span></span>
<span data-ttu-id="04fac-131">비 캐시 프로세스에 예약 된 메모리를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="04fac-131">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="04fac-132">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="04fac-132">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="04fac-133">maxmemory-정책.</span><span class="sxs-lookup"><span data-stu-id="04fac-133">maxmemory-policy.</span></span>
<span data-ttu-id="04fac-134">캐시에 대 한 제거 정책을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="04fac-134">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="04fac-135">모든 가격 책정 계층</span><span class="sxs-lookup"><span data-stu-id="04fac-135">All pricing tiers.</span></span> 
- <span data-ttu-id="04fac-136">notify-keyspace-이벤트</span><span class="sxs-lookup"><span data-stu-id="04fac-136">notify-keyspace-events.</span></span>
<span data-ttu-id="04fac-137">Keyspace 알림을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="04fac-137">Configures keyspace notifications.</span></span>
<span data-ttu-id="04fac-138">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="04fac-138">Standard and premium tiers.</span></span> 
- <span data-ttu-id="04fac-139">hash-최대 ziplist-항목.</span><span class="sxs-lookup"><span data-stu-id="04fac-139">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="04fac-140">작은 집계 데이터 형식에 대 한 메모리 최적화를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="04fac-140">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="04fac-141">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="04fac-141">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="04fac-142">hash-max-ziplist-값.</span><span class="sxs-lookup"><span data-stu-id="04fac-142">hash-max-ziplist-value.</span></span>
<span data-ttu-id="04fac-143">작은 집계 데이터 형식에 대 한 메모리 최적화를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="04fac-143">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="04fac-144">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="04fac-144">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="04fac-145">set-max-intset-항목</span><span class="sxs-lookup"><span data-stu-id="04fac-145">set-max-intset-entries.</span></span>
<span data-ttu-id="04fac-146">작은 집계 데이터 형식에 대 한 메모리 최적화를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="04fac-146">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="04fac-147">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="04fac-147">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="04fac-148">zset-max-ziplist 항목.</span><span class="sxs-lookup"><span data-stu-id="04fac-148">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="04fac-149">작은 집계 데이터 형식에 대 한 메모리 최적화를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="04fac-149">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="04fac-150">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="04fac-150">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="04fac-151">zset-max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="04fac-151">zset-max-ziplist-value.</span></span>
<span data-ttu-id="04fac-152">작은 집계 데이터 형식에 대 한 메모리 최적화를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="04fac-152">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="04fac-153">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="04fac-153">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="04fac-154">databases.</span><span class="sxs-lookup"><span data-stu-id="04fac-154">databases.</span></span>
<span data-ttu-id="04fac-155">데이터베이스 수를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="04fac-155">Configures the number of databases.</span></span>
<span data-ttu-id="04fac-156">이 속성은 캐시 생성 시에만 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04fac-156">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="04fac-157">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="04fac-157">Standard and Premium tiers.</span></span>
<span data-ttu-id="04fac-158">자세한 내용은 Azure PowerShell을 사용 하 여 Azure Redis 캐시 관리 https://go.microsoft.com/fwlink/?LinkId=800051 ()를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="04fac-158">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="04fac-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04fac-159">-ResourceGroupName</span></span>
<span data-ttu-id="04fac-160">Redis 캐시를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04fac-160">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="04fac-161">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="04fac-161">-ShardCount</span></span>
<span data-ttu-id="04fac-162">프리미엄 클러스터 캐시에서 만들 shards 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04fac-162">Specifies the number of shards to create on a Premium cluster cache.</span></span>

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

### <span data-ttu-id="04fac-163">-크기</span><span class="sxs-lookup"><span data-stu-id="04fac-163">-Size</span></span>
<span data-ttu-id="04fac-164">Redis 캐시의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04fac-164">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="04fac-165">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="04fac-165">Valid values are:</span></span> 
- <span data-ttu-id="04fac-166">P1</span><span class="sxs-lookup"><span data-stu-id="04fac-166">P1</span></span>
- <span data-ttu-id="04fac-167">즉</span><span class="sxs-lookup"><span data-stu-id="04fac-167">P2</span></span>
- <span data-ttu-id="04fac-168">P3</span><span class="sxs-lookup"><span data-stu-id="04fac-168">P3</span></span>
- <span data-ttu-id="04fac-169">P4</span><span class="sxs-lookup"><span data-stu-id="04fac-169">P4</span></span>
- <span data-ttu-id="04fac-170">C0</span><span class="sxs-lookup"><span data-stu-id="04fac-170">C0</span></span>
- <span data-ttu-id="04fac-171">C1</span><span class="sxs-lookup"><span data-stu-id="04fac-171">C1</span></span>
- <span data-ttu-id="04fac-172">만족할</span><span class="sxs-lookup"><span data-stu-id="04fac-172">C2</span></span>
- <span data-ttu-id="04fac-173">C3</span><span class="sxs-lookup"><span data-stu-id="04fac-173">C3</span></span>
- <span data-ttu-id="04fac-174">C4</span><span class="sxs-lookup"><span data-stu-id="04fac-174">C4</span></span>
- <span data-ttu-id="04fac-175">C 5</span><span class="sxs-lookup"><span data-stu-id="04fac-175">C5</span></span>
- <span data-ttu-id="04fac-176">C6</span><span class="sxs-lookup"><span data-stu-id="04fac-176">C6</span></span>
- <span data-ttu-id="04fac-177">250MB</span><span class="sxs-lookup"><span data-stu-id="04fac-177">250MB</span></span>
- <span data-ttu-id="04fac-178">1GB</span><span class="sxs-lookup"><span data-stu-id="04fac-178">1GB</span></span>
- <span data-ttu-id="04fac-179">2.5 GB</span><span class="sxs-lookup"><span data-stu-id="04fac-179">2.5GB</span></span>
- <span data-ttu-id="04fac-180">6GB</span><span class="sxs-lookup"><span data-stu-id="04fac-180">6GB</span></span>
- <span data-ttu-id="04fac-181">13GB</span><span class="sxs-lookup"><span data-stu-id="04fac-181">13GB</span></span>
- <span data-ttu-id="04fac-182">26GB</span><span class="sxs-lookup"><span data-stu-id="04fac-182">26GB</span></span>
- <span data-ttu-id="04fac-183">53GB 기본 값은 1GB 또는 C1입니다.</span><span class="sxs-lookup"><span data-stu-id="04fac-183">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="04fac-184">-Sku</span><span class="sxs-lookup"><span data-stu-id="04fac-184">-Sku</span></span>
<span data-ttu-id="04fac-185">만들 Redis Cache의 SKU를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04fac-185">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="04fac-186">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="04fac-186">Valid values are:</span></span> 
- <span data-ttu-id="04fac-187">기본적</span><span class="sxs-lookup"><span data-stu-id="04fac-187">Basic</span></span>
- <span data-ttu-id="04fac-188">표준이</span><span class="sxs-lookup"><span data-stu-id="04fac-188">Standard</span></span>
- <span data-ttu-id="04fac-189">Premium 기본 값은 표준입니다.</span><span class="sxs-lookup"><span data-stu-id="04fac-189">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="04fac-190">태그</span><span class="sxs-lookup"><span data-stu-id="04fac-190">-Tag</span></span>
<span data-ttu-id="04fac-191">태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="04fac-191">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="04fac-192">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="04fac-192">-TenantSettings</span></span>
<span data-ttu-id="04fac-193">이 매개 변수는 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04fac-193">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="04fac-194">-확인</span><span class="sxs-lookup"><span data-stu-id="04fac-194">-Confirm</span></span>
<span data-ttu-id="04fac-195">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="04fac-195">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04fac-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04fac-196">-WhatIf</span></span>
<span data-ttu-id="04fac-197">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="04fac-197">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="04fac-198">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04fac-198">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04fac-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04fac-199">CommonParameters</span></span>
<span data-ttu-id="04fac-200">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="04fac-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04fac-201">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04fac-201">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04fac-202">입력</span><span class="sxs-lookup"><span data-stu-id="04fac-202">INPUTS</span></span>

### <span data-ttu-id="04fac-203">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="04fac-203">System.String</span></span>

### <span data-ttu-id="04fac-204">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="04fac-204">System.Collections.Hashtable</span></span>

### <span data-ttu-id="04fac-205">시스템 Null 허용 ' 1 [[CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="04fac-205">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="04fac-206">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e])</span><span class="sxs-lookup"><span data-stu-id="04fac-206">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="04fac-207">출력</span><span class="sxs-lookup"><span data-stu-id="04fac-207">OUTPUTS</span></span>

### <span data-ttu-id="04fac-208">RedisCacheAttributesWithAccessKeys. 모델. m e.</span><span class="sxs-lookup"><span data-stu-id="04fac-208">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="04fac-209">상속자</span><span class="sxs-lookup"><span data-stu-id="04fac-209">NOTES</span></span>

## <span data-ttu-id="04fac-210">관련 링크</span><span class="sxs-lookup"><span data-stu-id="04fac-210">RELATED LINKS</span></span>

[<span data-ttu-id="04fac-211">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="04fac-211">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="04fac-212">새로운 AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="04fac-212">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="04fac-213">제거-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="04fac-213">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)


