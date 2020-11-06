---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcher.md
ms.openlocfilehash: d69c4b3a21849db14d53760c8796b91399e742b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537076"
---
# Get-AzureRmNetworkWatcher

## SYNOPSIS
네트워크 감시자의 속성을 가져옵니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

### 가져오기
```
Get-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### 목록
```
Get-AzureRmNetworkWatcher [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## 설명은
Get-AzureRmNetworkWatcher cmdlet은 하나 이상의 Azure 네트워크 감시자 리소스를 가져옵니다.

## 예제의

### --------------------------예제 1: 네트워크 감시자를 가져옵니다--------------------------
```
Get-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"ac624778-0214-49b9-a04c-794863485fa6"
Location          : westcentralus
Tags              : 
ProvisioningState : Succeeded
```

리소스 그룹 NetworkWatcherRG의 NetworkWatcher_westcentralus 라는 네트워크 감시자를 가져옵니다.

## 변수

### -이름
네트워크 감시자 이름입니다.

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
리소스 그룹 이름입니다.

```yaml
Type: System.String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### 않아야

## 출력

### Microsoft. 네트워크 모델. PSNetworkWatcher

## 상속자
키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 네트워크, 네트워킹, 네트워크 감시자 

## 관련 링크

[새로운 AzureRmNetworkWatcher](./New-AzureRmNetworkWatcher.md)

[제거-AzureRmNetworkWatcher](./Remove-AzureRmNetworkWatcher.md)

[새로운 AzureRmNetworkWatcherPacketCapture](./New-AzureRmNetworkWatcherPacketCapture.md)

[새로운 AzureRmPacketCaptureFilterConfig](./New-AzureRmPacketCaptureFilterConfig.md)

[Get-AzureRmNetworkWatcherPacketCapture](./Get-AzureRmNetworkWatcherPacketCapture.md)

[제거-AzureRmNetworkWatcherPacketCapture](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[중지-AzureRmNetworkWatcherPacketCapture](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[테스트-AzureRmNetworkWatcherIPFlow](./Test-AzureRmNetworkWatcherIPFlow.md)

[Get-AzureRmNetworkWatcherNextHop](./Get-AzureRmNetworkWatcherNextHop.md)

[Get-AzureRmNetworkWatcherSecurityGroupView](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[Get-AzureRmNetworkWatcherTopology](./Get-AzureRmNetworkWatcherTopology.md)

[시작-AzureRmNetworkWatcherResourceTroubleshooting](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
