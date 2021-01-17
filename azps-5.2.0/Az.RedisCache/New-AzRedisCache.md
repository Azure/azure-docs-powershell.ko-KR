---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/new-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
ms.openlocfilehash: 2c11e12fa398c7a76fa10f1129bc5cf3696ae68c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336465"
---
# <span data-ttu-id="a88f8-101">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="a88f8-101">New-AzRedisCache</span></span>

## <span data-ttu-id="a88f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a88f8-102">SYNOPSIS</span></span>
<span data-ttu-id="a88f8-103">Redis Cache를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a88f8-103">Creates a Redis Cache.</span></span>

## <span data-ttu-id="a88f8-104">구문</span><span class="sxs-lookup"><span data-stu-id="a88f8-104">SYNTAX</span></span>

```
New-AzRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-MinimumTlsVersion <String>] [-SubnetId <String>] [-StaticIP <String>]
 [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a88f8-105">설명</span><span class="sxs-lookup"><span data-stu-id="a88f8-105">DESCRIPTION</span></span>
<span data-ttu-id="a88f8-106">**New-AzRedisCache** cmdlet은 Azure Redis Cache를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a88f8-106">The **New-AzRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="a88f8-107">예제</span><span class="sxs-lookup"><span data-stu-id="a88f8-107">EXAMPLES</span></span>

### <span data-ttu-id="a88f8-108">예제 1: Redis Cache 만들기</span><span class="sxs-lookup"><span data-stu-id="a88f8-108">Example 1: Create a Redis Cache</span></span>
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

<span data-ttu-id="a88f8-109">이 명령은 Redis Cache를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a88f8-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="a88f8-110">예제 2: 표준 SKU Redis Cache 만들기</span><span class="sxs-lookup"><span data-stu-id="a88f8-110">Example 2: Create a Standard SKU Redis Cache</span></span>
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

<span data-ttu-id="a88f8-111">이 명령은 Redis Cache를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a88f8-111">This command creates a Redis Cache.</span></span>

## <span data-ttu-id="a88f8-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a88f8-112">PARAMETERS</span></span>

### <span data-ttu-id="a88f8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a88f8-113">-DefaultProfile</span></span>
<span data-ttu-id="a88f8-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a88f8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a88f8-115">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="a88f8-115">-EnableNonSslPort</span></span>
<span data-ttu-id="a88f8-116">비 SSL 포트를 사용하도록 설정되어 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a88f8-116">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="a88f8-117">기본값은 $False(비 SSL 포트를 사용하지 않도록 설정)입니다.</span><span class="sxs-lookup"><span data-stu-id="a88f8-117">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="a88f8-118">-Location</span><span class="sxs-lookup"><span data-stu-id="a88f8-118">-Location</span></span>
<span data-ttu-id="a88f8-119">Redis Cache를 만들 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a88f8-119">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="a88f8-120">유효한 값은</span><span class="sxs-lookup"><span data-stu-id="a88f8-120">Valid values are:</span></span> 
- <span data-ttu-id="a88f8-121">미국 중북부</span><span class="sxs-lookup"><span data-stu-id="a88f8-121">North Central US</span></span>
- <span data-ttu-id="a88f8-122">미국 중남부</span><span class="sxs-lookup"><span data-stu-id="a88f8-122">South Central US</span></span>
- <span data-ttu-id="a88f8-123">미국 중부</span><span class="sxs-lookup"><span data-stu-id="a88f8-123">Central US</span></span>
- <span data-ttu-id="a88f8-124">유럽 서부</span><span class="sxs-lookup"><span data-stu-id="a88f8-124">West Europe</span></span>
- <span data-ttu-id="a88f8-125">북유럽</span><span class="sxs-lookup"><span data-stu-id="a88f8-125">North Europe</span></span>
- <span data-ttu-id="a88f8-126">미국 서부</span><span class="sxs-lookup"><span data-stu-id="a88f8-126">West US</span></span>
- <span data-ttu-id="a88f8-127">미국 동부</span><span class="sxs-lookup"><span data-stu-id="a88f8-127">East US</span></span>
- <span data-ttu-id="a88f8-128">미국 동부 2</span><span class="sxs-lookup"><span data-stu-id="a88f8-128">East US 2</span></span>
- <span data-ttu-id="a88f8-129">일본 동부</span><span class="sxs-lookup"><span data-stu-id="a88f8-129">Japan East</span></span>
- <span data-ttu-id="a88f8-130">일본 서부</span><span class="sxs-lookup"><span data-stu-id="a88f8-130">Japan West</span></span>
- <span data-ttu-id="a88f8-131">브라질 남부</span><span class="sxs-lookup"><span data-stu-id="a88f8-131">Brazil South</span></span>
- <span data-ttu-id="a88f8-132">동남 아시아</span><span class="sxs-lookup"><span data-stu-id="a88f8-132">Southeast Asia</span></span>
- <span data-ttu-id="a88f8-133">동아시아</span><span class="sxs-lookup"><span data-stu-id="a88f8-133">East Asia</span></span>
- <span data-ttu-id="a88f8-134">오스트레일리아 동부</span><span class="sxs-lookup"><span data-stu-id="a88f8-134">Australia East</span></span>
- <span data-ttu-id="a88f8-135">오스트레일리아 남동부</span><span class="sxs-lookup"><span data-stu-id="a88f8-135">Australia Southeast</span></span>

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

### <span data-ttu-id="a88f8-136">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="a88f8-136">-MinimumTlsVersion</span></span>
<span data-ttu-id="a88f8-137">클라이언트가 캐시에 연결하는 데 필요한 TLS 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a88f8-137">Specify the TLS version required by clients to connect to cache.</span></span>

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

### <span data-ttu-id="a88f8-138">-Name</span><span class="sxs-lookup"><span data-stu-id="a88f8-138">-Name</span></span>
<span data-ttu-id="a88f8-139">만들 Redis Cache의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a88f8-139">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="a88f8-140">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="a88f8-140">-RedisConfiguration</span></span>
<span data-ttu-id="a88f8-141">Redis 구성 설정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a88f8-141">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="a88f8-142">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="a88f8-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a88f8-143">rdb-backup을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a88f8-143">rdb-backup-enabled.</span></span>
<span data-ttu-id="a88f8-144">Redis 데이터 지속성 사용으로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a88f8-144">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="a88f8-145">프리미엄 계층만 해당됩니다.</span><span class="sxs-lookup"><span data-stu-id="a88f8-145">Premium tier only.</span></span>
- <span data-ttu-id="a88f8-146">rdb-storage-connection-string.</span><span class="sxs-lookup"><span data-stu-id="a88f8-146">rdb-storage-connection-string.</span></span>
<span data-ttu-id="a88f8-147">Redis 데이터 지속성에 대한 Storage 계정에 대한 연결 문자열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a88f8-147">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="a88f8-148">프리미엄 계층만 해당됩니다.</span><span class="sxs-lookup"><span data-stu-id="a88f8-148">Premium tier only.</span></span>
- <span data-ttu-id="a88f8-149">rdb-backup-frequency.</span><span class="sxs-lookup"><span data-stu-id="a88f8-149">rdb-backup-frequency.</span></span>
<span data-ttu-id="a88f8-150">Redis 데이터 지속성에 대한 백업 빈도를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a88f8-150">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="a88f8-151">프리미엄 계층만 해당됩니다.</span><span class="sxs-lookup"><span data-stu-id="a88f8-151">Premium tier only.</span></span> 
- <span data-ttu-id="a88f8-152">maxmemory-reserved.</span><span class="sxs-lookup"><span data-stu-id="a88f8-152">maxmemory-reserved.</span></span>
<span data-ttu-id="a88f8-153">비 캐시 프로세스에 대해 예약된 메모리를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="a88f8-153">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="a88f8-154">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="a88f8-154">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="a88f8-155">maxmemory-policy.</span><span class="sxs-lookup"><span data-stu-id="a88f8-155">maxmemory-policy.</span></span>
<span data-ttu-id="a88f8-156">캐시에 대한 삭제 정책을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="a88f8-156">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="a88f8-157">모든 가격 책정 계층.</span><span class="sxs-lookup"><span data-stu-id="a88f8-157">All pricing tiers.</span></span> 
- <span data-ttu-id="a88f8-158">notify-keyspace-events.</span><span class="sxs-lookup"><span data-stu-id="a88f8-158">notify-keyspace-events.</span></span>
<span data-ttu-id="a88f8-159">키스페이스 알림을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="a88f8-159">Configures keyspace notifications.</span></span>
<span data-ttu-id="a88f8-160">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="a88f8-160">Standard and premium tiers.</span></span> 
- <span data-ttu-id="a88f8-161">hash-max-ziplist-entries.</span><span class="sxs-lookup"><span data-stu-id="a88f8-161">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="a88f8-162">작은 집계 데이터 형식에 대한 메모리 최적화를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="a88f8-162">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="a88f8-163">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="a88f8-163">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="a88f8-164">hash-max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="a88f8-164">hash-max-ziplist-value.</span></span>
<span data-ttu-id="a88f8-165">작은 집계 데이터 형식에 대한 메모리 최적화를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="a88f8-165">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="a88f8-166">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="a88f8-166">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="a88f8-167">set-max-intset-entries.</span><span class="sxs-lookup"><span data-stu-id="a88f8-167">set-max-intset-entries.</span></span>
<span data-ttu-id="a88f8-168">작은 집계 데이터 형식에 대한 메모리 최적화를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="a88f8-168">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="a88f8-169">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="a88f8-169">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="a88f8-170">zset-max-ziplist-entries.</span><span class="sxs-lookup"><span data-stu-id="a88f8-170">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="a88f8-171">작은 집계 데이터 형식에 대한 메모리 최적화를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="a88f8-171">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="a88f8-172">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="a88f8-172">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="a88f8-173">zset-max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="a88f8-173">zset-max-ziplist-value.</span></span>
<span data-ttu-id="a88f8-174">작은 집계 데이터 형식에 대한 메모리 최적화를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="a88f8-174">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="a88f8-175">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="a88f8-175">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="a88f8-176">데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a88f8-176">databases.</span></span>
<span data-ttu-id="a88f8-177">데이터베이스 수를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="a88f8-177">Configures the number of databases.</span></span>
<span data-ttu-id="a88f8-178">이 속성은 캐시를 만들 때만 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a88f8-178">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="a88f8-179">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="a88f8-179">Standard and Premium tiers.</span></span>
<span data-ttu-id="a88f8-180">자세한 내용은 Azure PowerShell을 사용하여 Azure Redis Cache http://go.microsoft.com/fwlink/?LinkId=800051 http://go.microsoft.com/fwlink/?LinkId=800051) 관리(.</span><span class="sxs-lookup"><span data-stu-id="a88f8-180">For more information, see Manage Azure Redis Cache with Azure PowerShellhttp://go.microsoft.com/fwlink/?LinkId=800051 (http://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="a88f8-181">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a88f8-181">-ResourceGroupName</span></span>
<span data-ttu-id="a88f8-182">Redis Cache를 만들 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a88f8-182">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="a88f8-183">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="a88f8-183">-ShardCount</span></span>
<span data-ttu-id="a88f8-184">프리미엄 클러스터 캐시에 만들 수 있는 Shard 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a88f8-184">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="a88f8-185">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="a88f8-185">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a88f8-186">1</span><span class="sxs-lookup"><span data-stu-id="a88f8-186">1</span></span>
- <span data-ttu-id="a88f8-187">2</span><span class="sxs-lookup"><span data-stu-id="a88f8-187">2</span></span>
- <span data-ttu-id="a88f8-188">3</span><span class="sxs-lookup"><span data-stu-id="a88f8-188">3</span></span>
- <span data-ttu-id="a88f8-189">4</span><span class="sxs-lookup"><span data-stu-id="a88f8-189">4</span></span>
- <span data-ttu-id="a88f8-190">5</span><span class="sxs-lookup"><span data-stu-id="a88f8-190">5</span></span>
- <span data-ttu-id="a88f8-191">6</span><span class="sxs-lookup"><span data-stu-id="a88f8-191">6</span></span>
- <span data-ttu-id="a88f8-192">7</span><span class="sxs-lookup"><span data-stu-id="a88f8-192">7</span></span>
- <span data-ttu-id="a88f8-193">8</span><span class="sxs-lookup"><span data-stu-id="a88f8-193">8</span></span>
- <span data-ttu-id="a88f8-194">9</span><span class="sxs-lookup"><span data-stu-id="a88f8-194">9</span></span> 
- <span data-ttu-id="a88f8-195">10</span><span class="sxs-lookup"><span data-stu-id="a88f8-195">10</span></span>

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

### <span data-ttu-id="a88f8-196">-Size</span><span class="sxs-lookup"><span data-stu-id="a88f8-196">-Size</span></span>
<span data-ttu-id="a88f8-197">Redis Cache의 크기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a88f8-197">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="a88f8-198">유효한 값은</span><span class="sxs-lookup"><span data-stu-id="a88f8-198">Valid values are:</span></span> 
- <span data-ttu-id="a88f8-199">P1</span><span class="sxs-lookup"><span data-stu-id="a88f8-199">P1</span></span>
- <span data-ttu-id="a88f8-200">P2</span><span class="sxs-lookup"><span data-stu-id="a88f8-200">P2</span></span>
- <span data-ttu-id="a88f8-201">P3</span><span class="sxs-lookup"><span data-stu-id="a88f8-201">P3</span></span>
- <span data-ttu-id="a88f8-202">P4</span><span class="sxs-lookup"><span data-stu-id="a88f8-202">P4</span></span>
- <span data-ttu-id="a88f8-203">P5</span><span class="sxs-lookup"><span data-stu-id="a88f8-203">P5</span></span>
- <span data-ttu-id="a88f8-204">C0</span><span class="sxs-lookup"><span data-stu-id="a88f8-204">C0</span></span>
- <span data-ttu-id="a88f8-205">C1</span><span class="sxs-lookup"><span data-stu-id="a88f8-205">C1</span></span>
- <span data-ttu-id="a88f8-206">C2</span><span class="sxs-lookup"><span data-stu-id="a88f8-206">C2</span></span>
- <span data-ttu-id="a88f8-207">C3</span><span class="sxs-lookup"><span data-stu-id="a88f8-207">C3</span></span>
- <span data-ttu-id="a88f8-208">C4</span><span class="sxs-lookup"><span data-stu-id="a88f8-208">C4</span></span>
- <span data-ttu-id="a88f8-209">C5</span><span class="sxs-lookup"><span data-stu-id="a88f8-209">C5</span></span>
- <span data-ttu-id="a88f8-210">C6</span><span class="sxs-lookup"><span data-stu-id="a88f8-210">C6</span></span>
- <span data-ttu-id="a88f8-211">250MB</span><span class="sxs-lookup"><span data-stu-id="a88f8-211">250MB</span></span>
- <span data-ttu-id="a88f8-212">1GB</span><span class="sxs-lookup"><span data-stu-id="a88f8-212">1GB</span></span>
- <span data-ttu-id="a88f8-213">2.5GB</span><span class="sxs-lookup"><span data-stu-id="a88f8-213">2.5GB</span></span>
- <span data-ttu-id="a88f8-214">6GB</span><span class="sxs-lookup"><span data-stu-id="a88f8-214">6GB</span></span>
- <span data-ttu-id="a88f8-215">13GB</span><span class="sxs-lookup"><span data-stu-id="a88f8-215">13GB</span></span>
- <span data-ttu-id="a88f8-216">26GB</span><span class="sxs-lookup"><span data-stu-id="a88f8-216">26GB</span></span>
- <span data-ttu-id="a88f8-217">53GB 기본값은 1GB 또는 C1입니다.</span><span class="sxs-lookup"><span data-stu-id="a88f8-217">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="a88f8-218">-Sku</span><span class="sxs-lookup"><span data-stu-id="a88f8-218">-Sku</span></span>
<span data-ttu-id="a88f8-219">만들 Redis Cache의 SKU를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a88f8-219">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="a88f8-220">유효한 값은</span><span class="sxs-lookup"><span data-stu-id="a88f8-220">Valid values are:</span></span> 
- <span data-ttu-id="a88f8-221">기본</span><span class="sxs-lookup"><span data-stu-id="a88f8-221">Basic</span></span>
- <span data-ttu-id="a88f8-222">표준</span><span class="sxs-lookup"><span data-stu-id="a88f8-222">Standard</span></span>
- <span data-ttu-id="a88f8-223">Premium 기본값은 Standard입니다.</span><span class="sxs-lookup"><span data-stu-id="a88f8-223">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="a88f8-224">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="a88f8-224">-StaticIP</span></span>
<span data-ttu-id="a88f8-225">Redis Cache에 대한 서브넷의 고유한 IP 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a88f8-225">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>
<span data-ttu-id="a88f8-226">이 매개 변수에 대한 값을 지정하지 않으면 이 cmdlet은 서브넷에서 IP 주소를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="a88f8-226">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="a88f8-227">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="a88f8-227">-SubnetId</span></span>
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

### <span data-ttu-id="a88f8-228">-Tag</span><span class="sxs-lookup"><span data-stu-id="a88f8-228">-Tag</span></span>
<span data-ttu-id="a88f8-229">태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="a88f8-229">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="a88f8-230">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="a88f8-230">-TenantSettings</span></span>
<span data-ttu-id="a88f8-231">이 매개 변수는 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a88f8-231">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="a88f8-232">-Zone</span><span class="sxs-lookup"><span data-stu-id="a88f8-232">-Zone</span></span>
<span data-ttu-id="a88f8-233">영역 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="a88f8-233">List of zones.</span></span>

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

### <span data-ttu-id="a88f8-234">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a88f8-234">-Confirm</span></span>
<span data-ttu-id="a88f8-235">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a88f8-235">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a88f8-236">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a88f8-236">-WhatIf</span></span>
<span data-ttu-id="a88f8-237">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a88f8-237">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a88f8-238">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a88f8-238">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a88f8-239">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a88f8-239">CommonParameters</span></span>
<span data-ttu-id="a88f8-240">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a88f8-240">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a88f8-241">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a88f8-241">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a88f8-242">입력</span><span class="sxs-lookup"><span data-stu-id="a88f8-242">INPUTS</span></span>

### <span data-ttu-id="a88f8-243">System.String</span><span class="sxs-lookup"><span data-stu-id="a88f8-243">System.String</span></span>

### <span data-ttu-id="a88f8-244">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="a88f8-244">System.Collections.Hashtable</span></span>

### <span data-ttu-id="a88f8-245">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a88f8-245">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a88f8-246">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a88f8-246">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a88f8-247">System.String[]</span><span class="sxs-lookup"><span data-stu-id="a88f8-247">System.String[]</span></span>

## <span data-ttu-id="a88f8-248">출력</span><span class="sxs-lookup"><span data-stu-id="a88f8-248">OUTPUTS</span></span>

### <span data-ttu-id="a88f8-249">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="a88f8-249">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="a88f8-250">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a88f8-250">NOTES</span></span>

## <span data-ttu-id="a88f8-251">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a88f8-251">RELATED LINKS</span></span>

[<span data-ttu-id="a88f8-252">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="a88f8-252">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="a88f8-253">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="a88f8-253">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="a88f8-254">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="a88f8-254">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


