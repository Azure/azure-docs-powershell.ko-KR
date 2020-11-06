---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 11A521DF-E77C-4D6F-A2D9-1C2CF8972F57
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogAlertRule.md
ms.openlocfilehash: 38644018ac9ae19d1c413123ca071f564d336fa7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537192"
---
# Add-AzureRmLogAlertRule

## SYNOPSIS
로그 알림 규칙을 추가 하거나 바꿉니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Add-AzureRmLogAlertRule [-TargetResourceGroup <String>] [-TargetResourceId <String>] [-Level <String>]
 -OperationName <String> [-TargetResourceProvider <String>] [-Status <String>] [-SubStatus <String>]
 -Location <String> [-Description <String>] [-DisableRule] -ResourceGroup <String> -Name <String>
 [-Actions <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## 설명은
**Add-AzureRmLogAlertRule** cmdlet은 이벤트 경고 규칙을 추가 하거나 바꿉니다.
추가 된 규칙이 리소스 그룹과 연결 되어 있으며 이름이 있습니다.

이전 릴리스에서 발표 된 것 처럼 **AzureRMLogAlertRule cmdlet은 이후 릴리스에서 더 이상 사용 되지 않습니다.** 이 cmdlet을 사용 하는 첫 번째 2017 년 10 월 이후이 기능은 활동 로그 알림으로 전환 되는 데 영향을 주지 않습니다. **_https://aka.ms/migratemealerts_** 자세한 내용은을 참조 하세요.

## 예제의

### 예제 1: 로그 알림 규칙 추가
```
PS C:\>Add-AzureRmLogAlertRule -Name "logRule" -Location "East US" -ResourceGroup "Default-Web-EastUS" -OperationName "Create" -TargetResourceId "/subscriptions/abbfb07c-6c93-40be-bc9b-4f0deba32f4c/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/misitiooeltuyo" -Description "My log rule"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

이 명령은 이벤트 기반 알림 규칙을 추가 하거나 업데이트 합니다.

## 변수

### -작업
쉼표로 구분 된 작업 목록을 지정 합니다.

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -설명
규칙에 대 한 설명을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DisableRule
규칙을 사용 하지 않습니다.
이 매개 변수를 지정 하지 않으면 규칙을 사용할 수 있습니다.

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

### 수준
규칙이 모니터링 하는 이벤트 수준을 지정 합니다.
이벤트 기반 규칙에 대해서만이 매개 변수를 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -위치
규칙의 위치를 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -이름
규칙의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OperationName
작업의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroup
규칙에 대 한 리소스 그룹의 이름을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -상태
상태를 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -하위 상태
하위 상태를 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TargetResourceGroup
규칙이 모니터링 하는 리소스의 리소스 그룹을 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TargetResourceId
규칙이 모니터링 하는 리소스의 ID를 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TargetResourceProvider
규칙이 모니터링 하는 리소스의 리소스 공급자를 지정 합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
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

### PSAddAlertRuleOperationResponse를 통해 출력 합니다.

## 상속자

## 관련 링크

[추가-AzureRmMetricAlertRule](./Add-AzureRmMetricAlertRule.md)

[추가-AzureRmWebtestAlertRule](./Add-AzureRmWebtestAlertRule.md)

[Get-AzureRmAlertHistory](./Get-AzureRmAlertHistory.md)

[새로운 AzureRmAlertRuleEmail](./New-AzureRmAlertRuleEmail.md)

[새로운 AzureRmAlertRuleWebhook](./New-AzureRmAlertRuleWebhook.md)


