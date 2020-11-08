---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 6C435518-06EA-41B7-9585-44107B026FF1
online version: ''
schema: 2.0.0
ms.openlocfilehash: b04ceff5c4c49fe0e03e1e2c3da94c118323d653
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045730"
---
# <span data-ttu-id="d4506-101">Add-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="d4506-101">Add-AzureEnvironment</span></span>

## <span data-ttu-id="d4506-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4506-102">SYNOPSIS</span></span>
<span data-ttu-id="d4506-103">Azure 환경을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d4506-103">Creates an Azure environment.</span></span>

## <span data-ttu-id="d4506-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d4506-104">SYNTAX</span></span>

```
Add-AzureEnvironment -Name <String> [-PublishSettingsFileUrl <String>] [-ServiceEndpoint <String>]
 [-ManagementPortalUrl <String>] [-StorageEndpoint <String>] [-ActiveDirectoryEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-GalleryEndpoint <String>]
 [-ActiveDirectoryServiceEndpointResourceId <String>] [-GraphEndpoint <String>]
 [-AzureKeyVaultDnsSuffix <String>] [-AzureKeyVaultServiceEndpointResourceId <String>]
 [-TrafficManagerDnsSuffix <String>] [-SqlDatabaseDnsSuffix <String>] [-EnableAdfsAuthentication]
 [-AdTenant <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d4506-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d4506-105">DESCRIPTION</span></span>
<span data-ttu-id="d4506-106">새 사용자 지정 Azure 계정 환경을 만들어 로밍 사용자 프로필에 저장 하는 **-azureenvironment** Cmdlet을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4506-106">The **Add-AzureEnvironment** cmdlet creates a new custom Azure account environment and saves it in your roaming user profile.</span></span>
<span data-ttu-id="d4506-107">Cmdlet은 새 환경을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4506-107">The cmdlet returns an object that represents the new environment.</span></span>
<span data-ttu-id="d4506-108">명령이 완료 되 면 Windows PowerShell에서 환경을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d4506-108">When the command completes, you can use the environment in Windows PowerShell.</span></span>

<span data-ttu-id="d4506-109">Azure 환경에서 글로벌 Azure 용 AzureCloud 및 중국의 21Vianet이 운영 하는 Azure 용 AzureChinaCloud와 같은 Microsoft Azure의 독립 배포입니다.</span><span class="sxs-lookup"><span data-stu-id="d4506-109">An Azure environment an independent deployment of Microsoft Azure, such as AzureCloud for global Azure and AzureChinaCloud for Azure operated by 21Vianet in China.</span></span>
<span data-ttu-id="d4506-110">Azure Pack 및 WAPack cmdlet을 사용 하 여 온-프레미스 Azure 환경을 만들 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d4506-110">You can also create on-premises Azure environments by using Azure Pack and the WAPack cmdlets.</span></span>
<span data-ttu-id="d4506-111">자세한 내용은 [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) ()을 참조 하세요 https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .</span><span class="sxs-lookup"><span data-stu-id="d4506-111">For more information, see [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) (https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx).</span></span>

<span data-ttu-id="d4506-112">이 cmdlet의 **Name** 매개 변수만 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="d4506-112">Only the **Name** parameter of this cmdlet is mandatory.</span></span>
<span data-ttu-id="d4506-113">매개 변수를 생략 하면 해당 값이 null ($Null)이 되 고 해당 끝점을 사용 하는 서비스가 올바르게 작동 하지 않을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d4506-113">If you omit a parameter, its value is null ($Null), and the service that uses that endpoint might not function properly.</span></span>
<span data-ttu-id="d4506-114">환경 속성의 값을 추가 하거나 변경 하려면 **Set-AzureEnvironment** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4506-114">To add or change the value of an environment property, use the **Set-AzureEnvironment** cmdlet.</span></span>

<span data-ttu-id="d4506-115">참고: 환경을 변경 하면 계정이 실패할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d4506-115">NOTE: Changing your environment can cause your account to fail.</span></span>
<span data-ttu-id="d4506-116">일반적으로 테스트 또는 문제 해결을 위한 환경만 추가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d4506-116">Typically, environments are added only for testing or troubleshooting.</span></span>

<span data-ttu-id="d4506-117">이 항목에서는 0.8.10 버전의 Microsoft Azure PowerShell 모듈에 대 한 cmdlet에 대해 설명 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4506-117">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="d4506-118">사용 중인 모듈 버전을 Azure PowerShell 콘솔에 가져오려면 다음을 입력 `(Get-Module -Name Azure).Version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4506-118">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

## <span data-ttu-id="d4506-119">예제의</span><span class="sxs-lookup"><span data-stu-id="d4506-119">EXAMPLES</span></span>

