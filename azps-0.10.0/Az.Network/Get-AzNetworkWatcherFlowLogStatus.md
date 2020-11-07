---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherflowlogstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherFlowLogStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherFlowLogStatus.md
ms.openlocfilehash: 2f855175065f743bdfec5fb8dc9c917af262b05b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875547"
---
# <span data-ttu-id="56f28-101">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="56f28-101">Get-AzNetworkWatcherFlowLogStatus</span></span>

## <span data-ttu-id="56f28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56f28-102">SYNOPSIS</span></span>
<span data-ttu-id="56f28-103">리소스에 대 한 흐름 로깅의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="56f28-103">Gets the status of flow logging on a resource.</span></span>

## <span data-ttu-id="56f28-104">구문과</span><span class="sxs-lookup"><span data-stu-id="56f28-104">SYNTAX</span></span>

### <span data-ttu-id="56f28-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="56f28-105">SetByResource (Default)</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56f28-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="56f28-106">SetByName</span></span>
```
Get-AzNetworkWatcherFlowLogStatus -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56f28-107">설명은</span><span class="sxs-lookup"><span data-stu-id="56f28-107">DESCRIPTION</span></span>
<span data-ttu-id="56f28-108">Get-AzNetworkWatcherFlowLogStatus cmdlet은 리소스에 대 한 흐름 로깅의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="56f28-108">The Get-AzNetworkWatcherFlowLogStatus cmdlet Gets the status of flow logging on a resource.</span></span> <span data-ttu-id="56f28-109">상태에는 제공 된 리소스에 대해 흐름 로깅이 사용 되는지 여부, 로그를 보낼 구성 된 저장소 계정, 로그에 대 한 보존 정책이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="56f28-109">The status includes whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="56f28-110">현재 네트워크 보안 그룹은 유동 로깅에 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="56f28-110">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="56f28-111">예제의</span><span class="sxs-lookup"><span data-stu-id="56f28-111">EXAMPLES</span></span>

### <span data-ttu-id="56f28-112">---예제 1: 지정 된 NSG에 대 한 흐름 로깅 상태 가져오기---</span><span class="sxs-lookup"><span data-stu-id="56f28-112">--- Example 1: Get the Flow Logging Status for a Specified NSG ---</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG

PS C:\> Get-AzNetworkWatcherFlowLogStatus -NetworkWatcher $NW -TargetResourceId $nsg.Id

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
Properties       : {
                     "Enabled": true,
                     "RetentionPolicy": {
                       "Days": 0,
                       "Enabled": false
                     },
                     "StorageId": "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"
                   }
```

<span data-ttu-id="56f28-113">이 예제에서는 네트워크 보안 그룹에 대 한 흐름 로깅 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="56f28-113">In this example we get the flow logging status for a Network Security Group.</span></span> <span data-ttu-id="56f28-114">지정 된 NSG에 흐름 로깅이 설정 되어 있으며 보존 정책이 설정 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="56f28-114">The specified NSG has flow logging enabled, and no retention policy set.</span></span>

## <span data-ttu-id="56f28-115">변수</span><span class="sxs-lookup"><span data-stu-id="56f28-115">PARAMETERS</span></span>

### <span data-ttu-id="56f28-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="56f28-116">-AsJob</span></span>
<span data-ttu-id="56f28-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="56f28-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="56f28-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56f28-118">-DefaultProfile</span></span>
<span data-ttu-id="56f28-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="56f28-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56f28-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="56f28-120">-NetworkWatcher</span></span>
<span data-ttu-id="56f28-121">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="56f28-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="56f28-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="56f28-122">-NetworkWatcherName</span></span>
<span data-ttu-id="56f28-123">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="56f28-123">The name of network watcher.</span></span>

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

### <span data-ttu-id="56f28-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56f28-124">-ResourceGroupName</span></span>
<span data-ttu-id="56f28-125">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="56f28-125">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="56f28-126">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="56f28-126">-TargetResourceId</span></span>
<span data-ttu-id="56f28-127">대상 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="56f28-127">The target resource ID.</span></span>

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

### <span data-ttu-id="56f28-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56f28-128">CommonParameters</span></span>
<span data-ttu-id="56f28-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="56f28-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56f28-130">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56f28-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56f28-131">입력</span><span class="sxs-lookup"><span data-stu-id="56f28-131">INPUTS</span></span>

### <span data-ttu-id="56f28-132">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="56f28-132">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="56f28-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="56f28-133">System.String</span></span>

## <span data-ttu-id="56f28-134">출력</span><span class="sxs-lookup"><span data-stu-id="56f28-134">OUTPUTS</span></span>

### <span data-ttu-id="56f28-135">Microsoft. 네트워크 모델. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="56f28-135">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="56f28-136">상속자</span><span class="sxs-lookup"><span data-stu-id="56f28-136">NOTES</span></span>
<span data-ttu-id="56f28-137">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 감시자, 흐름, 로그, flowlog, 로깅</span><span class="sxs-lookup"><span data-stu-id="56f28-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="56f28-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="56f28-138">RELATED LINKS</span></span>

[<span data-ttu-id="56f28-139">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="56f28-139">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="56f28-140">새로운 AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="56f28-140">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="56f28-141">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="56f28-141">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="56f28-142">제거-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="56f28-142">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="56f28-143">새로운 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="56f28-143">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="56f28-144">새로운 AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="56f28-144">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="56f28-145">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="56f28-145">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="56f28-146">제거-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="56f28-146">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="56f28-147">중지-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="56f28-147">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="56f28-148">테스트-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="56f28-148">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="56f28-149">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="56f28-149">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="56f28-150">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="56f28-150">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="56f28-151">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="56f28-151">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="56f28-152">시작-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="56f28-152">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="56f28-153">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="56f28-153">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)
