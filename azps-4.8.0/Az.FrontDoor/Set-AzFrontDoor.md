---
external help file: Microsoft.Azure.PowerShell.Cmdlets.FrontDoor.dll-Help.xml
Module Name: Az.FrontDoor
online version: https://docs.microsoft.com/en-us/powershell/module/az.frontdoor/set-azfrontdoor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/FrontDoor/FrontDoor/help/Set-AzFrontDoor.md
ms.openlocfilehash: 344041291f0d7f52aeebb0c968e99268ac042188
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212773"
---
# <span data-ttu-id="4619b-101">Set-AzFrontDoor</span><span class="sxs-lookup"><span data-stu-id="4619b-101">Set-AzFrontDoor</span></span>

## <span data-ttu-id="4619b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4619b-102">SYNOPSIS</span></span>
<span data-ttu-id="4619b-103">전방 도어 부하 분산 장치 업데이트</span><span class="sxs-lookup"><span data-stu-id="4619b-103">Update a Front Door load balancer</span></span>

## <span data-ttu-id="4619b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4619b-104">SYNTAX</span></span>

### <span data-ttu-id="4619b-105">ByFieldsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="4619b-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzFrontDoor -ResourceGroupName <String> -Name <String> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4619b-106">ByFieldsWithCertificateNameCheckParameterSet</span><span class="sxs-lookup"><span data-stu-id="4619b-106">ByFieldsWithCertificateNameCheckParameterSet</span></span>
```
Set-AzFrontDoor -ResourceGroupName <String> -Name <String> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DisableCertificateNameCheck]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4619b-107">ByFieldsWithBackendPoolsSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="4619b-107">ByFieldsWithBackendPoolsSettingParameterSet</span></span>
```
Set-AzFrontDoor -ResourceGroupName <String> -Name <String> [-RoutingRule <PSRoutingRule[]>]
 [-BackendPool <PSBackendPool[]>] [-FrontendEndpoint <PSFrontendEndpoint[]>]
 [-LoadBalancingSetting <PSLoadBalancingSetting[]>] [-HealthProbeSetting <PSHealthProbeSetting[]>]
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] -BackendPoolsSetting <PSBackendPoolsSetting>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4619b-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4619b-108">ByObjectParameterSet</span></span>
```
Set-AzFrontDoor -InputObject <PSFrontDoor> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4619b-109">ByObjectWithCertificateNameCheckParameterSet</span><span class="sxs-lookup"><span data-stu-id="4619b-109">ByObjectWithCertificateNameCheckParameterSet</span></span>
```
Set-AzFrontDoor -InputObject <PSFrontDoor> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DisableCertificateNameCheck] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4619b-110">ByObjectWithBackendPoolsSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="4619b-110">ByObjectWithBackendPoolsSettingParameterSet</span></span>
```
Set-AzFrontDoor -InputObject <PSFrontDoor> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 -BackendPoolsSetting <PSBackendPoolsSetting> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4619b-111">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4619b-111">ByResourceIdParameterSet</span></span>
```
Set-AzFrontDoor -ResourceId <String> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4619b-112">ByResourceIdWithCertificateNameCheckParameterSet</span><span class="sxs-lookup"><span data-stu-id="4619b-112">ByResourceIdWithCertificateNameCheckParameterSet</span></span>
```
Set-AzFrontDoor -ResourceId <String> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 [-DisableCertificateNameCheck] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4619b-113">ByResourceIdWithBackendPoolsSettingParameterSet</span><span class="sxs-lookup"><span data-stu-id="4619b-113">ByResourceIdWithBackendPoolsSettingParameterSet</span></span>
```
Set-AzFrontDoor -ResourceId <String> [-RoutingRule <PSRoutingRule[]>] [-BackendPool <PSBackendPool[]>]
 [-FrontendEndpoint <PSFrontendEndpoint[]>] [-LoadBalancingSetting <PSLoadBalancingSetting[]>]
 [-HealthProbeSetting <PSHealthProbeSetting[]>] [-Tag <Hashtable>] [-EnabledState <PSEnabledState>]
 -BackendPoolsSetting <PSBackendPoolsSetting> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4619b-114">설명은</span><span class="sxs-lookup"><span data-stu-id="4619b-114">DESCRIPTION</span></span>
<span data-ttu-id="4619b-115">**AzFrontDoor** Cmdlet은 전방 도어 부하 분산을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4619b-115">The **Set-AzFrontDoor** cmdlet updates a Front Door load balancer.</span></span> <span data-ttu-id="4619b-116">입력 매개 변수를 제공 하지 않으면 기존 전방 도어의 이전 매개 변수가 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4619b-116">If input parameters are not provided, old parameters from the existing Front Door will be used.</span></span>

