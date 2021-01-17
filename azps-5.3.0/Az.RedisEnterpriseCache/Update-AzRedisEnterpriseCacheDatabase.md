---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/update-azredisenterprisecachedatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCacheDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCacheDatabase.md
ms.openlocfilehash: 9b41dbeaa10b77ed86567a51ec5fb106648e8ebd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378155"
---
# <span data-ttu-id="1a277-101">Update-AzRedisEnterpriseCacheDatabase</span><span class="sxs-lookup"><span data-stu-id="1a277-101">Update-AzRedisEnterpriseCacheDatabase</span></span>

## <span data-ttu-id="1a277-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a277-102">SYNOPSIS</span></span>
<span data-ttu-id="1a277-103">데이터베이스 업데이트</span><span class="sxs-lookup"><span data-stu-id="1a277-103">Updates a database</span></span>

## <span data-ttu-id="1a277-104">구문</span><span class="sxs-lookup"><span data-stu-id="1a277-104">SYNTAX</span></span>

### <span data-ttu-id="1a277-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="1a277-105">UpdateExpanded (Default)</span></span>
```
Update-AzRedisEnterpriseCacheDatabase -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClientProtocol <Protocol>] [-ClusteringPolicy <ClusteringPolicy>]
 [-EvictionPolicy <EvictionPolicy>] [-Module <IModule[]>] [-Port <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1a277-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="1a277-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzRedisEnterpriseCacheDatabase -InputObject <IRedisEnterpriseCacheIdentity>
 [-ClientProtocol <Protocol>] [-ClusteringPolicy <ClusteringPolicy>] [-EvictionPolicy <EvictionPolicy>]
 [-Module <IModule[]>] [-Port <Int32>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="1a277-107">설명</span><span class="sxs-lookup"><span data-stu-id="1a277-107">DESCRIPTION</span></span>
<span data-ttu-id="1a277-108">데이터베이스 업데이트</span><span class="sxs-lookup"><span data-stu-id="1a277-108">Updates a database</span></span>

## <span data-ttu-id="1a277-109">예제</span><span class="sxs-lookup"><span data-stu-id="1a277-109">EXAMPLES</span></span>

### <span data-ttu-id="1a277-110">예제 1: 클라이언트 프로토콜 업데이트</span><span class="sxs-lookup"><span data-stu-id="1a277-110">Example 1: Update client protocol</span></span>
```powershell
PS C:\> Update-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -ClientProtocol "Plaintext"

Name    Type
----    ----
default Microsoft.Cache/redisEnterprise/databases

```

<span data-ttu-id="1a277-111">이 명령은 MyCache라는 Redis Enterprise Cache에 대한 데이터베이스의 클라이언트 프로토콜을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1a277-111">This command updates the client protocol of the database for the Redis Enterprise Cache named MyCache.</span></span>

### <span data-ttu-id="1a277-112">예제 2: 클라이언트 프로토콜 및 지우기 정책 업데이트</span><span class="sxs-lookup"><span data-stu-id="1a277-112">Example 2: Update client protocol and eviction policy</span></span>
```powershell
PS C:\> Update-AzRedisEnterpriseCacheDatabase -Name "MyCache" -ResourceGroupName "MyGroup" -ClientProtocol "Encrypted" -EvictionPolicy "NoEviction"

Name    Type
----    ----
default Microsoft.Cache/redisEnterprise/databases

