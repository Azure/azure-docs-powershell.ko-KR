---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 48CF206C-AF63-4013-834E-8EC3646D180B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 544db2f0e23cb510c81fb64898b6bcf856e760e5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188009"
---
# Set-AzSqlDatabaseDataMaskingRule

## SYNOPSIS
데이터베이스에 대한 데이터 마스킹 규칙의 속성을 설정합니다.

## 구문

```
Set-AzSqlDatabaseDataMaskingRule [-MaskingFunction <String>] [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 설명
**Set-AzSqlDatabaseDataMaskingRule** cmdlet은 Azure SQL 데이터베이스에 대한 데이터 마스킹 규칙을 설정합니다.
cmdlet을 사용하려면 *ResourceGroupName,* *ServerName,* *DatabaseName* 및 *RuleId* 매개 변수를 입력하여 규칙을 식별합니다.
*SchemaName,* *TableName* 및 *ColumnName의* 매개 변수를 입력하여 규칙을 다시 설정할 수 있습니다.
*MaskingFunction* 매개 변수를 지정하여 데이터가 마스킹되는 방법을 수정합니다.
*MaskingFunction에* 대한 숫자 또는 텍스트 값을 지정하는 경우 숫자 마스킹에 *대한 NumberFrom* 및 *NumberTo* 매개 변수 또는 텍스트 마스킹에 대한 *PrefixSize,* *ReplacementString* 및 *SuffixSize* 매개 변수를 지정할 수 있습니다.
명령이 성공하고 *PassThru* 매개 변수를 지정하면 cmdlet은 데이터 마스킹 규칙 속성 및 규칙 식별자를 설명하는 개체를 반환합니다.
규칙 식별자는 **ResourceGroupName,** **ServerName, DatabaseName** 및 RuleId를 포함하지만 **제한되지 않습니다.**
이 cmdlet은 Azure의 SQL Server Stretch Database 서비스에서도 지원됩니다.

## 예제

### 예제 1: 데이터베이스의 데이터 마스킹 규칙 범위 변경
```powershell
PS C:\>Set-AzSqlDatabaseDataMaskingRule -ResourceGroupName $params.rgname -ServerName $params.serverName  -DatabaseName $params.databaseName -SchemaName "dbo" -TableName  "table1" -ColumnName "column1" -MaskingFunction "Default"
```

이 명령은 ID Rule17이 있는 데이터 마스킹 규칙을 수정합니다.
이 규칙은 Server01의 Database01 데이터베이스에서 작동됩니다.
이 명령은 난수가 마스킹된 값으로 생성되는 간격의 경계를 변경합니다.
새 범위는 23에서 42 사이입니다.

### 예제 2

데이터베이스에 대한 데이터 마스킹 규칙의 속성을 설정합니다. (자동Generated)

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlDatabaseDataMaskingRule -ColumnName 'column1' -DatabaseName $params.databaseName -MaskingFunction NoMasking -NumberFrom 5 -NumberTo 14 -PrefixSize <UInt32> -ReplacementString <String> -ResourceGroupName $params.rgname -SchemaName 'dbo' -ServerName $params.serverName -SuffixSize <UInt32> -TableName 'table1'
```

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

Required: False
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
기본값은 0입니다.

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

[New-AzSqlDatabaseDataMaskingRule](./New-AzSqlDatabaseDataMaskingRule.md)

[Remove-AzSqlDatabaseDataMaskingRule](./Remove-AzSqlDatabaseDataMaskingRule.md)

[SQL 데이터베이스 설명서](https://docs.microsoft.com/azure/sql-database/)


