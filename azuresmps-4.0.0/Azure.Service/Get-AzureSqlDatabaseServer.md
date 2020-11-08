---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 0ACEDE22-1C2B-4846-A949-710AF6C148D0
online version: ''
schema: 2.0.0
ms.openlocfilehash: d513d6d019c84984923541624063e657e2250b61
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045571"
---
# Get-AzureSqlDatabaseServer

## SYNOPSIS
Azure SQL 데이터베이스 서버에 대 한 정보를 가져옵니다.

## 구문과

```
Get-AzureSqlDatabaseServer [-ServerName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**AzureSqlDatabaseServer** cmdlet은 현재 구독에 있는 Azure SQL 데이터베이스 서버의 인스턴스에 대 한 정보를 가져옵니다.
서버를 이름으로 지정 하면이 cmdlet은 해당 서버에 대 한 정보를 포함 하는 개체를 반환 합니다.
그렇지 않으면 cmdlet이 모든 서버에 대 한 정보를 반환 합니다.

## 예제의

### 예제 1: 모든 서버에 대 한 정보 가져오기
```
PS C:\> Get-AzureSqlDatabaseServer
```

이 명령은 현재 구독에서 Azure SQL 데이터베이스 서버의 모든 인스턴스에 대 한 정보를 반환 합니다.

### 예제 2: 특정 서버에 대 한 정보 가져오기
```
PS C:\> Get-AzureSqlDatabaseServer -ServerName "lpqd0zbr8y"
```

이 명령은 lpqd0zbr8y 이라는 서버에 대 한 정보를 반환 합니다.

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

### -ServerName
이 cmdlet이 제거할 서버의 이름을 지정 합니다.
정규화 된 DNS 이름이 아니라 서버 이름을 지정 합니다.

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

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### WindowsAzure. SqlDatabase. SqlDatabaseServerContext

## 출력

### IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerContext\>

## 상속자

## 관련 링크

[Azure SQL 데이터베이스](https://azure.microsoft.com/en-us/services/sql-database/)

[서버 목록 표시](https://msdn.microsoft.com/en-us/library/azure/dn505702.aspx)

[Azure SQL 데이터베이스에 대 한 작업](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[새로운 AzureSqlDatabaseServer](./New-AzureSqlDatabaseServer.md)

[제거-AzureSqlDatabaseServer](./Remove-AzureSqlDatabaseServer.md)

[Set-AzureSqlDatabaseServer](./Set-AzureSqlDatabaseServer.md)


