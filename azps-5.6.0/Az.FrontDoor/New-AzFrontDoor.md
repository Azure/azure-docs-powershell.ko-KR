---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/powershell/module/az.frontdoor/new-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
ms.openlocfilehash: f3a5b61561b0886af32aa13103f3234098c76357
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977120"
---
# <span data-ttu-id="6fcce-101">New-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="6fcce-101">New-AzFrontDoor</span></span>

## <span data-ttu-id="6fcce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fcce-102">SYNOPSIS</span></span>
<span data-ttu-id="6fcce-103">새 Azure Front Door 부하 균형 조정기 만들기</span><span class="sxs-lookup"><span data-stu-id="6fcce-103">Create a new Azure Front Door load balancer</span></span>

## <span data-ttu-id="6fcce-104">구문</span><span class="sxs-lookup"><span data-stu-id="6fcce-104">SYNTAX</span></span>

### <span data-ttu-id="6fcce-105">ByFieldsWithBackendPoolsSettingParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="6fcce-105">ByFieldsWithBackendPoolsSettingParameterSet (Default)</span></span>
```
New-AzFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-BackendPoolsSetting <PSBackendPoolsSetting>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fcce-106">ByFieldsWithCertificateNameCheckParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fcce-106">ByFieldsWithCertificateNameCheckParameterSet</span></span>
```
New-AzFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DisableCertificateNameCheck]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fcce-107">설명</span><span class="sxs-lookup"><span data-stu-id="6fcce-107">DESCRIPTION</span></span>
<span data-ttu-id="6fcce-108">**New-AzFrontDoor** cmdlet은 현재 구독에서 지정된 리소스 그룹에 새 Azure Front Door 부하 균형 조정기를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6fcce-108">The **New-AzFrontDoor** cmdlet creates a new Azure Front Door load balancer in the specified resource group under current subscription</span></span>

## <span data-ttu-id="6fcce-109">예제</span><span class="sxs-lookup"><span data-stu-id="6fcce-109">EXAMPLES</span></span>

### <span data-ttu-id="6fcce-110">예제 1: 주어진 매개 변수에 따라 Front Door 만들기</span><span class="sxs-lookup"><span data-stu-id="6fcce-110">Example 1: Create a Front Door based on given parameters.</span></span>
```powershell
PS C:\> New-AzFrontDoor -Name "frontDoor1" -ResourceGroupName "rg1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1 -BackendPoolsSetting $backendPoolsSetting1

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
BackendPoolsSetting         : {backendPoolsSetting1}
EnforceCertificateNameCheck : {backendPoolsSetting1.EnforceCertificateNameCheck}
HealthProbeSettings         : {healthProbeSetting1}
LoadBalancingSettings       : {loadbalancingsetting1}
FrontendEndpoints           : {frontendendpoint1}
EnabledState                : Enabled
ResourceState               : Enabled
ProvisioningState           : Succeeded
Cname                       :
Tags                        : {tag1, tag2}
Id                          : /subscriptions/{guid}/resourcegroups/rg1/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoors
```

<span data-ttu-id="6fcce-111">주어진 매개 변수에 따라 Front Door를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="6fcce-111">Create a Front Door based on given parameters.</span></span>

## <span data-ttu-id="6fcce-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6fcce-112">PARAMETERS</span></span>

