---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: BF5E3E1A-14B6-4630-8168-628057009D5E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 284d1601746254b2e10fdfe042e5882e94ca1bd9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046352"
---
# <span data-ttu-id="001e9-101">Get-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="001e9-101">Get-AzureEnvironment</span></span>

## <span data-ttu-id="001e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="001e9-102">SYNOPSIS</span></span>
<span data-ttu-id="001e9-103">Azure 환경을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="001e9-103">Gets Azure environments</span></span>

## <span data-ttu-id="001e9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="001e9-104">SYNTAX</span></span>

```
Get-AzureEnvironment [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="001e9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="001e9-105">DESCRIPTION</span></span>
<span data-ttu-id="001e9-106">**Get AzureEnvironment** Cmdlet은 Windows PowerShell에서 사용할 수 있는 Azure 환경을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="001e9-106">The **Get-AzureEnvironment** cmdlet gets the Azure environments that are available to Windows PowerShell.</span></span>

<span data-ttu-id="001e9-107">Azure 환경에서 글로벌 Azure 용 AzureCloud 및 중국의 21Vianet이 운영 하는 Azure 용 AzureChinaCloud와 같은 Microsoft Azure의 독립 배포입니다.</span><span class="sxs-lookup"><span data-stu-id="001e9-107">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="001e9-108">Azure Pack 및 WAPack cmdlet을 사용 하 여 온-프레미스 Azure 환경을 만들 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="001e9-108">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="001e9-109">자세한 내용은 [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ()을 참조 하세요 https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="001e9-109">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

<span data-ttu-id="001e9-110">**Get-AzureEnvironment** Cmdlet은 Azure가 아닌 구독 데이터 파일에서 환경을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="001e9-110">The **Get-AzureEnvironment** cmdlet gets environments from your subscription data file, not from Azure.</span></span>
<span data-ttu-id="001e9-111">구독 데이터 파일이 오래 된 경우 **추가-AzureAccount** 또는 **import-module settingsfile** cmdlet을 실행 하 여 새로 고칩니다.</span><span class="sxs-lookup"><span data-stu-id="001e9-111">If the subscription data file is outdated, run the **Add-AzureAccount** or **Import-PublishSettingsFile** cmdlet to refresh it.</span></span>

<span data-ttu-id="001e9-112">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="001e9-112">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="001e9-113">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="001e9-113">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="001e9-114">예제의</span><span class="sxs-lookup"><span data-stu-id="001e9-114">EXAMPLES</span></span>

### <span data-ttu-id="001e9-115">예제 1: 모든 환경 가져오기</span><span class="sxs-lookup"><span data-stu-id="001e9-115">Example 1: Get all environments</span></span>
```
PS C:\> Get-AzureEnvironment

EnvironmentName               ServiceEndpoint               ResourceManagerEndpoint       PublishSettingsFileUrl
---------------               ---------------               -----------------------       ----------------------

AzureCloud                    https://management.core.wi... https://management.azure.com/ https://go.microsoft.com/fw... 
AzureChinaCloud               https://management.core.ch... https://not-supported-serv... https://go.microsoft.com/fw...
```

<span data-ttu-id="001e9-116">이 명령은 Windows PowerShell에서 사용할 수 있는 모든 환경을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="001e9-116">This command gets all environments that are available to Windows PowerShell.</span></span>

### <span data-ttu-id="001e9-117">예제 2: 이름으로 환경 가져오기</span><span class="sxs-lookup"><span data-stu-id="001e9-117">Example 2: Get an environment by name</span></span>
```
PS C:\> Get-AzureEnvironment -Name AzureCloud

Name                          : AzureCloud

PublishSettingsFileUrl        : https://go.microsoft.com/fwlink/?LinkID=301775

ServiceEndpoint               : https://management.core.windows.net/

ResourceManagerEndpoint       : https://management.azure.com/

ManagementPortalUrl           : https://go.microsoft.com/fwlink/?LinkId=254433

ActiveDirectoryEndpoint       : https://login.windows.net/

ActiveDirectoryCommonTenantId : common

StorageEndpointSuffix         : core.windows.net

StorageBlobEndpointFormat     : {0}://{1}.blob.core.windows.net/

StorageQueueEndpointFormat    : {0}://{1}.queue.core.windows.net/

StorageTableEndpointFormat    : {0}://{1}.table.core.windows.net/