### <span data-ttu-id="d4506-120">예제 1: Azure 환경 추가</span><span class="sxs-lookup"><span data-stu-id="d4506-120">Example 1: Add an Azure environment</span></span>
```
PS C:\> Add-AzureEnvironment -Name ContosoEnv -PublishSettingsFileUrl https://contoso.com/fwlink/?LinkID=101 -ServiceEndpoint https://contoso.com/fwlink/?LinkID=102

Name                          : ContosoEnv

PublishSettingsFileUrl        : https://contoso.com/fwlink/?LinkID=101

ServiceEndpoint               : https://contoso.com/fwlink/?LinkID=102

ResourceManagerEndpoint       : 

ManagementPortalUrl           : 

ActiveDirectoryEndpoint       : 

ActiveDirectoryCommonTenantId : 

StorageEndpointSuffix         : 

StorageBlobEndpointFormat     : 

StorageQueueEndpointFormat    : 

StorageTableEndpointFormat    : 

GalleryEndpoint               :
```

<span data-ttu-id="d4506-121">이 명령은 ContosoEnv Azure 환경을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d4506-121">This command creates the ContosoEnv Azure environment.</span></span>

## <span data-ttu-id="d4506-122">변수</span><span class="sxs-lookup"><span data-stu-id="d4506-122">PARAMETERS</span></span>

### <span data-ttu-id="d4506-123">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="d4506-123">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="d4506-124">새 환경에서 Azure Active Directory 인증에 대 한 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4506-124">Specifies the endpoint for Azure Active Directory authentication in the new environment.</span></span>

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

### <span data-ttu-id="d4506-125">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="d4506-125">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="d4506-126">Azure Active Directory에서 액세스를 관리 하는 관리 API의 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4506-126">Specifies the resource ID of a management API whose access is managed by Azure Active Directory.</span></span>

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

### <span data-ttu-id="d4506-127">-AdTenant 넌 트</span><span class="sxs-lookup"><span data-stu-id="d4506-127">-AdTenant</span></span>
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

### <span data-ttu-id="d4506-128">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="d4506-128">-AzureKeyVaultDnsSuffix</span></span>
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

### <span data-ttu-id="d4506-129">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="d4506-129">-AzureKeyVaultServiceEndpointResourceId</span></span>
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

### <span data-ttu-id="d4506-130">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="d4506-130">-EnableAdfsAuthentication</span></span>
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

### <span data-ttu-id="d4506-131">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="d4506-131">-GalleryEndpoint</span></span>
<span data-ttu-id="d4506-132">리소스 그룹 갤러리 서식 파일을 저장 하는 Azure Resource Manager 갤러리의 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4506-132">Specifies the endpoint for the Azure Resource Manager gallery, which stores resource group gallery templates.</span></span>
<span data-ttu-id="d4506-133">Azure 리소스 그룹 및 갤러리 서식 파일에 대 한 자세한 내용은 Get-help에 대 한 도움말 항목 AzureResourceGroupGalleryTemplate을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=393052 .</span><span class="sxs-lookup"><span data-stu-id="d4506-133">For more information about Azure resource groups and gallery templates, see the help topic for Get-AzureResourceGroupGalleryTemplatehttps://go.microsoft.com/fwlink/?LinkID=393052.</span></span>

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

### <span data-ttu-id="d4506-134">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="d4506-134">-GraphEndpoint</span></span>
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

### <span data-ttu-id="d4506-135">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="d4506-135">-ManagementPortalUrl</span></span>
<span data-ttu-id="d4506-136">새 환경에서 Azure 관리 포털의 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4506-136">Specifies the URL of the Azure Management Portal in the new environment.</span></span>

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

### <span data-ttu-id="d4506-137">-이름</span><span class="sxs-lookup"><span data-stu-id="d4506-137">-Name</span></span>
<span data-ttu-id="d4506-138">환경의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4506-138">Specifies a name for the environment.</span></span>
<span data-ttu-id="d4506-139">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="d4506-139">This parameter is required.</span></span>
<span data-ttu-id="d4506-140">기본 환경, AzureCloud 및 AzureChinaCloud의 이름을 사용 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="d4506-140">Do not use the names of the default environments, AzureCloud and AzureChinaCloud.</span></span>

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

