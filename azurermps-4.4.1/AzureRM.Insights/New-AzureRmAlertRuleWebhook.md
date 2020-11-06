---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 0137ECA3-37E1-4064-8A65-A582519E9017
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleWebhook.md
ms.openlocfilehash: ed8b8fe18e6320a297635b09089ff95bd52fe1e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536391"
---
# New-AzureRmAlertRuleWebhook

## SYNOPSIS
알림 규칙 webhook을 만듭니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
New-AzureRmAlertRuleWebhook [-ServiceUri] <String> [[-Properties] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzureRmAlertRuleWebhook** cmdlet은 알림 규칙 webhook을 만듭니다.

## 예제의

### 예제 1: 알림 규칙 webhook 만들기
```
PS C:\>New-AzureRmAlertRuleWebhook -ServiceUri "http://contoso.com"
```

이 명령은 서비스 URI만 지정 하 여 알림 규칙 webhook을 만듭니다.

### 예제 2: 하나의 속성을 사용 하 여 webhook 만들기
```
PS C:\>$Actual = New-AzureRmAlertRuleWebhook -ServiceUri "http://contoso.com" -Properties @{prop1 = 'value1'}
```

이 명령은 하나의 속성이 있는 Contoso.com에 대 한 알림 규칙 webhook을 만든 다음이를 $Actual 변수에 저장 합니다.

## 변수

### -속성
@ (Property1 = ' value1 ',.... 형식으로 속성 목록을 지정 합니다.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceUri
서비스 URI를 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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

### RuleWebhookAction를 통해 관리 합니다.

## 상속자

## 관련 링크

[추가-AzureRmLogAlertRule](./Add-AzureRmLogAlertRule.md)

[추가-AzureRmMetricAlertRule](./Add-AzureRmMetricAlertRule.md)

[추가-AzureRmWebtestAlertRule](./Add-AzureRmWebtestAlertRule.md)

[새로운 AzureRmAlertRuleEmail](./New-AzureRmAlertRuleEmail.md)

[새로운 AzureRmAutoscaleWebhook](./New-AzureRmAutoscaleWebhook.md)


