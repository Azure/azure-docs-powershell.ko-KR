---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 7B2D9768-919B-4F54-BBC7-8882CC2C973A
online version: ''
schema: 2.0.0
ms.openlocfilehash: a9ce55e573881a29291085e9bf25381170bbf052
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046371"
---
# Get-AzureAutomationAccount

## SYNOPSIS

Azure Automation 계정을 가져옵니다.

## 구문과

```
Get-AzureAutomationAccount [-Name <String>] [-Location <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## 설명은

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

**Get-AzureAutomationAccount** cmdlet은 구독에 대 한 Microsoft Azure Automation 계정을 가져옵니다.
Automation 계정은 다른 자동화 계정의 리소스에서 격리 된 자동화 리소스에 대 한 컨테이너입니다.
자동화 리소스에는 runbook, 작업, 자산 등이 포함 됩니다.

## 예제의

### 예제 1: Automation 계정 가져오기
```
PS C:\> Get-AzureAutomationAccount -Name "Contoso17"
```

이 명령은 Contoso17 이라는 자동화 계정을 가져옵니다.

## 변수

### -위치
자동화 계정과 연결 된 Azure 위치를 지정 합니다.

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

### -이름
Azure Automation 계정의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: False
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

### Microsoft Azure. *.

## 상속자

## 관련 링크

[새-AzureAutomationAccount](./New-AzureAutomationAccount.md)

[-AzureAutomationAccount 제거](./Remove-AzureAutomationAccount.md)


