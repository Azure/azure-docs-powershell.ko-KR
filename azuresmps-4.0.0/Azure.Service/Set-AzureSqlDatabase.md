---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: 82F4DB8F-8DAF-40D2-8031-3EDBF5D08417
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6274d3851042c15791707807471ae1bc6a2733ab
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045865"
---
# Set-AzureSqlDatabase

## SYNOPSIS
Azure SQL 데이터베이스에 대 한 속성을 설정 합니다.

## 구문과

### ByNameWithConnectionContext
```
Set-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -DatabaseName <String>
 [-NewDatabaseName <String>] [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByObjectWithConnectionContext
```
Set-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -Database <Database>
 [-NewDatabaseName <String>] [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByNameWithServerName
```
Set-AzureSqlDatabase -ServerName <String> -DatabaseName <String> [-NewDatabaseName <String>]
 [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### ByObjectWithServerName
```
Set-AzureSqlDatabase -ServerName <String> -Database <Database> [-NewDatabaseName <String>]
 [-Edition <DatabaseEdition>] [-MaxSizeGB <Int32>] [-MaxSizeBytes <Int64>]
 [-ServiceObjective <ServiceObjective>] [-PassThru] [-Force] [-Sync] [-Profile <AzureSMProfile>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## 설명은
**Set-AzureSqlDatabase** Cmdlet은 Azure SQL 데이터베이스의 속성을 설정 합니다.
이름을 기준으로 데이터베이스를 지정 하거나 파이프라인을 통해 Azure SQL 데이터베이스 개체를 전달할 수 있습니다.
이름을 기준으로 서버를 지정 하거나 Azure SQL 데이터베이스 서버 연결 컨텍스트를 전달할 수 있습니다.
**새 AzureSqlDatabaseServerContext** cmdlet을 실행 하 여 연결 컨텍스트를 만듭니다.
서버를 이름으로 지정 하는 경우 cmdlet은 현재 Azure 구독 정보를 사용 하 여 요청을 인증 합니다.

## 예제의

### 예제 1: 연결 컨텍스트를 사용 하 여 데이터베이스 크기 변경
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01"
PS C:\> Set-AzureSqlDatabase -ConnectionContext $Context -Database $Database01 -MaxSizeGB 20
```

이 예제에서는 Azure SQL 데이터베이스 서버 연결 컨텍스트 $Context에서 Database01 이라는 데이터베이스의 크기를 20gb로 변경 합니다.

### 예제 2: 서버 이름을 사용 하 여 데이터베이스 크기 변경
```
PS C:\> $Database01 = Get-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01"
PS C:\> Set-AzureSqlDatabase -ServerName "lpqd0zbr8y" -Database $Database01 -MaxSizeGB 20
```

이 예제에서는 lpqd0zbr8y 이라는 서버에서 Database01 이라는 데이터베이스의 크기를 20gb로 변경 합니다.

## 변수

### -ConnectionContext
서버의 연결 컨텍스트를 지정 합니다.

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByNameWithConnectionContext, ByObjectWithConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -데이터베이스
이 cmdlet이 수정 하는 Azure SQL 데이터베이스를 나타내는 개체를 지정 합니다.

```yaml
Type: Database
Parameter Sets: ByObjectWithConnectionContext, ByObjectWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseName
이 cmdlet이 수정 하는 데이터베이스의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: ByNameWithConnectionContext, ByNameWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -에디션
Azure SQL 데이터베이스에 대 한 새 버전을 지정 합니다.
유효한 값은 다음과 같습니다. 

- 않아야
- 웹
- 조직
- 기본적
- 표준이
-  Premium

```yaml
Type: DatabaseEdition
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
확인 메시지를 표시 하지 않고 작업을 완료할 수 있습니다.

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

### -MaxSizeBytes
데이터베이스의 새로운 최대 크기 (바이트)를 지정 합니다.
이 매개 변수 또는 *Maxsizegb* 매개 변수 중 하나를 지정할 수 있습니다.
에디션에 기반 하 여 허용 되는 값은 *Maxsizegb* 매개 변수를 참조 하세요.

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MaxSizeGB
데이터베이스의 새 최대 크기 (기가바이트)를 지정 합니다.
이 매개 변수 또는 *Maxsizebytes* 매개 변수 중 하나를 지정할 수 있습니다.
허용 되는 값은 버전에 따라 다릅니다.

기본 에디션 값: 1 또는 2

스탠더드 버전 값: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200 또는 250

Premium Edition 값: 1, 2, 5, 10, 20, 30, 40, 50, 100, 150, 200, 250, 300, 400, 500

웹 버전 값: 1 또는 5

Business Edition values: 10, 20, 30, 40, 50, 100 또는 150

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NewDatabaseName
데이터베이스의 새 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
Aliases: NewName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
업데이트 된 Azure SQL 데이터베이스를 반환 합니다.

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
이 cmdlet이 수정 하는 데이터베이스를 포함 하는 서버의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: ByNameWithServerName, ByObjectWithServerName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceObjective
이 데이터베이스에 대 한 새 서비스 목표 (성능 수준)를 나타내는 개체를 지정 합니다.
유효한 값은 다음과 같습니다. 

- 기본: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c
- Standard (S0): f1173c43-91bd-4aaa-973c-54e79e15235b
- 표준 (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928
- Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7
- * Standard (S3): 789681b8-ca10-4eb0-bdf2-e0b050601b40
- Premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d
- Premium (P2): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0
- 프리미엄 (P3): a7c4c615-cfb1-464b-b252-925be0a19446

* 표준 (S3)은 최신 SQL Database 업데이트 V12 (preview)의 일부입니다.
자세한 내용은 Azure SQL Database V12 Preview의 새로운 기능을 참조 하세요 https://azure.microsoft.com/documentation/articles/sql-database-preview-whats-new/ .

```yaml
Type: ServiceObjective
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -동기화
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

### -확인
Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.
Cmdlet이 실행 되지 않습니다.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

### WindowsAzure. SqlDatabase. * 데이터베이스

## 출력

### WindowsAzure. SqlDatabase. * 데이터베이스

## 상속자

## 관련 링크

[Azure SQL 데이터베이스](https://azure.microsoft.com/en-us/services/sql-database/)

[Azure SQL 데이터베이스에 대 한 작업](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[데이터베이스 업데이트](https://msdn.microsoft.com/en-us/library/azure/dn505718.aspx)

[Get-AzureSqlDatabase](./Get-AzureSqlDatabase.md)

[새로운 AzureSqlDatabase](./New-AzureSqlDatabase.md)

[제거-AzureSqlDatabase](./Remove-AzureSqlDatabase.md)

[새로운 AzureSqlDatabaseServerContext](./New-AzureSqlDatabaseServerContext.md)


