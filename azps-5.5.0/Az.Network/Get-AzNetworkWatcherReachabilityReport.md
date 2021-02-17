---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityreport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNetworkWatcherReachabilityReport.md
ms.openlocfilehash: f29ab593ffac847ec6b089efdc39bc594ad1d785
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100412846"
---
# Get-AzNetworkWatcherReachabilityReport

## SYNOPSIS
인터넷 서비스 공급자의 상대적 대기 시간 점수를 지정된 위치에서 Azure 지역으로 얻습니다.

## 구문

### SetByName(기본값)
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Provider <String[]>] [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>]
 [-State <String>] [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResource
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher <PSNetworkWatcher> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByResourceId
```
Get-AzNetworkWatcherReachabilityReport -ResourceId <String> [-Provider <String[]>] [-Location <String[]>]
 -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>] [-City <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SetByLocation
```
Get-AzNetworkWatcherReachabilityReport -NetworkWatcherLocation <String> [-Provider <String[]>]
 [-Location <String[]>] -StartTime <DateTime> -EndTime <DateTime> [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
이 Get-AzNetworkWatcherReachabilityReport 지정된 위치에서 Azure 지역으로 인터넷 서비스 공급자에 대한 상대적 대기 시간 점수를 얻습니다.

## 예제

### 예제 1
```powershell
$nw = Get-AzNetworkWatcher -Name NetworkWatcher -ResourceGroupName NetworkWatcherRG
Get-AzNetworkWatcherReachabilityReport -NetworkWatcher $nw -Location "West US" -Country "United States" -StartTime "2017-10-10" -EndTime "2017-10-12"

"aggregationLevel" : "Country",
"providerLocation" : {
    "country" : "United States"
},
"reachabilityReport" : [
    {
        "provider" : "Frontier Communications of America, Inc. - ASN 5650",
        "azureLocation": "West US",
        "latencies": [
            {
                "timeStamp": "2017-10-10T00:00:00Z",
                "score": 94
            },
            {
                "timeStamp": "2017-10-11T00:00:00Z",
                "score": 94
            },
            {
                "timeStamp": "2017-10-12T00:00:00Z",
                "score": 94    
            }
        ]  
    }
]
```

미국 내 2017-10-10에서 2017-10-12까지 미국 서부의 Azure 데이터 센터에 대한 상대적 대기 시간을 얻습니다.

### 예제 2

인터넷 서비스 공급자의 상대적 대기 시간 점수를 지정된 위치에서 Azure 지역으로 얻습니다. (자동 재생)

<!-- Aladdin Generated Example -->
```powershell
Get-AzNetworkWatcherReachabilityReport -Country 'United States' -EndTime '2017-10-12' -Location 'West US' -NetworkWatcherName nw1 -ResourceGroupName myresourcegroup -StartTime '2017-10-10' -State 'washington'
```

## PARAMETERS

### -AsJob
백그라운드에서 cmdlet 실행

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

### -City
도시 이름입니다.

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

### -Country
국가 이름입니다.

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

### -EndTime
Azure 도달 가능성 보고서의 종료 시간입니다.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Location
쿼리 범위를 지정하는 선택적 Azure 지역입니다.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NetworkWatcher
Network Watcher 리소스

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

### -NetworkWatcherLocation
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

### -NetworkWatcherName
Network Watcher의 이름입니다.

```yaml
Type: System.String
Parameter Sets: SetByName
Aliases: ResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Provider
인터넷 서비스 공급자 목록입니다.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
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
Network Watcher 리소스의 ID입니다.

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

### -StartTime
Azure 도달 가능성 보고서의 시작 시간입니다.

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -State
상태의 이름입니다.

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

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher

### System.String

## 출력

### Microsoft.Azure.Commands.Network.Models.PSAzureReachabilityReport

## 참고 사항
키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자, 연결 가능성, 보고서

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
