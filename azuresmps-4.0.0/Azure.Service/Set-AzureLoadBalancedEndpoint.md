---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7259C717-250C-454A-B0DF-738B70747FF8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 298633bbc95bfb13ae340dea242c6c04267d479e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045953"
---
# <span data-ttu-id="a16e7-101">Set-AzureLoadBalancedEndpoint</span><span class="sxs-lookup"><span data-stu-id="a16e7-101">Set-AzureLoadBalancedEndpoint</span></span>

## <span data-ttu-id="a16e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a16e7-102">SYNOPSIS</span></span>
<span data-ttu-id="a16e7-103">Azure 서비스 내의 부하 분산 장치 집합에 있는 모든 끝점을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a16e7-103">Modifies all of the endpoints in a load balancer set within an Azure service.</span></span>

## <span data-ttu-id="a16e7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a16e7-104">SYNTAX</span></span>

### <span data-ttu-id="a16e7-105">DefaultProbe (기본값)</span><span class="sxs-lookup"><span data-stu-id="a16e7-105">DefaultProbe (Default)</span></span>
```
Set-AzureLoadBalancedEndpoint -LBSetName <String> [-Protocol <String>] [-LocalPort <Int32>]
 [-PublicPort <Int32>] [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="a16e7-106">TCPProbe</span><span class="sxs-lookup"><span data-stu-id="a16e7-106">TCPProbe</span></span>
```
Set-AzureLoadBalancedEndpoint -LBSetName <String> [-Protocol <String>] [-LocalPort <Int32>]
 [-PublicPort <Int32>] [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] [-ProbeProtocolTCP]
 [-ProbePort <Int32>] [-ProbeIntervalInSeconds <Int32>] [-ProbeTimeoutInSeconds <Int32>]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="a16e7-107">HTTPProbe</span><span class="sxs-lookup"><span data-stu-id="a16e7-107">HTTPProbe</span></span>
```
Set-AzureLoadBalancedEndpoint -LBSetName <String> [-Protocol <String>] [-LocalPort <Int32>]
 [-PublicPort <Int32>] [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] [-ProbeProtocolHTTP]
 -ProbePath <String> [-ProbePort <Int32>] [-ProbeIntervalInSeconds <Int32>] [-ProbeTimeoutInSeconds <Int32>]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a16e7-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a16e7-108">DESCRIPTION</span></span>
<span data-ttu-id="a16e7-109">**AzureLoadBalancedEndpoint** Cmdlet은 Azure 서비스의 부하 분산 집합에 있는 모든 끝점을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a16e7-109">The **Set-AzureLoadBalancedEndpoint** cmdlet modifies all of the endpoints in a load balancer set in an Azure service.</span></span>

## <span data-ttu-id="a16e7-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a16e7-110">EXAMPLES</span></span>

### <span data-ttu-id="a16e7-111">예제 1: 부하 분산 장치 집합의 끝점 수정</span><span class="sxs-lookup"><span data-stu-id="a16e7-111">Example 1: Modify the endpoints in a load balancer set</span></span>
```
PS C:\> Set-AzureLoadBalancedEndpoint -ServiceName "ContosoService" -LBSetName "LBSet01" -Protocol "TCP" -LocalPort 80 -ProbeProtocolTCP -ProbePort 8080
```

<span data-ttu-id="a16e7-112">이 명령은 LBSet01 이라는 부하 분산 장치 집합의 모든 끝점을 수정 하 여 TCP 프로토콜 및 개인 포트 80를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a16e7-112">This command modifies all endpoints in the load balancer set named LBSet01 to use the TCP protocol and private port 80.</span></span>
<span data-ttu-id="a16e7-113">명령에서 포트 8080의 TCP 프로토콜을 사용 하도록 부하 분산 장치 검색을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a16e7-113">The command sets the load balancer probe to use the TCP protocol on port 8080.</span></span>

### <span data-ttu-id="a16e7-114">예제 2: 다른 가상 IP 지정</span><span class="sxs-lookup"><span data-stu-id="a16e7-114">Example 2: Specify a different virtual IP</span></span>
```
PS C:\> Set-AzureLoadBalancedEndpoint -ServiceName "ContosoService" -LBSetName "LBSet02" -VirtualIPName "Vip01"
```

<span data-ttu-id="a16e7-115">이 명령은 부하 분산 장치 집합 이름을 가진 부하 분산을 수정 하 여 Vip01 이라는 가상 IP를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a16e7-115">This command modifies the load balancer that has the load balancer set name to use a virtual IP named Vip01.</span></span>

## <span data-ttu-id="a16e7-116">변수</span><span class="sxs-lookup"><span data-stu-id="a16e7-116">PARAMETERS</span></span>

### <span data-ttu-id="a16e7-117">-ACL</span><span class="sxs-lookup"><span data-stu-id="a16e7-117">-ACL</span></span>
<span data-ttu-id="a16e7-118">이 cmdlet이 끝점에 적용 하는 ACL (액세스 제어 목록) 구성 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a16e7-118">Specifies an access control list (ACL) configuration object that this cmdlet applies to the endpoints.</span></span>

```yaml
Type: NetworkAclObject
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a16e7-119">-DirectServerReturn</span><span class="sxs-lookup"><span data-stu-id="a16e7-119">-DirectServerReturn</span></span>
<span data-ttu-id="a16e7-120">이 cmdlet이 직접 서버 반환을 사용할 수 있는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a16e7-120">Specifies whether this cmdlet enables direct server return.</span></span>
<span data-ttu-id="a16e7-121">사용할 $True를 지정 하거나 사용 하지 않을 $False.</span><span class="sxs-lookup"><span data-stu-id="a16e7-121">Specify $True to enable, or $False to disable.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a16e7-122">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="a16e7-122">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="a16e7-123">끝점에 대 한 TCP 유휴 시간 제한 기간 (분)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a16e7-123">Specifies the TCP idle time-out period, in minutes, for the endpoints.</span></span>

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

