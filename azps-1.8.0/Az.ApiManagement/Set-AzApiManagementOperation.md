---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 67EE6EFB-3297-4D21-A6EC-B03F5FE82F84
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOperation.md
ms.openlocfilehash: d30b48a7e1860610dc772555bc7e7428ec1ee3f1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869334"
---
# <span data-ttu-id="6a02e-101">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="6a02e-101">Set-AzApiManagementOperation</span></span>

## <span data-ttu-id="6a02e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a02e-102">SYNOPSIS</span></span>
<span data-ttu-id="6a02e-103">API 작업 세부 정보를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a02e-103">Sets API operation details.</span></span>

## <span data-ttu-id="6a02e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6a02e-104">SYNTAX</span></span>

```
Set-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6a02e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6a02e-105">DESCRIPTION</span></span>
<span data-ttu-id="6a02e-106">**AzApiManagementOperation** CMDLET은 API 작업 세부 정보를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a02e-106">The **Set-AzApiManagementOperation** cmdlet sets API operation details.</span></span>

## <span data-ttu-id="6a02e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6a02e-107">EXAMPLES</span></span>

### <span data-ttu-id="6a02e-108">예제 1: 작업 세부 정보 설정</span><span class="sxs-lookup"><span data-stu-id="6a02e-108">Example 1: Set the operation details</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementOperation -Context $apimContext -ApiId $APIID -OperationId $OperationId -Name "Get Resource" -Method GET -UrlTemplate "/newresource" -Description "Use this operation to get newresource"
```

<span data-ttu-id="6a02e-109">이 명령은 API management에 대 한 작업 세부 정보를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a02e-109">This command sets the operation details for API management.</span></span>

## <span data-ttu-id="6a02e-110">변수</span><span class="sxs-lookup"><span data-stu-id="6a02e-110">PARAMETERS</span></span>

### <span data-ttu-id="6a02e-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="6a02e-111">-ApiId</span></span>
<span data-ttu-id="6a02e-112">API의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a02e-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="6a02e-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="6a02e-113">-ApiRevision</span></span>
<span data-ttu-id="6a02e-114">API 개정판의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="6a02e-114">Identifier of API Revision.</span></span> <span data-ttu-id="6a02e-115">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="6a02e-115">This parameter is optional.</span></span> <span data-ttu-id="6a02e-116">지정 하지 않으면 현재 활성 상태인 api 개정판에서 작업이 업데이트 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6a02e-116">If not specified, the operation will be updated in the currently active api revision.</span></span>

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

### <span data-ttu-id="6a02e-117">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="6a02e-117">-Context</span></span>
<span data-ttu-id="6a02e-118">**PsApiManagementContext** 의 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a02e-118">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="6a02e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a02e-119">-DefaultProfile</span></span>
<span data-ttu-id="6a02e-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6a02e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a02e-121">-설명</span><span class="sxs-lookup"><span data-stu-id="6a02e-121">-Description</span></span>
<span data-ttu-id="6a02e-122">새 작업에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a02e-122">Specifies the description of the new operation.</span></span>

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

### <span data-ttu-id="6a02e-123">-메서드</span><span class="sxs-lookup"><span data-stu-id="6a02e-123">-Method</span></span>
<span data-ttu-id="6a02e-124">새 작업의 HTTP 메서드를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a02e-124">Specifies the HTTP method of the new operation.</span></span>

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

### <span data-ttu-id="6a02e-125">-이름</span><span class="sxs-lookup"><span data-stu-id="6a02e-125">-Name</span></span>
<span data-ttu-id="6a02e-126">새 작업의 표시 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a02e-126">Specifies the display name of the new operation.</span></span>

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

### <span data-ttu-id="6a02e-127">-OperationId</span><span class="sxs-lookup"><span data-stu-id="6a02e-127">-OperationId</span></span>
<span data-ttu-id="6a02e-128">기존 작업의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a02e-128">Specifies the identifier of the existing operation.</span></span>

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

