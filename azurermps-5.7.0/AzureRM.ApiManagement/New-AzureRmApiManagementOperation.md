---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 0BC53178-8463-4EF5-8268-FBEC4753AD97
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementOperation.md
ms.openlocfilehash: 36560b23d9108ff1f8cd981abdb44a3c24f25402
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525407"
---
# <span data-ttu-id="f6b5a-101">New-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="f6b5a-101">New-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="f6b5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6b5a-102">SYNOPSIS</span></span>
<span data-ttu-id="f6b5a-103">API 관리 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f6b5a-103">Creates an API management operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6b5a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f6b5a-104">SYNTAX</span></span>

```
New-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-OperationId <String>]
 -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6b5a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f6b5a-105">DESCRIPTION</span></span>
<span data-ttu-id="f6b5a-106">**새 AzureRmApiManagementOperation** CMDLET은 API 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f6b5a-106">The **New-AzureRmApiManagementOperation** cmdlet create an API operation.</span></span>

## <span data-ttu-id="f6b5a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f6b5a-107">EXAMPLES</span></span>

### <span data-ttu-id="f6b5a-108">예제 1: API management 작업 만들기</span><span class="sxs-lookup"><span data-stu-id="f6b5a-108">Example 1: Create an API management operation</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIId -OperationId "Operation001" -Name "Operation" -Method "GET" -UrlTemplate "/resource" -Description "Use this operation to get resource"
```

<span data-ttu-id="f6b5a-109">이 명령은 API 관리 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f6b5a-109">This command creates an API management operation.</span></span>

### <span data-ttu-id="f6b5a-110">예제 2: 요청 및 응답 세부 정보를 사용 하 여 API 관리 작업 만들기</span><span class="sxs-lookup"><span data-stu-id="f6b5a-110">Example 2: Create an API management operation with request and response details</span></span>
```
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

<span data-ttu-id="f6b5a-111">이 예제에서는 요청 및 응답 세부 정보를 사용 하 여 API 관리 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f6b5a-111">This example creates an API management operation with request and response details.</span></span>

## <span data-ttu-id="f6b5a-112">변수</span><span class="sxs-lookup"><span data-stu-id="f6b5a-112">PARAMETERS</span></span>

### <span data-ttu-id="f6b5a-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="f6b5a-113">-ApiId</span></span>
<span data-ttu-id="f6b5a-114">API management 작업의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6b5a-114">Specifies the identifier of the API management operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6b5a-115">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="f6b5a-115">-Context</span></span>
<span data-ttu-id="f6b5a-116">**PsApiManagementContext** 개체의 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6b5a-116">Specifies the instance of the **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6b5a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6b5a-117">-DefaultProfile</span></span>
<span data-ttu-id="f6b5a-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f6b5a-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6b5a-119">-설명</span><span class="sxs-lookup"><span data-stu-id="f6b5a-119">-Description</span></span>
<span data-ttu-id="f6b5a-120">새 API 작업에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6b5a-120">Specifies the description of new API operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6b5a-121">-메서드</span><span class="sxs-lookup"><span data-stu-id="f6b5a-121">-Method</span></span>
<span data-ttu-id="f6b5a-122">새 API 관리 작업의 HTTP 메서드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6b5a-122">Specifies the HTTP method of the new API management operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6b5a-123">-이름</span><span class="sxs-lookup"><span data-stu-id="f6b5a-123">-Name</span></span>
<span data-ttu-id="f6b5a-124">새 API 관리 작업의 표시 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6b5a-124">Specifies the display name of new API management operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6b5a-125">-OperationId</span><span class="sxs-lookup"><span data-stu-id="f6b5a-125">-OperationId</span></span>
<span data-ttu-id="f6b5a-126">API management 작업의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6b5a-126">Specifies the identifier of the API management operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6b5a-127">-요청</span><span class="sxs-lookup"><span data-stu-id="f6b5a-127">-Request</span></span>
<span data-ttu-id="f6b5a-128">API management 작업의 세부 정보를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6b5a-128">Specifies the details of the API management operation.</span></span>

```yaml
Type: PsApiManagementRequest
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6b5a-129">-응답</span><span class="sxs-lookup"><span data-stu-id="f6b5a-129">-Responses</span></span>
<span data-ttu-id="f6b5a-130">사용할 수 있는 API management 작업 응답의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6b5a-130">Specifies an array of possible API management operation responses.</span></span>

```yaml
Type: PsApiManagementResponse[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6b5a-131">-서식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="f6b5a-131">-TemplateParameters</span></span>
<span data-ttu-id="f6b5a-132">매개 변수 *Urltemplate* 에 정의 된 매개 변수의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6b5a-132">Specifies an array of parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="f6b5a-133">이 매개 변수를 지정 하지 않으면 *Urltemplate* 에 따라 기본값이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f6b5a-133">If you do not specify this parameter, a default value will be generated based on the *UrlTemplate*.</span></span>

```yaml
Type: PsApiManagementParameter[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6b5a-134">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="f6b5a-134">-UrlTemplate</span></span>
<span data-ttu-id="f6b5a-135">URL 서식 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6b5a-135">Specifies the URL template.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6b5a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6b5a-136">CommonParameters</span></span>
<span data-ttu-id="f6b5a-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6b5a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6b5a-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6b5a-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6b5a-139">입력</span><span class="sxs-lookup"><span data-stu-id="f6b5a-139">INPUTS</span></span>

### <span data-ttu-id="f6b5a-140">않아야</span><span class="sxs-lookup"><span data-stu-id="f6b5a-140">None</span></span>
<span data-ttu-id="f6b5a-141">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f6b5a-141">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f6b5a-142">출력</span><span class="sxs-lookup"><span data-stu-id="f6b5a-142">OUTPUTS</span></span>

### <span data-ttu-id="f6b5a-143">ApiManagement. ServiceManagement. \ PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="f6b5a-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="f6b5a-144">상속자</span><span class="sxs-lookup"><span data-stu-id="f6b5a-144">NOTES</span></span>

## <span data-ttu-id="f6b5a-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f6b5a-145">RELATED LINKS</span></span>

[<span data-ttu-id="f6b5a-146">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="f6b5a-146">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="f6b5a-147">제거-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="f6b5a-147">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)

[<span data-ttu-id="f6b5a-148">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="f6b5a-148">Set-AzureRmApiManagementOperation</span></span>](./Set-AzureRmApiManagementOperation.md)


