---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: E94B88AA-B8B0-49F0-AD36-6707E17B40AD
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementProduct.md
ms.openlocfilehash: 12de4862e91555b90a4168ac7ac5908b897d6e49
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988526"
---
# <span data-ttu-id="f6c05-101">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="f6c05-101">New-AzApiManagementProduct</span></span>

## <span data-ttu-id="f6c05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6c05-102">SYNOPSIS</span></span>
<span data-ttu-id="f6c05-103">API Management 제품을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f6c05-103">Creates an API Management product.</span></span>

## <span data-ttu-id="f6c05-104">구문</span><span class="sxs-lookup"><span data-stu-id="f6c05-104">SYNTAX</span></span>

```
New-AzApiManagementProduct -Context <PsApiManagementContext> [-ProductId <String>] -Title <String>
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6c05-105">설명</span><span class="sxs-lookup"><span data-stu-id="f6c05-105">DESCRIPTION</span></span>
<span data-ttu-id="f6c05-106">**New-AzApiManagementProduct** cmdlet은 API Management 제품을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f6c05-106">The **New-AzApiManagementProduct** cmdlet creates an API Management product.</span></span>

## <span data-ttu-id="f6c05-107">예제</span><span class="sxs-lookup"><span data-stu-id="f6c05-107">EXAMPLES</span></span>

### <span data-ttu-id="f6c05-108">예제 1: 구독이 필요하지 않은 제품 만들기</span><span class="sxs-lookup"><span data-stu-id="f6c05-108">Example 1: Create a product that does not require a subscription</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $False -State "Published"
```

<span data-ttu-id="f6c05-109">이 명령은 API Management 제품을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f6c05-109">This command creates an API Management product.</span></span>
<span data-ttu-id="f6c05-110">구독이 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f6c05-110">No subscription is required.</span></span>

