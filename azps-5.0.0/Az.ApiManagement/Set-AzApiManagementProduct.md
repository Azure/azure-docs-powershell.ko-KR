---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 223FBBA6-4405-4B7A-BA63-5F2434A2A50D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProduct.md
ms.openlocfilehash: 9bee67dd299163b8e660b0e17c4e3bc11da5b40e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309722"
---
# <span data-ttu-id="2a742-101">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="2a742-101">Set-AzApiManagementProduct</span></span>

## <span data-ttu-id="2a742-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a742-102">SYNOPSIS</span></span>
<span data-ttu-id="2a742-103">API Management 제품 세부 정보를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a742-103">Sets the API Management product details.</span></span>

## <span data-ttu-id="2a742-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2a742-104">SYNTAX</span></span>

```
Set-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-Title <String>]
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a742-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2a742-105">DESCRIPTION</span></span>
<span data-ttu-id="2a742-106">**AzApiManagementProduct** CMDLET은 API 관리 제품 세부 정보를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a742-106">The **Set-AzApiManagementProduct** cmdlet sets the API Management product details.</span></span>

## <span data-ttu-id="2a742-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2a742-107">EXAMPLES</span></span>

### <span data-ttu-id="2a742-108">예제 1: 제품 세부 정보 업데이트</span><span class="sxs-lookup"><span data-stu-id="2a742-108">Example 1: Update the product details</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $True -State "NotPublished"
```

<span data-ttu-id="2a742-109">이 명령은 API Management 제품 세부 정보를 업데이트 하 고, 구독을 요청 하 고, 게시를 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a742-109">This command updates the API Management product details, requires a subscription, and then unpublishes.</span></span>

## <span data-ttu-id="2a742-110">변수</span><span class="sxs-lookup"><span data-stu-id="2a742-110">PARAMETERS</span></span>

### <span data-ttu-id="2a742-111">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="2a742-111">-ApprovalRequired</span></span>
<span data-ttu-id="2a742-112">제품 구독에 승인이 필요한 지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2a742-112">Indicates whether the subscription to the product requires approval.</span></span>
<span data-ttu-id="2a742-113">기본값은 **$False** 입니다.</span><span class="sxs-lookup"><span data-stu-id="2a742-113">The default value is **$False**.</span></span>

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

### <span data-ttu-id="2a742-114">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="2a742-114">-Context</span></span>
<span data-ttu-id="2a742-115">**PsApiManagementContext** 개체의 인스턴스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a742-115">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="2a742-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a742-116">-DefaultProfile</span></span>
<span data-ttu-id="2a742-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2a742-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a742-118">-설명</span><span class="sxs-lookup"><span data-stu-id="2a742-118">-Description</span></span>
<span data-ttu-id="2a742-119">제품 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a742-119">Specifies the product description.</span></span>

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

### <span data-ttu-id="2a742-120">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="2a742-120">-LegalTerms</span></span>
<span data-ttu-id="2a742-121">제품의 약관 사용 약관을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a742-121">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="2a742-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2a742-122">-PassThru</span></span>
<span data-ttu-id="2a742-123">passthru</span><span class="sxs-lookup"><span data-stu-id="2a742-123">passthru</span></span>

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

### <span data-ttu-id="2a742-124">-ProductId</span><span class="sxs-lookup"><span data-stu-id="2a742-124">-ProductId</span></span>
<span data-ttu-id="2a742-125">기존 제품의 식별자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a742-125">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="2a742-126">-상태</span><span class="sxs-lookup"><span data-stu-id="2a742-126">-State</span></span>
<span data-ttu-id="2a742-127">제품 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a742-127">Specifies the product state.</span></span>
<span data-ttu-id="2a742-128">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="2a742-128">psdx_paramvalues</span></span>
- <span data-ttu-id="2a742-129">NotPublished 됨</span><span class="sxs-lookup"><span data-stu-id="2a742-129">NotPublished</span></span>
- <span data-ttu-id="2a742-130">게시자</span><span class="sxs-lookup"><span data-stu-id="2a742-130">Published</span></span>

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

### <span data-ttu-id="2a742-131">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="2a742-131">-SubscriptionRequired</span></span>
<span data-ttu-id="2a742-132">제품에 구독이 필요한 지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2a742-132">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="2a742-133">이 매개 변수의 기본값은 **$True** 입니다.</span><span class="sxs-lookup"><span data-stu-id="2a742-133">The default value for this parameter is **$True**.</span></span>

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

### <span data-ttu-id="2a742-134">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="2a742-134">-SubscriptionsLimit</span></span>
<span data-ttu-id="2a742-135">최대 동시 구독 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a742-135">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="2a742-136">이 매개 변수의 기본값은 없음입니다.</span><span class="sxs-lookup"><span data-stu-id="2a742-136">The default value for this parameter is None.</span></span>

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

### <span data-ttu-id="2a742-137">-Title</span><span class="sxs-lookup"><span data-stu-id="2a742-137">-Title</span></span>
<span data-ttu-id="2a742-138">이 cmdlet이 설정 하는 제품 타이틀을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a742-138">Specifies the product title this cmdlet sets.</span></span>

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

### <span data-ttu-id="2a742-139">-확인</span><span class="sxs-lookup"><span data-stu-id="2a742-139">-Confirm</span></span>
<span data-ttu-id="2a742-140">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a742-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a742-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a742-141">-WhatIf</span></span>
<span data-ttu-id="2a742-142">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2a742-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2a742-143">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2a742-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a742-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a742-144">CommonParameters</span></span>
<span data-ttu-id="2a742-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a742-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a742-146">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2a742-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a742-147">입력</span><span class="sxs-lookup"><span data-stu-id="2a742-147">INPUTS</span></span>

### <span data-ttu-id="2a742-148">ApiManagement. ServiceManagement. \ PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2a742-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2a742-149">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2a742-149">System.String</span></span>

### <span data-ttu-id="2a742-150">시스템 Null 허용 ' 1 [[CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2a742-150">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="2a742-151">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e])</span><span class="sxs-lookup"><span data-stu-id="2a742-151">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="2a742-152">시스템 Null 허용 ' 1 [[ApiManagement]. ServiceManagement, PsApiManagementProductState, Microsoft azure. PowerShell. ApiManagement, Version = 1.0.0.0, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="2a742-152">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="2a742-153">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="2a742-153">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2a742-154">출력</span><span class="sxs-lookup"><span data-stu-id="2a742-154">OUTPUTS</span></span>

### <span data-ttu-id="2a742-155">ApiManagement. ServiceManagement. \ PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="2a742-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="2a742-156">상속자</span><span class="sxs-lookup"><span data-stu-id="2a742-156">NOTES</span></span>

## <span data-ttu-id="2a742-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2a742-157">RELATED LINKS</span></span>

[<span data-ttu-id="2a742-158">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="2a742-158">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="2a742-159">새로운 AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="2a742-159">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="2a742-160">제거-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="2a742-160">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)


