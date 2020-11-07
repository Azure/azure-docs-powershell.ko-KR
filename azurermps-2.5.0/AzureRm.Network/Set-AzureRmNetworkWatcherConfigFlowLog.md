---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkwatcherconfigflowlog
schema: 2.0.0
ms.openlocfilehash: e8e8462ded1f122a050c85877e8e82b2ecc0dd9d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880638"
---
# <span data-ttu-id="b13ad-101">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="b13ad-101">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>

## <span data-ttu-id="b13ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b13ad-102">SYNOPSIS</span></span>
<span data-ttu-id="b13ad-103">대상 리소스에 대 한 흐름 로깅을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b13ad-103">Configures flow logging for a target resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b13ad-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b13ad-104">SYNTAX</span></span>

### <span data-ttu-id="b13ad-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="b13ad-105">SetByResource (Default)</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b13ad-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="b13ad-106">SetByName</span></span>
```
Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b13ad-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b13ad-107">DESCRIPTION</span></span>
<span data-ttu-id="b13ad-108">Set-AzureRmNetworkWatcherConfigFlowLog는 대상 리소스에 대 한 흐름 로깅을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b13ad-108">The Set-AzureRmNetworkWatcherConfigFlowLog configures flow logging for a target resource.</span></span> <span data-ttu-id="b13ad-109">구성할 속성에는 제공 된 리소스에 대해 흐름 로깅이 설정 되어 있는지 여부, 로그를 보낼 구성 된 저장소 계정, 로그에 대 한 보존 정책 등이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b13ad-109">Properties to configure include: whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="b13ad-110">현재 네트워크 보안 그룹은 유동 로깅에 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b13ad-110">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="b13ad-111">예제의</span><span class="sxs-lookup"><span data-stu-id="b13ad-111">EXAMPLES</span></span>

### <span data-ttu-id="b13ad-112">---예제 1: 지정 된 NSG---에 대 한 흐름 로깅 구성</span><span class="sxs-lookup"><span data-stu-id="b13ad-112">--- Example 1: Configure Flow Logging for a Specified NSG ---</span></span>
```
PS C:\> $NW = Get-AzurermNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzureRmNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"


PS C:\> Set-AzureRmNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
```

<span data-ttu-id="b13ad-113">이 예제에서는 네트워크 보안 그룹에 대 한 흐름 로깅 상태를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b13ad-113">In this example we configure flow logging status for a Network Security Group.</span></span> <span data-ttu-id="b13ad-114">응답에서 지정 된 NSG에 흐름 로깅이 설정 되어 있고 보존 정책이 설정 되지 않은 것을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b13ad-114">In the response, we see the specified NSG has flow logging enabled, and no retention policy set.</span></span>

## <span data-ttu-id="b13ad-115">변수</span><span class="sxs-lookup"><span data-stu-id="b13ad-115">PARAMETERS</span></span>

### <span data-ttu-id="b13ad-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b13ad-116">-AsJob</span></span>
<span data-ttu-id="b13ad-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="b13ad-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b13ad-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b13ad-118">-DefaultProfile</span></span>
<span data-ttu-id="b13ad-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b13ad-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b13ad-120">-EnableFlowLog</span><span class="sxs-lookup"><span data-stu-id="b13ad-120">-EnableFlowLog</span></span>
<span data-ttu-id="b13ad-121">흐름 로깅을 사용 하거나 사용 하지 않도록 설정 하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="b13ad-121">Flag to enable/disable flow logging.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b13ad-122">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="b13ad-122">-EnableRetention</span></span>
<span data-ttu-id="b13ad-123">보존을 설정/해제 하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="b13ad-123">Flag to enable/disable retention.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b13ad-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b13ad-124">-NetworkWatcher</span></span>
<span data-ttu-id="b13ad-125">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="b13ad-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="b13ad-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="b13ad-126">-NetworkWatcherName</span></span>
<span data-ttu-id="b13ad-127">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b13ad-127">The name of network watcher.</span></span>

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

### <span data-ttu-id="b13ad-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b13ad-128">-ResourceGroupName</span></span>
<span data-ttu-id="b13ad-129">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b13ad-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="b13ad-130">-보존 기간</span><span class="sxs-lookup"><span data-stu-id="b13ad-130">-RetentionInDays</span></span>
<span data-ttu-id="b13ad-131">흐름 로그 기록을 유지할 일 수입니다.</span><span class="sxs-lookup"><span data-stu-id="b13ad-131">Number of days to retain flow log records.</span></span>

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

### <span data-ttu-id="b13ad-132">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="b13ad-132">-StorageAccountId</span></span>
<span data-ttu-id="b13ad-133">흐름 로그를 저장 하는 데 사용 되는 저장소 계정의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b13ad-133">ID of the storage account which is used to store the flow log.</span></span>

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

### <span data-ttu-id="b13ad-134">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="b13ad-134">-TargetResourceId</span></span>
<span data-ttu-id="b13ad-135">대상 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b13ad-135">The target resource ID.</span></span>

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

### <span data-ttu-id="b13ad-136">-확인</span><span class="sxs-lookup"><span data-stu-id="b13ad-136">-Confirm</span></span>
<span data-ttu-id="b13ad-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b13ad-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b13ad-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b13ad-138">-WhatIf</span></span>
<span data-ttu-id="b13ad-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b13ad-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b13ad-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b13ad-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b13ad-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b13ad-141">CommonParameters</span></span>
<span data-ttu-id="b13ad-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b13ad-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b13ad-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b13ad-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b13ad-144">입력</span><span class="sxs-lookup"><span data-stu-id="b13ad-144">INPUTS</span></span>

### <span data-ttu-id="b13ad-145">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b13ad-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="b13ad-146">시스템. i i a 시스템. Int32</span><span class="sxs-lookup"><span data-stu-id="b13ad-146">System.String System.Boolean System.Int32</span></span>

## <span data-ttu-id="b13ad-147">출력</span><span class="sxs-lookup"><span data-stu-id="b13ad-147">OUTPUTS</span></span>

### <span data-ttu-id="b13ad-148">Microsoft. 네트워크 모델. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="b13ad-148">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="b13ad-149">상속자</span><span class="sxs-lookup"><span data-stu-id="b13ad-149">NOTES</span></span>
<span data-ttu-id="b13ad-150">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 감시자, 흐름, 로그, flowlog, 로깅</span><span class="sxs-lookup"><span data-stu-id="b13ad-150">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="b13ad-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b13ad-151">RELATED LINKS</span></span>

[<span data-ttu-id="b13ad-152">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="b13ad-152">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="b13ad-153">새로운 AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b13ad-153">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="b13ad-154">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b13ad-154">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="b13ad-155">제거-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b13ad-155">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="b13ad-156">새로운 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b13ad-156">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b13ad-157">새로운 AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="b13ad-157">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="b13ad-158">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b13ad-158">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b13ad-159">제거-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b13ad-159">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b13ad-160">중지-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b13ad-160">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b13ad-161">테스트-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="b13ad-161">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="b13ad-162">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="b13ad-162">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="b13ad-163">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="b13ad-163">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="b13ad-164">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="b13ad-164">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="b13ad-165">시작-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="b13ad-165">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="b13ad-166">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="b13ad-166">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)
