---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiSchema.md
ms.openlocfilehash: 7714c9118364f0d2ecc6e8773983acb916702281
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178105"
---
# <span data-ttu-id="17193-101">New-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="17193-101">New-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="17193-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17193-102">SYNOPSIS</span></span>
<span data-ttu-id="17193-103">ApiManagement 서비스에서 새 API Schema를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="17193-103">Creates the new API Schema in the ApiManagement service</span></span>

## <span data-ttu-id="17193-104">구문</span><span class="sxs-lookup"><span data-stu-id="17193-104">SYNTAX</span></span>

### <span data-ttu-id="17193-105">SchemaDocumentInline(기본값)</span><span class="sxs-lookup"><span data-stu-id="17193-105">SchemaDocumentInline (Default)</span></span>
```
New-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 -SchemaDocumentContentType <String> -SchemaDocument <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17193-106">SchemaDocumentFromFile</span><span class="sxs-lookup"><span data-stu-id="17193-106">SchemaDocumentFromFile</span></span>
```
New-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 -SchemaDocumentContentType <String> -SchemaDocumentFilePath <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17193-107">설명</span><span class="sxs-lookup"><span data-stu-id="17193-107">DESCRIPTION</span></span>
<span data-ttu-id="17193-108">API의 새 API Schema를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="17193-108">Creates the new API Schema of the API.</span></span>

## <span data-ttu-id="17193-109">예제</span><span class="sxs-lookup"><span data-stu-id="17193-109">EXAMPLES</span></span>

### <span data-ttu-id="17193-110">예제 1: Swagger Petstore 광범위한 API에 대한 새 Schema 만들기</span><span class="sxs-lookup"><span data-stu-id="17193-110">Example 1: Create new Schema for Swagger Petstore Extensive API</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/resourceGroupName/providers/Microsoft.ApiManagement/service/sdktestapim4163
PS D:\github\azure-powershell> New-AzApiManagementApiSchema -Context $context -ApiId swagger-petstore-extensive -SchemaDocumentContentType swaggerdefinition -SchemaDocumentFilePath C:\Users\sasolank\Downloads\petstoreschema.json
Schema Id                            Api Id                     Schema ContentType
---------                            ------                     ------------------
3e8892eb-98e4-408d-b77a-f424185c1044 swagger-petstore-extensive swaggerdefinition
```

<span data-ttu-id="17193-111">**New-AzApiManagementApiSchema** cmdlet은 aPI의 스마마를 생성하거나 `swagger-petstore-extensive` 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="17193-111">The cmdlet **New-AzApiManagementApiSchema** creates or updates the schema of the `swagger-petstore-extensive` aPI.</span></span>

## <span data-ttu-id="17193-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17193-112">PARAMETERS</span></span>

### <span data-ttu-id="17193-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="17193-113">-ApiId</span></span>
<span data-ttu-id="17193-114">API의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="17193-114">Identifier of api.</span></span> <span data-ttu-id="17193-115">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="17193-115">This parameter is required.</span></span>

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

### <span data-ttu-id="17193-116">-Context</span><span class="sxs-lookup"><span data-stu-id="17193-116">-Context</span></span>
<span data-ttu-id="17193-117">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="17193-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="17193-118">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="17193-118">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17193-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17193-119">-DefaultProfile</span></span>
<span data-ttu-id="17193-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="17193-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17193-121">-SchemaDocument</span><span class="sxs-lookup"><span data-stu-id="17193-121">-SchemaDocument</span></span>
<span data-ttu-id="17193-122">API 스마마 문서를 문자열로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="17193-122">Api schema document as a string.</span></span> <span data-ttu-id="17193-123">이 매개 변수는 -SchemaDocumentFile이 지정되지 않은 것입니다.</span><span class="sxs-lookup"><span data-stu-id="17193-123">This parameter is required is -SchemaDocumentFile is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: SchemaDocumentInline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17193-124">-SchemaDocumentContentType</span><span class="sxs-lookup"><span data-stu-id="17193-124">-SchemaDocumentContentType</span></span>
<span data-ttu-id="17193-125">api Schema의 ContentType입니다.</span><span class="sxs-lookup"><span data-stu-id="17193-125">ContentType of the api Schema.</span></span> <span data-ttu-id="17193-126">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="17193-126">This parameter is required.</span></span>

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

### <span data-ttu-id="17193-127">-SchemaDocumentFilePath</span><span class="sxs-lookup"><span data-stu-id="17193-127">-SchemaDocumentFilePath</span></span>
<span data-ttu-id="17193-128">Api schema 문서 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="17193-128">Api schema document file path.</span></span> <span data-ttu-id="17193-129">이 매개 변수는 -SchemaDocument가 지정되지 않은 것입니다.</span><span class="sxs-lookup"><span data-stu-id="17193-129">This parameter is required is -SchemaDocument is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: SchemaDocumentFromFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17193-130">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="17193-130">-SchemaId</span></span>
<span data-ttu-id="17193-131">새 schema의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="17193-131">Identifier of new schema.</span></span>
<span data-ttu-id="17193-132">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="17193-132">This parameter is optional.</span></span>
<span data-ttu-id="17193-133">지정하지 않으면 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="17193-133">If not specified will be generated.</span></span>

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

### <span data-ttu-id="17193-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="17193-134">-Confirm</span></span>
<span data-ttu-id="17193-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="17193-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17193-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17193-136">-WhatIf</span></span>
<span data-ttu-id="17193-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="17193-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17193-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="17193-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17193-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17193-139">CommonParameters</span></span>
<span data-ttu-id="17193-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="17193-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17193-141">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="17193-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17193-142">입력</span><span class="sxs-lookup"><span data-stu-id="17193-142">INPUTS</span></span>

### <span data-ttu-id="17193-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="17193-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="17193-144">System.String</span><span class="sxs-lookup"><span data-stu-id="17193-144">System.String</span></span>

## <span data-ttu-id="17193-145">출력</span><span class="sxs-lookup"><span data-stu-id="17193-145">OUTPUTS</span></span>

### <span data-ttu-id="17193-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="17193-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

## <span data-ttu-id="17193-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="17193-147">NOTES</span></span>

## <span data-ttu-id="17193-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="17193-148">RELATED LINKS</span></span>

[<span data-ttu-id="17193-149">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="17193-149">Get-AzApiManagementApiSchema</span></span>](./Get-AzApiManagementApiSchema.md)

[<span data-ttu-id="17193-150">Remove-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="17193-150">Remove-AzApiManagementApiSchema</span></span>](./Remove-AzApiManagementApiSchema.md)

[<span data-ttu-id="17193-151">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="17193-151">Set-AzApiManagementApiSchema</span></span>](./Set-AzApiManagementApiSchema.md)