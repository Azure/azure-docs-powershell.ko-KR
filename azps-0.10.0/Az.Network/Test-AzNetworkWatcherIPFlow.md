---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/test-aznetworkwatcheripflow
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Test-AzNetworkWatcherIPFlow.md
ms.openlocfilehash: 307bb2c954526b744f31763f0d3a09d0163c8057
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876517"
---
# <span data-ttu-id="a0f33-101">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="a0f33-101">Test-AzNetworkWatcherIPFlow</span></span>

## <span data-ttu-id="a0f33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0f33-102">SYNOPSIS</span></span>
<span data-ttu-id="a0f33-103">특정 대상에서 패킷을 허용 또는 거부 하는지 여부를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0f33-103">Returns whether the packet is allowed or denied to or from a particular destination.</span></span>

## <span data-ttu-id="a0f33-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a0f33-104">SYNTAX</span></span>

### <span data-ttu-id="a0f33-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="a0f33-105">SetByResource (Default)</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -Direction <String> -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0f33-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="a0f33-106">SetByName</span></span>
```
Test-AzNetworkWatcherIPFlow -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -Direction <String> -Protocol <String> -RemoteIPAddress <String>
 -LocalIPAddress <String> -LocalPort <String> [-RemotePort <String>] [-TargetNetworkInterfaceId <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0f33-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a0f33-107">DESCRIPTION</span></span>
<span data-ttu-id="a0f33-108">지정 된 VM 리소스와 로컬 및 원격 IP 주소 및 포트를 사용 하는 지정 된 방향의 패킷에 대 한 Test-AzNetworkWatcherIPFlow cmdlet은 패킷이 허용 되는지 거부 되는지를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0f33-108">The Test-AzNetworkWatcherIPFlow cmdlet, for a specified VM resource and a packet with specified direction using local and remote, IP addresses and ports, returns whether the packet is allowed or denied.</span></span>

## <span data-ttu-id="a0f33-109">예제의</span><span class="sxs-lookup"><span data-stu-id="a0f33-109">EXAMPLES</span></span>

### <span data-ttu-id="a0f33-110">---예제 1: Test-AzNetworkWatcherIPFlow---실행</span><span class="sxs-lookup"><span data-stu-id="a0f33-110">--- Example 1: Run Test-AzNetworkWatcherIPFlow ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName testResourceGroup -Name VM0 
$Nics = Get-AzNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}

Test-AzNetworkWatcherIPFlow -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -Direction Outbound -Protocol TCP -LocalIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress -LocalPort 6895 -RemoteIPAddress 204.79.197.200 -RemotePort 80
```

<span data-ttu-id="a0f33-111">이 플랜에 대 한 서쪽 중앙 US의 네트워크 감시자를 다운로드 한 다음 VM과 연결 된 네트워크 인터페이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a0f33-111">Get's the Network Watcher in West Central US for this subscription, then gets the VM and it's associated Network Interfaces.</span></span> <span data-ttu-id="a0f33-112">그런 다음 첫 번째 네트워크 인터페이스에 대해 첫 번째 네트워크 인터페이스에서 인터넷 IP에 대 한 아웃 바운드 연결의 첫 번째 IP를 사용 하 여 Test-AzNetworkWatcherIPFlow를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0f33-112">Then for the first Network Interface, runs Test-AzNetworkWatcherIPFlow using the first IP from the first Network Interface for an outbound connection to an IP on the internet.</span></span>

## <span data-ttu-id="a0f33-113">변수</span><span class="sxs-lookup"><span data-stu-id="a0f33-113">PARAMETERS</span></span>

