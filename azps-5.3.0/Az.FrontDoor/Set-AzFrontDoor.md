---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/set-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoor.md
ms.openlocfilehash: 344041291f0d7f52aeebb0c968e99268ac042188
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489691"
---
# <span data-ttu-id="ca4b3-101">Set-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="ca4b3-101">Set-AzFrontDoor</span></span>

## <span data-ttu-id="ca4b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca4b3-102">SYNOPSIS</span></span>
<span data-ttu-id="ca4b3-103">Front Door 부하 균형 조정기 업데이트</span><span class="sxs-lookup"><span data-stu-id="ca4b3-103">Update a Front Door load balancer</span></span>

## <span data-ttu-id="ca4b3-104">구문</span><span class="sxs-lookup"><span data-stu-id="ca4b3-104">SYNTAX</span></span>

### <span data-ttu-id="ca4b3-105">ByFieldsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="ca4b3-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzFrontDoor -ResourceGroupName <String> -Name <String> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca4b3-106">ByFieldsWithCertificateNameCheckParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca4b3-106">ByFieldsWithCertificateNameCheckParameterSet</span></span>
```
Set-AzFrontDoor -ResourceGroupName <String> -Name <String> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DisableCertificateNameCheck]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca4b3-107">ByFieldsWithBackendPoolsSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca4b3-107">ByFieldsWithBackendPoolsSettingParameterSet</span></span>
```
Set-AzFrontDoor -ResourceGroupName <String> -Name <String> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] -BackendPoolsSetting <PSBackendPoolsSetting>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca4b3-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca4b3-108">ByObjectParameterSet</span></span>
```
Set-AzFrontDoor -InputObject <PSFrontDoor> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca4b3-109">ByObjectWithCertificateNameCheckParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca4b3-109">ByObjectWithCertificateNameCheckParameterSet</span></span>
```
Set-AzFrontDoor -InputObject <PSFrontDoor> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DisableCertificateNameCheck] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ca4b3-110">ByObjectWithBackendPoolsSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca4b3-110">ByObjectWithBackendPoolsSettingParameterSet</span></span>
```
Set-AzFrontDoor -InputObject <PSFrontDoor> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 -BackendPoolsSetting <PSBackendPoolsSetting> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ca4b3-111">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca4b3-111">ByResourceIdParameterSet</span></span>
```
Set-AzFrontDoor -ResourceId <String> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca4b3-112">ByResourceIdWithCertificateNameCheckParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca4b3-112">ByResourceIdWithCertificateNameCheckParameterSet</span></span>
```
Set-AzFrontDoor -ResourceId <String> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DisableCertificateNameCheck] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ca4b3-113">ByResourceIdWithBackendPoolsSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca4b3-113">ByResourceIdWithBackendPoolsSettingParameterSet</span></span>
```
Set-AzFrontDoor -ResourceId <String> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 -BackendPoolsSetting <PSBackendPoolsSetting> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ca4b3-114">설명</span><span class="sxs-lookup"><span data-stu-id="ca4b3-114">DESCRIPTION</span></span>
<span data-ttu-id="ca4b3-115">**Set-AzFrontDoor** cmdlet은 Front Door 부하 균형 조정을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ca4b3-115">The **Set-AzFrontDoor** cmdlet updates a Front Door load balancer.</span></span> <span data-ttu-id="ca4b3-116">입력 매개 변수가 제공되지 않는 경우 기존 Front Door의 이전 매개 변수가 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="ca4b3-116">If input parameters are not provided, old parameters from the existing Front Door will be used.</span></span>

## <span data-ttu-id="ca4b3-117">예제</span><span class="sxs-lookup"><span data-stu-id="ca4b3-117">EXAMPLES</span></span>

### <span data-ttu-id="ca4b3-118">예제 1: FrontDoorName 및 ResourceGroupName으로 기존 Front Door를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ca4b3-118">Example 1: update an existing Front Door with FrontDoorName and ResourceGroupName.</span></span>
```powershell
PS C:\> Set-AzFrontDoor -Name "frontDoor1" -ResourceGroupName "resourceGroup1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1 -BackendPoolsSetting $backendPoolsSetting1

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
Id                          : /subscriptions/{guid}/resourcegroups/{guid}/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoors
```

<span data-ttu-id="ca4b3-119">기존 FrontDoor를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ca4b3-119">update an existing FrontDoor.</span></span>

### <span data-ttu-id="ca4b3-120">예제 2: PSFrontDoor 개체를 통해 기존 Front Door를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ca4b3-120">Example 2: update an existing Front Door with PSFrontDoor object.</span></span>
```powershell
PS C:\>  Set-AzFrontDoor -InputObject $frontDoor1 -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1 -BackendPoolsSetting $backendPoolsSetting1

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
Id                          : /subscriptions/{guid}/resourcegroups/{guid}/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoor1
```

