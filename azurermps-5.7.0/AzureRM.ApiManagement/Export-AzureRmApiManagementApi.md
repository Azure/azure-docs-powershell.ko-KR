---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 2BA76B02-B786-4A77-86E0-E7D4191120B5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/export-azurermapimanagementapi
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Export-AzureRmApiManagementApi.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Export-AzureRmApiManagementApi.md
ms.openlocfilehash: 3985f393e642645ddf9f023756e78db20074c214
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93538099"
---
# <span data-ttu-id="92f49-101">Export-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="92f49-101">Export-AzureRmApiManagementApi</span></span>

## <span data-ttu-id="92f49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92f49-102">SYNOPSIS</span></span>
<span data-ttu-id="92f49-103">API를 파일로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="92f49-103">Exports an API to a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92f49-104">구문과</span><span class="sxs-lookup"><span data-stu-id="92f49-104">SYNTAX</span></span>

### <span data-ttu-id="92f49-105">ExportToPipeline (기본값)</span><span class="sxs-lookup"><span data-stu-id="92f49-105">ExportToPipeline (Default)</span></span>
```
Export-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String>
 -SpecificationFormat <PsApiManagementApiFormat> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92f49-106">내보내기 Tofile</span><span class="sxs-lookup"><span data-stu-id="92f49-106">ExportToFile</span></span>
```
Export-AzureRmApiManagementApi -Context <PsApiManagementContext> -ApiId <String>
 -SpecificationFormat <PsApiManagementApiFormat> -SaveAs <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92f49-107">설명은</span><span class="sxs-lookup"><span data-stu-id="92f49-107">DESCRIPTION</span></span>
<span data-ttu-id="92f49-108">**Export-AzureRmApiManagementApi** cmdlet은 지원 되는 형식 중 하나로 Azure API Management api를 파일로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="92f49-108">The **Export-AzureRmApiManagementApi** cmdlet exports an Azure API Management API to a file in one of the supported formats.</span></span>

## <span data-ttu-id="92f49-109">예제의</span><span class="sxs-lookup"><span data-stu-id="92f49-109">EXAMPLES</span></span>

### <span data-ttu-id="92f49-110">예제 1: WADL (웹 응용 프로그램 설명 언어) 형식으로 API 내보내기</span><span class="sxs-lookup"><span data-stu-id="92f49-110">Example 1: Export an API in Web Application Description Language (WADL) format</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Export-AzureRmApiManagementApi -Context $ApiMgmtContext -ApiId "0123456789" -SpecificationFormat "Wadl" -SaveAs "C:\contoso\specifications\0123456789.wadl"
```

<span data-ttu-id="92f49-111">이 명령은 API를 WADL 파일로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="92f49-111">This command exports an API to a WADL file.</span></span>

## <span data-ttu-id="92f49-112">변수</span><span class="sxs-lookup"><span data-stu-id="92f49-112">PARAMETERS</span></span>

### <span data-ttu-id="92f49-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="92f49-113">-ApiId</span></span>
<span data-ttu-id="92f49-114">내보낼 API의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="92f49-114">Specifies the ID of the API to export.</span></span>

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

### <span data-ttu-id="92f49-115">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="92f49-115">-Context</span></span>
<span data-ttu-id="92f49-116">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="92f49-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="92f49-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92f49-117">-DefaultProfile</span></span>
<span data-ttu-id="92f49-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="92f49-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="92f49-119">-Force</span><span class="sxs-lookup"><span data-stu-id="92f49-119">-Force</span></span>
<span data-ttu-id="92f49-120">이 작업이 이미 있는 경우 같은 이름의 파일을 덮어쓰도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="92f49-120">Indicates that this operation overwrites the file of the same name if it already exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ExportToFile
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92f49-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="92f49-121">-PassThru</span></span>
<span data-ttu-id="92f49-122">API가 성공적으로 내보내질 경우이 작업이 $True를 반환 하 고, 그렇지 않은 경우 $False 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="92f49-122">Indicates that this operation returns $True if the API is exported successfully, or $False otherwise.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ExportToFile
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92f49-123">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="92f49-123">-SaveAs</span></span>
<span data-ttu-id="92f49-124">내보낸 API를 저장할 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="92f49-124">Specifies the file path to which to save the exported API.</span></span>

```yaml
Type: String
Parameter Sets: ExportToFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92f49-125">-사양 형식</span><span class="sxs-lookup"><span data-stu-id="92f49-125">-SpecificationFormat</span></span>
<span data-ttu-id="92f49-126">API 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="92f49-126">Specifies the API format.</span></span>
<span data-ttu-id="92f49-127">psdx_paramvalues Wadl 및 Swagger.</span><span class="sxs-lookup"><span data-stu-id="92f49-127">psdx_paramvalues Wadl and Swagger.</span></span>

```yaml
Type: PsApiManagementApiFormat
Parameter Sets: (All)
Aliases: 
Accepted values: Wadl, Swagger, Wsdl

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92f49-128">-확인</span><span class="sxs-lookup"><span data-stu-id="92f49-128">-Confirm</span></span>
<span data-ttu-id="92f49-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="92f49-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92f49-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92f49-130">-WhatIf</span></span>
<span data-ttu-id="92f49-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="92f49-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92f49-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="92f49-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92f49-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92f49-133">CommonParameters</span></span>
<span data-ttu-id="92f49-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="92f49-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92f49-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92f49-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92f49-136">입력</span><span class="sxs-lookup"><span data-stu-id="92f49-136">INPUTS</span></span>

### <span data-ttu-id="92f49-137">않아야</span><span class="sxs-lookup"><span data-stu-id="92f49-137">None</span></span>
<span data-ttu-id="92f49-138">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="92f49-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="92f49-139">출력</span><span class="sxs-lookup"><span data-stu-id="92f49-139">OUTPUTS</span></span>

### <span data-ttu-id="92f49-140">이름</span><span class="sxs-lookup"><span data-stu-id="92f49-140">String</span></span>
<span data-ttu-id="92f49-141">이 cmdlet은 내보낸 API 콘텐츠를 문자열로 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="92f49-141">This cmdlet returns the exported API content as a string.</span></span>

## <span data-ttu-id="92f49-142">상속자</span><span class="sxs-lookup"><span data-stu-id="92f49-142">NOTES</span></span>

## <span data-ttu-id="92f49-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="92f49-143">RELATED LINKS</span></span>

[<span data-ttu-id="92f49-144">Get-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="92f49-144">Get-AzureRmApiManagementApi</span></span>](./Get-AzureRmApiManagementApi.md)

[<span data-ttu-id="92f49-145">가져오기-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="92f49-145">Import-AzureRmApiManagementApi</span></span>](./Import-AzureRmApiManagementApi.md)

[<span data-ttu-id="92f49-146">새로운 AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="92f49-146">New-AzureRmApiManagementApi</span></span>](./New-AzureRmApiManagementApi.md)

[<span data-ttu-id="92f49-147">제거-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="92f49-147">Remove-AzureRmApiManagementApi</span></span>](./Remove-AzureRmApiManagementApi.md)

[<span data-ttu-id="92f49-148">Set-AzureRmApiManagementApi</span><span class="sxs-lookup"><span data-stu-id="92f49-148">Set-AzureRmApiManagementApi</span></span>](./Set-AzureRmApiManagementApi.md)


