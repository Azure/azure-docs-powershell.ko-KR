---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 1094497D-2CBE-41DF-9ED1-8E7D3F14B05A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 82bd806d35f36a07958f2bdeeeda42853cd453b9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045967"
---
# <span data-ttu-id="a6618-101">Set-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="a6618-101">Set-AzureEnvironment</span></span>

## <span data-ttu-id="a6618-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6618-102">SYNOPSIS</span></span>
<span data-ttu-id="a6618-103">Azure 환경의 속성을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6618-103">Changes the properties of an Azure environment.</span></span>

## <span data-ttu-id="a6618-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a6618-104">SYNTAX</span></span>

```
Set-AzureEnvironment -Name <String> [-PublishSettingsFileUrl <String>] [-ServiceEndpoint <String>]
 [-ManagementPortalUrl <String>] [-StorageEndpoint <String>] [-ActiveDirectoryEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-GalleryEndpoint <String>]
 [-ActiveDirectoryServiceEndpointResourceId <String>] [-GraphEndpoint <String>]
 [-AzureKeyVaultDnsSuffix <String>] [-AzureKeyVaultServiceEndpointResourceId <String>]
 [-TrafficManagerDnsSuffix <String>] [-SqlDatabaseDnsSuffix <String>] [-EnableAdfsAuthentication]
 [-AdTenant <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a6618-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a6618-105">DESCRIPTION</span></span>
<span data-ttu-id="a6618-106">**Set AzureEnvironment** Cmdlet은 Azure 환경의 속성을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6618-106">The **Set-AzureEnvironment** cmdlet changes the properties of an Azure environment.</span></span>
<span data-ttu-id="a6618-107">새 속성 값을 사용 하 여 환경을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6618-107">It returns an object that represents the environment with its new property values.</span></span>
<span data-ttu-id="a6618-108">**Name** 매개 변수를 사용 하 여 환경과 다른 매개 변수를 식별 하 여 속성 값을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6618-108">Use the **Name** parameter to identify the environment and the other parameters to change property values.</span></span>
<span data-ttu-id="a6618-109">**Set AzureEnvironment** 를 사용 하 여 Azure 환경의 이름을 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a6618-109">You cannot use **Set-AzureEnvironment** to change the name of an Azure environment.</span></span>

<span data-ttu-id="a6618-110">Azure 환경에서 글로벌 Azure 용 AzureCloud 및 중국의 21Vianet이 운영 하는 Azure 용 AzureChinaCloud와 같은 Microsoft Azure의 독립 배포입니다.</span><span class="sxs-lookup"><span data-stu-id="a6618-110">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="a6618-111">Azure Pack 및 WAPack cmdlet을 사용 하 여 온-프레미스 Azure 환경을 만들 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a6618-111">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="a6618-112">자세한 내용은 [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) ()을 참조 하세요 https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="a6618-112">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

<span data-ttu-id="a6618-113">참고: AzureCloud 또는 AzureChinaCloud 환경의 속성은 변경 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="a6618-113">NOTE:  Do not change the properties of the AzureCloud or AzureChinaCloud environments.</span></span>
<span data-ttu-id="a6618-114">이 cmdlet을 사용 하 여 만드는 개인 환경의 값을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6618-114">Use this cmdlet to change the values of private environments that you create.</span></span>

## <span data-ttu-id="a6618-115">예제의</span><span class="sxs-lookup"><span data-stu-id="a6618-115">EXAMPLES</span></span>

### <span data-ttu-id="a6618-116">예제 1: 환경 속성 변경</span><span class="sxs-lookup"><span data-stu-id="a6618-116">Example 1: Change environment properties</span></span>
```
PS C:\> Set-AzureEnvironment -Name ContosoEnv -PublishSettingsFileUrl "https://contoso.com" -StorageEndpoint "contoso.com"
```

<span data-ttu-id="a6618-117">이 명령은 ContosoEnv 환경의 **PublishSettingsFileUrl** 및 **storageendpoint** 속성의 값을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6618-117">This command changes the values of the **PublishSettingsFileUrl** and **StorageEndpoint** properties of the ContosoEnv environment.</span></span>

## <span data-ttu-id="a6618-118">변수</span><span class="sxs-lookup"><span data-stu-id="a6618-118">PARAMETERS</span></span>

### <span data-ttu-id="a6618-119">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="a6618-119">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="a6618-120">Azure Active Directory 인증의 끝점을 지정 된 값으로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6618-120">Changes the endpoint for Azure Active Directory authentication to the specified value.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AdEndpointUrl, ActiveDirectory, ActiveDirectoryAuthority

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6618-121">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="a6618-121">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="a6618-122">Azure Active Directory에서 액세스를 관리 하는 관리 API의 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6618-122">Specifies the resource ID of a management API whose access is managed by Azure Active Directory.</span></span>

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

### <span data-ttu-id="a6618-123">-AdTenant 넌 트</span><span class="sxs-lookup"><span data-stu-id="a6618-123">-AdTenant</span></span>
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

### <span data-ttu-id="a6618-124">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="a6618-124">-AzureKeyVaultDnsSuffix</span></span>
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

### <span data-ttu-id="a6618-125">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="a6618-125">-AzureKeyVaultServiceEndpointResourceId</span></span>
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

### <span data-ttu-id="a6618-126">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="a6618-126">-EnableAdfsAuthentication</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: OnPremise

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6618-127">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="a6618-127">-GalleryEndpoint</span></span>
<span data-ttu-id="a6618-128">Azure Resource Manager 갤러리의 끝점을 지정 된 값으로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6618-128">Changes the endpoint for the Azure Resource Manager gallery to the specified value.</span></span>
<span data-ttu-id="a6618-129">갤러리 끝점은 리소스 그룹 갤러리 서식 파일의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="a6618-129">The gallery endpoint is the location for resource group gallery templates.</span></span>
<span data-ttu-id="a6618-130">Azure 리소스 그룹 및 갤러리 서식 파일에 대 한 자세한 내용은 Get-help에 대 한 도움말 항목 [AzureResourceGroupGalleryTemplate](https://go.microsoft.com/fwlink/?LinkID=393052)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a6618-130">For more information about Azure resource groups and gallery templates, see the help topic for [Get-AzureResourceGroupGalleryTemplate](https://go.microsoft.com/fwlink/?LinkID=393052).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Gallery, GalleryUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6618-131">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="a6618-131">-GraphEndpoint</span></span>
```yaml
Type: String
Parameter Sets: (All)
Aliases: Graph, GraphUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6618-132">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="a6618-132">-ManagementPortalUrl</span></span>
<span data-ttu-id="a6618-133">Azure 관리 포털의 URL을 지정 된 값으로 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6618-133">Changes the URL of the Azure Management Portal to the specified value.</span></span>

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

