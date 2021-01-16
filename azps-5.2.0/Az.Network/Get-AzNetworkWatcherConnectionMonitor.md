---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherconnectionmonitor
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitor.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherConnectionMonitor.md
ms.openlocfilehash: c2da2b9173b3977a606699fd8e1def3dae2a68d9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335625"
---
# Get-AzNetworkWatcherConnectionMonitor

## SYNOPSIS
지정된 이름 또는 연결 모니터 목록이 있는 연결 모니터를 반환합니다.

## 구문

### SetByName(기본값)
```
Get-AzNetworkWatcherConnectionMonitor -NetworkWatcherName <String> -ResourceGroupName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResource
```
Get-AzNetworkWatcherConnectionMonitor -NetworkWatcher <PSNetworkWatcher> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByLocation
```
Get-AzNetworkWatcherConnectionMonitor -Location <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResourceId
```
Get-AzNetworkWatcherConnectionMonitor -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명
Get-AzNetworkWatcherConnectionMonitor cmdlet은 지정된 이름/resourceId 또는 지정된 네트워크 감시자/위치에 해당하는 연결 모니터 목록을 사용하여 연결 모니터를 반환합니다.

## 예제

### 예제 1
```powershell
PS C:\> Get-AzNetworkWatcherConnectionMonitor -Location centraluseuap -Name cm
```

이름 : cm Id : /subscriptions/00000000-0000-0000-0000-0000000000/resourceGro ups/NetworkWatcherRG/providers /Microsoft.Network/networkWatcher s/NetworkWatcher_centraluseuap/connectionMonitors/cm Etag : W/"40961b58-e379-4204-a47b-0c477739b095" ProvisioningState : 성공한 원본 : { "ResourceId": "/subscriptions/96e68903-0a56-4819-9987-8d08ad6 a1f99/resourceGroups/VarunRgCentralUSEUAP/providers/Microsoft.C ompute/virtualMachines/irinavm", "Port": 0 } Destination : { "Address": "google.com", "Port": 80 } MonitoringIntervalInSeconds : 60 AutoStart : True StartTime : 1/12/2018 7:19:28 PM MonitoringStatus : Stopped Location : centraluseuap Type : Microsoft.Network/networkWatchers/connectionMonitors Tags : { "key1": "value1" }

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

### -Location
네트워크 감시자 위치입니다.

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

### -Name
연결 모니터 이름입니다.

```yaml
Type: System.String
Parameter Sets: SetByName, SetByResource, SetByLocation
Aliases: ConnectionMonitorName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NetworkWatcher
네트워크 감시자 리소스입니다.

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

### -NetworkWatcherName
Network Watcher의 이름입니다.

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

### -ResourceGroupName
Network Watcher 리소스 그룹의 이름입니다.

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

### -ResourceId
리소스 ID입니다.

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

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher

### System.String

## 출력

### Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV1

### Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorResultV2

## 참고 사항

## 관련 링크
