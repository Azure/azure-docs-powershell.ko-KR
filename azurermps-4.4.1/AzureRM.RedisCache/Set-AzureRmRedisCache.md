---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
ms.openlocfilehash: bac4176671f5583072142b5973d12bc62205a0a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529183"
---
# <span data-ttu-id="1d75e-101">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="1d75e-101">Set-AzureRmRedisCache</span></span>

## <span data-ttu-id="1d75e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d75e-102">SYNOPSIS</span></span>
<span data-ttu-id="1d75e-103">Redis 캐시를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d75e-103">Modifies a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1d75e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1d75e-104">SYNTAX</span></span>

```
Set-AzureRmRedisCache -ResourceGroupName <String> -Name <String> [-Size <String>] [-Sku <String>]
 [-MaxMemoryPolicy <String>] [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>]
 [-TenantSettings <Hashtable>] [-ShardCount <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1d75e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1d75e-105">DESCRIPTION</span></span>
<span data-ttu-id="1d75e-106">**Set-AzureRmRedisCache** Cmdlet은 Azure Redis Cache를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d75e-106">The **Set-AzureRmRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="1d75e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1d75e-107">EXAMPLES</span></span>

### <span data-ttu-id="1d75e-108">예제 1: Redis 캐시 수정</span><span class="sxs-lookup"><span data-stu-id="1d75e-108">Example 1: Modify a Redis Cache</span></span>
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
```

<span data-ttu-id="1d75e-109">이 명령은 MyCache 라는 Redis Cache에 대 한 maxmemory 정책을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d75e-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="1d75e-110">변수</span><span class="sxs-lookup"><span data-stu-id="1d75e-110">PARAMETERS</span></span>

### <span data-ttu-id="1d75e-111">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="1d75e-111">-EnableNonSslPort</span></span>
<span data-ttu-id="1d75e-112">비 SSL 포트를 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1d75e-112">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="1d75e-113">기본값은 $False (비 SSL 포트를 사용할 수 없음)입니다.</span><span class="sxs-lookup"><span data-stu-id="1d75e-113">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="1d75e-114">-MaxMemoryPolicy</span><span class="sxs-lookup"><span data-stu-id="1d75e-114">-MaxMemoryPolicy</span></span>
<span data-ttu-id="1d75e-115">이 매개 변수는 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1d75e-115">This parameter has been deprecated.</span></span>
<span data-ttu-id="1d75e-116">*Redisconfiguration* 매개 변수를 사용 하 여 maxmemory-정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d75e-116">Use the *RedisConfiguration* parameter to set maxmemory-policy.</span></span>
<span data-ttu-id="1d75e-117">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="1d75e-117">For example:</span></span> 

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

### <span data-ttu-id="1d75e-118">-이름</span><span class="sxs-lookup"><span data-stu-id="1d75e-118">-Name</span></span>
<span data-ttu-id="1d75e-119">업데이트할 Redis 캐시의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d75e-119">Specifies the name of the Redis Cache to update.</span></span>

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

