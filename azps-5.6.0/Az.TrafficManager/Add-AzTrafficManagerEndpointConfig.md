---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33D
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/add-aztrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerEndpointConfig.md
ms.openlocfilehash: 79e3547a8065b20b693b05b7fe4582bbd775abdd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987387"
---
# <span data-ttu-id="f7073-101">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="f7073-101">Add-AzTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="f7073-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7073-102">SYNOPSIS</span></span>
<span data-ttu-id="f7073-103">로컬 Traffic Manager 프로필 개체에 엔드포인트를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="f7073-103">Adds an endpoint to a local Traffic Manager profile object.</span></span>

## <span data-ttu-id="f7073-104">구문</span><span class="sxs-lookup"><span data-stu-id="f7073-104">SYNTAX</span></span>

```
Add-AzTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7073-105">설명</span><span class="sxs-lookup"><span data-stu-id="f7073-105">DESCRIPTION</span></span>
<span data-ttu-id="f7073-106">**Add-AzTrafficManagerEndpointConfig** cmdlet은 로컬 Azure Traffic Manager 프로필 개체에 엔드포인트를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="f7073-106">The **Add-AzTrafficManagerEndpointConfig** cmdlet adds an endpoint to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="f7073-107">New-AzTrafficManagerProfile cmdlet을 사용하여 New-AzTrafficManagerProfile Get-AzTrafficManagerProfile 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f7073-107">You can get a profile by using the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="f7073-108">이 cmdlet은 로컬 프로필 개체에서 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="f7073-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="f7073-109">Set-AzTrafficManagerProfile cmdlet을 사용하여 Traffic Manager 프로필에 변경 내용을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="f7073-109">Commit your changes to the profile for Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="f7073-110">엔드포인트를 만들고 단일 작업에서 변경을 커밋하기 위해 New-AzTrafficManagerEndpoint cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7073-110">To create an endpoint and commit the change in a single operation, use the New-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="f7073-111">예제</span><span class="sxs-lookup"><span data-stu-id="f7073-111">EXAMPLES</span></span>

### <span data-ttu-id="f7073-112">예제 1: 프로필에 엔드포인트 추가</span><span class="sxs-lookup"><span data-stu-id="f7073-112">Example 1: Add an endpoint to a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzTrafficManagerEndpointConfig -EndpointName "contoso" -EndpointStatus Enabled -Target "www.contoso.com" -TrafficManagerProfile $TrafficManagerProfile -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Weight 10
PS C:\> Set-AzTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="f7073-113">첫 번째 명령은 **Get-AzTrafficManagerProfile** cmdlet을 사용하여 Azure Traffic Manager 프로필을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f7073-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="f7073-114">명령은 로컬 프로필을 $TrafficManagerProfile 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="f7073-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="f7073-115">두 번째 명령은 에 저장된 프로필에 contoso라는 엔드포인트를 $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="f7073-115">The second command adds an endpoint named contoso to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="f7073-116">명령에는 엔드포인트에 대한 구성 데이터가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="f7073-116">The command includes configuration data for the endpoint.</span></span>
<span data-ttu-id="f7073-117">이 명령은 로컬 개체만 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="f7073-117">This command changes only the local object.</span></span>

<span data-ttu-id="f7073-118">마지막 명령은 Azure의 Traffic Manager 프로필을 업데이트하여 Azure의 로컬 값과 $TrafficManagerProfile.</span><span class="sxs-lookup"><span data-stu-id="f7073-118">The final command updates the Traffic Manager profile in Azure to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="f7073-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f7073-119">PARAMETERS</span></span>

### <span data-ttu-id="f7073-120">-CustomHeader</span><span class="sxs-lookup"><span data-stu-id="f7073-120">-CustomHeader</span></span>
<span data-ttu-id="f7073-121">프로브 요청에 대한 사용자 지정 헤더 이름 및 값 쌍 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="f7073-121">List of custom header name and value pairs for probe requests.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7073-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7073-122">-DefaultProfile</span></span>
<span data-ttu-id="f7073-123">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f7073-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f7073-124">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="f7073-124">-EndpointLocation</span></span>
<span data-ttu-id="f7073-125">성능 트래픽 라우팅 메서드에서 사용할 엔드포인트의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f7073-125">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="f7073-126">이 매개 변수는 ExternalEndpoints 또는 NestedEndpoints 형식의 엔드포인트에만 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f7073-126">This parameter is only applicable to endpoints of the ExternalEndpoints or the NestedEndpoints type.</span></span>
<span data-ttu-id="f7073-127">성능 트래픽 라우팅 메서드를 사용할 때 이 매개 변수를 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f7073-127">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="f7073-128">Azure 지역 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f7073-128">Specify an Azure region name.</span></span>
<span data-ttu-id="f7073-129">Azure 지역 전체 목록은 Azure 지역(을)을 http://azure.microsoft.com/regions/ http://azure.microsoft.com/regions/) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f7073-129">For a full list of Azure regions, see Azure Regionshttp://azure.microsoft.com/regions/ (http://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="f7073-130">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="f7073-130">-EndpointName</span></span>
<span data-ttu-id="f7073-131">이 cmdlet이 추가하는 Traffic Manager 엔드포인트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f7073-131">Specifies the name of the Traffic Manager endpoint that this cmdlet adds.</span></span>

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

### <span data-ttu-id="f7073-132">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="f7073-132">-EndpointStatus</span></span>
<span data-ttu-id="f7073-133">엔드포인트의 상태를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f7073-133">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="f7073-134">유효한 값은:</span><span class="sxs-lookup"><span data-stu-id="f7073-134">Valid values are:</span></span> 

- <span data-ttu-id="f7073-135">사용 가능</span><span class="sxs-lookup"><span data-stu-id="f7073-135">Enabled</span></span> 
- <span data-ttu-id="f7073-136">사용하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="f7073-136">Disabled</span></span> 

<span data-ttu-id="f7073-137">상태를 사용하도록 설정하면 엔드포인트가 엔드포인트 상태에 대해 프로브되어 트래픽 라우팅 메서드에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="f7073-137">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7073-138">-GeoMapping</span><span class="sxs-lookup"><span data-stu-id="f7073-138">-GeoMapping</span></span>
<span data-ttu-id="f7073-139">'지리적' 트래픽 라우팅 메서드를 사용할 때 이 엔드포인트에 매핑된 지역 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="f7073-139">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="f7073-140">허용되는 값의 전체 목록은 Traffic Manager [설명서를 참조하세요.](https://docs.microsoft.com/azure/traffic-manager/traffic-manager-geographic-regions)</span><span class="sxs-lookup"><span data-stu-id="f7073-140">Please consult Traffic Manager documentation for a [full list of accepted values](https://docs.microsoft.com/azure/traffic-manager/traffic-manager-geographic-regions).</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7073-141">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="f7073-141">-MinChildEndpoints</span></span>
<span data-ttu-id="f7073-142">부모 프로필에서 중첩된 엔드포인트를 사용할 수 있도록 자식 프로필에서 사용할 수 있어야 하는 최소 엔드포인트 수입니다.</span><span class="sxs-lookup"><span data-stu-id="f7073-142">The minimum number of endpoints that must be available in the child profile in order for the Nested Endpoint in the parent profile to be considered available.</span></span>
<span data-ttu-id="f7073-143">'NestedEndpoints'형식의 엔드포인트에만 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f7073-143">Only applicable to endpoint of type 'NestedEndpoints'.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7073-144">-Priority</span><span class="sxs-lookup"><span data-stu-id="f7073-144">-Priority</span></span>
<span data-ttu-id="f7073-145">Traffic Manager가 엔드포인트에 할당하는 우선 순위를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f7073-145">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="f7073-146">이 매개 변수는 Traffic Manager 프로필이 우선 순위 트래픽 라우팅 메서드로 구성된 경우만 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="f7073-146">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="f7073-147">유효한 값은 1에서 1000까지의 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="f7073-147">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="f7073-148">값이 낮을수록 우선 순위가 높을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f7073-148">Lower values represent higher priority.</span></span>

<span data-ttu-id="f7073-149">우선 순위를 지정하는 경우 프로필의 모든 엔드포인트에 우선 순위를 지정해야 합니다. 두 엔드포인트가 동일한 우선 순위 값을 공유할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f7073-149">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="f7073-150">우선 순위를 지정하지 않으면 Traffic Manager는 엔드포인트를 나열하는 순서대로 1(1)부터 엔드포인트에 기본 우선 순위 값을 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="f7073-150">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7073-151">-SubnetMapping</span><span class="sxs-lookup"><span data-stu-id="f7073-151">-SubnetMapping</span></span>
<span data-ttu-id="f7073-152">'서브넷' 트래픽 라우팅 메서드를 사용할 때 이 엔드포인트에 매핑된 주소 범위 또는 서브넷 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="f7073-152">The list of address ranges or subnets mapped to this endpoint when using the 'Subnet' traffic routing method.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7073-153">-Target</span><span class="sxs-lookup"><span data-stu-id="f7073-153">-Target</span></span>
<span data-ttu-id="f7073-154">엔드포인트의 정식 DNS 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f7073-154">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="f7073-155">Traffic Manager는 트래픽을 이 엔드포인트로 지시할 때 DNS 응답에서 이 값을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f7073-155">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="f7073-156">외부 엔드포인트 엔드포인트 형식에만 이 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f7073-156">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="f7073-157">다른 엔드포인트 형식의 경우 *TargetResourceId 매개* 변수를 대신 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f7073-157">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

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

### <span data-ttu-id="f7073-158">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="f7073-158">-TargetResourceId</span></span>
<span data-ttu-id="f7073-159">대상의 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f7073-159">Specifies resource ID of the target.</span></span>
<span data-ttu-id="f7073-160">AzureEndpoints 및 NestedEndpoints 엔드포인트 형식에만 이 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f7073-160">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="f7073-161">ExternalEndpoints 엔드포인트 형식의 경우 대상 매개 *변수를* 대신 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f7073-161">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

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

### <span data-ttu-id="f7073-162">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f7073-162">-TrafficManagerProfile</span></span>
<span data-ttu-id="f7073-163">로컬 **TrafficManagerProfile** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f7073-163">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="f7073-164">이 cmdlet은 이 로컬 개체를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="f7073-164">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="f7073-165">**TrafficManagerProfile** 개체를 얻은 경우 Get-AzTrafficManagerProfile cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="f7073-165">To obtain a **TrafficManagerProfile** object, use the Get-AzTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7073-166">-Type</span><span class="sxs-lookup"><span data-stu-id="f7073-166">-Type</span></span>
<span data-ttu-id="f7073-167">이 cmdlet이 Azure Traffic Manager 프로필에 추가하는 엔드포인트 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f7073-167">Specifies the type of endpoint that this cmdlet adds to the Azure Traffic Manager profile.</span></span>
<span data-ttu-id="f7073-168">유효한 값은:</span><span class="sxs-lookup"><span data-stu-id="f7073-168">Valid values are:</span></span> 

- <span data-ttu-id="f7073-169">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="f7073-169">AzureEndpoints</span></span>
- <span data-ttu-id="f7073-170">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="f7073-170">ExternalEndpoints</span></span>
- <span data-ttu-id="f7073-171">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="f7073-171">NestedEndpoints</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7073-172">-Weight</span><span class="sxs-lookup"><span data-stu-id="f7073-172">-Weight</span></span>
<span data-ttu-id="f7073-173">Traffic Manager가 엔드포인트에 할당하는 가중치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f7073-173">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="f7073-174">유효한 값은 1에서 1000까지의 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="f7073-174">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="f7073-175">기본값은 1(1)입니다.</span><span class="sxs-lookup"><span data-stu-id="f7073-175">The default value is one (1).</span></span>
<span data-ttu-id="f7073-176">이 매개 변수는 Traffic Manager 프로필이 가중 트래픽 라우팅 메서드로 구성된 경우만 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="f7073-176">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7073-177">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7073-177">CommonParameters</span></span>
<span data-ttu-id="f7073-178">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f7073-178">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7073-179">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f7073-179">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7073-180">입력</span><span class="sxs-lookup"><span data-stu-id="f7073-180">INPUTS</span></span>

### <span data-ttu-id="f7073-181">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f7073-181">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="f7073-182">출력</span><span class="sxs-lookup"><span data-stu-id="f7073-182">OUTPUTS</span></span>

### <span data-ttu-id="f7073-183">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f7073-183">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="f7073-184">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f7073-184">NOTES</span></span>

## <span data-ttu-id="f7073-185">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f7073-185">RELATED LINKS</span></span>

[<span data-ttu-id="f7073-186">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f7073-186">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="f7073-187">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f7073-187">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="f7073-188">Remove-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="f7073-188">Remove-AzTrafficManagerEndpointConfig</span></span>](./Remove-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="f7073-189">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f7073-189">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


