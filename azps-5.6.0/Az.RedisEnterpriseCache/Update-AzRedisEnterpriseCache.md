---
external help file: ''
Module Name: Az.RedisEnterpriseCache
online version: https://docs.microsoft.com/powershell/module/az.redisenterprisecache/update-azredisenterprisecache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisEnterpriseCache/help/Update-AzRedisEnterpriseCache.md
ms.openlocfilehash: 1b16f30b068eb41bf0202c65e95f55f94769ba2d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000688"
---
# <span data-ttu-id="b386c-101">Update-AzRedisEnterpriseCache</span><span class="sxs-lookup"><span data-stu-id="b386c-101">Update-AzRedisEnterpriseCache</span></span>

## <span data-ttu-id="b386c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b386c-102">SYNOPSIS</span></span>
<span data-ttu-id="b386c-103">기존 RedisEnterprise 클러스터 업데이트</span><span class="sxs-lookup"><span data-stu-id="b386c-103">Updates an existing RedisEnterprise cluster</span></span>

## <span data-ttu-id="b386c-104">구문</span><span class="sxs-lookup"><span data-stu-id="b386c-104">SYNTAX</span></span>

### <span data-ttu-id="b386c-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="b386c-105">UpdateExpanded (Default)</span></span>
```
Update-AzRedisEnterpriseCache -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Capacity <Int32>] [-MinimumTlsVersion <String>] [-Sku <SkuName>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b386c-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b386c-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzRedisEnterpriseCache -InputObject <IRedisEnterpriseCacheIdentity> [-Capacity <Int32>]
 [-MinimumTlsVersion <String>] [-Sku <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b386c-107">설명</span><span class="sxs-lookup"><span data-stu-id="b386c-107">DESCRIPTION</span></span>
<span data-ttu-id="b386c-108">기존 RedisEnterprise 클러스터 업데이트</span><span class="sxs-lookup"><span data-stu-id="b386c-108">Updates an existing RedisEnterprise cluster</span></span>

## <span data-ttu-id="b386c-109">예제</span><span class="sxs-lookup"><span data-stu-id="b386c-109">EXAMPLES</span></span>

### <span data-ttu-id="b386c-110">예제 1: Redis Enterprise Cache 업데이트</span><span class="sxs-lookup"><span data-stu-id="b386c-110">Example 1: Update Redis Enterprise Cache</span></span>
```powershell
PS C:\> Update-AzRedisEnterpriseCache -Name "MyCache" -ResourceGroupName "MyGroup" -MinimumTlsVersion "1.2" -Tag @{"tag" = "value"}

Location Name    Type                            Zone Database
-------- ----    ----                            ---- --------
West US  MyCache Microsoft.Cache/redisEnterprise      {default}

