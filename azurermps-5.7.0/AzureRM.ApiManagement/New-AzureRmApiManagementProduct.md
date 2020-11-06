---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: E94B88AA-B8B0-49F0-AD36-6707E17B40AD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProduct.md
ms.openlocfilehash: 673aa943263a789e7d8be0a63634ddd176e09cae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525404"
---
# <span data-ttu-id="e493b-101">New-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="e493b-101">New-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="e493b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e493b-102">SYNOPSIS</span></span>
<span data-ttu-id="e493b-103">API Management 제품을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e493b-103">Creates an API Management product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e493b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e493b-104">SYNTAX</span></span>

```
New-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-ProductId <String>] -Title <String>
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e493b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e493b-105">DESCRIPTION</span></span>
<span data-ttu-id="e493b-106">**AzureRmApiManagementProduct** CMDLET은 API 관리 제품을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e493b-106">The **New-AzureRmApiManagementProduct** cmdlet creates an API Management product.</span></span>

## <span data-ttu-id="e493b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e493b-107">EXAMPLES</span></span>

### <span data-ttu-id="e493b-108">예제 1: 구독이 필요 하지 않은 제품 만들기</span><span class="sxs-lookup"><span data-stu-id="e493b-108">Example 1: Create a product that does not require a subscription</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $False -State "Published"
```

<span data-ttu-id="e493b-109">이 명령은 API 관리 제품을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e493b-109">This command creates an API Management product.</span></span>
<span data-ttu-id="e493b-110">구독이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e493b-110">No subscription is required.</span></span>

### <span data-ttu-id="e493b-111">예제 2: 구독 및 승인이 필요한 제품 만들기</span><span class="sxs-lookup"><span data-stu-id="e493b-111">Example 2: Create a product that requires a subscription and approval</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementProduct -Context $apimContext -ProductId "9876543210" -Title "Unlimited" -Description "Subscribers have completely unlimited access to the API. Administrator approval is required." -LegalTerms "Free for all" -ApprovalRequired $True -State "Published" -NotificationPeriod "D10" -SubscriptionPeriod "Y1"
```

<span data-ttu-id="e493b-112">이 명령은 제품을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e493b-112">This command creates a product.</span></span>
<span data-ttu-id="e493b-113">구독 및 승인이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="e493b-113">A subscription and approval are required.</span></span>
<span data-ttu-id="e493b-114">이 명령은 알림 기간을 10 일로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e493b-114">This command sets the notification period to 10 days.</span></span>
<span data-ttu-id="e493b-115">구독 기간이 1 년으로 설정 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e493b-115">The subscription duration is set to one year.</span></span>

## <span data-ttu-id="e493b-116">변수</span><span class="sxs-lookup"><span data-stu-id="e493b-116">PARAMETERS</span></span>

### <span data-ttu-id="e493b-117">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="e493b-117">-ApprovalRequired</span></span>
<span data-ttu-id="e493b-118">제품에 대 한 구독에 승인이 필요한 지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e493b-118">Indicates whether the subscription to the product requires approval or not.</span></span>
<span data-ttu-id="e493b-119">기본적으로이 매개 변수는 **$False** 입니다.</span><span class="sxs-lookup"><span data-stu-id="e493b-119">By default, this parameter is **$False**.</span></span>

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

### <span data-ttu-id="e493b-120">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="e493b-120">-Context</span></span>
<span data-ttu-id="e493b-121">**PsApiManagementContext** 개체의 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e493b-121">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="e493b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e493b-122">-DefaultProfile</span></span>
<span data-ttu-id="e493b-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e493b-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="e493b-124">-설명</span><span class="sxs-lookup"><span data-stu-id="e493b-124">-Description</span></span>
<span data-ttu-id="e493b-125">제품 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e493b-125">Specifies the product description.</span></span>

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

### <span data-ttu-id="e493b-126">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="e493b-126">-LegalTerms</span></span>
<span data-ttu-id="e493b-127">제품의 약관 사용 약관을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e493b-127">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="e493b-128">-ProductId</span><span class="sxs-lookup"><span data-stu-id="e493b-128">-ProductId</span></span>
<span data-ttu-id="e493b-129">새 제품의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e493b-129">Specifies the identifier of new product.</span></span>
<span data-ttu-id="e493b-130">이 매개 변수를 지정 하지 않으면 새 제품이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e493b-130">If you do not specify this parameter, a new product is generated.</span></span>

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

### <span data-ttu-id="e493b-131">-상태</span><span class="sxs-lookup"><span data-stu-id="e493b-131">-State</span></span>
<span data-ttu-id="e493b-132">제품 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e493b-132">Specifies the product state.</span></span>
<span data-ttu-id="e493b-133">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="e493b-133">psdx_paramvalues</span></span>

- <span data-ttu-id="e493b-134">NotPublished 됨</span><span class="sxs-lookup"><span data-stu-id="e493b-134">NotPublished</span></span>
- <span data-ttu-id="e493b-135">게시자</span><span class="sxs-lookup"><span data-stu-id="e493b-135">Published</span></span> 

<span data-ttu-id="e493b-136">기본값은 NotPublished 값입니다.</span><span class="sxs-lookup"><span data-stu-id="e493b-136">The default value is NotPublished.</span></span>

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

### <span data-ttu-id="e493b-137">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="e493b-137">-SubscriptionRequired</span></span>
<span data-ttu-id="e493b-138">제품에 구독이 필요한 지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e493b-138">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="e493b-139">기본값은 **$True** 입니다.</span><span class="sxs-lookup"><span data-stu-id="e493b-139">The default value is **$True**.</span></span>

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

### <span data-ttu-id="e493b-140">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="e493b-140">-SubscriptionsLimit</span></span>
<span data-ttu-id="e493b-141">최대 동시 구독 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e493b-141">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="e493b-142">기본값은 1입니다.</span><span class="sxs-lookup"><span data-stu-id="e493b-142">The default value is 1.</span></span>

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

### <span data-ttu-id="e493b-143">-Title</span><span class="sxs-lookup"><span data-stu-id="e493b-143">-Title</span></span>
<span data-ttu-id="e493b-144">제품 제목을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e493b-144">Specifies the product title.</span></span>

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

### <span data-ttu-id="e493b-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e493b-145">CommonParameters</span></span>
<span data-ttu-id="e493b-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e493b-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e493b-147">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e493b-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e493b-148">입력</span><span class="sxs-lookup"><span data-stu-id="e493b-148">INPUTS</span></span>

### <span data-ttu-id="e493b-149">않아야</span><span class="sxs-lookup"><span data-stu-id="e493b-149">None</span></span>
<span data-ttu-id="e493b-150">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e493b-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e493b-151">출력</span><span class="sxs-lookup"><span data-stu-id="e493b-151">OUTPUTS</span></span>

### <span data-ttu-id="e493b-152">ApiManagement. ServiceManagement. \ PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="e493b-152">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="e493b-153">상속자</span><span class="sxs-lookup"><span data-stu-id="e493b-153">NOTES</span></span>

## <span data-ttu-id="e493b-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e493b-154">RELATED LINKS</span></span>

[<span data-ttu-id="e493b-155">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="e493b-155">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="e493b-156">제거-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="e493b-156">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)

[<span data-ttu-id="e493b-157">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="e493b-157">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


