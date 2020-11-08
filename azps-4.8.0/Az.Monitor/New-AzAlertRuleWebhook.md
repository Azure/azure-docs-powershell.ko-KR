---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 0137ECA3-37E1-4064-8A65-A582519E9017
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azalertrulewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
ms.openlocfilehash: 03459cedbebaeba46331edf7aeb9a7972711912a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213480"
---
# New-AzAlertRuleWebhook

## SYNOPSIS
알림 규칙 webhook을 만듭니다.

## 구문과

```
New-AzAlertRuleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzAlertRuleWebhook** cmdlet은 알림 규칙 webhook을 만듭니다.

## 예제의

### 예제 1: 알림 규칙 webhook 만들기
```
PS C:\>New-AzAlertRuleWebhook -ServiceUri "http://contoso.com"
```

이 명령은 서비스 URI만 지정 하 여 알림 규칙 webhook을 만듭니다.

### 예제 2: 하나의 속성을 사용 하 여 webhook 만들기
```
PS C:\>$Actual = New-AzAlertRuleWebhook -ServiceUri "http://contoso.com" -Property @{prop1 = 'value1'}
```

이 명령은 하나의 속성이 있는 Contoso.com에 대 한 알림 규칙 webhook을 만든 다음이를 $Actual 변수에 저장 합니다.

## 변수

### -DefaultProfile
Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### System. 문자열

### System.webserver. 컬렉션 테이블

## 출력

### RuleWebhookAction를 통해 관리 합니다.

## 상속자

## 관련 링크

[추가-AzLogAlertRule](./Add-AzLogAlertRule.md)

[추가-AzMetricAlertRule](./Add-AzMetricAlertRule.md)

[추가-AzWebtestAlertRule](./Add-AzWebtestAlertRule.md)

[새로운 AzAlertRuleEmail](./New-AzAlertRuleEmail.md)

[새로운 AzAutoscaleWebhook](./New-AzAutoscaleWebhook.md)


