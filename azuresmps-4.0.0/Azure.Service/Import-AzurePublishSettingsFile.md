---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 79D64D7C-6671-4F03-8776-70A716F36512
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2bc0525ee7238de421842b74f52f7dd4fa59df1a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046261"
---
# <span data-ttu-id="f23c8-101">Import-AzurePublishSettingsFile</span><span class="sxs-lookup"><span data-stu-id="f23c8-101">Import-AzurePublishSettingsFile</span></span>

## <span data-ttu-id="f23c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f23c8-102">SYNOPSIS</span></span>
<span data-ttu-id="f23c8-103">Windows PowerShell에서 Azure 계정을 관리할 수 있는 게시 설정 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f23c8-103">Imports a publish settings file that lets you manage your Azure accounts in Windows PowerShell.</span></span>

## <span data-ttu-id="f23c8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f23c8-104">SYNTAX</span></span>

```
Import-AzurePublishSettingsFile -PublishSettingsFile <String> [-Environment <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="f23c8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f23c8-105">DESCRIPTION</span></span>
<span data-ttu-id="f23c8-106">**가져오기-Azure버전 파일** Cmdlet은 Azure 계정에 대 한 정보가 포함 된 게시 설정 파일 (\* publishsettings)을 가져오고 구독 데이터 파일을 컴퓨터에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f23c8-106">The **Import-AzurePublishSettingsFile** cmdlet imports a publish settings file (\*.publishsettings) that contains information about your Azure accounts and saves a subscription data file on your computer.</span></span>
<span data-ttu-id="f23c8-107">Cmdlet이 완료 되 면 Windows PowerShell에서 Azure 계정을 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f23c8-107">When the cmdlet completes, you can manage your Azure accounts in Windows PowerShell.</span></span>

<span data-ttu-id="f23c8-108">가져오기 **-Azure# settingsfile** 을 실행 하기 전에 가져올 수 있도록 게시 설정 파일을 다운로드 하 여 저장 하는 **Get-azure# settingsfile** 을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="f23c8-108">Before running **Import-AzurePublishSettingsFile** , run **Get-AzurePublishSettingsFile** , which downloads and saves the publish settings file so you can import it.</span></span>

<span data-ttu-id="f23c8-109">Windows PowerShell에서 Azure 계정을 사용할 수 있도록 하려면 게시 설정 파일 또는 **추가-AzureAccount** cmdlet을 사용 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f23c8-109">To make your Azure account available to Windows PowerShell, you can use a publish settings file or the **Add-AzureAccount** cmdlet.</span></span>
<span data-ttu-id="f23c8-110">게시 설정 파일을 사용 하면 세션을 미리 준비 하 여 스크립트와 백그라운드 작업을 무인 모드로 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f23c8-110">Publish settings files let you prepare the session in advance so you can run scripts and background jobs unattended.</span></span>
<span data-ttu-id="f23c8-111">그러나 모든 서비스에서 설정 파일 게시를 지원 하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f23c8-111">However, not all services support publish settings files.</span></span>
<span data-ttu-id="f23c8-112">예를 들어 **AzureResourceManager** 모듈은 게시 설정 파일을 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f23c8-112">For example, the **AzureResourceManager** module does not support publish settings files.</span></span>

<span data-ttu-id="f23c8-113">**보안 참고 사항:** 게시 설정 파일에는 인코딩되어 있지만 암호화 되지 않은 관리 인증서가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f23c8-113">**Security Note:** Publish settings files contain a management certificate that is encoded, but not encrypted.</span></span>
<span data-ttu-id="f23c8-114">악의적인 사용자가 게시 설정 파일에 액세스 하는 경우 Azure 서비스를 편집, 만들기, 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f23c8-114">If  malicious users access your publish settings file,  they might be able to edit, create, and delete your Azure services.</span></span>
<span data-ttu-id="f23c8-115">최상의 보안을 위해 파일을 다운로드 또는 문서 폴더의 위치에 저장 한 다음 **가져오기-Azure# settingsfile** cmdlet을 사용 하 여 설정을 가져와 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="f23c8-115">As a security best practice, save the file to a location in your Downloads or Documents folder and then delete it after using **Import-AzurePublishSettingsFile** cmdlet to import the settings.</span></span>

## <span data-ttu-id="f23c8-116">예제의</span><span class="sxs-lookup"><span data-stu-id="f23c8-116">EXAMPLES</span></span>

### <span data-ttu-id="f23c8-117">예제 1: 파일 가져오기</span><span class="sxs-lookup"><span data-stu-id="f23c8-117">Example 1: Import a file</span></span>
```
PS C:\> Import-AzurePublishSettingsFile -PublishSettingsFile C:\Temp\MyAccount.publishsettings
```

<span data-ttu-id="f23c8-118">이 명령은 "C:\Temp\MyAccount.publishsettings" 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f23c8-118">This command imports the "C:\Temp\MyAccount.publishsettings" file.</span></span>

## <span data-ttu-id="f23c8-119">변수</span><span class="sxs-lookup"><span data-stu-id="f23c8-119">PARAMETERS</span></span>

### <span data-ttu-id="f23c8-120">-환경</span><span class="sxs-lookup"><span data-stu-id="f23c8-120">-Environment</span></span>
<span data-ttu-id="f23c8-121">Azure 환경을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f23c8-121">Specifies an Azure environment.</span></span>

<span data-ttu-id="f23c8-122">Azure 환경에서 글로벌 Azure 용 AzureCloud 및 중국의 21Vianet이 운영 하는 Azure 용 AzureChinaCloud와 같은 Microsoft Azure의 독립 배포입니다.</span><span class="sxs-lookup"><span data-stu-id="f23c8-122">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="f23c8-123">Azure Pack 및 WAPack cmdlet을 사용 하 여 온-프레미스 Azure 환경을 만들 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f23c8-123">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="f23c8-124">자세한 내용은 [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ()을 참조 하세요 https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f23c8-124">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

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

### <span data-ttu-id="f23c8-125">-프로필</span><span class="sxs-lookup"><span data-stu-id="f23c8-125">-Profile</span></span>
<span data-ttu-id="f23c8-126">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f23c8-126">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="f23c8-127">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="f23c8-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f23c8-128">-# 파일</span><span class="sxs-lookup"><span data-stu-id="f23c8-128">-PublishSettingsFile</span></span>
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

### <span data-ttu-id="f23c8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f23c8-129">CommonParameters</span></span>
<span data-ttu-id="f23c8-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f23c8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f23c8-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f23c8-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f23c8-132">입력</span><span class="sxs-lookup"><span data-stu-id="f23c8-132">INPUTS</span></span>

### <span data-ttu-id="f23c8-133">않아야</span><span class="sxs-lookup"><span data-stu-id="f23c8-133">None</span></span>
<span data-ttu-id="f23c8-134">속성 이름으로이 cmdlet에 대 한 입력을 파이프로 지정할 수 있지만 값을 기준으로 하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f23c8-134">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="f23c8-135">출력</span><span class="sxs-lookup"><span data-stu-id="f23c8-135">OUTPUTS</span></span>

### <span data-ttu-id="f23c8-136">않아야</span><span class="sxs-lookup"><span data-stu-id="f23c8-136">None</span></span>
<span data-ttu-id="f23c8-137">이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f23c8-137">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="f23c8-138">상속자</span><span class="sxs-lookup"><span data-stu-id="f23c8-138">NOTES</span></span>
* <span data-ttu-id="f23c8-139">"게시 설정 파일"은 확장명이 publishsettings 인 XML 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="f23c8-139">A "publish settings file" is an XML file with a .publishsettings file name extension.</span></span> <span data-ttu-id="f23c8-140">파일에는 Azure 구독에 대 한 관리 자격 증명을 제공 하는 인코딩된 인증서가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f23c8-140">The file contains an encoded certificate that provides management credentials for your Azure subscriptions.</span></span> <span data-ttu-id="f23c8-141">이 파일을 가져온 후에는 보안 위험을 방지 하기 위해 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="f23c8-141">After you import this file, delete it to avoid security risks.</span></span>
* <span data-ttu-id="f23c8-142">"구독 데이터 파일"은 컴퓨터에 안전 하 게 저장할 수 있는 XML 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="f23c8-142">A "subscription data file" is an XML file that can be saved on your computer safely.</span></span> <span data-ttu-id="f23c8-143">기본적으로 사용자 로밍 프로필 ($home/AppData/Roaming)에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f23c8-143">By default, it's saved in your roaming user profile ($home/AppData/Roaming).</span></span>

## <span data-ttu-id="f23c8-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f23c8-144">RELATED LINKS</span></span>

[<span data-ttu-id="f23c8-145">Azure PowerShell을 설치 하 고 구성 하는 방법</span><span class="sxs-lookup"><span data-stu-id="f23c8-145">How to Install and Configure Azure PowerShell</span></span>](https://azure.microsoft.com/documentation/articles/install-configure-powershell/)

[<span data-ttu-id="f23c8-146">추가-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="f23c8-146">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="f23c8-147">Get-Azure도움말 파일</span><span class="sxs-lookup"><span data-stu-id="f23c8-147">Get-AzurePublishSettingsFile</span></span>](./Get-AzurePublishSettingsFile.md)


