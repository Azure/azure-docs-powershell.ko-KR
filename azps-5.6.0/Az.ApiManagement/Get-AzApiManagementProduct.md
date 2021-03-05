---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B64E9C13-97A6-4E8B-92DB-EFAF8A48C5B8
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProduct.md
ms.openlocfilehash: 589338afde60e069646cb677205da11e322ba7da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012864"
---
# <span data-ttu-id="4aed3-101">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="4aed3-101">Get-AzApiManagementProduct</span></span>

## <span data-ttu-id="4aed3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4aed3-102">SYNOPSIS</span></span>
<span data-ttu-id="4aed3-103">목록 또는 특정 제품을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4aed3-103">Gets a list or a particular product.</span></span>

## <span data-ttu-id="4aed3-104">구문</span><span class="sxs-lookup"><span data-stu-id="4aed3-104">SYNTAX</span></span>

### <span data-ttu-id="4aed3-105">GetAllProducts(기본값)</span><span class="sxs-lookup"><span data-stu-id="4aed3-105">GetAllProducts (Default)</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4aed3-106">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="4aed3-106">GetByProductId</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4aed3-107">GetByTitle</span><span class="sxs-lookup"><span data-stu-id="4aed3-107">GetByTitle</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> [-Title <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4aed3-108">GetByApiId</span><span class="sxs-lookup"><span data-stu-id="4aed3-108">GetByApiId</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> -ApiId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4aed3-109">설명</span><span class="sxs-lookup"><span data-stu-id="4aed3-109">DESCRIPTION</span></span>
<span data-ttu-id="4aed3-110">**Get-AzApiManagementProduct** cmdlet은 목록 또는 특정 제품을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4aed3-110">The **Get-AzApiManagementProduct** cmdlet gets a list or a particular product.</span></span>

## <span data-ttu-id="4aed3-111">예제</span><span class="sxs-lookup"><span data-stu-id="4aed3-111">EXAMPLES</span></span>

### <span data-ttu-id="4aed3-112">예제 1: 모든 제품 사용</span><span class="sxs-lookup"><span data-stu-id="4aed3-112">Example 1: Get all products</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProduct -Context $apimContext
```

<span data-ttu-id="4aed3-113">이 명령은 모든 API Management 제품을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4aed3-113">This command get all API Management products.</span></span>

### <span data-ttu-id="4aed3-114">예제 2: ID로 제품 얻기</span><span class="sxs-lookup"><span data-stu-id="4aed3-114">Example 2: Get a product by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProduct -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="4aed3-115">이 명령은 ID로 API Management 제품을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4aed3-115">This command get an API Management product by ID.</span></span>

## <span data-ttu-id="4aed3-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="4aed3-116">PARAMETERS</span></span>

### <span data-ttu-id="4aed3-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="4aed3-117">-ApiId</span></span>
<span data-ttu-id="4aed3-118">ApiId의 상관 관계 제품을 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4aed3-118">ApiId of the Api to find the correlated products.</span></span> <span data-ttu-id="4aed3-119">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="4aed3-119">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4aed3-120">-Context</span><span class="sxs-lookup"><span data-stu-id="4aed3-120">-Context</span></span>
<span data-ttu-id="4aed3-121">**PsApiManagementContext** 개체의 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4aed3-121">Specifies an instance of a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4aed3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4aed3-122">-DefaultProfile</span></span>
<span data-ttu-id="4aed3-123">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4aed3-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4aed3-124">-ProductId</span><span class="sxs-lookup"><span data-stu-id="4aed3-124">-ProductId</span></span>
<span data-ttu-id="4aed3-125">검색할 제품의 식별자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4aed3-125">Specifies the identifier of the product to search for.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByProductId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4aed3-126">-Title</span><span class="sxs-lookup"><span data-stu-id="4aed3-126">-Title</span></span>
<span data-ttu-id="4aed3-127">찾아야 할 제품의 제목을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4aed3-127">Specifies the title of the product to look for.</span></span>
<span data-ttu-id="4aed3-128">지정된 경우 cmdlet은 타이틀을 통해 제품을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4aed3-128">If specified, the cmdlet attempts to get the product by title.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByTitle
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4aed3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4aed3-129">CommonParameters</span></span>
<span data-ttu-id="4aed3-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4aed3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4aed3-131">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4aed3-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4aed3-132">입력</span><span class="sxs-lookup"><span data-stu-id="4aed3-132">INPUTS</span></span>

### <span data-ttu-id="4aed3-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4aed3-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4aed3-134">System.String</span><span class="sxs-lookup"><span data-stu-id="4aed3-134">System.String</span></span>

## <span data-ttu-id="4aed3-135">출력</span><span class="sxs-lookup"><span data-stu-id="4aed3-135">OUTPUTS</span></span>

### <span data-ttu-id="4aed3-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.psApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="4aed3-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="4aed3-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4aed3-137">NOTES</span></span>

## <span data-ttu-id="4aed3-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4aed3-138">RELATED LINKS</span></span>

[<span data-ttu-id="4aed3-139">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="4aed3-139">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="4aed3-140">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="4aed3-140">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)

[<span data-ttu-id="4aed3-141">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="4aed3-141">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