### <span data-ttu-id="a6618-134">-이름</span><span class="sxs-lookup"><span data-stu-id="a6618-134">-Name</span></span>
<span data-ttu-id="a6618-135">변경 되는 환경을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6618-135">Identifies the environment that is being changed.</span></span>
<span data-ttu-id="a6618-136">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="a6618-136">This parameter is required.</span></span>
<span data-ttu-id="a6618-137">매개 변수 값은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6618-137">The parameter value is case-sensitive.</span></span>
<span data-ttu-id="a6618-138">와일드 카드 문자는 허용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a6618-138">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="a6618-139">-프로필</span><span class="sxs-lookup"><span data-stu-id="a6618-139">-Profile</span></span>
<span data-ttu-id="a6618-140">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6618-140">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="a6618-141">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="a6618-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a6618-142">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="a6618-142">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="a6618-143">지정 된 환경의 게시 설정 파일에 대 한 URL을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6618-143">Changes the URL for publish settings files in the specified environment.</span></span>
<span data-ttu-id="a6618-144">Azure 게시 설정 파일은 Windows PowerShell이 사용자를 대신해 Azure 계정에 로그인 하는 데 사용할 수 있는 계정 및 관리 인증서에 대 한 정보를 포함 하는 XML 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="a6618-144">An Azure publish settings file is an XML file that contains information about your account and a management certificate that allows Windows PowerShell to sign into your Azure account on your behalf.</span></span>

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

