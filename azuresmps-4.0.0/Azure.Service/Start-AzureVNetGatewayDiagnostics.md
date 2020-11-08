---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 9FCECA04-9855-461C-9470-85312993C4B1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5bb7bb3e708720b481edc4489d858c70736eac95
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046026"
---
# Start-AzureVNetGatewayDiagnostics

## SYNOPSIS
VPN 게이트웨이에 대 한 게이트웨이 진단을 시작 합니다.

## 구문과

```
Start-AzureVNetGatewayDiagnostics -VNetName <String> -CaptureDurationInSeconds <Int32>
 [-ContainerName <String>] -StorageContext <AzureStorageContext> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## 설명은
**시작-Azurevnet2| 진단** cmdlet은 가상 개인 네트워크 (VPN) 게이트웨이에 대 한 새 게이트웨이 진단 세션을 시작 합니다.
게이트웨이 진단 세션은 한 번에 하나만 실행할 수 있습니다.
게이트웨이 진단 세션이 실행 되는 동안이 cmdlet을 실행 하면이 cmdlet은 오류를 반환 합니다.

## 예제의

## 변수

### -CaptureDurationInSeconds
캡처 지속 시간 (초)을 지정 합니다.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContainerName
Azure 컨테이너의 이름을 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 컨테이너에 결과를 저장 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -프로필
이 cmdlet이 읽는 Azure 프로필을 지정 합니다. 프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageContext
Azure 저장소 컨텍스트를 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 저장소 컨텍스트를 사용 하 여 결과를 저장 합니다.

```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VNetName
이 cmdlet이 진단 유틸리티를 실행 하는 가상 네트워크 게이트웨이를 포함 하는 가상 네트워크를 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

## 상속자

## 관련 링크

[Get-Azurevnet게이트웨이 진단](./Get-AzureVNetGatewayDiagnostics.md)

[중지-Azurevnet2| 진단](./Stop-AzureVNetGatewayDiagnostics.md)


