---
external help file: Microsoft.WindowsAzure.Commands.TrafficManager.dll-Help.xml
ms.assetid: 2287E103-442D-47FB-8279-0AE5936412C9
online version: ''
schema: 2.0.0
ms.openlocfilehash: f6a12f0e74964e096577b5a4fec0a46fd41d7872
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046202"
---
# <span data-ttu-id="3ac18-101">New-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3ac18-101">New-AzureTrafficManagerProfile</span></span>

## <span data-ttu-id="3ac18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ac18-102">SYNOPSIS</span></span>
<span data-ttu-id="3ac18-103">Traffic Manager 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3ac18-103">Creates a Traffic Manager profile.</span></span>

## <span data-ttu-id="3ac18-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3ac18-104">SYNTAX</span></span>

```
New-AzureTrafficManagerProfile -Name <String> -DomainName <String> -LoadBalancingMethod <String>
 -MonitorPort <Int32> -MonitorProtocol <String> -MonitorRelativePath <String> -Ttl <Int32>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3ac18-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3ac18-105">DESCRIPTION</span></span>
<span data-ttu-id="3ac18-106">**AzureTrafficManagerProfile** Cmdlet은 Microsoft Azure Traffic Manager 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3ac18-106">The **New-AzureTrafficManagerProfile** cmdlet creates a Microsoft Azure Traffic Manager profile.</span></span>

<span data-ttu-id="3ac18-107">*LoadBalancingMethod* 값을 "장애 조치 (Failover)"로 설정한 프로필을 만든 후에는 Add-AzureTrafficManagerEndpoint cmdlet을 사용 하 여 프로필에 추가 하는 끝점의 장애 조치 순서를 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3ac18-107">After you create a profile where you set the *LoadBalancingMethod* value to "Failover", you can determine the failover order of the endpoints you add to your profile with the Add-AzureTrafficManagerEndpoint cmdlet.</span></span>
<span data-ttu-id="3ac18-108">자세한 내용은 아래 예제 2를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3ac18-108">For more information, see Example 2 below.</span></span>

## <span data-ttu-id="3ac18-109">예제의</span><span class="sxs-lookup"><span data-stu-id="3ac18-109">EXAMPLES</span></span>

### <span data-ttu-id="3ac18-110">예제 1: Traffic Manager 프로필 만들기</span><span class="sxs-lookup"><span data-stu-id="3ac18-110">Example 1: Create a Traffic Manager profile</span></span>
```
PS C:\>New-AzureTrafficManagerProfile -Name "MyProfile" -DomainName "My.profile.trafficmanager.net" -LoadBalancingMethod "RoundRobin" -Ttl 30 -MonitorProtocol "Http" -MonitorPort 80 -MonitorRelativePath "/"
```

<span data-ttu-id="3ac18-111">이 명령은 라운드 로빈 부하 분산 방법, 30 초의 TTL, HTTP 모니터링 프로토콜, 모니터링 포트 80, 지정 된 경로를 사용 하 여 지정 된 Traffic Manager 도메인에 MyProfile 이라는 트래픽 관리자 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3ac18-111">This command creates a Traffic Manager profile named MyProfile in the specified Traffic Manager domain with a Round Robin load balancing method, a TTL of 30 seconds, HTTP monitoring protocol, monitoring port 80, and with the specified path.</span></span>

### <span data-ttu-id="3ac18-112">예제 2: 원하는 장애 조치 순서로 끝점 순서 변경</span><span class="sxs-lookup"><span data-stu-id="3ac18-112">Example 2: Reorder endpoints to desired failover order</span></span>
```
PS C:\>$Profile = Get-AzureTrafficManagerProfile -Name "MyProfile"
PS C:\> $Profile.Endpoints[0],$Profile.Endpoints[1] = $Profile.Endpoints[1],$Profile.Endpoints[0]
PS C:\> $Profile = Set-AzureTrafficManagerProfile
```

<span data-ttu-id="3ac18-113">이 예제에서는 MyProfile에 추가한 끝점을 원하는 장애 조치 순서에 따라 순서를 재정리 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac18-113">This example reorders the endpoints added to MyProfile to the desired failover order.</span></span>

<span data-ttu-id="3ac18-114">첫 번째 명령은 MyProfile 이라는 트래픽 관리자 프로필 개체를 가져와 개체를 $Profile 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac18-114">The first command gets the Traffic Manager profile object named MyProfile and stores the object in the $Profile variable.</span></span>

<span data-ttu-id="3ac18-115">두 번째 명령은 끝점 배열의 끝점을 장애 조치 발생 순서에 따라 다시 정렬 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac18-115">The second command re-orders the endpoints from  the endpoints array to the order in which failover should occur.</span></span>

<span data-ttu-id="3ac18-116">마지막 명령은 새 끝점 순서를 사용 하 여 $Profile에 저장 된 Traffic Manager 프로필을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac18-116">The last command updates the Traffic Manager profile stored in $Profile with the new endpoint order.</span></span>

## <span data-ttu-id="3ac18-117">변수</span><span class="sxs-lookup"><span data-stu-id="3ac18-117">PARAMETERS</span></span>

### <span data-ttu-id="3ac18-118">-DomainName</span><span class="sxs-lookup"><span data-stu-id="3ac18-118">-DomainName</span></span>
<span data-ttu-id="3ac18-119">Traffic Manager 프로필의 도메인 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac18-119">Specifies the domain name of the Traffic Manager profile.</span></span>
<span data-ttu-id="3ac18-120">Trafficmanager.net의 하위 도메인 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac18-120">This must be a subdomain of trafficmanager.net.</span></span>

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

### <span data-ttu-id="3ac18-121">-LoadBalancingMethod</span><span class="sxs-lookup"><span data-stu-id="3ac18-121">-LoadBalancingMethod</span></span>
<span data-ttu-id="3ac18-122">연결을 배포 하는 데 사용할 부하 분산 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac18-122">Specifies the load balancing method to use to distribute the connection.</span></span>
<span data-ttu-id="3ac18-123">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="3ac18-123">Valid values are:</span></span> 

- <span data-ttu-id="3ac18-124">성능을</span><span class="sxs-lookup"><span data-stu-id="3ac18-124">Performance</span></span>
- <span data-ttu-id="3ac18-125">장애 조치</span><span class="sxs-lookup"><span data-stu-id="3ac18-125">Failover</span></span>
- <span data-ttu-id="3ac18-126">RoundRobin</span><span class="sxs-lookup"><span data-stu-id="3ac18-126">RoundRobin</span></span>

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

### <span data-ttu-id="3ac18-127">-모니터 포트</span><span class="sxs-lookup"><span data-stu-id="3ac18-127">-MonitorPort</span></span>
<span data-ttu-id="3ac18-128">끝점 상태를 모니터링 하는 데 사용 되는 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac18-128">Specifies the port used to monitor endpoint health.</span></span>
<span data-ttu-id="3ac18-129">유효한 값은 0 보다 크고 65535 보다 작거나 같은 정수 값입니다.</span><span class="sxs-lookup"><span data-stu-id="3ac18-129">Valid values are integer values greater than 0 and less than or equal to 65,535.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ac18-130">-모니터 프로토콜</span><span class="sxs-lookup"><span data-stu-id="3ac18-130">-MonitorProtocol</span></span>
<span data-ttu-id="3ac18-131">끝점 상태를 모니터링 하는 데 사용할 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac18-131">Specifies the protocol to use to monitor endpoint health.</span></span>
<span data-ttu-id="3ac18-132">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="3ac18-132">Valid values are:</span></span> 

- <span data-ttu-id="3ac18-133">Http</span><span class="sxs-lookup"><span data-stu-id="3ac18-133">Http</span></span>

- <span data-ttu-id="3ac18-134">Https</span><span class="sxs-lookup"><span data-stu-id="3ac18-134">Https</span></span>

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

### <span data-ttu-id="3ac18-135">-MonitorRelativePath</span><span class="sxs-lookup"><span data-stu-id="3ac18-135">-MonitorRelativePath</span></span>
<span data-ttu-id="3ac18-136">상태를 검색 하기 위해 끝점 도메인 이름에 상대적인 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac18-136">Specifies the path relative to the endpoint domain name to probe for health state.</span></span>
<span data-ttu-id="3ac18-137">경로는 다음 제한을 충족 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac18-137">The path must meet the following restrictions:</span></span> 

- <span data-ttu-id="3ac18-138">경로는 1 ~ 1000 자 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac18-138">The path must be from 1 through 1000 characters.</span></span>

- <span data-ttu-id="3ac18-139">슬래시,/으로 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac18-139">It must start with a forward slash, /.</span></span>

- <span data-ttu-id="3ac18-140">XML 요소를 포함 하지 않아야 \<\> 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac18-140">It must contain no XML elements, \<\>.</span></span>

- <span data-ttu-id="3ac18-141">이중 슬래시,//를 포함 하지 않아야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac18-141">It must contain no double slashes, //.</span></span>

- <span data-ttu-id="3ac18-142">잘못 된 HTML 이스케이프 문자가 포함 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac18-142">It must contain no invalid HTML escape characters.</span></span>
<span data-ttu-id="3ac18-143">예를 들면% XY입니다.</span><span class="sxs-lookup"><span data-stu-id="3ac18-143">For example, %XY.</span></span>

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

### <span data-ttu-id="3ac18-144">-이름</span><span class="sxs-lookup"><span data-stu-id="3ac18-144">-Name</span></span>
<span data-ttu-id="3ac18-145">만들려는 Traffic Manager 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac18-145">Specifies the name of the Traffic Manager profile to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3ac18-146">-프로필</span><span class="sxs-lookup"><span data-stu-id="3ac18-146">-Profile</span></span>
<span data-ttu-id="3ac18-147">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac18-147">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="3ac18-148">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="3ac18-148">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3ac18-149">-Ttl</span><span class="sxs-lookup"><span data-stu-id="3ac18-149">-Ttl</span></span>
<span data-ttu-id="3ac18-150">DNS 항목을 캐시할 수 있는 시간을 로컬 DNS 확인자에 알리는 DNS TTL (Time to Live)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac18-150">Specifies the DNS Time-to-Live (TTL) that informs the Local DNS resolvers how long to cache DNS entries.</span></span>
<span data-ttu-id="3ac18-151">유효한 값은 30부터 999999 까지의 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="3ac18-151">Valid values are integers from 30 through 999,999.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3ac18-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ac18-152">CommonParameters</span></span>
<span data-ttu-id="3ac18-153">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac18-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ac18-154">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ac18-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ac18-155">입력</span><span class="sxs-lookup"><span data-stu-id="3ac18-155">INPUTS</span></span>

## <span data-ttu-id="3ac18-156">출력</span><span class="sxs-lookup"><span data-stu-id="3ac18-156">OUTPUTS</span></span>

### <span data-ttu-id="3ac18-157">WindowsAzure. TrafficManager. 유틸리티. IProfileWithDefinition</span><span class="sxs-lookup"><span data-stu-id="3ac18-157">Microsoft.WindowsAzure.Commands.Utilities.TrafficManager.Models.IProfileWithDefinition</span></span>
<span data-ttu-id="3ac18-158">이 cmdlet은 Traffic Manager 프로필 개체를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="3ac18-158">This cmdlet generates a Traffic Manager profile object.</span></span>

## <span data-ttu-id="3ac18-159">상속자</span><span class="sxs-lookup"><span data-stu-id="3ac18-159">NOTES</span></span>

## <span data-ttu-id="3ac18-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3ac18-160">RELATED LINKS</span></span>

[<span data-ttu-id="3ac18-161">Disable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3ac18-161">Disable-AzureTrafficManagerProfile</span></span>](./Disable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="3ac18-162">Enable-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3ac18-162">Enable-AzureTrafficManagerProfile</span></span>](./Enable-AzureTrafficManagerProfile.md)

[<span data-ttu-id="3ac18-163">Get-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3ac18-163">Get-AzureTrafficManagerProfile</span></span>](./Get-AzureTrafficManagerProfile.md)

[<span data-ttu-id="3ac18-164">제거-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3ac18-164">Remove-AzureTrafficManagerProfile</span></span>](./Remove-AzureTrafficManagerProfile.md)

[<span data-ttu-id="3ac18-165">Set-AzureTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="3ac18-165">Set-AzureTrafficManagerProfile</span></span>](./Set-AzureTrafficManagerProfile.md)


