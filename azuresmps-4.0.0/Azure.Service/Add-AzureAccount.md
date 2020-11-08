---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 03EAFFB2-EA64-4227-A33B-D24EB4A75F71
online version: ''
schema: 2.0.0
ms.openlocfilehash: ac88bc2494bad975c6169262edd05c7b821061bb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046396"
---
# <span data-ttu-id="8bcb7-101">Add-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="8bcb7-101">Add-AzureAccount</span></span>

## <span data-ttu-id="8bcb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8bcb7-102">SYNOPSIS</span></span>
<span data-ttu-id="8bcb7-103">Windows PowerShell에 Azure 계정을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bcb7-103">Adds the Azure account to Windows PowerShell.</span></span>

## <span data-ttu-id="8bcb7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8bcb7-104">SYNTAX</span></span>

### <span data-ttu-id="8bcb7-105">사용자 (기본값)</span><span class="sxs-lookup"><span data-stu-id="8bcb7-105">User (Default)</span></span>
```
Add-AzureAccount [-Environment <String>] [-Credential <PSCredential>] [-Tenant <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="8bcb7-106">ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="8bcb7-106">ServicePrincipal</span></span>
```
Add-AzureAccount [-Environment <String>] -Credential <PSCredential> [-ServicePrincipal] -Tenant <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8bcb7-107">설명은</span><span class="sxs-lookup"><span data-stu-id="8bcb7-107">DESCRIPTION</span></span>
<span data-ttu-id="8bcb7-108">Windows PowerShell에서 Azure 계정 및 해당 구독을 사용할 수 있도록 **추가-azureaccount** cmdlet을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bcb7-108">The **Add-AzureAccount** cmdlet makes your Azure account and its subscriptions available in Windows PowerShell.</span></span>
<span data-ttu-id="8bcb7-109">Windows PowerShell에서 Azure 계정으로 로그인 하는 것과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="8bcb7-109">It's like logging into your Azure account in Windows PowerShell.</span></span>
<span data-ttu-id="8bcb7-110">계정에서 로그 아웃 하려면 **제거-AzureAccount** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bcb7-110">To log out of the account, use the **Remove-AzureAccount** cmdlet.</span></span>

<span data-ttu-id="8bcb7-111">**-Azureaccount** Azure 계정에 대 한 정보를 다운로드 하 고 로밍 사용자 프로필의 구독 데이터 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bcb7-111">**Add-AzureAccount** downloads information about your Azure account and saves it in a subscription data file in your roaming user profile.</span></span>
<span data-ttu-id="8bcb7-112">또한 Windows PowerShell에서 사용자 대신 Azure 계정에 액세스할 수 있도록 하는 액세스 토큰을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8bcb7-112">It also gets an access token that allows Windows PowerShell to access your Azure account on your behalf.</span></span>
<span data-ttu-id="8bcb7-113">명령이 완료 되 면 Windows PowerShell에서 Azure 계정을 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8bcb7-113">When the command completes, you can manage your Azure account in Windows PowerShell.</span></span>

