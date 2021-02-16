---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: A7A908A1-7326-4725-A3F9-4D05E40C5F73
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/new-aztrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerEndpoint.md
ms.openlocfilehash: 9a32176afba8f4182ee1300e9b38936e9f35746c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195513"
---
# <span data-ttu-id="16c04-101">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="16c04-101">New-AzTrafficManagerEndpoint</span></span>

## <span data-ttu-id="16c04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16c04-102">SYNOPSIS</span></span>
<span data-ttu-id="16c04-103">Traffic Manager 프로필에서 엔드포인트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="16c04-103">Creates an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="16c04-104">구문</span><span class="sxs-lookup"><span data-stu-id="16c04-104">SYNTAX</span></span>

```
New-AzTrafficManagerEndpoint -Name <String> -ProfileName <String> -ResourceGroupName <String> -Type <String>
 [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>]
 [-SubnetMapping <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerIpAddressRange]>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="16c04-105">설명</span><span class="sxs-lookup"><span data-stu-id="16c04-105">DESCRIPTION</span></span>
<span data-ttu-id="16c04-106">**New-AzTrafficManagerEndpoint** cmdlet은 Azure Traffic Manager 프로필에 엔드포인트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="16c04-106">The **New-AzTrafficManagerEndpoint** cmdlet creates an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="16c04-107">이 cmdlet은 Traffic Manager 서비스에 각 새 엔드포인트를 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="16c04-107">This cmdlet commits each new endpoint to the Traffic Manager service.</span></span>
<span data-ttu-id="16c04-108">로컬 Traffic Manager 프로필 개체에 여러 엔드포인트를 추가하고 단일 작업에서 변경 내용을 커밋하려면 Add-AzTrafficManagerEndpointConfig cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="16c04-108">To add multiple endpoints to a local Traffic Manager profile object and commit changes in a single operation, use the Add-AzTrafficManagerEndpointConfig cmdlet.</span></span>

## <span data-ttu-id="16c04-109">예제</span><span class="sxs-lookup"><span data-stu-id="16c04-109">EXAMPLES</span></span>

### <span data-ttu-id="16c04-110">예제 1: 프로필에 대한 외부 엔드포인트 만들기</span><span class="sxs-lookup"><span data-stu-id="16c04-110">Example 1: Create an external endpoint for a profile</span></span>
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Target "www.contoso.com" -Weight 10
```

<span data-ttu-id="16c04-111">이 명령은 ResourceGroup11이라는 리소스 그룹의 ContosoProfile 프로필에 contoso라는 외부 엔드포인트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="16c04-111">This command creates an external endpoint named contoso in the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="16c04-112">예제 2: 프로필에 대한 Azure 엔드포인트 만들기</span><span class="sxs-lookup"><span data-stu-id="16c04-112">Example 2: Create an Azure endpoint for a profile</span></span>
```
PS C:\>New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
```

<span data-ttu-id="16c04-113">이 명령은 리소스 그룹 ResourceGroup11의 ContosoProfile 프로필에 contoso라는 Azure 엔드포인트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="16c04-113">This command creates an Azure endpoint named contoso in the profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="16c04-114">Azure 엔드포인트는 *TargetResourceId의* URI 경로에 의해 Azure Resource Manager ID가 부여된 Azure 웹앱을 대상으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="16c04-114">The Azure endpoint points to the Azure Web App whose Azure Resource Manager ID is given by the URI path in *TargetResourceId*.</span></span>
<span data-ttu-id="16c04-115">웹앱 리소스가 위치를 제공하기 때문에 이 명령은 *EndpointLocation* 매개 변수를 지정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="16c04-115">The command does not specify the *EndpointLocation* parameter because the Web App resource supplies the location.</span></span>

## <span data-ttu-id="16c04-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16c04-116">PARAMETERS</span></span>

### <span data-ttu-id="16c04-117">-CustomHeader</span><span class="sxs-lookup"><span data-stu-id="16c04-117">-CustomHeader</span></span>
<span data-ttu-id="16c04-118">프로브 요청에 대한 사용자 지정 헤더 이름 및 값 쌍 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="16c04-118">List of custom header name and value pairs for probe requests.</span></span>

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

