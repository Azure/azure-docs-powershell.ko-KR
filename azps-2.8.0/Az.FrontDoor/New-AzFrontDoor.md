---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/new-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/New-AzFrontDoor.md
ms.openlocfilehash: cea5b69b279b6f7f7a8e783d4ed328237377c18f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689890"
---
# <span data-ttu-id="c59b0-101">New-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="c59b0-101">New-AzFrontDoor</span></span>

## <span data-ttu-id="c59b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c59b0-102">SYNOPSIS</span></span>
<span data-ttu-id="c59b0-103">새 Azure 프론트 도어 부하 분산 장치 만들기</span><span class="sxs-lookup"><span data-stu-id="c59b0-103">Create a new Azure Front Door load balancer</span></span>

## <span data-ttu-id="c59b0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c59b0-104">SYNTAX</span></span>

```
New-AzFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DisableCertificateNameCheck]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c59b0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c59b0-105">DESCRIPTION</span></span>
<span data-ttu-id="c59b0-106">**AzFrontDoor** cmdlet은 현재 구독 아래의 지정 된 리소스 그룹에 새 Azure 전면 도어 부하 분산을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c59b0-106">The **New-AzFrontDoor** cmdlet creates a new Azure Front Door load balancer in the specified resource group under current subscription</span></span>

## <span data-ttu-id="c59b0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c59b0-107">EXAMPLES</span></span>

### <span data-ttu-id="c59b0-108">예제 1: 주어진 매개 변수를 기반으로 하는 전방 도어를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c59b0-108">Example 1: Create a Front Door based on given parameters.</span></span>
```powershell
PS C:\> New-AzFrontDoor -Name "frontDoor1" -ResourceGroupName "rg1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

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
Id                          : /subscriptions/{guid}/resourcegroups/rg1/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoors
```

<span data-ttu-id="c59b0-109">지정 된 매개 변수를 기반으로 하는 전방 도어를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c59b0-109">Create a Front Door based on given parameters.</span></span>

## <span data-ttu-id="c59b0-110">변수</span><span class="sxs-lookup"><span data-stu-id="c59b0-110">PARAMETERS</span></span>

### <span data-ttu-id="c59b0-111">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="c59b0-111">-BackendPool</span></span>
<span data-ttu-id="c59b0-112">Backendpools는 라우팅 규칙에 사용 가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="c59b0-112">Backendpools available to routing rule.</span></span>

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

### <span data-ttu-id="c59b0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c59b0-113">-DefaultProfile</span></span>
<span data-ttu-id="c59b0-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c59b0-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c59b0-115">-DisableCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="c59b0-115">-DisableCertificateNameCheck</span></span>
<span data-ttu-id="c59b0-116">모든 백 엔드 풀에 대 한 HTTPS 요청에서 인증서 이름 검사를 사용할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c59b0-116">Whether to disable certificate name check on HTTPS requests to all backend pools.</span></span> <span data-ttu-id="c59b0-117">비 HTTPS 요청에는 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c59b0-117">No effect on non-HTTPS requests.</span></span>

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

### <span data-ttu-id="c59b0-118">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="c59b0-118">-EnabledState</span></span>
<span data-ttu-id="c59b0-119">전방 도어 부하 분산 장치의 EnabledState입니다.</span><span class="sxs-lookup"><span data-stu-id="c59b0-119">EnabledState of the Front Door load balancer.</span></span>
<span data-ttu-id="c59b0-120">기본값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c59b0-120">Default value is Enabled</span></span>

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

### <span data-ttu-id="c59b0-121">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="c59b0-121">-FrontendEndpoint</span></span>
<span data-ttu-id="c59b0-122">라우팅 규칙에 사용할 수 있는 프런트 엔드 끝점입니다.</span><span class="sxs-lookup"><span data-stu-id="c59b0-122">Frontend endpoints available to routing rule.</span></span>

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

### <span data-ttu-id="c59b0-123">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="c59b0-123">-HealthProbeSetting</span></span>
<span data-ttu-id="c59b0-124">이 전면 도어 인스턴스와 연결 된 상태 검색 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="c59b0-124">Health probe settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="c59b0-125">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="c59b0-125">-LoadBalancingSetting</span></span>
<span data-ttu-id="c59b0-126">이 전면 도어 인스턴스와 연결 된 부하 분산 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="c59b0-126">Load balancing settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="c59b0-127">-이름</span><span class="sxs-lookup"><span data-stu-id="c59b0-127">-Name</span></span>
<span data-ttu-id="c59b0-128">전방 문 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c59b0-128">Front Door name.</span></span>

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

### <span data-ttu-id="c59b0-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c59b0-129">-ResourceGroupName</span></span>
<span data-ttu-id="c59b0-130">앞 문이 생성 될 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c59b0-130">The resource group name that the Front Door will be created in.</span></span>

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

### <span data-ttu-id="c59b0-131">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="c59b0-131">-RoutingRule</span></span>
<span data-ttu-id="c59b0-132">이 FrontDoor 연결 된 라우팅 규칙</span><span class="sxs-lookup"><span data-stu-id="c59b0-132">Routing rules associated with this FrontDoor</span></span>

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

### <span data-ttu-id="c59b0-133">태그</span><span class="sxs-lookup"><span data-stu-id="c59b0-133">-Tag</span></span>
<span data-ttu-id="c59b0-134">FrontDoor와 연결 된 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="c59b0-134">The tags associate with the FrontDoor.</span></span>

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

### <span data-ttu-id="c59b0-135">-확인</span><span class="sxs-lookup"><span data-stu-id="c59b0-135">-Confirm</span></span>
<span data-ttu-id="c59b0-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c59b0-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c59b0-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c59b0-137">-WhatIf</span></span>
<span data-ttu-id="c59b0-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c59b0-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c59b0-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c59b0-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c59b0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c59b0-140">CommonParameters</span></span>
<span data-ttu-id="c59b0-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c59b0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c59b0-142">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c59b0-142">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c59b0-143">입력</span><span class="sxs-lookup"><span data-stu-id="c59b0-143">INPUTS</span></span>

### <span data-ttu-id="c59b0-144">않아야</span><span class="sxs-lookup"><span data-stu-id="c59b0-144">None</span></span>

## <span data-ttu-id="c59b0-145">출력</span><span class="sxs-lookup"><span data-stu-id="c59b0-145">OUTPUTS</span></span>

### <span data-ttu-id="c59b0-146">FrontDoor. PSFrontDoor/.</span><span class="sxs-lookup"><span data-stu-id="c59b0-146">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="c59b0-147">상속자</span><span class="sxs-lookup"><span data-stu-id="c59b0-147">NOTES</span></span>

## <span data-ttu-id="c59b0-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c59b0-148">RELATED LINKS</span></span>

<span data-ttu-id="c59b0-149">[Get-AzFrontDoor](./Get-AzFrontDoor.md) 
 [Set-AzFrontDoor](./Set-AzFrontDoor.md) 
 [제거-AzFrontDoor](./Remove-AzFrontDoor.md) 
 [새로운 AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md) 
 [새로운 AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md) 
 [새로운 AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md) 
 [새로운 AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md) 
 [새로운 AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="c59b0-149">[Get-AzFrontDoor](./Get-AzFrontDoor.md)
[Set-AzFrontDoor](./Set-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)
[New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md)
[New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md)
[New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md)
[New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md)
[New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span></span>