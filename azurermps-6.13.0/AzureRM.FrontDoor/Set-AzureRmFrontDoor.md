---
external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml
Module Name: AzureRM.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/set-azurermfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Set-AzureRmFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/Set-AzureRmFrontDoor.md
ms.openlocfilehash: 250fa8a5638e1aa9d67d212fd45352c7756d2aef
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524399"
---
# <span data-ttu-id="0278a-101">Set-AzureRmFrontDoor</span><span class="sxs-lookup"><span data-stu-id="0278a-101">Set-AzureRmFrontDoor</span></span>

## <span data-ttu-id="0278a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0278a-102">SYNOPSIS</span></span>
<span data-ttu-id="0278a-103">전방 도어 부하 분산 장치 업데이트</span><span class="sxs-lookup"><span data-stu-id="0278a-103">Update a Front Door load balancer</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0278a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0278a-104">SYNTAX</span></span>

### <span data-ttu-id="0278a-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="0278a-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzureRmFrontDoor -ResourceGroupName <String> -Name <String> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0278a-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0278a-106">ByObjectParameterSet</span></span>
```
Set-AzureRmFrontDoor -InputObject <PSFrontDoor> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0278a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0278a-107">ResourceIdParameterSet</span></span>
```
Set-AzureRmFrontDoor -ResourceId <String> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0278a-108">설명은</span><span class="sxs-lookup"><span data-stu-id="0278a-108">DESCRIPTION</span></span>
<span data-ttu-id="0278a-109">**AzureRmFrontDoor** Cmdlet은 전방 도어 부하 분산을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0278a-109">The **Set-AzureRmFrontDoor** cmdlet updates a Front Door load balancer.</span></span> <span data-ttu-id="0278a-110">입력 매개 변수를 제공 하지 않으면 기존 전방 도어의 이전 매개 변수가 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0278a-110">If input parameters are not provided, old parameters from the existing Front Door will be used.</span></span>

## <span data-ttu-id="0278a-111">예제의</span><span class="sxs-lookup"><span data-stu-id="0278a-111">EXAMPLES</span></span>

### <span data-ttu-id="0278a-112">예제 1: FrontDoorName 및 ResourceGroupName를 사용 하 여 기존 전방 도어를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0278a-112">Example 1: update an existing Front Door with FrontDoorName and ResourceGroupName.</span></span>
```powershell
PS C:\> Set-AzureRmFrontDoor -Name "frontDoor1" -ResourceGroupName "resourceGroup1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/{guid}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="0278a-113">기존 FrontDoor를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0278a-113">update an existing FrontDoor.</span></span>

### <span data-ttu-id="0278a-114">예제 2: PSFrontDoor 개체를 사용 하 여 기존 전방 도어를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0278a-114">Example 2: update an existing Front Door with PSFrontDoor object.</span></span>
```powershell
PS C:\>  Set-AzureRmFrontDoor -InputObject $frontDoor1 -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/{guid}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="0278a-115">기존 FrontDoor를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0278a-115">update an existing FrontDoor.</span></span>

