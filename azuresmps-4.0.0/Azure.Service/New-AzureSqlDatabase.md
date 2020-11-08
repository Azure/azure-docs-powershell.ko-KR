---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: F4FE79DB-B481-49BD-A33B-7C642A136890
online version: ''
schema: 2.0.0
ms.openlocfilehash: 588fcf73c258364e41117eed05c62de7eaa231e9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045973"
---
# New-AzureSqlDatabase

## SYNOPSIS
Azure SQL 데이터베이스를 만듭니다.

## 구문과

### ByConnectionContext
```
New-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -DatabaseName <String>
 [-Collation <String>] [-Edition <DatabaseEdition>] [-ServiceObjective <ServiceObjective>] [-MaxSizeGB <Int32>]
 [-MaxSizeBytes <Int64>] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByServerName
```
New-AzureSqlDatabase -ServerName <String> -DatabaseName <String> [-Collation <String>]
 [-Edition <DatabaseEdition>] [-ServiceObjective <ServiceObjective>] [-MaxSizeGB <Int32>]
 [-MaxSizeBytes <Int64>] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**AzureSqlDatabase** Cmdlet은 Azure SQL 데이터베이스를 만듭니다.
**새 AzureSqlDatabaseServerContext** cmdlet을 사용 하 여 만든 Azure SQL 데이터베이스 서버 연결 컨텍스트를 사용 하 여 서버를 지정할 수 있습니다.
또는 서버 이름을 지정 하는 경우 cmdlet은 현재 Azure 구독 정보를 사용 하 여 서버에 대 한 액세스 요청을 인증 합니다.

Azure SQL 데이터베이스 서버를 지정 하 여 새 데이터베이스를 만들면 **새 AzureSqlDatabase** cmdlet이 지정 된 서버 이름과 현재 Azure 구독 정보를 사용 하 여 임시 연결 컨텍스트를 만들어 작업을 수행 합니다.

## 예제의

### 예제 1: 데이터베이스 만들기
```
PS C:\> $Database01 = New-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01" -Edition "Business" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

이 명령은 Azure SQL 데이터베이스 서버 연결 컨텍스트 $Context에 Database1 이라는 Azure SQL 데이터베이스를 만듭니다.

### 예제 2: 현재 구독에서 데이터베이스 만들기
```
PS C:\> $Database01 = New-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01" -Edition "Business" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

이 예제에서는 lpqd0zbr8y 이라는 지정 된 Azure SQL 데이터베이스 서버에 Database1 이라는 데이터베이스를 만듭니다.
Cmdlet은 현재 Azure 구독 정보를 사용 하 여 서버에 대 한 요청을 인증 합니다.

## 변수

### -데이터 정렬
새 데이터베이스에 대 한 데이터 정렬을 지정 합니다.

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

### -ConnectionContext
이 cmdlet이 데이터베이스를 만드는 서버의 연결 컨텍스트를 지정 합니다.

```yaml
Type: IServerDataServiceContext
Parameter Sets: ByConnectionContext
Aliases: Context

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseName
새 데이터베이스의 이름을 지정 합니다.

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

### -에디션
새 Azure SQL 데이터베이스의 에디션을 지정 합니다.
유효한 값은 다음과 같습니다. 

- 않아야
- 웹
- 조직
- 기본적
- 표준이
-  Premium

기본값은 웹용 값입니다.

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
사용자에 게 확인 메시지를 표시 하지 않고 작업을 완료할 수 있도록 합니다.

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
데이터베이스의 최대 크기 (바이트)를 지정 합니다.
이 매개 변수 또는 *Maxsizegb* 매개 변수 중 하나를 지정할 수 있습니다.
에디션에 기반 하 여 허용 되는 값에 대 한 *Maxsizegb* 매개 변수 설명을 참조 하세요.

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
데이터베이스의 최대 크기 (기가바이트)를 지정 합니다.
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
새 데이터베이스를 포함할 Azure SQL 데이터베이스 서버의 이름을 지정 합니다.

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
이 데이터베이스에 대 한 새 서비스 목표 (성능 수준)를 나타내는 개체를 지정 합니다.
이 값은이 데이터베이스에 할당 된 리소스 수준을 나타냅니다.
유효한 값은 다음과 같습니다. 

기본: dd6d99bb-f193-4ec1-86f2-43d3bccbc49c Standard (S0): f1173c43-91bd-4aaa-973c-54e79e15235b Standard (S1): 1b1ebd4d-d903-4baa-97f9-4ea675f5e928 Standard (S2): 455330e1-00cd-488b-b5fa-177c226f28b7 * Standard (S3): 89681b8-7203483a-c4fb-4304-9e9f-17c71c904f5d 10-4eb0-bdf2-e0b050601b40premium (P1): 7203483a-c4fb-4304-9e9f-17c71c904f5d premium (P1): a7d1b92d-c987-4375-b54d-2b1d0e0f5bb0 premium (P3): a7c4c615-cfb1-464b-b252-925be0a19446 Premium (P3):

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

## 출력

### WindowsAzure. SqlDatabase. * 데이터베이스

## 상속자
* **새 AzureSqlDatabase** 에서 만든 데이터베이스를 삭제 하려면 Remove-AzureSqlDatabase cmdlet을 사용 합니다.

## 관련 링크

[Azure SQL 데이터베이스](https://azure.microsoft.com/en-us/services/sql-database/)

[데이터베이스 만들기](https://msdn.microsoft.com/en-us/library/azure/dn505701.aspx)

[Azure SQL 데이터베이스에 대 한 작업](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-AzureSqlDatabase](./Get-AzureSqlDatabase.md)

[새로운 AzureSqlDatabaseServerContext](./New-AzureSqlDatabaseServerContext.md)

[제거-AzureSqlDatabase](./Remove-AzureSqlDatabase.md)

[Set-AzureSqlDatabase](./Set-AzureSqlDatabase.md)