### <span data-ttu-id="6fcce-113">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="6fcce-113">-BackendPool</span></span>
<span data-ttu-id="6fcce-114">라우팅 규칙에 사용할 수 있는 백렌드풀입니다.</span><span class="sxs-lookup"><span data-stu-id="6fcce-114">Backendpools available to routing rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPool[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fcce-115">-BackendPoolsSetting</span><span class="sxs-lookup"><span data-stu-id="6fcce-115">-BackendPoolsSetting</span></span>
<span data-ttu-id="6fcce-116">모든 백endPool에 대한 설정</span><span class="sxs-lookup"><span data-stu-id="6fcce-116">Settings for all backendPools</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPoolsSetting
Parameter Sets: ByFieldsWithBackendPoolsSettingParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fcce-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fcce-117">-DefaultProfile</span></span>
<span data-ttu-id="6fcce-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6fcce-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fcce-119">-DisableCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="6fcce-119">-DisableCertificateNameCheck</span></span>
<span data-ttu-id="6fcce-120">모든 백end 풀에 대한 HTTPS 요청에서 인증서 이름 확인을 사용하지 않도록 설정할지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="6fcce-120">Whether to disable certificate name check on HTTPS requests to all backend pools.</span></span> <span data-ttu-id="6fcce-121">HTTPS가 아닌 요청에는 영향을주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6fcce-121">No effect on non-HTTPS requests.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFieldsWithCertificateNameCheckParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fcce-122">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="6fcce-122">-EnabledState</span></span>
<span data-ttu-id="6fcce-123">Front Door 부하 저울의 EnabledState입니다.</span><span class="sxs-lookup"><span data-stu-id="6fcce-123">EnabledState of the Front Door load balancer.</span></span>
<span data-ttu-id="6fcce-124">기본값이 사용하도록 설정되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6fcce-124">Default value is Enabled</span></span>

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

### <span data-ttu-id="6fcce-125">-FrontendPoint</span><span class="sxs-lookup"><span data-stu-id="6fcce-125">-FrontendEndpoint</span></span>
<span data-ttu-id="6fcce-126">라우팅 규칙에 사용할 수 있는 프런트 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="6fcce-126">Frontend endpoints available to routing rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontendEndpoint[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fcce-127">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="6fcce-127">-HealthProbeSetting</span></span>
<span data-ttu-id="6fcce-128">이 Front Door 인스턴스와 연결된 상태 프로브 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="6fcce-128">Health probe settings associated with this Front Door instance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSHealthProbeSetting[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fcce-129">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="6fcce-129">-LoadBalancingSetting</span></span>
<span data-ttu-id="6fcce-130">이 Front Door 인스턴스와 연결된 부하 분산 설정.</span><span class="sxs-lookup"><span data-stu-id="6fcce-130">Load balancing settings associated with this Front Door instance.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSLoadBalancingSetting[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fcce-131">-Name</span><span class="sxs-lookup"><span data-stu-id="6fcce-131">-Name</span></span>
<span data-ttu-id="6fcce-132">프런트 도어 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6fcce-132">Front Door name.</span></span>

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

### <span data-ttu-id="6fcce-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fcce-133">-ResourceGroupName</span></span>
<span data-ttu-id="6fcce-134">Front Door에서 만들 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6fcce-134">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="6fcce-135">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="6fcce-135">-RoutingRule</span></span>
<span data-ttu-id="6fcce-136">이 FrontDoor와 연결된 라우팅 규칙</span><span class="sxs-lookup"><span data-stu-id="6fcce-136">Routing rules associated with this FrontDoor</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSRoutingRule[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fcce-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="6fcce-137">-Tag</span></span>
<span data-ttu-id="6fcce-138">태그는 FrontDoor와 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="6fcce-138">The tags associate with the FrontDoor.</span></span>

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

### <span data-ttu-id="6fcce-139">-확인</span><span class="sxs-lookup"><span data-stu-id="6fcce-139">-Confirm</span></span>
<span data-ttu-id="6fcce-140">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6fcce-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fcce-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fcce-141">-WhatIf</span></span>
<span data-ttu-id="6fcce-142">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="6fcce-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fcce-143">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6fcce-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fcce-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fcce-144">CommonParameters</span></span>
<span data-ttu-id="6fcce-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6fcce-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fcce-146">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6fcce-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fcce-147">입력</span><span class="sxs-lookup"><span data-stu-id="6fcce-147">INPUTS</span></span>

### <span data-ttu-id="6fcce-148">없음</span><span class="sxs-lookup"><span data-stu-id="6fcce-148">None</span></span>
## <span data-ttu-id="6fcce-149">출력</span><span class="sxs-lookup"><span data-stu-id="6fcce-149">OUTPUTS</span></span>

### <span data-ttu-id="6fcce-150">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="6fcce-150">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>
## <span data-ttu-id="6fcce-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6fcce-151">NOTES</span></span>

## <span data-ttu-id="6fcce-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6fcce-152">RELATED LINKS</span></span>

<span data-ttu-id="6fcce-153">[Get-AzFrontDoor](./Get-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md) 
 [Remove-AzFrontDoor](./Remove-AzFrontDoor.md) 
 [New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md) 
 [New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md) 
 [New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md) 
 [New-AzFrontDoorFrontendendpointObject](./New-AzFrontDoorFrontendEndpointObject.md) 
 [New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="6fcce-153">[Get-AzFrontDoor](./Get-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)
[New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md)
[New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md)
[New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md)
[New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md)
[New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span></span>