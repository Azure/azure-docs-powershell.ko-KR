---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7B29875-D2E5-4E96-AD4B-83032AB18D02
online version: ''
schema: 2.0.0
ms.openlocfilehash: cdcd4788e3eefdce858cb88c0bf1885353f8a673
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045970"
---
# New-AzureSqlDatabaseServerContext

## SYNOPSIS
서버 연결 컨텍스트를 만듭니다.

## 구문과

### ByServerNameWithSqlAuth (기본값)
```
New-AzureSqlDatabaseServerContext -ServerName <String> -Credential <PSCredential> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### ByManageUrlWithSqlAuth
```
New-AzureSqlDatabaseServerContext [-ServerName <String>] -ManageUrl <Uri> -Credential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByServerNameWithCertAuth
```
New-AzureSqlDatabaseServerContext -ServerName <String> [-UseSubscription] [-SubscriptionName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByFullyQualifiedServerNameWithSqlAuth
```
New-AzureSqlDatabaseServerContext -FullyQualifiedServerName <String> -Credential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ByFullyQualifiedServerNameWithCertAuth
```
New-AzureSqlDatabaseServerContext -FullyQualifiedServerName <String> [-UseSubscription]
 [-SubscriptionName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## 설명은
**AzureSqlDatabaseServerContext** Cmdlet은 Azure SQL 데이터베이스 서버 연결 컨텍스트를 만듭니다.
SQL Server 인증을 사용 하 여 지정 된 자격 증명을 사용 하 여 SQL 데이터베이스 서버에 대 한 연결 컨텍스트를 만듭니다.
SQL 데이터베이스 서버를 이름, 정규화 된 이름 또는 URL을 기준으로 지정할 수 있습니다.
자격 증명을 얻으려면 사용자 이름 및 암호를 지정 하 라는 메시지가 표시 되는 Get-Credential cmdlet을 사용 합니다.

**새 AzureSqlDatabaseServerContext** cmdlet을 인증서 기반 인증을 사용 하 여 지정 된 Azure 구독 데이터를 사용 하 여 지정 된 SQL 데이터베이스 서버에 대 한 연결 컨텍스트를 만듭니다.
SQL 데이터베이스 서버를 이름 또는 정규화 된 이름으로 지정할 수 있습니다.
구독 데이터를 매개 변수로 지정 하거나 현재 Azure 구독에서 검색할 수 있습니다.
선택-AzureSubscription https://msdn.microsoft.com/library/windowsazure/jj152833.aspx cmdlet을 사용 하 여 현재 Azure 구독을 선택 합니다.

## 예제의

### 예제 1: SQL Server 인증을 사용 하 여 컨텍스트 만들기
```
PS C:\> $Credential = Get-Credential
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -Credential $Credential
PS C:\> $Database17 = New-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database17" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

이 예제에서는 SQL Server 인증을 사용 합니다.

첫 번째 명령은 서버 관리자 자격 증명을 묻는 메시지를 표시 하 고 자격 증명을 $Credential 변수에 저장 합니다.

두 번째 명령은 $Credential를 사용 하 여 lpqd0zbr8y 라는 SQL 데이터베이스 서버에 연결 합니다.

마지막 명령은 $Context 컨텍스트의 일부인 서버에서 Database17 라는 데이터베이스를 만듭니다.

### 예제 2: 인증서 기반 인증을 사용 하 여 컨텍스트 만들기
```
PS C:\> $SubscriptionId = <Subscription ID>
PS C:\> $Thumbprint = <Certificate Thumbprint>
PS C:\> $Certificate = Get-Item "Cert:\CurrentUser\My\$Thumbprint"
PS C:\> Set-AzureSubscription -SubscriptionName "Subscription07" -SubscriptionId $SubscriptionId -Certificate $Certificate
PS C:\> Select-AzureSubscription -SubscriptionName "Subscription07"
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -UseSubscription
```

이 예제에서는 인증서 기반 인증을 사용 합니다.

처음 두 명령은 $SubscriptionId 및 $Thumbprint 변수에 값을 할당 합니다.

세 번째 명령은 $Thumbprint의 손도장으로 식별 되는 인증서를 가져와 $Certificate에 저장 합니다.

네 번째 명령은 구독을 Subscription07으로 설정 하 고 다섯 번째 명령은 해당 구독을 선택 합니다.

마지막 명령은 lpqd0zbr8y 이라는 서버의 현재 구독에 컨텍스트를 만듭니다.

## 변수

### -Credential
서버에 액세스 하는 데 사용할 수 있는 SQL Server 인증을 제공 하는 credential 개체를 지정 합니다.

```yaml
Type: PSCredential
Parameter Sets: ByServerNameWithSqlAuth, ByManageUrlWithSqlAuth, ByFullyQualifiedServerNameWithSqlAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FullyQualifiedServerName
Azure SQL Database server의 FQDN (정규화 된 도메인 이름) 이름을 지정 합니다.
예를 Server02.database.windows.net.

```yaml
Type: String
Parameter Sets: ByFullyQualifiedServerNameWithSqlAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ManageUrl
이 cmdlet이 서버의 Azure SQL DatabaseManagement 포털에 액세스 하는 데 사용 하는 URL을 지정 합니다.

```yaml
Type: Uri
Parameter Sets: ByManageUrlWithSqlAuth
Aliases: 

Required: True
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
데이터베이스 서버의 이름을 지정 합니다.

```yaml
Type: String
Parameter Sets: ByServerNameWithSqlAuth, ByServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByManageUrlWithSqlAuth
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SubscriptionName
이 cmdlet이 연결 컨텍스트를 만드는 데 사용 하는 Azure 구독의 이름을 지정 합니다.
이 매개 변수에 대 한 값을 지정 하지 않으면 cmdlet은 현재 구독을 사용 합니다.
Select-AzureSubscription cmdlet을 실행 하 여 현재 구독을 변경 합니다.

```yaml
Type: String
Parameter Sets: ByServerNameWithCertAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -UseSubscription
이 cmdlet이 연결 컨텍스트를 만들기 위해 Azure 구독을 사용 함을 나타냅니다.

```yaml
Type: SwitchParameter
Parameter Sets: ByServerNameWithCertAuth, ByFullyQualifiedServerNameWithCertAuth
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다. 자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .

## 입력

## 출력

### WindowsAzure. SqlDatabase. * IServerDataServiceContext

## 상속자
* 도메인을 지정 하지 않고 인증 하는 경우 Windows PowerShell 2.0를 사용 하는 경우 Get-Credential cmdlet은 \\ 사용자 이름 앞에 (예: \user.)가 있는 백슬래시 ()를 반환 합니다. Windows PowerShell 3.0에는 백슬래시가 추가 되지 않습니다. 이 백슬래시는 **New-AzureSqlDatabaseServerContext** Cmdlet의 *Credential* 매개 변수에 의해 인식 되지 않습니다. 제거 하려면 다음과 같은 명령을 사용 합니다.

  `PS C:\\\> $Credential = Get-Credential`
`PS C:\\\> $Credential = New-Object -TypeName 'System.Management.Automation.PSCredential' -ArgumentList $Credential.Username.Replace("\",""),$Credential.Password`

## 관련 링크

[Azure SQL 데이터베이스 Cmdlet](./Azure.SQLDatabase.md)

[Get-AzureSqlDatabase](./Get-AzureSqlDatabase.md)

[새로운 AzureSqlDatabase](./New-AzureSqlDatabase.md)

[제거-AzureSqlDatabase](./Remove-AzureSqlDatabase.md)

[Set-AzureSqlDatabase](./Set-AzureSqlDatabase.md)


