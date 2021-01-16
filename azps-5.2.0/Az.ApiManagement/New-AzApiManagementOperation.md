---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 0BC53178-8463-4EF5-8268-FBEC4753AD97
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementOperation.md
ms.openlocfilehash: 3cba96c2b68a3045448aa6f6f6ccd011964c6e16
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344330"
---
# <span data-ttu-id="98166-101">New-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="98166-101">New-AzApiManagementOperation</span></span>

## <span data-ttu-id="98166-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98166-102">SYNOPSIS</span></span>
<span data-ttu-id="98166-103">API 관리 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="98166-103">Creates an API management operation.</span></span>

## <span data-ttu-id="98166-104">구문</span><span class="sxs-lookup"><span data-stu-id="98166-104">SYNTAX</span></span>

```
New-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-OperationId <String>] -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98166-105">설명</span><span class="sxs-lookup"><span data-stu-id="98166-105">DESCRIPTION</span></span>
<span data-ttu-id="98166-106">**New-AzApiManagementOperation** cmdlet은 API 작업을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="98166-106">The **New-AzApiManagementOperation** cmdlet create an API operation.</span></span>

## <span data-ttu-id="98166-107">예제</span><span class="sxs-lookup"><span data-stu-id="98166-107">EXAMPLES</span></span>

### <span data-ttu-id="98166-108">예제 1: API 관리 작업 만들기</span><span class="sxs-lookup"><span data-stu-id="98166-108">Example 1: Create an API management operation</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation001" -Name "Operation" -Method "GET" -UrlTemplate "/resource" -Description "Use this operation to get resource"
```

<span data-ttu-id="98166-109">이 명령은 API 관리 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="98166-109">This command creates an API management operation.</span></span>

