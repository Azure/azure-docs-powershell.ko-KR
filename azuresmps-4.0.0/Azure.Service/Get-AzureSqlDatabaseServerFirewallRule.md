---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: BE00A25D-3ECE-4B27-9D79-78128CFEBDB0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 100202df1871610aff3af1fe90bb7d603c141d62
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045572"
---
# Get-AzureSqlDatabaseServerFirewallRule

## SYNOPSIS
Azure SQL 데이터베이스 서버에 대 한 방화벽 규칙을 가져옵니다.

## 구문과

```
Get-AzureSqlDatabaseServerFirewallRule -ServerName <String> [-RuleName <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## 설명은
**AzureSqlDatabaseServerFirewallRule** Cmdlet은 Azure SQL 데이터베이스 서버의 인스턴스에 대 한 방화벽 규칙을 가져옵니다.
이름을 기준으로 방화벽 규칙을 지정 하는 경우이 cmdlet은 해당 방화벽 규칙에 대 한 정보를 반환 합니다.
그렇지 않으면 cmdlet이 지정 된 Azure SQL 데이터베이스 서버의 모든 방화벽 규칙에 대 한 정보를 반환 합니다.

## 예제의

### 예제 1: 서버에서 모든 방화벽 규칙 가져오기
```
PS C:\> Get-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y"
```

이 명령은 lpqd0zbr8y 이라는 Azure SQL 데이터베이스 서버의 모든 방화벽 규칙을 가져옵니다.

### 예제 2: 이름을 사용 하 여 방화벽 규칙 가져오기
```
PS C:\> Get-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -RuleName "FirewallRule24"
```

이 명령은 lpqd0zbr8y 이라는 서버에서 FirewallRule24 이라는 방화벽 규칙을 가져옵니다.

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

### -RuleName
이 cmdlet이 가져오는 방화벽 규칙의 이름을 지정 합니다.

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
이 cmdlet은이 매개 변수에서 지정 하는 서버에서 방화벽 규칙을 가져옵니다.
정규화 된 DNS 이름이 아니라 서버 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: (All)
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

### WindowsAzure. SqlDatabase. SqlDatabaseServerFirewallRuleContext

## 출력

### IEnumerable\<Microsoft.WindowsAzure.Commands.SqlDatabase.Model.SqlDatabaseServerFirewallRuleContext\>

## 상속자

## 관련 링크

[Azure SQL 데이터베이스](https://azure.microsoft.com/en-us/services/sql-database/)

[방화벽 규칙 목록 표시](https://msdn.microsoft.com/en-us/library/azure/dn505715.aspx)

[Azure SQL 데이터베이스에 대 한 작업](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[새로운 AzureSqlDatabaseServerFirewallRule](./New-AzureSqlDatabaseServerFirewallRule.md)

[제거-AzureSqlDatabaseServerFirewallRule](./Remove-AzureSqlDatabaseServerFirewallRule.md)

[Set-AzureSqlDatabaseServerFirewallRule](./Set-AzureSqlDatabaseServerFirewallRule.md)


