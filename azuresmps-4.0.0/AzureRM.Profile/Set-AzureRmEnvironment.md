---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 37e8952ab7337ae69e5c23ed4ab09e651acfac8c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523171"
---
# <span data-ttu-id="625a6-101">Set-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="625a6-101">Set-AzureRmEnvironment</span></span>

## <span data-ttu-id="625a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="625a6-102">SYNOPSIS</span></span>
<span data-ttu-id="625a6-103">Azure 환경에 대 한 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="625a6-103">Sets properties for an Azure environment.</span></span>

## <span data-ttu-id="625a6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="625a6-104">SYNTAX</span></span>

```
Set-AzureRmEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
 [[-ManagementPortalUrl] <String>] [[-StorageEndpoint] <String>] [[-ActiveDirectoryEndpoint] <String>]
 [[-ResourceManagerEndpoint] <String>] [[-GalleryEndpoint] <String>]
 [[-ActiveDirectoryServiceEndpointResourceId] <String>] [[-GraphEndpoint] <String>]
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-TrafficManagerDnsSuffix] <String>] [[-SqlDatabaseDnsSuffix] <String>]
 [[-AzureDataLakeStoreFileSystemEndpointSuffix] <String>]
 [[-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix] <String>] [-EnableAdfsAuthentication]
 [[-AdTenant] <String>] [[-GraphAudience] <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="625a6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="625a6-105">DESCRIPTION</span></span>
<span data-ttu-id="625a6-106">Set-AzureRMEnvironment cmdlet은 Azure의 인스턴스에 연결 하기 위한 끝점 및 메타 데이터를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="625a6-106">The Set-AzureRMEnvironment cmdlet sets endpoints and metadata for connecting to an instance of Azure.</span></span>

## <span data-ttu-id="625a6-107">예제의</span><span class="sxs-lookup"><span data-stu-id="625a6-107">EXAMPLES</span></span>

### <span data-ttu-id="625a6-108">예제 1: 새 환경 만들기 및 수정</span><span class="sxs-lookup"><span data-stu-id="625a6-108">Example 1: Creating and modifying a new environment</span></span>
```
PS C:\> Add-AzureRmEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint TestADEndpoint `
        -ActiveDirectoryServiceEndpointResourceId TestADApplicationId `
        -ResourceManagerEndpoint TestRMEndpoint `
        -GalleryEndpoint TestGalleryEndpoint `
        -GraphEndpoint TestGraphEndpoint

Name                                              : TestEnvironment
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : TestADApplicationId
AdTenant                                          :
GalleryUrl                                        : TestGalleryEndpoint
ManagementPortalUrl                               :
ServiceManagementUrl                              : 
PublishSettingsFileUrl                            :
ResourceManagerUrl                                : TestRMEndpoint
SqlDatabaseDnsSuffix                              :
StorageEndpointSuffix                             :
ActiveDirectoryAuthority                          : TestADEndpoint
GraphUrl                                          : TestGraphEndpoint
GraphEndpointResourceId                           :
TrafficManagerDnsSuffix                           :
AzureKeyVaultDnsSuffix                            :
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            :

PS C:\> Set-AzureRmEnvironment -Name TestEnvironment
        -ActiveDirectoryEndpoint NewTestADEndpoint
        -GraphEndpoint NewTestGraphEndpoint

