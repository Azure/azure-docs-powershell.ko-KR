---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: DE31891A-0EF7-44D7-B955-A3279D27CC21
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/new-aztrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/New-AzTrafficManagerProfile.md
ms.openlocfilehash: c5e1f69e8a11f09e4f7b838c5e489c8a240d40e6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198244"
---
# <span data-ttu-id="9b1d8-101">New-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9b1d8-101">New-AzTrafficManagerProfile</span></span>

## <span data-ttu-id="9b1d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b1d8-102">SYNOPSIS</span></span>
<span data-ttu-id="9b1d8-103">Traffic Manager 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d8-103">Creates a Traffic Manager profile.</span></span>

## <span data-ttu-id="9b1d8-104">구문</span><span class="sxs-lookup"><span data-stu-id="9b1d8-104">SYNTAX</span></span>

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

## <span data-ttu-id="9b1d8-105">설명</span><span class="sxs-lookup"><span data-stu-id="9b1d8-105">DESCRIPTION</span></span>
<span data-ttu-id="9b1d8-106">**New-AzTrafficManagerProfile** cmdlet은 Azure Traffic Manager 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d8-106">The **New-AzTrafficManagerProfile** cmdlet creates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="9b1d8-107">이름 매개 *변수 및* 필수 설정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d8-107">Specify the *Name* parameter and required settings.</span></span>
<span data-ttu-id="9b1d8-108">이 cmdlet은 새 프로필을 나타내는 로컬 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d8-108">This cmdlet returns a local object that represents the new profile.</span></span>

<span data-ttu-id="9b1d8-109">이 cmdlet은 Traffic Manager 엔드포인트를 구성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d8-109">This cmdlet does not configure Traffic Manager endpoints.</span></span>
<span data-ttu-id="9b1d8-110">Add-AzTrafficManagerEndpointConfig cmdlet을 사용하여 로컬 프로필 개체를 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d8-110">You can update the local profile object by using the Add-AzTrafficManagerEndpointConfig cmdlet.</span></span>
<span data-ttu-id="9b1d8-111">그런 다음, Set-AzTrafficManagerProfile cmdlet을 사용하여 Traffic Manager에 변경 내용을 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d8-111">Then upload changes to Traffic Manager by using the Set-AzTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="9b1d8-112">또는 New-AzTrafficManagerEndpoint cmdlet을 사용하여 엔드포인트를 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d8-112">Alternatively, you can add endpoints by using the New-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="9b1d8-113">예제</span><span class="sxs-lookup"><span data-stu-id="9b1d8-113">EXAMPLES</span></span>

### <span data-ttu-id="9b1d8-114">예제 1: 프로필 만들기</span><span class="sxs-lookup"><span data-stu-id="9b1d8-114">Example 1: Create a profile</span></span>
```
PS C:\>New-AzTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" -ProfileStatus Enabled -TrafficRoutingMethod Performance -RelativeDnsName "contosoapp" -TTL 30 -MonitorProtocol HTTP -MonitorPort 80 -MonitorPath "/default.aspx"
```

<span data-ttu-id="9b1d8-115">이 명령은 리소스 그룹 ResourceGroup11에 ContosoProfile이라는 Azure Traffic Manager 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d8-115">This command creates an Azure Traffic Manager profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="9b1d8-116">DNS FQDN이 contosoapp.trafficmanager.net.</span><span class="sxs-lookup"><span data-stu-id="9b1d8-116">The DNS FQDN is contosoapp.trafficmanager.net.</span></span>

## <span data-ttu-id="9b1d8-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b1d8-117">PARAMETERS</span></span>

### <span data-ttu-id="9b1d8-118">-CustomHeader</span><span class="sxs-lookup"><span data-stu-id="9b1d8-118">-CustomHeader</span></span>
<span data-ttu-id="9b1d8-119">프로브 요청에 대한 사용자 지정 헤더 이름 및 값 쌍의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d8-119">List of custom header name and value pairs for probe requests.</span></span>

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

### <span data-ttu-id="9b1d8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b1d8-120">-DefaultProfile</span></span>
<span data-ttu-id="9b1d8-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d8-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b1d8-122">-ExpectedStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="9b1d8-122">-ExpectedStatusCodeRange</span></span>
<span data-ttu-id="9b1d8-123">프로브 요청에 대해 예상되는 HTTP 상태 코드 범위 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d8-123">List of expected HTTP status code ranges for probe requests.</span></span>

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

### <span data-ttu-id="9b1d8-124">-MaxReturn</span><span class="sxs-lookup"><span data-stu-id="9b1d8-124">-MaxReturn</span></span>
<span data-ttu-id="9b1d8-125">다중값 라우팅 방법을 사용하여 프로필에 대해 반환된 최대 답변 수입니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d8-125">The maximum number of answers returned for profiles with a MultiValue routing method.</span></span>

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

