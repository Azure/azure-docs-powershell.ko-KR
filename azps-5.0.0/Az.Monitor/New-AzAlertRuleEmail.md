---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azalertruleemail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
ms.openlocfilehash: 592329ff0793fc99f8e5b0e7031a2248342102f9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226749"
---
# New-AzAlertRuleEmail

## SYNOPSIS
경고 규칙에 대 한 전자 메일 작업을 만듭니다.

## 구문과

```
New-AzAlertRuleEmail [[-CustomEmail] <String[]>] [-SendToServiceOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**AzAlertRuleEmail** cmdlet은 경고 규칙에 대 한 전자 메일 작업을 만듭니다.

## 예제의

### 예제 1: 서비스 소유자를 위한 알림 규칙 만들기 전자 메일 작업
```
PS C:\>New-AzAlertRuleEmail -SendToServiceOwners
```

이 명령은 경고 규칙이 발생 했을 때 해당 서비스 소유자에 게 보낼 알림 규칙 전자 메일 작업을 만듭니다.

### 예제 2: 서비스를 지원 하지 않는 소유자를 위한 알림 규칙 만들기 전자 메일 작업
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.com,davidchew@contoso.net
```

이 명령은 지정 된 전자 메일 주소에 대 한 알림 규칙 전자 메일 작업을 만들지만 서비스 소유자에 게는 해당 하지 않습니다.

### 예제 3: 서비스 소유자 및 비 서비스 소유자에 대 한 알림 규칙 만들기 전자 메일 작업
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.net -SendToServiceOwners
```

이 명령은 지정 된 주소와 해당 서비스 소유자에 대 한 알림 규칙 전자 메일 작업을 만듭니다.

## 변수

### -CustomEmail
쉼표로 구분 된 전자 메일 주소 목록을 지정 합니다.

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

### -SendToServiceOwner
이 작업이 규칙이 실행 될 때 서비스 소유자에 게 전자 메일을 보내도록 지정 합니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### System.webserver []

### System.webserver 매개 변수

## 출력

### Microsoft. 경영진. 관리자. RuleEmailAction

## 상속자

## 관련 링크

[추가-AzLogAlertRule](./Add-AzLogAlertRule.md)

[추가-AzMetricAlertRule](./Add-AzMetricAlertRule.md)

[추가-AzWebtestAlertRule](./Add-AzWebtestAlertRule.md)

[새로운 AzAlertRuleWebhook](./New-AzAlertRuleWebhook.md)


