---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 223FBBA6-4405-4B7A-BA63-5F2434A2A50D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProduct.md
ms.openlocfilehash: dac6e48faba1590897161ab59fed05f1f0b331df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531248"
---
# <span data-ttu-id="a31a1-101">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="a31a1-101">Set-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="a31a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a31a1-102">SYNOPSIS</span></span>
<span data-ttu-id="a31a1-103">API Management 제품 세부 정보를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a31a1-103">Sets the API Management product details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a31a1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a31a1-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-Title <String>]
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a31a1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a31a1-105">DESCRIPTION</span></span>
<span data-ttu-id="a31a1-106">**AzureRmApiManagementProduct** CMDLET은 API 관리 제품 세부 정보를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a31a1-106">The **Set-AzureRmApiManagementProduct** cmdlet sets the API Management product details.</span></span>

## <span data-ttu-id="a31a1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a31a1-107">EXAMPLES</span></span>

### <span data-ttu-id="a31a1-108">예제 1: 제품 세부 정보 업데이트</span><span class="sxs-lookup"><span data-stu-id="a31a1-108">Example 1: Update the product details</span></span>
```
PS C:\>Set-AzureRmApiManagementProduct -Context $APImContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $True -State "NotPublished"
```

<span data-ttu-id="a31a1-109">이 명령은 API Management 제품 세부 정보를 업데이트 하 고, 구독을 요청 하 고, 게시를 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="a31a1-109">This command updates the API Management product details, requires a subscription, and then unpublishes.</span></span>

## <span data-ttu-id="a31a1-110">변수</span><span class="sxs-lookup"><span data-stu-id="a31a1-110">PARAMETERS</span></span>

### <span data-ttu-id="a31a1-111">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="a31a1-111">-ApprovalRequired</span></span>
<span data-ttu-id="a31a1-112">제품 구독에 승인이 필요한 지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a31a1-112">Indicates whether the subscription to the product requires approval.</span></span>
<span data-ttu-id="a31a1-113">기본값은 **$False** 입니다.</span><span class="sxs-lookup"><span data-stu-id="a31a1-113">The default value is **$False**.</span></span>

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

### <span data-ttu-id="a31a1-114">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="a31a1-114">-Context</span></span>
<span data-ttu-id="a31a1-115">**PsApiManagementContext** 개체의 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a31a1-115">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="a31a1-116">-설명</span><span class="sxs-lookup"><span data-stu-id="a31a1-116">-Description</span></span>
<span data-ttu-id="a31a1-117">제품 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a31a1-117">Specifies the product description.</span></span>

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

### <span data-ttu-id="a31a1-118">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="a31a1-118">-LegalTerms</span></span>
<span data-ttu-id="a31a1-119">제품의 약관 사용 약관을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a31a1-119">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="a31a1-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a31a1-120">-PassThru</span></span>
<span data-ttu-id="a31a1-121">passthru</span><span class="sxs-lookup"><span data-stu-id="a31a1-121">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a31a1-122">-ProductId</span><span class="sxs-lookup"><span data-stu-id="a31a1-122">-ProductId</span></span>
<span data-ttu-id="a31a1-123">기존 제품의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a31a1-123">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="a31a1-124">-상태</span><span class="sxs-lookup"><span data-stu-id="a31a1-124">-State</span></span>
<span data-ttu-id="a31a1-125">제품 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a31a1-125">Specifies the product state.</span></span>
<span data-ttu-id="a31a1-126">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="a31a1-126">psdx_paramvalues</span></span>

- <span data-ttu-id="a31a1-127">NotPublished 됨</span><span class="sxs-lookup"><span data-stu-id="a31a1-127">NotPublished</span></span>
- <span data-ttu-id="a31a1-128">게시자</span><span class="sxs-lookup"><span data-stu-id="a31a1-128">Published</span></span>

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

### <span data-ttu-id="a31a1-129">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="a31a1-129">-SubscriptionRequired</span></span>
<span data-ttu-id="a31a1-130">제품에 구독이 필요한 지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="a31a1-130">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="a31a1-131">이 매개 변수의 기본값은 **$True** 입니다.</span><span class="sxs-lookup"><span data-stu-id="a31a1-131">The default value for this parameter is **$True**.</span></span>

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

### <span data-ttu-id="a31a1-132">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="a31a1-132">-SubscriptionsLimit</span></span>
<span data-ttu-id="a31a1-133">최대 동시 구독 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a31a1-133">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="a31a1-134">이 매개 변수의 기본값은 1입니다.</span><span class="sxs-lookup"><span data-stu-id="a31a1-134">The default value for this parameter is 1.</span></span>

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

### <span data-ttu-id="a31a1-135">-Title</span><span class="sxs-lookup"><span data-stu-id="a31a1-135">-Title</span></span>
<span data-ttu-id="a31a1-136">이 cmdlet이 설정 하는 제품 타이틀을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a31a1-136">Specifies the product title this cmdlet sets.</span></span>

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

### <span data-ttu-id="a31a1-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a31a1-137">-DefaultProfile</span></span>
<span data-ttu-id="a31a1-138">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a31a1-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a31a1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a31a1-139">CommonParameters</span></span>
<span data-ttu-id="a31a1-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a31a1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a31a1-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a31a1-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a31a1-142">입력</span><span class="sxs-lookup"><span data-stu-id="a31a1-142">INPUTS</span></span>

## <span data-ttu-id="a31a1-143">출력</span><span class="sxs-lookup"><span data-stu-id="a31a1-143">OUTPUTS</span></span>

### <span data-ttu-id="a31a1-144">ApiManagement. ServiceManagement. \ PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="a31a1-144">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="a31a1-145">상속자</span><span class="sxs-lookup"><span data-stu-id="a31a1-145">NOTES</span></span>

## <span data-ttu-id="a31a1-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a31a1-146">RELATED LINKS</span></span>

[<span data-ttu-id="a31a1-147">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="a31a1-147">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="a31a1-148">새로운 AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="a31a1-148">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="a31a1-149">제거-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="a31a1-149">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)


