---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 383F36F3-3F52-4FC3-99F7-831096E6037D
online version: ''
schema: 2.0.0
ms.openlocfilehash: ff7c7cd50b06a4110b6af12611f3d91eaedfd227
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045426"
---
# Start-AzureSqlDatabaseRestore

## SYNOPSIS
데이터베이스의 특정 시점 복원을 수행 합니다.

## 구문과

### BySourceDatabaseObject
```
Start-AzureSqlDatabaseRestore [-SourceServerName <String>] -SourceDatabase <Database>
 [-TargetServerName <String>] -TargetDatabaseName <String> [-PointInTime <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### BySourceRestorableDroppedDatabaseObject
```
Start-AzureSqlDatabaseRestore [-SourceServerName <String>]
 -SourceRestorableDroppedDatabase <RestorableDroppedDatabase> [-TargetServerName <String>]
 -TargetDatabaseName <String> [-PointInTime <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### BySourceDatabaseName
```
Start-AzureSqlDatabaseRestore -SourceServerName <String> -SourceDatabaseName <String>
 [-TargetServerName <String>] -TargetDatabaseName <String> [-PointInTime <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### BySourceRestorableDroppedDatabaseName
```
Start-AzureSqlDatabaseRestore -SourceServerName <String> -SourceDatabaseName <String>
 -SourceDatabaseDeletionDate <DateTime> [-TargetServerName <String>] [-RestorableDropped]
 -TargetDatabaseName <String> [-PointInTime <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**AzureSqlDatabaseRestore** Cmdlet은 기본, 표준 또는 Premium 데이터베이스의 특정 시점 복원을 수행 합니다.
Azure SQL Database에는 7 일, 표준, 14 일간의 기본 데이터베이스 백업 및 35 일간의 Premium이 유지 됩니다.
복원 작업을 수행 하면 새 데이터베이스가 만들어집니다.
원본 데이터베이스가 삭제 되지 않은 경우 *sourcedatabasename* 및 *targetdatabasename* 매개 변수는 다른 값을 가져야 합니다.

Azure SQL Database는 현재 교차 서버 복원을 지원 하지 않습니다.
원본 및 대상 서버 이름은 동일 해야 합니다.

## 예제의

### 예제 1: 개체를 지정 된 시점으로 복원
```
PS C:\> $Database = Get-AzureSqlDatabase -ServerName "Server01" -DatabaseName "Database17" 
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceDatabase $Database -TargetDatabaseName "DatabaseRestored" -PointInTime "2013-01-01 06:00:00"
```

첫 번째 명령은 Server01 이라는 서버의 Database17 이라는 데이터베이스의 데이터베이스 개체를 가져온 다음이를 $Database 변수에 저장 합니다.

두 번째 명령은 데이터베이스를 지정 된 시점으로 복원 합니다.
명령이 새 데이터베이스의 이름을 지정 합니다.

### 예제 2: 이름으로 지정 된 데이터베이스를 특정 시점으로 복원
```
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceServerName "Server01" -SourceDatabaseName "Database17" -TargetDatabaseName "DatabaseRestored" -PointInTime "2013-01-01 06:00:00"
```

이 명령은 Database17 이라는 데이터베이스를 지정 된 시점으로 복원 합니다.
명령이 새 데이터베이스의 이름을 지정 합니다.

### 예제 3: 개체를 지정 된 시점에 놓을 때 손실 되는 데이터베이스 복원
```
PS C:\> $Database = Get-AzureSqlDatabase -RestorableDropped -ServerName "Server01" -DatabaseName "Database01" -DatabaseDeletionDate "2012-11-09T22:59:43.000Z" 
PS C:\> $Operation = Start-AzureSqlDatabaseRestore -SourceRestorableDroppedDatabase $Database -TargetDatabaseName "DroppedDatabaseRestored"
```

첫 번째 명령은 Server01 라는 서버의 Database01 이라는 데이터베이스의 데이터베이스 개체를 가져옵니다.
명령에서 *RestorableDropped* 매개 변수를 지정 합니다.
따라서 cmdlet은 지정 된 복원 지점을 restorable 하 여 데이터베이스를 삭제 했습니다.
명령이 $Database 변수에 해당 데이터베이스 개체를 저장 합니다.

두 번째 명령은 $Database에서 지정한 손실 된 데이터베이스를 복원 합니다.
명령이 새 데이터베이스의 이름을 지정 합니다.

## 변수

### -PointInTime
데이터베이스를 복원할 복원 지점을 지정 합니다.
복원 작업이 완료 되 면 데이터베이스는이 매개 변수에서 지정 하는 날짜 및 시간에 원래 상태로 복원 됩니다.
현재 시간으로 설정 된 라이브 데이터베이스와 손실 된 데이터베이스의 경우 기본적으로이 cmdlet은 데이터베이스가 삭제 된 시간을 사용 합니다.

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -RestorableDropped
이 cmdlet이 restorable 손실 된 데이터베이스를 복원 함을 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -원본 데이터베이스
이 cmdlet이 복원 하는 데이터베이스의 이름을 지정 합니다.

```yaml
Type: Database
Parameter Sets: BySourceDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SourceDatabaseDeletionDate
데이터베이스가 삭제 된 날짜와 시간을 지정 합니다.
실제 데이터베이스 삭제 시간과 일치 하는 시간을 지정할 때는 밀리초를 포함 해야 합니다.

```yaml
Type: DateTime
Parameter Sets: BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceDatabaseName
이 cmdlet이 복원 하는 라이브 데이터베이스의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: BySourceDatabaseName, BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceRestorableDroppedDatabase
이 cmdlet이 복원 하는 restorable 손실 된 데이터베이스를 나타내는 개체를 지정 합니다.
**RestorableDroppedDatabase** 개체를 가져오려면 Get-AzureSqlDatabase cmdlet을 사용 하 고 *RestorableDropped* 매개 변수를 지정 합니다.

```yaml
Type: RestorableDroppedDatabase
Parameter Sets: BySourceRestorableDroppedDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -SourceServerName
원본 데이터베이스가 실시간으로 실행 되는 서버의 이름을 지정 하거나 원본 데이터베이스를 삭제 하기 전에 실행 합니다.

```yaml
Type: String
Parameter Sets: BySourceDatabaseObject, BySourceRestorableDroppedDatabaseObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: BySourceDatabaseName, BySourceRestorableDroppedDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetDatabaseName
복원 작업이 만드는 새 데이터베이스의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TargetServerName
이 cmdlet이 데이터베이스를 복원할 서버의 이름을 지정 합니다.

Azure SQL Database는 현재 교차 서버 복원을 지원 하지 않습니다.
원본 및 대상 서버 이름은 동일 해야 합니다.

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

### WindowsAzure. SqlDatabase에 대 한 RestorableDroppedDatabase

### WindowsAzure. SqlDatabase. * 데이터베이스

## 출력

### WindowsAzure. SqlDatabase에 대 한 RestoreDatabaseOperation

## 상속자
* 이 cmdlet을 실행 하려면 인증서 기반 인증을 사용 해야 합니다. 이 cmdlet을 실행 하는 컴퓨터에서 다음 명령을 실행 합니다. 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## 관련 링크

[Azure SQL 데이터베이스](https://azure.microsoft.com/en-us/services/sql-database/)

[데이터베이스 복원 요청 만들기](https://msdn.microsoft.com/en-us/library/dn509571.aspx)

[Azure SQL 데이터베이스에 대 한 작업](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-AzureSqlDatabase](./Get-AzureSqlDatabase.md)


