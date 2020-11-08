---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: CF1FC482-812D-4BAD-BA3A-D88E614A5165
online version: ''
schema: 2.0.0
ms.openlocfilehash: 79f212e83ece1def42c6d8de343a42e087f5181a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046376"
---
# <span data-ttu-id="b85e1-101">Add-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b85e1-101">Add-AzureTrafficManagerEndpoint</span></span>

## <span data-ttu-id="b85e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b85e1-102">SYNOPSIS</span></span>
<span data-ttu-id="b85e1-103">Traffic Manager 프로필에 끝점을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b85e1-103">Adds an endpoint to a Traffic Manager profile.</span></span>

## <span data-ttu-id="b85e1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b85e1-104">SYNTAX</span></span>

```
Add-AzureTrafficManagerEndpoint -DomainName <String> [-Location <String>] -Type <String> -Status <String>
 [-Weight <Int32>] [-MinChildEndpoints <Int32>] -TrafficManagerProfile <IProfileWithDefinition>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b85e1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b85e1-105">DESCRIPTION</span></span>
<span data-ttu-id="b85e1-106">**Add-AzureTrafficManagerEndpoint** Cmdlet은 Microsoft Azure Traffic Manager 프로필에 끝점을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b85e1-106">The **Add-AzureTrafficManagerEndpoint** cmdlet adds an endpoint to a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="b85e1-107">끝점을 추가한 후 파이프라인 연산자를 사용 하 여 결과를 **Set-AzureTrafficManagerProfile** cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="b85e1-107">After you add an endpoint, pass the result to the **Set-AzureTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="b85e1-108">해당 cmdlet이 Azure에 연결 하 여 변경 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b85e1-108">That cmdlet connects to Azure to save your changes.</span></span>

## <span data-ttu-id="b85e1-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b85e1-109">EXAMPLES</span></span>

### <span data-ttu-id="b85e1-110">예제 1: 프로필에 끝점 추가</span><span class="sxs-lookup"><span data-stu-id="b85e1-110">Example 1: Add an endpoint to a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureTrafficManagerProfile -Name "ContosoProfile"
PS C:\> Add-AzureTrafficManagerEndpoint -TrafficManagerProfile $TrafficManagerProfile -DomainName "Contoso02App.cloudapp.net" -Status "Enabled" -Type "CloudService" | Set-AzureTrafficManagerProfile
```

<span data-ttu-id="b85e1-111">첫 번째 명령은 **AzureTrafficManagerProfile** cmdlet을 사용 하 여 ContosoProfile 이라는 프로필을 가져오고이를 $TrafficManagerProfile 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b85e1-111">The first command uses the **Get-AzureTrafficManagerProfile** cmdlet to get the profile named ContosoProfile, and then stores it in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="b85e1-112">두 번째 명령은 $TrafficManagerProfile에 저장 된 Traffic Manager 프로필에 끝점을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b85e1-112">The second command adds an endpoint to Traffic Manager profile that is stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="b85e1-113">끝점에는 도메인 이름 Contoso02App.couldapp.net 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b85e1-113">The endpoint has the domain name Contoso02App.couldapp.net.</span></span>
<span data-ttu-id="b85e1-114">또한 명령을 사용 하는지 여부와 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b85e1-114">The command also specifies whether it is enabled and its type.</span></span>
<span data-ttu-id="b85e1-115">이 명령은 프로필 개체를 **Set-AzureTrafficManagerProfile** cmdlet에 전달 하 여 Azure에 연결 하 여 변경 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b85e1-115">The command passes the profile object to the **Set-AzureTrafficManagerProfile** cmdlet to connect to Azure to save your changes.</span></span>

### <span data-ttu-id="b85e1-116">예제 2: 지정 된 위치 및 두께가 있는 끝점 추가</span><span class="sxs-lookup"><span data-stu-id="b85e1-116">Example 2: Add an endpoint that has a specified location and weight</span></span>
```
PS C:\>Add-AzureTrafficManagerEndpoint -TrafficManagerProfile ContosoTrafficManagerProfile -DomainName " Contoso02App.cloudapp.net" -Status Enabled -Type CloudService -Weight 2 -Location myLocation | Set-AzureTrafficManagerProfile
```

