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
# <span data-ttu-id="9ac7b-101">New-AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="9ac7b-101">New-AzureSqlDatabaseServerContext</span></span>

## <span data-ttu-id="9ac7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ac7b-102">SYNOPSIS</span></span>
<span data-ttu-id="9ac7b-103">서버 연결 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9ac7b-103">Creates a server connection context.</span></span>

## <span data-ttu-id="9ac7b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9ac7b-104">SYNTAX</span></span>

### <span data-ttu-id="9ac7b-105">ByServerNameWithSqlAuth (기본값)</span><span class="sxs-lookup"><span data-stu-id="9ac7b-105">ByServerNameWithSqlAuth (Default)</span></span>
```
New-AzureSqlDatabaseServerContext -ServerName <String> -Credential <PSCredential> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="9ac7b-106">ByManageUrlWithSqlAuth</span><span class="sxs-lookup"><span data-stu-id="9ac7b-106">ByManageUrlWithSqlAuth</span></span>
```
New-AzureSqlDatabaseServerContext [-ServerName <String>] -ManageUrl <Uri> -Credential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9ac7b-107">ByServerNameWithCertAuth</span><span class="sxs-lookup"><span data-stu-id="9ac7b-107">ByServerNameWithCertAuth</span></span>
```
New-AzureSqlDatabaseServerContext -ServerName <String> [-UseSubscription] [-SubscriptionName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9ac7b-108">ByFullyQualifiedServerNameWithSqlAuth</span><span class="sxs-lookup"><span data-stu-id="9ac7b-108">ByFullyQualifiedServerNameWithSqlAuth</span></span>
```
New-AzureSqlDatabaseServerContext -FullyQualifiedServerName <String> -Credential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9ac7b-109">ByFullyQualifiedServerNameWithCertAuth</span><span class="sxs-lookup"><span data-stu-id="9ac7b-109">ByFullyQualifiedServerNameWithCertAuth</span></span>
```
New-AzureSqlDatabaseServerContext -FullyQualifiedServerName <String> [-UseSubscription]
 [-SubscriptionName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9ac7b-110">설명은</span><span class="sxs-lookup"><span data-stu-id="9ac7b-110">DESCRIPTION</span></span>
<span data-ttu-id="9ac7b-111">**AzureSqlDatabaseServerContext** Cmdlet은 Azure SQL 데이터베이스 서버 연결 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9ac7b-111">The **New-AzureSqlDatabaseServerContext** cmdlet creates an Azure SQL Database server connection context.</span></span>
<span data-ttu-id="9ac7b-112">SQL Server 인증을 사용 하 여 지정 된 자격 증명을 사용 하 여 SQL 데이터베이스 서버에 대 한 연결 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9ac7b-112">Use SQL Server authentication to create a connection context to a SQL Database server by using the specified credentials.</span></span>
<span data-ttu-id="9ac7b-113">SQL 데이터베이스 서버를 이름, 정규화 된 이름 또는 URL을 기준으로 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9ac7b-113">You can specify the SQL Database server by name, by the fully qualified name, or by URL.</span></span>
<span data-ttu-id="9ac7b-114">자격 증명을 얻으려면 사용자 이름 및 암호를 지정 하 라는 메시지가 표시 되는 Get-Credential cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac7b-114">To obtain a credential, use the Get-Credential cmdlet that prompts you to specify the user name and password.</span></span>

<span data-ttu-id="9ac7b-115">**새 AzureSqlDatabaseServerContext** cmdlet을 인증서 기반 인증을 사용 하 여 지정 된 Azure 구독 데이터를 사용 하 여 지정 된 SQL 데이터베이스 서버에 대 한 연결 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9ac7b-115">Use the **New-AzureSqlDatabaseServerContext** cmdlet with certificate based authentication to create a connection context to the specified SQL Database server by using the specified Azure subscription data.</span></span>
<span data-ttu-id="9ac7b-116">SQL 데이터베이스 서버를 이름 또는 정규화 된 이름으로 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9ac7b-116">You can specify SQL Database server by name or by the fully qualified name.</span></span>
<span data-ttu-id="9ac7b-117">구독 데이터를 매개 변수로 지정 하거나 현재 Azure 구독에서 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9ac7b-117">You can specify the subscription data as a parameter or it can be retrieved from the current Azure subscription.</span></span>
<span data-ttu-id="9ac7b-118">선택-AzureSubscription https://msdn.microsoft.com/library/windowsazure/jj152833.aspx cmdlet을 사용 하 여 현재 Azure 구독을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac7b-118">Use the Select-AzureSubscriptionhttps://msdn.microsoft.com/library/windowsazure/jj152833.aspx cmdlet to select the current Azure subscription.</span></span>

## <span data-ttu-id="9ac7b-119">예제의</span><span class="sxs-lookup"><span data-stu-id="9ac7b-119">EXAMPLES</span></span>

### <span data-ttu-id="9ac7b-120">예제 1: SQL Server 인증을 사용 하 여 컨텍스트 만들기</span><span class="sxs-lookup"><span data-stu-id="9ac7b-120">Example 1: Create a context by using SQL Server authentication</span></span>
```
PS C:\> $Credential = Get-Credential
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -Credential $Credential
PS C:\> $Database17 = New-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database17" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

