---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: E94B88AA-B8B0-49F0-AD36-6707E17B40AD
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProduct.md
ms.openlocfilehash: 1b99a5ac02364b54cf4411a0341ceaf749b8fa70
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698033"
---
# <span data-ttu-id="40b06-101">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="40b06-101">New-AzApiManagementProduct</span></span>

## <span data-ttu-id="40b06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40b06-102">SYNOPSIS</span></span>
<span data-ttu-id="40b06-103">API Management 제품을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="40b06-103">Creates an API Management product.</span></span>

## <span data-ttu-id="40b06-104">구문과</span><span class="sxs-lookup"><span data-stu-id="40b06-104">SYNTAX</span></span>

```
New-AzApiManagementProduct -Context <PsApiManagementContext> [-ProductId <String>] -Title <String>
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40b06-105">설명은</span><span class="sxs-lookup"><span data-stu-id="40b06-105">DESCRIPTION</span></span>
<span data-ttu-id="40b06-106">**AzApiManagementProduct** CMDLET은 API 관리 제품을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="40b06-106">The **New-AzApiManagementProduct** cmdlet creates an API Management product.</span></span>

## <span data-ttu-id="40b06-107">예제의</span><span class="sxs-lookup"><span data-stu-id="40b06-107">EXAMPLES</span></span>

### <span data-ttu-id="40b06-108">예제 1: 구독이 필요 하지 않은 제품 만들기</span><span class="sxs-lookup"><span data-stu-id="40b06-108">Example 1: Create a product that does not require a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $False -State "Published"
```

<span data-ttu-id="40b06-109">이 명령은 API 관리 제품을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="40b06-109">This command creates an API Management product.</span></span>
<span data-ttu-id="40b06-110">구독이 필요 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="40b06-110">No subscription is required.</span></span>

