---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/add-azurermtrafficmanagerendpointconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerEndpointConfig.md
ms.openlocfilehash: e9e6817d9a290acf1e91067edfd90cdf8081f1f0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532583"
---
# <span data-ttu-id="89dc2-101">Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="89dc2-101">Add-AzureRmTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="89dc2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89dc2-102">SYNOPSIS</span></span>
<span data-ttu-id="89dc2-103">로컬 트래픽 관리자 프로필 개체에 끝점을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="89dc2-103">Adds an endpoint to a local Traffic Manager profile object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89dc2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="89dc2-104">SYNTAX</span></span>

```
Add-AzureRmTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="89dc2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="89dc2-105">DESCRIPTION</span></span>
<span data-ttu-id="89dc2-106">**Add-AzureRmTrafficManagerEndpointConfig** cmdlet은 로컬 Azure Traffic Manager 프로필 개체에 끝점을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="89dc2-106">The **Add-AzureRmTrafficManagerEndpointConfig** cmdlet adds an endpoint to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="89dc2-107">New-AzureRmTrafficManagerProfile 또는 Get-AzureRmTrafficManagerProfile cmdlet을 사용 하 여 프로필을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="89dc2-107">You can get a profile by using the New-AzureRmTrafficManagerProfile or Get-AzureRmTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="89dc2-108">이 cmdlet은 로컬 프로필 개체에서 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="89dc2-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="89dc2-109">Set-AzureRmTrafficManagerProfile cmdlet을 사용 하 여 트래픽 관리자의 프로필에 대 한 변경 내용을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="89dc2-109">Commit your changes to the profile for Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="89dc2-110">끝점을 만들고 단일 작업으로 변경 내용을 커밋하려면 New-AzureRmTrafficManagerEndpoint cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="89dc2-110">To create an endpoint and commit the change in a single operation, use the New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="89dc2-111">예제의</span><span class="sxs-lookup"><span data-stu-id="89dc2-111">EXAMPLES</span></span>

### <span data-ttu-id="89dc2-112">예제 1: 프로필에 끝점 추가</span><span class="sxs-lookup"><span data-stu-id="89dc2-112">Example 1: Add an endpoint to a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzureRmTrafficManagerEndpointConfig -EndpointName "contoso" -EndpointStatus Enabled -Target "www.contoso.com" -TrafficManagerProfile $TrafficManagerProfile -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Weight 10
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="89dc2-113">첫 번째 명령은 **AzureRmTrafficManagerProfile** cmdlet을 사용 하 여 Azure Traffic Manager 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="89dc2-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzureRmTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="89dc2-114">명령은 로컬 프로필을 $TrafficManagerProfile 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="89dc2-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="89dc2-115">두 번째 명령은 contoso 이라는 이름의 끝점을 $TrafficManagerProfile에 저장 된 프로필에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="89dc2-115">The second command adds an endpoint named contoso to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="89dc2-116">명령에 끝점에 대 한 구성 데이터가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="89dc2-116">The command includes configuration data for the endpoint.</span></span>
<span data-ttu-id="89dc2-117">이 명령은 로컬 개체만 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="89dc2-117">This command changes only the local object.</span></span>

<span data-ttu-id="89dc2-118">마지막 명령은 $TrafficManagerProfile의 로컬 값과 일치 하도록 Azure의 Traffic Manager 프로필을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="89dc2-118">The final command updates the Traffic Manager profile in Azure to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="89dc2-119">변수</span><span class="sxs-lookup"><span data-stu-id="89dc2-119">PARAMETERS</span></span>

### <span data-ttu-id="89dc2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89dc2-120">-DefaultProfile</span></span>
<span data-ttu-id="89dc2-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="89dc2-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89dc2-122">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="89dc2-122">-EndpointLocation</span></span>
<span data-ttu-id="89dc2-123">성능 트래픽 라우팅 메서드에 사용할 끝점의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89dc2-123">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="89dc2-124">이 매개 변수는 ExternalEndpoints 또는 NestedEndpoints 형식의 끝점에만 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="89dc2-124">This parameter is only applicable to endpoints of the ExternalEndpoints or the NestedEndpoints type.</span></span>
<span data-ttu-id="89dc2-125">성능 트래픽 라우팅 메서드를 사용 하는 경우이 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="89dc2-125">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="89dc2-126">Azure 지역 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89dc2-126">Specify an Azure region name.</span></span>
<span data-ttu-id="89dc2-127">Azure 지역 전체 목록은 Azure 지역 https://azure.microsoft.com/regions/ (()을 참조 하세요 https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="89dc2-127">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="89dc2-128">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="89dc2-128">-EndpointName</span></span>
<span data-ttu-id="89dc2-129">이 cmdlet이 추가 하는 Traffic Manager 끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89dc2-129">Specifies the name of the Traffic Manager endpoint that this cmdlet adds.</span></span>

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

### <span data-ttu-id="89dc2-130">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="89dc2-130">-EndpointStatus</span></span>
<span data-ttu-id="89dc2-131">끝점의 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89dc2-131">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="89dc2-132">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="89dc2-132">Valid values are:</span></span> 

- <span data-ttu-id="89dc2-133">수</span><span class="sxs-lookup"><span data-stu-id="89dc2-133">Enabled</span></span> 
- <span data-ttu-id="89dc2-134">비활성화</span><span class="sxs-lookup"><span data-stu-id="89dc2-134">Disabled</span></span> 

<span data-ttu-id="89dc2-135">상태를 사용 하는 경우 끝점은 끝점 상태를 조사 하 고 트래픽 라우팅 메서드에 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="89dc2-135">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

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

### <span data-ttu-id="89dc2-136">-GeoMapping</span><span class="sxs-lookup"><span data-stu-id="89dc2-136">-GeoMapping</span></span>
<span data-ttu-id="89dc2-137">' 지역 ' 트래픽 라우팅 방법을 사용할 때이 끝점에 매핑되는 영역의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="89dc2-137">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="89dc2-138">허용 되는 [값의 전체 목록은](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions)Traffic Manager 설명서를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="89dc2-138">Please consult Traffic Manager documentation for a [full list of accepted values](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions).</span></span>
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

### <span data-ttu-id="89dc2-139">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="89dc2-139">-MinChildEndpoints</span></span>
<span data-ttu-id="89dc2-140">Azure 지역 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89dc2-140">Specify an Azure region name.</span></span>
<span data-ttu-id="89dc2-141">Azure 지역 전체 목록은 Azure 지역 https://azure.microsoft.com/regions/ (()을 참조 하세요 https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="89dc2-141">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="89dc2-142">-우선 순위</span><span class="sxs-lookup"><span data-stu-id="89dc2-142">-Priority</span></span>
<span data-ttu-id="89dc2-143">트래픽 관리자가 끝점에 할당 하는 우선 순위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89dc2-143">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="89dc2-144">이 매개 변수는 트래픽 관리자 프로필이 우선 순위의 트래픽 라우팅 메서드를 사용 하 여 구성 된 경우에만 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="89dc2-144">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="89dc2-145">유효한 값은 1부터 1000 까지의 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="89dc2-145">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="89dc2-146">값이 낮을수록 높은 우선 순위를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="89dc2-146">Lower values represent higher priority.</span></span>

<span data-ttu-id="89dc2-147">우선 순위를 지정 하는 경우 프로필의 모든 끝점에 대 한 우선 순위를 지정 해야 하며, 두 종점이 같은 우선 순위 값을 공유할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="89dc2-147">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="89dc2-148">우선 순위를 지정 하지 않으면 트래픽 관리자가 끝점에 기본 우선 순위 값 (1)부터 끝점을 나열 하는 순서 대로 해당 프로필에 대 한 기본값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89dc2-148">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

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

### <span data-ttu-id="89dc2-149">-대상</span><span class="sxs-lookup"><span data-stu-id="89dc2-149">-Target</span></span>
<span data-ttu-id="89dc2-150">끝점의 정규화 된 DNS 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89dc2-150">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="89dc2-151">트래픽 관리자는 트래픽을이 끝점으로 이동할 때 DNS 응답에이 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="89dc2-151">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="89dc2-152">이 매개 변수는 ExternalEndpoints 끝점 형식에만 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89dc2-152">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="89dc2-153">다른 끝점 형식의 경우 대신 *TargetResourceId* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89dc2-153">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

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

### <span data-ttu-id="89dc2-154">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="89dc2-154">-TargetResourceId</span></span>
<span data-ttu-id="89dc2-155">대상의 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89dc2-155">Specifies resource ID of the target.</span></span>
<span data-ttu-id="89dc2-156">AzureEndpoints 및 NestedEndpoints endpoint 형식에 대해서만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89dc2-156">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="89dc2-157">ExternalEndpoints 끝점 형식의 경우 *Target* 매개 변수를 대신 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89dc2-157">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

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

### <span data-ttu-id="89dc2-158">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="89dc2-158">-TrafficManagerProfile</span></span>
<span data-ttu-id="89dc2-159">로컬 **TrafficManagerProfile** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89dc2-159">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="89dc2-160">이 cmdlet은이 로컬 개체를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89dc2-160">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="89dc2-161">**TrafficManagerProfile** 개체를 가져오려면 Get-AzureRmTrafficManagerProfile cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="89dc2-161">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

```yaml
Type: TrafficManagerProfile
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89dc2-162">-Type</span><span class="sxs-lookup"><span data-stu-id="89dc2-162">-Type</span></span>
<span data-ttu-id="89dc2-163">이 cmdlet이 Azure Traffic Manager 프로필에 추가 하는 끝점 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89dc2-163">Specifies the type of endpoint that this cmdlet adds to the Azure Traffic Manager profile.</span></span>
<span data-ttu-id="89dc2-164">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="89dc2-164">Valid values are:</span></span> 