### <span data-ttu-id="98166-110">예제 2: 요청 및 응답 세부 정보를 사용하여 API 관리 작업 만들기</span><span class="sxs-lookup"><span data-stu-id="98166-110">Example 2: Create an API management operation with request and response details</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$RID = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter
$RID.Name = "RID"
$RID.Description = "Resource identifier"
$RID.Type = "string"
$Query = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter
$Query.Name = "query"
$Query.Description = "Query string"
$Query.Type = 'string'
$Request = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest
$Request.Description = "Create/update resource request"
$DummyQp = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter
$DummyQp.Name = 'dummy'
$DummyQp.Type = 'string'
$DummyQp.Required = $FALSE
$Request.QueryParameters = @($DummyQp)
$Header = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter
$Header.Name = 'x-custom-header'
$Header.Type = 'string'
$Request.Headers = @($Header)
$RequestRepresentation = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRepresentation
$RequestRepresentation.ContentType = 'application/json'
$RequestRepresentation.Sample = '{ "propName": "propValue" }'
$Request.Representations = @($requestRepresentation)
$Response = New-Object -TypeName Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse
$Response.StatusCode = 204
PS C:\>New-AzApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "01234567890" -Name 'Create/update resource' -Method 'PUT' -UrlTemplate '/resource/{rid}?q={query}' -Description "Use this operation to create new or update existing resource" -TemplateParameters @($rid, $query) -Request $Request -Responses @($response)
```

<span data-ttu-id="98166-111">이 예제에서는 요청 및 응답 세부 정보를 통해 API 관리 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="98166-111">This example creates an API management operation with request and response details.</span></span>

## <span data-ttu-id="98166-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="98166-112">PARAMETERS</span></span>

### <span data-ttu-id="98166-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="98166-113">-ApiId</span></span>
<span data-ttu-id="98166-114">API 관리 작업의 식별자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="98166-114">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="98166-115">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="98166-115">-ApiRevision</span></span>
<span data-ttu-id="98166-116">API 개정의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="98166-116">Identifier of API Revision.</span></span> <span data-ttu-id="98166-117">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="98166-117">This parameter is optional.</span></span> <span data-ttu-id="98166-118">지정하지 않으면 작업이 현재 활성 API 개정에 연결됩니다.</span><span class="sxs-lookup"><span data-stu-id="98166-118">If not specified, the operation will be attached to the currently active api revision.</span></span>

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

### <span data-ttu-id="98166-119">-Context</span><span class="sxs-lookup"><span data-stu-id="98166-119">-Context</span></span>
<span data-ttu-id="98166-120">**PsApiManagementContext** 개체의 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="98166-120">Specifies the instance of the **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98166-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98166-121">-DefaultProfile</span></span>
<span data-ttu-id="98166-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="98166-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98166-123">-Description</span><span class="sxs-lookup"><span data-stu-id="98166-123">-Description</span></span>
<span data-ttu-id="98166-124">새 API 작업에 대한 설명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="98166-124">Specifies the description of new API operation.</span></span>

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

### <span data-ttu-id="98166-125">-Method</span><span class="sxs-lookup"><span data-stu-id="98166-125">-Method</span></span>
<span data-ttu-id="98166-126">새 API 관리 작업의 HTTP 메서드를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="98166-126">Specifies the HTTP method of the new API management operation.</span></span>

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

### <span data-ttu-id="98166-127">-Name</span><span class="sxs-lookup"><span data-stu-id="98166-127">-Name</span></span>
<span data-ttu-id="98166-128">새 API 관리 작업의 표시 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="98166-128">Specifies the display name of new API management operation.</span></span>

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

### <span data-ttu-id="98166-129">-OperationId</span><span class="sxs-lookup"><span data-stu-id="98166-129">-OperationId</span></span>
<span data-ttu-id="98166-130">API 관리 작업의 식별자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="98166-130">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="98166-131">-Request</span><span class="sxs-lookup"><span data-stu-id="98166-131">-Request</span></span>
<span data-ttu-id="98166-132">API 관리 작업의 세부 정보를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="98166-132">Specifies the details of the API management operation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98166-133">-Responses</span><span class="sxs-lookup"><span data-stu-id="98166-133">-Responses</span></span>
<span data-ttu-id="98166-134">가능한 API Management 작업 응답의 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="98166-134">Specifies an array of possible API management operation responses.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98166-135">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="98166-135">-TemplateParameters</span></span>
<span data-ttu-id="98166-136">UrlTemplate 매개 변수에 정의된 매개 변수 *배열을 지정합니다.*</span><span class="sxs-lookup"><span data-stu-id="98166-136">Specifies an array of parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="98166-137">이 매개 변수를 지정하지 않으면 *UrlTemplate에 따라 기본값이 생성됩니다.*</span><span class="sxs-lookup"><span data-stu-id="98166-137">If you do not specify this parameter, a default value will be generated based on the *UrlTemplate*.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98166-138">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="98166-138">-UrlTemplate</span></span>
<span data-ttu-id="98166-139">URL 템플릿을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="98166-139">Specifies the URL template.</span></span>

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

### <span data-ttu-id="98166-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98166-140">CommonParameters</span></span>
<span data-ttu-id="98166-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="98166-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98166-142">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="98166-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98166-143">입력</span><span class="sxs-lookup"><span data-stu-id="98166-143">INPUTS</span></span>

### <span data-ttu-id="98166-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="98166-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="98166-145">System.String</span><span class="sxs-lookup"><span data-stu-id="98166-145">System.String</span></span>

### <span data-ttu-id="98166-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]</span><span class="sxs-lookup"><span data-stu-id="98166-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]</span></span>

### <span data-ttu-id="98166-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest</span><span class="sxs-lookup"><span data-stu-id="98166-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest</span></span>

### <span data-ttu-id="98166-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]</span><span class="sxs-lookup"><span data-stu-id="98166-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]</span></span>

## <span data-ttu-id="98166-149">출력</span><span class="sxs-lookup"><span data-stu-id="98166-149">OUTPUTS</span></span>

### <span data-ttu-id="98166-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="98166-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="98166-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="98166-151">NOTES</span></span>

## <span data-ttu-id="98166-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="98166-152">RELATED LINKS</span></span>

[<span data-ttu-id="98166-153">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="98166-153">Get-AzApiManagementOperation</span></span>](./Get-AzApiManagementOperation.md)

[<span data-ttu-id="98166-154">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="98166-154">Remove-AzApiManagementOperation</span></span>](./Remove-AzApiManagementOperation.md)

[<span data-ttu-id="98166-155">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="98166-155">Set-AzApiManagementOperation</span></span>](./Set-AzApiManagementOperation.md)

