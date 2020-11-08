---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: B4102F33-979B-4649-99F4-96A295EAE43C
online version: ''
schema: 2.0.0
ms.openlocfilehash: ddb0ac79f5164fb5c953dd1cf1efeff8391d30fd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045465"
---
# Reset-AzureVNetGateway

## SYNOPSIS
가상 네트워크 VPN 게이트웨이를 다시 설정 합니다.

## 구문과

```
Reset-AzureVNetGateway -VNetName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**Reset-AzureVNetGateway** cmdlet은 가상 개인 네트워크 (VPN) 가상 네트워크 게이트웨이를 다시 설정 하 고 다시 시작 합니다.

## 예제의

### 예제 1: 가상 네트워크 게이트웨이 다시 설정
```
PS C:\> Reset-AzureVNetGateway -VNetName "ContosoVN07"
```

이 명령은 ContosoVN07 이라는 가상 네트워크에서 가상 네트워크 게이트웨이를 재설정 합니다.

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
이 cmdlet이 다시 설정 하는 가상 네트워크 게이트웨이를 포함 하는 가상 네트워크를 지정 합니다.

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

[-AzureVNetGateway 제거](./Remove-AzureVNetGateway.md)

[크기 조정-AzureVNetGateway](./Resize-AzureVNetGateway.md)

[Set-Azurevnet2| Key](./Set-AzureVNetGatewayKey.md)


