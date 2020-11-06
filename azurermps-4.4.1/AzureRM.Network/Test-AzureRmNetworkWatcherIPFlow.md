---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherIPFlow.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Test-AzureRmNetworkWatcherIPFlow.md
ms.openlocfilehash: 6e9700f91a9d6f8db5983604a0146f9d864dafd8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537139"
---
# <span data-ttu-id="5280f-101">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="5280f-101">Test-AzureRmNetworkWatcherIPFlow</span></span>

## <span data-ttu-id="5280f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5280f-102">SYNOPSIS</span></span>
<span data-ttu-id="5280f-103">특정 대상에서 패킷을 허용 또는 거부 하는지 여부를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="5280f-103">Returns whether the packet is allowed or denied to or from a particular destination.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5280f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5280f-104">SYNTAX</span></span>

### <span data-ttu-id="5280f-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="5280f-105">SetByResource (Default)</span></span>
```
Test-AzureRmNetworkWatcherIPFlow -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -Direction <String> -Protocol <String> -RemoteIPAddress <String> -LocalIPAddress <String> -LocalPort <String>
 [-RemotePort <String>] [-TargetNetworkInterfaceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5280f-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="5280f-106">SetByName</span></span>
```
Test-AzureRmNetworkWatcherIPFlow -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -Direction <String> -Protocol <String> -RemoteIPAddress <String>
 -LocalIPAddress <String> -LocalPort <String> [-RemotePort <String>] [-TargetNetworkInterfaceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5280f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="5280f-107">DESCRIPTION</span></span>
<span data-ttu-id="5280f-108">지정 된 VM 리소스와 로컬 및 원격 IP 주소 및 포트를 사용 하는 지정 된 방향의 패킷에 대 한 Test-AzureRmNetworkWatcherIPFlow cmdlet은 패킷이 허용 되는지 거부 되는지를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="5280f-108">The Test-AzureRmNetworkWatcherIPFlow cmdlet, for a specified VM resource and a packet with specified direction using local and remote, IP addresses and ports, returns whether the packet is allowed or denied.</span></span>

## <span data-ttu-id="5280f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="5280f-109">EXAMPLES</span></span>

### <span data-ttu-id="5280f-110">---예제 1: Test-AzureRmNetworkWatcherIPFlow---실행</span><span class="sxs-lookup"><span data-stu-id="5280f-110">--- Example 1: Run Test-AzureRmNetworkWatcherIPFlow ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName testResourceGroup -Name VM0 
$Nics = Get-AzureRmNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}

