---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MarketplaceOrdering.dll-Help.xml
Module Name: Az.MarketplaceOrdering
online version: https://docs.microsoft.com/powershell/module/az.marketplaceordering/get-azmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Get-AzMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Get-AzMarketplaceTerms.md
ms.openlocfilehash: 9878bdaa508d2cc229f494dcd53467f9c7d62ed1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965755"
---
# <span data-ttu-id="dcbf0-101">Get-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="dcbf0-101">Get-AzMarketplaceTerms</span></span>

## <span data-ttu-id="dcbf0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dcbf0-102">SYNOPSIS</span></span>
<span data-ttu-id="dcbf0-103">주어진 게시자 ID(Publisher), 제품 ID(제품) 및 계획 ID(이름)에 대한 계약 조건을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dcbf0-103">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="dcbf0-104">이 명령에서 반환되는 용어 개체는 법적 Set-AzMarketplaceTerms 전달해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcbf0-104">The terms object which is returned by this command should be passed to Set-AzMarketplaceTerms to accept the legal terms.</span></span>

## <span data-ttu-id="dcbf0-105">구문</span><span class="sxs-lookup"><span data-stu-id="dcbf0-105">SYNTAX</span></span>

```
Get-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dcbf0-106">설명</span><span class="sxs-lookup"><span data-stu-id="dcbf0-106">DESCRIPTION</span></span>
<span data-ttu-id="dcbf0-107">**Get-AzMarketplaceTerms** cmdlet은 주어진 게시자 ID(Publisher), 제품 ID(제품) 및 계획 ID(이름) 튜플에 대한 용어를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="dcbf0-107">The **Get-AzMarketplaceTerms** cmdlet returns terms for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="dcbf0-108">예제</span><span class="sxs-lookup"><span data-stu-id="dcbf0-108">EXAMPLES</span></span>

### <span data-ttu-id="dcbf0-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="dcbf0-109">Example 1</span></span>
```
PS C:\> Get-AzMarketplaceTerms -Publisher "microsoft-ads" -Product "windows-data-science-vm" -Name "windows2016"
Publisher         : microsoft-ads
Product           : windows-data-science-vm
Plan              : windows2016
LicenseTextLink   : <LicenseTextLink>
PrivacyPolicyLink : <PrivacyPolicyLink>
Signature         : <Signature>
Accepted          : True
RetrieveDatetime  : <RetrieveDatetime>
```

## <span data-ttu-id="dcbf0-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="dcbf0-110">PARAMETERS</span></span>

### <span data-ttu-id="dcbf0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcbf0-111">-DefaultProfile</span></span>
<span data-ttu-id="dcbf0-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dcbf0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dcbf0-113">-Name</span><span class="sxs-lookup"><span data-stu-id="dcbf0-113">-Name</span></span>
<span data-ttu-id="dcbf0-114">배포할 이미지의 식별자 문자열을 계획합니다.</span><span class="sxs-lookup"><span data-stu-id="dcbf0-114">Plan identifier string of image being deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcbf0-115">-Product</span><span class="sxs-lookup"><span data-stu-id="dcbf0-115">-Product</span></span>
<span data-ttu-id="dcbf0-116">배포되는 이미지의 식별자 문자열을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="dcbf0-116">Offer identifier string of image being deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcbf0-117">-Publisher</span><span class="sxs-lookup"><span data-stu-id="dcbf0-117">-Publisher</span></span>
<span data-ttu-id="dcbf0-118">배포되는 이미지의 게시자 식별자 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="dcbf0-118">Publisher identifier string of image being deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcbf0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcbf0-119">CommonParameters</span></span>
<span data-ttu-id="dcbf0-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="dcbf0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcbf0-121">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="dcbf0-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcbf0-122">입력</span><span class="sxs-lookup"><span data-stu-id="dcbf0-122">INPUTS</span></span>

### <span data-ttu-id="dcbf0-123">없음</span><span class="sxs-lookup"><span data-stu-id="dcbf0-123">None</span></span>

## <span data-ttu-id="dcbf0-124">출력</span><span class="sxs-lookup"><span data-stu-id="dcbf0-124">OUTPUTS</span></span>

### <span data-ttu-id="dcbf0-125">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="dcbf0-125">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="dcbf0-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="dcbf0-126">NOTES</span></span>

## <span data-ttu-id="dcbf0-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dcbf0-127">RELATED LINKS</span></span>
