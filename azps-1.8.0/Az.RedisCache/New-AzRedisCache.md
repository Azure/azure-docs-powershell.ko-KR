---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
ms.openlocfilehash: ab0b84578339568e48458de8a89daccd83092e65
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699547"
---
# <span data-ttu-id="ad4fa-101">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="ad4fa-101">New-AzRedisCache</span></span>

## <span data-ttu-id="ad4fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad4fa-102">SYNOPSIS</span></span>
<span data-ttu-id="ad4fa-103">Redis 캐시를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-103">Creates a Redis Cache.</span></span>

## <span data-ttu-id="ad4fa-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ad4fa-104">SYNTAX</span></span>

```
New-AzRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-SubnetId <String>] [-StaticIP <String>] [-Tag <Hashtable>] [-Zone <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad4fa-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ad4fa-105">DESCRIPTION</span></span>
<span data-ttu-id="ad4fa-106">**AzRedisCache** Cmdlet은 Azure Redis Cache를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-106">The **New-AzRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="ad4fa-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ad4fa-107">EXAMPLES</span></span>

### <span data-ttu-id="ad4fa-108">예제 1: Redis 캐시 만들기</span><span class="sxs-lookup"><span data-stu-id="ad4fa-108">Example 1: Create a Redis Cache</span></span>
```
PS C:\>New-AzRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US"

          PrimaryKey         : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          SecondaryKey       : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          ResourceGroupName  : MyGroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/mygroup/providers/Microsoft.Cache/Redis/mycache
          Location           : North Central US
          Name               : MyCache
          Type               : Microsoft.Cache/Redis
          HostName           : mycache.redis.cache.windows.net 
          Port               : 6379
          ProvisioningState  : creating
          SslPort            : 6380
          RedisConfiguration : {}
          EnableNonSslPort   : False
          RedisVersion       : 2.8
          Size               : 1GB
          Sku                : Standard
          Tag                : {}
          Zone               : []
```

<span data-ttu-id="ad4fa-109">이 명령은 Redis Cache를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="ad4fa-110">예제 2: 표준 SKU Redis 캐시 만들기</span><span class="sxs-lookup"><span data-stu-id="ad4fa-110">Example 2: Create a Standard SKU Redis Cache</span></span>
```
PS C:\>New-AzRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US" -Size 250MB -Sku "Standard" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"} -Force

          PrimaryKey         : pJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          SecondaryKey       : sJ+jruGKPHDKsEC8kmoybobH3TZx2njBR3ipEsquZFo=
          ResourceGroupName  : MyGroup
          Id                 : /subscriptions/a559b6fd-3a84-40bb-a450-b0db5ed37dfe/resourceGroups/mygroup/providers/Microsoft.Cache/Redis/MyCache
          Location           : North Central US
          Name               : mycache
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

<span data-ttu-id="ad4fa-111">이 명령은 Redis Cache를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-111">This command creates a Redis Cache.</span></span>

## <span data-ttu-id="ad4fa-112">변수</span><span class="sxs-lookup"><span data-stu-id="ad4fa-112">PARAMETERS</span></span>

### <span data-ttu-id="ad4fa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad4fa-113">-DefaultProfile</span></span>
<span data-ttu-id="ad4fa-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad4fa-115">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="ad4fa-115">-EnableNonSslPort</span></span>
<span data-ttu-id="ad4fa-116">비 SSL 포트를 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-116">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="ad4fa-117">기본값은 $False (비 SSL 포트를 사용할 수 없음)입니다.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-117">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="ad4fa-118">-위치</span><span class="sxs-lookup"><span data-stu-id="ad4fa-118">-Location</span></span>
<span data-ttu-id="ad4fa-119">Redis 캐시를 만들 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-119">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="ad4fa-120">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-120">Valid values are:</span></span> 
- <span data-ttu-id="ad4fa-121">대한민국 미국 중부</span><span class="sxs-lookup"><span data-stu-id="ad4fa-121">North Central US</span></span>
- <span data-ttu-id="ad4fa-122">미국 중부 US</span><span class="sxs-lookup"><span data-stu-id="ad4fa-122">South Central US</span></span>
- <span data-ttu-id="ad4fa-123">중부 US</span><span class="sxs-lookup"><span data-stu-id="ad4fa-123">Central US</span></span>
- <span data-ttu-id="ad4fa-124">유럽 서유럽</span><span class="sxs-lookup"><span data-stu-id="ad4fa-124">West Europe</span></span>
- <span data-ttu-id="ad4fa-125">동유럽</span><span class="sxs-lookup"><span data-stu-id="ad4fa-125">North Europe</span></span>
- <span data-ttu-id="ad4fa-126">미국 서 부</span><span class="sxs-lookup"><span data-stu-id="ad4fa-126">West US</span></span>
- <span data-ttu-id="ad4fa-127">미국 동부</span><span class="sxs-lookup"><span data-stu-id="ad4fa-127">East US</span></span>
- <span data-ttu-id="ad4fa-128">미국 동부 2</span><span class="sxs-lookup"><span data-stu-id="ad4fa-128">East US 2</span></span>
- <span data-ttu-id="ad4fa-129">일본 동부</span><span class="sxs-lookup"><span data-stu-id="ad4fa-129">Japan East</span></span>
- <span data-ttu-id="ad4fa-130">일본 서쪽</span><span class="sxs-lookup"><span data-stu-id="ad4fa-130">Japan West</span></span>
- <span data-ttu-id="ad4fa-131">브라질 남부</span><span class="sxs-lookup"><span data-stu-id="ad4fa-131">Brazil South</span></span>
- <span data-ttu-id="ad4fa-132">동남 아시아</span><span class="sxs-lookup"><span data-stu-id="ad4fa-132">Southeast Asia</span></span>
- <span data-ttu-id="ad4fa-133">동아시아</span><span class="sxs-lookup"><span data-stu-id="ad4fa-133">East Asia</span></span>
- <span data-ttu-id="ad4fa-134">오스트레일리아 동부</span><span class="sxs-lookup"><span data-stu-id="ad4fa-134">Australia East</span></span>
- <span data-ttu-id="ad4fa-135">오스트레일리아 남동쪽</span><span class="sxs-lookup"><span data-stu-id="ad4fa-135">Australia Southeast</span></span>

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

