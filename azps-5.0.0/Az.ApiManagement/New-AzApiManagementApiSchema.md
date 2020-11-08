---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementapischema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementApiSchema.md
ms.openlocfilehash: 7714c9118364f0d2ecc6e8773983acb916702281
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217883"
---
# <span data-ttu-id="ec5ba-101">New-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="ec5ba-101">New-AzApiManagementApiSchema</span></span>

## <span data-ttu-id="ec5ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec5ba-102">SYNOPSIS</span></span>
<span data-ttu-id="ec5ba-103">ApiManagement 서비스에서 새 API 스키마를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ec5ba-103">Creates the new API Schema in the ApiManagement service</span></span>

## <span data-ttu-id="ec5ba-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ec5ba-104">SYNTAX</span></span>

### <span data-ttu-id="ec5ba-105">SchemaDocumentInline (기본값)</span><span class="sxs-lookup"><span data-stu-id="ec5ba-105">SchemaDocumentInline (Default)</span></span>
```
New-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 -SchemaDocumentContentType <String> -SchemaDocument <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec5ba-106">SchemaDocumentFromFile</span><span class="sxs-lookup"><span data-stu-id="ec5ba-106">SchemaDocumentFromFile</span></span>
```
New-AzApiManagementApiSchema -Context <PsApiManagementContext> -ApiId <String> [-SchemaId <String>]
 -SchemaDocumentContentType <String> -SchemaDocumentFilePath <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec5ba-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ec5ba-107">DESCRIPTION</span></span>
<span data-ttu-id="ec5ba-108">API의 새 API 스키마를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ec5ba-108">Creates the new API Schema of the API.</span></span>

## <span data-ttu-id="ec5ba-109">예제의</span><span class="sxs-lookup"><span data-stu-id="ec5ba-109">EXAMPLES</span></span>

### <span data-ttu-id="ec5ba-110">예제 1: Swagger Petstore 확장 API에 대 한 새 스키마 만들기</span><span class="sxs-lookup"><span data-stu-id="ec5ba-110">Example 1: Create new Schema for Swagger Petstore Extensive API</span></span>
```powershell
PS D:\github\azure-powershell> $context = New-AzApiManagementContext -ResourceId /subscriptions/subid/resourceGroups/resourceGroupName/providers/Microsoft.ApiManagement/service/sdktestapim4163
PS D:\github\azure-powershell> New-AzApiManagementApiSchema -Context $context -ApiId swagger-petstore-extensive -SchemaDocumentContentType swaggerdefinition -SchemaDocumentFilePath C:\Users\sasolank\Downloads\petstoreschema.json
Schema Id                            Api Id                     Schema ContentType
---------                            ------                     ------------------
3e8892eb-98e4-408d-b77a-f424185c1044 swagger-petstore-extensive swaggerdefinition
```

<span data-ttu-id="ec5ba-111">Cmdlet **AzApiManagementApiSchema** 는 aPI의 스키마를 만들거나 업데이트 합니다 `swagger-petstore-extensive` .</span><span class="sxs-lookup"><span data-stu-id="ec5ba-111">The cmdlet **New-AzApiManagementApiSchema** creates or updates the schema of the `swagger-petstore-extensive` aPI.</span></span>

## <span data-ttu-id="ec5ba-112">변수</span><span class="sxs-lookup"><span data-stu-id="ec5ba-112">PARAMETERS</span></span>

### <span data-ttu-id="ec5ba-113">-ApiId</span><span class="sxs-lookup"><span data-stu-id="ec5ba-113">-ApiId</span></span>
<span data-ttu-id="ec5ba-114">Api의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="ec5ba-114">Identifier of api.</span></span> <span data-ttu-id="ec5ba-115">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="ec5ba-115">This parameter is required.</span></span>

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

### <span data-ttu-id="ec5ba-116">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="ec5ba-116">-Context</span></span>
<span data-ttu-id="ec5ba-117">PsApiManagementContext의 인스턴스입니다.</span><span class="sxs-lookup"><span data-stu-id="ec5ba-117">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="ec5ba-118">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="ec5ba-118">This parameter is required.</span></span>

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