### <span data-ttu-id="a16e7-124">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="a16e7-124">-InformationAction</span></span>
<span data-ttu-id="a16e7-125">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a16e7-125">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a16e7-126">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a16e7-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a16e7-127">하기로</span><span class="sxs-lookup"><span data-stu-id="a16e7-127">Continue</span></span>
- <span data-ttu-id="a16e7-128">숨기기</span><span class="sxs-lookup"><span data-stu-id="a16e7-128">Ignore</span></span>
- <span data-ttu-id="a16e7-129">Inquire</span><span class="sxs-lookup"><span data-stu-id="a16e7-129">Inquire</span></span>
- <span data-ttu-id="a16e7-130">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="a16e7-130">SilentlyContinue</span></span>
- <span data-ttu-id="a16e7-131">중지가</span><span class="sxs-lookup"><span data-stu-id="a16e7-131">Stop</span></span>
- <span data-ttu-id="a16e7-132">대기</span><span class="sxs-lookup"><span data-stu-id="a16e7-132">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a16e7-133">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="a16e7-133">-InformationVariable</span></span>
<span data-ttu-id="a16e7-134">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a16e7-134">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a16e7-135">-InternalLoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="a16e7-135">-InternalLoadBalancerName</span></span>
<span data-ttu-id="a16e7-136">이 cmdlet가 구성에 포함 하는 내부 부하 분산의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a16e7-136">Specifies the name of the internal load balancer that this cmdlet includes in the configuration.</span></span>

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

### <span data-ttu-id="a16e7-137">-LBSetName</span><span class="sxs-lookup"><span data-stu-id="a16e7-137">-LBSetName</span></span>
<span data-ttu-id="a16e7-138">이 cmdlet이 업데이트 하는 부하 분산 장치 집합의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a16e7-138">Specifies the name of the load balancer set that this cmdlet updates.</span></span>

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

