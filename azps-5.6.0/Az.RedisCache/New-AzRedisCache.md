---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: 81179AFE-6524-4F59-8BC2-3E152F51D1DD
online version: https://docs.microsoft.com/powershell/module/az.rediscache/new-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/New-AzRedisCache.md
ms.openlocfilehash: 25469aa93f673d6a49bbbaa54fcaf22a91019d9a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997369"
---
# <span data-ttu-id="16e4c-101">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="16e4c-101">New-AzRedisCache</span></span>

## <span data-ttu-id="16e4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16e4c-102">SYNOPSIS</span></span>
<span data-ttu-id="16e4c-103">Redis Cache를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="16e4c-103">Creates a Redis Cache.</span></span>

## <span data-ttu-id="16e4c-104">구문</span><span class="sxs-lookup"><span data-stu-id="16e4c-104">SYNTAX</span></span>

```
New-AzRedisCache -ResourceGroupName <String> -Name <String> -Location <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-MinimumTlsVersion <String>] [-SubnetId <String>] [-StaticIP <String>]
 [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="16e4c-105">설명</span><span class="sxs-lookup"><span data-stu-id="16e4c-105">DESCRIPTION</span></span>
<span data-ttu-id="16e4c-106">**New-AzRedisCache** cmdlet은 Azure Redis Cache를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="16e4c-106">The **New-AzRedisCache** cmdlet creates an Azure Redis Cache.</span></span>

## <span data-ttu-id="16e4c-107">예제</span><span class="sxs-lookup"><span data-stu-id="16e4c-107">EXAMPLES</span></span>

### <span data-ttu-id="16e4c-108">예제 1: Redis Cache 만들기</span><span class="sxs-lookup"><span data-stu-id="16e4c-108">Example 1: Create a Redis Cache</span></span>
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

<span data-ttu-id="16e4c-109">이 명령은 Redis Cache를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="16e4c-109">This command creates a Redis Cache.</span></span>

### <span data-ttu-id="16e4c-110">예제 2: 표준 SKU Redis Cache 만들기</span><span class="sxs-lookup"><span data-stu-id="16e4c-110">Example 2: Create a Standard SKU Redis Cache</span></span>
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

<span data-ttu-id="16e4c-111">이 명령은 Redis Cache를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="16e4c-111">This command creates a Redis Cache.</span></span>

## <span data-ttu-id="16e4c-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="16e4c-112">PARAMETERS</span></span>

### <span data-ttu-id="16e4c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16e4c-113">-DefaultProfile</span></span>
<span data-ttu-id="16e4c-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="16e4c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16e4c-115">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="16e4c-115">-EnableNonSslPort</span></span>
<span data-ttu-id="16e4c-116">비 SSL 포트를 사용하도록 설정되어 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="16e4c-116">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="16e4c-117">기본값은 $False(비 SSL 포트를 사용하지 않도록 설정)입니다.</span><span class="sxs-lookup"><span data-stu-id="16e4c-117">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="16e4c-118">-Location</span><span class="sxs-lookup"><span data-stu-id="16e4c-118">-Location</span></span>
<span data-ttu-id="16e4c-119">Redis Cache를 만들 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="16e4c-119">Specifies the location in which to create a Redis Cache.</span></span>
<span data-ttu-id="16e4c-120">유효한 값은:</span><span class="sxs-lookup"><span data-stu-id="16e4c-120">Valid values are:</span></span> 
- <span data-ttu-id="16e4c-121">미국 중북부</span><span class="sxs-lookup"><span data-stu-id="16e4c-121">North Central US</span></span>
- <span data-ttu-id="16e4c-122">미국 중남부</span><span class="sxs-lookup"><span data-stu-id="16e4c-122">South Central US</span></span>
- <span data-ttu-id="16e4c-123">미국 중부</span><span class="sxs-lookup"><span data-stu-id="16e4c-123">Central US</span></span>
- <span data-ttu-id="16e4c-124">유럽 서부</span><span class="sxs-lookup"><span data-stu-id="16e4c-124">West Europe</span></span>
- <span data-ttu-id="16e4c-125">북유럽</span><span class="sxs-lookup"><span data-stu-id="16e4c-125">North Europe</span></span>
- <span data-ttu-id="16e4c-126">미국 서부</span><span class="sxs-lookup"><span data-stu-id="16e4c-126">West US</span></span>
- <span data-ttu-id="16e4c-127">미국 동부</span><span class="sxs-lookup"><span data-stu-id="16e4c-127">East US</span></span>
- <span data-ttu-id="16e4c-128">미국 동부 2</span><span class="sxs-lookup"><span data-stu-id="16e4c-128">East US 2</span></span>
- <span data-ttu-id="16e4c-129">일본 동부</span><span class="sxs-lookup"><span data-stu-id="16e4c-129">Japan East</span></span>
- <span data-ttu-id="16e4c-130">일본 서부</span><span class="sxs-lookup"><span data-stu-id="16e4c-130">Japan West</span></span>
- <span data-ttu-id="16e4c-131">브라질 남부</span><span class="sxs-lookup"><span data-stu-id="16e4c-131">Brazil South</span></span>
- <span data-ttu-id="16e4c-132">동남 아시아</span><span class="sxs-lookup"><span data-stu-id="16e4c-132">Southeast Asia</span></span>
- <span data-ttu-id="16e4c-133">동아시아</span><span class="sxs-lookup"><span data-stu-id="16e4c-133">East Asia</span></span>
- <span data-ttu-id="16e4c-134">오스트레일리아 동부</span><span class="sxs-lookup"><span data-stu-id="16e4c-134">Australia East</span></span>
- <span data-ttu-id="16e4c-135">오스트레일리아 남동부</span><span class="sxs-lookup"><span data-stu-id="16e4c-135">Australia Southeast</span></span>

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

### <span data-ttu-id="16e4c-136">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="16e4c-136">-MinimumTlsVersion</span></span>
<span data-ttu-id="16e4c-137">캐시에 연결하는 데 필요한 TLS 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="16e4c-137">Specify the TLS version required by clients to connect to cache.</span></span>

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

### <span data-ttu-id="16e4c-138">-Name</span><span class="sxs-lookup"><span data-stu-id="16e4c-138">-Name</span></span>
<span data-ttu-id="16e4c-139">만들 Redis Cache의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="16e4c-139">Specifies the name of the Redis Cache to create.</span></span>

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

### <span data-ttu-id="16e4c-140">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="16e4c-140">-RedisConfiguration</span></span>
<span data-ttu-id="16e4c-141">Redis 구성 설정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="16e4c-141">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="16e4c-142">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="16e4c-142">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="16e4c-143">rdb-backup을 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="16e4c-143">rdb-backup-enabled.</span></span>
<span data-ttu-id="16e4c-144">Redis 데이터 지속성이 사용하도록 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="16e4c-144">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="16e4c-145">프리미엄 계층만 해당합니다.</span><span class="sxs-lookup"><span data-stu-id="16e4c-145">Premium tier only.</span></span>
- <span data-ttu-id="16e4c-146">rdb-storage-connection-string.</span><span class="sxs-lookup"><span data-stu-id="16e4c-146">rdb-storage-connection-string.</span></span>
<span data-ttu-id="16e4c-147">Redis 데이터 지속성에 대한 Storage 계정에 대한 연결 문자열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="16e4c-147">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="16e4c-148">프리미엄 계층만 해당합니다.</span><span class="sxs-lookup"><span data-stu-id="16e4c-148">Premium tier only.</span></span>
- <span data-ttu-id="16e4c-149">rdb-backup-frequency.</span><span class="sxs-lookup"><span data-stu-id="16e4c-149">rdb-backup-frequency.</span></span>
<span data-ttu-id="16e4c-150">Redis 데이터 지속성에 대한 백업 빈도를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="16e4c-150">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="16e4c-151">프리미엄 계층만 해당합니다.</span><span class="sxs-lookup"><span data-stu-id="16e4c-151">Premium tier only.</span></span> 
- <span data-ttu-id="16e4c-152">maxmemory-reserved.</span><span class="sxs-lookup"><span data-stu-id="16e4c-152">maxmemory-reserved.</span></span>
<span data-ttu-id="16e4c-153">캐시가 아닌 프로세스에 대해 예약된 메모리를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="16e4c-153">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="16e4c-154">표준 및 프리미엄 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="16e4c-154">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="16e4c-155">maxmemory-policy.</span><span class="sxs-lookup"><span data-stu-id="16e4c-155">maxmemory-policy.</span></span>
<span data-ttu-id="16e4c-156">캐시에 대한 삭제 정책을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="16e4c-156">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="16e4c-157">모든 가격 책정 계층.</span><span class="sxs-lookup"><span data-stu-id="16e4c-157">All pricing tiers.</span></span> 
- <span data-ttu-id="16e4c-158">notify-keyspace-events.</span><span class="sxs-lookup"><span data-stu-id="16e4c-158">notify-keyspace-events.</span></span>
<span data-ttu-id="16e4c-159">키스페이스 알림을 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="16e4c-159">Configures keyspace notifications.</span></span>
<span data-ttu-id="16e4c-160">표준 및 프리미엄 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="16e4c-160">Standard and premium tiers.</span></span> 
- <span data-ttu-id="16e4c-161">hash-max-ziplist-entries.</span><span class="sxs-lookup"><span data-stu-id="16e4c-161">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="16e4c-162">작은 집계 데이터 형식에 대한 메모리 최적화를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="16e4c-162">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="16e4c-163">표준 및 프리미엄 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="16e4c-163">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="16e4c-164">해시-max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="16e4c-164">hash-max-ziplist-value.</span></span>
<span data-ttu-id="16e4c-165">작은 집계 데이터 형식에 대한 메모리 최적화를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="16e4c-165">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="16e4c-166">표준 및 프리미엄 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="16e4c-166">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="16e4c-167">set-max-intset-entries.</span><span class="sxs-lookup"><span data-stu-id="16e4c-167">set-max-intset-entries.</span></span>
<span data-ttu-id="16e4c-168">작은 집계 데이터 형식에 대한 메모리 최적화를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="16e4c-168">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="16e4c-169">표준 및 프리미엄 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="16e4c-169">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="16e4c-170">zset-max-ziplist-entries.</span><span class="sxs-lookup"><span data-stu-id="16e4c-170">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="16e4c-171">작은 집계 데이터 형식에 대한 메모리 최적화를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="16e4c-171">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="16e4c-172">표준 및 프리미엄 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="16e4c-172">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="16e4c-173">zset-max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="16e4c-173">zset-max-ziplist-value.</span></span>
<span data-ttu-id="16e4c-174">작은 집계 데이터 형식에 대한 메모리 최적화를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="16e4c-174">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="16e4c-175">표준 및 프리미엄 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="16e4c-175">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="16e4c-176">데이터베이스.</span><span class="sxs-lookup"><span data-stu-id="16e4c-176">databases.</span></span>
<span data-ttu-id="16e4c-177">데이터베이스 수를 구성합니다.</span><span class="sxs-lookup"><span data-stu-id="16e4c-177">Configures the number of databases.</span></span>
<span data-ttu-id="16e4c-178">이 속성은 캐시를 만들 때만 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16e4c-178">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="16e4c-179">표준 및 프리미엄 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="16e4c-179">Standard and Premium tiers.</span></span>
<span data-ttu-id="16e4c-180">자세한 내용은 Azure PowerShell을 사용하여 Azure Redis Cache 관리를 http://go.microsoft.com/fwlink/?LinkId=800051 http://go.microsoft.com/fwlink/?LinkId=800051) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="16e4c-180">For more information, see Manage Azure Redis Cache with Azure PowerShellhttp://go.microsoft.com/fwlink/?LinkId=800051 (http://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="16e4c-181">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16e4c-181">-ResourceGroupName</span></span>
<span data-ttu-id="16e4c-182">Redis Cache를 만들 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="16e4c-182">Specifies the name of the resource group in which to create the Redis Cache.</span></span>

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

### <span data-ttu-id="16e4c-183">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="16e4c-183">-ShardCount</span></span>
<span data-ttu-id="16e4c-184">Premium 클러스터 캐시에서 만들 수 있는 샤드 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="16e4c-184">Specifies the number of shards to create on a Premium cluster cache.</span></span>
<span data-ttu-id="16e4c-185">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="16e4c-185">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="16e4c-186">1</span><span class="sxs-lookup"><span data-stu-id="16e4c-186">1</span></span>
- <span data-ttu-id="16e4c-187">2</span><span class="sxs-lookup"><span data-stu-id="16e4c-187">2</span></span>
- <span data-ttu-id="16e4c-188">3</span><span class="sxs-lookup"><span data-stu-id="16e4c-188">3</span></span>
- <span data-ttu-id="16e4c-189">4</span><span class="sxs-lookup"><span data-stu-id="16e4c-189">4</span></span>
- <span data-ttu-id="16e4c-190">5</span><span class="sxs-lookup"><span data-stu-id="16e4c-190">5</span></span>
- <span data-ttu-id="16e4c-191">6</span><span class="sxs-lookup"><span data-stu-id="16e4c-191">6</span></span>
- <span data-ttu-id="16e4c-192">7</span><span class="sxs-lookup"><span data-stu-id="16e4c-192">7</span></span>
- <span data-ttu-id="16e4c-193">8</span><span class="sxs-lookup"><span data-stu-id="16e4c-193">8</span></span>
- <span data-ttu-id="16e4c-194">9</span><span class="sxs-lookup"><span data-stu-id="16e4c-194">9</span></span> 
- <span data-ttu-id="16e4c-195">10</span><span class="sxs-lookup"><span data-stu-id="16e4c-195">10</span></span>

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

### <span data-ttu-id="16e4c-196">-Size</span><span class="sxs-lookup"><span data-stu-id="16e4c-196">-Size</span></span>
<span data-ttu-id="16e4c-197">Redis Cache의 크기를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="16e4c-197">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="16e4c-198">유효한 값은:</span><span class="sxs-lookup"><span data-stu-id="16e4c-198">Valid values are:</span></span> 
- <span data-ttu-id="16e4c-199">P1</span><span class="sxs-lookup"><span data-stu-id="16e4c-199">P1</span></span>
- <span data-ttu-id="16e4c-200">P2</span><span class="sxs-lookup"><span data-stu-id="16e4c-200">P2</span></span>
- <span data-ttu-id="16e4c-201">P3</span><span class="sxs-lookup"><span data-stu-id="16e4c-201">P3</span></span>
- <span data-ttu-id="16e4c-202">P4</span><span class="sxs-lookup"><span data-stu-id="16e4c-202">P4</span></span>
- <span data-ttu-id="16e4c-203">P5</span><span class="sxs-lookup"><span data-stu-id="16e4c-203">P5</span></span>
- <span data-ttu-id="16e4c-204">C0</span><span class="sxs-lookup"><span data-stu-id="16e4c-204">C0</span></span>
- <span data-ttu-id="16e4c-205">C1</span><span class="sxs-lookup"><span data-stu-id="16e4c-205">C1</span></span>
- <span data-ttu-id="16e4c-206">C2</span><span class="sxs-lookup"><span data-stu-id="16e4c-206">C2</span></span>
- <span data-ttu-id="16e4c-207">C3</span><span class="sxs-lookup"><span data-stu-id="16e4c-207">C3</span></span>
- <span data-ttu-id="16e4c-208">C4</span><span class="sxs-lookup"><span data-stu-id="16e4c-208">C4</span></span>
- <span data-ttu-id="16e4c-209">C5</span><span class="sxs-lookup"><span data-stu-id="16e4c-209">C5</span></span>
- <span data-ttu-id="16e4c-210">C6</span><span class="sxs-lookup"><span data-stu-id="16e4c-210">C6</span></span>
- <span data-ttu-id="16e4c-211">250MB</span><span class="sxs-lookup"><span data-stu-id="16e4c-211">250MB</span></span>
- <span data-ttu-id="16e4c-212">1GB</span><span class="sxs-lookup"><span data-stu-id="16e4c-212">1GB</span></span>
- <span data-ttu-id="16e4c-213">2.5GB</span><span class="sxs-lookup"><span data-stu-id="16e4c-213">2.5GB</span></span>
- <span data-ttu-id="16e4c-214">6GB</span><span class="sxs-lookup"><span data-stu-id="16e4c-214">6GB</span></span>
- <span data-ttu-id="16e4c-215">13GB</span><span class="sxs-lookup"><span data-stu-id="16e4c-215">13GB</span></span>
- <span data-ttu-id="16e4c-216">26GB</span><span class="sxs-lookup"><span data-stu-id="16e4c-216">26GB</span></span>
- <span data-ttu-id="16e4c-217">53GB 기본값은 1GB 또는 C1입니다.</span><span class="sxs-lookup"><span data-stu-id="16e4c-217">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="16e4c-218">-Sku</span><span class="sxs-lookup"><span data-stu-id="16e4c-218">-Sku</span></span>
<span data-ttu-id="16e4c-219">만들 Redis Cache의 SKU를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="16e4c-219">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="16e4c-220">유효한 값은:</span><span class="sxs-lookup"><span data-stu-id="16e4c-220">Valid values are:</span></span> 
- <span data-ttu-id="16e4c-221">기본</span><span class="sxs-lookup"><span data-stu-id="16e4c-221">Basic</span></span>
- <span data-ttu-id="16e4c-222">표준</span><span class="sxs-lookup"><span data-stu-id="16e4c-222">Standard</span></span>
- <span data-ttu-id="16e4c-223">Premium 기본값은 Standard입니다.</span><span class="sxs-lookup"><span data-stu-id="16e4c-223">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="16e4c-224">-StaticIP</span><span class="sxs-lookup"><span data-stu-id="16e4c-224">-StaticIP</span></span>
<span data-ttu-id="16e4c-225">Redis Cache의 서브넷에 고유한 IP 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="16e4c-225">Specifies a unique IP address in the subnet for the Redis Cache.</span></span>
<span data-ttu-id="16e4c-226">이 매개 변수에 대한 값을 지정하지 않으면 이 cmdlet은 서브넷에서 IP 주소를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="16e4c-226">If you do not specify a value for this parameter, this cmdlet chooses an IP address from the subnet.</span></span>

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

### <span data-ttu-id="16e4c-227">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="16e4c-227">-SubnetId</span></span>
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

### <span data-ttu-id="16e4c-228">-Tag</span><span class="sxs-lookup"><span data-stu-id="16e4c-228">-Tag</span></span>
<span data-ttu-id="16e4c-229">태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="16e4c-229">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="16e4c-230">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="16e4c-230">-TenantSettings</span></span>
<span data-ttu-id="16e4c-231">이 매개 변수는 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="16e4c-231">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="16e4c-232">-Zone</span><span class="sxs-lookup"><span data-stu-id="16e4c-232">-Zone</span></span>
<span data-ttu-id="16e4c-233">영역 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="16e4c-233">List of zones.</span></span>

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

### <span data-ttu-id="16e4c-234">-확인</span><span class="sxs-lookup"><span data-stu-id="16e4c-234">-Confirm</span></span>
<span data-ttu-id="16e4c-235">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="16e4c-235">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16e4c-236">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16e4c-236">-WhatIf</span></span>
<span data-ttu-id="16e4c-237">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="16e4c-237">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="16e4c-238">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="16e4c-238">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16e4c-239">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16e4c-239">CommonParameters</span></span>
<span data-ttu-id="16e4c-240">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="16e4c-240">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16e4c-241">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="16e4c-241">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16e4c-242">입력</span><span class="sxs-lookup"><span data-stu-id="16e4c-242">INPUTS</span></span>

### <span data-ttu-id="16e4c-243">System.String</span><span class="sxs-lookup"><span data-stu-id="16e4c-243">System.String</span></span>

### <span data-ttu-id="16e4c-244">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="16e4c-244">System.Collections.Hashtable</span></span>

### <span data-ttu-id="16e4c-245">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="16e4c-245">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="16e4c-246">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="16e4c-246">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="16e4c-247">System.String[]</span><span class="sxs-lookup"><span data-stu-id="16e4c-247">System.String[]</span></span>

## <span data-ttu-id="16e4c-248">출력</span><span class="sxs-lookup"><span data-stu-id="16e4c-248">OUTPUTS</span></span>

### <span data-ttu-id="16e4c-249">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span><span class="sxs-lookup"><span data-stu-id="16e4c-249">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="16e4c-250">참고 사항</span><span class="sxs-lookup"><span data-stu-id="16e4c-250">NOTES</span></span>

## <span data-ttu-id="16e4c-251">관련 링크</span><span class="sxs-lookup"><span data-stu-id="16e4c-251">RELATED LINKS</span></span>

[<span data-ttu-id="16e4c-252">Get-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="16e4c-252">Get-AzRedisCache</span></span>](./Get-AzRedisCache.md)

[<span data-ttu-id="16e4c-253">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="16e4c-253">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="16e4c-254">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="16e4c-254">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


