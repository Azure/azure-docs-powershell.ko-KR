---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4FCC7D8B-A46E-4E5B-8BE2-F62B3D3E715D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerAuditingPolicy.md
ms.openlocfilehash: daec1290dfa70166e532265da98bdb507b1318e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531798"
---
# Set-AzureRmSqlServerAuditingPolicy

## SYNOPSIS
SQL 데이터베이스 서버의 감사 정책을 변경 합니다.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## 구문과

```
Set-AzureRmSqlServerAuditingPolicy [-AuditType <AuditType>] [-AuditActionGroup <AuditActionGroups[]>]
 [-PassThru] [-EventType <String[]>] [-StorageAccountName <String>] [-StorageKeyType <String>]
 [-RetentionInDays <UInt32>] [-TableIdentifier <String>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**AzureRmSqlServerAuditingPolicy** Cmdlet은 Azure SQL 데이터베이스 서버의 감사 정책을 변경 합니다.
*ResourceGroupName* 및 *ServerName* 매개 변수를 지정 하 여 서버를 식별 하 고, *storageaccountname* 매개 변수를 감사 로그에 대 한 저장소 계정을 지정 하 고, *storageaccountname* 매개 변수를 사용 하 여 사용할 저장소 키를 정의 합니다.

보존 *기간 및* *tableidentifier* 매개 변수 값을 설정 하 여 감사 로그 테이블 이름에 대 한 기간과 시드를 정의 하는 감사 로그 테이블에 대 한 보존을 정의할 수도 있습니다.
*EventType* 매개 변수를 지정 하 여 감사할 이벤트 유형을 정의 합니다.
이 cmdlet을 실행 한 후에는이 서버의 정책을 사용 하는 데이터베이스의 감사를 사용할 수 있습니다.
Cmdlet이 성공 하 고 *PassThru* 매개 변수를 지정 하면 cmdlet은 현재 감사 정책 및 서버 식별자를 설명 하는 개체를 반환 합니다.
서버 식별자에는 **ResourceGroupName** 및 **ServerName** 이 포함 됩니다.

## 예제의

### 예제 1: Azure SQL server의 감사 정책 설정 테이블 감사 사용
```
PS C:\>Set-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AuditType Table -StorageAccountName "Storage22"
```

이 명령은 Server01 이라는 서버의 감사 정책을 Storage22 이라는 저장소 계정을 사용 하도록 설정 합니다.

### 예제 2: Azure SQL server의 기존 감사 정책의 저장소 계정 키 설정
```
PS C:\>Set-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -StorageAccountKey Secondary
```

이 명령은 Server01 이라는 서버의 감사 정책을 보조 키를 사용 하도록 설정 합니다.
이 명령은 저장소 계정 이름을 수정 하지 않습니다.

### 예제 3: 특정 이벤트 유형을 사용 하도록 Azure SQL server의 감사 정책 설정
```
PS C:\>Set-AzureRmSqlServerAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -EventType Login_Failure
```

### 예제 4: Blob 감사를 사용 하도록 데이터베이스의 감사 정책 설정
```
PS C:\>Set-AzureRmSqlDatabaseAuditingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AuditType Blob -StorageAccountName "Storage31" -AuditActionGroup "SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP", "FAILED_DATABASE_AUTHENTICATION_GROUP" -RetentionInDays 8
```

이 명령은 Server01 이라는 서버의 감사 정책을 설정 하 여 Login_Failure 이벤트 유형을 사용 합니다.
이 명령은 다른 설정을 수정 하지 않습니다.

## 변수

### -AuditActionGroup
하나 이상의 감사 작업 그룹을 지정 합니다. 이 매개 변수는 Blob 감사에만 적용할 수 있습니다.

```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditActionGroups[]
Parameter Sets: (All)
Aliases: 
Accepted values: BATCH_STARTED_GROUP, BATCH_COMPLETED_GROUP, APPLICATION_ROLE_CHANGE_PASSWORD_GROUP, BACKUP_RESTORE_GROUP, DATABASE_LOGOUT_GROUP, DATABASE_OBJECT_CHANGE_GROUP, DATABASE_OBJECT_OWNERSHIP_CHANGE_GROUP, DATABASE_OBJECT_PERMISSION_CHANGE_GROUP, DATABASE_OPERATION_GROUP, DATABASE_PERMISSION_CHANGE_GROUP, DATABASE_PRINCIPAL_CHANGE_GROUP, DATABASE_PRINCIPAL_IMPERSONATION_GROUP, DATABASE_ROLE_MEMBER_CHANGE_GROUP, FAILED_DATABASE_AUTHENTICATION_GROUP, SCHEMA_OBJECT_ACCESS_GROUP, SCHEMA_OBJECT_CHANGE_GROUP, SCHEMA_OBJECT_OWNERSHIP_CHANGE_GROUP, SCHEMA_OBJECT_PERMISSION_CHANGE_GROUP, SUCCESSFUL_DATABASE_AUTHENTICATION_GROUP, USER_CHANGE_PASSWORD_GROUP

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AuditType
감사 유형을 지정 합니다. 감사 로그를 테이블 저장소 또는 Blob 저장소에 기록할 수 있습니다. Blob 감사는 성능을 향상 하 고 개체 수준 감사를 지원 합니다.