### <span data-ttu-id="16c04-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16c04-119">-DefaultProfile</span></span>
<span data-ttu-id="16c04-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="16c04-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16c04-121">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="16c04-121">-EndpointLocation</span></span>
<span data-ttu-id="16c04-122">성능 트래픽 라우팅 메서드에 사용할 엔드포인트의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="16c04-122">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="16c04-123">이 매개 변수는 ExternalEndpoints 또는 NestedEndpoints 유형의 엔드포인트에만 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16c04-123">This parameter is only applicable to endpoints of the ExternalEndpoints or NestedEndpoints type.</span></span>
<span data-ttu-id="16c04-124">성능 트래픽 라우팅 메서드를 사용할 때 이 매개 변수를 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="16c04-124">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="16c04-125">Azure 지역 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="16c04-125">Specify an Azure region name.</span></span>
<span data-ttu-id="16c04-126">Azure 지역 전체 목록은 Azure http://azure.microsoft.com/regions/ http://azure.microsoft.com/regions/) 지역(.</span><span class="sxs-lookup"><span data-stu-id="16c04-126">For a full list of Azure regions, see Azure Regionshttp://azure.microsoft.com/regions/ (http://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="16c04-127">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="16c04-127">-EndpointStatus</span></span>
<span data-ttu-id="16c04-128">엔드포인트의 상태를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="16c04-128">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="16c04-129">유효한 값은</span><span class="sxs-lookup"><span data-stu-id="16c04-129">Valid values are:</span></span> 

- <span data-ttu-id="16c04-130">사용</span><span class="sxs-lookup"><span data-stu-id="16c04-130">Enabled</span></span> 
- <span data-ttu-id="16c04-131">사용 안</span><span class="sxs-lookup"><span data-stu-id="16c04-131">Disabled</span></span> 

<span data-ttu-id="16c04-132">상태가 사용되면 엔드포인트가 엔드포인트 상태에 대해 프로브되어 트래픽 라우팅 메서드에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="16c04-132">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

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

### <span data-ttu-id="16c04-133">-GeoMapping</span><span class="sxs-lookup"><span data-stu-id="16c04-133">-GeoMapping</span></span>
<span data-ttu-id="16c04-134">'지리적' 트래픽 라우팅 방법을 사용하는 경우 이 엔드포인트에 매핑된 지역 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="16c04-134">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="16c04-135">허용되는 값의 전체 목록은 Traffic Manager 설명서를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="16c04-135">Please consult Traffic Manager documentation for a full list of accepted values.</span></span>

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

### <span data-ttu-id="16c04-136">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="16c04-136">-MinChildEndpoints</span></span>
<span data-ttu-id="16c04-137">Azure 지역 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="16c04-137">Specify an Azure region name.</span></span>
<span data-ttu-id="16c04-138">Azure 지역 전체 목록은 Azure http://azure.microsoft.com/regions/ http://azure.microsoft.com/regions/) 지역(.</span><span class="sxs-lookup"><span data-stu-id="16c04-138">For a full list of Azure regions, see Azure Regionshttp://azure.microsoft.com/regions/ (http://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="16c04-139">-Name</span><span class="sxs-lookup"><span data-stu-id="16c04-139">-Name</span></span>
<span data-ttu-id="16c04-140">이 cmdlet에서 만드는 Traffic Manager 엔드포인트의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="16c04-140">Specifies the name of the Traffic Manager endpoint that this cmdlet creates.</span></span>

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

### <span data-ttu-id="16c04-141">-Priority</span><span class="sxs-lookup"><span data-stu-id="16c04-141">-Priority</span></span>
<span data-ttu-id="16c04-142">Traffic Manager가 엔드포인트에 할당하는 우선 순위를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="16c04-142">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="16c04-143">이 매개 변수는 Traffic Manager 프로필이 우선 순위 트래픽 라우팅 메서드로 구성된 경우만 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="16c04-143">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="16c04-144">유효한 값은 1에서 1000까지의 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="16c04-144">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="16c04-145">낮은 값은 높은 우선 순위를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="16c04-145">Lower values represent higher priority.</span></span>

<span data-ttu-id="16c04-146">우선 순위를 지정하는 경우 프로필의 모든 엔드포인트에 우선 순위를 지정해야 합니다. 두 엔드포인트가 동일한 우선 순위 값을 공유할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="16c04-146">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="16c04-147">우선 순위를 지정하지 않으면 Traffic Manager는 엔드포인트에 기본 우선 순위 값을 할당합니다( 1부터 시작하여 프로필이 엔드포인트를 나열하는 순서대로).</span><span class="sxs-lookup"><span data-stu-id="16c04-147">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

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

### <span data-ttu-id="16c04-148">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="16c04-148">-ProfileName</span></span>
<span data-ttu-id="16c04-149">이 cmdlet에서 엔드포인트를 추가하는 Traffic Manager 프로필의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="16c04-149">Specifies the name of a Traffic Manager profile to which this cmdlet adds an endpoint.</span></span>
<span data-ttu-id="16c04-150">프로필을 얻습니다. New-AzTrafficManagerProfile Get-AzTrafficManagerProfile cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="16c04-150">To obtain a profile, use the New-AzTrafficManagerProfile or Get-AzTrafficManagerProfile cmdlets.</span></span>

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

