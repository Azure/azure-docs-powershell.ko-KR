---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermnetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: 0c84927ede94724da94351a219c9c0ec594c688d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93538020"
---
# <span data-ttu-id="3972a-101">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3972a-101">New-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="3972a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3972a-102">SYNOPSIS</span></span>
<span data-ttu-id="3972a-103">새 패킷 캡처 리소스를 만들고 VM에서 패킷 캡처 세션을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="3972a-103">Creates a new packet capture resource and starts a packet capture session on a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3972a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3972a-104">SYNTAX</span></span>

### <span data-ttu-id="3972a-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="3972a-105">SetByResource (Default)</span></span>
```
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 -TargetVirtualMachineId <String> [-StorageAccountId <String>] [-StoragePath <String>]
 [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>] [-TotalBytesPerSession <Int32>]
 [-TimeLimitInSeconds <Int32>]
 [-Filter <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3972a-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="3972a-106">SetByName</span></span>
```
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> -TargetVirtualMachineId <String> [-StorageAccountId <String>]
 [-StoragePath <String>] [-LocalFilePath <String>] [-BytesToCapturePerPacket <Int32>]
 [-TotalBytesPerSession <Int32>] [-TimeLimitInSeconds <Int32>]
 [-Filter <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3972a-107">설명은</span><span class="sxs-lookup"><span data-stu-id="3972a-107">DESCRIPTION</span></span>
<span data-ttu-id="3972a-108">New-AzureRmNetworkWatcherPacketCapture cmdlet은 새 패킷 캡처 리소스를 만들고 VM에서 패킷 캡처 세션을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="3972a-108">The New-AzureRmNetworkWatcherPacketCapture cmdlet creates a new packet capture resource and starts a packet capture session on a VM.</span></span>
<span data-ttu-id="3972a-109">패킷 캡처 세션의 길이는 시간 제약 조건이 나 크기 제약 조건을 통해 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3972a-109">The length of the Packet Capture sessions can be configured via a time constraint or a size constraint.</span></span> <span data-ttu-id="3972a-110">각 패킷에 대해 캡처한 데이터의 양을 구성할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3972a-110">The amount of data captured for each packet can also be configured.</span></span>
<span data-ttu-id="3972a-111">지정 된 패킷 캡처 세션에 필터를 적용 하 여 캡처한 패킷의 유형을 사용자 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3972a-111">Filters can be applied to a given packet capture session, allowing you to customize the type of packets captured.</span></span> <span data-ttu-id="3972a-112">필터는 주소 범위, 로컬 및 원격 포트 & 포트 범위, 캡처할 세션 수준 프로토콜 & 로컬 및 원격 IP 주소에서 패킷을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3972a-112">Filters can restrict packets on local and remote IP addresses & address ranges, local and remote ports & port ranges, and the session level protocol to be captured.</span></span> <span data-ttu-id="3972a-113">필터는 구성할 수 있으며 여러 필터를 적용 하 여 캡처의 세분성을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="3972a-113">Filters are composable, and multiple filters can be applied to provide you with granularity of capture.</span></span>

## <span data-ttu-id="3972a-114">예제의</span><span class="sxs-lookup"><span data-stu-id="3972a-114">EXAMPLES</span></span>

### <span data-ttu-id="3972a-115">---예제 1: 여러 필터를 사용 하 여 패킷 캡처 만들기---</span><span class="sxs-lookup"><span data-stu-id="3972a-115">--- Example 1: Create a Packet Capture with multiple filters ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filter $filter1, $filter2
```

<span data-ttu-id="3972a-116">이 예제에서는 여러 필터 및 시간 제한을 사용 하 여 "PacketCaptureTest" 라는 패킷 캡처를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3972a-116">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="3972a-117">세션이 완료 되 면 지정 된 저장소 계정에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3972a-117">Once the session is complete, it will be saved to the specified storage account.</span></span> 

<span data-ttu-id="3972a-118">참고: 패킷 캡처를 만들려면 대상 가상 컴퓨터에 Azure 네트워크 감시자 확장을 설치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3972a-118">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="3972a-119">변수</span><span class="sxs-lookup"><span data-stu-id="3972a-119">PARAMETERS</span></span>

### <span data-ttu-id="3972a-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3972a-120">-AsJob</span></span>
<span data-ttu-id="3972a-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="3972a-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3972a-122">-BytesToCapturePerPacket</span><span class="sxs-lookup"><span data-stu-id="3972a-122">-BytesToCapturePerPacket</span></span>
<span data-ttu-id="3972a-123">패킷 당 캡처할 바이트 수입니다.</span><span class="sxs-lookup"><span data-stu-id="3972a-123">Bytes to capture per packet.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3972a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3972a-124">-DefaultProfile</span></span>
<span data-ttu-id="3972a-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3972a-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3972a-126">-필터</span><span class="sxs-lookup"><span data-stu-id="3972a-126">-Filter</span></span>
<span data-ttu-id="3972a-127">패킷 캡처 세션에 대 한 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="3972a-127">Filters for packet capture session.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3972a-128">-LocalFilePath</span><span class="sxs-lookup"><span data-stu-id="3972a-128">-LocalFilePath</span></span>
<span data-ttu-id="3972a-129">로컬 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="3972a-129">Local file path.</span></span>

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

### <span data-ttu-id="3972a-130">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3972a-130">-NetworkWatcher</span></span>
<span data-ttu-id="3972a-131">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="3972a-131">The network watcher resource.</span></span>

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

### <span data-ttu-id="3972a-132">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="3972a-132">-NetworkWatcherName</span></span>
<span data-ttu-id="3972a-133">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3972a-133">The name of network watcher.</span></span>

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

### <span data-ttu-id="3972a-134">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="3972a-134">-PacketCaptureName</span></span>
<span data-ttu-id="3972a-135">패킷 캡처 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3972a-135">The packet capture name.</span></span>

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

### <span data-ttu-id="3972a-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3972a-136">-ResourceGroupName</span></span>
<span data-ttu-id="3972a-137">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3972a-137">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="3972a-138">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="3972a-138">-StorageAccountId</span></span>
<span data-ttu-id="3972a-139">저장소 계정 Id.</span><span class="sxs-lookup"><span data-stu-id="3972a-139">Storage account Id.</span></span>

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

### <span data-ttu-id="3972a-140">-StoragePath</span><span class="sxs-lookup"><span data-stu-id="3972a-140">-StoragePath</span></span>
<span data-ttu-id="3972a-141">저장소 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="3972a-141">Storage path.</span></span>

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

### <span data-ttu-id="3972a-142">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="3972a-142">-TargetVirtualMachineId</span></span>
<span data-ttu-id="3972a-143">대상 가상 컴퓨터 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3972a-143">The target virtual machine ID.</span></span>

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

### <span data-ttu-id="3972a-144">-TimeLimitInSeconds</span><span class="sxs-lookup"><span data-stu-id="3972a-144">-TimeLimitInSeconds</span></span>
<span data-ttu-id="3972a-145">시간 제한 (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="3972a-145">Time limit in seconds.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3972a-146">-TotalBytesPerSession</span><span class="sxs-lookup"><span data-stu-id="3972a-146">-TotalBytesPerSession</span></span>
<span data-ttu-id="3972a-147">세션당 총 바이트 수.</span><span class="sxs-lookup"><span data-stu-id="3972a-147">Total bytes per session.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3972a-148">-확인</span><span class="sxs-lookup"><span data-stu-id="3972a-148">-Confirm</span></span>
<span data-ttu-id="3972a-149">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3972a-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3972a-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3972a-150">-WhatIf</span></span>
<span data-ttu-id="3972a-151">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3972a-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3972a-152">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3972a-152">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3972a-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3972a-153">CommonParameters</span></span>
<span data-ttu-id="3972a-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3972a-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3972a-155">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3972a-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3972a-156">입력</span><span class="sxs-lookup"><span data-stu-id="3972a-156">INPUTS</span></span>

### <span data-ttu-id="3972a-157">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3972a-157">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="3972a-158">시스템. 문자열 시스템. \` \[ \[ Int32, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = b77a5c561934e089\]\]</span><span class="sxs-lookup"><span data-stu-id="3972a-158">System.String System.Nullable\`1\[\[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089\]\]</span></span>

## <span data-ttu-id="3972a-159">출력</span><span class="sxs-lookup"><span data-stu-id="3972a-159">OUTPUTS</span></span>

### <span data-ttu-id="3972a-160">Microsoft. \* PSPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3972a-160">Microsoft.Azure.Commands.Network.Models.PSPacketCapture</span></span>

## <span data-ttu-id="3972a-161">상속자</span><span class="sxs-lookup"><span data-stu-id="3972a-161">NOTES</span></span>
<span data-ttu-id="3972a-162">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 패킷, 캡처, 트래픽</span><span class="sxs-lookup"><span data-stu-id="3972a-162">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span> 

## <span data-ttu-id="3972a-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3972a-163">RELATED LINKS</span></span>

[<span data-ttu-id="3972a-164">새로운 AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="3972a-164">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="3972a-165">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3972a-165">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3972a-166">제거-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3972a-166">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3972a-167">중지-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="3972a-167">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="3972a-168">새로운 AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3972a-168">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="3972a-169">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3972a-169">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="3972a-170">제거-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="3972a-170">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="3972a-171">테스트-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="3972a-171">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="3972a-172">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="3972a-172">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="3972a-173">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="3972a-173">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="3972a-174">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="3972a-174">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="3972a-175">시작-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="3972a-175">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)


