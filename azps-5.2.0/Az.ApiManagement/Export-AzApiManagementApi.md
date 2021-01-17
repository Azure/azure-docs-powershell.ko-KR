---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2BA76B02-B786-4A77-86E0-E7D4191120B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/export-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Export-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Export-AzApiManagementApi.md
ms.openlocfilehash: 3981d1fd0a921f467007afc85c00b726b6037fad
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351002"
---
# <span data-ttu-id="c7579-101">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c7579-101">Export-AzApiManagementApi</span></span>

## <span data-ttu-id="c7579-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7579-102">SYNOPSIS</span></span>
<span data-ttu-id="c7579-103">API를 파일로 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c7579-103">Exports an API to a file.</span></span>

## <span data-ttu-id="c7579-104">구문</span><span class="sxs-lookup"><span data-stu-id="c7579-104">SYNTAX</span></span>

### <span data-ttu-id="c7579-105">ExportToPipeline(기본값)</span><span class="sxs-lookup"><span data-stu-id="c7579-105">ExportToPipeline (Default)</span></span>
```
Export-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7579-106">ExportToFile</span><span class="sxs-lookup"><span data-stu-id="c7579-106">ExportToFile</span></span>
```
Export-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SaveAs <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7579-107">설명</span><span class="sxs-lookup"><span data-stu-id="c7579-107">DESCRIPTION</span></span>
<span data-ttu-id="c7579-108">**Export-AzApiManagementApi** cmdlet은 Azure API Management API를 지원되는 형식 중 하나의 파일로 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c7579-108">The **Export-AzApiManagementApi** cmdlet exports an Azure API Management API to a file in one of the supported formats.</span></span>

## <span data-ttu-id="c7579-109">예제</span><span class="sxs-lookup"><span data-stu-id="c7579-109">EXAMPLES</span></span>

### <span data-ttu-id="c7579-110">예제 1: WADL(웹 애플리케이션 설명 언어) 형식으로 API 내보내기</span><span class="sxs-lookup"><span data-stu-id="c7579-110">Example 1: Export an API in Web Application Description Language (WADL) format</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Export-AzApiManagementApi -Context $ApiMgmtContext -ApiId "0123456789" -SpecificationFormat "Wadl" -SaveAs "C:\contoso\specifications\0123456789.wadl"
```

<span data-ttu-id="c7579-111">이 명령은 API를 WADL 파일로 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c7579-111">This command exports an API to a WADL file.</span></span>

### <span data-ttu-id="c7579-112">예제 2: OpenApi 3.0 사양 형식으로 Json 문서로 API 내보내기</span><span class="sxs-lookup"><span data-stu-id="c7579-112">Example 2: Export an API in OpenApi 3.0 Specification Format as Json Document</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Export-AzApiManagementApi -Context $context -ApiId swagger-petstore -SpecificationFormat OpenApiJson -SaveAs D:\github\petstore.json
```

<span data-ttu-id="c7579-113">이 명령은 Api 정의를 Open Api 형식으로 Json 문서로 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c7579-113">This command exports an API definitions in Open Api format as Json document</span></span>

## <span data-ttu-id="c7579-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c7579-114">PARAMETERS</span></span>

### <span data-ttu-id="c7579-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="c7579-115">-ApiId</span></span>
<span data-ttu-id="c7579-116">내보낼 API의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c7579-116">Specifies the ID of the API to export.</span></span>

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

### <span data-ttu-id="c7579-117">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="c7579-117">-ApiRevision</span></span>
<span data-ttu-id="c7579-118">API 개정의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="c7579-118">Identifier of API Revision.</span></span> <span data-ttu-id="c7579-119">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="c7579-119">This parameter is optional.</span></span> <span data-ttu-id="c7579-120">지정하지 않으면 현재 활성 API 개정에 대해 내보내기 수행됩니다.</span><span class="sxs-lookup"><span data-stu-id="c7579-120">If not specified, the export will be done for the currently active api revision.</span></span>

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

### <span data-ttu-id="c7579-121">-Context</span><span class="sxs-lookup"><span data-stu-id="c7579-121">-Context</span></span>
<span data-ttu-id="c7579-122">**PsApiManagementContext 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="c7579-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="c7579-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7579-123">-DefaultProfile</span></span>
<span data-ttu-id="c7579-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c7579-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7579-125">-Force</span><span class="sxs-lookup"><span data-stu-id="c7579-125">-Force</span></span>
<span data-ttu-id="c7579-126">이 작업이 이미 있는 경우 동일한 이름의 파일을 덮어써야 를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c7579-126">Indicates that this operation overwrites the file of the same name if it already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExportToFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7579-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c7579-127">-PassThru</span></span>
<span data-ttu-id="c7579-128">API를 성공적으로 내보내거나 $True 경우 이 작업이 $False 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c7579-128">Indicates that this operation returns $True if the API is exported successfully, or $False otherwise.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExportToFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7579-129">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="c7579-129">-SaveAs</span></span>
<span data-ttu-id="c7579-130">내보낼 API를 저장할 파일 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c7579-130">Specifies the file path to which to save the exported API.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportToFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7579-131">-SpecificationFormat</span><span class="sxs-lookup"><span data-stu-id="c7579-131">-SpecificationFormat</span></span>
<span data-ttu-id="c7579-132">API 형식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c7579-132">Specifies the API format.</span></span>
<span data-ttu-id="c7579-133">psdx_paramvalues Wadl, Wsdl, Swagger, OpenApi 및 OpenApiJson</span><span class="sxs-lookup"><span data-stu-id="c7579-133">psdx_paramvalues Wadl, Wsdl, Swagger, OpenApi and OpenApiJson</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat
Parameter Sets: (All)
Aliases:
Accepted values: Wadl, Swagger, Wsdl, OpenApi, OpenApiJson

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7579-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c7579-134">-Confirm</span></span>
<span data-ttu-id="c7579-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c7579-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7579-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7579-136">-WhatIf</span></span>
<span data-ttu-id="c7579-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c7579-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7579-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c7579-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7579-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7579-139">CommonParameters</span></span>
<span data-ttu-id="c7579-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c7579-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7579-141">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c7579-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7579-142">입력</span><span class="sxs-lookup"><span data-stu-id="c7579-142">INPUTS</span></span>

### <span data-ttu-id="c7579-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c7579-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c7579-144">System.String</span><span class="sxs-lookup"><span data-stu-id="c7579-144">System.String</span></span>

### <span data-ttu-id="c7579-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span><span class="sxs-lookup"><span data-stu-id="c7579-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="c7579-146">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c7579-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c7579-147">출력</span><span class="sxs-lookup"><span data-stu-id="c7579-147">OUTPUTS</span></span>

### <span data-ttu-id="c7579-148">System.String</span><span class="sxs-lookup"><span data-stu-id="c7579-148">System.String</span></span>

## <span data-ttu-id="c7579-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c7579-149">NOTES</span></span>

## <span data-ttu-id="c7579-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c7579-150">RELATED LINKS</span></span>

[<span data-ttu-id="c7579-151">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c7579-151">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="c7579-152">Import-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c7579-152">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="c7579-153">New-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c7579-153">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="c7579-154">Remove-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c7579-154">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="c7579-155">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="c7579-155">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


