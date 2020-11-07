---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcherpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkWatcherPacketCapture.md
ms.openlocfilehash: b3095aace7fa8e1959e51ef64aa92b6d2bcaffba
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876659"
---
# <span data-ttu-id="0cbc4-101">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0cbc4-101">Remove-AzNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="0cbc4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0cbc4-102">SYNOPSIS</span></span>
<span data-ttu-id="0cbc4-103">패킷 캡처 리소스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cbc4-103">Removes a packet capture resource.</span></span>

## <span data-ttu-id="0cbc4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0cbc4-104">SYNTAX</span></span>

### <span data-ttu-id="0cbc4-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="0cbc4-105">SetByResource (Default)</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0cbc4-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="0cbc4-106">SetByName</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0cbc4-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0cbc4-107">DESCRIPTION</span></span>
<span data-ttu-id="0cbc4-108">Remove-AzNetworkWatcherPacketCapture는 패킷 캡처 리소스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cbc4-108">The Remove-AzNetworkWatcherPacketCapture removes a packet capture resource.</span></span> <span data-ttu-id="0cbc4-109">Remove-AzNetworkWatcherPacketCapture를 호출 하기 전에 Stop-AzNetworkWatcherPacketCapture를 호출 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="0cbc4-109">It is recommended to call Stop-AzNetworkWatcherPacketCapture before calling Remove-AzNetworkWatcherPacketCapture.</span></span> <span data-ttu-id="0cbc4-110">Remove-AzNetworkWatcherPacketCapture를 호출할 때 패킷 캡처 세션을 실행 중인 경우 패킷 캡처는 저장 되지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0cbc4-110">If the packet capture session is running when Remove-AzNetworkWatcherPacketCapture is called the packet capture may not be saved.</span></span> <span data-ttu-id="0cbc4-111">제거 하기 전에 세션이 중지 된 경우 캡처 데이터를 포함 하는 cap 파일은 제거 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0cbc4-111">If the session is stopped prior to removal the .cap file containing capture data is not removed.</span></span> 

## <span data-ttu-id="0cbc4-112">예제의</span><span class="sxs-lookup"><span data-stu-id="0cbc4-112">EXAMPLES</span></span>

### <span data-ttu-id="0cbc4-113">---예제 1: 패킷 캡처 세션 제거--</span><span class="sxs-lookup"><span data-stu-id="0cbc4-113">--- Example 1: Remove a packet capture session --</span></span>
```
Remove-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="0cbc4-114">이 예제에서는 "PacketCaptureTest" 이라는 기존 패킷 캡처 세션을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cbc4-114">In this example we remove an existing packet capture session named "PacketCaptureTest".</span></span>

## <span data-ttu-id="0cbc4-115">변수</span><span class="sxs-lookup"><span data-stu-id="0cbc4-115">PARAMETERS</span></span>

### <span data-ttu-id="0cbc4-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0cbc4-116">-AsJob</span></span>
<span data-ttu-id="0cbc4-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="0cbc4-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0cbc4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0cbc4-118">-DefaultProfile</span></span>
<span data-ttu-id="0cbc4-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0cbc4-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0cbc4-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0cbc4-120">-NetworkWatcher</span></span>
<span data-ttu-id="0cbc4-121">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="0cbc4-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="0cbc4-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="0cbc4-122">-NetworkWatcherName</span></span>
<span data-ttu-id="0cbc4-123">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0cbc4-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="0cbc4-124">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="0cbc4-124">-PacketCaptureName</span></span>
<span data-ttu-id="0cbc4-125">패킷 캡처 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0cbc4-125">The packet capture name.</span></span>

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

### <span data-ttu-id="0cbc4-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0cbc4-126">-PassThru</span></span>
<span data-ttu-id="0cbc4-127">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="0cbc4-127">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cbc4-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cbc4-128">-ResourceGroupName</span></span>
<span data-ttu-id="0cbc4-129">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0cbc4-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="0cbc4-130">-확인</span><span class="sxs-lookup"><span data-stu-id="0cbc4-130">-Confirm</span></span>
<span data-ttu-id="0cbc4-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cbc4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0cbc4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0cbc4-132">-WhatIf</span></span>
<span data-ttu-id="0cbc4-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0cbc4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0cbc4-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0cbc4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0cbc4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cbc4-135">CommonParameters</span></span>
<span data-ttu-id="0cbc4-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0cbc4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cbc4-137">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cbc4-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cbc4-138">입력</span><span class="sxs-lookup"><span data-stu-id="0cbc4-138">INPUTS</span></span>

### <span data-ttu-id="0cbc4-139">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0cbc4-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="0cbc4-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0cbc4-140">System.String</span></span>

## <span data-ttu-id="0cbc4-141">출력</span><span class="sxs-lookup"><span data-stu-id="0cbc4-141">OUTPUTS</span></span>

### <span data-ttu-id="0cbc4-142">System. 개체</span><span class="sxs-lookup"><span data-stu-id="0cbc4-142">System.Object</span></span>

## <span data-ttu-id="0cbc4-143">상속자</span><span class="sxs-lookup"><span data-stu-id="0cbc4-143">NOTES</span></span>
<span data-ttu-id="0cbc4-144">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 패킷, 캡처, 트래픽, 제거</span><span class="sxs-lookup"><span data-stu-id="0cbc4-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span></span>

## <span data-ttu-id="0cbc4-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0cbc4-145">RELATED LINKS</span></span>

[<span data-ttu-id="0cbc4-146">새로운 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0cbc4-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0cbc4-147">새로운 AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="0cbc4-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="0cbc4-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0cbc4-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0cbc4-149">중지-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0cbc4-149">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0cbc4-150">새로운 AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0cbc4-150">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="0cbc4-151">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0cbc4-151">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="0cbc4-152">제거-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0cbc4-152">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="0cbc4-153">테스트-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="0cbc4-153">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="0cbc4-154">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="0cbc4-154">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="0cbc4-155">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="0cbc4-155">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="0cbc4-156">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="0cbc4-156">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="0cbc4-157">시작-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="0cbc4-157">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)
