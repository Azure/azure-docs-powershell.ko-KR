---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.redisenterprisecache/update-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCache.md
ms.openlocfilehash: ef1ef3d45594b0e290a014fb3aa98d670e5681a2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378169"
---
# <span data-ttu-id="c2878-101">Update-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="c2878-101">Update-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="c2878-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2878-102">SYNOPSIS</span></span>
<span data-ttu-id="c2878-103">기존 RedisEnterprise 클러스터를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c2878-103">Updates an existing RedisEnterprise cluster</span></span>

## <span data-ttu-id="c2878-104">구문</span><span class="sxs-lookup"><span data-stu-id="c2878-104">SYNTAX</span></span>

### <span data-ttu-id="c2878-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="c2878-105">UpdateExpanded (Default)</span></span>
```
Update-AzRedisEnterpriseCache -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Capacity <Int32>] [-MinimumTlsVersion <String>] [-Sku <SkuName>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c2878-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="c2878-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzRedisEnterpriseCache -InputObject <IRedisEnterpriseCacheIdentity> [-Capacity <Int32>]
 [-MinimumTlsVersion <String>] [-Sku <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c2878-107">설명</span><span class="sxs-lookup"><span data-stu-id="c2878-107">DESCRIPTION</span></span>
<span data-ttu-id="c2878-108">기존 RedisEnterprise 클러스터를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c2878-108">Updates an existing RedisEnterprise cluster</span></span>

## <span data-ttu-id="c2878-109">예제</span><span class="sxs-lookup"><span data-stu-id="c2878-109">EXAMPLES</span></span>

### <span data-ttu-id="c2878-110">예제 1: Redis Enterprise Cache 업데이트</span><span class="sxs-lookup"><span data-stu-id="c2878-110">Example 1: Update Redis Enterprise Cache</span></span>
```powershell
PS C:\> Update-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -MinimumTlsVersion "1.2" -Tag @{"tag" = "value"}

Location Name    Type                            Zone Database
-------- ----    ----                            ---- --------
West US  MyCache Microsoft.Cache/redisEnterprise      {default}

