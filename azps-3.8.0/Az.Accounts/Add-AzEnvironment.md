---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/add-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Add-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Add-AzEnvironment.md
ms.openlocfilehash: c1df1917a4133cf43f7cf0db89f1d59ad2c9c151
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043042"
---
# <span data-ttu-id="a37e0-101">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="a37e0-101">Add-AzEnvironment</span></span>

## <span data-ttu-id="a37e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a37e0-102">SYNOPSIS</span></span>
<span data-ttu-id="a37e0-103">Azure Resource Manager 인스턴스에 대 한 끝점 및 메타 데이터를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="a37e0-103">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

## <span data-ttu-id="a37e0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a37e0-104">SYNTAX</span></span>

### <span data-ttu-id="a37e0-105">Name (기본값)</span><span class="sxs-lookup"><span data-stu-id="a37e0-105">Name (Default)</span></span>
```
Add-AzEnvironment [-Name] <String> [[-PublishSettingsFileUrl] <String>] [[-ServiceEndpoint] <String>]
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
 [-AzureAnalysisServicesEndpointResourceId <String>] [-AzureAttestationServiceEndpointSuffix <String>]
 [-AzureAttestationServiceEndpointResourceId <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a37e0-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="a37e0-106">ARMEndpoint</span></span>
```
Add-AzEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-AzureAnalysisServicesEndpointSuffix <String>] [-AzureAnalysisServicesEndpointResourceId <String>]
 [-AzureAttestationServiceEndpointSuffix <String>] [-AzureAttestationServiceEndpointResourceId <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a37e0-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a37e0-107">DESCRIPTION</span></span>
<span data-ttu-id="a37e0-108">Add-AzEnvironment cmdlet은 azure resource manager cmdlet이 Azure Resource Manager의 새 인스턴스와 연결할 수 있도록 끝점 및 메타 데이터를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="a37e0-108">The Add-AzEnvironment cmdlet adds endpoints and metadata to enable Azure Resource Manager cmdlets to connect with a new instance of Azure Resource Manager.</span></span>
<span data-ttu-id="a37e0-109">기본 제공 환경 AzureCloud와 AzureChinaCloud는 Azure 리소스 관리자의 기존 공용 인스턴스를 대상으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="a37e0-109">The built-in environments AzureCloud and AzureChinaCloud target existing public instances of Azure Resource Manager.</span></span>

## <span data-ttu-id="a37e0-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a37e0-110">EXAMPLES</span></span>

### <span data-ttu-id="a37e0-111">예제 1: 새 환경 만들기 및 수정</span><span class="sxs-lookup"><span data-stu-id="a37e0-111">Example 1: Creating and modifying a new environment</span></span>
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

PS C:\> Set-AzEnvironment -Name TestEnvironment `
        -ActiveDirectoryEndpoint NewTestADEndpoint `
        -GraphEndpoint NewTestGraphEndpoint | Format-List

Name                                              : TestEnvironment
EnableAdfsAuthentication                          : False
OnPremise                                         : False
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
DataLakeEndpointResourceId                        :
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            :
AzureOperationalInsightsEndpointResourceId        :
AzureOperationalInsightsEndpoint                  :
AzureAnalysisServicesEndpointSuffix               :
AzureAttestationServiceEndpointSuffix             :
AzureAttestationServiceEndpointResourceId         :
VersionProfiles                                   : {}
ExtendedProperties                                : {}
BatchEndpointResourceId                           :

In this example we are creating a new Azure environment with sample endpoints using Add-AzEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzEnvironment.
```

## <span data-ttu-id="a37e0-112">변수</span><span class="sxs-lookup"><span data-stu-id="a37e0-112">PARAMETERS</span></span>

### <span data-ttu-id="a37e0-113">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="a37e0-113">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="a37e0-114">Azure Active Directory 인증에 대 한 기본 인증 기관을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a37e0-114">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="a37e0-115">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="a37e0-115">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="a37e0-116">Azure Resource Manager 또는 RDFE (서비스 관리) 끝점에 대 한 요청을 인증 하는 토큰에 대 한 대상 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a37e0-116">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="a37e0-117">-AdTenant 넌 트</span><span class="sxs-lookup"><span data-stu-id="a37e0-117">-AdTenant</span></span>
<span data-ttu-id="a37e0-118">기본 Active Directory 테 넌 트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a37e0-118">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="a37e0-119">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="a37e0-119">-ARMEndpoint</span></span>
<span data-ttu-id="a37e0-120">Azure 리소스 관리자 끝점</span><span class="sxs-lookup"><span data-stu-id="a37e0-120">The Azure Resource Manager endpoint</span></span>

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

### <span data-ttu-id="a37e0-121">-AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="a37e0-121">-AzureAnalysisServicesEndpointResourceId</span></span>
<span data-ttu-id="a37e0-122">Azure Analysis Services 리소스의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="a37e0-122">The resource identifier of the Azure Analysis Services resource.</span></span>

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

### <span data-ttu-id="a37e0-123">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="a37e0-123">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="a37e0-124">Azure 로그 분석 API와 통신할 때 사용할 끝점입니다.</span><span class="sxs-lookup"><span data-stu-id="a37e0-124">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="a37e0-125">-AzureAttestationServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="a37e0-125">-AzureAttestationServiceEndpointResourceId</span></span>
<span data-ttu-id="a37e0-126">요청 된 토큰의 받는 사람이 되는 Azure 증명 서비스의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="a37e0-126">The The resource identifier of the Azure Attestation service that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="a37e0-127">-AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="a37e0-127">-AzureAttestationServiceEndpointSuffix</span></span>
<span data-ttu-id="a37e0-128">Azure 증명 서비스의 Dns 접미사입니다.</span><span class="sxs-lookup"><span data-stu-id="a37e0-128">Dns suffix of Azure Attestation service.</span></span>

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

### <span data-ttu-id="a37e0-129">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="a37e0-129">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="a37e0-130">Azure Data Lake Analytics 작업 및 카탈로그 서비스의 Dns 접미사</span><span class="sxs-lookup"><span data-stu-id="a37e0-130">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="a37e0-131">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="a37e0-131">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="a37e0-132">Azure Data Lake Store 파일 시스템의 Dns 접미사.</span><span class="sxs-lookup"><span data-stu-id="a37e0-132">Dns Suffix of Azure Data Lake Store FileSystem.</span></span> <span data-ttu-id="a37e0-133">예: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="a37e0-133">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="a37e0-134">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="a37e0-134">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="a37e0-135">Azure 키 보관소 서비스의 Dns 접미사.</span><span class="sxs-lookup"><span data-stu-id="a37e0-135">Dns suffix of Azure Key Vault service.</span></span> <span data-ttu-id="a37e0-136">예를 vault-int.azure-int.net</span><span class="sxs-lookup"><span data-stu-id="a37e0-136">Example is vault-int.azure-int.net</span></span>

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

### <span data-ttu-id="a37e0-137">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="a37e0-137">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="a37e0-138">요청한 토큰의 받는 사람이 되는 Azure 키 보관소 데이터 서비스의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="a37e0-138">Resource identifier of Azure Key Vault data service that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="a37e0-139">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="a37e0-139">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="a37e0-140">Azure 로그 분석 API와 통신할 때 사용할 끝점입니다.</span><span class="sxs-lookup"><span data-stu-id="a37e0-140">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="a37e0-141">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="a37e0-141">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="a37e0-142">Azure 로그 분석 API를 사용 하 여 인증 하는 토큰에 대 한 대상 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="a37e0-142">The audience for tokens authenticating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="a37e0-143">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="a37e0-143">-BatchEndpointResourceId</span></span>
<span data-ttu-id="a37e0-144">요청 된 토큰의 받는 사람에 해당 하는 Azure 일괄 처리 서비스의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="a37e0-144">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

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

### <span data-ttu-id="a37e0-145">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="a37e0-145">-DataLakeAudience</span></span>
<span data-ttu-id="a37e0-146">AD Data Lake 서비스 끝점을 사용 하 여 인증 하는 토큰의 대상 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="a37e0-146">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

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

### <span data-ttu-id="a37e0-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a37e0-147">-DefaultProfile</span></span>
<span data-ttu-id="a37e0-148">Azure와 통신 하는 데 사용 되는 자격 증명, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a37e0-148">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a37e0-149">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="a37e0-149">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="a37e0-150">ADFS (Active Directory Federation Services) 온-프레미스 인증이 허용 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a37e0-150">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="a37e0-151">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="a37e0-151">-GalleryEndpoint</span></span>
<span data-ttu-id="a37e0-152">배포 서식 파일의 Azure Resource Manager 갤러리에 대 한 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a37e0-152">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="a37e0-153">-GraphAudience 대상</span><span class="sxs-lookup"><span data-stu-id="a37e0-153">-GraphAudience</span></span>
<span data-ttu-id="a37e0-154">광고 그래프 끝점을 사용 하 여 인증 하는 토큰에 대 한 대상 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="a37e0-154">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="a37e0-155">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="a37e0-155">-GraphEndpoint</span></span>
<span data-ttu-id="a37e0-156">그래프 (Active Directory 메타 데이터) 요청에 대 한 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a37e0-156">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="a37e0-157">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="a37e0-157">-ManagementPortalUrl</span></span>
<span data-ttu-id="a37e0-158">관리 포털에 대 한 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a37e0-158">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="a37e0-159">-이름</span><span class="sxs-lookup"><span data-stu-id="a37e0-159">-Name</span></span>
<span data-ttu-id="a37e0-160">추가할 환경의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a37e0-160">Specifies the name of the environment to add.</span></span>

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

### <span data-ttu-id="a37e0-161">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="a37e0-161">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="a37e0-162">Publishsettings 파일을 다운로드할 수 있는 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a37e0-162">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="a37e0-163">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a37e0-163">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="a37e0-164">Azure Resource Manager 요청에 대 한 URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a37e0-164">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="a37e0-165">-범위</span><span class="sxs-lookup"><span data-stu-id="a37e0-165">-Scope</span></span>
<span data-ttu-id="a37e0-166">컨텍스트 변경의 범위 (예: 변경 내용이 현재 프로세스에만 적용 되는지 또는이 사용자가 시작한 모든 세션)를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a37e0-166">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="a37e0-167">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="a37e0-167">-ServiceEndpoint</span></span>
<span data-ttu-id="a37e0-168">RDFE (서비스 관리) 요청에 대 한 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a37e0-168">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="a37e0-169">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="a37e0-169">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="a37e0-170">Azure SQL 데이터베이스 서버의 도메인 이름 접미사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a37e0-170">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="a37e0-171">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="a37e0-171">-StorageEndpoint</span></span>
<span data-ttu-id="a37e0-172">저장소 (blob, 테이블, 큐 및 파일) 액세스에 대 한 끝점을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a37e0-172">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="a37e0-173">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="a37e0-173">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="a37e0-174">Azure Traffic Manager 서비스에 대 한 도메인 이름 접미사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a37e0-174">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="a37e0-175">-확인</span><span class="sxs-lookup"><span data-stu-id="a37e0-175">-Confirm</span></span>
<span data-ttu-id="a37e0-176">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a37e0-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a37e0-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a37e0-177">-WhatIf</span></span>
<span data-ttu-id="a37e0-178">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a37e0-178">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a37e0-179">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a37e0-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a37e0-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a37e0-180">CommonParameters</span></span>
<span data-ttu-id="a37e0-181">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a37e0-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a37e0-182">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a37e0-182">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a37e0-183">입력</span><span class="sxs-lookup"><span data-stu-id="a37e0-183">INPUTS</span></span>

### <span data-ttu-id="a37e0-184">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a37e0-184">System.String</span></span>

### <span data-ttu-id="a37e0-185">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="a37e0-185">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a37e0-186">출력</span><span class="sxs-lookup"><span data-stu-id="a37e0-186">OUTPUTS</span></span>

### <span data-ttu-id="a37e0-187">Microsoft. Azure. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="a37e0-187">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="a37e0-188">상속자</span><span class="sxs-lookup"><span data-stu-id="a37e0-188">NOTES</span></span>

## <span data-ttu-id="a37e0-189">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a37e0-189">RELATED LINKS</span></span>

[<span data-ttu-id="a37e0-190">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="a37e0-190">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="a37e0-191">제거-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="a37e0-191">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

[<span data-ttu-id="a37e0-192">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="a37e0-192">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

