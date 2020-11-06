---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: A123CB7F-2F95-49EE-9F57-E264EB1F9093
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabasedatamaskingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseDataMaskingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseDataMaskingRule.md
ms.openlocfilehash: b53b32b30e1b69da94ac8319ed3a5f4eee7ffc0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524820"
---
# New-AzureRmSqlDatabaseDataMaskingRule

## SYNOPSIS
데이터베이스에 대 한 데이터 마스킹 규칙을 만듭니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
New-AzureRmSqlDatabaseDataMaskingRule -MaskingFunction <String> [-PrefixSize <UInt32>]
 [-ReplacementString <String>] [-SuffixSize <UInt32>] [-NumberFrom <Double>] [-NumberTo <Double>] [-PassThru]
 -SchemaName <String> -TableName <String> -ColumnName <String> [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 설명은
**AzureRmSqlDatabaseDataMaskingRule** Cmdlet은 Azure SQL 데이터베이스에 대 한 데이터 마스킹 규칙을 만듭니다.
Cmdlet을 사용 하려면 *ResourceGroupName* , *ServerName* , *DatabaseName* 및 *RuleId* 매개 변수를 사용 하 여 규칙을 식별 합니다.
*TableName* 및 *ColumnName* 을 제공 하 여 규칙의 대상을 지정 하 고 *MaskingFunction* 매개 변수를 입력 하 여 데이터 마스크 방법을 정의 합니다.

*MaskingFunction* 에 Number 또는 text 값이 있으면 숫자 *의 시작* 및 *번호를* 매개 변수로 지정 하거나, 숫자 마스킹 또는 *PrefixSize* , *ReplacementString* , 텍스트 마스킹에 *SuffixSize* 을 지정할 수 있습니다.

명령이 성공 하 고 *PassThru* 매개 변수를 사용 하는 경우 cmdlet은 규칙 식별자 외에도 데이터 마스킹 규칙 속성에 대해 설명 하는 개체를 반환 합니다.
규칙 식별자에는 *ResourceGroupName* , *ServerName* , *DatabaseName* , *RuleID* 이 포함 되지만이에 제한 되지 않습니다.

이 cmdlet은 Azure의 SQL Server 스트레치 데이터베이스 서비스 에서도 지원 됩니다.

## 예제의

### 예제 1: 데이터베이스의 숫자 열에 대 한 데이터 마스킹 규칙 만들기
```
PS C:\>New-AzureRmSqlDatabaseDataMaskingRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -RuleId "Rule01" -SchemaName "Schema01" -TableName "Table01" -ColumnName "Column01" -MaskingFunction "Number" -NumberFrom 5 -NumberTo 14
```

이 명령은 Schema01 이라는 스키마의 Table01 테이블에서 Column01 이라는 열에 대 한 데이터 마스킹 규칙을 만듭니다.
Database01 라는 데이터베이스에는 이러한 항목이 모두 포함 됩니다.
규칙은 5와 14 사이의 난수를 마스크 값으로 사용 하는 숫자 마스킹 규칙입니다.
규칙의 이름은 Rule01입니다.

## 변수

### -ColumnName
마스킹 규칙을 대상으로 하는 열의 이름을 지정 합니다.

```yaml
Type: String
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
Type: String
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

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
- 메일 주소

기본값은 기본 값입니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: NoMasking, Default, Text, Number, SocialSecurityNumber, CreditCardNumber, Email

Required: True
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
Type: Double
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
Type: Double
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
Type: SwitchParameter
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
Type: UInt32
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
기본값은 빈 문자열입니다.

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

### -ResourceGroupName
데이터베이스가 할당 된 리소스 그룹의 이름을 지정 합니다.

```yaml
Type: String
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
Type: String
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
Type: String
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
Type: UInt32
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
Type: String
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
Type: SwitchParameter
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

###  
않아야.

## 출력

### DatabaseDataMaskingRuleModel을 (를) 보세요.

## 상속자

## 관련 링크

[Get-AzureRmSqlDatabaseDataMaskingRule](./Get-AzureRmSqlDatabaseDataMaskingRule.md)

[제거-AzureRmSqlDatabaseDataMaskingRule](./Remove-AzureRmSqlDatabaseDataMaskingRule.md)

[Set-AzureRmSqlDatabaseDataMaskingRule](./Set-AzureRmSqlDatabaseDataMaskingRule.md)

[SQL 데이터베이스 설명서](https://docs.microsoft.com/azure/sql-database/)


