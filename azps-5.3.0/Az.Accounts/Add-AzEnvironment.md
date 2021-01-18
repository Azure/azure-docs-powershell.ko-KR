---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/add-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Add-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Add-AzEnvironment.md
ms.openlocfilehash: 92a8c816f1c5a76b0f3725b70a627b798b9de2b0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492725"
---
# <span data-ttu-id="53bfb-101">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="53bfb-101">Add-AzEnvironment</span></span>

## <span data-ttu-id="53bfb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53bfb-102">SYNOPSIS</span></span>
<span data-ttu-id="53bfb-103">Azure Resource Manager의 인스턴스에 대한 엔드포인트 및 메타데이터를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="53bfb-103">Adds endpoints and metadata for an instance of Azure Resource Manager.</span></span>

## <span data-ttu-id="53bfb-104">구문</span><span class="sxs-lookup"><span data-stu-id="53bfb-104">SYNTAX</span></span>

### <span data-ttu-id="53bfb-105">이름(기본값)</span><span class="sxs-lookup"><span data-stu-id="53bfb-105">Name (Default)</span></span>
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
 [-AzureAttestationServiceEndpointResourceId <String>] [-AzureSynapseAnalyticsEndpointSuffix <String>]
 [-ContainerRegistryEndpointSuffix <String>] [-AzureSynapseAnalyticsEndpointResourceId <String>]
 [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="53bfb-106">ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="53bfb-106">ARMEndpoint</span></span>
```
Add-AzEnvironment [-Name] <String> [[-StorageEndpoint] <String>] [-ARMEndpoint] <String>
 [[-AzureKeyVaultDnsSuffix] <String>] [[-AzureKeyVaultServiceEndpointResourceId] <String>]
 [[-DataLakeAudience] <String>] [[-BatchEndpointResourceId] <String>]
 [[-AzureOperationalInsightsEndpointResourceId] <String>] [[-AzureOperationalInsightsEndpoint] <String>]
 [-AzureAnalysisServicesEndpointSuffix <String>] [-AzureAnalysisServicesEndpointResourceId <String>]
 [-AzureAttestationServiceEndpointSuffix <String>] [-AzureAttestationServiceEndpointResourceId <String>]
 [-AzureSynapseAnalyticsEndpointSuffix <String>] [-ContainerRegistryEndpointSuffix <String>]
 [-AzureSynapseAnalyticsEndpointResourceId <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53bfb-107">검색</span><span class="sxs-lookup"><span data-stu-id="53bfb-107">Discovery</span></span>
```
Add-AzEnvironment [-AutoDiscover] [-Uri <Uri>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53bfb-108">설명</span><span class="sxs-lookup"><span data-stu-id="53bfb-108">DESCRIPTION</span></span>
<span data-ttu-id="53bfb-109">이 Add-AzEnvironment cmdlet은 엔드포인트 및 메타데이터를 추가하여 Azure Resource Manager cmdlet이 Azure Resource Manager의 새 인스턴스와 연결할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="53bfb-109">The Add-AzEnvironment cmdlet adds endpoints and metadata to enable Azure Resource Manager cmdlets to connect with a new instance of Azure Resource Manager.</span></span>
<span data-ttu-id="53bfb-110">기본 제공 환경인 AzureCloud 및 AzureChinaCloud는 Azure Resource Manager의 기존 공용 인스턴스를 대상으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="53bfb-110">The built-in environments AzureCloud and AzureChinaCloud target existing public instances of Azure Resource Manager.</span></span>

## <span data-ttu-id="53bfb-111">예제</span><span class="sxs-lookup"><span data-stu-id="53bfb-111">EXAMPLES</span></span>

### <span data-ttu-id="53bfb-112">예제 1: 새 환경 만들기 및 수정</span><span class="sxs-lookup"><span data-stu-id="53bfb-112">Example 1: Creating and modifying a new environment</span></span>
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
AzureSynapseAnalyticsEndpointSuffix               :
AzureSynapseAnalyticsEndpointResourceId           :
VersionProfiles                                   : {}
ExtendedProperties                                : {}
BatchEndpointResourceId                           :
```

<span data-ttu-id="53bfb-113">이 예제에서는 Add-AzEnvironment를 사용하여 샘플 엔드포인트가 있는 새 Azure 환경을 만든 다음 Set-AzEnvironment cmdlet을 사용하여 만든 환경의 ActiveDirectoryEndpoint 및 GraphEndpoint 특성 값을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="53bfb-113">In this example we are creating a new Azure environment with sample endpoints using Add-AzEnvironment, and then we are changing the value of the ActiveDirectoryEndpoint and GraphEndpoint attributes of the created environment using the cmdlet Set-AzEnvironment.</span></span>

### <span data-ttu-id="53bfb-114">예제 2: Uri를 통해 새 환경 검색</span><span class="sxs-lookup"><span data-stu-id="53bfb-114">Example 2: Discovering a new environment via Uri</span></span>
```
<#
Uri https://configuredmetadata.net returns an array of environment metadata. The following example contains a payload for the AzureCloud default environment.

[
  {
    "portal": "https://portal.azure.com",
    "authentication": {
      "loginEndpoint": "https://login.microsoftonline.com/",
      "audiences": [
        "https://management.core.windows.net/"
      ],
      "tenant": "common",
      "identityProvider": "AAD"
    },
    "media": "https://rest.media.azure.net",
    "graphAudience": "https://graph.windows.net/",
    "graph": "https://graph.windows.net/",
    "name": "AzureCloud",
    "suffixes": {
      "azureDataLakeStoreFileSystem": "azuredatalakestore.net",
      "acrLoginServer": "azurecr.io",
      "sqlServerHostname": ".database.windows.net",
      "azureDataLakeAnalyticsCatalogAndJob": "azuredatalakeanalytics.net",
      "keyVaultDns": "vault.azure.net",
      "storage": "core.windows.net",
      "azureFrontDoorEndpointSuffix": "azurefd.net"
    },
    "batch": "https://batch.core.windows.net/",
    "resourceManager": "https://management.azure.com/",
    "vmImageAliasDoc": "https://raw.githubusercontent.com/Azure/azure-rest-api-specs/master/arm-compute/quickstart-templates/aliases.json",
    "activeDirectoryDataLake": "https://datalake.azure.net/",
    "sqlManagement": "https://management.core.windows.net:8443/",
    "gallery": "https://gallery.azure.com/"
  },
……
]
#>

PS C:\> Add-AzEnvironment -AutoDiscover -Uri https://configuredmetadata.net

Name            Resource Manager Url ActiveDirectory Authority
----            -------------------- -------------------------
TestEnvironment TestRMEndpoint       TestADEndpoint/
```

<span data-ttu-id="53bfb-115">이 예제에서는 Uri에서 새 Azure 환경을 `https://configuredmetadata.net` 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="53bfb-115">In this example, we are discovering a new Azure environment from the `https://configuredmetadata.net` Uri.</span></span>

## <span data-ttu-id="53bfb-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53bfb-116">PARAMETERS</span></span>

### <span data-ttu-id="53bfb-117">-ActiveDirectoryEndpoint</span><span class="sxs-lookup"><span data-stu-id="53bfb-117">-ActiveDirectoryEndpoint</span></span>
<span data-ttu-id="53bfb-118">Azure Active Directory 인증에 대한 기본 기관을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="53bfb-118">Specifies the base authority for Azure Active Directory authentication.</span></span>

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

### <span data-ttu-id="53bfb-119">-ActiveDirectoryServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="53bfb-119">-ActiveDirectoryServiceEndpointResourceId</span></span>
<span data-ttu-id="53bfb-120">Azure Resource Manager 또는 RDFE(서비스 관리) 엔드포인트에 대한 요청을 인증하는 토큰의 대상을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="53bfb-120">Specifies the audience for tokens that authenticate requests to Azure Resource Manager or Service Management (RDFE) endpoints.</span></span>

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

### <span data-ttu-id="53bfb-121">-AdTenant</span><span class="sxs-lookup"><span data-stu-id="53bfb-121">-AdTenant</span></span>
<span data-ttu-id="53bfb-122">기본 Active Directory 테넌트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="53bfb-122">Specifies the default Active Directory tenant.</span></span>

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

### <span data-ttu-id="53bfb-123">-ARMEndpoint</span><span class="sxs-lookup"><span data-stu-id="53bfb-123">-ARMEndpoint</span></span>
<span data-ttu-id="53bfb-124">Azure Resource Manager 엔드포인트</span><span class="sxs-lookup"><span data-stu-id="53bfb-124">The Azure Resource Manager endpoint</span></span>

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

### <span data-ttu-id="53bfb-125">-AutoDiscover</span><span class="sxs-lookup"><span data-stu-id="53bfb-125">-AutoDiscover</span></span>
<span data-ttu-id="53bfb-126">기본 또는 구성된 엔드포인트를 통해 환경을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="53bfb-126">Discovers environments via default or configured endpoint.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Discovery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53bfb-127">-AzureAnalysisServicesEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="53bfb-127">-AzureAnalysisServicesEndpointResourceId</span></span>
<span data-ttu-id="53bfb-128">Azure Analysis Services 리소스의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="53bfb-128">The resource identifier of the Azure Analysis Services resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53bfb-129">-AzureAnalysisServicesEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="53bfb-129">-AzureAnalysisServicesEndpointSuffix</span></span>
<span data-ttu-id="53bfb-130">Azure Log Analytics API와 통신할 때 사용할 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="53bfb-130">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53bfb-131">-AzureAttestationServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="53bfb-131">-AzureAttestationServiceEndpointResourceId</span></span>
<span data-ttu-id="53bfb-132">요청된 토큰의 받는 사람인 Azure Attestation 서비스의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="53bfb-132">The The resource identifier of the Azure Attestation service that is the recipient of the requested token.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53bfb-133">-AzureAttestationServiceEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="53bfb-133">-AzureAttestationServiceEndpointSuffix</span></span>
<span data-ttu-id="53bfb-134">Azure Attestation 서비스의 Dns 접미사입니다.</span><span class="sxs-lookup"><span data-stu-id="53bfb-134">Dns suffix of Azure Attestation service.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53bfb-135">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="53bfb-135">-AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix</span></span>
<span data-ttu-id="53bfb-136">Azure Data Lake Analytics 작업 및 카탈로그 서비스의 Dns 접미사</span><span class="sxs-lookup"><span data-stu-id="53bfb-136">Dns Suffix of Azure Data Lake Analytics job and catalog services</span></span>

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

### <span data-ttu-id="53bfb-137">-AzureDataLakeStoreFileSystemEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="53bfb-137">-AzureDataLakeStoreFileSystemEndpointSuffix</span></span>
<span data-ttu-id="53bfb-138">Azure Data Lake Store FileSystem의 Dns 접미사입니다.</span><span class="sxs-lookup"><span data-stu-id="53bfb-138">Dns Suffix of Azure Data Lake Store FileSystem.</span></span> <span data-ttu-id="53bfb-139">예: azuredatalake.net</span><span class="sxs-lookup"><span data-stu-id="53bfb-139">Example: azuredatalake.net</span></span>

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

### <span data-ttu-id="53bfb-140">-AzureKeyVaultDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="53bfb-140">-AzureKeyVaultDnsSuffix</span></span>
<span data-ttu-id="53bfb-141">Azure Key Vault 서비스의 Dns 접미사입니다.</span><span class="sxs-lookup"><span data-stu-id="53bfb-141">Dns suffix of Azure Key Vault service.</span></span> <span data-ttu-id="53bfb-142">예제는 vault-int.azure-int.net</span><span class="sxs-lookup"><span data-stu-id="53bfb-142">Example is vault-int.azure-int.net</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53bfb-143">-AzureKeyVaultServiceEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="53bfb-143">-AzureKeyVaultServiceEndpointResourceId</span></span>
<span data-ttu-id="53bfb-144">요청된 토큰의 받는 사람인 Azure Key Vault 데이터 서비스의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="53bfb-144">Resource identifier of Azure Key Vault data service that is the recipient of the requested token.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: 11
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53bfb-145">-AzureOperationalInsightsEndpoint</span><span class="sxs-lookup"><span data-stu-id="53bfb-145">-AzureOperationalInsightsEndpoint</span></span>
<span data-ttu-id="53bfb-146">Azure Log Analytics API와 통신할 때 사용할 엔드포인트입니다.</span><span class="sxs-lookup"><span data-stu-id="53bfb-146">The endpoint to use when communicating with the Azure Log Analytics API.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: 22
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53bfb-147">-AzureOperationalInsightsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="53bfb-147">-AzureOperationalInsightsEndpointResourceId</span></span>
<span data-ttu-id="53bfb-148">Azure Log Analytics API를 사용하여 인증하는 토큰의 대상입니다.</span><span class="sxs-lookup"><span data-stu-id="53bfb-148">The audience for tokens authenticating with the Azure Log Analytics API.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: 21
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53bfb-149">-AzureSynapseAnalyticsEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="53bfb-149">-AzureSynapseAnalyticsEndpointResourceId</span></span>
<span data-ttu-id="53bfb-150">요청된 토큰의 받는 사람인 Azure Synapse Analytics의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="53bfb-150">The The resource identifier of the Azure Synapse Analytics that is the recipient of the requested token.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53bfb-151">-AzureSynapseAnalyticsEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="53bfb-151">-AzureSynapseAnalyticsEndpointSuffix</span></span>
<span data-ttu-id="53bfb-152">Azure Synapse Analytics의 Dns 접미사입니다.</span><span class="sxs-lookup"><span data-stu-id="53bfb-152">Dns suffix of Azure Synapse Analytics.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53bfb-153">-BatchEndpointResourceId</span><span class="sxs-lookup"><span data-stu-id="53bfb-153">-BatchEndpointResourceId</span></span>
<span data-ttu-id="53bfb-154">요청된 토큰의 받는 사람인 Azure Batch 서비스의 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="53bfb-154">The resource identifier of the Azure Batch service that is the recipient of the requested token</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases: BatchResourceId, BatchAudience

Required: False
Position: 20
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53bfb-155">-ContainerRegistryEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="53bfb-155">-ContainerRegistryEndpointSuffix</span></span>
<span data-ttu-id="53bfb-156">Azure Container Registry의 접미사입니다.</span><span class="sxs-lookup"><span data-stu-id="53bfb-156">Suffix of Azure Container Registry.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53bfb-157">-DataLakeAudience</span><span class="sxs-lookup"><span data-stu-id="53bfb-157">-DataLakeAudience</span></span>
<span data-ttu-id="53bfb-158">AD Data Lake 서비스 엔드포인트를 사용하여 인증하는 토큰의 대상입니다.</span><span class="sxs-lookup"><span data-stu-id="53bfb-158">The audience for tokens authenticating with the AD Data Lake services Endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases: DataLakeEndpointResourceId, DataLakeResourceId

Required: False
Position: 19
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53bfb-159">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53bfb-159">-DefaultProfile</span></span>
<span data-ttu-id="53bfb-160">Azure와의 통신에 사용되는 자격 증명, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="53bfb-160">The credentials, tenant and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="53bfb-161">-EnableAdfsAuthentication</span><span class="sxs-lookup"><span data-stu-id="53bfb-161">-EnableAdfsAuthentication</span></span>
<span data-ttu-id="53bfb-162">ADFS(Active Directory Federation Services) 프레미스 인증이 허용된 경우를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="53bfb-162">Indicates that Active Directory Federation Services (ADFS) on-premise authentication is allowed.</span></span>

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

### <span data-ttu-id="53bfb-163">-GalleryEndpoint</span><span class="sxs-lookup"><span data-stu-id="53bfb-163">-GalleryEndpoint</span></span>
<span data-ttu-id="53bfb-164">배포 템플릿의 Azure Resource Manager 갤러리에 대한 엔드포인트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="53bfb-164">Specifies the endpoint for the Azure Resource Manager gallery of deployment templates.</span></span>

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

### <span data-ttu-id="53bfb-165">-GraphAudience</span><span class="sxs-lookup"><span data-stu-id="53bfb-165">-GraphAudience</span></span>
<span data-ttu-id="53bfb-166">AD Graph 엔드포인트를 사용하여 인증하는 토큰의 대상입니다.</span><span class="sxs-lookup"><span data-stu-id="53bfb-166">The audience for tokens authenticating with the AD Graph Endpoint.</span></span>

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

### <span data-ttu-id="53bfb-167">-GraphEndpoint</span><span class="sxs-lookup"><span data-stu-id="53bfb-167">-GraphEndpoint</span></span>
<span data-ttu-id="53bfb-168">Graph(Active Directory 메타데이터) 요청에 대한 URL을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="53bfb-168">Specifies the URL for Graph (Active Directory metadata) requests.</span></span>

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

### <span data-ttu-id="53bfb-169">-ManagementPortalUrl</span><span class="sxs-lookup"><span data-stu-id="53bfb-169">-ManagementPortalUrl</span></span>
<span data-ttu-id="53bfb-170">관리 포털의 URL을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="53bfb-170">Specifies the URL for the Management Portal.</span></span>

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

### <span data-ttu-id="53bfb-171">-Name</span><span class="sxs-lookup"><span data-stu-id="53bfb-171">-Name</span></span>
<span data-ttu-id="53bfb-172">추가할 환경의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="53bfb-172">Specifies the name of the environment to add.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53bfb-173">-PublishSettingsFileUrl</span><span class="sxs-lookup"><span data-stu-id="53bfb-173">-PublishSettingsFileUrl</span></span>
<span data-ttu-id="53bfb-174">.publishsettings 파일을 다운로드할 수 있는 URL을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="53bfb-174">Specifies the URL from which .publishsettings files can be downloaded.</span></span>

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

### <span data-ttu-id="53bfb-175">-ResourceManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="53bfb-175">-ResourceManagerEndpoint</span></span>
<span data-ttu-id="53bfb-176">Azure Resource Manager 요청에 대한 URL을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="53bfb-176">Specifies the URL for Azure Resource Manager requests.</span></span>

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

### <span data-ttu-id="53bfb-177">-Scope</span><span class="sxs-lookup"><span data-stu-id="53bfb-177">-Scope</span></span>
<span data-ttu-id="53bfb-178">컨텍스트 변경 범위(예: 변경 내용이 현재 프로세스에만 적용되는지 또는 이 사용자가 시작한 모든 세션에 적용되는지 여부)를 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="53bfb-178">Determines the scope of context changes, for example, whether changes apply only to the current process, or to all sessions started by this user.</span></span>

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

### <span data-ttu-id="53bfb-179">-ServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="53bfb-179">-ServiceEndpoint</span></span>
<span data-ttu-id="53bfb-180">RDFE(서비스 관리) 요청에 대한 엔드포인트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="53bfb-180">Specifies the endpoint for Service Management (RDFE) requests.</span></span>

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

### <span data-ttu-id="53bfb-181">-SqlDatabaseDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="53bfb-181">-SqlDatabaseDnsSuffix</span></span>
<span data-ttu-id="53bfb-182">Azure SQL Database 서버에 대한 도메인 이름 접미사를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="53bfb-182">Specifies the domain-name suffix for Azure SQL Database servers.</span></span>

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

### <span data-ttu-id="53bfb-183">-StorageEndpoint</span><span class="sxs-lookup"><span data-stu-id="53bfb-183">-StorageEndpoint</span></span>
<span data-ttu-id="53bfb-184">저장소(Blob, 테이블, 큐 및 파일) 액세스에 대한 엔드포인트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="53bfb-184">Specifies the endpoint for storage (blob, table, queue, and file) access.</span></span>

```yaml
Type: System.String
Parameter Sets: Name, ARMEndpoint
Aliases: StorageEndpointSuffix

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53bfb-185">-TrafficManagerDnsSuffix</span><span class="sxs-lookup"><span data-stu-id="53bfb-185">-TrafficManagerDnsSuffix</span></span>
<span data-ttu-id="53bfb-186">Azure Traffic Manager 서비스에 대한 도메인 이름 접미사를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="53bfb-186">Specifies the domain-name suffix for Azure Traffic Manager services.</span></span>

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

### <span data-ttu-id="53bfb-187">-Uri</span><span class="sxs-lookup"><span data-stu-id="53bfb-187">-Uri</span></span>
<span data-ttu-id="53bfb-188">환경을 인치할 인터넷 리소스의 URI를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="53bfb-188">Specifies URI of the internet resource to fetch environments.</span></span>

```yaml
Type: System.Uri
Parameter Sets: Discovery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53bfb-189">-Confirm</span><span class="sxs-lookup"><span data-stu-id="53bfb-189">-Confirm</span></span>
<span data-ttu-id="53bfb-190">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="53bfb-190">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53bfb-191">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53bfb-191">-WhatIf</span></span>
<span data-ttu-id="53bfb-192">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="53bfb-192">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="53bfb-193">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="53bfb-193">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53bfb-194">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53bfb-194">CommonParameters</span></span>
<span data-ttu-id="53bfb-195">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="53bfb-195">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53bfb-196">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="53bfb-196">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53bfb-197">입력</span><span class="sxs-lookup"><span data-stu-id="53bfb-197">INPUTS</span></span>

### <span data-ttu-id="53bfb-198">System.String</span><span class="sxs-lookup"><span data-stu-id="53bfb-198">System.String</span></span>

### <span data-ttu-id="53bfb-199">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="53bfb-199">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="53bfb-200">출력</span><span class="sxs-lookup"><span data-stu-id="53bfb-200">OUTPUTS</span></span>

### <span data-ttu-id="53bfb-201">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="53bfb-201">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="53bfb-202">참고 사항</span><span class="sxs-lookup"><span data-stu-id="53bfb-202">NOTES</span></span>

## <span data-ttu-id="53bfb-203">관련 링크</span><span class="sxs-lookup"><span data-stu-id="53bfb-203">RELATED LINKS</span></span>

[<span data-ttu-id="53bfb-204">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="53bfb-204">Get-AzEnvironment</span></span>](./Get-AzEnvironment.md)

[<span data-ttu-id="53bfb-205">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="53bfb-205">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

[<span data-ttu-id="53bfb-206">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="53bfb-206">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