<span data-ttu-id="ca4b3-121">기존 FrontDoor를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ca4b3-121">update an existing FrontDoor.</span></span>

### <span data-ttu-id="ca4b3-122">예제 3: ResourceId를 통해 기존 Front Door 업데이트</span><span class="sxs-lookup"><span data-stu-id="ca4b3-122">Example 3: update an existing Front Door with ResourceId</span></span>
```powershell
PS C:\>  Set-AzFrontDoor -ResourceId {resourceId} -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1 -BackendPoolsSetting $backendPoolsSetting1

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
Id                          : /subscriptions/{guid}/resourcegroups/{guid}/providers/Microsoft.Network/frontdoors/frontdoor1
Name                        : frontdoor1
Type                        : Microsoft.Network/frontdoor1
```

<span data-ttu-id="ca4b3-123">기존 FrontDoor를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ca4b3-123">update an existing FrontDoor.</span></span>

### <span data-ttu-id="ca4b3-124">예제 4: -DisableCertificateNameCheck 스위치 매개 변수를 사용하여 기존 Front Door의 BackendPoolSetting 속성 EnforceCertificateNameCheck 업데이트</span><span class="sxs-lookup"><span data-stu-id="ca4b3-124">Example 4: update BackendPoolSetting property EnforceCertificateNameCheck of an existing Front Door with -DisableCertificateNameCheck switch parameter</span></span>
<span data-ttu-id="ca4b3-125">업데이트할 Front Door는 FrontoorName 및 ResourceGroupName, PSFrontDoor 개체 또는 ResourceId를 사용하여 식별할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca4b3-125">Front Door to be updated can be identified using FrontoorName and ResourceGroupName, PSFrontDoor object, or ResourceId.</span></span> <span data-ttu-id="ca4b3-126">(위의 3개 예제를 참조합니다.) 아래 예제에서는 PSFrontDoor 개체를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="ca4b3-126">(See above 3 examples for example) The below example uses PSFrontDoor object.</span></span>

