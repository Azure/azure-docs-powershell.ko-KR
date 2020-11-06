---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/set-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
ms.openlocfilehash: 951198c93918c08f69f28dc6db3c5fe605e6d3bc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529745"
---
# <span data-ttu-id="b0db6-101">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="b0db6-101">Set-AzureRmRedisCache</span></span>

## <span data-ttu-id="b0db6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0db6-102">SYNOPSIS</span></span>
<span data-ttu-id="b0db6-103">Redis 캐시를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0db6-103">Modifies a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0db6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b0db6-104">SYNTAX</span></span>

```
Set-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-MaxMemoryPolicy <String>] [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>]
 [-TenantSettings <Hashtable>] [-ShardCount <Int32>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0db6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b0db6-105">DESCRIPTION</span></span>
<span data-ttu-id="b0db6-106">**Set-AzureRmRedisCache** Cmdlet은 Azure Redis Cache를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0db6-106">The **Set-AzureRmRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="b0db6-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b0db6-107">EXAMPLES</span></span>

### <span data-ttu-id="b0db6-108">예제 1: Redis 캐시 수정</span><span class="sxs-lookup"><span data-stu-id="b0db6-108">Example 1: Modify a Redis Cache</span></span>
```
PS C:\>Set-AzureRmRedisCache -ResourceGroupName "MyGroup" -Name "MyCache" -RedisConfiguration @{"maxmemory-policy" = "allkeys-random"}

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

<span data-ttu-id="b0db6-109">이 명령은 MyCache 라는 Redis Cache에 대 한 maxmemory 정책을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0db6-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="b0db6-110">변수</span><span class="sxs-lookup"><span data-stu-id="b0db6-110">PARAMETERS</span></span>

### <span data-ttu-id="b0db6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0db6-111">-DefaultProfile</span></span>
<span data-ttu-id="b0db6-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b0db6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0db6-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="b0db6-113">-EnableNonSslPort</span></span>
<span data-ttu-id="b0db6-114">비 SSL 포트를 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b0db6-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="b0db6-115">기본값은 $False (비 SSL 포트를 사용할 수 없음)입니다.</span><span class="sxs-lookup"><span data-stu-id="b0db6-115">The default value is $False (the non-SSL port is disabled).</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0db6-116">-MaxMemoryPolicy</span><span class="sxs-lookup"><span data-stu-id="b0db6-116">-MaxMemoryPolicy</span></span>
<span data-ttu-id="b0db6-117">이 매개 변수는 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b0db6-117">This parameter has been deprecated.</span></span>
<span data-ttu-id="b0db6-118">*Redisconfiguration* 매개 변수를 사용 하 여 maxmemory-정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0db6-118">Use the *RedisConfiguration* parameter to set maxmemory-policy.</span></span>
<span data-ttu-id="b0db6-119">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="b0db6-119">For example:</span></span> 

