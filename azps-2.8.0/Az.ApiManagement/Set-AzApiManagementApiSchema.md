---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementApiSchema.md
ms.openlocfilehash: 02091c1a207bc10fbdb539fb9a301d002b631827
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697949"
---
# <span data-ttu-id="0611e-101">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="0611e-101">Set-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="0611e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0611e-102">SYNOPSIS</span></span>
<span data-ttu-id="0611e-103">API 스키마 수정</span><span class="sxs-lookup"><span data-stu-id="0611e-103">Modifies an API Schema</span></span>

## <span data-ttu-id="0611e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0611e-104">SYNTAX</span></span>

### <span data-ttu-id="0611e-105">ExpandedParameter (기본값)</span><span class="sxs-lookup"><span data-stu-id="0611e-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> -SchemaId <String>
 [-SchemaDocumentContentType <String>] [-SchemaDocument <String>] [-SchemaDocumentFilePath <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0611e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0611e-106">ByInputObject</span></span>
```
Set-AzApiManagementApiSchema -InputObject <PsApiManagementApiSchema> [-SchemaDocumentContentType <String>]
 [-SchemaDocument <String>] [-SchemaDocumentFilePath <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0611e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0611e-107">ByResourceId</span></span>
```
Set-AzApiManagementApiSchema -ResourceId <String> [-SchemaDocumentContentType <String>]
 [-SchemaDocument <String>] [-SchemaDocumentFilePath <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0611e-108">설명은</span><span class="sxs-lookup"><span data-stu-id="0611e-108">DESCRIPTION</span></span>
<span data-ttu-id="0611e-109">**AzApiManagementApiSchema** Cmdlet은 Azure API Management api 스키마를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0611e-109">The **Set-AzApiManagementApiSchema** cmdlet modifies an Azure API Management API Schema.</span></span>

## <span data-ttu-id="0611e-110">예제의</span><span class="sxs-lookup"><span data-stu-id="0611e-110">EXAMPLES</span></span>

### <span data-ttu-id="0611e-111">예제 1: API 스키마 수정</span><span class="sxs-lookup"><span data-stu-id="0611e-111">Example 1 : Modifies an API Schema</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementApiSchema -Context $ApiMgmtContext -ApiId "echo-api" -SchemaId "2"
```

<span data-ttu-id="0611e-112">이 예제에서는 Api 스키마를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0611e-112">The example updates the Api Schema</span></span>

## <span data-ttu-id="0611e-113">변수</span><span class="sxs-lookup"><span data-stu-id="0611e-113">PARAMETERS</span></span>

### <span data-ttu-id="0611e-114">-ApiId</span><span class="sxs-lookup"><span data-stu-id="0611e-114">-ApiId</span></span>
<span data-ttu-id="0611e-115">기존 API의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="0611e-115">Identifier of existing API.</span></span>
<span data-ttu-id="0611e-116">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="0611e-116">This parameter is required.</span></span>

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

### <span data-ttu-id="0611e-117">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="0611e-117">-Context</span></span>
<span data-ttu-id="0611e-118">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="0611e-118">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="0611e-119">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="0611e-119">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0611e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0611e-120">-DefaultProfile</span></span>
<span data-ttu-id="0611e-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0611e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0611e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0611e-122">-InputObject</span></span>
<span data-ttu-id="0611e-123">PsApiManagementApiSchema의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="0611e-123">Instance of PsApiManagementApiSchema.</span></span>
<span data-ttu-id="0611e-124">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="0611e-124">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0611e-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0611e-125">-PassThru</span></span>
<span data-ttu-id="0611e-126">지정한 경우, set API를 나타내는 ApiManagement의 인스턴스를 PsApiManagementApi 형식으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0611e-126">If specified then instance of Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi type representing the set API.</span></span>

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

### <span data-ttu-id="0611e-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0611e-127">-ResourceId</span></span>
<span data-ttu-id="0611e-128">진단 또는 Api 스키마의 팔 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="0611e-128">Arm ResourceId of Diagnostic or Api Schema.</span></span> <span data-ttu-id="0611e-129">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="0611e-129">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0611e-130">-SchemaDocument</span><span class="sxs-lookup"><span data-stu-id="0611e-130">-SchemaDocument</span></span>
<span data-ttu-id="0611e-131">Api 스키마 문서를 문자열로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0611e-131">Api schema document as a string.</span></span> <span data-ttu-id="0611e-132">이 매개 변수는 필수입니다-SchemaDocumentFile가 지정 되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="0611e-132">This parameter is required is -SchemaDocumentFile is not specified.</span></span>

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

### <span data-ttu-id="0611e-133">-SchemaDocumentContentType</span><span class="sxs-lookup"><span data-stu-id="0611e-133">-SchemaDocumentContentType</span></span>
<span data-ttu-id="0611e-134">Api 스키마의 ContentType</span><span class="sxs-lookup"><span data-stu-id="0611e-134">ContentType of the api Schema.</span></span> <span data-ttu-id="0611e-135">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="0611e-135">This parameter is optional.</span></span>

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

### <span data-ttu-id="0611e-136">-SchemaDocumentFilePath</span><span class="sxs-lookup"><span data-stu-id="0611e-136">-SchemaDocumentFilePath</span></span>
<span data-ttu-id="0611e-137">Api 스키마 문서 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="0611e-137">Api schema document file path.</span></span> <span data-ttu-id="0611e-138">이 매개 변수는 필수입니다-SchemaDocument가 지정 되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="0611e-138">This parameter is required is -SchemaDocument is not specified.</span></span>

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

### <span data-ttu-id="0611e-139">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="0611e-139">-SchemaId</span></span>
<span data-ttu-id="0611e-140">기존 스키마의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="0611e-140">Identifier of existing Schema.</span></span>
<span data-ttu-id="0611e-141">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="0611e-141">This parameter is required.</span></span>

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

### <span data-ttu-id="0611e-142">-확인</span><span class="sxs-lookup"><span data-stu-id="0611e-142">-Confirm</span></span>
<span data-ttu-id="0611e-143">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0611e-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0611e-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0611e-144">-WhatIf</span></span>
<span data-ttu-id="0611e-145">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0611e-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0611e-146">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0611e-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0611e-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0611e-147">CommonParameters</span></span>
<span data-ttu-id="0611e-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0611e-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0611e-149">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0611e-149">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0611e-150">입력</span><span class="sxs-lookup"><span data-stu-id="0611e-150">INPUTS</span></span>

### <span data-ttu-id="0611e-151">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="0611e-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="0611e-152">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0611e-152">System.String</span></span>

### <span data-ttu-id="0611e-153">ApiManagement. ServiceManagement. \ PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="0611e-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

### <span data-ttu-id="0611e-154">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="0611e-154">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="0611e-155">출력</span><span class="sxs-lookup"><span data-stu-id="0611e-155">OUTPUTS</span></span>

### <span data-ttu-id="0611e-156">ApiManagement. ServiceManagement. \ PsApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="0611e-156">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApi</span></span>

## <span data-ttu-id="0611e-157">상속자</span><span class="sxs-lookup"><span data-stu-id="0611e-157">NOTES</span></span>

## <span data-ttu-id="0611e-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0611e-158">RELATED LINKS</span></span>

[<span data-ttu-id="0611e-159">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="0611e-159">Get-AzApiManagementApiSchema</span></span>](./Get-AzApiManagementApiSchema.md)

[<span data-ttu-id="0611e-160">새로운 AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="0611e-160">New-AzApiManagementApiSchema</span></span>](./New-AzApiManagementApiSchema.md)

[<span data-ttu-id="0611e-161">제거-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="0611e-161">Remove-AzApiManagementApiSchema</span></span>](./Remove-AzApiManagementApiSchema.md)

