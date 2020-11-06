---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherNextHop.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherNextHop.md
ms.openlocfilehash: d26f50768c561e05b4dc27ad829c063b73c5a336
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537075"
---
# <span data-ttu-id="4f0ff-101">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="4f0ff-101">Get-AzureRmNetworkWatcherNextHop</span></span>

## <span data-ttu-id="4f0ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f0ff-102">SYNOPSIS</span></span>
<span data-ttu-id="4f0ff-103">VM에서 다음 홉을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4f0ff-103">Gets the next hop from a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4f0ff-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4f0ff-104">SYNTAX</span></span>

### <span data-ttu-id="4f0ff-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="4f0ff-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 -DestinationIPAddress <String> -SourceIPAddress <String> [-TargetNetworkInterfaceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f0ff-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="4f0ff-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherNextHop -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> -DestinationIPAddress <String> -SourceIPAddress <String>
 [-TargetNetworkInterfaceId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f0ff-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4f0ff-107">DESCRIPTION</span></span>
<span data-ttu-id="4f0ff-108">Get-AzureRmNetworkWatcherNextHop cmdlet은 VM에서 다음 홉을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4f0ff-108">The Get-AzureRmNetworkWatcherNextHop cmdlet gets the next hop from a VM.</span></span> <span data-ttu-id="4f0ff-109">다음 홉을 사용 하면 Azure 리소스의 유형, 해당 리소스의 연결 된 IP 주소, 경로를 담당 하는 라우팅 테이블 규칙이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4f0ff-109">Next hop allows you to view the type of Azure resource, the associated IP address of that resource, and the routing table rule that is responsible for the route.</span></span>

## <span data-ttu-id="4f0ff-110">예제의</span><span class="sxs-lookup"><span data-stu-id="4f0ff-110">EXAMPLES</span></span>

### <span data-ttu-id="4f0ff-111">--예 1: 인터넷 IP와 통신 하는 경우 다음 홉을 확인 하세요.</span><span class="sxs-lookup"><span data-stu-id="4f0ff-111">-- Example 1: Get the Next Hop when communicating with an Internet IP --</span></span>
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

<span data-ttu-id="4f0ff-112">지정 된 가상 Vachine (www.bing.com)에서 기본 네트워크 인터페이스의 다음 홉을 기준으로 통신을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f0ff-112">Get's the Next Hop for outbound communication from the primary Network Interface on the specified Virtual Vachine to 204.79.197.200 (www.bing.com)</span></span>

## <span data-ttu-id="4f0ff-113">변수</span><span class="sxs-lookup"><span data-stu-id="4f0ff-113">PARAMETERS</span></span>

### <span data-ttu-id="4f0ff-114">-DestinationIPAddress</span><span class="sxs-lookup"><span data-stu-id="4f0ff-114">-DestinationIPAddress</span></span>
<span data-ttu-id="4f0ff-115">대상 IP 주소</span><span class="sxs-lookup"><span data-stu-id="4f0ff-115">Destination IP address.</span></span>

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

### <span data-ttu-id="4f0ff-116">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4f0ff-116">-NetworkWatcher</span></span>
<span data-ttu-id="4f0ff-117">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="4f0ff-117">The network watcher resource.</span></span>

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

### <span data-ttu-id="4f0ff-118">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="4f0ff-118">-NetworkWatcherName</span></span>
<span data-ttu-id="4f0ff-119">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4f0ff-119">The name of network watcher.</span></span>

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

### <span data-ttu-id="4f0ff-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f0ff-120">-ResourceGroupName</span></span>
<span data-ttu-id="4f0ff-121">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4f0ff-121">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="4f0ff-122">-SourceIPAddress</span><span class="sxs-lookup"><span data-stu-id="4f0ff-122">-SourceIPAddress</span></span>
<span data-ttu-id="4f0ff-123">원본 IP 주소</span><span class="sxs-lookup"><span data-stu-id="4f0ff-123">Source IP address.</span></span>

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

### <span data-ttu-id="4f0ff-124">-TargetNetworkInterfaceId</span><span class="sxs-lookup"><span data-stu-id="4f0ff-124">-TargetNetworkInterfaceId</span></span>
<span data-ttu-id="4f0ff-125">대상 네트워크 인터페이스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="4f0ff-125">Target network interface Id.</span></span>

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

### <span data-ttu-id="4f0ff-126">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="4f0ff-126">-TargetVirtualMachineId</span></span>
<span data-ttu-id="4f0ff-127">대상 가상 컴퓨터 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4f0ff-127">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="4f0ff-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f0ff-128">-DefaultProfile</span></span>
<span data-ttu-id="4f0ff-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4f0ff-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f0ff-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f0ff-130">CommonParameters</span></span>
<span data-ttu-id="4f0ff-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f0ff-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f0ff-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f0ff-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f0ff-133">입력</span><span class="sxs-lookup"><span data-stu-id="4f0ff-133">INPUTS</span></span>

### <span data-ttu-id="4f0ff-134">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4f0ff-134">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="4f0ff-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4f0ff-135">System.String</span></span>

## <span data-ttu-id="4f0ff-136">출력</span><span class="sxs-lookup"><span data-stu-id="4f0ff-136">OUTPUTS</span></span>

### <span data-ttu-id="4f0ff-137">PSNextHopResult에 대 한.</span><span class="sxs-lookup"><span data-stu-id="4f0ff-137">Microsoft.Azure.Commands.Network.Models.PSNextHopResult</span></span>

## <span data-ttu-id="4f0ff-138">상속자</span><span class="sxs-lookup"><span data-stu-id="4f0ff-138">NOTES</span></span>
<span data-ttu-id="4f0ff-139">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, next, 홉</span><span class="sxs-lookup"><span data-stu-id="4f0ff-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="4f0ff-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4f0ff-140">RELATED LINKS</span></span>

[<span data-ttu-id="4f0ff-141">새로운 AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4f0ff-141">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="4f0ff-142">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4f0ff-142">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="4f0ff-143">제거-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="4f0ff-143">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="4f0ff-144">테스트-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="4f0ff-144">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="4f0ff-145">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="4f0ff-145">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="4f0ff-146">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="4f0ff-146">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="4f0ff-147">시작-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="4f0ff-147">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="4f0ff-148">새로운 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4f0ff-148">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4f0ff-149">새로운 AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="4f0ff-149">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="4f0ff-150">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4f0ff-150">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4f0ff-151">제거-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4f0ff-151">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="4f0ff-152">중지-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="4f0ff-152">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

