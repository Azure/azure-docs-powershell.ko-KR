---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D767F017-6545-4BC6-927E-E7A99A08D5D2
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5b3122795f2af33a28206936b7b28322ad171b19
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045733"
---
# <span data-ttu-id="378d7-101">Add-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="378d7-101">Add-AzureEndpoint</span></span>

## <span data-ttu-id="378d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="378d7-102">SYNOPSIS</span></span>
<span data-ttu-id="378d7-103">끝점을 가상 컴퓨터에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="378d7-103">Adds an endpoint to a virtual machine.</span></span>

## <span data-ttu-id="378d7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="378d7-104">SYNTAX</span></span>

### <span data-ttu-id="378d7-105">NoLB (기본값)</span><span class="sxs-lookup"><span data-stu-id="378d7-105">NoLB (Default)</span></span>
```
Add-AzureEndpoint [-Name] <String> [-Protocol] <String> [-LocalPort] <Int32> [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] [-InternalLoadBalancerName <String>]
 [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>] [-VirtualIPName <String>]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="378d7-106">LBNoProbe</span><span class="sxs-lookup"><span data-stu-id="378d7-106">LBNoProbe</span></span>
```
Add-AzureEndpoint [-Name] <String> [-Protocol] <String> [-LocalPort] <Int32> [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] -LBSetName <String> [-NoProbe]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="378d7-107">LBDefaultProbe</span><span class="sxs-lookup"><span data-stu-id="378d7-107">LBDefaultProbe</span></span>
```
Add-AzureEndpoint [-Name] <String> [-Protocol] <String> [-LocalPort] <Int32> [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] -LBSetName <String> [-DefaultProbe]
 [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>] [-LoadBalancerDistribution <String>]
 [-VirtualIPName <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="378d7-108">LBCustomProbe</span><span class="sxs-lookup"><span data-stu-id="378d7-108">LBCustomProbe</span></span>
```
Add-AzureEndpoint [-Name] <String> [-Protocol] <String> [-LocalPort] <Int32> [-PublicPort <Int32>]
 [-DirectServerReturn <Boolean>] [-ACL <NetworkAclObject>] -LBSetName <String> -ProbePort <Int32>
 -ProbeProtocol <String> [-ProbePath <String>] [-ProbeIntervalInSeconds <Int32>]
 [-ProbeTimeoutInSeconds <Int32>] [-InternalLoadBalancerName <String>] [-IdleTimeoutInMinutes <Int32>]
 [-LoadBalancerDistribution <String>] [-VirtualIPName <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="378d7-109">설명은</span><span class="sxs-lookup"><span data-stu-id="378d7-109">DESCRIPTION</span></span>
<span data-ttu-id="378d7-110">**추가-AzureEndpoint** Cmdlet은 Azure 가상 컴퓨터 개체에 끝점을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="378d7-110">The **Add-AzureEndpoint** cmdlet adds an endpoint to an Azure virtual machine object.</span></span>

## <span data-ttu-id="378d7-111">예제의</span><span class="sxs-lookup"><span data-stu-id="378d7-111">EXAMPLES</span></span>

### <span data-ttu-id="378d7-112">예제 1: 끝점 추가</span><span class="sxs-lookup"><span data-stu-id="378d7-112">Example 1: Add an endpoint</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirutalMachine01" | Add-AzureEndpoint -Name "HttpIn" -Protocol "tcp" -PublicPort 80 -LocalPort 8080 | Update-AzureVM
```

<span data-ttu-id="378d7-113">이 명령은 **get-help** cmdlet을 사용 하 여 VirtualMachine01 이라는 가상 컴퓨터의 구성을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="378d7-113">This command retrieves the configuration of a virtual machine named VirtualMachine01 by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="378d7-114">이 명령은 파이프라인 연산자를 사용 하 여이를 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="378d7-114">The command passes it to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="378d7-115">이 cmdlet은 HttpIn 이라는 끝점을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="378d7-115">This cmdlet adds an endpoint named HttpIn.</span></span>
<span data-ttu-id="378d7-116">끝점에는 공용 포트 80 및 로컬 포트 8080이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="378d7-116">The endpoint has a public port 80 and local port 8080.</span></span>
<span data-ttu-id="378d7-117">이 명령은 가상 컴퓨터 개체를 **업데이트-add-azurevm** cmdlet에 전달 하 여 변경 내용을 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="378d7-117">The command passes the virtual machine object to the **Update-AzureVM** cmdlet, which implements your changes.</span></span>

### <span data-ttu-id="378d7-118">예제 2: 부하 분산 그룹에 속하는 끝점 추가</span><span class="sxs-lookup"><span data-stu-id="378d7-118">Example 2: Add an endpoint that belongs to a load balanced group</span></span>
```
PS C:\> Get-AzureVM -ServiceName "LoadBalancedService" -Name "VirtualMachine12" | Add-AzureEndpoint -Name "HttpIn" -Protocol "tcp" -PublicPort 80 -LocalPort 8080 -LBSetName "WebFarm" -ProbePort 80 -ProbeProtocol "http" -ProbePath '/' | Update-AzureVM
```

<span data-ttu-id="378d7-119">이 명령은 VirtualMachine07 이라는 가상 컴퓨터의 구성을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="378d7-119">This command retrieves the configuration of a virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="378d7-120">현재 cmdlet은 HttpIn 이라는 끝점을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="378d7-120">The current cmdlet adds an endpoint named HttpIn.</span></span>
<span data-ttu-id="378d7-121">끝점에는 공용 포트 80 및 로컬 포트 8080이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="378d7-121">The endpoint has a public port 80 and local port 8080.</span></span>
<span data-ttu-id="378d7-122">끝점은 WebFarm 이라는 공유 부하 분산 그룹에 속합니다.</span><span class="sxs-lookup"><span data-stu-id="378d7-122">The endpoint belongs to the shared load balanced group named WebFarm.</span></span>
<span data-ttu-id="378d7-123">'/' 경로를 사용 하는 포트 80에서 HTTP 프로브는 끝점의 가용성을 모니터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="378d7-123">An HTTP probe on port 80 with a path of '/' monitors the availability of the endpoint.</span></span>
<span data-ttu-id="378d7-124">명령이 변경 내용을 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="378d7-124">The command implements your changes.</span></span>

### <span data-ttu-id="378d7-125">예제 3: 끝점에 가상 IP 연결</span><span class="sxs-lookup"><span data-stu-id="378d7-125">Example 3: Associate a virtual IP to an endpoint</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ContosoService" -Name "VirtualMachine25" | Add-AzureEndpoint -Name "HttpIn" -Protocol "tcp" -LocalPort 8080 -PublicPort 80 -VirtualIPName "ContosoVip11" | Update-AzureVM
```

<span data-ttu-id="378d7-126">이 명령은 VirtualMachine25 이라는 가상 컴퓨터의 구성을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="378d7-126">This command retrieves the configuration of a virtual machine named VirtualMachine25.</span></span>
<span data-ttu-id="378d7-127">현재 cmdlet은 HttpIn 이라는 끝점을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="378d7-127">The current cmdlet adds an endpoint named HttpIn.</span></span>
<span data-ttu-id="378d7-128">끝점에는 공용 포트 80 및 로컬 포트 8080이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="378d7-128">The endpoint has a public port 80 and local port 8080.</span></span>
<span data-ttu-id="378d7-129">이 명령은 가상 IP를 끝점에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="378d7-129">This command associates a virtual IP to the endpoint.</span></span>
<span data-ttu-id="378d7-130">명령이 변경 내용을 구현 합니다.</span><span class="sxs-lookup"><span data-stu-id="378d7-130">The command implements your changes.</span></span>

## <span data-ttu-id="378d7-131">변수</span><span class="sxs-lookup"><span data-stu-id="378d7-131">PARAMETERS</span></span>

### <span data-ttu-id="378d7-132">-ACL</span><span class="sxs-lookup"><span data-stu-id="378d7-132">-ACL</span></span>
<span data-ttu-id="378d7-133">끝점에 대 한 ACL (액세스 제어 목록) 구성 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="378d7-133">Specifies an access control list (ACL) configuration object for the endpoint.</span></span>

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

### <span data-ttu-id="378d7-134">-DefaultProbe</span><span class="sxs-lookup"><span data-stu-id="378d7-134">-DefaultProbe</span></span>
<span data-ttu-id="378d7-135">이 cmdlet이 기본 프로브 설정을 사용 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="378d7-135">Indicates that this cmdlet uses the default probe setting.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LBDefaultProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="378d7-136">-DirectServerReturn</span><span class="sxs-lookup"><span data-stu-id="378d7-136">-DirectServerReturn</span></span>
<span data-ttu-id="378d7-137">이 cmdlet이 직접 서버 반환을 사용할 수 있는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="378d7-137">Specifies whether this cmdlet enables direct server return.</span></span>
<span data-ttu-id="378d7-138">사용할 $True를 지정 하거나 사용 하지 않을 $False.</span><span class="sxs-lookup"><span data-stu-id="378d7-138">Specify $True to enable, or $False to disable.</span></span>

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

### <span data-ttu-id="378d7-139">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="378d7-139">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="378d7-140">끝점에 대 한 TCP 유휴 시간 제한 기간 (분)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="378d7-140">Specifies the TCP idle time-out period, in minutes, for the endpoint.</span></span>

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

### <span data-ttu-id="378d7-141">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="378d7-141">-InformationAction</span></span>
<span data-ttu-id="378d7-142">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="378d7-142">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="378d7-143">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="378d7-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="378d7-144">하기로</span><span class="sxs-lookup"><span data-stu-id="378d7-144">Continue</span></span>
- <span data-ttu-id="378d7-145">숨기기</span><span class="sxs-lookup"><span data-stu-id="378d7-145">Ignore</span></span>
- <span data-ttu-id="378d7-146">Inquire</span><span class="sxs-lookup"><span data-stu-id="378d7-146">Inquire</span></span>
- <span data-ttu-id="378d7-147">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="378d7-147">SilentlyContinue</span></span>
- <span data-ttu-id="378d7-148">중지가</span><span class="sxs-lookup"><span data-stu-id="378d7-148">Stop</span></span>
- <span data-ttu-id="378d7-149">대기</span><span class="sxs-lookup"><span data-stu-id="378d7-149">Suspend</span></span>

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

### <span data-ttu-id="378d7-150">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="378d7-150">-InformationVariable</span></span>
<span data-ttu-id="378d7-151">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="378d7-151">Specifies an information variable.</span></span>

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

### <span data-ttu-id="378d7-152">-InternalLoadBalancerName</span><span class="sxs-lookup"><span data-stu-id="378d7-152">-InternalLoadBalancerName</span></span>
<span data-ttu-id="378d7-153">내부 부하 분산의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="378d7-153">Specifies the name of the internal load balancer.</span></span>

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

### <span data-ttu-id="378d7-154">-LBSetName</span><span class="sxs-lookup"><span data-stu-id="378d7-154">-LBSetName</span></span>
<span data-ttu-id="378d7-155">끝점에 대 한 부하 분산 장치 집합의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="378d7-155">Specifies the name of the load balancer set for the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: LBNoProbe, LBDefaultProbe, LBCustomProbe
Aliases: LoadBalancedEndpointSetName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="378d7-156">-LoadBalancerDistribution</span><span class="sxs-lookup"><span data-stu-id="378d7-156">-LoadBalancerDistribution</span></span>
<span data-ttu-id="378d7-157">부하 분산 장치 배포 알고리즘을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="378d7-157">Specifies the load balancer distribution algorithm.</span></span>
<span data-ttu-id="378d7-158">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="378d7-158">Valid values are:</span></span> 

- <span data-ttu-id="378d7-159">sourceIP.</span><span class="sxs-lookup"><span data-stu-id="378d7-159">sourceIP.</span></span>
<span data-ttu-id="378d7-160">두 가지 튜플 선호도: 원본 IP, 대상 IP</span><span class="sxs-lookup"><span data-stu-id="378d7-160">A two tuple affinity: Source IP, Destination IP</span></span> 
- <span data-ttu-id="378d7-161">sourceIPProtocol.</span><span class="sxs-lookup"><span data-stu-id="378d7-161">sourceIPProtocol.</span></span>
<span data-ttu-id="378d7-162">세 가지 튜플 선호도: 원본 IP, 대상 IP, 프로토콜</span><span class="sxs-lookup"><span data-stu-id="378d7-162">A three tuple affinity: Source IP, Destination IP, Protocol</span></span> 
- <span data-ttu-id="378d7-163">않아야.</span><span class="sxs-lookup"><span data-stu-id="378d7-163">none.</span></span>
<span data-ttu-id="378d7-164">5 개의 튜플 선호도: 원본 IP, 원본 포트, 대상 IP, 대상 포트, 프로토콜</span><span class="sxs-lookup"><span data-stu-id="378d7-164">A five tuple affinity: Source IP, Source Port, Destination IP, Destination Port, Protocol</span></span> 

<span data-ttu-id="378d7-165">기본값은 없음입니다.</span><span class="sxs-lookup"><span data-stu-id="378d7-165">The default value is none.</span></span>

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

### <span data-ttu-id="378d7-166">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="378d7-166">-LocalPort</span></span>
<span data-ttu-id="378d7-167">이 끝점에서 사용 하는 로컬, 개인 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="378d7-167">Specifies the local, private, port that this endpoint uses.</span></span>
<span data-ttu-id="378d7-168">가상 컴퓨터 내의 응용 프로그램은이 끝점에 대 한 서비스 입력 요청에 대해이 포트에서 수신 대기 합니다.</span><span class="sxs-lookup"><span data-stu-id="378d7-168">Applications within the virtual machine listen on this port for service input requests for this endpoint.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="378d7-169">-이름</span><span class="sxs-lookup"><span data-stu-id="378d7-169">-Name</span></span>
<span data-ttu-id="378d7-170">끝점의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="378d7-170">Specifies a name for the endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="378d7-171">-NoProbe</span><span class="sxs-lookup"><span data-stu-id="378d7-171">-NoProbe</span></span>
<span data-ttu-id="378d7-172">이 cmdlet이 프로브 없음 설정이 사용 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="378d7-172">Indicates that this cmdlet uses the no probe setting.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: LBNoProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="378d7-173">-ProbeIntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="378d7-173">-ProbeIntervalInSeconds</span></span>
<span data-ttu-id="378d7-174">끝점에 대 한 프로브 폴링 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="378d7-174">Specifies the probe polling interval, in seconds, for the endpoint.</span></span>

```yaml
Type: Int32
Parameter Sets: LBCustomProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="378d7-175">-ProbePath</span><span class="sxs-lookup"><span data-stu-id="378d7-175">-ProbePath</span></span>
<span data-ttu-id="378d7-176">HTTP 프로브에 대 한 상대 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="378d7-176">Specifies the relative path to the HTTP probe.</span></span>

```yaml
Type: String
Parameter Sets: LBCustomProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="378d7-177">-ProbePort</span><span class="sxs-lookup"><span data-stu-id="378d7-177">-ProbePort</span></span>
<span data-ttu-id="378d7-178">끝점에서 사용 하는 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="378d7-178">Specifies the port that the endpoint uses.</span></span>

```yaml
Type: Int32
Parameter Sets: LBCustomProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="378d7-179">-ProbeProtocol</span><span class="sxs-lookup"><span data-stu-id="378d7-179">-ProbeProtocol</span></span>
<span data-ttu-id="378d7-180">포트 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="378d7-180">Specifies the port protocol.</span></span>
<span data-ttu-id="378d7-181">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="378d7-181">Valid values are:</span></span> 

- <span data-ttu-id="378d7-182">net.tcp</span><span class="sxs-lookup"><span data-stu-id="378d7-182">tcp</span></span> 
- <span data-ttu-id="378d7-183">http</span><span class="sxs-lookup"><span data-stu-id="378d7-183">http</span></span>

```yaml
Type: String
Parameter Sets: LBCustomProbe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="378d7-184">-ProbeTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="378d7-184">-ProbeTimeoutInSeconds</span></span>
<span data-ttu-id="378d7-185">프로브 폴링 시간 종료 기간 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="378d7-185">Specifies the probe polling time-out period in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: LBCustomProbe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="378d7-186">-프로필</span><span class="sxs-lookup"><span data-stu-id="378d7-186">-Profile</span></span>
<span data-ttu-id="378d7-187">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="378d7-187">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="378d7-188">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="378d7-188">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="378d7-189">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="378d7-189">-Protocol</span></span>
<span data-ttu-id="378d7-190">끝점의 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="378d7-190">Specifies the protocol of the endpoint.</span></span>
<span data-ttu-id="378d7-191">유효한 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="378d7-191">Valid values are:</span></span> 

- <span data-ttu-id="378d7-192">net.tcp</span><span class="sxs-lookup"><span data-stu-id="378d7-192">tcp</span></span> 
- <span data-ttu-id="378d7-193">udp</span><span class="sxs-lookup"><span data-stu-id="378d7-193">udp</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="378d7-194">-PublicPort</span><span class="sxs-lookup"><span data-stu-id="378d7-194">-PublicPort</span></span>
<span data-ttu-id="378d7-195">끝점에서 사용 하는 공용 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="378d7-195">Specifies the public port that the endpoint uses.</span></span>
<span data-ttu-id="378d7-196">값을 지정 하지 않으면 Azure에서 사용 가능한 포트를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="378d7-196">If you do not specify a value, Azure assigns an available port.</span></span>

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

### <span data-ttu-id="378d7-197">-VirtualIPName</span><span class="sxs-lookup"><span data-stu-id="378d7-197">-VirtualIPName</span></span>
<span data-ttu-id="378d7-198">Azure가 끝점에 연결 하는 가상 IP 주소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="378d7-198">Specifies the name of a virtual IP address that Azure associates to the endpoint.</span></span>
<span data-ttu-id="378d7-199">서비스에 여러 개의 가상 Ip가 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="378d7-199">Your service can have multiple virtual IPs.</span></span>
<span data-ttu-id="378d7-200">가상 Ip를 만들려면 **Add-AzureVirtualIP** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="378d7-200">To create virtual IPs, use the **Add-AzureVirtualIP** cmdlet.</span></span>

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

### <span data-ttu-id="378d7-201">-VM</span><span class="sxs-lookup"><span data-stu-id="378d7-201">-VM</span></span>
<span data-ttu-id="378d7-202">끝점이 속한 가상 컴퓨터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="378d7-202">Specifies the virtual machine to which the endpoint belongs.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="378d7-203">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="378d7-203">CommonParameters</span></span>
<span data-ttu-id="378d7-204">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="378d7-204">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="378d7-205">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="378d7-205">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="378d7-206">입력</span><span class="sxs-lookup"><span data-stu-id="378d7-206">INPUTS</span></span>

## <span data-ttu-id="378d7-207">출력</span><span class="sxs-lookup"><span data-stu-id="378d7-207">OUTPUTS</span></span>

### <span data-ttu-id="378d7-208">System. 개체</span><span class="sxs-lookup"><span data-stu-id="378d7-208">System.Object</span></span>

## <span data-ttu-id="378d7-209">상속자</span><span class="sxs-lookup"><span data-stu-id="378d7-209">NOTES</span></span>

## <span data-ttu-id="378d7-210">관련 링크</span><span class="sxs-lookup"><span data-stu-id="378d7-210">RELATED LINKS</span></span>

[<span data-ttu-id="378d7-211">추가-AzureVirtualIP</span><span class="sxs-lookup"><span data-stu-id="378d7-211">Add-AzureVirtualIP</span></span>](./Add-AzureVirtualIP.md)

[<span data-ttu-id="378d7-212">Get-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="378d7-212">Get-AzureEndpoint</span></span>](./Get-AzureEndpoint.md)

[<span data-ttu-id="378d7-213">다운로드-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="378d7-213">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="378d7-214">-AzureEndpoint 제거</span><span class="sxs-lookup"><span data-stu-id="378d7-214">Remove-AzureEndpoint</span></span>](./Remove-AzureEndpoint.md)

[<span data-ttu-id="378d7-215">Set-AzureEndpoint</span><span class="sxs-lookup"><span data-stu-id="378d7-215">Set-AzureEndpoint</span></span>](./Set-AzureEndpoint.md)

[<span data-ttu-id="378d7-216">업데이트-Add-azurevm</span><span class="sxs-lookup"><span data-stu-id="378d7-216">Update-AzureVM</span></span>](./Update-AzureVM.md)


