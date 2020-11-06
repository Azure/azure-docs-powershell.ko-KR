---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: 6234F211-6ED4-443F-9B83-DEB9AC51B763
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/set-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Set-AzureRmRedisCache.md
ms.openlocfilehash: 484c72dd77ada862536b064cb2bcaec07ef51bb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535655"
---
# <span data-ttu-id="2fc70-101">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="2fc70-101">Set-AzureRmRedisCache</span></span>

## <span data-ttu-id="2fc70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2fc70-102">SYNOPSIS</span></span>
<span data-ttu-id="2fc70-103">Redis 캐시를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc70-103">Modifies a Redis Cache.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2fc70-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2fc70-104">SYNTAX</span></span>

```
Set-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> [-Size <String>] [-Sku <String>]
 [-RedisConfiguration <Hashtable>] [-EnableNonSslPort <Boolean>] [-TenantSettings <Hashtable>]
 [-ShardCount <Int32>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2fc70-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2fc70-105">DESCRIPTION</span></span>
<span data-ttu-id="2fc70-106">**Set-AzureRmRedisCache** Cmdlet은 Azure Redis Cache를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc70-106">The **Set-AzureRmRedisCache** cmdlet modifies an Azure Redis Cache.</span></span>

## <span data-ttu-id="2fc70-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2fc70-107">EXAMPLES</span></span>

### <span data-ttu-id="2fc70-108">예제 1: Redis 캐시 수정</span><span class="sxs-lookup"><span data-stu-id="2fc70-108">Example 1: Modify a Redis Cache</span></span>
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

<span data-ttu-id="2fc70-109">이 명령은 MyCache 라는 Redis Cache에 대 한 maxmemory 정책을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc70-109">This command updates the maxmemory-policy for the Redis Cache named MyCache.</span></span>

## <span data-ttu-id="2fc70-110">변수</span><span class="sxs-lookup"><span data-stu-id="2fc70-110">PARAMETERS</span></span>

### <span data-ttu-id="2fc70-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fc70-111">-DefaultProfile</span></span>
<span data-ttu-id="2fc70-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2fc70-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2fc70-113">-EnableNonSslPort</span><span class="sxs-lookup"><span data-stu-id="2fc70-113">-EnableNonSslPort</span></span>
<span data-ttu-id="2fc70-114">비 SSL 포트를 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2fc70-114">Indicates whether the non-SSL port is enabled.</span></span>
<span data-ttu-id="2fc70-115">기본값은 $False (비 SSL 포트를 사용할 수 없음)입니다.</span><span class="sxs-lookup"><span data-stu-id="2fc70-115">The default value is $False (the non-SSL port is disabled).</span></span>

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

### <span data-ttu-id="2fc70-116">-이름</span><span class="sxs-lookup"><span data-stu-id="2fc70-116">-Name</span></span>
<span data-ttu-id="2fc70-117">업데이트할 Redis 캐시의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc70-117">Specifies the name of the Redis Cache to update.</span></span>

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

### <span data-ttu-id="2fc70-118">-RedisConfiguration</span><span class="sxs-lookup"><span data-stu-id="2fc70-118">-RedisConfiguration</span></span>
<span data-ttu-id="2fc70-119">Redis 구성 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc70-119">Specifies Redis configuration settings.</span></span>
<span data-ttu-id="2fc70-120">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2fc70-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2fc70-121">rdb-백업-사용 가능.</span><span class="sxs-lookup"><span data-stu-id="2fc70-121">rdb-backup-enabled.</span></span>
<span data-ttu-id="2fc70-122">Redis 데이터 지 속성을 사용 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc70-122">Specifies that Redis data persistence is enabled.</span></span>
<span data-ttu-id="2fc70-123">프리미엄 계층만.</span><span class="sxs-lookup"><span data-stu-id="2fc70-123">Premium tier only.</span></span>
- <span data-ttu-id="2fc70-124">rdb-저장소-연결 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="2fc70-124">rdb-storage-connection-string.</span></span>
<span data-ttu-id="2fc70-125">Redis 데이터 지 속성에 대 한 저장소 계정에 대 한 연결 문자열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc70-125">Specifies the connection string to the Storage account for Redis data persistence.</span></span>
<span data-ttu-id="2fc70-126">프리미엄 계층만.</span><span class="sxs-lookup"><span data-stu-id="2fc70-126">Premium tier only.</span></span>
- <span data-ttu-id="2fc70-127">rdb-백업-빈도</span><span class="sxs-lookup"><span data-stu-id="2fc70-127">rdb-backup-frequency.</span></span>
<span data-ttu-id="2fc70-128">Redis 데이터 지 속성에 대 한 백업 빈도를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc70-128">Specifies the backup frequency for Redis data persistence.</span></span>
<span data-ttu-id="2fc70-129">프리미엄 계층만.</span><span class="sxs-lookup"><span data-stu-id="2fc70-129">Premium tier only.</span></span> 
- <span data-ttu-id="2fc70-130">maxmemory-예약 됨.</span><span class="sxs-lookup"><span data-stu-id="2fc70-130">maxmemory-reserved.</span></span>
<span data-ttu-id="2fc70-131">비 캐시 프로세스에 예약 된 메모리를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc70-131">Configures the memory reserved for non-cache processes.</span></span>
<span data-ttu-id="2fc70-132">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="2fc70-132">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="2fc70-133">maxmemory-정책.</span><span class="sxs-lookup"><span data-stu-id="2fc70-133">maxmemory-policy.</span></span>
<span data-ttu-id="2fc70-134">캐시에 대 한 제거 정책을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc70-134">Configures the eviction policy for the cache.</span></span>
<span data-ttu-id="2fc70-135">모든 가격 책정 계층</span><span class="sxs-lookup"><span data-stu-id="2fc70-135">All pricing tiers.</span></span> 
- <span data-ttu-id="2fc70-136">notify-keyspace-이벤트</span><span class="sxs-lookup"><span data-stu-id="2fc70-136">notify-keyspace-events.</span></span>
<span data-ttu-id="2fc70-137">Keyspace 알림을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc70-137">Configures keyspace notifications.</span></span>
<span data-ttu-id="2fc70-138">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="2fc70-138">Standard and premium tiers.</span></span> 
- <span data-ttu-id="2fc70-139">hash-최대 ziplist-항목.</span><span class="sxs-lookup"><span data-stu-id="2fc70-139">hash-max-ziplist-entries.</span></span>
<span data-ttu-id="2fc70-140">작은 집계 데이터 형식에 대 한 메모리 최적화를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc70-140">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="2fc70-141">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="2fc70-141">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="2fc70-142">hash-max-ziplist-값.</span><span class="sxs-lookup"><span data-stu-id="2fc70-142">hash-max-ziplist-value.</span></span>
<span data-ttu-id="2fc70-143">작은 집계 데이터 형식에 대 한 메모리 최적화를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc70-143">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="2fc70-144">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="2fc70-144">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="2fc70-145">set-max-intset-항목</span><span class="sxs-lookup"><span data-stu-id="2fc70-145">set-max-intset-entries.</span></span>
<span data-ttu-id="2fc70-146">작은 집계 데이터 형식에 대 한 메모리 최적화를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc70-146">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="2fc70-147">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="2fc70-147">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="2fc70-148">zset-max-ziplist 항목.</span><span class="sxs-lookup"><span data-stu-id="2fc70-148">zset-max-ziplist-entries.</span></span>
<span data-ttu-id="2fc70-149">작은 집계 데이터 형식에 대 한 메모리 최적화를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc70-149">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="2fc70-150">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="2fc70-150">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="2fc70-151">zset-max-ziplist-value.</span><span class="sxs-lookup"><span data-stu-id="2fc70-151">zset-max-ziplist-value.</span></span>
<span data-ttu-id="2fc70-152">작은 집계 데이터 형식에 대 한 메모리 최적화를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc70-152">Configures memory optimization for small aggregate data types.</span></span>
<span data-ttu-id="2fc70-153">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="2fc70-153">Standard and Premium tiers.</span></span> 
- <span data-ttu-id="2fc70-154">databases.</span><span class="sxs-lookup"><span data-stu-id="2fc70-154">databases.</span></span>
<span data-ttu-id="2fc70-155">데이터베이스 수를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc70-155">Configures the number of databases.</span></span>
<span data-ttu-id="2fc70-156">이 속성은 캐시 생성 시에만 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2fc70-156">This property can be configured only at cache creation.</span></span>
<span data-ttu-id="2fc70-157">표준 및 프리미엄 계층.</span><span class="sxs-lookup"><span data-stu-id="2fc70-157">Standard and Premium tiers.</span></span>
<span data-ttu-id="2fc70-158">자세한 내용은 Azure PowerShell을 사용 하 여 Azure Redis 캐시 관리 https://go.microsoft.com/fwlink/?LinkId=800051 ()를 참조 하세요 https://go.microsoft.com/fwlink/?LinkId=800051) .</span><span class="sxs-lookup"><span data-stu-id="2fc70-158">For more information, see Manage Azure Redis Cache with Azure PowerShellhttps://go.microsoft.com/fwlink/?LinkId=800051 (https://go.microsoft.com/fwlink/?LinkId=800051).</span></span>

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

### <span data-ttu-id="2fc70-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fc70-159">-ResourceGroupName</span></span>
<span data-ttu-id="2fc70-160">Redis 캐시를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc70-160">Specifies the name of the resource group that contains the Redis Cache.</span></span>

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

### <span data-ttu-id="2fc70-161">-ShardCount</span><span class="sxs-lookup"><span data-stu-id="2fc70-161">-ShardCount</span></span>
<span data-ttu-id="2fc70-162">프리미엄 클러스터 캐시에서 만들 shards 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc70-162">Specifies the number of shards to create on a Premium cluster cache.</span></span>

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

### <span data-ttu-id="2fc70-163">-크기</span><span class="sxs-lookup"><span data-stu-id="2fc70-163">-Size</span></span>
<span data-ttu-id="2fc70-164">Redis 캐시의 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc70-164">Specifies the size of the Redis Cache.</span></span>
<span data-ttu-id="2fc70-165">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2fc70-165">Valid values are:</span></span> 
- <span data-ttu-id="2fc70-166">P1</span><span class="sxs-lookup"><span data-stu-id="2fc70-166">P1</span></span>
- <span data-ttu-id="2fc70-167">즉</span><span class="sxs-lookup"><span data-stu-id="2fc70-167">P2</span></span>
- <span data-ttu-id="2fc70-168">P3</span><span class="sxs-lookup"><span data-stu-id="2fc70-168">P3</span></span>
- <span data-ttu-id="2fc70-169">P4</span><span class="sxs-lookup"><span data-stu-id="2fc70-169">P4</span></span>
- <span data-ttu-id="2fc70-170">C0</span><span class="sxs-lookup"><span data-stu-id="2fc70-170">C0</span></span>
- <span data-ttu-id="2fc70-171">C1</span><span class="sxs-lookup"><span data-stu-id="2fc70-171">C1</span></span>
- <span data-ttu-id="2fc70-172">만족할</span><span class="sxs-lookup"><span data-stu-id="2fc70-172">C2</span></span>
- <span data-ttu-id="2fc70-173">C3</span><span class="sxs-lookup"><span data-stu-id="2fc70-173">C3</span></span>
- <span data-ttu-id="2fc70-174">C4</span><span class="sxs-lookup"><span data-stu-id="2fc70-174">C4</span></span>
- <span data-ttu-id="2fc70-175">C 5</span><span class="sxs-lookup"><span data-stu-id="2fc70-175">C5</span></span>
- <span data-ttu-id="2fc70-176">C6</span><span class="sxs-lookup"><span data-stu-id="2fc70-176">C6</span></span>
- <span data-ttu-id="2fc70-177">250MB</span><span class="sxs-lookup"><span data-stu-id="2fc70-177">250MB</span></span>
- <span data-ttu-id="2fc70-178">1GB</span><span class="sxs-lookup"><span data-stu-id="2fc70-178">1GB</span></span>
- <span data-ttu-id="2fc70-179">2.5 GB</span><span class="sxs-lookup"><span data-stu-id="2fc70-179">2.5GB</span></span>
- <span data-ttu-id="2fc70-180">6GB</span><span class="sxs-lookup"><span data-stu-id="2fc70-180">6GB</span></span>
- <span data-ttu-id="2fc70-181">13GB</span><span class="sxs-lookup"><span data-stu-id="2fc70-181">13GB</span></span>
- <span data-ttu-id="2fc70-182">26GB</span><span class="sxs-lookup"><span data-stu-id="2fc70-182">26GB</span></span>
- <span data-ttu-id="2fc70-183">53GB 기본 값은 1GB 또는 C1입니다.</span><span class="sxs-lookup"><span data-stu-id="2fc70-183">53GB The default value is 1GB or C1.</span></span>

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

### <span data-ttu-id="2fc70-184">-Sku</span><span class="sxs-lookup"><span data-stu-id="2fc70-184">-Sku</span></span>
<span data-ttu-id="2fc70-185">만들 Redis Cache의 SKU를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc70-185">Specifies the SKU of the Redis Cache to create.</span></span>
<span data-ttu-id="2fc70-186">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2fc70-186">Valid values are:</span></span> 
- <span data-ttu-id="2fc70-187">기본적</span><span class="sxs-lookup"><span data-stu-id="2fc70-187">Basic</span></span>
- <span data-ttu-id="2fc70-188">표준이</span><span class="sxs-lookup"><span data-stu-id="2fc70-188">Standard</span></span>
- <span data-ttu-id="2fc70-189">Premium 기본 값은 표준입니다.</span><span class="sxs-lookup"><span data-stu-id="2fc70-189">Premium The default value is Standard.</span></span>

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

### <span data-ttu-id="2fc70-190">태그</span><span class="sxs-lookup"><span data-stu-id="2fc70-190">-Tag</span></span>
<span data-ttu-id="2fc70-191">태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="2fc70-191">A hash table which represents tags.</span></span>

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

### <span data-ttu-id="2fc70-192">-TenantSettings</span><span class="sxs-lookup"><span data-stu-id="2fc70-192">-TenantSettings</span></span>
<span data-ttu-id="2fc70-193">이 매개 변수는 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2fc70-193">This parameter has been deprecated.</span></span>

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

### <span data-ttu-id="2fc70-194">-확인</span><span class="sxs-lookup"><span data-stu-id="2fc70-194">-Confirm</span></span>
<span data-ttu-id="2fc70-195">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc70-195">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fc70-196">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fc70-196">-WhatIf</span></span>
<span data-ttu-id="2fc70-197">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2fc70-197">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2fc70-198">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2fc70-198">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fc70-199">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fc70-199">CommonParameters</span></span>
<span data-ttu-id="2fc70-200">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc70-200">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fc70-201">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fc70-201">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fc70-202">입력</span><span class="sxs-lookup"><span data-stu-id="2fc70-202">INPUTS</span></span>

### <span data-ttu-id="2fc70-203">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2fc70-203">System.String</span></span>

### <span data-ttu-id="2fc70-204">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="2fc70-204">System.Collections.Hashtable</span></span>

### <span data-ttu-id="2fc70-205">시스템 Null 허용 ' 1 [[b77a5c561934e089] [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken =]]</span><span class="sxs-lookup"><span data-stu-id="2fc70-205">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="2fc70-206">시스템 Null 허용 ' 1 [[b77a5c561934e089, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken =]]</span><span class="sxs-lookup"><span data-stu-id="2fc70-206">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="2fc70-207">출력</span><span class="sxs-lookup"><span data-stu-id="2fc70-207">OUTPUTS</span></span>

### <span data-ttu-id="2fc70-208">RedisCacheAttributesWithAccessKeys. 모델. m e.</span><span class="sxs-lookup"><span data-stu-id="2fc70-208">Microsoft.Azure.Commands.RedisCache.Models.RedisCacheAttributesWithAccessKeys</span></span>

## <span data-ttu-id="2fc70-209">상속자</span><span class="sxs-lookup"><span data-stu-id="2fc70-209">NOTES</span></span>

## <span data-ttu-id="2fc70-210">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2fc70-210">RELATED LINKS</span></span>

[<span data-ttu-id="2fc70-211">Get-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="2fc70-211">Get-AzureRmRedisCache</span></span>](./Get-AzureRmRedisCache.md)

[<span data-ttu-id="2fc70-212">새로운 AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="2fc70-212">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="2fc70-213">제거-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="2fc70-213">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)


