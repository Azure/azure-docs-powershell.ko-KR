---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: CB601E21-424D-4B09-85E5-A4B2A5068267
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7716587787515221a6e016436a6e3d030c1ab0eb
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405621"
---
# Stop-AzureSqlDatabaseCopy

## SYNOPSIS
연속 복사 관계를 종료합니다.

## 구문

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

## 설명
**Stop-AzureSqlDatabaseCopy** cmdlet은 연속 복사 관계를 종료합니다.
이 cmdlet은 원본 데이터베이스와 보조 또는 대상 데이터베이스 간의 데이터 이동을 중지한 다음 보조 데이터베이스의 상태를 독립 실행형 온라인 데이터베이스로 변경합니다.

데이터 손실이 가능한 경우 연속 복사 관계, 종료 또는 계획된 종료 및 강제 종료를 종료하는 두 가지 방법이 있습니다.
원본 데이터베이스를 호스트하는 서버에서 종료 또는 강제 종료 모드에서 이 cmdlet을 실행할 수 있습니다.
보조 데이터베이스를 호스트하는 서버에서 강제 종료 모드를 사용해야 합니다.

계획된 종료는 cmdlet을 실행할 때 원본 데이터베이스의 모든 커밋된 트랜잭션이 보조 데이터베이스에 복제될 때까지 대기합니다.
강제 종료는 미해결 커밋된 트랜잭션의 복제를 기다릴 수 없습니다. 보조 데이터베이스에서 가능한 데이터 손실이 발생할 수 있습니다.

복제 상태가 보류 중인 동안 강제 종료만 연속 복사 관계를 성공적으로 종료할 수 있습니다.
복제 상태가 보류 중이면 강제로 종료되지 않는 종료는 지원되지 않습니다.

## 예제

### 예제 1: 연속 복사 관계 종료
```
PS C:\>Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders" -PartnerServer "bk0b8kf658"
```

이 명령은 lpqd0zbr8y라는 서버에서 Orders라는 데이터베이스의 연속 복사 관계를 종료합니다.
bk0b8kf658이라는 서버는 보조 데이터베이스를 호스트합니다.

### 예제 2: 연속 복사 관계의 종료
```
PS C:\>$DatabaseCopy = Get-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -DatabaseName "Orders"
PS C:\> $DatabaseCopy | Stop-AzureSqlDatabaseCopy -ServerName "lpqd0zbr8y" -ForcedTermination
```

첫 번째 명령은 lpqd0zbr8y라는 서버에서 Orders라는 데이터베이스에 대한 데이터베이스 복사 관계를 얻습니다.

두 번째 명령은 보조 데이터베이스를 호스트하는 서버에서 연속 복사 관계를 억지로 종료합니다.

## PARAMETERS

### -Database
원본 Azure SQL 데이터베이스를 나타내는 개체를 지정합니다.
이 cmdlet은 이 매개 변수가 지정하는 데이터베이스의 연속 복사 관계를 종료합니다.

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
이 cmdlet은 이 매개 변수가 지정하는 데이터베이스의 연속 복사 관계를 종료합니다.
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
데이터베이스의 이름을 지정합니다.
이 cmdlet은 이 매개 변수가 지정하는 데이터베이스의 연속 복사 관계를 종료합니다.

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
사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.

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
이 cmdlet이 강제로 연속 복사 관계가 종료되는 경우를 나타냅니다.
강제 종료로 인해 데이터 손실이 발생할 수 있습니다.
대상 데이터베이스를 호스트하는 서버에서 이 cmdlet을 실행하려면 이 매개 변수를 지정해야 합니다.
원본 데이터베이스를 호스트하는 서버에서 이 cmdlet을 실행하려면 보조 데이터베이스를 사용할 수 없는 경우 이 매개 변수를 지정해야 합니다.

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

### -PartnerDatabase
보조 데이터베이스의 이름을 지정합니다.
이름을 지정하는 경우 원본 데이터베이스의 이름과 일치해야 합니다.

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

### -PartnerServer
대상 데이터베이스를 호스트하는 서버의 이름을 지정합니다.

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
원본 데이터베이스가 있는 서버의 이름을 지정합니다.

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

### -Confirm
cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.

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
cmdlet이 실행되는 경우의 결과 표시
cmdlet이 실행되지 않습니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

### Microsoft.WindowsAzure.Commands.SqlDatabase.Model.DatabaseCopy

### Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.Database

## 출력

### 없음

## 참고 사항
* 인증: 이 cmdlet에는 인증서 기반 인증이 필요합니다. 인증서 기반 인증을 사용하여 현재 구독을 설정하는 방법의 예제는 **New-AzureSqlDatabaseServerContext** cmdlet을 참조하세요.
* 제한 사항: 보조 데이터베이스를 호스트하는 서버에서 강제 종료만 지원됩니다.
* 이전 보조 데이터베이스에 대한 종료의 영향: 종료 후 보조 데이터베이스는 독립 데이터베이스가 됩니다. 보조 데이터베이스에서 이미 시드가 완료된 경우 종료 후 이 데이터베이스가 전체 액세스에 대해 열려 있습니다. 원본 데이터베이스가 읽기-쓰기 데이터베이스인 경우 이전 보조 데이터베이스도 읽기-쓰기 데이터베이스가 됩니다.

  시드가 현재 진행 중인 경우 시드가 중단되고 이전 보조 데이터베이스는 보조 데이터베이스를 호스트하는 서버에서 표시되지 않습니다.

* 원본 데이터베이스를 읽기 전용 모드로 설정할 수 있습니다. 이렇게 하면 종료 후 원본 및 보조 데이터베이스가 동기화될 수 있으며 종료하는 동안 트랜잭션이 커밋되지 않습니다. 종료가 완료되면 원본을 다시 읽기-쓰기 모드로 설정합니다. 선택적으로 이전 보조 데이터베이스를 읽기-쓰기 모드로 설정할 수도 있습니다.
* 모니터링: 연속 복사 관계의 원본 및 대상 모두에서 작업의 상태를 확인하기 위해 **Get-AzureSqlDatabaseOperation** cmdlet을 사용하세요.

## 관련 링크

[Azure SQL Database](https://azure.microsoft.com/en-us/services/sql-database/)

[Azure SQL 데이터베이스에 대한 작업](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[데이터베이스 복사 중지](https://msdn.microsoft.com/en-us/library/dn509573.aspx)



[Get-AzureSqlDatabaseCopy](./Get-AzureSqlDatabaseCopy.md)

[Start-AzureSqlDatabaseCopy](./Start-AzureSqlDatabaseCopy.md)