### <span data-ttu-id="9b1d8-126">-MonitorIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="9b1d8-126">-MonitorIntervalInSeconds</span></span>
<span data-ttu-id="9b1d8-127">Traffic Manager가 이 프로필의 각 엔드포인트의 상태 확인 간격(초)입니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d8-127">The interval (in seconds) at which Traffic Manager will check the health of each endpoint in this profile.</span></span> <span data-ttu-id="9b1d8-128">기본값은 30입니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d8-128">The default is 30.</span></span>

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

### <span data-ttu-id="9b1d8-129">-MonitorPath</span><span class="sxs-lookup"><span data-stu-id="9b1d8-129">-MonitorPath</span></span>
<span data-ttu-id="9b1d8-130">엔드포인트 상태 모니터링에 사용되는 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d8-130">Specifies the path that is used to monitor endpoint health.</span></span>
<span data-ttu-id="9b1d8-131">엔드포인트 도메인 이름에 상대적인 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d8-131">Specify a value relative to the endpoint domain name.</span></span>
<span data-ttu-id="9b1d8-132">이 값은 슬래시(/)로 시작해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d8-132">This value must begin with a slash (/).</span></span>

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

### <span data-ttu-id="9b1d8-133">-MonitorPort</span><span class="sxs-lookup"><span data-stu-id="9b1d8-133">-MonitorPort</span></span>
<span data-ttu-id="9b1d8-134">엔드포인트 상태 모니터링에 사용되는 TCP 포트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d8-134">Specifies the TCP port that is used to monitor endpoint health.</span></span>
<span data-ttu-id="9b1d8-135">유효한 값은 1에서 65535까지의 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d8-135">Valid values are integers from 1 through 65535.</span></span>

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

### <span data-ttu-id="9b1d8-136">-MonitorProtocol</span><span class="sxs-lookup"><span data-stu-id="9b1d8-136">-MonitorProtocol</span></span>
<span data-ttu-id="9b1d8-137">엔드포인트 상태 모니터링에 사용할 프로토콜을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d8-137">Specifies the protocol to use to monitor endpoint health.</span></span>
<span data-ttu-id="9b1d8-138">유효한 값은</span><span class="sxs-lookup"><span data-stu-id="9b1d8-138">Valid values are:</span></span>

- <span data-ttu-id="9b1d8-139">HTTP</span><span class="sxs-lookup"><span data-stu-id="9b1d8-139">HTTP</span></span>
- <span data-ttu-id="9b1d8-140">HTTPS</span><span class="sxs-lookup"><span data-stu-id="9b1d8-140">HTTPS</span></span>

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

### <span data-ttu-id="9b1d8-141">-MonitorTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="9b1d8-141">-MonitorTimeoutInSeconds</span></span>
<span data-ttu-id="9b1d8-142">Traffic Manager에서 이 프로필의 엔드포인트가 상태 검사에 응답할 수 있는 시간(초)입니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d8-142">The time (in seconds) that Traffic Manager allows endpoints in this profile to respond to the health check.</span></span> <span data-ttu-id="9b1d8-143">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d8-143">The default is 10.</span></span>

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

### <span data-ttu-id="9b1d8-144">-MonitorToleratedNumberOfFailures</span><span class="sxs-lookup"><span data-stu-id="9b1d8-144">-MonitorToleratedNumberOfFailures</span></span>
<span data-ttu-id="9b1d8-145">Traffic Manager가 다음에 연속적으로 실패한 상태 검사 후 Degraded 프로필에서 엔드포인트를 선언하기 전에 Traffic Manager가 이를 수락하는 연속 실패 상태 검사의 수입니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d8-145">The number of consecutive failed health checks that Traffic Manager tolerates before declaring an endpoint in this profile Degraded after the next consecutive failed health check.</span></span> <span data-ttu-id="9b1d8-146">기본값은 3입니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d8-146">The default is 3.</span></span>

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

### <span data-ttu-id="9b1d8-147">-Name</span><span class="sxs-lookup"><span data-stu-id="9b1d8-147">-Name</span></span>
<span data-ttu-id="9b1d8-148">이 cmdlet에서 만드는 Traffic Manager 프로필의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d8-148">Specifies a name for the Traffic Manager profile that this cmdlet creates.</span></span>

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

### <span data-ttu-id="9b1d8-149">-ProfileStatus</span><span class="sxs-lookup"><span data-stu-id="9b1d8-149">-ProfileStatus</span></span>
<span data-ttu-id="9b1d8-150">프로필의 상태를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d8-150">Specifies the status of the profile.</span></span>
<span data-ttu-id="9b1d8-151">유효한 값은 Enabled 및 Disabled입니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d8-151">Valid values are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="9b1d8-152">-RelativeDnsName</span><span class="sxs-lookup"><span data-stu-id="9b1d8-152">-RelativeDnsName</span></span>
<span data-ttu-id="9b1d8-153">이 Traffic Manager 프로필에서 제공하는 상대 DNS 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d8-153">Specifies the relative DNS name that this Traffic Manager profile provides.</span></span>
<span data-ttu-id="9b1d8-154">Traffic Manager는 이 값과 Azure Traffic Manager가 프로필의 FQDN(정식 도메인 이름)을 형성하는 데 사용하는 DNS 도메인 이름을 결합합니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d8-154">Traffic Manager combines this value and the DNS domain name that Azure Traffic Manager uses to form the fully qualified domain name (FQDN) of the profile.</span></span>

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

