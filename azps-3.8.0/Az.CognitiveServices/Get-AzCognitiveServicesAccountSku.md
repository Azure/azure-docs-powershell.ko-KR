---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CognitiveServices.dll-Help.xml
Module Name: Az.CognitiveServices
ms.assetid: 386F09F0-2EEC-4B55-825C-F2E88D3B60AA
online version: https://docs.microsoft.com/en-us/powershell/module/az.cognitiveservices/get-azcognitiveservicesaccountsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CognitiveServices/CognitiveServices/help/Get-AzCognitiveServicesAccountSku.md
ms.openlocfilehash: 3c632e6ffbf26e3aaacb725e9b663ffafbc49ec2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94033777"
---
# <span data-ttu-id="caf19-101">Get-AzCognitiveServicesAccountSku</span><span class="sxs-lookup"><span data-stu-id="caf19-101">Get-AzCognitiveServicesAccountSku</span></span>

## <span data-ttu-id="caf19-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="caf19-102">SYNOPSIS</span></span>
<span data-ttu-id="caf19-103">계정에 사용할 수 있는 Sku를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="caf19-103">Gets the available SKUs for an account.</span></span>

## <span data-ttu-id="caf19-104">구문과</span><span class="sxs-lookup"><span data-stu-id="caf19-104">SYNTAX</span></span>

```
Get-AzCognitiveServicesAccountSku [-Type <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="caf19-105">설명은</span><span class="sxs-lookup"><span data-stu-id="caf19-105">DESCRIPTION</span></span>
<span data-ttu-id="caf19-106">**AzCognitiveServicesAccountSku** Cmdlet은 인식 서비스 계정에 사용할 수 있는 sku를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="caf19-106">The **Get-AzCognitiveServicesAccountSku** cmdlet gets the available SKUs for a Cognitive Services account.</span></span>
<span data-ttu-id="caf19-107">SKU는 거래처에 대 한 계층 계획입니다.</span><span class="sxs-lookup"><span data-stu-id="caf19-107">The SKU is the tier plan for an account.</span></span>
<span data-ttu-id="caf19-108">계정에 대 한 가격, 통화 제한 및 요금을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="caf19-108">It defines the price, call limit, and rate for the account.</span></span>
<span data-ttu-id="caf19-109">F0 SKU는 무료 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="caf19-109">The F0 SKU is a free tier.</span></span>
<span data-ttu-id="caf19-110">유료 계층에는 S0, S1, S2 등이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="caf19-110">Paid tiers include S0, S1, S2, and so on.</span></span>

## <span data-ttu-id="caf19-111">예제의</span><span class="sxs-lookup"><span data-stu-id="caf19-111">EXAMPLES</span></span>

### <span data-ttu-id="caf19-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="caf19-112">Example 1</span></span>
```powershell
PS C:\> (Get-AzCognitiveServicesAccountSku -Type 'TextAnalytics' -Location "westus").Value | Select-Object -E
xpandProperty Sku;

Name     Tier
----     ----
F0       Free
S0   Standard
```

## <span data-ttu-id="caf19-113">변수</span><span class="sxs-lookup"><span data-stu-id="caf19-113">PARAMETERS</span></span>

### <span data-ttu-id="caf19-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="caf19-114">-DefaultProfile</span></span>
<span data-ttu-id="caf19-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="caf19-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="caf19-116">-위치</span><span class="sxs-lookup"><span data-stu-id="caf19-116">-Location</span></span>
<span data-ttu-id="caf19-117">인식 서비스 계정 위치.</span><span class="sxs-lookup"><span data-stu-id="caf19-117">Cognitive Services Account Location.</span></span>

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

### <span data-ttu-id="caf19-118">-Type</span><span class="sxs-lookup"><span data-stu-id="caf19-118">-Type</span></span>
<span data-ttu-id="caf19-119">인식 서비스 계정 유형.</span><span class="sxs-lookup"><span data-stu-id="caf19-119">Cognitive Services Account Type.</span></span>

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

### <span data-ttu-id="caf19-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="caf19-120">CommonParameters</span></span>
<span data-ttu-id="caf19-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="caf19-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="caf19-122">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="caf19-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="caf19-123">입력</span><span class="sxs-lookup"><span data-stu-id="caf19-123">INPUTS</span></span>

### <span data-ttu-id="caf19-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="caf19-124">System.String</span></span>

## <span data-ttu-id="caf19-125">출력</span><span class="sxs-lookup"><span data-stu-id="caf19-125">OUTPUTS</span></span>

### <span data-ttu-id="caf19-126">CognitiveServices. ResourceSku/.</span><span class="sxs-lookup"><span data-stu-id="caf19-126">Microsoft.Azure.Management.CognitiveServices.Models.ResourceSku</span></span>

## <span data-ttu-id="caf19-127">상속자</span><span class="sxs-lookup"><span data-stu-id="caf19-127">NOTES</span></span>

## <span data-ttu-id="caf19-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="caf19-128">RELATED LINKS</span></span>
