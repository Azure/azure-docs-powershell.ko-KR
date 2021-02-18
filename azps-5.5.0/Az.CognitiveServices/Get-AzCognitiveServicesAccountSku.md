---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 386F09F0-2EEC-4B55-825C-F2E88D3B60AA
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountSku.md
ms.openlocfilehash: 3c632e6ffbf26e3aaacb725e9b663ffafbc49ec2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181769"
---
# <span data-ttu-id="7298c-101">Get-AzCognitiveServicesAccountSku</span><span class="sxs-lookup"><span data-stu-id="7298c-101">Get-AzCognitiveServicesAccountSku</span></span>

## <span data-ttu-id="7298c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7298c-102">SYNOPSIS</span></span>
<span data-ttu-id="7298c-103">계정에 사용 가능한 SKUS를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7298c-103">Gets the available SKUs for an account.</span></span>

## <span data-ttu-id="7298c-104">구문</span><span class="sxs-lookup"><span data-stu-id="7298c-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountSku [-Type <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7298c-105">설명</span><span class="sxs-lookup"><span data-stu-id="7298c-105">DESCRIPTION</span></span>
<span data-ttu-id="7298c-106">**Get-AzCognitiveServicesAccountSku** cmdlet은 Cognitive Services 계정에 사용 가능한 SKU를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7298c-106">The **Get-AzCognitiveServicesAccountSku** cmdlet gets the available SKUs for a Cognitive Services account.</span></span>
<span data-ttu-id="7298c-107">SKU는 계정에 대한 계층 계획입니다.</span><span class="sxs-lookup"><span data-stu-id="7298c-107">The SKU is the tier plan for an account.</span></span>
<span data-ttu-id="7298c-108">계정에 대한 가격, 호출 제한 및 요금을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="7298c-108">It defines the price, call limit, and rate for the account.</span></span>
<span data-ttu-id="7298c-109">F0 SKU는 무료 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="7298c-109">The F0 SKU is a free tier.</span></span>
<span data-ttu-id="7298c-110">유료 계층에는 S0, S1, S2 등이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="7298c-110">Paid tiers include S0, S1, S2, and so on.</span></span>

## <span data-ttu-id="7298c-111">예제</span><span class="sxs-lookup"><span data-stu-id="7298c-111">EXAMPLES</span></span>

### <span data-ttu-id="7298c-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="7298c-112">Example 1</span></span>
```powershell
PS C:\> (Get-AzCognitiveServicesAccountSku -Type 'TextAnalytics' -Location "westus").Value | Select-Object -E
xpandProperty Sku;

Name     Tier
----     ----
F0       Free
S0   Standard
```

## <span data-ttu-id="7298c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7298c-113">PARAMETERS</span></span>

### <span data-ttu-id="7298c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7298c-114">-DefaultProfile</span></span>
<span data-ttu-id="7298c-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7298c-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7298c-116">-Location</span><span class="sxs-lookup"><span data-stu-id="7298c-116">-Location</span></span>
<span data-ttu-id="7298c-117">Cognitive Services 계정 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="7298c-117">Cognitive Services Account Location.</span></span>

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

### <span data-ttu-id="7298c-118">-Type</span><span class="sxs-lookup"><span data-stu-id="7298c-118">-Type</span></span>
<span data-ttu-id="7298c-119">Cognitive Services 계정 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="7298c-119">Cognitive Services Account Type.</span></span>

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

### <span data-ttu-id="7298c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7298c-120">CommonParameters</span></span>
<span data-ttu-id="7298c-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7298c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7298c-122">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7298c-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7298c-123">입력</span><span class="sxs-lookup"><span data-stu-id="7298c-123">INPUTS</span></span>

### <span data-ttu-id="7298c-124">System.String</span><span class="sxs-lookup"><span data-stu-id="7298c-124">System.String</span></span>

## <span data-ttu-id="7298c-125">출력</span><span class="sxs-lookup"><span data-stu-id="7298c-125">OUTPUTS</span></span>

### <span data-ttu-id="7298c-126">Microsoft.Azure.Management.CognitiveServices.Models.ResourceSku</span><span class="sxs-lookup"><span data-stu-id="7298c-126">Microsoft.Azure.Management.CognitiveServices.Models.ResourceSku</span></span>

## <span data-ttu-id="7298c-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7298c-127">NOTES</span></span>

## <span data-ttu-id="7298c-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7298c-128">RELATED LINKS</span></span>
