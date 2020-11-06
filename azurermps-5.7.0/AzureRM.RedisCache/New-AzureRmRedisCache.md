---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/new-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/New-AzureRmRedisCache.md
ms.openlocfilehash: bbba6372be7176b8ac1aec553a9abbbf83c7da31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528857"
---
# <span data-ttu-id="b6ff9-101">New-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="b6ff9-101">New-AzureRmRedisCache</span></span>

## <span data-ttu-id="b6ff9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6ff9-102">SYNOPSIS</span></span>
<span data-ttu-id="b6ff9-103">Redis 캐시를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-103">Creates a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6ff9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b6ff9-104">SYNTAX</span></span>

```
New-AzureRmRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-RedisVersion <String>]
 [-Size <String>] [-Sku <String>] [-MaxMemoryPolicy <String>] [-RedisConfiguration <Hashtable>]
 [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>] [-ShardCount <Int32>] [-VirtualNetwork <String>]
 [-Subnet <String>] [-SubnetId <String>] [-StaticIP <String>] [-Tag <Hashtable>] [-Zone <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6ff9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b6ff9-105">DESCRIPTION</span></span>
<span data-ttu-id="b6ff9-106">**AzureRmRedisCache** Cmdlet은 Azure Redis Cache를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-106">The **New-AzureRmRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="b6ff9-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b6ff9-107">EXAMPLES</span></span>

### <span data-ttu-id="b6ff9-108">예제 1: Redis 캐시 만들기</span><span class="sxs-lookup"><span data-stu-id="b6ff9-108">Example 1: Create a Redis Cache</span></span>
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
          Tag                : {}
          Zone               : []
```

<span data-ttu-id="b6ff9-109">이 명령은 Redis Cache를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="b6ff9-110">예제 2: 표준 SKU Redis 캐시 만들기</span><span class="sxs-lookup"><span data-stu-id="b6ff9-110">Example 2: Create a Standard SKU Redis Cache</span></span>
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
          Tag                : {}
          Zone               : []
