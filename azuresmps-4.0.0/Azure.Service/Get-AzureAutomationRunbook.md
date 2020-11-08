---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 304F71E0-9E89-46E6-BD25-7584601CC845
online version: ''
schema: 2.0.0
ms.openlocfilehash: e507b1b35bf8739c80bbdf92f02f29099ceb3284
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045657"
---
# Get-AzureAutomationRunbook

## SYNOPSIS

Runbook을 가져옵니다.

## 구문과

### ByAll (기본값)
```
Get-AzureAutomationRunbook -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByRunbookName
```
Get-AzureAutomationRunbook -Name <String> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## 설명은

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

**Get-AzureAutomationRunbook** cmdlet은 하나 이상의 Microsoft Azure 자동화 runbook을 가져옵니다.
기본적으로 모든 runbook이 반환 됩니다.
특정 runbook을 가져오려면 해당 이름 또는 ID를 지정 합니다.
특정 일정에 연결 된 모든 runbook을 가져오려면 일정 이름을 지정 합니다.

## 예제의

### 예제 1: 모든 runbook 가져오기
```
PS C:\> Get-AzureAutomationRunbook -AutomationAccountName "Contoso17"
```

이 명령은 Contoso17 이라는 Azure Automation 계정의 모든 runbook을 가져옵니다.

## 변수

### -AutomationAccountName
Azure Automation 계정의 이름을 지정 합니다.

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
Runbook의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: ByRunbookName
Aliases: RunbookName

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

### Microsoft. Azure. i a m. Runbook

## 상속자

## 관련 링크

[새-AzureAutomationRunbook](./New-AzureAutomationRunbook.md)

[게시-AzureAutomationRunbook](./Publish-AzureAutomationRunbook.md)

[-AzureAutomationRunbook 제거](./Remove-AzureAutomationRunbook.md)

[Set-AzureAutomationRunbook](./Set-AzureAutomationRunbook.md)

[시작-AzureAutomationRunbook](./Start-AzureAutomationRunbook.md)