### <span data-ttu-id="40b06-111">예제 2: 구독 및 승인이 필요한 제품 만들기</span><span class="sxs-lookup"><span data-stu-id="40b06-111">Example 2: Create a product that requires a subscription and approval</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementProduct -Context $apimContext -ProductId "9876543210" -Title "Unlimited" -Description "Subscribers have completely unlimited access to the API. Administrator approval is required." -LegalTerms "Free for all" -ApprovalRequired $True -State "Published" -NotificationPeriod "D10" -SubscriptionPeriod "Y1"
```

<span data-ttu-id="40b06-112">이 명령은 제품을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="40b06-112">This command creates a product.</span></span>
<span data-ttu-id="40b06-113">구독 및 승인이 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b06-113">A subscription and approval are required.</span></span>
<span data-ttu-id="40b06-114">이 명령은 알림 기간을 10 일로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b06-114">This command sets the notification period to 10 days.</span></span>
<span data-ttu-id="40b06-115">구독 기간이 1 년으로 설정 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="40b06-115">The subscription duration is set to one year.</span></span>

## <span data-ttu-id="40b06-116">변수</span><span class="sxs-lookup"><span data-stu-id="40b06-116">PARAMETERS</span></span>

### <span data-ttu-id="40b06-117">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="40b06-117">-ApprovalRequired</span></span>
<span data-ttu-id="40b06-118">제품에 대 한 구독에 승인이 필요한 지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="40b06-118">Indicates whether the subscription to the product requires approval or not.</span></span>
<span data-ttu-id="40b06-119">기본적으로이 매개 변수는 **$False** 입니다.</span><span class="sxs-lookup"><span data-stu-id="40b06-119">By default, this parameter is **$False**.</span></span>

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

### <span data-ttu-id="40b06-120">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="40b06-120">-Context</span></span>
<span data-ttu-id="40b06-121">**PsApiManagementContext** 개체의 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b06-121">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="40b06-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40b06-122">-DefaultProfile</span></span>
<span data-ttu-id="40b06-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="40b06-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40b06-124">-설명</span><span class="sxs-lookup"><span data-stu-id="40b06-124">-Description</span></span>
<span data-ttu-id="40b06-125">제품 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b06-125">Specifies the product description.</span></span>

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

### <span data-ttu-id="40b06-126">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="40b06-126">-LegalTerms</span></span>
<span data-ttu-id="40b06-127">제품의 약관 사용 약관을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b06-127">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="40b06-128">-ProductId</span><span class="sxs-lookup"><span data-stu-id="40b06-128">-ProductId</span></span>
<span data-ttu-id="40b06-129">새 제품의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b06-129">Specifies the identifier of new product.</span></span>
<span data-ttu-id="40b06-130">이 매개 변수를 지정 하지 않으면 새 제품이 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="40b06-130">If you do not specify this parameter, a new product is generated.</span></span>

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

### <span data-ttu-id="40b06-131">-상태</span><span class="sxs-lookup"><span data-stu-id="40b06-131">-State</span></span>
<span data-ttu-id="40b06-132">제품 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b06-132">Specifies the product state.</span></span>
<span data-ttu-id="40b06-133">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="40b06-133">psdx_paramvalues</span></span>
- <span data-ttu-id="40b06-134">NotPublished 됨</span><span class="sxs-lookup"><span data-stu-id="40b06-134">NotPublished</span></span>
- <span data-ttu-id="40b06-135">게시 된 기본값은 NotPublished입니다.</span><span class="sxs-lookup"><span data-stu-id="40b06-135">Published The default value is NotPublished.</span></span>

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

### <span data-ttu-id="40b06-136">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="40b06-136">-SubscriptionRequired</span></span>
<span data-ttu-id="40b06-137">제품에 구독이 필요한 지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="40b06-137">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="40b06-138">기본값은 **$True** 입니다.</span><span class="sxs-lookup"><span data-stu-id="40b06-138">The default value is **$True**.</span></span>

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

### <span data-ttu-id="40b06-139">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="40b06-139">-SubscriptionsLimit</span></span>
<span data-ttu-id="40b06-140">최대 동시 구독 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b06-140">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="40b06-141">기본값은 1입니다.</span><span class="sxs-lookup"><span data-stu-id="40b06-141">The default value is 1.</span></span>

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

### <span data-ttu-id="40b06-142">-Title</span><span class="sxs-lookup"><span data-stu-id="40b06-142">-Title</span></span>
<span data-ttu-id="40b06-143">제품 제목을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b06-143">Specifies the product title.</span></span>

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

### <span data-ttu-id="40b06-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40b06-144">CommonParameters</span></span>
<span data-ttu-id="40b06-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b06-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40b06-146">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="40b06-146">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40b06-147">입력</span><span class="sxs-lookup"><span data-stu-id="40b06-147">INPUTS</span></span>

### <span data-ttu-id="40b06-148">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="40b06-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="40b06-149">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="40b06-149">System.String</span></span>

### <span data-ttu-id="40b06-150">시스템 Null 허용 ' 1 [[CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="40b06-150">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="40b06-151">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e])</span><span class="sxs-lookup"><span data-stu-id="40b06-151">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="40b06-152">시스템 Null 허용 ' 1 [[ApiManagement]. ServiceManagement, PsApiManagementProductState, Microsoft azure. PowerShell. ApiManagement, Version = 1.0.0.0, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="40b06-152">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="40b06-153">출력</span><span class="sxs-lookup"><span data-stu-id="40b06-153">OUTPUTS</span></span>

### <span data-ttu-id="40b06-154">ApiManagement. ServiceManagement. \ PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="40b06-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="40b06-155">상속자</span><span class="sxs-lookup"><span data-stu-id="40b06-155">NOTES</span></span>

## <span data-ttu-id="40b06-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="40b06-156">RELATED LINKS</span></span>

[<span data-ttu-id="40b06-157">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="40b06-157">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="40b06-158">제거-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="40b06-158">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)

[<span data-ttu-id="40b06-159">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="40b06-159">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


