---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: A723D12D-DCF5-4F0C-AAC2-8BADFBAC3328
online version: ''
schema: 2.0.0
ms.openlocfilehash: a0383e451d8346d4b6465390cc78850b270f6ac3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045969"
---
# New-AzureSqlDatabaseServerFirewallRule

## SYNOPSIS
Azure SQL 데이터베이스 서버에서 방화벽 규칙을 만듭니다.

## 구문과

### IpRange (기본값)
```
New-AzureSqlDatabaseServerFirewallRule -ServerName <String> -RuleName <String> -StartIpAddress <String>
 -EndIpAddress <String> [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AllowAllAzureServices
```
New-AzureSqlDatabaseServerFirewallRule -ServerName <String> [-RuleName <String>] [-AllowAllAzureServices]
 [-Force] [-Profile <AzureSMProfile>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## 설명은
**AzureSqlDatabaseServerFirewallRule** cmdlet은 현재 구독에 있는 지정 된 Azure SQL 데이터베이스 서버 인스턴스에서 방화벽 규칙을 만듭니다.

*StartIpAddress* 및 *EndIpAddress* 매개 변수를 사용 하 여이 규칙이 Azure SQL 데이터베이스 서버에 연결할 수 있도록 허용 하는 IP 주소 범위를 지정 합니다.

*AllowAllAzureServices* 매개 변수를 지정 하 여 서버에 대 한 Azure 연결을 허용 하는 규칙을 만듭니다.
규칙에 0.0.0.0의 시작 및 종료 IP 주소 값이 있습니다.
방화벽 규칙 이름을 지정 하지 않으면이 cmdlet은 기본 이름 AllowAllAzureServices를 할당 합니다.

## 예제의

### 예제 1: 방화벽 규칙 만들기
```
PS C:\>New-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -RuleName "FirewallRule24" -StartIpAddress 10.1.1.1 -EndIpAddress 10.1.1.2
```

이 명령은 lpqd0zbr8y 이라는 Azure SQL 데이터베이스 서버에서 방화벽 규칙 FirewallRule24를 만듭니다.
명령이 IP 주소 범위를 지정 합니다.

### 예제 2: 모든 Azure 서비스를 허용 하는 규칙 만들기
```
PS C:\>New-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -AllowAllAzureServices -RuleName "AzureConnections"
```

이 명령은 Azure 연결을 허용 하는 lpqd0zbr8y 이라는 서버에서 AzureConnections 라는 방화벽 규칙을 만듭니다.

### 예제 3: 기본 이름을 사용 하는 모든 Azure 서비스에 사용할 수 있는 규칙 만들기 기본 이름을 사용 하는 모든 Azure 서비스를 허용 하는 규칙 만들기
```
PS C:\>New-AzureSqlDatabaseServerFirewallRule -ServerName "lpqd0zbr8y" -AllowAllAzureServices
```

이 명령은 Azure 연결을 허용 하는 lpqd0zbr8y 이라는 지정 된 서버에 대 한 방화벽 규칙을 만듭니다.
명령이 기본 규칙 이름 AllowAllAzureServices를 할당 합니다.

## 변수

### -AllowAllAzureServices
이 방화벽 규칙이 모든 Azure IP 주소에서 서버에 액세스할 수 있도록 설정 함을 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: AllowAllAzureServices
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EndIpAddress
이 규칙에 대 한 IP 주소 범위의 끝 값을 지정 합니다.

```yaml
Type: String
Parameter Sets: IpRange
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
새 방화벽 규칙의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: IpRange
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: AllowAllAzureServices
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerName
서버의 이름을 지정 합니다.
이 cmdlet은이 cmdlet이 지정 하는 서버에서 방화벽 규칙을 만듭니다.
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

### -StartIpAddress
방화벽 규칙에 대 한 IP 주소 범위의 시작 값을 지정 합니다.

```yaml
Type: String
Parameter Sets: IpRange
Aliases: 

Required: True
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

### WindowsAzure. SqlDatabase. SqlDatabaseServerFirewallRuleContext

## 상속자

## 관련 링크

[Azure SQL 데이터베이스](https://azure.microsoft.com/en-us/services/sql-database/)

[방화벽 규칙 만들기](https://msdn.microsoft.com/en-us/library/azure/dn505712.aspx)

[Azure SQL 데이터베이스에 대 한 작업](https://msdn.microsoft.com/en-us/library/azure/dn505719.aspx)

[Get-AzureSqlDatabaseServerFirewallRule](./Get-AzureSqlDatabaseServerFirewallRule.md)

[제거-AzureSqlDatabaseServerFirewallRule](./Remove-AzureSqlDatabaseServerFirewallRule.md)

[Set-AzureSqlDatabaseServerFirewallRule](./Set-AzureSqlDatabaseServerFirewallRule.md)


