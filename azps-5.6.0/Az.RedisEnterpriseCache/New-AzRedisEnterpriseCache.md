---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/new-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/New-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/New-AzRedisEnterpriseCache.md
ms.openlocfilehash: 43ad21450666fb2db9a25e1e2803651eacf511d4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000763"
---
# <span data-ttu-id="aaa14-101">New-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="aaa14-101">New-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="aaa14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aaa14-102">SYNOPSIS</span></span>
<span data-ttu-id="aaa14-103">Redis Enterpise 캐시 클러스터 및 연결된 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aaa14-103">Creates a Redis Enterpise cache cluster and an associated database</span></span>

## <span data-ttu-id="aaa14-104">구문</span><span class="sxs-lookup"><span data-stu-id="aaa14-104">SYNTAX</span></span>

```
New-AzRedisEnterpriseCache -ClusterName <String> -ResourceGroupName <String> -Location <String> -Sku <SkuName>
 [-SubscriptionId <String>] [-Capacity <Int32>] [-ClientProtocol <Protocol>]
 [-ClusteringPolicy <ClusteringPolicy>] [-EvictionPolicy <EvictionPolicy>] [-MinimumTlsVersion <String>]
 [-Module <IModule[]>] [-Port <Int32>] [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="aaa14-105">설명</span><span class="sxs-lookup"><span data-stu-id="aaa14-105">DESCRIPTION</span></span>
<span data-ttu-id="aaa14-106">기존(잠재적 다운타임으로 덮어 작성/다시 생성) 캐시 클러스터 및 'default'라는 연결된 데이터베이스를 생성하거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="aaa14-106">Creates or updates an existing (overwrite/recreate, with potential downtime) cache cluster and an associated database named 'default'</span></span>

## <span data-ttu-id="aaa14-107">예제</span><span class="sxs-lookup"><span data-stu-id="aaa14-107">EXAMPLES</span></span>

### <span data-ttu-id="aaa14-108">예제 1: Redis Enterprise Cache 만들기</span><span class="sxs-lookup"><span data-stu-id="aaa14-108">Example 1: Create a Redis Enterprise Cache</span></span>
```powershell
PS C:\> New-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -Location "West US" -Sku "Enterprise_E10"

Location Name    Type                            Zone Database
-------- ----    ----                            ---- --------
West US  MyCache Microsoft.Cache/redisEnterprise      {default}

```

<span data-ttu-id="aaa14-109">이 명령은 MyCache라는 Redis Enterprise Cache를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aaa14-109">This command creates a Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="aaa14-110">예제 2: 일부 선택적 매개 변수를 사용하여 Redis Enterprise Cache 만들기</span><span class="sxs-lookup"><span data-stu-id="aaa14-110">Example 2: Create a Redis Enterprise Cache using some optional parameters</span></span>
```powershell
PS C:\> New-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -Location "East US" -Sku "Enterprise_E20" -Capacity 4 -Zone "1","2","3" -Module "{name:RedisBloom, args:`"ERROR_RATE 0.00 INITIAL_SIZE 400`"}","{name:RedisTimeSeries, args:`"RETENTION_POLICY 20`"}","{name:RediSearch}" -ClientProtocol "Plaintext" -EvictionPolicy "NoEviction" -ClusteringPolicy "EnterpriseCluster" -Tag @{"tag" = "value"}

Location Name    Type                            Zone      Database
-------- ----    ----                            ----      --------
East US  MyCache Microsoft.Cache/redisEnterprise {1, 2, 3} {default}

