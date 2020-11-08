---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 0AED21E8-A638-4019-9B23-447472E56C7A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 202066cfc2649b0f56810123e211bbeb5d69720f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045670"
---
# Get-AzureApplicationGateway

## SYNOPSIS
응용 프로그램 게이트웨이를 가져옵니다.

## 구문과

```
Get-AzureApplicationGateway [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**Get-AzureApplicationGateway** cmdlet은 기존 Azure Application gateway를 가져옵니다.

## 예제의

### 예제 1: 응용 프로그램 게이트웨이 가져오기
```
PS C:\> Get-AzureApplicationGateway -Name "ApplicationGateway06"
```

이 명령은 ApplicationGateway06 이라는 응용 프로그램 게이트웨이를 가져옵니다.

### 예제 2: 모든 응용 프로그램 게이트웨이 가져오기
```
PS C:\> Get-AzureApplicationGateway
```

이 명령은 구독 하는 모든 응용 프로그램 게이트웨이를 가져옵니다.

## 변수

### -이름
이 cmdlet이 가져오는 응용 프로그램 게이트웨이의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
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

### Microsoft. 네트워킹과. i m m. i m a m a i m a m a i m a i<. i m a i m a i m a i m/ApplicationGateway object>

## 상속자

## 관련 링크

[새 AzureApplicationGateway](./New-AzureApplicationGateway.md)

[-AzureApplicationGateway 제거](./Remove-AzureApplicationGateway.md)

[시작-AzureApplicationGateway](./Start-AzureApplicationGateway.md)

[Stop-AzureApplicationGateway](./Stop-AzureApplicationGateway.md)

[업데이트-AzureApplicationGateway](./Update-AzureApplicationGateway.md)


