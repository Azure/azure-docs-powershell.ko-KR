---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 348767f145c2dd407fc277549f89c44386c8a564
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041780"
---
# <span data-ttu-id="cbf5a-101">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cbf5a-101">New-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="cbf5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cbf5a-102">SYNOPSIS</span></span>
<span data-ttu-id="cbf5a-103">새 패킷 캡처 리소스를 만들고 VM에서 패킷 캡처 세션을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf5a-103">Creates a new packet capture resource and starts a packet capture session on a VM.</span></span>

## <span data-ttu-id="cbf5a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cbf5a-104">SYNTAX</span></span>

### <span data-ttu-id="cbf5a-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="cbf5a-105">SetByResource (Default)</span></span>
```
New-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>] [-Filter <PSPacketCaptureFilter[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbf5a-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="cbf5a-106">SetByName</span></span>
```
New-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> -TargetVirtualMachineId <String> [-StorageAccountId <String>]
 [-StoragePath <String>] [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>]
 [-TotalBytesPerSession <Int32>] [-TimeLimitInSeconds <Int32>] [-Filter <PSPacketCaptureFilter[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cbf5a-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="cbf5a-107">SetByLocation</span></span>
```
New-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>] [-Filter <PSPacketCaptureFilter[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cbf5a-108">설명은</span><span class="sxs-lookup"><span data-stu-id="cbf5a-108">DESCRIPTION</span></span>
<span data-ttu-id="cbf5a-109">New-AzNetworkWatcherPacketCapture cmdlet은 새 패킷 캡처 리소스를 만들고 VM에서 패킷 캡처 세션을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf5a-109">The New-AzNetworkWatcherPacketCapture cmdlet creates a new packet capture resource and starts a packet capture session on a VM.</span></span>
<span data-ttu-id="cbf5a-110">패킷 캡처 세션의 길이는 시간 제약 조건이 나 크기 제약 조건을 통해 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cbf5a-110">The length of the Packet Capture sessions can be configured via a time constraint or a size constraint.</span></span> <span data-ttu-id="cbf5a-111">각 패킷에 대해 캡처한 데이터의 양을 구성할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cbf5a-111">The amount of data captured for each packet can also be configured.</span></span>
<span data-ttu-id="cbf5a-112">지정 된 패킷 캡처 세션에 필터를 적용 하 여 캡처한 패킷의 유형을 사용자 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cbf5a-112">Filters can be applied to a given packet capture session, allowing you to customize the type of packets captured.</span></span> <span data-ttu-id="cbf5a-113">필터는 주소 범위, 로컬 및 원격 포트 & 포트 범위, 캡처할 세션 수준 프로토콜 & 로컬 및 원격 IP 주소에서 패킷을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cbf5a-113">Filters can restrict packets on local and remote IP addresses & address ranges, local and remote ports & port ranges, and the session level protocol to be captured.</span></span> <span data-ttu-id="cbf5a-114">필터는 구성할 수 있으며 여러 필터를 적용 하 여 캡처의 세분성을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf5a-114">Filters are composable, and multiple filters can be applied to provide you with granularity of capture.</span></span>

## <span data-ttu-id="cbf5a-115">예제의</span><span class="sxs-lookup"><span data-stu-id="cbf5a-115">EXAMPLES</span></span>

### <span data-ttu-id="cbf5a-116">예제 1: 여러 필터를 사용 하 여 패킷 캡처 만들기</span><span class="sxs-lookup"><span data-stu-id="cbf5a-116">Example 1: Create a Packet Capture with multiple filters</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filter $filter1, $filter2
```

<span data-ttu-id="cbf5a-117">이 예제에서는 여러 필터 및 시간 제한을 사용 하 여 "PacketCaptureTest" 라는 패킷 캡처를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="cbf5a-117">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="cbf5a-118">세션이 완료 되 면 지정 된 저장소 계정에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="cbf5a-118">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="cbf5a-119">참고: 패킷 캡처를 만들려면 대상 가상 컴퓨터에 Azure 네트워크 감시자 확장을 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf5a-119">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="cbf5a-120">변수</span><span class="sxs-lookup"><span data-stu-id="cbf5a-120">PARAMETERS</span></span>

### <span data-ttu-id="cbf5a-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cbf5a-121">-AsJob</span></span>
<span data-ttu-id="cbf5a-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="cbf5a-122">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbf5a-123">-BytesToCapturePerPacket</span><span class="sxs-lookup"><span data-stu-id="cbf5a-123">-BytesToCapturePerPacket</span></span>
<span data-ttu-id="cbf5a-124">패킷 당 캡처할 바이트 수입니다.</span><span class="sxs-lookup"><span data-stu-id="cbf5a-124">Bytes to capture per packet.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbf5a-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbf5a-125">-DefaultProfile</span></span>
<span data-ttu-id="cbf5a-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cbf5a-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbf5a-127">-필터</span><span class="sxs-lookup"><span data-stu-id="cbf5a-127">-Filter</span></span>
<span data-ttu-id="cbf5a-128">패킷 캡처 세션에 대 한 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="cbf5a-128">Filters for packet capture session.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbf5a-129">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="cbf5a-129">-LocalFilePath</span></span>
<span data-ttu-id="cbf5a-130">로컬 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="cbf5a-130">Local file path.</span></span>

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

### <span data-ttu-id="cbf5a-131">-위치</span><span class="sxs-lookup"><span data-stu-id="cbf5a-131">-Location</span></span>
<span data-ttu-id="cbf5a-132">네트워크 감시자의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="cbf5a-132">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbf5a-133">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cbf5a-133">-NetworkWatcher</span></span>
<span data-ttu-id="cbf5a-134">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="cbf5a-134">The network watcher resource.</span></span>

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

### <span data-ttu-id="cbf5a-135">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="cbf5a-135">-NetworkWatcherName</span></span>
<span data-ttu-id="cbf5a-136">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cbf5a-136">The name of network watcher.</span></span>

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

### <span data-ttu-id="cbf5a-137">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="cbf5a-137">-PacketCaptureName</span></span>
<span data-ttu-id="cbf5a-138">패킷 캡처 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cbf5a-138">The packet capture name.</span></span>

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

### <span data-ttu-id="cbf5a-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cbf5a-139">-ResourceGroupName</span></span>
<span data-ttu-id="cbf5a-140">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cbf5a-140">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="cbf5a-141">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="cbf5a-141">-StorageAccountId</span></span>
<span data-ttu-id="cbf5a-142">저장소 계정 Id.</span><span class="sxs-lookup"><span data-stu-id="cbf5a-142">Storage account Id.</span></span>

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

### <span data-ttu-id="cbf5a-143">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="cbf5a-143">-StoragePath</span></span>
<span data-ttu-id="cbf5a-144">저장소 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="cbf5a-144">Storage path.</span></span>

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

### <span data-ttu-id="cbf5a-145">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="cbf5a-145">-TargetVirtualMachineId</span></span>
<span data-ttu-id="cbf5a-146">대상 가상 컴퓨터 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="cbf5a-146">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="cbf5a-147">-TimeLimitInSeconds</span><span class="sxs-lookup"><span data-stu-id="cbf5a-147">-TimeLimitInSeconds</span></span>
<span data-ttu-id="cbf5a-148">시간 제한 (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="cbf5a-148">Time limit in seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbf5a-149">-TotalBytesPerSession</span><span class="sxs-lookup"><span data-stu-id="cbf5a-149">-TotalBytesPerSession</span></span>
<span data-ttu-id="cbf5a-150">세션당 총 바이트 수.</span><span class="sxs-lookup"><span data-stu-id="cbf5a-150">Total bytes per session.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbf5a-151">-확인</span><span class="sxs-lookup"><span data-stu-id="cbf5a-151">-Confirm</span></span>
<span data-ttu-id="cbf5a-152">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf5a-152">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbf5a-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cbf5a-153">-WhatIf</span></span>
<span data-ttu-id="cbf5a-154">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cbf5a-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cbf5a-155">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cbf5a-155">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbf5a-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbf5a-156">CommonParameters</span></span>
<span data-ttu-id="cbf5a-157">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cbf5a-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbf5a-158">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbf5a-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbf5a-159">입력</span><span class="sxs-lookup"><span data-stu-id="cbf5a-159">INPUTS</span></span>

### <span data-ttu-id="cbf5a-160">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cbf5a-160">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="cbf5a-161">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cbf5a-161">System.String</span></span>

### <span data-ttu-id="cbf5a-162">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e])</span><span class="sxs-lookup"><span data-stu-id="cbf5a-162">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="cbf5a-163">출력</span><span class="sxs-lookup"><span data-stu-id="cbf5a-163">OUTPUTS</span></span>

### <span data-ttu-id="cbf5a-164">PSPacketCaptureResult에 대 한.</span><span class="sxs-lookup"><span data-stu-id="cbf5a-164">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureResult</span></span>

## <span data-ttu-id="cbf5a-165">상속자</span><span class="sxs-lookup"><span data-stu-id="cbf5a-165">NOTES</span></span>
<span data-ttu-id="cbf5a-166">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 패킷, 캡처, 트래픽</span><span class="sxs-lookup"><span data-stu-id="cbf5a-166">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span> 

## <span data-ttu-id="cbf5a-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cbf5a-167">RELATED LINKS</span></span>

[<span data-ttu-id="cbf5a-168">새로운 AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cbf5a-168">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="cbf5a-169">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cbf5a-169">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="cbf5a-170">제거-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="cbf5a-170">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="cbf5a-171">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="cbf5a-171">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="cbf5a-172">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="cbf5a-172">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="cbf5a-173">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="cbf5a-173">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="cbf5a-174">시작-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="cbf5a-174">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="cbf5a-175">새로운 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cbf5a-175">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cbf5a-176">새로운 AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="cbf5a-176">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="cbf5a-177">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cbf5a-177">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cbf5a-178">제거-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cbf5a-178">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cbf5a-179">중지-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cbf5a-179">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="cbf5a-180">새로운 AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="cbf5a-180">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="cbf5a-181">테스트-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="cbf5a-181">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="cbf5a-182">테스트-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="cbf5a-182">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="cbf5a-183">중지-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cbf5a-183">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cbf5a-184">시작-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cbf5a-184">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cbf5a-185">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cbf5a-185">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cbf5a-186">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="cbf5a-186">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="cbf5a-187">제거-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cbf5a-187">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cbf5a-188">새로운 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cbf5a-188">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="cbf5a-189">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="cbf5a-189">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="cbf5a-190">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="cbf5a-190">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="cbf5a-191">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="cbf5a-191">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="cbf5a-192">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="cbf5a-192">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="cbf5a-193">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="cbf5a-193">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="cbf5a-194">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="cbf5a-194">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)


