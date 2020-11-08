---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 128AD64D-709A-4B59-B233-4221A9120AE1
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4803fd24952066c4dcea72daaf0c999b64ae4c5d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046497"
---
# Remove-AzureApplicationGateway

## SYNOPSIS
응용 프로그램 게이트웨이를 제거 합니다.

## 구문과

```
Remove-AzureApplicationGateway -Name <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**제거-AzureApplicationGateway** cmdlet은 응용 프로그램 게이트웨이를 제거 합니다.

## 예제의

### 예제 1: 응용 프로그램 게이트웨이 제거
```
PS C:\> Remove-AzureApplicationGateway -Name "ApplicationGateway06"
```

이 명령은 ApplicationGateway06 이라는 응용 프로그램 게이트웨이를 제거 합니다.

## 변수

### -이름
이 cmdlet이 제거 하는 응용 프로그램 게이트웨이의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### System. 문자열

## 출력

### WindowsAzure의. i a m a 관리 응답

## 상속자

## 관련 링크

[Get-AzureApplicationGateway](./Get-AzureApplicationGateway.md)

[새 AzureApplicationGateway](./New-AzureApplicationGateway.md)

[시작-AzureApplicationGateway](./Start-AzureApplicationGateway.md)

[Stop-AzureApplicationGateway](./Stop-AzureApplicationGateway.md)

[업데이트-AzureApplicationGateway](./Update-AzureApplicationGateway.md)


