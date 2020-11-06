---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherFlowLogStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherFlowLogStatus.md
ms.openlocfilehash: 1c7e67eacc52e995632a526514c84bf7a9f45425
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533972"
---
# <span data-ttu-id="33cdc-101">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="33cdc-101">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>

## <span data-ttu-id="33cdc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33cdc-102">SYNOPSIS</span></span>
<span data-ttu-id="33cdc-103">리소스에 대 한 흐름 로깅의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="33cdc-103">Gets the status of flow logging on a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33cdc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="33cdc-104">SYNTAX</span></span>

### <span data-ttu-id="33cdc-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="33cdc-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherFlowLogStatus -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33cdc-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="33cdc-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherFlowLogStatus -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33cdc-107">설명은</span><span class="sxs-lookup"><span data-stu-id="33cdc-107">DESCRIPTION</span></span>
<span data-ttu-id="33cdc-108">Get-AzureRmNetworkWatcherFlowLogStatus cmdlet은 리소스에 대 한 흐름 로깅의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="33cdc-108">The Get-AzureRmNetworkWatcherFlowLogStatus cmdlet Gets the status of flow logging on a resource.</span></span> <span data-ttu-id="33cdc-109">상태에는 제공 된 리소스에 대해 흐름 로깅이 사용 되는지 여부, 로그를 보낼 구성 된 저장소 계정, 로그에 대 한 보존 정책이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="33cdc-109">The status includes whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="33cdc-110">현재 네트워크 보안 그룹은 유동 로깅에 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="33cdc-110">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="33cdc-111">예제의</span><span class="sxs-lookup"><span data-stu-id="33cdc-111">EXAMPLES</span></span>

### <span data-ttu-id="33cdc-112">---예제 1: 지정 된 NSG에 대 한 흐름 로깅 상태 가져오기---</span><span class="sxs-lookup"><span data-stu-id="33cdc-112">--- Example 1: Get the Flow Logging Status for a Specified NSG ---</span></span>
```
PS C:\> $NW = Get-AzurermNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzureRmNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG

PS C:\> Get-AzureRmNetworkWatcherFlowLogStatus -NetworkWatcher $NW -TargetResourceId $nsg.Id

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

<span data-ttu-id="33cdc-113">이 예제에서는 네트워크 보안 그룹에 대 한 흐름 로깅 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="33cdc-113">In this example we get the flow logging status for a Network Security Group.</span></span> <span data-ttu-id="33cdc-114">지정 된 NSG에 흐름 로깅이 설정 되어 있으며 보존 정책이 설정 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="33cdc-114">The specified NSG has flow logging enabled, and no retention policy set.</span></span>

## <span data-ttu-id="33cdc-115">변수</span><span class="sxs-lookup"><span data-stu-id="33cdc-115">PARAMETERS</span></span>

### <span data-ttu-id="33cdc-116">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="33cdc-116">-NetworkWatcher</span></span>
<span data-ttu-id="33cdc-117">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="33cdc-117">The network watcher resource.</span></span>

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

### <span data-ttu-id="33cdc-118">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="33cdc-118">-NetworkWatcherName</span></span>
<span data-ttu-id="33cdc-119">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="33cdc-119">The name of network watcher.</span></span>

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

### <span data-ttu-id="33cdc-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33cdc-120">-ResourceGroupName</span></span>
<span data-ttu-id="33cdc-121">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="33cdc-121">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="33cdc-122">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="33cdc-122">-TargetResourceId</span></span>
<span data-ttu-id="33cdc-123">대상 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="33cdc-123">The target resource ID.</span></span>

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

### <span data-ttu-id="33cdc-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33cdc-124">-DefaultProfile</span></span>
<span data-ttu-id="33cdc-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="33cdc-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33cdc-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33cdc-126">CommonParameters</span></span>
<span data-ttu-id="33cdc-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="33cdc-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33cdc-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33cdc-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33cdc-129">입력</span><span class="sxs-lookup"><span data-stu-id="33cdc-129">INPUTS</span></span>

### <span data-ttu-id="33cdc-130">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="33cdc-130">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="33cdc-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="33cdc-131">System.String</span></span>

## <span data-ttu-id="33cdc-132">출력</span><span class="sxs-lookup"><span data-stu-id="33cdc-132">OUTPUTS</span></span>

### <span data-ttu-id="33cdc-133">Microsoft. 네트워크 모델. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="33cdc-133">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="33cdc-134">상속자</span><span class="sxs-lookup"><span data-stu-id="33cdc-134">NOTES</span></span>
<span data-ttu-id="33cdc-135">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 감시자, 흐름, 로그, flowlog, 로깅</span><span class="sxs-lookup"><span data-stu-id="33cdc-135">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="33cdc-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="33cdc-136">RELATED LINKS</span></span>

[<span data-ttu-id="33cdc-137">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="33cdc-137">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="33cdc-138">새로운 AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="33cdc-138">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="33cdc-139">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="33cdc-139">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="33cdc-140">제거-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="33cdc-140">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="33cdc-141">새로운 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="33cdc-141">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="33cdc-142">새로운 AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="33cdc-142">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="33cdc-143">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="33cdc-143">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="33cdc-144">제거-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="33cdc-144">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="33cdc-145">중지-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="33cdc-145">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="33cdc-146">테스트-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="33cdc-146">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="33cdc-147">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="33cdc-147">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="33cdc-148">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="33cdc-148">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="33cdc-149">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="33cdc-149">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="33cdc-150">시작-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="33cdc-150">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="33cdc-151">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="33cdc-151">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)
