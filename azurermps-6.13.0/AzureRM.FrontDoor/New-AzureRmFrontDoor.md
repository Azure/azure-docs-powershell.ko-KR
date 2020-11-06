---
<span data-ttu-id="cf643-101">외부 도움말 파일: 모듈 이름: AzureRM FrontDoor online 버전: 해당 URL은 다음과 같아야 합니다. https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoor schema: 2.0.0 content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoor.md original_content_git_url: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml. https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoor.md</span><span class="sxs-lookup"><span data-stu-id="cf643-101">external help file: Microsoft.Azure.Commands.FrontDoor.dll-Help.xml Module Name: AzureRM.FrontDoor online version: The corresponding URL should be the following: https://docs.microsoft.com/en-us/powershell/module/azurerm.frontdoor/new-azurermfrontdoor schema: 2.0.0 content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoor.md original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/FrontDoor/Commands.FrontDoor/help/New-AzureRmFrontDoor.md</span></span>
---

# <a name="new-azurermfrontdoor"></a><span data-ttu-id="cf643-102">New-AzureRmFrontDoor</span><span class="sxs-lookup"><span data-stu-id="cf643-102">New-AzureRmFrontDoor</span></span>

## <a name="synopsis"></a><span data-ttu-id="cf643-103">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cf643-103">SYNOPSIS</span></span>
<span data-ttu-id="cf643-104">새 Azure 프론트 도어 부하 분산 장치 만들기</span><span class="sxs-lookup"><span data-stu-id="cf643-104">Create a new Azure Front Door load balancer</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <a name="syntax"></a><span data-ttu-id="cf643-105">구문과</span><span class="sxs-lookup"><span data-stu-id="cf643-105">SYNTAX</span></span>

```
New-AzureRmFrontDoor -ResourceGroupName <String> -Name <String> -RoutingRule <PSRoutingRule[]>
 -BackendPool <PSBackendPool[]> -FrontendEndpoint <PSFrontendEndpoint[]>
 -LoadBalancingSetting <PSLoadBalancingSetting[]> -HealthProbeSetting <PSHealthProbeSetting[]>
 [-Tag <Hashtable>] [-EnabledState <PSEnabledState>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <a name="description"></a><span data-ttu-id="cf643-106">설명은</span><span class="sxs-lookup"><span data-stu-id="cf643-106">DESCRIPTION</span></span>
<span data-ttu-id="cf643-107">**AzureRmFrontDoor** cmdlet은 현재 구독 아래의 지정 된 리소스 그룹에 새 Azure 전면 도어 부하 분산을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cf643-107">The **New-AzureRmFrontDoor** cmdlet creates a new Azure Front Door load balancer in the specified resource group under current subscription</span></span>

## <a name="examples"></a><span data-ttu-id="cf643-108">예제의</span><span class="sxs-lookup"><span data-stu-id="cf643-108">EXAMPLES</span></span>

### <a name="example-1-create-a-front-door-based-on-given-parameters"></a><span data-ttu-id="cf643-109">예제 1: 주어진 매개 변수를 기반으로 하는 전방 도어를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cf643-109">Example 1: Create a Front Door based on given parameters.</span></span>
```powershell
PS C:\> New-AzureRmFrontDoor -Name "frontDoor1" -ResourceGroupName "rg1" -RoutingRule $routingrule1 -BackendPool $backendpool1 -FrontendEndpoint $frontendEndpoint1 -LoadBalancingSetting $loadBalancingSetting1 -HealthProbeSetting $healthProbeSetting1

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
Id                    : /subscriptions/{guid}/resourcegroups/rg1/providers/M
                        icrosoft.Network/frontdoors/frontdoor1
