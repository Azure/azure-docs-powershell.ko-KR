---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/new-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
ms.openlocfilehash: 7f91fee2e8cc772be291662af325fd87edebdfd9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495721"
---
# <span data-ttu-id="3996f-101">New-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="3996f-101">New-AzCustomProvider</span></span>

## <span data-ttu-id="3996f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3996f-102">SYNOPSIS</span></span>
<span data-ttu-id="3996f-103">사용자 지정 리소스 공급자를 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="3996f-103">Creates or updates the custom resource provider.</span></span>

## <span data-ttu-id="3996f-104">구문</span><span class="sxs-lookup"><span data-stu-id="3996f-104">SYNTAX</span></span>

```
New-AzCustomProvider -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Action <ICustomRpActionRouteDefinition[]>] [-ResourceType <ICustomRpResourceTypeRouteDefinition[]>]
 [-Tag <Hashtable>] [-Validation <ICustomRpValidations[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3996f-105">설명</span><span class="sxs-lookup"><span data-stu-id="3996f-105">DESCRIPTION</span></span>
<span data-ttu-id="3996f-106">사용자 지정 리소스 공급자를 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="3996f-106">Creates or updates the custom resource provider.</span></span>

## <span data-ttu-id="3996f-107">예제</span><span class="sxs-lookup"><span data-stu-id="3996f-107">EXAMPLES</span></span>

### <span data-ttu-id="3996f-108">예제 1: 사용자 지정 공급자 만들기</span><span class="sxs-lookup"><span data-stu-id="3996f-108">Example 1: Create a custom provider</span></span>
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}


Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="3996f-109">사용자 지정 리소스 공급자 만들기</span><span class="sxs-lookup"><span data-stu-id="3996f-109">Create a custom resource provider</span></span>

### <span data-ttu-id="3996f-110">예제 2: 연결로 사용자 지정 공급자 만들기</span><span class="sxs-lookup"><span data-stu-id="3996f-110">Example 2: Create a custom provider with associations</span></span>
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace2.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}, @{Name="Associations"; Endpoint="https://contoso.com/myService", RoutingType="Proxy,Cache,Extension"}

Location  Name             Type
--------  ----             ----
West US 2 Namespace2.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="3996f-111">사용자 지정 공급자 연결에 대한 경로를 사용하여 사용자 지정 공급자를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3996f-111">Create a custom provider, with a route for Custom provider associations.</span></span>

## <span data-ttu-id="3996f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3996f-112">PARAMETERS</span></span>

### <span data-ttu-id="3996f-113">-Action</span><span class="sxs-lookup"><span data-stu-id="3996f-113">-Action</span></span>
<span data-ttu-id="3996f-114">사용자 지정 리소스 공급자가 구현하는 작업 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="3996f-114">A list of actions that the custom resource provider implements.</span></span>
<span data-ttu-id="3996f-115">생성을 위해 ACTION 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="3996f-115">To construct, see NOTES section for ACTION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpActionRouteDefinition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3996f-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3996f-116">-AsJob</span></span>
<span data-ttu-id="3996f-117">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="3996f-117">Run the command as a job</span></span>

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

### <span data-ttu-id="3996f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3996f-118">-DefaultProfile</span></span>
<span data-ttu-id="3996f-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3996f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3996f-120">-Location</span><span class="sxs-lookup"><span data-stu-id="3996f-120">-Location</span></span>
<span data-ttu-id="3996f-121">리소스 위치</span><span class="sxs-lookup"><span data-stu-id="3996f-121">Resource location</span></span>

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

### <span data-ttu-id="3996f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="3996f-122">-Name</span></span>
<span data-ttu-id="3996f-123">리소스 공급자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3996f-123">The name of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceProviderName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3996f-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3996f-124">-NoWait</span></span>
<span data-ttu-id="3996f-125">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="3996f-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3996f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3996f-126">-ResourceGroupName</span></span>
<span data-ttu-id="3996f-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3996f-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="3996f-128">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="3996f-128">-ResourceType</span></span>
<span data-ttu-id="3996f-129">사용자 지정 리소스 공급자가 구현하는 리소스 종류 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="3996f-129">A list of resource types that the custom resource provider implements.</span></span>
<span data-ttu-id="3996f-130">생성을 위해 RESOURCETYPE 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="3996f-130">To construct, see NOTES section for RESOURCETYPE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpResourceTypeRouteDefinition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3996f-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3996f-131">-SubscriptionId</span></span>
<span data-ttu-id="3996f-132">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3996f-132">The Azure subscription ID.</span></span>
<span data-ttu-id="3996f-133">GUID 형식 문자열입니다(예: 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="3996f-133">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="3996f-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="3996f-134">-Tag</span></span>
<span data-ttu-id="3996f-135">리소스 태그</span><span class="sxs-lookup"><span data-stu-id="3996f-135">Resource tags</span></span>

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

### <span data-ttu-id="3996f-136">-Validation</span><span class="sxs-lookup"><span data-stu-id="3996f-136">-Validation</span></span>
<span data-ttu-id="3996f-137">사용자 지정 리소스 공급자의 요청에서 실행할 유효성 검사 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="3996f-137">A list of validations to run on the custom resource provider's requests.</span></span>
<span data-ttu-id="3996f-138">유효성 검사 속성에 대한 참고 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="3996f-138">To construct, see NOTES section for VALIDATION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpValidations[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3996f-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3996f-139">-Confirm</span></span>
<span data-ttu-id="3996f-140">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3996f-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3996f-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3996f-141">-WhatIf</span></span>
<span data-ttu-id="3996f-142">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="3996f-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3996f-143">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3996f-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3996f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3996f-144">CommonParameters</span></span>
<span data-ttu-id="3996f-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3996f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3996f-146">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3996f-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3996f-147">입력</span><span class="sxs-lookup"><span data-stu-id="3996f-147">INPUTS</span></span>

## <span data-ttu-id="3996f-148">출력</span><span class="sxs-lookup"><span data-stu-id="3996f-148">OUTPUTS</span></span>

### <span data-ttu-id="3996f-149">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span><span class="sxs-lookup"><span data-stu-id="3996f-149">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="3996f-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3996f-150">NOTES</span></span>

<span data-ttu-id="3996f-151">별칭</span><span class="sxs-lookup"><span data-stu-id="3996f-151">ALIASES</span></span>

<span data-ttu-id="3996f-152">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="3996f-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3996f-153">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="3996f-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3996f-154">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3996f-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3996f-155">ACTION <ICustomRpActionRouteDefinition[]>: 사용자 지정 리소스 공급자가 구현하는 작업 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="3996f-155">ACTION <ICustomRpActionRouteDefinition[]>: A list of actions that the custom resource provider implements.</span></span>
  - <span data-ttu-id="3996f-156">`Endpoint <String>`: 사용자 지정 리소스 공급자가 프록시할 경로 정의 엔드포인트 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="3996f-156">`Endpoint <String>`: The route definition endpoint URI that the custom resource provider will proxy requests to.</span></span> <span data-ttu-id="3996f-157">이는 플랫 URI(예: '')의 형태일 수 있습니다. 또는 경로(예: '')를 통해 라우팅할 수 https://testendpoint/ https://testendpoint/{requestPath} 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3996f-157">This can be in the form of a flat URI (e.g. 'https://testendpoint/') or can specify to route via a path (e.g. 'https://testendpoint/{requestPath}')</span></span>
  - <span data-ttu-id="3996f-158">`Name <String>`: 경로 정의의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3996f-158">`Name <String>`: The name of the route definition.</span></span> <span data-ttu-id="3996f-159">이 이름은 ARM 확장의 이름이 됩니다(예: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}').</span><span class="sxs-lookup"><span data-stu-id="3996f-159">This becomes the name for the ARM extension (e.g. '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')</span></span>
  - <span data-ttu-id="3996f-160">`[RoutingType <ActionRouting?>]`: 작업 요청에 지원되는 라우팅 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="3996f-160">`[RoutingType <ActionRouting?>]`: The routing types that are supported for action requests.</span></span>

<span data-ttu-id="3996f-161">RESOURCETYPE <ICustomRpResourceTypeRouteDefinition[]>: 사용자 지정 리소스 공급자가 구현하는 리소스 종류 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="3996f-161">RESOURCETYPE <ICustomRpResourceTypeRouteDefinition[]>: A list of resource types that the custom resource provider implements.</span></span>
  - <span data-ttu-id="3996f-162">`Endpoint <String>`: 사용자 지정 리소스 공급자가 프록시할 경로 정의 엔드포인트 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="3996f-162">`Endpoint <String>`: The route definition endpoint URI that the custom resource provider will proxy requests to.</span></span> <span data-ttu-id="3996f-163">이는 플랫 URI(예: '')의 형태일 수 있습니다. 또는 경로(예: '')를 통해 라우팅할 수 https://testendpoint/ https://testendpoint/{requestPath} 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3996f-163">This can be in the form of a flat URI (e.g. 'https://testendpoint/') or can specify to route via a path (e.g. 'https://testendpoint/{requestPath}')</span></span>
  - <span data-ttu-id="3996f-164">`Name <String>`: 경로 정의의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3996f-164">`Name <String>`: The name of the route definition.</span></span> <span data-ttu-id="3996f-165">이 이름은 ARM 확장의 이름이 됩니다(예: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}').</span><span class="sxs-lookup"><span data-stu-id="3996f-165">This becomes the name for the ARM extension (e.g. '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')</span></span>
  - <span data-ttu-id="3996f-166">`[RoutingType <ResourceTypeRouting?>]`: 리소스 요청에 지원되는 라우팅 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="3996f-166">`[RoutingType <ResourceTypeRouting?>]`: The routing types that are supported for resource requests.</span></span>

<span data-ttu-id="3996f-167">유효성 <ICustomRpValidations[]>: 사용자 지정 리소스 공급자의 요청에서 실행할 유효성 검사 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="3996f-167">VALIDATION <ICustomRpValidations[]>: A list of validations to run on the custom resource provider's requests.</span></span>
  - <span data-ttu-id="3996f-168">`Specification <String>`: 유효성 검사 사양에 대한 링크입니다.</span><span class="sxs-lookup"><span data-stu-id="3996f-168">`Specification <String>`: A link to the validation specification.</span></span> <span data-ttu-id="3996f-169">사양은 다음에서 호스트되어야 raw.githubusercontent.com.</span><span class="sxs-lookup"><span data-stu-id="3996f-169">The specification must be hosted on raw.githubusercontent.com.</span></span>
  - <span data-ttu-id="3996f-170">`[ValidationType <ValidationType?>]`: 일치하는 요청에 대해 실행할 유효성 검사 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="3996f-170">`[ValidationType <ValidationType?>]`: The type of validation to run against a matching request.</span></span>

## <span data-ttu-id="3996f-171">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3996f-171">RELATED LINKS</span></span>

