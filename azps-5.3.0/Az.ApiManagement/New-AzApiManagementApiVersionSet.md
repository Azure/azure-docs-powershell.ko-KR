---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiVersionSet.md
ms.openlocfilehash: 0e007634659d842b0c59712a2ee191a79e1aeb58
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494400"
---
# <span data-ttu-id="9952f-101">New-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="9952f-101">New-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="9952f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9952f-102">SYNOPSIS</span></span>
<span data-ttu-id="9952f-103">API 버전 집합을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9952f-103">Creates an API Version Set.</span></span>

## <span data-ttu-id="9952f-104">구문</span><span class="sxs-lookup"><span data-stu-id="9952f-104">SYNTAX</span></span>

```
New-AzApiManagementApiVersionSet -Context <PsApiManagementContext> [-ApiVersionSetId <String>] -Name <String>
 -Scheme <PsApiManagementVersioningScheme> [-HeaderName <String>] [-QueryName <String>] [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9952f-105">설명</span><span class="sxs-lookup"><span data-stu-id="9952f-105">DESCRIPTION</span></span>
<span data-ttu-id="9952f-106">**New-AzApiManagementApiVersionSet** cmdlet은 Azure API Management 컨텍스트에서 API 버전 집합 엔터티를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9952f-106">The **New-AzApiManagementApiVersionSet** cmdlet creates an API Version set entity in the Azure API Management context.</span></span>

## <span data-ttu-id="9952f-107">예제</span><span class="sxs-lookup"><span data-stu-id="9952f-107">EXAMPLES</span></span>

### <span data-ttu-id="9952f-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="9952f-108">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> New-AzApiManagementApiVersionSet -Context $ApiMgmtContext  -Name "newversion" -Scheme Header -HeaderName "x-ms-version" -Description "version by xmsversion"

ApiVersionSetId   : ea9a87cd-a699-4a75-bf7d-909846b91268
Description       : version by xmsversion
VersionQueryName  :
VersionHeaderName : x-ms-version
DisplayName       : newversion
VersioningScheme  : Header
Id                : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/api-version-sets/ea9a87cd-a699-4a75-bf7d-909846b91268
ResourceGroupName : Api-Default-WestUS
ServiceName       : contoso
```

<span data-ttu-id="9952f-109">이 명령은 버전 관리 체계 및 쿼리 매개 변수를 지정하는 API `Query` 버전 집합을 `api-version` 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9952f-109">This command creates an API Version Set which versioning scheme `Query` and Query parameter `api-version`.</span></span>

## <span data-ttu-id="9952f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9952f-110">PARAMETERS</span></span>

### <span data-ttu-id="9952f-111">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="9952f-111">-ApiVersionSetId</span></span>
<span data-ttu-id="9952f-112">새 API 버전 집합에 대한 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="9952f-112">Identifier for new API Version Set.</span></span>
<span data-ttu-id="9952f-113">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="9952f-113">This parameter is optional.</span></span>
<span data-ttu-id="9952f-114">지정하지 않으면 식별자가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="9952f-114">If not specified an identifier will be generated.</span></span>

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

### <span data-ttu-id="9952f-115">-Context</span><span class="sxs-lookup"><span data-stu-id="9952f-115">-Context</span></span>
<span data-ttu-id="9952f-116">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="9952f-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="9952f-117">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="9952f-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9952f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9952f-118">-DefaultProfile</span></span>
<span data-ttu-id="9952f-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9952f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9952f-120">-Description</span><span class="sxs-lookup"><span data-stu-id="9952f-120">-Description</span></span>
<span data-ttu-id="9952f-121">API 버전 집합에 대한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="9952f-121">Description of the Api Version set.</span></span>

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

### <span data-ttu-id="9952f-122">-HeaderName</span><span class="sxs-lookup"><span data-stu-id="9952f-122">-HeaderName</span></span>
<span data-ttu-id="9952f-123">버전 정보를 포함할 헤더 값입니다.</span><span class="sxs-lookup"><span data-stu-id="9952f-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="9952f-124">버전 지정 체계 헤더를 선택한 경우 이 값을 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9952f-124">If versioning Scheme HEADER is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="9952f-125">-Name</span><span class="sxs-lookup"><span data-stu-id="9952f-125">-Name</span></span>
<span data-ttu-id="9952f-126">ApiVersion 집합의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9952f-126">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="9952f-127">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="9952f-127">This parameter is required.</span></span>

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

### <span data-ttu-id="9952f-128">-QueryName</span><span class="sxs-lookup"><span data-stu-id="9952f-128">-QueryName</span></span>
<span data-ttu-id="9952f-129">버전 정보를 포함할 쿼리 값입니다.</span><span class="sxs-lookup"><span data-stu-id="9952f-129">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="9952f-130">버전 구성표 쿼리를 선택한 경우 이 값을 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9952f-130">If versioning Scheme Query is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="9952f-131">-Scheme</span><span class="sxs-lookup"><span data-stu-id="9952f-131">-Scheme</span></span>
<span data-ttu-id="9952f-132">API 버전 관리 집합에 대해 선택할 버전 관리 체계입니다.</span><span class="sxs-lookup"><span data-stu-id="9952f-132">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="9952f-133">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="9952f-133">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme
Parameter Sets: (All)
Aliases:
Accepted values: Segment, Query, Header

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9952f-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9952f-134">-Confirm</span></span>
<span data-ttu-id="9952f-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9952f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9952f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9952f-136">-WhatIf</span></span>
<span data-ttu-id="9952f-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="9952f-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9952f-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9952f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9952f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9952f-139">CommonParameters</span></span>
<span data-ttu-id="9952f-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9952f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9952f-141">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9952f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9952f-142">입력</span><span class="sxs-lookup"><span data-stu-id="9952f-142">INPUTS</span></span>

### <span data-ttu-id="9952f-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9952f-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9952f-144">System.String</span><span class="sxs-lookup"><span data-stu-id="9952f-144">System.String</span></span>

### <span data-ttu-id="9952f-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span><span class="sxs-lookup"><span data-stu-id="9952f-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="9952f-146">출력</span><span class="sxs-lookup"><span data-stu-id="9952f-146">OUTPUTS</span></span>

### <span data-ttu-id="9952f-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="9952f-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="9952f-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9952f-148">NOTES</span></span>

## <span data-ttu-id="9952f-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9952f-149">RELATED LINKS</span></span>

[<span data-ttu-id="9952f-150">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="9952f-150">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="9952f-151">Remove-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="9952f-151">Remove-AzApiManagementApiVersionSet</span></span>](./Remove-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="9952f-152">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="9952f-152">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)