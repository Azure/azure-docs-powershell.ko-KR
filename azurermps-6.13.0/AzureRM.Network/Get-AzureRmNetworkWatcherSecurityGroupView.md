---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatchersecuritygroupview
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherSecurityGroupView.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherSecurityGroupView.md
ms.openlocfilehash: 9fe23ea5fa9bef544feae6112879cb1be6eeae7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527848"
---
# <span data-ttu-id="7b0b9-101">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="7b0b9-101">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>

## <span data-ttu-id="7b0b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b0b9-102">SYNOPSIS</span></span>
<span data-ttu-id="7b0b9-103">VM에 적용 되는 구성 된 유효 네트워크 보안 그룹 규칙을 봅니다.</span><span class="sxs-lookup"><span data-stu-id="7b0b9-103">View the configured and effective network security group rules applied on a VM.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b0b9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7b0b9-104">SYNTAX</span></span>

### <span data-ttu-id="7b0b9-105">SetByResource (기본값)</span><span class="sxs-lookup"><span data-stu-id="7b0b9-105">SetByResource (Default)</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcher <PSNetworkWatcher> -TargetVirtualMachineId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b0b9-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="7b0b9-106">SetByName</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetVirtualMachineId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b0b9-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="7b0b9-107">SetByLocation</span></span>
```
Get-AzureRmNetworkWatcherSecurityGroupView -Location <String> -TargetVirtualMachineId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b0b9-108">설명은</span><span class="sxs-lookup"><span data-stu-id="7b0b9-108">DESCRIPTION</span></span>
<span data-ttu-id="7b0b9-109">Get-AzureRmNetworkWatcherSecurityGroupView를 사용 하 여 VM에 적용 되는 구성 된 유효 네트워크 보안 그룹 규칙을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7b0b9-109">The Get-AzureRmNetworkWatcherSecurityGroupView enables you to view the configured and effective network security group rules applied on a VM.</span></span>

## <span data-ttu-id="7b0b9-110">예제의</span><span class="sxs-lookup"><span data-stu-id="7b0b9-110">EXAMPLES</span></span>

### <span data-ttu-id="7b0b9-111">예제 1: VM에서 보안 그룹 보기 호출 하기</span><span class="sxs-lookup"><span data-stu-id="7b0b9-111">Example 1: Make a Security Group View call on a VM</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 
$VM = Get-AzurermVM -ResourceGroupName ContosoResourceGroup -Name VM0 
Get-AzureRmNetworkWatcherSecurityGroupView -NetworkWatcher $networkWatcher -TargetVirtualMachineId $VM.Id
```

<span data-ttu-id="7b0b9-112">위 예제에서는 먼저 지역 네트워크 감시자를 얻은 다음 지역에서 VM을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7b0b9-112">In the above example, we first get the regional Network Watcher, then a VM in the region.</span></span> <span data-ttu-id="7b0b9-113">그런 다음 지정 된 VM에서 보안 그룹 보기 호출을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b0b9-113">Then we make a Security Group View call on the specified VM.</span></span>

## <span data-ttu-id="7b0b9-114">변수</span><span class="sxs-lookup"><span data-stu-id="7b0b9-114">PARAMETERS</span></span>

### <span data-ttu-id="7b0b9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7b0b9-115">-AsJob</span></span>
<span data-ttu-id="7b0b9-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7b0b9-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7b0b9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b0b9-117">-DefaultProfile</span></span>
<span data-ttu-id="7b0b9-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7b0b9-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b0b9-119">-위치</span><span class="sxs-lookup"><span data-stu-id="7b0b9-119">-Location</span></span>
<span data-ttu-id="7b0b9-120">네트워크 감시자의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="7b0b9-120">Location of the network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLocation
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7b0b9-121">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7b0b9-121">-NetworkWatcher</span></span>
<span data-ttu-id="7b0b9-122">네트워크 감시자 리소스.</span><span class="sxs-lookup"><span data-stu-id="7b0b9-122">The network watcher resource.</span></span>

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

### <span data-ttu-id="7b0b9-123">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="7b0b9-123">-NetworkWatcherName</span></span>
<span data-ttu-id="7b0b9-124">네트워크 감시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7b0b9-124">The name of network watcher.</span></span>

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

### <span data-ttu-id="7b0b9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b0b9-125">-ResourceGroupName</span></span>
<span data-ttu-id="7b0b9-126">네트워크 감시자 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7b0b9-126">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="7b0b9-127">-TargetVirtualMachineId</span><span class="sxs-lookup"><span data-stu-id="7b0b9-127">-TargetVirtualMachineId</span></span>
<span data-ttu-id="7b0b9-128">대상 VM Id</span><span class="sxs-lookup"><span data-stu-id="7b0b9-128">The target VM Id</span></span>

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

