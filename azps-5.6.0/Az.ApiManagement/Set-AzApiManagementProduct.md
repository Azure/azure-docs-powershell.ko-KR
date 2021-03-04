---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 223FBBA6-4405-4B7A-BA63-5F2434A2A50D
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/set-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProduct.md
ms.openlocfilehash: e827fcf43c151f0812d96456de430f57686d4562
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959835"
---
# <span data-ttu-id="9e15a-101">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="9e15a-101">Set-AzApiManagementProduct</span></span>

## <span data-ttu-id="9e15a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e15a-102">SYNOPSIS</span></span>
<span data-ttu-id="9e15a-103">API Management 제품 세부 정보를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="9e15a-103">Sets the API Management product details.</span></span>

## <span data-ttu-id="9e15a-104">구문</span><span class="sxs-lookup"><span data-stu-id="9e15a-104">SYNTAX</span></span>

```
Set-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-Title <String>]
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e15a-105">설명</span><span class="sxs-lookup"><span data-stu-id="9e15a-105">DESCRIPTION</span></span>
<span data-ttu-id="9e15a-106">**Set-AzApiManagementProduct** cmdlet은 API Management 제품 세부 정보를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="9e15a-106">The **Set-AzApiManagementProduct** cmdlet sets the API Management product details.</span></span>

## <span data-ttu-id="9e15a-107">예제</span><span class="sxs-lookup"><span data-stu-id="9e15a-107">EXAMPLES</span></span>

### <span data-ttu-id="9e15a-108">예제 1: 제품 세부 정보 업데이트</span><span class="sxs-lookup"><span data-stu-id="9e15a-108">Example 1: Update the product details</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $True -State "NotPublished"
```

<span data-ttu-id="9e15a-109">이 명령은 API Management 제품 세부 정보를 업데이트하고 구독을 요구한 다음 게시를 취소합니다.</span><span class="sxs-lookup"><span data-stu-id="9e15a-109">This command updates the API Management product details, requires a subscription, and then unpublishes.</span></span>

## <span data-ttu-id="9e15a-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="9e15a-110">PARAMETERS</span></span>

### <span data-ttu-id="9e15a-111">-approvalRequired</span><span class="sxs-lookup"><span data-stu-id="9e15a-111">-ApprovalRequired</span></span>
<span data-ttu-id="9e15a-112">제품에 대한 구독에 승인이 필요한지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9e15a-112">Indicates whether the subscription to the product requires approval.</span></span>
<span data-ttu-id="9e15a-113">기본값은 **$False.**</span><span class="sxs-lookup"><span data-stu-id="9e15a-113">The default value is **$False**.</span></span>

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

### <span data-ttu-id="9e15a-114">-Context</span><span class="sxs-lookup"><span data-stu-id="9e15a-114">-Context</span></span>
<span data-ttu-id="9e15a-115">**PsApiManagementContext** 개체의 인스턴스를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9e15a-115">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="9e15a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e15a-116">-DefaultProfile</span></span>
<span data-ttu-id="9e15a-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9e15a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e15a-118">-Description</span><span class="sxs-lookup"><span data-stu-id="9e15a-118">-Description</span></span>
<span data-ttu-id="9e15a-119">제품 설명을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9e15a-119">Specifies the product description.</span></span>

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

### <span data-ttu-id="9e15a-120">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="9e15a-120">-LegalTerms</span></span>
<span data-ttu-id="9e15a-121">제품의 법적 사용 약관을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9e15a-121">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="9e15a-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9e15a-122">-PassThru</span></span>
<span data-ttu-id="9e15a-123">passthru</span><span class="sxs-lookup"><span data-stu-id="9e15a-123">passthru</span></span>

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

### <span data-ttu-id="9e15a-124">-ProductId</span><span class="sxs-lookup"><span data-stu-id="9e15a-124">-ProductId</span></span>
<span data-ttu-id="9e15a-125">기존 제품의 식별자를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9e15a-125">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="9e15a-126">-State</span><span class="sxs-lookup"><span data-stu-id="9e15a-126">-State</span></span>
<span data-ttu-id="9e15a-127">제품 상태를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9e15a-127">Specifies the product state.</span></span>
<span data-ttu-id="9e15a-128">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="9e15a-128">psdx_paramvalues</span></span>
- <span data-ttu-id="9e15a-129">NotPublished</span><span class="sxs-lookup"><span data-stu-id="9e15a-129">NotPublished</span></span>
- <span data-ttu-id="9e15a-130">게시</span><span class="sxs-lookup"><span data-stu-id="9e15a-130">Published</span></span>

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

### <span data-ttu-id="9e15a-131">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="9e15a-131">-SubscriptionRequired</span></span>
<span data-ttu-id="9e15a-132">제품에 구독이 필요한지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9e15a-132">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="9e15a-133">이 매개 변수의 기본값은 **$True.**</span><span class="sxs-lookup"><span data-stu-id="9e15a-133">The default value for this parameter is **$True**.</span></span>

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

### <span data-ttu-id="9e15a-134">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="9e15a-134">-SubscriptionsLimit</span></span>
<span data-ttu-id="9e15a-135">최대 동시 구독 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9e15a-135">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="9e15a-136">이 매개 변수의 기본값은 없음입니다.</span><span class="sxs-lookup"><span data-stu-id="9e15a-136">The default value for this parameter is None.</span></span>

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

### <span data-ttu-id="9e15a-137">-Title</span><span class="sxs-lookup"><span data-stu-id="9e15a-137">-Title</span></span>
<span data-ttu-id="9e15a-138">이 cmdlet 집합의 제품 제목을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9e15a-138">Specifies the product title this cmdlet sets.</span></span>

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

### <span data-ttu-id="9e15a-139">-확인</span><span class="sxs-lookup"><span data-stu-id="9e15a-139">-Confirm</span></span>
<span data-ttu-id="9e15a-140">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9e15a-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e15a-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e15a-141">-WhatIf</span></span>
<span data-ttu-id="9e15a-142">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="9e15a-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9e15a-143">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9e15a-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e15a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e15a-144">CommonParameters</span></span>
<span data-ttu-id="9e15a-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9e15a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e15a-146">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9e15a-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e15a-147">입력</span><span class="sxs-lookup"><span data-stu-id="9e15a-147">INPUTS</span></span>

### <span data-ttu-id="9e15a-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9e15a-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9e15a-149">System.String</span><span class="sxs-lookup"><span data-stu-id="9e15a-149">System.String</span></span>

### <span data-ttu-id="9e15a-150">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9e15a-150">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="9e15a-151">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9e15a-151">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="9e15a-152">System.Nullable'1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="9e15a-152">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="9e15a-153">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9e15a-153">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9e15a-154">출력</span><span class="sxs-lookup"><span data-stu-id="9e15a-154">OUTPUTS</span></span>

### <span data-ttu-id="9e15a-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.psApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="9e15a-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="9e15a-156">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9e15a-156">NOTES</span></span>

## <span data-ttu-id="9e15a-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9e15a-157">RELATED LINKS</span></span>

[<span data-ttu-id="9e15a-158">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="9e15a-158">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="9e15a-159">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="9e15a-159">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="9e15a-160">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="9e15a-160">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)


