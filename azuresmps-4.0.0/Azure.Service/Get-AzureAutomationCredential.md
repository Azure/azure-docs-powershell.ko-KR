---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: C69558DB-78C3-4162-99C3-1300C3FE5287
online version: ''
schema: 2.0.0
ms.openlocfilehash: aa73cf467ffc3675b17b6c59ef5bd07483803267
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045659"
---
# Get-AzureAutomationCredential

## SYNOPSIS

Azure Automation 자격 증명을 가져옵니다.

## 구문과

### ByAll (기본값)
```
Get-AzureAutomationCredential -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByName
```
Get-AzureAutomationCredential -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## 설명은

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

**Get-AzureAutomationCredential** cmdlet은 하나 이상의 Microsoft Azure Automation 자격 증명을 가져옵니다.
기본적으로 모든 자격 증명이 반환 됩니다.
특정 자격 증명을 가져오려면 해당 이름을 지정 합니다.

## 예제의

### 예제 1: 모든 자격 증명 가져오기
```
PS C:\> Get-AzureAutomationCredential -AutomationAccountName "Contoso17"
```

이 명령은 Contoso17 이라는 자동화 계정에 있는 모든 자격 증명을 가져옵니다.

### 예제 2: 자격 증명 가져오기
```
PS C:\> Get-AzureAutomationCredential -AutomationAccountName "Contoso17" -Name "MyCredential"
```

이 명령은 MyCredential 이라는 자격 증명을 가져옵니다.

## 변수

### -AutomationAccountName
검색할 자격 증명이 있는 automation 계정의 이름을 지정 합니다.

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

### -이름
검색할 자격 증명의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -프로필
이 cmdlet이 읽는 Azure 프로필을 지정 합니다.
프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.

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

## 출력

### Microsoft Azure.. m a. 모델-.pst 정보

## 상속자

## 관련 링크

[새-AzureAutomationCredential](./New-AzureAutomationCredential.md)

[-AzureAutomationCredential 제거](./Remove-AzureAutomationCredential.md)

[Set-AzureAutomationCredential](./Set-AzureAutomationCredential.md)


