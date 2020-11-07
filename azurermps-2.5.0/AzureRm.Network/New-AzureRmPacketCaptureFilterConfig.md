---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermpacketcapturefilterconfig
schema: 2.0.0
ms.openlocfilehash: 1d6054307ad1e499fbb36342f6c81e7e32227f37
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881362"
---
# <span data-ttu-id="7f6f8-101">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="7f6f8-101">New-AzureRmPacketCaptureFilterConfig</span></span>

## <span data-ttu-id="7f6f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f6f8-102">SYNOPSIS</span></span>
<span data-ttu-id="7f6f8-103">새 패킷 캡처 필터 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7f6f8-103">Creates a new packet capture filter object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f6f8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7f6f8-104">SYNTAX</span></span>

```
New-AzureRmPacketCaptureFilterConfig [-Protocol <String>] [-RemoteIPAddress <String>]
 [-LocalIPAddress <String>] [-LocalPort <String>] [-RemotePort <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f6f8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7f6f8-105">DESCRIPTION</span></span>
<span data-ttu-id="7f6f8-106">New-AzureRmPacketCaptureFilterConfig cmdlet은 새 패킷 캡처 필터 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7f6f8-106">The New-AzureRmPacketCaptureFilterConfig cmdlet creates a new packet capture filter object.</span></span> <span data-ttu-id="7f6f8-107">이 개체는 지정 된 기준을 사용 하 여 패킷 캡처 세션 중에 캡처한 패킷의 유형을 제한 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7f6f8-107">This object is used to restrict the type of packets that are captured during a packet capture session using the specified criteria.</span></span> <span data-ttu-id="7f6f8-108">New-AzureRmNetworkWatcherPacketCapture cmdlet은 여러 필터 개체를 허용 하 여 작성 가능한 캡처 세션을 사용 하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7f6f8-108">The New-AzureRmNetworkWatcherPacketCapture cmdlet can accept multiple filter objects to enable composable capture sessions.</span></span>

## <span data-ttu-id="7f6f8-109">예제의</span><span class="sxs-lookup"><span data-stu-id="7f6f8-109">EXAMPLES</span></span>

### <span data-ttu-id="7f6f8-110">---예제 1: 여러 필터를 사용 하 여 패킷 캡처 만들기---</span><span class="sxs-lookup"><span data-stu-id="7f6f8-110">--- Example 1: Create a Packet Capture with multiple filters ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2
```

<span data-ttu-id="7f6f8-111">이 예제에서는 여러 필터 및 시간 제한을 사용 하 여 "PacketCaptureTest" 라는 패킷 캡처를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7f6f8-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="7f6f8-112">세션이 완료 되 면 지정 된 저장소 계정에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7f6f8-112">Once the session is complete, it will be saved to the specified storage account.</span></span> 

<span data-ttu-id="7f6f8-113">참고: 패킷 캡처를 만들려면 대상 가상 컴퓨터에 Azure 네트워크 감시자 확장을 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f6f8-113">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="7f6f8-114">변수</span><span class="sxs-lookup"><span data-stu-id="7f6f8-114">PARAMETERS</span></span>

