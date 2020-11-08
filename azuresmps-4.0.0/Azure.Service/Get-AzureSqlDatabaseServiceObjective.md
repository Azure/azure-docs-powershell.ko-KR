---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: A2C22A8A-EF50-4BE3-82DF-5ED6F69C00CA
online version: ''
schema: 2.0.0
ms.openlocfilehash: 457775a74fb7921a3c8b6b5e635bd7df7e704faa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045568"
---
# Get-AzureSqlDatabaseServiceObjective

## SYNOPSIS
Azure SQL 데이터베이스 서버의 서비스 목표를 가져옵니다.

## 구문과

### ByConnectionContext (기본값)
```
Get-AzureSqlDatabaseServiceObjective -Context <IServerDataServiceContext>
 [-ServiceObjective <ServiceObjective>] [-ServiceObjectiveName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### ByServerName
```
Get-AzureSqlDatabaseServiceObjective -ServerName <String> [-ServiceObjective <ServiceObjective>]
 [-ServiceObjectiveName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**AzureSqlDatabaseServiceObjective** Cmdlet은 Azure SQL 데이터베이스 서버의 서비스 목표를 가져옵니다.
서비스 목표는 성능 수준 이라고 합니다.
서비스 목표를 지정 하지 않으면이 cmdlet은 지정 된 서버에 대 한 유효한 서비스 목표를 모두 반환 합니다.

이 cmdlet은 기본, 표준 및 프리미엄 서비스 계층에 적용 됩니다.

## 예제의

### 예제 1: 연결 컨텍스트를 사용 하 여 모든 서비스 목표 가져오기
```
PS C:\> Get-AzureSqlDatabaseServiceObjective -Context $Context
```

이 명령은 연결 컨텍스트에서 $Context 지정 하는 서버의 모든 서비스 목표를 가져옵니다.

### 예제 2: 서버 이름을 사용 하 여 모든 서비스 목표 가져오기
```
PS C:\> Get-AzureSqlDatabaseServiceObjective -ServerName "Server01"
```

이 명령은 Server01 이라는 서버에 대 한 모든 서비스 목표를 가져옵니다.

## 변수

### -컨텍스트
서버의 연결 컨텍스트를 지정 합니다.

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: 

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

### -ServiceObjective
이 cmdlet이 가져오는 서비스 목표를 나타내는 개체를 지정 합니다.
유효한 값은 다음과 같습니다. 

- 기본: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c
- Standard (S0): f1173c43-91bd-4aaa-973c-54e79e15235b
- 표준 (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928
- Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7
- * Standard (S3): 789681b8-ca10-4eb0-bdf2-e0b050601b40
- Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d
- Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d
- Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0
- 프리미엄 (P3): a7c4c615-cfb1-464b-b252-925be0a19446

* 표준 (S3)은 최신 SQL Database 업데이트 V12 (preview)의 일부입니다.
자세한 내용은 Azure library의 [AZURE SQL Database V12 Preview ()에 있는 새로운 기능](https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/) 을 참조 하세요 `https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/` .

```yaml
Type: ServiceObjective
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ServiceObjectiveName
가져올 서비스 목표의 이름을 지정 합니다.
유효한 값은 Basic, S0, S1, S2, S3, P1, P2, P3입니다.

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

### WindowsAzure. SqlDatabase의 목표입니다.

## 출력

### IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.ServiceObjective\>

## 상속자

## 관련 링크

[Azure SQL 데이터베이스](https://msdn.microsoft.com/library/ee336279.aspx)

[서비스 수준 목표 가져오기](https://msdn.microsoft.com/en-us/library/azure/dn505709.aspx)

[Azure SQL 데이터베이스에 대 한 작업](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[새로운 AzureSqlDatabaseServerContext](./New-AzureSqlDatabaseServerContext.md)