### <span data-ttu-id="16c04-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16c04-151">-ResourceGroupName</span></span>
<span data-ttu-id="16c04-152">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="16c04-152">Specifies the name of a resource group.</span></span>
<span data-ttu-id="16c04-153">이 cmdlet은 이 매개 변수가 지정하는 그룹에 Traffic Manager 엔드포인트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="16c04-153">This cmdlet creates a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="16c04-154">-SubnetMapping</span><span class="sxs-lookup"><span data-stu-id="16c04-154">-SubnetMapping</span></span>
<span data-ttu-id="16c04-155">'서브넷' 트래픽 라우팅 방법을 사용할 때 이 엔드포인트에 매핑된 주소 범위 또는 서브넷 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="16c04-155">The list of address ranges or subnets mapped to this endpoint when using the 'Subnet' traffic routing method.</span></span>

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

### <span data-ttu-id="16c04-156">-Target</span><span class="sxs-lookup"><span data-stu-id="16c04-156">-Target</span></span>
<span data-ttu-id="16c04-157">엔드포인트의 정식 DNS 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="16c04-157">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="16c04-158">Traffic Manager는 트래픽을 이 엔드포인트로 지시할 때 DNS 응답에서 이 값을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="16c04-158">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="16c04-159">ExternalEndpoints 엔드포인트 형식에만 이 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="16c04-159">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="16c04-160">다른 엔드포인트 형식의 경우 *TargetResourceId* 매개 변수를 대신 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="16c04-160">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

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

### <span data-ttu-id="16c04-161">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="16c04-161">-TargetResourceId</span></span>
<span data-ttu-id="16c04-162">대상의 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="16c04-162">Specifies resource ID of the target.</span></span>
<span data-ttu-id="16c04-163">AzureEndpoints 및 NestedEndpoints 엔드포인트 유형에만 이 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="16c04-163">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="16c04-164">ExternalEndpoints 엔드포인트 형식의 경우 대상 매개 *변수를 대신* 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="16c04-164">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

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

### <span data-ttu-id="16c04-165">-Type</span><span class="sxs-lookup"><span data-stu-id="16c04-165">-Type</span></span>
<span data-ttu-id="16c04-166">이 cmdlet이 Traffic Manager 프로필에 추가하는 엔드포인트의 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="16c04-166">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="16c04-167">유효한 값은</span><span class="sxs-lookup"><span data-stu-id="16c04-167">Valid values are:</span></span> 

- <span data-ttu-id="16c04-168">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="16c04-168">AzureEndpoints</span></span>
- <span data-ttu-id="16c04-169">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="16c04-169">ExternalEndpoints</span></span>
- <span data-ttu-id="16c04-170">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="16c04-170">NestedEndpoints</span></span>

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

### <span data-ttu-id="16c04-171">-Weight</span><span class="sxs-lookup"><span data-stu-id="16c04-171">-Weight</span></span>
<span data-ttu-id="16c04-172">Traffic Manager가 엔드포인트에 할당하는 가중치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="16c04-172">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="16c04-173">유효한 값은 1에서 1000까지의 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="16c04-173">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="16c04-174">기본값은 1(1)입니다.</span><span class="sxs-lookup"><span data-stu-id="16c04-174">The default value is one (1).</span></span>
<span data-ttu-id="16c04-175">이 매개 변수는 Traffic Manager 프로필이 가중 트래픽 라우팅 메서드로 구성된 경우만 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="16c04-175">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

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

### <span data-ttu-id="16c04-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16c04-176">CommonParameters</span></span>
<span data-ttu-id="16c04-177">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="16c04-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16c04-178">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="16c04-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16c04-179">입력</span><span class="sxs-lookup"><span data-stu-id="16c04-179">INPUTS</span></span>

### <span data-ttu-id="16c04-180">없음</span><span class="sxs-lookup"><span data-stu-id="16c04-180">None</span></span>

## <span data-ttu-id="16c04-181">출력</span><span class="sxs-lookup"><span data-stu-id="16c04-181">OUTPUTS</span></span>

### <span data-ttu-id="16c04-182">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="16c04-182">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="16c04-183">참고 사항</span><span class="sxs-lookup"><span data-stu-id="16c04-183">NOTES</span></span>

## <span data-ttu-id="16c04-184">관련 링크</span><span class="sxs-lookup"><span data-stu-id="16c04-184">RELATED LINKS</span></span>

[<span data-ttu-id="16c04-185">Disable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="16c04-185">Disable-AzTrafficManagerEndpoint</span></span>](./Disable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="16c04-186">Enable-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="16c04-186">Enable-AzTrafficManagerEndpoint</span></span>](./Enable-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="16c04-187">Get-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="16c04-187">Get-AzTrafficManagerEndpoint</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="16c04-188">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="16c04-188">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="16c04-189">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="16c04-189">New-AzTrafficManagerProfile</span></span>](./New-AzTrafficManagerProfile.md)

[<span data-ttu-id="16c04-190">Remove-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="16c04-190">Remove-AzTrafficManagerEndpoint</span></span>](./Remove-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="16c04-191">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="16c04-191">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)

