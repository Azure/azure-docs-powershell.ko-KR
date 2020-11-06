---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/set-azurermenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Set-AzureRmEnvironment.md
ms.openlocfilehash: 073126f3f750f2decf7189c53733c5fcaaabee31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529436"
---
# <span data-ttu-id="71b6d-101">Set-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="71b6d-101">Set-AzureRmEnvironment</span></span>

## <span data-ttu-id="71b6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71b6d-102">SYNOPSIS</span></span>
<span data-ttu-id="71b6d-103">Azure 환경에 대 한 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71b6d-103">Sets properties for an Azure environment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71b6d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="71b6d-104">SYNTAX</span></span>

### <span data-ttu-id="71b6d-105">Name (기본값)</span><span class="sxs-lookup"><span data-stu-id="71b6d-105">Name (Default)</span></span>
```
Set-AzureRmEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
 [[-ManagementPortalUrl] <String>] [[-StorageEndpoint] <String>] [[-ActiveDirectoryEndpoint] <String>]
 [[-ResourceManagerEndpoint] <String>] [[-GalleryEndpoint] <String>]
 [[-ActiveDirectoryServiceEndpointResourceId] <String>] [[-GraphEndpoint] <String>]
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-TrafficManagerDnsSuffix] <String>] [[-SqlDatabaseDnsSuffix] <String>]
 [[-AzureDataLakeStoreFileSystemEndpointSuffix] <String>]
 [[-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix] <String>] [-EnableAdfsAuthentication]
 [[-AdTenant] <String>] [[-GraphAudience] <String>] [[-DataLakeAudience] <String>]
 [[-BatchEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpoint] <String>] [[-AzureAnalysisServicesEndpointSuffix] <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71b6d-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="71b6d-106">ARMEndpoint</span></span>
```
Set-AzureRmEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="71b6d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="71b6d-107">DESCRIPTION</span></span>
<span data-ttu-id="71b6d-108">Set-AzureRMEnvironment cmdlet은 Azure의 인스턴스에 연결 하기 위한 끝점 및 메타 데이터를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71b6d-108">The Set-AzureRMEnvironment cmdlet sets endpoints and metadata for connecting to an instance of Azure.</span></span>

## <span data-ttu-id="71b6d-109">예제의</span><span class="sxs-lookup"><span data-stu-id="71b6d-109">EXAMPLES</span></span>

### <span data-ttu-id="71b6d-110">예제 1: 새 환경 만들기 및 수정</span><span class="sxs-lookup"><span data-stu-id="71b6d-110">Example 1: Creating and modifying a new environment</span></span>
```
PS C:\> Add-AzureRmEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint TestADEndpoint `
        -ActiveDirectoryServiceEndpointResourceId TestADApplicationId `
        -ResourceManagerEndpoint TestRMEndpoint `
        -GalleryEndpoint TestGalleryEndpoint `
        -GraphEndpoint TestGraphEndpoint

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/

PS C:\> Set-AzureRmEnvironment -Name TestEnvironment
        -ActiveDirectoryEndpoint NewTestADEndpoint
        -GraphEndpoint NewTestGraphEndpoint | Format-List

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
BatchEndpointResourceId                           :
AzureOperationalInsightsEndpoint                  :
AzureOperationalInsightsEndpointResourceId        :
```

<span data-ttu-id="71b6d-111">이 예제에서는 Add-AzureRmEnvironment를 사용 하 여 샘플 끝점을 사용 하 여 새 Azure 환경을 만든 다음, cmdlet 집합-AzureRmEnvironment를 사용 하 여 생성 된 환경의 ActiveDirectoryEndpoint 및 GraphEndpoint 특성 값을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="71b6d-111">In this example we are creating a new Azure environment with sample endpoints using Add-AzureRmEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzureRmEnvironment.</span></span>

## <span data-ttu-id="71b6d-112">변수</span><span class="sxs-lookup"><span data-stu-id="71b6d-112">PARAMETERS</span></span>

