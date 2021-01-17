---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/invoke-aznetworkwatchernetworkconfigurationdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic.md
ms.openlocfilehash: 5a1500554c1026b591faea63074ca9c12fef1b10
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371855"
---
# <span data-ttu-id="2f27e-101">Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic</span><span class="sxs-lookup"><span data-stu-id="2f27e-101">Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic</span></span>

## <span data-ttu-id="2f27e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f27e-102">SYNOPSIS</span></span>
<span data-ttu-id="2f27e-103">대상 리소스에서 지정된 네트워크 프로필에 대한 네트워크 구성 진단 세션을 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="2f27e-103">Invoke network configuration diagnostic session for specified network profiles on target resource.</span></span>

## <span data-ttu-id="2f27e-104">구문</span><span class="sxs-lookup"><span data-stu-id="2f27e-104">SYNTAX</span></span>

### <span data-ttu-id="2f27e-105">SetByResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="2f27e-105">SetByResource (Default)</span></span>
```
Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -NetworkWatcher <PSNetworkWatcher>
 -TargetResourceId <String> [-VerbosityLevel <String>]
 -Profile <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f27e-106">SetByName</span><span class="sxs-lookup"><span data-stu-id="2f27e-106">SetByName</span></span>
```
Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -NetworkWatcherName <String> -ResourceGroupName <String>
 -TargetResourceId <String> [-VerbosityLevel <String>]
 -Profile <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f27e-107">SetByLocation</span><span class="sxs-lookup"><span data-stu-id="2f27e-107">SetByLocation</span></span>
```
Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -Location <String> -TargetResourceId <String>
 [-VerbosityLevel <String>]
 -Profile <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f27e-108">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="2f27e-108">SetByResourceId</span></span>
```
Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -ResourceId <String> -TargetResourceId <String>
 [-VerbosityLevel <String>]
 -Profile <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2f27e-109">설명</span><span class="sxs-lookup"><span data-stu-id="2f27e-109">DESCRIPTION</span></span>
<span data-ttu-id="2f27e-110">이 Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic cmdlet은 대상 리소스에서 지정된 네트워크 프로필에 대한 네트워크 구성 진단 세션을 호출합니다.</span><span class="sxs-lookup"><span data-stu-id="2f27e-110">The Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic cmdlet invoke network configuration diagnostic session for specified network profiles on target resource.</span></span>

## <span data-ttu-id="2f27e-111">예제</span><span class="sxs-lookup"><span data-stu-id="2f27e-111">EXAMPLES</span></span>

### <span data-ttu-id="2f27e-112">예제 1: VM 및 지정된 네트워크 프로필에 대한 네트워크 구성 진단 세션 호출</span><span class="sxs-lookup"><span data-stu-id="2f27e-112">Example 1: Invoke network configuration diagnostic session for VM and specified network profile</span></span>
```
PS C:\> $profile = New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile -Direction Inbound -Protocol Tcp -Source 10.1.1.4 -Destination * -DestinationPort 50
PS C:\> Invoke-AzNetworkWatcherNetworkConfigurationDiagnostic -Location eastus -TargetResourceId /subscriptions/61cc8a98-a8be-4bfe-a04e-0b461f93fe35/resourceGroups/NwRgEastUS/providers/Microsoft.Compute/virtualMachines/vm1 -Profile $profile

Results : [
            {
              "Profile": {
                "Direction": "Inbound",
                "Protocol": "Tcp",
                "Source": "10.1.1.4",
                "Destination": "*",
                "DestinationPort": "50"
              },
              "NetworkSecurityGroupResult": {
                "SecurityRuleAccessResult": "Allow",
                "EvaluatedNetworkSecurityGroups": [
                  {
                    "NetworkSecurityGroupId": "/subscriptions/61cc8a98-a8be-4bfe-a04e-0b461f93fe35/resourceGroups/clean
          upservice/providers/Microsoft.Network/networkSecurityGroups/rg-cleanupservice-nsg1",
                    "MatchedRule": {
                      "RuleName": "UserRule_Cleanuptool-Allow-4001",
                      "Action": "Allow"
                    },
                    "RulesEvaluationResult": [
                      {
                        "Name": "UserRule_Cleanuptool-Allow-100",
                        "ProtocolMatched": true,
                        "SourceMatched": false,
                        "SourcePortMatched": true,
                        "DestinationMatched": true,
                        "DestinationPortMatched": false
                      },
```

## <span data-ttu-id="2f27e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2f27e-113">PARAMETERS</span></span>

### <span data-ttu-id="2f27e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2f27e-114">-AsJob</span></span>
<span data-ttu-id="2f27e-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="2f27e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2f27e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f27e-116">-DefaultProfile</span></span>
<span data-ttu-id="2f27e-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2f27e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f27e-118">-Location</span><span class="sxs-lookup"><span data-stu-id="2f27e-118">-Location</span></span>
<span data-ttu-id="2f27e-119">네트워크 감시자 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="2f27e-119">Location of the network watcher.</span></span>

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

