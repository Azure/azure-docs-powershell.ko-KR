---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerEndpointConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerEndpointConfig.md
ms.openlocfilehash: f2abe6acd0406f78ba2bb691b562cd0bcbffeb35
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525476"
---
# <span data-ttu-id="bb441-101">Add-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="bb441-101">Add-AzureRmTrafficManagerEndpointConfig</span></span>

## <span data-ttu-id="bb441-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb441-102">SYNOPSIS</span></span>
<span data-ttu-id="bb441-103">로컬 트래픽 관리자 프로필 개체에 끝점을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb441-103">Adds an endpoint to a local Traffic Manager profile object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bb441-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bb441-104">SYNTAX</span></span>

```
Add-AzureRmTrafficManagerEndpointConfig -EndpointName <String> -TrafficManagerProfile <TrafficManagerProfile>
 -Type <String> [-TargetResourceId <String>] [-Target <String>] -EndpointStatus <String> [-Weight <UInt32>]
 [-Priority <UInt32>] [-EndpointLocation <String>] [-MinChildEndpoints <UInt32>]
 [-GeoMapping <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bb441-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bb441-105">DESCRIPTION</span></span>
<span data-ttu-id="bb441-106">**Add-AzureRmTrafficManagerEndpointConfig** cmdlet은 로컬 Azure Traffic Manager 프로필 개체에 끝점을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb441-106">The **Add-AzureRmTrafficManagerEndpointConfig** cmdlet adds an endpoint to a local Azure Traffic Manager profile object.</span></span>
<span data-ttu-id="bb441-107">New-AzureRmTrafficManagerProfile 또는 Get-AzureRmTrafficManagerProfile cmdlet을 사용 하 여 프로필을 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bb441-107">You can get a profile by using the New-AzureRmTrafficManagerProfile or Get-AzureRmTrafficManagerProfile cmdlets.</span></span>

<span data-ttu-id="bb441-108">이 cmdlet은 로컬 프로필 개체에서 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb441-108">This cmdlet operates on the local profile object.</span></span>
<span data-ttu-id="bb441-109">Set-AzureRmTrafficManagerProfile cmdlet을 사용 하 여 트래픽 관리자의 프로필에 대 한 변경 내용을 커밋합니다.</span><span class="sxs-lookup"><span data-stu-id="bb441-109">Commit your changes to the profile for Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="bb441-110">끝점을 만들고 단일 작업으로 변경 내용을 커밋하려면 New-AzureRmTrafficManagerEndpoint cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb441-110">To create an endpoint and commit the change in a single operation, use the New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="bb441-111">예제의</span><span class="sxs-lookup"><span data-stu-id="bb441-111">EXAMPLES</span></span>

### <span data-ttu-id="bb441-112">예제 1: 프로필에 끝점 추가</span><span class="sxs-lookup"><span data-stu-id="bb441-112">Example 1: Add an endpoint to a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11"
PS C:\> Add-AzureRmTrafficManagerEndpointConfig -EndpointName "contoso" -EndpointStatus Enabled -Target "www.contoso.com" -TrafficManagerProfile $TrafficManagerProfile -Type ExternalEndpoints -EndpointLocation "North Europe" -Priority 1 -Weight 10
PS C:\> Set-AzureRmTrafficManagerProfile -TrafficManagerProfile $TrafficManagerProfile
```

<span data-ttu-id="bb441-113">첫 번째 명령은 **AzureRmTrafficManagerProfile** cmdlet을 사용 하 여 Azure Traffic Manager 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bb441-113">The first command gets an Azure Traffic Manager profile by using the **Get-AzureRmTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="bb441-114">명령은 로컬 프로필을 $TrafficManagerProfile 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb441-114">The command stores the local profile in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="bb441-115">두 번째 명령은 contoso 이라는 이름의 끝점을 $TrafficManagerProfile에 저장 된 프로필에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb441-115">The second command adds an endpoint named contoso to the profile stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="bb441-116">명령에 끝점에 대 한 구성 데이터가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bb441-116">The command includes configuration data for the endpoint.</span></span>
<span data-ttu-id="bb441-117">이 명령은 로컬 개체만 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb441-117">This command changes only the local object.</span></span>