GalleryEndpoint               : https://gallery.azure.com/
```

<span data-ttu-id="001e9-118">이 예제에서는 AzureCloud 환경을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="001e9-118">This example gets the AzureCloud environment.</span></span>

### <span data-ttu-id="001e9-119">예제 3: 모든 환경의 모든 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="001e9-119">Example 3: Get all properties of all environments</span></span>
```
PS C:\> Get-AzureEnvironment | ForEach-Object {Get-AzureEnvironment -Name $_.EnvironmentName}
```

<span data-ttu-id="001e9-120">이 명령은 모든 환경의 모든 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="001e9-120">This command gets all properties of all environments.</span></span>

<span data-ttu-id="001e9-121">이 명령은 **Get AzureEnvironment** cmdlet을 사용 하 여이 계정에 대 한 모든 Azure 환경을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="001e9-121">The command uses the **Get-AzureEnvironment** cmdlet to get all Azure environments for this account.</span></span>
<span data-ttu-id="001e9-122">그런 다음 **Foreach-개체** cmdlet을 사용 하 여 각 환경의 **Name** 매개 변수를 사용 하 여 **Get-azureenvironment** 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="001e9-122">Then, it uses the **Foreach-Object** cmdlet to run a **Get-AzureEnvironment** command with the **Name** parameter on each environment.</span></span>
<span data-ttu-id="001e9-123">**Name** 매개 변수 값은 각 환경의 environment **이름** 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="001e9-123">The value of the **Name** parameter is the **EnvironmentName** property of each environment.</span></span>

<span data-ttu-id="001e9-124">**Get-AzureEnvironment** 는 매개 변수 없이 환경의 선택 된 속성만 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="001e9-124">Without parameters, **Get-AzureEnvironment** gets only selected properties of an environment.</span></span>

## <span data-ttu-id="001e9-125">변수</span><span class="sxs-lookup"><span data-stu-id="001e9-125">PARAMETERS</span></span>

### <span data-ttu-id="001e9-126">-이름</span><span class="sxs-lookup"><span data-stu-id="001e9-126">-Name</span></span>
<span data-ttu-id="001e9-127">지정 된 환경만 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="001e9-127">Gets only the specified environment.</span></span>
<span data-ttu-id="001e9-128">환경 이름을 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="001e9-128">Type the environment name.</span></span>
<span data-ttu-id="001e9-129">매개 변수 값은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="001e9-129">The parameter value is case-sensitive.</span></span>
<span data-ttu-id="001e9-130">와일드 카드 문자는 허용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="001e9-130">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="001e9-131">-프로필</span><span class="sxs-lookup"><span data-stu-id="001e9-131">-Profile</span></span>
<span data-ttu-id="001e9-132">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="001e9-132">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="001e9-133">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="001e9-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="001e9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="001e9-134">CommonParameters</span></span>
<span data-ttu-id="001e9-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="001e9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="001e9-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="001e9-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="001e9-137">입력</span><span class="sxs-lookup"><span data-stu-id="001e9-137">INPUTS</span></span>

### <span data-ttu-id="001e9-138">않아야</span><span class="sxs-lookup"><span data-stu-id="001e9-138">None</span></span>
<span data-ttu-id="001e9-139">속성 이름으로이 cmdlet에 대 한 입력을 파이프로 지정할 수 있지만 값을 기준으로 하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="001e9-139">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="001e9-140">출력</span><span class="sxs-lookup"><span data-stu-id="001e9-140">OUTPUTS</span></span>

### <span data-ttu-id="001e9-141">PSCustomObject (Management)</span><span class="sxs-lookup"><span data-stu-id="001e9-141">System.Management.Automation.PSCustomObject</span></span>
<span data-ttu-id="001e9-142">기본적으로 **Get-AzureEnvironment** 는 사용자 지정 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="001e9-142">By default, **Get-AzureEnvironment** returns a custom object.</span></span>

### <span data-ttu-id="001e9-143">WindowsAzure. 유틸리티. 공용 WindowsAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="001e9-143">Microsoft.WindowsAzure.Commands.Utilities.Common.WindowsAzureEnvironment</span></span>
<span data-ttu-id="001e9-144">**Name** 매개 변수를 사용 하 여 **가져오기-azureenvironment** 를 실행 하는 경우 **windowsazureenvironment** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="001e9-144">When you run **Get-AzureEnvironment** with the **Name** parameter, it returns a  **WindowsAzureEnvironment** object.</span></span>

## <span data-ttu-id="001e9-145">상속자</span><span class="sxs-lookup"><span data-stu-id="001e9-145">NOTES</span></span>

## <span data-ttu-id="001e9-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="001e9-146">RELATED LINKS</span></span>

[<span data-ttu-id="001e9-147">추가-AzureAccount</span><span class="sxs-lookup"><span data-stu-id="001e9-147">Add-AzureAccount</span></span>](./Add-AzureAccount.md)

[<span data-ttu-id="001e9-148">-AzureEnvironment 추가</span><span class="sxs-lookup"><span data-stu-id="001e9-148">Add-AzureEnvironment</span></span>](./Add-AzureEnvironment.md)

[<span data-ttu-id="001e9-149">Get-Azure도움말 파일</span><span class="sxs-lookup"><span data-stu-id="001e9-149">Get-AzurePublishSettingsFile</span></span>](./Get-AzurePublishSettingsFile.md)

[<span data-ttu-id="001e9-150">가져오기-Azure# settingsfile</span><span class="sxs-lookup"><span data-stu-id="001e9-150">Import-AzurePublishSettingsFile</span></span>](./Import-AzurePublishSettingsFile.md)

[<span data-ttu-id="001e9-151">-AzureEnvironment 제거</span><span class="sxs-lookup"><span data-stu-id="001e9-151">Remove-AzureEnvironment</span></span>](./Remove-AzureEnvironment.md)

[<span data-ttu-id="001e9-152">Set AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="001e9-152">Set-AzureEnvironment</span></span>](./Set-AzureEnvironment.md)


