---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/set-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Set-AzEnvironment.md
ms.openlocfilehash: 7764a40f71b689835d340e8061616e6e5a548621
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199929"
---
# <span data-ttu-id="4b62b-101">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="4b62b-101">Set-AzEnvironment</span></span>

## <span data-ttu-id="4b62b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b62b-102">SYNOPSIS</span></span>
<span data-ttu-id="4b62b-103">Azure 환경에 대한 속성을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4b62b-103">Sets properties for an Azure environment.</span></span>

## <span data-ttu-id="4b62b-104">구문</span><span class="sxs-lookup"><span data-stu-id="4b62b-104">SYNTAX</span></span>

### <span data-ttu-id="4b62b-105">이름(기본값)</span><span class="sxs-lookup"><span data-stu-id="4b62b-105">Name (Default)</span></span>
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
 [-AzureAnalysisServicesEndpointResourceId <String>] [-AzureAttestationServiceEndpointSuffix <String>]
 [-AzureAttestationServiceEndpointResourceId <String>] [-AzureSynapseAnalyticsEndpointSuffix <String>]
 [-ContainerRegistryEndpointSuffix <String>] [-AzureSynapseAnalyticsEndpointResourceId <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4b62b-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="4b62b-106">ARMEndpoint</span></span>
```
Set-AzEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-AzureAnalysisServicesEndpointSuffix <String>] [-AzureAnalysisServicesEndpointResourceId <String>]
 [-AzureAttestationServiceEndpointSuffix <String>] [-AzureAttestationServiceEndpointResourceId <String>]
 [-AzureSynapseAnalyticsEndpointSuffix <String>] [-ContainerRegistryEndpointSuffix <String>]
 [-AzureSynapseAnalyticsEndpointResourceId <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b62b-107">설명</span><span class="sxs-lookup"><span data-stu-id="4b62b-107">DESCRIPTION</span></span>
<span data-ttu-id="4b62b-108">이 Set-AzEnvironment cmdlet은 Azure 인스턴스에 연결하기 위한 엔드포인트 및 메타데이터를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4b62b-108">The Set-AzEnvironment cmdlet sets endpoints and metadata for connecting to an instance of Azure.</span></span>

## <span data-ttu-id="4b62b-109">예제</span><span class="sxs-lookup"><span data-stu-id="4b62b-109">EXAMPLES</span></span>

### <span data-ttu-id="4b62b-110">예제 1: 새 환경 만들기 및 수정</span><span class="sxs-lookup"><span data-stu-id="4b62b-110">Example 1: Creating and modifying a new environment</span></span>
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
AzureAttestationServiceEndpointSuffix             :
AzureAttestationServiceEndpointResourceId         :
AzureSynapseAnalyticsEndpointSuffix               :
AzureSynapseAnalyticsEndpointResourceId           :
```

<span data-ttu-id="4b62b-111">이 예제에서는 Add-AzEnvironment를 사용하여 샘플 엔드포인트가 있는 새 Azure 환경을 만든 다음, Set-AzEnvironment cmdlet을 사용하여 만든 환경의 ActiveDirectoryEndpoint 및 GraphEndpoint 특성 값을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="4b62b-111">In this example we are creating a new Azure environment with sample endpoints using Add-AzEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzEnvironment.</span></span>

## <span data-ttu-id="4b62b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b62b-112">PARAMETERS</span></span>

### <span data-ttu-id="4b62b-113">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="4b62b-113">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="4b62b-114">Azure Active Directory 인증에 대한 기본 기관을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4b62b-114">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="4b62b-115">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="4b62b-115">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="4b62b-116">Azure Resource Manager 또는 RDFE(서비스 관리) 엔드포인트에 대한 요청을 인증하는 토큰의 대상을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4b62b-116">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="4b62b-117">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="4b62b-117">-AdTenant</span></span>
<span data-ttu-id="4b62b-118">기본 Active Directory 테넌트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4b62b-118">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="4b62b-119">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="4b62b-119">-ARMEndpoint</span></span>
<span data-ttu-id="4b62b-120">Azure Resource Manager 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="4b62b-120">The Azure Resource Manager endpoint.</span></span>

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

### <span data-ttu-id="4b62b-121">-AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="4b62b-121">-AzureAnalysisServicesEndpointResourceId</span></span>
<span data-ttu-id="4b62b-122">Azure Analysis Services 리소스의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="4b62b-122">The resource identifier of the Azure Analysis Services resource.</span></span>

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

### <span data-ttu-id="4b62b-123">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="4b62b-123">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="4b62b-124">Azure Log Analytics API와 통신할 때 사용할 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="4b62b-124">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="4b62b-125">-AzureAttestationServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="4b62b-125">-AzureAttestationServiceEndpointResourceId</span></span>
<span data-ttu-id="4b62b-126">요청된 토큰의 받는 사람인 Azure Attestation 서비스의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="4b62b-126">The The resource identifier of the Azure Attestation service that is the recipient of the requested token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b62b-127">-AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="4b62b-127">-AzureAttestationServiceEndpointSuffix</span></span>
<span data-ttu-id="4b62b-128">Azure Attestation 서비스의 Dns 접미사입니다.</span><span class="sxs-lookup"><span data-stu-id="4b62b-128">Dns suffix of Azure Attestation service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b62b-129">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="4b62b-129">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="4b62b-130">Azure Data Lake Analytics 작업 및 카탈로그 서비스의 Dns 접미사</span><span class="sxs-lookup"><span data-stu-id="4b62b-130">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="4b62b-131">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="4b62b-131">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="4b62b-132">Azure Data Lake Store FileSystem의 Dns 접미사입니다.</span><span class="sxs-lookup"><span data-stu-id="4b62b-132">Dns Suffix of Azure Data Lake Store FileSystem.</span></span> <span data-ttu-id="4b62b-133">예: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="4b62b-133">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="4b62b-134">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="4b62b-134">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="4b62b-135">Azure Key Vault 서비스의 Dns 접미사입니다.</span><span class="sxs-lookup"><span data-stu-id="4b62b-135">Dns suffix of Azure Key Vault service.</span></span> <span data-ttu-id="4b62b-136">예제는 vault-int.azure-int.net</span><span class="sxs-lookup"><span data-stu-id="4b62b-136">Example is vault-int.azure-int.net</span></span>

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

### <span data-ttu-id="4b62b-137">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="4b62b-137">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="4b62b-138">요청된 토큰의 받는 사람인 Azure Key Vault 데이터 서비스의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="4b62b-138">Resource identifier of Azure Key Vault data service that is the recipient of the requested token.</span></span>

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

### <span data-ttu-id="4b62b-139">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="4b62b-139">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="4b62b-140">Azure Log Analytics API와 통신할 때 사용할 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="4b62b-140">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="4b62b-141">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="4b62b-141">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="4b62b-142">Azure Log Analytics API를 사용하여 인증하는 토큰에 대한 대상입니다.</span><span class="sxs-lookup"><span data-stu-id="4b62b-142">The audience for tokens authenticating with the Azure Log Analytics API.</span></span>

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

### <span data-ttu-id="4b62b-143">-AzureSynapseAnalyticsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="4b62b-143">-AzureSynapseAnalyticsEndpointResourceId</span></span>
<span data-ttu-id="4b62b-144">요청된 토큰의 받는 사람인 Azure Synapse Analytics의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="4b62b-144">The The resource identifier of the Azure Synapse Analytics that is the recipient of the requested token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b62b-145">-AzureSynapseAnalyticsEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="4b62b-145">-AzureSynapseAnalyticsEndpointSuffix</span></span>
<span data-ttu-id="4b62b-146">Azure Synapse Analytics의 Dns 접미사입니다.</span><span class="sxs-lookup"><span data-stu-id="4b62b-146">Dns suffix of Azure Synapse Analytics.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b62b-147">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="4b62b-147">-BatchEndpointResourceId</span></span>
<span data-ttu-id="4b62b-148">요청된 토큰의 받는 사람인 Azure Batch 서비스의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="4b62b-148">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

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

### <span data-ttu-id="4b62b-149">-ContainerRegistryEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="4b62b-149">-ContainerRegistryEndpointSuffix</span></span>
<span data-ttu-id="4b62b-150">Azure Container Registry의 접미사입니다.</span><span class="sxs-lookup"><span data-stu-id="4b62b-150">Suffix of Azure Container Registry.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b62b-151">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="4b62b-151">-DataLakeAudience</span></span>
<span data-ttu-id="4b62b-152">AD Data Lake 서비스 엔드포인트를 사용하여 인증하는 토큰의 대상입니다.</span><span class="sxs-lookup"><span data-stu-id="4b62b-152">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

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

### <span data-ttu-id="4b62b-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b62b-153">-DefaultProfile</span></span>
<span data-ttu-id="4b62b-154">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4b62b-154">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b62b-155">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="4b62b-155">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="4b62b-156">ADFS(Active Directory Federation Services) -프레미스 인증이 허용된 경우를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4b62b-156">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="4b62b-157">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="4b62b-157">-GalleryEndpoint</span></span>
<span data-ttu-id="4b62b-158">배포 템플릿의 Azure Resource Manager 갤러리에 대한 엔드포인트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4b62b-158">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="4b62b-159">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="4b62b-159">-GraphAudience</span></span>
<span data-ttu-id="4b62b-160">AD Graph 엔드포인트를 사용하여 인증하는 토큰의 대상입니다.</span><span class="sxs-lookup"><span data-stu-id="4b62b-160">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="4b62b-161">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="4b62b-161">-GraphEndpoint</span></span>
<span data-ttu-id="4b62b-162">Graph(Active Directory 메타데이터) 요청에 대한 URL을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4b62b-162">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="4b62b-163">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="4b62b-163">-ManagementPortalUrl</span></span>
<span data-ttu-id="4b62b-164">관리 포털의 URL을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4b62b-164">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="4b62b-165">-Name</span><span class="sxs-lookup"><span data-stu-id="4b62b-165">-Name</span></span>
<span data-ttu-id="4b62b-166">수정할 환경의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4b62b-166">Specifies the name of the environment to modify.</span></span>

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

### <span data-ttu-id="4b62b-167">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="4b62b-167">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="4b62b-168">.publishsettings 파일을 다운로드할 수 있는 URL을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4b62b-168">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="4b62b-169">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4b62b-169">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="4b62b-170">Azure Resource Manager 요청에 대한 URL을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4b62b-170">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="4b62b-171">-Scope</span><span class="sxs-lookup"><span data-stu-id="4b62b-171">-Scope</span></span>
<span data-ttu-id="4b62b-172">컨텍스트 변경 범위(예: 변경 내용이 현재 프로세스에만 적용되는지 또는 이 사용자가 시작한 모든 세션에 적용되는지 여부)를 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="4b62b-172">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="4b62b-173">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="4b62b-173">-ServiceEndpoint</span></span>
<span data-ttu-id="4b62b-174">RDFE(서비스 관리) 요청에 대한 엔드포인트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4b62b-174">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="4b62b-175">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="4b62b-175">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="4b62b-176">Azure SQL Database 서버에 대한 도메인 이름 접미사를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4b62b-176">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="4b62b-177">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="4b62b-177">-StorageEndpoint</span></span>
<span data-ttu-id="4b62b-178">저장소(Blob, 테이블, 큐 및 파일) 액세스에 대한 엔드포인트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4b62b-178">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

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

### <span data-ttu-id="4b62b-179">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="4b62b-179">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="4b62b-180">Azure Traffic Manager 서비스에 대한 도메인 이름 접미사를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4b62b-180">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="4b62b-181">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4b62b-181">-Confirm</span></span>
<span data-ttu-id="4b62b-182">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4b62b-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b62b-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b62b-183">-WhatIf</span></span>
<span data-ttu-id="4b62b-184">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="4b62b-184">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4b62b-185">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4b62b-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b62b-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b62b-186">CommonParameters</span></span>
<span data-ttu-id="4b62b-187">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4b62b-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b62b-188">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4b62b-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b62b-189">입력</span><span class="sxs-lookup"><span data-stu-id="4b62b-189">INPUTS</span></span>

### <span data-ttu-id="4b62b-190">System.String</span><span class="sxs-lookup"><span data-stu-id="4b62b-190">System.String</span></span>

### <span data-ttu-id="4b62b-191">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="4b62b-191">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4b62b-192">출력</span><span class="sxs-lookup"><span data-stu-id="4b62b-192">OUTPUTS</span></span>

### <span data-ttu-id="4b62b-193">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="4b62b-193">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="4b62b-194">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4b62b-194">NOTES</span></span>

## <span data-ttu-id="4b62b-195">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4b62b-195">RELATED LINKS</span></span>

[<span data-ttu-id="4b62b-196">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="4b62b-196">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="4b62b-197">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="4b62b-197">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="4b62b-198">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="4b62b-198">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

