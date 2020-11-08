---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: DE31891A-0EF7-44D7-B955-A3279D27CC21
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/new-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerProfile.md
ms.openlocfilehash: c5e1f69e8a11f09e4f7b838c5e489c8a240d40e6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042602"
---
# <span data-ttu-id="33be6-101">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="33be6-101">New-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="33be6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33be6-102">SYNOPSIS</span></span>
<span data-ttu-id="33be6-103">Traffic Manager 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="33be6-103">Creates a Traffic Manager profile.</span></span>

## <span data-ttu-id="33be6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="33be6-104">SYNTAX</span></span>

```
New-AzTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-ProfileStatus <String>]
 -RelativeDnsName <String> -Ttl <UInt32> -TrafficRoutingMethod <String> -MonitorProtocol <String>
 -MonitorPort <UInt32> [-MonitorPath <String>] [-MonitorIntervalInSeconds <Int32>]
 [-MonitorTimeoutInSeconds <Int32>] [-MonitorToleratedNumberOfFailures <Int32>] [-MaxReturn <Int64>]
 [-Tag <Hashtable>]
 [-CustomHeader <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerCustomHeader]>]
 [-ExpectedStatusCodeRange <System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerExpectedStatusCodeRange]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33be6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="33be6-105">DESCRIPTION</span></span>
<span data-ttu-id="33be6-106">**새 AzTrafficManagerProfile** Cmdlet은 Azure Traffic Manager 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="33be6-106">The **New-AzTrafficManagerProfile** cmdlet creates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="33be6-107">*Name* 매개 변수 및 필수 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33be6-107">Specify the *Name* parameter and required settings.</span></span>
<span data-ttu-id="33be6-108">이 cmdlet은 새 프로필을 나타내는 local 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="33be6-108">This cmdlet returns a local object that represents the new profile.</span></span>

<span data-ttu-id="33be6-109">이 cmdlet은 Traffic Manager 끝점을 구성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="33be6-109">This cmdlet does not configure Traffic Manager endpoints.</span></span>
<span data-ttu-id="33be6-110">Add-AzTrafficManagerEndpointConfig cmdlet을 사용 하 여 로컬 프로필 개체를 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="33be6-110">You can update the local profile object by using the Add-AzTrafficManagerEndpointConfig cmdlet.</span></span>
<span data-ttu-id="33be6-111">그런 다음 Set-AzTrafficManagerProfile cmdlet을 사용 하 여 Traffic Manager 변경 내용을 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="33be6-111">Then upload changes to Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="33be6-112">또는 New-AzTrafficManagerEndpoint cmdlet을 사용 하 여 끝점을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="33be6-112">Alternatively, you can add endpoints by using the New-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="33be6-113">예제의</span><span class="sxs-lookup"><span data-stu-id="33be6-113">EXAMPLES</span></span>

### <span data-ttu-id="33be6-114">예제 1: 프로필 만들기</span><span class="sxs-lookup"><span data-stu-id="33be6-114">Example 1: Create a profile</span></span>
```
PS C:\>New-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" -ProfileStatus Enabled -TrafficRoutingMethod Performance -RelativeDnsName "contosoapp" -TTL 30 -MonitorProtocol HTTP -MonitorPort 80 -MonitorPath "/default.aspx"
```

<span data-ttu-id="33be6-115">이 명령은 리소스 그룹 ResourceGroup11에서 ContosoProfile 이라는 Azure Traffic Manager 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="33be6-115">This command creates an Azure Traffic Manager profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="33be6-116">DNS FQDN은 contosoapp.trafficmanager.net입니다.</span><span class="sxs-lookup"><span data-stu-id="33be6-116">The DNS FQDN is contosoapp.trafficmanager.net.</span></span>

## <span data-ttu-id="33be6-117">변수</span><span class="sxs-lookup"><span data-stu-id="33be6-117">PARAMETERS</span></span>

### <span data-ttu-id="33be6-118">-CustomHeader</span><span class="sxs-lookup"><span data-stu-id="33be6-118">-CustomHeader</span></span>
<span data-ttu-id="33be6-119">검색 요청에 대 한 사용자 지정 헤더 이름 및 값 쌍의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="33be6-119">List of custom header name and value pairs for probe requests.</span></span>

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

### <span data-ttu-id="33be6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33be6-120">-DefaultProfile</span></span>
<span data-ttu-id="33be6-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="33be6-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33be6-122">-ExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="33be6-122">-ExpectedStatusCodeRange</span></span>
<span data-ttu-id="33be6-123">프로브 요청에 대해 예상 되는 HTTP 상태 코드 범위 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="33be6-123">List of expected HTTP status code ranges for probe requests.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerExpectedStatusCodeRange]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33be6-124">-MaxReturn</span><span class="sxs-lookup"><span data-stu-id="33be6-124">-MaxReturn</span></span>
<span data-ttu-id="33be6-125">다중값 라우팅 메서드를 사용 하 여 프로필에 대해 반환 되는 최대 응답 수입니다.</span><span class="sxs-lookup"><span data-stu-id="33be6-125">The maximum number of answers returned for profiles with a MultiValue routing method.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33be6-126">-MonitorIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="33be6-126">-MonitorIntervalInSeconds</span></span>
<span data-ttu-id="33be6-127">트래픽 관리자가이 프로필에서 각 끝점의 상태를 확인 하는 간격 (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="33be6-127">The interval (in seconds) at which Traffic Manager will check the health of each endpoint in this profile.</span></span> <span data-ttu-id="33be6-128">기본값은 30입니다.</span><span class="sxs-lookup"><span data-stu-id="33be6-128">The default is 30.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: IntervalInSecondsForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33be6-129">-MonitorPath</span><span class="sxs-lookup"><span data-stu-id="33be6-129">-MonitorPath</span></span>
<span data-ttu-id="33be6-130">끝점 상태를 모니터링 하는 데 사용 되는 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33be6-130">Specifies the path that is used to monitor endpoint health.</span></span>
<span data-ttu-id="33be6-131">끝점 도메인 이름에 상대적인 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33be6-131">Specify a value relative to the endpoint domain name.</span></span>
<span data-ttu-id="33be6-132">이 값은 슬래시 (/)로 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="33be6-132">This value must begin with a slash (/).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PathForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33be6-133">-모니터 포트</span><span class="sxs-lookup"><span data-stu-id="33be6-133">-MonitorPort</span></span>
<span data-ttu-id="33be6-134">끝점 상태를 모니터링 하는 데 사용 되는 TCP 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33be6-134">Specifies the TCP port that is used to monitor endpoint health.</span></span>
<span data-ttu-id="33be6-135">유효한 값은 1부터 65535 까지의 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="33be6-135">Valid values are integers from 1 through 65535.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases: PortForMonitor

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33be6-136">-모니터 프로토콜</span><span class="sxs-lookup"><span data-stu-id="33be6-136">-MonitorProtocol</span></span>
<span data-ttu-id="33be6-137">끝점 상태를 모니터링 하는 데 사용할 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33be6-137">Specifies the protocol to use to monitor endpoint health.</span></span>
<span data-ttu-id="33be6-138">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="33be6-138">Valid values are:</span></span>

- <span data-ttu-id="33be6-139">HTTP</span><span class="sxs-lookup"><span data-stu-id="33be6-139">HTTP</span></span>
- <span data-ttu-id="33be6-140">HTTPS</span><span class="sxs-lookup"><span data-stu-id="33be6-140">HTTPS</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ProtocolForMonitor
Accepted values: HTTP, HTTPS, TCP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33be6-141">-MonitorTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="33be6-141">-MonitorTimeoutInSeconds</span></span>
<span data-ttu-id="33be6-142">트래픽 관리자가이 프로필의 끝점에 상태 검사에 응답할 수 있도록 허용 하는 시간 (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="33be6-142">The time (in seconds) that Traffic Manager allows endpoints in this profile to respond to the health check.</span></span> <span data-ttu-id="33be6-143">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="33be6-143">The default is 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: TimeoutInSecondsForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33be6-144">-MonitorToleratedNumberOfFailures</span><span class="sxs-lookup"><span data-stu-id="33be6-144">-MonitorToleratedNumberOfFailures</span></span>
<span data-ttu-id="33be6-145">실패 한 연속 상태 검사 수는이 프로필의 끝점을 선언 하기 전에 트래픽 관리자 tolerates에서 다음 번의 연속 되지 않은 상태 검사 후에 성능이 저하 됩니다.</span><span class="sxs-lookup"><span data-stu-id="33be6-145">The number of consecutive failed health checks that Traffic Manager tolerates before declaring an endpoint in this profile Degraded after the next consecutive failed health check.</span></span> <span data-ttu-id="33be6-146">기본값은 3입니다.</span><span class="sxs-lookup"><span data-stu-id="33be6-146">The default is 3.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ToleratedNumberOfFailuresForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33be6-147">-이름</span><span class="sxs-lookup"><span data-stu-id="33be6-147">-Name</span></span>
<span data-ttu-id="33be6-148">이 cmdlet이 만드는 Traffic Manager 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33be6-148">Specifies a name for the Traffic Manager profile that this cmdlet creates.</span></span>

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

### <span data-ttu-id="33be6-149">-ProfileStatus</span><span class="sxs-lookup"><span data-stu-id="33be6-149">-ProfileStatus</span></span>
<span data-ttu-id="33be6-150">프로필의 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33be6-150">Specifies the status of the profile.</span></span>
<span data-ttu-id="33be6-151">유효한 값은 사용 및 사용 안 함입니다.</span><span class="sxs-lookup"><span data-stu-id="33be6-151">Valid values are: Enabled and Disabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33be6-152">-RelativeDnsName</span><span class="sxs-lookup"><span data-stu-id="33be6-152">-RelativeDnsName</span></span>
<span data-ttu-id="33be6-153">이 트래픽 관리자 프로필이 제공 하는 상대 DNS 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33be6-153">Specifies the relative DNS name that this Traffic Manager profile provides.</span></span>
<span data-ttu-id="33be6-154">Traffic Manager는 Azure 트래픽 관리자가 프로필의 FQDN (정규화 된 도메인 이름)을 형성 하는 데 사용 하는 DNS 도메인 이름 및이 값을 결합 합니다.</span><span class="sxs-lookup"><span data-stu-id="33be6-154">Traffic Manager combines this value and the DNS domain name that Azure Traffic Manager uses to form the fully qualified domain name (FQDN) of the profile.</span></span>

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

### <span data-ttu-id="33be6-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33be6-155">-ResourceGroupName</span></span>
<span data-ttu-id="33be6-156">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33be6-156">Specifies the name of a resource group.</span></span>
<span data-ttu-id="33be6-157">이 cmdlet은이 매개 변수에서 지정 하는 그룹에 Traffic Manager 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="33be6-157">This cmdlet creates a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="33be6-158">태그</span><span class="sxs-lookup"><span data-stu-id="33be6-158">-Tag</span></span>
<span data-ttu-id="33be6-159">서버에서 태그로 설정 된 해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="33be6-159">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="33be6-160">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="33be6-160">For example:</span></span>

<span data-ttu-id="33be6-161">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="33be6-161">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33be6-162">-TrafficRoutingMethod</span><span class="sxs-lookup"><span data-stu-id="33be6-162">-TrafficRoutingMethod</span></span>
<span data-ttu-id="33be6-163">트래픽 라우팅 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33be6-163">Specifies the traffic routing method.</span></span>
<span data-ttu-id="33be6-164">이 메서드는 들어오는 DNS 쿼리에 대 한 응답으로 반환 되는 끝점 트래픽 관리자를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="33be6-164">This method determines which endpoint Traffic Manager returns in response to incoming DNS queries.</span></span>
<span data-ttu-id="33be6-165">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="33be6-165">Valid values are:</span></span>

- <span data-ttu-id="33be6-166">성능을</span><span class="sxs-lookup"><span data-stu-id="33be6-166">Performance</span></span>
- <span data-ttu-id="33be6-167">중</span><span class="sxs-lookup"><span data-stu-id="33be6-167">Weighted</span></span>
- <span data-ttu-id="33be6-168">중요도</span><span class="sxs-lookup"><span data-stu-id="33be6-168">Priority</span></span>
- <span data-ttu-id="33be6-169">지역을</span><span class="sxs-lookup"><span data-stu-id="33be6-169">Geographic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Performance, Weighted, Priority, Geographic, Subnet, MultiValue

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33be6-170">-Ttl</span><span class="sxs-lookup"><span data-stu-id="33be6-170">-Ttl</span></span>
<span data-ttu-id="33be6-171">TTL (Time to Live) 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33be6-171">Specifies the DNS Time to Live (TTL) value.</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33be6-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33be6-172">CommonParameters</span></span>
<span data-ttu-id="33be6-173">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="33be6-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33be6-174">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33be6-174">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33be6-175">입력</span><span class="sxs-lookup"><span data-stu-id="33be6-175">INPUTS</span></span>

### <span data-ttu-id="33be6-176">않아야</span><span class="sxs-lookup"><span data-stu-id="33be6-176">None</span></span>

## <span data-ttu-id="33be6-177">출력</span><span class="sxs-lookup"><span data-stu-id="33be6-177">OUTPUTS</span></span>

### <span data-ttu-id="33be6-178">TrafficManager. TrafficManagerProfile/.</span><span class="sxs-lookup"><span data-stu-id="33be6-178">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="33be6-179">상속자</span><span class="sxs-lookup"><span data-stu-id="33be6-179">NOTES</span></span>

## <span data-ttu-id="33be6-180">관련 링크</span><span class="sxs-lookup"><span data-stu-id="33be6-180">RELATED LINKS</span></span>

[<span data-ttu-id="33be6-181">추가-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="33be6-181">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="33be6-182">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="33be6-182">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="33be6-183">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="33be6-183">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="33be6-184">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="33be6-184">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="33be6-185">제거-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="33be6-185">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="33be6-186">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="33be6-186">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