<span data-ttu-id="9ac7b-121">이 예제에서는 SQL Server 인증을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac7b-121">This example uses the SQL Server authentication.</span></span>

<span data-ttu-id="9ac7b-122">첫 번째 명령은 서버 관리자 자격 증명을 묻는 메시지를 표시 하 고 자격 증명을 $Credential 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac7b-122">The first command prompts you for server administrator credentials, and stores the credentials in the $Credential variable.</span></span>

<span data-ttu-id="9ac7b-123">두 번째 명령은 $Credential를 사용 하 여 lpqd0zbr8y 라는 SQL 데이터베이스 서버에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac7b-123">The second command connects to the SQL Database server named lpqd0zbr8y by using $Credential.</span></span>

<span data-ttu-id="9ac7b-124">마지막 명령은 $Context 컨텍스트의 일부인 서버에서 Database17 라는 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9ac7b-124">The final command creates a database named Database17 on the server that is part of the context in $Context.</span></span>

### <span data-ttu-id="9ac7b-125">예제 2: 인증서 기반 인증을 사용 하 여 컨텍스트 만들기</span><span class="sxs-lookup"><span data-stu-id="9ac7b-125">Example 2: Create a context by using certificate based authentication</span></span>
```
PS C:\> $SubscriptionId = <Subscription ID>
PS C:\> $Thumbprint = <Certificate Thumbprint>
PS C:\> $Certificate = Get-Item "Cert:\CurrentUser\My\$Thumbprint"
PS C:\> Set-AzureSubscription -SubscriptionName "Subscription07" -SubscriptionId $SubscriptionId -Certificate $Certificate
PS C:\> Select-AzureSubscription -SubscriptionName "Subscription07"
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -UseSubscription
```

<span data-ttu-id="9ac7b-126">이 예제에서는 인증서 기반 인증을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac7b-126">This example uses the certificate based authentication.</span></span>

<span data-ttu-id="9ac7b-127">처음 두 명령은 $SubscriptionId 및 $Thumbprint 변수에 값을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac7b-127">The first two commands assign values to the $SubscriptionId and $Thumbprint variables.</span></span>

<span data-ttu-id="9ac7b-128">세 번째 명령은 $Thumbprint의 손도장으로 식별 되는 인증서를 가져와 $Certificate에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac7b-128">The third command gets the certificate identified by the thumbprint in $Thumbprint, and stores it in $Certificate.</span></span>

<span data-ttu-id="9ac7b-129">네 번째 명령은 구독을 Subscription07으로 설정 하 고 다섯 번째 명령은 해당 구독을 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac7b-129">The fourth command sets the subscription to be Subscription07, and the fifth command selects that subscription.</span></span>

<span data-ttu-id="9ac7b-130">마지막 명령은 lpqd0zbr8y 이라는 서버의 현재 구독에 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9ac7b-130">The final command creates a context in the current subscription for the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="9ac7b-131">변수</span><span class="sxs-lookup"><span data-stu-id="9ac7b-131">PARAMETERS</span></span>

### <span data-ttu-id="9ac7b-132">-Credential</span><span class="sxs-lookup"><span data-stu-id="9ac7b-132">-Credential</span></span>
<span data-ttu-id="9ac7b-133">서버에 액세스 하는 데 사용할 수 있는 SQL Server 인증을 제공 하는 credential 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac7b-133">Specifies a credential object that provides SQL Server authentication for you to access the server.</span></span>

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

### <span data-ttu-id="9ac7b-134">-FullyQualifiedServerName</span><span class="sxs-lookup"><span data-stu-id="9ac7b-134">-FullyQualifiedServerName</span></span>
<span data-ttu-id="9ac7b-135">Azure SQL Database server의 FQDN (정규화 된 도메인 이름) 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac7b-135">Specifies the fully qualified domain name (FQDN) name for the Azure SQL Database server.</span></span>
<span data-ttu-id="9ac7b-136">예를 Server02.database.windows.net.</span><span class="sxs-lookup"><span data-stu-id="9ac7b-136">For example, Server02.database.windows.net.</span></span>

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

### <span data-ttu-id="9ac7b-137">-ManageUrl</span><span class="sxs-lookup"><span data-stu-id="9ac7b-137">-ManageUrl</span></span>
<span data-ttu-id="9ac7b-138">이 cmdlet이 서버의 Azure SQL DatabaseManagement 포털에 액세스 하는 데 사용 하는 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac7b-138">Specifies the URL that this cmdlet uses to access the Azure SQL DatabaseManagement Portal for the server.</span></span>

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

