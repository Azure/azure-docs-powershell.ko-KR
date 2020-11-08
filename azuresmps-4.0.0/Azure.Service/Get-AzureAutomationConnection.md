---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: DD881317-7366-4B55-B1CC-6AF0286F1C5D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 69ef6fc78280180a3722492e5a4b53a52c7bde2a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046370"
---
# Get-AzureAutomationConnection

## SYNOPSIS

Azure Automation 연결을 가져옵니다.

## 구문과

### ByAll (기본값)
```
Get-AzureAutomationConnection -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByConnectionName
```
Get-AzureAutomationConnection -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### ByConnectionTypeName
```
Get-AzureAutomationConnection -ConnectionTypeName <String> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

**Get-AzureAutomationConnection** cmdlet은 하나 이상의 Microsoft Azure Automation 연결을 가져옵니다.
기본적으로 모든 연결이 반환 됩니다.
특정 연결을 얻으려면 해당 이름을 지정 합니다.
특정 유형의 모든 연결을 얻으려면 연결 형식 이름을 지정 합니다.

## 예제의

### 예제 1: 모든 연결 가져오기
```
PS C:\> Get-AzureAutomationConnection -AutomationAccountName "Contoso17"
```

이 명령은 Contoso17 이라는 자동화 계정에 있는 모든 연결을 가져옵니다.

### 예제 2: 형식의 모든 연결 가져오기
```
PS C:\> Get-AzureAutomationConnection -AutomationAccountName "Contoso17" -ConnectionTypeName "Azure"
```

이 명령은 Contoso17 이라는 자동화 계정에 있는 모든 Azure 연결을 가져옵니다.

### 예제 3: 연결 하기
```
PS C:\> Get-AzureAutomationConnection -AutomationAccountName "Contoso17" -Name "Azure"
```

이 명령은 MyConnection 이라는 연결을 가져옵니다.

## 변수

### -AutomationAccountName
검색할 연결이 있는 automation 계정의 이름을 지정 합니다.

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

### -ConnectionTypeName
검색할 연결의 연결 형식 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: ByConnectionTypeName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -이름
검색할 연결의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: ByConnectionName
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

### Microsoft. Azure. 연결

## 상속자

## 관련 링크

[새-AzureAutomationConnection](./New-AzureAutomationConnection.md)

[-AzureAutomationConnection 제거](./Remove-AzureAutomationConnection.md)

[Set-AzureAutomationConnectionFieldValue](./Set-AzureAutomationConnectionFieldValue.md)