### <span data-ttu-id="2f27e-120">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2f27e-120">-NetworkWatcher</span></span>
<span data-ttu-id="2f27e-121">네트워크 감시자 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="2f27e-121">The network watcher resource.</span></span>

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

### <span data-ttu-id="2f27e-122">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="2f27e-122">-NetworkWatcherName</span></span>
<span data-ttu-id="2f27e-123">Network Watcher의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2f27e-123">The name of network watcher.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f27e-124">-Profile</span><span class="sxs-lookup"><span data-stu-id="2f27e-124">-Profile</span></span>
<span data-ttu-id="2f27e-125">네트워크 구성 진단 프로필 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="2f27e-125">List of network configuration diagnostic profiles.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f27e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f27e-126">-ResourceGroupName</span></span>
<span data-ttu-id="2f27e-127">Network Watcher 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2f27e-127">The name of the network watcher resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f27e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f27e-128">-ResourceId</span></span>
<span data-ttu-id="2f27e-129">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2f27e-129">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f27e-130">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="2f27e-130">-TargetResourceId</span></span>
<span data-ttu-id="2f27e-131">네트워크 구성 진단을 수행할 대상 리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2f27e-131">The ID of the target resource to perform network configuration diagnostic.</span></span>
<span data-ttu-id="2f27e-132">유효한 옵션은 VM, NetworkInterface, VMSS/NetworkInterface 및 Application Gateway입니다.</span><span class="sxs-lookup"><span data-stu-id="2f27e-132">Valid options are VM, NetworkInterface, VMSS/NetworkInterface and Application Gateway.</span></span>

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

### <span data-ttu-id="2f27e-133">-VerbosityLevel</span><span class="sxs-lookup"><span data-stu-id="2f27e-133">-VerbosityLevel</span></span>
<span data-ttu-id="2f27e-134">Verbosity 수준입니다.</span><span class="sxs-lookup"><span data-stu-id="2f27e-134">Verbosity level.</span></span>
<span data-ttu-id="2f27e-135">허용되는 값은 'Normal', 'Minimum', 'Full'입니다.</span><span class="sxs-lookup"><span data-stu-id="2f27e-135">Accepted values are 'Normal', 'Minimum', 'Full'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f27e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f27e-136">CommonParameters</span></span>
<span data-ttu-id="2f27e-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2f27e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f27e-138">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="2f27e-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f27e-139">입력</span><span class="sxs-lookup"><span data-stu-id="2f27e-139">INPUTS</span></span>

### <span data-ttu-id="2f27e-140">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2f27e-140">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

### <span data-ttu-id="2f27e-141">System.String</span><span class="sxs-lookup"><span data-stu-id="2f27e-141">System.String</span></span>

## <span data-ttu-id="2f27e-142">출력</span><span class="sxs-lookup"><span data-stu-id="2f27e-142">OUTPUTS</span></span>

### <span data-ttu-id="2f27e-143">Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticResponse</span><span class="sxs-lookup"><span data-stu-id="2f27e-143">Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticResponse</span></span>

## <span data-ttu-id="2f27e-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2f27e-144">NOTES</span></span>
<span data-ttu-id="2f27e-145">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹, 감시자, 진단, 프로필</span><span class="sxs-lookup"><span data-stu-id="2f27e-145">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, diagnostic, profile</span></span>

## <span data-ttu-id="2f27e-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2f27e-146">RELATED LINKS</span></span>

[<span data-ttu-id="2f27e-147">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2f27e-147">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="2f27e-148">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2f27e-148">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="2f27e-149">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="2f27e-149">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="2f27e-150">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="2f27e-150">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="2f27e-151">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="2f27e-151">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="2f27e-152">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="2f27e-152">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="2f27e-153">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="2f27e-153">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="2f27e-154">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2f27e-154">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2f27e-155">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="2f27e-155">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="2f27e-156">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2f27e-156">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2f27e-157">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2f27e-157">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2f27e-158">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="2f27e-158">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="2f27e-159">New-AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="2f27e-159">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="2f27e-160">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="2f27e-160">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="2f27e-161">Test-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="2f27e-161">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="2f27e-162">Stop-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2f27e-162">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2f27e-163">Start-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2f27e-163">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2f27e-164">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2f27e-164">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2f27e-165">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="2f27e-165">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="2f27e-166">Remove-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2f27e-166">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2f27e-167">New-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2f27e-167">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="2f27e-168">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="2f27e-168">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="2f27e-169">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="2f27e-169">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="2f27e-170">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="2f27e-170">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="2f27e-171">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="2f27e-171">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="2f27e-172">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="2f27e-172">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="2f27e-173">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="2f27e-173">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