```

<span data-ttu-id="1a277-113">이 명령은 MyCache라는 Redis Enterprise Cache에 대한 데이터베이스의 클라이언트 프로토콜 및 삭제 정책을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="1a277-113">This command updates the client protocol and eviction policy of the database for the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="1a277-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a277-114">PARAMETERS</span></span>

### <span data-ttu-id="1a277-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1a277-115">-AsJob</span></span>
<span data-ttu-id="1a277-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="1a277-116">Run the command as a job</span></span>

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

### <span data-ttu-id="1a277-117">-ClientProtocol</span><span class="sxs-lookup"><span data-stu-id="1a277-117">-ClientProtocol</span></span>
<span data-ttu-id="1a277-118">Redis 클라이언트가 TLS 암호화 또는 일반 텍스트 Redis 프로토콜을 사용하여 연결할 수 있는지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1a277-118">Specifies whether redis clients can connect using TLS-encrypted or plaintext redis protocols.</span></span>
<span data-ttu-id="1a277-119">기본값은 TLS 암호화입니다.</span><span class="sxs-lookup"><span data-stu-id="1a277-119">Default is TLS-encrypted.</span></span>

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

### <span data-ttu-id="1a277-120">-ClusteringPolicy</span><span class="sxs-lookup"><span data-stu-id="1a277-120">-ClusteringPolicy</span></span>
<span data-ttu-id="1a277-121">클러스터링 정책 - 기본값은 OSSCluster입니다.</span><span class="sxs-lookup"><span data-stu-id="1a277-121">Clustering policy - default is OSSCluster.</span></span>
<span data-ttu-id="1a277-122">만들기 시 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="1a277-122">Specified at create time.</span></span>

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

### <span data-ttu-id="1a277-123">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="1a277-123">-ClusterName</span></span>
<span data-ttu-id="1a277-124">RedisEnterprise 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1a277-124">The name of the RedisEnterprise cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a277-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a277-125">-DefaultProfile</span></span>
<span data-ttu-id="1a277-126">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1a277-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a277-127">-EvictionPolicy</span><span class="sxs-lookup"><span data-stu-id="1a277-127">-EvictionPolicy</span></span>
<span data-ttu-id="1a277-128">Redis eviction policy - 기본값: VolatileLRU</span><span class="sxs-lookup"><span data-stu-id="1a277-128">Redis eviction policy - default is VolatileLRU</span></span>

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

### <span data-ttu-id="1a277-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1a277-129">-InputObject</span></span>
<span data-ttu-id="1a277-130">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="1a277-130">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a277-131">-Module</span><span class="sxs-lookup"><span data-stu-id="1a277-131">-Module</span></span>
<span data-ttu-id="1a277-132">이 데이터베이스에서 사용하도록 설정하기 위한 선택적 redis 모듈 집합 - 모듈은 생성 시에만 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a277-132">Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
<span data-ttu-id="1a277-133">생성을 위해 MODULE 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="1a277-133">To construct, see NOTES section for MODULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="1a277-134">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1a277-134">-NoWait</span></span>
<span data-ttu-id="1a277-135">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="1a277-135">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1a277-136">-Port</span><span class="sxs-lookup"><span data-stu-id="1a277-136">-Port</span></span>
<span data-ttu-id="1a277-137">데이터베이스 엔드포인트의 TCP 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="1a277-137">TCP port of the database endpoint.</span></span>
<span data-ttu-id="1a277-138">만들기 시 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="1a277-138">Specified at create time.</span></span>
<span data-ttu-id="1a277-139">기본값은 사용 가능한 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="1a277-139">Defaults to an available port.</span></span>

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

### <span data-ttu-id="1a277-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a277-140">-ResourceGroupName</span></span>
<span data-ttu-id="1a277-141">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1a277-141">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a277-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1a277-142">-SubscriptionId</span></span>
<span data-ttu-id="1a277-143">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1a277-143">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="1a277-144">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="1a277-144">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a277-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1a277-145">-Confirm</span></span>
<span data-ttu-id="1a277-146">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1a277-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a277-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a277-147">-WhatIf</span></span>
<span data-ttu-id="1a277-148">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1a277-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a277-149">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1a277-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a277-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a277-150">CommonParameters</span></span>
<span data-ttu-id="1a277-151">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1a277-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a277-152">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1a277-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a277-153">입력</span><span class="sxs-lookup"><span data-stu-id="1a277-153">INPUTS</span></span>

### <span data-ttu-id="1a277-154">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span><span class="sxs-lookup"><span data-stu-id="1a277-154">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span></span>

## <span data-ttu-id="1a277-155">출력</span><span class="sxs-lookup"><span data-stu-id="1a277-155">OUTPUTS</span></span>

### <span data-ttu-id="1a277-156">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IDatabase</span><span class="sxs-lookup"><span data-stu-id="1a277-156">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.IDatabase</span></span>

## <span data-ttu-id="1a277-157">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1a277-157">NOTES</span></span>

<span data-ttu-id="1a277-158">별칭</span><span class="sxs-lookup"><span data-stu-id="1a277-158">ALIASES</span></span>

<span data-ttu-id="1a277-159">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="1a277-159">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1a277-160">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="1a277-160">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1a277-161">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1a277-161">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1a277-162">INPUTOBJECT: <IRedisEnterpriseCacheIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="1a277-162">INPUTOBJECT <IRedisEnterpriseCacheIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1a277-163">`[ClusterName <String>]`: RedisEnterprise 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1a277-163">`[ClusterName <String>]`: The name of the RedisEnterprise cluster.</span></span>
  - <span data-ttu-id="1a277-164">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1a277-164">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="1a277-165">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="1a277-165">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1a277-166">`[Location <String>]`: 작업이 있는 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="1a277-166">`[Location <String>]`: The region the operation is in.</span></span>
  - <span data-ttu-id="1a277-167">`[OperationId <String>]`: 작업의 고유 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="1a277-167">`[OperationId <String>]`: The operation's unique identifier.</span></span>
  - <span data-ttu-id="1a277-168">`[PrivateEndpointConnectionName <String>]`: Azure 리소스와 연결된 개인 엔드포인트 연결의 이름</span><span class="sxs-lookup"><span data-stu-id="1a277-168">`[PrivateEndpointConnectionName <String>]`: The name of the private endpoint connection associated with the Azure resource</span></span>
  - <span data-ttu-id="1a277-169">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1a277-169">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="1a277-170">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="1a277-170">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="1a277-171">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="1a277-171">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="1a277-172">MODULE <IModule[]>: 이 데이터베이스에서 사용하도록 설정하기 위한 선택적 redis 모듈 집합 - 모듈은 생성 시에만 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1a277-172">MODULE <IModule[]>: Optional set of redis modules to enable in this database - modules can only be added at creation time.</span></span>
  - <span data-ttu-id="1a277-173">`Name <String>`: 모듈의 이름(예: 'RedisBloom', 'RediSearch', 'RedisTimeSeries')</span><span class="sxs-lookup"><span data-stu-id="1a277-173">`Name <String>`: The name of the module, e.g. 'RedisBloom', 'RediSearch', 'RedisTimeSeries'</span></span>
  - <span data-ttu-id="1a277-174">`[Arg <String>]`: 모듈에 대한 구성 옵션(예: 'ERROR_RATE 0.00 INITIAL_SIZE 400').</span><span class="sxs-lookup"><span data-stu-id="1a277-174">`[Arg <String>]`: Configuration options for the module, e.g. 'ERROR_RATE 0.00 INITIAL_SIZE 400'.</span></span>

## <span data-ttu-id="1a277-175">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1a277-175">RELATED LINKS</span></span>