### <span data-ttu-id="a6618-145">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a6618-145">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="a6618-146">계정과 연결 된 리소스 그룹에 대 한 데이터를 포함 하 여 Azure Resource Manager 데이터의 끝점을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6618-146">Changes the endpoint for Azure Resource Manager data, including data about resource groups associated with the account.</span></span>
<span data-ttu-id="a6618-147">Azure 리소스 관리자에 대 한 자세한 내용은 [Azure Resource Manager cmdlet](https://go.microsoft.com/fwlink/?LinkID=394765)  ( https://go.microsoft.com/fwlink/?LinkID=394765) 및 [Windows PowerShell을 사용 하 여 리소스 관리자](https://go.microsoft.com/fwlink/?LinkID=394767)  ()를 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=394767) .</span><span class="sxs-lookup"><span data-stu-id="a6618-147">For more information about Azure Resource Manager, see [Azure Resource Manager Cmdlets](https://go.microsoft.com/fwlink/?LinkID=394765)  (https://go.microsoft.com/fwlink/?LinkID=394765) and [Using Windows PowerShell with Resource Manager](https://go.microsoft.com/fwlink/?LinkID=394767)  (https://go.microsoft.com/fwlink/?LinkID=394767).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceManager, ResourceManagerUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6618-148">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="a6618-148">-ServiceEndpoint</span></span>
<span data-ttu-id="a6618-149">지정 된 환경에서 Azure service 끝점의 URL을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6618-149">Changes the URL of the Azure service endpoint in the specified environment.</span></span>
<span data-ttu-id="a6618-150">Azure 서비스 끝점은 전역 Azure platform, 중국에서 21Vianet에서 운영 하는 Azure 또는 사설 Azure 설치를 통해 응용 프로그램을 관리 하는지 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6618-150">The Azure service endpoint determines whether your application is managed by the global Azure platform, Azure operated by 21Vianet in China, or a private Azure installation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceManagement, ServiceManagementUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6618-151">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="a6618-151">-SqlDatabaseDnsSuffix</span></span>
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

### <span data-ttu-id="a6618-152">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="a6618-152">-StorageEndpoint</span></span>
<span data-ttu-id="a6618-153">지정 된 환경에서 저장소 서비스의 기본 끝점을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6618-153">Changes the default endpoint of storage services in the specified environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageEndpointSuffix

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6618-154">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="a6618-154">-TrafficManagerDnsSuffix</span></span>
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

### <span data-ttu-id="a6618-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6618-155">CommonParameters</span></span>
<span data-ttu-id="a6618-156">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6618-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6618-157">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6618-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6618-158">입력</span><span class="sxs-lookup"><span data-stu-id="a6618-158">INPUTS</span></span>

### <span data-ttu-id="a6618-159">않아야</span><span class="sxs-lookup"><span data-stu-id="a6618-159">None</span></span>
<span data-ttu-id="a6618-160">속성 이름으로이 cmdlet에 대 한 입력을 파이프로 지정할 수 있지만 값을 기준으로 하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a6618-160">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="a6618-161">출력</span><span class="sxs-lookup"><span data-stu-id="a6618-161">OUTPUTS</span></span>

### <span data-ttu-id="a6618-162">WindowsAzure. 유틸리티. 공용 WindowsAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="a6618-162">Microsoft.WindowsAzure.Commands.Utilities.Common.WindowsAzureEnvironment</span></span>

## <span data-ttu-id="a6618-163">상속자</span><span class="sxs-lookup"><span data-stu-id="a6618-163">NOTES</span></span>

## <span data-ttu-id="a6618-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a6618-164">RELATED LINKS</span></span>

[<span data-ttu-id="a6618-165">-AzureEnvironment 추가</span><span class="sxs-lookup"><span data-stu-id="a6618-165">Add-AzureEnvironment</span></span>](./Add-AzureEnvironment.md)

[<span data-ttu-id="a6618-166">가져오기-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="a6618-166">Get-AzureEnvironment</span></span>](./Get-AzureEnvironment.md)

[<span data-ttu-id="a6618-167">-AzureEnvironment 제거</span><span class="sxs-lookup"><span data-stu-id="a6618-167">Remove-AzureEnvironment</span></span>](./Remove-AzureEnvironment.md)