### <span data-ttu-id="1d75e-120">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="1d75e-120">-RedisConfiguration</span></span>
<span data-ttu-id="1d75e-121">Redis 구성 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d75e-121">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="1d75e-122">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1d75e-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="1d75e-123">rdb-백업-사용 가능.</span><span class="sxs-lookup"><span data-stu-id="1d75e-123">rdb-backup-enabled.</span></span>
<span data-ttu-id="1d75e-124">Redis 데이터 지 속성을 사용 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d75e-124">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="1d75e-125">프리미엄 계층만.</span><span class="sxs-lookup"><span data-stu-id="1d75e-125">Premium tier only.</span></span>
- <span data-ttu-id="1d75e-126">rdb-저장소-연결 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="1d75e-126">rdb-storage-connection-string.</span></span>
<span data-ttu-id="1d75e-127">Redis 데이터 지 속성에 대 한 저장소 계정에 대 한 연결 문자열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d75e-127">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="1d75e-128">프리미엄 계층만.</span><span class="sxs-lookup"><span data-stu-id="1d75e-128">Premium tier only.</span></span>
- <span data-ttu-id="1d75e-129">rdb-백업-빈도</span><span class="sxs-lookup"><span data-stu-id="1d75e-129">rdb-backup-frequency.</span></span>
<span data-ttu-id="1d75e-130">Redis 데이터 지 속성에 대 한 백업 빈도를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d75e-130">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="1d75e-131">프리미엄 계층만.</span><span class="sxs-lookup"><span data-stu-id="1d75e-131">Premium tier only.</span></span> 
- <span data-ttu-id="1d75e-132">maxmemory-예약 됨.</span><span class="sxs-lookup"><span data-stu-id="1d75e-132">maxmemory-reserved.</span></span>
<span data-ttu-id="1d75e-133">비 캐시 프로세스에 예약 된 메모리를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d75e-133">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="1d75e-134">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="1d75e-134">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="1d75e-135">maxmemory-정책.</span><span class="sxs-lookup"><span data-stu-id="1d75e-135">maxmemory-policy.</span></span>
<span data-ttu-id="1d75e-136">캐시에 대 한 제거 정책을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d75e-136">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="1d75e-137">모든 가격 책정 계층</span><span class="sxs-lookup"><span data-stu-id="1d75e-137">All pricing tiers.</span></span> 
- <span data-ttu-id="1d75e-138">notify-keyspace-이벤트</span><span class="sxs-lookup"><span data-stu-id="1d75e-138">notify-keyspace-events.</span></span>
<span data-ttu-id="1d75e-139">Keyspace 알림을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d75e-139">Configures keyspace notifications.</span></span>
<span data-ttu-id="1d75e-140">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="1d75e-140">Standard and premium tiers.</span></span> 
- <span data-ttu-id="1d75e-141">hash-최대 ziplist-항목.</span><span class="sxs-lookup"><span data-stu-id="1d75e-141">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="1d75e-142">작은 집계 데이터 형식에 대 한 메모리 최적화를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d75e-142">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="1d75e-143">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="1d75e-143">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="1d75e-144">hash-max-ziplist-값.</span><span class="sxs-lookup"><span data-stu-id="1d75e-144">hash-max-ziplist-value.</span></span>
<span data-ttu-id="1d75e-145">작은 집계 데이터 형식에 대 한 메모리 최적화를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d75e-145">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="1d75e-146">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="1d75e-146">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="1d75e-147">set-max-intset-항목</span><span class="sxs-lookup"><span data-stu-id="1d75e-147">set-max-intset-entries.</span></span>
<span data-ttu-id="1d75e-148">작은 집계 데이터 형식에 대 한 메모리 최적화를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d75e-148">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="1d75e-149">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="1d75e-149">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="1d75e-150">zset-max-ziplist 항목.</span><span class="sxs-lookup"><span data-stu-id="1d75e-150">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="1d75e-151">작은 집계 데이터 형식에 대 한 메모리 최적화를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d75e-151">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="1d75e-152">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="1d75e-152">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="1d75e-153">zset-max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="1d75e-153">zset-max-ziplist-value.</span></span>
<span data-ttu-id="1d75e-154">작은 집계 데이터 형식에 대 한 메모리 최적화를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d75e-154">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="1d75e-155">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="1d75e-155">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="1d75e-156">databases.</span><span class="sxs-lookup"><span data-stu-id="1d75e-156">databases.</span></span>
<span data-ttu-id="1d75e-157">데이터베이스 수를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d75e-157">Configures the number of databases.</span></span>
<span data-ttu-id="1d75e-158">이 속성은 캐시 생성 시에만 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1d75e-158">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="1d75e-159">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="1d75e-159">Standard and Premium tiers.</span></span>

<span data-ttu-id="1d75e-160">자세한 내용은 Azure PowerShell을 사용 하 여 Azure Redis 캐시 관리 https://go.microsoft.com/fwlink/?LinkId=800051 ()를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="1d75e-160">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="1d75e-161">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d75e-161">-ResourceGroupName</span></span>
<span data-ttu-id="1d75e-162">Redis 캐시를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d75e-162">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="1d75e-163">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="1d75e-163">-ShardCount</span></span>
<span data-ttu-id="1d75e-164">프리미엄 클러스터 캐시에서 만들 shards 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d75e-164">Specifies the number of shards to create on a Premium cluster cache.</span></span>

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

### <span data-ttu-id="1d75e-165">-크기</span><span class="sxs-lookup"><span data-stu-id="1d75e-165">-Size</span></span>
<span data-ttu-id="1d75e-166">Redis 캐시의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d75e-166">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="1d75e-167">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1d75e-167">Valid values are:</span></span> 

