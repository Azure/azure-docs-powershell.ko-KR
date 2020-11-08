---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatchernetworkconfigurationdiagnosticprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile.md
ms.openlocfilehash: c559001c68126c42c3d4ae6eaead2beda3ded5f0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94203979"
---
# <span data-ttu-id="5b35c-101">New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile</span><span class="sxs-lookup"><span data-stu-id="5b35c-101">New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile</span></span>

## <span data-ttu-id="5b35c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b35c-102">SYNOPSIS</span></span>
<span data-ttu-id="5b35c-103">새 네트워크 구성 진단 프로필 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b35c-103">Creates a new network configuration diagnostic profile object.</span></span> <span data-ttu-id="5b35c-104">이 개체는 지정 된 기준을 사용 하 여 진단 세션 중에 네트워크 구성을 제한 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b35c-104">This object is used to restrict the network configuration during a diagnostic session using the specified criteria.</span></span>

## <span data-ttu-id="5b35c-105">구문과</span><span class="sxs-lookup"><span data-stu-id="5b35c-105">SYNTAX</span></span>

```
New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile -Direction <String> -Protocol <String>
 -Source <String> -Destination <String> -DestinationPort <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5b35c-106">설명은</span><span class="sxs-lookup"><span data-stu-id="5b35c-106">DESCRIPTION</span></span>
<span data-ttu-id="5b35c-107">New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile cmdlet은 새 진단 프로필 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b35c-107">The New-AzNetworkWatcherNetworkConfigurationDiagnosticProfile cmdlet creates a new diagnostic profile object.</span></span> <span data-ttu-id="5b35c-108">이 개체는 지정 된 기준을 사용 하 여 네트워크 구성 진단 세션 중 네트워크 구성을 제한 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5b35c-108">This object is used to restrict the network configuration during a network configuration diagnostic session using the specified criteria.</span></span>

## <span data-ttu-id="5b35c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="5b35c-109">EXAMPLES</span></span>

### <span data-ttu-id="5b35c-110">예제 1: VM 및 지정 된 네트워크 프로필에 대 한 네트워크 구성 진단 세션 호출</span><span class="sxs-lookup"><span data-stu-id="5b35c-110">Example 1: Invoke network configuration diagnostic session for VM and specified network profile</span></span>
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

## <span data-ttu-id="5b35c-111">변수</span><span class="sxs-lookup"><span data-stu-id="5b35c-111">PARAMETERS</span></span>

### <span data-ttu-id="5b35c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b35c-112">-DefaultProfile</span></span>
<span data-ttu-id="5b35c-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5b35c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b35c-114">-대상</span><span class="sxs-lookup"><span data-stu-id="5b35c-114">-Destination</span></span>
<span data-ttu-id="5b35c-115">트래픽 목적지.</span><span class="sxs-lookup"><span data-stu-id="5b35c-115">Traffic destination.</span></span>
<span data-ttu-id="5b35c-116">허용 되는 값은 ' \* ', IP 주소/CIDR, 서비스 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="5b35c-116">Accepted values are: '\*', IP Address/CIDR, Service Tag.</span></span>

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

### <span data-ttu-id="5b35c-117">-DestinationPort</span><span class="sxs-lookup"><span data-stu-id="5b35c-117">-DestinationPort</span></span>
<span data-ttu-id="5b35c-118">트래픽 대상 포트.</span><span class="sxs-lookup"><span data-stu-id="5b35c-118">Traffic destination port.</span></span>
<span data-ttu-id="5b35c-119">허용 되는 값은 ' \* ', 포트 (예: 3389) 및 포트 범위 (예: 80-100)입니다.</span><span class="sxs-lookup"><span data-stu-id="5b35c-119">Accepted values are '\*', port (for example, 3389) and port range (for example, 80-100).</span></span>

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

### <span data-ttu-id="5b35c-120">방향</span><span class="sxs-lookup"><span data-stu-id="5b35c-120">-Direction</span></span>
<span data-ttu-id="5b35c-121">트래픽 방향입니다.</span><span class="sxs-lookup"><span data-stu-id="5b35c-121">The direction of the traffic.</span></span>
<span data-ttu-id="5b35c-122">허용 되는 값은 ' Inbound ' 및 ' Outbound '입니다.</span><span class="sxs-lookup"><span data-stu-id="5b35c-122">Accepted values are 'Inbound' and 'Outbound'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b35c-123">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="5b35c-123">-Protocol</span></span>
<span data-ttu-id="5b35c-124">확인할 프로토콜입니다.</span><span class="sxs-lookup"><span data-stu-id="5b35c-124">Protocol to be verified on.</span></span>
<span data-ttu-id="5b35c-125">허용 되는 값은 ' \* ', TCP, UDP입니다.</span><span class="sxs-lookup"><span data-stu-id="5b35c-125">Accepted values are '\*', TCP, UDP.</span></span>

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

### <span data-ttu-id="5b35c-126">-원본</span><span class="sxs-lookup"><span data-stu-id="5b35c-126">-Source</span></span>
<span data-ttu-id="5b35c-127">트래픽 원본</span><span class="sxs-lookup"><span data-stu-id="5b35c-127">Traffic source.</span></span>
<span data-ttu-id="5b35c-128">허용 되는 값은 ' \* ', IP 주소/CIDR, 서비스 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="5b35c-128">Accepted values are '\*', IP Address/CIDR, Service Tag.</span></span>

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

### <span data-ttu-id="5b35c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b35c-129">CommonParameters</span></span>
<span data-ttu-id="5b35c-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5b35c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b35c-131">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5b35c-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b35c-132">입력</span><span class="sxs-lookup"><span data-stu-id="5b35c-132">INPUTS</span></span>

### <span data-ttu-id="5b35c-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5b35c-133">System.String</span></span>

## <span data-ttu-id="5b35c-134">출력</span><span class="sxs-lookup"><span data-stu-id="5b35c-134">OUTPUTS</span></span>

### <span data-ttu-id="5b35c-135">PSNetworkConfigurationDiagnosticProfile에 대 한.</span><span class="sxs-lookup"><span data-stu-id="5b35c-135">Microsoft.Azure.Commands.Network.Models.PSNetworkConfigurationDiagnosticProfile</span></span>

## <span data-ttu-id="5b35c-136">상속자</span><span class="sxs-lookup"><span data-stu-id="5b35c-136">NOTES</span></span>
<span data-ttu-id="5b35c-137">키워드: azure, azurerm, arm, resource, 관리, 관리자, 네트워크, 네트워킹, 감시자, 진단, 프로필</span><span class="sxs-lookup"><span data-stu-id="5b35c-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, diagnostic, profile</span></span>

## <span data-ttu-id="5b35c-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5b35c-138">RELATED LINKS</span></span>

[<span data-ttu-id="5b35c-139">새로운 AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5b35c-139">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="5b35c-140">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5b35c-140">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="5b35c-141">제거-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="5b35c-141">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="5b35c-142">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="5b35c-142">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="5b35c-143">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="5b35c-143">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="5b35c-144">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="5b35c-144">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="5b35c-145">시작-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="5b35c-145">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="5b35c-146">새로운 AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5b35c-146">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5b35c-147">새로운 AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="5b35c-147">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="5b35c-148">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5b35c-148">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5b35c-149">제거-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5b35c-149">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5b35c-150">중지-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5b35c-150">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="5b35c-151">새로운 AzNetworkWatcherProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="5b35c-151">New-AzNetworkWatcherProtocolConfiguration</span></span>](./New-AzNetworkWatcherProtocolConfiguration.md)

[<span data-ttu-id="5b35c-152">테스트-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="5b35c-152">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="5b35c-153">테스트-AzNetworkWatcherConnectivity</span><span class="sxs-lookup"><span data-stu-id="5b35c-153">Test-AzNetworkWatcherConnectivity</span></span>](./Test-AzNetworkWatcherConnectivity.md)

[<span data-ttu-id="5b35c-154">중지-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5b35c-154">Stop-AzNetworkWatcherConnectionMonitor</span></span>](./Stop-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5b35c-155">시작-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5b35c-155">Start-AzNetworkWatcherConnectionMonitor</span></span>](./Start-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5b35c-156">Set-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5b35c-156">Set-AzNetworkWatcherConnectionMonitor</span></span>](./Set-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5b35c-157">Set-AzNetworkWatcherConfigFlowLog</span><span class="sxs-lookup"><span data-stu-id="5b35c-157">Set-AzNetworkWatcherConfigFlowLog</span></span>](./Set-AzNetworkWatcherConfigFlowLog.md)

[<span data-ttu-id="5b35c-158">제거-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5b35c-158">Remove-AzNetworkWatcherConnectionMonitor</span></span>](./Remove-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5b35c-159">새로운 AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5b35c-159">New-AzNetworkWatcherConnectionMonitor</span></span>](./New-AzNetworkWatcherConnectionMonitor.md)

[<span data-ttu-id="5b35c-160">Get-AzNetworkWatcherTroubleshootingResult</span><span class="sxs-lookup"><span data-stu-id="5b35c-160">Get-AzNetworkWatcherTroubleshootingResult</span></span>](./Get-AzNetworkWatcherTroubleshootingResult.md)

[<span data-ttu-id="5b35c-161">Get-AzNetworkWatcherReachabilityReport</span><span class="sxs-lookup"><span data-stu-id="5b35c-161">Get-AzNetworkWatcherReachabilityReport</span></span>](./Get-AzNetworkWatcherReachabilityReport.md)

[<span data-ttu-id="5b35c-162">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="5b35c-162">Get-AzNetworkWatcherReachabilityProvidersList</span></span>](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[<span data-ttu-id="5b35c-163">Get-AzNetworkWatcherFlowLogStatus</span><span class="sxs-lookup"><span data-stu-id="5b35c-163">Get-AzNetworkWatcherFlowLogStatus</span></span>](./Get-AzNetworkWatcherFlowLogStatus.md)

[<span data-ttu-id="5b35c-164">Get-AzNetworkWatcherConnectionMonitorReport</span><span class="sxs-lookup"><span data-stu-id="5b35c-164">Get-AzNetworkWatcherConnectionMonitorReport</span></span>](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[<span data-ttu-id="5b35c-165">Get-AzNetworkWatcherConnectionMonitor</span><span class="sxs-lookup"><span data-stu-id="5b35c-165">Get-AzNetworkWatcherConnectionMonitor</span></span>](./Get-AzNetworkWatcherConnectionMonitor)
