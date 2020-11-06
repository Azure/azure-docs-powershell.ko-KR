---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmNetworkWatcherPacketCapture.md
ms.openlocfilehash: 3f1206b79f8e80793106b1e294b591e21b9fb77d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527368"
---
# <span data-ttu-id="bc607-101">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bc607-101">Stop-AzureRmNetworkWatcherPacketCapture</span></span>

## <span data-ttu-id="bc607-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc607-102">SYNOPSIS</span></span>
<span data-ttu-id="bc607-103">실행 중인 패킷 캡처 세션을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc607-103">Stops a running packet capture session</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc607-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bc607-104">SYNTAX</span></span>

### <span data-ttu-id="bc607-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="bc607-105">SetByResource (Default)</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcher <PSNetworkWatcher> -PacketCaptureName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc607-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="bc607-106">SetByName</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcherName <String> -ResourceGroupName <String>
 -PacketCaptureName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bc607-107">설명은</span><span class="sxs-lookup"><span data-stu-id="bc607-107">DESCRIPTION</span></span>
<span data-ttu-id="bc607-108">Stop-AzureRmNetworkWatcherPacketCapture 실행 중인 패킷 캡처 세션을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc607-108">The Stop-AzureRmNetworkWatcherPacketCapture stops a running packet capture session.</span></span> <span data-ttu-id="bc607-109">세션을 중지 한 후에는 해당 구성에 따라 패킷 캡처 파일이 저장소에 업로드 되거나 VM에 로컬로 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bc607-109">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="bc607-110">예제의</span><span class="sxs-lookup"><span data-stu-id="bc607-110">EXAMPLES</span></span>

### <span data-ttu-id="bc607-111">---예제 1: 패킷 캡처 세션 중지---</span><span class="sxs-lookup"><span data-stu-id="bc607-111">--- Example 1: Stop a packet capture session ---</span></span>
```
Stop-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -PacketCaptureName "PacketCaptureTest"
```

<span data-ttu-id="bc607-112">이 예제에서는 "PacketCaptureTest" 라는 실행 되는 패킷 캡처 세션을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc607-112">In this example we stop a running packet capture session named "PacketCaptureTest".</span></span> <span data-ttu-id="bc607-113">세션을 중지 한 후에는 해당 구성에 따라 패킷 캡처 파일이 저장소에 업로드 되거나 VM에 로컬로 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bc607-113">After the session is stopped, the packet capture file is uploaded to storage and/or saved locally on the VM depending on its configuration.</span></span>

## <span data-ttu-id="bc607-114">변수</span><span class="sxs-lookup"><span data-stu-id="bc607-114">PARAMETERS</span></span>

### <span data-ttu-id="bc607-115">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bc607-115">-NetworkWatcher</span></span>
<span data-ttu-id="bc607-116">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="bc607-116">The network watcher resource.</span></span>

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

### <span data-ttu-id="bc607-117">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="bc607-117">-NetworkWatcherName</span></span>
<span data-ttu-id="bc607-118">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bc607-118">The name of network watcher.</span></span>

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

### <span data-ttu-id="bc607-119">-PacketCaptureName</span><span class="sxs-lookup"><span data-stu-id="bc607-119">-PacketCaptureName</span></span>
<span data-ttu-id="bc607-120">패킷 캡처 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bc607-120">The packet capture name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc607-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bc607-121">-PassThru</span></span>
<span data-ttu-id="bc607-122">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="bc607-122">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="bc607-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc607-123">-ResourceGroupName</span></span>
<span data-ttu-id="bc607-124">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bc607-124">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="bc607-125">-확인</span><span class="sxs-lookup"><span data-stu-id="bc607-125">-Confirm</span></span>
<span data-ttu-id="bc607-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc607-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bc607-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc607-127">-WhatIf</span></span>
<span data-ttu-id="bc607-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="bc607-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc607-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bc607-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bc607-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc607-130">-DefaultProfile</span></span>
<span data-ttu-id="bc607-131">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bc607-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bc607-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc607-132">CommonParameters</span></span>
<span data-ttu-id="bc607-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc607-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc607-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc607-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc607-135">입력</span><span class="sxs-lookup"><span data-stu-id="bc607-135">INPUTS</span></span>

### <span data-ttu-id="bc607-136">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bc607-136">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="bc607-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="bc607-137">System.String</span></span>

## <span data-ttu-id="bc607-138">출력</span><span class="sxs-lookup"><span data-stu-id="bc607-138">OUTPUTS</span></span>

### <span data-ttu-id="bc607-139">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="bc607-139">System.Boolean</span></span>

## <span data-ttu-id="bc607-140">상속자</span><span class="sxs-lookup"><span data-stu-id="bc607-140">NOTES</span></span>
<span data-ttu-id="bc607-141">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 패킷, 캡처, 트래픽</span><span class="sxs-lookup"><span data-stu-id="bc607-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, packet, capture, traffic</span></span>

## <span data-ttu-id="bc607-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bc607-142">RELATED LINKS</span></span>

[<span data-ttu-id="bc607-143">새로운 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bc607-143">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bc607-144">새로운 AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="bc607-144">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="bc607-145">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bc607-145">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bc607-146">제거-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bc607-146">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bc607-147">새로운 AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bc607-147">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="bc607-148">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bc607-148">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="bc607-149">제거-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bc607-149">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="bc607-150">테스트-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="bc607-150">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="bc607-151">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="bc607-151">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="bc607-152">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="bc607-152">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="bc607-153">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="bc607-153">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="bc607-154">시작-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="bc607-154">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
