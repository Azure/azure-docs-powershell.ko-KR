---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPacketCaptureFilterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmPacketCaptureFilterConfig.md
ms.openlocfilehash: ad6d2baaccdc17ec6ca414ae4b0cee84db20c94b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529295"
---
# <span data-ttu-id="9a4be-101">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="9a4be-101">New-AzureRmPacketCaptureFilterConfig</span></span>

## <span data-ttu-id="9a4be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a4be-102">SYNOPSIS</span></span>
<span data-ttu-id="9a4be-103">새 패킷 캡처 필터 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9a4be-103">Creates a new packet capture filter object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a4be-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9a4be-104">SYNTAX</span></span>

```
New-AzureRmPacketCaptureFilterConfig [-Protocol <String>] [-RemoteIPAddress <String>]
 [-LocalIPAddress <String>] [-LocalPort <String>] [-RemotePort <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a4be-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9a4be-105">DESCRIPTION</span></span>
<span data-ttu-id="9a4be-106">New-AzureRmPacketCaptureFilterConfig cmdlet은 새 패킷 캡처 필터 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9a4be-106">The New-AzureRmPacketCaptureFilterConfig cmdlet creates a new packet capture filter object.</span></span> <span data-ttu-id="9a4be-107">이 개체는 지정 된 기준을 사용 하 여 패킷 캡처 세션 중에 캡처한 패킷의 유형을 제한 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9a4be-107">This object is used to restrict the type of packets that are captured during a packet capture session using the specified criteria.</span></span> <span data-ttu-id="9a4be-108">New-AzureRmNetworkWatcherPacketCapture cmdlet은 여러 필터 개체를 허용 하 여 작성 가능한 캡처 세션을 사용 하도록 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9a4be-108">The New-AzureRmNetworkWatcherPacketCapture cmdlet can accept multiple filter objects to enable composable capture sessions.</span></span>

## <span data-ttu-id="9a4be-109">예제의</span><span class="sxs-lookup"><span data-stu-id="9a4be-109">EXAMPLES</span></span>

### <span data-ttu-id="9a4be-110">---예제 1: 여러 필터를 사용 하 여 패킷 캡처 만들기---</span><span class="sxs-lookup"><span data-stu-id="9a4be-110">--- Example 1: Create a Packet Capture with multiple filters ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2
```

<span data-ttu-id="9a4be-111">이 예제에서는 여러 필터 및 시간 제한을 사용 하 여 "PacketCaptureTest" 라는 패킷 캡처를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9a4be-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="9a4be-112">세션이 완료 되 면 지정 된 저장소 계정에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9a4be-112">Once the session is complete, it will be saved to the specified storage account.</span></span> 

<span data-ttu-id="9a4be-113">참고: 패킷 캡처를 만들려면 대상 가상 컴퓨터에 Azure 네트워크 감시자 확장을 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a4be-113">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="9a4be-114">변수</span><span class="sxs-lookup"><span data-stu-id="9a4be-114">PARAMETERS</span></span>

