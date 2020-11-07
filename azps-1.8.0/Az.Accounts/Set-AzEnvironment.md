---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/set-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzEnvironment.md
ms.openlocfilehash: cb7617f8db1e8aadd181fc5e978006bbeaae5c0b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689228"
---
# <span data-ttu-id="3f7a6-101">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="3f7a6-101">Set-AzEnvironment</span></span>

## <span data-ttu-id="3f7a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f7a6-102">SYNOPSIS</span></span>
<span data-ttu-id="3f7a6-103">Azure 환경에 대 한 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f7a6-103">Sets properties for an Azure environment.</span></span>

## <span data-ttu-id="3f7a6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3f7a6-104">SYNTAX</span></span>

### <span data-ttu-id="3f7a6-105">Name (기본값)</span><span class="sxs-lookup"><span data-stu-id="3f7a6-105">Name (Default)</span></span>
```
Set-AzEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
 [[-ManagementPortalUrl] <String>] [[-StorageEndpoint] <String>] [[-ActiveDirectoryEndpoint] <String>]
 [[-ResourceManagerEndpoint] <String>] [[-GalleryEndpoint] <String>]
 [[-ActiveDirectoryServiceEndpointResourceId] <String>] [[-GraphEndpoint] <String>]
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-TrafficManagerDnsSuffix] <String>] [[-SqlDatabaseDnsSuffix] <String>]
 [[-AzureDataLakeStoreFileSystemEndpointSuffix] <String>]
 [[-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix] <String>] [-EnableAdfsAuthentication]
 [[-AdTenant] <String>] [[-GraphAudience] <String>] [[-DataLakeAudience] <String>]
 [[-BatchEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpoint] <String>] [-AzureAnalysisServicesEndpointSuffix <String>]
 [-AzureAnalysisServicesEndpointResourceId <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f7a6-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="3f7a6-106">ARMEndpoint</span></span>
```
Set-AzEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-AzureAnalysisServicesEndpointSuffix <String>] [-AzureAnalysisServicesEndpointResourceId <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3f7a6-107">설명은</span><span class="sxs-lookup"><span data-stu-id="3f7a6-107">DESCRIPTION</span></span>
<span data-ttu-id="3f7a6-108">Set-AzEnvironment cmdlet은 Azure의 인스턴스에 연결 하기 위한 끝점 및 메타 데이터를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f7a6-108">The Set-AzEnvironment cmdlet sets endpoints and metadata for connecting to an instance of Azure.</span></span>

## <span data-ttu-id="3f7a6-109">예제의</span><span class="sxs-lookup"><span data-stu-id="3f7a6-109">EXAMPLES</span></span>

### <span data-ttu-id="3f7a6-110">예제 1: 새 환경 만들기 및 수정</span><span class="sxs-lookup"><span data-stu-id="3f7a6-110">Example 1: Creating and modifying a new environment</span></span>
```
PS C:\> Add-AzEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint TestADEndpoint `
        -ActiveDirectoryServiceEndpointResourceId TestADApplicationId `
        -ResourceManagerEndpoint TestRMEndpoint `
        -GalleryEndpoint TestGalleryEndpoint `
        -GraphEndpoint TestGraphEndpoint

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/

PS C:\> Set-AzEnvironment -Name TestEnvironment
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

<span data-ttu-id="3f7a6-111">이 예제에서는 Add-AzEnvironment를 사용 하 여 샘플 끝점을 사용 하 여 새 Azure 환경을 만든 다음, cmdlet 집합-AzEnvironment를 사용 하 여 생성 된 환경의 ActiveDirectoryEndpoint 및 GraphEndpoint 특성 값을 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f7a6-111">In this example we are creating a new Azure environment with sample endpoints using Add-AzEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzEnvironment.</span></span>

## <span data-ttu-id="3f7a6-112">변수</span><span class="sxs-lookup"><span data-stu-id="3f7a6-112">PARAMETERS</span></span>

### <span data-ttu-id="3f7a6-113">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="3f7a6-113">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="3f7a6-114">Azure Active Directory 인증에 대 한 기본 인증 기관을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f7a6-114">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="3f7a6-115">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="3f7a6-115">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="3f7a6-116">Azure Resource Manager 또는 RDFE (서비스 관리) 끝점에 대 한 요청을 인증 하는 토큰에 대 한 대상 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f7a6-116">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="3f7a6-117">-AdTenant 넌 트</span><span class="sxs-lookup"><span data-stu-id="3f7a6-117">-AdTenant</span></span>
<span data-ttu-id="3f7a6-118">기본 Active Directory 테 넌 트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f7a6-118">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="3f7a6-119">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="3f7a6-119">-ARMEndpoint</span></span>
<span data-ttu-id="3f7a6-120">Azure 리소스 관리자 끝점입니다.</span><span class="sxs-lookup"><span data-stu-id="3f7a6-120">The Azure Resource Manager endpoint.</span></span>

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

### <span data-ttu-id="3f7a6-121">-AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="3f7a6-121">-AzureAnalysisServicesEndpointResourceId</span></span>
<span data-ttu-id="3f7a6-122">Azure Analysis Services 리소스의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="3f7a6-122">The resource identifier of the Azure Analysis Services resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f7a6-123">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="3f7a6-123">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="3f7a6-124">Azure 로그 분석 API와 통신할 때 사용할 끝점입니다.</span><span class="sxs-lookup"><span data-stu-id="3f7a6-124">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f7a6-125">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="3f7a6-125">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="3f7a6-126">Azure Data Lake Analytics 작업 및 카탈로그 서비스의 Dns 접미사</span><span class="sxs-lookup"><span data-stu-id="3f7a6-126">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="3f7a6-127">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="3f7a6-127">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="3f7a6-128">Azure Data Lake Store 파일 시스템의 Dns 접미사.</span><span class="sxs-lookup"><span data-stu-id="3f7a6-128">Dns Suffix of Azure Data Lake Store FileSystem.</span></span> <span data-ttu-id="3f7a6-129">예: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="3f7a6-129">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="3f7a6-130">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="3f7a6-130">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="3f7a6-131">Azure 키 보관소 서비스의 Dns 접미사.</span><span class="sxs-lookup"><span data-stu-id="3f7a6-131">Dns suffix of Azure Key Vault service.</span></span> <span data-ttu-id="3f7a6-132">예를 vault-int.azure-int.net</span><span class="sxs-lookup"><span data-stu-id="3f7a6-132">Example is vault-int.azure-int.net</span></span>

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

### <span data-ttu-id="3f7a6-133">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="3f7a6-133">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="3f7a6-134">요청한 토큰의 받는 사람이 되는 Azure 키 보관소 데이터 서비스의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="3f7a6-134">Resource identifier of Azure Key Vault data service that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="3f7a6-135">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="3f7a6-135">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="3f7a6-136">Azure 로그 분석 API와 통신할 때 사용할 끝점입니다.</span><span class="sxs-lookup"><span data-stu-id="3f7a6-136">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="3f7a6-137">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="3f7a6-137">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="3f7a6-138">Azure 로그 분석 API를 사용 하 여 인증 하는 토큰에 대 한 대상 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="3f7a6-138">The audience for tokens authenticating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="3f7a6-139">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="3f7a6-139">-BatchEndpointResourceId</span></span>
<span data-ttu-id="3f7a6-140">요청 된 토큰의 받는 사람에 해당 하는 Azure 일괄 처리 서비스의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="3f7a6-140">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

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

### <span data-ttu-id="3f7a6-141">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="3f7a6-141">-DataLakeAudience</span></span>
<span data-ttu-id="3f7a6-142">AD Data Lake 서비스 끝점을 사용 하 여 인증 하는 토큰의 대상 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="3f7a6-142">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

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

### <span data-ttu-id="3f7a6-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f7a6-143">-DefaultProfile</span></span>
<span data-ttu-id="3f7a6-144">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3f7a6-144">The credentials, account, tenant and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3f7a6-145">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="3f7a6-145">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="3f7a6-146">ADFS (Active Directory Federation Services) 온-프레미스 인증이 허용 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3f7a6-146">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="3f7a6-147">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="3f7a6-147">-GalleryEndpoint</span></span>
<span data-ttu-id="3f7a6-148">배포 서식 파일의 Azure Resource Manager 갤러리에 대 한 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f7a6-148">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="3f7a6-149">-GraphAudience 대상</span><span class="sxs-lookup"><span data-stu-id="3f7a6-149">-GraphAudience</span></span>
<span data-ttu-id="3f7a6-150">광고 그래프 끝점을 사용 하 여 인증 하는 토큰에 대 한 대상 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="3f7a6-150">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="3f7a6-151">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="3f7a6-151">-GraphEndpoint</span></span>
<span data-ttu-id="3f7a6-152">그래프 (Active Directory 메타 데이터) 요청에 대 한 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f7a6-152">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="3f7a6-153">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="3f7a6-153">-ManagementPortalUrl</span></span>
<span data-ttu-id="3f7a6-154">관리 포털에 대 한 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f7a6-154">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="3f7a6-155">-이름</span><span class="sxs-lookup"><span data-stu-id="3f7a6-155">-Name</span></span>
<span data-ttu-id="3f7a6-156">수정할 환경의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f7a6-156">Specifies the name of the environment to modify.</span></span>

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

### <span data-ttu-id="3f7a6-157">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="3f7a6-157">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="3f7a6-158">Publishsettings 파일을 다운로드할 수 있는 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f7a6-158">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="3f7a6-159">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="3f7a6-159">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="3f7a6-160">Azure Resource Manager 요청에 대 한 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f7a6-160">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="3f7a6-161">-범위</span><span class="sxs-lookup"><span data-stu-id="3f7a6-161">-Scope</span></span>
<span data-ttu-id="3f7a6-162">컨텍스트 변경의 범위 (예: 변경 내용이 현재 프로세스에만 적용 되는지 또는이 사용자가 시작한 모든 세션)를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f7a6-162">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="3f7a6-163">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="3f7a6-163">-ServiceEndpoint</span></span>
<span data-ttu-id="3f7a6-164">RDFE (서비스 관리) 요청에 대 한 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f7a6-164">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="3f7a6-165">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="3f7a6-165">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="3f7a6-166">Azure SQL 데이터베이스 서버의 도메인 이름 접미사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f7a6-166">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="3f7a6-167">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="3f7a6-167">-StorageEndpoint</span></span>
<span data-ttu-id="3f7a6-168">저장소 (blob, 테이블, 큐 및 파일) 액세스에 대 한 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f7a6-168">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="3f7a6-169">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="3f7a6-169">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="3f7a6-170">Azure Traffic Manager 서비스에 대 한 도메인 이름 접미사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f7a6-170">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="3f7a6-171">-확인</span><span class="sxs-lookup"><span data-stu-id="3f7a6-171">-Confirm</span></span>
<span data-ttu-id="3f7a6-172">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f7a6-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f7a6-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f7a6-173">-WhatIf</span></span>
<span data-ttu-id="3f7a6-174">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3f7a6-174">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3f7a6-175">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3f7a6-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f7a6-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f7a6-176">CommonParameters</span></span>
<span data-ttu-id="3f7a6-177">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f7a6-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f7a6-178">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f7a6-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f7a6-179">입력</span><span class="sxs-lookup"><span data-stu-id="3f7a6-179">INPUTS</span></span>

### <span data-ttu-id="3f7a6-180">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3f7a6-180">System.String</span></span>

### <span data-ttu-id="3f7a6-181">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="3f7a6-181">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="3f7a6-182">출력</span><span class="sxs-lookup"><span data-stu-id="3f7a6-182">OUTPUTS</span></span>

### <span data-ttu-id="3f7a6-183">Microsoft. Azure. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="3f7a6-183">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="3f7a6-184">상속자</span><span class="sxs-lookup"><span data-stu-id="3f7a6-184">NOTES</span></span>

## <span data-ttu-id="3f7a6-185">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3f7a6-185">RELATED LINKS</span></span>

[<span data-ttu-id="3f7a6-186">추가-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="3f7a6-186">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="3f7a6-187">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="3f7a6-187">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="3f7a6-188">제거-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="3f7a6-188">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

