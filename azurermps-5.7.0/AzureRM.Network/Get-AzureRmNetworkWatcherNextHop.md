---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatchernexthop
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherNextHop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherNextHop.md
ms.openlocfilehash: 641678db33e8e7436bda103f95863aefbf31eb96
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526783"
---
# <span data-ttu-id="0e987-101">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="0e987-101">Get-AzureRmNetworkWatcherNextHop</span></span>

## <span data-ttu-id="0e987-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e987-102">SYNOPSIS</span></span>
<span data-ttu-id="0e987-103">VM에서 다음 홉을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0e987-103">Gets the next hop from a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0e987-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0e987-104">SYNTAX</span></span>

### <span data-ttu-id="0e987-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="0e987-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0e987-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="0e987-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0e987-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0e987-107">DESCRIPTION</span></span>
<span data-ttu-id="0e987-108">Get-AzureRmNetworkWatcherNextHop cmdlet은 VM에서 다음 홉을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0e987-108">The Get-AzureRmNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="0e987-109">다음 홉을 사용 하면 Azure 리소스의 유형, 해당 리소스의 연결 된 IP 주소, 경로를 담당 하는 라우팅 테이블 규칙이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0e987-109">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="0e987-110">예제의</span><span class="sxs-lookup"><span data-stu-id="0e987-110">EXAMPLES</span></span>

### <span data-ttu-id="0e987-111">--예 1: 인터넷 IP와 통신 하는 경우 다음 홉을 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="0e987-111">-- Example 1: Get the Next Hop when communicating with an Internet IP --</span></span>
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

<span data-ttu-id="0e987-112">지정 된 가상 Vachine (www.bing.com)에서 기본 네트워크 인터페이스의 다음 홉을 기준으로 통신을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e987-112">Get's the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Vachine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="0e987-113">변수</span><span class="sxs-lookup"><span data-stu-id="0e987-113">PARAMETERS</span></span>

### <span data-ttu-id="0e987-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0e987-114">-AsJob</span></span>
<span data-ttu-id="0e987-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="0e987-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0e987-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e987-116">-DefaultProfile</span></span>
<span data-ttu-id="0e987-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0e987-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0e987-118">-DestinationIPAddress</span><span class="sxs-lookup"><span data-stu-id="0e987-118">-DestinationIPAddress</span></span>
<span data-ttu-id="0e987-119">대상 IP 주소</span><span class="sxs-lookup"><span data-stu-id="0e987-119">Destination IP address.</span></span>

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

### <span data-ttu-id="0e987-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0e987-120">-NetworkWatcher</span></span>
<span data-ttu-id="0e987-121">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="0e987-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="0e987-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="0e987-122">-NetworkWatcherName</span></span>
<span data-ttu-id="0e987-123">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0e987-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="0e987-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e987-124">-ResourceGroupName</span></span>
<span data-ttu-id="0e987-125">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0e987-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="0e987-126">-SourceIPAddress</span><span class="sxs-lookup"><span data-stu-id="0e987-126">-SourceIPAddress</span></span>
<span data-ttu-id="0e987-127">원본 IP 주소</span><span class="sxs-lookup"><span data-stu-id="0e987-127">Source IP address.</span></span>

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

### <span data-ttu-id="0e987-128">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="0e987-128">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="0e987-129">대상 네트워크 인터페이스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="0e987-129">Target network interface Id.</span></span>

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

### <span data-ttu-id="0e987-130">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="0e987-130">-TargetVirtualMachineId</span></span>
<span data-ttu-id="0e987-131">대상 가상 컴퓨터 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0e987-131">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="0e987-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e987-132">CommonParameters</span></span>
<span data-ttu-id="0e987-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0e987-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e987-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0e987-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e987-135">입력</span><span class="sxs-lookup"><span data-stu-id="0e987-135">INPUTS</span></span>

### <span data-ttu-id="0e987-136">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0e987-136">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="0e987-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0e987-137">System.String</span></span>

## <span data-ttu-id="0e987-138">출력</span><span class="sxs-lookup"><span data-stu-id="0e987-138">OUTPUTS</span></span>

### <span data-ttu-id="0e987-139">PSNextHopResult에 대 한.</span><span class="sxs-lookup"><span data-stu-id="0e987-139">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="0e987-140">상속자</span><span class="sxs-lookup"><span data-stu-id="0e987-140">NOTES</span></span>
<span data-ttu-id="0e987-141">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, next, 홉</span><span class="sxs-lookup"><span data-stu-id="0e987-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="0e987-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0e987-142">RELATED LINKS</span></span>

[<span data-ttu-id="0e987-143">새로운 AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0e987-143">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="0e987-144">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0e987-144">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="0e987-145">제거-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0e987-145">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="0e987-146">테스트-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="0e987-146">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="0e987-147">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="0e987-147">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="0e987-148">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="0e987-148">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="0e987-149">시작-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="0e987-149">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="0e987-150">새로운 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0e987-150">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0e987-151">새로운 AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="0e987-151">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="0e987-152">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0e987-152">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0e987-153">제거-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0e987-153">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0e987-154">중지-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0e987-154">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

