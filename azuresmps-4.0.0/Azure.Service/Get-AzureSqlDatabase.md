---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 7427A101-9439-45B9-B72E-F8C2DA85E412
online version: ''
schema: 2.0.0
ms.openlocfilehash: c10ae808d105079b9739516bf9eaf316241b1b11
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046298"
---
# Get-AzureSqlDatabase

## SYNOPSIS
하나 이상의 데이터베이스를 검색 합니다.

## 구문과

### ByConnectionContext (기본값)
```
Get-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> [-Database <Database>]
 [-DatabaseName <String>] [-RestorableDropped] [-RestorableDroppedDatabase <RestorableDroppedDatabase>]
 [-DatabaseDeletionDate <DateTime>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByServerName
```
Get-AzureSqlDatabase -ServerName <String> [-Database <Database>] [-DatabaseName <String>] [-RestorableDropped]
 [-RestorableDroppedDatabase <RestorableDroppedDatabase>] [-DatabaseDeletionDate <DateTime>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**AzureSqlDatabase** Cmdlet은 Azure sql 데이터베이스 서버에서 Azure sql 데이터베이스 인스턴스를 하나 이상 검색 합니다.
**AzureSqlDatabaseServerContext** cmdlet을 사용 하 여 만드는 Azure SQL 데이터베이스 서버 연결 컨텍스트를 사용 하 여 서버를 지정할 수 있습니다.
또는 Azure SQL 데이터베이스 서버 이름을 지정 하는 경우 cmdlet은 현재 Azure 구독 정보를 사용 하 여 서버에 대 한 액세스 요청을 인증 합니다.

데이터베이스를 지정 하지 않으면 **AzureSqlDatabase** cmdlet은 지정 된 서버의 모든 데이터베이스를 반환 합니다.

Restorable 손실 된 데이터베이스 검색:

*RestorableDropped* 매개 변수를 사용 하 여 restorable 손실 된 데이터베이스를 검색 합니다.
모든 restorable 삭제 된 데이터베이스를 반환 하려면 *DatabaseName* 및 *DatabaseDeletionDate* 없이 *RestorableDropped* 매개 변수를 사용 합니다.
특정 restorable 손실 된 데이터베이스를 반환 하려면 *DatabaseName* 및 *DatabaseDeletionDate* 매개 변수와 함께 *RestorableDropped* 매개 변수를 사용 합니다.
*DatabaseName* 매개 변수를 사용 하 여 손실 된 특정 restorable 데이터베이스를 검색 하는 경우 *DatabaseDeletionDate* 매개 변수도 포함 해야 하며 지정 된 *DatabaseDeletionDate* 값에는 원하는 데이터베이스와 일치 하는 밀리초가 포함 되어야 합니다.

**AzureSqlDatabase** cmdlet은 서버에서 restorable 손실 된 모든 데이터베이스 또는 *DatabaseName* 과 *DatabaseDeletionDate* 와 모두 일치 하는 특정 데이터베이스 하나를 반환 합니다.
특정 이름의 모든 restorable 손실 된 데이터베이스와 같이 다른 조건을 충족 하는 restorable 데이터베이스를 반환 하려면 삭제 한 모든 데이터베이스를 반환 하 고 클라이언트에서 결과를 필터링 해야 합니다.

## 예제의

### 예제 1: 서버의 모든 데이터베이스 검색
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y"
```

이 명령은 lpqd0zbr8y 이라는 서버의 모든 데이터베이스를 검색 합니다.

### 예제 2: 서버에서 restorable 삭제 된 모든 데이터베이스 검색
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -RestorableDropped
```

이 명령은 lpqd0zbr8y 이라는 서버에서 restorable 손실 된 모든 데이터베이스를 검색 합니다.

### 예제 3: 연결 컨텍스트에 지정 된 서버에서 데이터베이스 검색
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01"
```

이 명령은 연결 컨텍스트 $Context에 지정 된 서버에서 Database01 이라는 데이터베이스를 검색 합니다.

### 예제 4: 변수에 데이터베이스 개체 저장
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01"
```

이 명령은 lpqd0zbr8y 이라는 서버에서 Database01 이라는 데이터베이스를 검색 합니다.
이 명령은 데이터베이스 개체를 $Database 01 변수에 저장 합니다.

### 예제 5: restorable 삭제 된 데이터베이스 검색
```
PS C:\> $DroppedDB = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01" -DatabaseDeletionDate "2012-11-09T22:59:43.000Z" -RestorableDropped
```

이 명령은 lpqd0zbr8y 서버에서 11/9/2012에 삭제 된 Database01 라는 restorable 데이터베이스를 검색 합니다.
이 명령은 $DroppedDB 변수에 결과를 저장 합니다.

### 예제 6: 서버에서 restorable 손실 된 모든 데이터베이스 검색 및 결과 필터링
```
PS C:\> Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -RestorableDropped | Where-Object {$_.Name -eq "ContactDB"}
```

이 명령은 lpqd0zbr8y 이라는 서버에서 restorable 손실 된 모든 데이터베이스를 검색 한 다음, 해당 결과를 라는 데이터베이스로만 필터링 합니다.

## 변수

### -ConnectionContext
데이터베이스를 검색할 서버의 연결 컨텍스트를 지정 합니다.

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -데이터베이스
이 cmdlet에서 검색 하는 데이터베이스를 나타내는 개체를 지정 합니다.

```yaml
Type: Database
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseDeletionDate
삭제 날짜와 시간을 지정 합니다.
*RestorableDropped* 매개 변수를 지정 하는 경우 삭제 날짜 및 시간을 기준으로 restorable 손실 된 데이터베이스를 검색 하려면이 매개 변수를 지정 합니다.

*DatabaseDeletionDate* 매개 변수는 원하는 데이터베이스 시간에 맞게 밀리초를 포함 해야 합니다.
값을 밀리초 없이 지정 하면 데이터베이스를 찾을 수 없습니다.

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

### -DatabaseName
이 cmdlet에서 검색 하는 데이터베이스의 이름을 지정 합니다.

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
이 cmdlet이 *데이터베이스* 개체 대신 *RestorableDroppedDatabase* 개체를 반환 함을 나타냅니다.
*DatabaseDeletionDate* 매개 변수를 사용 하 여 특정 restorable 끌어 놓은 데이터베이스를 선택할 수 있습니다.

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

### -RestorableDroppedDatabase
이 cmdlet에서 검색 하는 restorable 손실 된 데이터베이스를 나타내는 개체를 지정 합니다.

```yaml
Type: RestorableDroppedDatabase
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ServerName
이 cmdlet이 검색 하는 데이터베이스를 포함 하는 서버의 이름을 지정 합니다.
Cmdlet은 현재 Azure 구독을 사용 하 여 서버에 액세스 합니다.

```yaml
Type: String
Parameter Sets: ByServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### WindowsAzure. SqlDatabase. * 데이터베이스

### WindowsAzure. SqlDatabase에 대 한 RestorableDroppedDatabase

## 출력

### IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database\>
*RestorableDropped* 매개 변수를 지정 하지 않으면이 Cmdlet은 *Database* 개체를 반환 합니다.

### IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.RestorableDroppedDatabase\>
*RestorableDropped* 매개 변수를 지정 하면이 Cmdlet은 *RestorableDroppedDatabase* 개체를 반환 합니다.

## 상속자

## 관련 링크

[Azure SQL 데이터베이스](https://azure.microsoft.com/en-us/services/sql-database/)

[Azure SQL 데이터베이스에 대 한 작업](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[새로운 AzureSqlDatabase](./New-AzureSqlDatabase.md)

[새로운 AzureSqlDatabaseServerContext](./New-AzureSqlDatabaseServerContext.md)

[제거-AzureSqlDatabase](./Remove-AzureSqlDatabase.md)

[Set-AzureSqlDatabase](./Set-AzureSqlDatabase.md)