### <span data-ttu-id="a16e7-139">-LoadBalancerDistribution</span><span class="sxs-lookup"><span data-stu-id="a16e7-139">-LoadBalancerDistribution</span></span>
<span data-ttu-id="a16e7-140">부하 분산 장치 배포 알고리즘을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a16e7-140">Specifies the load balancer distribution algorithm.</span></span>
<span data-ttu-id="a16e7-141">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a16e7-141">Valid values are:</span></span> 

- <span data-ttu-id="a16e7-142">sourceIP.</span><span class="sxs-lookup"><span data-stu-id="a16e7-142">sourceIP.</span></span>
<span data-ttu-id="a16e7-143">두 가지 튜플 선호도: 원본 IP, 대상 IP</span><span class="sxs-lookup"><span data-stu-id="a16e7-143">A two tuple affinity: Source IP, Destination IP</span></span> 
- <span data-ttu-id="a16e7-144">sourceIPProtocol.</span><span class="sxs-lookup"><span data-stu-id="a16e7-144">sourceIPProtocol.</span></span>
<span data-ttu-id="a16e7-145">세 가지 튜플 선호도: 원본 IP, 대상 IP, 프로토콜</span><span class="sxs-lookup"><span data-stu-id="a16e7-145">A three tuple affinity: Source IP, Destination IP, Protocol</span></span> 
- <span data-ttu-id="a16e7-146">않아야.</span><span class="sxs-lookup"><span data-stu-id="a16e7-146">none.</span></span>
<span data-ttu-id="a16e7-147">5 개의 튜플 선호도: 원본 IP, 원본 포트, 대상 IP, 대상 포트, 프로토콜</span><span class="sxs-lookup"><span data-stu-id="a16e7-147">A five tuple affinity: Source IP, Source Port, Destination IP, Destination Port, Protocol</span></span> 

<span data-ttu-id="a16e7-148">기본값은 없음입니다.</span><span class="sxs-lookup"><span data-stu-id="a16e7-148">The default value is none.</span></span>

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

### <span data-ttu-id="a16e7-149">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="a16e7-149">-LocalPort</span></span>
<span data-ttu-id="a16e7-150">이러한 끝점에서 사용 하는 로컬, 개인 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a16e7-150">Specifies the local, private, port that these endpoints use.</span></span>
<span data-ttu-id="a16e7-151">가상 컴퓨터의 응용 프로그램은이 끝점에 대 한 서비스 입력 요청에 대해이 포트에서 수신 대기 합니다.</span><span class="sxs-lookup"><span data-stu-id="a16e7-151">Applications in the virtual machine listen on this port for service input requests for this endpoint.</span></span>

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

### <span data-ttu-id="a16e7-152">-ProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="a16e7-152">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="a16e7-153">끝점에 대 한 프로브 폴링 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a16e7-153">Specifies the probe polling interval, in seconds, for the endpoints.</span></span>

```yaml
Type: Int32
Parameter Sets: TCPProbe, HTTPProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a16e7-154">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="a16e7-154">-ProbePath</span></span>
<span data-ttu-id="a16e7-155">HTTP 프로브의 상대 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a16e7-155">Specifies the relative path of the HTTP Probe.</span></span>

```yaml
Type: String
Parameter Sets: HTTPProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a16e7-156">-ProbePort</span><span class="sxs-lookup"><span data-stu-id="a16e7-156">-ProbePort</span></span>
<span data-ttu-id="a16e7-157">부하 분산 장치 검색에 사용 되는 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a16e7-157">Specifies the port that the load balancer probe uses.</span></span>

