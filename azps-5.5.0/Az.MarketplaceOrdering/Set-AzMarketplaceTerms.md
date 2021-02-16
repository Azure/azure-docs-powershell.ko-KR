---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MarketplaceOrdering.dll-Help.xml
Module Name: Az.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering/set-azmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Set-AzMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Set-AzMarketplaceTerms.md
ms.openlocfilehash: fb40d1c103da1cc9f1cfe306ebdaab5abf6ec316
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180257"
---
# <span data-ttu-id="aaaba-101">Set-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="aaaba-101">Set-AzMarketplaceTerms</span></span>

## <span data-ttu-id="aaaba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aaaba-102">SYNOPSIS</span></span>
<span data-ttu-id="aaaba-103">제공된 게시자 ID(퍼블리셔), 제품 ID(제품) 및 계획 ID(이름)에 대한 약관에 동의하거나 거부합니다.</span><span class="sxs-lookup"><span data-stu-id="aaaba-103">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="aaaba-104">계약 조건을 Get-AzMarketplaceTerms 사용하시기 바랍니다.</span><span class="sxs-lookup"><span data-stu-id="aaaba-104">Please use Get-AzMarketplaceTerms to get the agreement terms.</span></span>

## <span data-ttu-id="aaaba-105">구문</span><span class="sxs-lookup"><span data-stu-id="aaaba-105">SYNTAX</span></span>

### <span data-ttu-id="aaaba-106">AgreementAcceptParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="aaaba-106">AgreementAcceptParameterSet (Default)</span></span>
```
Set-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Accept]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aaaba-107">AgreementRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aaaba-107">AgreementRejectParameterSet</span></span>
```
Set-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Reject]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aaaba-108">InputObjectAcceptParameterSet</span><span class="sxs-lookup"><span data-stu-id="aaaba-108">InputObjectAcceptParameterSet</span></span>
```
Set-AzMarketplaceTerms [-Accept] [-InputObject] <PSAgreementTerms> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aaaba-109">InputObjectRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="aaaba-109">InputObjectRejectParameterSet</span></span>
```
Set-AzMarketplaceTerms [-Reject] [-InputObject] <PSAgreementTerms> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aaaba-110">설명</span><span class="sxs-lookup"><span data-stu-id="aaaba-110">DESCRIPTION</span></span>
<span data-ttu-id="aaaba-111">**Set-AzMarketplaceTerms** cmdlet은 제공된 게시자 ID(게시자), 제품 ID(제품) 및 계획 ID(이름) 튜플에 대한 용어 개체를 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="aaaba-111">The **Set-AzMarketplaceTerms** cmdlet saves the terms object for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="aaaba-112">예제</span><span class="sxs-lookup"><span data-stu-id="aaaba-112">EXAMPLES</span></span>

### <span data-ttu-id="aaaba-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="aaaba-113">Example 1</span></span>
<span data-ttu-id="aaaba-114">마켓플레이스 게시자 계약을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="aaaba-114">Get the marketplace publisher agreement</span></span>


```
PS C:\> Get-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" | Set-AzMarketplaceTerms -Accept
```

### <span data-ttu-id="aaaba-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="aaaba-115">Example 2</span></span>
<span data-ttu-id="aaaba-116">게시자 계약을 '수락'으로 설정</span><span class="sxs-lookup"><span data-stu-id="aaaba-116">Set the publisher agreement to 'Accept'.</span></span> <span data-ttu-id="aaaba-117">'Get-AzMarketplaceTerms' cmdlet에서 'Terms' 매개 변수의 값을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="aaaba-117">Get the value for the 'Terms' parameter from the 'Get-AzMarketplaceTerms' cmdlet</span></span>


```
PS C:\> Set-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" -Terms $agreementTerms -Accept
```

## <span data-ttu-id="aaaba-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aaaba-118">PARAMETERS</span></span>

### <span data-ttu-id="aaaba-119">-Accept</span><span class="sxs-lookup"><span data-stu-id="aaaba-119">-Accept</span></span>
<span data-ttu-id="aaaba-120">약관에 동의하기 위해 이 계약을 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="aaaba-120">Pass this to accept the legal terms.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AgreementAcceptParameterSet, InputObjectAcceptParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaaba-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaaba-121">-DefaultProfile</span></span>
<span data-ttu-id="aaaba-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aaaba-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aaaba-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aaaba-123">-InputObject</span></span>
<span data-ttu-id="aaaba-124">Get-AzMarketplaceTerms cmdlet에서 반환된 용어 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="aaaba-124">Terms object returned in Get-AzMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="aaaba-125">수락 매개 변수가 true인 경우 필수 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="aaaba-125">This is a mandatory parameter if Accepted parameter is true.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms
Parameter Sets: InputObjectAcceptParameterSet, InputObjectRejectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="aaaba-126">-Name</span><span class="sxs-lookup"><span data-stu-id="aaaba-126">-Name</span></span>
<span data-ttu-id="aaaba-127">배포되는 이미지의 계획 식별자 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="aaaba-127">Plan identifier string of image being deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaaba-128">-Product</span><span class="sxs-lookup"><span data-stu-id="aaaba-128">-Product</span></span>
<span data-ttu-id="aaaba-129">배포되는 이미지의 제품 식별자 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="aaaba-129">Offer identifier string of image being deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaaba-130">-Publisher</span><span class="sxs-lookup"><span data-stu-id="aaaba-130">-Publisher</span></span>
<span data-ttu-id="aaaba-131">배포되는 이미지의 게시자 식별자 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="aaaba-131">Publisher identifier string of image being deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaaba-132">-Reject</span><span class="sxs-lookup"><span data-stu-id="aaaba-132">-Reject</span></span>
<span data-ttu-id="aaaba-133">약관을 거부하기 위해 이를 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="aaaba-133">Pass this to reject the legal terms.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AgreementRejectParameterSet, InputObjectRejectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaaba-134">-Terms</span><span class="sxs-lookup"><span data-stu-id="aaaba-134">-Terms</span></span>
<span data-ttu-id="aaaba-135">Get-AzMarketplaceTerms cmdlet에서 반환된 용어 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="aaaba-135">Terms object returned in Get-AzMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="aaaba-136">수락 매개 변수가 true인 경우 필수 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="aaaba-136">This is a mandatory parameter if Accepted parameter is true.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms
Parameter Sets: AgreementAcceptParameterSet, AgreementRejectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aaaba-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aaaba-137">-Confirm</span></span>
<span data-ttu-id="aaaba-138">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="aaaba-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aaaba-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aaaba-139">-WhatIf</span></span>
<span data-ttu-id="aaaba-140">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="aaaba-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aaaba-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aaaba-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aaaba-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaaba-142">CommonParameters</span></span>
<span data-ttu-id="aaaba-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="aaaba-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaaba-144">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="aaaba-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaaba-145">입력</span><span class="sxs-lookup"><span data-stu-id="aaaba-145">INPUTS</span></span>

### <span data-ttu-id="aaaba-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="aaaba-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="aaaba-147">출력</span><span class="sxs-lookup"><span data-stu-id="aaaba-147">OUTPUTS</span></span>

### <span data-ttu-id="aaaba-148">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="aaaba-148">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="aaaba-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="aaaba-149">NOTES</span></span>

## <span data-ttu-id="aaaba-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aaaba-150">RELATED LINKS</span></span>