<span data-ttu-id="8bcb7-114">Azure 계정을 Windows PowerShell에서 사용할 수 있도록 하는 방법에는 두 가지 방법이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8bcb7-114">There are two different ways to make your Azure account available to Windows PowerShell.</span></span>
<span data-ttu-id="8bcb7-115">Azure AD (azure Active Directory) 인증 액세스 토큰 또는 관리 인증서를 사용 하는 **가져오기-Azureaccount Settingsfile** 을 사용 하는 **추가-azureaccount** cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8bcb7-115">You can use the **Add-AzureAccount** cmdlet, which uses Azure Active Directory (Azure AD) authentication access tokens, or **Import-AzurePublishSettingsFile** , which uses a management certificate.</span></span>
<span data-ttu-id="8bcb7-116">사용할 방법에 대 한 지침은 [방법: 구독에 연결](https://azure.microsoft.com/documentation/articles/install-configure-powershell) ()을 참조 하세요 https://azure.microsoft.com/documentation/articles/install-configure-powershell/#Connect) .</span><span class="sxs-lookup"><span data-stu-id="8bcb7-116">For guidance on which method to use, see [How to: Connect to your subscription](https://azure.microsoft.com/documentation/articles/install-configure-powershell) (https://azure.microsoft.com/documentation/articles/install-configure-powershell/#Connect).</span></span>

<span data-ttu-id="8bcb7-117">**-AzureAccount** 를 실행 하면 Azure 계정에 로그인 하 라는 메시지가 대화형 창으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8bcb7-117">When you run **Add-AzureAccount** , it displays an interactive window that prompts you to sign into your Azure account.</span></span>
<span data-ttu-id="8bcb7-118">이 로그인은 액세스 토큰이 만료 될 때까지 유효 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bcb7-118">This sign-in is valid until the access token expires.</span></span>
<span data-ttu-id="8bcb7-119">만료 되는 경우 계정에 액세스 해야 하는 cmdlet **은 추가 AzureAccount** 를 다시 실행 하 라는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bcb7-119">When it expires, cmdlets that require access to your account prompt you to run **Add-AzureAccount** again.</span></span>

<span data-ttu-id="8bcb7-120">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bcb7-120">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="8bcb7-121">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bcb7-121">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="8bcb7-122">예제의</span><span class="sxs-lookup"><span data-stu-id="8bcb7-122">EXAMPLES</span></span>

### <span data-ttu-id="8bcb7-123">예제 1: 계정 추가</span><span class="sxs-lookup"><span data-stu-id="8bcb7-123">Example 1: Add an account</span></span>
```
PS C:\> Add-AzureAccount
```

<span data-ttu-id="8bcb7-124">이 명령은 Windows PowerShell에 Azure 계정을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bcb7-124">This command adds an Azure account to Windows PowerShell.</span></span>
<span data-ttu-id="8bcb7-125">명령을 실행 하면 windows에서 계정의 사용자 이름 및 암호를 요청 하기 위해 팝업을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bcb7-125">When you run the command, a windows pops up to request the user name and password of the account.</span></span>

### <span data-ttu-id="8bcb7-126">예제 2: 대체 구독 데이터 파일 사용</span><span class="sxs-lookup"><span data-stu-id="8bcb7-126">Example 2: Use an alternate subscription data file</span></span>
```
PS C:\> Add-AzureAccount -SubscriptionDataFile C:\Testing\SDF.xml
```

<span data-ttu-id="8bcb7-127">이 명령은 **subscriptiondatafile** 매개 변수를 사용 하 여 기본 파일 대신 C:\Testing\SDF.xml 파일에 계정 데이터를 저장 하도록 **-Azureaccount 직접 추가** 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bcb7-127">This command uses the **SubscriptionDataFile** parameter to direct **Add-AzureAccount** to store the account data in the C:\Testing\SDF.xml file, instead of the default file.</span></span>

## <span data-ttu-id="8bcb7-128">변수</span><span class="sxs-lookup"><span data-stu-id="8bcb7-128">PARAMETERS</span></span>

### <span data-ttu-id="8bcb7-129">-Credential</span><span class="sxs-lookup"><span data-stu-id="8bcb7-129">-Credential</span></span>
```yaml
Type: PSCredential
Parameter Sets: User
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: PSCredential
Parameter Sets: ServicePrincipal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bcb7-130">-환경</span><span class="sxs-lookup"><span data-stu-id="8bcb7-130">-Environment</span></span>
<span data-ttu-id="8bcb7-131">Azure 환경을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bcb7-131">Specifies an Azure environment.</span></span>

<span data-ttu-id="8bcb7-132">Azure 환경에서 글로벌 Azure 용 AzureCloud 및 중국의 21Vianet이 운영 하는 Azure 용 AzureChinaCloud와 같은 Microsoft Azure의 독립 배포입니다.</span><span class="sxs-lookup"><span data-stu-id="8bcb7-132">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="8bcb7-133">Azure Pack 및 WAPack cmdlet을 사용 하 여 온-프레미스 Azure 환경을 만들 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8bcb7-133">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="8bcb7-134">자세한 내용은 [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ()을 참조 하세요 https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="8bcb7-134">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

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

### <span data-ttu-id="8bcb7-135">-프로필</span><span class="sxs-lookup"><span data-stu-id="8bcb7-135">-Profile</span></span>
<span data-ttu-id="8bcb7-136">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bcb7-136">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="8bcb7-137">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="8bcb7-137">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8bcb7-138">-ServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="8bcb7-138">-ServicePrincipal</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: ServicePrincipal
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bcb7-139">-테 넌 트</span><span class="sxs-lookup"><span data-stu-id="8bcb7-139">-Tenant</span></span>
```yaml
Type: String
Parameter Sets: User
Aliases: TenantId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ServicePrincipal
Aliases: TenantId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8bcb7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bcb7-140">CommonParameters</span></span>
<span data-ttu-id="8bcb7-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bcb7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bcb7-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8bcb7-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bcb7-143">입력</span><span class="sxs-lookup"><span data-stu-id="8bcb7-143">INPUTS</span></span>

### <span data-ttu-id="8bcb7-144">않아야</span><span class="sxs-lookup"><span data-stu-id="8bcb7-144">None</span></span>
<span data-ttu-id="8bcb7-145">이 cmdlet에는 입력을 파이프로 지정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="8bcb7-145">You cannot pipe input to this cmdlet</span></span>

## <span data-ttu-id="8bcb7-146">출력</span><span class="sxs-lookup"><span data-stu-id="8bcb7-146">OUTPUTS</span></span>

### <span data-ttu-id="8bcb7-147">않아야</span><span class="sxs-lookup"><span data-stu-id="8bcb7-147">None</span></span>
<span data-ttu-id="8bcb7-148">이 cmdlet은 출력을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8bcb7-148">This cmdlet does not return any output.</span></span>

## <span data-ttu-id="8bcb7-149">상속자</span><span class="sxs-lookup"><span data-stu-id="8bcb7-149">NOTES</span></span>
* <span data-ttu-id="8bcb7-150">**추가-AzureAccount** (및 Azure AD 인증 방법)는 **AzurePublishSettings** (및 관리 인증서 방법) 보다 우선 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bcb7-150">**Add-AzureAccount** (and the Azure AD authentication method) takes precedence over **Import-AzurePublishSettings** (and the management certificate method).</span></span> <span data-ttu-id="8bcb7-151">계정에서 **추가-AzureAccount** 를 사용 하는 경우 Azure AD 인증 방법이 사용 되 고 관리 인증서는 무시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8bcb7-151">If you use **Add-AzureAccount** even once on your account, the Azure AD authentication method is used and the management certificate is ignored.</span></span> <span data-ttu-id="8bcb7-152">Azure AD 토큰을 제거 하 고 관리 인증서 메서드를 복원 하려면 **제거-AzureAccount** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bcb7-152">To remove the Azure AD token and restore the management certificate method, use the **Remove-AzureAccount** cmdlet.</span></span> <span data-ttu-id="8bcb7-153">자세한 내용은 **Get-help 제거-AzureAccount** 를 입력 하세요.</span><span class="sxs-lookup"><span data-stu-id="8bcb7-153">For more information, type: **Get-Help Remove-AzureAccount**.</span></span>
* <span data-ttu-id="8bcb7-154">"귀하의 자격 증명이 만료 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="8bcb7-154">The error, "Your credentials have expired.</span></span> <span data-ttu-id="8bcb7-155">Add-AzureAccount을 (를) 사용 하 여 다시 로그인 하십시오. "</span><span class="sxs-lookup"><span data-stu-id="8bcb7-155">Please use Add-AzureAccount to log in again."</span></span> <span data-ttu-id="8bcb7-156">액세스 토큰이 만료 되 고 Windows PowerShell에서 Azure 계정에 액세스할 수 없음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8bcb7-156">indicates that your access token is expired and Windows PowerShell cannot access your Azure account.</span></span> <span data-ttu-id="8bcb7-157">계정에 대 한 액세스를 복원 하려면 **-Azureaccount 추가** 를 다시 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="8bcb7-157">To restore access to your account, run **Add-AzureAccount** again.</span></span>
* <span data-ttu-id="8bcb7-158">Azure PowerShell 계정 및 구독 cmdlet은 live Azure 계정이 아닌 구독 데이터 파일에서 데이터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8bcb7-158">The Azure PowerShell account and subscription cmdlets get their data from the  subscription data file, not from the live Azure account.</span></span> <span data-ttu-id="8bcb7-159">Azure 관리 포털을 사용 하는 등 Windows PowerShell 외부에서 계정 또는 구독을 변경 하는 경우 **-AzureAccount** 를 다시 실행 하 여 구독 데이터 파일을 새로 고칩니다.</span><span class="sxs-lookup"><span data-stu-id="8bcb7-159">If you change your account or subscriptions outside of Windows PowerShell, such as by using the Azure Management Portal, run **Add-AzureAccount** again to refresh the subscription data file.</span></span>

## <span data-ttu-id="8bcb7-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8bcb7-160">RELATED LINKS</span></span>

[<span data-ttu-id="8bcb7-161">-AzureEnvironment 추가</span><span class="sxs-lookup"><span data-stu-id="8bcb7-161">Add-AzureEnvironment</span></span>](./Add-AzureEnvironment.md)

[<span data-ttu-id="8bcb7-162">가져오기-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="8bcb7-162">Get-AzureEnvironment</span></span>](./Get-AzureEnvironment.md)

[<span data-ttu-id="8bcb7-163">가져오기-Azure# settingsfile</span><span class="sxs-lookup"><span data-stu-id="8bcb7-163">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)

[<span data-ttu-id="8bcb7-164">Get-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="8bcb7-164">Get-AzureAccount</span></span>](./Get-AzureAccount.md)

[<span data-ttu-id="8bcb7-165">-AzureAccount 제거</span><span class="sxs-lookup"><span data-stu-id="8bcb7-165">Remove-AzureAccount</span></span>](./Remove-AzureAccount.md)


