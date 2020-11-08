---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 6723557D-8052-4BFA-872C-384B1423B3AE
online version: ''
schema: 2.0.0
ms.openlocfilehash: 185ad06375fe9bbd11cb25c26b25704baeaa1dfe
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045570"
---
# Get-AzureSqlDatabaseServerQuota

## SYNOPSIS
Azure SQL 데이터베이스 서버에 대 한 할당량 정보를 가져옵니다.

## 구문과

### ByConnectionContext
```
Get-AzureSqlDatabaseServerQuota -ConnectionContext <IServerDataServiceContext> [-QuotaName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByServerName
```
Get-AzureSqlDatabaseServerQuota -ServerName <String> [-QuotaName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## 설명은
**AzureSqlDatabaseServerQuota** cmdlet은 지정 된 Azure SQL 데이터베이스 서버의 인스턴스에 대 한 할당량 정보를 가져옵니다.
연결 컨텍스트 또는 서버 이름을 지정 합니다.
할당량 이름을 지정 하지 않으면이 cmdlet은 서버에 대 한 모든 할당량 정보를 가져옵니다.

## 예제의

### 예제 1: 특정 할당량에 대 한 정보 가져오기
```
PS C:\> $QuotaPremium = GetAzureSqlDatabaseServerQuota $Context -QuotaName "Premium_Databases"
```

이 명령은 $Context 변수에 저장 된 연결에서 지정한 Azure SQL 데이터베이스 서버에서 Premium_Databases 라는 할당량을 가져옵니다.

### 예제 2: 모든 할당량에 대 한 정보 가져오기
```
PS C:\> $QuotaList = GetAzureSqlDatabaseServerQuota $Context
```

이 명령은 연결 $Context에 지정 된 서버에서 모든 할당량 값을 가져옵니다.

## 변수

### -ConnectionContext
서버의 연결 컨텍스트를 지정 합니다.

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

### -QuotaName
이 cmdlet이 가져오는 할당량 값의 이름을 지정 합니다.

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

### -ServerName
서버의 이름을 지정 합니다.

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

## 출력

### WindowsAzure. SqlDatabase?. ServerQuota []

## 상속자
* 인증:이 cmdlet은 SQL Server 인증 또는 인증서 기반 인증을 사용할 수 있습니다. 인증 설정에 대 한 예제는 New-AzureSqlDatabaseServerContext cmdlet을 참조 하세요.

## 관련 링크

[Azure SQL 데이터베이스](https://azure.microsoft.com/en-us/services/sql-database/)

[Azure SQL 데이터베이스에 대 한 작업](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[새로운 AzureSqlDatabaseServerContext](./New-AzureSqlDatabaseServerContext.md)