### <span data-ttu-id="0278a-116">예제 3: ResourceId를 사용 하 여 기존 전방 도어 업데이트</span><span class="sxs-lookup"><span data-stu-id="0278a-116">Example 3: update an existing Front Door with ResourceId</span></span>
```powershell
PS C:\>  Set-AzureRmFrontDoor -ResourceId {resourceId} -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

FriendlyName          : frontdoor1
RoutingRules          : {routingrule1}
BackendPools          : {backendpool1}
HealthProbeSettings   : {healthProbeSetting1}
LoadBalancingSettings : {loadbalancingsetting1}
FrontendEndpoints     : {frontendendpoint1}
EnabledState          : Enabled
ResourceState         : Enabled
ProvisioningState     : Succeeded
Cname                 :
Tags                  : {tag1, tag2}
Id                    : /subscriptions/{guid}/resourcegroups/{guid}/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="0278a-117">기존 FrontDoor를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0278a-117">update an existing FrontDoor.</span></span>

## <span data-ttu-id="0278a-118">변수</span><span class="sxs-lookup"><span data-stu-id="0278a-118">PARAMETERS</span></span>

### <span data-ttu-id="0278a-119">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="0278a-119">-BackendPool</span></span>
<span data-ttu-id="0278a-120">Backendpools는 라우팅 규칙에 사용 가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="0278a-120">Backendpools available to routing rule.</span></span>

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

### <span data-ttu-id="0278a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0278a-121">-DefaultProfile</span></span>
<span data-ttu-id="0278a-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0278a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0278a-123">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="0278a-123">-EnabledState</span></span>
<span data-ttu-id="0278a-124">전방 도어 부하 분산 장치의 작동 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="0278a-124">Operational status of the Front Door load balancer.</span></span>

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

### <span data-ttu-id="0278a-125">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="0278a-125">-FrontendEndpoint</span></span>
<span data-ttu-id="0278a-126">라우팅 규칙에 사용할 수 있는 프런트 엔드 끝점입니다.</span><span class="sxs-lookup"><span data-stu-id="0278a-126">Frontend endpoints available to routing rule.</span></span>

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

### <span data-ttu-id="0278a-127">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="0278a-127">-HealthProbeSetting</span></span>
<span data-ttu-id="0278a-128">이 전면 도어 인스턴스와 연결 된 상태 검색 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="0278a-128">Health probe settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="0278a-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0278a-129">-InputObject</span></span>
<span data-ttu-id="0278a-130">업데이트할 프론트 도어 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="0278a-130">The Front Door object to update.</span></span>

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

### <span data-ttu-id="0278a-131">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="0278a-131">-LoadBalancingSetting</span></span>
<span data-ttu-id="0278a-132">이 전면 도어 인스턴스와 연결 된 부하 분산 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="0278a-132">Load balancing settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="0278a-133">-이름</span><span class="sxs-lookup"><span data-stu-id="0278a-133">-Name</span></span>
<span data-ttu-id="0278a-134">업데이트할 앞면 도어의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0278a-134">The name of the Front Door to update.</span></span>

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

### <span data-ttu-id="0278a-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0278a-135">-ResourceGroupName</span></span>
<span data-ttu-id="0278a-136">앞 문이 속한 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="0278a-136">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="0278a-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0278a-137">-ResourceId</span></span>
<span data-ttu-id="0278a-138">업데이트할 앞면 도어의 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="0278a-138">Resource Id of the Front Door to update</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0278a-139">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="0278a-139">-RoutingRule</span></span>
<span data-ttu-id="0278a-140">이 FrontDoor 연결 된 라우팅 규칙</span><span class="sxs-lookup"><span data-stu-id="0278a-140">Routing rules associated with this FrontDoor</span></span>

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

### <span data-ttu-id="0278a-141">태그</span><span class="sxs-lookup"><span data-stu-id="0278a-141">-Tag</span></span>
<span data-ttu-id="0278a-142">FrontDoor와 연결 된 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="0278a-142">The tags associate with the FrontDoor.</span></span>

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

### <span data-ttu-id="0278a-143">-확인</span><span class="sxs-lookup"><span data-stu-id="0278a-143">-Confirm</span></span>
<span data-ttu-id="0278a-144">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0278a-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0278a-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0278a-145">-WhatIf</span></span>
<span data-ttu-id="0278a-146">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0278a-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0278a-147">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0278a-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0278a-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0278a-148">CommonParameters</span></span>
<span data-ttu-id="0278a-149">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0278a-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0278a-150">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0278a-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0278a-151">입력</span><span class="sxs-lookup"><span data-stu-id="0278a-151">INPUTS</span></span>

### <span data-ttu-id="0278a-152">FrontDoor. PSFrontDoor/.</span><span class="sxs-lookup"><span data-stu-id="0278a-152">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

### <span data-ttu-id="0278a-153">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0278a-153">System.String</span></span>

## <span data-ttu-id="0278a-154">출력</span><span class="sxs-lookup"><span data-stu-id="0278a-154">OUTPUTS</span></span>

### <span data-ttu-id="0278a-155">FrontDoor. PSFrontDoor/.</span><span class="sxs-lookup"><span data-stu-id="0278a-155">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <span data-ttu-id="0278a-156">상속자</span><span class="sxs-lookup"><span data-stu-id="0278a-156">NOTES</span></span>

## <span data-ttu-id="0278a-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0278a-157">RELATED LINKS</span></span>

<span data-ttu-id="0278a-158">[새로운 AzureRmFrontDoor](./New-AzureRmFrontDoor.md) 
 [Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md) 
 [제거-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md) 
 [새로운 AzureRmFrontDoorRoutingRuleObject](./New-AzureRmFrontDoorRoutingRuleObject.md) 
 [새로운 AzureRmFrontDoorHealthProbeSettingObject](./New-AzureRmFrontHealthProbeSettingObject.md) 
 [새로운 AzureRmFrontDoorLoadBalancingSettingObject](./New-AzureRmFrontDoorLoadBalancingSettingObject.md) 
 [새로운 AzureRmFrontDoorFrontendEndpointObject](./New-AzureRmFrontDoorFrontendEndpointObject.md) 
 [새로운 AzureRmFrontDoorBackendPoolObject](./New-AzureRmFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="0278a-158">[New-AzureRmFrontDoor](./New-AzureRmFrontDoor.md)
[Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md)
[Remove-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md)
[New-AzureRmFrontDoorRoutingRuleObject](./New-AzureRmFrontDoorRoutingRuleObject.md)
[New-AzureRmFrontDoorHealthProbeSettingObject](./New-AzureRmFrontHealthProbeSettingObject.md)
[New-AzureRmFrontDoorLoadBalancingSettingObject](./New-AzureRmFrontDoorLoadBalancingSettingObject.md)
[New-AzureRmFrontDoorFrontendEndpointObject](./New-AzureRmFrontDoorFrontendEndpointObject.md)
[New-AzureRmFrontDoorBackendPoolObject](./New-AzureRmFrontDoorBackendPoolObject.md)</span></span>
