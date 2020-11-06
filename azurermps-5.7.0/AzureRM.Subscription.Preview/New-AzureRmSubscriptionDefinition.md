---
external help file: Microsoft.Azure.Commands.SubscriptionDefinition.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.subscription.preview/new-azurermsubscriptiondefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Subscription/Commands.Subscription/help/New-AzureRmSubscriptionDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Subscription/Commands.Subscription/help/New-AzureRmSubscriptionDefinition.md
ms.openlocfilehash: 7acaca4977114a1a57f88f5050f658753a9b6214
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533547"
---
# <span data-ttu-id="9f02d-101">New-AzureRmSubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="9f02d-101">New-AzureRmSubscriptionDefinition</span></span>

## <span data-ttu-id="9f02d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f02d-102">SYNOPSIS</span></span>
<span data-ttu-id="9f02d-103">구독 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9f02d-103">Creates a subscription definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9f02d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9f02d-104">SYNTAX</span></span>

### <span data-ttu-id="9f02d-105">구독 정의 만들기</span><span class="sxs-lookup"><span data-stu-id="9f02d-105">Create subscription definition</span></span>
```
New-AzureRmSubscriptionDefinition -Name <String> -OfferType <String> [-SubscriptionDisplayName <String>]
```

## <span data-ttu-id="9f02d-106">설명은</span><span class="sxs-lookup"><span data-stu-id="9f02d-106">DESCRIPTION</span></span>
<span data-ttu-id="9f02d-107">**새 AzureRmSubscriptionDefinition** cmdlet은 구독 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9f02d-107">The **New-AzureRmSubscriptionDefinition** cmdlet creates a subscription definition.</span></span>

## <span data-ttu-id="9f02d-108">예제의</span><span class="sxs-lookup"><span data-stu-id="9f02d-108">EXAMPLES</span></span>

### <span data-ttu-id="9f02d-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="9f02d-109">Example 1</span></span>
```
PS C:\> New-AzureRmSubscriptionDefinition -Name MySubDef -OfferType MS-AZR-0017P

Name                    : MySubDef
SubscriptionId          : 86869d42-1782-4337-98b0-c905fb937d46
SubscriptionDisplayName : MySubDef
OfferType               : MS-AZR-0017P
```

<span data-ttu-id="9f02d-110">기본 구독 표시 이름을 사용 하 여 구독 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9f02d-110">Creates a subscription definition with a default subscription display name.</span></span>

### <span data-ttu-id="9f02d-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="9f02d-111">Example 2</span></span>
```
PS C:\> New-AzureRmSubscriptionDefinition -Name MySubDef -OfferType MS-AZR-0017P -SubscriptionDisplayName MyPaygoSub

Name                    : MySubDef
SubscriptionId          : 86869d42-1782-4337-98b0-c905fb937d46
SubscriptionDisplayName : MyPaygoSub
OfferType               : MS-AZR-0017P
```

<span data-ttu-id="9f02d-112">사용자 지정 구독 표시 이름을 사용 하 여 구독 정의를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9f02d-112">Creates a subscription definition with a custom subscription display name.</span></span>

## <span data-ttu-id="9f02d-113">변수</span><span class="sxs-lookup"><span data-stu-id="9f02d-113">PARAMETERS</span></span>

### <span data-ttu-id="9f02d-114">-이름</span><span class="sxs-lookup"><span data-stu-id="9f02d-114">-Name</span></span>
<span data-ttu-id="9f02d-115">만들 구독 정의의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9f02d-115">The name of the subscription definition to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f02d-116">-OfferType</span><span class="sxs-lookup"><span data-stu-id="9f02d-116">-OfferType</span></span>
<span data-ttu-id="9f02d-117">기본 구독을 만들 때 사용할 제공의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="9f02d-117">The type of offer to use when creating the underlying subscription.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f02d-118">-SubscriptionDisplayName</span><span class="sxs-lookup"><span data-stu-id="9f02d-118">-SubscriptionDisplayName</span></span>
<span data-ttu-id="9f02d-119">구독 정의의 기본 구독을 만들 때 사용할 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9f02d-119">The display name to use when creating the subscription definition's underlying subscription.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: Name
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f02d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f02d-120">CommonParameters</span></span>
<span data-ttu-id="9f02d-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9f02d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f02d-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f02d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f02d-123">입력</span><span class="sxs-lookup"><span data-stu-id="9f02d-123">INPUTS</span></span>

### <span data-ttu-id="9f02d-124">않아야</span><span class="sxs-lookup"><span data-stu-id="9f02d-124">None</span></span>

## <span data-ttu-id="9f02d-125">출력</span><span class="sxs-lookup"><span data-stu-id="9f02d-125">OUTPUTS</span></span>

### <span data-ttu-id="9f02d-126">Microsoft. i m.. m a i 구독 정의.</span><span class="sxs-lookup"><span data-stu-id="9f02d-126">Microsoft.Azure.Commands.SubscriptionDefinition.Models.PSSubscriptionDefinition</span></span>

## <span data-ttu-id="9f02d-127">상속자</span><span class="sxs-lookup"><span data-stu-id="9f02d-127">NOTES</span></span>

## <span data-ttu-id="9f02d-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9f02d-128">RELATED LINKS</span></span>

