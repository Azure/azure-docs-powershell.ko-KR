---
external help file: Microsoft.WindowsAzure.Commands.SqlDatabase.dll-Help.xml
ms.assetid: B7B29875-D2E5-4E96-AD4B-83032AB18D02
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5312556cb49d02ea901b4cb2526a36f7237f66d1
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100404176"
---
# New-AzureSqlDatabaseServerContext

## SYNOPSIS
서버 연결 컨텍스트를 만듭니다.

## 구문

### ByServerNameWithSqlAuth(기본값)
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

## 설명
**New-AzureSqlDatabaseServerContext** cmdlet은 Azure SQL 데이터베이스 서버 연결 컨텍스트를 만듭니다.
SQL Server 인증을 사용하여 지정된 자격 증명을 사용하여 SQL Database 서버에 대한 연결 컨텍스트를 만듭니다.
이름, SQL URL로 SQL 데이터베이스 서버를 지정할 수 있습니다.
자격 증명을 얻게 Get-Credential 사용자 이름 및 암호를 지정하라는 메시지를 표시하는 Get-Credential cmdlet을 사용하세요.

인증서 기반 인증과 **함께 New-AzureSqlDatabaseServerContext** cmdlet을 사용하여 지정된 Azure 구독 데이터를 사용하여 SQL Database 서버에 대한 연결 컨텍스트를 만듭니다.
이름 또는 SQL 데이터베이스 서버를 지정할 수 있습니다.
구독 데이터를 매개 변수로 지정하거나 현재 Azure 구독에서 검색할 수 있습니다.
Select-AzureSubscription cmdlet을 사용하여 현재 https://msdn.microsoft.com/library/windowsazure/jj152833.aspx Azure 구독을 선택합니다.

## 예제

### 예제 1: 인증을 사용하여 컨텍스트 SQL Server
```
PS C:\> $Credential = Get-Credential
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -Credential $Credential
PS C:\> $Database17 = New-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database17" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

이 예제에서는 SQL Server 인증을 사용 합니다.

첫 번째 명령은 서버 관리자 자격 증명을 묻는 메시지를 표시하고 자격 증명을 $Credential 저장합니다.

두 번째 명령은 SQL 사용하여 lpqd0zbr8y라는 $Credential.

마지막 명령은 서버에서 컨텍스트의 일부인 Database17이라는 데이터베이스를 $Context.

### 예제 2: 인증서 기반 인증을 사용하여 컨텍스트 만들기
```
PS C:\> $SubscriptionId = <Subscription ID>
PS C:\> $Thumbprint = <Certificate Thumbprint>
PS C:\> $Certificate = Get-Item "Cert:\CurrentUser\My\$Thumbprint"
PS C:\> Set-AzureSubscription -SubscriptionName "Subscription07" -SubscriptionId $SubscriptionId -Certificate $Certificate
PS C:\> Select-AzureSubscription -SubscriptionName "Subscription07"
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -UseSubscription
```

이 예제에서는 인증서 기반 인증을 사용 합니다.

처음 두 명령은 변수 및 $SubscriptionId $Thumbprint 할당합니다.

세 번째 명령은 지문으로 식별된 인증서를 $Thumbprint 인증서를 $Certificate.

네 번째 명령은 구독을 Subscription07로 설정하고 다섯 번째 명령은 해당 구독을 선택합니다.

마지막 명령은 lpqd0zbr8y라는 서버에 대한 현재 구독에 컨텍스트를 만듭니다.

## PARAMETERS

### -Credential
서버에 액세스할 수 있도록 SQL Server 인증을 제공하는 자격 증명 개체를 지정합니다.

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
Azure SQL Database 서버에 대한 FQDN(정식 도메인 이름) 이름을 지정합니다.
예를 들어, Server02.database.windows.net.

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
이 cmdlet이 서버에 대한 Azure SQL DatabaseManagement 포털에 액세스하는 데 사용하는 URL을 지정합니다.

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
데이터베이스 서버의 이름을 지정합니다.

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
이 cmdlet이 연결 컨텍스트를 만드는 데 사용하는 Azure 구독의 이름을 지정합니다.
이 매개 변수에 대한 값을 지정하지 않으면 cmdlet은 현재 구독을 사용합니다.
Select-AzureSubscription cmdlet을 실행하여 현재 구독을 변경합니다.

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
이 cmdlet이 연결 컨텍스트를 만드는 데 Azure 구독을 사용 중입니다.

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
이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다. 자세한 내용은 다음 about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.

## 입력

## 출력

### Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.IServerDataServiceContext

## 참고 사항
* 도메인을 지정하지 않고 인증하고 Windows PowerShell 2.0을 사용하는 경우 Get-Credential cmdlet은 사용자 이름(예: \user)에 추가된 백슬래시()를 \\ 반환합니다. Windows PowerShell 3.0에서는 백 슬래시를 추가하지 않습니다. 이 백슬래시는 **New-AzureSqlDatabaseServerContext** cmdlet의 자격 증명 매개 변수에서 인식되지 않습니다.  제거하려면 다음과 유사한 명령을 사용 합니다.

  `PS C:\\\> $Credential = Get-Credential`
`PS C:\\\> $Credential = New-Object -TypeName 'System.Management.Automation.PSCredential' -ArgumentList $Credential.Username.Replace("\",""),$Credential.Password`

## 관련 링크



[Get-AzureSqlDatabase](./Get-AzureSqlDatabase.md)

[New-AzureSqlDatabase](./New-AzureSqlDatabase.md)

[Remove-AzureSqlDatabase](./Remove-AzureSqlDatabase.md)

[Set-AzureSqlDatabase](./Set-AzureSqlDatabase.md)