### <span data-ttu-id="71b6d-113">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="71b6d-113">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="71b6d-114">Azure Active Directory 인증에 대 한 기본 인증 기관을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71b6d-114">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="71b6d-115">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="71b6d-115">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="71b6d-116">Azure Resource Manager 또는 RDFE (서비스 관리) 끝점에 대 한 요청을 인증 하는 토큰에 대 한 대상 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71b6d-116">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="71b6d-117">-AdTenant 넌 트</span><span class="sxs-lookup"><span data-stu-id="71b6d-117">-AdTenant</span></span>
<span data-ttu-id="71b6d-118">기본 Active Directory 테 넌 트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71b6d-118">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="71b6d-119">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="71b6d-119">-ARMEndpoint</span></span>
<span data-ttu-id="71b6d-120">Azure 리소스 관리자 끝점입니다.</span><span class="sxs-lookup"><span data-stu-id="71b6d-120">The Azure Resource Manager endpoint.</span></span>

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

### <span data-ttu-id="71b6d-121">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="71b6d-121">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="71b6d-122">Azure Analysis Services 서비스 끝점의 Dns 접미사</span><span class="sxs-lookup"><span data-stu-id="71b6d-122">Dns Suffix of Azure Analysis Services service endpoints</span></span>

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

### <span data-ttu-id="71b6d-123">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="71b6d-123">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="71b6d-124">Azure Data Lake Analytics 작업 및 카탈로그 서비스의 Dns 접미사</span><span class="sxs-lookup"><span data-stu-id="71b6d-124">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="71b6d-125">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="71b6d-125">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="71b6d-126">Azure Data Lake Store 파일 시스템의 Dns 접미사.</span><span class="sxs-lookup"><span data-stu-id="71b6d-126">Dns Suffix of Azure Data Lake Store FileSystem.</span></span>
<span data-ttu-id="71b6d-127">예: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="71b6d-127">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="71b6d-128">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="71b6d-128">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="71b6d-129">키 보관소 서비스에 대 한 도메인 이름 접미사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71b6d-129">Specifies the domain name suffix for Key Vault services.</span></span>

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

### <span data-ttu-id="71b6d-130">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="71b6d-130">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="71b6d-131">키 자격 증명 모음 서비스에 대 한 요청을 승인 하는 액세스 토큰에 대 한 대상을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71b6d-131">Specifies the audience for access tokens that authorize requests for Key Vault services.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71b6d-132">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="71b6d-132">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="71b6d-133">Operational Insights 쿼리 액세스에 대 한 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71b6d-133">Specifies the endpoint for the Operational Insights query access.</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 22
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71b6d-134">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="71b6d-134">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="71b6d-135">Operational Insights 서비스에 대 한 요청을 승인 하는 액세스 토큰의 대상을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71b6d-135">Specifies the audience for access tokens that authorize requests for Operational Insights services.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 21
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71b6d-136">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="71b6d-136">-BatchEndpointResourceId</span></span>
<span data-ttu-id="71b6d-137">요청 된 토큰의 받는 사람에 해당 하는 Azure 일괄 처리 서비스의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="71b6d-137">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BatchResourceId, BatchAudience

Required: False
Position: 20
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71b6d-138">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="71b6d-138">-DataLakeAudience</span></span>
<span data-ttu-id="71b6d-139">AD Data Lake 서비스 끝점을 사용 하 여 인증 하는 토큰의 대상 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="71b6d-139">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

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

