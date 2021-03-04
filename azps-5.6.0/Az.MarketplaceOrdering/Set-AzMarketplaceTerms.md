---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MarketplaceOrdering.dll-Help.xml
Module Name: Az.MarketplaceOrdering
online version: https://docs.microsoft.com/powershell/module/az.marketplaceordering/set-azmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Set-AzMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Set-AzMarketplaceTerms.md
ms.openlocfilehash: b4098481db78bf045abad04aee4e2e5076f71ce1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952331"
---
# <span data-ttu-id="33e9a-101">Set-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="33e9a-101">Set-AzMarketplaceTerms</span></span>

## <span data-ttu-id="33e9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33e9a-102">SYNOPSIS</span></span>
<span data-ttu-id="33e9a-103">주어진 게시자 ID(게시자), 제품 ID(제품) 및 계획 ID(이름)에 대한 약관을 수락하거나 거부합니다.</span><span class="sxs-lookup"><span data-stu-id="33e9a-103">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="33e9a-104">계약 조건을 Get-AzMarketplaceTerms 사용하시기 바랍니다.</span><span class="sxs-lookup"><span data-stu-id="33e9a-104">Please use Get-AzMarketplaceTerms to get the agreement terms.</span></span>

## <span data-ttu-id="33e9a-105">구문</span><span class="sxs-lookup"><span data-stu-id="33e9a-105">SYNTAX</span></span>

### <span data-ttu-id="33e9a-106">AgreementAcceptParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="33e9a-106">AgreementAcceptParameterSet (Default)</span></span>
```
Set-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Accept]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="33e9a-107">AgreementRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="33e9a-107">AgreementRejectParameterSet</span></span>
```
Set-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Reject]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="33e9a-108">InputObjectAcceptParameterSet</span><span class="sxs-lookup"><span data-stu-id="33e9a-108">InputObjectAcceptParameterSet</span></span>
```
Set-AzMarketplaceTerms [-Accept] [-InputObject] <PSAgreementTerms> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33e9a-109">InputObjectRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="33e9a-109">InputObjectRejectParameterSet</span></span>
```
Set-AzMarketplaceTerms [-Reject] [-InputObject] <PSAgreementTerms> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33e9a-110">설명</span><span class="sxs-lookup"><span data-stu-id="33e9a-110">DESCRIPTION</span></span>
<span data-ttu-id="33e9a-111">**Set-AzMarketplaceTerms** cmdlet은 주어진 게시자 ID(Publisher), 제품 ID(제품) 및 계획 ID(이름) 튜플에 대한 용어 개체를 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="33e9a-111">The **Set-AzMarketplaceTerms** cmdlet saves the terms object for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="33e9a-112">예제</span><span class="sxs-lookup"><span data-stu-id="33e9a-112">EXAMPLES</span></span>

### <span data-ttu-id="33e9a-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="33e9a-113">Example 1</span></span>
<span data-ttu-id="33e9a-114">마켓플레이스 퍼블리셔 계약을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="33e9a-114">Get the marketplace publisher agreement</span></span>


```
PS C:\> Get-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" | Set-AzMarketplaceTerms -Accept
```

### <span data-ttu-id="33e9a-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="33e9a-115">Example 2</span></span>
<span data-ttu-id="33e9a-116">게시자 계약을 '수락'으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="33e9a-116">Set the publisher agreement to 'Accept'.</span></span> <span data-ttu-id="33e9a-117">'Get-AzMarketplaceTerms' cmdlet에서 'Terms' 매개 변수의 값을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="33e9a-117">Get the value for the 'Terms' parameter from the 'Get-AzMarketplaceTerms' cmdlet</span></span>


```
PS C:\> Set-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" -Terms $agreementTerms -Accept
```

## <span data-ttu-id="33e9a-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="33e9a-118">PARAMETERS</span></span>

### <span data-ttu-id="33e9a-119">-Accept</span><span class="sxs-lookup"><span data-stu-id="33e9a-119">-Accept</span></span>
<span data-ttu-id="33e9a-120">이를 전달하여 법적 용어에 동의합니다.</span><span class="sxs-lookup"><span data-stu-id="33e9a-120">Pass this to accept the legal terms.</span></span>

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

### <span data-ttu-id="33e9a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33e9a-121">-DefaultProfile</span></span>
<span data-ttu-id="33e9a-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="33e9a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33e9a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="33e9a-123">-InputObject</span></span>
<span data-ttu-id="33e9a-124">Get-AzMarketplaceTerms cmdlet에서 반환되는 용어 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="33e9a-124">Terms object returned in Get-AzMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="33e9a-125">수락 매개 변수가 true인 경우 필수 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="33e9a-125">This is a mandatory parameter if Accepted parameter is true.</span></span>

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

### <span data-ttu-id="33e9a-126">-Name</span><span class="sxs-lookup"><span data-stu-id="33e9a-126">-Name</span></span>
<span data-ttu-id="33e9a-127">배포할 이미지의 식별자 문자열을 계획합니다.</span><span class="sxs-lookup"><span data-stu-id="33e9a-127">Plan identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="33e9a-128">-Product</span><span class="sxs-lookup"><span data-stu-id="33e9a-128">-Product</span></span>
<span data-ttu-id="33e9a-129">배포되는 이미지의 식별자 문자열을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="33e9a-129">Offer identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="33e9a-130">-Publisher</span><span class="sxs-lookup"><span data-stu-id="33e9a-130">-Publisher</span></span>
<span data-ttu-id="33e9a-131">배포되는 이미지의 게시자 식별자 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="33e9a-131">Publisher identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="33e9a-132">-Reject</span><span class="sxs-lookup"><span data-stu-id="33e9a-132">-Reject</span></span>
<span data-ttu-id="33e9a-133">이를 전달하여 법적 용어를 거부합니다.</span><span class="sxs-lookup"><span data-stu-id="33e9a-133">Pass this to reject the legal terms.</span></span>

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

### <span data-ttu-id="33e9a-134">-Terms</span><span class="sxs-lookup"><span data-stu-id="33e9a-134">-Terms</span></span>
<span data-ttu-id="33e9a-135">Get-AzMarketplaceTerms cmdlet에서 반환되는 용어 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="33e9a-135">Terms object returned in Get-AzMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="33e9a-136">수락 매개 변수가 true인 경우 필수 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="33e9a-136">This is a mandatory parameter if Accepted parameter is true.</span></span>

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

### <span data-ttu-id="33e9a-137">-확인</span><span class="sxs-lookup"><span data-stu-id="33e9a-137">-Confirm</span></span>
<span data-ttu-id="33e9a-138">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="33e9a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33e9a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33e9a-139">-WhatIf</span></span>
<span data-ttu-id="33e9a-140">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="33e9a-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="33e9a-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="33e9a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33e9a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33e9a-142">CommonParameters</span></span>
<span data-ttu-id="33e9a-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="33e9a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33e9a-144">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="33e9a-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33e9a-145">입력</span><span class="sxs-lookup"><span data-stu-id="33e9a-145">INPUTS</span></span>

### <span data-ttu-id="33e9a-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="33e9a-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="33e9a-147">출력</span><span class="sxs-lookup"><span data-stu-id="33e9a-147">OUTPUTS</span></span>

### <span data-ttu-id="33e9a-148">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="33e9a-148">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="33e9a-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="33e9a-149">NOTES</span></span>

## <span data-ttu-id="33e9a-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="33e9a-150">RELATED LINKS</span></span>
