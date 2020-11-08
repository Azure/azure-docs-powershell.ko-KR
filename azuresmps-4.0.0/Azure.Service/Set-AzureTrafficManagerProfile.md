---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 700AC44E-4FD5-4516-80F3-B8C9E4DF6ABC
online version: ''
schema: 2.0.0
ms.openlocfilehash: d37397b4e0ce9f1d9878860eb5e7a431e58a20a9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045794"
---
# <span data-ttu-id="8eaad-101">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8eaad-101">Set-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="8eaad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8eaad-102">SYNOPSIS</span></span>
<span data-ttu-id="8eaad-103">Traffic Manager 프로필의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8eaad-103">Updates the properties of a Traffic Manager profile.</span></span>

## <span data-ttu-id="8eaad-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8eaad-104">SYNTAX</span></span>

```
Set-AzureTrafficManagerProfile [-Name <String>] [-LoadBalancingMethod <String>] [-MonitorPort <Int32>]
 [-MonitorProtocol <String>] [-MonitorRelativePath <String>] [-Ttl <Int32>]
 -TrafficManagerProfile <IProfileWithDefinition> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8eaad-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8eaad-105">DESCRIPTION</span></span>
<span data-ttu-id="8eaad-106">**AzureTrafficManagerProfile** Cmdlet은 Microsoft Azure Traffic Manager 프로필의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8eaad-106">The **Set-AzureTrafficManagerProfile** cmdlet updates the properties of a Microsoft Azure Traffic Manager profile.</span></span>

<span data-ttu-id="8eaad-107">*LoadBalancingMethod* 값을 "장애 조치"로 설정한 프로필의 경우 Add-AzureTrafficManagerEndpoint cmdlet을 사용 하 여 프로필에 추가한 끝점의 장애 조치 순서를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8eaad-107">For profiles for which you have set the *LoadBalancingMethod* value to "Failover", you can determine the failover order of the endpoints you have added to your profile with the Add-AzureTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="8eaad-108">자세한 내용은 아래 예제 3을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8eaad-108">For more information, see Example 3 below.</span></span>

## <span data-ttu-id="8eaad-109">예제의</span><span class="sxs-lookup"><span data-stu-id="8eaad-109">EXAMPLES</span></span>

### <span data-ttu-id="8eaad-110">예제 1: Traffic Manager 프로필의 TTL 설정</span><span class="sxs-lookup"><span data-stu-id="8eaad-110">Example 1: Set the TTL for a Traffic Manager profile</span></span>
```
PS C:\>Set-AzureTrafficManagerProfile -TrafficManagerProfile $MyTrafficManagerProfile -Ttl 60
```

<span data-ttu-id="8eaad-111">이 명령은 Traffic Manager 프로필 개체 MyTrafficManagerProfile에 대 한 TTL을 60 초로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8eaad-111">This command sets the TTL to 60 seconds for the Traffic Manager profile object MyTrafficManagerProfile.</span></span>

### <span data-ttu-id="8eaad-112">예제 2: 프로필에 여러 값 설정</span><span class="sxs-lookup"><span data-stu-id="8eaad-112">Example 2: Set several values for a profile</span></span>
```
PS C:\>Get-AzureTrafficManagerProfile -Name "MyProfile" | Set-AzureTrafficManagerProfile -LoadBalancingMethod "RoundRobin" -Ttl 30 -MonitorProtocol "Http" -MonitorPort 80 -MonitorRelativePath "/"
```

<span data-ttu-id="8eaad-113">이 명령은 **AzureTrafficManagerProfile** cmdlet을 사용 하 여 myprofile 이라는 Traffic Manager 프로필을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8eaad-113">This command gets a Traffic Manager profile named MyProfile by using the **Get-AzureTrafficManagerProfile** cmdlet.</span></span>
<span data-ttu-id="8eaad-114">프로필은 RoundRobin 부하 분산 방법, 30 초의 TTL, 모니터 프로토콜 HTTP, 모니터 포트, Traffic Manager 프로필에 대 한 상대 경로를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8eaad-114">The profile uses the RoundRobin load balancing method, a TTL of 30 seconds,  the monitor protocol HTTP, the monitor port, and the relative path for a Traffic Manager profile.</span></span>

### <span data-ttu-id="8eaad-115">예제 3: 원하는 장애 조치 순서에 따라 끝점 순서 변경</span><span class="sxs-lookup"><span data-stu-id="8eaad-115">Example 3: Reorder endpoints to desired failover order</span></span>
```
PS C:\>$Profile = Get-AzureTrafficManagerProfile -Name "MyProfile"
PS C:\> $Profile.Endpoints[0],$Profile.Endpoints[1] = $Profile.Endpoints[1],$Profile.Endpoints[0]
PS C:\> $Profile = Set-AzureTrafficManagerProfile
```

<span data-ttu-id="8eaad-116">이 예제에서는 MyProfile에 추가한 끝점을 원하는 장애 조치 순서에 따라 순서를 재정리 합니다.</span><span class="sxs-lookup"><span data-stu-id="8eaad-116">This example reorders the endpoints added to MyProfile to the desired failover order.</span></span>

<span data-ttu-id="8eaad-117">첫 번째 명령은 MyProfile 이라는 트래픽 관리자 프로필 개체를 가져와 개체를 $Profile 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8eaad-117">The first command gets the Traffic Manager profile object named MyProfile and stores the object in the $Profile variable.</span></span>

<span data-ttu-id="8eaad-118">두 번째 명령은 끝점 배열의 끝점을 장애 조치 발생 순서에 따라 다시 정렬 합니다.</span><span class="sxs-lookup"><span data-stu-id="8eaad-118">The second command re-orders the endpoints from  the endpoints array to the order in which failover should occur.</span></span>

<span data-ttu-id="8eaad-119">마지막 명령은 새 끝점 순서를 사용 하 여 $Profile에 저장 된 Traffic Manager 프로필을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8eaad-119">The last command updates the Traffic Manager profile stored in $Profile with the new endpoint order.</span></span>

## <span data-ttu-id="8eaad-120">변수</span><span class="sxs-lookup"><span data-stu-id="8eaad-120">PARAMETERS</span></span>

### <span data-ttu-id="8eaad-121">-LoadBalancingMethod</span><span class="sxs-lookup"><span data-stu-id="8eaad-121">-LoadBalancingMethod</span></span>
<span data-ttu-id="8eaad-122">연결을 배포 하는 데 사용할 부하 분산 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8eaad-122">Specifies the load balancing method to use to distribute the connection.</span></span>
<span data-ttu-id="8eaad-123">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="8eaad-123">Valid values are:</span></span> 

- <span data-ttu-id="8eaad-124">성능을</span><span class="sxs-lookup"><span data-stu-id="8eaad-124">Performance</span></span>
- <span data-ttu-id="8eaad-125">장애 조치</span><span class="sxs-lookup"><span data-stu-id="8eaad-125">Failover</span></span>
- <span data-ttu-id="8eaad-126">RoundRobin</span><span class="sxs-lookup"><span data-stu-id="8eaad-126">RoundRobin</span></span>

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

### <span data-ttu-id="8eaad-127">-모니터 포트</span><span class="sxs-lookup"><span data-stu-id="8eaad-127">-MonitorPort</span></span>
<span data-ttu-id="8eaad-128">끝점 상태를 모니터링 하는 데 사용 되는 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8eaad-128">Specifies the port used to monitor endpoint health.</span></span>
<span data-ttu-id="8eaad-129">유효한 값은 0 보다 크고 65535 보다 작거나 같은 정수 값입니다.</span><span class="sxs-lookup"><span data-stu-id="8eaad-129">Valid values are integer values greater than 0 and less than or equal to 65,535.</span></span>

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

### <span data-ttu-id="8eaad-130">-모니터 프로토콜</span><span class="sxs-lookup"><span data-stu-id="8eaad-130">-MonitorProtocol</span></span>
<span data-ttu-id="8eaad-131">끝점 상태를 모니터링 하는 데 사용할 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8eaad-131">Specifies the protocol to use to monitor endpoint health.</span></span>
<span data-ttu-id="8eaad-132">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="8eaad-132">Valid values are:</span></span> 

- <span data-ttu-id="8eaad-133">Http</span><span class="sxs-lookup"><span data-stu-id="8eaad-133">Http</span></span>
- <span data-ttu-id="8eaad-134">Https</span><span class="sxs-lookup"><span data-stu-id="8eaad-134">Https</span></span>

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

### <span data-ttu-id="8eaad-135">-MonitorRelativePath</span><span class="sxs-lookup"><span data-stu-id="8eaad-135">-MonitorRelativePath</span></span>
<span data-ttu-id="8eaad-136">상태를 검색 하기 위해 끝점 도메인 이름에 상대적인 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8eaad-136">Specifies the path relative to the endpoint domain name to probe for health state.</span></span>
<span data-ttu-id="8eaad-137">경로는 다음 제한을 충족 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8eaad-137">The path must meet the following restrictions:</span></span> 

- <span data-ttu-id="8eaad-138">경로는 1 ~ 1000 자 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8eaad-138">The path must be from 1 through 1000 characters.</span></span>
- <span data-ttu-id="8eaad-139">슬래시,/으로 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8eaad-139">It must start with a forward slash, /.</span></span>
- <span data-ttu-id="8eaad-140">XML 요소를 포함 하지 않아야 \<\> 합니다.</span><span class="sxs-lookup"><span data-stu-id="8eaad-140">It must contain no XML elements, \<\>.</span></span>
- <span data-ttu-id="8eaad-141">이중 슬래시,//를 포함 하지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8eaad-141">It must contain no double slashes, //.</span></span>
- <span data-ttu-id="8eaad-142">잘못 된 HTML 이스케이프 문자가 포함 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8eaad-142">It must contain no invalid HTML escape characters.</span></span>
<span data-ttu-id="8eaad-143">예를 들면% XY입니다.</span><span class="sxs-lookup"><span data-stu-id="8eaad-143">For example, %XY.</span></span>

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

### <span data-ttu-id="8eaad-144">-이름</span><span class="sxs-lookup"><span data-stu-id="8eaad-144">-Name</span></span>
<span data-ttu-id="8eaad-145">업데이트할 Traffic Manager 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8eaad-145">Specifies the name of the Traffic Manager profile to update.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8eaad-146">-프로필</span><span class="sxs-lookup"><span data-stu-id="8eaad-146">-Profile</span></span>
<span data-ttu-id="8eaad-147">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8eaad-147">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="8eaad-148">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="8eaad-148">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8eaad-149">-TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8eaad-149">-TrafficManagerProfile</span></span>
<span data-ttu-id="8eaad-150">프로필을 설정 하는 데 사용 하는 Traffic Manager 프로필 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8eaad-150">Specifies the Traffic Manager profile object you use to set the profile.</span></span>

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

### <span data-ttu-id="8eaad-151">-Ttl</span><span class="sxs-lookup"><span data-stu-id="8eaad-151">-Ttl</span></span>
<span data-ttu-id="8eaad-152">DNS 항목을 캐시할 수 있는 시간을 로컬 DNS 확인자에 알리는 DNS TTL (Time to Live)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8eaad-152">Specifies the DNS Time-to-Live (TTL) that informs the Local DNS resolvers how long to cache DNS entries.</span></span>
<span data-ttu-id="8eaad-153">유효한 값은 30부터 999999 까지의 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="8eaad-153">Valid values are an integer from 30 through 999,999.</span></span>

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

### <span data-ttu-id="8eaad-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8eaad-154">CommonParameters</span></span>
<span data-ttu-id="8eaad-155">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8eaad-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8eaad-156">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8eaad-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8eaad-157">입력</span><span class="sxs-lookup"><span data-stu-id="8eaad-157">INPUTS</span></span>

## <span data-ttu-id="8eaad-158">출력</span><span class="sxs-lookup"><span data-stu-id="8eaad-158">OUTPUTS</span></span>

### <span data-ttu-id="8eaad-159">WindowsAzure. TrafficManager. 유틸리티. IProfileWithDefinition</span><span class="sxs-lookup"><span data-stu-id="8eaad-159">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="8eaad-160">이 cmdlet은 Traffic Manager 프로필 개체를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="8eaad-160">This cmdlet generates a Traffic Manager profile object.</span></span>

## <span data-ttu-id="8eaad-161">상속자</span><span class="sxs-lookup"><span data-stu-id="8eaad-161">NOTES</span></span>

## <span data-ttu-id="8eaad-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8eaad-162">RELATED LINKS</span></span>

[<span data-ttu-id="8eaad-163">Disable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8eaad-163">Disable-AzureTrafficManagerProfile</span></span>](./Disable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="8eaad-164">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8eaad-164">Enable-AzureTrafficManagerProfile</span></span>](./Enable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="8eaad-165">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8eaad-165">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="8eaad-166">새로운 AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8eaad-166">New-AzureTrafficManagerProfile</span></span>](./New-AzureTrafficManagerProfile.md)

[<span data-ttu-id="8eaad-167">제거-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8eaad-167">Remove-AzureTrafficManagerProfile</span></span>](./Remove-AzureTrafficManagerProfile.md)


