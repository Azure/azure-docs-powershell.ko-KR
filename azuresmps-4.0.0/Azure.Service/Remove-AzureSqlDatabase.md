---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B3813F54-E5B7-4605-BB1C-67417FDDB076
online version: ''
schema: 2.0.0
ms.openlocfilehash: a3f9817ebe556bc80364d012040387cca72c56c4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046108"
---
# Remove-AzureSqlDatabase

## SYNOPSIS
Azure SQL 데이터베이스를 삭제 합니다.

## 구문과

### ByNameWithConnectionContext
```
Remove-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -DatabaseName <String> [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByObjectWithConnectionContext
```
Remove-AzureSqlDatabase -ConnectionContext <IServerDataServiceContext> -Database <Database> [-Force]
 [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByNameWithServerName
```
Remove-AzureSqlDatabase -ServerName <String> -DatabaseName <String> [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ByObjectWithServerName
```
Remove-AzureSqlDatabase -ServerName <String> -Database <Database> [-Force] [-Profile <AzureSMProfile>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**AzureSqlDatabase** cmdlet은 서버 연결 컨텍스트 또는 서버 이름으로 Azure SQL 데이터베이스를 삭제 합니다.
**새 AzureSqlDatabaseServerContext** cmdlet을 사용 하 여 Azure SQL 데이터베이스 서버 연결 컨텍스트를 만든 다음이 cmdlet에서 사용할 수 있습니다.

Azure SQL 데이터베이스 서버 이름을 지정 하 여 데이터베이스를 삭제 하는 경우 **AzureSqlDatabase** cmdlet은 이름과 현재 Azure 구독 정보를 사용 하 여 작업을 수행 합니다.

## 예제의

### 예제 1: 데이터베이스 제거
```
PS C:\> Remove-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database01"
```

이 명령은 Azure SQL 데이터베이스 서버 연결 컨텍스트 $Context에서 Database01 이라는 데이터베이스를 제거 합니다.

### 예제 2: 서버 이름을 사용 하 여 데이터베이스 제거
```
PS C:\> Remove-AzureSqlDatabase -ServerName "lpqd0zbr8y" -DatabaseName "Database01"
```

이 명령은 lpqd0zbr8y 이라는 Azure SQL 데이터베이스 서버에서 Database01 이라는 데이터베이스를 제거 합니다.

### 예제 3: 파이프라인을 사용 하 여 데이터베이스 제거
```
PS C:\> $Database01 | Remove-AzureSqlDatabase -ConnectionContext $Context
PS C:\> $Database01 | Remove-AzureSqlDatabase -ServerName "lpqd0zbr8y"
```

이 예제에서는 파이프라인을 통해 데이터베이스 개체를 전달 하는 다른 방법을 보여 줍니다.

## 변수

### -ConnectionContext
이 cmdlet이 데이터베이스를 제거할 서버의 연결 컨텍스트를 지정 합니다.

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
이 cmdlet이 제거 하는 데이터베이스를 나타내는 개체를 지정 합니다.

```yaml
Type: Database
Parameter Sets: ByObjectWithConnectionContext, ByObjectWithServerName
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DatabaseName
이 cmdlet이 제거 하는 데이터베이스의 이름을 지정 합니다.

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
이 cmdlet이 데이터베이스를 삭제 하는 서버의 이름을 지정 합니다.

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

## 상속자
* 작업의 심각성 때문에이 cmdlet은 기본적으로 확인을 요청 하는 메시지를 표시 합니다. 확인을 건너뛰려면 *Force* 매개 변수를 지정 합니다.

## 관련 링크

[Azure SQL 데이터베이스](https://azure.microsoft.com/en-us/services/sql-database/)

[데이터베이스 삭제](https://msdn.microsoft.com/en-us/library/azure/dn505705.aspx)

[Azure SQL 데이터베이스에 대 한 작업](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-AzureSqlDatabase](./Get-AzureSqlDatabase.md)

[새로운 AzureSqlDatabase](./New-AzureSqlDatabase.md)

[새로운 AzureSqlDatabaseServerContext](./New-AzureSqlDatabaseServerContext.md)

[Set-AzureSqlDatabase](./Set-AzureSqlDatabase.md)