```

<span data-ttu-id="b386c-111">이 명령은 최소 TLS 버전을 업데이트하고 MyCache라는 Redis Enterprise Cache에 태그를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="b386c-111">This command updates the minimum TLS version and adds a tag to the Redis Enterprise Cache named MyCache.</span></span>

## <span data-ttu-id="b386c-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b386c-112">PARAMETERS</span></span>

### <span data-ttu-id="b386c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b386c-113">-AsJob</span></span>
<span data-ttu-id="b386c-114">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="b386c-114">Run the command as a job</span></span>

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

### <span data-ttu-id="b386c-115">-Capacity</span><span class="sxs-lookup"><span data-stu-id="b386c-115">-Capacity</span></span>
<span data-ttu-id="b386c-116">RedisEnterprise 클러스터의 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="b386c-116">The size of the RedisEnterprise cluster.</span></span>
<span data-ttu-id="b386c-117">SKU에 따라 기본값은 2 또는 3입니다.</span><span class="sxs-lookup"><span data-stu-id="b386c-117">Defaults to 2 or 3 depending on SKU.</span></span>
<span data-ttu-id="b386c-118">유효한 값은 Enterprise SKUS의 경우(2, 4, 6, ...) 및 Flash SKUS의 경우(3, 9, 15, ...)입니다.</span><span class="sxs-lookup"><span data-stu-id="b386c-118">Valid values are (2, 4, 6, ...) for Enterprise SKUs and (3, 9, 15, ...) for Flash SKUs.</span></span>

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

### <span data-ttu-id="b386c-119">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="b386c-119">-ClusterName</span></span>
<span data-ttu-id="b386c-120">RedisEnterprise 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b386c-120">The name of the RedisEnterprise cluster.</span></span>

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

### <span data-ttu-id="b386c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b386c-121">-DefaultProfile</span></span>
<span data-ttu-id="b386c-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b386c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b386c-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b386c-123">-InputObject</span></span>
<span data-ttu-id="b386c-124">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="b386c-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b386c-125">-MinimumTlsVersion</span><span class="sxs-lookup"><span data-stu-id="b386c-125">-MinimumTlsVersion</span></span>
<span data-ttu-id="b386c-126">지원할 클러스터의 최소 TLS 버전(예: '1.2'</span><span class="sxs-lookup"><span data-stu-id="b386c-126">The minimum TLS version for the cluster to support, e.g. '1.2'</span></span>

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

### <span data-ttu-id="b386c-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="b386c-127">-NoWait</span></span>
<span data-ttu-id="b386c-128">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="b386c-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b386c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b386c-129">-ResourceGroupName</span></span>
<span data-ttu-id="b386c-130">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b386c-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="b386c-131">-Sku</span><span class="sxs-lookup"><span data-stu-id="b386c-131">-Sku</span></span>
<span data-ttu-id="b386c-132">배포할 RedisEnterprise 클러스터의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="b386c-132">The type of RedisEnterprise cluster to deploy.</span></span>
<span data-ttu-id="b386c-133">가능한 값: (Enterprise_E10, EnterpriseFlash_F300 등)</span><span class="sxs-lookup"><span data-stu-id="b386c-133">Possible values: (Enterprise_E10, EnterpriseFlash_F300 etc.)</span></span>

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

### <span data-ttu-id="b386c-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b386c-134">-SubscriptionId</span></span>
<span data-ttu-id="b386c-135">Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b386c-135">Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span>
<span data-ttu-id="b386c-136">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="b386c-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b386c-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="b386c-137">-Tag</span></span>
<span data-ttu-id="b386c-138">리소스 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="b386c-138">Resource tags.</span></span>

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

### <span data-ttu-id="b386c-139">-확인</span><span class="sxs-lookup"><span data-stu-id="b386c-139">-Confirm</span></span>
<span data-ttu-id="b386c-140">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b386c-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b386c-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b386c-141">-WhatIf</span></span>
<span data-ttu-id="b386c-142">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="b386c-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b386c-143">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b386c-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b386c-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b386c-144">CommonParameters</span></span>
<span data-ttu-id="b386c-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b386c-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b386c-146">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b386c-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b386c-147">입력</span><span class="sxs-lookup"><span data-stu-id="b386c-147">INPUTS</span></span>

### <span data-ttu-id="b386c-148">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span><span class="sxs-lookup"><span data-stu-id="b386c-148">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.IRedisEnterpriseCacheIdentity</span></span>

## <span data-ttu-id="b386c-149">출력</span><span class="sxs-lookup"><span data-stu-id="b386c-149">OUTPUTS</span></span>

### <span data-ttu-id="b386c-150">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span><span class="sxs-lookup"><span data-stu-id="b386c-150">Microsoft.Azure.PowerShell.Cmdlets.RedisEnterpriseCache.Models.Api20201001Preview.ICluster</span></span>

## <span data-ttu-id="b386c-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b386c-151">NOTES</span></span>

<span data-ttu-id="b386c-152">별칭</span><span class="sxs-lookup"><span data-stu-id="b386c-152">ALIASES</span></span>

<span data-ttu-id="b386c-153">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="b386c-153">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b386c-154">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="b386c-154">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b386c-155">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b386c-155">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b386c-156">INPUTOBJECT <IRedisEnterpriseCacheIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="b386c-156">INPUTOBJECT <IRedisEnterpriseCacheIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b386c-157">`[ClusterName <String>]`: RedisEnterprise 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b386c-157">`[ClusterName <String>]`: The name of the RedisEnterprise cluster.</span></span>
  - <span data-ttu-id="b386c-158">`[DatabaseName <String>]`: 데이터베이스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b386c-158">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="b386c-159">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="b386c-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b386c-160">`[Location <String>]`: 작업이 있는 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="b386c-160">`[Location <String>]`: The region the operation is in.</span></span>
  - <span data-ttu-id="b386c-161">`[OperationId <String>]`: 작업의 고유 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="b386c-161">`[OperationId <String>]`: The operation's unique identifier.</span></span>
  - <span data-ttu-id="b386c-162">`[PrivateEndpointConnectionName <String>]`: Azure 리소스와 연결된 개인 엔드포인트 연결의 이름</span><span class="sxs-lookup"><span data-stu-id="b386c-162">`[PrivateEndpointConnectionName <String>]`: The name of the private endpoint connection associated with the Azure resource</span></span>
  - <span data-ttu-id="b386c-163">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b386c-163">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="b386c-164">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유하게 식별하는 구독 자격 증명을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b386c-164">`[SubscriptionId <String>]`: Gets subscription credentials which uniquely identify the Microsoft Azure subscription.</span></span> <span data-ttu-id="b386c-165">구독 ID는 모든 서비스 호출에 대한 URI의 일부를 형성합니다.</span><span class="sxs-lookup"><span data-stu-id="b386c-165">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="b386c-166">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b386c-166">RELATED LINKS</span></span>

