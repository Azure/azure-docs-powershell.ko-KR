---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: 7f9417fe4ad6e115e73502e953dfcab965ccd17b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527391"
---
# <span data-ttu-id="fcc49-101">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fcc49-101">Remove-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="fcc49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fcc49-102">SYNOPSIS</span></span>
<span data-ttu-id="fcc49-103">패킷 캡처 리소스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcc49-103">Removes a packet capture resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fcc49-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fcc49-104">SYNTAX</span></span>

### <span data-ttu-id="fcc49-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="fcc49-105">SetByResource (Default)</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcc49-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="fcc49-106">SetByName</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fcc49-107">설명은</span><span class="sxs-lookup"><span data-stu-id="fcc49-107">DESCRIPTION</span></span>
<span data-ttu-id="fcc49-108">Remove-AzureRmNetworkWatcherPacketCapture는 패킷 캡처 리소스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcc49-108">The Remove-AzureRmNetworkWatcherPacketCapture removes a packet capture resource.</span></span> <span data-ttu-id="fcc49-109">Remove-AzureRmNetworkWatcherPacketCapture를 호출 하기 전에 Stop-AzureRmNetworkWatcherPacketCapture를 호출 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="fcc49-109">It is recommended to call Stop-AzureRmNetworkWatcherPacketCapture before calling Remove-AzureRmNetworkWatcherPacketCapture.</span></span> <span data-ttu-id="fcc49-110">Remove-AzureRmNetworkWatcherPacketCapture를 호출할 때 패킷 캡처 세션을 실행 중인 경우 패킷 캡처는 저장 되지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fcc49-110">If the packet capture session is running when Remove-AzureRmNetworkWatcherPacketCapture is called the packet capture may not be saved.</span></span> <span data-ttu-id="fcc49-111">제거 하기 전에 세션이 중지 된 경우 캡처 데이터를 포함 하는 cap 파일은 제거 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fcc49-111">If the session is stopped prior to removal the .cap file containing capture data is not removed.</span></span> 

## <span data-ttu-id="fcc49-112">예제의</span><span class="sxs-lookup"><span data-stu-id="fcc49-112">EXAMPLES</span></span>

### <span data-ttu-id="fcc49-113">---예제 1: 패킷 캡처 세션 제거--</span><span class="sxs-lookup"><span data-stu-id="fcc49-113">--- Example 1: Remove a packet capture session --</span></span>
```
Remove-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="fcc49-114">이 예제에서는 "PacketCaptureTest" 이라는 기존 패킷 캡처 세션을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcc49-114">In this example we remove an existing packet capture session named "PacketCaptureTest".</span></span>

## <span data-ttu-id="fcc49-115">변수</span><span class="sxs-lookup"><span data-stu-id="fcc49-115">PARAMETERS</span></span>

### <span data-ttu-id="fcc49-116">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fcc49-116">-NetworkWatcher</span></span>
<span data-ttu-id="fcc49-117">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="fcc49-117">The network watcher resource.</span></span>

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

### <span data-ttu-id="fcc49-118">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="fcc49-118">-NetworkWatcherName</span></span>
<span data-ttu-id="fcc49-119">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fcc49-119">The name of network watcher.</span></span>

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

### <span data-ttu-id="fcc49-120">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="fcc49-120">-PacketCaptureName</span></span>
<span data-ttu-id="fcc49-121">패킷 캡처 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fcc49-121">The packet capture name.</span></span>

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

### <span data-ttu-id="fcc49-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fcc49-122">-PassThru</span></span>
<span data-ttu-id="fcc49-123">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="fcc49-123">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcc49-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcc49-124">-ResourceGroupName</span></span>
<span data-ttu-id="fcc49-125">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fcc49-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="fcc49-126">-확인</span><span class="sxs-lookup"><span data-stu-id="fcc49-126">-Confirm</span></span>
<span data-ttu-id="fcc49-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcc49-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcc49-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcc49-128">-WhatIf</span></span>
<span data-ttu-id="fcc49-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fcc49-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fcc49-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fcc49-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcc49-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcc49-131">-DefaultProfile</span></span>
<span data-ttu-id="fcc49-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fcc49-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fcc49-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcc49-133">CommonParameters</span></span>
<span data-ttu-id="fcc49-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcc49-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcc49-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcc49-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcc49-136">입력</span><span class="sxs-lookup"><span data-stu-id="fcc49-136">INPUTS</span></span>

### <span data-ttu-id="fcc49-137">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fcc49-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="fcc49-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fcc49-138">System.String</span></span>

## <span data-ttu-id="fcc49-139">출력</span><span class="sxs-lookup"><span data-stu-id="fcc49-139">OUTPUTS</span></span>

### <span data-ttu-id="fcc49-140">System. 개체</span><span class="sxs-lookup"><span data-stu-id="fcc49-140">System.Object</span></span>

## <span data-ttu-id="fcc49-141">상속자</span><span class="sxs-lookup"><span data-stu-id="fcc49-141">NOTES</span></span>
<span data-ttu-id="fcc49-142">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 패킷, 캡처, 트래픽, 제거</span><span class="sxs-lookup"><span data-stu-id="fcc49-142">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic, remove</span></span>

## <span data-ttu-id="fcc49-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fcc49-143">RELATED LINKS</span></span>

[<span data-ttu-id="fcc49-144">새로운 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fcc49-144">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="fcc49-145">새로운 AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="fcc49-145">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="fcc49-146">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fcc49-146">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="fcc49-147">중지-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fcc49-147">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="fcc49-148">새로운 AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fcc49-148">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="fcc49-149">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fcc49-149">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="fcc49-150">제거-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="fcc49-150">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="fcc49-151">테스트-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="fcc49-151">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="fcc49-152">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="fcc49-152">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="fcc49-153">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="fcc49-153">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="fcc49-154">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="fcc49-154">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="fcc49-155">시작-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="fcc49-155">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
