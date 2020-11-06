---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 67EE6EFB-3297-4D21-A6EC-B03F5FE82F84
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOperation.md
ms.openlocfilehash: 4800d7d56d03071b57d25cdacfcf271defa9276f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530580"
---
# <span data-ttu-id="bc253-101">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="bc253-101">Set-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="bc253-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc253-102">SYNOPSIS</span></span>
<span data-ttu-id="bc253-103">API 작업 세부 정보를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc253-103">Sets API operation details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bc253-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bc253-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bc253-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bc253-105">DESCRIPTION</span></span>
<span data-ttu-id="bc253-106">**AzureRmApiManagementOperation** CMDLET은 API 작업 세부 정보를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc253-106">The **Set-AzureRmApiManagementOperation** cmdlet sets API operation details.</span></span>

## <span data-ttu-id="bc253-107">예제의</span><span class="sxs-lookup"><span data-stu-id="bc253-107">EXAMPLES</span></span>

### <span data-ttu-id="bc253-108">예제 1: 작업 세부 정보 설정</span><span class="sxs-lookup"><span data-stu-id="bc253-108">Example 1: Set the operation details</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIID -OperationId $OperationId -Name "Get Resource" -Method GET -UrlTemplate "/newresource" -Description "Use this operation to get newresource"
```

<span data-ttu-id="bc253-109">이 명령은 API management에 대 한 작업 세부 정보를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc253-109">This command sets the operation details for API management.</span></span>

## <span data-ttu-id="bc253-110">변수</span><span class="sxs-lookup"><span data-stu-id="bc253-110">PARAMETERS</span></span>

### <span data-ttu-id="bc253-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="bc253-111">-ApiId</span></span>
<span data-ttu-id="bc253-112">API의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc253-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="bc253-113">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="bc253-113">-Context</span></span>
<span data-ttu-id="bc253-114">**PsApiManagementContext** 의 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc253-114">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="bc253-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc253-115">-DefaultProfile</span></span>
<span data-ttu-id="bc253-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bc253-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="bc253-117">-설명</span><span class="sxs-lookup"><span data-stu-id="bc253-117">-Description</span></span>
<span data-ttu-id="bc253-118">새 작업에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc253-118">Specifies the description of the new operation.</span></span>

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

### <span data-ttu-id="bc253-119">-메서드</span><span class="sxs-lookup"><span data-stu-id="bc253-119">-Method</span></span>
<span data-ttu-id="bc253-120">새 작업의 HTTP 메서드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc253-120">Specifies the HTTP method of the new operation.</span></span>

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

### <span data-ttu-id="bc253-121">-이름</span><span class="sxs-lookup"><span data-stu-id="bc253-121">-Name</span></span>
<span data-ttu-id="bc253-122">새 작업의 표시 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc253-122">Specifies the display name of the new operation.</span></span>

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

### <span data-ttu-id="bc253-123">-OperationId</span><span class="sxs-lookup"><span data-stu-id="bc253-123">-OperationId</span></span>
<span data-ttu-id="bc253-124">기존 작업의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc253-124">Specifies the identifier of the existing operation.</span></span>

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

### <span data-ttu-id="bc253-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bc253-125">-PassThru</span></span>
<span data-ttu-id="bc253-126">passthru</span><span class="sxs-lookup"><span data-stu-id="bc253-126">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc253-127">-요청</span><span class="sxs-lookup"><span data-stu-id="bc253-127">-Request</span></span>
<span data-ttu-id="bc253-128">작업 요청 세부 정보를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc253-128">Specifies the operation request details.</span></span>

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

### <span data-ttu-id="bc253-129">-응답</span><span class="sxs-lookup"><span data-stu-id="bc253-129">-Responses</span></span>
<span data-ttu-id="bc253-130">사용할 수 있는 작업 응답의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc253-130">Specifies an array of possible operation responses.</span></span>

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

### <span data-ttu-id="bc253-131">-서식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="bc253-131">-TemplateParameters</span></span>
<span data-ttu-id="bc253-132">매개 변수 *Urltemplate* 에 정의 된 배열 또는 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc253-132">Specifies an array or parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="bc253-133">값을 지정 하지 않으면 UrlTemplate에 따라 기본값이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bc253-133">If you do not specify a value, a default value will be generated based on the UrlTemplate.</span></span>
<span data-ttu-id="bc253-134">매개 변수를 사용 하 여 설명, 형식 및 기타 가능 값과 같은 매개 변수에 대 한 자세한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc253-134">Use the parameter to give more details on parameters such as description, type, and other possible values.</span></span>

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

### <span data-ttu-id="bc253-135">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="bc253-135">-UrlTemplate</span></span>
<span data-ttu-id="bc253-136">URL 서식 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc253-136">Specifies the URL template.</span></span>
<span data-ttu-id="bc253-137">예: 고객/{cid}/orders/{oid}/? date = {date}.</span><span class="sxs-lookup"><span data-stu-id="bc253-137">For instance: customers/{cid}/orders/{oid}/?date={date}.</span></span>

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

### <span data-ttu-id="bc253-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc253-138">CommonParameters</span></span>
<span data-ttu-id="bc253-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc253-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc253-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc253-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc253-141">입력</span><span class="sxs-lookup"><span data-stu-id="bc253-141">INPUTS</span></span>

### <span data-ttu-id="bc253-142">않아야</span><span class="sxs-lookup"><span data-stu-id="bc253-142">None</span></span>
<span data-ttu-id="bc253-143">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bc253-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bc253-144">출력</span><span class="sxs-lookup"><span data-stu-id="bc253-144">OUTPUTS</span></span>

### <span data-ttu-id="bc253-145">ApiManagement. ServiceManagement. \ PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="bc253-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="bc253-146">상속자</span><span class="sxs-lookup"><span data-stu-id="bc253-146">NOTES</span></span>

## <span data-ttu-id="bc253-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bc253-147">RELATED LINKS</span></span>

[<span data-ttu-id="bc253-148">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="bc253-148">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="bc253-149">새로운 AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="bc253-149">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="bc253-150">제거-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="bc253-150">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)