### <span data-ttu-id="6a02e-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6a02e-129">-PassThru</span></span>
<span data-ttu-id="6a02e-130">passthru</span><span class="sxs-lookup"><span data-stu-id="6a02e-130">passthru</span></span>

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

### <span data-ttu-id="6a02e-131">-요청</span><span class="sxs-lookup"><span data-stu-id="6a02e-131">-Request</span></span>
<span data-ttu-id="6a02e-132">작업 요청 세부 정보를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a02e-132">Specifies the operation request details.</span></span>

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

### <span data-ttu-id="6a02e-133">-응답</span><span class="sxs-lookup"><span data-stu-id="6a02e-133">-Responses</span></span>
<span data-ttu-id="6a02e-134">사용할 수 있는 작업 응답의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a02e-134">Specifies an array of possible operation responses.</span></span>

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

### <span data-ttu-id="6a02e-135">-서식 매개 변수</span><span class="sxs-lookup"><span data-stu-id="6a02e-135">-TemplateParameters</span></span>
<span data-ttu-id="6a02e-136">매개 변수 *Urltemplate* 에 정의 된 배열 또는 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a02e-136">Specifies an array or parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="6a02e-137">값을 지정 하지 않으면 UrlTemplate에 따라 기본값이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6a02e-137">If you do not specify a value, a default value will be generated based on the UrlTemplate.</span></span>
<span data-ttu-id="6a02e-138">매개 변수를 사용 하 여 설명, 형식 및 기타 가능 값과 같은 매개 변수에 대 한 자세한 정보를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a02e-138">Use the parameter to give more details on parameters such as description, type, and other possible values.</span></span>

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

### <span data-ttu-id="6a02e-139">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="6a02e-139">-UrlTemplate</span></span>
<span data-ttu-id="6a02e-140">URL 서식 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a02e-140">Specifies the URL template.</span></span>
<span data-ttu-id="6a02e-141">예: 고객/{cid}/orders/{oid}/? date = {date}.</span><span class="sxs-lookup"><span data-stu-id="6a02e-141">For instance: customers/{cid}/orders/{oid}/?date={date}.</span></span>

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

### <span data-ttu-id="6a02e-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a02e-142">CommonParameters</span></span>
<span data-ttu-id="6a02e-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a02e-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a02e-144">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a02e-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a02e-145">입력</span><span class="sxs-lookup"><span data-stu-id="6a02e-145">INPUTS</span></span>

### <span data-ttu-id="6a02e-146">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6a02e-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6a02e-147">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6a02e-147">System.String</span></span>

### <span data-ttu-id="6a02e-148">ApiManagement [] ServiceManagement. PsApiManagementParameter []</span><span class="sxs-lookup"><span data-stu-id="6a02e-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]</span></span>

### <span data-ttu-id="6a02e-149">ApiManagement. ServiceManagement. \ PsApiManagementRequest</span><span class="sxs-lookup"><span data-stu-id="6a02e-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest</span></span>

### <span data-ttu-id="6a02e-150">ApiManagement [] ServiceManagement. PsApiManagementResponse []</span><span class="sxs-lookup"><span data-stu-id="6a02e-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]</span></span>

### <span data-ttu-id="6a02e-151">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="6a02e-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6a02e-152">출력</span><span class="sxs-lookup"><span data-stu-id="6a02e-152">OUTPUTS</span></span>

### <span data-ttu-id="6a02e-153">ApiManagement. ServiceManagement. \ PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="6a02e-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="6a02e-154">상속자</span><span class="sxs-lookup"><span data-stu-id="6a02e-154">NOTES</span></span>

## <span data-ttu-id="6a02e-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6a02e-155">RELATED LINKS</span></span>

[<span data-ttu-id="6a02e-156">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="6a02e-156">Get-AzApiManagementOperation</span></span>](./Get-AzApiManagementOperation.md)

[<span data-ttu-id="6a02e-157">새로운 AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="6a02e-157">New-AzApiManagementOperation</span></span>](./New-AzApiManagementOperation.md)

[<span data-ttu-id="6a02e-158">제거-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="6a02e-158">Remove-AzApiManagementOperation</span></span>](./Remove-AzApiManagementOperation.md)