## <span data-ttu-id="4619b-117">예제의</span><span class="sxs-lookup"><span data-stu-id="4619b-117">EXAMPLES</span></span>

### <span data-ttu-id="4619b-118">예제 1: FrontDoorName 및 ResourceGroupName를 사용 하 여 기존 전방 도어를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4619b-118">Example 1: update an existing Front Door with FrontDoorName and ResourceGroupName.</span></span>
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

<span data-ttu-id="4619b-119">기존 FrontDoor를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4619b-119">update an existing FrontDoor.</span></span>

### <span data-ttu-id="4619b-120">예제 2: PSFrontDoor 개체를 사용 하 여 기존 전방 도어를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4619b-120">Example 2: update an existing Front Door with PSFrontDoor object.</span></span>
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

<span data-ttu-id="4619b-121">기존 FrontDoor를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4619b-121">update an existing FrontDoor.</span></span>

### <span data-ttu-id="4619b-122">예제 3: ResourceId를 사용 하 여 기존 전방 도어 업데이트</span><span class="sxs-lookup"><span data-stu-id="4619b-122">Example 3: update an existing Front Door with ResourceId</span></span>
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

<span data-ttu-id="4619b-123">기존 FrontDoor를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4619b-123">update an existing FrontDoor.</span></span>

### <span data-ttu-id="4619b-124">예제 4:-DisableCertificateNameCheck 스위치 매개 변수를 사용 하 여 기존 전방 도어의 BackendPoolSetting 속성 EnforceCertificateNameCheck 업데이트</span><span class="sxs-lookup"><span data-stu-id="4619b-124">Example 4: update BackendPoolSetting property EnforceCertificateNameCheck of an existing Front Door with -DisableCertificateNameCheck switch parameter</span></span>
<span data-ttu-id="4619b-125">업데이트 될 전면 도어는 FrontoorName 및 ResourceGroupName, PSFrontDoor 개체 또는 ResourceId를 사용 하 여 식별할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4619b-125">Front Door to be updated can be identified using FrontoorName and ResourceGroupName, PSFrontDoor object, or ResourceId.</span></span> <span data-ttu-id="4619b-126">(예를 들어 3 예제 참조) 아래 예제에서는 PSFrontDoor object를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4619b-126">(See above 3 examples for example) The below example uses PSFrontDoor object.</span></span>

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

<span data-ttu-id="4619b-127">기존 FrontDoor를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4619b-127">update an existing FrontDoor.</span></span>

## <span data-ttu-id="4619b-128">변수</span><span class="sxs-lookup"><span data-stu-id="4619b-128">PARAMETERS</span></span>

### <span data-ttu-id="4619b-129">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="4619b-129">-BackendPool</span></span>
<span data-ttu-id="4619b-130">Backendpools는 라우팅 규칙에 사용 가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="4619b-130">Backendpools available to routing rule.</span></span>

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

### <span data-ttu-id="4619b-131">-BackendPoolsSetting</span><span class="sxs-lookup"><span data-stu-id="4619b-131">-BackendPoolsSetting</span></span>
<span data-ttu-id="4619b-132">모든 backendPools에 대 한 설정</span><span class="sxs-lookup"><span data-stu-id="4619b-132">Settings for all backendPools.</span></span>

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

### <span data-ttu-id="4619b-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4619b-133">-DefaultProfile</span></span>
<span data-ttu-id="4619b-134">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4619b-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4619b-135">-DisableCertificateNameCheck</span><span class="sxs-lookup"><span data-stu-id="4619b-135">-DisableCertificateNameCheck</span></span>
<span data-ttu-id="4619b-136">모든 백 엔드 풀에 대 한 HTTPS 요청에서 인증서 이름 검사를 사용할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4619b-136">Whether to disable certificate name check on HTTPS requests to all backend pools.</span></span> <span data-ttu-id="4619b-137">비 HTTPS 요청에는 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4619b-137">No effect on non-HTTPS requests.</span></span>

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

### <span data-ttu-id="4619b-138">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="4619b-138">-EnabledState</span></span>
<span data-ttu-id="4619b-139">전방 도어 부하 분산 장치의 작동 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="4619b-139">Operational status of the Front Door load balancer.</span></span>

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

### <span data-ttu-id="4619b-140">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="4619b-140">-FrontendEndpoint</span></span>
<span data-ttu-id="4619b-141">라우팅 규칙에 사용할 수 있는 프런트 엔드 끝점입니다.</span><span class="sxs-lookup"><span data-stu-id="4619b-141">Frontend endpoints available to routing rule.</span></span>

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

