---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MarketplaceOrdering.dll-Help.xml
Module Name: Az.MarketplaceOrdering
online version: https://docs.microsoft.com/en-us/powershell/module/az.marketplaceordering/get-azmarketplaceterms
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Get-AzMarketplaceTerms.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MarketplaceOrdering/MarketplaceOrdering/help/Get-AzMarketplaceTerms.md
ms.openlocfilehash: b729eb0ca1c0cc3b051600b59f260ebfb16d6b6e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213518"
---
# <span data-ttu-id="db6a7-101">Get-AzMarketplaceTerms</span><span class="sxs-lookup"><span data-stu-id="db6a7-101">Get-AzMarketplaceTerms</span></span>

## <span data-ttu-id="db6a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db6a7-102">SYNOPSIS</span></span>
<span data-ttu-id="db6a7-103">지정 된 게시자 id (게시자), 제안 id (제품) 및 계획 id (이름)에 대 한 계약 조건을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="db6a7-103">Get the agreement terms for a given publisher id(Publisher), offer id(Product) and plan id(Name).</span></span> <span data-ttu-id="db6a7-104">이 명령으로 반환 되는 약관 개체는 약관에 동의 하도록 Set-AzMarketplaceTerms에 전달 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="db6a7-104">The terms object which is returned by this command should be passed to Set-AzMarketplaceTerms to accept the legal terms.</span></span>

## <span data-ttu-id="db6a7-105">구문과</span><span class="sxs-lookup"><span data-stu-id="db6a7-105">SYNTAX</span></span>

```
Get-AzMarketplaceTerms -Publisher <String> -Product <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db6a7-106">설명은</span><span class="sxs-lookup"><span data-stu-id="db6a7-106">DESCRIPTION</span></span>
<span data-ttu-id="db6a7-107">**AzMarketplaceTerms** cmdlet은 지정 된 게시자 Id (게시자), 제안 Id (제품) 및 계획 Id (이름) 튜플의 조건을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="db6a7-107">The **Get-AzMarketplaceTerms** cmdlet returns terms for given publisher id(Publisher), offer id(Product) and plan id(Name) tuple.</span></span>

## <span data-ttu-id="db6a7-108">예제의</span><span class="sxs-lookup"><span data-stu-id="db6a7-108">EXAMPLES</span></span>

### <span data-ttu-id="db6a7-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="db6a7-109">Example 1</span></span>
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

## <span data-ttu-id="db6a7-110">변수</span><span class="sxs-lookup"><span data-stu-id="db6a7-110">PARAMETERS</span></span>

### <span data-ttu-id="db6a7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db6a7-111">-DefaultProfile</span></span>
<span data-ttu-id="db6a7-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="db6a7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db6a7-113">-이름</span><span class="sxs-lookup"><span data-stu-id="db6a7-113">-Name</span></span>
<span data-ttu-id="db6a7-114">배포할 이미지의 계획 식별자 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="db6a7-114">Plan identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="db6a7-115">-제품</span><span class="sxs-lookup"><span data-stu-id="db6a7-115">-Product</span></span>
<span data-ttu-id="db6a7-116">배포 되는 이미지의 제공 식별자 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="db6a7-116">Offer identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="db6a7-117">-Publisher</span><span class="sxs-lookup"><span data-stu-id="db6a7-117">-Publisher</span></span>
<span data-ttu-id="db6a7-118">배포할 이미지의 게시자 식별자 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="db6a7-118">Publisher identifier string of image being deployed.</span></span>

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

### <span data-ttu-id="db6a7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db6a7-119">CommonParameters</span></span>
<span data-ttu-id="db6a7-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="db6a7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db6a7-121">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db6a7-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db6a7-122">입력</span><span class="sxs-lookup"><span data-stu-id="db6a7-122">INPUTS</span></span>

### <span data-ttu-id="db6a7-123">않아야</span><span class="sxs-lookup"><span data-stu-id="db6a7-123">None</span></span>

## <span data-ttu-id="db6a7-124">출력</span><span class="sxs-lookup"><span data-stu-id="db6a7-124">OUTPUTS</span></span>

### <span data-ttu-id="db6a7-125">MarketplaceOrdering. PSAgreementTerms/.</span><span class="sxs-lookup"><span data-stu-id="db6a7-125">Microsoft.Azure.Commands.MarketplaceOrdering.Models.PSAgreementTerms</span></span>

## <span data-ttu-id="db6a7-126">상속자</span><span class="sxs-lookup"><span data-stu-id="db6a7-126">NOTES</span></span>

## <span data-ttu-id="db6a7-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="db6a7-127">RELATED LINKS</span></span>