Name                  : frontdoor1
Type                  : Microsoft.Network/frontdoor1
```

<span data-ttu-id="cf643-110">지정 된 매개 변수를 기반으로 하는 전방 도어를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cf643-110">Create a Front Door based on given parameters.</span></span>

## <a name="parameters"></a><span data-ttu-id="cf643-111">변수</span><span class="sxs-lookup"><span data-stu-id="cf643-111">PARAMETERS</span></span>

### <a name="-backendpool"></a><span data-ttu-id="cf643-112">-BackendPool</span><span class="sxs-lookup"><span data-stu-id="cf643-112">-BackendPool</span></span>
<span data-ttu-id="cf643-113">Backendpools는 라우팅 규칙에 사용 가능 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf643-113">Backendpools available to routing rule.</span></span>

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

### <a name="-defaultprofile"></a><span data-ttu-id="cf643-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf643-114">-DefaultProfile</span></span>
<span data-ttu-id="cf643-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cf643-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <a name="-enabledstate"></a><span data-ttu-id="cf643-116">-EnabledState</span><span class="sxs-lookup"><span data-stu-id="cf643-116">-EnabledState</span></span>
<span data-ttu-id="cf643-117">전방 도어 부하 분산 장치의 EnabledState입니다.</span><span class="sxs-lookup"><span data-stu-id="cf643-117">EnabledState of the Front Door load balancer.</span></span>
<span data-ttu-id="cf643-118">기본값을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf643-118">Default value is Enabled</span></span>

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

### <a name="-frontendendpoint"></a><span data-ttu-id="cf643-119">-FrontendEndpoint</span><span class="sxs-lookup"><span data-stu-id="cf643-119">-FrontendEndpoint</span></span>
<span data-ttu-id="cf643-120">라우팅 규칙에 사용할 수 있는 프런트 엔드 끝점입니다.</span><span class="sxs-lookup"><span data-stu-id="cf643-120">Frontend endpoints available to routing rule.</span></span>

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

### <a name="-healthprobesetting"></a><span data-ttu-id="cf643-121">-HealthProbeSetting</span><span class="sxs-lookup"><span data-stu-id="cf643-121">-HealthProbeSetting</span></span>
<span data-ttu-id="cf643-122">이 전면 도어 인스턴스와 연결 된 상태 검색 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="cf643-122">Health probe settings associated with this Front Door instance.</span></span>

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

### <a name="-loadbalancingsetting"></a><span data-ttu-id="cf643-123">-LoadBalancingSetting</span><span class="sxs-lookup"><span data-stu-id="cf643-123">-LoadBalancingSetting</span></span>
<span data-ttu-id="cf643-124">이 전면 도어 인스턴스와 연결 된 부하 분산 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="cf643-124">Load balancing settings associated with this Front Door instance.</span></span>

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

### <a name="-name"></a><span data-ttu-id="cf643-125">-이름</span><span class="sxs-lookup"><span data-stu-id="cf643-125">-Name</span></span>
<span data-ttu-id="cf643-126">전방 문 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cf643-126">Front Door name.</span></span>

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

### <a name="-resourcegroupname"></a><span data-ttu-id="cf643-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf643-127">-ResourceGroupName</span></span>
<span data-ttu-id="cf643-128">앞 문이 생성 될 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cf643-128">The resource group name that the Front Door will be created in.</span></span>

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

### <a name="-routingrule"></a><span data-ttu-id="cf643-129">-RoutingRule</span><span class="sxs-lookup"><span data-stu-id="cf643-129">-RoutingRule</span></span>
<span data-ttu-id="cf643-130">이 FrontDoor 연결 된 라우팅 규칙</span><span class="sxs-lookup"><span data-stu-id="cf643-130">Routing rules associated with this FrontDoor</span></span>

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

### <a name="-tag"></a><span data-ttu-id="cf643-131">태그</span><span class="sxs-lookup"><span data-stu-id="cf643-131">-Tag</span></span>
<span data-ttu-id="cf643-132">FrontDoor와 연결 된 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="cf643-132">The tags associate with the FrontDoor.</span></span>

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

### <a name="-confirm"></a><span data-ttu-id="cf643-133">-확인</span><span class="sxs-lookup"><span data-stu-id="cf643-133">-Confirm</span></span>
<span data-ttu-id="cf643-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf643-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <a name="-whatif"></a><span data-ttu-id="cf643-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf643-135">-WhatIf</span></span>
<span data-ttu-id="cf643-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cf643-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cf643-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cf643-137">The cmdlet is not run.</span></span>

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

### <a name="commonparameters"></a><span data-ttu-id="cf643-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf643-138">CommonParameters</span></span>
<span data-ttu-id="cf643-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cf643-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf643-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cf643-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <a name="inputs"></a><span data-ttu-id="cf643-141">입력</span><span class="sxs-lookup"><span data-stu-id="cf643-141">INPUTS</span></span>

### <a name="systemstring"></a><span data-ttu-id="cf643-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cf643-142">System.String</span></span>

## <a name="outputs"></a><span data-ttu-id="cf643-143">출력</span><span class="sxs-lookup"><span data-stu-id="cf643-143">OUTPUTS</span></span>

### <a name="microsoftazurecommandsfrontdoormodelspsfrontdoor"></a><span data-ttu-id="cf643-144">FrontDoor. PSFrontDoor/.</span><span class="sxs-lookup"><span data-stu-id="cf643-144">Microsoft.Azure.Commands.FrontDoor.Models.PSFrontDoor</span></span>

## <a name="notes"></a><span data-ttu-id="cf643-145">상속자</span><span class="sxs-lookup"><span data-stu-id="cf643-145">NOTES</span></span>

## <a name="related-links"></a><span data-ttu-id="cf643-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cf643-146">RELATED LINKS</span></span>

<span data-ttu-id="cf643-147">[Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md) 
 [Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md) 
 [제거-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md) 
 [새로운 AzureRmFrontDoorRoutingRuleObject](./New-AzureRmFrontDoorRoutingRuleObject.md) 
 [새로운 AzureRmFrontDoorHealthProbeSettingObject](./New-AzureRmFrontHealthProbeSettingObject.md) 
 [새로운 AzureRmFrontDoorLoadBalancingSettingObject](./New-AzureRmFrontDoorLoadBalancingSettingObject.md) 
 [새로운 AzureRmFrontDoorFrontendEndpointObject](./New-AzureRmFrontDoorFrontendEndpointObject.md) 
 [새로운 AzureRmFrontDoorBackendPoolObject](./New-AzureRmFrontDoorBackendPoolObject.md)</span><span class="sxs-lookup"><span data-stu-id="cf643-147">[Get-AzureRmFrontDoor](./Get-AzureRmFrontDoor.md)
[Set-AzureRmFrontDoor](./Set-AzureRmFrontDoor.md)
[Remove-AzureRmFrontDoor](./Remove-AzureRmFrontDoor.md)
[New-AzureRmFrontDoorRoutingRuleObject](./New-AzureRmFrontDoorRoutingRuleObject.md)
[New-AzureRmFrontDoorHealthProbeSettingObject](./New-AzureRmFrontHealthProbeSettingObject.md)
[New-AzureRmFrontDoorLoadBalancingSettingObject](./New-AzureRmFrontDoorLoadBalancingSettingObject.md)
[New-AzureRmFrontDoorFrontendEndpointObject](./New-AzureRmFrontDoorFrontendEndpointObject.md)
[New-AzureRmFrontDoorBackendPoolObject](./New-AzureRmFrontDoorBackendPoolObject.md)</span></span>
