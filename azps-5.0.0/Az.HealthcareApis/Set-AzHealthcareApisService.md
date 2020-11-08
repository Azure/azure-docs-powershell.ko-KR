---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/set-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Set-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Set-AzHealthcareApisService.md
ms.openlocfilehash: a944982688dac8f9a28c10b3d26e71a8331451ad
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217374"
---
# <span data-ttu-id="08239-101">Set-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="08239-101">Set-AzHealthcareApisService</span></span>

## <span data-ttu-id="08239-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08239-102">SYNOPSIS</span></span>
<span data-ttu-id="08239-103">기존 healthcareApis fa r 서비스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="08239-103">Updates an existing healthcareApis fhir service.</span></span>

## <span data-ttu-id="08239-104">구문과</span><span class="sxs-lookup"><span data-stu-id="08239-104">SYNTAX</span></span>

### <span data-ttu-id="08239-105">ServiceNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="08239-105">ServiceNameParameterSet (Default)</span></span>
```
Set-AzHealthcareApisService -Name <String> -ResourceGroupName <String> [-CosmosOfferThroughput <Int32>]
 [-Authority <String>] [-Audience <String>] [-EnableSmartProxy] [-DisableSmartProxy] [-CorsOrigin <String[]>]
 [-CorsHeader <String[]>] [-CorsMethod <String[]>] [-CorsMaxAge <Int32>] [-AllowCorsCredential]
 [-DisableCorsCredential] [-ExportStorageAccountName <String>] [-AccessPolicyObjectId <String[]>]
 [-EnableManagedIdentity] [-DisableManagedIdentity] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08239-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="08239-106">ResourceIdParameterSet</span></span>
```
Set-AzHealthcareApisService [-CosmosOfferThroughput <Int32>] [-Authority <String>] [-Audience <String>]
 [-EnableSmartProxy] [-DisableSmartProxy] [-CorsOrigin <String[]>] [-CorsHeader <String[]>]
 [-CorsMethod <String[]>] [-CorsMaxAge <Int32>] [-AllowCorsCredential] [-DisableCorsCredential]
 [-ExportStorageAccountName <String>] [-AccessPolicyObjectId <String[]>] [-EnableManagedIdentity]
 [-DisableManagedIdentity] [-Tag <Hashtable>] -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08239-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="08239-107">InputObjectParameterSet</span></span>
```
Set-AzHealthcareApisService -InputObject <PSHealthcareApisService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08239-108">설명은</span><span class="sxs-lookup"><span data-stu-id="08239-108">DESCRIPTION</span></span>
<span data-ttu-id="08239-109">기존 healthcareApis fa r 서비스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="08239-109">Updates an existing healthcareApis fhir service.</span></span>

## <span data-ttu-id="08239-110">예제의</span><span class="sxs-lookup"><span data-stu-id="08239-110">EXAMPLES</span></span>

### <span data-ttu-id="08239-111">예제 1: cosmosdb OfferThroughput = 500에서 리소스 그룹 MyResourceGroup의 MyService 라는 기존 healthcareapis 서비스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="08239-111">Example 1 : Updates the existing healthcareapis service named MyService in the resource group MyResourceGroup  with the cosmosdb OfferThroughput = 500.</span></span>

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

### <span data-ttu-id="08239-112">예제 2: 리소스 그룹 MyResourceGroup의 MyService 이라는 기존 healthcareapis 서비스를 cosmosdb OfferThroughput = 500에 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="08239-112">Example 2: Updates the existing healthcareapis service named MyService in the resource group MyResourceGroup  with the cosmosdb OfferThroughput = 500.</span></span>

```powershell
PS C:\> $ResourceId = "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.HealthcareApis/services/MyService"
PS C:\> Set-AzHealthcareApisService -ResourceId $ResourceId  -CosmosOfferThroughput 500

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
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

## <span data-ttu-id="08239-113">변수</span><span class="sxs-lookup"><span data-stu-id="08239-113">PARAMETERS</span></span>

### <span data-ttu-id="08239-114">-AccessPolicyObjectId</span><span class="sxs-lookup"><span data-stu-id="08239-114">-AccessPolicyObjectId</span></span>
<span data-ttu-id="08239-115">액세스 정책 개체 Id의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="08239-115">List of Access Policy Object IDs.</span></span>

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

