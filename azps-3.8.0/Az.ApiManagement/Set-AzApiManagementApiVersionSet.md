---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapiversionset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiVersionSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiVersionSet.md
ms.openlocfilehash: d85d480adc5d6c588c7da2f03c514258dc96a9e8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043862"
---
# <span data-ttu-id="33c1b-101">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="33c1b-101">Set-AzApiManagementApiVersionSet</span></span>

## <span data-ttu-id="33c1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33c1b-102">SYNOPSIS</span></span>
<span data-ttu-id="33c1b-103">API 관리 컨텍스트에서 설정 된 API 버전을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="33c1b-103">Updates an API Version Set in the API Management Context.</span></span>

## <span data-ttu-id="33c1b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="33c1b-104">SYNTAX</span></span>

### <span data-ttu-id="33c1b-105">ExpandedParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="33c1b-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiVersionSet -Context <PsApiManagementContext> -ApiVersionSetId <String> [-Name <String>]
 [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="33c1b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="33c1b-106">ByInputObject</span></span>
```
Set-AzApiManagementApiVersionSet -InputObject <PsApiManagementApiVersionSet> [-Name <String>]
 [-Scheme <PsApiManagementVersioningScheme>] [-HeaderName <String>] [-QueryName <String>]
 [-Description <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="33c1b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="33c1b-107">DESCRIPTION</span></span>

<span data-ttu-id="33c1b-108">**AzApiManagementApiVersionSet** Cmdlet은 Azure API Management Api 버전 집합을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="33c1b-108">The **Set-AzApiManagementApiVersionSet** cmdlet modifies an Azure API Management API Version Set.</span></span>

## <span data-ttu-id="33c1b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="33c1b-109">EXAMPLES</span></span>

### <span data-ttu-id="33c1b-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="33c1b-110">Example 1</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiVersionSet -Context $ApiMgmtContext -ApiVersionSetId "query-verion-set" -Scheme Header -HeaderName "api-version" -Description "Azure version header string"
```

<span data-ttu-id="33c1b-111">이 명령은 버전 지정 체계 및 헤더 매개 변수를 사용 하 여 기존 API 버전 집합을 업데이트 `Header` `api-version` 합니다.</span><span class="sxs-lookup"><span data-stu-id="33c1b-111">This command updates an existing API Version Set with versioning scheme `Header` and Header parameter `api-version`.</span></span>

## <span data-ttu-id="33c1b-112">변수</span><span class="sxs-lookup"><span data-stu-id="33c1b-112">PARAMETERS</span></span>

### <span data-ttu-id="33c1b-113">-ApiVersionSetId</span><span class="sxs-lookup"><span data-stu-id="33c1b-113">-ApiVersionSetId</span></span>
<span data-ttu-id="33c1b-114">새 API 버전 집합의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="33c1b-114">Identifier for new API Version Set.</span></span>

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

### <span data-ttu-id="33c1b-115">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="33c1b-115">-Context</span></span>
<span data-ttu-id="33c1b-116">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="33c1b-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="33c1b-117">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="33c1b-117">This parameter is required.</span></span>

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

### <span data-ttu-id="33c1b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33c1b-118">-DefaultProfile</span></span>
<span data-ttu-id="33c1b-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="33c1b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33c1b-120">-설명</span><span class="sxs-lookup"><span data-stu-id="33c1b-120">-Description</span></span>
<span data-ttu-id="33c1b-121">Api 버전 집합에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="33c1b-121">Description of the Api Version set.</span></span>

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

### <span data-ttu-id="33c1b-122">-인원 Ername</span><span class="sxs-lookup"><span data-stu-id="33c1b-122">-HeaderName</span></span>
<span data-ttu-id="33c1b-123">버전 관리 정보가 포함 될 헤더 값입니다.</span><span class="sxs-lookup"><span data-stu-id="33c1b-123">The Header value which will contain the versioning information.</span></span>
<span data-ttu-id="33c1b-124">버전 지정 체계 헤더가 선택 된 경우에는이 값을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="33c1b-124">If versioning Scheme HEADER is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="33c1b-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="33c1b-125">-InputObject</span></span>
<span data-ttu-id="33c1b-126">PsApiManagementApiVersionSet의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="33c1b-126">Instance of PsApiManagementApiVersionSet.</span></span> <span data-ttu-id="33c1b-127">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="33c1b-127">This parameter is required.</span></span>

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

### <span data-ttu-id="33c1b-128">-이름</span><span class="sxs-lookup"><span data-stu-id="33c1b-128">-Name</span></span>
<span data-ttu-id="33c1b-129">ApiVersion Set의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="33c1b-129">The name of the ApiVersion Set.</span></span>
<span data-ttu-id="33c1b-130">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="33c1b-130">This parameter is optional.</span></span>

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

### <span data-ttu-id="33c1b-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="33c1b-131">-PassThru</span></span>
<span data-ttu-id="33c1b-132">지정한 경우 ApiManagement의 인스턴스는 수정 된 apiVersionSet을 나타내는 ServiceManagement 유형의 PsApiManagementApiVersionSet 형식으로 출력에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="33c1b-132">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet type  representing the modified apiVersionSet will be written to output.</span></span>

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

### <span data-ttu-id="33c1b-133">-QueryName</span><span class="sxs-lookup"><span data-stu-id="33c1b-133">-QueryName</span></span>
<span data-ttu-id="33c1b-134">버전 관리 정보를 포함할 쿼리 값입니다.</span><span class="sxs-lookup"><span data-stu-id="33c1b-134">The Query value which will contain the versioning information.</span></span>
<span data-ttu-id="33c1b-135">버전 지정 체계 쿼리를 선택한 경우에는이 값을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="33c1b-135">If versioning Scheme Query is chosen, then this value must be specified.</span></span>

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

### <span data-ttu-id="33c1b-136">-구성표</span><span class="sxs-lookup"><span data-stu-id="33c1b-136">-Scheme</span></span>
<span data-ttu-id="33c1b-137">Api 버전 설정에 대해 선택할 버전 지정 체계입니다.</span><span class="sxs-lookup"><span data-stu-id="33c1b-137">Versioning Scheme to select for the Api Versioning Set.</span></span>
<span data-ttu-id="33c1b-138">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="33c1b-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="33c1b-139">-확인</span><span class="sxs-lookup"><span data-stu-id="33c1b-139">-Confirm</span></span>
<span data-ttu-id="33c1b-140">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="33c1b-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33c1b-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33c1b-141">-WhatIf</span></span>
<span data-ttu-id="33c1b-142">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="33c1b-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="33c1b-143">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="33c1b-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33c1b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33c1b-144">CommonParameters</span></span>
<span data-ttu-id="33c1b-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="33c1b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33c1b-146">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="33c1b-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33c1b-147">입력</span><span class="sxs-lookup"><span data-stu-id="33c1b-147">INPUTS</span></span>

### <span data-ttu-id="33c1b-148">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="33c1b-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="33c1b-149">ApiManagement. ServiceManagement. \ PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="33c1b-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

### <span data-ttu-id="33c1b-150">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="33c1b-150">System.String</span></span>

### <span data-ttu-id="33c1b-151">ApiManagement. ServiceManagement. \ PsApiManagementVersioningScheme</span><span class="sxs-lookup"><span data-stu-id="33c1b-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementVersioningScheme</span></span>

## <span data-ttu-id="33c1b-152">출력</span><span class="sxs-lookup"><span data-stu-id="33c1b-152">OUTPUTS</span></span>

### <span data-ttu-id="33c1b-153">ApiManagement. ServiceManagement. \ PsApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="33c1b-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiVersionSet</span></span>

## <span data-ttu-id="33c1b-154">상속자</span><span class="sxs-lookup"><span data-stu-id="33c1b-154">NOTES</span></span>

## <span data-ttu-id="33c1b-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="33c1b-155">RELATED LINKS</span></span>

[<span data-ttu-id="33c1b-156">Get-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="33c1b-156">Get-AzApiManagementApiVersionSet</span></span>](./Get-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="33c1b-157">새로운 AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="33c1b-157">New-AzApiManagementApiVersionSet</span></span>](./New-AzApiManagementApiVersionSet.md)

[<span data-ttu-id="33c1b-158">Set-AzApiManagementApiVersionSet</span><span class="sxs-lookup"><span data-stu-id="33c1b-158">Set-AzApiManagementApiVersionSet</span></span>](./Set-AzApiManagementApiVersionSet.md)