```

<span data-ttu-id="aaa14-111">이 명령은 몇 가지 선택적 매개 변수를 사용하여 MyCache라는 Redis Enterprise Cache를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aaa14-111">This command creates a Redis Enterprise Cache named MyCache using some optional parameters.</span></span>

## <span data-ttu-id="aaa14-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="aaa14-112">PARAMETERS</span></span>

### <span data-ttu-id="aaa14-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aaa14-113">-AsJob</span></span>
<span data-ttu-id="aaa14-114">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="aaa14-114">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaa14-115">-Capacity</span><span class="sxs-lookup"><span data-stu-id="aaa14-115">-Capacity</span></span>
<span data-ttu-id="aaa14-116">RedisEnterprise 클러스터의 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="aaa14-116">The size of the RedisEnterprise cluster.</span></span>
<span data-ttu-id="aaa14-117">SKU에 따라 기본값은 2 또는 3입니다.</span><span class="sxs-lookup"><span data-stu-id="aaa14-117">Defaults to 2 or 3 depending on SKU.</span></span>
<span data-ttu-id="aaa14-118">유효한 값은 Enterprise SKUS의 경우(2, 4, 6, ...) 및 Flash SKUS의 경우(3, 9, 15, ...)입니다.</span><span class="sxs-lookup"><span data-stu-id="aaa14-118">Valid values are (2, 4, 6, ...) for Enterprise SKUs and (3, 9, 15, ...) for Flash SKUs.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: SkuCapacity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaa14-119">-ClientProtocol</span><span class="sxs-lookup"><span data-stu-id="aaa14-119">-ClientProtocol</span></span>
<span data-ttu-id="aaa14-120">Redis 클라이언트가 TLS 암호화 또는 일반 텍스트 redis 프로토콜을 사용하여 연결할 수 있는지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aaa14-120">Specifies whether redis clients can connect using TLS-encrypted or plaintext redis protocols.</span></span>
<span data-ttu-id="aaa14-121">기본값은 TLS 암호화입니다.</span><span class="sxs-lookup"><span data-stu-id="aaa14-121">Default is TLS-encrypted.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.Protocol
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaa14-122">-ClusteringPolicy</span><span class="sxs-lookup"><span data-stu-id="aaa14-122">-ClusteringPolicy</span></span>
<span data-ttu-id="aaa14-123">클러스터링 정책 - 기본값은 OSSCluster입니다.</span><span class="sxs-lookup"><span data-stu-id="aaa14-123">Clustering policy - default is OSSCluster.</span></span>
<span data-ttu-id="aaa14-124">만들기 시 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="aaa14-124">Specified at create time.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.ClusteringPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaa14-125">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="aaa14-125">-ClusterName</span></span>
<span data-ttu-id="aaa14-126">RedisEnterprise 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aaa14-126">The name of the RedisEnterprise cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaa14-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaa14-127">-DefaultProfile</span></span>
<span data-ttu-id="aaa14-128">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aaa14-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaa14-129">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="aaa14-129">-EvictionPolicy</span></span>
<span data-ttu-id="aaa14-130">Redis eviction 정책 - 기본값은 VolatileLRU입니다.</span><span class="sxs-lookup"><span data-stu-id="aaa14-130">Redis eviction policy - default is VolatileLRU.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.EvictionPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaa14-131">-Location</span><span class="sxs-lookup"><span data-stu-id="aaa14-131">-Location</span></span>
<span data-ttu-id="aaa14-132">리소스가 있는 지리적 위치</span><span class="sxs-lookup"><span data-stu-id="aaa14-132">The geo-location where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaa14-133">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="aaa14-133">-MinimumTlsVersion</span></span>
<span data-ttu-id="aaa14-134">클러스터에서 지원할 최소 TLS 버전(예: 1.2)</span><span class="sxs-lookup"><span data-stu-id="aaa14-134">The minimum TLS version for the cluster to support, e.g. 1.2</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaa14-135">-Module</span><span class="sxs-lookup"><span data-stu-id="aaa14-135">-Module</span></span>
<span data-ttu-id="aaa14-136">이 데이터베이스에서 사용하도록 설정하는 선택적 redis 모듈 집합 - 모듈은 생성 시에만 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aaa14-136">Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
<span data-ttu-id="aaa14-137">생성을 위해 MODULE 속성에 대한 메모 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="aaa14-137">To construct, see NOTES section for MODULE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IModule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaa14-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="aaa14-138">-NoWait</span></span>
<span data-ttu-id="aaa14-139">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="aaa14-139">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaa14-140">-Port</span><span class="sxs-lookup"><span data-stu-id="aaa14-140">-Port</span></span>
<span data-ttu-id="aaa14-141">데이터베이스 엔드포인트의 TCP 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="aaa14-141">TCP port of the database endpoint.</span></span>
<span data-ttu-id="aaa14-142">만들기 시 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="aaa14-142">Specified at create time.</span></span>
<span data-ttu-id="aaa14-143">사용 가능한 포트를 기본값으로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aaa14-143">Defaults to an available port.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaa14-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aaa14-144">-ResourceGroupName</span></span>
<span data-ttu-id="aaa14-145">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aaa14-145">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaa14-146">-Sku</span><span class="sxs-lookup"><span data-stu-id="aaa14-146">-Sku</span></span>
<span data-ttu-id="aaa14-147">배포할 RedisEnterprise 클러스터의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="aaa14-147">The type of RedisEnterprise cluster to deploy.</span></span>
<span data-ttu-id="aaa14-148">가능한 값: (Enterprise_E10, EnterpriseFlash_F300 등)</span><span class="sxs-lookup"><span data-stu-id="aaa14-148">Possible values: (Enterprise_E10, EnterpriseFlash_F300 etc.)</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.SkuName
Parameter Sets: (All)
Aliases: SkuName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaa14-149">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aaa14-149">-SubscriptionId</span></span>
<span data-ttu-id="aaa14-150">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="aaa14-150">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="aaa14-151">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="aaa14-151">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaa14-152">-Tag</span><span class="sxs-lookup"><span data-stu-id="aaa14-152">-Tag</span></span>
<span data-ttu-id="aaa14-153">리소스 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="aaa14-153">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaa14-154">-Zone</span><span class="sxs-lookup"><span data-stu-id="aaa14-154">-Zone</span></span>
<span data-ttu-id="aaa14-155">이 클러스터가 배포될 영역입니다.</span><span class="sxs-lookup"><span data-stu-id="aaa14-155">The zones where this cluster will be deployed.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaa14-156">-확인</span><span class="sxs-lookup"><span data-stu-id="aaa14-156">-Confirm</span></span>
<span data-ttu-id="aaa14-157">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="aaa14-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aaa14-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aaa14-158">-WhatIf</span></span>
<span data-ttu-id="aaa14-159">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="aaa14-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aaa14-160">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aaa14-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aaa14-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaa14-161">CommonParameters</span></span>
<span data-ttu-id="aaa14-162">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="aaa14-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaa14-163">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aaa14-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaa14-164">입력</span><span class="sxs-lookup"><span data-stu-id="aaa14-164">INPUTS</span></span>

## <span data-ttu-id="aaa14-165">출력</span><span class="sxs-lookup"><span data-stu-id="aaa14-165">OUTPUTS</span></span>

### <span data-ttu-id="aaa14-166">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span><span class="sxs-lookup"><span data-stu-id="aaa14-166">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span></span>

## <span data-ttu-id="aaa14-167">참고 사항</span><span class="sxs-lookup"><span data-stu-id="aaa14-167">NOTES</span></span>

<span data-ttu-id="aaa14-168">별칭</span><span class="sxs-lookup"><span data-stu-id="aaa14-168">ALIASES</span></span>

<span data-ttu-id="aaa14-169">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="aaa14-169">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="aaa14-170">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="aaa14-170">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="aaa14-171">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="aaa14-171">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="aaa14-172">모듈 <IModule[]>: 이 데이터베이스에서 사용하도록 설정하는 redis 모듈의 선택적 집합 - 모듈은 생성 시에만 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aaa14-172">MODULE <IModule[]>: Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
  - <span data-ttu-id="aaa14-173">`Name <String>`: 모듈의 이름(예: 'RedisBloom', 'RediSearch', 'RedisTimeSeries')</span><span class="sxs-lookup"><span data-stu-id="aaa14-173">`Name <String>`: The name of the module, e.g. 'RedisBloom', 'RediSearch', 'RedisTimeSeries'</span></span>
  - <span data-ttu-id="aaa14-174">`[Arg <String>]`: 모듈에 대한 구성 옵션(예: 'ERROR_RATE 0.00 INITIAL_SIZE 400').</span><span class="sxs-lookup"><span data-stu-id="aaa14-174">`[Arg <String>]`: Configuration options for the module, e.g. 'ERROR_RATE 0.00 INITIAL_SIZE 400'.</span></span>

## <span data-ttu-id="aaa14-175">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aaa14-175">RELATED LINKS</span></span>

