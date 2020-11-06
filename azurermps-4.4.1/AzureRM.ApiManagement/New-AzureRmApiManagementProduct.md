---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: E94B88AA-B8B0-49F0-AD36-6707E17B40AD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementProduct.md
ms.openlocfilehash: a978fce4d44a061796597f2f3ae08c78c1021bdd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531257"
---
# <span data-ttu-id="b5131-101">New-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="b5131-101">New-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="b5131-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5131-102">SYNOPSIS</span></span>
<span data-ttu-id="b5131-103">API Management 제품을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b5131-103">Creates an API Management product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5131-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b5131-104">SYNTAX</span></span>

```
New-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-ProductId <String>] -Title <String>
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b5131-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b5131-105">DESCRIPTION</span></span>
<span data-ttu-id="b5131-106">**AzureRmApiManagementProduct** CMDLET은 API 관리 제품을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b5131-106">The **New-AzureRmApiManagementProduct** cmdlet creates an API Management product.</span></span>

## <span data-ttu-id="b5131-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b5131-107">EXAMPLES</span></span>

### <span data-ttu-id="b5131-108">예제 1: 구독이 필요 하지 않은 제품 만들기</span><span class="sxs-lookup"><span data-stu-id="b5131-108">Example 1: Create a product that does not require a subscription</span></span>
```
PS C:\>New-AzureRmApiManagementProduct -Context $APImContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $False -State "Published"
```

<span data-ttu-id="b5131-109">이 명령은 API 관리 제품을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b5131-109">This command creates an API Management product.</span></span>
<span data-ttu-id="b5131-110">구독이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b5131-110">No subscription is required.</span></span>

### <span data-ttu-id="b5131-111">예제 2: 구독 및 승인이 필요한 제품 만들기</span><span class="sxs-lookup"><span data-stu-id="b5131-111">Example 2: Create a product that requires a subscription and approval</span></span>
```
PS C:\>New-AzureRmApiManagementProduct -Context $APImContext -ProductId "9876543210" -Title "Unlimited" -Description "Subscribers have completely unlimited access to the API. Administrator approval is required." -LegalTerms "Free for all" -ApprovalRequired $True -State "Published" -NotificationPeriod "D10" -SubscriptionPeriod "Y1"
```

<span data-ttu-id="b5131-112">이 명령은 제품을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b5131-112">This command creates a product.</span></span>
<span data-ttu-id="b5131-113">구독 및 승인이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5131-113">A subscription and approval are required.</span></span>
<span data-ttu-id="b5131-114">이 명령은 알림 기간을 10 일로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5131-114">This command sets the notification period to 10 days.</span></span>
<span data-ttu-id="b5131-115">구독 기간이 1 년으로 설정 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b5131-115">The subscription duration is set to one year.</span></span>

## <span data-ttu-id="b5131-116">변수</span><span class="sxs-lookup"><span data-stu-id="b5131-116">PARAMETERS</span></span>

### <span data-ttu-id="b5131-117">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="b5131-117">-ApprovalRequired</span></span>
<span data-ttu-id="b5131-118">제품에 대 한 구독에 승인이 필요한 지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b5131-118">Indicates whether the subscription to the product requires approval or not.</span></span>
<span data-ttu-id="b5131-119">기본적으로이 매개 변수는 **$False** 입니다.</span><span class="sxs-lookup"><span data-stu-id="b5131-119">By default, this parameter is **$False**.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5131-120">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="b5131-120">-Context</span></span>
<span data-ttu-id="b5131-121">**PsApiManagementContext** 개체의 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5131-121">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="b5131-122">-설명</span><span class="sxs-lookup"><span data-stu-id="b5131-122">-Description</span></span>
<span data-ttu-id="b5131-123">제품 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5131-123">Specifies the product description.</span></span>

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

### <span data-ttu-id="b5131-124">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="b5131-124">-LegalTerms</span></span>
<span data-ttu-id="b5131-125">제품의 약관 사용 약관을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5131-125">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="b5131-126">-ProductId</span><span class="sxs-lookup"><span data-stu-id="b5131-126">-ProductId</span></span>
<span data-ttu-id="b5131-127">새 제품의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5131-127">Specifies the identifier of new product.</span></span>
<span data-ttu-id="b5131-128">이 매개 변수를 지정 하지 않으면 새 제품이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b5131-128">If you do not specify this parameter, a new product is generated.</span></span>

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

### <span data-ttu-id="b5131-129">-상태</span><span class="sxs-lookup"><span data-stu-id="b5131-129">-State</span></span>
<span data-ttu-id="b5131-130">제품 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5131-130">Specifies the product state.</span></span>
<span data-ttu-id="b5131-131">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="b5131-131">psdx_paramvalues</span></span>

- <span data-ttu-id="b5131-132">NotPublished 됨</span><span class="sxs-lookup"><span data-stu-id="b5131-132">NotPublished</span></span>
- <span data-ttu-id="b5131-133">게시자</span><span class="sxs-lookup"><span data-stu-id="b5131-133">Published</span></span> 

<span data-ttu-id="b5131-134">기본값은 NotPublished 값입니다.</span><span class="sxs-lookup"><span data-stu-id="b5131-134">The default value is NotPublished.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState]
Parameter Sets: (All)
Aliases: 
Accepted values: NotPublished, Published

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5131-135">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="b5131-135">-SubscriptionRequired</span></span>
<span data-ttu-id="b5131-136">제품에 구독이 필요한 지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b5131-136">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="b5131-137">기본값은 **$True** 입니다.</span><span class="sxs-lookup"><span data-stu-id="b5131-137">The default value is **$True**.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5131-138">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="b5131-138">-SubscriptionsLimit</span></span>
<span data-ttu-id="b5131-139">최대 동시 구독 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5131-139">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="b5131-140">기본값은 1입니다.</span><span class="sxs-lookup"><span data-stu-id="b5131-140">The default value is 1.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5131-141">-Title</span><span class="sxs-lookup"><span data-stu-id="b5131-141">-Title</span></span>
<span data-ttu-id="b5131-142">제품 제목을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5131-142">Specifies the product title.</span></span>

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

### <span data-ttu-id="b5131-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5131-143">-DefaultProfile</span></span>
<span data-ttu-id="b5131-144">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b5131-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b5131-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5131-145">CommonParameters</span></span>
<span data-ttu-id="b5131-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5131-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5131-147">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5131-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5131-148">입력</span><span class="sxs-lookup"><span data-stu-id="b5131-148">INPUTS</span></span>

## <span data-ttu-id="b5131-149">출력</span><span class="sxs-lookup"><span data-stu-id="b5131-149">OUTPUTS</span></span>

### <span data-ttu-id="b5131-150">ApiManagement. ServiceManagement. \ PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="b5131-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="b5131-151">상속자</span><span class="sxs-lookup"><span data-stu-id="b5131-151">NOTES</span></span>

## <span data-ttu-id="b5131-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b5131-152">RELATED LINKS</span></span>

[<span data-ttu-id="b5131-153">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="b5131-153">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="b5131-154">제거-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="b5131-154">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)

[<span data-ttu-id="b5131-155">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="b5131-155">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


