---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B64E9C13-97A6-4E8B-92DB-EFAF8A48C5B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProduct.md
ms.openlocfilehash: 10b17f60ae100004c23a16f341924de6de11b0eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524748"
---
# <span data-ttu-id="981f4-101">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="981f4-101">Get-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="981f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="981f4-102">SYNOPSIS</span></span>
<span data-ttu-id="981f4-103">목록 또는 특정 제품을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="981f4-103">Gets a list or a particular product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="981f4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="981f4-104">SYNTAX</span></span>

### <span data-ttu-id="981f4-105">GetAllProducts (기본값)</span><span class="sxs-lookup"><span data-stu-id="981f4-105">GetAllProducts (Default)</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="981f4-106">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="981f4-106">GetByProductId</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="981f4-107">GetByTitle</span><span class="sxs-lookup"><span data-stu-id="981f4-107">GetByTitle</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-Title <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="981f4-108">설명은</span><span class="sxs-lookup"><span data-stu-id="981f4-108">DESCRIPTION</span></span>
<span data-ttu-id="981f4-109">**Get-AzureRmApiManagementProduct** cmdlet은 목록 또는 특정 제품을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="981f4-109">The **Get-AzureRmApiManagementProduct** cmdlet gets a list or a particular product.</span></span>

## <span data-ttu-id="981f4-110">예제의</span><span class="sxs-lookup"><span data-stu-id="981f4-110">EXAMPLES</span></span>

### <span data-ttu-id="981f4-111">예제 1: 모든 제품 가져오기</span><span class="sxs-lookup"><span data-stu-id="981f4-111">Example 1: Get all products</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementProduct -Context $apimContext
```

<span data-ttu-id="981f4-112">이 명령은 모든 API Management 제품을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="981f4-112">This command get all API Management products.</span></span>

### <span data-ttu-id="981f4-113">예제 2: ID를 기준으로 제품 가져오기</span><span class="sxs-lookup"><span data-stu-id="981f4-113">Example 2: Get a product by ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementProduct -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="981f4-114">이 명령은 ID를 기준으로 API 관리 제품을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="981f4-114">This command get an API Management product by ID.</span></span>

## <span data-ttu-id="981f4-115">변수</span><span class="sxs-lookup"><span data-stu-id="981f4-115">PARAMETERS</span></span>

### <span data-ttu-id="981f4-116">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="981f4-116">-Context</span></span>
<span data-ttu-id="981f4-117">**PsApiManagementContext** 개체의 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="981f4-117">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="981f4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="981f4-118">-DefaultProfile</span></span>
<span data-ttu-id="981f4-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="981f4-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="981f4-120">-ProductId</span><span class="sxs-lookup"><span data-stu-id="981f4-120">-ProductId</span></span>
<span data-ttu-id="981f4-121">검색할 제품의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="981f4-121">Specifies the identifier of the product to search for.</span></span>

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

### <span data-ttu-id="981f4-122">-Title</span><span class="sxs-lookup"><span data-stu-id="981f4-122">-Title</span></span>
<span data-ttu-id="981f4-123">찾을 제품의 제목을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="981f4-123">Specifies the title of the product to look for.</span></span>
<span data-ttu-id="981f4-124">지정 된 경우 cmdlet은 제품을 제목별로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="981f4-124">If specified, the cmdlet attempts to get the product by title.</span></span>

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

### <span data-ttu-id="981f4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="981f4-125">CommonParameters</span></span>
<span data-ttu-id="981f4-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="981f4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="981f4-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="981f4-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="981f4-128">입력</span><span class="sxs-lookup"><span data-stu-id="981f4-128">INPUTS</span></span>

### <span data-ttu-id="981f4-129">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="981f4-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="981f4-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="981f4-130">System.String</span></span>

## <span data-ttu-id="981f4-131">출력</span><span class="sxs-lookup"><span data-stu-id="981f4-131">OUTPUTS</span></span>

### <span data-ttu-id="981f4-132">ApiManagement. ServiceManagement. \ PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="981f4-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="981f4-133">상속자</span><span class="sxs-lookup"><span data-stu-id="981f4-133">NOTES</span></span>

## <span data-ttu-id="981f4-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="981f4-134">RELATED LINKS</span></span>

[<span data-ttu-id="981f4-135">새로운 AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="981f4-135">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="981f4-136">제거-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="981f4-136">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)

[<span data-ttu-id="981f4-137">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="981f4-137">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


