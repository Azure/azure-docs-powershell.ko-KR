---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM
ms.assetid: DE31891A-0EF7-44D7-B955-A3279D27CC21
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/new-azurermtrafficmanagerprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/New-AzureRmTrafficManagerProfile.md
ms.openlocfilehash: 896324e8d08cae69f24c195de9b44b325985c2c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529684"
---
# <span data-ttu-id="4d17f-101">New-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4d17f-101">New-AzureRmTrafficManagerProfile</span></span>

## <span data-ttu-id="4d17f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d17f-102">SYNOPSIS</span></span>
<span data-ttu-id="4d17f-103">Traffic Manager 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4d17f-103">Creates a Traffic Manager profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d17f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4d17f-104">SYNTAX</span></span>

```
New-AzureRmTrafficManagerProfile -Name <String> -ResourceGroupName <String> [-ProfileStatus <String>]
 -RelativeDnsName <String> -Ttl <UInt32> -TrafficRoutingMethod <String> -MonitorProtocol <String>
 -MonitorPort <UInt32> [-MonitorPath <String>] [-MonitorIntervalInSeconds <Int32>]
 [-MonitorTimeoutInSeconds <Int32>] [-MonitorToleratedNumberOfFailures <Int32>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d17f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4d17f-105">DESCRIPTION</span></span>
<span data-ttu-id="4d17f-106">**새 AzureRmTrafficManagerProfile** Cmdlet은 Azure Traffic Manager 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4d17f-106">The **New-AzureRmTrafficManagerProfile** cmdlet creates an Azure Traffic Manager profile.</span></span>
<span data-ttu-id="4d17f-107">*Name* 매개 변수 및 필수 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d17f-107">Specify the *Name* parameter and required settings.</span></span>
<span data-ttu-id="4d17f-108">이 cmdlet은 새 프로필을 나타내는 local 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d17f-108">This cmdlet returns a local object that represents the new profile.</span></span>

<span data-ttu-id="4d17f-109">이 cmdlet은 Traffic Manager 끝점을 구성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4d17f-109">This cmdlet does not configure Traffic Manager endpoints.</span></span>
<span data-ttu-id="4d17f-110">Add-AzureRmTrafficManagerEndpointConfig cmdlet을 사용 하 여 로컬 프로필 개체를 업데이트할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4d17f-110">You can update the local profile object by using the Add-AzureRmTrafficManagerEndpointConfig cmdlet.</span></span>
<span data-ttu-id="4d17f-111">그런 다음 Set-AzureRmTrafficManagerProfile cmdlet을 사용 하 여 Traffic Manager 변경 내용을 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d17f-111">Then upload changes to Traffic Manager by using the Set-AzureRmTrafficManagerProfile cmdlet.</span></span>
<span data-ttu-id="4d17f-112">또는 New-AzureRmTrafficManagerEndpoint cmdlet을 사용 하 여 끝점을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4d17f-112">Alternatively, you can add endpoints by using the New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="4d17f-113">예제의</span><span class="sxs-lookup"><span data-stu-id="4d17f-113">EXAMPLES</span></span>

### <span data-ttu-id="4d17f-114">예제 1: 프로필 만들기</span><span class="sxs-lookup"><span data-stu-id="4d17f-114">Example 1: Create a profile</span></span>
```
PS C:\>New-AzureRmTrafficManagerProfile -Name "ContosoProfile" -ResourceGroupName "ResourceGroup11" -ProfileStatus Enabled -TrafficRoutingMethod Performance -RelativeDnsName "contosoapp" -TTL 30 -MonitorProtocol HTTP -MonitorPort 80 -MonitorPath "/default.aspx"
```

<span data-ttu-id="4d17f-115">이 명령은 리소스 그룹 ResourceGroup11에서 ContosoProfile 이라는 Azure Traffic Manager 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4d17f-115">This command creates an Azure Traffic Manager profile named ContosoProfile in resource group ResourceGroup11.</span></span>
<span data-ttu-id="4d17f-116">DNS FQDN은 contosoapp.trafficmanager.net입니다.</span><span class="sxs-lookup"><span data-stu-id="4d17f-116">The DNS FQDN is contosoapp.trafficmanager.net.</span></span>

## <span data-ttu-id="4d17f-117">변수</span><span class="sxs-lookup"><span data-stu-id="4d17f-117">PARAMETERS</span></span>

### <span data-ttu-id="4d17f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d17f-118">-DefaultProfile</span></span>
<span data-ttu-id="4d17f-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4d17f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d17f-120">-MonitorIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="4d17f-120">-MonitorIntervalInSeconds</span></span>
<span data-ttu-id="4d17f-121">트래픽 관리자가이 프로필에서 각 끝점의 상태를 확인 하는 간격 (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="4d17f-121">The interval (in seconds) at which Traffic Manager will check the health of each endpoint in this profile.</span></span> <span data-ttu-id="4d17f-122">기본값은 30입니다.</span><span class="sxs-lookup"><span data-stu-id="4d17f-122">The default is 30.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: IntervalInSecondsForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d17f-123">-MonitorPath</span><span class="sxs-lookup"><span data-stu-id="4d17f-123">-MonitorPath</span></span>
<span data-ttu-id="4d17f-124">끝점 상태를 모니터링 하는 데 사용 되는 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d17f-124">Specifies the path that is used to monitor endpoint health.</span></span>
<span data-ttu-id="4d17f-125">끝점 도메인 이름에 상대적인 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d17f-125">Specify a value relative to the endpoint domain name.</span></span>
<span data-ttu-id="4d17f-126">이 값은 슬래시 (/)로 시작 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d17f-126">This value must begin with a slash (/).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: PathForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d17f-127">-모니터 포트</span><span class="sxs-lookup"><span data-stu-id="4d17f-127">-MonitorPort</span></span>
<span data-ttu-id="4d17f-128">끝점 상태를 모니터링 하는 데 사용 되는 TCP 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d17f-128">Specifies the TCP port that is used to monitor endpoint health.</span></span>
<span data-ttu-id="4d17f-129">유효한 값은 1부터 65535 까지의 정수입니다.</span><span class="sxs-lookup"><span data-stu-id="4d17f-129">Valid values are integers from 1 through 65535.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: PortForMonitor

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d17f-130">-모니터 프로토콜</span><span class="sxs-lookup"><span data-stu-id="4d17f-130">-MonitorProtocol</span></span>
<span data-ttu-id="4d17f-131">끝점 상태를 모니터링 하는 데 사용할 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d17f-131">Specifies the protocol to use to monitor endpoint health.</span></span>
<span data-ttu-id="4d17f-132">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4d17f-132">Valid values are:</span></span>

- <span data-ttu-id="4d17f-133">HTTP</span><span class="sxs-lookup"><span data-stu-id="4d17f-133">HTTP</span></span>
- <span data-ttu-id="4d17f-134">HTTPS</span><span class="sxs-lookup"><span data-stu-id="4d17f-134">HTTPS</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ProtocolForMonitor
Accepted values: HTTP, HTTPS, TCP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d17f-135">-MonitorTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="4d17f-135">-MonitorTimeoutInSeconds</span></span>
<span data-ttu-id="4d17f-136">트래픽 관리자가이 프로필의 끝점에 상태 검사에 응답할 수 있도록 허용 하는 시간 (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="4d17f-136">The time (in seconds) that Traffic Manager allows endpoints in this profile to respond to the health check.</span></span> <span data-ttu-id="4d17f-137">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="4d17f-137">The default is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: TimeoutInSecondsForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d17f-138">-MonitorToleratedNumberOfFailures</span><span class="sxs-lookup"><span data-stu-id="4d17f-138">-MonitorToleratedNumberOfFailures</span></span>
<span data-ttu-id="4d17f-139">실패 한 연속 상태 검사 수는이 프로필의 끝점을 선언 하기 전에 트래픽 관리자 tolerates에서 다음 번의 연속 되지 않은 상태 검사 후에 성능이 저하 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4d17f-139">The number of consecutive failed health checks that Traffic Manager tolerates before declaring an endpoint in this profile Degraded after the next consecutive failed health check.</span></span> <span data-ttu-id="4d17f-140">기본값은 3입니다.</span><span class="sxs-lookup"><span data-stu-id="4d17f-140">The default is 3.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: ToleratedNumberOfFailuresForMonitor

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d17f-141">-이름</span><span class="sxs-lookup"><span data-stu-id="4d17f-141">-Name</span></span>
<span data-ttu-id="4d17f-142">이 cmdlet이 만드는 Traffic Manager 프로필의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d17f-142">Specifies a name for the Traffic Manager profile that this cmdlet creates.</span></span>

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

### <span data-ttu-id="4d17f-143">-ProfileStatus</span><span class="sxs-lookup"><span data-stu-id="4d17f-143">-ProfileStatus</span></span>
<span data-ttu-id="4d17f-144">프로필의 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d17f-144">Specifies the status of the profile.</span></span>
<span data-ttu-id="4d17f-145">유효한 값은 사용 및 사용 안 함입니다.</span><span class="sxs-lookup"><span data-stu-id="4d17f-145">Valid values are: Enabled and Disabled.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d17f-146">-RelativeDnsName</span><span class="sxs-lookup"><span data-stu-id="4d17f-146">-RelativeDnsName</span></span>
<span data-ttu-id="4d17f-147">이 트래픽 관리자 프로필이 제공 하는 상대 DNS 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d17f-147">Specifies the relative DNS name that this Traffic Manager profile provides.</span></span>
<span data-ttu-id="4d17f-148">Traffic Manager는 Azure 트래픽 관리자가 프로필의 FQDN (정규화 된 도메인 이름)을 형성 하는 데 사용 하는 DNS 도메인 이름 및이 값을 결합 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d17f-148">Traffic Manager combines this value and the DNS domain name that Azure Traffic Manager uses to form the fully qualified domain name (FQDN) of the profile.</span></span>

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

### <span data-ttu-id="4d17f-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d17f-149">-ResourceGroupName</span></span>
<span data-ttu-id="4d17f-150">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d17f-150">Specifies the name of a resource group.</span></span>
<span data-ttu-id="4d17f-151">이 cmdlet은이 매개 변수에서 지정 하는 그룹에 Traffic Manager 프로필을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4d17f-151">This cmdlet creates a Traffic Manager profile in the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="4d17f-152">태그</span><span class="sxs-lookup"><span data-stu-id="4d17f-152">-Tag</span></span>
<span data-ttu-id="4d17f-153">서버에서 태그로 설정 된 해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="4d17f-153">Key-value pairs in the form of a hash table set as tags on the server.</span></span> <span data-ttu-id="4d17f-154">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="4d17f-154">For example:</span></span>

<span data-ttu-id="4d17f-155">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="4d17f-155">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d17f-156">-TrafficRoutingMethod</span><span class="sxs-lookup"><span data-stu-id="4d17f-156">-TrafficRoutingMethod</span></span>
<span data-ttu-id="4d17f-157">트래픽 라우팅 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d17f-157">Specifies the traffic routing method.</span></span>
<span data-ttu-id="4d17f-158">이 메서드는 들어오는 DNS 쿼리에 대 한 응답으로 반환 되는 끝점 트래픽 관리자를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d17f-158">This method determines which endpoint Traffic Manager returns in response to incoming DNS queries.</span></span>
<span data-ttu-id="4d17f-159">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4d17f-159">Valid values are:</span></span>

- <span data-ttu-id="4d17f-160">성능을</span><span class="sxs-lookup"><span data-stu-id="4d17f-160">Performance</span></span>
- <span data-ttu-id="4d17f-161">중</span><span class="sxs-lookup"><span data-stu-id="4d17f-161">Weighted</span></span>
- <span data-ttu-id="4d17f-162">중요도</span><span class="sxs-lookup"><span data-stu-id="4d17f-162">Priority</span></span>
- <span data-ttu-id="4d17f-163">지역을</span><span class="sxs-lookup"><span data-stu-id="4d17f-163">Geographic</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Performance, Weighted, Priority, Geographic

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d17f-164">-Ttl</span><span class="sxs-lookup"><span data-stu-id="4d17f-164">-Ttl</span></span>
<span data-ttu-id="4d17f-165">TTL (Time to Live) 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d17f-165">Specifies the DNS Time to Live (TTL) value.</span></span>

```yaml
Type: UInt32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d17f-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d17f-166">CommonParameters</span></span>
<span data-ttu-id="4d17f-167">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d17f-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d17f-168">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d17f-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d17f-169">입력</span><span class="sxs-lookup"><span data-stu-id="4d17f-169">INPUTS</span></span>

