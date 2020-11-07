---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/set-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoor.md
ms.openlocfilehash: 57f1bf57495e75167a1936799c24aff5e6387722
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868338"
---
# <span data-ttu-id="b8071-101">Set-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="b8071-101">Set-AzFrontDoor</span></span>

## <span data-ttu-id="b8071-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8071-102">SYNOPSIS</span></span>
<span data-ttu-id="b8071-103">전방 도어 부하 분산 장치 업데이트</span><span class="sxs-lookup"><span data-stu-id="b8071-103">Update a Front Door load balancer</span></span>

## <span data-ttu-id="b8071-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b8071-104">SYNTAX</span></span>

### <span data-ttu-id="b8071-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="b8071-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzFrontDoor -ResourceGroupName <String> -Name <String> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DisableCertificateNameCheck]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b8071-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8071-106">ByObjectParameterSet</span></span>
```
Set-AzFrontDoor -InputObject <PSFrontDoor> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DisableCertificateNameCheck] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b8071-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8071-107">ByResourceIdParameterSet</span></span>
```
Set-AzFrontDoor -ResourceId <String> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DisableCertificateNameCheck] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b8071-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b8071-108">DESCRIPTION</span></span>
<span data-ttu-id="b8071-109">**AzFrontDoor** Cmdlet은 전방 도어 부하 분산을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8071-109">The **Set-AzFrontDoor** cmdlet updates a Front Door load balancer.</span></span> <span data-ttu-id="b8071-110">입력 매개 변수를 제공 하지 않으면 기존 전방 도어의 이전 매개 변수가 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b8071-110">If input parameters are not provided, old parameters from the existing Front Door will be used.</span></span>

## <span data-ttu-id="b8071-111">예제의</span><span class="sxs-lookup"><span data-stu-id="b8071-111">EXAMPLES</span></span>

### <span data-ttu-id="b8071-112">예제 1: FrontDoorName 및 ResourceGroupName를 사용 하 여 기존 전방 도어를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8071-112">Example 1: update an existing Front Door with FrontDoorName and ResourceGroupName.</span></span>
```powershell
PS C:\> Set-AzFrontDoor -Name "frontDoor1" -ResourceGroupName "resourceGroup1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
EnforceCertificateNameCheck : Enabled
HealthProbeSettings         : {healthProbeSetting1}
LoadBalancingSettings       : {loadbalancingsetting1}
FrontendEndpoints           : {frontendendpoint1}
EnabledState                : Enabled
ResourceState               : Enabled
ProvisioningState           : Succeeded
Cname                       :
Tags                        : {tag1, tag2}
Id                          : /subscriptions/{guid}/resourcegroups/{guid}/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoors
```

<span data-ttu-id="b8071-113">기존 FrontDoor를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8071-113">update an existing FrontDoor.</span></span>

### <span data-ttu-id="b8071-114">예제 2: PSFrontDoor 개체를 사용 하 여 기존 전방 도어를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8071-114">Example 2: update an existing Front Door with PSFrontDoor object.</span></span>
```powershell
PS C:\>  Set-AzFrontDoor -InputObject $frontDoor1 -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
EnforceCertificateNameCheck : Enabled
HealthProbeSettings         : {healthProbeSetting1}
LoadBalancingSettings       : {loadbalancingsetting1}
FrontendEndpoints           : {frontendendpoint1}
EnabledState                : Enabled
ResourceState               : Enabled
ProvisioningState           : Succeeded
Cname                       :
Tags                        : {tag1, tag2}
Id                          : /subscriptions/{guid}/resourcegroups/{guid}/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoor1
```

<span data-ttu-id="b8071-115">기존 FrontDoor를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8071-115">update an existing FrontDoor.</span></span>

### <span data-ttu-id="b8071-116">예제 3: ResourceId를 사용 하 여 기존 전방 도어 업데이트</span><span class="sxs-lookup"><span data-stu-id="b8071-116">Example 3: update an existing Front Door with ResourceId</span></span>
```powershell
PS C:\>  Set-AzFrontDoor -ResourceId {resourceId} -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
EnforceCertificateNameCheck : Enabled
HealthProbeSettings         : {healthProbeSetting1}
LoadBalancingSettings       : {loadbalancingsetting1}
FrontendEndpoints           : {frontendendpoint1}
EnabledState                : Enabled
ResourceState               : Enabled
ProvisioningState           : Succeeded
Cname                       :
Tags                        : {tag1, tag2}
Id                          : /subscriptions/{guid}/resourcegroups/{guid}/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoor1
```

<span data-ttu-id="b8071-117">기존 FrontDoor를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8071-117">update an existing FrontDoor.</span></span>

## <span data-ttu-id="b8071-118">변수</span><span class="sxs-lookup"><span data-stu-id="b8071-118">PARAMETERS</span></span>

