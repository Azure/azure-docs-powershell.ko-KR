---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 386F09F0-2EEC-4B55-825C-F2E88D3B60AA
online version: https://docs.microsoft.com/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountSku.md
ms.openlocfilehash: eb9865d69d51fffc7488379bada256a812503a24
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981227"
---
# <span data-ttu-id="05b6b-101">Get-AzCognitiveServicesAccountSku</span><span class="sxs-lookup"><span data-stu-id="05b6b-101">Get-AzCognitiveServicesAccountSku</span></span>

## <span data-ttu-id="05b6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05b6b-102">SYNOPSIS</span></span>
<span data-ttu-id="05b6b-103">계정에 사용할 수 있는 SKUS를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="05b6b-103">Gets the available SKUs for an account.</span></span>

## <span data-ttu-id="05b6b-104">구문</span><span class="sxs-lookup"><span data-stu-id="05b6b-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountSku [-Type <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="05b6b-105">설명</span><span class="sxs-lookup"><span data-stu-id="05b6b-105">DESCRIPTION</span></span>
<span data-ttu-id="05b6b-106">**Get-AzCognitiveServicesAccountSku** cmdlet은 Cognitive Services 계정에 사용할 수 있는 SKU를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="05b6b-106">The **Get-AzCognitiveServicesAccountSku** cmdlet gets the available SKUs for a Cognitive Services account.</span></span>
<span data-ttu-id="05b6b-107">SKU는 계정에 대한 계층 계획입니다.</span><span class="sxs-lookup"><span data-stu-id="05b6b-107">The SKU is the tier plan for an account.</span></span>
<span data-ttu-id="05b6b-108">계정의 가격, 통화 한도 및 비율을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="05b6b-108">It defines the price, call limit, and rate for the account.</span></span>
<span data-ttu-id="05b6b-109">F0 SKU는 무료 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="05b6b-109">The F0 SKU is a free tier.</span></span>
<span data-ttu-id="05b6b-110">유료 계층에는 S0, S1, S2가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="05b6b-110">Paid tiers include S0, S1, S2, and so on.</span></span>

## <span data-ttu-id="05b6b-111">예제</span><span class="sxs-lookup"><span data-stu-id="05b6b-111">EXAMPLES</span></span>

### <span data-ttu-id="05b6b-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="05b6b-112">Example 1</span></span>
```powershell
PS C:\> (Get-AzCognitiveServicesAccountSku -Type 'TextAnalytics' -Location "westus").Value | Select-Object -E
xpandProperty Sku;

Name     Tier
----     ----
F0       Free
S0   Standard
```

## <span data-ttu-id="05b6b-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="05b6b-113">PARAMETERS</span></span>

### <span data-ttu-id="05b6b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05b6b-114">-DefaultProfile</span></span>
<span data-ttu-id="05b6b-115">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="05b6b-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="05b6b-116">-Location</span><span class="sxs-lookup"><span data-stu-id="05b6b-116">-Location</span></span>
<span data-ttu-id="05b6b-117">Cognitive Services 계정 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="05b6b-117">Cognitive Services Account Location.</span></span>

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

### <span data-ttu-id="05b6b-118">-Type</span><span class="sxs-lookup"><span data-stu-id="05b6b-118">-Type</span></span>
<span data-ttu-id="05b6b-119">Cognitive Services 계정 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="05b6b-119">Cognitive Services Account Type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountType, AccountType, Kind

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05b6b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05b6b-120">CommonParameters</span></span>
<span data-ttu-id="05b6b-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="05b6b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05b6b-122">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="05b6b-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05b6b-123">입력</span><span class="sxs-lookup"><span data-stu-id="05b6b-123">INPUTS</span></span>

### <span data-ttu-id="05b6b-124">System.String</span><span class="sxs-lookup"><span data-stu-id="05b6b-124">System.String</span></span>

## <span data-ttu-id="05b6b-125">출력</span><span class="sxs-lookup"><span data-stu-id="05b6b-125">OUTPUTS</span></span>

### <span data-ttu-id="05b6b-126">Microsoft.Azure.Management.CognitiveServices.Models.ResourceSku</span><span class="sxs-lookup"><span data-stu-id="05b6b-126">Microsoft.Azure.Management.CognitiveServices.Models.ResourceSku</span></span>

## <span data-ttu-id="05b6b-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="05b6b-127">NOTES</span></span>

## <span data-ttu-id="05b6b-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="05b6b-128">RELATED LINKS</span></span>
