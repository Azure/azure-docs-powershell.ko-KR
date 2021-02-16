---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: 9825562ad5f0bec36da0efd14f2e06b93a3ad588
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100406757"
---
# <span data-ttu-id="3eb91-101">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3eb91-101">New-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="3eb91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3eb91-102">SYNOPSIS</span></span>
<span data-ttu-id="3eb91-103">새 패킷 캡처 리소스를 만들고 VM에서 패킷 캡처 세션을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="3eb91-103">Creates a new packet capture resource and starts a packet capture session on a VM.</span></span>

## <span data-ttu-id="3eb91-104">구문</span><span class="sxs-lookup"><span data-stu-id="3eb91-104">SYNTAX</span></span>

### <span data-ttu-id="3eb91-105">SetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="3eb91-105">SetByResource (Default)</span></span>
```
New-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>] [-Filter <PSPacketCaptureFilter[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3eb91-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="3eb91-106">SetByName</span></span>
```
New-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> -TargetVirtualMachineId <String> [-StorageAccountId <String>]
 [-StoragePath <String>] [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>]
 [-TotalBytesPerSession <Int32>] [-TimeLimitInSeconds <Int32>] [-Filter <PSPacketCaptureFilter[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3eb91-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="3eb91-107">SetByLocation</span></span>
```
New-AzNetworkWatcherPacketCapture -Location <String> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>] [-Filter <PSPacketCaptureFilter[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3eb91-108">설명</span><span class="sxs-lookup"><span data-stu-id="3eb91-108">DESCRIPTION</span></span>
<span data-ttu-id="3eb91-109">New-AzNetworkWatcherPacketCapture cmdlet은 새 패킷 캡처 리소스를 만들고 VM에서 패킷 캡처 세션을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="3eb91-109">The New-AzNetworkWatcherPacketCapture cmdlet creates a new packet capture resource and starts a packet capture session on a VM.</span></span>
<span data-ttu-id="3eb91-110">패킷 캡처 세션의 길이는 시간 제약 조건 또는 크기 제약 조건을 통해 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3eb91-110">The length of the Packet Capture sessions can be configured via a time constraint or a size constraint.</span></span> <span data-ttu-id="3eb91-111">각 패킷에 대해 캡처된 데이터의 양도 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3eb91-111">The amount of data captured for each packet can also be configured.</span></span>
<span data-ttu-id="3eb91-112">필터를 특정 패킷 캡처 세션에 적용할 수 있어 캡처된 패킷 유형을 사용자 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3eb91-112">Filters can be applied to a given packet capture session, allowing you to customize the type of packets captured.</span></span> <span data-ttu-id="3eb91-113">필터는 주소 범위, 로컬 및 원격 포트& 포트 범위 및 캡처할 세션 수준 프로토콜에 & 로컬 및 원격 IP 주소의 패킷을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3eb91-113">Filters can restrict packets on local and remote IP addresses & address ranges, local and remote ports & port ranges, and the session level protocol to be captured.</span></span> <span data-ttu-id="3eb91-114">필터는 구성 가능하고 여러 필터를 적용하여 캡처의 세분성을 제공할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3eb91-114">Filters are composable, and multiple filters can be applied to provide you with granularity of capture.</span></span>

## <span data-ttu-id="3eb91-115">예제</span><span class="sxs-lookup"><span data-stu-id="3eb91-115">EXAMPLES</span></span>

### <span data-ttu-id="3eb91-116">예제 1: 여러 필터를 사용하여 패킷 캡처 만들기</span><span class="sxs-lookup"><span data-stu-id="3eb91-116">Example 1: Create a Packet Capture with multiple filters</span></span>
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filter $filter1, $filter2
```

<span data-ttu-id="3eb91-117">이 예제에서는 여러 필터와 시간 제한이 있는 "PacketCaptureTest"라는 패킷 캡처를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3eb91-117">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="3eb91-118">세션이 완료되면 지정된 저장소 계정에 저장됩니다.</span><span class="sxs-lookup"><span data-stu-id="3eb91-118">Once the session is complete, it will be saved to the specified storage account.</span></span> <span data-ttu-id="3eb91-119">참고: 패킷 캡처를 만들 대상 가상 머신에 Azure Network Watcher 확장을 설치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3eb91-119">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="3eb91-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3eb91-120">PARAMETERS</span></span>

### <span data-ttu-id="3eb91-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3eb91-121">-AsJob</span></span>
<span data-ttu-id="3eb91-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="3eb91-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3eb91-123">-BytesToCapturePerPacket</span><span class="sxs-lookup"><span data-stu-id="3eb91-123">-BytesToCapturePerPacket</span></span>
<span data-ttu-id="3eb91-124">패킷당 캡처할 Bytes입니다.</span><span class="sxs-lookup"><span data-stu-id="3eb91-124">Bytes to capture per packet.</span></span>

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

### <span data-ttu-id="3eb91-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3eb91-125">-DefaultProfile</span></span>
<span data-ttu-id="3eb91-126">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3eb91-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3eb91-127">-Filter</span><span class="sxs-lookup"><span data-stu-id="3eb91-127">-Filter</span></span>
<span data-ttu-id="3eb91-128">패킷 캡처 세션에 대한 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="3eb91-128">Filters for packet capture session.</span></span>

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

### <span data-ttu-id="3eb91-129">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="3eb91-129">-LocalFilePath</span></span>
<span data-ttu-id="3eb91-130">로컬 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="3eb91-130">Local file path.</span></span>

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

### <span data-ttu-id="3eb91-131">-Location</span><span class="sxs-lookup"><span data-stu-id="3eb91-131">-Location</span></span>
<span data-ttu-id="3eb91-132">네트워크 감시자 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="3eb91-132">Location of the network watcher.</span></span>

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

### <span data-ttu-id="3eb91-133">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3eb91-133">-NetworkWatcher</span></span>
<span data-ttu-id="3eb91-134">네트워크 감시자 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="3eb91-134">The network watcher resource.</span></span>

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

### <span data-ttu-id="3eb91-135">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="3eb91-135">-NetworkWatcherName</span></span>
<span data-ttu-id="3eb91-136">Network Watcher의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3eb91-136">The name of network watcher.</span></span>

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

### <span data-ttu-id="3eb91-137">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="3eb91-137">-PacketCaptureName</span></span>
<span data-ttu-id="3eb91-138">패킷 캡처 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3eb91-138">The packet capture name.</span></span>

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

### <span data-ttu-id="3eb91-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3eb91-139">-ResourceGroupName</span></span>
<span data-ttu-id="3eb91-140">Network Watcher 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3eb91-140">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="3eb91-141">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="3eb91-141">-StorageAccountId</span></span>
<span data-ttu-id="3eb91-142">저장소 계정 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3eb91-142">Storage account Id.</span></span>

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

### <span data-ttu-id="3eb91-143">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="3eb91-143">-StoragePath</span></span>
<span data-ttu-id="3eb91-144">저장소 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="3eb91-144">Storage path.</span></span>

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

### <span data-ttu-id="3eb91-145">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="3eb91-145">-TargetVirtualMachineId</span></span>
<span data-ttu-id="3eb91-146">대상 가상 머신 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3eb91-146">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="3eb91-147">-TimeLimitInSeconds</span><span class="sxs-lookup"><span data-stu-id="3eb91-147">-TimeLimitInSeconds</span></span>
<span data-ttu-id="3eb91-148">시간 제한(초)입니다.</span><span class="sxs-lookup"><span data-stu-id="3eb91-148">Time limit in seconds.</span></span>

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

### <span data-ttu-id="3eb91-149">-TotalBytesPerSession</span><span class="sxs-lookup"><span data-stu-id="3eb91-149">-TotalBytesPerSession</span></span>
<span data-ttu-id="3eb91-150">세션당 총 bytes입니다.</span><span class="sxs-lookup"><span data-stu-id="3eb91-150">Total bytes per session.</span></span>

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

### <span data-ttu-id="3eb91-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3eb91-151">-Confirm</span></span>
<span data-ttu-id="3eb91-152">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3eb91-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3eb91-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3eb91-153">-WhatIf</span></span>
<span data-ttu-id="3eb91-154">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="3eb91-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3eb91-155">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3eb91-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3eb91-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3eb91-156">CommonParameters</span></span>
<span data-ttu-id="3eb91-157">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3eb91-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3eb91-158">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="3eb91-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3eb91-159">입력</span><span class="sxs-lookup"><span data-stu-id="3eb91-159">INPUTS</span></span>

### <span data-ttu-id="3eb91-160">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3eb91-160">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="3eb91-161">System.String</span><span class="sxs-lookup"><span data-stu-id="3eb91-161">System.String</span></span>

### <span data-ttu-id="3eb91-162">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="3eb91-162">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="3eb91-163">출력</span><span class="sxs-lookup"><span data-stu-id="3eb91-163">OUTPUTS</span></span>

### <span data-ttu-id="3eb91-164">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="3eb91-164">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureResult</span></span>

## <span data-ttu-id="3eb91-165">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3eb91-165">NOTES</span></span>
<span data-ttu-id="3eb91-166">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 패킷, 캡처, 트래픽</span><span class="sxs-lookup"><span data-stu-id="3eb91-166">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span> 

## <span data-ttu-id="3eb91-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3eb91-167">RELATED LINKS</span></span>

[<span data-ttu-id="3eb91-168">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3eb91-168">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="3eb91-169">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3eb91-169">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="3eb91-170">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3eb91-170">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="3eb91-171">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="3eb91-171">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="3eb91-172">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="3eb91-172">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="3eb91-173">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="3eb91-173">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="3eb91-174">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="3eb91-174">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="3eb91-175">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3eb91-175">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3eb91-176">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="3eb91-176">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="3eb91-177">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3eb91-177">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3eb91-178">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3eb91-178">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3eb91-179">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3eb91-179">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3eb91-180">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="3eb91-180">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="3eb91-181">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="3eb91-181">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="3eb91-182">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="3eb91-182">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="3eb91-183">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3eb91-183">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3eb91-184">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3eb91-184">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3eb91-185">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3eb91-185">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3eb91-186">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="3eb91-186">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="3eb91-187">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3eb91-187">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3eb91-188">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3eb91-188">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="3eb91-189">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="3eb91-189">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="3eb91-190">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="3eb91-190">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="3eb91-191">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="3eb91-191">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="3eb91-192">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="3eb91-192">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="3eb91-193">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="3eb91-193">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="3eb91-194">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="3eb91-194">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor.md)