### <span data-ttu-id="7f6f8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f6f8-115">-DefaultProfile</span></span>
<span data-ttu-id="7f6f8-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7f6f8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f6f8-117">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="7f6f8-117">-LocalIPAddress</span></span>
<span data-ttu-id="7f6f8-118">필터링 할 로컬 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f6f8-118">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="7f6f8-119">예제 입력: 단일 주소 항목의 경우 "127.0.0.1"입니다.</span><span class="sxs-lookup"><span data-stu-id="7f6f8-119">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="7f6f8-120">범위에 대해 "127.0.0.1-127.0.0.255".</span><span class="sxs-lookup"><span data-stu-id="7f6f8-120">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="7f6f8-121">여러 항목에 대해 "127.0.0.1; 127.0.0.5;"</span><span class="sxs-lookup"><span data-stu-id="7f6f8-121">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="7f6f8-122">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="7f6f8-122">-LocalPort</span></span>
<span data-ttu-id="7f6f8-123">필터링 할 로컬 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f6f8-123">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="7f6f8-124">예제 입력: 단일 주소 항목의 경우 "127.0.0.1"입니다.</span><span class="sxs-lookup"><span data-stu-id="7f6f8-124">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="7f6f8-125">범위에 대해 "127.0.0.1-127.0.0.255".</span><span class="sxs-lookup"><span data-stu-id="7f6f8-125">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="7f6f8-126">여러 항목에 대해 "127.0.0.1; 127.0.0.5;"</span><span class="sxs-lookup"><span data-stu-id="7f6f8-126">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="7f6f8-127">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="7f6f8-127">-Protocol</span></span>
<span data-ttu-id="7f6f8-128">필터링 할 Procotol를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f6f8-128">Specifies the Procotol to filter on.</span></span> <span data-ttu-id="7f6f8-129">허용 되는 값 "TCP", "UDP", "모든"</span><span class="sxs-lookup"><span data-stu-id="7f6f8-129">Acceptable values "TCP","UDP","Any"</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7f6f8-130">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="7f6f8-130">-RemoteIPAddress</span></span>
<span data-ttu-id="7f6f8-131">필터링 할 원격 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f6f8-131">Specifies the remote IP address to filter on.</span></span>
<span data-ttu-id="7f6f8-132">예제 입력: 단일 주소 항목의 경우 "127.0.0.1"입니다.</span><span class="sxs-lookup"><span data-stu-id="7f6f8-132">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="7f6f8-133">범위에 대해 "127.0.0.1-127.0.0.255".</span><span class="sxs-lookup"><span data-stu-id="7f6f8-133">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="7f6f8-134">여러 항목에 대해 "127.0.0.1; 127.0.0.5;"</span><span class="sxs-lookup"><span data-stu-id="7f6f8-134">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="7f6f8-135">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="7f6f8-135">-RemotePort</span></span>
<span data-ttu-id="7f6f8-136">필터링 할 원격 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f6f8-136">Specifies the Remote Port to filter on.</span></span>
<span data-ttu-id="7f6f8-137">원격 포트 예제 입력: 단일 포트 항목의 경우 "80".</span><span class="sxs-lookup"><span data-stu-id="7f6f8-137">Remote port Example inputs: "80" for single port entry.</span></span>
<span data-ttu-id="7f6f8-138">범위에 대 한 "80-85".</span><span class="sxs-lookup"><span data-stu-id="7f6f8-138">"80-85" for range.</span></span>
<span data-ttu-id="7f6f8-139">여러 항목에 대해 "80; 443;"</span><span class="sxs-lookup"><span data-stu-id="7f6f8-139">"80;443;" for multiple entries.</span></span>

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

### <span data-ttu-id="7f6f8-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f6f8-140">CommonParameters</span></span>
<span data-ttu-id="7f6f8-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f6f8-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f6f8-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f6f8-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f6f8-143">입력</span><span class="sxs-lookup"><span data-stu-id="7f6f8-143">INPUTS</span></span>

### <span data-ttu-id="7f6f8-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7f6f8-144">System.String</span></span>

## <span data-ttu-id="7f6f8-145">출력</span><span class="sxs-lookup"><span data-stu-id="7f6f8-145">OUTPUTS</span></span>

### <span data-ttu-id="7f6f8-146">PSPacketCaptureFilter에 대 한.</span><span class="sxs-lookup"><span data-stu-id="7f6f8-146">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter</span></span>

## <span data-ttu-id="7f6f8-147">상속자</span><span class="sxs-lookup"><span data-stu-id="7f6f8-147">NOTES</span></span>
<span data-ttu-id="7f6f8-148">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 감시자, 패킷, 캡처, 트래픽, 필터</span><span class="sxs-lookup"><span data-stu-id="7f6f8-148">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span></span> 

## <span data-ttu-id="7f6f8-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7f6f8-149">RELATED LINKS</span></span>

[<span data-ttu-id="7f6f8-150">새로운 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7f6f8-150">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7f6f8-151">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7f6f8-151">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7f6f8-152">제거-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7f6f8-152">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7f6f8-153">중지-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7f6f8-153">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7f6f8-154">새로운 AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7f6f8-154">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="7f6f8-155">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7f6f8-155">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="7f6f8-156">제거-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7f6f8-156">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="7f6f8-157">테스트-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="7f6f8-157">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="7f6f8-158">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="7f6f8-158">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="7f6f8-159">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="7f6f8-159">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="7f6f8-160">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="7f6f8-160">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="7f6f8-161">시작-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="7f6f8-161">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