Test-AzureRmNetworkWatcherIPFlow -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -Direction Outbound -Protocol TCP -LocalIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress -LocalPort 6895 -RemoteIPAddress 204.79.197.200 -RemotePort 80
```

<span data-ttu-id="5280f-111">이 플랜에 대 한 서쪽 중앙 US의 네트워크 감시자를 다운로드 한 다음 VM과 연결 된 네트워크 인터페이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5280f-111">Get's the Network Watcher in West Central US for this subscription, then gets the VM and it's associated Network Interfaces.</span></span> <span data-ttu-id="5280f-112">그런 다음 첫 번째 네트워크 인터페이스에 대해 첫 번째 네트워크 인터페이스에서 인터넷 IP에 대 한 아웃 바운드 연결의 첫 번째 IP를 사용 하 여 Test-AzureRmNetworkWatcherIPFlow를 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="5280f-112">Then for the first Network Interface, runs Test-AzureRmNetworkWatcherIPFlow using the first IP from the first Network Interface for an outbound connection to an IP on the internet.</span></span>

## <span data-ttu-id="5280f-113">변수</span><span class="sxs-lookup"><span data-stu-id="5280f-113">PARAMETERS</span></span>

### <span data-ttu-id="5280f-114">방향</span><span class="sxs-lookup"><span data-stu-id="5280f-114">-Direction</span></span>
<span data-ttu-id="5280f-115">지침.</span><span class="sxs-lookup"><span data-stu-id="5280f-115">Direction.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Inbound, Outbound

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5280f-116">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="5280f-116">-LocalIPAddress</span></span>
<span data-ttu-id="5280f-117">로컬 IP 주소</span><span class="sxs-lookup"><span data-stu-id="5280f-117">Local IP Address.</span></span>

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

### <span data-ttu-id="5280f-118">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="5280f-118">-LocalPort</span></span>
<span data-ttu-id="5280f-119">로컬 포트.</span><span class="sxs-lookup"><span data-stu-id="5280f-119">Local Port.</span></span>

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

### <span data-ttu-id="5280f-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5280f-120">-NetworkWatcher</span></span>
<span data-ttu-id="5280f-121">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="5280f-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="5280f-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="5280f-122">-NetworkWatcherName</span></span>
<span data-ttu-id="5280f-123">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5280f-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="5280f-124">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="5280f-124">-Protocol</span></span>
<span data-ttu-id="5280f-125">프로토콜별.</span><span class="sxs-lookup"><span data-stu-id="5280f-125">Protocol.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: TCP, UDP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5280f-126">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="5280f-126">-RemoteIPAddress</span></span>
<span data-ttu-id="5280f-127">원격 IP 주소</span><span class="sxs-lookup"><span data-stu-id="5280f-127">Remote IP Address.</span></span>

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

### <span data-ttu-id="5280f-128">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="5280f-128">-RemotePort</span></span>
<span data-ttu-id="5280f-129">원격 포트.</span><span class="sxs-lookup"><span data-stu-id="5280f-129">Remote port.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5280f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5280f-130">-ResourceGroupName</span></span>
<span data-ttu-id="5280f-131">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5280f-131">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="5280f-132">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="5280f-132">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="5280f-133">대상 네트워크 인터페이스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="5280f-133">Target network interface Id.</span></span>

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

### <span data-ttu-id="5280f-134">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="5280f-134">-TargetVirtualMachineId</span></span>
<span data-ttu-id="5280f-135">대상 가상 컴퓨터 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5280f-135">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="5280f-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5280f-136">-DefaultProfile</span></span>
<span data-ttu-id="5280f-137">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5280f-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5280f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5280f-138">CommonParameters</span></span>
<span data-ttu-id="5280f-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5280f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5280f-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5280f-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5280f-141">입력</span><span class="sxs-lookup"><span data-stu-id="5280f-141">INPUTS</span></span>

### <span data-ttu-id="5280f-142">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5280f-142">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="5280f-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5280f-143">System.String</span></span>

## <span data-ttu-id="5280f-144">출력</span><span class="sxs-lookup"><span data-stu-id="5280f-144">OUTPUTS</span></span>

### <span data-ttu-id="5280f-145">PSIPFlowVerifyResult에 대 한.</span><span class="sxs-lookup"><span data-stu-id="5280f-145">Microsoft.Azure.Commands.Network.Models.PSIPFlowVerifyResult</span></span>

## <span data-ttu-id="5280f-146">상속자</span><span class="sxs-lookup"><span data-stu-id="5280f-146">NOTES</span></span>
<span data-ttu-id="5280f-147">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 흐름, ip</span><span class="sxs-lookup"><span data-stu-id="5280f-147">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="5280f-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5280f-148">RELATED LINKS</span></span>

[<span data-ttu-id="5280f-149">새로운 AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5280f-149">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="5280f-150">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5280f-150">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="5280f-151">제거-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5280f-151">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="5280f-152">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="5280f-152">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="5280f-153">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="5280f-153">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="5280f-154">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="5280f-154">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="5280f-155">시작-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="5280f-155">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="5280f-156">새로운 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5280f-156">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5280f-157">새로운 AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="5280f-157">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="5280f-158">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5280f-158">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5280f-159">제거-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5280f-159">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5280f-160">중지-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5280f-160">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)
