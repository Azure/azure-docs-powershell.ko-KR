---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 8e2e7a25b2c6e2c9eaa5e53234d7c1c9c3d0fa9f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875544"
---
# <span data-ttu-id="7b9c0-101">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7b9c0-101">Get-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="7b9c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b9c0-102">SYNOPSIS</span></span>
<span data-ttu-id="7b9c0-103">패킷 캡처 리소스의 정보 및 속성 및 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7b9c0-103">Gets information and properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="7b9c0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7b9c0-104">SYNTAX</span></span>

### <span data-ttu-id="7b9c0-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="7b9c0-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> [-PacketCaptureName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b9c0-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="7b9c0-106">SetByName</span></span>
```
Get-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 [-PacketCaptureName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b9c0-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7b9c0-107">DESCRIPTION</span></span>
<span data-ttu-id="7b9c0-108">Get-AzNetworkWatcherPacketCapture는 패킷 캡처 리소스의 속성 및 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7b9c0-108">The Get-AzNetworkWatcherPacketCapture gets the properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="7b9c0-109">예제의</span><span class="sxs-lookup"><span data-stu-id="7b9c0-109">EXAMPLES</span></span>

### <span data-ttu-id="7b9c0-110">---예제 1: 여러 필터를 사용 하 여 패킷 캡처를 만들고 해당 상태를 검색---</span><span class="sxs-lookup"><span data-stu-id="7b9c0-110">--- Example 1: Create a Packet Capture with multiple filters and retrieve its status ---</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2

Get-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="7b9c0-111">이 예제에서는 여러 필터 및 시간 제한을 사용 하 여 "PacketCaptureTest" 라는 패킷 캡처를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7b9c0-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="7b9c0-112">세션이 완료 되 면 지정 된 저장소 계정에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7b9c0-112">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="7b9c0-113">그런 다음 Get-AzNetworkWatcherPacketCapture를 호출 하 여 캡처 세션의 상태를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b9c0-113">We then call Get-AzNetworkWatcherPacketCapture to retrieve the status of the capture session.</span></span> 

<span data-ttu-id="7b9c0-114">참고: 패킷 캡처를 만들려면 대상 가상 컴퓨터에 Azure 네트워크 감시자 확장을 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b9c0-114">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="7b9c0-115">변수</span><span class="sxs-lookup"><span data-stu-id="7b9c0-115">PARAMETERS</span></span>

### <span data-ttu-id="7b9c0-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7b9c0-116">-AsJob</span></span>
<span data-ttu-id="7b9c0-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7b9c0-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7b9c0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b9c0-118">-DefaultProfile</span></span>
<span data-ttu-id="7b9c0-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7b9c0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b9c0-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7b9c0-120">-NetworkWatcher</span></span>
<span data-ttu-id="7b9c0-121">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="7b9c0-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="7b9c0-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="7b9c0-122">-NetworkWatcherName</span></span>
<span data-ttu-id="7b9c0-123">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7b9c0-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="7b9c0-124">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="7b9c0-124">-PacketCaptureName</span></span>
<span data-ttu-id="7b9c0-125">패킷 캡처 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7b9c0-125">The packet capture name.</span></span>

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

### <span data-ttu-id="7b9c0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b9c0-126">-ResourceGroupName</span></span>
<span data-ttu-id="7b9c0-127">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7b9c0-127">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="7b9c0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b9c0-128">CommonParameters</span></span>
<span data-ttu-id="7b9c0-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b9c0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b9c0-130">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b9c0-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b9c0-131">입력</span><span class="sxs-lookup"><span data-stu-id="7b9c0-131">INPUTS</span></span>

### <span data-ttu-id="7b9c0-132">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7b9c0-132">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="7b9c0-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7b9c0-133">System.String</span></span>

## <span data-ttu-id="7b9c0-134">출력</span><span class="sxs-lookup"><span data-stu-id="7b9c0-134">OUTPUTS</span></span>

### <span data-ttu-id="7b9c0-135">PSGetPacketCaptureResult에 대 한.</span><span class="sxs-lookup"><span data-stu-id="7b9c0-135">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span></span>

## <span data-ttu-id="7b9c0-136">상속자</span><span class="sxs-lookup"><span data-stu-id="7b9c0-136">NOTES</span></span>
<span data-ttu-id="7b9c0-137">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 패킷, 캡처, 트래픽</span><span class="sxs-lookup"><span data-stu-id="7b9c0-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="7b9c0-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7b9c0-138">RELATED LINKS</span></span>

[<span data-ttu-id="7b9c0-139">새로운 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7b9c0-139">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7b9c0-140">새로운 AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="7b9c0-140">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="7b9c0-141">제거-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7b9c0-141">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7b9c0-142">중지-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7b9c0-142">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7b9c0-143">새로운 AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7b9c0-143">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="7b9c0-144">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7b9c0-144">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="7b9c0-145">제거-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7b9c0-145">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="7b9c0-146">테스트-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="7b9c0-146">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="7b9c0-147">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="7b9c0-147">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="7b9c0-148">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="7b9c0-148">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="7b9c0-149">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="7b9c0-149">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="7b9c0-150">시작-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="7b9c0-150">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

