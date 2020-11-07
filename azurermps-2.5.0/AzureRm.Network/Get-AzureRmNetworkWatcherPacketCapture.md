---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherpacketcapture
schema: 2.0.0
ms.openlocfilehash: aeadada7c6e2e2d7cb94a484e7ca3223e03b4426
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880690"
---
# <span data-ttu-id="65e59-101">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="65e59-101">Get-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="65e59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65e59-102">SYNOPSIS</span></span>
<span data-ttu-id="65e59-103">패킷 캡처 리소스의 정보 및 속성 및 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="65e59-103">Gets information and properties and status of a packet capture resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65e59-104">구문과</span><span class="sxs-lookup"><span data-stu-id="65e59-104">SYNTAX</span></span>

### <span data-ttu-id="65e59-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="65e59-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> [-PacketCaptureName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65e59-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="65e59-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 [-PacketCaptureName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65e59-107">설명은</span><span class="sxs-lookup"><span data-stu-id="65e59-107">DESCRIPTION</span></span>
<span data-ttu-id="65e59-108">Get-AzureRmNetworkWatcherPacketCapture는 패킷 캡처 리소스의 속성 및 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="65e59-108">The Get-AzureRmNetworkWatcherPacketCapture gets the properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="65e59-109">예제의</span><span class="sxs-lookup"><span data-stu-id="65e59-109">EXAMPLES</span></span>

### <span data-ttu-id="65e59-110">---예제 1: 여러 필터를 사용 하 여 패킷 캡처를 만들고 해당 상태를 검색---</span><span class="sxs-lookup"><span data-stu-id="65e59-110">--- Example 1: Create a Packet Capture with multiple filters and retrieve its status ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2

Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="65e59-111">이 예제에서는 여러 필터 및 시간 제한을 사용 하 여 "PacketCaptureTest" 라는 패킷 캡처를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="65e59-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="65e59-112">세션이 완료 되 면 지정 된 저장소 계정에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="65e59-112">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="65e59-113">그런 다음 Get-AzureRmNetworkWatcherPacketCapture를 호출 하 여 캡처 세션의 상태를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="65e59-113">We then call Get-AzureRmNetworkWatcherPacketCapture to retrieve the status of the capture session.</span></span> 

<span data-ttu-id="65e59-114">참고: 패킷 캡처를 만들려면 대상 가상 컴퓨터에 Azure 네트워크 감시자 확장을 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="65e59-114">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="65e59-115">변수</span><span class="sxs-lookup"><span data-stu-id="65e59-115">PARAMETERS</span></span>

### <span data-ttu-id="65e59-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="65e59-116">-AsJob</span></span>
<span data-ttu-id="65e59-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="65e59-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="65e59-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65e59-118">-DefaultProfile</span></span>
<span data-ttu-id="65e59-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="65e59-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65e59-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="65e59-120">-NetworkWatcher</span></span>
<span data-ttu-id="65e59-121">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="65e59-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="65e59-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="65e59-122">-NetworkWatcherName</span></span>
<span data-ttu-id="65e59-123">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="65e59-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="65e59-124">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="65e59-124">-PacketCaptureName</span></span>
<span data-ttu-id="65e59-125">패킷 캡처 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="65e59-125">The packet capture name.</span></span>

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

### <span data-ttu-id="65e59-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65e59-126">-ResourceGroupName</span></span>
<span data-ttu-id="65e59-127">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="65e59-127">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="65e59-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65e59-128">CommonParameters</span></span>
<span data-ttu-id="65e59-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="65e59-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65e59-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65e59-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65e59-131">입력</span><span class="sxs-lookup"><span data-stu-id="65e59-131">INPUTS</span></span>

### <span data-ttu-id="65e59-132">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="65e59-132">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="65e59-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="65e59-133">System.String</span></span>

## <span data-ttu-id="65e59-134">출력</span><span class="sxs-lookup"><span data-stu-id="65e59-134">OUTPUTS</span></span>

### <span data-ttu-id="65e59-135">PSGetPacketCaptureResult에 대 한.</span><span class="sxs-lookup"><span data-stu-id="65e59-135">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span></span>

## <span data-ttu-id="65e59-136">상속자</span><span class="sxs-lookup"><span data-stu-id="65e59-136">NOTES</span></span>
<span data-ttu-id="65e59-137">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 패킷, 캡처, 트래픽</span><span class="sxs-lookup"><span data-stu-id="65e59-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="65e59-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="65e59-138">RELATED LINKS</span></span>

[<span data-ttu-id="65e59-139">새로운 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="65e59-139">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="65e59-140">새로운 AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="65e59-140">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="65e59-141">제거-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="65e59-141">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="65e59-142">중지-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="65e59-142">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="65e59-143">새로운 AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="65e59-143">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="65e59-144">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="65e59-144">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="65e59-145">제거-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="65e59-145">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="65e59-146">테스트-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="65e59-146">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="65e59-147">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="65e59-147">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="65e59-148">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="65e59-148">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="65e59-149">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="65e59-149">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="65e59-150">시작-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="65e59-150">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