<span data-ttu-id="b85e1-117">이 명령은 Traffic Manager 프로필에 끝점을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="b85e1-117">This command adds an endpoint to a Traffic Manager profile.</span></span>
<span data-ttu-id="b85e1-118">끝점에는 도메인 이름 Contoso02App.couldapp.net 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b85e1-118">The endpoint has the domain name Contoso02App.couldapp.net.</span></span>
<span data-ttu-id="b85e1-119">또한 명령을 사용 하는지 여부와 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b85e1-119">The command also specifies whether it is enabled and its type.</span></span>
<span data-ttu-id="b85e1-120">또한이 명령은 끝점의 두께 및 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b85e1-120">The command also specifies the weight and location for the endpoint.</span></span>
<span data-ttu-id="b85e1-121">이 명령은 프로필 개체를 전달 하 여 AzureTrafficManagerProfile에서 Azure에 연결 하 여 변경 내용을 저장 하도록 **설정** 합니다.</span><span class="sxs-lookup"><span data-stu-id="b85e1-121">The command passes the profile object to **Set-AzureTrafficManagerProfile** to connect to Azure to save your changes.</span></span>

## <span data-ttu-id="b85e1-122">변수</span><span class="sxs-lookup"><span data-stu-id="b85e1-122">PARAMETERS</span></span>

### <span data-ttu-id="b85e1-123">-DomainName</span><span class="sxs-lookup"><span data-stu-id="b85e1-123">-DomainName</span></span>
<span data-ttu-id="b85e1-124">추가할 끝점의 도메인 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b85e1-124">Specifies the domain name of the endpoint to add.</span></span>

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

### <span data-ttu-id="b85e1-125">-위치</span><span class="sxs-lookup"><span data-stu-id="b85e1-125">-Location</span></span>
<span data-ttu-id="b85e1-126">Cmdlet이 추가 하는 끝점의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b85e1-126">Specifies the location of the endpoint the cmdlet adds.</span></span>
<span data-ttu-id="b85e1-127">Azure 위치 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b85e1-127">This must be an Azure location.</span></span>

<span data-ttu-id="b85e1-128">이 매개 변수는 부하 분산 메서드가 "성능"으로 설정 된 프로필에서 "모든" 또는 "TrafficManager" 형식의 끝점에 대 한 값을 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b85e1-128">This parameter must contain a value for endpoints of the type "Any" or of type "TrafficManager" in a profile that has the load balancing method set to "Performance".</span></span>
<span data-ttu-id="b85e1-129">사용할 수 있는 값은 Azure 지역 이름에 나열 되어 https://azure.microsoft.com/regions/ 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b85e1-129">The possible values are the Azure region names, as listed at https://azure.microsoft.com/regions/.</span></span>

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

### <span data-ttu-id="b85e1-130">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="b85e1-130">-MinChildEndpoints</span></span>
<span data-ttu-id="b85e1-131">이 끝점을 온라인으로 간주 하기 위해 중첩 된 프로필이 온라인 상태 여야 하는 최소 끝점 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b85e1-131">Specifies the minimum number of endpoints the nested profile must have online for this endpoint to be considered online.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b85e1-132">-프로필</span><span class="sxs-lookup"><span data-stu-id="b85e1-132">-Profile</span></span>
<span data-ttu-id="b85e1-133">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b85e1-133">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="b85e1-134">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="b85e1-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b85e1-135">-상태</span><span class="sxs-lookup"><span data-stu-id="b85e1-135">-Status</span></span>
<span data-ttu-id="b85e1-136">모니터링 끝점의 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b85e1-136">Specifies the status of the monitoring endpoint.</span></span>
<span data-ttu-id="b85e1-137">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b85e1-137">Valid values are:</span></span> 

- <span data-ttu-id="b85e1-138">수</span><span class="sxs-lookup"><span data-stu-id="b85e1-138">Enabled</span></span>
- <span data-ttu-id="b85e1-139">비활성화</span><span class="sxs-lookup"><span data-stu-id="b85e1-139">Disabled</span></span>

