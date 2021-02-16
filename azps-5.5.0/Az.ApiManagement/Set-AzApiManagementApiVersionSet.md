---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiVersionSet.md
ms.openlocfilehash: d85d480adc5d6c588c7da2f03c514258dc96a9e8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205613"
---
# <span data-ttu-id="2f109-101">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="2f109-101">Set-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="2f109-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f109-102">SYNOPSIS</span></span>
<span data-ttu-id="2f109-103">API Management 컨텍스트에서 API 버전 집합을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2f109-103">Updates an API Version Set in the API Management Context.</span></span>

## <span data-ttu-id="2f109-104">구문</span><span class="sxs-lookup"><span data-stu-id="2f109-104">SYNTAX</span></span>

### <span data-ttu-id="2f109-105">ExpandedParameter(기본값)</span><span class="sxs-lookup"><span data-stu-id="2f109-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-Name <String>]
 [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2f109-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2f109-106">ByInputObject</span></span>
```
Set-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-Name <String>]
 [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2f109-107">설명</span><span class="sxs-lookup"><span data-stu-id="2f109-107">DESCRIPTION</span></span>

<span data-ttu-id="2f109-108">**Set-AzApiManagementApiVersionSet** cmdlet은 Azure API Management API 버전 집합을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="2f109-108">The **Set-AzApiManagementApiVersionSet** cmdlet modifies an Azure API Management API Version Set.</span></span>

## <span data-ttu-id="2f109-109">예제</span><span class="sxs-lookup"><span data-stu-id="2f109-109">EXAMPLES</span></span>

### <span data-ttu-id="2f109-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="2f109-110">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiVersionSet -Context $ApiMgmtContext -ApiVersionSetId "query-verion-set" -Scheme Header -HeaderName "api-version" -Description "Azure version header string"
```

<span data-ttu-id="2f109-111">이 명령은 버전 관리 체계 및 헤더 매개 변수를 사용하여 기존 API 버전 `Header` 집합을 `api-version` 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2f109-111">This command updates an existing API Version Set with versioning scheme `Header` and Header parameter `api-version`.</span></span>

## <span data-ttu-id="2f109-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2f109-112">PARAMETERS</span></span>

### <span data-ttu-id="2f109-113">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="2f109-113">-ApiVersionSetId</span></span>
<span data-ttu-id="2f109-114">새 API 버전 집합에 대한 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="2f109-114">Identifier for new API Version Set.</span></span>

```yaml
Type: System.String
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f109-115">-Context</span><span class="sxs-lookup"><span data-stu-id="2f109-115">-Context</span></span>
<span data-ttu-id="2f109-116">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="2f109-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="2f109-117">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="2f109-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f109-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f109-118">-DefaultProfile</span></span>
<span data-ttu-id="2f109-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2f109-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f109-120">-Description</span><span class="sxs-lookup"><span data-stu-id="2f109-120">-Description</span></span>
<span data-ttu-id="2f109-121">API 버전 집합에 대한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="2f109-121">Description of the Api Version set.</span></span>

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

### <span data-ttu-id="2f109-122">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="2f109-122">-HeaderName</span></span>
<span data-ttu-id="2f109-123">버전 정보를 포함할 헤더 값입니다.</span><span class="sxs-lookup"><span data-stu-id="2f109-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="2f109-124">버전 지정 체계 헤더를 선택한 경우 이 값을 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f109-124">If versioning Scheme HEADER is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="2f109-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f109-125">-InputObject</span></span>
<span data-ttu-id="2f109-126">PsApiManagementApiVersionSet의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="2f109-126">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="2f109-127">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="2f109-127">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f109-128">-Name</span><span class="sxs-lookup"><span data-stu-id="2f109-128">-Name</span></span>
<span data-ttu-id="2f109-129">ApiVersion 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2f109-129">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="2f109-130">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="2f109-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="2f109-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f109-131">-PassThru</span></span>
<span data-ttu-id="2f109-132">지정된 경우 수정된 apiVersionSet을 나타내는 Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet 형식의 인스턴스가 출력에 기록됩니다.</span><span class="sxs-lookup"><span data-stu-id="2f109-132">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet type  representing the modified apiVersionSet will be written to output.</span></span>

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

### <span data-ttu-id="2f109-133">-QueryName</span><span class="sxs-lookup"><span data-stu-id="2f109-133">-QueryName</span></span>
<span data-ttu-id="2f109-134">버전 정보를 포함할 쿼리 값입니다.</span><span class="sxs-lookup"><span data-stu-id="2f109-134">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="2f109-135">버전 구성표 쿼리를 선택한 경우 이 값을 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="2f109-135">If versioning Scheme Query is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="2f109-136">-Scheme</span><span class="sxs-lookup"><span data-stu-id="2f109-136">-Scheme</span></span>
<span data-ttu-id="2f109-137">API 버전 관리 집합에 대해 선택할 버전 관리 체계입니다.</span><span class="sxs-lookup"><span data-stu-id="2f109-137">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="2f109-138">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="2f109-138">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme
Parameter Sets: (All)
Aliases:
Accepted values: Segment, Query, Header

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f109-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2f109-139">-Confirm</span></span>
<span data-ttu-id="2f109-140">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2f109-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f109-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f109-141">-WhatIf</span></span>
<span data-ttu-id="2f109-142">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="2f109-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2f109-143">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2f109-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f109-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f109-144">CommonParameters</span></span>
<span data-ttu-id="2f109-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2f109-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f109-146">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2f109-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f109-147">입력</span><span class="sxs-lookup"><span data-stu-id="2f109-147">INPUTS</span></span>

### <span data-ttu-id="2f109-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2f109-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2f109-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="2f109-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="2f109-150">System.String</span><span class="sxs-lookup"><span data-stu-id="2f109-150">System.String</span></span>

### <span data-ttu-id="2f109-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span><span class="sxs-lookup"><span data-stu-id="2f109-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="2f109-152">출력</span><span class="sxs-lookup"><span data-stu-id="2f109-152">OUTPUTS</span></span>

### <span data-ttu-id="2f109-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="2f109-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="2f109-154">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2f109-154">NOTES</span></span>

## <span data-ttu-id="2f109-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2f109-155">RELATED LINKS</span></span>

[<span data-ttu-id="2f109-156">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="2f109-156">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="2f109-157">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="2f109-157">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="2f109-158">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="2f109-158">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)
