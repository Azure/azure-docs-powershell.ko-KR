---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 48CF206C-AF63-4013-834E-8EC3646D180B
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: 544db2f0e23cb510c81fb64898b6bcf856e760e5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226505"
---
# Set-AzSqlDatabaseDataMaskingRule

## SYNOPSIS
데이터베이스에 대 한 데이터 마스킹 규칙의 속성을 설정 합니다.

## 구문과

```
Set-AzSqlDatabaseDataMaskingRule [-MaskingFunction <String>] [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 설명은
**AzSqlDatabaseDataMaskingRule** Cmdlet은 Azure SQL 데이터베이스에 대 한 데이터 마스킹 규칙을 설정 합니다.
Cmdlet을 사용 하려면 *ResourceGroupName* , *ServerName* , *DatabaseName* 및 *RuleId* 매개 변수를 제공 하 여 규칙을 식별 합니다.
*SchemaName* , *TableName* , *ColumnName* 의 매개 변수를 제공 하 여 규칙의 대상을 변경할 수 있습니다.
*MaskingFunction* 매개 변수를 지정 하 여 데이터 마스크 방법을 수정 합니다.
Number 또는 *MaskingFunction* 에 대 한 텍스트 값을 지정 *하는 경우* 숫자 마스킹에 대 한 매개 변수 및 번호 *를* 지정할 수 있으며, 텍스트 마스킹에 대 한 *PrefixSize* , *ReplacementString* 및 *SuffixSize* 매개 변수를 지정 합니다.
명령이 성공 하 고 *PassThru* 매개 변수를 지정 하면 cmdlet은 데이터 마스킹 규칙 속성 및 규칙 식별자를 설명 하는 개체를 반환 합니다.
규칙 식별자에는 **ResourceGroupName** , **ServerName** , **DatabaseName** , **RuleId** 이 포함 되지만이에 제한 되지 않습니다.
이 cmdlet은 Azure의 SQL Server 스트레치 데이터베이스 서비스 에서도 지원 됩니다.

## 예제의

### 예제 1: 데이터베이스의 데이터 마스킹 규칙 범위 변경
```powershell
PS C:\>Set-AzSqlDatabaseDataMaskingRule -ResourceGroupName $params.rgname -ServerName $params.serverName  -DatabaseName $params.databaseName -SchemaName "dbo" -TableName  "table1" -ColumnName "column1" -MaskingFunction "Default"
```

이 명령은 ID Rule17 인 데이터 마스킹 규칙을 수정 합니다.
이 규칙은 서버 Server01의 Database01 라는 데이터베이스에서 작동 합니다.
이 명령은 임의의 숫자가 마스킹된 값으로 생성 되는 간격의 경계를 변경 합니다.
새 범위는 23 ~ 42입니다.

### 예제 2

데이터베이스에 대 한 데이터 마스킹 규칙의 속성을 설정 합니다. 생성

```powershell
<!-- Aladdin Generated Example --> 
Set-AzSqlDatabaseDataMaskingRule -ColumnName 'column1' -DatabaseName $params.databaseName -MaskingFunction NoMasking -NumberFrom 5 -NumberTo 14 -PrefixSize <UInt32> -ReplacementString <String> -ResourceGroupName $params.rgname -SchemaName 'dbo' -ServerName $params.serverName -SuffixSize <UInt32> -TableName 'table1'
```

## 변수

### -ColumnName
마스킹 규칙을 대상으로 하는 열의 이름을 지정 합니다.

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
데이터베이스의 이름을 지정 합니다.

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

### -MaskingFunction
규칙에서 사용 하는 마스킹 기능을 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.
- 기본값
- NoMasking
- 본문
- 숫자로
- 사회 Alsecurity번호
- CreditCardNumber
- 전자 메일 기본값은 기본 값입니다.

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

### -번호
임의의 값이 선택 되는 간격의 하한값을 지정 합니다.
*MaskingFunction* 매개 변수에 Number 값을 지정 하는 경우에만이 매개 변수를 지정 합니다.
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

### -번호를
임의 값이 선택 된 간격의 상한 번호를 지정 합니다.
*MaskingFunction* 매개 변수에 Number 값을 지정 하는 경우에만이 매개 변수를 지정 합니다.
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
작업 중인 항목을 나타내는 개체를 반환 합니다.
기본적으로이 cmdlet은 출력을 생성 하지 않습니다.

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
마스크 되지 않은 텍스트의 시작 부분에 있는 문자 수를 지정 합니다.
*MaskingFunction* 매개 변수에 대 한 텍스트 값을 지정 하는 경우에만이 매개 변수를 지정 합니다.
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
마스크 되지 않은 텍스트의 끝에 있는 문자 수를 지정 합니다.
*MaskingFunction* 매개 변수에 대 한 텍스트 값을 지정 하는 경우에만이 매개 변수를 지정 합니다.
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
데이터베이스가 할당 된 리소스 그룹의 이름을 지정 합니다.

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
스키마의 이름을 지정 합니다.

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
데이터베이스를 호스트 하는 서버의 이름을 지정 합니다.

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
마스크 되지 않은 텍스트의 끝에 있는 문자 수를 지정 합니다.
*MaskingFunction* 매개 변수에 대 한 텍스트 값을 지정 하는 경우에만이 매개 변수를 지정 합니다.
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
마스킹된 열을 포함 하는 데이터베이스 테이블의 이름을 지정 합니다.

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

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

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
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

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
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.

## 입력

### System. 문자열

### 시스템 Null 허용 ' 1 [[System.webserver, System.webserver, CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]

### 시스템 Null 허용 ' 1 [[4.0.0.0] [[System.webserver, System.webserver, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]

## 출력

### DataMasking. DatabaseDataMaskingRuleModel에 대 한

## 상속자

## 관련 링크

[Get-AzSqlDatabaseDataMaskingRule](./Get-AzSqlDatabaseDataMaskingRule.md)

[새로운 AzSqlDatabaseDataMaskingRule](./New-AzSqlDatabaseDataMaskingRule.md)

[제거-AzSqlDatabaseDataMaskingRule](./Remove-AzSqlDatabaseDataMaskingRule.md)

[SQL 데이터베이스 설명서](https://docs.microsoft.com/azure/sql-database/)


