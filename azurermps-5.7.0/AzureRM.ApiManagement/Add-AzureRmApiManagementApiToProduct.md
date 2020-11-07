---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 7C86B385-D784-45FD-9B57-31C895115A2C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/add-azurermapimanagementapitoproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementApiToProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementApiToProduct.md
ms.openlocfilehash: 08d6d8e5ecbcaa8b6810bd173062c5bb244ec5e8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703066"
---
# <span data-ttu-id="41be8-101">Add-AzureRmApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="41be8-101">Add-AzureRmApiManagementApiToProduct</span></span>

## <span data-ttu-id="41be8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41be8-102">SYNOPSIS</span></span>
<span data-ttu-id="41be8-103">제품에 API를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="41be8-103">Adds an API to a product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41be8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="41be8-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementApiToProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41be8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="41be8-105">DESCRIPTION</span></span>
<span data-ttu-id="41be8-106">**Add-AzureRmApiManagementApiToProduct** cmdlet은 제품에 Azure API Management api를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="41be8-106">The **Add-AzureRmApiManagementApiToProduct** cmdlet adds an Azure API Management API to a product.</span></span>

## <span data-ttu-id="41be8-107">예제의</span><span class="sxs-lookup"><span data-stu-id="41be8-107">EXAMPLES</span></span>

### <span data-ttu-id="41be8-108">예제 1: 제품에 API 추가</span><span class="sxs-lookup"><span data-stu-id="41be8-108">Example 1: Add an API to a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzureRmApiManagementApiToProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001"
```

<span data-ttu-id="41be8-109">이 명령은 지정 된 제품에 지정한 API를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="41be8-109">This command adds the specified API to the specified product.</span></span>

## <span data-ttu-id="41be8-110">변수</span><span class="sxs-lookup"><span data-stu-id="41be8-110">PARAMETERS</span></span>

### <span data-ttu-id="41be8-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="41be8-111">-ApiId</span></span>
<span data-ttu-id="41be8-112">제품에 추가할 API의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41be8-112">Specifies the ID of an API to add to a product.</span></span>

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

### <span data-ttu-id="41be8-113">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="41be8-113">-Context</span></span>
<span data-ttu-id="41be8-114">**PsApiManagementContext** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41be8-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="41be8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41be8-115">-DefaultProfile</span></span>
<span data-ttu-id="41be8-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="41be8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41be8-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="41be8-117">-PassThru</span></span>
<span data-ttu-id="41be8-118">passthru</span><span class="sxs-lookup"><span data-stu-id="41be8-118">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41be8-119">-ProductId</span><span class="sxs-lookup"><span data-stu-id="41be8-119">-ProductId</span></span>
<span data-ttu-id="41be8-120">API를 추가할 제품의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41be8-120">Specifies the ID of the product to which to add the API.</span></span>

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

### <span data-ttu-id="41be8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41be8-121">CommonParameters</span></span>
<span data-ttu-id="41be8-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="41be8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41be8-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41be8-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41be8-124">입력</span><span class="sxs-lookup"><span data-stu-id="41be8-124">INPUTS</span></span>

### <span data-ttu-id="41be8-125">않아야</span><span class="sxs-lookup"><span data-stu-id="41be8-125">None</span></span>
<span data-ttu-id="41be8-126">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="41be8-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="41be8-127">출력</span><span class="sxs-lookup"><span data-stu-id="41be8-127">OUTPUTS</span></span>

### <span data-ttu-id="41be8-128">나타내는</span><span class="sxs-lookup"><span data-stu-id="41be8-128">Boolean</span></span>

## <span data-ttu-id="41be8-129">상속자</span><span class="sxs-lookup"><span data-stu-id="41be8-129">NOTES</span></span>

## <span data-ttu-id="41be8-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="41be8-130">RELATED LINKS</span></span>

[<span data-ttu-id="41be8-131">제거-AzureRmApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="41be8-131">Remove-AzureRmApiManagementApiFromProduct</span></span>](./Remove-AzureRmApiManagementApiFromProduct.md)


