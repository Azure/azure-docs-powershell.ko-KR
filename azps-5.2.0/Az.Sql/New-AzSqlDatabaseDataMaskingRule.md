---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A123CB7F-2F95-49EE-9F57-E264EB1F9093
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 35f2bc63366a86501650af1808274a3a0403e77f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360627"
---
# New-AzSqlDatabaseDataMaskingRule

## SYNOPSIS
데이터베이스에 대한 데이터 마스킹 규칙을 만듭니다.

## 구문

```
New-AzSqlDatabaseDataMaskingRule -MaskingFunction <String> [-PrefixSize <UInt32>] [-ReplacementString <String>]
 [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru] -SchemaName <String>
 -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 설명
**New-AzSqlDatabaseDataMaskingRule** cmdlet은 Azure SQL 데이터베이스에 대한 데이터 마스킹 규칙을 만듭니다.
cmdlet을 사용하려면 *ResourceGroupName,* *ServerName* 및 *DatabaseName* 매개 변수를 사용하여 규칙을 식별합니다.
*TableName* 및 *ColumnName을* 제공하여 규칙의 대상 및 *MaskingFunction* 매개 변수를 지정하여 데이터가 마스킹되는 방법을 정의합니다.
*MaskingFunction에* 숫자 또는 텍스트 값이 있는 경우 숫자 마스킹의 *경우 NumberFrom* 및 *NumberTo* 매개 변수를 지정하거나 텍스트 마스킹에 대한 *PrefixSize,* *ReplacementString* 및 *SuffixSize를* 지정할 수 있습니다.
명령이 성공하고 *PassThru* 매개 변수를 사용하는 경우 cmdlet은 규칙 식별자 외에도 데이터 마스킹 규칙 속성을 설명하는 개체를 반환합니다.
규칙 식별자는 *ResourceGroupName,* *ServerName, DatabaseName* 및 RuleID를 포함하지만 *제한되지 않습니다.*
이 cmdlet은 Azure의 SQL Server Stretch Database 서비스에서도 지원됩니다.

## 예제

### 예제 1: 데이터베이스의 숫자 열에 대한 데이터 마스킹 규칙 만들기
```
PS C:\>New-AzSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"  -SchemaName "Schema01" -TableName "Table01" -ColumnName "Column01" -MaskingFunction "Number" -NumberFrom 5 -NumberTo 14
```

이 명령은 Schema01이라는 이름의 테이블에 Table01이라는 열에 대한 데이터 마스킹 규칙을 만듭니다.
Database01이라는 데이터베이스에는 이러한 모든 항목이 포함되어 있습니다.
규칙은 5에서 14 사이의 난수로 마스크 값을 사용하는 숫자 마스킹 규칙입니다.

## PARAMETERS

### -ColumnName
마스킹 규칙에 의해 대상이 지정된 열의 이름을 지정합니다.

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

### -DatabaseName
데이터베이스의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
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

### -MaskingFunction
규칙에서 사용하는 마스킹 함수를 지정합니다.
이 매개 변수에 허용되는 값은
- 기본값
- NoMasking
- 텍스트
- 숫자
- SocialSecurityNumber
- CreditCardNumber
- 전자 메일의 기본값은 기본값입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: NoMasking, Default, Text, Number, SocialSecurityNumber, CreditCardNumber, Email

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NumberFrom
임의 값이 선택된 간격의 하한 번호를 지정합니다.
*MaskingFunction* 매개 변수에 대한 Number 값을 지정하는 경우 이 매개 변수를 지정합니다.
기본값은 0입니다.

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NumberTo
임의 값이 선택된 간격의 상한 번호를 지정합니다.
*MaskingFunction* 매개 변수에 대한 Number 값을 지정하는 경우 이 매개 변수를 지정합니다.
기본값은 0입니다.

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
작업하는 항목을 나타내는 개체를 반환합니다.
기본적으로 이 cmdlet은 출력을 생성하지 않습니다.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrefixSize
마스킹되지 않은 텍스트의 시작에 있는 문자 수를 지정합니다.
*MaskingFunction* 매개 변수에 대한 텍스트 값을 지정하는 경우 이 매개 변수를 지정합니다.
기본값은 0입니다.

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ReplacementString
마스킹되지 않은 텍스트의 끝에 있는 문자 수를 지정합니다.
*MaskingFunction* 매개 변수에 대한 텍스트 값을 지정하는 경우 이 매개 변수를 지정합니다.
기본값은 빈 문자열입니다.

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

### -ResourceGroupName
데이터베이스가 할당된 리소스 그룹의 이름을 지정합니다.

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

### -SchemaName
스마마의 이름을 지정합니다.

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

### -ServerName
데이터베이스를 호스트하는 서버의 이름을 지정합니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SuffixSize
마스킹되지 않은 텍스트의 끝에 있는 문자 수를 지정합니다.
*MaskingFunction* 매개 변수에 대한 텍스트 값을 지정하는 경우 이 매개 변수를 지정합니다.
기본값은 0입니다.

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TableName
마스킹된 열이 포함된 데이터베이스 테이블의 이름을 지정합니다.

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
cmdlet이 실행되는 경우의 결과 표시
cmdlet이 실행되지 않습니다.

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

### System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### System.Nullable'1[[System.Double, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

## 출력

### Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingRuleModel

## 참고 사항

## 관련 링크

[Get-AzSqlDatabaseDataMaskingRule](./Get-AzSqlDatabaseDataMaskingRule.md)

[Remove-AzSqlDatabaseDataMaskingRule](./Remove-AzSqlDatabaseDataMaskingRule.md)

[Set-AzSqlDatabaseDataMaskingRule](./Set-AzSqlDatabaseDataMaskingRule.md)

[SQL 데이터베이스 설명서](https://docs.microsoft.com/azure/sql-database/)


