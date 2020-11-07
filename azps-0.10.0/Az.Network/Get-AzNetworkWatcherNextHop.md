---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatchernexthop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherNextHop.md
ms.openlocfilehash: 02e24fd35fbe2e5aec5fc8b6ed73d3608d07c5b2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875546"
---
# <span data-ttu-id="87f3b-101">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="87f3b-101">Get-AzNetworkWatcherNextHop</span></span>

## <span data-ttu-id="87f3b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87f3b-102">SYNOPSIS</span></span>
<span data-ttu-id="87f3b-103">VM에서 다음 홉을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="87f3b-103">Gets the next hop from a VM.</span></span>

## <span data-ttu-id="87f3b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="87f3b-104">SYNTAX</span></span>

### <span data-ttu-id="87f3b-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="87f3b-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87f3b-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="87f3b-106">SetByName</span></span>
```
Get-AzNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87f3b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="87f3b-107">DESCRIPTION</span></span>
<span data-ttu-id="87f3b-108">Get-AzNetworkWatcherNextHop cmdlet은 VM에서 다음 홉을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="87f3b-108">The Get-AzNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="87f3b-109">다음 홉을 사용 하면 Azure 리소스의 유형, 해당 리소스의 연결 된 IP 주소, 경로를 담당 하는 라우팅 테이블 규칙이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="87f3b-109">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="87f3b-110">예제의</span><span class="sxs-lookup"><span data-stu-id="87f3b-110">EXAMPLES</span></span>

### <span data-ttu-id="87f3b-111">--예 1: 인터넷 IP와 통신 하는 경우 다음 홉을 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="87f3b-111">-- Example 1: Get the Next Hop when communicating with an Internet IP --</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzVM -ResourceGroupName ContosoResourceGroup -Name VM0
$Nics = Get-AzNetworkInterface | Where {$_.Id -eq $vm.NetworkInterfaceIDs.ForEach({$_})}
Get-AzNetworkWatcherNextHop -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id -SourceIPAddress $nics[0].IpConfigurations[0].PrivateIpAddress  -DestinationIPAddress 204.79.197.200


NextHopIpAddress NextHopType RouteTableId
---------------- ----------- ------------
                 Internet    System Route
```

<span data-ttu-id="87f3b-112">지정 된 가상 Vachine (www.bing.com)에서 기본 네트워크 인터페이스의 다음 홉을 기준으로 통신을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="87f3b-112">Get's the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Vachine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="87f3b-113">변수</span><span class="sxs-lookup"><span data-stu-id="87f3b-113">PARAMETERS</span></span>

### <span data-ttu-id="87f3b-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="87f3b-114">-AsJob</span></span>
<span data-ttu-id="87f3b-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="87f3b-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="87f3b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87f3b-116">-DefaultProfile</span></span>
<span data-ttu-id="87f3b-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="87f3b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="87f3b-118">-DestinationIPAddress</span><span class="sxs-lookup"><span data-stu-id="87f3b-118">-DestinationIPAddress</span></span>
<span data-ttu-id="87f3b-119">대상 IP 주소</span><span class="sxs-lookup"><span data-stu-id="87f3b-119">Destination IP address.</span></span>

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

### <span data-ttu-id="87f3b-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="87f3b-120">-NetworkWatcher</span></span>
<span data-ttu-id="87f3b-121">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="87f3b-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="87f3b-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="87f3b-122">-NetworkWatcherName</span></span>
<span data-ttu-id="87f3b-123">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="87f3b-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="87f3b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87f3b-124">-ResourceGroupName</span></span>
<span data-ttu-id="87f3b-125">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="87f3b-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="87f3b-126">-SourceIPAddress</span><span class="sxs-lookup"><span data-stu-id="87f3b-126">-SourceIPAddress</span></span>
<span data-ttu-id="87f3b-127">원본 IP 주소</span><span class="sxs-lookup"><span data-stu-id="87f3b-127">Source IP address.</span></span>

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

### <span data-ttu-id="87f3b-128">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="87f3b-128">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="87f3b-129">대상 네트워크 인터페이스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="87f3b-129">Target network interface Id.</span></span>

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

### <span data-ttu-id="87f3b-130">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="87f3b-130">-TargetVirtualMachineId</span></span>
<span data-ttu-id="87f3b-131">대상 가상 컴퓨터 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="87f3b-131">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="87f3b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87f3b-132">CommonParameters</span></span>
<span data-ttu-id="87f3b-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="87f3b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87f3b-134">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87f3b-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87f3b-135">입력</span><span class="sxs-lookup"><span data-stu-id="87f3b-135">INPUTS</span></span>

### <span data-ttu-id="87f3b-136">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="87f3b-136">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="87f3b-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="87f3b-137">System.String</span></span>

## <span data-ttu-id="87f3b-138">출력</span><span class="sxs-lookup"><span data-stu-id="87f3b-138">OUTPUTS</span></span>

### <span data-ttu-id="87f3b-139">PSNextHopResult에 대 한.</span><span class="sxs-lookup"><span data-stu-id="87f3b-139">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="87f3b-140">상속자</span><span class="sxs-lookup"><span data-stu-id="87f3b-140">NOTES</span></span>
<span data-ttu-id="87f3b-141">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, next, 홉</span><span class="sxs-lookup"><span data-stu-id="87f3b-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="87f3b-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="87f3b-142">RELATED LINKS</span></span>

[<span data-ttu-id="87f3b-143">새로운 AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="87f3b-143">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="87f3b-144">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="87f3b-144">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="87f3b-145">제거-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="87f3b-145">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="87f3b-146">테스트-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="87f3b-146">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="87f3b-147">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="87f3b-147">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="87f3b-148">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="87f3b-148">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="87f3b-149">시작-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="87f3b-149">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="87f3b-150">새로운 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="87f3b-150">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="87f3b-151">새로운 AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="87f3b-151">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="87f3b-152">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="87f3b-152">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="87f3b-153">제거-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="87f3b-153">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="87f3b-154">중지-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="87f3b-154">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

