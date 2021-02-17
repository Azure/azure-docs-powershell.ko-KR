---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/set-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Set-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Set-AzHealthcareApisService.md
ms.openlocfilehash: c8eb7c58300e3252422d8b599422a3a14eb5c1fe
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192476"
---
# <span data-ttu-id="14726-101">Set-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="14726-101">Set-AzHealthcareApisService</span></span>

## <span data-ttu-id="14726-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14726-102">SYNOPSIS</span></span>
<span data-ttu-id="14726-103">기존 HealthcareApis fhir 서비스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="14726-103">Updates an existing healthcareApis fhir service.</span></span>

## <span data-ttu-id="14726-104">구문</span><span class="sxs-lookup"><span data-stu-id="14726-104">SYNTAX</span></span>

### <span data-ttu-id="14726-105">ServiceNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="14726-105">ServiceNameParameterSet (Default)</span></span>
```
Set-AzHealthcareApisService -Name <String> -ResourceGroupName <String> [-CosmosOfferThroughput <Int32>]
 [-CosmosKeyVaultKeyUri <String>] [-Authority <String>] [-Audience <String>] [-EnableSmartProxy]
 [-DisableSmartProxy] [-CorsOrigin <String[]>] [-CorsHeader <String[]>] [-CorsMethod <String[]>]
 [-CorsMaxAge <Int32>] [-AllowCorsCredential] [-DisableCorsCredential] [-ExportStorageAccountName <String>]
 [-AccessPolicyObjectId <String[]>] [-EnableManagedIdentity] [-DisableManagedIdentity] [-Tag <Hashtable>]
 [-AsJob] [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="14726-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="14726-106">ResourceIdParameterSet</span></span>
```
Set-AzHealthcareApisService [-CosmosOfferThroughput <Int32>] [-CosmosKeyVaultKeyUri <String>]
 [-Authority <String>] [-Audience <String>] [-EnableSmartProxy] [-DisableSmartProxy] [-CorsOrigin <String[]>]
 [-CorsHeader <String[]>] [-CorsMethod <String[]>] [-CorsMaxAge <Int32>] [-AllowCorsCredential]
 [-DisableCorsCredential] [-ExportStorageAccountName <String>] [-AccessPolicyObjectId <String[]>]
 [-EnableManagedIdentity] [-DisableManagedIdentity] [-Tag <Hashtable>] -ResourceId <String> [-AsJob]
 [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="14726-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="14726-107">InputObjectParameterSet</span></span>
```
Set-AzHealthcareApisService -InputObject <PSHealthcareApisService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14726-108">설명</span><span class="sxs-lookup"><span data-stu-id="14726-108">DESCRIPTION</span></span>
<span data-ttu-id="14726-109">기존 HealthcareApis fhir 서비스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="14726-109">Updates an existing healthcareApis fhir service.</span></span>

## <span data-ttu-id="14726-110">예제</span><span class="sxs-lookup"><span data-stu-id="14726-110">EXAMPLES</span></span>

### <span data-ttu-id="14726-111">예제 1: 리소스 그룹 MyResourceGroup의 MyService라는 기존 Healthcareapis 서비스를 cosmosdb OfferThroughput = 500으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="14726-111">Example 1 : Updates the existing healthcareapis service named MyService in the resource group MyResourceGroup  with the cosmosdb OfferThroughput = 500.</span></span>

```powershell
PS C:\> Set-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup -CosmosOfferThroughput 500

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosKeyVaultKeyUri    : 
CosmosDbOfferThroughput : 500
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False
```

### <span data-ttu-id="14726-112">예제 2: Cosmosdb OfferThroughput = 500 및 키 자격 증명 모음 키 URI "https:// \<my-keyvault> .vault.azure.net/keys/" 리소스 그룹 MyResourceGroup의 MyService라는 기존 의료 서비스 업데이트 \<my-key></span><span class="sxs-lookup"><span data-stu-id="14726-112">Example 2: Updates the existing healthcareapis service named MyService in the resource group MyResourceGroup  with the cosmosdb OfferThroughput = 500 and key vault key uri "https://\<my-keyvault>.vault.azure.net/keys/\<my-key>"</span></span>

```powershell
PS C:\> $ResourceId = "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.HealthcareApis/services/MyService"
PS C:\> Set-AzHealthcareApisService -ResourceId $ResourceId  -CosmosOfferThroughput 500 -CosmosKeyVaultKeyUri "https://<my-keyvault>.vault.azure.net/keys/<my-key>"

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosKeyVaultKeyUri    : https://<my-keyvault>.vault.azure.net/keys/<my-key>
CosmosDbOfferThroughput : 500
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False
```

## <span data-ttu-id="14726-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14726-113">PARAMETERS</span></span>

### <span data-ttu-id="14726-114">-AccessPolicyObjectId</span><span class="sxs-lookup"><span data-stu-id="14726-114">-AccessPolicyObjectId</span></span>
<span data-ttu-id="14726-115">액세스 정책 개체의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="14726-115">List of Access Policy Object IDs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14726-116">-AllowCorsCredential</span><span class="sxs-lookup"><span data-stu-id="14726-116">-AllowCorsCredential</span></span>
<span data-ttu-id="14726-117">HealthcareApis FhirService AllowCorsCredential.</span><span class="sxs-lookup"><span data-stu-id="14726-117">HealthcareApis FhirService AllowCorsCredential.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14726-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="14726-118">-AsJob</span></span>
<span data-ttu-id="14726-119">백그라운드에서 작업으로 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="14726-119">Run cmdlet as a job in the background.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14726-120">-Audience</span><span class="sxs-lookup"><span data-stu-id="14726-120">-Audience</span></span>
<span data-ttu-id="14726-121">HealthcareApis FhirService 대상.</span><span class="sxs-lookup"><span data-stu-id="14726-121">HealthcareApis FhirService Audience.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14726-122">-Authority</span><span class="sxs-lookup"><span data-stu-id="14726-122">-Authority</span></span>
<span data-ttu-id="14726-123">HealthcareApis FhirService Authority.</span><span class="sxs-lookup"><span data-stu-id="14726-123">HealthcareApis FhirService Authority.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14726-124">-CorsHeader</span><span class="sxs-lookup"><span data-stu-id="14726-124">-CorsHeader</span></span>
<span data-ttu-id="14726-125">HealthcareApis FhirService Cors 헤더 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="14726-125">HealthcareApis FhirService List of Cors Headers.</span></span>
<span data-ttu-id="14726-126">요청 중에 사용할 수 있는 HTTP 헤더를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="14726-126">Specify HTTP headers which can be used during the request.</span></span>
<span data-ttu-id="14726-127">모든 헤더에 " \* "를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="14726-127">Use " \* " for any header.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14726-128">-CorsMaxAge</span><span class="sxs-lookup"><span data-stu-id="14726-128">-CorsMaxAge</span></span>
<span data-ttu-id="14726-129">HealthcareApis FhirService Cors Max Age.</span><span class="sxs-lookup"><span data-stu-id="14726-129">HealthcareApis FhirService Cors Max Age.</span></span>
<span data-ttu-id="14726-130">요청의 결과를 몇 초 만에 캐시할 수 있는 기간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="14726-130">Specify how long a result from a request can be cached in seconds.</span></span>
<span data-ttu-id="14726-131">예: 600은 10분을 의미합니다.</span><span class="sxs-lookup"><span data-stu-id="14726-131">Example: 600 means 10 minutes.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14726-132">-CorsMethod</span><span class="sxs-lookup"><span data-stu-id="14726-132">-CorsMethod</span></span>
<span data-ttu-id="14726-133">HealthcareApis FhirService Cors 메서드 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="14726-133">HealthcareApis FhirService List of Cors Methods.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14726-134">-CorsOrigin</span><span class="sxs-lookup"><span data-stu-id="14726-134">-CorsOrigin</span></span>
<span data-ttu-id="14726-135">HealthcareApis FhirService Cors Origins 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="14726-135">HealthcareApis FhirService List of Cors Origins.</span></span>
<span data-ttu-id="14726-136">이 API에 액세스할 수 있는 원본 사이트의 URL을 지정하거나 " \* "를 사용하여 모든 사이트에서 액세스를 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="14726-136">Specify URLs of origin sites that can access this API, or use " \* " to allow access from any site.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14726-137">-CosmosKeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="14726-137">-CosmosKeyVaultKeyUri</span></span>
<span data-ttu-id="14726-138">HealthcareApis Fhir Service CosmosKeyVaultKeyUri.</span><span class="sxs-lookup"><span data-stu-id="14726-138">HealthcareApis Fhir Service CosmosKeyVaultKeyUri.</span></span>
<span data-ttu-id="14726-139">백업 데이터베이스에 대한 고객 관리 키의 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="14726-139">The URI of the customer-managed key for the backing database.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14726-140">-CosmosOfferThroughput</span><span class="sxs-lookup"><span data-stu-id="14726-140">-CosmosOfferThroughput</span></span>
<span data-ttu-id="14726-141">HealthcareApis FhirService CosmosOfferThroughput.</span><span class="sxs-lookup"><span data-stu-id="14726-141">HealthcareApis FhirService CosmosOfferThroughput.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14726-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14726-142">-DefaultProfile</span></span>
<span data-ttu-id="14726-143">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="14726-143">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14726-144">-DisableCorsCredential</span><span class="sxs-lookup"><span data-stu-id="14726-144">-DisableCorsCredential</span></span>
<span data-ttu-id="14726-145">HealthcareApis FhirService CorsCredentials 허용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="14726-145">HealthcareApis FhirService CorsCredentials Not Allowed.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14726-146">-DisableManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="14726-146">-DisableManagedIdentity</span></span>
<span data-ttu-id="14726-147">관리 ID를 사용하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="14726-147">Disable Managed Identity.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14726-148">-DisableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="14726-148">-DisableSmartProxy</span></span>
<span data-ttu-id="14726-149">HealthcareApis FhirService DisableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="14726-149">HealthcareApis FhirService DisableSmartProxy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14726-150">-EnableManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="14726-150">-EnableManagedIdentity</span></span>
<span data-ttu-id="14726-151">관리 ID를 사용하도록 설정</span><span class="sxs-lookup"><span data-stu-id="14726-151">Enable Managed Identity.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14726-152">-EnableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="14726-152">-EnableSmartProxy</span></span>
<span data-ttu-id="14726-153">HealthcareApis FhirService EnableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="14726-153">HealthcareApis FhirService EnableSmartProxy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14726-154">-ExportStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="14726-154">-ExportStorageAccountName</span></span>
<span data-ttu-id="14726-155">HealthcareApis Fhir Service 내보내기 저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="14726-155">HealthcareApis Fhir Service Export Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14726-156">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14726-156">-InputObject</span></span>
<span data-ttu-id="14726-157">Get-AzHealthcareApisFhirService에서 파이프된 HealthcareApis fhir 서비스입니다.</span><span class="sxs-lookup"><span data-stu-id="14726-157">HealthcareApis fhir service piped from Get-AzHealthcareApisFhirService.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14726-158">-Name</span><span class="sxs-lookup"><span data-stu-id="14726-158">-Name</span></span>
<span data-ttu-id="14726-159">HealthcareApis 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="14726-159">HealthcareApis Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14726-160">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="14726-160">-PublicNetworkAccess</span></span>
<span data-ttu-id="14726-161">Fhir 서비스에 대한 네트워크 액세스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="14726-161">The network access type for Fhir service.</span></span> <span data-ttu-id="14726-162">일반적으로 `Enabled` 또는 `Disabled` .</span><span class="sxs-lookup"><span data-stu-id="14726-162">Commonly `Enabled` or `Disabled`.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14726-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14726-163">-ResourceGroupName</span></span>
<span data-ttu-id="14726-164">HealthcareApis 서비스 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="14726-164">HealthcareApis Service Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14726-165">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14726-165">-ResourceId</span></span>
<span data-ttu-id="14726-166">HealthcareApis Fhir Service ResourceId.</span><span class="sxs-lookup"><span data-stu-id="14726-166">HealthcareApis Fhir Service ResourceId.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14726-167">-Tag</span><span class="sxs-lookup"><span data-stu-id="14726-167">-Tag</span></span>
<span data-ttu-id="14726-168">HealthcareApis Fhir 서비스 계정 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="14726-168">HealthcareApis Fhir Service Account Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14726-169">-Confirm</span><span class="sxs-lookup"><span data-stu-id="14726-169">-Confirm</span></span>
<span data-ttu-id="14726-170">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="14726-170">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14726-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14726-171">-WhatIf</span></span>
<span data-ttu-id="14726-172">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="14726-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14726-173">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="14726-173">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14726-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14726-174">CommonParameters</span></span>
<span data-ttu-id="14726-175">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="14726-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14726-176">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="14726-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14726-177">입력</span><span class="sxs-lookup"><span data-stu-id="14726-177">INPUTS</span></span>

### <span data-ttu-id="14726-178">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="14726-178">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span></span>

### <span data-ttu-id="14726-179">System.String</span><span class="sxs-lookup"><span data-stu-id="14726-179">System.String</span></span>

## <span data-ttu-id="14726-180">출력</span><span class="sxs-lookup"><span data-stu-id="14726-180">OUTPUTS</span></span>

### <span data-ttu-id="14726-181">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="14726-181">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="14726-182">참고 사항</span><span class="sxs-lookup"><span data-stu-id="14726-182">NOTES</span></span>

## <span data-ttu-id="14726-183">관련 링크</span><span class="sxs-lookup"><span data-stu-id="14726-183">RELATED LINKS</span></span>
