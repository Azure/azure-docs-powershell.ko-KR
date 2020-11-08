---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 73F90276-FABD-414A-B29D-83F371C1ED21
online version: ''
schema: 2.0.0
ms.openlocfilehash: 0544b4d5fafcb388b65271e736f43a15f02980c5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046368"
---
# Get-AzureAutomationModule

## SYNOPSIS

Azure Automation 모듈을 가져옵니다.

## 구문과

### ByAll (기본값)
```
Get-AzureAutomationModule -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByName
```
Get-AzureAutomationModule -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## 설명은

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

**Get-AzureAutomationModule** cmdlet은 하나 이상의 Microsoft Azure 자동화 모듈을 가져옵니다.
기본적으로 모든 모듈이 반환 됩니다.
특정 모듈을 가져오려면 해당 이름을 지정 합니다.

## 예제의

### 예제 1: 모든 모듈 가져오기
```
PS C:\> Get-AzureAutomationModule -AutomationAccountName "Contoso17"
```

이 명령은 Contoso17 이라는 Azure Automation 계정의 모든 모듈을 가져옵니다.

### 예제 2: 모듈 가져오기
```
PS C:\> Get-AzureAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule"
```

이 명령은 Contoso17 이라는 Azure Automation 계정에서 ContosoModule 라는 모듈을 가져옵니다.

## 변수

### -AutomationAccountName
검색할 runbook이 있는 Automation 계정의 이름을 지정 합니다.

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
검색할 모듈의 이름을 지정 합니다.

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

### Microsoft Azure. 모듈별. 모듈

## 상속자

## 관련 링크

[새-AzureAutomationModule](./New-AzureAutomationModule.md)

[-AzureAutomationModule 제거](./Remove-AzureAutomationModule.md)

[Set AzureAutomationModule](./Set-AzureAutomationModule.md)