### <span data-ttu-id="9a4be-115">-LocalIPAddress</span><span class="sxs-lookup"><span data-stu-id="9a4be-115">-LocalIPAddress</span></span>
<span data-ttu-id="9a4be-116">필터링 할 로컬 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a4be-116">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="9a4be-117">예제 입력: 단일 주소 항목의 경우 "127.0.0.1"입니다.</span><span class="sxs-lookup"><span data-stu-id="9a4be-117">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="9a4be-118">범위에 대해 "127.0.0.1-127.0.0.255".</span><span class="sxs-lookup"><span data-stu-id="9a4be-118">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="9a4be-119">여러 항목에 대해 "127.0.0.1; 127.0.0.5;"</span><span class="sxs-lookup"><span data-stu-id="9a4be-119">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="9a4be-120">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="9a4be-120">-LocalPort</span></span>
<span data-ttu-id="9a4be-121">필터링 할 로컬 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a4be-121">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="9a4be-122">예제 입력: 단일 주소 항목의 경우 "127.0.0.1"입니다.</span><span class="sxs-lookup"><span data-stu-id="9a4be-122">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="9a4be-123">범위에 대해 "127.0.0.1-127.0.0.255".</span><span class="sxs-lookup"><span data-stu-id="9a4be-123">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="9a4be-124">여러 항목에 대해 "127.0.0.1; 127.0.0.5;"</span><span class="sxs-lookup"><span data-stu-id="9a4be-124">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="9a4be-125">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="9a4be-125">-Protocol</span></span>
<span data-ttu-id="9a4be-126">필터링 할 Procotol를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a4be-126">Specifies the Procotol to filter on.</span></span> <span data-ttu-id="9a4be-127">허용 되는 값 "TCP", "UDP", "모든"</span><span class="sxs-lookup"><span data-stu-id="9a4be-127">Acceptable values "TCP","UDP","Any"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a4be-128">-RemoteIPAddress</span><span class="sxs-lookup"><span data-stu-id="9a4be-128">-RemoteIPAddress</span></span>
<span data-ttu-id="9a4be-129">필터링 할 원격 IP 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a4be-129">Specifies the remote IP address to filter on.</span></span>
<span data-ttu-id="9a4be-130">예제 입력: 단일 주소 항목의 경우 "127.0.0.1"입니다.</span><span class="sxs-lookup"><span data-stu-id="9a4be-130">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="9a4be-131">범위에 대해 "127.0.0.1-127.0.0.255".</span><span class="sxs-lookup"><span data-stu-id="9a4be-131">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="9a4be-132">여러 항목에 대해 "127.0.0.1; 127.0.0.5;"</span><span class="sxs-lookup"><span data-stu-id="9a4be-132">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="9a4be-133">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="9a4be-133">-RemotePort</span></span>
<span data-ttu-id="9a4be-134">필터링 할 원격 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a4be-134">Specifies the Remote Port to filter on.</span></span>
<span data-ttu-id="9a4be-135">원격 포트 예제 입력: 단일 포트 항목의 경우 "80".</span><span class="sxs-lookup"><span data-stu-id="9a4be-135">Remote port Example inputs: "80" for single port entry.</span></span>
<span data-ttu-id="9a4be-136">범위에 대 한 "80-85".</span><span class="sxs-lookup"><span data-stu-id="9a4be-136">"80-85" for range.</span></span>
<span data-ttu-id="9a4be-137">여러 항목에 대해 "80; 443;"</span><span class="sxs-lookup"><span data-stu-id="9a4be-137">"80;443;" for multiple entries.</span></span>

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

### <span data-ttu-id="9a4be-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a4be-138">-DefaultProfile</span></span>
<span data-ttu-id="9a4be-139">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9a4be-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a4be-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a4be-140">CommonParameters</span></span>
<span data-ttu-id="9a4be-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a4be-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a4be-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a4be-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a4be-143">입력</span><span class="sxs-lookup"><span data-stu-id="9a4be-143">INPUTS</span></span>

### <span data-ttu-id="9a4be-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9a4be-144">System.String</span></span>

## <span data-ttu-id="9a4be-145">출력</span><span class="sxs-lookup"><span data-stu-id="9a4be-145">OUTPUTS</span></span>

### <span data-ttu-id="9a4be-146">PSPacketCaptureFilter에 대 한.</span><span class="sxs-lookup"><span data-stu-id="9a4be-146">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter</span></span>

## <span data-ttu-id="9a4be-147">상속자</span><span class="sxs-lookup"><span data-stu-id="9a4be-147">NOTES</span></span>
<span data-ttu-id="9a4be-148">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 감시자, 패킷, 캡처, 트래픽, 필터</span><span class="sxs-lookup"><span data-stu-id="9a4be-148">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span></span> 

## <span data-ttu-id="9a4be-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9a4be-149">RELATED LINKS</span></span>

[<span data-ttu-id="9a4be-150">새로운 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9a4be-150">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9a4be-151">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9a4be-151">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9a4be-152">제거-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9a4be-152">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9a4be-153">중지-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9a4be-153">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="9a4be-154">새로운 AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9a4be-154">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="9a4be-155">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9a4be-155">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="9a4be-156">제거-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="9a4be-156">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="9a4be-157">테스트-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="9a4be-157">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="9a4be-158">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="9a4be-158">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="9a4be-159">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="9a4be-159">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="9a4be-160">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="9a4be-160">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="9a4be-161">시작-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="9a4be-161">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