<span data-ttu-id="b85e1-140">사용 값을 지정 하면 트래픽 관리자가 끝점을 모니터링 하 고 부하 분산 메서드는 트래픽을 관리할 때이를 고려 합니다.</span><span class="sxs-lookup"><span data-stu-id="b85e1-140">If you specify a value of Enabled, Traffic Manager monitors the endpoint and the load-balancing method considers it when managing traffic.</span></span>

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

### <span data-ttu-id="b85e1-141">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b85e1-141">-TrafficManagerProfile</span></span>
<span data-ttu-id="b85e1-142">끝점을 추가할 Traffic Manager 프로필 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b85e1-142">Specifies the Traffic Manager profile object to which to add the endpoint.</span></span>

```yaml
Type: IProfileWithDefinition
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b85e1-143">-Type</span><span class="sxs-lookup"><span data-stu-id="b85e1-143">-Type</span></span>
<span data-ttu-id="b85e1-144">끝점 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b85e1-144">Specifies the type of endpoint.</span></span>
<span data-ttu-id="b85e1-145">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b85e1-145">Valid values are:</span></span> 

- <span data-ttu-id="b85e1-146">CloudService</span><span class="sxs-lookup"><span data-stu-id="b85e1-146">CloudService</span></span>
- <span data-ttu-id="b85e1-147">AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="b85e1-147">AzureWebsite</span></span>
- <span data-ttu-id="b85e1-148">TrafficManager</span><span class="sxs-lookup"><span data-stu-id="b85e1-148">TrafficManager</span></span>

- <span data-ttu-id="b85e1-149">이상</span><span class="sxs-lookup"><span data-stu-id="b85e1-149">Any</span></span> 

<span data-ttu-id="b85e1-150">둘 이상의 AzureWebsite 끝점을 사용할 경우 끝점은 서로 다른 데이터 센터에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b85e1-150">If there is more than one AzureWebsite endpoint, the endpoints must be in different datacenters.</span></span>

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

### <span data-ttu-id="b85e1-151">-중량</span><span class="sxs-lookup"><span data-stu-id="b85e1-151">-Weight</span></span>
<span data-ttu-id="b85e1-152">Cmdlet이 추가 하는 끝점의 두께를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b85e1-152">Specifies the weight of the endpoint the cmdlet adds.</span></span>
<span data-ttu-id="b85e1-153">이 매개 변수의 유효한 값 범위는 \[ 1, 1000 \] 입니다.</span><span class="sxs-lookup"><span data-stu-id="b85e1-153">The valid value range for this parameter is \[1,1000\].</span></span>

<span data-ttu-id="b85e1-154">이 매개 변수는 RoundRobin 부하 분산 정책에만 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b85e1-154">This parameter is only used for RoundRobin load balancing policies.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b85e1-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b85e1-155">CommonParameters</span></span>
<span data-ttu-id="b85e1-156">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b85e1-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b85e1-157">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b85e1-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b85e1-158">입력</span><span class="sxs-lookup"><span data-stu-id="b85e1-158">INPUTS</span></span>

## <span data-ttu-id="b85e1-159">출력</span><span class="sxs-lookup"><span data-stu-id="b85e1-159">OUTPUTS</span></span>

### <span data-ttu-id="b85e1-160">WindowsAzure. TrafficManager. 유틸리티. IProfileWithDefinition</span><span class="sxs-lookup"><span data-stu-id="b85e1-160">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="b85e1-161">이 cmdlet은 업데이트 된 프로필에 대 한 정보를 포함 하는 Traffic Manager 프로필 개체를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b85e1-161">This cmdlet generates a Traffic Manager profile object, which contains information about the updated profile.</span></span>

## <span data-ttu-id="b85e1-162">상속자</span><span class="sxs-lookup"><span data-stu-id="b85e1-162">NOTES</span></span>

## <span data-ttu-id="b85e1-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b85e1-163">RELATED LINKS</span></span>

[<span data-ttu-id="b85e1-164">제거-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b85e1-164">Remove-AzureTrafficManagerEndpoint</span></span>](./Remove-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="b85e1-165">Set-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="b85e1-165">Set-AzureTrafficManagerEndpoint</span></span>](./Set-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="b85e1-166">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b85e1-166">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="b85e1-167">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="b85e1-167">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


