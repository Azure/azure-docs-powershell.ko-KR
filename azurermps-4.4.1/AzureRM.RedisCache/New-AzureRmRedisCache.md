---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
ms.openlocfilehash: 493a8e7a4e356284b2ae14241715a7631d99839c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702420"
---
# <span data-ttu-id="006ac-101">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="006ac-101">New-AzureRmRedisCache</span></span>

## <span data-ttu-id="006ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="006ac-102">SYNOPSIS</span></span>
<span data-ttu-id="006ac-103">Redis 캐시를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="006ac-103">Creates a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="006ac-104">구문과</span><span class="sxs-lookup"><span data-stu-id="006ac-104">SYNTAX</span></span>

```
New-AzureRmRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-RedisVersion <String>]
 [-Size <String>] [-Sku <String>] [-MaxMemoryPolicy <String>] [-RedisConfiguration <Hashtable>]
 [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>] [-ShardCount <Int32>] [-VirtualNetwork <String>]
 [-Subnet <String>] [-SubnetId <String>] [-StaticIP <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="006ac-105">설명은</span><span class="sxs-lookup"><span data-stu-id="006ac-105">DESCRIPTION</span></span>
<span data-ttu-id="006ac-106">**AzureRmRedisCache** Cmdlet은 Azure Redis Cache를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="006ac-106">The **New-AzureRmRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="006ac-107">예제의</span><span class="sxs-lookup"><span data-stu-id="006ac-107">EXAMPLES</span></span>

### <span data-ttu-id="006ac-108">예제 1: Redis 캐시 만들기</span><span class="sxs-lookup"><span data-stu-id="006ac-108">Example 1: Create a Redis Cache</span></span>
```
PS C:\>New-AzureRmRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US"


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
```

<span data-ttu-id="006ac-109">이 명령은 Redis Cache를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="006ac-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="006ac-110">예제 2: 표준 SKU Redis 캐시 만들기</span><span class="sxs-lookup"><span data-stu-id="006ac-110">Example 2: Create a Standard SKU Redis Cache</span></span>
```
PS C:\>New-AzureRmRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -Location "North Central US" -Size 250MB -Sku "Standard" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"} -Force


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
```

<span data-ttu-id="006ac-111">이 명령은 Redis 캐시를 만들거나 Redis Cache (이미 있는 경우)를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="006ac-111">This command creates a Redis Cache or updates the Redis Cache if it already exists.</span></span>

## <span data-ttu-id="006ac-112">변수</span><span class="sxs-lookup"><span data-stu-id="006ac-112">PARAMETERS</span></span>

### <span data-ttu-id="006ac-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="006ac-113">-EnableNonSslPort</span></span>
<span data-ttu-id="006ac-114">비 SSL 포트를 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="006ac-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="006ac-115">기본값은 $False (비 SSL 포트를 사용할 수 없음)입니다.</span><span class="sxs-lookup"><span data-stu-id="006ac-115">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="006ac-116">-위치</span><span class="sxs-lookup"><span data-stu-id="006ac-116">-Location</span></span>
<span data-ttu-id="006ac-117">Redis 캐시를 만들 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="006ac-117">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="006ac-118">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="006ac-118">Valid values are:</span></span> 

- <span data-ttu-id="006ac-119">대한민국 미국 중부</span><span class="sxs-lookup"><span data-stu-id="006ac-119">North Central US</span></span>
- <span data-ttu-id="006ac-120">미국 중부 US</span><span class="sxs-lookup"><span data-stu-id="006ac-120">South Central US</span></span>
- <span data-ttu-id="006ac-121">중부 US</span><span class="sxs-lookup"><span data-stu-id="006ac-121">Central US</span></span>
- <span data-ttu-id="006ac-122">유럽 서유럽</span><span class="sxs-lookup"><span data-stu-id="006ac-122">West Europe</span></span>
- <span data-ttu-id="006ac-123">동유럽</span><span class="sxs-lookup"><span data-stu-id="006ac-123">North Europe</span></span>
- <span data-ttu-id="006ac-124">미국 서 부</span><span class="sxs-lookup"><span data-stu-id="006ac-124">West US</span></span>
- <span data-ttu-id="006ac-125">미국 동부</span><span class="sxs-lookup"><span data-stu-id="006ac-125">East US</span></span>
- <span data-ttu-id="006ac-126">미국 동부 2</span><span class="sxs-lookup"><span data-stu-id="006ac-126">East US 2</span></span>
- <span data-ttu-id="006ac-127">일본 동부</span><span class="sxs-lookup"><span data-stu-id="006ac-127">Japan East</span></span>
- <span data-ttu-id="006ac-128">일본 서쪽</span><span class="sxs-lookup"><span data-stu-id="006ac-128">Japan West</span></span>
- <span data-ttu-id="006ac-129">브라질 남부</span><span class="sxs-lookup"><span data-stu-id="006ac-129">Brazil South</span></span>
- <span data-ttu-id="006ac-130">동남 아시아</span><span class="sxs-lookup"><span data-stu-id="006ac-130">Southeast Asia</span></span>
- <span data-ttu-id="006ac-131">동아시아</span><span class="sxs-lookup"><span data-stu-id="006ac-131">East Asia</span></span>
- <span data-ttu-id="006ac-132">오스트레일리아 동부</span><span class="sxs-lookup"><span data-stu-id="006ac-132">Australia East</span></span>
- <span data-ttu-id="006ac-133">오스트레일리아 남동쪽</span><span class="sxs-lookup"><span data-stu-id="006ac-133">Australia Southeast</span></span>

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

### <span data-ttu-id="006ac-134">-MaxMemoryPolicy</span><span class="sxs-lookup"><span data-stu-id="006ac-134">-MaxMemoryPolicy</span></span>
<span data-ttu-id="006ac-135">이 매개 변수는 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="006ac-135">This parameter has been deprecated.</span></span>
<span data-ttu-id="006ac-136">*Redisconfiguration* 매개 변수를 사용 하 여 maxmemory-정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="006ac-136">Use the *RedisConfiguration* parameter to set maxmemory-policy.</span></span>
<span data-ttu-id="006ac-137">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="006ac-137">For example:</span></span> 

`-RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}`

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

### <span data-ttu-id="006ac-138">-이름</span><span class="sxs-lookup"><span data-stu-id="006ac-138">-Name</span></span>
<span data-ttu-id="006ac-139">만들 Redis 캐시의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="006ac-139">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="006ac-140">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="006ac-140">-RedisConfiguration</span></span>
<span data-ttu-id="006ac-141">Redis 구성 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="006ac-141">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="006ac-142">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="006ac-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="006ac-143">rdb-백업-사용 가능.</span><span class="sxs-lookup"><span data-stu-id="006ac-143">rdb-backup-enabled.</span></span>
<span data-ttu-id="006ac-144">Redis 데이터 지 속성을 사용 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="006ac-144">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="006ac-145">프리미엄 계층만.</span><span class="sxs-lookup"><span data-stu-id="006ac-145">Premium tier only.</span></span>
- <span data-ttu-id="006ac-146">rdb-저장소-연결 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="006ac-146">rdb-storage-connection-string.</span></span>
<span data-ttu-id="006ac-147">Redis 데이터 지 속성에 대 한 저장소 계정에 대 한 연결 문자열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="006ac-147">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="006ac-148">프리미엄 계층만.</span><span class="sxs-lookup"><span data-stu-id="006ac-148">Premium tier only.</span></span>
- <span data-ttu-id="006ac-149">rdb-백업-빈도</span><span class="sxs-lookup"><span data-stu-id="006ac-149">rdb-backup-frequency.</span></span>
<span data-ttu-id="006ac-150">Redis 데이터 지 속성에 대 한 백업 빈도를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="006ac-150">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="006ac-151">프리미엄 계층만.</span><span class="sxs-lookup"><span data-stu-id="006ac-151">Premium tier only.</span></span> 
- <span data-ttu-id="006ac-152">maxmemory-예약 됨.</span><span class="sxs-lookup"><span data-stu-id="006ac-152">maxmemory-reserved.</span></span>
<span data-ttu-id="006ac-153">비 캐시 프로세스에 예약 된 메모리를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="006ac-153">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="006ac-154">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="006ac-154">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="006ac-155">maxmemory-정책.</span><span class="sxs-lookup"><span data-stu-id="006ac-155">maxmemory-policy.</span></span>
<span data-ttu-id="006ac-156">캐시에 대 한 제거 정책을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="006ac-156">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="006ac-157">모든 가격 책정 계층</span><span class="sxs-lookup"><span data-stu-id="006ac-157">All pricing tiers.</span></span> 
- <span data-ttu-id="006ac-158">notify-keyspace-이벤트</span><span class="sxs-lookup"><span data-stu-id="006ac-158">notify-keyspace-events.</span></span>
<span data-ttu-id="006ac-159">Keyspace 알림을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="006ac-159">Configures keyspace notifications.</span></span>
<span data-ttu-id="006ac-160">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="006ac-160">Standard and premium tiers.</span></span> 
- <span data-ttu-id="006ac-161">hash-최대 ziplist-항목.</span><span class="sxs-lookup"><span data-stu-id="006ac-161">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="006ac-162">작은 집계 데이터 형식에 대 한 메모리 최적화를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="006ac-162">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="006ac-163">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="006ac-163">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="006ac-164">hash-max-ziplist-값.</span><span class="sxs-lookup"><span data-stu-id="006ac-164">hash-max-ziplist-value.</span></span>
<span data-ttu-id="006ac-165">작은 집계 데이터 형식에 대 한 메모리 최적화를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="006ac-165">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="006ac-166">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="006ac-166">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="006ac-167">set-max-intset-항목</span><span class="sxs-lookup"><span data-stu-id="006ac-167">set-max-intset-entries.</span></span>
<span data-ttu-id="006ac-168">작은 집계 데이터 형식에 대 한 메모리 최적화를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="006ac-168">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="006ac-169">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="006ac-169">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="006ac-170">zset-max-ziplist 항목.</span><span class="sxs-lookup"><span data-stu-id="006ac-170">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="006ac-171">작은 집계 데이터 형식에 대 한 메모리 최적화를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="006ac-171">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="006ac-172">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="006ac-172">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="006ac-173">zset-max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="006ac-173">zset-max-ziplist-value.</span></span>
<span data-ttu-id="006ac-174">작은 집계 데이터 형식에 대 한 메모리 최적화를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="006ac-174">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="006ac-175">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="006ac-175">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="006ac-176">databases.</span><span class="sxs-lookup"><span data-stu-id="006ac-176">databases.</span></span>
<span data-ttu-id="006ac-177">데이터베이스 수를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="006ac-177">Configures the number of databases.</span></span>
<span data-ttu-id="006ac-178">이 속성은 캐시 생성 시에만 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="006ac-178">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="006ac-179">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="006ac-179">Standard and Premium tiers.</span></span>

<span data-ttu-id="006ac-180">자세한 내용은 Azure PowerShell을 사용 하 여 Azure Redis 캐시 관리 https://go.microsoft.com/fwlink/?LinkId=800051 ()를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="006ac-180">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="006ac-181">-버전 재</span><span class="sxs-lookup"><span data-stu-id="006ac-181">-RedisVersion</span></span>
<span data-ttu-id="006ac-182">이 매개 변수는 더 이상 사용 되지 않으며 이후 릴리스에서 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="006ac-182">This parameter is deprecated and will be removed from future releases.</span></span>

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

### <span data-ttu-id="006ac-183">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="006ac-183">-ResourceGroupName</span></span>
<span data-ttu-id="006ac-184">Redis 캐시를 만들 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="006ac-184">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="006ac-185">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="006ac-185">-ShardCount</span></span>
<span data-ttu-id="006ac-186">프리미엄 클러스터 캐시에서 만들 shards 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="006ac-186">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="006ac-187">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="006ac-187">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="006ac-188">raid-1</span><span class="sxs-lookup"><span data-stu-id="006ac-188">1</span></span>
- <span data-ttu-id="006ac-189">2</span><span class="sxs-lookup"><span data-stu-id="006ac-189">2</span></span>
- <span data-ttu-id="006ac-190">3-4</span><span class="sxs-lookup"><span data-stu-id="006ac-190">3</span></span>
- <span data-ttu-id="006ac-191">4(tcp/ipv4)</span><span class="sxs-lookup"><span data-stu-id="006ac-191">4</span></span>
- <span data-ttu-id="006ac-192">5mb</span><span class="sxs-lookup"><span data-stu-id="006ac-192">5</span></span>
- <span data-ttu-id="006ac-193">26</span><span class="sxs-lookup"><span data-stu-id="006ac-193">6</span></span>
- <span data-ttu-id="006ac-194">7</span><span class="sxs-lookup"><span data-stu-id="006ac-194">7</span></span>
- <span data-ttu-id="006ac-195">20cm(8</span><span class="sxs-lookup"><span data-stu-id="006ac-195">8</span></span>
- <span data-ttu-id="006ac-196">되었는지</span><span class="sxs-lookup"><span data-stu-id="006ac-196">9</span></span> 
- <span data-ttu-id="006ac-197">1천만</span><span class="sxs-lookup"><span data-stu-id="006ac-197">10</span></span>

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

### <span data-ttu-id="006ac-198">-크기</span><span class="sxs-lookup"><span data-stu-id="006ac-198">-Size</span></span>
<span data-ttu-id="006ac-199">Redis 캐시의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="006ac-199">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="006ac-200">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="006ac-200">Valid values are:</span></span> 

- <span data-ttu-id="006ac-201">P1</span><span class="sxs-lookup"><span data-stu-id="006ac-201">P1</span></span>
- <span data-ttu-id="006ac-202">즉</span><span class="sxs-lookup"><span data-stu-id="006ac-202">P2</span></span>
- <span data-ttu-id="006ac-203">P3</span><span class="sxs-lookup"><span data-stu-id="006ac-203">P3</span></span>
- <span data-ttu-id="006ac-204">P4</span><span class="sxs-lookup"><span data-stu-id="006ac-204">P4</span></span>
- <span data-ttu-id="006ac-205">C0</span><span class="sxs-lookup"><span data-stu-id="006ac-205">C0</span></span>
- <span data-ttu-id="006ac-206">C1</span><span class="sxs-lookup"><span data-stu-id="006ac-206">C1</span></span>
- <span data-ttu-id="006ac-207">만족할</span><span class="sxs-lookup"><span data-stu-id="006ac-207">C2</span></span>
- <span data-ttu-id="006ac-208">C3</span><span class="sxs-lookup"><span data-stu-id="006ac-208">C3</span></span>
- <span data-ttu-id="006ac-209">C4</span><span class="sxs-lookup"><span data-stu-id="006ac-209">C4</span></span>
- <span data-ttu-id="006ac-210">C 5</span><span class="sxs-lookup"><span data-stu-id="006ac-210">C5</span></span>
- <span data-ttu-id="006ac-211">C6</span><span class="sxs-lookup"><span data-stu-id="006ac-211">C6</span></span>
- <span data-ttu-id="006ac-212">250MB</span><span class="sxs-lookup"><span data-stu-id="006ac-212">250MB</span></span>
- <span data-ttu-id="006ac-213">1GB</span><span class="sxs-lookup"><span data-stu-id="006ac-213">1GB</span></span>
- <span data-ttu-id="006ac-214">2.5 GB</span><span class="sxs-lookup"><span data-stu-id="006ac-214">2.5GB</span></span>
- <span data-ttu-id="006ac-215">6GB</span><span class="sxs-lookup"><span data-stu-id="006ac-215">6GB</span></span>
- <span data-ttu-id="006ac-216">13GB</span><span class="sxs-lookup"><span data-stu-id="006ac-216">13GB</span></span>
- <span data-ttu-id="006ac-217">26GB</span><span class="sxs-lookup"><span data-stu-id="006ac-217">26GB</span></span>
- <span data-ttu-id="006ac-218">53GB</span><span class="sxs-lookup"><span data-stu-id="006ac-218">53GB</span></span>

<span data-ttu-id="006ac-219">기본값은 1GB 또는 C1입니다.</span><span class="sxs-lookup"><span data-stu-id="006ac-219">The default value is 1GB or C1.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: P1, P2, P3, P4, C0, C1, C2, C3, C4, C5, C6, 250MB, 1GB, 2.5GB, 6GB, 13GB, 26GB, 53GB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="006ac-220">-Sku</span><span class="sxs-lookup"><span data-stu-id="006ac-220">-Sku</span></span>
<span data-ttu-id="006ac-221">만들 Redis Cache의 SKU를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="006ac-221">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="006ac-222">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="006ac-222">Valid values are:</span></span> 

- <span data-ttu-id="006ac-223">기본적</span><span class="sxs-lookup"><span data-stu-id="006ac-223">Basic</span></span>
- <span data-ttu-id="006ac-224">표준이</span><span class="sxs-lookup"><span data-stu-id="006ac-224">Standard</span></span>
- <span data-ttu-id="006ac-225">Premium</span><span class="sxs-lookup"><span data-stu-id="006ac-225">Premium</span></span>

<span data-ttu-id="006ac-226">기본값은 표준입니다.</span><span class="sxs-lookup"><span data-stu-id="006ac-226">The default value is Standard.</span></span>

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

### <span data-ttu-id="006ac-227">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="006ac-227">-StaticIP</span></span>
<span data-ttu-id="006ac-228">Redis 캐시에 대 한 서브넷의 고유한 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="006ac-228">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>

<span data-ttu-id="006ac-229">이 매개 변수에 대 한 값을 지정 하지 않으면이 cmdlet은 서브넷에서 IP 주소를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="006ac-229">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="006ac-230">-서브넷</span><span class="sxs-lookup"><span data-stu-id="006ac-230">-Subnet</span></span>
<span data-ttu-id="006ac-231">Redis 캐시를 배포할 서브넷의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="006ac-231">Specifies the name of the subnet in which to deploy the Redis Cache.</span></span>

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

### <span data-ttu-id="006ac-232">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="006ac-232">-SubnetId</span></span>
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

### <span data-ttu-id="006ac-233">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="006ac-233">-TenantSettings</span></span>
<span data-ttu-id="006ac-234">이 매개 변수는 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="006ac-234">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="006ac-235">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="006ac-235">-VirtualNetwork</span></span>
<span data-ttu-id="006ac-236">Redis 캐시를 배포할 가상 네트워크의 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="006ac-236">Specifies the resource ID of the virtual network in which to deploy the Redis Cache.</span></span>

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

### <span data-ttu-id="006ac-237">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="006ac-237">-DefaultProfile</span></span>
<span data-ttu-id="006ac-238">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="006ac-238">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="006ac-239">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="006ac-239">CommonParameters</span></span>
<span data-ttu-id="006ac-240">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="006ac-240">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="006ac-241">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="006ac-241">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="006ac-242">입력</span><span class="sxs-lookup"><span data-stu-id="006ac-242">INPUTS</span></span>

### <span data-ttu-id="006ac-243">않아야</span><span class="sxs-lookup"><span data-stu-id="006ac-243">None</span></span>
<span data-ttu-id="006ac-244">이름으로이 cmdlet에 대 한 입력을 파이프 할 수 있지만 값을 기준으로 하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="006ac-244">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="006ac-245">출력</span><span class="sxs-lookup"><span data-stu-id="006ac-245">OUTPUTS</span></span>

### <span data-ttu-id="006ac-246">RedisCacheAttributesWithAccessKeys. 모델. m e.</span><span class="sxs-lookup"><span data-stu-id="006ac-246">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>
<span data-ttu-id="006ac-247">이 cmdlet은 기본 및 보조 선택 키를 포함 하 여 Redis 캐시의 모든 특성을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="006ac-247">This cmdlet returns all attributes of a Redis Cache including primary and secondary access keys.</span></span>

## <span data-ttu-id="006ac-248">상속자</span><span class="sxs-lookup"><span data-stu-id="006ac-248">NOTES</span></span>

## <span data-ttu-id="006ac-249">관련 링크</span><span class="sxs-lookup"><span data-stu-id="006ac-249">RELATED LINKS</span></span>

[<span data-ttu-id="006ac-250">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="006ac-250">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="006ac-251">제거-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="006ac-251">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="006ac-252">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="006ac-252">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


