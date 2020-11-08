---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2BA76B02-B786-4A77-86E0-E7D4191120B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/export-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Export-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Export-AzApiManagementApi.md
ms.openlocfilehash: 3981d1fd0a921f467007afc85c00b726b6037fad
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041959"
---
# <span data-ttu-id="f4ef9-101">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="f4ef9-101">Export-AzApiManagementApi</span></span>

## <span data-ttu-id="f4ef9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4ef9-102">SYNOPSIS</span></span>
<span data-ttu-id="f4ef9-103">API를 파일로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="f4ef9-103">Exports an API to a file.</span></span>

## <span data-ttu-id="f4ef9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f4ef9-104">SYNTAX</span></span>

### <span data-ttu-id="f4ef9-105">ExportToPipeline (기본값)</span><span class="sxs-lookup"><span data-stu-id="f4ef9-105">ExportToPipeline (Default)</span></span>
```
Export-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4ef9-106">내보내기 Tofile</span><span class="sxs-lookup"><span data-stu-id="f4ef9-106">ExportToFile</span></span>
```
Export-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SaveAs <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4ef9-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f4ef9-107">DESCRIPTION</span></span>
<span data-ttu-id="f4ef9-108">**Export-AzApiManagementApi** cmdlet은 지원 되는 형식 중 하나로 Azure API Management api를 파일로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="f4ef9-108">The **Export-AzApiManagementApi** cmdlet exports an Azure API Management API to a file in one of the supported formats.</span></span>

## <span data-ttu-id="f4ef9-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f4ef9-109">EXAMPLES</span></span>

### <span data-ttu-id="f4ef9-110">예제 1: WADL (웹 응용 프로그램 설명 언어) 형식으로 API 내보내기</span><span class="sxs-lookup"><span data-stu-id="f4ef9-110">Example 1: Export an API in Web Application Description Language (WADL) format</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Export-AzApiManagementApi -Context $ApiMgmtContext -ApiId "0123456789" -SpecificationFormat "Wadl" -SaveAs "C:\contoso\specifications\0123456789.wadl"
```

<span data-ttu-id="f4ef9-111">이 명령은 API를 WADL 파일로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="f4ef9-111">This command exports an API to a WADL file.</span></span>

### <span data-ttu-id="f4ef9-112">예제 2: OpenApi 3.0 사양의 서식에서 API를 Json 문서로 내보내기</span><span class="sxs-lookup"><span data-stu-id="f4ef9-112">Example 2: Export an API in OpenApi 3.0 Specification Format as Json Document</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Export-AzApiManagementApi -Context $context -ApiId swagger-petstore -SpecificationFormat OpenApiJson -SaveAs D:\github\petstore.json
```

<span data-ttu-id="f4ef9-113">이 명령은 열려 있는 Api 형식의 API 정의를 Json 문서로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="f4ef9-113">This command exports an API definitions in Open Api format as Json document</span></span>

## <span data-ttu-id="f4ef9-114">변수</span><span class="sxs-lookup"><span data-stu-id="f4ef9-114">PARAMETERS</span></span>

### <span data-ttu-id="f4ef9-115">-ApiId</span><span class="sxs-lookup"><span data-stu-id="f4ef9-115">-ApiId</span></span>
<span data-ttu-id="f4ef9-116">내보낼 API의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4ef9-116">Specifies the ID of the API to export.</span></span>

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

### <span data-ttu-id="f4ef9-117">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="f4ef9-117">-ApiRevision</span></span>
<span data-ttu-id="f4ef9-118">API 개정판의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="f4ef9-118">Identifier of API Revision.</span></span> <span data-ttu-id="f4ef9-119">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="f4ef9-119">This parameter is optional.</span></span> <span data-ttu-id="f4ef9-120">지정 하지 않으면 현재 활성 상태인 api 수정에 대해 내보내기가 완료 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f4ef9-120">If not specified, the export will be done for the currently active api revision.</span></span>

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

### <span data-ttu-id="f4ef9-121">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="f4ef9-121">-Context</span></span>
<span data-ttu-id="f4ef9-122">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4ef9-122">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="f4ef9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4ef9-123">-DefaultProfile</span></span>
<span data-ttu-id="f4ef9-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f4ef9-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4ef9-125">-Force</span><span class="sxs-lookup"><span data-stu-id="f4ef9-125">-Force</span></span>
<span data-ttu-id="f4ef9-126">이 작업이 이미 있는 경우 같은 이름의 파일을 덮어쓰도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4ef9-126">Indicates that this operation overwrites the file of the same name if it already exists.</span></span>

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

### <span data-ttu-id="f4ef9-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f4ef9-127">-PassThru</span></span>
<span data-ttu-id="f4ef9-128">API가 성공적으로 내보내질 경우이 작업이 $True를 반환 하 고, 그렇지 않은 경우 $False 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f4ef9-128">Indicates that this operation returns $True if the API is exported successfully, or $False otherwise.</span></span>

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

### <span data-ttu-id="f4ef9-129">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="f4ef9-129">-SaveAs</span></span>
<span data-ttu-id="f4ef9-130">내보낸 API를 저장할 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4ef9-130">Specifies the file path to which to save the exported API.</span></span>

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

### <span data-ttu-id="f4ef9-131">-사양 형식</span><span class="sxs-lookup"><span data-stu-id="f4ef9-131">-SpecificationFormat</span></span>
<span data-ttu-id="f4ef9-132">API 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4ef9-132">Specifies the API format.</span></span>
<span data-ttu-id="f4ef9-133">psdx_paramvalues Wadl, Wsdl, Swagger, OpenApi 및 OpenApiJson</span><span class="sxs-lookup"><span data-stu-id="f4ef9-133">psdx_paramvalues Wadl, Wsdl, Swagger, OpenApi and OpenApiJson</span></span>

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

### <span data-ttu-id="f4ef9-134">-확인</span><span class="sxs-lookup"><span data-stu-id="f4ef9-134">-Confirm</span></span>
<span data-ttu-id="f4ef9-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4ef9-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4ef9-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4ef9-136">-WhatIf</span></span>
<span data-ttu-id="f4ef9-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f4ef9-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4ef9-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f4ef9-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4ef9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4ef9-139">CommonParameters</span></span>
<span data-ttu-id="f4ef9-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4ef9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4ef9-141">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f4ef9-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4ef9-142">입력</span><span class="sxs-lookup"><span data-stu-id="f4ef9-142">INPUTS</span></span>

### <span data-ttu-id="f4ef9-143">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f4ef9-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f4ef9-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f4ef9-144">System.String</span></span>

### <span data-ttu-id="f4ef9-145">ApiManagement. ServiceManagement. \ PsApiManagementApiFormat</span><span class="sxs-lookup"><span data-stu-id="f4ef9-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="f4ef9-146">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="f4ef9-146">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f4ef9-147">출력</span><span class="sxs-lookup"><span data-stu-id="f4ef9-147">OUTPUTS</span></span>

### <span data-ttu-id="f4ef9-148">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f4ef9-148">System.String</span></span>

## <span data-ttu-id="f4ef9-149">상속자</span><span class="sxs-lookup"><span data-stu-id="f4ef9-149">NOTES</span></span>

## <span data-ttu-id="f4ef9-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f4ef9-150">RELATED LINKS</span></span>

[<span data-ttu-id="f4ef9-151">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="f4ef9-151">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="f4ef9-152">가져오기-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="f4ef9-152">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="f4ef9-153">새로운 AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="f4ef9-153">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="f4ef9-154">제거-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="f4ef9-154">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="f4ef9-155">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="f4ef9-155">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