Name                                              : TestEnvironment
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : TestADApplicationId
AdTenant                                          :
GalleryUrl                                        : TestGalleryEndpoint
ManagementPortalUrl                               :
ServiceManagementUrl                              : 
PublishSettingsFileUrl                            :
ResourceManagerUrl                                : TestRMEndpoint
SqlDatabaseDnsSuffix                              :
StorageEndpointSuffix                             :
ActiveDirectoryAuthority                          : NewTestADEndpoint
GraphUrl                                          : NewTestGraphEndpoint
GraphEndpointResourceId                           :
TrafficManagerDnsSuffix                           :
AzureKeyVaultDnsSuffix                            :
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            :
```

<span data-ttu-id="625a6-109">이 예제에서는 Add-AzureRmEnvironment를 사용 하 여 샘플 끝점을 사용 하 여 새 Azure 환경을 만든 다음, cmdlet 집합-AzureRmEnvironment를 사용 하 여 생성 된 환경의 ActiveDirectoryEndpoint 및 GraphEndpoint 특성 값을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="625a6-109">In this example we are creating a new Azure environment with sample endpoints using Add-AzureRmEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzureRmEnvironment.</span></span>

## <span data-ttu-id="625a6-110">변수</span><span class="sxs-lookup"><span data-stu-id="625a6-110">PARAMETERS</span></span>

### <span data-ttu-id="625a6-111">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="625a6-111">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="625a6-112">Azure Active Directory 인증에 대 한 기본 인증 기관을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="625a6-112">Specifies the base authority for Azure Active Directory authentication.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AdEndpointUrl, ActiveDirectory, ActiveDirectoryAuthority

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="625a6-113">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="625a6-113">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="625a6-114">Azure Resource Manager 또는 RDFE (서비스 관리) 끝점에 대 한 요청을 인증 하는 토큰에 대 한 대상 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="625a6-114">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="625a6-115">-AdTenant 넌 트</span><span class="sxs-lookup"><span data-stu-id="625a6-115">-AdTenant</span></span>
<span data-ttu-id="625a6-116">기본 Active Directory 테 넌 트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="625a6-116">Specifies the default Active Directory tenant.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 17
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="625a6-117">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="625a6-117">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="625a6-118">Azure Data Lake Analytics 작업 및 카탈로그 서비스의 Dns 접미사</span><span class="sxs-lookup"><span data-stu-id="625a6-118">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="625a6-119">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="625a6-119">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="625a6-120">Azure Data Lake Store 파일 시스템의 Dns 접미사.</span><span class="sxs-lookup"><span data-stu-id="625a6-120">Dns Suffix of Azure Data Lake Store FileSystem.</span></span>
<span data-ttu-id="625a6-121">예: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="625a6-121">Example: azuredatalake.net</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 14
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="625a6-122">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="625a6-122">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="625a6-123">키 보관소 서비스에 대 한 도메인 이름 접미사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="625a6-123">Specifies the domain name suffix for Key Vault services.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="625a6-124">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="625a6-124">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="625a6-125">키 자격 증명 모음 서비스에 대 한 요청을 승인 하는 액세스 토큰에 대 한 대상을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="625a6-125">Specifies the audience for access tokens that authorize requests for Key Vault services.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="625a6-126">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="625a6-126">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="625a6-127">ADFS (Active Directory Federation Services) 온-프레미스 인증이 허용 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="625a6-127">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: OnPremise

Required: False
Position: 16
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="625a6-128">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="625a6-128">-GalleryEndpoint</span></span>
<span data-ttu-id="625a6-129">배포 서식 파일의 Azure Resource Manager 갤러리에 대 한 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="625a6-129">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Gallery, GalleryUrl

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="625a6-130">-GraphAudience 대상</span><span class="sxs-lookup"><span data-stu-id="625a6-130">-GraphAudience</span></span>
<span data-ttu-id="625a6-131">광고 그래프 끝점을 사용 하 여 인증 하는 토큰에 대 한 대상 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="625a6-131">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: GraphEndpointResourceId, GraphResourceId

Required: False
Position: 18
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="625a6-132">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="625a6-132">-GraphEndpoint</span></span>
<span data-ttu-id="625a6-133">그래프 (Active Directory 메타 데이터) 요청에 대 한 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="625a6-133">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Graph, GraphUrl

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="625a6-134">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="625a6-134">-ManagementPortalUrl</span></span>
<span data-ttu-id="625a6-135">관리 포털에 대 한 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="625a6-135">Specifies the URL for the Management Portal.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="625a6-136">-이름</span><span class="sxs-lookup"><span data-stu-id="625a6-136">-Name</span></span>
<span data-ttu-id="625a6-137">수정할 환경의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="625a6-137">Specifies the name of the environment to modify.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="625a6-138">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="625a6-138">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="625a6-139">Publishsettings 파일을 다운로드할 수 있는 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="625a6-139">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="625a6-140">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="625a6-140">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="625a6-141">Azure Resource Manager 요청에 대 한 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="625a6-141">Specifies the URL for Azure Resource Manager requests.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceManager, ResourceManagerUrl

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="625a6-142">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="625a6-142">-ServiceEndpoint</span></span>
<span data-ttu-id="625a6-143">RDFE (서비스 관리) 요청에 대 한 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="625a6-143">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceManagement, ServiceManagementUrl

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="625a6-144">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="625a6-144">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="625a6-145">Azure SQL 데이터베이스 서버의 도메인 이름 접미사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="625a6-145">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="625a6-146">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="625a6-146">-StorageEndpoint</span></span>
<span data-ttu-id="625a6-147">저장소 (blob, 테이블, 큐 및 파일) 액세스에 대 한 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="625a6-147">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageEndpointSuffix

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="625a6-148">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="625a6-148">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="625a6-149">Azure Traffic Manager 서비스에 대 한 도메인 이름 접미사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="625a6-149">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="625a6-150">-확인</span><span class="sxs-lookup"><span data-stu-id="625a6-150">-Confirm</span></span>
<span data-ttu-id="625a6-151">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="625a6-151">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="625a6-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="625a6-152">-WhatIf</span></span>
<span data-ttu-id="625a6-153">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="625a6-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="625a6-154">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="625a6-154">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="625a6-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="625a6-155">CommonParameters</span></span>
<span data-ttu-id="625a6-156">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="625a6-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="625a6-157">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="625a6-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="625a6-158">입력</span><span class="sxs-lookup"><span data-stu-id="625a6-158">INPUTS</span></span>

## <span data-ttu-id="625a6-159">출력</span><span class="sxs-lookup"><span data-stu-id="625a6-159">OUTPUTS</span></span>

### <span data-ttu-id="625a6-160">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="625a6-160">PSAzureEnvironment</span></span>

## <span data-ttu-id="625a6-161">상속자</span><span class="sxs-lookup"><span data-stu-id="625a6-161">NOTES</span></span>

## <span data-ttu-id="625a6-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="625a6-162">RELATED LINKS</span></span>

[<span data-ttu-id="625a6-163">추가-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="625a6-163">Add-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="625a6-164">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="625a6-164">Get-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="625a6-165">제거-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="625a6-165">Remove-AzureRMEnvironment</span></span>]()

