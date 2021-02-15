---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azalertruleemail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
ms.openlocfilehash: 7d9ed01346c04974fb43d7e3b233badb7a185dc2
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100396033"
---
# New-AzAlertRuleEmail

## SYNOPSIS
경고 규칙에 대한 전자 메일 작업을 만듭니다.

## 구문

```
New-AzAlertRuleEmail [[-CustomEmail] <String[]>] [-SendToServiceOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명
**New-AzAlertRuleEmail** cmdlet은 경고 규칙에 대한 전자 메일 작업을 만듭니다.

## 예제

### 예제 1: 서비스 소유자에 대한 경고 규칙 전자 메일 작업 만들기
```
PS C:\>New-AzAlertRuleEmail -SendToServiceOwners
```

이 명령은 경고 규칙이 실행된 경우 해당 서비스 소유자에 대해 보낼 경고 규칙 전자 메일 작업을 만듭니다.

### 예제 2: 비 서비스 소유자에 대한 경고 규칙 전자 메일 작업 만들기
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.com,davidchew@contoso.net
```

이 명령은 지정된 전자 메일 주소에 대한 경고 규칙 전자 메일 작업을 만들고 서비스 소유자에 대한 작업은 만듭니다.

### 예제 3: 서비스 소유자 및 비 서비스 소유자에 대한 경고 규칙 전자 메일 작업 만들기
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.net -SendToServiceOwners
```

이 명령은 지정된 주소 및 해당 서비스 소유자에 대한 경고 규칙 전자 메일 작업을 만듭니다.

## PARAMETERS

### -CustomEmail
콤마로 구분된 전자 메일 주소 목록을 지정합니다.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독

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

### -SendToServiceOwner
규칙이 발생하면 이 작업이 서비스 소유자에게 전자 메일을 보내고 있습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### System.String[]

### System.Management.Automation.SwitchParameter

## 출력

### Microsoft.Azure.Management.Monitor.Management.Models.RuleEmailAction

## 참고 사항

## 관련 링크


[Add-AzMetricAlertRule](./Add-AzMetricAlertRule.md)

[Add-AzWebtestAlertRule](./Add-AzWebtestAlertRule.md)

[New-AzAlertRuleWebhook](./New-AzAlertRuleWebhook.md)


