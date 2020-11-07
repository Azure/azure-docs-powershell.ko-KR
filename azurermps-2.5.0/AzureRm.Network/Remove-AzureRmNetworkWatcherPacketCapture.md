---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkwatcherpacketcapture
schema: 2.0.0
ms.openlocfilehash: eb8997025a9fa73c394c2c51c23f00c211604cb2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880637"
---
# <span data-ttu-id="32390-101">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="32390-101">Remove-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="32390-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32390-102">SYNOPSIS</span></span>
<span data-ttu-id="32390-103">패킷 캡처 리소스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="32390-103">Removes a packet capture resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32390-104">구문과</span><span class="sxs-lookup"><span data-stu-id="32390-104">SYNTAX</span></span>

### <span data-ttu-id="32390-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="32390-105">SetByResource (Default)</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="32390-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="32390-106">SetByName</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32390-107">설명은</span><span class="sxs-lookup"><span data-stu-id="32390-107">DESCRIPTION</span></span>
<span data-ttu-id="32390-108">Remove-AzureRmNetworkWatcherPacketCapture는 패킷 캡처 리소스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="32390-108">The Remove-AzureRmNetworkWatcherPacketCapture removes a packet capture resource.</span></span> <span data-ttu-id="32390-109">Remove-AzureRmNetworkWatcherPacketCapture를 호출 하기 전에 Stop-AzureRmNetworkWatcherPacketCapture를 호출 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="32390-109">It is recommended to call Stop-AzureRmNetworkWatcherPacketCapture before calling Remove-AzureRmNetworkWatcherPacketCapture.</span></span> <span data-ttu-id="32390-110">Remove-AzureRmNetworkWatcherPacketCapture를 호출할 때 패킷 캡처 세션을 실행 중인 경우 패킷 캡처는 저장 되지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="32390-110">If the packet capture session is running when Remove-AzureRmNetworkWatcherPacketCapture is called the packet capture may not be saved.</span></span> <span data-ttu-id="32390-111">제거 하기 전에 세션이 중지 된 경우 캡처 데이터를 포함 하는 cap 파일은 제거 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="32390-111">If the session is stopped prior to removal the .cap file containing capture data is not removed.</span></span> 

## <span data-ttu-id="32390-112">예제의</span><span class="sxs-lookup"><span data-stu-id="32390-112">EXAMPLES</span></span>

### <span data-ttu-id="32390-113">---예제 1: 패킷 캡처 세션 제거--</span><span class="sxs-lookup"><span data-stu-id="32390-113">--- Example 1: Remove a packet capture session --</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="32390-114">이 예제에서는 "PacketCaptureTest" 이라는 기존 패킷 캡처 세션을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="32390-114">In this example we remove an existing packet capture session named "PacketCaptureTest".</span></span>

## <span data-ttu-id="32390-115">변수</span><span class="sxs-lookup"><span data-stu-id="32390-115">PARAMETERS</span></span>

### <span data-ttu-id="32390-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="32390-116">-AsJob</span></span>
<span data-ttu-id="32390-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="32390-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="32390-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32390-118">-DefaultProfile</span></span>
<span data-ttu-id="32390-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="32390-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32390-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="32390-120">-NetworkWatcher</span></span>
<span data-ttu-id="32390-121">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="32390-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="32390-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="32390-122">-NetworkWatcherName</span></span>
<span data-ttu-id="32390-123">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="32390-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="32390-124">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="32390-124">-PacketCaptureName</span></span>
<span data-ttu-id="32390-125">패킷 캡처 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="32390-125">The packet capture name.</span></span>

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

### <span data-ttu-id="32390-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="32390-126">-PassThru</span></span>
<span data-ttu-id="32390-127">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="32390-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="32390-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32390-128">-ResourceGroupName</span></span>
<span data-ttu-id="32390-129">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="32390-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="32390-130">-확인</span><span class="sxs-lookup"><span data-stu-id="32390-130">-Confirm</span></span>
<span data-ttu-id="32390-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="32390-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32390-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32390-132">-WhatIf</span></span>
<span data-ttu-id="32390-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="32390-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32390-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="32390-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32390-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32390-135">CommonParameters</span></span>
<span data-ttu-id="32390-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="32390-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32390-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32390-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32390-138">입력</span><span class="sxs-lookup"><span data-stu-id="32390-138">INPUTS</span></span>

### <span data-ttu-id="32390-139">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="32390-139">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="32390-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="32390-140">System.String</span></span>

## <span data-ttu-id="32390-141">출력</span><span class="sxs-lookup"><span data-stu-id="32390-141">OUTPUTS</span></span>

### <span data-ttu-id="32390-142">System. 개체</span><span class="sxs-lookup"><span data-stu-id="32390-142">System.Object</span></span>

## <span data-ttu-id="32390-143">상속자</span><span class="sxs-lookup"><span data-stu-id="32390-143">NOTES</span></span>
<span data-ttu-id="32390-144">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 패킷, 캡처, 트래픽, 제거</span><span class="sxs-lookup"><span data-stu-id="32390-144">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span></span>

## <span data-ttu-id="32390-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="32390-145">RELATED LINKS</span></span>

[<span data-ttu-id="32390-146">새로운 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="32390-146">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="32390-147">새로운 AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="32390-147">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="32390-148">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="32390-148">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="32390-149">중지-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="32390-149">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="32390-150">새로운 AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="32390-150">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="32390-151">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="32390-151">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="32390-152">제거-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="32390-152">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="32390-153">테스트-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="32390-153">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="32390-154">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="32390-154">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="32390-155">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="32390-155">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="32390-156">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="32390-156">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="32390-157">시작-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="32390-157">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