### <span data-ttu-id="ec5ba-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec5ba-119">-DefaultProfile</span></span>
<span data-ttu-id="ec5ba-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ec5ba-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec5ba-121">-SchemaDocument</span><span class="sxs-lookup"><span data-stu-id="ec5ba-121">-SchemaDocument</span></span>
<span data-ttu-id="ec5ba-122">Api 스키마 문서를 문자열로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ec5ba-122">Api schema document as a string.</span></span> <span data-ttu-id="ec5ba-123">이 매개 변수는 필수입니다-SchemaDocumentFile가 지정 되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="ec5ba-123">This parameter is required is -SchemaDocumentFile is not specified.</span></span>

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

### <span data-ttu-id="ec5ba-124">-SchemaDocumentContentType</span><span class="sxs-lookup"><span data-stu-id="ec5ba-124">-SchemaDocumentContentType</span></span>
<span data-ttu-id="ec5ba-125">Api 스키마의 ContentType</span><span class="sxs-lookup"><span data-stu-id="ec5ba-125">ContentType of the api Schema.</span></span> <span data-ttu-id="ec5ba-126">이 매개 변수는 필수입니다.</span><span class="sxs-lookup"><span data-stu-id="ec5ba-126">This parameter is required.</span></span>

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

### <span data-ttu-id="ec5ba-127">-SchemaDocumentFilePath</span><span class="sxs-lookup"><span data-stu-id="ec5ba-127">-SchemaDocumentFilePath</span></span>
<span data-ttu-id="ec5ba-128">Api 스키마 문서 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="ec5ba-128">Api schema document file path.</span></span> <span data-ttu-id="ec5ba-129">이 매개 변수는 필수입니다-SchemaDocument가 지정 되지 않았습니다.</span><span class="sxs-lookup"><span data-stu-id="ec5ba-129">This parameter is required is -SchemaDocument is not specified.</span></span>

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

### <span data-ttu-id="ec5ba-130">-SchemaId</span><span class="sxs-lookup"><span data-stu-id="ec5ba-130">-SchemaId</span></span>
<span data-ttu-id="ec5ba-131">새 스키마의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="ec5ba-131">Identifier of new schema.</span></span>
<span data-ttu-id="ec5ba-132">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="ec5ba-132">This parameter is optional.</span></span>
<span data-ttu-id="ec5ba-133">지정 하지 않으면가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec5ba-133">If not specified will be generated.</span></span>

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

### <span data-ttu-id="ec5ba-134">-확인</span><span class="sxs-lookup"><span data-stu-id="ec5ba-134">-Confirm</span></span>
<span data-ttu-id="ec5ba-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec5ba-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec5ba-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec5ba-136">-WhatIf</span></span>
<span data-ttu-id="ec5ba-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ec5ba-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec5ba-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ec5ba-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec5ba-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec5ba-139">CommonParameters</span></span>
<span data-ttu-id="ec5ba-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec5ba-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec5ba-141">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ec5ba-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec5ba-142">입력</span><span class="sxs-lookup"><span data-stu-id="ec5ba-142">INPUTS</span></span>

### <span data-ttu-id="ec5ba-143">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ec5ba-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ec5ba-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ec5ba-144">System.String</span></span>

## <span data-ttu-id="ec5ba-145">출력</span><span class="sxs-lookup"><span data-stu-id="ec5ba-145">OUTPUTS</span></span>

### <span data-ttu-id="ec5ba-146">ApiManagement. ServiceManagement. \ PsApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="ec5ba-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementApiSchema</span></span>

## <span data-ttu-id="ec5ba-147">상속자</span><span class="sxs-lookup"><span data-stu-id="ec5ba-147">NOTES</span></span>

## <span data-ttu-id="ec5ba-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ec5ba-148">RELATED LINKS</span></span>

[<span data-ttu-id="ec5ba-149">Get-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="ec5ba-149">Get-AzApiManagementApiSchema</span></span>](./Get-AzApiManagementApiSchema.md)

[<span data-ttu-id="ec5ba-150">제거-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="ec5ba-150">Remove-AzApiManagementApiSchema</span></span>](./Remove-AzApiManagementApiSchema.md)

[<span data-ttu-id="ec5ba-151">Set-AzApiManagementApiSchema</span><span class="sxs-lookup"><span data-stu-id="ec5ba-151">Set-AzApiManagementApiSchema</span></span>](./Set-AzApiManagementApiSchema.md)
