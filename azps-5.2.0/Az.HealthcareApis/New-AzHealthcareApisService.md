---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/new-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/New-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/New-AzHealthcareApisService.md
ms.openlocfilehash: 33f1af70b0fef7e89ccb584ed3b69f32e2810690
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368775"
---
# <span data-ttu-id="e1b7d-101">New-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="e1b7d-101">New-AzHealthcareApisService</span></span>

## <span data-ttu-id="e1b7d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1b7d-102">SYNOPSIS</span></span>
<span data-ttu-id="e1b7d-103">서비스 인스턴스의 메타데이터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e1b7d-103">Creates the metadata of a service instance.</span></span>

## <span data-ttu-id="e1b7d-104">구문</span><span class="sxs-lookup"><span data-stu-id="e1b7d-104">SYNTAX</span></span>

```
New-AzHealthcareApisService -Name <String> -ResourceGroupName <String> -Location <String> [-Kind <String>]
 [-AccessPolicyObjectId <String[]>] [-AllowCorsCredential] [-Audience <String>] [-Authority <String>]
 [-CorsHeader <String[]>] [-CorsMaxAge <Int32>] [-CorsMethod <String[]>] [-CorsOrigin <String[]>]
 [-CosmosOfferThroughput <Int32>] [-CosmosKeyVaultKeyUri <String>] [-ExportStorageAccountName <String>]
 [-EnableSmartProxy] [-ManagedIdentity] [-FhirVersion <String>] [-Tag <Hashtable>] [-AsJob]
 [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e1b7d-105">설명</span><span class="sxs-lookup"><span data-stu-id="e1b7d-105">DESCRIPTION</span></span>
<span data-ttu-id="e1b7d-106">서비스 인스턴스의 메타데이터를 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e1b7d-106">Creates or updates the metadata of a service instance.</span></span>

## <span data-ttu-id="e1b7d-107">예제</span><span class="sxs-lookup"><span data-stu-id="e1b7d-107">EXAMPLES</span></span>

### <span data-ttu-id="e1b7d-108">예제 1: cosmosdb 제품 프로비전이 400인 location westus2의 리소스 그룹 MyResourceGroup에 MyService라는 새 Azure Healthcareapis fhir 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e1b7d-108">Example 1 : Creates a new Azure healthcareapis fhir service named MyService in the resource group MyResourceGroup in a location westus2 with cosmosdb offer throughput = 400</span></span>
```powershell
PS C:\> New-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup -Location MyLocation -Kind fhir-R4 -CosmosOfferThroughput 400

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbKeyVaultKeyUri  : 
CosmosDbOfferThroughput : 400
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