### <span data-ttu-id="08239-116">-AllowCorsCredential</span><span class="sxs-lookup"><span data-stu-id="08239-116">-AllowCorsCredential</span></span>
<span data-ttu-id="08239-117">HealthcareApis FhirService AllowCorsCredential.</span><span class="sxs-lookup"><span data-stu-id="08239-117">HealthcareApis FhirService AllowCorsCredential.</span></span>

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

### <span data-ttu-id="08239-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="08239-118">-AsJob</span></span>
<span data-ttu-id="08239-119">백그라운드에서 cmdlet을 작업으로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="08239-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="08239-120">-청중</span><span class="sxs-lookup"><span data-stu-id="08239-120">-Audience</span></span>
<span data-ttu-id="08239-121">HealthcareApis FhirService 청중.</span><span class="sxs-lookup"><span data-stu-id="08239-121">HealthcareApis FhirService Audience.</span></span>

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

### <span data-ttu-id="08239-122">-기관</span><span class="sxs-lookup"><span data-stu-id="08239-122">-Authority</span></span>
<span data-ttu-id="08239-123">HealthcareApis FhirService 기관.</span><span class="sxs-lookup"><span data-stu-id="08239-123">HealthcareApis FhirService Authority.</span></span>

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

### <span data-ttu-id="08239-124">-CorsHeader</span><span class="sxs-lookup"><span data-stu-id="08239-124">-CorsHeader</span></span>
<span data-ttu-id="08239-125">Cors 헤더의 HealthcareApis Fa r 서비스 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="08239-125">HealthcareApis Fhir Service List of Cors Header.</span></span> <span data-ttu-id="08239-126">요청 중 사용할 수 있는 HTTP 헤더를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="08239-126">Specify HTTP headers which can be used during the request.</span></span> <span data-ttu-id="08239-127">모든 머리글에 \*를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="08239-127">Use \* for any header.</span></span>

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

### <span data-ttu-id="08239-128">-CorsMaxAge</span><span class="sxs-lookup"><span data-stu-id="08239-128">-CorsMaxAge</span></span>
<span data-ttu-id="08239-129">HealthcareApis f r 서비스 Cors 최대 연령입니다.</span><span class="sxs-lookup"><span data-stu-id="08239-129">HealthcareApis Fhir Service Cors Max Age.</span></span> <span data-ttu-id="08239-130">요청 결과가 몇 초 후에 캐시 될 수 있는 기간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="08239-130">Specify how long a result from a request can be cached in seconds.</span></span> <span data-ttu-id="08239-131">예: 600은 10 분을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="08239-131">Example: 600 means 10 minutes.</span></span>

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

### <span data-ttu-id="08239-132">-CorsMethod</span><span class="sxs-lookup"><span data-stu-id="08239-132">-CorsMethod</span></span>
<span data-ttu-id="08239-133">HealthcareApis FhirService Cors 메서드 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="08239-133">HealthcareApis FhirService List of Cors Methods.</span></span>

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

### <span data-ttu-id="08239-134">-CorsOrigin</span><span class="sxs-lookup"><span data-stu-id="08239-134">-CorsOrigin</span></span>
<span data-ttu-id="08239-135">HealthcareApis FhirService Cors 원본 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="08239-135">HealthcareApis FhirService List of Cors Origins.</span></span> <span data-ttu-id="08239-136">Cors 원본에 대 한 HealthcareApis Fa r 서비스 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="08239-136">HealthcareApis Fhir Service List of Cors Origin.</span></span> <span data-ttu-id="08239-137">이 API에 액세스할 수 있는 원본 사이트의 Url을 지정 하거나 \*를 사용 하 여 사이트에서 액세스를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="08239-137">Specify URLs of origin sites that can access this API, or use \* to allow access from any site.</span></span>

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

### <span data-ttu-id="08239-138">-CosmosOfferThroughput</span><span class="sxs-lookup"><span data-stu-id="08239-138">-CosmosOfferThroughput</span></span>
<span data-ttu-id="08239-139">HealthcareApis FhirService CosmosOfferThroughput.</span><span class="sxs-lookup"><span data-stu-id="08239-139">HealthcareApis FhirService CosmosOfferThroughput.</span></span>

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

### <span data-ttu-id="08239-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08239-140">-DefaultProfile</span></span>
<span data-ttu-id="08239-141">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="08239-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08239-142">-DisableCorsCredential</span><span class="sxs-lookup"><span data-stu-id="08239-142">-DisableCorsCredential</span></span>
<span data-ttu-id="08239-143">HealthcareApis FhirService CorsCredentials 허용 되지 않음.</span><span class="sxs-lookup"><span data-stu-id="08239-143">HealthcareApis FhirService CorsCredentials Not Allowed.</span></span>

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