### <span data-ttu-id="9b1d8-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b1d8-155">-ResourceGroupName</span></span>
<span data-ttu-id="9b1d8-156">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d8-156">Specifies the name of a resource group.</span></span>
<span data-ttu-id="9b1d8-157">이 cmdlet은 이 매개 변수가 지정하는 그룹에 Traffic Manager 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d8-157">This cmdlet creates a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="9b1d8-158">-Tag</span><span class="sxs-lookup"><span data-stu-id="9b1d8-158">-Tag</span></span>
<span data-ttu-id="9b1d8-159">서버의 태그로 설정된 해시 테이블 형식의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d8-159">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="9b1d8-160">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="9b1d8-160">For example:</span></span>

<span data-ttu-id="9b1d8-161">@{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="9b1d8-161">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="9b1d8-162">-TrafficRoutingMethod</span><span class="sxs-lookup"><span data-stu-id="9b1d8-162">-TrafficRoutingMethod</span></span>
<span data-ttu-id="9b1d8-163">트래픽 라우팅 방법을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d8-163">Specifies the traffic routing method.</span></span>
<span data-ttu-id="9b1d8-164">이 메서드는 들어오는 DNS 쿼리에 대한 응답으로 반환하는 엔드포인트 Traffic Manager를 판단합니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d8-164">This method determines which endpoint Traffic Manager returns in response to incoming DNS queries.</span></span>
<span data-ttu-id="9b1d8-165">유효한 값은</span><span class="sxs-lookup"><span data-stu-id="9b1d8-165">Valid values are:</span></span>

- <span data-ttu-id="9b1d8-166">성능</span><span class="sxs-lookup"><span data-stu-id="9b1d8-166">Performance</span></span>
- <span data-ttu-id="9b1d8-167">가중치</span><span class="sxs-lookup"><span data-stu-id="9b1d8-167">Weighted</span></span>
- <span data-ttu-id="9b1d8-168">우선 순위</span><span class="sxs-lookup"><span data-stu-id="9b1d8-168">Priority</span></span>
- <span data-ttu-id="9b1d8-169">지리적</span><span class="sxs-lookup"><span data-stu-id="9b1d8-169">Geographic</span></span>

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

### <span data-ttu-id="9b1d8-170">-Ttl</span><span class="sxs-lookup"><span data-stu-id="9b1d8-170">-Ttl</span></span>
<span data-ttu-id="9b1d8-171">DNS TTL(Time to Live) 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d8-171">Specifies the DNS Time to Live (TTL) value.</span></span>

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

### <span data-ttu-id="9b1d8-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b1d8-172">CommonParameters</span></span>
<span data-ttu-id="9b1d8-173">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9b1d8-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b1d8-174">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9b1d8-174">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b1d8-175">입력</span><span class="sxs-lookup"><span data-stu-id="9b1d8-175">INPUTS</span></span>

### <span data-ttu-id="9b1d8-176">없음</span><span class="sxs-lookup"><span data-stu-id="9b1d8-176">None</span></span>

## <span data-ttu-id="9b1d8-177">출력</span><span class="sxs-lookup"><span data-stu-id="9b1d8-177">OUTPUTS</span></span>

### <span data-ttu-id="9b1d8-178">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9b1d8-178">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerProfile</span></span>

## <span data-ttu-id="9b1d8-179">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9b1d8-179">NOTES</span></span>

## <span data-ttu-id="9b1d8-180">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9b1d8-180">RELATED LINKS</span></span>

[<span data-ttu-id="9b1d8-181">Add-AzTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="9b1d8-181">Add-AzTrafficManagerEndpointConfig</span></span>](./Add-AzTrafficManagerEndpointConfig.md)

[<span data-ttu-id="9b1d8-182">Disable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9b1d8-182">Disable-AzTrafficManagerProfile</span></span>](./Disable-AzTrafficManagerProfile.md)

[<span data-ttu-id="9b1d8-183">Enable-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9b1d8-183">Enable-AzTrafficManagerProfile</span></span>](./Enable-AzTrafficManagerProfile.md)

[<span data-ttu-id="9b1d8-184">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9b1d8-184">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerProfile.md)

[<span data-ttu-id="9b1d8-185">Remove-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9b1d8-185">Remove-AzTrafficManagerProfile</span></span>](./Remove-AzTrafficManagerProfile.md)

[<span data-ttu-id="9b1d8-186">Set-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9b1d8-186">Set-AzTrafficManagerProfile</span></span>](./Set-AzTrafficManagerProfile.md)


