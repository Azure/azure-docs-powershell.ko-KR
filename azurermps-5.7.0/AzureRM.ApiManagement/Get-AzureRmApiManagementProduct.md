---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B64E9C13-97A6-4E8B-92DB-EFAF8A48C5B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProduct.md
ms.openlocfilehash: a4bbc330b5cd4d7eaeec1d2e68252ceb5dd261f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529966"
---
# <span data-ttu-id="8cea2-101">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="8cea2-101">Get-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="8cea2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8cea2-102">SYNOPSIS</span></span>
<span data-ttu-id="8cea2-103">목록 또는 특정 제품을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8cea2-103">Gets a list or a particular product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8cea2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8cea2-104">SYNTAX</span></span>

### <span data-ttu-id="8cea2-105">GetAllProducts (기본값)</span><span class="sxs-lookup"><span data-stu-id="8cea2-105">GetAllProducts (Default)</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8cea2-106">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="8cea2-106">GetByProductId</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8cea2-107">GetByTitle</span><span class="sxs-lookup"><span data-stu-id="8cea2-107">GetByTitle</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-Title <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8cea2-108">설명은</span><span class="sxs-lookup"><span data-stu-id="8cea2-108">DESCRIPTION</span></span>
<span data-ttu-id="8cea2-109">**Get-AzureRmApiManagementProduct** cmdlet은 목록 또는 특정 제품을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8cea2-109">The **Get-AzureRmApiManagementProduct** cmdlet gets a list or a particular product.</span></span>

## <span data-ttu-id="8cea2-110">예제의</span><span class="sxs-lookup"><span data-stu-id="8cea2-110">EXAMPLES</span></span>

### <span data-ttu-id="8cea2-111">예제 1: 모든 제품 가져오기</span><span class="sxs-lookup"><span data-stu-id="8cea2-111">Example 1: Get all products</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementProduct -Context $apimContext
```

<span data-ttu-id="8cea2-112">이 명령은 모든 API Management 제품을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8cea2-112">This command get all API Management products.</span></span>

### <span data-ttu-id="8cea2-113">예제 2: ID를 기준으로 제품 가져오기</span><span class="sxs-lookup"><span data-stu-id="8cea2-113">Example 2: Get a product by ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementProduct -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="8cea2-114">이 명령은 ID를 기준으로 API 관리 제품을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8cea2-114">This command get an API Management product by ID.</span></span>

## <span data-ttu-id="8cea2-115">변수</span><span class="sxs-lookup"><span data-stu-id="8cea2-115">PARAMETERS</span></span>

### <span data-ttu-id="8cea2-116">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="8cea2-116">-Context</span></span>
<span data-ttu-id="8cea2-117">**PsApiManagementContext** 개체의 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cea2-117">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="8cea2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cea2-118">-DefaultProfile</span></span>
<span data-ttu-id="8cea2-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8cea2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="8cea2-120">-ProductId</span><span class="sxs-lookup"><span data-stu-id="8cea2-120">-ProductId</span></span>
<span data-ttu-id="8cea2-121">검색할 제품의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cea2-121">Specifies the identifier of the product to search for.</span></span>

```yaml
Type: String
Parameter Sets: GetByProductId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cea2-122">-Title</span><span class="sxs-lookup"><span data-stu-id="8cea2-122">-Title</span></span>
<span data-ttu-id="8cea2-123">찾을 제품의 제목을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cea2-123">Specifies the title of the product to look for.</span></span>
<span data-ttu-id="8cea2-124">지정 된 경우 cmdlet은 제품을 제목별로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8cea2-124">If specified, the cmdlet attempts to get the product by title.</span></span>

```yaml
Type: String
Parameter Sets: GetByTitle
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8cea2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cea2-125">CommonParameters</span></span>
<span data-ttu-id="8cea2-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cea2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cea2-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cea2-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cea2-128">입력</span><span class="sxs-lookup"><span data-stu-id="8cea2-128">INPUTS</span></span>

### <span data-ttu-id="8cea2-129">않아야</span><span class="sxs-lookup"><span data-stu-id="8cea2-129">None</span></span>
<span data-ttu-id="8cea2-130">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8cea2-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8cea2-131">출력</span><span class="sxs-lookup"><span data-stu-id="8cea2-131">OUTPUTS</span></span>

### <span data-ttu-id="8cea2-132">ApiManagement. ServiceManagement. \ PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="8cea2-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>
<span data-ttu-id="8cea2-133">API Management 서비스의 제품에 대 한 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="8cea2-133">The details of the Product in API Management service.</span></span>

### <span data-ttu-id="8cea2-134">IList를<ApiManagement> ServiceManagement. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="8cea2-134">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct></span></span>
<span data-ttu-id="8cea2-135">API Management 서비스의 제품 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="8cea2-135">The list of Product in API Management service.</span></span>

## <span data-ttu-id="8cea2-136">상속자</span><span class="sxs-lookup"><span data-stu-id="8cea2-136">NOTES</span></span>

## <span data-ttu-id="8cea2-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8cea2-137">RELATED LINKS</span></span>

[<span data-ttu-id="8cea2-138">새로운 AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="8cea2-138">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="8cea2-139">제거-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="8cea2-139">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)

[<span data-ttu-id="8cea2-140">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="8cea2-140">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