<span data-ttu-id="bb441-118">마지막 명령은 $TrafficManagerProfile의 로컬 값과 일치 하도록 Azure의 Traffic Manager 프로필을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb441-118">The final command updates the Traffic Manager profile in Azure to match the local value in $TrafficManagerProfile.</span></span>

## <span data-ttu-id="bb441-119">변수</span><span class="sxs-lookup"><span data-stu-id="bb441-119">PARAMETERS</span></span>

### <span data-ttu-id="bb441-120">-EndpointLocation</span><span class="sxs-lookup"><span data-stu-id="bb441-120">-EndpointLocation</span></span>
<span data-ttu-id="bb441-121">성능 트래픽 라우팅 메서드에 사용할 끝점의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb441-121">Specifies the location of the endpoint to use in the Performance traffic-routing method.</span></span>
<span data-ttu-id="bb441-122">이 매개 변수는 ExternalEndpoints 또는 NestedEndpoints 형식의 끝점에만 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bb441-122">This parameter is only applicable to endpoints of the ExternalEndpoints or the NestedEndpoints type.</span></span>
<span data-ttu-id="bb441-123">성능 트래픽 라우팅 메서드를 사용 하는 경우이 매개 변수를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb441-123">You must specify this parameter when the Performance traffic-routing method is used.</span></span>

<span data-ttu-id="bb441-124">Azure 지역 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb441-124">Specify an Azure region name.</span></span>
<span data-ttu-id="bb441-125">Azure 지역 전체 목록은 Azure 지역 https://azure.microsoft.com/regions/ (()을 참조 하세요 https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="bb441-125">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="bb441-126">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="bb441-126">-EndpointName</span></span>
<span data-ttu-id="bb441-127">이 cmdlet이 추가 하는 Traffic Manager 끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb441-127">Specifies the name of the Traffic Manager endpoint that this cmdlet adds.</span></span>

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

### <span data-ttu-id="bb441-128">-EndpointStatus</span><span class="sxs-lookup"><span data-stu-id="bb441-128">-EndpointStatus</span></span>
<span data-ttu-id="bb441-129">끝점의 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb441-129">Specifies the status of the endpoint.</span></span>
<span data-ttu-id="bb441-130">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="bb441-130">Valid values are:</span></span> 

- <span data-ttu-id="bb441-131">수</span><span class="sxs-lookup"><span data-stu-id="bb441-131">Enabled</span></span> 
- <span data-ttu-id="bb441-132">비활성화</span><span class="sxs-lookup"><span data-stu-id="bb441-132">Disabled</span></span> 

<span data-ttu-id="bb441-133">상태를 사용 하는 경우 끝점은 끝점 상태를 조사 하 고 트래픽 라우팅 메서드에 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bb441-133">If the status is Enabled, the endpoint is probed for endpoint health and is included in the traffic-routing method.</span></span>

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

