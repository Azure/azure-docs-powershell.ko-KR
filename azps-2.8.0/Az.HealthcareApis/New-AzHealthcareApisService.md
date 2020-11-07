---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/new-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/New-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/New-AzHealthcareApisService.md
ms.openlocfilehash: 374b443157bf6ef36f39d3ee0dba34ae59419931
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689773"
---
# <span data-ttu-id="aafc4-101">New-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="aafc4-101">New-AzHealthcareApisService</span></span>

## <span data-ttu-id="aafc4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aafc4-102">SYNOPSIS</span></span>
<span data-ttu-id="aafc4-103">서비스 인스턴스의 메타 데이터를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aafc4-103">Creates the metadata of a service instance.</span></span>

## <span data-ttu-id="aafc4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="aafc4-104">SYNTAX</span></span>

```
New-AzHealthcareApisService -Name <String> -ResourceGroupName <String> -Location <String> [-Kind <String>]
 [-AccessPolicyObjectId <String[]>] [-AllowCorsCredential] [-Audience <String>] [-Authority <String>]
 [-CorsHeader <String[]>] [-CorsMaxAge <Int32>] [-CorsMethod <String[]>] [-CorsOrigin <String[]>]
 [-CosmosOfferThroughput <Int32>] [-EnableSmartProxy] [-FhirVersion <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aafc4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="aafc4-105">DESCRIPTION</span></span>
<span data-ttu-id="aafc4-106">서비스 인스턴스의 메타 데이터를 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="aafc4-106">Creates or updates the metadata of a service instance.</span></span>

## <span data-ttu-id="aafc4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="aafc4-107">EXAMPLES</span></span>

### <span data-ttu-id="aafc4-108">예제 1: 위치 westus2의 리소스 그룹 MyResourceGroup에 MyService 이라는 새 Azure healthcareapis fto r 서비스를 만듭니다 cosmosdb 제공 처리량 = 400</span><span class="sxs-lookup"><span data-stu-id="aafc4-108">Example 1 : Creates a new Azure healthcareapis fhir service named MyService in the resource group MyResourceGroup in a location westus2 with cosmosdb offer throughput = 400</span></span>
```powershell
PS C:\> New-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup -Location MyLocation -Kind fhir-R4 -CosmosOfferThroughput  400

ResourceGroupName Name Location        Kind   CosmosOfferThroughput
----------------- ----------- -------------------------------
MyResourceGroup   MyService   westus2    fhir-R4   400

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
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

## <span data-ttu-id="aafc4-109">변수</span><span class="sxs-lookup"><span data-stu-id="aafc4-109">PARAMETERS</span></span>

### <span data-ttu-id="aafc4-110">-AccessPolicyObjectId</span><span class="sxs-lookup"><span data-stu-id="aafc4-110">-AccessPolicyObjectId</span></span>
<span data-ttu-id="aafc4-111">액세스 정책 개체 Id의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="aafc4-111">List of Access Policy Object IDs.</span></span>

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

### <span data-ttu-id="aafc4-112">-AllowCorsCredential</span><span class="sxs-lookup"><span data-stu-id="aafc4-112">-AllowCorsCredential</span></span>
<span data-ttu-id="aafc4-113">HealthcareApis f r 서비스 AllowCorsCredential.</span><span class="sxs-lookup"><span data-stu-id="aafc4-113">HealthcareApis Fhir Service AllowCorsCredential.</span></span>

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

### <span data-ttu-id="aafc4-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aafc4-114">-AsJob</span></span>
<span data-ttu-id="aafc4-115">백그라운드에서 cmdlet을 작업으로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="aafc4-115">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="aafc4-116">-청중</span><span class="sxs-lookup"><span data-stu-id="aafc4-116">-Audience</span></span>
<span data-ttu-id="aafc4-117">HealthcareApis Fa r 서비스 청중.</span><span class="sxs-lookup"><span data-stu-id="aafc4-117">HealthcareApis Fhir Service Audience.</span></span>

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

### <span data-ttu-id="aafc4-118">-기관</span><span class="sxs-lookup"><span data-stu-id="aafc4-118">-Authority</span></span>
<span data-ttu-id="aafc4-119">HealthcareApis Fa r 서비스 기관.</span><span class="sxs-lookup"><span data-stu-id="aafc4-119">HealthcareApis Fhir Service Authority.</span></span>

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

### <span data-ttu-id="aafc4-120">-CorsHeader</span><span class="sxs-lookup"><span data-stu-id="aafc4-120">-CorsHeader</span></span>
<span data-ttu-id="aafc4-121">Cors 헤더의 HealthcareApis Fa r 서비스 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="aafc4-121">HealthcareApis Fhir Service List of Cors Header.</span></span> <span data-ttu-id="aafc4-122">요청 중 사용할 수 있는 HTTP 헤더를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aafc4-122">Specify HTTP headers which can be used during the request.</span></span> <span data-ttu-id="aafc4-123">모든 머리글에 \*를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="aafc4-123">Use \* for any header.</span></span>

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

### <span data-ttu-id="aafc4-124">-CorsMaxAge</span><span class="sxs-lookup"><span data-stu-id="aafc4-124">-CorsMaxAge</span></span>
<span data-ttu-id="aafc4-125">HealthcareApis f r 서비스 Cors 최대 연령입니다.</span><span class="sxs-lookup"><span data-stu-id="aafc4-125">HealthcareApis Fhir Service Cors Max Age.</span></span> <span data-ttu-id="aafc4-126">요청 결과가 몇 초 후에 캐시 될 수 있는 기간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aafc4-126">Specify how long a result from a request can be cached in seconds.</span></span> <span data-ttu-id="aafc4-127">예: 600은 10 분을 의미 합니다.</span><span class="sxs-lookup"><span data-stu-id="aafc4-127">Example: 600 means 10 minutes.</span></span>

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