### <span data-ttu-id="d4506-141">-프로필</span><span class="sxs-lookup"><span data-stu-id="d4506-141">-Profile</span></span>
<span data-ttu-id="d4506-142">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4506-142">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="d4506-143">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="d4506-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d4506-144">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="d4506-144">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="d4506-145">계정에 대 한 게시 설정 파일의 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4506-145">Specifies the URL of the publish settings files for your account.</span></span>
<span data-ttu-id="d4506-146">Azure 게시 설정 파일은 Windows PowerShell이 사용자를 대신해 Azure 계정에 로그인 하는 데 사용할 수 있는 계정 및 관리 인증서에 대 한 정보를 포함 하는 XML 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="d4506-146">An Azure publish settings file is an XML file that contains information about your account and a management certificate that allows Windows PowerShell to sign into your Azure account on your behalf.</span></span>

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

### <span data-ttu-id="d4506-147">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d4506-147">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="d4506-148">계정과 연결 된 리소스 그룹에 대 한 데이터를 포함 하 여 Azure Resource Manager 데이터에 대 한 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4506-148">Specifies the endpoint for Azure Resource Manager data, including data about resource groups associated with the account.</span></span>
<span data-ttu-id="d4506-149">Azure 리소스 관리자에 대 한 자세한 내용은 [Azure Resource Manager cmdlet](https://go.microsoft.com/fwlink/?LinkID=394765)  ( https://go.microsoft.com/fwlink/?LinkID=394765) 및 [Windows PowerShell을 사용 하 여 리소스 관리자](https://go.microsoft.com/fwlink/?LinkID=394767)  ()를 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=394767) .</span><span class="sxs-lookup"><span data-stu-id="d4506-149">For more information about Azure Resource Manager, see [Azure Resource Manager Cmdlets](https://go.microsoft.com/fwlink/?LinkID=394765)  (https://go.microsoft.com/fwlink/?LinkID=394765) and [Using Windows PowerShell with Resource Manager](https://go.microsoft.com/fwlink/?LinkID=394767)  (https://go.microsoft.com/fwlink/?LinkID=394767).</span></span>

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

### <span data-ttu-id="d4506-150">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="d4506-150">-ServiceEndpoint</span></span>
<span data-ttu-id="d4506-151">Azure 서비스 끝점의 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4506-151">Specifies the URL of the Azure service endpoint.</span></span>
<span data-ttu-id="d4506-152">Azure 서비스 끝점은 전역 Azure platform, 중국에서 21Vianet에서 운영 하는 Azure 또는 사설 Azure 설치를 통해 응용 프로그램을 관리 하는지 여부를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4506-152">The Azure service endpoint determines whether your application is managed by the global Azure platform, Azure operated by 21Vianet in China, or a private Azure installation.</span></span>

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

### <span data-ttu-id="d4506-153">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="d4506-153">-SqlDatabaseDnsSuffix</span></span>
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

### <span data-ttu-id="d4506-154">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="d4506-154">-StorageEndpoint</span></span>
<span data-ttu-id="d4506-155">새 환경에서 저장소 서비스의 기본 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4506-155">Specifies the default endpoint of storage services in the new environment.</span></span>

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

### <span data-ttu-id="d4506-156">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="d4506-156">-TrafficManagerDnsSuffix</span></span>
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

### <span data-ttu-id="d4506-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4506-157">CommonParameters</span></span>
<span data-ttu-id="d4506-158">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4506-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4506-159">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4506-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4506-160">입력</span><span class="sxs-lookup"><span data-stu-id="d4506-160">INPUTS</span></span>

### <span data-ttu-id="d4506-161">않아야</span><span class="sxs-lookup"><span data-stu-id="d4506-161">None</span></span>
<span data-ttu-id="d4506-162">속성 이름으로이 cmdlet에 대 한 입력을 파이프로 지정할 수 있지만 값을 기준으로 하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d4506-162">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="d4506-163">출력</span><span class="sxs-lookup"><span data-stu-id="d4506-163">OUTPUTS</span></span>

### <span data-ttu-id="d4506-164">WindowsAzure. 유틸리티. 공용 WindowsAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="d4506-164">Microsoft.WindowsAzure.Commands.Utilities.Common.WindowsAzureEnvironment</span></span>

## <span data-ttu-id="d4506-165">상속자</span><span class="sxs-lookup"><span data-stu-id="d4506-165">NOTES</span></span>

## <span data-ttu-id="d4506-166">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d4506-166">RELATED LINKS</span></span>

[<span data-ttu-id="d4506-167">가져오기-AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="d4506-167">Get-AzureEnvironment</span></span>](./Get-AzureEnvironment.md)

[<span data-ttu-id="d4506-168">-AzureEnvironment 제거</span><span class="sxs-lookup"><span data-stu-id="d4506-168">Remove-AzureEnvironment</span></span>](./Remove-AzureEnvironment.md)

[<span data-ttu-id="d4506-169">Set AzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="d4506-169">Set-AzureEnvironment</span></span>](./Set-AzureEnvironment.md)