`-RedisConfiguration @{"maxmemory-policy" = "allkeys-lru"}`

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0db6-120">-이름</span><span class="sxs-lookup"><span data-stu-id="b0db6-120">-Name</span></span>
<span data-ttu-id="b0db6-121">업데이트할 Redis 캐시의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0db6-121">Specifies the name of the Redis Cache to update.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0db6-122">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="b0db6-122">-RedisConfiguration</span></span>
<span data-ttu-id="b0db6-123">Redis 구성 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0db6-123">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="b0db6-124">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b0db6-124">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b0db6-125">rdb-백업-사용 가능.</span><span class="sxs-lookup"><span data-stu-id="b0db6-125">rdb-backup-enabled.</span></span>
<span data-ttu-id="b0db6-126">Redis 데이터 지 속성을 사용 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0db6-126">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="b0db6-127">프리미엄 계층만.</span><span class="sxs-lookup"><span data-stu-id="b0db6-127">Premium tier only.</span></span>
- <span data-ttu-id="b0db6-128">rdb-저장소-연결 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="b0db6-128">rdb-storage-connection-string.</span></span>
<span data-ttu-id="b0db6-129">Redis 데이터 지 속성에 대 한 저장소 계정에 대 한 연결 문자열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0db6-129">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="b0db6-130">프리미엄 계층만.</span><span class="sxs-lookup"><span data-stu-id="b0db6-130">Premium tier only.</span></span>
- <span data-ttu-id="b0db6-131">rdb-백업-빈도</span><span class="sxs-lookup"><span data-stu-id="b0db6-131">rdb-backup-frequency.</span></span>
<span data-ttu-id="b0db6-132">Redis 데이터 지 속성에 대 한 백업 빈도를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0db6-132">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="b0db6-133">프리미엄 계층만.</span><span class="sxs-lookup"><span data-stu-id="b0db6-133">Premium tier only.</span></span> 
- <span data-ttu-id="b0db6-134">maxmemory-예약 됨.</span><span class="sxs-lookup"><span data-stu-id="b0db6-134">maxmemory-reserved.</span></span>
<span data-ttu-id="b0db6-135">비 캐시 프로세스에 예약 된 메모리를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0db6-135">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="b0db6-136">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="b0db6-136">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="b0db6-137">maxmemory-정책.</span><span class="sxs-lookup"><span data-stu-id="b0db6-137">maxmemory-policy.</span></span>
<span data-ttu-id="b0db6-138">캐시에 대 한 제거 정책을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0db6-138">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="b0db6-139">모든 가격 책정 계층</span><span class="sxs-lookup"><span data-stu-id="b0db6-139">All pricing tiers.</span></span> 
- <span data-ttu-id="b0db6-140">notify-keyspace-이벤트</span><span class="sxs-lookup"><span data-stu-id="b0db6-140">notify-keyspace-events.</span></span>
<span data-ttu-id="b0db6-141">Keyspace 알림을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0db6-141">Configures keyspace notifications.</span></span>
<span data-ttu-id="b0db6-142">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="b0db6-142">Standard and premium tiers.</span></span> 
- <span data-ttu-id="b0db6-143">hash-최대 ziplist-항목.</span><span class="sxs-lookup"><span data-stu-id="b0db6-143">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="b0db6-144">작은 집계 데이터 형식에 대 한 메모리 최적화를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0db6-144">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="b0db6-145">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="b0db6-145">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="b0db6-146">hash-max-ziplist-값.</span><span class="sxs-lookup"><span data-stu-id="b0db6-146">hash-max-ziplist-value.</span></span>
<span data-ttu-id="b0db6-147">작은 집계 데이터 형식에 대 한 메모리 최적화를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0db6-147">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="b0db6-148">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="b0db6-148">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="b0db6-149">set-max-intset-항목</span><span class="sxs-lookup"><span data-stu-id="b0db6-149">set-max-intset-entries.</span></span>
<span data-ttu-id="b0db6-150">작은 집계 데이터 형식에 대 한 메모리 최적화를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0db6-150">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="b0db6-151">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="b0db6-151">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="b0db6-152">zset-max-ziplist 항목.</span><span class="sxs-lookup"><span data-stu-id="b0db6-152">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="b0db6-153">작은 집계 데이터 형식에 대 한 메모리 최적화를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0db6-153">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="b0db6-154">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="b0db6-154">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="b0db6-155">zset-max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="b0db6-155">zset-max-ziplist-value.</span></span>
<span data-ttu-id="b0db6-156">작은 집계 데이터 형식에 대 한 메모리 최적화를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0db6-156">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="b0db6-157">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="b0db6-157">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="b0db6-158">databases.</span><span class="sxs-lookup"><span data-stu-id="b0db6-158">databases.</span></span>
<span data-ttu-id="b0db6-159">데이터베이스 수를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0db6-159">Configures the number of databases.</span></span>
<span data-ttu-id="b0db6-160">이 속성은 캐시 생성 시에만 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b0db6-160">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="b0db6-161">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="b0db6-161">Standard and Premium tiers.</span></span>

<span data-ttu-id="b0db6-162">자세한 내용은 Azure PowerShell을 사용 하 여 Azure Redis 캐시 관리 https://go.microsoft.com/fwlink/?LinkId=800051 ()를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="b0db6-162">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0db6-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0db6-163">-ResourceGroupName</span></span>
<span data-ttu-id="b0db6-164">Redis 캐시를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0db6-164">Specifies the name of the resource group that contains the Redis Cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0db6-165">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="b0db6-165">-ShardCount</span></span>
<span data-ttu-id="b0db6-166">프리미엄 클러스터 캐시에서 만들 shards 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0db6-166">Specifies the number of shards to create on a Premium cluster cache.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0db6-167">-크기</span><span class="sxs-lookup"><span data-stu-id="b0db6-167">-Size</span></span>
<span data-ttu-id="b0db6-168">Redis 캐시의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0db6-168">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="b0db6-169">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b0db6-169">Valid values are:</span></span> 

