---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B64E9C13-97A6-4E8B-92DB-EFAF8A48C5B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProduct.md
ms.openlocfilehash: 8e59cbb9885587ee57103b78400ce8ece9aafd46
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310403"
---
# <span data-ttu-id="1f350-101">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="1f350-101">Get-AzApiManagementProduct</span></span>

## <span data-ttu-id="1f350-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f350-102">SYNOPSIS</span></span>
<span data-ttu-id="1f350-103">목록 또는 특정 제품을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1f350-103">Gets a list or a particular product.</span></span>

## <span data-ttu-id="1f350-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1f350-104">SYNTAX</span></span>

### <span data-ttu-id="1f350-105">GetAllProducts (기본값)</span><span class="sxs-lookup"><span data-stu-id="1f350-105">GetAllProducts (Default)</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1f350-106">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="1f350-106">GetByProductId</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f350-107">GetByTitle</span><span class="sxs-lookup"><span data-stu-id="1f350-107">GetByTitle</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> [-Title <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1f350-108">GetByApiId</span><span class="sxs-lookup"><span data-stu-id="1f350-108">GetByApiId</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> -ApiId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f350-109">설명은</span><span class="sxs-lookup"><span data-stu-id="1f350-109">DESCRIPTION</span></span>
<span data-ttu-id="1f350-110">**Get-AzApiManagementProduct** cmdlet은 목록 또는 특정 제품을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1f350-110">The **Get-AzApiManagementProduct** cmdlet gets a list or a particular product.</span></span>

## <span data-ttu-id="1f350-111">예제의</span><span class="sxs-lookup"><span data-stu-id="1f350-111">EXAMPLES</span></span>

### <span data-ttu-id="1f350-112">예제 1: 모든 제품 가져오기</span><span class="sxs-lookup"><span data-stu-id="1f350-112">Example 1: Get all products</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProduct -Context $apimContext
```

<span data-ttu-id="1f350-113">이 명령은 모든 API Management 제품을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1f350-113">This command get all API Management products.</span></span>

### <span data-ttu-id="1f350-114">예제 2: ID를 기준으로 제품 가져오기</span><span class="sxs-lookup"><span data-stu-id="1f350-114">Example 2: Get a product by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProduct -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="1f350-115">이 명령은 ID를 기준으로 API 관리 제품을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1f350-115">This command get an API Management product by ID.</span></span>

## <span data-ttu-id="1f350-116">변수</span><span class="sxs-lookup"><span data-stu-id="1f350-116">PARAMETERS</span></span>

### <span data-ttu-id="1f350-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="1f350-117">-ApiId</span></span>
<span data-ttu-id="1f350-118">상호 관련 된 제품을 찾는 Api의 ApiId입니다.</span><span class="sxs-lookup"><span data-stu-id="1f350-118">ApiId of the Api to find the correlated products.</span></span> <span data-ttu-id="1f350-119">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="1f350-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="1f350-120">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="1f350-120">-Context</span></span>
<span data-ttu-id="1f350-121">**PsApiManagementContext** 개체의 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f350-121">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="1f350-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f350-122">-DefaultProfile</span></span>
<span data-ttu-id="1f350-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1f350-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f350-124">-ProductId</span><span class="sxs-lookup"><span data-stu-id="1f350-124">-ProductId</span></span>
<span data-ttu-id="1f350-125">검색할 제품의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f350-125">Specifies the identifier of the product to search for.</span></span>

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

### <span data-ttu-id="1f350-126">-Title</span><span class="sxs-lookup"><span data-stu-id="1f350-126">-Title</span></span>
<span data-ttu-id="1f350-127">찾을 제품의 제목을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f350-127">Specifies the title of the product to look for.</span></span>
<span data-ttu-id="1f350-128">지정 된 경우 cmdlet은 제품을 제목별로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1f350-128">If specified, the cmdlet attempts to get the product by title.</span></span>

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

### <span data-ttu-id="1f350-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f350-129">CommonParameters</span></span>
<span data-ttu-id="1f350-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f350-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f350-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1f350-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f350-132">입력</span><span class="sxs-lookup"><span data-stu-id="1f350-132">INPUTS</span></span>

### <span data-ttu-id="1f350-133">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1f350-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1f350-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1f350-134">System.String</span></span>

## <span data-ttu-id="1f350-135">출력</span><span class="sxs-lookup"><span data-stu-id="1f350-135">OUTPUTS</span></span>

### <span data-ttu-id="1f350-136">ApiManagement. ServiceManagement. \ PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="1f350-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="1f350-137">상속자</span><span class="sxs-lookup"><span data-stu-id="1f350-137">NOTES</span></span>

## <span data-ttu-id="1f350-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1f350-138">RELATED LINKS</span></span>

[<span data-ttu-id="1f350-139">새로운 AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="1f350-139">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="1f350-140">제거-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="1f350-140">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)

[<span data-ttu-id="1f350-141">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="1f350-141">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