```yaml
Type: Microsoft.Azure.Commands.Sql.Auditing.Model.AuditType
Parameter Sets: (All)
Aliases: 
Accepted values: NotSet, Table, Blob

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EventType
감사할 이벤트 유형을 지정 합니다.
이 매개 변수는 테이블 감사에만 적용 됩니다.

여러 이벤트 유형을 지정할 수 있습니다.
모든 이벤트 유형을 감사 하도록 All을 지정 하거나 없음으로 이벤트 감사를 지정 하지 않을 수 있습니다.
모두 또는 모두를 동시에 지정 하지 않으면 명령이 실패 합니다.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 
Accepted values: PlainSQL_Success, PlainSQL_Failure, ParameterizedSQL_Success, ParameterizedSQL_Failure, StoredProcedure_Success, StoredProcedure_Failure, Login_Success, Login_Failure, TransactionManagement_Success, TransactionManagement_Failure, All, None

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

### -ResourceGroupName
데이터베이스를 포함 하는 리소스 그룹의 이름을 지정 합니다.

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

### -보존 기간
감사 로그 테이블의 보존 일 수를 지정 합니다.
값이 0 이면 테이블이 보존 되지 않는다는 의미입니다.
이는 기본값입니다.
0 보다 큰 값을 지정 하는 경우 *Tableidentifer* 매개 변수에 대 한 값도 지정 해야 합니다.

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

### -ServerName
데이터베이스를 포함 하는 서버의 이름을 지정 합니다.

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

### -StorageAccountName
데이터베이스 감사를 위한 저장소 계정의 이름을 지정 합니다.
와일드 카드 문자는 허용 되지 않습니다.
이 매개 변수를 지정 하지 않으면 이전에 데이터베이스의 감사 정책 일부로 정의한 저장소 계정이 cmdlet에 사용 됩니다.
데이터베이스 감사 정책을 처음 정의 하 고이 매개 변수를 지정 하지 않으면 명령이 실패 합니다.

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

### -StorageKeyType
사용할 저장소 선택 키를 지정 합니다.
이 매개 변수에 허용 되는 값은 다음과 같습니다.

- 주요한
- 보조

기본값은 기본 값입니다.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Primary, Secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TableIdentifier
감사 로그 테이블의 이름을 지정 합니다.
*보존 기간* 매개 변수에 대해 0 보다 큰 값을 지정 하는 경우이 값을 지정 합니다.

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

### Microsoft. Test.sql. Security. Model. ServerAuditingPolicyModel

## 상속자

## 관련 링크

[Get-AzureRmSqlServerAuditingPolicy](./Get-AzureRmSqlServerAuditingPolicy.md)

[-AzureRmSqlServerAuditingPolicy 사용](./Use-AzureRmSqlServerAuditingPolicy.md)

[SQL 데이터베이스 설명서](https://docs.microsoft.com/azure/sql-database/)


