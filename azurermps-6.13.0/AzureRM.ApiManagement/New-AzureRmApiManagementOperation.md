---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 0BC53178-8463-4EF5-8268-FBEC4753AD97
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOperation.md
ms.openlocfilehash: d7411b99847b76db5f6e01215b49056842d4e444
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526400"
---
# <span data-ttu-id="b0d14-101">New-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="b0d14-101">New-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="b0d14-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0d14-102">SYNOPSIS</span></span>
<span data-ttu-id="b0d14-103">API 관리 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b0d14-103">Creates an API management operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0d14-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b0d14-104">SYNTAX</span></span>

```
New-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 [-OperationId <String>] -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0d14-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b0d14-105">DESCRIPTION</span></span>
<span data-ttu-id="b0d14-106">**새 AzureRmApiManagementOperation** CMDLET은 API 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b0d14-106">The **New-AzureRmApiManagementOperation** cmdlet create an API operation.</span></span>

## <span data-ttu-id="b0d14-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b0d14-107">EXAMPLES</span></span>

### <span data-ttu-id="b0d14-108">예제 1: API management 작업 만들기</span><span class="sxs-lookup"><span data-stu-id="b0d14-108">Example 1: Create an API management operation</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation001" -Name "Operation" -Method "GET" -UrlTemplate "/resource" -Description "Use this operation to get resource"
```

<span data-ttu-id="b0d14-109">이 명령은 API 관리 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b0d14-109">This command creates an API management operation.</span></span>

### <span data-ttu-id="b0d14-110">예제 2: 요청 및 응답 세부 정보를 사용 하 여 API 관리 작업 만들기</span><span class="sxs-lookup"><span data-stu-id="b0d14-110">Example 2: Create an API management operation with request and response details</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
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
PS C:\>New-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "01234567890" -Name 'Create/update resource' -Method 'PUT' -UrlTemplate '/resource/{rid}?q={query}' -Description "Use this operation to create new or update existing resource" -TemplateParameters @($rid, $query) -Request $Request -Responses @($response)
```

<span data-ttu-id="b0d14-111">이 예제에서는 요청 및 응답 세부 정보를 사용 하 여 API 관리 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b0d14-111">This example creates an API management operation with request and response details.</span></span>

## <span data-ttu-id="b0d14-112">변수</span><span class="sxs-lookup"><span data-stu-id="b0d14-112">PARAMETERS</span></span>

### <span data-ttu-id="b0d14-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="b0d14-113">-ApiId</span></span>
<span data-ttu-id="b0d14-114">API management 작업의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0d14-114">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="b0d14-115">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="b0d14-115">-ApiRevision</span></span>
<span data-ttu-id="b0d14-116">API 개정판의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="b0d14-116">Identifier of API Revision.</span></span> <span data-ttu-id="b0d14-117">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="b0d14-117">This parameter is optional.</span></span> <span data-ttu-id="b0d14-118">지정 하지 않으면 작업이 현재 활성 api 개정판에 연결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b0d14-118">If not specified, the operation will be attached to the currently active api revision.</span></span>

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

### <span data-ttu-id="b0d14-119">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="b0d14-119">-Context</span></span>
<span data-ttu-id="b0d14-120">**PsApiManagementContext** 개체의 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0d14-120">Specifies the instance of the **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0d14-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0d14-121">-DefaultProfile</span></span>
<span data-ttu-id="b0d14-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b0d14-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0d14-123">-설명</span><span class="sxs-lookup"><span data-stu-id="b0d14-123">-Description</span></span>
<span data-ttu-id="b0d14-124">새 API 작업에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0d14-124">Specifies the description of new API operation.</span></span>

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

### <span data-ttu-id="b0d14-125">-메서드</span><span class="sxs-lookup"><span data-stu-id="b0d14-125">-Method</span></span>
<span data-ttu-id="b0d14-126">새 API 관리 작업의 HTTP 메서드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0d14-126">Specifies the HTTP method of the new API management operation.</span></span>

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

### <span data-ttu-id="b0d14-127">-이름</span><span class="sxs-lookup"><span data-stu-id="b0d14-127">-Name</span></span>
<span data-ttu-id="b0d14-128">새 API 관리 작업의 표시 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0d14-128">Specifies the display name of new API management operation.</span></span>

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

### <span data-ttu-id="b0d14-129">-OperationId</span><span class="sxs-lookup"><span data-stu-id="b0d14-129">-OperationId</span></span>
<span data-ttu-id="b0d14-130">API management 작업의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0d14-130">Specifies the identifier of the API management operation.</span></span>

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

### <span data-ttu-id="b0d14-131">-요청</span><span class="sxs-lookup"><span data-stu-id="b0d14-131">-Request</span></span>
<span data-ttu-id="b0d14-132">API management 작업의 세부 정보를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0d14-132">Specifies the details of the API management operation.</span></span>

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

### <span data-ttu-id="b0d14-133">-응답</span><span class="sxs-lookup"><span data-stu-id="b0d14-133">-Responses</span></span>
<span data-ttu-id="b0d14-134">사용할 수 있는 API management 작업 응답의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0d14-134">Specifies an array of possible API management operation responses.</span></span>

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

### <span data-ttu-id="b0d14-135">-서식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="b0d14-135">-TemplateParameters</span></span>
<span data-ttu-id="b0d14-136">매개 변수 *Urltemplate* 에 정의 된 매개 변수의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0d14-136">Specifies an array of parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="b0d14-137">이 매개 변수를 지정 하지 않으면 *Urltemplate* 에 따라 기본값이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b0d14-137">If you do not specify this parameter, a default value will be generated based on the *UrlTemplate*.</span></span>

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

### <span data-ttu-id="b0d14-138">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="b0d14-138">-UrlTemplate</span></span>
<span data-ttu-id="b0d14-139">URL 서식 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0d14-139">Specifies the URL template.</span></span>

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

### <span data-ttu-id="b0d14-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0d14-140">CommonParameters</span></span>
<span data-ttu-id="b0d14-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0d14-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0d14-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0d14-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0d14-143">입력</span><span class="sxs-lookup"><span data-stu-id="b0d14-143">INPUTS</span></span>

### <span data-ttu-id="b0d14-144">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b0d14-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b0d14-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b0d14-145">System.String</span></span>

### <span data-ttu-id="b0d14-146">ApiManagement [] ServiceManagement. PsApiManagementParameter []</span><span class="sxs-lookup"><span data-stu-id="b0d14-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]</span></span>

### <span data-ttu-id="b0d14-147">ApiManagement. ServiceManagement. \ PsApiManagementRequest</span><span class="sxs-lookup"><span data-stu-id="b0d14-147">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest</span></span>

### <span data-ttu-id="b0d14-148">ApiManagement [] ServiceManagement. PsApiManagementResponse []</span><span class="sxs-lookup"><span data-stu-id="b0d14-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]</span></span>

## <span data-ttu-id="b0d14-149">출력</span><span class="sxs-lookup"><span data-stu-id="b0d14-149">OUTPUTS</span></span>

### <span data-ttu-id="b0d14-150">ApiManagement. ServiceManagement. \ PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="b0d14-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="b0d14-151">상속자</span><span class="sxs-lookup"><span data-stu-id="b0d14-151">NOTES</span></span>

## <span data-ttu-id="b0d14-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b0d14-152">RELATED LINKS</span></span>

[<span data-ttu-id="b0d14-153">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="b0d14-153">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="b0d14-154">제거-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="b0d14-154">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)

[<span data-ttu-id="b0d14-155">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="b0d14-155">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)

