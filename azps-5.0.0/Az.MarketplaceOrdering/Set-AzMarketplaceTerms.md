---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MarketplaceOrdering.dll-Help.xml
Module Name: Az.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering/set-azmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Set-AzMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Set-AzMarketplaceTerms.md
ms.openlocfilehash: fb40d1c103da1cc9f1cfe306ebdaab5abf6ec316
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226805"
---
# <span data-ttu-id="50295-101">Set-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="50295-101">Set-AzMarketplaceTerms</span></span>

## <span data-ttu-id="50295-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50295-102">SYNOPSIS</span></span>
<span data-ttu-id="50295-103">지정 된 게시자 id (게시자), 제안 id (제품) 및 계획 id (이름)에 대 한 조건을 적용 하거나 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="50295-103">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="50295-104">Get-AzMarketplaceTerms를 사용 하 여 약관에 동의 하세요.</span><span class="sxs-lookup"><span data-stu-id="50295-104">Please use Get-AzMarketplaceTerms to get the agreement terms.</span></span>

## <span data-ttu-id="50295-105">구문과</span><span class="sxs-lookup"><span data-stu-id="50295-105">SYNTAX</span></span>

### <span data-ttu-id="50295-106">AgreementAcceptParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="50295-106">AgreementAcceptParameterSet (Default)</span></span>
```
Set-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Accept]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="50295-107">AgreementRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="50295-107">AgreementRejectParameterSet</span></span>
```
Set-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Reject]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="50295-108">InputObjectAcceptParameterSet</span><span class="sxs-lookup"><span data-stu-id="50295-108">InputObjectAcceptParameterSet</span></span>
```
Set-AzMarketplaceTerms [-Accept] [-InputObject] <PSAgreementTerms> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50295-109">InputObjectRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="50295-109">InputObjectRejectParameterSet</span></span>
```
Set-AzMarketplaceTerms [-Reject] [-InputObject] <PSAgreementTerms> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50295-110">설명은</span><span class="sxs-lookup"><span data-stu-id="50295-110">DESCRIPTION</span></span>
<span data-ttu-id="50295-111">**AzMarketplaceTerms** cmdlet은 지정 된 게시자 Id (게시자), 제안 Id (제품) 및 계획 Id (이름) 튜플에 대 한 약관 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="50295-111">The **Set-AzMarketplaceTerms** cmdlet saves the terms object for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="50295-112">예제의</span><span class="sxs-lookup"><span data-stu-id="50295-112">EXAMPLES</span></span>

### <span data-ttu-id="50295-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="50295-113">Example 1</span></span>
<span data-ttu-id="50295-114">마켓플레이스 게시자 계약 받기</span><span class="sxs-lookup"><span data-stu-id="50295-114">Get the marketplace publisher agreement</span></span>


```
PS C:\> Get-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" | Set-AzMarketplaceTerms -Accept
```

### <span data-ttu-id="50295-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="50295-115">Example 2</span></span>
<span data-ttu-id="50295-116">게시자 계약을 ' 수락 '으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="50295-116">Set the publisher agreement to 'Accept'.</span></span> <span data-ttu-id="50295-117">' AzMarketplaceTerms ' cmdlet에서 ' 약관 ' 매개 변수에 대 한 값을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="50295-117">Get the value for the 'Terms' parameter from the 'Get-AzMarketplaceTerms' cmdlet</span></span>


```
PS C:\> Set-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" -Terms $agreementTerms -Accept
```

## <span data-ttu-id="50295-118">변수</span><span class="sxs-lookup"><span data-stu-id="50295-118">PARAMETERS</span></span>

### <span data-ttu-id="50295-119">-수락</span><span class="sxs-lookup"><span data-stu-id="50295-119">-Accept</span></span>
<span data-ttu-id="50295-120">약관에 동의 하는 것으로 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="50295-120">Pass this to accept the legal terms.</span></span>

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

### <span data-ttu-id="50295-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50295-121">-DefaultProfile</span></span>
<span data-ttu-id="50295-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="50295-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50295-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="50295-123">-InputObject</span></span>
<span data-ttu-id="50295-124">Get-AzMarketplaceTerms cmdlet에 약관 개체가 반환 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="50295-124">Terms object returned in Get-AzMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="50295-125">허용 되는 매개 변수가 true 인 경우 필수 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="50295-125">This is a mandatory parameter if Accepted parameter is true.</span></span>

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

### <span data-ttu-id="50295-126">-이름</span><span class="sxs-lookup"><span data-stu-id="50295-126">-Name</span></span>
<span data-ttu-id="50295-127">배포할 이미지의 계획 식별자 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="50295-127">Plan identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="50295-128">-제품</span><span class="sxs-lookup"><span data-stu-id="50295-128">-Product</span></span>
<span data-ttu-id="50295-129">배포 되는 이미지의 제공 식별자 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="50295-129">Offer identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="50295-130">-Publisher</span><span class="sxs-lookup"><span data-stu-id="50295-130">-Publisher</span></span>
<span data-ttu-id="50295-131">배포할 이미지의 게시자 식별자 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="50295-131">Publisher identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="50295-132">-거부</span><span class="sxs-lookup"><span data-stu-id="50295-132">-Reject</span></span>
<span data-ttu-id="50295-133">약관에 동의 하는 것을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="50295-133">Pass this to reject the legal terms.</span></span>

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

### <span data-ttu-id="50295-134">-약관</span><span class="sxs-lookup"><span data-stu-id="50295-134">-Terms</span></span>
<span data-ttu-id="50295-135">Get-AzMarketplaceTerms cmdlet에 약관 개체가 반환 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="50295-135">Terms object returned in Get-AzMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="50295-136">허용 되는 매개 변수가 true 인 경우 필수 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="50295-136">This is a mandatory parameter if Accepted parameter is true.</span></span>

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

### <span data-ttu-id="50295-137">-확인</span><span class="sxs-lookup"><span data-stu-id="50295-137">-Confirm</span></span>
<span data-ttu-id="50295-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="50295-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50295-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50295-139">-WhatIf</span></span>
<span data-ttu-id="50295-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="50295-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="50295-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="50295-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50295-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50295-142">CommonParameters</span></span>
<span data-ttu-id="50295-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="50295-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50295-144">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50295-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50295-145">입력</span><span class="sxs-lookup"><span data-stu-id="50295-145">INPUTS</span></span>

### <span data-ttu-id="50295-146">MarketplaceOrdering. PSAgreementTerms/.</span><span class="sxs-lookup"><span data-stu-id="50295-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="50295-147">출력</span><span class="sxs-lookup"><span data-stu-id="50295-147">OUTPUTS</span></span>

### <span data-ttu-id="50295-148">MarketplaceOrdering. PSAgreementTerms/.</span><span class="sxs-lookup"><span data-stu-id="50295-148">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="50295-149">상속자</span><span class="sxs-lookup"><span data-stu-id="50295-149">NOTES</span></span>

## <span data-ttu-id="50295-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="50295-150">RELATED LINKS</span></span>