```yaml
Type: Int32
Parameter Sets: TCPProbe, HTTPProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a16e7-158">-ProbeProtocolHTTP</span><span class="sxs-lookup"><span data-stu-id="a16e7-158">-ProbeProtocolHTTP</span></span>
<span data-ttu-id="a16e7-159">부하 분산 장치 끝점에서 HTTP 프로브를 사용 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a16e7-159">Specifies that the load balancer endpoints use an HTTP Probe.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: HTTPProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a16e7-160">-ProbeProtocolTCP</span><span class="sxs-lookup"><span data-stu-id="a16e7-160">-ProbeProtocolTCP</span></span>
<span data-ttu-id="a16e7-161">부하 분산 장치 끝점에서 TCP 프로브를 사용 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a16e7-161">Specifies that the load balancer endpoints use a TCP Probe.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: TCPProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a16e7-162">-ProbeTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="a16e7-162">-ProbeTimeoutInSeconds</span></span>
<span data-ttu-id="a16e7-163">프로브 폴링 제한 시간 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a16e7-163">Specifies the probe polling time-out in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: TCPProbe, HTTPProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a16e7-164">-프로필</span><span class="sxs-lookup"><span data-stu-id="a16e7-164">-Profile</span></span>
<span data-ttu-id="a16e7-165">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a16e7-165">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a16e7-166">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="a16e7-166">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a16e7-167">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="a16e7-167">-Protocol</span></span>
<span data-ttu-id="a16e7-168">끝점의 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a16e7-168">Specifies the protocol of the endpoints.</span></span>
<span data-ttu-id="a16e7-169">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="a16e7-169">Valid values are:</span></span> 

- <span data-ttu-id="a16e7-170">NET.TCP</span><span class="sxs-lookup"><span data-stu-id="a16e7-170">TCP</span></span> 
- <span data-ttu-id="a16e7-171">UDP</span><span class="sxs-lookup"><span data-stu-id="a16e7-171">UDP</span></span>

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

### <span data-ttu-id="a16e7-172">-PublicPort</span><span class="sxs-lookup"><span data-stu-id="a16e7-172">-PublicPort</span></span>
<span data-ttu-id="a16e7-173">끝점에서 사용 하는 공용 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a16e7-173">Specifies the public port that the endpoint uses.</span></span>
<span data-ttu-id="a16e7-174">값을 지정 하지 않으면 Azure에서 사용 가능한 포트를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="a16e7-174">If you do not specify a value, Azure assigns an available port.</span></span>

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

### <span data-ttu-id="a16e7-175">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a16e7-175">-ServiceName</span></span>
<span data-ttu-id="a16e7-176">이 cmdlet이 수정 하는 끝점을 포함 하는 Azure 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a16e7-176">Specifies the name of the Azure service that contains the endpoints that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a16e7-177">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="a16e7-177">-VirtualIPName</span></span>
<span data-ttu-id="a16e7-178">Azure가 끝점에 연결 하는 가상 IP 주소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a16e7-178">Specifies the name of a virtual IP address that Azure associates to the endpoints.</span></span>
<span data-ttu-id="a16e7-179">서비스에 가상 Ip를 추가 하려면 **추가-AzureVirtualIP** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a16e7-179">To add virtual IPs to your service, use the **Add-AzureVirtualIP** cmdlet.</span></span>

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

### <span data-ttu-id="a16e7-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a16e7-180">CommonParameters</span></span>
<span data-ttu-id="a16e7-181">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a16e7-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a16e7-182">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a16e7-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a16e7-183">입력</span><span class="sxs-lookup"><span data-stu-id="a16e7-183">INPUTS</span></span>

## <span data-ttu-id="a16e7-184">출력</span><span class="sxs-lookup"><span data-stu-id="a16e7-184">OUTPUTS</span></span>

## <span data-ttu-id="a16e7-185">상속자</span><span class="sxs-lookup"><span data-stu-id="a16e7-185">NOTES</span></span>

## <span data-ttu-id="a16e7-186">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a16e7-186">RELATED LINKS</span></span>

[<span data-ttu-id="a16e7-187">추가-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="a16e7-187">Add-AzureVirtualIP</span></span>](./Add-AzureVirtualIP.md)

[<span data-ttu-id="a16e7-188">Set-AzureInternalLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="a16e7-188">Set-AzureInternalLoadBalancer</span></span>](./Set-AzureInternalLoadBalancer.md)


