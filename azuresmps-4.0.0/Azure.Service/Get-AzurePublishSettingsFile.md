---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: A5419F76-B85E-445D-84EA-CC695B175C8D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1364cf1bbec1fdca2a8c9901556d38de0b620358
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045633"
---
# <span data-ttu-id="2e883-101">Get-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="2e883-101">Get-AzurePublishSettingsFile</span></span>

## <span data-ttu-id="2e883-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e883-102">SYNOPSIS</span></span>
<span data-ttu-id="2e883-103">Azure 구독에 대 한 게시 설정 파일을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e883-103">Downloads the publish settings file for an Azure subscription.</span></span>

## <span data-ttu-id="2e883-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2e883-104">SYNTAX</span></span>

```
Get-AzurePublishSettingsFile [-Environment <String>] [-Realm <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="2e883-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2e883-105">DESCRIPTION</span></span>
<span data-ttu-id="2e883-106">**Get-azure게시 설정 파일** cmdlet은 사용자의 계정에 대 한 구독에 대 한 제작 설정 파일을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e883-106">The **Get-AzurePublishSettingsFile** cmdlet downloads a publish settings file for a subscription in your account.</span></span>
<span data-ttu-id="2e883-107">명령이 완료 되 면 **Import-module settingsfile** cmdlet을 사용 하 여 Windows PowerShell에서 파일의 설정을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2e883-107">When the command completes, you can use the **Import-PublishSettingsFile** cmdlet to make the settings in the file available to Windows PowerShell.</span></span>

<span data-ttu-id="2e883-108">Windows PowerShell에서 Azure 계정을 사용할 수 있도록 하려면 게시 설정 파일 또는 **추가-AzureAccount** cmdlet을 사용 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2e883-108">To make your Azure account available to Windows PowerShell, you can use a publish settings file or the **Add-AzureAccount** cmdlet.</span></span>
<span data-ttu-id="2e883-109">게시 설정 파일을 사용 하면 세션을 미리 준비 하 여 스크립트와 백그라운드 작업을 무인 모드로 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2e883-109">Publish settings files let you prepare the session in advance so you can run scripts and background jobs unattended.</span></span>
<span data-ttu-id="2e883-110">그러나 모든 서비스에서 설정 파일 게시를 지원 하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2e883-110">However, not all services support publish settings files.</span></span>
<span data-ttu-id="2e883-111">예를 들어 **AzureResourceManager** 모듈은 게시 설정 파일을 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2e883-111">For example, the **AzureResourceManager** module does not support publish settings files.</span></span>

<span data-ttu-id="2e883-112">**Get-Azure# settingsfile** 을 실행할 때 기본 브라우저가 열리고 Azure 계정에 로그인 하 라는 메시지가 표시 되 면 구독을 선택 하 고 게시 설정 파일에 대 한 파일 시스템 위치를 선택 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e883-112">When you run **Get-AzurePublishSettingsFile** , it opens your default browser and prompts you to sign into your Azure account, select a subscription, and select a file system location for the publish settings file.</span></span>
<span data-ttu-id="2e883-113">그런 다음 구독에 대 한 게시 설정 파일을 선택한 파일에 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e883-113">Then, it downloads the publish settings file for your subscription into the file that you selected.</span></span>

<span data-ttu-id="2e883-114">"게시 설정 파일"은 확장명이 publishsettings 인 XML 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="2e883-114">A "publish settings file" is an XML file with a .publishsettings file name extension.</span></span>
<span data-ttu-id="2e883-115">파일에는 Azure 구독에 대 한 관리 자격 증명을 제공 하는 인코딩된 인증서가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2e883-115">The file contains an encoded certificate that provides management credentials for your Azure subscriptions.</span></span>

<span data-ttu-id="2e883-116">**보안 참고 사항:** 게시 설정 파일에는 Azure 구독 및 서비스를 관리 하는 데 사용 되는 자격 증명이 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2e883-116">**Security Note:** Publish settings files contains credentials that are used to administer your Azure subscriptions and services.</span></span>
<span data-ttu-id="2e883-117">악의적인 사용자가 게시 설정 파일에 액세스 하는 경우 Azure 서비스를 편집, 만들기, 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2e883-117">If  malicious users access your publish settings file,  they can edit, create, and delete your Azure services.</span></span>
<span data-ttu-id="2e883-118">최상의 보안을 위해 파일을 다운로드 또는 문서 폴더의 위치에 저장 한 다음 **가져오기-Azure# settingsfile** cmdlet을 사용 하 여 설정을 가져와 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e883-118">As a security best practice, save the file to a location in your Downloads or Documents folder and then delete it after using **Import-AzurePublishSettingsFile** cmdlet to import the settings.</span></span>

<span data-ttu-id="2e883-119">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e883-119">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="2e883-120">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e883-120">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="2e883-121">예제의</span><span class="sxs-lookup"><span data-stu-id="2e883-121">EXAMPLES</span></span>

### <span data-ttu-id="2e883-122">예제 1: 게시 설정 파일 다운로드</span><span class="sxs-lookup"><span data-stu-id="2e883-122">Example 1: Download a publish settings file</span></span>
```
PS C:\> Get-AzurePublishSettingsFile
```

<span data-ttu-id="2e883-123">이 명령은 기본 브라우저를 열고 Windows Azure 계정에 연결한 다음 계정에 대 한 publishsettings 파일을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e883-123">This command opens your default browser, connects to your Windows Azure account, and then downloads the .publishsettings file for your account.</span></span>

### <span data-ttu-id="2e883-124">예제 2: 영역 지정</span><span class="sxs-lookup"><span data-stu-id="2e883-124">Example 2: Specify a realm</span></span>
```
PS C:\> Get-AzurePublishSettingsFile -Realm contoso.com -Passthru
```

<span data-ttu-id="2e883-125">이 명령은 contoso.com 도메인의 계정에 대 한 게시 설정 파일을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e883-125">This command downloads the publish settings file for an account in the contoso.com domain.</span></span>
<span data-ttu-id="2e883-126">Microsoft 계정 대신 조직 계정으로 Azure에 로그인 하는 경우에는 **Realm** 매개 변수와 함께 명령을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e883-126">Use a command with the **Realm** parameter when you sign into Azure with an organizational account, instead of a Microsoft account.</span></span>

## <span data-ttu-id="2e883-127">변수</span><span class="sxs-lookup"><span data-stu-id="2e883-127">PARAMETERS</span></span>

### <span data-ttu-id="2e883-128">-환경</span><span class="sxs-lookup"><span data-stu-id="2e883-128">-Environment</span></span>
<span data-ttu-id="2e883-129">Azure 환경을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e883-129">Specifies an Azure environment.</span></span>

<span data-ttu-id="2e883-130">Azure 환경에서 글로벌 Azure 용 AzureCloud 및 중국의 21Vianet이 운영 하는 Azure 용 AzureChinaCloud와 같은 Microsoft Azure의 독립 배포입니다.</span><span class="sxs-lookup"><span data-stu-id="2e883-130">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="2e883-131">Azure Pack 및 WAPack cmdlet을 사용 하 여 온-프레미스 Azure 환경을 만들 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2e883-131">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="2e883-132">자세한 내용은 [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ()을 참조 하세요 https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="2e883-132">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

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

### <span data-ttu-id="2e883-133">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2e883-133">-PassThru</span></span>
<span data-ttu-id="2e883-134">명령이 성공한 경우 $True를 반환 하 고 오류가 발생 하면 $False 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e883-134">Returns $True if the command succeeds and $False if it fails.</span></span>
<span data-ttu-id="2e883-135">기본적으로이 cmdlet은 출력을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2e883-135">By default, this cmdlet does not return any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2e883-136">-프로필</span><span class="sxs-lookup"><span data-stu-id="2e883-136">-Profile</span></span>
<span data-ttu-id="2e883-137">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e883-137">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="2e883-138">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="2e883-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2e883-139">-영역</span><span class="sxs-lookup"><span data-stu-id="2e883-139">-Realm</span></span>
<span data-ttu-id="2e883-140">조직을 조직 ID로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e883-140">Specifies the organization in an organizational ID.</span></span>
<span data-ttu-id="2e883-141">예를 들어 Azure에 로그인 하는 경우 admin@contoso.com **Realm** 매개 변수 값은 contoso.com입니다.</span><span class="sxs-lookup"><span data-stu-id="2e883-141">For example, if you sign into Azure as admin@contoso.com, the value of the **Realm** parameter is contoso.com.</span></span>
<span data-ttu-id="2e883-142">조직 ID를 사용 하 여 Azure 포털에 로그인 하는 경우이 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e883-142">Use this parameter when you use an organizational ID to sign into the Azure portal.</span></span>
<span data-ttu-id="2e883-143">Outlook.com 또는 live.com 계정 등의 Microsoft 계정을 사용 하는 경우이 매개 변수는 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2e883-143">This parameter is not required when you use a Microsoft account, such as an outlook.com or live.com account.</span></span>

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

### <span data-ttu-id="2e883-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e883-144">CommonParameters</span></span>
<span data-ttu-id="2e883-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e883-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e883-146">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e883-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e883-147">입력</span><span class="sxs-lookup"><span data-stu-id="2e883-147">INPUTS</span></span>

### <span data-ttu-id="2e883-148">않아야</span><span class="sxs-lookup"><span data-stu-id="2e883-148">None</span></span>
<span data-ttu-id="2e883-149">속성 이름으로이 cmdlet에 대 한 입력을 파이프로 지정할 수 있지만 값을 기준으로 하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2e883-149">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="2e883-150">출력</span><span class="sxs-lookup"><span data-stu-id="2e883-150">OUTPUTS</span></span>

### <span data-ttu-id="2e883-151">없음 또는 시스템 부울</span><span class="sxs-lookup"><span data-stu-id="2e883-151">None or System.Boolean</span></span>
<span data-ttu-id="2e883-152">*PassThru* 매개 변수를 사용 하는 경우이 Cmdlet은 부울 값을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e883-152">When you use the *PassThru* parameter, this cmdlet returns a Boolean value.</span></span>
<span data-ttu-id="2e883-153">그렇지 않으면이 cmdlet은 출력을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2e883-153">Otherwise, this cmdlet does not return any output</span></span>

## <span data-ttu-id="2e883-154">상속자</span><span class="sxs-lookup"><span data-stu-id="2e883-154">NOTES</span></span>

## <span data-ttu-id="2e883-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2e883-155">RELATED LINKS</span></span>

[<span data-ttu-id="2e883-156">추가-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="2e883-156">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="2e883-157">가져오기-Azure# settingsfile</span><span class="sxs-lookup"><span data-stu-id="2e883-157">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)