### <span data-ttu-id="aafc4-128">-CorsMethod</span><span class="sxs-lookup"><span data-stu-id="aafc4-128">-CorsMethod</span></span>
<span data-ttu-id="aafc4-129">Cors 방법의 HealthcareApis Fa r 서비스 목록.</span><span class="sxs-lookup"><span data-stu-id="aafc4-129">HealthcareApis Fhir Service List of Cors Method.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: DELETE, GET, OPTIONS, PATCH, POST, PUT

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aafc4-130">-CorsOrigin</span><span class="sxs-lookup"><span data-stu-id="aafc4-130">-CorsOrigin</span></span>
<span data-ttu-id="aafc4-131">Cors 원본에 대 한 HealthcareApis Fa r 서비스 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="aafc4-131">HealthcareApis Fhir Service List of Cors Origin.</span></span> <span data-ttu-id="aafc4-132">이 API에 액세스할 수 있는 원본 사이트의 Url을 지정 하거나 \*를 사용 하 여 사이트에서 액세스를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="aafc4-132">Specify URLs of origin sites that can access this API, or use \* to allow access from any site.</span></span>

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

### <span data-ttu-id="aafc4-133">-CosmosOfferThroughput</span><span class="sxs-lookup"><span data-stu-id="aafc4-133">-CosmosOfferThroughput</span></span>
<span data-ttu-id="aafc4-134">HealthcareApis f r 서비스 CosmosOfferThroughput.</span><span class="sxs-lookup"><span data-stu-id="aafc4-134">HealthcareApis Fhir Service CosmosOfferThroughput.</span></span>

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

### <span data-ttu-id="aafc4-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aafc4-135">-DefaultProfile</span></span>
<span data-ttu-id="aafc4-136">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aafc4-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aafc4-137">-EnableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="aafc4-137">-EnableSmartProxy</span></span>
<span data-ttu-id="aafc4-138">HealthcareApis f r 서비스 EnableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="aafc4-138">HealthcareApis Fhir Service EnableSmartProxy.</span></span>

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

### <span data-ttu-id="aafc4-139">-Frr 버전</span><span class="sxs-lookup"><span data-stu-id="aafc4-139">-FhirVersion</span></span>
<span data-ttu-id="aafc4-140">이력서 버전.</span><span class="sxs-lookup"><span data-stu-id="aafc4-140">Fhir Version.</span></span>

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

### <span data-ttu-id="aafc4-141">-종류</span><span class="sxs-lookup"><span data-stu-id="aafc4-141">-Kind</span></span>
<span data-ttu-id="aafc4-142">HealthcareApis 서비스의 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="aafc4-142">Kind of HealthcareApis Service.</span></span>
<span data-ttu-id="aafc4-143">기본 값은 Fa r입니다.</span><span class="sxs-lookup"><span data-stu-id="aafc4-143">The default value is Fhir</span></span>

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

### <span data-ttu-id="aafc4-144">-위치</span><span class="sxs-lookup"><span data-stu-id="aafc4-144">-Location</span></span>
<span data-ttu-id="aafc4-145">HealthcareApis 서비스 위치.</span><span class="sxs-lookup"><span data-stu-id="aafc4-145">HealthcareApis Service Location.</span></span>

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

### <span data-ttu-id="aafc4-146">-이름</span><span class="sxs-lookup"><span data-stu-id="aafc4-146">-Name</span></span>
<span data-ttu-id="aafc4-147">HealthcareApis 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aafc4-147">HealthcareApis Service Name.</span></span>

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

### <span data-ttu-id="aafc4-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aafc4-148">-ResourceGroupName</span></span>
<span data-ttu-id="aafc4-149">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aafc4-149">Resource Group Name.</span></span>

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

### <span data-ttu-id="aafc4-150">태그</span><span class="sxs-lookup"><span data-stu-id="aafc4-150">-Tag</span></span>
<span data-ttu-id="aafc4-151">HealthcareApis Fa r 서비스 계정 태그.</span><span class="sxs-lookup"><span data-stu-id="aafc4-151">HealthcareApis Fhir Service Account Tags.</span></span>

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

### <span data-ttu-id="aafc4-152">-확인</span><span class="sxs-lookup"><span data-stu-id="aafc4-152">-Confirm</span></span>
<span data-ttu-id="aafc4-153">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="aafc4-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aafc4-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aafc4-154">-WhatIf</span></span>
<span data-ttu-id="aafc4-155">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="aafc4-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aafc4-156">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aafc4-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aafc4-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aafc4-157">CommonParameters</span></span>
<span data-ttu-id="aafc4-158">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aafc4-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aafc4-159">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="aafc4-159">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aafc4-160">입력</span><span class="sxs-lookup"><span data-stu-id="aafc4-160">INPUTS</span></span>

### <span data-ttu-id="aafc4-161">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="aafc4-161">System.String</span></span>

## <span data-ttu-id="aafc4-162">출력</span><span class="sxs-lookup"><span data-stu-id="aafc4-162">OUTPUTS</span></span>

### <span data-ttu-id="aafc4-163">HealthcareApisService. PSHealthcareApisService/.</span><span class="sxs-lookup"><span data-stu-id="aafc4-163">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="aafc4-164">상속자</span><span class="sxs-lookup"><span data-stu-id="aafc4-164">NOTES</span></span>

## <span data-ttu-id="aafc4-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aafc4-165">RELATED LINKS</span></span>