```powershell
PS C:\>  Set-AzFrontDoor -InputObject $frontDoor1 -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1 -DisableCertificateNameCheck

FriendlyName                : frontdoor1
RoutingRules                : {routingrule1}
BackendPools                : {backendpool1}
BackendPoolsSetting         : {PSBackendPoolsSetting object with EnforceCertificateNameCheck is set to Disabled}
EnforceCertificateNameCheck : Disabled
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

<span data-ttu-id="ca4b3-127">기존 FrontDoor를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="ca4b3-127">update an existing FrontDoor.</span></span>

## <span data-ttu-id="ca4b3-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca4b3-128">PARAMETERS</span></span>

### <span data-ttu-id="ca4b3-129">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="ca4b3-129">-BackendPool</span></span>
<span data-ttu-id="ca4b3-130">라우팅 규칙에 사용할 수 있는 Backendpools입니다.</span><span class="sxs-lookup"><span data-stu-id="ca4b3-130">Backendpools available to routing rule.</span></span>

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

### <span data-ttu-id="ca4b3-131">-BackendPoolsSetting</span><span class="sxs-lookup"><span data-stu-id="ca4b3-131">-BackendPoolsSetting</span></span>
<span data-ttu-id="ca4b3-132">모든 backendPools에 대한 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="ca4b3-132">Settings for all backendPools.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSBackendPoolsSetting
Parameter Sets: ByFieldsWithBackendPoolsSettingParameterSet, ByObjectWithBackendPoolsSettingParameterSet, ByResourceIdWithBackendPoolsSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca4b3-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca4b3-133">-DefaultProfile</span></span>
<span data-ttu-id="ca4b3-134">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ca4b3-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca4b3-135">-DisableCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="ca4b3-135">-DisableCertificateNameCheck</span></span>
<span data-ttu-id="ca4b3-136">모든 백end 풀에 대한 HTTPS 요청에서 인증서 이름 확인을 사용하지 않도록 설정할지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="ca4b3-136">Whether to disable certificate name check on HTTPS requests to all backend pools.</span></span> <span data-ttu-id="ca4b3-137">HTTPS가 아닌 요청에는 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ca4b3-137">No effect on non-HTTPS requests.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFieldsWithCertificateNameCheckParameterSet, ByObjectWithCertificateNameCheckParameterSet, ByResourceIdWithCertificateNameCheckParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca4b3-138">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="ca4b3-138">-EnabledState</span></span>
<span data-ttu-id="ca4b3-139">Front Door 부하 균형 조정의 작동 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="ca4b3-139">Operational status of the Front Door load balancer.</span></span>

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

### <span data-ttu-id="ca4b3-140">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="ca4b3-140">-FrontendEndpoint</span></span>
<span data-ttu-id="ca4b3-141">라우팅 규칙에 사용할 수 있는 프런트 엔드 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="ca4b3-141">Frontend endpoints available to routing rule.</span></span>

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

### <span data-ttu-id="ca4b3-142">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="ca4b3-142">-HealthProbeSetting</span></span>
<span data-ttu-id="ca4b3-143">이 Front Door 인스턴스와 연결된 상태 프로브 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="ca4b3-143">Health probe settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="ca4b3-144">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca4b3-144">-InputObject</span></span>
<span data-ttu-id="ca4b3-145">업데이트할 Front Door 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ca4b3-145">The Front Door object to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor
Parameter Sets: ByObjectParameterSet, ByObjectWithCertificateNameCheckParameterSet, ByObjectWithBackendPoolsSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca4b3-146">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="ca4b3-146">-LoadBalancingSetting</span></span>
<span data-ttu-id="ca4b3-147">이 Front Door 인스턴스와 연결된 부하 분산 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="ca4b3-147">Load balancing settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="ca4b3-148">-Name</span><span class="sxs-lookup"><span data-stu-id="ca4b3-148">-Name</span></span>
<span data-ttu-id="ca4b3-149">업데이트할 Front Door의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ca4b3-149">The name of the Front Door to update.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsWithCertificateNameCheckParameterSet, ByFieldsWithBackendPoolsSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca4b3-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca4b3-150">-ResourceGroupName</span></span>
<span data-ttu-id="ca4b3-151">Front Door가 속한 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="ca4b3-151">The resource group to which the Front Door belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByFieldsWithCertificateNameCheckParameterSet, ByFieldsWithBackendPoolsSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca4b3-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ca4b3-152">-ResourceId</span></span>
<span data-ttu-id="ca4b3-153">업데이트할 Front Door의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="ca4b3-153">Resource Id of the Front Door to update</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet, ByResourceIdWithCertificateNameCheckParameterSet, ByResourceIdWithBackendPoolsSettingParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca4b3-154">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="ca4b3-154">-RoutingRule</span></span>
<span data-ttu-id="ca4b3-155">이 FrontDoor와 연결된 라우팅 규칙</span><span class="sxs-lookup"><span data-stu-id="ca4b3-155">Routing rules associated with this FrontDoor</span></span>

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

### <span data-ttu-id="ca4b3-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="ca4b3-156">-Tag</span></span>
<span data-ttu-id="ca4b3-157">태그는 FrontDoor와 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="ca4b3-157">The tags associate with the FrontDoor.</span></span>

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

### <span data-ttu-id="ca4b3-158">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ca4b3-158">-Confirm</span></span>
<span data-ttu-id="ca4b3-159">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ca4b3-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca4b3-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca4b3-160">-WhatIf</span></span>
<span data-ttu-id="ca4b3-161">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ca4b3-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca4b3-162">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ca4b3-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca4b3-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca4b3-163">CommonParameters</span></span>
<span data-ttu-id="ca4b3-164">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ca4b3-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca4b3-165">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ca4b3-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca4b3-166">입력</span><span class="sxs-lookup"><span data-stu-id="ca4b3-166">INPUTS</span></span>

### <span data-ttu-id="ca4b3-167">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="ca4b3-167">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>
### <span data-ttu-id="ca4b3-168">System.String</span><span class="sxs-lookup"><span data-stu-id="ca4b3-168">System.String</span></span>
## <span data-ttu-id="ca4b3-169">출력</span><span class="sxs-lookup"><span data-stu-id="ca4b3-169">OUTPUTS</span></span>

### <span data-ttu-id="ca4b3-170">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span><span class="sxs-lookup"><span data-stu-id="ca4b3-170">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>
## <span data-ttu-id="ca4b3-171">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ca4b3-171">NOTES</span></span>

## <span data-ttu-id="ca4b3-172">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ca4b3-172">RELATED LINKS</span></span>

<span data-ttu-id="ca4b3-173">[New-AzFrontDoor](./New-AzFrontDoor.md) 
 [Get-AzFrontDoor](./Get-AzFrontDoor.md) 
 [Remove-AzFrontDoor](./Remove-AzFrontDoor.md) 
 [New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md) 
 [New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md) 
 [New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md) 
 [New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md) 
 [New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="ca4b3-173">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Get-AzFrontDoor](./Get-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)
[New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md)
[New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md)
[New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md)
[New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md)
[New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span></span>