- <span data-ttu-id="89dc2-165">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="89dc2-165">AzureEndpoints</span></span>
- <span data-ttu-id="89dc2-166">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="89dc2-166">ExternalEndpoints</span></span>
- <span data-ttu-id="89dc2-167">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="89dc2-167">NestedEndpoints</span></span>

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

### <span data-ttu-id="89dc2-168">-중량</span><span class="sxs-lookup"><span data-stu-id="89dc2-168">-Weight</span></span>
<span data-ttu-id="89dc2-169">트래픽 관리자가 끝점에 할당 하는 가중치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89dc2-169">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="89dc2-170">유효한 값은 1부터 1000 까지의 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="89dc2-170">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="89dc2-171">기본값은 1입니다.</span><span class="sxs-lookup"><span data-stu-id="89dc2-171">The default value is one (1).</span></span>
<span data-ttu-id="89dc2-172">이 매개 변수는 트래픽 관리자 프로필이 가중치가 있는 트래픽 라우팅 방법으로 구성 된 경우에만 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="89dc2-172">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

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

### <span data-ttu-id="89dc2-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89dc2-173">CommonParameters</span></span>
<span data-ttu-id="89dc2-174">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="89dc2-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89dc2-175">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89dc2-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89dc2-176">입력</span><span class="sxs-lookup"><span data-stu-id="89dc2-176">INPUTS</span></span>