### <span data-ttu-id="b8071-119">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="b8071-119">-BackendPool</span></span>
<span data-ttu-id="b8071-120">Backendpools는 라우팅 규칙에 사용 가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8071-120">Backendpools available to routing rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8071-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8071-121">-DefaultProfile</span></span>
<span data-ttu-id="b8071-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b8071-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8071-123">-DisableCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="b8071-123">-DisableCertificateNameCheck</span></span>
<span data-ttu-id="b8071-124">모든 백 엔드 풀에 대 한 HTTPS 요청에서 인증서 이름 검사를 사용할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8071-124">Whether to disable certificate name check on HTTPS requests to all backend pools.</span></span> <span data-ttu-id="b8071-125">비 HTTPS 요청에는 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b8071-125">No effect on non-HTTPS requests.</span></span>

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

### <span data-ttu-id="b8071-126">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="b8071-126">-EnabledState</span></span>
<span data-ttu-id="b8071-127">전방 도어 부하 분산 장치의 작동 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="b8071-127">Operational status of the Front Door load balancer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSEnabledState
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8071-128">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="b8071-128">-FrontendEndpoint</span></span>
<span data-ttu-id="b8071-129">라우팅 규칙에 사용할 수 있는 프런트 엔드 끝점입니다.</span><span class="sxs-lookup"><span data-stu-id="b8071-129">Frontend endpoints available to routing rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8071-130">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="b8071-130">-HealthProbeSetting</span></span>
<span data-ttu-id="b8071-131">이 전면 도어 인스턴스와 연결 된 상태 검색 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="b8071-131">Health probe settings associated with this Front Door instance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8071-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b8071-132">-InputObject</span></span>
<span data-ttu-id="b8071-133">업데이트할 프론트 도어 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b8071-133">The Front Door object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b8071-134">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="b8071-134">-LoadBalancingSetting</span></span>
<span data-ttu-id="b8071-135">이 전면 도어 인스턴스와 연결 된 부하 분산 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="b8071-135">Load balancing settings associated with this Front Door instance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8071-136">-이름</span><span class="sxs-lookup"><span data-stu-id="b8071-136">-Name</span></span>
<span data-ttu-id="b8071-137">업데이트할 앞면 도어의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b8071-137">The name of the Front Door to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8071-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8071-138">-ResourceGroupName</span></span>
<span data-ttu-id="b8071-139">앞 문이 속한 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="b8071-139">The resource group to which the Front Door belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8071-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8071-140">-ResourceId</span></span>
<span data-ttu-id="b8071-141">업데이트할 앞면 도어의 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="b8071-141">Resource Id of the Front Door to update</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8071-142">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="b8071-142">-RoutingRule</span></span>
<span data-ttu-id="b8071-143">이 FrontDoor 연결 된 라우팅 규칙</span><span class="sxs-lookup"><span data-stu-id="b8071-143">Routing rules associated with this FrontDoor</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8071-144">태그</span><span class="sxs-lookup"><span data-stu-id="b8071-144">-Tag</span></span>
<span data-ttu-id="b8071-145">FrontDoor와 연결 된 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="b8071-145">The tags associate with the FrontDoor.</span></span>

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

### <span data-ttu-id="b8071-146">-확인</span><span class="sxs-lookup"><span data-stu-id="b8071-146">-Confirm</span></span>
<span data-ttu-id="b8071-147">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8071-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8071-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8071-148">-WhatIf</span></span>
<span data-ttu-id="b8071-149">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b8071-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8071-150">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b8071-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8071-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8071-151">CommonParameters</span></span>
<span data-ttu-id="b8071-152">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b8071-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8071-153">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b8071-153">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8071-154">입력</span><span class="sxs-lookup"><span data-stu-id="b8071-154">INPUTS</span></span>

### <span data-ttu-id="b8071-155">FrontDoor. PSFrontDoor/.</span><span class="sxs-lookup"><span data-stu-id="b8071-155">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

### <span data-ttu-id="b8071-156">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b8071-156">System.String</span></span>

## <span data-ttu-id="b8071-157">출력</span><span class="sxs-lookup"><span data-stu-id="b8071-157">OUTPUTS</span></span>

### <span data-ttu-id="b8071-158">FrontDoor. PSFrontDoor/.</span><span class="sxs-lookup"><span data-stu-id="b8071-158">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="b8071-159">상속자</span><span class="sxs-lookup"><span data-stu-id="b8071-159">NOTES</span></span>

## <span data-ttu-id="b8071-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b8071-160">RELATED LINKS</span></span>

<span data-ttu-id="b8071-161">[새로운 AzFrontDoor](./New-AzFrontDoor.md) 
 [Get-AzFrontDoor](./Get-AzFrontDoor.md) 
 [제거-AzFrontDoor](./Remove-AzFrontDoor.md) 
 [새로운 AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md) 
 [새로운 AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md) 
 [새로운 AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md) 
 [새로운 AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md) 
 [새로운 AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="b8071-161">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Get-AzFrontDoor](./Get-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)
[New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md)
[New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md)
[New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md)
[New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md)
[New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span></span>
