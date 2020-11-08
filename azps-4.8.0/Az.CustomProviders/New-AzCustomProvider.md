---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/new-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
ms.openlocfilehash: 7f91fee2e8cc772be291662af325fd87edebdfd9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214600"
---
# <span data-ttu-id="16c44-101">New-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="16c44-101">New-AzCustomProvider</span></span>

## <span data-ttu-id="16c44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16c44-102">SYNOPSIS</span></span>
<span data-ttu-id="16c44-103">사용자 지정 리소스 공급자를 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="16c44-103">Creates or updates the custom resource provider.</span></span>

## <span data-ttu-id="16c44-104">구문과</span><span class="sxs-lookup"><span data-stu-id="16c44-104">SYNTAX</span></span>

```
New-AzCustomProvider -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Action <ICustomRpActionRouteDefinition[]>] [-ResourceType <ICustomRpResourceTypeRouteDefinition[]>]
 [-Tag <Hashtable>] [-Validation <ICustomRpValidations[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="16c44-105">설명은</span><span class="sxs-lookup"><span data-stu-id="16c44-105">DESCRIPTION</span></span>
<span data-ttu-id="16c44-106">사용자 지정 리소스 공급자를 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="16c44-106">Creates or updates the custom resource provider.</span></span>

## <span data-ttu-id="16c44-107">예제의</span><span class="sxs-lookup"><span data-stu-id="16c44-107">EXAMPLES</span></span>

### <span data-ttu-id="16c44-108">예제 1: 사용자 지정 공급자 만들기</span><span class="sxs-lookup"><span data-stu-id="16c44-108">Example 1: Create a custom provider</span></span>
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}


Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="16c44-109">사용자 지정 리소스 공급자 만들기</span><span class="sxs-lookup"><span data-stu-id="16c44-109">Create a custom resource provider</span></span>

### <span data-ttu-id="16c44-110">예제 2: 연결을 사용 하 여 사용자 지정 공급자 만들기</span><span class="sxs-lookup"><span data-stu-id="16c44-110">Example 2: Create a custom provider with associations</span></span>
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace2.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}, @{Name="Associations"; Endpoint="https://contoso.com/myService", RoutingType="Proxy,Cache,Extension"}

Location  Name             Type
--------  ----             ----
West US 2 Namespace2.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="16c44-111">사용자 지정 공급자 연결에 대 한 경로를 사용 하 여 사용자 지정 공급자를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="16c44-111">Create a custom provider, with a route for Custom provider associations.</span></span>

## <span data-ttu-id="16c44-112">변수</span><span class="sxs-lookup"><span data-stu-id="16c44-112">PARAMETERS</span></span>

### <span data-ttu-id="16c44-113">-작업</span><span class="sxs-lookup"><span data-stu-id="16c44-113">-Action</span></span>
<span data-ttu-id="16c44-114">사용자 지정 리소스 공급자가 구현 하는 작업 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="16c44-114">A list of actions that the custom resource provider implements.</span></span>
<span data-ttu-id="16c44-115">생성 하려면 작업 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="16c44-115">To construct, see NOTES section for ACTION properties and create a hash table.</span></span>

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

### <span data-ttu-id="16c44-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="16c44-116">-AsJob</span></span>
<span data-ttu-id="16c44-117">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="16c44-117">Run the command as a job</span></span>

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

### <span data-ttu-id="16c44-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16c44-118">-DefaultProfile</span></span>
<span data-ttu-id="16c44-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="16c44-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16c44-120">-위치</span><span class="sxs-lookup"><span data-stu-id="16c44-120">-Location</span></span>
<span data-ttu-id="16c44-121">리소스 위치</span><span class="sxs-lookup"><span data-stu-id="16c44-121">Resource location</span></span>

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

### <span data-ttu-id="16c44-122">-이름</span><span class="sxs-lookup"><span data-stu-id="16c44-122">-Name</span></span>
<span data-ttu-id="16c44-123">리소스 공급자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="16c44-123">The name of the resource provider.</span></span>

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

### <span data-ttu-id="16c44-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="16c44-124">-NoWait</span></span>
<span data-ttu-id="16c44-125">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="16c44-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="16c44-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16c44-126">-ResourceGroupName</span></span>
<span data-ttu-id="16c44-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="16c44-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="16c44-128">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="16c44-128">-ResourceType</span></span>
<span data-ttu-id="16c44-129">사용자 지정 리소스 공급자가 구현 하는 리소스 종류 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="16c44-129">A list of resource types that the custom resource provider implements.</span></span>
<span data-ttu-id="16c44-130">생성 하려면 RESOURCETYPE 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="16c44-130">To construct, see NOTES section for RESOURCETYPE properties and create a hash table.</span></span>

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

### <span data-ttu-id="16c44-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="16c44-131">-SubscriptionId</span></span>
<span data-ttu-id="16c44-132">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="16c44-132">The Azure subscription ID.</span></span>
<span data-ttu-id="16c44-133">GUID 형식 문자열입니다 (예: 00000000-0000-0000-0000-000000000000).</span><span class="sxs-lookup"><span data-stu-id="16c44-133">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="16c44-134">태그</span><span class="sxs-lookup"><span data-stu-id="16c44-134">-Tag</span></span>
<span data-ttu-id="16c44-135">리소스 태그</span><span class="sxs-lookup"><span data-stu-id="16c44-135">Resource tags</span></span>

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

### <span data-ttu-id="16c44-136">-유효성 검사</span><span class="sxs-lookup"><span data-stu-id="16c44-136">-Validation</span></span>
<span data-ttu-id="16c44-137">사용자 지정 리소스 공급자의 요청에 대해 실행할 유효성 검사 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="16c44-137">A list of validations to run on the custom resource provider's requests.</span></span>
<span data-ttu-id="16c44-138">생성 하려면 유효성 검사 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="16c44-138">To construct, see NOTES section for VALIDATION properties and create a hash table.</span></span>

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

### <span data-ttu-id="16c44-139">-확인</span><span class="sxs-lookup"><span data-stu-id="16c44-139">-Confirm</span></span>
<span data-ttu-id="16c44-140">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="16c44-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16c44-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16c44-141">-WhatIf</span></span>
<span data-ttu-id="16c44-142">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="16c44-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16c44-143">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="16c44-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16c44-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16c44-144">CommonParameters</span></span>
<span data-ttu-id="16c44-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="16c44-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16c44-146">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="16c44-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16c44-147">입력</span><span class="sxs-lookup"><span data-stu-id="16c44-147">INPUTS</span></span>

## <span data-ttu-id="16c44-148">출력</span><span class="sxs-lookup"><span data-stu-id="16c44-148">OUTPUTS</span></span>

### <span data-ttu-id="16c44-149">Api20180901Preview. ICustomRpManifest에 대 한 Microsoft.</span><span class="sxs-lookup"><span data-stu-id="16c44-149">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="16c44-150">상속자</span><span class="sxs-lookup"><span data-stu-id="16c44-150">NOTES</span></span>

<span data-ttu-id="16c44-151">별칭과</span><span class="sxs-lookup"><span data-stu-id="16c44-151">ALIASES</span></span>

<span data-ttu-id="16c44-152">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="16c44-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="16c44-153">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="16c44-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="16c44-154">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="16c44-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="16c44-155">ACTION <ICustomRpActionRouteDefinition [] >: 사용자 지정 리소스 공급자가 구현 하는 작업 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="16c44-155">ACTION <ICustomRpActionRouteDefinition[]>: A list of actions that the custom resource provider implements.</span></span>
  - <span data-ttu-id="16c44-156">`Endpoint <String>`: 사용자 지정 리소스 공급자가 요청을 프록시 하는 경로 정의 끝점 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="16c44-156">`Endpoint <String>`: The route definition endpoint URI that the custom resource provider will proxy requests to.</span></span> <span data-ttu-id="16c44-157">이는 플랫 URI (예: ' https://testendpoint/ ') 형식 이거나 경로를 통해 라우팅하도록 지정할 수 있습니다 (예: ' https://testendpoint/{requestPath} ').</span><span class="sxs-lookup"><span data-stu-id="16c44-157">This can be in the form of a flat URI (e.g. 'https://testendpoint/') or can specify to route via a path (e.g. 'https://testendpoint/{requestPath}')</span></span>
  - <span data-ttu-id="16c44-158">`Name <String>`: 경로 정의의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="16c44-158">`Name <String>`: The name of the route definition.</span></span> <span data-ttu-id="16c44-159">ARM 확장의 이름이 됩니다 (예: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name} ').</span><span class="sxs-lookup"><span data-stu-id="16c44-159">This becomes the name for the ARM extension (e.g. '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')</span></span>
  - <span data-ttu-id="16c44-160">`[RoutingType <ActionRouting?>]`: 작업 요청에 대해 지원 되는 라우팅 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="16c44-160">`[RoutingType <ActionRouting?>]`: The routing types that are supported for action requests.</span></span>

<span data-ttu-id="16c44-161">RESOURCETYPE <ICustomRpResourceTypeRouteDefinition [] >: 사용자 지정 리소스 공급자가 구현 하는 리소스 종류 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="16c44-161">RESOURCETYPE <ICustomRpResourceTypeRouteDefinition[]>: A list of resource types that the custom resource provider implements.</span></span>
  - <span data-ttu-id="16c44-162">`Endpoint <String>`: 사용자 지정 리소스 공급자가 요청을 프록시 하는 경로 정의 끝점 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="16c44-162">`Endpoint <String>`: The route definition endpoint URI that the custom resource provider will proxy requests to.</span></span> <span data-ttu-id="16c44-163">이는 플랫 URI (예: ' https://testendpoint/ ') 형식 이거나 경로를 통해 라우팅하도록 지정할 수 있습니다 (예: ' https://testendpoint/{requestPath} ').</span><span class="sxs-lookup"><span data-stu-id="16c44-163">This can be in the form of a flat URI (e.g. 'https://testendpoint/') or can specify to route via a path (e.g. 'https://testendpoint/{requestPath}')</span></span>
  - <span data-ttu-id="16c44-164">`Name <String>`: 경로 정의의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="16c44-164">`Name <String>`: The name of the route definition.</span></span> <span data-ttu-id="16c44-165">ARM 확장의 이름이 됩니다 (예: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name} ').</span><span class="sxs-lookup"><span data-stu-id="16c44-165">This becomes the name for the ARM extension (e.g. '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')</span></span>
  - <span data-ttu-id="16c44-166">`[RoutingType <ResourceTypeRouting?>]`: 리소스 요청에 대해 지원 되는 라우팅 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="16c44-166">`[RoutingType <ResourceTypeRouting?>]`: The routing types that are supported for resource requests.</span></span>

<span data-ttu-id="16c44-167">유효성 검사 <ICustomRpValidations [] >: 사용자 지정 리소스 공급자의 요청에 대해 실행할 유효성 검사 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="16c44-167">VALIDATION <ICustomRpValidations[]>: A list of validations to run on the custom resource provider's requests.</span></span>
  - <span data-ttu-id="16c44-168">`Specification <String>`: 유효성 검사 사양에 대 한 링크입니다.</span><span class="sxs-lookup"><span data-stu-id="16c44-168">`Specification <String>`: A link to the validation specification.</span></span> <span data-ttu-id="16c44-169">Raw.githubusercontent.com에서 사양을 호스트 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="16c44-169">The specification must be hosted on raw.githubusercontent.com.</span></span>
  - <span data-ttu-id="16c44-170">`[ValidationType <ValidationType?>]`: 일치 하는 요청에 대해 실행할 유효성 검사의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="16c44-170">`[ValidationType <ValidationType?>]`: The type of validation to run against a matching request.</span></span>

## <span data-ttu-id="16c44-171">관련 링크</span><span class="sxs-lookup"><span data-stu-id="16c44-171">RELATED LINKS</span></span>

