---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkwatcherconfigflowlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzNetworkWatcherConfigFlowLog.md
ms.openlocfilehash: f250615837f4953f63a4c5ff5f0a0ea965691856
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876562"
---
# <span data-ttu-id="870d0-101">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="870d0-101">Set-AzNetworkWatcherConfigFlowLog</span></span>

## <span data-ttu-id="870d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="870d0-102">SYNOPSIS</span></span>
<span data-ttu-id="870d0-103">대상 리소스에 대 한 흐름 로깅을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="870d0-103">Configures flow logging for a target resource.</span></span>

## <span data-ttu-id="870d0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="870d0-104">SYNTAX</span></span>

### <span data-ttu-id="870d0-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="870d0-105">SetByResource (Default)</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher <PSNetworkWatcher> -TargetResourceId <String>
 -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>] [-RetentionInDays <Int32>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="870d0-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="870d0-106">SetByName</span></span>
```
Set-AzNetworkWatcherConfigFlowLog -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> -EnableFlowLog <Boolean> -StorageAccountId <String> [-EnableRetention <Boolean>]
 [-RetentionInDays <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="870d0-107">설명은</span><span class="sxs-lookup"><span data-stu-id="870d0-107">DESCRIPTION</span></span>
<span data-ttu-id="870d0-108">Set-AzNetworkWatcherConfigFlowLog는 대상 리소스에 대 한 흐름 로깅을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="870d0-108">The Set-AzNetworkWatcherConfigFlowLog configures flow logging for a target resource.</span></span> <span data-ttu-id="870d0-109">구성할 속성에는 제공 된 리소스에 대해 흐름 로깅이 설정 되어 있는지 여부, 로그를 보낼 구성 된 저장소 계정, 로그에 대 한 보존 정책 등이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="870d0-109">Properties to configure include: whether or not flow logging is enabled for the resource provided, the configured storage account to send logs, and the retention policy for the logs.</span></span> <span data-ttu-id="870d0-110">현재 네트워크 보안 그룹은 유동 로깅에 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="870d0-110">Currently Network Security Groups are supported for flow logging.</span></span> 

## <span data-ttu-id="870d0-111">예제의</span><span class="sxs-lookup"><span data-stu-id="870d0-111">EXAMPLES</span></span>

### <span data-ttu-id="870d0-112">---예제 1: 지정 된 NSG---에 대 한 흐름 로깅 구성</span><span class="sxs-lookup"><span data-stu-id="870d0-112">--- Example 1: Configure Flow Logging for a Specified NSG ---</span></span>
```
PS C:\> $NW = Get-AzNetworkWatcher -ResourceGroupName NetworkWatcherRg -Name NetworkWatcher_westcentralus
PS C:\> $nsg = Get-AzNetworkSecurityGroup -ResourceGroupName NSGRG -Name appNSG
PS C:\> $storageId = "/subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123"


PS C:\> Set-AzNetworkWatcherConfigFlowLog -NetworkWatcher $NW -TargetResourceId $nsg.Id -EnableFlowLog $true -StorageAccountId $storageID

TargetResourceId : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Network/networkSecurityGroups/appNSG
StorageId        : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NSGRG/providers/Microsoft.Storage/storageAccounts/contosostorageacct123
Enabled          : True
RetentionPolicy  : {
                     "Days": 0,
                     "Enabled": false
                   }
```

<span data-ttu-id="870d0-113">이 예제에서는 네트워크 보안 그룹에 대 한 흐름 로깅 상태를 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="870d0-113">In this example we configure flow logging status for a Network Security Group.</span></span> <span data-ttu-id="870d0-114">응답에서 지정 된 NSG에 흐름 로깅이 설정 되어 있고 보존 정책이 설정 되지 않은 것을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="870d0-114">In the response, we see the specified NSG has flow logging enabled, and no retention policy set.</span></span>

## <span data-ttu-id="870d0-115">변수</span><span class="sxs-lookup"><span data-stu-id="870d0-115">PARAMETERS</span></span>

### <span data-ttu-id="870d0-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="870d0-116">-AsJob</span></span>
<span data-ttu-id="870d0-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="870d0-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="870d0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="870d0-118">-DefaultProfile</span></span>
<span data-ttu-id="870d0-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="870d0-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="870d0-120">-EnableFlowLog</span><span class="sxs-lookup"><span data-stu-id="870d0-120">-EnableFlowLog</span></span>
<span data-ttu-id="870d0-121">흐름 로깅을 사용 하거나 사용 하지 않도록 설정 하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="870d0-121">Flag to enable/disable flow logging.</span></span>

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

### <span data-ttu-id="870d0-122">-EnableRetention</span><span class="sxs-lookup"><span data-stu-id="870d0-122">-EnableRetention</span></span>
<span data-ttu-id="870d0-123">보존을 설정/해제 하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="870d0-123">Flag to enable/disable retention.</span></span>

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

### <span data-ttu-id="870d0-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="870d0-124">-NetworkWatcher</span></span>
<span data-ttu-id="870d0-125">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="870d0-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="870d0-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="870d0-126">-NetworkWatcherName</span></span>
<span data-ttu-id="870d0-127">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="870d0-127">The name of network watcher.</span></span>

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

### <span data-ttu-id="870d0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="870d0-128">-ResourceGroupName</span></span>
<span data-ttu-id="870d0-129">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="870d0-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="870d0-130">-보존 기간</span><span class="sxs-lookup"><span data-stu-id="870d0-130">-RetentionInDays</span></span>
<span data-ttu-id="870d0-131">흐름 로그 기록을 유지할 일 수입니다.</span><span class="sxs-lookup"><span data-stu-id="870d0-131">Number of days to retain flow log records.</span></span>

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

### <span data-ttu-id="870d0-132">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="870d0-132">-StorageAccountId</span></span>
<span data-ttu-id="870d0-133">흐름 로그를 저장 하는 데 사용 되는 저장소 계정의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="870d0-133">ID of the storage account which is used to store the flow log.</span></span>

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

### <span data-ttu-id="870d0-134">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="870d0-134">-TargetResourceId</span></span>
<span data-ttu-id="870d0-135">대상 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="870d0-135">The target resource ID.</span></span>

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

### <span data-ttu-id="870d0-136">-확인</span><span class="sxs-lookup"><span data-stu-id="870d0-136">-Confirm</span></span>
<span data-ttu-id="870d0-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="870d0-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="870d0-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="870d0-138">-WhatIf</span></span>
<span data-ttu-id="870d0-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="870d0-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="870d0-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="870d0-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="870d0-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="870d0-141">CommonParameters</span></span>
<span data-ttu-id="870d0-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="870d0-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="870d0-143">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="870d0-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="870d0-144">입력</span><span class="sxs-lookup"><span data-stu-id="870d0-144">INPUTS</span></span>

### <span data-ttu-id="870d0-145">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="870d0-145">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="870d0-146">시스템. i i a 시스템. Int32</span><span class="sxs-lookup"><span data-stu-id="870d0-146">System.String System.Boolean System.Int32</span></span>

## <span data-ttu-id="870d0-147">출력</span><span class="sxs-lookup"><span data-stu-id="870d0-147">OUTPUTS</span></span>

### <span data-ttu-id="870d0-148">Microsoft. 네트워크 모델. PSFlowLog</span><span class="sxs-lookup"><span data-stu-id="870d0-148">Microsoft.Azure.Commands.Network.Models.PSFlowLog</span></span>

## <span data-ttu-id="870d0-149">상속자</span><span class="sxs-lookup"><span data-stu-id="870d0-149">NOTES</span></span>
<span data-ttu-id="870d0-150">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 감시자, 흐름, 로그, flowlog, 로깅</span><span class="sxs-lookup"><span data-stu-id="870d0-150">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, flow, logs, flowlog, logging</span></span>

## <span data-ttu-id="870d0-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="870d0-151">RELATED LINKS</span></span>

[<span data-ttu-id="870d0-152">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="870d0-152">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="870d0-153">새로운 AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="870d0-153">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="870d0-154">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="870d0-154">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="870d0-155">제거-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="870d0-155">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="870d0-156">새로운 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="870d0-156">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="870d0-157">새로운 AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="870d0-157">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="870d0-158">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="870d0-158">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="870d0-159">제거-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="870d0-159">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="870d0-160">중지-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="870d0-160">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="870d0-161">테스트-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="870d0-161">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="870d0-162">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="870d0-162">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="870d0-163">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="870d0-163">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="870d0-164">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="870d0-164">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="870d0-165">시작-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="870d0-165">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="870d0-166">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="870d0-166">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)
