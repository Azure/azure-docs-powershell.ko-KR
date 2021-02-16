---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MarketplaceOrdering.dll-Help.xml
Module Name: Az.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering/get-azmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Get-AzMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Get-AzMarketplaceTerms.md
ms.openlocfilehash: b729eb0ca1c0cc3b051600b59f260ebfb16d6b6e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180260"
---
# <span data-ttu-id="8b706-101">Get-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="8b706-101">Get-AzMarketplaceTerms</span></span>

## <span data-ttu-id="8b706-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b706-102">SYNOPSIS</span></span>
<span data-ttu-id="8b706-103">제공된 게시자 ID(게시자), 제품 ID(제품) 및 계획 ID(이름)에 대한 계약 조건을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8b706-103">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="8b706-104">이 명령에서 반환되는 용어 개체는 약관에 동의하기 위해 Set-AzMarketplaceTerms 전달해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b706-104">The terms object which is returned by this command should be passed to Set-AzMarketplaceTerms to accept the legal terms.</span></span>

## <span data-ttu-id="8b706-105">구문</span><span class="sxs-lookup"><span data-stu-id="8b706-105">SYNTAX</span></span>

```
Get-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b706-106">설명</span><span class="sxs-lookup"><span data-stu-id="8b706-106">DESCRIPTION</span></span>
<span data-ttu-id="8b706-107">**Get-AzMarketplaceTerms** cmdlet은 제공된 게시자 ID(게시자), 제품 ID(제품) 및 계획 ID(이름) 튜플에 대한 용어를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="8b706-107">The **Get-AzMarketplaceTerms** cmdlet returns terms for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="8b706-108">예제</span><span class="sxs-lookup"><span data-stu-id="8b706-108">EXAMPLES</span></span>

### <span data-ttu-id="8b706-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="8b706-109">Example 1</span></span>
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

## <span data-ttu-id="8b706-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b706-110">PARAMETERS</span></span>

### <span data-ttu-id="8b706-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b706-111">-DefaultProfile</span></span>
<span data-ttu-id="8b706-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8b706-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b706-113">-Name</span><span class="sxs-lookup"><span data-stu-id="8b706-113">-Name</span></span>
<span data-ttu-id="8b706-114">배포되는 이미지의 계획 식별자 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="8b706-114">Plan identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="8b706-115">-Product</span><span class="sxs-lookup"><span data-stu-id="8b706-115">-Product</span></span>
<span data-ttu-id="8b706-116">배포되는 이미지의 제품 식별자 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="8b706-116">Offer identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="8b706-117">-Publisher</span><span class="sxs-lookup"><span data-stu-id="8b706-117">-Publisher</span></span>
<span data-ttu-id="8b706-118">배포되는 이미지의 게시자 식별자 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="8b706-118">Publisher identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="8b706-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b706-119">CommonParameters</span></span>
<span data-ttu-id="8b706-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8b706-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b706-121">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8b706-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b706-122">입력</span><span class="sxs-lookup"><span data-stu-id="8b706-122">INPUTS</span></span>

### <span data-ttu-id="8b706-123">없음</span><span class="sxs-lookup"><span data-stu-id="8b706-123">None</span></span>

## <span data-ttu-id="8b706-124">출력</span><span class="sxs-lookup"><span data-stu-id="8b706-124">OUTPUTS</span></span>

### <span data-ttu-id="8b706-125">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span><span class="sxs-lookup"><span data-stu-id="8b706-125">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="8b706-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8b706-126">NOTES</span></span>

## <span data-ttu-id="8b706-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8b706-127">RELATED LINKS</span></span>