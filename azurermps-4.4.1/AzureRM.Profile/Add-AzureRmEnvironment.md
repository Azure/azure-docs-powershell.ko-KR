---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.profile
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Add-AzureRmEnvironment.md
ms.openlocfilehash: 510e191f29936b04e1d3e49b71ca1a6dfa160d20
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711256"
---
# <span data-ttu-id="819f4-101">Add-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="819f4-101">Add-AzureRmEnvironment</span></span>

## <span data-ttu-id="819f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="819f4-102">SYNOPSIS</span></span>
<span data-ttu-id="819f4-103">Azure Resource Manager 인스턴스에 대 한 끝점 및 메타 데이터를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="819f4-103">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="819f4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="819f4-104">SYNTAX</span></span>

### <span data-ttu-id="819f4-105">Name (기본값)</span><span class="sxs-lookup"><span data-stu-id="819f4-105">Name (Default)</span></span>
```
Add-AzureRmEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
 [[-ManagementPortalUrl] <String>] [[-StorageEndpoint] <String>] [[-ActiveDirectoryEndpoint] <String>]
 [[-ResourceManagerEndpoint] <String>] [[-GalleryEndpoint] <String>]
 [[-ActiveDirectoryServiceEndpointResourceId] <String>] [[-GraphEndpoint] <String>]
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-TrafficManagerDnsSuffix] <String>] [[-SqlDatabaseDnsSuffix] <String>]
 [[-AzureDataLakeStoreFileSystemEndpointSuffix] <String>]
 [[-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix] <String>] [-EnableAdfsAuthentication]
 [[-AdTenant] <String>] [[-GraphAudience] <String>] [[-DataLakeAudience] <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="819f4-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="819f4-106">ARMEndpoint</span></span>
```
Add-AzureRmEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-DataLakeAudience] <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="819f4-107">설명은</span><span class="sxs-lookup"><span data-stu-id="819f4-107">DESCRIPTION</span></span>
<span data-ttu-id="819f4-108">Add-AzureRmEnvironment cmdlet은 azure resource manager cmdlet이 Azure Resource Manager의 새 인스턴스와 연결할 수 있도록 끝점 및 메타 데이터를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="819f4-108">The Add-AzureRmEnvironment cmdlet adds endpoints and metadata to enable Azure Resource Manager cmdlets to connect with a new instance of Azure Resource Manager.</span></span>
<span data-ttu-id="819f4-109">기본 제공 환경 AzureCloud와 AzureChinaCloud는 Azure 리소스 관리자의 기존 공용 인스턴스를 대상으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="819f4-109">The built-in environments AzureCloud and AzureChinaCloud target existing public instances of Azure Resource Manager.</span></span>

## <span data-ttu-id="819f4-110">예제의</span><span class="sxs-lookup"><span data-stu-id="819f4-110">EXAMPLES</span></span>

### <span data-ttu-id="819f4-111">예제 1: 새 환경 만들기 및 수정</span><span class="sxs-lookup"><span data-stu-id="819f4-111">Example 1: Creating and modifying a new environment</span></span>
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

<span data-ttu-id="819f4-112">이 예제에서는 Add-AzureRmEnvironment를 사용 하 여 샘플 끝점을 사용 하 여 새 Azure 환경을 만든 다음, cmdlet 집합-AzureRmEnvironment를 사용 하 여 생성 된 환경의 ActiveDirectoryEndpoint 및 GraphEndpoint 특성 값을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="819f4-112">In this example we are creating a new Azure environment with sample endpoints using Add-AzureRmEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzureRmEnvironment.</span></span>

## <span data-ttu-id="819f4-113">변수</span><span class="sxs-lookup"><span data-stu-id="819f4-113">PARAMETERS</span></span>

