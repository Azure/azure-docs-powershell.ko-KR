---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/powershell/module/az.healthcareapis/new-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/New-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/New-AzHealthcareApisService.md
ms.openlocfilehash: e99c060cc7446cbecc46040ec4a498cf9f545e7b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013179"
---
# <span data-ttu-id="32907-101">New-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="32907-101">New-AzHealthcareApisService</span></span>

## <span data-ttu-id="32907-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32907-102">SYNOPSIS</span></span>
<span data-ttu-id="32907-103">서비스 인스턴스의 메타데이터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="32907-103">Creates the metadata of a service instance.</span></span>

## <span data-ttu-id="32907-104">구문</span><span class="sxs-lookup"><span data-stu-id="32907-104">SYNTAX</span></span>

```
New-AzHealthcareApisService -Name <String> -ResourceGroupName <String> -Location <String> [-Kind <String>]
 [-AccessPolicyObjectId <String[]>] [-AllowCorsCredential] [-Audience <String>] [-Authority <String>]
 [-CorsHeader <String[]>] [-CorsMaxAge <Int32>] [-CorsMethod <String[]>] [-CorsOrigin <String[]>]
 [-CosmosOfferThroughput <Int32>] [-CosmosKeyVaultKeyUri <String>] [-ExportStorageAccountName <String>]
 [-EnableSmartProxy] [-ManagedIdentity] [-FhirVersion <String>] [-Tag <Hashtable>] [-AsJob]
 [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="32907-105">설명</span><span class="sxs-lookup"><span data-stu-id="32907-105">DESCRIPTION</span></span>
<span data-ttu-id="32907-106">서비스 인스턴스의 메타데이터를 만들거나 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="32907-106">Creates or updates the metadata of a service instance.</span></span>

## <span data-ttu-id="32907-107">예제</span><span class="sxs-lookup"><span data-stu-id="32907-107">EXAMPLES</span></span>

### <span data-ttu-id="32907-108">예제 1 : cosmosdb 제품 프로비전을 사용하여 위치 westus2의 리소스 그룹 MyResourceGroup에서 MyService라는 새 Azure Healthcareapis fhir 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="32907-108">Example 1 : Creates a new Azure healthcareapis fhir service named MyService in the resource group MyResourceGroup in a location westus2 with cosmosdb offer throughput = 400</span></span>
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

### <span data-ttu-id="32907-109">예제 2 : cosmosdb 제품 프로비전 = 400 및 키 자격 증명 모음 키 uri "https:// .vault.azure.net/keys/ " 로 위치 westus2의 리소스 그룹 MyResourceGroup에서 MyService라는 새 Azure healthcareapis fhir \<my-keyvault> 서비스를 \<my-key> 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="32907-109">Example 2 : Creates a new Azure healthcareapis fhir service named MyService in the resource group MyResourceGroup in a location westus2 with cosmosdb offer throughput = 400 and key vault key uri "https://\<my-keyvault>.vault.azure.net/keys/\<my-key>"</span></span>
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

## <span data-ttu-id="32907-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="32907-110">PARAMETERS</span></span>

### <span data-ttu-id="32907-111">-AccessPolicyObjectId</span><span class="sxs-lookup"><span data-stu-id="32907-111">-AccessPolicyObjectId</span></span>
<span data-ttu-id="32907-112">액세스 정책 개체 아이디 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="32907-112">List of Access Policy Object IDs.</span></span>

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

### <span data-ttu-id="32907-113">-AllowCorsCredential</span><span class="sxs-lookup"><span data-stu-id="32907-113">-AllowCorsCredential</span></span>
<span data-ttu-id="32907-114">HealthcareApis Fhir Service AllowCorsCredentials.</span><span class="sxs-lookup"><span data-stu-id="32907-114">HealthcareApis Fhir Service AllowCorsCredentials.</span></span>

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

### <span data-ttu-id="32907-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="32907-115">-AsJob</span></span>
<span data-ttu-id="32907-116">백그라운드에서 작업으로 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="32907-116">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="32907-117">-Audience</span><span class="sxs-lookup"><span data-stu-id="32907-117">-Audience</span></span>
<span data-ttu-id="32907-118">HealthcareApis Fhir Service Audience.</span><span class="sxs-lookup"><span data-stu-id="32907-118">HealthcareApis Fhir Service Audience.</span></span>

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

### <span data-ttu-id="32907-119">-Authority</span><span class="sxs-lookup"><span data-stu-id="32907-119">-Authority</span></span>
<span data-ttu-id="32907-120">HealthcareApis Fhir Service Authority.</span><span class="sxs-lookup"><span data-stu-id="32907-120">HealthcareApis Fhir Service Authority.</span></span>

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

### <span data-ttu-id="32907-121">-CorsHeader</span><span class="sxs-lookup"><span data-stu-id="32907-121">-CorsHeader</span></span>
<span data-ttu-id="32907-122">HealthcareApis Fhir Cors 헤더의 서비스 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="32907-122">HealthcareApis Fhir Service List of Cors Header.</span></span>
<span data-ttu-id="32907-123">요청 중에 사용할 수 있는 HTTP 헤더를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="32907-123">Specify HTTP headers which can be used during the request.</span></span>
<span data-ttu-id="32907-124">모든 헤더에 "\* " 를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="32907-124">Use " \* " for any header.</span></span>

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

### <span data-ttu-id="32907-125">-CorsMaxAge</span><span class="sxs-lookup"><span data-stu-id="32907-125">-CorsMaxAge</span></span>
<span data-ttu-id="32907-126">HealthcareApis Fhir Service Cors Max Age</span><span class="sxs-lookup"><span data-stu-id="32907-126">HealthcareApis Fhir Service Cors Max Age.</span></span>
<span data-ttu-id="32907-127">요청의 결과를 몇 초 만에 캐시할 수 있는 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="32907-127">Specify how long a result from a request can be cached in seconds.</span></span>
<span data-ttu-id="32907-128">예: 600은 10분을 의미합니다.</span><span class="sxs-lookup"><span data-stu-id="32907-128">Example: 600 means 10 minutes.</span></span>

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

### <span data-ttu-id="32907-129">-CorsMethod</span><span class="sxs-lookup"><span data-stu-id="32907-129">-CorsMethod</span></span>
<span data-ttu-id="32907-130">HealthcareApis Fhir Cors 메서드의 서비스 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="32907-130">HealthcareApis Fhir Service List of Cors Method.</span></span>

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

### <span data-ttu-id="32907-131">-CorsOrigin</span><span class="sxs-lookup"><span data-stu-id="32907-131">-CorsOrigin</span></span>
<span data-ttu-id="32907-132">HealthcareApis Fhir Cors Origin의 서비스 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="32907-132">HealthcareApis Fhir Service List of Cors Origin.</span></span>
<span data-ttu-id="32907-133">이 API에 액세스할 수 있는 원본 사이트의 URL을 지정하거나 " \* " 를 사용하여 모든 사이트에서 액세스를 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="32907-133">Specify URLs of origin sites that can access this API, or use " \* " to allow access from any site.</span></span>

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

### <span data-ttu-id="32907-134">-CosmosKeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="32907-134">-CosmosKeyVaultKeyUri</span></span>
<span data-ttu-id="32907-135">HealthcareApis Fhir Service CosmosKeyVaultKeyUri.</span><span class="sxs-lookup"><span data-stu-id="32907-135">HealthcareApis Fhir Service CosmosKeyVaultKeyUri.</span></span>
<span data-ttu-id="32907-136">백업 데이터베이스에 대한 고객 관리 키의 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="32907-136">The URI of the customer-managed key for the backing database.</span></span>

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

### <span data-ttu-id="32907-137">-CosmosOfferThroughput</span><span class="sxs-lookup"><span data-stu-id="32907-137">-CosmosOfferThroughput</span></span>
<span data-ttu-id="32907-138">HealthcareApis Fhir Service CosmosOfferThroughput.</span><span class="sxs-lookup"><span data-stu-id="32907-138">HealthcareApis Fhir Service CosmosOfferThroughput.</span></span>

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

### <span data-ttu-id="32907-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32907-139">-DefaultProfile</span></span>
<span data-ttu-id="32907-140">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="32907-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32907-141">-enableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="32907-141">-EnableSmartProxy</span></span>
<span data-ttu-id="32907-142">HealthcareApis Fhir Service enableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="32907-142">HealthcareApis Fhir Service EnableSmartProxy.</span></span>

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

### <span data-ttu-id="32907-143">-ExportStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="32907-143">-ExportStorageAccountName</span></span>
<span data-ttu-id="32907-144">HealthcareApis Fhir Service Export Storage 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="32907-144">HealthcareApis Fhir Service Export Storage Account Name.</span></span>

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

### <span data-ttu-id="32907-145">-FhirVersion</span><span class="sxs-lookup"><span data-stu-id="32907-145">-FhirVersion</span></span>
<span data-ttu-id="32907-146">Fhir 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="32907-146">Fhir Version.</span></span>

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

### <span data-ttu-id="32907-147">-Kind</span><span class="sxs-lookup"><span data-stu-id="32907-147">-Kind</span></span>
<span data-ttu-id="32907-148">HealthcareApis Service의 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="32907-148">Kind of HealthcareApis Service.</span></span>
<span data-ttu-id="32907-149">기본값은 Fhir입니다.</span><span class="sxs-lookup"><span data-stu-id="32907-149">The default value is Fhir</span></span>

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

### <span data-ttu-id="32907-150">-Location</span><span class="sxs-lookup"><span data-stu-id="32907-150">-Location</span></span>
<span data-ttu-id="32907-151">HealthcareApis 서비스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="32907-151">HealthcareApis Service Location.</span></span>

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

### <span data-ttu-id="32907-152">-ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="32907-152">-ManagedIdentity</span></span>
<span data-ttu-id="32907-153">관리 ID를 사용하나요?</span><span class="sxs-lookup"><span data-stu-id="32907-153">Use Managed Identity?</span></span>

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

### <span data-ttu-id="32907-154">-Name</span><span class="sxs-lookup"><span data-stu-id="32907-154">-Name</span></span>
<span data-ttu-id="32907-155">HealthcareApis 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="32907-155">HealthcareApis Service Name.</span></span>

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

### <span data-ttu-id="32907-156">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="32907-156">-PublicNetworkAccess</span></span>
<span data-ttu-id="32907-157">Fhir 서비스에 대한 네트워크 액세스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="32907-157">The network access type for Fhir service.</span></span> <span data-ttu-id="32907-158">일반적으로 `Enabled` 또는 `Disabled` .</span><span class="sxs-lookup"><span data-stu-id="32907-158">Commonly `Enabled` or `Disabled`.</span></span>

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

### <span data-ttu-id="32907-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32907-159">-ResourceGroupName</span></span>
<span data-ttu-id="32907-160">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="32907-160">Resource Group Name.</span></span>

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

### <span data-ttu-id="32907-161">-Tag</span><span class="sxs-lookup"><span data-stu-id="32907-161">-Tag</span></span>
<span data-ttu-id="32907-162">HealthcareApis Fhir Service 계정 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="32907-162">HealthcareApis Fhir Service Account Tags.</span></span>

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

### <span data-ttu-id="32907-163">-확인</span><span class="sxs-lookup"><span data-stu-id="32907-163">-Confirm</span></span>
<span data-ttu-id="32907-164">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="32907-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32907-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32907-165">-WhatIf</span></span>
<span data-ttu-id="32907-166">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="32907-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32907-167">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="32907-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32907-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32907-168">CommonParameters</span></span>
<span data-ttu-id="32907-169">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="32907-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32907-170">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="32907-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32907-171">입력</span><span class="sxs-lookup"><span data-stu-id="32907-171">INPUTS</span></span>

### <span data-ttu-id="32907-172">System.String</span><span class="sxs-lookup"><span data-stu-id="32907-172">System.String</span></span>

## <span data-ttu-id="32907-173">출력</span><span class="sxs-lookup"><span data-stu-id="32907-173">OUTPUTS</span></span>

### <span data-ttu-id="32907-174">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="32907-174">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="32907-175">참고 사항</span><span class="sxs-lookup"><span data-stu-id="32907-175">NOTES</span></span>

## <span data-ttu-id="32907-176">관련 링크</span><span class="sxs-lookup"><span data-stu-id="32907-176">RELATED LINKS</span></span>
