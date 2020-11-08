---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: CB601E21-424D-4B09-85E5-A4B2A5068267
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2b7674cb5b7abc489dc6aa6d3746f499b9686312
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046403"
---
# Stop-AzureSqlDatabaseCopy

## SYNOPSIS
연속 복사 관계를 종료 합니다.

## 구문과

### ByInputObject
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseCopy <DatabaseCopy> [-ForcedTermination] [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByDatabase
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -Database <Database> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### ByDatabaseName
```
Stop-AzureSqlDatabaseCopy -ServerName <String> -DatabaseName <String> [-PartnerServer <String>]
 [-PartnerDatabase <String>] [-ForcedTermination] [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## 설명은
**AzureSqlDatabaseCopy** cmdlet은 연속 복사 관계를 종료 합니다.
이 cmdlet은 원본 데이터베이스와 보조 또는 대상 데이터베이스 간의 데이터 이동을 중지 한 다음 보조 데이터베이스의 상태를 독립 실행형 온라인 데이터베이스로 변경 합니다.

연속 복사 관계, 종료 또는 계획 된 종료 및 데이터 손실 가능성을 가진 강제 종료를 두 가지 방법으로 끝낼 수 있습니다.
원본 데이터베이스를 호스트 하는 서버에서이 cmdlet을 종료 또는 강제 종료 모드에서 실행할 수 있습니다.
보조 데이터베이스를 호스팅하는 서버에서 강제 종료 모드를 사용 해야 합니다.

계획 된 종료는 cmdlet을 실행할 때 원본 데이터베이스에서 커밋된 모든 트랜잭션이 보조 데이터베이스로 복제 될 때까지 대기 합니다.
강제 종료는 처리 되지 않은 커밋된 거래의 복제를 기다리지 않으며 보조 데이터베이스에서 가능한 데이터 손실을 유발할 수 있습니다.

복제 상태가 보류 중 이지만 강제 종료는 연속 복사 관계를 성공적으로 종료할 수 있습니다.
복제 상태가 보류 중인 경우 강제 적용 되지 않는 종료는 지원 되지 않습니다.

## 예제의

### 예제 1: 연속 복사 관계 종료
```
PS C:\>Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

이 명령은 lpqd0zbr8y 이라는 서버에서 Order 라는 데이터베이스의 연속 복사 관계를 종료 합니다.
Bk0b8kf658 라는 서버는 보조 데이터베이스를 호스팅합니다.

### 예제 2: 연속 복사 관계 강제 종료
```
PS C:\>$DatabaseCopy = Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders"
PS C:\> $DatabaseCopy | Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -ForcedTermination
```

첫 번째 명령은 lpqd0zbr8y 이라는 서버에서 Order 라는 데이터베이스의 데이터베이스 복사 관계를 가져옵니다.

두 번째 명령은 보조 데이터베이스를 호스트 하는 서버에서 연속 복사 관계를 강제로 종료 합니다.

## 변수

### -데이터베이스
원본 Azure SQL 데이터베이스를 나타내는 개체를 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 데이터베이스의 연속 복사 관계를 종료 합니다.

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
이 cmdlet은이 매개 변수에서 지정 하는 데이터베이스의 연속 복사 관계를 종료 합니다.
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
데이터베이스의 이름을 지정 합니다.
이 cmdlet은이 매개 변수에서 지정 하는 데이터베이스의 연속 복사 관계를 종료 합니다.

```yaml
Type: String
Parameter Sets: ByDatabaseName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.

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

### -ForcedTermination
이 cmdlet이 연속 복사 관계의 강제 종료를 발생 시키는 것을 나타냅니다.
강제 종료로 인해 데이터가 손실 될 수 있습니다.
대상 데이터베이스를 호스트 하는 서버에서이 cmdlet을 실행 하려면이 매개 변수를 지정 해야 합니다.
원본 데이터베이스를 호스트 하는 서버에서이 cmdlet을 실행 하려면 보조 데이터베이스를 사용할 수 없는 경우이 매개 변수를 지정 해야 합니다.

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

### -데이터 데이터베이스
보조 데이터베이스의 이름을 지정 합니다.
이름을 지정 하는 경우에는 원본 데이터베이스의 이름과 일치 해야 합니다.

```yaml
Type: String
Parameter Sets: ByDatabase, ByDatabaseName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -또는 서버
대상 데이터베이스를 호스트 하는 서버의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: ByDatabase, ByDatabaseName
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
원본 데이터베이스가 상주 하는 서버의 이름을 지정 합니다.

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

### WindowsAzure. SqlDatabase. DatabaseCopy

### WindowsAzure. SqlDatabase. * 데이터베이스

## 출력

### 않아야

## 상속자
* 인증:이 cmdlet을 사용 하려면 인증서 기반 인증이 필요 합니다. 인증서 기반 인증을 사용 하 여 현재 구독을 설정 하는 방법의 예는 **AzureSqlDatabaseServerContext** cmdlet을 참조 하세요.
* 제한: 보조 데이터베이스를 호스트 하는 서버에서 강제 종료만 지원 됩니다.
* 이전 보조 데이터베이스의 종료에 대 한 영향: 종료 후 보조 데이터베이스가 독립 데이터베이스가 됩니다. 보조 데이터베이스에서 시드가 이미 완료 된 경우이 데이터베이스는 전체 액세스 권한이 열려 있습니다. 원본 데이터베이스가 읽기-쓰기 데이터베이스인 경우 이전 보조 데이터베이스도 읽기/쓰기 데이터베이스가 됩니다.

  현재 시드가 진행 중인 경우 시드가 중단 되 고, 보조 데이터베이스를 호스트 하는 서버에 이전 보조 데이터베이스가 표시 되지 않습니다.

* 원본 데이터베이스를 읽기 전용 모드로 설정할 수 있습니다. 이렇게 하면 원본 및 보조 데이터베이스가 종료 된 후에 동기화 되며 종료 중에 트랜잭션이 커밋되지 않도록 합니다. 종료가 완료 되 면 원본을 읽기-쓰기 모드로 다시 설정 합니다. 필요에 따라 이전 보조 데이터베이스를 읽기-쓰기 모드로 설정할 수도 있습니다.
* 모니터링: 연속 복사 관계의 원본 및 대상 모두에서 작업의 상태를 확인 하려면 **AzureSqlDatabaseOperation** cmdlet을 사용 합니다.

## 관련 링크

[Azure SQL 데이터베이스](https://azure.microsoft.com/en-us/services/sql-database/)

[Azure SQL 데이터베이스에 대 한 작업](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[데이터베이스 복사본 중지](https://msdn.microsoft.com/en-us/library/dn509573.aspx)

[Azure SQL 데이터베이스 Cmdlet](./Azure.SQLDatabase.md)

[Get-AzureSqlDatabaseCopy](./Get-AzureSqlDatabaseCopy.md)

[시작-AzureSqlDatabaseCopy](./Start-AzureSqlDatabaseCopy.md)