### <span data-ttu-id="4619b-142">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="4619b-142">-HealthProbeSetting</span></span>
<span data-ttu-id="4619b-143">이 전면 도어 인스턴스와 연결 된 상태 검색 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="4619b-143">Health probe settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="4619b-144">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4619b-144">-InputObject</span></span>
<span data-ttu-id="4619b-145">업데이트할 프론트 도어 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="4619b-145">The Front Door object to update.</span></span>

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

### <span data-ttu-id="4619b-146">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="4619b-146">-LoadBalancingSetting</span></span>
<span data-ttu-id="4619b-147">이 전면 도어 인스턴스와 연결 된 부하 분산 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="4619b-147">Load balancing settings associated with this Front Door instance.</span></span>

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

### <span data-ttu-id="4619b-148">-이름</span><span class="sxs-lookup"><span data-stu-id="4619b-148">-Name</span></span>
<span data-ttu-id="4619b-149">업데이트할 앞면 도어의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4619b-149">The name of the Front Door to update.</span></span>

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

### <span data-ttu-id="4619b-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4619b-150">-ResourceGroupName</span></span>
<span data-ttu-id="4619b-151">앞 문이 속한 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="4619b-151">The resource group to which the Front Door belongs.</span></span>

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

### <span data-ttu-id="4619b-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4619b-152">-ResourceId</span></span>
<span data-ttu-id="4619b-153">업데이트할 앞면 도어의 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="4619b-153">Resource Id of the Front Door to update</span></span>

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

### <span data-ttu-id="4619b-154">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="4619b-154">-RoutingRule</span></span>
<span data-ttu-id="4619b-155">이 FrontDoor 연결 된 라우팅 규칙</span><span class="sxs-lookup"><span data-stu-id="4619b-155">Routing rules associated with this FrontDoor</span></span>

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

### <span data-ttu-id="4619b-156">태그</span><span class="sxs-lookup"><span data-stu-id="4619b-156">-Tag</span></span>
<span data-ttu-id="4619b-157">FrontDoor와 연결 된 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="4619b-157">The tags associate with the FrontDoor.</span></span>

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

### <span data-ttu-id="4619b-158">-확인</span><span class="sxs-lookup"><span data-stu-id="4619b-158">-Confirm</span></span>
<span data-ttu-id="4619b-159">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4619b-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4619b-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4619b-160">-WhatIf</span></span>
<span data-ttu-id="4619b-161">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4619b-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4619b-162">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4619b-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4619b-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4619b-163">CommonParameters</span></span>
<span data-ttu-id="4619b-164">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4619b-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4619b-165">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4619b-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4619b-166">입력</span><span class="sxs-lookup"><span data-stu-id="4619b-166">INPUTS</span></span>

### <span data-ttu-id="4619b-167">FrontDoor. PSFrontDoor/.</span><span class="sxs-lookup"><span data-stu-id="4619b-167">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>
### <span data-ttu-id="4619b-168">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4619b-168">System.String</span></span>
## <span data-ttu-id="4619b-169">출력</span><span class="sxs-lookup"><span data-stu-id="4619b-169">OUTPUTS</span></span>

### <span data-ttu-id="4619b-170">FrontDoor. PSFrontDoor/.</span><span class="sxs-lookup"><span data-stu-id="4619b-170">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>
## <span data-ttu-id="4619b-171">상속자</span><span class="sxs-lookup"><span data-stu-id="4619b-171">NOTES</span></span>

## <span data-ttu-id="4619b-172">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4619b-172">RELATED LINKS</span></span>

<span data-ttu-id="4619b-173">[새로운 AzFrontDoor](./New-AzFrontDoor.md) 
 [Get-AzFrontDoor](./Get-AzFrontDoor.md) 
 [제거-AzFrontDoor](./Remove-AzFrontDoor.md) 
 [새로운 AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md) 
 [새로운 AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md) 
 [새로운 AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md) 
 [새로운 AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md) 
 [새로운 AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="4619b-173">[New-AzFrontDoor](./New-AzFrontDoor.md)
[Get-AzFrontDoor](./Get-AzFrontDoor.md)
[Remove-AzFrontDoor](./Remove-AzFrontDoor.md)
[New-AzFrontDoorRoutingRuleObject](./New-AzFrontDoorRoutingRuleObject.md)
[New-AzFrontDoorHealthProbeSettingObject](./New-AzFrontDoorHealthProbeSettingObject.md)
[New-AzFrontDoorLoadBalancingSettingObject](./New-AzFrontDoorLoadBalancingSettingObject.md)
[New-AzFrontDoorFrontendEndpointObject](./New-AzFrontDoorFrontendEndpointObject.md)
[New-AzFrontDoorBackendPoolObject](./New-AzFrontDoorBackendPoolObject.md)</span></span>
