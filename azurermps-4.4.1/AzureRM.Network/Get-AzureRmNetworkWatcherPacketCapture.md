---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: 4cf1cb9149c0f821ad0e6164cd7c817b12ccc147
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529296"
---
# <span data-ttu-id="6c1b0-101">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6c1b0-101">Get-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="6c1b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c1b0-102">SYNOPSIS</span></span>
<span data-ttu-id="6c1b0-103">패킷 캡처 리소스의 정보 및 속성 및 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6c1b0-103">Gets information and properties and status of a packet capture resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6c1b0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6c1b0-104">SYNTAX</span></span>

### <span data-ttu-id="6c1b0-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="6c1b0-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> [-PacketCaptureName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c1b0-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="6c1b0-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 [-PacketCaptureName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c1b0-107">설명은</span><span class="sxs-lookup"><span data-stu-id="6c1b0-107">DESCRIPTION</span></span>
<span data-ttu-id="6c1b0-108">Get-AzureRmNetworkWatcherPacketCapture는 패킷 캡처 리소스의 속성 및 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6c1b0-108">The Get-AzureRmNetworkWatcherPacketCapture gets the properties and status of a packet capture resource.</span></span>

## <span data-ttu-id="6c1b0-109">예제의</span><span class="sxs-lookup"><span data-stu-id="6c1b0-109">EXAMPLES</span></span>

### <span data-ttu-id="6c1b0-110">---예제 1: 여러 필터를 사용 하 여 패킷 캡처를 만들고 해당 상태를 검색---</span><span class="sxs-lookup"><span data-stu-id="6c1b0-110">--- Example 1: Create a Packet Capture with multiple filters and retrieve its status ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2

Get-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="6c1b0-111">이 예제에서는 여러 필터 및 시간 제한을 사용 하 여 "PacketCaptureTest" 라는 패킷 캡처를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6c1b0-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="6c1b0-112">세션이 완료 되 면 지정 된 저장소 계정에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6c1b0-112">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="6c1b0-113">그런 다음 Get-AzureRmNetworkWatcherPacketCapture를 호출 하 여 캡처 세션의 상태를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c1b0-113">We then call Get-AzureRmNetworkWatcherPacketCapture to retrieve the status of the capture session.</span></span> 

<span data-ttu-id="6c1b0-114">참고: 패킷 캡처를 만들려면 대상 가상 컴퓨터에 Azure 네트워크 감시자 확장을 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c1b0-114">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="6c1b0-115">변수</span><span class="sxs-lookup"><span data-stu-id="6c1b0-115">PARAMETERS</span></span>

### <span data-ttu-id="6c1b0-116">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6c1b0-116">-NetworkWatcher</span></span>
<span data-ttu-id="6c1b0-117">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="6c1b0-117">The network watcher resource.</span></span>

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

### <span data-ttu-id="6c1b0-118">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="6c1b0-118">-NetworkWatcherName</span></span>
<span data-ttu-id="6c1b0-119">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6c1b0-119">The name of network watcher.</span></span>

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

### <span data-ttu-id="6c1b0-120">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="6c1b0-120">-PacketCaptureName</span></span>
<span data-ttu-id="6c1b0-121">패킷 캡처 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6c1b0-121">The packet capture name.</span></span>

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

### <span data-ttu-id="6c1b0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c1b0-122">-ResourceGroupName</span></span>
<span data-ttu-id="6c1b0-123">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6c1b0-123">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="6c1b0-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c1b0-124">-DefaultProfile</span></span>
<span data-ttu-id="6c1b0-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6c1b0-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c1b0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c1b0-126">CommonParameters</span></span>
<span data-ttu-id="6c1b0-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c1b0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c1b0-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6c1b0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c1b0-129">입력</span><span class="sxs-lookup"><span data-stu-id="6c1b0-129">INPUTS</span></span>

### <span data-ttu-id="6c1b0-130">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6c1b0-130">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="6c1b0-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6c1b0-131">System.String</span></span>

## <span data-ttu-id="6c1b0-132">출력</span><span class="sxs-lookup"><span data-stu-id="6c1b0-132">OUTPUTS</span></span>

### <span data-ttu-id="6c1b0-133">PSGetPacketCaptureResult에 대 한.</span><span class="sxs-lookup"><span data-stu-id="6c1b0-133">Microsoft.Azure.Commands.Network.Models.PSGetPacketCaptureResult</span></span>

## <span data-ttu-id="6c1b0-134">상속자</span><span class="sxs-lookup"><span data-stu-id="6c1b0-134">NOTES</span></span>
<span data-ttu-id="6c1b0-135">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 패킷, 캡처, 트래픽</span><span class="sxs-lookup"><span data-stu-id="6c1b0-135">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="6c1b0-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6c1b0-136">RELATED LINKS</span></span>

[<span data-ttu-id="6c1b0-137">새로운 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6c1b0-137">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6c1b0-138">새로운 AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="6c1b0-138">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="6c1b0-139">제거-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6c1b0-139">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6c1b0-140">중지-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="6c1b0-140">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="6c1b0-141">새로운 AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6c1b0-141">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="6c1b0-142">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6c1b0-142">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="6c1b0-143">제거-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="6c1b0-143">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="6c1b0-144">테스트-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="6c1b0-144">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="6c1b0-145">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="6c1b0-145">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="6c1b0-146">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="6c1b0-146">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="6c1b0-147">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="6c1b0-147">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="6c1b0-148">시작-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="6c1b0-148">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

