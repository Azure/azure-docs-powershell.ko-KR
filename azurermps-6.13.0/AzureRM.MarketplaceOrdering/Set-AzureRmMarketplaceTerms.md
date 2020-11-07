---
external help file: Microsoft.Azure.Commands.MarketplaceOrdering.dll-Help.xml
Module Name: AzureRM.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.marketplaceordering/set-azurermmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Set-AzureRmMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MarketplaceOrdering/Commands.MarketplaceOrdering/help/Set-AzureRmMarketplaceTerms.md
ms.openlocfilehash: 7932a733fcd672d8ee92e6452765745281ee0a2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702244"
---
# <span data-ttu-id="9d8f2-101">Set-AzureRmMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="9d8f2-101">Set-AzureRmMarketplaceTerms</span></span>

## <span data-ttu-id="9d8f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d8f2-102">SYNOPSIS</span></span>
<span data-ttu-id="9d8f2-103">지정 된 게시자 id (게시자), 제안 id (제품) 및 계획 id (이름)에 대 한 조건을 적용 하거나 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d8f2-103">Accept or reject terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="9d8f2-104">Get-AzureRmMarketplaceTerms를 사용 하 여 약관에 동의 하세요.</span><span class="sxs-lookup"><span data-stu-id="9d8f2-104">Please use Get-AzureRmMarketplaceTerms to get the agreement terms.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9d8f2-105">구문과</span><span class="sxs-lookup"><span data-stu-id="9d8f2-105">SYNTAX</span></span>

