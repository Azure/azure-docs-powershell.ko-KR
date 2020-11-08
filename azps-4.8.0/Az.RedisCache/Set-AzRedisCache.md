---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/set-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
ms.openlocfilehash: 5cb3723e95acbc05b5fffce55a1f768c8a3b7fba
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204918"
---
# <span data-ttu-id="56213-101">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="56213-101">Set-AzRedisCache</span></span>

## <span data-ttu-id="56213-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56213-102">SYNOPSIS</span></span>
<span data-ttu-id="56213-103">Redis 캐시를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56213-103">Modifies a Redis Cache.</span></span>

## <span data-ttu-id="56213-104">구문과</span><span class="sxs-lookup"><span data-stu-id="56213-104">SYNTAX</span></span>

```
Set-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-MinimumTlsVersion <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56213-105">설명은</span><span class="sxs-lookup"><span data-stu-id="56213-105">DESCRIPTION</span></span>
<span data-ttu-id="56213-106">**Set-AzRedisCache** Cmdlet은 Azure Redis Cache를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56213-106">The **Set-AzRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="56213-107">예제의</span><span class="sxs-lookup"><span data-stu-id="56213-107">EXAMPLES</span></span>

### <span data-ttu-id="56213-108">예제 1: Redis 캐시 수정</span><span class="sxs-lookup"><span data-stu-id="56213-108">Example 1: Modify a Redis Cache</span></span>
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

<span data-ttu-id="56213-109">이 명령은 MyCache 라는 Redis Cache에 대 한 maxmemory 정책을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="56213-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="56213-110">변수</span><span class="sxs-lookup"><span data-stu-id="56213-110">PARAMETERS</span></span>

### <span data-ttu-id="56213-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56213-111">-DefaultProfile</span></span>
<span data-ttu-id="56213-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="56213-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56213-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="56213-113">-EnableNonSslPort</span></span>
<span data-ttu-id="56213-114">비 SSL 포트를 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="56213-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="56213-115">기본값은 $False (비 SSL 포트를 사용할 수 없음)입니다.</span><span class="sxs-lookup"><span data-stu-id="56213-115">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="56213-116">-없음 Tls 버전</span><span class="sxs-lookup"><span data-stu-id="56213-116">-MinimumTlsVersion</span></span>
<span data-ttu-id="56213-117">클라이언트가 캐시에 연결 하는 데 필요한 TLS 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56213-117">Specify the TLS version required by clients to connect to cache.</span></span>

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

### <span data-ttu-id="56213-118">-이름</span><span class="sxs-lookup"><span data-stu-id="56213-118">-Name</span></span>
<span data-ttu-id="56213-119">업데이트할 Redis 캐시의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56213-119">Specifies the name of the Redis Cache to update.</span></span>

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

### <span data-ttu-id="56213-120">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="56213-120">-RedisConfiguration</span></span>
<span data-ttu-id="56213-121">Redis 구성 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56213-121">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="56213-122">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="56213-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="56213-123">rdb-백업-사용 가능.</span><span class="sxs-lookup"><span data-stu-id="56213-123">rdb-backup-enabled.</span></span>
<span data-ttu-id="56213-124">Redis 데이터 지 속성을 사용 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56213-124">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="56213-125">프리미엄 계층만.</span><span class="sxs-lookup"><span data-stu-id="56213-125">Premium tier only.</span></span>
- <span data-ttu-id="56213-126">rdb-저장소-연결 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="56213-126">rdb-storage-connection-string.</span></span>
<span data-ttu-id="56213-127">Redis 데이터 지 속성에 대 한 저장소 계정에 대 한 연결 문자열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56213-127">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="56213-128">프리미엄 계층만.</span><span class="sxs-lookup"><span data-stu-id="56213-128">Premium tier only.</span></span>
- <span data-ttu-id="56213-129">rdb-백업-빈도</span><span class="sxs-lookup"><span data-stu-id="56213-129">rdb-backup-frequency.</span></span>
<span data-ttu-id="56213-130">Redis 데이터 지 속성에 대 한 백업 빈도를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56213-130">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="56213-131">프리미엄 계층만.</span><span class="sxs-lookup"><span data-stu-id="56213-131">Premium tier only.</span></span> 
- <span data-ttu-id="56213-132">maxmemory-예약 됨.</span><span class="sxs-lookup"><span data-stu-id="56213-132">maxmemory-reserved.</span></span>
<span data-ttu-id="56213-133">비 캐시 프로세스에 예약 된 메모리를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="56213-133">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="56213-134">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="56213-134">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="56213-135">maxmemory-정책.</span><span class="sxs-lookup"><span data-stu-id="56213-135">maxmemory-policy.</span></span>
<span data-ttu-id="56213-136">캐시에 대 한 제거 정책을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="56213-136">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="56213-137">모든 가격 책정 계층</span><span class="sxs-lookup"><span data-stu-id="56213-137">All pricing tiers.</span></span> 
- <span data-ttu-id="56213-138">notify-keyspace-이벤트</span><span class="sxs-lookup"><span data-stu-id="56213-138">notify-keyspace-events.</span></span>
<span data-ttu-id="56213-139">Keyspace 알림을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="56213-139">Configures keyspace notifications.</span></span>
<span data-ttu-id="56213-140">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="56213-140">Standard and premium tiers.</span></span> 
- <span data-ttu-id="56213-141">hash-최대 ziplist-항목.</span><span class="sxs-lookup"><span data-stu-id="56213-141">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="56213-142">작은 집계 데이터 형식에 대 한 메모리 최적화를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="56213-142">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="56213-143">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="56213-143">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="56213-144">hash-max-ziplist-값.</span><span class="sxs-lookup"><span data-stu-id="56213-144">hash-max-ziplist-value.</span></span>
<span data-ttu-id="56213-145">작은 집계 데이터 형식에 대 한 메모리 최적화를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="56213-145">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="56213-146">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="56213-146">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="56213-147">set-max-intset-항목</span><span class="sxs-lookup"><span data-stu-id="56213-147">set-max-intset-entries.</span></span>
<span data-ttu-id="56213-148">작은 집계 데이터 형식에 대 한 메모리 최적화를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="56213-148">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="56213-149">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="56213-149">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="56213-150">zset-max-ziplist 항목.</span><span class="sxs-lookup"><span data-stu-id="56213-150">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="56213-151">작은 집계 데이터 형식에 대 한 메모리 최적화를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="56213-151">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="56213-152">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="56213-152">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="56213-153">zset-max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="56213-153">zset-max-ziplist-value.</span></span>
<span data-ttu-id="56213-154">작은 집계 데이터 형식에 대 한 메모리 최적화를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="56213-154">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="56213-155">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="56213-155">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="56213-156">databases.</span><span class="sxs-lookup"><span data-stu-id="56213-156">databases.</span></span>
<span data-ttu-id="56213-157">데이터베이스 수를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="56213-157">Configures the number of databases.</span></span>
<span data-ttu-id="56213-158">이 속성은 캐시 생성 시에만 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="56213-158">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="56213-159">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="56213-159">Standard and Premium tiers.</span></span>
<span data-ttu-id="56213-160">자세한 내용은 Azure PowerShell을 사용 하 여 Azure Redis 캐시 관리 http://go.microsoft.com/fwlink/?LinkId=800051 ()를 참조 하세요 http://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="56213-160">For more information, see Manage Azure Redis Cache with Azure PowerShellhttp://go.microsoft.com/fwlink/?LinkId=800051 (http://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="56213-161">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56213-161">-ResourceGroupName</span></span>
<span data-ttu-id="56213-162">Redis 캐시를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56213-162">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="56213-163">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="56213-163">-ShardCount</span></span>
<span data-ttu-id="56213-164">프리미엄 클러스터 캐시에서 만들 shards 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56213-164">Specifies the number of shards to create on a Premium cluster cache.</span></span>

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

### <span data-ttu-id="56213-165">-크기</span><span class="sxs-lookup"><span data-stu-id="56213-165">-Size</span></span>
<span data-ttu-id="56213-166">Redis 캐시의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56213-166">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="56213-167">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="56213-167">Valid values are:</span></span> 
- <span data-ttu-id="56213-168">P1</span><span class="sxs-lookup"><span data-stu-id="56213-168">P1</span></span>
- <span data-ttu-id="56213-169">즉</span><span class="sxs-lookup"><span data-stu-id="56213-169">P2</span></span>
- <span data-ttu-id="56213-170">P3</span><span class="sxs-lookup"><span data-stu-id="56213-170">P3</span></span>
- <span data-ttu-id="56213-171">P4</span><span class="sxs-lookup"><span data-stu-id="56213-171">P4</span></span>
- <span data-ttu-id="56213-172">P5</span><span class="sxs-lookup"><span data-stu-id="56213-172">P5</span></span>
- <span data-ttu-id="56213-173">C0</span><span class="sxs-lookup"><span data-stu-id="56213-173">C0</span></span>
- <span data-ttu-id="56213-174">C1</span><span class="sxs-lookup"><span data-stu-id="56213-174">C1</span></span>
- <span data-ttu-id="56213-175">만족할</span><span class="sxs-lookup"><span data-stu-id="56213-175">C2</span></span>
- <span data-ttu-id="56213-176">C3</span><span class="sxs-lookup"><span data-stu-id="56213-176">C3</span></span>
- <span data-ttu-id="56213-177">C4</span><span class="sxs-lookup"><span data-stu-id="56213-177">C4</span></span>
- <span data-ttu-id="56213-178">C 5</span><span class="sxs-lookup"><span data-stu-id="56213-178">C5</span></span>
- <span data-ttu-id="56213-179">C6</span><span class="sxs-lookup"><span data-stu-id="56213-179">C6</span></span>
- <span data-ttu-id="56213-180">250MB</span><span class="sxs-lookup"><span data-stu-id="56213-180">250MB</span></span>
- <span data-ttu-id="56213-181">1GB</span><span class="sxs-lookup"><span data-stu-id="56213-181">1GB</span></span>
- <span data-ttu-id="56213-182">2.5 GB</span><span class="sxs-lookup"><span data-stu-id="56213-182">2.5GB</span></span>
- <span data-ttu-id="56213-183">6GB</span><span class="sxs-lookup"><span data-stu-id="56213-183">6GB</span></span>
- <span data-ttu-id="56213-184">13GB</span><span class="sxs-lookup"><span data-stu-id="56213-184">13GB</span></span>
- <span data-ttu-id="56213-185">26GB</span><span class="sxs-lookup"><span data-stu-id="56213-185">26GB</span></span>
- <span data-ttu-id="56213-186">53GB</span><span class="sxs-lookup"><span data-stu-id="56213-186">53GB</span></span>
- <span data-ttu-id="56213-187">120GB 기본 값은 1GB 또는 C1입니다.</span><span class="sxs-lookup"><span data-stu-id="56213-187">120GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="56213-188">-Sku</span><span class="sxs-lookup"><span data-stu-id="56213-188">-Sku</span></span>
<span data-ttu-id="56213-189">만들 Redis Cache의 SKU를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56213-189">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="56213-190">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="56213-190">Valid values are:</span></span> 
- <span data-ttu-id="56213-191">기본적</span><span class="sxs-lookup"><span data-stu-id="56213-191">Basic</span></span>
- <span data-ttu-id="56213-192">표준이</span><span class="sxs-lookup"><span data-stu-id="56213-192">Standard</span></span>
- <span data-ttu-id="56213-193">Premium 기본 값은 표준입니다.</span><span class="sxs-lookup"><span data-stu-id="56213-193">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="56213-194">태그</span><span class="sxs-lookup"><span data-stu-id="56213-194">-Tag</span></span>
<span data-ttu-id="56213-195">태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="56213-195">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="56213-196">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="56213-196">-TenantSettings</span></span>
<span data-ttu-id="56213-197">이 매개 변수는 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="56213-197">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="56213-198">-확인</span><span class="sxs-lookup"><span data-stu-id="56213-198">-Confirm</span></span>
<span data-ttu-id="56213-199">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="56213-199">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56213-200">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56213-200">-WhatIf</span></span>
<span data-ttu-id="56213-201">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="56213-201">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="56213-202">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="56213-202">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56213-203">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56213-203">CommonParameters</span></span>
<span data-ttu-id="56213-204">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="56213-204">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56213-205">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="56213-205">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56213-206">입력</span><span class="sxs-lookup"><span data-stu-id="56213-206">INPUTS</span></span>

### <span data-ttu-id="56213-207">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="56213-207">System.String</span></span>

### <span data-ttu-id="56213-208">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="56213-208">System.Collections.Hashtable</span></span>

### <span data-ttu-id="56213-209">시스템 Null 허용 ' 1 [[CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="56213-209">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="56213-210">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e])</span><span class="sxs-lookup"><span data-stu-id="56213-210">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="56213-211">출력</span><span class="sxs-lookup"><span data-stu-id="56213-211">OUTPUTS</span></span>

### <span data-ttu-id="56213-212">RedisCacheAttributesWithAccessKeys. 모델. m e.</span><span class="sxs-lookup"><span data-stu-id="56213-212">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="56213-213">상속자</span><span class="sxs-lookup"><span data-stu-id="56213-213">NOTES</span></span>

## <span data-ttu-id="56213-214">관련 링크</span><span class="sxs-lookup"><span data-stu-id="56213-214">RELATED LINKS</span></span>

[<span data-ttu-id="56213-215">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="56213-215">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="56213-216">새로운 AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="56213-216">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="56213-217">제거-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="56213-217">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)