### <span data-ttu-id="e1b7d-109">예제 2: cosmosdb 제품 서비스량 = 400 및 키 자격 증명 모음 키 uri "https:// .vault.azure.net/keys/" 키를 사용하여 westus2의 리소스 그룹 MyResourceGroup에 MyService라는 새 Azure Healthcareapis fhir 서비스를 만듭니다. \<my-keyvault> \<my-key></span><span class="sxs-lookup"><span data-stu-id="e1b7d-109">Example 2 : Creates a new Azure healthcareapis fhir service named MyService in the resource group MyResourceGroup in a location westus2 with cosmosdb offer throughput = 400 and key vault key uri "https://\<my-keyvault>.vault.azure.net/keys/\<my-key>"</span></span>
```powershell
PS C:\> New-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup -Location MyLocation -Kind fhir-R4 -CosmosOfferThroughput 400 -CosmosKeyVaultKeyUri "https://<my-keyvault>.vault.azure.net/keys/<my-key>"

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbKeyVaultKeyUri  : https://<my-keyvault>.vault.azure.net/keys/<my-key>
CosmosDbOfferThroughput : 400
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

## <span data-ttu-id="e1b7d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1b7d-110">PARAMETERS</span></span>

### <span data-ttu-id="e1b7d-111">-AccessPolicyObjectId</span><span class="sxs-lookup"><span data-stu-id="e1b7d-111">-AccessPolicyObjectId</span></span>
<span data-ttu-id="e1b7d-112">액세스 정책 개체의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="e1b7d-112">List of Access Policy Object IDs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1b7d-113">-AllowCorsCredential</span><span class="sxs-lookup"><span data-stu-id="e1b7d-113">-AllowCorsCredential</span></span>
<span data-ttu-id="e1b7d-114">HealthcareApis Fhir Service AllowCorsCredentials.</span><span class="sxs-lookup"><span data-stu-id="e1b7d-114">HealthcareApis Fhir Service AllowCorsCredentials.</span></span>

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

### <span data-ttu-id="e1b7d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e1b7d-115">-AsJob</span></span>
<span data-ttu-id="e1b7d-116">백그라운드에서 작업으로 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e1b7d-116">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="e1b7d-117">-Audience</span><span class="sxs-lookup"><span data-stu-id="e1b7d-117">-Audience</span></span>
<span data-ttu-id="e1b7d-118">HealthcareApis Fhir 서비스 대상.</span><span class="sxs-lookup"><span data-stu-id="e1b7d-118">HealthcareApis Fhir Service Audience.</span></span>

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

### <span data-ttu-id="e1b7d-119">-Authority</span><span class="sxs-lookup"><span data-stu-id="e1b7d-119">-Authority</span></span>
<span data-ttu-id="e1b7d-120">HealthcareApis Fhir Service Authority.</span><span class="sxs-lookup"><span data-stu-id="e1b7d-120">HealthcareApis Fhir Service Authority.</span></span>

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

### <span data-ttu-id="e1b7d-121">-CorsHeader</span><span class="sxs-lookup"><span data-stu-id="e1b7d-121">-CorsHeader</span></span>
<span data-ttu-id="e1b7d-122">HealthcareApis Fhir 서비스 목록 Cors 헤더입니다.</span><span class="sxs-lookup"><span data-stu-id="e1b7d-122">HealthcareApis Fhir Service List of Cors Header.</span></span>
<span data-ttu-id="e1b7d-123">요청 중에 사용할 수 있는 HTTP 헤더를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e1b7d-123">Specify HTTP headers which can be used during the request.</span></span>
<span data-ttu-id="e1b7d-124">모든 헤더에 " \* "를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1b7d-124">Use " \* " for any header.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1b7d-125">-CorsMaxAge</span><span class="sxs-lookup"><span data-stu-id="e1b7d-125">-CorsMaxAge</span></span>
<span data-ttu-id="e1b7d-126">HealthcareApis Fhir Service Cors Max Age.</span><span class="sxs-lookup"><span data-stu-id="e1b7d-126">HealthcareApis Fhir Service Cors Max Age.</span></span>
<span data-ttu-id="e1b7d-127">요청의 결과를 몇 초 만에 캐시할 수 있는 기간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e1b7d-127">Specify how long a result from a request can be cached in seconds.</span></span>
<span data-ttu-id="e1b7d-128">예: 600은 10분을 의미합니다.</span><span class="sxs-lookup"><span data-stu-id="e1b7d-128">Example: 600 means 10 minutes.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1b7d-129">-CorsMethod</span><span class="sxs-lookup"><span data-stu-id="e1b7d-129">-CorsMethod</span></span>
<span data-ttu-id="e1b7d-130">HealthcareApis Fhir 서비스 Cors 메서드 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="e1b7d-130">HealthcareApis Fhir Service List of Cors Method.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1b7d-131">-CorsOrigin</span><span class="sxs-lookup"><span data-stu-id="e1b7d-131">-CorsOrigin</span></span>
<span data-ttu-id="e1b7d-132">Cors Origin의 HealthcareApis Fhir 서비스 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="e1b7d-132">HealthcareApis Fhir Service List of Cors Origin.</span></span>
<span data-ttu-id="e1b7d-133">이 API에 액세스할 수 있는 원본 사이트의 URL을 지정하거나 " \* "를 사용하여 모든 사이트에서 액세스를 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="e1b7d-133">Specify URLs of origin sites that can access this API, or use " \* " to allow access from any site.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1b7d-134">-CosmosKeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="e1b7d-134">-CosmosKeyVaultKeyUri</span></span>
<span data-ttu-id="e1b7d-135">HealthcareApis Fhir Service CosmosKeyVaultKeyUri.</span><span class="sxs-lookup"><span data-stu-id="e1b7d-135">HealthcareApis Fhir Service CosmosKeyVaultKeyUri.</span></span>
<span data-ttu-id="e1b7d-136">백업 데이터베이스에 대한 고객 관리 키의 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="e1b7d-136">The URI of the customer-managed key for the backing database.</span></span>

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

### <span data-ttu-id="e1b7d-137">-CosmosOfferThroughput</span><span class="sxs-lookup"><span data-stu-id="e1b7d-137">-CosmosOfferThroughput</span></span>
<span data-ttu-id="e1b7d-138">HealthcareApis Fhir Service CosmosOfferThroughput.</span><span class="sxs-lookup"><span data-stu-id="e1b7d-138">HealthcareApis Fhir Service CosmosOfferThroughput.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1b7d-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1b7d-139">-DefaultProfile</span></span>
<span data-ttu-id="e1b7d-140">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e1b7d-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1b7d-141">-EnableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="e1b7d-141">-EnableSmartProxy</span></span>
<span data-ttu-id="e1b7d-142">HealthcareApis Fhir Service EnableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="e1b7d-142">HealthcareApis Fhir Service EnableSmartProxy.</span></span>

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

### <span data-ttu-id="e1b7d-143">-ExportStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="e1b7d-143">-ExportStorageAccountName</span></span>
<span data-ttu-id="e1b7d-144">HealthcareApis Fhir Service 내보내기 저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e1b7d-144">HealthcareApis Fhir Service Export Storage Account Name.</span></span>

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

### <span data-ttu-id="e1b7d-145">-FhirVersion</span><span class="sxs-lookup"><span data-stu-id="e1b7d-145">-FhirVersion</span></span>
<span data-ttu-id="e1b7d-146">Fhir 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="e1b7d-146">Fhir Version.</span></span>

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

### <span data-ttu-id="e1b7d-147">-Kind</span><span class="sxs-lookup"><span data-stu-id="e1b7d-147">-Kind</span></span>
<span data-ttu-id="e1b7d-148">HealthcareApis 서비스의 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="e1b7d-148">Kind of HealthcareApis Service.</span></span>
<span data-ttu-id="e1b7d-149">기본값은 Fhir입니다.</span><span class="sxs-lookup"><span data-stu-id="e1b7d-149">The default value is Fhir</span></span>

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

### <span data-ttu-id="e1b7d-150">-Location</span><span class="sxs-lookup"><span data-stu-id="e1b7d-150">-Location</span></span>
<span data-ttu-id="e1b7d-151">HealthcareApis 서비스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="e1b7d-151">HealthcareApis Service Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1b7d-152">-ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="e1b7d-152">-ManagedIdentity</span></span>
<span data-ttu-id="e1b7d-153">관리 ID를 사용하나요?</span><span class="sxs-lookup"><span data-stu-id="e1b7d-153">Use Managed Identity?</span></span>

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

### <span data-ttu-id="e1b7d-154">-Name</span><span class="sxs-lookup"><span data-stu-id="e1b7d-154">-Name</span></span>
<span data-ttu-id="e1b7d-155">HealthcareApis 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e1b7d-155">HealthcareApis Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1b7d-156">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="e1b7d-156">-PublicNetworkAccess</span></span>
<span data-ttu-id="e1b7d-157">Fhir 서비스에 대한 네트워크 액세스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="e1b7d-157">The network access type for Fhir service.</span></span> <span data-ttu-id="e1b7d-158">일반적으로 `Enabled` 또는 `Disabled` .</span><span class="sxs-lookup"><span data-stu-id="e1b7d-158">Commonly `Enabled` or `Disabled`.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1b7d-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1b7d-159">-ResourceGroupName</span></span>
<span data-ttu-id="e1b7d-160">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e1b7d-160">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1b7d-161">-Tag</span><span class="sxs-lookup"><span data-stu-id="e1b7d-161">-Tag</span></span>
<span data-ttu-id="e1b7d-162">HealthcareApis Fhir 서비스 계정 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="e1b7d-162">HealthcareApis Fhir Service Account Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1b7d-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e1b7d-163">-Confirm</span></span>
<span data-ttu-id="e1b7d-164">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e1b7d-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1b7d-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1b7d-165">-WhatIf</span></span>
<span data-ttu-id="e1b7d-166">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e1b7d-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1b7d-167">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e1b7d-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1b7d-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1b7d-168">CommonParameters</span></span>
<span data-ttu-id="e1b7d-169">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e1b7d-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1b7d-170">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e1b7d-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1b7d-171">입력</span><span class="sxs-lookup"><span data-stu-id="e1b7d-171">INPUTS</span></span>

### <span data-ttu-id="e1b7d-172">System.String</span><span class="sxs-lookup"><span data-stu-id="e1b7d-172">System.String</span></span>

## <span data-ttu-id="e1b7d-173">출력</span><span class="sxs-lookup"><span data-stu-id="e1b7d-173">OUTPUTS</span></span>

### <span data-ttu-id="e1b7d-174">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="e1b7d-174">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="e1b7d-175">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e1b7d-175">NOTES</span></span>

## <span data-ttu-id="e1b7d-176">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e1b7d-176">RELATED LINKS</span></span>