### <span data-ttu-id="9d8f2-106">AgreementAcceptParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="9d8f2-106">AgreementAcceptParameterSet (Default)</span></span>
```
Set-AzureRmMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Accept]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9d8f2-107">AgreementRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d8f2-107">AgreementRejectParameterSet</span></span>
```
Set-AzureRmMarketplaceTerms -Publisher <String> -Product <String> -Name <String> [-Reject]
 [-Terms <PSAgreementTerms>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9d8f2-108">InputObjectAcceptParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d8f2-108">InputObjectAcceptParameterSet</span></span>
```
Set-AzureRmMarketplaceTerms [-Accept] [-InputObject] <PSAgreementTerms>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d8f2-109">InputObjectRejectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d8f2-109">InputObjectRejectParameterSet</span></span>
```
Set-AzureRmMarketplaceTerms [-Reject] [-InputObject] <PSAgreementTerms>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d8f2-110">설명은</span><span class="sxs-lookup"><span data-stu-id="9d8f2-110">DESCRIPTION</span></span>
<span data-ttu-id="9d8f2-111">**AzureRmMarketplaceTerms** cmdlet은 지정 된 게시자 Id (게시자), 제안 Id (제품) 및 계획 Id (이름) 튜플에 대 한 약관 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d8f2-111">The **Set-AzureRmMarketplaceTerms** cmdlet saves the terms object for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="9d8f2-112">예제의</span><span class="sxs-lookup"><span data-stu-id="9d8f2-112">EXAMPLES</span></span>

### <span data-ttu-id="9d8f2-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="9d8f2-113">Example 1</span></span>
<span data-ttu-id="9d8f2-114">마켓플레이스 게시자 계약 받기</span><span class="sxs-lookup"><span data-stu-id="9d8f2-114">Get the marketplace publisher agreement</span></span>
```
PS C:\> Get-AzureRmMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" | Set-AzureRmMarketplaceTerms -Accept
```

### <span data-ttu-id="9d8f2-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="9d8f2-115">Example 2</span></span>
<span data-ttu-id="9d8f2-116">게시자 계약을 ' 수락 '으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d8f2-116">Set the publisher agreement to 'Accept'.</span></span> <span data-ttu-id="9d8f2-117">' AzureRmMarketplaceTerms ' cmdlet에서 ' 약관 ' 매개 변수에 대 한 값을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9d8f2-117">Get the value for the 'Terms' parameter from the 'Get-AzureRmMarketplaceTerms' cmdlet</span></span>
```
PS C:\> Set-AzureRmMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016" -Terms $agreementTerms -Accept
```


## <span data-ttu-id="9d8f2-118">변수</span><span class="sxs-lookup"><span data-stu-id="9d8f2-118">PARAMETERS</span></span>

### <span data-ttu-id="9d8f2-119">-수락</span><span class="sxs-lookup"><span data-stu-id="9d8f2-119">-Accept</span></span>
<span data-ttu-id="9d8f2-120">약관에 동의 하는 것으로 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d8f2-120">Pass this to accept the legal terms.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AgreementAcceptParameterSet, InputObjectAcceptParametrSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d8f2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d8f2-121">-DefaultProfile</span></span>
<span data-ttu-id="9d8f2-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9d8f2-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d8f2-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9d8f2-123">-InputObject</span></span>
<span data-ttu-id="9d8f2-124">Get-AzureRmMarketplaceTerms cmdlet에 약관 개체가 반환 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="9d8f2-124">Terms object returned in Get-AzureRmMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="9d8f2-125">허용 되는 매개 변수가 true 인 경우 이것은 필수 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="9d8f2-125">This is a mandatory parameter if Accepted paramter is true.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms
Parameter Sets: InputObjectAcceptParametrSet, InputObjectRejectParametrSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d8f2-126">-이름</span><span class="sxs-lookup"><span data-stu-id="9d8f2-126">-Name</span></span>
<span data-ttu-id="9d8f2-127">배포할 이미지의 계획 식별자 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="9d8f2-127">Plan identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="9d8f2-128">-제품</span><span class="sxs-lookup"><span data-stu-id="9d8f2-128">-Product</span></span>
<span data-ttu-id="9d8f2-129">배포 되는 이미지의 제공 식별자 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="9d8f2-129">Offer identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="9d8f2-130">-Publisher</span><span class="sxs-lookup"><span data-stu-id="9d8f2-130">-Publisher</span></span>
<span data-ttu-id="9d8f2-131">배포할 이미지의 게시자 식별자 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="9d8f2-131">Publisher identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="9d8f2-132">-거부</span><span class="sxs-lookup"><span data-stu-id="9d8f2-132">-Reject</span></span>
<span data-ttu-id="9d8f2-133">약관에 동의 하는 것을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d8f2-133">Pass this to reject the legal terms.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AgreementRejectParameterSet, InputObjectRejectParametrSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d8f2-134">-약관</span><span class="sxs-lookup"><span data-stu-id="9d8f2-134">-Terms</span></span>
<span data-ttu-id="9d8f2-135">Get-AzureRmMarketplaceTerms cmdlet에 약관 개체가 반환 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="9d8f2-135">Terms object returned in Get-AzureRmMarketplaceTerms cmdlet.</span></span> <span data-ttu-id="9d8f2-136">허용 되는 매개 변수가 true 인 경우 이것은 필수 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="9d8f2-136">This is a mandatory parameter if Accepted paramter is true.</span></span>

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

### <span data-ttu-id="9d8f2-137">-확인</span><span class="sxs-lookup"><span data-stu-id="9d8f2-137">-Confirm</span></span>
<span data-ttu-id="9d8f2-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d8f2-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d8f2-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d8f2-139">-WhatIf</span></span>
<span data-ttu-id="9d8f2-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9d8f2-140">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9d8f2-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9d8f2-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d8f2-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d8f2-142">CommonParameters</span></span>
<span data-ttu-id="9d8f2-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9d8f2-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d8f2-144">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d8f2-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d8f2-145">입력</span><span class="sxs-lookup"><span data-stu-id="9d8f2-145">INPUTS</span></span>

### <span data-ttu-id="9d8f2-146">MarketplaceOrdering. PSAgreementTerms/.</span><span class="sxs-lookup"><span data-stu-id="9d8f2-146">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>
<span data-ttu-id="9d8f2-147">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9d8f2-147">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="9d8f2-148">출력</span><span class="sxs-lookup"><span data-stu-id="9d8f2-148">OUTPUTS</span></span>

### <span data-ttu-id="9d8f2-149">MarketplaceOrdering. PSAgreementTerms/.</span><span class="sxs-lookup"><span data-stu-id="9d8f2-149">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="9d8f2-150">상속자</span><span class="sxs-lookup"><span data-stu-id="9d8f2-150">NOTES</span></span>

## <span data-ttu-id="9d8f2-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9d8f2-151">RELATED LINKS</span></span>
