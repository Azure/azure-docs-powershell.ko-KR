---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: FAEA7859-7E58-4343-AD57-7EFC0D87432E
online version: ''
schema: 2.0.0
ms.openlocfilehash: d2886faacd3e9f7d02a008a056dc2145844f8b30
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045434"
---
# <span data-ttu-id="91cd8-101">Set-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="91cd8-101">Set-AzureTrafficManagerEndpoint</span></span>

## <span data-ttu-id="91cd8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="91cd8-102">SYNOPSIS</span></span>
<span data-ttu-id="91cd8-103">Traffic Manager 프로필에서 끝점의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="91cd8-103">Updates the properties of an endpoint in a Traffic Manager profile.</span></span>

## <span data-ttu-id="91cd8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="91cd8-104">SYNTAX</span></span>

```
Set-AzureTrafficManagerEndpoint -DomainName <String> [-Location <String>] [-Type <String>] [-Status <String>]
 [-Weight <Int32>] [-MinChildEndpoints <Int32>] -TrafficManagerProfile <IProfileWithDefinition>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="91cd8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="91cd8-105">DESCRIPTION</span></span>
<span data-ttu-id="91cd8-106">**AzureTrafficManagerEndpoint** Cmdlet은 Microsoft Azure Traffic Manager 프로필의 끝점 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="91cd8-106">The **Set-AzureTrafficManagerEndpoint** cmdlet updates the properties of an endpoint in a Microsoft Azure Traffic Manager profile.</span></span>
<span data-ttu-id="91cd8-107">끝점이 현재 프로필에 없으면이 cmdlet이 끝점을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="91cd8-107">If the endpoint does not exist in the current profile, this cmdlet creates it.</span></span>
<span data-ttu-id="91cd8-108">끝점을 추가한 후 파이프라인 연산자를 사용 하 여 결과를 **Set-AzureTrafficManagerProfile** cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="91cd8-108">After you add an endpoint, pass the result to the **Set-AzureTrafficManagerProfile** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="91cd8-109">해당 cmdlet이 Azure에 연결 하 여 변경 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="91cd8-109">That cmdlet connects to Azure to save your changes.</span></span>

## <span data-ttu-id="91cd8-110">예제의</span><span class="sxs-lookup"><span data-stu-id="91cd8-110">EXAMPLES</span></span>

### <span data-ttu-id="91cd8-111">예제 1: 프로필의 끝점 업데이트</span><span class="sxs-lookup"><span data-stu-id="91cd8-111">Example 1: Update an endpoint for a profile</span></span>
```
PS C:\>$TrafficManagerProfile = Get-AzureTrafficManagerProfile -Name "ContosoProfile"
PS C:\> Set-AzureTrafficManagerEndpoint -TrafficManagerProfile $TrafficManagerProfile -DomainName "ContosoApp02.cloudapp.net" -Status "Enabled" -Type "CloudService" -Weight 2 -Location myLocation | Set-AzureTrafficManagerProfile
```

<span data-ttu-id="91cd8-112">첫 번째 명령은 **AzureTrafficManagerProfile** cmdlet을 사용 하 여 ContosoProfile 이라는 프로필을 가져오고이를 $TrafficManagerProfile 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="91cd8-112">The first command uses the **Get-AzureTrafficManagerProfile** cmdlet to get the profile named ContosoProfile, and then stores it in the $TrafficManagerProfile variable.</span></span>

<span data-ttu-id="91cd8-113">두 번째 명령은 $TrafficManagerProfile에 저장 된 Traffic Manager 프로필의 끝점을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="91cd8-113">The second command updates the endpoint in the Traffic Manager profile that is stored in $TrafficManagerProfile.</span></span>
<span data-ttu-id="91cd8-114">끝점에는 도메인 이름 ContosoApp02.cloudapp.net 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91cd8-114">The endpoint has the domain name ContosoApp02.cloudapp.net.</span></span>
<span data-ttu-id="91cd8-115">또한이 명령은 끝점의 상태, 형식, 두께 및 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="91cd8-115">The command also specifies the status, type, weight, and location of the endpoint.</span></span>
<span data-ttu-id="91cd8-116">이 명령은 수정 된 프로필을 **Set-AzureTrafficManagerProfile** cmdlet에 전달 하 여 Azure에 연결 하 여 변경 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="91cd8-116">The command passes the modified profile to the **Set-AzureTrafficManagerProfile** cmdlet to connect to Azure to save your changes.</span></span>

## <span data-ttu-id="91cd8-117">변수</span><span class="sxs-lookup"><span data-stu-id="91cd8-117">PARAMETERS</span></span>

### <span data-ttu-id="91cd8-118">-DomainName</span><span class="sxs-lookup"><span data-stu-id="91cd8-118">-DomainName</span></span>
<span data-ttu-id="91cd8-119">수정할 끝점의 도메인 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="91cd8-119">Specifies the domain name of the endpoint to modify.</span></span>

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

### <span data-ttu-id="91cd8-120">-위치</span><span class="sxs-lookup"><span data-stu-id="91cd8-120">-Location</span></span>
<span data-ttu-id="91cd8-121">Cmdlet이 추가 하는 끝점의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="91cd8-121">Specifies the location of the endpoint the cmdlet adds.</span></span>
<span data-ttu-id="91cd8-122">Azure 위치 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="91cd8-122">This must be an Azure location.</span></span>

<span data-ttu-id="91cd8-123">이 매개 변수는 부하 분산 메서드가 "성능"으로 설정 된 프로필에서 "모든" 또는 "TrafficManager" 형식의 끝점에 대 한 값을 포함 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="91cd8-123">This parameter must contain a value for endpoints of the type "Any" or of type "TrafficManager" in a profile that has the load balancing method set to "Performance".</span></span>
<span data-ttu-id="91cd8-124">사용할 수 있는 값은 Azure 지역 이름에 나열 되어  https://azure.microsoft.com/regions/https://azure.microsoft.com/regions/ 있습니다.</span><span class="sxs-lookup"><span data-stu-id="91cd8-124">The possible values are the Azure region names, as listed at  https://azure.microsoft.com/regions/https://azure.microsoft.com/regions/.</span></span>

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

### <span data-ttu-id="91cd8-125">-MinChildEndpoints</span><span class="sxs-lookup"><span data-stu-id="91cd8-125">-MinChildEndpoints</span></span>
<span data-ttu-id="91cd8-126">이 끝점을 온라인으로 간주 하기 위해 중첩 된 프로필이 온라인 상태 여야 하는 최소 끝점 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="91cd8-126">Specifies the minimum number of endpoints the nested profile must have online for this endpoint to be considered online.</span></span>

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

### <span data-ttu-id="91cd8-127">-프로필</span><span class="sxs-lookup"><span data-stu-id="91cd8-127">-Profile</span></span>
<span data-ttu-id="91cd8-128">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="91cd8-128">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="91cd8-129">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="91cd8-129">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="91cd8-130">-상태</span><span class="sxs-lookup"><span data-stu-id="91cd8-130">-Status</span></span>
<span data-ttu-id="91cd8-131">모니터링 끝점의 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="91cd8-131">Specifies the status of the monitoring endpoint.</span></span>
<span data-ttu-id="91cd8-132">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="91cd8-132">Valid values are:</span></span> 

- <span data-ttu-id="91cd8-133">수</span><span class="sxs-lookup"><span data-stu-id="91cd8-133">Enabled</span></span>
- <span data-ttu-id="91cd8-134">비활성화</span><span class="sxs-lookup"><span data-stu-id="91cd8-134">Disabled</span></span>

<span data-ttu-id="91cd8-135">사용 값을 지정 하면 트래픽 관리자가 끝점을 모니터링 하 고 부하 분산 메서드는 트래픽을 관리할 때이를 고려 합니다.</span><span class="sxs-lookup"><span data-stu-id="91cd8-135">If you specify a value of Enabled, Traffic Manager monitors the endpoint and the load-balancing method considers it when managing traffic.</span></span>

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

### <span data-ttu-id="91cd8-136">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="91cd8-136">-TrafficManagerProfile</span></span>
<span data-ttu-id="91cd8-137">끝점을 수정할 Traffic Manager 프로필 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="91cd8-137">Specifies the Traffic Manager profile object for which to modify the endpoint.</span></span>

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

### <span data-ttu-id="91cd8-138">-Type</span><span class="sxs-lookup"><span data-stu-id="91cd8-138">-Type</span></span>
<span data-ttu-id="91cd8-139">끝점 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="91cd8-139">Specifies the type of endpoint.</span></span>
<span data-ttu-id="91cd8-140">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="91cd8-140">Valid values are:</span></span> 

- <span data-ttu-id="91cd8-141">CloudService</span><span class="sxs-lookup"><span data-stu-id="91cd8-141">CloudService</span></span>
- <span data-ttu-id="91cd8-142">AzureWebsite</span><span class="sxs-lookup"><span data-stu-id="91cd8-142">AzureWebsite</span></span>
- <span data-ttu-id="91cd8-143">TrafficManager</span><span class="sxs-lookup"><span data-stu-id="91cd8-143">TrafficManager</span></span>

- <span data-ttu-id="91cd8-144">이상</span><span class="sxs-lookup"><span data-stu-id="91cd8-144">Any</span></span> 

<span data-ttu-id="91cd8-145">둘 이상의 AzureWebsite 끝점을 사용할 경우 끝점은 서로 다른 데이터 센터에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="91cd8-145">If there is more than one AzureWebsite endpoint, the endpoints must be in different datacenters.</span></span>

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

### <span data-ttu-id="91cd8-146">-중량</span><span class="sxs-lookup"><span data-stu-id="91cd8-146">-Weight</span></span>
<span data-ttu-id="91cd8-147">Cmdlet이 추가 하는 끝점의 두께를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="91cd8-147">Specifies the weight of the endpoint the cmdlet adds.</span></span>
<span data-ttu-id="91cd8-148">이 매개 변수의 유효한 값 범위는 \[ 1, 1000 \] 입니다.</span><span class="sxs-lookup"><span data-stu-id="91cd8-148">The valid value range for this parameter is \[1,1000\].</span></span>

<span data-ttu-id="91cd8-149">이 매개 변수는 RoundRobin 부하 분산 정책에만 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="91cd8-149">This parameter is only used for RoundRobin load balancing policies.</span></span>

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

### <span data-ttu-id="91cd8-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91cd8-150">CommonParameters</span></span>
<span data-ttu-id="91cd8-151">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="91cd8-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91cd8-152">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91cd8-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91cd8-153">입력</span><span class="sxs-lookup"><span data-stu-id="91cd8-153">INPUTS</span></span>

## <span data-ttu-id="91cd8-154">출력</span><span class="sxs-lookup"><span data-stu-id="91cd8-154">OUTPUTS</span></span>

### <span data-ttu-id="91cd8-155">WindowsAzure. TrafficManager. 유틸리티. IProfileWithDefinition</span><span class="sxs-lookup"><span data-stu-id="91cd8-155">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="91cd8-156">이 cmdlet은 업데이트 된 프로필에 대 한 정보를 포함 하는 Traffic Manager 프로필 개체를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="91cd8-156">This cmdlet generates a Traffic Manager profile object, which contains information about the updated profile.</span></span>

## <span data-ttu-id="91cd8-157">상속자</span><span class="sxs-lookup"><span data-stu-id="91cd8-157">NOTES</span></span>

## <span data-ttu-id="91cd8-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="91cd8-158">RELATED LINKS</span></span>

[<span data-ttu-id="91cd8-159">추가-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="91cd8-159">Add-AzureTrafficManagerEndpoint</span></span>](./Add-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="91cd8-160">제거-AzureTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="91cd8-160">Remove-AzureTrafficManagerEndpoint</span></span>](./Remove-AzureTrafficManagerEndpoint.md)

[<span data-ttu-id="91cd8-161">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="91cd8-161">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="91cd8-162">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="91cd8-162">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


