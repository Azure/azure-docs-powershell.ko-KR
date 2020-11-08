---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 83E8DAD8-151A-408D-819F-274CB813ABDA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6f9a5753fdf4f87afc6baacbe9fc4c33c9be08ef
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046559"
---
# Get-AzureSqlRecoverableDatabase

## SYNOPSIS
지정 된 서버에서 복구 가능한 데이터베이스를 가져옵니다.

## 구문과

### AllDatabasesOnGivenServer (기본값)
```
Get-AzureSqlRecoverableDatabase -ServerName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### GivenDatabaseOnGivenServer
```
Get-AzureSqlRecoverableDatabase -ServerName <String> -DatabaseName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### GivenDatabaseObject
```
Get-AzureSqlRecoverableDatabase -Database <RecoverableDatabase> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## 설명은
**AzureSqlRecoverableDatabase** cmdlet은 지정 된 서버에서 복구 가능한 데이터베이스를 가져옵니다.
이 cmdlet은 복구 가능한 특정 데이터베이스 또는 서버의 복구 가능한 모든 데이터베이스를 가져옵니다.

## 예제의

### 예제 1: 복구 가능한 모든 데이터베이스 가져오기
```
PS C:\> Get-AzureSqlRecoverableDatabase -ServerName "Server01"
```

이 명령은 Server01 이라는 서버의 복구 가능한 모든 데이터베이스를 가져옵니다.

### 예제 2: 복구 가능한 특정 데이터베이스 가져오기
```
PS C:\> Get-AzureSqlRecoverableDatabase -ServerName "Server01" -DatabaseName "Database17"
```

이 명령은 Server01 이라는 서버에서 Database17 이라는 데이터베이스를 검색 합니다.

## 변수

### -데이터베이스
이 cmdlet이 가져오는 복구 가능한 데이터베이스를 나타내는 개체를 지정 합니다.

```yaml
Type: RecoverableDatabase
Parameter Sets: GivenDatabaseObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseName
이 cmdlet이 가져오는 복구 가능한 데이터베이스의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: GivenDatabaseOnGivenServer
Aliases: 

Required: True
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
이 cmdlet이 복구 가능한 데이터베이스를 가져오는 서버의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: AllDatabasesOnGivenServer, GivenDatabaseOnGivenServer
Aliases: 

Required: True
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

### IEnumerable\<Microsoft.WindowsAzure.Management.Sql.Models.RecoverableDatabase\>

## 상속자
* 이 cmdlet을 실행 하려면 인증서 기반 인증을 사용 해야 합니다. 이 cmdlet을 실행 하는 컴퓨터에서 다음 명령을 실행 합니다. 

`PS C:\\\> $subId = \<Subscription ID\>`
`PS C:\\\> $thumbprint = \<Certificate Thumbprint\>`
`PS C:\\\> $myCert = Get-Item Cert:\CurrentUser\My\$thumbprint`
`PS C:\\\> Set-AzureSubscription -SubscriptionName "mySubscription" -SubscriptionId $subId -Certificate $myCert`
`PS C:\\\> Select-AzureSubscription -SubscriptionName "mySubscription"`

## 관련 링크

[Azure SQL 데이터베이스](https://azure.microsoft.com/en-us/services/sql-database/)

[복구 가능한 데이터베이스 가져오기](https://msdn.microsoft.com/en-us/library/azure/dn800985.aspx)

[Azure SQL 데이터베이스에 대 한 작업](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[시작-AzureSqlDatabaseRecovery](./Start-AzureSqlDatabaseRecovery.md)