```

<span data-ttu-id="b6ff9-111">이 명령은 Redis Cache를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-111">This command creates a Redis Cache.</span></span>

## <span data-ttu-id="b6ff9-112">변수</span><span class="sxs-lookup"><span data-stu-id="b6ff9-112">PARAMETERS</span></span>

### <span data-ttu-id="b6ff9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6ff9-113">-DefaultProfile</span></span>
<span data-ttu-id="b6ff9-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b6ff9-115">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="b6ff9-115">-EnableNonSslPort</span></span>
<span data-ttu-id="b6ff9-116">비 SSL 포트를 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-116">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="b6ff9-117">기본값은 $False (비 SSL 포트를 사용할 수 없음)입니다.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-117">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="b6ff9-118">-위치</span><span class="sxs-lookup"><span data-stu-id="b6ff9-118">-Location</span></span>
<span data-ttu-id="b6ff9-119">Redis 캐시를 만들 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-119">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="b6ff9-120">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-120">Valid values are:</span></span> 

- <span data-ttu-id="b6ff9-121">대한민국 미국 중부</span><span class="sxs-lookup"><span data-stu-id="b6ff9-121">North Central US</span></span>
- <span data-ttu-id="b6ff9-122">미국 중부 US</span><span class="sxs-lookup"><span data-stu-id="b6ff9-122">South Central US</span></span>
- <span data-ttu-id="b6ff9-123">중부 US</span><span class="sxs-lookup"><span data-stu-id="b6ff9-123">Central US</span></span>
- <span data-ttu-id="b6ff9-124">유럽 서유럽</span><span class="sxs-lookup"><span data-stu-id="b6ff9-124">West Europe</span></span>
- <span data-ttu-id="b6ff9-125">동유럽</span><span class="sxs-lookup"><span data-stu-id="b6ff9-125">North Europe</span></span>
- <span data-ttu-id="b6ff9-126">미국 서 부</span><span class="sxs-lookup"><span data-stu-id="b6ff9-126">West US</span></span>
- <span data-ttu-id="b6ff9-127">미국 동부</span><span class="sxs-lookup"><span data-stu-id="b6ff9-127">East US</span></span>
- <span data-ttu-id="b6ff9-128">미국 동부 2</span><span class="sxs-lookup"><span data-stu-id="b6ff9-128">East US 2</span></span>
- <span data-ttu-id="b6ff9-129">일본 동부</span><span class="sxs-lookup"><span data-stu-id="b6ff9-129">Japan East</span></span>
- <span data-ttu-id="b6ff9-130">일본 서쪽</span><span class="sxs-lookup"><span data-stu-id="b6ff9-130">Japan West</span></span>
- <span data-ttu-id="b6ff9-131">브라질 남부</span><span class="sxs-lookup"><span data-stu-id="b6ff9-131">Brazil South</span></span>
- <span data-ttu-id="b6ff9-132">동남 아시아</span><span class="sxs-lookup"><span data-stu-id="b6ff9-132">Southeast Asia</span></span>
- <span data-ttu-id="b6ff9-133">동아시아</span><span class="sxs-lookup"><span data-stu-id="b6ff9-133">East Asia</span></span>
- <span data-ttu-id="b6ff9-134">오스트레일리아 동부</span><span class="sxs-lookup"><span data-stu-id="b6ff9-134">Australia East</span></span>
- <span data-ttu-id="b6ff9-135">오스트레일리아 남동쪽</span><span class="sxs-lookup"><span data-stu-id="b6ff9-135">Australia Southeast</span></span>

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

### <span data-ttu-id="b6ff9-136">-MaxMemoryPolicy</span><span class="sxs-lookup"><span data-stu-id="b6ff9-136">-MaxMemoryPolicy</span></span>
<span data-ttu-id="b6ff9-137">이 매개 변수는 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-137">This parameter has been deprecated.</span></span>
<span data-ttu-id="b6ff9-138">*Redisconfiguration* 매개 변수를 사용 하 여 maxmemory-정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-138">Use the *RedisConfiguration* parameter to set maxmemory-policy.</span></span>
<span data-ttu-id="b6ff9-139">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="b6ff9-139">For example:</span></span> 

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

### <span data-ttu-id="b6ff9-140">-이름</span><span class="sxs-lookup"><span data-stu-id="b6ff9-140">-Name</span></span>
<span data-ttu-id="b6ff9-141">만들 Redis 캐시의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-141">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="b6ff9-142">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="b6ff9-142">-RedisConfiguration</span></span>
<span data-ttu-id="b6ff9-143">Redis 구성 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-143">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="b6ff9-144">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b6ff9-145">rdb-백업-사용 가능.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-145">rdb-backup-enabled.</span></span>
<span data-ttu-id="b6ff9-146">Redis 데이터 지 속성을 사용 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-146">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="b6ff9-147">프리미엄 계층만.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-147">Premium tier only.</span></span>
- <span data-ttu-id="b6ff9-148">rdb-저장소-연결 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-148">rdb-storage-connection-string.</span></span>
<span data-ttu-id="b6ff9-149">Redis 데이터 지 속성에 대 한 저장소 계정에 대 한 연결 문자열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-149">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="b6ff9-150">프리미엄 계층만.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-150">Premium tier only.</span></span>
- <span data-ttu-id="b6ff9-151">rdb-백업-빈도</span><span class="sxs-lookup"><span data-stu-id="b6ff9-151">rdb-backup-frequency.</span></span>
<span data-ttu-id="b6ff9-152">Redis 데이터 지 속성에 대 한 백업 빈도를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-152">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="b6ff9-153">프리미엄 계층만.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-153">Premium tier only.</span></span> 
- <span data-ttu-id="b6ff9-154">maxmemory-예약 됨.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-154">maxmemory-reserved.</span></span>
<span data-ttu-id="b6ff9-155">비 캐시 프로세스에 예약 된 메모리를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-155">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="b6ff9-156">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-156">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="b6ff9-157">maxmemory-정책.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-157">maxmemory-policy.</span></span>
<span data-ttu-id="b6ff9-158">캐시에 대 한 제거 정책을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-158">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="b6ff9-159">모든 가격 책정 계층</span><span class="sxs-lookup"><span data-stu-id="b6ff9-159">All pricing tiers.</span></span> 
- <span data-ttu-id="b6ff9-160">notify-keyspace-이벤트</span><span class="sxs-lookup"><span data-stu-id="b6ff9-160">notify-keyspace-events.</span></span>
<span data-ttu-id="b6ff9-161">Keyspace 알림을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-161">Configures keyspace notifications.</span></span>
<span data-ttu-id="b6ff9-162">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-162">Standard and premium tiers.</span></span> 
- <span data-ttu-id="b6ff9-163">hash-최대 ziplist-항목.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-163">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="b6ff9-164">작은 집계 데이터 형식에 대 한 메모리 최적화를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-164">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="b6ff9-165">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-165">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="b6ff9-166">hash-max-ziplist-값.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-166">hash-max-ziplist-value.</span></span>
<span data-ttu-id="b6ff9-167">작은 집계 데이터 형식에 대 한 메모리 최적화를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-167">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="b6ff9-168">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-168">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="b6ff9-169">set-max-intset-항목</span><span class="sxs-lookup"><span data-stu-id="b6ff9-169">set-max-intset-entries.</span></span>
<span data-ttu-id="b6ff9-170">작은 집계 데이터 형식에 대 한 메모리 최적화를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-170">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="b6ff9-171">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-171">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="b6ff9-172">zset-max-ziplist 항목.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-172">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="b6ff9-173">작은 집계 데이터 형식에 대 한 메모리 최적화를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-173">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="b6ff9-174">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-174">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="b6ff9-175">zset-max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-175">zset-max-ziplist-value.</span></span>
<span data-ttu-id="b6ff9-176">작은 집계 데이터 형식에 대 한 메모리 최적화를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-176">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="b6ff9-177">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-177">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="b6ff9-178">databases.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-178">databases.</span></span>
<span data-ttu-id="b6ff9-179">데이터베이스 수를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-179">Configures the number of databases.</span></span>
<span data-ttu-id="b6ff9-180">이 속성은 캐시 생성 시에만 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-180">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="b6ff9-181">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-181">Standard and Premium tiers.</span></span>

<span data-ttu-id="b6ff9-182">자세한 내용은 Azure PowerShell을 사용 하 여 Azure Redis 캐시 관리 https://go.microsoft.com/fwlink/?LinkId=800051 ()를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="b6ff9-182">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="b6ff9-183">-버전 재</span><span class="sxs-lookup"><span data-stu-id="b6ff9-183">-RedisVersion</span></span>
<span data-ttu-id="b6ff9-184">이 매개 변수는 더 이상 사용 되지 않으며 이후 릴리스에서 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-184">This parameter is deprecated and will be removed from future releases.</span></span>

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

### <span data-ttu-id="b6ff9-185">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b6ff9-185">-ResourceGroupName</span></span>
<span data-ttu-id="b6ff9-186">Redis 캐시를 만들 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-186">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="b6ff9-187">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="b6ff9-187">-ShardCount</span></span>
<span data-ttu-id="b6ff9-188">프리미엄 클러스터 캐시에서 만들 shards 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-188">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="b6ff9-189">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-189">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b6ff9-190">raid-1</span><span class="sxs-lookup"><span data-stu-id="b6ff9-190">1</span></span>
- <span data-ttu-id="b6ff9-191">2</span><span class="sxs-lookup"><span data-stu-id="b6ff9-191">2</span></span>
- <span data-ttu-id="b6ff9-192">3-4</span><span class="sxs-lookup"><span data-stu-id="b6ff9-192">3</span></span>
- <span data-ttu-id="b6ff9-193">4(tcp/ipv4)</span><span class="sxs-lookup"><span data-stu-id="b6ff9-193">4</span></span>
- <span data-ttu-id="b6ff9-194">5mb</span><span class="sxs-lookup"><span data-stu-id="b6ff9-194">5</span></span>
- <span data-ttu-id="b6ff9-195">26</span><span class="sxs-lookup"><span data-stu-id="b6ff9-195">6</span></span>
- <span data-ttu-id="b6ff9-196">7</span><span class="sxs-lookup"><span data-stu-id="b6ff9-196">7</span></span>
- <span data-ttu-id="b6ff9-197">20cm(8</span><span class="sxs-lookup"><span data-stu-id="b6ff9-197">8</span></span>
- <span data-ttu-id="b6ff9-198">되었는지</span><span class="sxs-lookup"><span data-stu-id="b6ff9-198">9</span></span> 
- <span data-ttu-id="b6ff9-199">1천만</span><span class="sxs-lookup"><span data-stu-id="b6ff9-199">10</span></span>

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

### <span data-ttu-id="b6ff9-200">-크기</span><span class="sxs-lookup"><span data-stu-id="b6ff9-200">-Size</span></span>
<span data-ttu-id="b6ff9-201">Redis 캐시의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-201">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="b6ff9-202">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-202">Valid values are:</span></span> 

- <span data-ttu-id="b6ff9-203">P1</span><span class="sxs-lookup"><span data-stu-id="b6ff9-203">P1</span></span>
- <span data-ttu-id="b6ff9-204">즉</span><span class="sxs-lookup"><span data-stu-id="b6ff9-204">P2</span></span>
- <span data-ttu-id="b6ff9-205">P3</span><span class="sxs-lookup"><span data-stu-id="b6ff9-205">P3</span></span>
- <span data-ttu-id="b6ff9-206">P4</span><span class="sxs-lookup"><span data-stu-id="b6ff9-206">P4</span></span>
- <span data-ttu-id="b6ff9-207">C0</span><span class="sxs-lookup"><span data-stu-id="b6ff9-207">C0</span></span>
- <span data-ttu-id="b6ff9-208">C1</span><span class="sxs-lookup"><span data-stu-id="b6ff9-208">C1</span></span>
- <span data-ttu-id="b6ff9-209">만족할</span><span class="sxs-lookup"><span data-stu-id="b6ff9-209">C2</span></span>
- <span data-ttu-id="b6ff9-210">C3</span><span class="sxs-lookup"><span data-stu-id="b6ff9-210">C3</span></span>
- <span data-ttu-id="b6ff9-211">C4</span><span class="sxs-lookup"><span data-stu-id="b6ff9-211">C4</span></span>
- <span data-ttu-id="b6ff9-212">C 5</span><span class="sxs-lookup"><span data-stu-id="b6ff9-212">C5</span></span>
- <span data-ttu-id="b6ff9-213">C6</span><span class="sxs-lookup"><span data-stu-id="b6ff9-213">C6</span></span>
- <span data-ttu-id="b6ff9-214">250MB</span><span class="sxs-lookup"><span data-stu-id="b6ff9-214">250MB</span></span>
- <span data-ttu-id="b6ff9-215">1GB</span><span class="sxs-lookup"><span data-stu-id="b6ff9-215">1GB</span></span>
- <span data-ttu-id="b6ff9-216">2.5 GB</span><span class="sxs-lookup"><span data-stu-id="b6ff9-216">2.5GB</span></span>
- <span data-ttu-id="b6ff9-217">6GB</span><span class="sxs-lookup"><span data-stu-id="b6ff9-217">6GB</span></span>
- <span data-ttu-id="b6ff9-218">13GB</span><span class="sxs-lookup"><span data-stu-id="b6ff9-218">13GB</span></span>
- <span data-ttu-id="b6ff9-219">26GB</span><span class="sxs-lookup"><span data-stu-id="b6ff9-219">26GB</span></span>
- <span data-ttu-id="b6ff9-220">53GB</span><span class="sxs-lookup"><span data-stu-id="b6ff9-220">53GB</span></span>

<span data-ttu-id="b6ff9-221">기본값은 1GB 또는 C1입니다.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-221">The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="b6ff9-222">-Sku</span><span class="sxs-lookup"><span data-stu-id="b6ff9-222">-Sku</span></span>
<span data-ttu-id="b6ff9-223">만들 Redis Cache의 SKU를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-223">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="b6ff9-224">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-224">Valid values are:</span></span> 

- <span data-ttu-id="b6ff9-225">기본적</span><span class="sxs-lookup"><span data-stu-id="b6ff9-225">Basic</span></span>
- <span data-ttu-id="b6ff9-226">표준이</span><span class="sxs-lookup"><span data-stu-id="b6ff9-226">Standard</span></span>
- <span data-ttu-id="b6ff9-227">Premium</span><span class="sxs-lookup"><span data-stu-id="b6ff9-227">Premium</span></span>

<span data-ttu-id="b6ff9-228">기본값은 표준입니다.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-228">The default value is Standard.</span></span>

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

### <span data-ttu-id="b6ff9-229">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="b6ff9-229">-StaticIP</span></span>
<span data-ttu-id="b6ff9-230">Redis 캐시에 대 한 서브넷의 고유한 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-230">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>

<span data-ttu-id="b6ff9-231">이 매개 변수에 대 한 값을 지정 하지 않으면이 cmdlet은 서브넷에서 IP 주소를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-231">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="b6ff9-232">-서브넷</span><span class="sxs-lookup"><span data-stu-id="b6ff9-232">-Subnet</span></span>
<span data-ttu-id="b6ff9-233">Redis 캐시를 배포할 서브넷의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-233">Specifies the name of the subnet in which to deploy the Redis Cache.</span></span>

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

### <span data-ttu-id="b6ff9-234">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="b6ff9-234">-SubnetId</span></span>
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

### <span data-ttu-id="b6ff9-235">태그</span><span class="sxs-lookup"><span data-stu-id="b6ff9-235">-Tag</span></span>
<span data-ttu-id="b6ff9-236">태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-236">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="b6ff9-237">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="b6ff9-237">-TenantSettings</span></span>
<span data-ttu-id="b6ff9-238">이 매개 변수는 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-238">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="b6ff9-239">-VirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="b6ff9-239">-VirtualNetwork</span></span>
<span data-ttu-id="b6ff9-240">Redis 캐시를 배포할 가상 네트워크의 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-240">Specifies the resource ID of the virtual network in which to deploy the Redis Cache.</span></span>

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

### <span data-ttu-id="b6ff9-241">-Zone</span><span class="sxs-lookup"><span data-stu-id="b6ff9-241">-Zone</span></span>
<span data-ttu-id="b6ff9-242">영역 목록.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-242">List of zones.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6ff9-243">-확인</span><span class="sxs-lookup"><span data-stu-id="b6ff9-243">-Confirm</span></span>
<span data-ttu-id="b6ff9-244">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-244">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6ff9-245">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6ff9-245">-WhatIf</span></span>
<span data-ttu-id="b6ff9-246">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-246">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b6ff9-247">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-247">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6ff9-248">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6ff9-248">CommonParameters</span></span>
<span data-ttu-id="b6ff9-249">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-249">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6ff9-250">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6ff9-250">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6ff9-251">입력</span><span class="sxs-lookup"><span data-stu-id="b6ff9-251">INPUTS</span></span>

### <span data-ttu-id="b6ff9-252">않아야</span><span class="sxs-lookup"><span data-stu-id="b6ff9-252">None</span></span>
<span data-ttu-id="b6ff9-253">이름으로이 cmdlet에 대 한 입력을 파이프 할 수 있지만 값을 기준으로 하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-253">You can pipe input to this cmdlet by name, but not by value.</span></span>

## <span data-ttu-id="b6ff9-254">출력</span><span class="sxs-lookup"><span data-stu-id="b6ff9-254">OUTPUTS</span></span>

### <span data-ttu-id="b6ff9-255">RedisCacheAttributesWithAccessKeys. 모델. m e.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-255">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>
<span data-ttu-id="b6ff9-256">이 cmdlet은 기본 및 보조 선택 키를 포함 하 여 Redis 캐시의 모든 특성을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6ff9-256">This cmdlet returns all attributes of a Redis Cache including primary and secondary access keys.</span></span>

## <span data-ttu-id="b6ff9-257">상속자</span><span class="sxs-lookup"><span data-stu-id="b6ff9-257">NOTES</span></span>

## <span data-ttu-id="b6ff9-258">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b6ff9-258">RELATED LINKS</span></span>

[<span data-ttu-id="b6ff9-259">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="b6ff9-259">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="b6ff9-260">제거-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="b6ff9-260">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="b6ff9-261">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="b6ff9-261">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


