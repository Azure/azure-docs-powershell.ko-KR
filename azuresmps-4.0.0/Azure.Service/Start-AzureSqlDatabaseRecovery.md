---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F63769D6-9A31-4A67-972A-1E0428853C86
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88f61718e363a630b70519590025a6da80364aeb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045423"
---
# Start-AzureSqlDatabaseRecovery

## SYNOPSIS
데이터베이스에 대 한 복원 요청을 시작 합니다.

## 구문과

### BySourceDatabaseName
```
Start-AzureSqlDatabaseRecovery -SourceServerName <String> -SourceDatabaseName <String>
 [-TargetServerName <String>] [-TargetDatabaseName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### BySourceDatabaseObject
```
Start-AzureSqlDatabaseRecovery -SourceDatabase <RecoverableDatabase> [-TargetServerName <String>]
 [-TargetDatabaseName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**AzureSqlDatabaseRecovery** cmdlet은 활성 또는 삭제 된 데이터베이스에 대 한 복원 요청을 시작 합니다.
이 cmdlet은 데이터베이스에 대해 마지막으로 사용 가능한 백업을 사용 하는 기본 복구를 지원 합니다.
복구 작업에서 새 데이터베이스를 만듭니다.
동일한 서버에서 라이브 데이터베이스를 복구 하는 경우 새 데이터베이스에 대해 다른 이름을 지정 해야 합니다.

데이터베이스에 대 한 특정 시점 복원을 수행 하려면 **AzureSqlDatabaseRestore** cmdlet을 대신 사용 합니다.

## 예제의

### 예제 1: 개체로 지정 된 데이터베이스 복구
```
PS C:\> $Database = Get-AzureSqlRecoverableDatabase -ServerName "Server01" -DatabaseName "Database17" 
PS C:\> $Operation = Start-AzureSqlDatabaseRecovery -SourceDatabase $Database -TargetDatabaseName "DatabaseRestored"
```

첫 번째 명령은 **AzureSqlRecoverableDatabase** cmdlet을 사용 하 여 데이터베이스 개체를 가져옵니다.
명령이 $Database 변수에 해당 개체를 저장 합니다.

두 번째 명령은 $Database에 저장 된 데이터베이스를 복구 합니다.

### 예제 2: 이름으로 지정 된 데이터베이스 복구
```
PS C:\> $Operation = Start-AzureSqlDatabaseRecovery -SourceServerName "Server01" -SourceDatabaseName "Database17" -TargetDatabaseName "DatabaseRestored"
```

이 명령은 데이터베이스 이름을 사용 하 여 데이터베이스를 복구 합니다.

## 변수

### -프로필
이 cmdlet이 읽는 Azure 프로필을 지정 합니다.
프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -원본 데이터베이스
이 cmdlet이 복구 하는 데이터베이스를 나타내는 database 개체를 지정 합니다.

```yaml
Type: RecoverableDatabase
Parameter Sets: BySourceDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SourceDatabaseName
이 cmdlet이 복구 하는 데이터베이스의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: BySourceDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceServerName
원본 데이터베이스가 실시간으로 실행 되는 서버의 이름을 지정 하거나 원본 데이터베이스를 삭제 하기 전에 실행 합니다.

```yaml
Type: String
Parameter Sets: BySourceDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetDatabaseName
복구 된 데이터베이스의 이름을 지정 합니다.
원본 데이터베이스가 여전히 활성 상태인 경우 동일한 서버로 복구 하려면 원본 데이터베이스 이름과 다른 이름을 지정 해야 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetServerName
데이터베이스를 복원할 서버의 이름을 지정 합니다.
데이터베이스를 동일한 서버나 다른 서버로 복원할 수 있습니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### WindowsAzure를 RecoverableDatabase 합니다.

## 출력

### WindowsAzure를 RecoverDatabaseOperation 합니다.

## 상속자
* 이 cmdlet을 실행 하려면 인증서 기반 인증을 사용 해야 합니다. 이 cmdlet을 실행 하는 컴퓨터에서 다음 명령을 실행 합니다. 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## 관련 링크

[Azure SQL 데이터베이스](https://azure.microsoft.com/en-us/services/sql-database/)

[데이터베이스 복구 요청 만들기](https://msdn.microsoft.com/en-us/library/dn800986.aspx)

[Azure SQL 데이터베이스의 지리적 복제](https://azure.microsoft.com/en-us/documentation/articles/sql-database-business-continuity-scenarios/)

[Azure SQL 데이터베이스에 대 한 작업](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-AzureSqlRecoverableDatabase](./Get-AzureSqlRecoverableDatabase.md)

[시작-AzureSqlDatabaseRestore](./Start-AzureSqlDatabaseRestore.md)


