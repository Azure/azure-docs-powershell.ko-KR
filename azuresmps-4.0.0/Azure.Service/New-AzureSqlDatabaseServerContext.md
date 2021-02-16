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
# <span data-ttu-id="64081-101">New-AzureSqlDatabaseServerContext</span><span class="sxs-lookup"><span data-stu-id="64081-101">New-AzureSqlDatabaseServerContext</span></span>

## <span data-ttu-id="64081-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64081-102">SYNOPSIS</span></span>
<span data-ttu-id="64081-103">서버 연결 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="64081-103">Creates a server connection context.</span></span>

## <span data-ttu-id="64081-104">구문</span><span class="sxs-lookup"><span data-stu-id="64081-104">SYNTAX</span></span>

### <span data-ttu-id="64081-105">ByServerNameWithSqlAuth(기본값)</span><span class="sxs-lookup"><span data-stu-id="64081-105">ByServerNameWithSqlAuth (Default)</span></span>
```
New-AzureSqlDatabaseServerContext -ServerName <String> -Credential <PSCredential> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="64081-106">ByManageUrlWithSqlAuth</span><span class="sxs-lookup"><span data-stu-id="64081-106">ByManageUrlWithSqlAuth</span></span>
```
New-AzureSqlDatabaseServerContext [-ServerName <String>] -ManageUrl <Uri> -Credential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="64081-107">ByServerNameWithCertAuth</span><span class="sxs-lookup"><span data-stu-id="64081-107">ByServerNameWithCertAuth</span></span>
```
New-AzureSqlDatabaseServerContext -ServerName <String> [-UseSubscription] [-SubscriptionName <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="64081-108">ByFullyQualifiedServerNameWithSqlAuth</span><span class="sxs-lookup"><span data-stu-id="64081-108">ByFullyQualifiedServerNameWithSqlAuth</span></span>
```
New-AzureSqlDatabaseServerContext -FullyQualifiedServerName <String> -Credential <PSCredential>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="64081-109">ByFullyQualifiedServerNameWithCertAuth</span><span class="sxs-lookup"><span data-stu-id="64081-109">ByFullyQualifiedServerNameWithCertAuth</span></span>
```
New-AzureSqlDatabaseServerContext -FullyQualifiedServerName <String> [-UseSubscription]
 [-SubscriptionName <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="64081-110">설명</span><span class="sxs-lookup"><span data-stu-id="64081-110">DESCRIPTION</span></span>
<span data-ttu-id="64081-111">**New-AzureSqlDatabaseServerContext** cmdlet은 Azure SQL 데이터베이스 서버 연결 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="64081-111">The **New-AzureSqlDatabaseServerContext** cmdlet creates an Azure SQL Database server connection context.</span></span>
<span data-ttu-id="64081-112">SQL Server 인증을 사용하여 지정된 자격 증명을 사용하여 SQL Database 서버에 대한 연결 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="64081-112">Use SQL Server authentication to create a connection context to a SQL Database server by using the specified credentials.</span></span>
<span data-ttu-id="64081-113">이름, SQL URL로 SQL 데이터베이스 서버를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64081-113">You can specify the SQL Database server by name, by the fully qualified name, or by URL.</span></span>
<span data-ttu-id="64081-114">자격 증명을 얻게 Get-Credential 사용자 이름 및 암호를 지정하라는 메시지를 표시하는 Get-Credential cmdlet을 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="64081-114">To obtain a credential, use the Get-Credential cmdlet that prompts you to specify the user name and password.</span></span>

<span data-ttu-id="64081-115">인증서 기반 인증과 **함께 New-AzureSqlDatabaseServerContext** cmdlet을 사용하여 지정된 Azure 구독 데이터를 사용하여 SQL Database 서버에 대한 연결 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="64081-115">Use the **New-AzureSqlDatabaseServerContext** cmdlet with certificate based authentication to create a connection context to the specified SQL Database server by using the specified Azure subscription data.</span></span>
<span data-ttu-id="64081-116">이름 또는 SQL 데이터베이스 서버를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64081-116">You can specify SQL Database server by name or by the fully qualified name.</span></span>
<span data-ttu-id="64081-117">구독 데이터를 매개 변수로 지정하거나 현재 Azure 구독에서 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64081-117">You can specify the subscription data as a parameter or it can be retrieved from the current Azure subscription.</span></span>
<span data-ttu-id="64081-118">Select-AzureSubscription cmdlet을 사용하여 현재 https://msdn.microsoft.com/library/windowsazure/jj152833.aspx Azure 구독을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="64081-118">Use the Select-AzureSubscriptionhttps://msdn.microsoft.com/library/windowsazure/jj152833.aspx cmdlet to select the current Azure subscription.</span></span>

## <span data-ttu-id="64081-119">예제</span><span class="sxs-lookup"><span data-stu-id="64081-119">EXAMPLES</span></span>

### <span data-ttu-id="64081-120">예제 1: 인증을 사용하여 컨텍스트 SQL Server</span><span class="sxs-lookup"><span data-stu-id="64081-120">Example 1: Create a context by using SQL Server authentication</span></span>
```
PS C:\> $Credential = Get-Credential
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -Credential $Credential
PS C:\> $Database17 = New-AzureSqlDatabase -ConnectionContext $Context -DatabaseName "Database17" -MaxSizeGB 50 -Collation "SQL_Latin1_General_CP1_CI_AS"
```

<span data-ttu-id="64081-121">이 예제에서는 SQL Server 인증을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="64081-121">This example uses the SQL Server authentication.</span></span>

<span data-ttu-id="64081-122">첫 번째 명령은 서버 관리자 자격 증명을 묻는 메시지를 표시하고 자격 증명을 $Credential 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="64081-122">The first command prompts you for server administrator credentials, and stores the credentials in the $Credential variable.</span></span>

<span data-ttu-id="64081-123">두 번째 명령은 SQL 사용하여 lpqd0zbr8y라는 $Credential.</span><span class="sxs-lookup"><span data-stu-id="64081-123">The second command connects to the SQL Database server named lpqd0zbr8y by using $Credential.</span></span>

<span data-ttu-id="64081-124">마지막 명령은 서버에서 컨텍스트의 일부인 Database17이라는 데이터베이스를 $Context.</span><span class="sxs-lookup"><span data-stu-id="64081-124">The final command creates a database named Database17 on the server that is part of the context in $Context.</span></span>

### <span data-ttu-id="64081-125">예제 2: 인증서 기반 인증을 사용하여 컨텍스트 만들기</span><span class="sxs-lookup"><span data-stu-id="64081-125">Example 2: Create a context by using certificate based authentication</span></span>
```
PS C:\> $SubscriptionId = <Subscription ID>
PS C:\> $Thumbprint = <Certificate Thumbprint>
PS C:\> $Certificate = Get-Item "Cert:\CurrentUser\My\$Thumbprint"
PS C:\> Set-AzureSubscription -SubscriptionName "Subscription07" -SubscriptionId $SubscriptionId -Certificate $Certificate
PS C:\> Select-AzureSubscription -SubscriptionName "Subscription07"
PS C:\> $Context = New-AzureSqlDatabaseServerContext -ServerName "lpqd0zbr8y" -UseSubscription
```

<span data-ttu-id="64081-126">이 예제에서는 인증서 기반 인증을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="64081-126">This example uses the certificate based authentication.</span></span>

<span data-ttu-id="64081-127">처음 두 명령은 변수 및 $SubscriptionId $Thumbprint 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="64081-127">The first two commands assign values to the $SubscriptionId and $Thumbprint variables.</span></span>

<span data-ttu-id="64081-128">세 번째 명령은 지문으로 식별된 인증서를 $Thumbprint 인증서를 $Certificate.</span><span class="sxs-lookup"><span data-stu-id="64081-128">The third command gets the certificate identified by the thumbprint in $Thumbprint, and stores it in $Certificate.</span></span>

<span data-ttu-id="64081-129">네 번째 명령은 구독을 Subscription07로 설정하고 다섯 번째 명령은 해당 구독을 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="64081-129">The fourth command sets the subscription to be Subscription07, and the fifth command selects that subscription.</span></span>

<span data-ttu-id="64081-130">마지막 명령은 lpqd0zbr8y라는 서버에 대한 현재 구독에 컨텍스트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="64081-130">The final command creates a context in the current subscription for the server named lpqd0zbr8y.</span></span>

## <span data-ttu-id="64081-131">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64081-131">PARAMETERS</span></span>

### <span data-ttu-id="64081-132">-Credential</span><span class="sxs-lookup"><span data-stu-id="64081-132">-Credential</span></span>
<span data-ttu-id="64081-133">서버에 액세스할 수 있도록 SQL Server 인증을 제공하는 자격 증명 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="64081-133">Specifies a credential object that provides SQL Server authentication for you to access the server.</span></span>

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

### <span data-ttu-id="64081-134">-FullyQualifiedServerName</span><span class="sxs-lookup"><span data-stu-id="64081-134">-FullyQualifiedServerName</span></span>
<span data-ttu-id="64081-135">Azure SQL Database 서버에 대한 FQDN(정식 도메인 이름) 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="64081-135">Specifies the fully qualified domain name (FQDN) name for the Azure SQL Database server.</span></span>
<span data-ttu-id="64081-136">예를 들어, Server02.database.windows.net.</span><span class="sxs-lookup"><span data-stu-id="64081-136">For example, Server02.database.windows.net.</span></span>

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

### <span data-ttu-id="64081-137">-ManageUrl</span><span class="sxs-lookup"><span data-stu-id="64081-137">-ManageUrl</span></span>
<span data-ttu-id="64081-138">이 cmdlet이 서버에 대한 Azure SQL DatabaseManagement 포털에 액세스하는 데 사용하는 URL을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="64081-138">Specifies the URL that this cmdlet uses to access the Azure SQL DatabaseManagement Portal for the server.</span></span>

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

### <span data-ttu-id="64081-139">-Profile</span><span class="sxs-lookup"><span data-stu-id="64081-139">-Profile</span></span>
<span data-ttu-id="64081-140">이 cmdlet이 읽을 Azure 프로필을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="64081-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="64081-141">프로필을 지정하지 않으면 이 cmdlet은 로컬 기본 프로필에서 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="64081-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="64081-142">-ServerName</span><span class="sxs-lookup"><span data-stu-id="64081-142">-ServerName</span></span>
<span data-ttu-id="64081-143">데이터베이스 서버의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="64081-143">Specifies the name of the database server.</span></span>

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

### <span data-ttu-id="64081-144">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="64081-144">-SubscriptionName</span></span>
<span data-ttu-id="64081-145">이 cmdlet이 연결 컨텍스트를 만드는 데 사용하는 Azure 구독의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="64081-145">Specifies the name of the Azure subscription that this cmdlet uses to create the connection context.</span></span>
<span data-ttu-id="64081-146">이 매개 변수에 대한 값을 지정하지 않으면 cmdlet은 현재 구독을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="64081-146">If you do not specify a value for this parameter, the cmdlet uses the current subscription.</span></span>
<span data-ttu-id="64081-147">Select-AzureSubscription cmdlet을 실행하여 현재 구독을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="64081-147">Run the Select-AzureSubscription cmdlet to change the current subscription.</span></span>

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

### <span data-ttu-id="64081-148">-UseSubscription</span><span class="sxs-lookup"><span data-stu-id="64081-148">-UseSubscription</span></span>
<span data-ttu-id="64081-149">이 cmdlet이 연결 컨텍스트를 만드는 데 Azure 구독을 사용 중입니다.</span><span class="sxs-lookup"><span data-stu-id="64081-149">Indicates that this cmdlet uses Azure subscription for creating the connection context.</span></span>

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

### <span data-ttu-id="64081-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64081-150">CommonParameters</span></span>
<span data-ttu-id="64081-151">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="64081-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64081-152">자세한 내용은 다음 about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="64081-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64081-153">입력</span><span class="sxs-lookup"><span data-stu-id="64081-153">INPUTS</span></span>

## <span data-ttu-id="64081-154">출력</span><span class="sxs-lookup"><span data-stu-id="64081-154">OUTPUTS</span></span>

### <span data-ttu-id="64081-155">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.IServerDataServiceContext</span><span class="sxs-lookup"><span data-stu-id="64081-155">Microsoft.WindowsAzure.Commands.SqlDatabase.Services.Server.IServerDataServiceContext</span></span>

## <span data-ttu-id="64081-156">참고 사항</span><span class="sxs-lookup"><span data-stu-id="64081-156">NOTES</span></span>
* <span data-ttu-id="64081-157">도메인을 지정하지 않고 인증하고 Windows PowerShell 2.0을 사용하는 경우 Get-Credential cmdlet은 사용자 이름(예: \user)에 추가된 백슬래시()를 \\ 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="64081-157">If you authenticate without specifying a domain, and if you use Windows PowerShell 2.0, the Get-Credential cmdlet returns a backslash (\\) prepended to the username, for example, \user.</span></span> <span data-ttu-id="64081-158">Windows PowerShell 3.0에서는 백 슬래시를 추가하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="64081-158">Windows PowerShell 3.0 does not add the backslash.</span></span> <span data-ttu-id="64081-159">이 백슬래시는 **New-AzureSqlDatabaseServerContext** cmdlet의 자격 증명 매개 변수에서 인식되지 않습니다. </span><span class="sxs-lookup"><span data-stu-id="64081-159">This backslash is not recognized by the *Credential* parameter of the **New-AzureSqlDatabaseServerContext** cmdlet.</span></span> <span data-ttu-id="64081-160">제거하려면 다음과 유사한 명령을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="64081-160">To remove it, use commands similar to the following:</span></span>

  `PS C:\\\> $Credential = Get-Credential`
`PS C:\\\> $Credential = New-Object -TypeName 'System.Management.Automation.PSCredential' -ArgumentList $Credential.Username.Replace("\",""),$Credential.Password`

## <span data-ttu-id="64081-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="64081-161">RELATED LINKS</span></span>



[<span data-ttu-id="64081-162">Get-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="64081-162">Get-AzureSqlDatabase</span></span>](./Get-AzureSqlDatabase.md)

[<span data-ttu-id="64081-163">New-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="64081-163">New-AzureSqlDatabase</span></span>](./New-AzureSqlDatabase.md)

[<span data-ttu-id="64081-164">Remove-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="64081-164">Remove-AzureSqlDatabase</span></span>](./Remove-AzureSqlDatabase.md)

[<span data-ttu-id="64081-165">Set-AzureSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="64081-165">Set-AzureSqlDatabase</span></span>](./Set-AzureSqlDatabase.md)


