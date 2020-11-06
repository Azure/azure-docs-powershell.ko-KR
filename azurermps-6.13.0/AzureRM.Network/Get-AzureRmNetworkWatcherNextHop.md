---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatchernexthop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherNextHop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherNextHop.md
ms.openlocfilehash: 4c6a1e179cf0c6086035488d092232e85c570637
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529548"
---
# <span data-ttu-id="a0d09-101">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="a0d09-101">Get-AzureRmNetworkWatcherNextHop</span></span>

## <span data-ttu-id="a0d09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0d09-102">SYNOPSIS</span></span>
<span data-ttu-id="a0d09-103">VM에서 다음 홉을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a0d09-103">Gets the next hop from a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0d09-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a0d09-104">SYNTAX</span></span>

### <span data-ttu-id="a0d09-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="a0d09-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0d09-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="a0d09-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0d09-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="a0d09-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherNextHop -Location <String> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0d09-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a0d09-108">DESCRIPTION</span></span>
<span data-ttu-id="a0d09-109">Get-AzureRmNetworkWatcherNextHop cmdlet은 VM에서 다음 홉을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a0d09-109">The Get-AzureRmNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="a0d09-110">다음 홉을 사용 하면 Azure 리소스의 유형, 해당 리소스의 연결 된 IP 주소, 경로를 담당 하는 라우팅 테이블 규칙이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a0d09-110">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="a0d09-111">예제의</span><span class="sxs-lookup"><span data-stu-id="a0d09-111">EXAMPLES</span></span>

### <span data-ttu-id="a0d09-112">예제 1: 인터넷 IP와 통신할 때 다음 홉 받기</span><span class="sxs-lookup"><span data-stu-id="a0d09-112">Example 1: Get the Next Hop when communicating with an Internet IP</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName ContosoResourceGroup -Name VM0
$Nics = Get-AzureRmNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}
Get-AzureRmNetworkWatcherNextHop -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -SourceIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress  -DestinationIPAddress 204.79.197.200


NextHopIpAddress NextHopType RouteTableId
---------------- ----------- ------------
                 Internet    System Route
```

<span data-ttu-id="a0d09-113">지정 된 가상 Vachine (www.bing.com)에서 기본 네트워크 인터페이스의 다음 홉을 기준으로 통신을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0d09-113">Get's the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Vachine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="a0d09-114">변수</span><span class="sxs-lookup"><span data-stu-id="a0d09-114">PARAMETERS</span></span>

### <span data-ttu-id="a0d09-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a0d09-115">-AsJob</span></span>
<span data-ttu-id="a0d09-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="a0d09-116">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0d09-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0d09-117">-DefaultProfile</span></span>
<span data-ttu-id="a0d09-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a0d09-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0d09-119">-DestinationIPAddress</span><span class="sxs-lookup"><span data-stu-id="a0d09-119">-DestinationIPAddress</span></span>
<span data-ttu-id="a0d09-120">대상 IP 주소</span><span class="sxs-lookup"><span data-stu-id="a0d09-120">Destination IP address.</span></span>

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

### <span data-ttu-id="a0d09-121">-위치</span><span class="sxs-lookup"><span data-stu-id="a0d09-121">-Location</span></span>
<span data-ttu-id="a0d09-122">네트워크 감시자의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="a0d09-122">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0d09-123">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a0d09-123">-NetworkWatcher</span></span>
<span data-ttu-id="a0d09-124">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="a0d09-124">The network watcher resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher
Parameter Sets: SetByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0d09-125">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="a0d09-125">-NetworkWatcherName</span></span>
<span data-ttu-id="a0d09-126">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a0d09-126">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0d09-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0d09-127">-ResourceGroupName</span></span>
<span data-ttu-id="a0d09-128">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a0d09-128">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0d09-129">-SourceIPAddress</span><span class="sxs-lookup"><span data-stu-id="a0d09-129">-SourceIPAddress</span></span>
<span data-ttu-id="a0d09-130">원본 IP 주소</span><span class="sxs-lookup"><span data-stu-id="a0d09-130">Source IP address.</span></span>

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

### <span data-ttu-id="a0d09-131">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="a0d09-131">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="a0d09-132">대상 네트워크 인터페이스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="a0d09-132">Target network interface Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0d09-133">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="a0d09-133">-TargetVirtualMachineId</span></span>
<span data-ttu-id="a0d09-134">대상 가상 컴퓨터 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a0d09-134">The target virtual machine ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0d09-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0d09-135">CommonParameters</span></span>
<span data-ttu-id="a0d09-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0d09-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0d09-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0d09-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0d09-138">입력</span><span class="sxs-lookup"><span data-stu-id="a0d09-138">INPUTS</span></span>

### <span data-ttu-id="a0d09-139">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a0d09-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="a0d09-140">매개 변수: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a0d09-140">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="a0d09-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a0d09-141">System.String</span></span>
<span data-ttu-id="a0d09-142">매개 변수: NetworkWatcherName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a0d09-142">Parameters: NetworkWatcherName (ByValue)</span></span>

## <span data-ttu-id="a0d09-143">출력</span><span class="sxs-lookup"><span data-stu-id="a0d09-143">OUTPUTS</span></span>

### <span data-ttu-id="a0d09-144">PSNextHopResult에 대 한.</span><span class="sxs-lookup"><span data-stu-id="a0d09-144">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="a0d09-145">상속자</span><span class="sxs-lookup"><span data-stu-id="a0d09-145">NOTES</span></span>
<span data-ttu-id="a0d09-146">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, next, 홉</span><span class="sxs-lookup"><span data-stu-id="a0d09-146">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="a0d09-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a0d09-147">RELATED LINKS</span></span>

[<span data-ttu-id="a0d09-148">새로운 AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a0d09-148">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="a0d09-149">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a0d09-149">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="a0d09-150">제거-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a0d09-150">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="a0d09-151">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="a0d09-151">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="a0d09-152">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="a0d09-152">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="a0d09-153">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="a0d09-153">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="a0d09-154">시작-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="a0d09-154">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="a0d09-155">새로운 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a0d09-155">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a0d09-156">새로운 AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="a0d09-156">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="a0d09-157">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a0d09-157">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a0d09-158">제거-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a0d09-158">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a0d09-159">중지-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a0d09-159">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a0d09-160">새로운 AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="a0d09-160">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="a0d09-161">테스트-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="a0d09-161">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="a0d09-162">테스트-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="a0d09-162">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="a0d09-163">중지-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a0d09-163">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a0d09-164">시작-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a0d09-164">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a0d09-165">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a0d09-165">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a0d09-166">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="a0d09-166">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="a0d09-167">제거-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a0d09-167">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a0d09-168">새로운 AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a0d09-168">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="a0d09-169">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="a0d09-169">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="a0d09-170">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="a0d09-170">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="a0d09-171">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="a0d09-171">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="a0d09-172">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="a0d09-172">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="a0d09-173">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="a0d09-173">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="a0d09-174">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="a0d09-174">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
