---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 5AEF7D44-624D-4794-86FF-156E6729BB56
online version: ''
schema: 2.0.0
ms.openlocfilehash: 95e276bf6af11698a4b3b82077175ec2ede2d7dc
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402425"
---
# Get-AzureSqlDatabaseCopy

## SYNOPSIS
복사 관계의 상태를 검사합니다.

## 구문

### ByServerNameOnly(기본값)
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

## 설명
**Get-AzureSqlDatabaseCopy** cmdlet은 하나 이상의 활성 복사 관계의 상태를 검사합니다.
cmdlet을 실행한 후 이 cmdlet을 Start-AzureSqlDatabaseCopy Stop-AzureSqlDatabaseCopy 실행합니다.
특정 복사 관계, 모든 복사 관계 또는 특정 대상 서버의 모든 복사본과 같은 필터링된 복사 관계 목록을 확인할 수 있습니다.
원본 또는 대상 데이터베이스를 호스트하는 서버에서 이 cmdlet을 실행할 수 있습니다.

이 cmdlet은 동기식입니다.
cmdlet은 상태 개체를 반환할 때까지 Azure PowerShell 콘솔을 차단합니다.

*PartnerServer 및* *PartnerDatabase* 매개 변수는 선택 사항입니다.
매개 변수를 지정하지 않으면 이 cmdlet은 결과 테이블을 반환합니다.
특정 데이터베이스에 대한 상태만 확인하려면 두 매개 변수를 모두 지정합니다.

## 예제

### 예제 1: 데이터베이스의 복사 상태 확인
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

이 명령은 lpqd0zbr8y라는 서버에서 Orders라는 데이터베이스의 상태를 얻습니다.
*PartnerServer 매개* 변수는 이 명령을 bk0b8kf658 서버로 제한합니다.

### 예제 2: serverGet 서버의 모든 복사본 상태 확인
```
PS C:\> Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y"
```

이 명령은 lpqd0zbr8y라는 서버에서 모든 활성 복사본의 상태를 얻습니다.

## PARAMETERS

### -Database
원본 Azure SQL 데이터베이스를 나타내는 개체를 지정합니다.
이 cmdlet은 이 매개 변수가 지정하는 데이터베이스의 복사 상태를 얻습니다.

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
데이터베이스를 나타내는 개체를 지정합니다.
이 cmdlet은 이 매개 변수가 지정하는 데이터베이스의 복사 상태를 얻습니다.
이 매개 변수는 파이프라인 입력을 허용합니다.

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
원본 데이터베이스의 이름을 지정합니다.
이 cmdlet은 이 매개 변수가 지정하는 데이터베이스의 복사 상태를 얻습니다.

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

### -PartnerDatabase
보조 데이터베이스의 이름을 지정합니다.
이 데이터베이스를 동적 관리 sys.dm_database_copies 찾을 수 없는 경우 이 cmdlet은 빈 상태 개체를 반환합니다.

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

### -PartnerServer
대상 데이터베이스를 호스트하는 서버의 이름을 지정합니다.
이 서버가 동적 관리 sys.dm_database_copies 없는 경우 이 cmdlet은 빈 상태 개체를 반환합니다.

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

### -Profile
이 cmdlet이 읽을 Azure 프로필을 지정합니다.
프로필을 지정하지 않으면 이 cmdlet은 로컬 기본 프로필에서 읽습니다.

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
데이터베이스 복사본이 있는 서버의 이름을 지정합니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy

### Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database

## 출력

### Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy

## 참고 사항
* 인증: 이 cmdlet에는 인증서 기반 인증이 필요합니다. 인증서 기반 인증을 사용하여 현재 구독을 설정하는 방법의 예제는 New-AzureSqlDatabaseServerContext cmdlet을 참조하세요.

## 관련 링크

[Azure SQL Database](https://azure.microsoft.com/en-us/services/sql-database/)

[Azure SQL 데이터베이스에 대한 작업](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)



[Start-AzureSqlDatabaseCopy](./Start-AzureSqlDatabaseCopy.md)

[Stop-AzureSqlDatabaseCopy](./Stop-AzureSqlDatabaseCopy.md)