### <span data-ttu-id="9ac7b-139">-프로필</span><span class="sxs-lookup"><span data-stu-id="9ac7b-139">-Profile</span></span>
<span data-ttu-id="9ac7b-140">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac7b-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9ac7b-141">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="9ac7b-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9ac7b-142">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9ac7b-142">-ServerName</span></span>
<span data-ttu-id="9ac7b-143">데이터베이스 서버의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac7b-143">Specifies the name of the database server.</span></span>

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

### <span data-ttu-id="9ac7b-144">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="9ac7b-144">-SubscriptionName</span></span>
<span data-ttu-id="9ac7b-145">이 cmdlet이 연결 컨텍스트를 만드는 데 사용 하는 Azure 구독의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac7b-145">Specifies the name of the Azure subscription that this cmdlet uses to create the connection context.</span></span>
<span data-ttu-id="9ac7b-146">이 매개 변수에 대 한 값을 지정 하지 않으면 cmdlet은 현재 구독을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac7b-146">If you do not specify a value for this parameter, the cmdlet uses the current subscription.</span></span>
<span data-ttu-id="9ac7b-147">Select-AzureSubscription cmdlet을 실행 하 여 현재 구독을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac7b-147">Run the Select-AzureSubscription cmdlet to change the current subscription.</span></span>

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

### <span data-ttu-id="9ac7b-148">-UseSubscription</span><span class="sxs-lookup"><span data-stu-id="9ac7b-148">-UseSubscription</span></span>
<span data-ttu-id="9ac7b-149">이 cmdlet이 연결 컨텍스트를 만들기 위해 Azure 구독을 사용 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9ac7b-149">Indicates that this cmdlet uses Azure subscription for creating the connection context.</span></span>

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

### <span data-ttu-id="9ac7b-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ac7b-150">CommonParameters</span></span>
<span data-ttu-id="9ac7b-151">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac7b-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ac7b-152">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ac7b-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ac7b-153">입력</span><span class="sxs-lookup"><span data-stu-id="9ac7b-153">INPUTS</span></span>

## <span data-ttu-id="9ac7b-154">출력</span><span class="sxs-lookup"><span data-stu-id="9ac7b-154">OUTPUTS</span></span>

### <span data-ttu-id="9ac7b-155">WindowsAzure. SqlDatabase. \* IServerDataServiceContext</span><span class="sxs-lookup"><span data-stu-id="9ac7b-155">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.IServerDataServiceContext</span></span>

## <span data-ttu-id="9ac7b-156">상속자</span><span class="sxs-lookup"><span data-stu-id="9ac7b-156">NOTES</span></span>
* <span data-ttu-id="9ac7b-157">도메인을 지정 하지 않고 인증 하는 경우 Windows PowerShell 2.0를 사용 하는 경우 Get-Credential cmdlet은 \\ 사용자 이름 앞에 (예: \user.)가 있는 백슬래시 ()를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac7b-157">If you authenticate without specifying a domain, and if you use Windows PowerShell 2.0, the Get-Credential cmdlet returns a backslash (\\) prepended to the username, for example, \user.</span></span> <span data-ttu-id="9ac7b-158">Windows PowerShell 3.0에는 백슬래시가 추가 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9ac7b-158">Windows PowerShell 3.0 does not add the backslash.</span></span> <span data-ttu-id="9ac7b-159">이 백슬래시는 **New-AzureSqlDatabaseServerContext** Cmdlet의 *Credential* 매개 변수에 의해 인식 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9ac7b-159">This backslash is not recognized by the *Credential* parameter of the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span> <span data-ttu-id="9ac7b-160">제거 하려면 다음과 같은 명령을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac7b-160">To remove it, use commands similar to the following:</span></span>

  `PS C:\\\> $Credential = Get-Credential`
`PS C:\\\> $Credential = New-Object -TypeName 'System.Management.Automation.PSCredential' -ArgumentList $Credential.Username.Replace("\",""),$Credential.Password`

## <span data-ttu-id="9ac7b-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9ac7b-161">RELATED LINKS</span></span>

[<span data-ttu-id="9ac7b-162">Azure SQL 데이터베이스 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9ac7b-162">Azure SQL Database Cmdlets</span></span>](./Azure.SQLDatabase.md)

[<span data-ttu-id="9ac7b-163">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="9ac7b-163">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="9ac7b-164">새로운 AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="9ac7b-164">New-AzureSqlDatabase</span></span>](./New-AzureSqlDatabase.md)

[<span data-ttu-id="9ac7b-165">제거-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="9ac7b-165">Remove-AzureSqlDatabase</span></span>](./Remove-AzureSqlDatabase.md)

[<span data-ttu-id="9ac7b-166">Set-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="9ac7b-166">Set-AzureSqlDatabase</span></span>](./Set-AzureSqlDatabase.md)


