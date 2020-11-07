---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 223FBBA6-4405-4B7A-BA63-5F2434A2A50D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProduct.md
ms.openlocfilehash: b050b55c978313cf038e8a27d5be0f7ad722905b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711451"
---
# <span data-ttu-id="187db-101">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="187db-101">Set-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="187db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="187db-102">SYNOPSIS</span></span>
<span data-ttu-id="187db-103">API Management 제품 세부 정보를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="187db-103">Sets the API Management product details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="187db-104">구문과</span><span class="sxs-lookup"><span data-stu-id="187db-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-Title <String>]
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="187db-105">설명은</span><span class="sxs-lookup"><span data-stu-id="187db-105">DESCRIPTION</span></span>
<span data-ttu-id="187db-106">**AzureRmApiManagementProduct** CMDLET은 API 관리 제품 세부 정보를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="187db-106">The **Set-AzureRmApiManagementProduct** cmdlet sets the API Management product details.</span></span>

## <span data-ttu-id="187db-107">예제의</span><span class="sxs-lookup"><span data-stu-id="187db-107">EXAMPLES</span></span>

### <span data-ttu-id="187db-108">예제 1: 제품 세부 정보 업데이트</span><span class="sxs-lookup"><span data-stu-id="187db-108">Example 1: Update the product details</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $True -State "NotPublished"
```

<span data-ttu-id="187db-109">이 명령은 API Management 제품 세부 정보를 업데이트 하 고, 구독을 요청 하 고, 게시를 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="187db-109">This command updates the API Management product details, requires a subscription, and then unpublishes.</span></span>

## <span data-ttu-id="187db-110">변수</span><span class="sxs-lookup"><span data-stu-id="187db-110">PARAMETERS</span></span>

### <span data-ttu-id="187db-111">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="187db-111">-ApprovalRequired</span></span>
<span data-ttu-id="187db-112">제품 구독에 승인이 필요한 지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="187db-112">Indicates whether the subscription to the product requires approval.</span></span>
<span data-ttu-id="187db-113">기본값은 **$False** 입니다.</span><span class="sxs-lookup"><span data-stu-id="187db-113">The default value is **$False**.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="187db-114">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="187db-114">-Context</span></span>
<span data-ttu-id="187db-115">**PsApiManagementContext** 개체의 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="187db-115">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="187db-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="187db-116">-DefaultProfile</span></span>
<span data-ttu-id="187db-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="187db-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="187db-118">-설명</span><span class="sxs-lookup"><span data-stu-id="187db-118">-Description</span></span>
<span data-ttu-id="187db-119">제품 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="187db-119">Specifies the product description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="187db-120">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="187db-120">-LegalTerms</span></span>
<span data-ttu-id="187db-121">제품의 약관 사용 약관을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="187db-121">Specifies the legal terms of use of the product.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="187db-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="187db-122">-PassThru</span></span>
<span data-ttu-id="187db-123">passthru</span><span class="sxs-lookup"><span data-stu-id="187db-123">passthru</span></span>

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

### <span data-ttu-id="187db-124">-ProductId</span><span class="sxs-lookup"><span data-stu-id="187db-124">-ProductId</span></span>
<span data-ttu-id="187db-125">기존 제품의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="187db-125">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="187db-126">-상태</span><span class="sxs-lookup"><span data-stu-id="187db-126">-State</span></span>
<span data-ttu-id="187db-127">제품 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="187db-127">Specifies the product state.</span></span>
<span data-ttu-id="187db-128">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="187db-128">psdx_paramvalues</span></span>

- <span data-ttu-id="187db-129">NotPublished 됨</span><span class="sxs-lookup"><span data-stu-id="187db-129">NotPublished</span></span>
- <span data-ttu-id="187db-130">게시자</span><span class="sxs-lookup"><span data-stu-id="187db-130">Published</span></span>

```yaml
Type: PsApiManagementProductState
Parameter Sets: (All)
Aliases: 
Accepted values: NotPublished, Published

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="187db-131">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="187db-131">-SubscriptionRequired</span></span>
<span data-ttu-id="187db-132">제품에 구독이 필요한 지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="187db-132">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="187db-133">이 매개 변수의 기본값은 **$True** 입니다.</span><span class="sxs-lookup"><span data-stu-id="187db-133">The default value for this parameter is **$True**.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="187db-134">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="187db-134">-SubscriptionsLimit</span></span>
<span data-ttu-id="187db-135">최대 동시 구독 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="187db-135">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="187db-136">이 매개 변수의 기본값은 1입니다.</span><span class="sxs-lookup"><span data-stu-id="187db-136">The default value for this parameter is 1.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="187db-137">-Title</span><span class="sxs-lookup"><span data-stu-id="187db-137">-Title</span></span>
<span data-ttu-id="187db-138">이 cmdlet이 설정 하는 제품 타이틀을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="187db-138">Specifies the product title this cmdlet sets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="187db-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="187db-139">CommonParameters</span></span>
<span data-ttu-id="187db-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="187db-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="187db-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="187db-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="187db-142">입력</span><span class="sxs-lookup"><span data-stu-id="187db-142">INPUTS</span></span>

### <span data-ttu-id="187db-143">않아야</span><span class="sxs-lookup"><span data-stu-id="187db-143">None</span></span>
<span data-ttu-id="187db-144">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="187db-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="187db-145">출력</span><span class="sxs-lookup"><span data-stu-id="187db-145">OUTPUTS</span></span>

### <span data-ttu-id="187db-146">ApiManagement. ServiceManagement. \ PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="187db-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="187db-147">상속자</span><span class="sxs-lookup"><span data-stu-id="187db-147">NOTES</span></span>

## <span data-ttu-id="187db-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="187db-148">RELATED LINKS</span></span>

[<span data-ttu-id="187db-149">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="187db-149">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="187db-150">새로운 AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="187db-150">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="187db-151">제거-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="187db-151">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)