### <span data-ttu-id="89dc2-177">TrafficManagerProfile (Network.)</span><span class="sxs-lookup"><span data-stu-id="89dc2-177">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="89dc2-178">이 cmdlet은이 cmdlet에 대 한 **TrafficManagerProfile** 개체를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="89dc2-178">This cmdlet accepts a **TrafficManagerProfile** object to this cmdlet.</span></span>

## <span data-ttu-id="89dc2-179">출력</span><span class="sxs-lookup"><span data-stu-id="89dc2-179">OUTPUTS</span></span>

### <span data-ttu-id="89dc2-180">TrafficManagerProfile (Network.)</span><span class="sxs-lookup"><span data-stu-id="89dc2-180">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="89dc2-181">이 cmdlet은 수정 된 **TrafficManagerProfile** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="89dc2-181">This cmdlet returns a modified **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="89dc2-182">상속자</span><span class="sxs-lookup"><span data-stu-id="89dc2-182">NOTES</span></span>

## <span data-ttu-id="89dc2-183">관련 링크</span><span class="sxs-lookup"><span data-stu-id="89dc2-183">RELATED LINKS</span></span>

[<span data-ttu-id="89dc2-184">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="89dc2-184">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="89dc2-185">새로운 AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="89dc2-185">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="89dc2-186">제거-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="89dc2-186">Remove-AzureRmTrafficManagerEndpointConfig</span></span>](./Remove-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="89dc2-187">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="89dc2-187">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


