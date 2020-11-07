---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Stop-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: c4d31de526132974defc6b3d28542e1ec8de4c67
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876520"
---
# <span data-ttu-id="a94fd-101">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a94fd-101">Stop-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="a94fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a94fd-102">SYNOPSIS</span></span>
<span data-ttu-id="a94fd-103">실행 중인 패킷 캡처 세션을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="a94fd-103">Stops a running packet capture session</span></span>

## <span data-ttu-id="a94fd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a94fd-104">SYNTAX</span></span>

### <span data-ttu-id="a94fd-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="a94fd-105">SetByResource (Default)</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a94fd-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="a94fd-106">SetByName</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a94fd-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a94fd-107">DESCRIPTION</span></span>
<span data-ttu-id="a94fd-108">Stop-AzNetworkWatcherPacketCapture 실행 중인 패킷 캡처 세션을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="a94fd-108">The Stop-AzNetworkWatcherPacketCapture stops a running packet capture session.</span></span> <span data-ttu-id="a94fd-109">세션을 중지 한 후에는 해당 구성에 따라 패킷 캡처 파일이 저장소에 업로드 되거나 VM에 로컬로 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a94fd-109">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="a94fd-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a94fd-110">EXAMPLES</span></span>

### <span data-ttu-id="a94fd-111">---예제 1: 패킷 캡처 세션 중지---</span><span class="sxs-lookup"><span data-stu-id="a94fd-111">--- Example 1: Stop a packet capture session ---</span></span>
```
Stop-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="a94fd-112">이 예제에서는 "PacketCaptureTest" 라는 실행 되는 패킷 캡처 세션을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="a94fd-112">In this example we stop a running packet capture session named "PacketCaptureTest".</span></span> <span data-ttu-id="a94fd-113">세션을 중지 한 후에는 해당 구성에 따라 패킷 캡처 파일이 저장소에 업로드 되거나 VM에 로컬로 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a94fd-113">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="a94fd-114">변수</span><span class="sxs-lookup"><span data-stu-id="a94fd-114">PARAMETERS</span></span>

### <span data-ttu-id="a94fd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a94fd-115">-AsJob</span></span>
<span data-ttu-id="a94fd-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="a94fd-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a94fd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a94fd-117">-DefaultProfile</span></span>
<span data-ttu-id="a94fd-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a94fd-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a94fd-119">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a94fd-119">-NetworkWatcher</span></span>
<span data-ttu-id="a94fd-120">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="a94fd-120">The network watcher resource.</span></span>

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

### <span data-ttu-id="a94fd-121">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="a94fd-121">-NetworkWatcherName</span></span>
<span data-ttu-id="a94fd-122">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a94fd-122">The name of network watcher.</span></span>

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

### <span data-ttu-id="a94fd-123">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="a94fd-123">-PacketCaptureName</span></span>
<span data-ttu-id="a94fd-124">패킷 캡처 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a94fd-124">The packet capture name.</span></span>

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

### <span data-ttu-id="a94fd-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a94fd-125">-PassThru</span></span>
<span data-ttu-id="a94fd-126">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="a94fd-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="a94fd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a94fd-127">-ResourceGroupName</span></span>
<span data-ttu-id="a94fd-128">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a94fd-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="a94fd-129">-확인</span><span class="sxs-lookup"><span data-stu-id="a94fd-129">-Confirm</span></span>
<span data-ttu-id="a94fd-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a94fd-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a94fd-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a94fd-131">-WhatIf</span></span>
<span data-ttu-id="a94fd-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a94fd-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a94fd-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a94fd-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a94fd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a94fd-134">CommonParameters</span></span>
<span data-ttu-id="a94fd-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a94fd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a94fd-136">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a94fd-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a94fd-137">입력</span><span class="sxs-lookup"><span data-stu-id="a94fd-137">INPUTS</span></span>

### <span data-ttu-id="a94fd-138">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a94fd-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="a94fd-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a94fd-139">System.String</span></span>

## <span data-ttu-id="a94fd-140">출력</span><span class="sxs-lookup"><span data-stu-id="a94fd-140">OUTPUTS</span></span>

### <span data-ttu-id="a94fd-141">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="a94fd-141">System.Boolean</span></span>

## <span data-ttu-id="a94fd-142">상속자</span><span class="sxs-lookup"><span data-stu-id="a94fd-142">NOTES</span></span>
<span data-ttu-id="a94fd-143">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 패킷, 캡처, 트래픽</span><span class="sxs-lookup"><span data-stu-id="a94fd-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="a94fd-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a94fd-144">RELATED LINKS</span></span>

[<span data-ttu-id="a94fd-145">새로운 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a94fd-145">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a94fd-146">새로운 AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="a94fd-146">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="a94fd-147">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a94fd-147">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a94fd-148">제거-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a94fd-148">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="a94fd-149">새로운 AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a94fd-149">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="a94fd-150">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a94fd-150">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="a94fd-151">제거-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="a94fd-151">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="a94fd-152">테스트-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="a94fd-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="a94fd-153">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="a94fd-153">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="a94fd-154">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="a94fd-154">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="a94fd-155">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="a94fd-155">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="a94fd-156">시작-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="a94fd-156">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)