### <span data-ttu-id="71b6d-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71b6d-140">-DefaultProfile</span></span>
<span data-ttu-id="71b6d-141">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="71b6d-141">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71b6d-142">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="71b6d-142">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="71b6d-143">ADFS (Active Directory Federation Services) 온-프레미스 인증이 허용 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="71b6d-143">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="71b6d-144">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="71b6d-144">-GalleryEndpoint</span></span>
<span data-ttu-id="71b6d-145">배포 서식 파일의 Azure Resource Manager 갤러리에 대 한 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71b6d-145">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="71b6d-146">-GraphAudience 대상</span><span class="sxs-lookup"><span data-stu-id="71b6d-146">-GraphAudience</span></span>
<span data-ttu-id="71b6d-147">광고 그래프 끝점을 사용 하 여 인증 하는 토큰에 대 한 대상 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="71b6d-147">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="71b6d-148">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="71b6d-148">-GraphEndpoint</span></span>
<span data-ttu-id="71b6d-149">그래프 (Active Directory 메타 데이터) 요청에 대 한 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71b6d-149">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="71b6d-150">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="71b6d-150">-ManagementPortalUrl</span></span>
<span data-ttu-id="71b6d-151">관리 포털에 대 한 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71b6d-151">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="71b6d-152">-이름</span><span class="sxs-lookup"><span data-stu-id="71b6d-152">-Name</span></span>
<span data-ttu-id="71b6d-153">수정할 환경의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71b6d-153">Specifies the name of the environment to modify.</span></span>

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

### <span data-ttu-id="71b6d-154">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="71b6d-154">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="71b6d-155">Publishsettings 파일을 다운로드할 수 있는 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71b6d-155">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="71b6d-156">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="71b6d-156">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="71b6d-157">Azure Resource Manager 요청에 대 한 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71b6d-157">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="71b6d-158">-범위</span><span class="sxs-lookup"><span data-stu-id="71b6d-158">-Scope</span></span>
<span data-ttu-id="71b6d-159">컨텍스트 변경의 범위 (예: 변경 내용이 현재 프로세스에만 적용 되는지 또는이 사용자가 시작한 모든 세션)를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71b6d-159">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="71b6d-160">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="71b6d-160">-ServiceEndpoint</span></span>
<span data-ttu-id="71b6d-161">RDFE (서비스 관리) 요청에 대 한 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71b6d-161">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="71b6d-162">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="71b6d-162">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="71b6d-163">Azure SQL 데이터베이스 서버의 도메인 이름 접미사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71b6d-163">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="71b6d-164">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="71b6d-164">-StorageEndpoint</span></span>
<span data-ttu-id="71b6d-165">저장소 (blob, 테이블, 큐 및 파일) 액세스에 대 한 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71b6d-165">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="71b6d-166">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="71b6d-166">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="71b6d-167">Azure Traffic Manager 서비스에 대 한 도메인 이름 접미사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71b6d-167">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="71b6d-168">-확인</span><span class="sxs-lookup"><span data-stu-id="71b6d-168">-Confirm</span></span>
<span data-ttu-id="71b6d-169">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="71b6d-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71b6d-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71b6d-170">-WhatIf</span></span>
<span data-ttu-id="71b6d-171">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="71b6d-171">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="71b6d-172">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="71b6d-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71b6d-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71b6d-173">CommonParameters</span></span>
<span data-ttu-id="71b6d-174">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="71b6d-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71b6d-175">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71b6d-175">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71b6d-176">입력</span><span class="sxs-lookup"><span data-stu-id="71b6d-176">INPUTS</span></span>

### <span data-ttu-id="71b6d-177">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="71b6d-177">System.String</span></span>

### <span data-ttu-id="71b6d-178">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="71b6d-178">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="71b6d-179">출력</span><span class="sxs-lookup"><span data-stu-id="71b6d-179">OUTPUTS</span></span>

### <span data-ttu-id="71b6d-180">Microsoft. Azure. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="71b6d-180">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="71b6d-181">상속자</span><span class="sxs-lookup"><span data-stu-id="71b6d-181">NOTES</span></span>

## <span data-ttu-id="71b6d-182">관련 링크</span><span class="sxs-lookup"><span data-stu-id="71b6d-182">RELATED LINKS</span></span>

[<span data-ttu-id="71b6d-183">추가-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="71b6d-183">Add-AzureRMEnvironment</span></span>](./Add-AzureRMEnvironment.md)

[<span data-ttu-id="71b6d-184">Get-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="71b6d-184">Get-AzureRMEnvironment</span></span>](./Get-AzureRMEnvironment.md)

[<span data-ttu-id="71b6d-185">제거-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="71b6d-185">Remove-AzureRMEnvironment</span></span>](./Remove-AzureRMEnvironment.md)

