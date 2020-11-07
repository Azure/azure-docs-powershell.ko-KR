---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: DE31891A-0EF7-44D7-B955-A3279D27CC21
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 8b88ee761ab9ee136777fb29e7726a2f72110553
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711466"
---
# <span data-ttu-id="5c1b5-101">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5c1b5-101">New-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="5c1b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c1b5-102">SYNOPSIS</span></span>
<span data-ttu-id="5c1b5-103">Traffic Manager 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5c1b5-103">Creates a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c1b5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5c1b5-104">SYNTAX</span></span>

```
New-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-ProfileStatus <String>]
 -RelativeDnsName <String> -Ttl <UInt32> -TrafficRoutingMethod <String> -MonitorProtocol <String>
 -MonitorPort <UInt32> [-MonitorPath <String>] [-MonitorIntervalInSeconds <Int32>]
 [-MonitorTimeoutInSeconds <Int32>] [-MonitorToleratedNumberOfFailures <Int32>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c1b5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5c1b5-105">DESCRIPTION</span></span>
<span data-ttu-id="5c1b5-106">**새 AzureRmTrafficManagerProfile** Cmdlet은 Azure Traffic Manager 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5c1b5-106">The **New-AzureRmTrafficManagerProfile** cmdlet creates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="5c1b5-107">*Name* 매개 변수 및 필수 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c1b5-107">Specify the *Name* parameter and required settings.</span></span>
<span data-ttu-id="5c1b5-108">이 cmdlet은 새 프로필을 나타내는 local 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c1b5-108">This cmdlet returns a local object that represents the new profile.</span></span>

<span data-ttu-id="5c1b5-109">이 cmdlet은 Traffic Manager 끝점을 구성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5c1b5-109">This cmdlet does not configure Traffic Manager endpoints.</span></span>
<span data-ttu-id="5c1b5-110">Add-AzureRmTrafficManagerEndpointConfig cmdlet을 사용 하 여 로컬 프로필 개체를 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5c1b5-110">You can update the local profile object by using the Add-AzureRmTrafficManagerEndpointConfig cmdlet.</span></span>
<span data-ttu-id="5c1b5-111">그런 다음 Set-AzureRmTrafficManagerProfile cmdlet을 사용 하 여 Traffic Manager 변경 내용을 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c1b5-111">Then upload changes to Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="5c1b5-112">또는 New-AzureRmTrafficManagerEndpoint cmdlet을 사용 하 여 끝점을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5c1b5-112">Alternatively, you can add endpoints by using the New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="5c1b5-113">예제의</span><span class="sxs-lookup"><span data-stu-id="5c1b5-113">EXAMPLES</span></span>

### <span data-ttu-id="5c1b5-114">예제 1: 프로필 만들기</span><span class="sxs-lookup"><span data-stu-id="5c1b5-114">Example 1: Create a profile</span></span>
```
PS C:\>New-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" -ProfileStatus Enabled -TrafficRoutingMethod Performance -RelativeDnsName "contosoapp" -TTL 30 -MonitorProtocol HTTP -MonitorPort 80 -MonitorPath "/default.aspx"
```

<span data-ttu-id="5c1b5-115">이 명령은 리소스 그룹 ResourceGroup11에서 ContosoProfile 이라는 Azure Traffic Manager 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5c1b5-115">This command creates an Azure Traffic Manager profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="5c1b5-116">DNS FQDN은 contosoapp.trafficmanager.net입니다.</span><span class="sxs-lookup"><span data-stu-id="5c1b5-116">The DNS FQDN is contosoapp.trafficmanager.net.</span></span>

## <span data-ttu-id="5c1b5-117">변수</span><span class="sxs-lookup"><span data-stu-id="5c1b5-117">PARAMETERS</span></span>

### <span data-ttu-id="5c1b5-118">-MonitorIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="5c1b5-118">-MonitorIntervalInSeconds</span></span>
<span data-ttu-id="5c1b5-119">트래픽 관리자가이 프로필에서 각 끝점의 상태를 확인 하는 간격 (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="5c1b5-119">The interval (in seconds) at which Traffic Manager will check the health of each endpoint in this profile.</span></span> <span data-ttu-id="5c1b5-120">기본값은 30입니다.</span><span class="sxs-lookup"><span data-stu-id="5c1b5-120">The default is 30.</span></span>

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

### <span data-ttu-id="5c1b5-121">-MonitorPath</span><span class="sxs-lookup"><span data-stu-id="5c1b5-121">-MonitorPath</span></span>
<span data-ttu-id="5c1b5-122">끝점 상태를 모니터링 하는 데 사용 되는 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c1b5-122">Specifies the path that is used to monitor endpoint health.</span></span>
<span data-ttu-id="5c1b5-123">끝점 도메인 이름에 상대적인 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c1b5-123">Specify a value relative to the endpoint domain name.</span></span>
<span data-ttu-id="5c1b5-124">이 값은 슬래시 (/)로 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c1b5-124">This value must begin with a slash (/).</span></span>

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

### <span data-ttu-id="5c1b5-125">-모니터 포트</span><span class="sxs-lookup"><span data-stu-id="5c1b5-125">-MonitorPort</span></span>
<span data-ttu-id="5c1b5-126">끝점 상태를 모니터링 하는 데 사용 되는 TCP 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c1b5-126">Specifies the TCP port that is used to monitor endpoint health.</span></span>
<span data-ttu-id="5c1b5-127">유효한 값은 1부터 65535 까지의 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="5c1b5-127">Valid values are integers from 1 through 65535.</span></span>

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

### <span data-ttu-id="5c1b5-128">-모니터 프로토콜</span><span class="sxs-lookup"><span data-stu-id="5c1b5-128">-MonitorProtocol</span></span>
<span data-ttu-id="5c1b5-129">끝점 상태를 모니터링 하는 데 사용할 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c1b5-129">Specifies the protocol to use to monitor endpoint health.</span></span>
<span data-ttu-id="5c1b5-130">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5c1b5-130">Valid values are:</span></span>

- <span data-ttu-id="5c1b5-131">HTTP</span><span class="sxs-lookup"><span data-stu-id="5c1b5-131">HTTP</span></span>
- <span data-ttu-id="5c1b5-132">HTTPS</span><span class="sxs-lookup"><span data-stu-id="5c1b5-132">HTTPS</span></span>

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

### <span data-ttu-id="5c1b5-133">-MonitorTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="5c1b5-133">-MonitorTimeoutInSeconds</span></span>
<span data-ttu-id="5c1b5-134">트래픽 관리자가이 프로필의 끝점에 상태 검사에 응답할 수 있도록 허용 하는 시간 (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="5c1b5-134">The time (in seconds) that Traffic Manager allows endpoints in this profile to respond to the health check.</span></span> <span data-ttu-id="5c1b5-135">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="5c1b5-135">The default is 10.</span></span>

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

### <span data-ttu-id="5c1b5-136">-MonitorToleratedNumberOfFailures</span><span class="sxs-lookup"><span data-stu-id="5c1b5-136">-MonitorToleratedNumberOfFailures</span></span>
<span data-ttu-id="5c1b5-137">실패 한 연속 상태 검사 수는이 프로필의 끝점을 선언 하기 전에 트래픽 관리자 tolerates에서 다음 번의 연속 되지 않은 상태 검사 후에 성능이 저하 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5c1b5-137">The number of consecutive failed health checks that Traffic Manager tolerates before declaring an endpoint in this profile Degraded after the next consecutive failed health check.</span></span> <span data-ttu-id="5c1b5-138">기본값은 3입니다.</span><span class="sxs-lookup"><span data-stu-id="5c1b5-138">The default is 3.</span></span>

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

### <span data-ttu-id="5c1b5-139">-이름</span><span class="sxs-lookup"><span data-stu-id="5c1b5-139">-Name</span></span>
<span data-ttu-id="5c1b5-140">이 cmdlet이 만드는 Traffic Manager 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c1b5-140">Specifies a name for the Traffic Manager profile that this cmdlet creates.</span></span>

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

### <span data-ttu-id="5c1b5-141">-ProfileStatus</span><span class="sxs-lookup"><span data-stu-id="5c1b5-141">-ProfileStatus</span></span>
<span data-ttu-id="5c1b5-142">프로필의 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c1b5-142">Specifies the status of the profile.</span></span>
<span data-ttu-id="5c1b5-143">유효한 값은 사용 및 사용 안 함입니다.</span><span class="sxs-lookup"><span data-stu-id="5c1b5-143">Valid values are: Enabled and Disabled.</span></span>

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

### <span data-ttu-id="5c1b5-144">-RelativeDnsName</span><span class="sxs-lookup"><span data-stu-id="5c1b5-144">-RelativeDnsName</span></span>
<span data-ttu-id="5c1b5-145">이 트래픽 관리자 프로필이 제공 하는 상대 DNS 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c1b5-145">Specifies the relative DNS name that this Traffic Manager profile provides.</span></span>
<span data-ttu-id="5c1b5-146">Traffic Manager는 Azure 트래픽 관리자가 프로필의 FQDN (정규화 된 도메인 이름)을 형성 하는 데 사용 하는 DNS 도메인 이름 및이 값을 결합 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c1b5-146">Traffic Manager combines this value and the DNS domain name that Azure Traffic Manager uses to form the fully qualified domain name (FQDN) of the profile.</span></span>

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

### <span data-ttu-id="5c1b5-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c1b5-147">-ResourceGroupName</span></span>
<span data-ttu-id="5c1b5-148">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c1b5-148">Specifies the name of a resource group.</span></span>
<span data-ttu-id="5c1b5-149">이 cmdlet은이 매개 변수에서 지정 하는 그룹에 Traffic Manager 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5c1b5-149">This cmdlet creates a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="5c1b5-150">태그</span><span class="sxs-lookup"><span data-stu-id="5c1b5-150">-Tag</span></span>
<span data-ttu-id="5c1b5-151">서버에서 태그로 설정 된 해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="5c1b5-151">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="5c1b5-152">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="5c1b5-152">For example:</span></span>

<span data-ttu-id="5c1b5-153">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="5c1b5-153">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="5c1b5-154">-TrafficRoutingMethod</span><span class="sxs-lookup"><span data-stu-id="5c1b5-154">-TrafficRoutingMethod</span></span>
<span data-ttu-id="5c1b5-155">트래픽 라우팅 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c1b5-155">Specifies the traffic routing method.</span></span>
<span data-ttu-id="5c1b5-156">이 메서드는 들어오는 DNS 쿼리에 대 한 응답으로 반환 되는 끝점 트래픽 관리자를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c1b5-156">This method determines which endpoint Traffic Manager returns in response to incoming DNS queries.</span></span>
<span data-ttu-id="5c1b5-157">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="5c1b5-157">Valid values are:</span></span>

- <span data-ttu-id="5c1b5-158">성능을</span><span class="sxs-lookup"><span data-stu-id="5c1b5-158">Performance</span></span>
- <span data-ttu-id="5c1b5-159">중</span><span class="sxs-lookup"><span data-stu-id="5c1b5-159">Weighted</span></span>
- <span data-ttu-id="5c1b5-160">중요도</span><span class="sxs-lookup"><span data-stu-id="5c1b5-160">Priority</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Performance, Weighted, Priority, Geographic

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c1b5-161">-Ttl</span><span class="sxs-lookup"><span data-stu-id="5c1b5-161">-Ttl</span></span>
<span data-ttu-id="5c1b5-162">TTL (Time to Live) 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c1b5-162">Specifies the DNS Time to Live (TTL) value.</span></span>

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

### <span data-ttu-id="5c1b5-163">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c1b5-163">-DefaultProfile</span></span>
<span data-ttu-id="5c1b5-164">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5c1b5-164">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c1b5-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c1b5-165">CommonParameters</span></span>
<span data-ttu-id="5c1b5-166">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c1b5-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c1b5-167">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c1b5-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c1b5-168">입력</span><span class="sxs-lookup"><span data-stu-id="5c1b5-168">INPUTS</span></span>

## <span data-ttu-id="5c1b5-169">출력</span><span class="sxs-lookup"><span data-stu-id="5c1b5-169">OUTPUTS</span></span>

### <span data-ttu-id="5c1b5-170">TrafficManagerProfile (Network.)</span><span class="sxs-lookup"><span data-stu-id="5c1b5-170">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="5c1b5-171">이 cmdlet은 새 TrafficManagerProfile 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c1b5-171">This cmdlet returns a new TrafficManagerProfile object.</span></span>

## <span data-ttu-id="5c1b5-172">상속자</span><span class="sxs-lookup"><span data-stu-id="5c1b5-172">NOTES</span></span>

## <span data-ttu-id="5c1b5-173">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5c1b5-173">RELATED LINKS</span></span>

[<span data-ttu-id="5c1b5-174">추가-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="5c1b5-174">Add-AzureRmTrafficManagerEndpointConfig</span></span>](./Add-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="5c1b5-175">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5c1b5-175">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="5c1b5-176">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5c1b5-176">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="5c1b5-177">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5c1b5-177">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="5c1b5-178">제거-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5c1b5-178">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="5c1b5-179">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="5c1b5-179">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