### <span data-ttu-id="bb441-134">-GeoMapping</span><span class="sxs-lookup"><span data-stu-id="bb441-134">-GeoMapping</span></span>
<span data-ttu-id="bb441-135">' 지역 ' 트래픽 라우팅 방법을 사용할 때이 끝점에 매핑되는 영역의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="bb441-135">The list of regions mapped to this endpoint when using the 'Geographic' traffic routing method.</span></span> <span data-ttu-id="bb441-136">허용 되는 [값의 전체 목록은](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions)Traffic Manager 설명서를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="bb441-136">Please consult Traffic Manager documentation for a [full list of accepted values](https://docs.microsoft.com/en-us/azure/traffic-manager/traffic-manager-geographic-regions).</span></span>
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

### <span data-ttu-id="bb441-137">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="bb441-137">-MinChildEndpoints</span></span>
<span data-ttu-id="bb441-138">Azure 지역 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb441-138">Specify an Azure region name.</span></span>
<span data-ttu-id="bb441-139">Azure 지역 전체 목록은 Azure 지역 https://azure.microsoft.com/regions/ (()을 참조 하세요 https://azure.microsoft.com/regions/) .</span><span class="sxs-lookup"><span data-stu-id="bb441-139">For a full list of Azure regions, see Azure Regionshttps://azure.microsoft.com/regions/ (https://azure.microsoft.com/regions/).</span></span>

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

### <span data-ttu-id="bb441-140">-우선 순위</span><span class="sxs-lookup"><span data-stu-id="bb441-140">-Priority</span></span>
<span data-ttu-id="bb441-141">트래픽 관리자가 끝점에 할당 하는 우선 순위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb441-141">Specifies the priority that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="bb441-142">이 매개 변수는 트래픽 관리자 프로필이 우선 순위의 트래픽 라우팅 메서드를 사용 하 여 구성 된 경우에만 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bb441-142">This parameter is used only if the Traffic Manager profile is configured with the for Priority traffic-routing method.</span></span>
<span data-ttu-id="bb441-143">유효한 값은 1부터 1000 까지의 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="bb441-143">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="bb441-144">값이 낮을수록 높은 우선 순위를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="bb441-144">Lower values represent higher priority.</span></span>

<span data-ttu-id="bb441-145">우선 순위를 지정 하는 경우 프로필의 모든 끝점에 대 한 우선 순위를 지정 해야 하며, 두 종점이 같은 우선 순위 값을 공유할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="bb441-145">If you specify a priority, you must specify priorities on all endpoints in the profile, and no two endpoints can share the same priority value.</span></span>
<span data-ttu-id="bb441-146">우선 순위를 지정 하지 않으면 트래픽 관리자가 끝점에 기본 우선 순위 값 (1)부터 끝점을 나열 하는 순서 대로 해당 프로필에 대 한 기본값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb441-146">If you do not specify priorities, Traffic Manager assigns default priority values to the endpoints, starting with one (1), in the order the profile lists the endpoints.</span></span>

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

### <span data-ttu-id="bb441-147">-대상</span><span class="sxs-lookup"><span data-stu-id="bb441-147">-Target</span></span>
<span data-ttu-id="bb441-148">끝점의 정규화 된 DNS 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb441-148">Specifies the fully qualified DNS name of the endpoint.</span></span>
<span data-ttu-id="bb441-149">트래픽 관리자는 트래픽을이 끝점으로 이동할 때 DNS 응답에이 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb441-149">Traffic Manager returns this value in DNS responses when it directs traffic to this endpoint.</span></span>
<span data-ttu-id="bb441-150">이 매개 변수는 ExternalEndpoints 끝점 형식에만 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb441-150">Specify this parameter only for the ExternalEndpoints endpoint type.</span></span>
<span data-ttu-id="bb441-151">다른 끝점 형식의 경우 대신 *TargetResourceId* 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb441-151">For other endpoint types, specify the *TargetResourceId* parameter instead.</span></span>

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

### <span data-ttu-id="bb441-152">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="bb441-152">-TargetResourceId</span></span>
<span data-ttu-id="bb441-153">대상의 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb441-153">Specifies resource ID of the target.</span></span>
<span data-ttu-id="bb441-154">AzureEndpoints 및 NestedEndpoints endpoint 형식에 대해서만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb441-154">Specify this parameter only for the AzureEndpoints and NestedEndpoints endpoint types.</span></span>
<span data-ttu-id="bb441-155">ExternalEndpoints 끝점 형식의 경우 *Target* 매개 변수를 대신 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb441-155">For the ExternalEndpoints endpoint type, specify the *Target* parameter instead.</span></span>

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

### <span data-ttu-id="bb441-156">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bb441-156">-TrafficManagerProfile</span></span>
<span data-ttu-id="bb441-157">로컬 **TrafficManagerProfile** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb441-157">Specifies a local **TrafficManagerProfile** object.</span></span>
<span data-ttu-id="bb441-158">이 cmdlet은이 로컬 개체를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb441-158">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="bb441-159">**TrafficManagerProfile** 개체를 가져오려면 Get-AzureRmTrafficManagerProfile cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb441-159">To obtain a **TrafficManagerProfile** object, use the Get-AzureRmTrafficManagerProfile cmdlet.</span></span>

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

### <span data-ttu-id="bb441-160">-Type</span><span class="sxs-lookup"><span data-stu-id="bb441-160">-Type</span></span>
<span data-ttu-id="bb441-161">이 cmdlet이 Azure Traffic Manager 프로필에 추가 하는 끝점 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb441-161">Specifies the type of endpoint that this cmdlet adds to the Azure Traffic Manager profile.</span></span>
<span data-ttu-id="bb441-162">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="bb441-162">Valid values are:</span></span> 

- <span data-ttu-id="bb441-163">AzureEndpoints</span><span class="sxs-lookup"><span data-stu-id="bb441-163">AzureEndpoints</span></span>
- <span data-ttu-id="bb441-164">ExternalEndpoints</span><span class="sxs-lookup"><span data-stu-id="bb441-164">ExternalEndpoints</span></span>
- <span data-ttu-id="bb441-165">NestedEndpoints</span><span class="sxs-lookup"><span data-stu-id="bb441-165">NestedEndpoints</span></span>

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

### <span data-ttu-id="bb441-166">-중량</span><span class="sxs-lookup"><span data-stu-id="bb441-166">-Weight</span></span>
<span data-ttu-id="bb441-167">트래픽 관리자가 끝점에 할당 하는 가중치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb441-167">Specifies the weight that Traffic Manager assigns to the endpoint.</span></span>
<span data-ttu-id="bb441-168">유효한 값은 1부터 1000 까지의 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="bb441-168">Valid values are integers from 1 through 1000.</span></span>
<span data-ttu-id="bb441-169">기본값은 1입니다.</span><span class="sxs-lookup"><span data-stu-id="bb441-169">The default value is one (1).</span></span>
<span data-ttu-id="bb441-170">이 매개 변수는 트래픽 관리자 프로필이 가중치가 있는 트래픽 라우팅 방법으로 구성 된 경우에만 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bb441-170">This parameter is used only if the Traffic Manager profile is configured with the Weighted traffic-routing method.</span></span>

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

### <span data-ttu-id="bb441-171">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb441-171">-DefaultProfile</span></span>
<span data-ttu-id="bb441-172">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bb441-172">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb441-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb441-173">CommonParameters</span></span>
<span data-ttu-id="bb441-174">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb441-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb441-175">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb441-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb441-176">입력</span><span class="sxs-lookup"><span data-stu-id="bb441-176">INPUTS</span></span>

### <span data-ttu-id="bb441-177">TrafficManagerProfile (Network.)</span><span class="sxs-lookup"><span data-stu-id="bb441-177">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="bb441-178">이 cmdlet은이 cmdlet에 대 한 **TrafficManagerProfile** 개체를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb441-178">This cmdlet accepts a **TrafficManagerProfile** object to this cmdlet.</span></span>

## <span data-ttu-id="bb441-179">출력</span><span class="sxs-lookup"><span data-stu-id="bb441-179">OUTPUTS</span></span>

### <span data-ttu-id="bb441-180">TrafficManagerProfile (Network.)</span><span class="sxs-lookup"><span data-stu-id="bb441-180">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="bb441-181">이 cmdlet은 수정 된 **TrafficManagerProfile** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="bb441-181">This cmdlet returns a modified **TrafficManagerProfile** object.</span></span>

## <span data-ttu-id="bb441-182">상속자</span><span class="sxs-lookup"><span data-stu-id="bb441-182">NOTES</span></span>

## <span data-ttu-id="bb441-183">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bb441-183">RELATED LINKS</span></span>

[<span data-ttu-id="bb441-184">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bb441-184">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="bb441-185">새로운 AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="bb441-185">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="bb441-186">제거-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="bb441-186">Remove-AzureRmTrafficManagerEndpointConfig</span></span>](./Remove-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="bb441-187">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="bb441-187">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