### <span data-ttu-id="f6c05-111">예제 2: 구독 및 승인이 필요한 제품 만들기</span><span class="sxs-lookup"><span data-stu-id="f6c05-111">Example 2: Create a product that requires a subscription and approval</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementProduct -Context $apimContext -ProductId "9876543210" -Title "Unlimited" -Description "Subscribers have completely unlimited access to the API. Administrator approval is required." -LegalTerms "Free for all" -ApprovalRequired $True -State "Published" -NotificationPeriod "D10" -SubscriptionPeriod "Y1"
```

<span data-ttu-id="f6c05-112">이 명령은 제품을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f6c05-112">This command creates a product.</span></span>
<span data-ttu-id="f6c05-113">구독 및 승인이 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="f6c05-113">A subscription and approval are required.</span></span>
<span data-ttu-id="f6c05-114">이 명령은 알림 기간을 10일로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="f6c05-114">This command sets the notification period to 10 days.</span></span>
<span data-ttu-id="f6c05-115">구독 기간은 1년으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="f6c05-115">The subscription duration is set to one year.</span></span>

## <span data-ttu-id="f6c05-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f6c05-116">PARAMETERS</span></span>

### <span data-ttu-id="f6c05-117">-approvalRequired</span><span class="sxs-lookup"><span data-stu-id="f6c05-117">-ApprovalRequired</span></span>
<span data-ttu-id="f6c05-118">제품에 대한 구독에 승인이 필요한지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f6c05-118">Indicates whether the subscription to the product requires approval or not.</span></span>
<span data-ttu-id="f6c05-119">기본적으로 이 매개 변수는 **$False.**</span><span class="sxs-lookup"><span data-stu-id="f6c05-119">By default, this parameter is **$False**.</span></span>

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

### <span data-ttu-id="f6c05-120">-Context</span><span class="sxs-lookup"><span data-stu-id="f6c05-120">-Context</span></span>
<span data-ttu-id="f6c05-121">**PsApiManagementContext** 개체의 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f6c05-121">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="f6c05-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6c05-122">-DefaultProfile</span></span>
<span data-ttu-id="f6c05-123">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f6c05-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6c05-124">-Description</span><span class="sxs-lookup"><span data-stu-id="f6c05-124">-Description</span></span>
<span data-ttu-id="f6c05-125">제품 설명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f6c05-125">Specifies the product description.</span></span>

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

### <span data-ttu-id="f6c05-126">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="f6c05-126">-LegalTerms</span></span>
<span data-ttu-id="f6c05-127">제품의 법적 사용 약관을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f6c05-127">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="f6c05-128">-ProductId</span><span class="sxs-lookup"><span data-stu-id="f6c05-128">-ProductId</span></span>
<span data-ttu-id="f6c05-129">새 제품의 식별자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f6c05-129">Specifies the identifier of new product.</span></span>
<span data-ttu-id="f6c05-130">이 매개 변수를 지정하지 않으면 새 제품이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="f6c05-130">If you do not specify this parameter, a new product is generated.</span></span>

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

### <span data-ttu-id="f6c05-131">-State</span><span class="sxs-lookup"><span data-stu-id="f6c05-131">-State</span></span>
<span data-ttu-id="f6c05-132">제품 상태를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f6c05-132">Specifies the product state.</span></span>
<span data-ttu-id="f6c05-133">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="f6c05-133">psdx_paramvalues</span></span>
- <span data-ttu-id="f6c05-134">NotPublished</span><span class="sxs-lookup"><span data-stu-id="f6c05-134">NotPublished</span></span>
- <span data-ttu-id="f6c05-135">게시된 기본값은 NotPublished입니다.</span><span class="sxs-lookup"><span data-stu-id="f6c05-135">Published The default value is NotPublished.</span></span>

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

### <span data-ttu-id="f6c05-136">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="f6c05-136">-SubscriptionRequired</span></span>
<span data-ttu-id="f6c05-137">제품에 구독이 필요한지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="f6c05-137">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="f6c05-138">기본값은 **$True.**</span><span class="sxs-lookup"><span data-stu-id="f6c05-138">The default value is **$True**.</span></span>

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

### <span data-ttu-id="f6c05-139">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="f6c05-139">-SubscriptionsLimit</span></span>
<span data-ttu-id="f6c05-140">최대 동시 구독 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f6c05-140">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="f6c05-141">기본값은 없음입니다.</span><span class="sxs-lookup"><span data-stu-id="f6c05-141">The default value is None.</span></span>

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

### <span data-ttu-id="f6c05-142">-Title</span><span class="sxs-lookup"><span data-stu-id="f6c05-142">-Title</span></span>
<span data-ttu-id="f6c05-143">제품 제목을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f6c05-143">Specifies the product title.</span></span>

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

### <span data-ttu-id="f6c05-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6c05-144">CommonParameters</span></span>
<span data-ttu-id="f6c05-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f6c05-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6c05-146">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f6c05-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6c05-147">입력</span><span class="sxs-lookup"><span data-stu-id="f6c05-147">INPUTS</span></span>

### <span data-ttu-id="f6c05-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f6c05-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f6c05-149">System.String</span><span class="sxs-lookup"><span data-stu-id="f6c05-149">System.String</span></span>

### <span data-ttu-id="f6c05-150">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f6c05-150">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="f6c05-151">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f6c05-151">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="f6c05-152">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="f6c05-152">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="f6c05-153">출력</span><span class="sxs-lookup"><span data-stu-id="f6c05-153">OUTPUTS</span></span>

### <span data-ttu-id="f6c05-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.psApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="f6c05-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="f6c05-155">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f6c05-155">NOTES</span></span>

## <span data-ttu-id="f6c05-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f6c05-156">RELATED LINKS</span></span>

[<span data-ttu-id="f6c05-157">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="f6c05-157">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="f6c05-158">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="f6c05-158">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)

[<span data-ttu-id="f6c05-159">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="f6c05-159">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


