---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2BA76B02-B786-4A77-86E0-E7D4191120B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/export-azapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Export-AzApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Export-AzApiManagementApi.md
ms.openlocfilehash: 1c322669431377b96f0bc45e1228c52ba70c6d68
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689165"
---
# <span data-ttu-id="e1110-101">Export-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e1110-101">Export-AzApiManagementApi</span></span>

## <span data-ttu-id="e1110-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1110-102">SYNOPSIS</span></span>
<span data-ttu-id="e1110-103">API를 파일로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="e1110-103">Exports an API to a file.</span></span>

## <span data-ttu-id="e1110-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e1110-104">SYNTAX</span></span>

### <span data-ttu-id="e1110-105">ExportToPipeline (기본값)</span><span class="sxs-lookup"><span data-stu-id="e1110-105">ExportToPipeline (Default)</span></span>
```
Export-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1110-106">내보내기 Tofile</span><span class="sxs-lookup"><span data-stu-id="e1110-106">ExportToFile</span></span>
```
Export-AzApiManagementApi -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -SpecificationFormat <PsApiManagementApiFormat> -SaveAs <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1110-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e1110-107">DESCRIPTION</span></span>
<span data-ttu-id="e1110-108">**Export-AzApiManagementApi** cmdlet은 지원 되는 형식 중 하나로 Azure API Management api를 파일로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="e1110-108">The **Export-AzApiManagementApi** cmdlet exports an Azure API Management API to a file in one of the supported formats.</span></span>

## <span data-ttu-id="e1110-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e1110-109">EXAMPLES</span></span>

### <span data-ttu-id="e1110-110">예제 1: WADL (웹 응용 프로그램 설명 언어) 형식으로 API 내보내기</span><span class="sxs-lookup"><span data-stu-id="e1110-110">Example 1: Export an API in Web Application Description Language (WADL) format</span></span>
```powershell
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Export-AzApiManagementApi -Context $ApiMgmtContext -ApiId "0123456789" -SpecificationFormat "Wadl" -SaveAs "C:\contoso\specifications\0123456789.wadl"
```

<span data-ttu-id="e1110-111">이 명령은 API를 WADL 파일로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="e1110-111">This command exports an API to a WADL file.</span></span>

## <span data-ttu-id="e1110-112">변수</span><span class="sxs-lookup"><span data-stu-id="e1110-112">PARAMETERS</span></span>

### <span data-ttu-id="e1110-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="e1110-113">-ApiId</span></span>
<span data-ttu-id="e1110-114">내보낼 API의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1110-114">Specifies the ID of the API to export.</span></span>

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

### <span data-ttu-id="e1110-115">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="e1110-115">-ApiRevision</span></span>
<span data-ttu-id="e1110-116">API 개정판의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="e1110-116">Identifier of API Revision.</span></span> <span data-ttu-id="e1110-117">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="e1110-117">This parameter is optional.</span></span> <span data-ttu-id="e1110-118">지정 하지 않으면 현재 활성 상태인 api 수정에 대해 내보내기가 완료 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e1110-118">If not specified, the export will be done for the currently active api revision.</span></span>

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

### <span data-ttu-id="e1110-119">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="e1110-119">-Context</span></span>
<span data-ttu-id="e1110-120">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1110-120">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="e1110-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1110-121">-DefaultProfile</span></span>
<span data-ttu-id="e1110-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e1110-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1110-123">-Force</span><span class="sxs-lookup"><span data-stu-id="e1110-123">-Force</span></span>
<span data-ttu-id="e1110-124">이 작업이 이미 있는 경우 같은 이름의 파일을 덮어쓰도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1110-124">Indicates that this operation overwrites the file of the same name if it already exists.</span></span>

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

### <span data-ttu-id="e1110-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e1110-125">-PassThru</span></span>
<span data-ttu-id="e1110-126">API가 성공적으로 내보내질 경우이 작업이 $True를 반환 하 고, 그렇지 않은 경우 $False 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e1110-126">Indicates that this operation returns $True if the API is exported successfully, or $False otherwise.</span></span>

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

### <span data-ttu-id="e1110-127">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="e1110-127">-SaveAs</span></span>
<span data-ttu-id="e1110-128">내보낸 API를 저장할 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1110-128">Specifies the file path to which to save the exported API.</span></span>

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

### <span data-ttu-id="e1110-129">-사양 형식</span><span class="sxs-lookup"><span data-stu-id="e1110-129">-SpecificationFormat</span></span>
<span data-ttu-id="e1110-130">API 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1110-130">Specifies the API format.</span></span>
<span data-ttu-id="e1110-131">psdx_paramvalues Wadl 및 Swagger.</span><span class="sxs-lookup"><span data-stu-id="e1110-131">psdx_paramvalues Wadl and Swagger.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat
Parameter Sets: (All)
Aliases:
Accepted values: Wadl, Swagger, Wsdl

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1110-132">-확인</span><span class="sxs-lookup"><span data-stu-id="e1110-132">-Confirm</span></span>
<span data-ttu-id="e1110-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1110-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1110-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1110-134">-WhatIf</span></span>
<span data-ttu-id="e1110-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e1110-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1110-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e1110-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1110-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1110-137">CommonParameters</span></span>
<span data-ttu-id="e1110-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1110-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1110-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1110-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1110-140">입력</span><span class="sxs-lookup"><span data-stu-id="e1110-140">INPUTS</span></span>

### <span data-ttu-id="e1110-141">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e1110-141">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e1110-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e1110-142">System.String</span></span>

### <span data-ttu-id="e1110-143">ApiManagement. ServiceManagement. \ PsApiManagementApiFormat</span><span class="sxs-lookup"><span data-stu-id="e1110-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiFormat</span></span>

### <span data-ttu-id="e1110-144">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="e1110-144">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e1110-145">출력</span><span class="sxs-lookup"><span data-stu-id="e1110-145">OUTPUTS</span></span>

### <span data-ttu-id="e1110-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e1110-146">System.String</span></span>

## <span data-ttu-id="e1110-147">상속자</span><span class="sxs-lookup"><span data-stu-id="e1110-147">NOTES</span></span>

## <span data-ttu-id="e1110-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e1110-148">RELATED LINKS</span></span>

[<span data-ttu-id="e1110-149">Get-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e1110-149">Get-AzApiManagementApi</span></span>](./Get-AzApiManagementApi.md)

[<span data-ttu-id="e1110-150">가져오기-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e1110-150">Import-AzApiManagementApi</span></span>](./Import-AzApiManagementApi.md)

[<span data-ttu-id="e1110-151">새로운 AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e1110-151">New-AzApiManagementApi</span></span>](./New-AzApiManagementApi.md)

[<span data-ttu-id="e1110-152">제거-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e1110-152">Remove-AzApiManagementApi</span></span>](./Remove-AzApiManagementApi.md)

[<span data-ttu-id="e1110-153">Set-AzApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="e1110-153">Set-AzApiManagementApi</span></span>](./Set-AzApiManagementApi.md)