### <span data-ttu-id="ad4fa-136">-이름</span><span class="sxs-lookup"><span data-stu-id="ad4fa-136">-Name</span></span>
<span data-ttu-id="ad4fa-137">만들 Redis 캐시의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-137">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="ad4fa-138">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="ad4fa-138">-RedisConfiguration</span></span>
<span data-ttu-id="ad4fa-139">Redis 구성 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-139">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="ad4fa-140">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-140">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ad4fa-141">rdb-백업-사용 가능.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-141">rdb-backup-enabled.</span></span>
<span data-ttu-id="ad4fa-142">Redis 데이터 지 속성을 사용 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-142">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="ad4fa-143">프리미엄 계층만.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-143">Premium tier only.</span></span>
- <span data-ttu-id="ad4fa-144">rdb-저장소-연결 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-144">rdb-storage-connection-string.</span></span>
<span data-ttu-id="ad4fa-145">Redis 데이터 지 속성에 대 한 저장소 계정에 대 한 연결 문자열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-145">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="ad4fa-146">프리미엄 계층만.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-146">Premium tier only.</span></span>
- <span data-ttu-id="ad4fa-147">rdb-백업-빈도</span><span class="sxs-lookup"><span data-stu-id="ad4fa-147">rdb-backup-frequency.</span></span>
<span data-ttu-id="ad4fa-148">Redis 데이터 지 속성에 대 한 백업 빈도를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-148">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="ad4fa-149">프리미엄 계층만.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-149">Premium tier only.</span></span> 
- <span data-ttu-id="ad4fa-150">maxmemory-예약 됨.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-150">maxmemory-reserved.</span></span>
<span data-ttu-id="ad4fa-151">비 캐시 프로세스에 예약 된 메모리를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-151">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="ad4fa-152">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-152">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="ad4fa-153">maxmemory-정책.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-153">maxmemory-policy.</span></span>
<span data-ttu-id="ad4fa-154">캐시에 대 한 제거 정책을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-154">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="ad4fa-155">모든 가격 책정 계층</span><span class="sxs-lookup"><span data-stu-id="ad4fa-155">All pricing tiers.</span></span> 
- <span data-ttu-id="ad4fa-156">notify-keyspace-이벤트</span><span class="sxs-lookup"><span data-stu-id="ad4fa-156">notify-keyspace-events.</span></span>
<span data-ttu-id="ad4fa-157">Keyspace 알림을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-157">Configures keyspace notifications.</span></span>
<span data-ttu-id="ad4fa-158">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-158">Standard and premium tiers.</span></span> 
- <span data-ttu-id="ad4fa-159">hash-최대 ziplist-항목.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-159">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="ad4fa-160">작은 집계 데이터 형식에 대 한 메모리 최적화를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-160">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="ad4fa-161">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-161">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="ad4fa-162">hash-max-ziplist-값.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-162">hash-max-ziplist-value.</span></span>
<span data-ttu-id="ad4fa-163">작은 집계 데이터 형식에 대 한 메모리 최적화를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-163">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="ad4fa-164">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-164">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="ad4fa-165">set-max-intset-항목</span><span class="sxs-lookup"><span data-stu-id="ad4fa-165">set-max-intset-entries.</span></span>
<span data-ttu-id="ad4fa-166">작은 집계 데이터 형식에 대 한 메모리 최적화를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-166">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="ad4fa-167">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-167">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="ad4fa-168">zset-max-ziplist 항목.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-168">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="ad4fa-169">작은 집계 데이터 형식에 대 한 메모리 최적화를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-169">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="ad4fa-170">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-170">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="ad4fa-171">zset-max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-171">zset-max-ziplist-value.</span></span>
<span data-ttu-id="ad4fa-172">작은 집계 데이터 형식에 대 한 메모리 최적화를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-172">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="ad4fa-173">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-173">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="ad4fa-174">databases.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-174">databases.</span></span>
<span data-ttu-id="ad4fa-175">데이터베이스 수를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-175">Configures the number of databases.</span></span>
<span data-ttu-id="ad4fa-176">이 속성은 캐시 생성 시에만 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-176">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="ad4fa-177">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-177">Standard and Premium tiers.</span></span>
<span data-ttu-id="ad4fa-178">자세한 내용은 Azure PowerShell을 사용 하 여 Azure Redis 캐시 관리 https://go.microsoft.com/fwlink/?LinkId=800051 ()를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="ad4fa-178">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="ad4fa-179">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad4fa-179">-ResourceGroupName</span></span>
<span data-ttu-id="ad4fa-180">Redis 캐시를 만들 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-180">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="ad4fa-181">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="ad4fa-181">-ShardCount</span></span>
<span data-ttu-id="ad4fa-182">프리미엄 클러스터 캐시에서 만들 shards 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-182">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="ad4fa-183">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-183">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ad4fa-184">raid-1</span><span class="sxs-lookup"><span data-stu-id="ad4fa-184">1</span></span>
- <span data-ttu-id="ad4fa-185">2</span><span class="sxs-lookup"><span data-stu-id="ad4fa-185">2</span></span>
- <span data-ttu-id="ad4fa-186">3-4</span><span class="sxs-lookup"><span data-stu-id="ad4fa-186">3</span></span>
- <span data-ttu-id="ad4fa-187">4(tcp/ipv4)</span><span class="sxs-lookup"><span data-stu-id="ad4fa-187">4</span></span>
- <span data-ttu-id="ad4fa-188">5mb</span><span class="sxs-lookup"><span data-stu-id="ad4fa-188">5</span></span>
- <span data-ttu-id="ad4fa-189">26</span><span class="sxs-lookup"><span data-stu-id="ad4fa-189">6</span></span>
- <span data-ttu-id="ad4fa-190">7</span><span class="sxs-lookup"><span data-stu-id="ad4fa-190">7</span></span>
- <span data-ttu-id="ad4fa-191">20cm(8</span><span class="sxs-lookup"><span data-stu-id="ad4fa-191">8</span></span>
- <span data-ttu-id="ad4fa-192">되었는지</span><span class="sxs-lookup"><span data-stu-id="ad4fa-192">9</span></span> 
- <span data-ttu-id="ad4fa-193">1천만</span><span class="sxs-lookup"><span data-stu-id="ad4fa-193">10</span></span>

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

### <span data-ttu-id="ad4fa-194">-크기</span><span class="sxs-lookup"><span data-stu-id="ad4fa-194">-Size</span></span>
<span data-ttu-id="ad4fa-195">Redis 캐시의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-195">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="ad4fa-196">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-196">Valid values are:</span></span> 
- <span data-ttu-id="ad4fa-197">P1</span><span class="sxs-lookup"><span data-stu-id="ad4fa-197">P1</span></span>
- <span data-ttu-id="ad4fa-198">즉</span><span class="sxs-lookup"><span data-stu-id="ad4fa-198">P2</span></span>
- <span data-ttu-id="ad4fa-199">P3</span><span class="sxs-lookup"><span data-stu-id="ad4fa-199">P3</span></span>
- <span data-ttu-id="ad4fa-200">P4</span><span class="sxs-lookup"><span data-stu-id="ad4fa-200">P4</span></span>
- <span data-ttu-id="ad4fa-201">C0</span><span class="sxs-lookup"><span data-stu-id="ad4fa-201">C0</span></span>
- <span data-ttu-id="ad4fa-202">C1</span><span class="sxs-lookup"><span data-stu-id="ad4fa-202">C1</span></span>
- <span data-ttu-id="ad4fa-203">만족할</span><span class="sxs-lookup"><span data-stu-id="ad4fa-203">C2</span></span>
- <span data-ttu-id="ad4fa-204">C3</span><span class="sxs-lookup"><span data-stu-id="ad4fa-204">C3</span></span>
- <span data-ttu-id="ad4fa-205">C4</span><span class="sxs-lookup"><span data-stu-id="ad4fa-205">C4</span></span>
- <span data-ttu-id="ad4fa-206">C 5</span><span class="sxs-lookup"><span data-stu-id="ad4fa-206">C5</span></span>
- <span data-ttu-id="ad4fa-207">C6</span><span class="sxs-lookup"><span data-stu-id="ad4fa-207">C6</span></span>
- <span data-ttu-id="ad4fa-208">250MB</span><span class="sxs-lookup"><span data-stu-id="ad4fa-208">250MB</span></span>
- <span data-ttu-id="ad4fa-209">1GB</span><span class="sxs-lookup"><span data-stu-id="ad4fa-209">1GB</span></span>
- <span data-ttu-id="ad4fa-210">2.5 GB</span><span class="sxs-lookup"><span data-stu-id="ad4fa-210">2.5GB</span></span>
- <span data-ttu-id="ad4fa-211">6GB</span><span class="sxs-lookup"><span data-stu-id="ad4fa-211">6GB</span></span>
- <span data-ttu-id="ad4fa-212">13GB</span><span class="sxs-lookup"><span data-stu-id="ad4fa-212">13GB</span></span>
- <span data-ttu-id="ad4fa-213">26GB</span><span class="sxs-lookup"><span data-stu-id="ad4fa-213">26GB</span></span>
- <span data-ttu-id="ad4fa-214">53GB 기본 값은 1GB 또는 C1입니다.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-214">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="ad4fa-215">-Sku</span><span class="sxs-lookup"><span data-stu-id="ad4fa-215">-Sku</span></span>
<span data-ttu-id="ad4fa-216">만들 Redis Cache의 SKU를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-216">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="ad4fa-217">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-217">Valid values are:</span></span> 
- <span data-ttu-id="ad4fa-218">기본적</span><span class="sxs-lookup"><span data-stu-id="ad4fa-218">Basic</span></span>
- <span data-ttu-id="ad4fa-219">표준이</span><span class="sxs-lookup"><span data-stu-id="ad4fa-219">Standard</span></span>
- <span data-ttu-id="ad4fa-220">Premium 기본 값은 표준입니다.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-220">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="ad4fa-221">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="ad4fa-221">-StaticIP</span></span>
<span data-ttu-id="ad4fa-222">Redis 캐시에 대 한 서브넷의 고유한 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-222">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>
<span data-ttu-id="ad4fa-223">이 매개 변수에 대 한 값을 지정 하지 않으면이 cmdlet은 서브넷에서 IP 주소를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-223">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="ad4fa-224">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="ad4fa-224">-SubnetId</span></span>
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

### <span data-ttu-id="ad4fa-225">태그</span><span class="sxs-lookup"><span data-stu-id="ad4fa-225">-Tag</span></span>
<span data-ttu-id="ad4fa-226">태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-226">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="ad4fa-227">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="ad4fa-227">-TenantSettings</span></span>
<span data-ttu-id="ad4fa-228">이 매개 변수는 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-228">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="ad4fa-229">-Zone</span><span class="sxs-lookup"><span data-stu-id="ad4fa-229">-Zone</span></span>
<span data-ttu-id="ad4fa-230">영역 목록.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-230">List of zones.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad4fa-231">-확인</span><span class="sxs-lookup"><span data-stu-id="ad4fa-231">-Confirm</span></span>
<span data-ttu-id="ad4fa-232">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-232">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad4fa-233">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad4fa-233">-WhatIf</span></span>
<span data-ttu-id="ad4fa-234">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-234">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ad4fa-235">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-235">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad4fa-236">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad4fa-236">CommonParameters</span></span>
<span data-ttu-id="ad4fa-237">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-237">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad4fa-238">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad4fa-238">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad4fa-239">입력</span><span class="sxs-lookup"><span data-stu-id="ad4fa-239">INPUTS</span></span>

### <span data-ttu-id="ad4fa-240">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ad4fa-240">System.String</span></span>

### <span data-ttu-id="ad4fa-241">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="ad4fa-241">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ad4fa-242">시스템 Null 허용 ' 1 [[CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ad4fa-242">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ad4fa-243">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e])</span><span class="sxs-lookup"><span data-stu-id="ad4fa-243">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ad4fa-244">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="ad4fa-244">System.String[]</span></span>

## <span data-ttu-id="ad4fa-245">출력</span><span class="sxs-lookup"><span data-stu-id="ad4fa-245">OUTPUTS</span></span>

### <span data-ttu-id="ad4fa-246">RedisCacheAttributesWithAccessKeys. 모델. m e.</span><span class="sxs-lookup"><span data-stu-id="ad4fa-246">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="ad4fa-247">상속자</span><span class="sxs-lookup"><span data-stu-id="ad4fa-247">NOTES</span></span>

## <span data-ttu-id="ad4fa-248">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ad4fa-248">RELATED LINKS</span></span>

[<span data-ttu-id="ad4fa-249">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="ad4fa-249">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="ad4fa-250">제거-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="ad4fa-250">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="ad4fa-251">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="ad4fa-251">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


