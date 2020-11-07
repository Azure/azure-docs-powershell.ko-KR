---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/stop-azurermnetworkwatcherpacketcapture
schema: 2.0.0
ms.openlocfilehash: 5f2b2bf738c4e83f8f8f3854e831601ea23c7d8e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880914"
---
# <span data-ttu-id="5e5dc-101">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5e5dc-101">Stop-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="5e5dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e5dc-102">SYNOPSIS</span></span>
<span data-ttu-id="5e5dc-103">실행 중인 패킷 캡처 세션을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e5dc-103">Stops a running packet capture session</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e5dc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5e5dc-104">SYNTAX</span></span>

### <span data-ttu-id="5e5dc-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="5e5dc-105">SetByResource (Default)</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e5dc-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="5e5dc-106">SetByName</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e5dc-107">설명은</span><span class="sxs-lookup"><span data-stu-id="5e5dc-107">DESCRIPTION</span></span>
<span data-ttu-id="5e5dc-108">Stop-AzureRmNetworkWatcherPacketCapture 실행 중인 패킷 캡처 세션을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e5dc-108">The Stop-AzureRmNetworkWatcherPacketCapture stops a running packet capture session.</span></span> <span data-ttu-id="5e5dc-109">세션을 중지 한 후에는 해당 구성에 따라 패킷 캡처 파일이 저장소에 업로드 되거나 VM에 로컬로 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e5dc-109">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="5e5dc-110">예제의</span><span class="sxs-lookup"><span data-stu-id="5e5dc-110">EXAMPLES</span></span>

### <span data-ttu-id="5e5dc-111">---예제 1: 패킷 캡처 세션 중지---</span><span class="sxs-lookup"><span data-stu-id="5e5dc-111">--- Example 1: Stop a packet capture session ---</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="5e5dc-112">이 예제에서는 "PacketCaptureTest" 라는 실행 되는 패킷 캡처 세션을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e5dc-112">In this example we stop a running packet capture session named "PacketCaptureTest".</span></span> <span data-ttu-id="5e5dc-113">세션을 중지 한 후에는 해당 구성에 따라 패킷 캡처 파일이 저장소에 업로드 되거나 VM에 로컬로 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5e5dc-113">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="5e5dc-114">변수</span><span class="sxs-lookup"><span data-stu-id="5e5dc-114">PARAMETERS</span></span>

### <span data-ttu-id="5e5dc-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5e5dc-115">-AsJob</span></span>
<span data-ttu-id="5e5dc-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="5e5dc-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5e5dc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e5dc-117">-DefaultProfile</span></span>
<span data-ttu-id="5e5dc-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5e5dc-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e5dc-119">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5e5dc-119">-NetworkWatcher</span></span>
<span data-ttu-id="5e5dc-120">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="5e5dc-120">The network watcher resource.</span></span>

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

### <span data-ttu-id="5e5dc-121">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="5e5dc-121">-NetworkWatcherName</span></span>
<span data-ttu-id="5e5dc-122">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5e5dc-122">The name of network watcher.</span></span>

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

### <span data-ttu-id="5e5dc-123">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="5e5dc-123">-PacketCaptureName</span></span>
<span data-ttu-id="5e5dc-124">패킷 캡처 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5e5dc-124">The packet capture name.</span></span>

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

### <span data-ttu-id="5e5dc-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5e5dc-125">-PassThru</span></span>
<span data-ttu-id="5e5dc-126">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="5e5dc-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="5e5dc-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e5dc-127">-ResourceGroupName</span></span>
<span data-ttu-id="5e5dc-128">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5e5dc-128">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="5e5dc-129">-확인</span><span class="sxs-lookup"><span data-stu-id="5e5dc-129">-Confirm</span></span>
<span data-ttu-id="5e5dc-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e5dc-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e5dc-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e5dc-131">-WhatIf</span></span>
<span data-ttu-id="5e5dc-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5e5dc-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e5dc-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5e5dc-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e5dc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e5dc-134">CommonParameters</span></span>
<span data-ttu-id="5e5dc-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e5dc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e5dc-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e5dc-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e5dc-137">입력</span><span class="sxs-lookup"><span data-stu-id="5e5dc-137">INPUTS</span></span>

### <span data-ttu-id="5e5dc-138">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5e5dc-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="5e5dc-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5e5dc-139">System.String</span></span>

## <span data-ttu-id="5e5dc-140">출력</span><span class="sxs-lookup"><span data-stu-id="5e5dc-140">OUTPUTS</span></span>

### <span data-ttu-id="5e5dc-141">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="5e5dc-141">System.Boolean</span></span>

## <span data-ttu-id="5e5dc-142">상속자</span><span class="sxs-lookup"><span data-stu-id="5e5dc-142">NOTES</span></span>
<span data-ttu-id="5e5dc-143">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 패킷, 캡처, 트래픽</span><span class="sxs-lookup"><span data-stu-id="5e5dc-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="5e5dc-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5e5dc-144">RELATED LINKS</span></span>

[<span data-ttu-id="5e5dc-145">새로운 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5e5dc-145">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5e5dc-146">새로운 AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="5e5dc-146">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="5e5dc-147">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5e5dc-147">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5e5dc-148">제거-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5e5dc-148">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5e5dc-149">새로운 AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5e5dc-149">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="5e5dc-150">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5e5dc-150">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="5e5dc-151">제거-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5e5dc-151">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="5e5dc-152">테스트-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="5e5dc-152">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="5e5dc-153">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="5e5dc-153">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="5e5dc-154">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="5e5dc-154">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="5e5dc-155">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="5e5dc-155">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="5e5dc-156">시작-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="5e5dc-156">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
