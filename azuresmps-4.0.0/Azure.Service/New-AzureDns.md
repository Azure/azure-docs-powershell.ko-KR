---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1085388B-0855-4E29-9043-3FE2C638F58D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 22c97045cb5f85256ec4d252cdbfb13c59643008
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045924"
---
# New-AzureDns

## SYNOPSIS
Azure DNS settings 개체를 만듭니다.

## 구문과

```
New-AzureDns [-Name] <String> [-IPAddress] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## 설명은
**새로운 azuredns** Cmdlet은 Azure dns 설정 개체를 만듭니다.
**새 add-azurevm** cmdlet을 사용 하 여 가상 컴퓨터를 만들 때 DNS 설정 개체를 사용할 수 있습니다.

## 예제의

### 예제 1: DNS 설정 개체 만들기
```
PS C:\> $Dns = New-AzureDns -Name "Dns01" -IPAddress "10.1.2.4"
```

이 명령은 Azure DNS 설정 개체를 만듭니다.
DNS 서버에는 지정 된 주소와 친근 한 이름 Dns01 있습니다.
이 명령은 **새 add-azurevm** cmdlet에서 사용할 개체를 $Dns 변수에 저장 합니다.

## 변수

### -InformationAction
이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.

이 매개 변수에 허용 되는 값은 다음과 같습니다.

- 하기로
- 숨기기
- Inquire
- SilentlyContinue
- 중지가
- 대기

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
정보 변수를 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IPAddress
DNS 서버의 IP 주소를 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -이름
DNS 서버에 대 한 친숙 한 이름을 지정 합니다.
이 이름은 완전히 정규화 된 도메인 이름이 아닐 수도 있습니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
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

[추가-AzureDns](./Add-AzureDns.md)

[Get-AzureDns](./Get-AzureDns.md)

[뉴욕](./New-AzureVM.md)

[-AzureDns 제거](./Remove-AzureDns.md)

[Set-AzureDns](./Set-AzureDns.md)


