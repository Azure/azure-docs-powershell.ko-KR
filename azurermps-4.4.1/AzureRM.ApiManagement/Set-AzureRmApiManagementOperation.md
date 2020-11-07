---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 67EE6EFB-3297-4D21-A6EC-B03F5FE82F84
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOperation.md
ms.openlocfilehash: 28bbc9158639faf066fa9a623f5dfacd6566d236
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93710994"
---
# <span data-ttu-id="4b352-101">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="4b352-101">Set-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="4b352-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b352-102">SYNOPSIS</span></span>
<span data-ttu-id="4b352-103">API 작업 세부 정보를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b352-103">Sets API operation details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b352-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4b352-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4b352-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4b352-105">DESCRIPTION</span></span>
<span data-ttu-id="4b352-106">**AzureRmApiManagementOperation** CMDLET은 API 작업 세부 정보를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b352-106">The **Set-AzureRmApiManagementOperation** cmdlet sets API operation details.</span></span>

## <span data-ttu-id="4b352-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4b352-107">EXAMPLES</span></span>

### <span data-ttu-id="4b352-108">예제 1: 작업 세부 정보 설정</span><span class="sxs-lookup"><span data-stu-id="4b352-108">Example 1: Set the operation details</span></span>
```
PS C:\>New-AzureRmApiManagementOperation -Context $APImContext -ApiId $APIID -OperationId $OperationId -Name "Get Resource" -Method GET -UrlTemplate "/newresource" -Description "Use this operation to get newresource"
```

<span data-ttu-id="4b352-109">이 명령은 API management에 대 한 작업 세부 정보를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b352-109">This command sets the operation details for API management.</span></span>

## <span data-ttu-id="4b352-110">변수</span><span class="sxs-lookup"><span data-stu-id="4b352-110">PARAMETERS</span></span>

### <span data-ttu-id="4b352-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="4b352-111">-ApiId</span></span>
<span data-ttu-id="4b352-112">API의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b352-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="4b352-113">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="4b352-113">-Context</span></span>
<span data-ttu-id="4b352-114">**PsApiManagementContext** 의 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b352-114">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="4b352-115">-설명</span><span class="sxs-lookup"><span data-stu-id="4b352-115">-Description</span></span>
<span data-ttu-id="4b352-116">새 작업에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b352-116">Specifies the description of the new operation.</span></span>

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

### <span data-ttu-id="4b352-117">-메서드</span><span class="sxs-lookup"><span data-stu-id="4b352-117">-Method</span></span>
<span data-ttu-id="4b352-118">새 작업의 HTTP 메서드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b352-118">Specifies the HTTP method of the new operation.</span></span>

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

### <span data-ttu-id="4b352-119">-이름</span><span class="sxs-lookup"><span data-stu-id="4b352-119">-Name</span></span>
<span data-ttu-id="4b352-120">새 작업의 표시 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b352-120">Specifies the display name of the new operation.</span></span>

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

### <span data-ttu-id="4b352-121">-OperationId</span><span class="sxs-lookup"><span data-stu-id="4b352-121">-OperationId</span></span>
<span data-ttu-id="4b352-122">기존 작업의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b352-122">Specifies the identifier of the existing operation.</span></span>

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

### <span data-ttu-id="4b352-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4b352-123">-PassThru</span></span>
<span data-ttu-id="4b352-124">passthru</span><span class="sxs-lookup"><span data-stu-id="4b352-124">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b352-125">-요청</span><span class="sxs-lookup"><span data-stu-id="4b352-125">-Request</span></span>
<span data-ttu-id="4b352-126">작업 요청 세부 정보를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b352-126">Specifies the operation request details.</span></span>

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

### <span data-ttu-id="4b352-127">-응답</span><span class="sxs-lookup"><span data-stu-id="4b352-127">-Responses</span></span>
<span data-ttu-id="4b352-128">사용할 수 있는 작업 응답의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b352-128">Specifies an array of possible operation responses.</span></span>

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

### <span data-ttu-id="4b352-129">-서식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="4b352-129">-TemplateParameters</span></span>
<span data-ttu-id="4b352-130">매개 변수 *Urltemplate* 에 정의 된 배열 또는 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b352-130">Specifies an array or parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="4b352-131">값을 지정 하지 않으면 UrlTemplate에 따라 기본값이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4b352-131">If you do not specify a value, a default value will be generated based on the UrlTemplate.</span></span>
<span data-ttu-id="4b352-132">매개 변수를 사용 하 여 설명, 형식 및 기타 가능 값과 같은 매개 변수에 대 한 자세한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b352-132">Use the parameter to give more details on parameters such as description, type, and other possible values.</span></span>

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

### <span data-ttu-id="4b352-133">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="4b352-133">-UrlTemplate</span></span>
<span data-ttu-id="4b352-134">URL 서식 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b352-134">Specifies the URL template.</span></span>
<span data-ttu-id="4b352-135">예: 고객/{cid}/orders/{oid}/? date = {date}.</span><span class="sxs-lookup"><span data-stu-id="4b352-135">For instance: customers/{cid}/orders/{oid}/?date={date}.</span></span>

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

### <span data-ttu-id="4b352-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b352-136">-DefaultProfile</span></span>
<span data-ttu-id="4b352-137">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4b352-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b352-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b352-138">CommonParameters</span></span>
<span data-ttu-id="4b352-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4b352-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b352-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b352-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b352-141">입력</span><span class="sxs-lookup"><span data-stu-id="4b352-141">INPUTS</span></span>

## <span data-ttu-id="4b352-142">출력</span><span class="sxs-lookup"><span data-stu-id="4b352-142">OUTPUTS</span></span>

### <span data-ttu-id="4b352-143">ApiManagement. ServiceManagement. \ PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="4b352-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="4b352-144">상속자</span><span class="sxs-lookup"><span data-stu-id="4b352-144">NOTES</span></span>

## <span data-ttu-id="4b352-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4b352-145">RELATED LINKS</span></span>

[<span data-ttu-id="4b352-146">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="4b352-146">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="4b352-147">새로운 AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="4b352-147">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="4b352-148">제거-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="4b352-148">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)


