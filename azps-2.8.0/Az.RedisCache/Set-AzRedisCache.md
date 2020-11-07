---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/set-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Set-AzRedisCache.md
ms.openlocfilehash: aaec1ed3f165338c0aea6bf93e38dfaa8460cdf3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871962"
---
# <span data-ttu-id="2ed8c-101">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="2ed8c-101">Set-AzRedisCache</span></span>

## <span data-ttu-id="2ed8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ed8c-102">SYNOPSIS</span></span>
<span data-ttu-id="2ed8c-103">Redis 캐시를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-103">Modifies a Redis Cache.</span></span>

## <span data-ttu-id="2ed8c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2ed8c-104">SYNTAX</span></span>

```
Set-AzRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2ed8c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2ed8c-105">DESCRIPTION</span></span>
<span data-ttu-id="2ed8c-106">**Set-AzRedisCache** Cmdlet은 Azure Redis Cache를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-106">The **Set-AzRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="2ed8c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2ed8c-107">EXAMPLES</span></span>

### <span data-ttu-id="2ed8c-108">예제 1: Redis 캐시 수정</span><span class="sxs-lookup"><span data-stu-id="2ed8c-108">Example 1: Modify a Redis Cache</span></span>
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

<span data-ttu-id="2ed8c-109">이 명령은 MyCache 라는 Redis Cache에 대 한 maxmemory 정책을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="2ed8c-110">변수</span><span class="sxs-lookup"><span data-stu-id="2ed8c-110">PARAMETERS</span></span>

### <span data-ttu-id="2ed8c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ed8c-111">-DefaultProfile</span></span>
<span data-ttu-id="2ed8c-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2ed8c-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="2ed8c-113">-EnableNonSslPort</span></span>
<span data-ttu-id="2ed8c-114">비 SSL 포트를 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="2ed8c-115">기본값은 $False (비 SSL 포트를 사용할 수 없음)입니다.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-115">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="2ed8c-116">-이름</span><span class="sxs-lookup"><span data-stu-id="2ed8c-116">-Name</span></span>
<span data-ttu-id="2ed8c-117">업데이트할 Redis 캐시의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-117">Specifies the name of the Redis Cache to update.</span></span>

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

### <span data-ttu-id="2ed8c-118">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="2ed8c-118">-RedisConfiguration</span></span>
<span data-ttu-id="2ed8c-119">Redis 구성 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-119">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="2ed8c-120">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2ed8c-121">rdb-백업-사용 가능.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-121">rdb-backup-enabled.</span></span>
<span data-ttu-id="2ed8c-122">Redis 데이터 지 속성을 사용 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-122">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="2ed8c-123">프리미엄 계층만.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-123">Premium tier only.</span></span>
- <span data-ttu-id="2ed8c-124">rdb-저장소-연결 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-124">rdb-storage-connection-string.</span></span>
<span data-ttu-id="2ed8c-125">Redis 데이터 지 속성에 대 한 저장소 계정에 대 한 연결 문자열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-125">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="2ed8c-126">프리미엄 계층만.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-126">Premium tier only.</span></span>
- <span data-ttu-id="2ed8c-127">rdb-백업-빈도</span><span class="sxs-lookup"><span data-stu-id="2ed8c-127">rdb-backup-frequency.</span></span>
<span data-ttu-id="2ed8c-128">Redis 데이터 지 속성에 대 한 백업 빈도를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-128">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="2ed8c-129">프리미엄 계층만.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-129">Premium tier only.</span></span> 
- <span data-ttu-id="2ed8c-130">maxmemory-예약 됨.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-130">maxmemory-reserved.</span></span>
<span data-ttu-id="2ed8c-131">비 캐시 프로세스에 예약 된 메모리를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-131">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="2ed8c-132">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-132">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="2ed8c-133">maxmemory-정책.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-133">maxmemory-policy.</span></span>
<span data-ttu-id="2ed8c-134">캐시에 대 한 제거 정책을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-134">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="2ed8c-135">모든 가격 책정 계층</span><span class="sxs-lookup"><span data-stu-id="2ed8c-135">All pricing tiers.</span></span> 
- <span data-ttu-id="2ed8c-136">notify-keyspace-이벤트</span><span class="sxs-lookup"><span data-stu-id="2ed8c-136">notify-keyspace-events.</span></span>
<span data-ttu-id="2ed8c-137">Keyspace 알림을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-137">Configures keyspace notifications.</span></span>
<span data-ttu-id="2ed8c-138">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-138">Standard and premium tiers.</span></span> 
- <span data-ttu-id="2ed8c-139">hash-최대 ziplist-항목.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-139">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="2ed8c-140">작은 집계 데이터 형식에 대 한 메모리 최적화를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-140">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="2ed8c-141">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-141">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="2ed8c-142">hash-max-ziplist-값.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-142">hash-max-ziplist-value.</span></span>
<span data-ttu-id="2ed8c-143">작은 집계 데이터 형식에 대 한 메모리 최적화를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-143">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="2ed8c-144">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-144">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="2ed8c-145">set-max-intset-항목</span><span class="sxs-lookup"><span data-stu-id="2ed8c-145">set-max-intset-entries.</span></span>
<span data-ttu-id="2ed8c-146">작은 집계 데이터 형식에 대 한 메모리 최적화를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-146">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="2ed8c-147">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-147">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="2ed8c-148">zset-max-ziplist 항목.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-148">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="2ed8c-149">작은 집계 데이터 형식에 대 한 메모리 최적화를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-149">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="2ed8c-150">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-150">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="2ed8c-151">zset-max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-151">zset-max-ziplist-value.</span></span>
<span data-ttu-id="2ed8c-152">작은 집계 데이터 형식에 대 한 메모리 최적화를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-152">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="2ed8c-153">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-153">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="2ed8c-154">databases.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-154">databases.</span></span>
<span data-ttu-id="2ed8c-155">데이터베이스 수를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-155">Configures the number of databases.</span></span>
<span data-ttu-id="2ed8c-156">이 속성은 캐시 생성 시에만 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-156">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="2ed8c-157">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-157">Standard and Premium tiers.</span></span>
<span data-ttu-id="2ed8c-158">자세한 내용은 Azure PowerShell을 사용 하 여 Azure Redis 캐시 관리 https://go.microsoft.com/fwlink/?LinkId=800051 ()를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="2ed8c-158">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="2ed8c-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ed8c-159">-ResourceGroupName</span></span>
<span data-ttu-id="2ed8c-160">Redis 캐시를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-160">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="2ed8c-161">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="2ed8c-161">-ShardCount</span></span>
<span data-ttu-id="2ed8c-162">프리미엄 클러스터 캐시에서 만들 shards 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-162">Specifies the number of shards to create on a Premium cluster cache.</span></span>

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

### <span data-ttu-id="2ed8c-163">-크기</span><span class="sxs-lookup"><span data-stu-id="2ed8c-163">-Size</span></span>
<span data-ttu-id="2ed8c-164">Redis 캐시의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-164">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="2ed8c-165">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-165">Valid values are:</span></span> 
- <span data-ttu-id="2ed8c-166">P1</span><span class="sxs-lookup"><span data-stu-id="2ed8c-166">P1</span></span>
- <span data-ttu-id="2ed8c-167">즉</span><span class="sxs-lookup"><span data-stu-id="2ed8c-167">P2</span></span>
- <span data-ttu-id="2ed8c-168">P3</span><span class="sxs-lookup"><span data-stu-id="2ed8c-168">P3</span></span>
- <span data-ttu-id="2ed8c-169">P4</span><span class="sxs-lookup"><span data-stu-id="2ed8c-169">P4</span></span>
- <span data-ttu-id="2ed8c-170">P5</span><span class="sxs-lookup"><span data-stu-id="2ed8c-170">P5</span></span>
- <span data-ttu-id="2ed8c-171">C0</span><span class="sxs-lookup"><span data-stu-id="2ed8c-171">C0</span></span>
- <span data-ttu-id="2ed8c-172">C1</span><span class="sxs-lookup"><span data-stu-id="2ed8c-172">C1</span></span>
- <span data-ttu-id="2ed8c-173">만족할</span><span class="sxs-lookup"><span data-stu-id="2ed8c-173">C2</span></span>
- <span data-ttu-id="2ed8c-174">C3</span><span class="sxs-lookup"><span data-stu-id="2ed8c-174">C3</span></span>
- <span data-ttu-id="2ed8c-175">C4</span><span class="sxs-lookup"><span data-stu-id="2ed8c-175">C4</span></span>
- <span data-ttu-id="2ed8c-176">C 5</span><span class="sxs-lookup"><span data-stu-id="2ed8c-176">C5</span></span>
- <span data-ttu-id="2ed8c-177">C6</span><span class="sxs-lookup"><span data-stu-id="2ed8c-177">C6</span></span>
- <span data-ttu-id="2ed8c-178">250MB</span><span class="sxs-lookup"><span data-stu-id="2ed8c-178">250MB</span></span>
- <span data-ttu-id="2ed8c-179">1GB</span><span class="sxs-lookup"><span data-stu-id="2ed8c-179">1GB</span></span>
- <span data-ttu-id="2ed8c-180">2.5 GB</span><span class="sxs-lookup"><span data-stu-id="2ed8c-180">2.5GB</span></span>
- <span data-ttu-id="2ed8c-181">6GB</span><span class="sxs-lookup"><span data-stu-id="2ed8c-181">6GB</span></span>
- <span data-ttu-id="2ed8c-182">13GB</span><span class="sxs-lookup"><span data-stu-id="2ed8c-182">13GB</span></span>
- <span data-ttu-id="2ed8c-183">26GB</span><span class="sxs-lookup"><span data-stu-id="2ed8c-183">26GB</span></span>
- <span data-ttu-id="2ed8c-184">53GB</span><span class="sxs-lookup"><span data-stu-id="2ed8c-184">53GB</span></span>
- <span data-ttu-id="2ed8c-185">120GB 기본 값은 1GB 또는 C1입니다.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-185">120GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="2ed8c-186">-Sku</span><span class="sxs-lookup"><span data-stu-id="2ed8c-186">-Sku</span></span>
<span data-ttu-id="2ed8c-187">만들 Redis Cache의 SKU를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-187">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="2ed8c-188">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-188">Valid values are:</span></span> 
- <span data-ttu-id="2ed8c-189">기본적</span><span class="sxs-lookup"><span data-stu-id="2ed8c-189">Basic</span></span>
- <span data-ttu-id="2ed8c-190">표준이</span><span class="sxs-lookup"><span data-stu-id="2ed8c-190">Standard</span></span>
- <span data-ttu-id="2ed8c-191">Premium 기본 값은 표준입니다.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-191">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="2ed8c-192">태그</span><span class="sxs-lookup"><span data-stu-id="2ed8c-192">-Tag</span></span>
<span data-ttu-id="2ed8c-193">태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-193">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="2ed8c-194">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="2ed8c-194">-TenantSettings</span></span>
<span data-ttu-id="2ed8c-195">이 매개 변수는 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-195">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="2ed8c-196">-확인</span><span class="sxs-lookup"><span data-stu-id="2ed8c-196">-Confirm</span></span>
<span data-ttu-id="2ed8c-197">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-197">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ed8c-198">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ed8c-198">-WhatIf</span></span>
<span data-ttu-id="2ed8c-199">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-199">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2ed8c-200">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-200">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ed8c-201">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ed8c-201">CommonParameters</span></span>
<span data-ttu-id="2ed8c-202">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-202">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ed8c-203">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ed8c-203">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ed8c-204">입력</span><span class="sxs-lookup"><span data-stu-id="2ed8c-204">INPUTS</span></span>

### <span data-ttu-id="2ed8c-205">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2ed8c-205">System.String</span></span>

### <span data-ttu-id="2ed8c-206">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="2ed8c-206">System.Collections.Hashtable</span></span>

### <span data-ttu-id="2ed8c-207">시스템 Null 허용 ' 1 [[CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2ed8c-207">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="2ed8c-208">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e])</span><span class="sxs-lookup"><span data-stu-id="2ed8c-208">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="2ed8c-209">출력</span><span class="sxs-lookup"><span data-stu-id="2ed8c-209">OUTPUTS</span></span>

### <span data-ttu-id="2ed8c-210">RedisCacheAttributesWithAccessKeys. 모델. m e.</span><span class="sxs-lookup"><span data-stu-id="2ed8c-210">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="2ed8c-211">상속자</span><span class="sxs-lookup"><span data-stu-id="2ed8c-211">NOTES</span></span>

## <span data-ttu-id="2ed8c-212">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2ed8c-212">RELATED LINKS</span></span>

[<span data-ttu-id="2ed8c-213">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="2ed8c-213">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="2ed8c-214">새로운 AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="2ed8c-214">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="2ed8c-215">제거-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="2ed8c-215">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)


