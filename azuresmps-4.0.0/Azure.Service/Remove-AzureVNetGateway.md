---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 3E6EF9B8-9709-4E59-A1E5-78CDA4EAAE1B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88dcd2f4bad149396d58948d3d656defdf055104
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045490"
---
# Remove-AzureVNetGateway

## SYNOPSIS
VPN 게이트웨이를 삭제 합니다.

## 구문과

```
Remove-AzureVNetGateway -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**제거-AzureVNetGateway** cmdlet은 가상 네트워크에 대 한 기존 VPN (가상 사설망) 게이트웨이를 삭제 합니다.

## 예제의

### 예제 1: 가상 네트워크 게이트웨이 제거
```
PS C:\> Remove-AzureVNetGateway -VNetName "ContosoVN07"
```

이 명령은 ContosoVN07 이라는 가상 네트워크에서 가상 네트워크 게이트웨이를 제거 합니다.

## 변수

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

### -VNetName
이 cmdlet이 VPN 게이트웨이를 삭제 하는 가상 네트워크를 지정 합니다.

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

[Get-AzureVNetGateway](./Get-AzureVNetGateway.md)

[새-AzureVNetGateway](./New-AzureVNetGateway.md)

[Reset-AzureVNetGateway](./Reset-AzureVNetGateway.md)

[크기 조정-AzureVNetGateway](./Resize-AzureVNetGateway.md)

[Set-Azurevnet2| Key](./Set-AzureVNetGatewayKey.md)