### <span data-ttu-id="a0f33-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a0f33-114">-AsJob</span></span>
<span data-ttu-id="a0f33-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="a0f33-115">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0f33-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0f33-116">-DefaultProfile</span></span>
<span data-ttu-id="a0f33-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a0f33-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a0f33-118">방향</span><span class="sxs-lookup"><span data-stu-id="a0f33-118">-Direction</span></span>
<span data-ttu-id="a0f33-119">지침.</span><span class="sxs-lookup"><span data-stu-id="a0f33-119">Direction.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Inbound, Outbound

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0f33-120">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="a0f33-120">-LocalIPAddress</span></span>
<span data-ttu-id="a0f33-121">로컬 IP 주소</span><span class="sxs-lookup"><span data-stu-id="a0f33-121">Local IP Address.</span></span>

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

### <span data-ttu-id="a0f33-122">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="a0f33-122">-LocalPort</span></span>
<span data-ttu-id="a0f33-123">로컬 포트.</span><span class="sxs-lookup"><span data-stu-id="a0f33-123">Local Port.</span></span>

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

### <span data-ttu-id="a0f33-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a0f33-124">-NetworkWatcher</span></span>
<span data-ttu-id="a0f33-125">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="a0f33-125">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0f33-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="a0f33-126">-NetworkWatcherName</span></span>
<span data-ttu-id="a0f33-127">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a0f33-127">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a0f33-128">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="a0f33-128">-Protocol</span></span>
<span data-ttu-id="a0f33-129">프로토콜별.</span><span class="sxs-lookup"><span data-stu-id="a0f33-129">Protocol.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: TCP, UDP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0f33-130">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="a0f33-130">-RemoteIPAddress</span></span>
<span data-ttu-id="a0f33-131">원격 IP 주소</span><span class="sxs-lookup"><span data-stu-id="a0f33-131">Remote IP Address.</span></span>

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

### <span data-ttu-id="a0f33-132">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="a0f33-132">-RemotePort</span></span>
<span data-ttu-id="a0f33-133">원격 포트.</span><span class="sxs-lookup"><span data-stu-id="a0f33-133">Remote port.</span></span>

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

### <span data-ttu-id="a0f33-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0f33-134">-ResourceGroupName</span></span>
<span data-ttu-id="a0f33-135">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a0f33-135">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0f33-136">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="a0f33-136">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="a0f33-137">대상 네트워크 인터페이스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="a0f33-137">Target network interface Id.</span></span>

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

### <span data-ttu-id="a0f33-138">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="a0f33-138">-TargetVirtualMachineId</span></span>
<span data-ttu-id="a0f33-139">대상 가상 컴퓨터 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a0f33-139">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="a0f33-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0f33-140">CommonParameters</span></span>
<span data-ttu-id="a0f33-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a0f33-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0f33-142">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0f33-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0f33-143">입력</span><span class="sxs-lookup"><span data-stu-id="a0f33-143">INPUTS</span></span>

### <span data-ttu-id="a0f33-144">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a0f33-144">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="a0f33-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a0f33-145">System.String</span></span>

## <span data-ttu-id="a0f33-146">출력</span><span class="sxs-lookup"><span data-stu-id="a0f33-146">OUTPUTS</span></span>

### <span data-ttu-id="a0f33-147">PSIPFlowVerifyResult에 대 한.</span><span class="sxs-lookup"><span data-stu-id="a0f33-147">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span></span>

## <span data-ttu-id="a0f33-148">상속자</span><span class="sxs-lookup"><span data-stu-id="a0f33-148">NOTES</span></span>
<span data-ttu-id="a0f33-149">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 흐름, ip</span><span class="sxs-lookup"><span data-stu-id="a0f33-149">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="a0f33-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a0f33-150">RELATED LINKS</span></span>

[<span data-ttu-id="a0f33-151">새로운 AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a0f33-151">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="a0f33-152">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a0f33-152">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="a0f33-153">제거-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a0f33-153">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="a0f33-154">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="a0f33-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="a0f33-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="a0f33-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="a0f33-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="a0f33-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="a0f33-157">시작-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="a0f33-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="a0f33-158">새로운 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a0f33-158">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a0f33-159">새로운 AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="a0f33-159">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="a0f33-160">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a0f33-160">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a0f33-161">제거-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a0f33-161">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a0f33-162">중지-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a0f33-162">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)
