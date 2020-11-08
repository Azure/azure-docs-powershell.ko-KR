---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 56026A74-A6DC-47A5-9643-5828C3D0E83B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 32219154f2036ee028b05a369c46be1d8e1def87
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046293"
---
# Get-AzureSqlDatabaseOperation

## SYNOPSIS
Azure 서버에서 데이터베이스 작업의 상태를 가져옵니다.

## 구문과

### ByConnectionContext (기본값)
```
Get-AzureSqlDatabaseOperation -ConnectionContext <IServerDataServiceContext> [-Database <Database>]
 [-DatabaseName <String>] [-OperationGuid <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByServerName
```
Get-AzureSqlDatabaseOperation -ServerName <String> [-Database <Database>] [-DatabaseName <String>]
 [-OperationGuid <Guid>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**AzureSqlDatabaseOperation** cmdlet은 지정 된 Azure 서버에서 데이터베이스 작업의 상태를 가져옵니다.
*ServerName* 또는 *connectioncontext* 매개 변수만 지정 하는 경우에는 cmdlet에서 서버에 대 한 모든 데이터베이스 작업을 가져옵니다.
*데이터베이스* 또는 *DatabaseName* 매개 변수를 사용 하 여 데이터베이스를 지정 하는 경우이 cmdlet은 지정 된 데이터베이스에 대 한 모든 작업을 가져옵니다.
작업 GUID와 *ServerName* 또는 *connectioncontext* 를 지정 하면 cmdlet은 단일 데이터베이스 작업을 가져옵니다.

## 예제의

### 예제 1: 데이터베이스에 대 한 모든 데이터베이스 작업의 상태 가져오기
```
PS C:\> $Operations = Get-AzureSqlDatabaseOperation -ConnectionContext $Context -DatabaseName "Database17"
```

이 명령은 연결 컨텍스트가 $Context 지정 하는 서버의 Database17 이라는 데이터베이스에서 모든 데이터베이스 작업의 상태를 가져옵니다.

### 예제 2: 서버에 대 한 모든 데이터베이스 작업의 상태 가져오기
```
PS C:\> $Operations = Get-AzureSqlDatabaseOperation -ConnectionContext $Context
```

이 명령은 연결 컨텍스트가 $Context 지정 하는 서버에 있는 모든 데이터베이스 작업의 상태를 가져옵니다.

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

### -데이터베이스
Azure SQL 데이터베이스를 나타내는 개체를 지정 합니다.
이 매개 변수를 지정 하는 경우 *ServerName* 매개 변수 또는 *connectioncontext* 매개 변수를 지정 해야 합니다.

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

### -DatabaseName
데이터베이스의 이름을 지정 합니다.
이 매개 변수를 지정 하는 경우 *ServerName* 매개 변수 또는 *connectioncontext* 매개 변수를 지정 해야 합니다.

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

### -OperationGuid
이 cmdlet이 상태를 가져오는 특정 데이터베이스 작업을 나타내는 작업 ID를 지정 합니다.
Azure SQL 데이터베이스 또는 서버에 대 한 모든 데이터베이스 작업을 요청 하 여 작업 Id를 얻을 수 있습니다.
이 매개 변수를 지정 하는 경우 *ServerName* 매개 변수 또는 *connectioncontext* 매개 변수를 지정 해야 합니다.

```yaml
Type: Guid
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### WindowsAzure. SqlDatabase. * 데이터베이스

### WindowsAzure. SqlDatabase. SqlDatabaseServerContext

### 시스템 Guid

## 출력

### WindowsAzure. SqlDatabase. * 데이터베이스의 DatabaseOperationResponseList []
이 cmdlet은 여러 작업을 가져오는 경우 **Databaseoperationresponselist** 개체의 배열을 반환 합니다.

### WindowsAzure를 SqlDatabase. *. DatabaseOperationResponse

## 상속자

## 관련 링크

[Azure SQL 데이터베이스](https://msdn.microsoft.com/library/ee336279.aspx)

[데이터베이스 작업 상태](https://msdn.microsoft.com/en-us/library/azure/dn720371.aspx)

[Azure SQL 데이터베이스에 대 한 작업](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-AzureSqlDatabase](./Get-AzureSqlDatabase.md)

[새로운 AzureSqlDatabaseServerContext](./New-AzureSqlDatabaseServerContext.md)