### <span data-ttu-id="08239-144">-DisableManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="08239-144">-DisableManagedIdentity</span></span>
<span data-ttu-id="08239-145">관리 Id를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="08239-145">Disable Managed Identity.</span></span>

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

### <span data-ttu-id="08239-146">-DisableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="08239-146">-DisableSmartProxy</span></span>
<span data-ttu-id="08239-147">HealthcareApis FhirService DisableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="08239-147">HealthcareApis FhirService DisableSmartProxy.</span></span>

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

### <span data-ttu-id="08239-148">-EnableManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="08239-148">-EnableManagedIdentity</span></span>
<span data-ttu-id="08239-149">관리 Id를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="08239-149">Enable Managed Identity.</span></span>

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

### <span data-ttu-id="08239-150">-EnableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="08239-150">-EnableSmartProxy</span></span>
<span data-ttu-id="08239-151">HealthcareApis FhirService EnableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="08239-151">HealthcareApis FhirService EnableSmartProxy.</span></span>

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

### <span data-ttu-id="08239-152">-ExportStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="08239-152">-ExportStorageAccountName</span></span>
<span data-ttu-id="08239-153">HealthcareApis f r 서비스 내보내기 저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="08239-153">HealthcareApis Fhir Service Export Storage Account Name.</span></span>

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

### <span data-ttu-id="08239-154">-InputObject</span><span class="sxs-lookup"><span data-stu-id="08239-154">-InputObject</span></span>
<span data-ttu-id="08239-155">AzHealthcareApisFhirService에서 HealthcareApis fa r 서비스를 시작 했습니다.</span><span class="sxs-lookup"><span data-stu-id="08239-155">HealthcareApis fhir service piped from Get-AzHealthcareApisFhirService.</span></span>

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

### <span data-ttu-id="08239-156">-이름</span><span class="sxs-lookup"><span data-stu-id="08239-156">-Name</span></span>
<span data-ttu-id="08239-157">HealthcareApis 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="08239-157">HealthcareApis Service Name.</span></span>

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

### <span data-ttu-id="08239-158">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08239-158">-ResourceGroupName</span></span>
<span data-ttu-id="08239-159">HealthcareApis 서비스 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="08239-159">HealthcareApis Service Resource Group Name.</span></span>

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

### <span data-ttu-id="08239-160">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="08239-160">-ResourceId</span></span>
<span data-ttu-id="08239-161">HealthcareApis Fa r 서비스 ResourceId.</span><span class="sxs-lookup"><span data-stu-id="08239-161">HealthcareApis Fhir Service ResourceId.</span></span>

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

### <span data-ttu-id="08239-162">태그</span><span class="sxs-lookup"><span data-stu-id="08239-162">-Tag</span></span>
<span data-ttu-id="08239-163">HealthcareApis Fa r 서비스 계정 태그.</span><span class="sxs-lookup"><span data-stu-id="08239-163">HealthcareApis Fhir Service Account Tags.</span></span>

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

### <span data-ttu-id="08239-164">-확인</span><span class="sxs-lookup"><span data-stu-id="08239-164">-Confirm</span></span>
<span data-ttu-id="08239-165">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="08239-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08239-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08239-166">-WhatIf</span></span>
<span data-ttu-id="08239-167">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="08239-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08239-168">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="08239-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08239-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08239-169">CommonParameters</span></span>
<span data-ttu-id="08239-170">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="08239-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08239-171">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="08239-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08239-172">입력</span><span class="sxs-lookup"><span data-stu-id="08239-172">INPUTS</span></span>

### <span data-ttu-id="08239-173">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="08239-173">System.String</span></span>

### <span data-ttu-id="08239-174">HealthcareApisService. PSHealthcareApisService/.</span><span class="sxs-lookup"><span data-stu-id="08239-174">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="08239-175">출력</span><span class="sxs-lookup"><span data-stu-id="08239-175">OUTPUTS</span></span>

### <span data-ttu-id="08239-176">HealthcareApisService. PSHealthcareApisService/.</span><span class="sxs-lookup"><span data-stu-id="08239-176">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="08239-177">상속자</span><span class="sxs-lookup"><span data-stu-id="08239-177">NOTES</span></span>

## <span data-ttu-id="08239-178">관련 링크</span><span class="sxs-lookup"><span data-stu-id="08239-178">RELATED LINKS</span></span>
