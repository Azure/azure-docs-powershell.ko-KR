---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 5AEF7D44-624D-4794-86FF-156E6729BB56
online version: ''
schema: 2.0.0
ms.openlocfilehash: f8752766572975ef97094a3915446086c903a7fd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046295"
---
# Get-AzureSqlDatabaseCopy

## SYNOPSIS
복사 관계의 상태를 확인 합니다.

## 구문과

### ByServerNameOnly (기본값)
```
Get-AzureSqlDatabaseCopy -ServerName <String> [-DatabaseName <String>] [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByInputObject
```
Get-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### ByDatabase
```
Get-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**AzureSqlDatabaseCopy** cmdlet은 하나 이상의 활성 복사본 관계의 상태를 확인 합니다.
Start-AzureSqlDatabaseCopy 또는 Stop-AzureSqlDatabaseCopy cmdlet을 실행 한 후이 cmdlet을 실행 합니다.
특정 복사본 관계, 모든 관계 복사 또는 특정 대상 서버의 모든 복사본과 같이 필터링 된 복사본 관계 목록을 확인할 수 있습니다.
원본 또는 대상 데이터베이스를 호스트 하는 서버에서이 cmdlet을 실행할 수 있습니다.

이 cmdlet은 동기적으로 실행할 수 있습니다.
Cmdlet은 status 개체를 반환할 때까지 Azure PowerShell 콘솔을 차단 합니다.

함께 *서버* 및 함께 *데이터베이스* 매개 변수를 선택 합니다.
매개 변수 중 하나를 지정 하지 않으면이 cmdlet은 결과 테이블을 반환 합니다.
특정 데이터베이스의 상태만 보려면 두 매개 변수를 모두 지정 합니다.

## 예제의

### 예제 1: 데이터베이스의 복사 상태 가져오기
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

이 명령은 lpqd0zbr8y 이라는 서버에서 Order 라는 데이터베이스의 상태를 가져옵니다.
함께 *서버* 매개 변수는이 명령을 bk0b8kf658 서버로 제한 합니다.

### 예제 2: 서버의 모든 복사본 상태 가져오기 서버에 있는 모든 복사본의 상태 가져오기
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y"
```

이 명령은 lpqd0zbr8y 이라는 서버에 있는 모든 활성 복사본의 상태를 가져옵니다.

## 변수

### -데이터베이스
원본 Azure SQL 데이터베이스를 나타내는 개체를 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 데이터베이스의 복사본 상태를 가져옵니다.

```yaml
Type: Database
Parameter Sets: ByDatabase
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseCopy
데이터베이스를 나타내는 개체를 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 데이터베이스의 복사본 상태를 가져옵니다.
이 매개 변수는 파이프라인 입력을 허용 합니다.

```yaml
Type: DatabaseCopy
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseName
원본 데이터베이스의 이름을 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 데이터베이스의 복사본 상태를 가져옵니다.

```yaml
Type: String
Parameter Sets: ByServerNameOnly
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -데이터 데이터베이스
보조 데이터베이스의 이름을 지정 합니다.
Sys.dm_database_copies 동적 관리 보기에서이 데이터베이스를 찾을 수 없는 경우이 cmdlet은 빈 상태 개체를 반환 합니다.

```yaml
Type: String
Parameter Sets: ByServerNameOnly, ByDatabase
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -또는 서버
대상 데이터베이스를 호스트 하는 서버의 이름을 지정 합니다.
Sys.dm_database_copies 동적 관리 보기에서이 서버를 찾을 수 없는 경우이 cmdlet은 빈 상태 개체를 반환 합니다.

```yaml
Type: String
Parameter Sets: ByServerNameOnly, ByDatabase
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

### -ServerName
데이터베이스 복사본이 있는 서버의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### WindowsAzure. SqlDatabase. DatabaseCopy

### WindowsAzure. SqlDatabase. * 데이터베이스

## 출력

### WindowsAzure. SqlDatabase. DatabaseCopy

## 상속자
* 인증:이 cmdlet을 사용 하려면 인증서 기반 인증이 필요 합니다. 인증서 기반 인증을 사용 하 여 현재 구독을 설정 하는 방법에 대 한 예제는 New-AzureSqlDatabaseServerContext cmdlet을 참조 하세요.

## 관련 링크

[Azure SQL 데이터베이스](https://azure.microsoft.com/en-us/services/sql-database/)

[Azure SQL 데이터베이스에 대 한 작업](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Azure SQL 데이터베이스 Cmdlet](./Azure.SQLDatabase.md)

[시작-AzureSqlDatabaseCopy](./Start-AzureSqlDatabaseCopy.md)

[중지-AzureSqlDatabaseCopy](./Stop-AzureSqlDatabaseCopy.md)


