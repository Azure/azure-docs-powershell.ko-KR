---
external help file: Microsoft.Azure.Commands.Management.CognitiveServices.dll-Help.xml
Module Name: AzureRM.CognitiveServices
ms.assetid: 386F09F0-2EEC-4B55-825C-F2E88D3B60AA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountSkus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/CognitiveServices/Commands.Management.CognitiveServices/help/Get-AzureRmCognitiveServicesAccountSkus.md
ms.openlocfilehash: de2640d8a2044a8124fb87bed53b9ee433977716
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531152"
---
# <span data-ttu-id="b1a70-101">Get-AzureRmCognitiveServicesAccountSkus</span><span class="sxs-lookup"><span data-stu-id="b1a70-101">Get-AzureRmCognitiveServicesAccountSkus</span></span>

## <span data-ttu-id="b1a70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1a70-102">SYNOPSIS</span></span>
<span data-ttu-id="b1a70-103">계정에 사용할 수 있는 Sku를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b1a70-103">Gets the available SKUs for an account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1a70-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b1a70-104">SYNTAX</span></span>

```
Get-AzureRmCognitiveServicesAccountSkus [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1a70-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b1a70-105">DESCRIPTION</span></span>
<span data-ttu-id="b1a70-106">**AzureRmCognitiveServicesAccountSkus** Cmdlet은 인식 서비스 계정에 사용할 수 있는 sku를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b1a70-106">The **Get-AzureRmCognitiveServicesAccountSkus** cmdlet gets the available SKUs for a Cognitive Services account.</span></span>

<span data-ttu-id="b1a70-107">SKU는 거래처에 대 한 계층 계획입니다.</span><span class="sxs-lookup"><span data-stu-id="b1a70-107">The SKU is the tier plan for an account.</span></span>
<span data-ttu-id="b1a70-108">계정에 대 한 가격, 통화 제한 및 요금을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1a70-108">It defines the price, call limit, and rate for the account.</span></span>
<span data-ttu-id="b1a70-109">F0 SKU는 무료 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="b1a70-109">The F0 SKU is a free tier.</span></span>
<span data-ttu-id="b1a70-110">유료 계층에는 S0, S1, S2 등이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1a70-110">Paid tiers include S0, S1, S2, and so on.</span></span>

## <span data-ttu-id="b1a70-111">예제의</span><span class="sxs-lookup"><span data-stu-id="b1a70-111">EXAMPLES</span></span>

## <span data-ttu-id="b1a70-112">변수</span><span class="sxs-lookup"><span data-stu-id="b1a70-112">PARAMETERS</span></span>

### <span data-ttu-id="b1a70-113">-이름</span><span class="sxs-lookup"><span data-stu-id="b1a70-113">-Name</span></span>
<span data-ttu-id="b1a70-114">계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1a70-114">Specifies the name of the account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CognitiveServicesAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1a70-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1a70-115">-ResourceGroupName</span></span>
<span data-ttu-id="b1a70-116">계정이 할당 되는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1a70-116">Specifies the name of the resource group the account is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1a70-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1a70-117">-DefaultProfile</span></span>
<span data-ttu-id="b1a70-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b1a70-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b1a70-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1a70-119">CommonParameters</span></span>
<span data-ttu-id="b1a70-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1a70-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1a70-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1a70-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1a70-122">입력</span><span class="sxs-lookup"><span data-stu-id="b1a70-122">INPUTS</span></span>

## <span data-ttu-id="b1a70-123">출력</span><span class="sxs-lookup"><span data-stu-id="b1a70-123">OUTPUTS</span></span>

### <span data-ttu-id="b1a70-124">CognitiveServices. PSCognitiveServicesSkus/. \*</span><span class="sxs-lookup"><span data-stu-id="b1a70-124">Microsoft.Azure.Commands.Management.CognitiveServices.Models.PSCognitiveServicesSkus</span></span>

## <span data-ttu-id="b1a70-125">상속자</span><span class="sxs-lookup"><span data-stu-id="b1a70-125">NOTES</span></span>

## <span data-ttu-id="b1a70-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b1a70-126">RELATED LINKS</span></span>

