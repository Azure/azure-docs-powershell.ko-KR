---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: A7A908A1-7326-4725-A3F9-4D05E40C5F73
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/new-azurermtrafficmanagerendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerEndpoint.md
ms.openlocfilehash: 6117bbae035653762d99096eb8735885c0554d0c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703201"
---
# <span data-ttu-id="9820c-101">New-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9820c-101">New-AzureRmTrafficManagerEndpoint</span></span>

## <span data-ttu-id="9820c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9820c-102">SYNOPSIS</span></span>
<span data-ttu-id="9820c-103">Traffic Manager 프로필에서 끝점을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9820c-103">Creates an endpoint in a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9820c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9820c-104">SYNTAX</span></span>

```
New-AzureRmTrafficManagerEndpoint -Name <String> -ProfileName <String> -ResourceGroupName <String>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9820c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9820c-105">DESCRIPTION</span></span>
<span data-ttu-id="9820c-106">**AzureRmTrafficManagerEndpoint** Cmdlet은 Azure Traffic Manager 프로필에서 끝점을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9820c-106">The **New-AzureRmTrafficManagerEndpoint** cmdlet creates an endpoint in an Azure Traffic Manager profile.</span></span>

<span data-ttu-id="9820c-107">이 cmdlet은 각 새 끝점을 Traffic Manager 서비스에 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="9820c-107">This cmdlet commits each new endpoint to the Traffic Manager service.</span></span>
<span data-ttu-id="9820c-108">로컬 Traffic Manager 프로필 개체에 여러 끝점을 추가 하 고 한 번의 작업으로 변경 내용을 커밋하려면 Add-AzureRmTrafficManagerEndpointConfig cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9820c-108">To add multiple endpoints to a local Traffic Manager profile object and commit changes in a single operation, use the Add-AzureRmTrafficManagerEndpointConfig cmdlet.</span></span>

## <span data-ttu-id="9820c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="9820c-109">EXAMPLES</span></span>

### <span data-ttu-id="9820c-110">예제 1: 프로필에 대 한 외부 끝점 만들기</span><span class="sxs-lookup"><span data-stu-id="9820c-110">Example 1: Create an external endpoint for a profile</span></span>
```
PS C:\>New-AzureRmTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Target "www.contoso.com" -Weight 10
```

<span data-ttu-id="9820c-111">이 명령은 ResourceGroup11 이라는 리소스 그룹의 ContosoProfile 이라는 프로필에 contoso 라는 외부 끝점을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9820c-111">This command creates an external endpoint named contoso in the profile named ContosoProfile in the resource group named ResourceGroup11.</span></span>

### <span data-ttu-id="9820c-112">예제 2: 프로필에 대 한 Azure 끝점 만들기</span><span class="sxs-lookup"><span data-stu-id="9820c-112">Example 2: Create an Azure endpoint for a profile</span></span>
```
PS C:\>New-AzureRmTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
```

<span data-ttu-id="9820c-113">이 명령은 리소스 그룹 ResouceGroup11의 ContosoProfile 라는 프로필에 contoso 라는 Azure 끝점을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9820c-113">This command creates an Azure endpoint named contoso in the profile named ContosoProfile in resource group ResouceGroup11.</span></span>
<span data-ttu-id="9820c-114">Azure endpoint는 Azure 리소스 관리자 ID가 *TargetResourceId* 의 URI 경로로 지정 된 Azure 웹 앱을 가리킵니다.</span><span class="sxs-lookup"><span data-stu-id="9820c-114">The Azure endpoint points to the Azure Web App whose Azure Resource Manager ID is given by the URI path in *TargetResourceId*.</span></span>
<span data-ttu-id="9820c-115">웹 앱 리소스가 위치를 제공 하기 때문에 명령이 *Endpointlocation* 매개 변수를 지정 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9820c-115">The command does not specify the *EndpointLocation* parameter because the Web App resource supplies the location.</span></span>

## <span data-ttu-id="9820c-116">변수</span><span class="sxs-lookup"><span data-stu-id="9820c-116">PARAMETERS</span></span>

### <span data-ttu-id="9820c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9820c-117">-DefaultProfile</span></span>
<span data-ttu-id="9820c-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9820c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9820c-119">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="9820c-119">-EndpointLocation</span></span>
<span data-ttu-id="9820c-120">성능 트래픽 라우팅 메서드에 사용할 끝점의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9820c-120">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="9820c-121">이 매개 변수는 ExternalEndpoints 또는 NestedEndpoints 형식의 끝점에만 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9820c-121">This parameter is only applicable to endpoints of the ExternalEndpoints or NestedEndpoints type.</span></span>
<span data-ttu-id="9820c-122">성능 트래픽 라우팅 메서드를 사용 하는 경우이 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9820c-122">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="9820c-123">Azure 지역 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9820c-123">Specify an Azure region name.</span></span>
<span data-ttu-id="9820c-124">Azure 지역 전체 목록은 Azure 지역 https://azure.microsoft.com/regions/ (()을 참조 하세요 https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="9820c-124">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9820c-125">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="9820c-125">-EndpointStatus</span></span>
<span data-ttu-id="9820c-126">끝점의 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9820c-126">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="9820c-127">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9820c-127">Valid values are:</span></span> 

- <span data-ttu-id="9820c-128">수</span><span class="sxs-lookup"><span data-stu-id="9820c-128">Enabled</span></span> 
- <span data-ttu-id="9820c-129">비활성화</span><span class="sxs-lookup"><span data-stu-id="9820c-129">Disabled</span></span> 

<span data-ttu-id="9820c-130">상태를 사용 하는 경우 끝점은 끝점 상태를 조사 하 고 트래픽 라우팅 메서드에 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9820c-130">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9820c-131">-GeoMapping</span><span class="sxs-lookup"><span data-stu-id="9820c-131">-GeoMapping</span></span>
<span data-ttu-id="9820c-132">' 지역 ' 트래픽 라우팅 방법을 사용할 때이 끝점에 매핑되는 영역의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="9820c-132">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="9820c-133">허용 되는 값의 전체 목록은 Traffic Manager 설명서를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9820c-133">Please consult Traffic Manager documentation for a full list of accepted values.</span></span>
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

### <span data-ttu-id="9820c-134">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="9820c-134">-MinChildEndpoints</span></span>
<span data-ttu-id="9820c-135">Azure 지역 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9820c-135">Specify an Azure region name.</span></span>
<span data-ttu-id="9820c-136">Azure 지역 전체 목록은 Azure 지역 https://azure.microsoft.com/regions/ (()을 참조 하세요 https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="9820c-136">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9820c-137">-이름</span><span class="sxs-lookup"><span data-stu-id="9820c-137">-Name</span></span>
<span data-ttu-id="9820c-138">이 cmdlet이 만드는 Traffic Manager 끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9820c-138">Specifies the name of the Traffic Manager endpoint that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9820c-139">-우선 순위</span><span class="sxs-lookup"><span data-stu-id="9820c-139">-Priority</span></span>
<span data-ttu-id="9820c-140">트래픽 관리자가 끝점에 할당 하는 우선 순위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9820c-140">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="9820c-141">이 매개 변수는 트래픽 관리자 프로필이 우선 순위의 트래픽 라우팅 메서드를 사용 하 여 구성 된 경우에만 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9820c-141">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="9820c-142">유효한 값은 1부터 1000 까지의 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="9820c-142">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="9820c-143">값이 낮을수록 높은 우선 순위를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9820c-143">Lower values represent higher priority.</span></span>

<span data-ttu-id="9820c-144">우선 순위를 지정 하는 경우 프로필의 모든 끝점에 대 한 우선 순위를 지정 해야 하며, 두 종점이 같은 우선 순위 값을 공유할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9820c-144">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="9820c-145">우선 순위를 지정 하지 않으면 트래픽 관리자가 끝점에 기본 우선 순위 값 (1)부터 끝점을 나열 하는 순서 대로 해당 프로필에 대 한 기본값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9820c-145">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9820c-146">-/Profile</span><span class="sxs-lookup"><span data-stu-id="9820c-146">-ProfileName</span></span>
<span data-ttu-id="9820c-147">이 cmdlet이 끝점을 추가 하는 Traffic Manager 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9820c-147">Specifies the name of a Traffic Manager profile to which this cmdlet adds an endpoint.</span></span>
<span data-ttu-id="9820c-148">프로필을 얻으려면 New-AzureRmTrafficManagerProfile 또는 Get-AzureRmTrafficManagerProfile cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9820c-148">To obtain a profile, use the New-AzureRmTrafficManagerProfile or Get-AzureRmTrafficManagerProfile cmdlets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9820c-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9820c-149">-ResourceGroupName</span></span>
<span data-ttu-id="9820c-150">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9820c-150">Specifies the name of a resource group.</span></span>
<span data-ttu-id="9820c-151">이 cmdlet은이 매개 변수에서 지정 하는 그룹에 트래픽 관리자 끝점을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9820c-151">This cmdlet creates a Traffic Manager endpoint in the group that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9820c-152">-대상</span><span class="sxs-lookup"><span data-stu-id="9820c-152">-Target</span></span>
<span data-ttu-id="9820c-153">끝점의 정규화 된 DNS 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9820c-153">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="9820c-154">트래픽 관리자는 트래픽을이 끝점으로 이동할 때 DNS 응답에이 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9820c-154">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="9820c-155">이 매개 변수는 ExternalEndpoints 끝점 형식에만 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9820c-155">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="9820c-156">다른 끝점 형식의 경우 대신 *TargetResourceId* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9820c-156">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9820c-157">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="9820c-157">-TargetResourceId</span></span>
<span data-ttu-id="9820c-158">대상의 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9820c-158">Specifies resource ID of the target.</span></span>
<span data-ttu-id="9820c-159">AzureEndpoints 및 NestedEndpoints endpoint 형식에 대해서만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9820c-159">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="9820c-160">ExternalEndpoints 끝점 형식의 경우 *Target* 매개 변수를 대신 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9820c-160">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9820c-161">-Type</span><span class="sxs-lookup"><span data-stu-id="9820c-161">-Type</span></span>
<span data-ttu-id="9820c-162">이 cmdlet이 Traffic Manager 프로필에 추가 하는 끝점 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9820c-162">Specifies the type of endpoint that this cmdlet adds to the Traffic Manager profile.</span></span>
<span data-ttu-id="9820c-163">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9820c-163">Valid values are:</span></span> 

- <span data-ttu-id="9820c-164">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="9820c-164">AzureEndpoints</span></span>
- <span data-ttu-id="9820c-165">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="9820c-165">ExternalEndpoints</span></span>
- <span data-ttu-id="9820c-166">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="9820c-166">NestedEndpoints</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AzureEndpoints, ExternalEndpoints, NestedEndpoints

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9820c-167">-중량</span><span class="sxs-lookup"><span data-stu-id="9820c-167">-Weight</span></span>
<span data-ttu-id="9820c-168">트래픽 관리자가 끝점에 할당 하는 가중치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9820c-168">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="9820c-169">유효한 값은 1부터 1000 까지의 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="9820c-169">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="9820c-170">기본값은 1입니다.</span><span class="sxs-lookup"><span data-stu-id="9820c-170">The default value is one (1).</span></span>
<span data-ttu-id="9820c-171">이 매개 변수는 트래픽 관리자 프로필이 가중치가 있는 트래픽 라우팅 방법으로 구성 된 경우에만 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9820c-171">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9820c-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9820c-172">CommonParameters</span></span>
<span data-ttu-id="9820c-173">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9820c-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9820c-174">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9820c-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9820c-175">입력</span><span class="sxs-lookup"><span data-stu-id="9820c-175">INPUTS</span></span>

### <span data-ttu-id="9820c-176">않아야</span><span class="sxs-lookup"><span data-stu-id="9820c-176">None</span></span>
<span data-ttu-id="9820c-177">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9820c-177">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9820c-178">출력</span><span class="sxs-lookup"><span data-stu-id="9820c-178">OUTPUTS</span></span>

### <span data-ttu-id="9820c-179">TrafficManager. TrafficManagerEndpoint/.</span><span class="sxs-lookup"><span data-stu-id="9820c-179">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="9820c-180">상속자</span><span class="sxs-lookup"><span data-stu-id="9820c-180">NOTES</span></span>

## <span data-ttu-id="9820c-181">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9820c-181">RELATED LINKS</span></span>

[<span data-ttu-id="9820c-182">Disable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9820c-182">Disable-AzureRmTrafficManagerEndpoint</span></span>](./Disable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="9820c-183">Enable-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9820c-183">Enable-AzureRmTrafficManagerEndpoint</span></span>](./Enable-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="9820c-184">Get-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9820c-184">Get-AzureRmTrafficManagerEndpoint</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="9820c-185">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9820c-185">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="9820c-186">새로운 AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9820c-186">New-AzureRmTrafficManagerProfile</span></span>](./New-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="9820c-187">제거-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9820c-187">Remove-AzureRmTrafficManagerEndpoint</span></span>](./Remove-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="9820c-188">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9820c-188">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