- <span data-ttu-id="1d75e-168">P1</span><span class="sxs-lookup"><span data-stu-id="1d75e-168">P1</span></span>
- <span data-ttu-id="1d75e-169">즉</span><span class="sxs-lookup"><span data-stu-id="1d75e-169">P2</span></span>
- <span data-ttu-id="1d75e-170">P3</span><span class="sxs-lookup"><span data-stu-id="1d75e-170">P3</span></span>
- <span data-ttu-id="1d75e-171">P4</span><span class="sxs-lookup"><span data-stu-id="1d75e-171">P4</span></span>
- <span data-ttu-id="1d75e-172">C0</span><span class="sxs-lookup"><span data-stu-id="1d75e-172">C0</span></span>
- <span data-ttu-id="1d75e-173">C1</span><span class="sxs-lookup"><span data-stu-id="1d75e-173">C1</span></span>
- <span data-ttu-id="1d75e-174">만족할</span><span class="sxs-lookup"><span data-stu-id="1d75e-174">C2</span></span>
- <span data-ttu-id="1d75e-175">C3</span><span class="sxs-lookup"><span data-stu-id="1d75e-175">C3</span></span>
- <span data-ttu-id="1d75e-176">C4</span><span class="sxs-lookup"><span data-stu-id="1d75e-176">C4</span></span>
- <span data-ttu-id="1d75e-177">C 5</span><span class="sxs-lookup"><span data-stu-id="1d75e-177">C5</span></span>
- <span data-ttu-id="1d75e-178">C6</span><span class="sxs-lookup"><span data-stu-id="1d75e-178">C6</span></span>
- <span data-ttu-id="1d75e-179">250MB</span><span class="sxs-lookup"><span data-stu-id="1d75e-179">250MB</span></span>
- <span data-ttu-id="1d75e-180">1GB</span><span class="sxs-lookup"><span data-stu-id="1d75e-180">1GB</span></span>
- <span data-ttu-id="1d75e-181">2.5 GB</span><span class="sxs-lookup"><span data-stu-id="1d75e-181">2.5GB</span></span>
- <span data-ttu-id="1d75e-182">6GB</span><span class="sxs-lookup"><span data-stu-id="1d75e-182">6GB</span></span>
- <span data-ttu-id="1d75e-183">13GB</span><span class="sxs-lookup"><span data-stu-id="1d75e-183">13GB</span></span>
- <span data-ttu-id="1d75e-184">26GB</span><span class="sxs-lookup"><span data-stu-id="1d75e-184">26GB</span></span>
- <span data-ttu-id="1d75e-185">53GB</span><span class="sxs-lookup"><span data-stu-id="1d75e-185">53GB</span></span>

<span data-ttu-id="1d75e-186">기본값은 1GB 또는 C1입니다.</span><span class="sxs-lookup"><span data-stu-id="1d75e-186">The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="1d75e-187">-Sku</span><span class="sxs-lookup"><span data-stu-id="1d75e-187">-Sku</span></span>
<span data-ttu-id="1d75e-188">만들 Redis Cache의 SKU를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d75e-188">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="1d75e-189">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1d75e-189">Valid values are:</span></span> 

- <span data-ttu-id="1d75e-190">기본적</span><span class="sxs-lookup"><span data-stu-id="1d75e-190">Basic</span></span>
- <span data-ttu-id="1d75e-191">표준이</span><span class="sxs-lookup"><span data-stu-id="1d75e-191">Standard</span></span>
- <span data-ttu-id="1d75e-192">Premium</span><span class="sxs-lookup"><span data-stu-id="1d75e-192">Premium</span></span>

<span data-ttu-id="1d75e-193">기본값은 표준입니다.</span><span class="sxs-lookup"><span data-stu-id="1d75e-193">The default value is Standard.</span></span>

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

### <span data-ttu-id="1d75e-194">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="1d75e-194">-TenantSettings</span></span>
<span data-ttu-id="1d75e-195">이 매개 변수는 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1d75e-195">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="1d75e-196">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d75e-196">-DefaultProfile</span></span>
<span data-ttu-id="1d75e-197">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1d75e-197">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d75e-198">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d75e-198">CommonParameters</span></span>
<span data-ttu-id="1d75e-199">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d75e-199">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d75e-200">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d75e-200">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d75e-201">입력</span><span class="sxs-lookup"><span data-stu-id="1d75e-201">INPUTS</span></span>

### <span data-ttu-id="1d75e-202">않아야</span><span class="sxs-lookup"><span data-stu-id="1d75e-202">None</span></span>
<span data-ttu-id="1d75e-203">속성 이름으로이 cmdlet에 대 한 입력을 파이프로 지정할 수 있지만 값을 기준으로 하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1d75e-203">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="1d75e-204">출력</span><span class="sxs-lookup"><span data-stu-id="1d75e-204">OUTPUTS</span></span>

### <span data-ttu-id="1d75e-205">RedisCacheAttributesWithAccessKeys. 모델. m e.</span><span class="sxs-lookup"><span data-stu-id="1d75e-205">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>
<span data-ttu-id="1d75e-206">기본 및 보조 선택 키를 포함 하 여 Redis Cache의 모든 특성을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d75e-206">Returns all attributes of a Redis Cache, including primary and secondary access keys.</span></span>

## <span data-ttu-id="1d75e-207">상속자</span><span class="sxs-lookup"><span data-stu-id="1d75e-207">NOTES</span></span>

## <span data-ttu-id="1d75e-208">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1d75e-208">RELATED LINKS</span></span>

[<span data-ttu-id="1d75e-209">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="1d75e-209">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="1d75e-210">새로운 AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="1d75e-210">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="1d75e-211">제거-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="1d75e-211">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)


