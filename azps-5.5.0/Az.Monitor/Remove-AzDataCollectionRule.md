---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azdatacollectionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDataCollectionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDataCollectionRule.md
ms.openlocfilehash: 24b5d7dc4209edfbd9bb3080bc87fc18a14977b0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190105"
---
# Remove-AzDataCollectionRule

## SYNOPSIS
데이터 수집 규칙을 삭제합니다.

## 구문

### ByName(기본값)
```
Remove-AzDataCollectionRule
   -ResourceGroupName <string> 
   -RuleName <string> 
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

### ByInputObject
```
Remove-AzDataCollectionRule
   -InputObject <PSDataCollectionRuleResource>
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

### ByResourceId
```
Remove-AzDataCollectionRule
   -RuleId <string>
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## 설명
**Remove-AzDataCollectionRule** cmdlet은 데이터 컬렉션 규칙을 삭제합니다.

DCR(데이터 수집 규칙)은 Azure Monitor로 들어오는 데이터를 정의하고 해당 데이터를 보내거나 저장할 위치를 지정합니다. 다음은 전체 [DCR 개요 문서입니다.](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-overview)

## 예제

### 예제 1: 이름 및 리소스 그룹 매개 변수를 사용하여 데이터 수집 규칙 삭제
```
PS C:\>Remove-AzDataCollectionRule -ResourceGroupName "testgroup" -RuleName "testDcr"             
```

### 예제 2: 이름 및 리소스 그룹 반환 bool을 사용하여 데이터 수집 규칙 삭제
```
PS C:\>Remove-AzDataCollectionRule -ResourceGroupName "testgroup" -RuleName "testDcr" -PassThru

True
```

### 예제 3: InputObject에서 데이터 수집 규칙 삭제
```
PS C:\>Get-AzDataCollectionRule -ResourceGroupName "testdcr" -RuleName "dcrFromPipe95" | Remove-AzDataCollectionRule
```

### 예제 4: 리소스 ID에서 데이터 수집 규칙 삭제
```
PS C:\>Remove-AzDataCollectionRule -RuleId "/subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/{dcrName}"
```

## PARAMETERS

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

### -ResourceGroupName
리소스 그룹 이름

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RuleName
리소스 이름입니다.

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RuleId
리소스 식별자입니다.

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirm
cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
cmdlet이 실행되는 경우의 결과 표시 cmdlet이 실행되지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.

## 입력

### System.String

## 출력

### Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource

## 참고 사항

## 관련 링크

[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md) 
 [Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md) 
 [New-AzDataCollectionRule](./New-AzDataCollectionRule.md) 
 [Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)