### <span data-ttu-id="819f4-114">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="819f4-114">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="819f4-115">Azure Active Directory 인증에 대 한 기본 인증 기관을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="819f4-115">Specifies the base authority for Azure Active Directory authentication.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: AdEndpointUrl, ActiveDirectory, ActiveDirectoryAuthority

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="819f4-116">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="819f4-116">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="819f4-117">Azure Resource Manager 또는 RDFE (서비스 관리) 끝점에 대 한 요청을 인증 하는 토큰에 대 한 대상 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="819f4-117">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="819f4-118">-AdTenant 넌 트</span><span class="sxs-lookup"><span data-stu-id="819f4-118">-AdTenant</span></span>
<span data-ttu-id="819f4-119">기본 Active Directory 테 넌 트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="819f4-119">Specifies the default Active Directory tenant.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: 

Required: False
Position: 17
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="819f4-120">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="819f4-120">-ARMEndpoint</span></span>
<span data-ttu-id="819f4-121">Azure 리소스 관리자 끝점</span><span class="sxs-lookup"><span data-stu-id="819f4-121">The Azure Resource Manager endpoint</span></span>

```yaml
Type: System.String
Parameter Sets: ARMEndpoint
Aliases: ArmUrl

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="819f4-122">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="819f4-122">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="819f4-123">Azure Data Lake Analytics 작업 및 카탈로그 서비스의 Dns 접미사</span><span class="sxs-lookup"><span data-stu-id="819f4-123">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: 

Required: False
Position: 15
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="819f4-124">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="819f4-124">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="819f4-125">Azure Data Lake Store 파일 시스템의 Dns 접미사.</span><span class="sxs-lookup"><span data-stu-id="819f4-125">Dns Suffix of Azure Data Lake Store FileSystem.</span></span>
<span data-ttu-id="819f4-126">예: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="819f4-126">Example: azuredatalake.net</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: 

Required: False
Position: 14
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="819f4-127">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="819f4-127">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="819f4-128">키 보관소 서비스에 대 한 도메인 이름 접미사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="819f4-128">Specifies the domain name suffix for Key Vault services.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="819f4-129">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="819f4-129">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="819f4-130">키 자격 증명 모음 서비스에 대 한 요청을 승인 하는 액세스 토큰에 대 한 대상을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="819f4-130">Specifies the audience for access tokens that authorize requests for Key Vault services.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="819f4-131">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="819f4-131">-DataLakeAudience</span></span>
<span data-ttu-id="819f4-132">AD Data Lake 서비스 끝점을 사용 하 여 인증 하는 토큰의 대상 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="819f4-132">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DataLakeEndpointResourceId, DataLakeResourceId

Required: False
Position: 19
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="819f4-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="819f4-133">-DefaultProfile</span></span>
<span data-ttu-id="819f4-134">Azure와 통신 하는 데 사용 되는 credeetnails, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="819f4-134">The credeetnails, tenant and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="819f4-135">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="819f4-135">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="819f4-136">ADFS (Active Directory Federation Services) 온-프레미스 인증이 허용 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="819f4-136">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Name
Aliases: OnPremise

Required: False
Position: 16
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="819f4-137">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="819f4-137">-GalleryEndpoint</span></span>
<span data-ttu-id="819f4-138">배포 서식 파일의 Azure Resource Manager 갤러리에 대 한 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="819f4-138">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: Gallery, GalleryUrl

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="819f4-139">-GraphAudience 대상</span><span class="sxs-lookup"><span data-stu-id="819f4-139">-GraphAudience</span></span>
<span data-ttu-id="819f4-140">광고 그래프 끝점을 사용 하 여 인증 하는 토큰에 대 한 대상 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="819f4-140">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: GraphEndpointResourceId, GraphResourceId

Required: False
Position: 18
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="819f4-141">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="819f4-141">-GraphEndpoint</span></span>
<span data-ttu-id="819f4-142">그래프 (Active Directory 메타 데이터) 요청에 대 한 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="819f4-142">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: Graph, GraphUrl

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="819f4-143">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="819f4-143">-ManagementPortalUrl</span></span>
<span data-ttu-id="819f4-144">관리 포털에 대 한 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="819f4-144">Specifies the URL for the Management Portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="819f4-145">-이름</span><span class="sxs-lookup"><span data-stu-id="819f4-145">-Name</span></span>
<span data-ttu-id="819f4-146">추가할 환경의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="819f4-146">Specifies the name of the environment to add.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="819f4-147">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="819f4-147">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="819f4-148">Publishsettings 파일을 다운로드할 수 있는 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="819f4-148">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="819f4-149">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="819f4-149">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="819f4-150">Azure Resource Manager 요청에 대 한 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="819f4-150">Specifies the URL for Azure Resource Manager requests.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: ResourceManager, ResourceManagerUrl

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="819f4-151">-범위</span><span class="sxs-lookup"><span data-stu-id="819f4-151">-Scope</span></span>
<span data-ttu-id="819f4-152">컨텍스트 변경의 범위 (예: 변경 내용이 현재 프로세스에만 적용 되는지 또는이 사용자가 시작한 모든 세션)를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="819f4-152">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases: 
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="819f4-153">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="819f4-153">-ServiceEndpoint</span></span>
<span data-ttu-id="819f4-154">RDFE (서비스 관리) 요청에 대 한 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="819f4-154">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: ServiceManagement, ServiceManagementUrl

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="819f4-155">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="819f4-155">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="819f4-156">Azure SQL 데이터베이스 서버의 도메인 이름 접미사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="819f4-156">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: 

Required: False
Position: 13
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="819f4-157">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="819f4-157">-StorageEndpoint</span></span>
<span data-ttu-id="819f4-158">저장소 (blob, 테이블, 큐 및 파일) 액세스에 대 한 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="819f4-158">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageEndpointSuffix

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="819f4-159">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="819f4-159">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="819f4-160">Azure Traffic Manager 서비스에 대 한 도메인 이름 접미사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="819f4-160">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

```yaml
Type: System.String
Parameter Sets: Name
Aliases: 