### <span data-ttu-id="7b0b9-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b0b9-129">CommonParameters</span></span>
<span data-ttu-id="7b0b9-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b0b9-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b0b9-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b0b9-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b0b9-132">입력</span><span class="sxs-lookup"><span data-stu-id="7b0b9-132">INPUTS</span></span>

### <span data-ttu-id="7b0b9-133">Microsoft. 네트워크 모델. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7b0b9-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="7b0b9-134">매개 변수: NetworkWatcher (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7b0b9-134">Parameters: NetworkWatcher (ByValue)</span></span>

### <span data-ttu-id="7b0b9-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7b0b9-135">System.String</span></span>
<span data-ttu-id="7b0b9-136">매개 변수: NetworkWatcherName (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7b0b9-136">Parameters: NetworkWatcherName (ByValue)</span></span>

## <span data-ttu-id="7b0b9-137">출력</span><span class="sxs-lookup"><span data-stu-id="7b0b9-137">OUTPUTS</span></span>

### <span data-ttu-id="7b0b9-138">Microsoft. 네트워크 모델. PSSecurityGroupViewResult</span><span class="sxs-lookup"><span data-stu-id="7b0b9-138">Microsoft.Azure.Commands.Network.Models.PSSecurityGroupViewResult</span></span>

## <span data-ttu-id="7b0b9-139">상속자</span><span class="sxs-lookup"><span data-stu-id="7b0b9-139">NOTES</span></span>
<span data-ttu-id="7b0b9-140">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 흐름, ip</span><span class="sxs-lookup"><span data-stu-id="7b0b9-140">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, flow, ip</span></span> 

## <span data-ttu-id="7b0b9-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7b0b9-141">RELATED LINKS</span></span>

[<span data-ttu-id="7b0b9-142">새로운 AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7b0b9-142">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="7b0b9-143">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7b0b9-143">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="7b0b9-144">제거-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7b0b9-144">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="7b0b9-145">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="7b0b9-145">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="7b0b9-146">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="7b0b9-146">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="7b0b9-147">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="7b0b9-147">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="7b0b9-148">시작-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="7b0b9-148">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="7b0b9-149">새로운 AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7b0b9-149">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7b0b9-150">새로운 AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="7b0b9-150">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="7b0b9-151">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7b0b9-151">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7b0b9-152">제거-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7b0b9-152">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7b0b9-153">중지-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7b0b9-153">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7b0b9-154">새로운 AzureRmNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="7b0b9-154">New-AzureRmNetworkWatcherProtocolConfiguration</span></span>](./New-AzureRmNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="7b0b9-155">테스트-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="7b0b9-155">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="7b0b9-156">테스트-AzureRmNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="7b0b9-156">Test-AzureRmNetworkWatcherConnectivity</span></span>](./Test-AzureRmNetworkWatcherConnectivity.md)

[<span data-ttu-id="7b0b9-157">중지-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7b0b9-157">Stop-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Stop-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7b0b9-158">시작-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7b0b9-158">Start-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Start-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7b0b9-159">Set-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7b0b9-159">Set-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Set-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7b0b9-160">Set-AzureRmNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="7b0b9-160">Set-AzureRmNetworkWatcherConfigFlowLog</span></span>](./Set-AzureRmNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="7b0b9-161">제거-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7b0b9-161">Remove-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Remove-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7b0b9-162">새로운 AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7b0b9-162">New-AzureRmNetworkWatcherConnectionMonitor</span></span>](./New-AzureRmNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="7b0b9-163">Get-AzureRmNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="7b0b9-163">Get-AzureRmNetworkWatcherTroubleshootingResult</span></span>](./Get-AzureRmNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="7b0b9-164">Get-AzureRMNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="7b0b9-164">Get-AzureRMNetworkWatcherReachabilityReport</span></span>](./Get-AzureRMNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="7b0b9-165">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="7b0b9-165">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzureRmNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="7b0b9-166">Get-AzureRmNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="7b0b9-166">Get-AzureRmNetworkWatcherFlowLogStatus</span></span>](./Get-AzureRmNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="7b0b9-167">Get-AzureRmNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="7b0b9-167">Get-AzureRmNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitorReport)

[<span data-ttu-id="7b0b9-168">Get-AzureRmNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="7b0b9-168">Get-AzureRmNetworkWatcherConnectionMonitor</span></span>](./Get-AzureRmNetworkWatcherConnectionMonitor)