### <span data-ttu-id="4d17f-170">않아야</span><span class="sxs-lookup"><span data-stu-id="4d17f-170">None</span></span>
<span data-ttu-id="4d17f-171">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4d17f-171">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4d17f-172">출력</span><span class="sxs-lookup"><span data-stu-id="4d17f-172">OUTPUTS</span></span>

### <span data-ttu-id="4d17f-173">TrafficManagerProfile (Network.)</span><span class="sxs-lookup"><span data-stu-id="4d17f-173">Microsoft.Azure.Commands.Network.TrafficManagerProfile</span></span>
<span data-ttu-id="4d17f-174">이 cmdlet은 새 TrafficManagerProfile 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d17f-174">This cmdlet returns a new TrafficManagerProfile object.</span></span>

## <span data-ttu-id="4d17f-175">상속자</span><span class="sxs-lookup"><span data-stu-id="4d17f-175">NOTES</span></span>

## <span data-ttu-id="4d17f-176">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4d17f-176">RELATED LINKS</span></span>

[<span data-ttu-id="4d17f-177">추가-AzureRmTrafficManagerEndpointConfig</span><span class="sxs-lookup"><span data-stu-id="4d17f-177">Add-AzureRmTrafficManagerEndpointConfig</span></span>](./Add-AzureRmTrafficManagerEndpointConfig.md)

[<span data-ttu-id="4d17f-178">Disable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4d17f-178">Disable-AzureRmTrafficManagerProfile</span></span>](./Disable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="4d17f-179">Enable-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4d17f-179">Enable-AzureRmTrafficManagerProfile</span></span>](./Enable-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="4d17f-180">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4d17f-180">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="4d17f-181">제거-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4d17f-181">Remove-AzureRmTrafficManagerProfile</span></span>](./Remove-AzureRmTrafficManagerProfile.md)

[<span data-ttu-id="4d17f-182">Set-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4d17f-182">Set-AzureRmTrafficManagerProfile</span></span>](./Set-AzureRmTrafficManagerProfile.md)