Required: False
Position: 12
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="819f4-161">-확인</span><span class="sxs-lookup"><span data-stu-id="819f4-161">-Confirm</span></span>
<span data-ttu-id="819f4-162">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="819f4-162">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="819f4-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="819f4-163">-WhatIf</span></span>
<span data-ttu-id="819f4-164">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="819f4-164">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="819f4-165">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="819f4-165">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="819f4-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="819f4-166">CommonParameters</span></span>
<span data-ttu-id="819f4-167">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="819f4-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="819f4-168">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="819f4-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="819f4-169">입력</span><span class="sxs-lookup"><span data-stu-id="819f4-169">INPUTS</span></span>

## <span data-ttu-id="819f4-170">출력</span><span class="sxs-lookup"><span data-stu-id="819f4-170">OUTPUTS</span></span>

### <span data-ttu-id="819f4-171">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="819f4-171">PSAzureEnvironment</span></span>
<span data-ttu-id="819f4-172">이 cmdlet은 Azure 인스턴스와 통신 하는 데 필요한 끝점 및 메타 데이터 집합을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="819f4-172">This cmdlet returns the set of endpoints and metadata needed to communicate with an instance of Azure.</span></span>

## <span data-ttu-id="819f4-173">상속자</span><span class="sxs-lookup"><span data-stu-id="819f4-173">NOTES</span></span>

## <span data-ttu-id="819f4-174">관련 링크</span><span class="sxs-lookup"><span data-stu-id="819f4-174">RELATED LINKS</span></span>

[<span data-ttu-id="819f4-175">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="819f4-175">Get-AzureRMEnvironment</span></span>](./Get-AzureRMEnvironment.md)

[<span data-ttu-id="819f4-176">제거-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="819f4-176">Remove-AzureRMEnvironment</span></span>](./Remove-AzureRMEnvironment.md)

[<span data-ttu-id="819f4-177">Set-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="819f4-177">Set-AzureRMEnvironment</span></span>](./Set-AzureRMEnvironment.md)

