---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 223FBBA6-4405-4B7A-BA63-5F2434A2A50D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProduct.md
ms.openlocfilehash: f60bf40cd6226979955f71e413be3914fc05c417
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869321"
---
# <span data-ttu-id="c8fba-101">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="c8fba-101">Set-AzApiManagementProduct</span></span>

## <span data-ttu-id="c8fba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c8fba-102">SYNOPSIS</span></span>
<span data-ttu-id="c8fba-103">API Management 제품 세부 정보를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8fba-103">Sets the API Management product details.</span></span>

## <span data-ttu-id="c8fba-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c8fba-104">SYNTAX</span></span>

```
Set-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-Title <String>]
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8fba-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c8fba-105">DESCRIPTION</span></span>
<span data-ttu-id="c8fba-106">**AzApiManagementProduct** CMDLET은 API 관리 제품 세부 정보를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8fba-106">The **Set-AzApiManagementProduct** cmdlet sets the API Management product details.</span></span>

## <span data-ttu-id="c8fba-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c8fba-107">EXAMPLES</span></span>

### <span data-ttu-id="c8fba-108">예제 1: 제품 세부 정보 업데이트</span><span class="sxs-lookup"><span data-stu-id="c8fba-108">Example 1: Update the product details</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $True -State "NotPublished"
```

<span data-ttu-id="c8fba-109">이 명령은 API Management 제품 세부 정보를 업데이트 하 고, 구독을 요청 하 고, 게시를 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8fba-109">This command updates the API Management product details, requires a subscription, and then unpublishes.</span></span>

## <span data-ttu-id="c8fba-110">변수</span><span class="sxs-lookup"><span data-stu-id="c8fba-110">PARAMETERS</span></span>

### <span data-ttu-id="c8fba-111">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="c8fba-111">-ApprovalRequired</span></span>
<span data-ttu-id="c8fba-112">제품 구독에 승인이 필요한 지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c8fba-112">Indicates whether the subscription to the product requires approval.</span></span>
<span data-ttu-id="c8fba-113">기본값은 **$False** 입니다.</span><span class="sxs-lookup"><span data-stu-id="c8fba-113">The default value is **$False**.</span></span>

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

### <span data-ttu-id="c8fba-114">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="c8fba-114">-Context</span></span>
<span data-ttu-id="c8fba-115">**PsApiManagementContext** 개체의 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8fba-115">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="c8fba-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8fba-116">-DefaultProfile</span></span>
<span data-ttu-id="c8fba-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c8fba-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8fba-118">-설명</span><span class="sxs-lookup"><span data-stu-id="c8fba-118">-Description</span></span>
<span data-ttu-id="c8fba-119">제품 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8fba-119">Specifies the product description.</span></span>

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

### <span data-ttu-id="c8fba-120">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="c8fba-120">-LegalTerms</span></span>
<span data-ttu-id="c8fba-121">제품의 약관 사용 약관을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8fba-121">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="c8fba-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c8fba-122">-PassThru</span></span>
<span data-ttu-id="c8fba-123">passthru</span><span class="sxs-lookup"><span data-stu-id="c8fba-123">passthru</span></span>

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

### <span data-ttu-id="c8fba-124">-ProductId</span><span class="sxs-lookup"><span data-stu-id="c8fba-124">-ProductId</span></span>
<span data-ttu-id="c8fba-125">기존 제품의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8fba-125">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="c8fba-126">-상태</span><span class="sxs-lookup"><span data-stu-id="c8fba-126">-State</span></span>
<span data-ttu-id="c8fba-127">제품 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8fba-127">Specifies the product state.</span></span>
<span data-ttu-id="c8fba-128">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="c8fba-128">psdx_paramvalues</span></span>
- <span data-ttu-id="c8fba-129">NotPublished 됨</span><span class="sxs-lookup"><span data-stu-id="c8fba-129">NotPublished</span></span>
- <span data-ttu-id="c8fba-130">게시자</span><span class="sxs-lookup"><span data-stu-id="c8fba-130">Published</span></span>

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

### <span data-ttu-id="c8fba-131">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="c8fba-131">-SubscriptionRequired</span></span>
<span data-ttu-id="c8fba-132">제품에 구독이 필요한 지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c8fba-132">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="c8fba-133">이 매개 변수의 기본값은 **$True** 입니다.</span><span class="sxs-lookup"><span data-stu-id="c8fba-133">The default value for this parameter is **$True**.</span></span>

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

### <span data-ttu-id="c8fba-134">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="c8fba-134">-SubscriptionsLimit</span></span>
<span data-ttu-id="c8fba-135">최대 동시 구독 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8fba-135">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="c8fba-136">이 매개 변수의 기본값은 1입니다.</span><span class="sxs-lookup"><span data-stu-id="c8fba-136">The default value for this parameter is 1.</span></span>

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

### <span data-ttu-id="c8fba-137">-Title</span><span class="sxs-lookup"><span data-stu-id="c8fba-137">-Title</span></span>
<span data-ttu-id="c8fba-138">이 cmdlet이 설정 하는 제품 타이틀을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8fba-138">Specifies the product title this cmdlet sets.</span></span>

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

### <span data-ttu-id="c8fba-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8fba-139">CommonParameters</span></span>
<span data-ttu-id="c8fba-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c8fba-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8fba-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8fba-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8fba-142">입력</span><span class="sxs-lookup"><span data-stu-id="c8fba-142">INPUTS</span></span>

### <span data-ttu-id="c8fba-143">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c8fba-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c8fba-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c8fba-144">System.String</span></span>

### <span data-ttu-id="c8fba-145">시스템 Null 허용 ' 1 [[CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="c8fba-145">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="c8fba-146">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e])</span><span class="sxs-lookup"><span data-stu-id="c8fba-146">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="c8fba-147">시스템 Null 허용 ' 1 [[ApiManagement]. ServiceManagement, PsApiManagementProductState, Microsoft azure. PowerShell. ApiManagement, Version = 1.0.0.0, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="c8fba-147">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="c8fba-148">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="c8fba-148">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c8fba-149">출력</span><span class="sxs-lookup"><span data-stu-id="c8fba-149">OUTPUTS</span></span>

### <span data-ttu-id="c8fba-150">ApiManagement. ServiceManagement. \ PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="c8fba-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="c8fba-151">상속자</span><span class="sxs-lookup"><span data-stu-id="c8fba-151">NOTES</span></span>

## <span data-ttu-id="c8fba-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c8fba-152">RELATED LINKS</span></span>

[<span data-ttu-id="c8fba-153">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="c8fba-153">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="c8fba-154">새로운 AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="c8fba-154">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="c8fba-155">제거-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="c8fba-155">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)