```

<span data-ttu-id="c2878-111">이 명령은 최소 TLS 버전을 업데이트하고 MyCache라는 Redis Enterprise Cache에 태그를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="c2878-111">This command updates the minimum TLS version and adds a tag to the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="c2878-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2878-112">PARAMETERS</span></span>

### <span data-ttu-id="c2878-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c2878-113">-AsJob</span></span>
<span data-ttu-id="c2878-114">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="c2878-114">Run the command as a job</span></span>

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

### <span data-ttu-id="c2878-115">-Capacity</span><span class="sxs-lookup"><span data-stu-id="c2878-115">-Capacity</span></span>
<span data-ttu-id="c2878-116">RedisEnterprise 클러스터의 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="c2878-116">The size of the RedisEnterprise cluster.</span></span>
<span data-ttu-id="c2878-117">기본값은 SKU에 따라 2 또는 3입니다.</span><span class="sxs-lookup"><span data-stu-id="c2878-117">Defaults to 2 or 3 depending on SKU.</span></span>
<span data-ttu-id="c2878-118">유효한 값은 Enterprise SKUS의 경우 (2, 4, 6, ...) 및 Flash SKUS의 경우 (3, 9, 15, ...)입니다.</span><span class="sxs-lookup"><span data-stu-id="c2878-118">Valid values are (2, 4, 6, ...) for Enterprise SKUs and (3, 9, 15, ...) for Flash SKUs.</span></span>

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

### <span data-ttu-id="c2878-119">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c2878-119">-ClusterName</span></span>
<span data-ttu-id="c2878-120">RedisEnterprise 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c2878-120">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="c2878-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2878-121">-DefaultProfile</span></span>
<span data-ttu-id="c2878-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c2878-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2878-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2878-123">-InputObject</span></span>
<span data-ttu-id="c2878-124">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="c2878-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c2878-125">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="c2878-125">-MinimumTlsVersion</span></span>
<span data-ttu-id="c2878-126">지원할 클러스터에 대한 최소 TLS 버전(예: '1.2')</span><span class="sxs-lookup"><span data-stu-id="c2878-126">The minimum TLS version for the cluster to support, e.g. '1.2'</span></span>

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

### <span data-ttu-id="c2878-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c2878-127">-NoWait</span></span>
<span data-ttu-id="c2878-128">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="c2878-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c2878-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2878-129">-ResourceGroupName</span></span>
<span data-ttu-id="c2878-130">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c2878-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="c2878-131">-Sku</span><span class="sxs-lookup"><span data-stu-id="c2878-131">-Sku</span></span>
<span data-ttu-id="c2878-132">배포할 RedisEnterprise 클러스터의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="c2878-132">The type of RedisEnterprise cluster to deploy.</span></span>
<span data-ttu-id="c2878-133">가능한 값: (Enterprise_E10, EnterpriseFlash_F300 등)</span><span class="sxs-lookup"><span data-stu-id="c2878-133">Possible values: (Enterprise_E10, EnterpriseFlash_F300 etc.)</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Support.SkuName
Parameter Sets: (All)
Aliases: SkuName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2878-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c2878-134">-SubscriptionId</span></span>
<span data-ttu-id="c2878-135">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c2878-135">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="c2878-136">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="c2878-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c2878-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="c2878-137">-Tag</span></span>
<span data-ttu-id="c2878-138">리소스 태그.</span><span class="sxs-lookup"><span data-stu-id="c2878-138">Resource tags.</span></span>

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

### <span data-ttu-id="c2878-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c2878-139">-Confirm</span></span>
<span data-ttu-id="c2878-140">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2878-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2878-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2878-141">-WhatIf</span></span>
<span data-ttu-id="c2878-142">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c2878-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2878-143">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c2878-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2878-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2878-144">CommonParameters</span></span>
<span data-ttu-id="c2878-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c2878-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2878-146">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c2878-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2878-147">입력</span><span class="sxs-lookup"><span data-stu-id="c2878-147">INPUTS</span></span>

### <span data-ttu-id="c2878-148">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span><span class="sxs-lookup"><span data-stu-id="c2878-148">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span></span>

## <span data-ttu-id="c2878-149">출력</span><span class="sxs-lookup"><span data-stu-id="c2878-149">OUTPUTS</span></span>

### <span data-ttu-id="c2878-150">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span><span class="sxs-lookup"><span data-stu-id="c2878-150">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span></span>

## <span data-ttu-id="c2878-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c2878-151">NOTES</span></span>

<span data-ttu-id="c2878-152">별칭</span><span class="sxs-lookup"><span data-stu-id="c2878-152">ALIASES</span></span>

<span data-ttu-id="c2878-153">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="c2878-153">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c2878-154">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="c2878-154">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c2878-155">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c2878-155">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c2878-156">INPUTOBJECT: <IRedisEnterpriseCacheIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="c2878-156">INPUTOBJECT <IRedisEnterpriseCacheIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c2878-157">`[ClusterName <String>]`: RedisEnterprise 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c2878-157">`[ClusterName <String>]`: The name of the RedisEnterprise cluster.</span></span>
  - <span data-ttu-id="c2878-158">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c2878-158">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="c2878-159">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="c2878-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c2878-160">`[Location <String>]`: 작업이 있는 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="c2878-160">`[Location <String>]`: The region the operation is in.</span></span>
  - <span data-ttu-id="c2878-161">`[OperationId <String>]`: 작업의 고유 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="c2878-161">`[OperationId <String>]`: The operation's unique identifier.</span></span>
  - <span data-ttu-id="c2878-162">`[PrivateEndpointConnectionName <String>]`: Azure 리소스와 연결된 개인 엔드포인트 연결의 이름</span><span class="sxs-lookup"><span data-stu-id="c2878-162">`[PrivateEndpointConnectionName <String>]`: The name of the private endpoint connection associated with the Azure resource</span></span>
  - <span data-ttu-id="c2878-163">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c2878-163">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="c2878-164">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c2878-164">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="c2878-165">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="c2878-165">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="c2878-166">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c2878-166">RELATED LINKS</span></span>