- <span data-ttu-id="b0db6-170">P1</span><span class="sxs-lookup"><span data-stu-id="b0db6-170">P1</span></span>
- <span data-ttu-id="b0db6-171">즉</span><span class="sxs-lookup"><span data-stu-id="b0db6-171">P2</span></span>
- <span data-ttu-id="b0db6-172">P3</span><span class="sxs-lookup"><span data-stu-id="b0db6-172">P3</span></span>
- <span data-ttu-id="b0db6-173">P4</span><span class="sxs-lookup"><span data-stu-id="b0db6-173">P4</span></span>
- <span data-ttu-id="b0db6-174">C0</span><span class="sxs-lookup"><span data-stu-id="b0db6-174">C0</span></span>
- <span data-ttu-id="b0db6-175">C1</span><span class="sxs-lookup"><span data-stu-id="b0db6-175">C1</span></span>
- <span data-ttu-id="b0db6-176">만족할</span><span class="sxs-lookup"><span data-stu-id="b0db6-176">C2</span></span>
- <span data-ttu-id="b0db6-177">C3</span><span class="sxs-lookup"><span data-stu-id="b0db6-177">C3</span></span>
- <span data-ttu-id="b0db6-178">C4</span><span class="sxs-lookup"><span data-stu-id="b0db6-178">C4</span></span>
- <span data-ttu-id="b0db6-179">C 5</span><span class="sxs-lookup"><span data-stu-id="b0db6-179">C5</span></span>
- <span data-ttu-id="b0db6-180">C6</span><span class="sxs-lookup"><span data-stu-id="b0db6-180">C6</span></span>
- <span data-ttu-id="b0db6-181">250MB</span><span class="sxs-lookup"><span data-stu-id="b0db6-181">250MB</span></span>
- <span data-ttu-id="b0db6-182">1GB</span><span class="sxs-lookup"><span data-stu-id="b0db6-182">1GB</span></span>
- <span data-ttu-id="b0db6-183">2.5 GB</span><span class="sxs-lookup"><span data-stu-id="b0db6-183">2.5GB</span></span>
- <span data-ttu-id="b0db6-184">6GB</span><span class="sxs-lookup"><span data-stu-id="b0db6-184">6GB</span></span>
- <span data-ttu-id="b0db6-185">13GB</span><span class="sxs-lookup"><span data-stu-id="b0db6-185">13GB</span></span>
- <span data-ttu-id="b0db6-186">26GB</span><span class="sxs-lookup"><span data-stu-id="b0db6-186">26GB</span></span>
- <span data-ttu-id="b0db6-187">53GB</span><span class="sxs-lookup"><span data-stu-id="b0db6-187">53GB</span></span>

<span data-ttu-id="b0db6-188">기본값은 1GB 또는 C1입니다.</span><span class="sxs-lookup"><span data-stu-id="b0db6-188">The default value is 1GB or C1.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: P1, P2, P3, P4, C0, C1, C2, C3, C4, C5, C6, 250MB, 1GB, 2.5GB, 6GB, 13GB, 26GB, 53GB

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0db6-189">-Sku</span><span class="sxs-lookup"><span data-stu-id="b0db6-189">-Sku</span></span>
<span data-ttu-id="b0db6-190">만들 Redis Cache의 SKU를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0db6-190">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="b0db6-191">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b0db6-191">Valid values are:</span></span> 

- <span data-ttu-id="b0db6-192">기본적</span><span class="sxs-lookup"><span data-stu-id="b0db6-192">Basic</span></span>
- <span data-ttu-id="b0db6-193">표준이</span><span class="sxs-lookup"><span data-stu-id="b0db6-193">Standard</span></span>
- <span data-ttu-id="b0db6-194">Premium</span><span class="sxs-lookup"><span data-stu-id="b0db6-194">Premium</span></span>

<span data-ttu-id="b0db6-195">기본값은 표준입니다.</span><span class="sxs-lookup"><span data-stu-id="b0db6-195">The default value is Standard.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0db6-196">태그</span><span class="sxs-lookup"><span data-stu-id="b0db6-196">-Tag</span></span>
<span data-ttu-id="b0db6-197">태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="b0db6-197">A hash table which represents tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0db6-198">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="b0db6-198">-TenantSettings</span></span>
<span data-ttu-id="b0db6-199">이 매개 변수는 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b0db6-199">This parameter has been deprecated.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0db6-200">-확인</span><span class="sxs-lookup"><span data-stu-id="b0db6-200">-Confirm</span></span>
<span data-ttu-id="b0db6-201">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0db6-201">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0db6-202">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0db6-202">-WhatIf</span></span>
<span data-ttu-id="b0db6-203">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b0db6-203">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b0db6-204">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b0db6-204">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0db6-205">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0db6-205">CommonParameters</span></span>
<span data-ttu-id="b0db6-206">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0db6-206">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0db6-207">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0db6-207">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0db6-208">입력</span><span class="sxs-lookup"><span data-stu-id="b0db6-208">INPUTS</span></span>

### <span data-ttu-id="b0db6-209">않아야</span><span class="sxs-lookup"><span data-stu-id="b0db6-209">None</span></span>
<span data-ttu-id="b0db6-210">속성 이름으로이 cmdlet에 대 한 입력을 파이프로 지정할 수 있지만 값을 기준으로 하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b0db6-210">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="b0db6-211">출력</span><span class="sxs-lookup"><span data-stu-id="b0db6-211">OUTPUTS</span></span>

### <span data-ttu-id="b0db6-212">RedisCacheAttributesWithAccessKeys. 모델. m e.</span><span class="sxs-lookup"><span data-stu-id="b0db6-212">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>
<span data-ttu-id="b0db6-213">기본 및 보조 선택 키를 포함 하 여 Redis Cache의 모든 특성을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0db6-213">Returns all attributes of a Redis Cache, including primary and secondary access keys.</span></span>

## <span data-ttu-id="b0db6-214">상속자</span><span class="sxs-lookup"><span data-stu-id="b0db6-214">NOTES</span></span>

## <span data-ttu-id="b0db6-215">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b0db6-215">RELATED LINKS</span></span>

[<span data-ttu-id="b0db6-216">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="b0db6-216">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="b0db6-217">새로운 AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="b0db6-217">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="b0db6-218">제거-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="b0db6-218">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)


