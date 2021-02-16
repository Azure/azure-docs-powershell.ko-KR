---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpacketcapturefilterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPacketCaptureFilterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPacketCaptureFilterConfig.md
ms.openlocfilehash: d7dac006abf09ec7c80d4a7e7659405936a8d20e
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100408545"
---
# New-AzPacketCaptureFilterConfig

## SYNOPSIS
새 패킷 캡처 필터 개체를 만듭니다.

## 구문

```
New-AzPacketCaptureFilterConfig [-Protocol <String>] [-RemoteIPAddress <String>] [-LocalIPAddress <String>]
 [-LocalPort <String>] [-RemotePort <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
New-AzPacketCaptureFilterConfig cmdlet은 새 패킷 캡처 필터 개체를 만듭니다. 이 개체는 지정된 조건을 사용하여 패킷 캡처 세션 중에 캡처되는 패킷의 유형을 제한하는 데 사용됩니다. 이 New-AzNetworkWatcherPacketCapture cmdlet은 여러 필터 개체를 수락하여 구성 가능한 캡처 세션을 사용할 수 있습니다.

## 예제

### 예제 1: 여러 필터를 사용하여 패킷 캡처 만들기
```
$nw = Get-AzResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzPacketCaptureFilterConfig -Protocol UDP 
New-AzNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2
```

이 예제에서는 여러 필터와 시간 제한이 있는 "PacketCaptureTest"라는 패킷 캡처를 만듭니다. 세션이 완료되면 지정된 저장소 계정에 저장됩니다. 참고: 패킷 캡처를 만들 대상 가상 머신에 Azure Network Watcher 확장을 설치해야 합니다.

## PARAMETERS

### -DefaultProfile
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.

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

### -LocalIPAddress
필터링할 로컬 IP 주소를 지정합니다.
예제 입력: 단일 주소 항목의 경우 "127.0.0.1"입니다.
범위에 대한 "127.0.0.1-127.0.0.255"입니다.
여러 항목에 대한 "127.0.0.1;127.0.0.5;"입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LocalPort
필터링할 로컬 IP 주소를 지정합니다.
예제 입력: 단일 주소 항목의 경우 "127.0.0.1"입니다.
범위에 대한 "127.0.0.1-127.0.0.255"입니다.
여러 항목에 대한 "127.0.0.1;127.0.0.5;"입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Protocol
필터링할 프로토콜을 지정합니다. 허용되는 값 "TCP","UDP","Any"

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RemoteIPAddress
필터링할 원격 IP 주소를 지정합니다.
예제 입력: 단일 주소 항목의 경우 "127.0.0.1"입니다.
범위에 대한 "127.0.0.1-127.0.0.255"입니다.
여러 항목에 대한 "127.0.0.1;127.0.0.5;"입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RemotePort
필터링할 원격 포트를 지정합니다.
원격 포트 예제 입력: 단일 포트 항목의 경우 "80"입니다.
범위의 경우 "80-85"입니다.
여러 항목에 대한 "80;443;"입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### System.String

## 출력

### Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter

## 참고 사항
키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹, 감시자, 패킷, 캡처, 트래픽, 필터 

## 관련 링크

[New-AzNetworkWatcher](./New-AzNetworkWatcher.md)

[Get-AzNetworkWatcher](./Get-AzNetworkWatcher.md)

[Remove-AzNetworkWatcher](./Remove-AzNetworkWatcher.md)

[Get-AzNetworkWatcherNextHop](./Get-AzNetworkWatcherNextHop.md)

[Get-AzNetworkWatcherSecurityGroupView](./Get-AzNetworkWatcherSecurityGroupView.md)

[Get-AzNetworkWatcherTopology](./Get-AzNetworkWatcherTopology.md)

[Start-AzNetworkWatcherResourceTroubleshooting](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[New-AzNetworkWatcherPacketCapture](./New-AzNetworkWatcherPacketCapture.md)

[New-AzPacketCaptureFilterConfig](./New-AzPacketCaptureFilterConfig.md)

[Get-AzNetworkWatcherPacketCapture](./Get-AzNetworkWatcherPacketCapture.md)

[Remove-AzNetworkWatcherPacketCapture](./Remove-AzNetworkWatcherPacketCapture.md)

[Stop-AzNetworkWatcherPacketCapture](./Stop-AzNetworkWatcherPacketCapture.md)

[New-AzNetworkWatcherProtocolConfiguration](./New-AzNetworkWatcherProtocolConfiguration.md)

[Test-AzNetworkWatcherIPFlow](./Test-AzNetworkWatcherIPFlow.md)

[Test-AzNetworkWatcherConnectivity](./Test-AzNetworkWatcherConnectivity.md)

[Stop-AzNetworkWatcherConnectionMonitor](./Stop-AzNetworkWatcherConnectionMonitor.md)

[Start-AzNetworkWatcherConnectionMonitor](./Start-AzNetworkWatcherConnectionMonitor.md)

[Set-AzNetworkWatcherConnectionMonitor](./Set-AzNetworkWatcherConnectionMonitor.md)

[Set-AzNetworkWatcherConfigFlowLog](./Set-AzNetworkWatcherConfigFlowLog.md)

[Remove-AzNetworkWatcherConnectionMonitor](./Remove-AzNetworkWatcherConnectionMonitor.md)

[New-AzNetworkWatcherConnectionMonitor](./New-AzNetworkWatcherConnectionMonitor.md)

[Get-AzNetworkWatcherTroubleshootingResult](./Get-AzNetworkWatcherTroubleshootingResult.md)

[Get-AzNetworkWatcherReachabilityReport](./Get-AzNetworkWatcherReachabilityReport.md)

[Get-AzNetworkWatcherReachabilityProvidersList](./Get-AzNetworkWatcherReachabilityProvidersList.md)

[Get-AzNetworkWatcherFlowLogStatus](./Get-AzNetworkWatcherFlowLogStatus.md)

[Get-AzNetworkWatcherConnectionMonitorReport](./Get-AzNetworkWatcherConnectionMonitorReport.md)

[Get-AzNetworkWatcherConnectionMonitor](./Get-AzNetworkWatcherConnectionMonitor.md)
