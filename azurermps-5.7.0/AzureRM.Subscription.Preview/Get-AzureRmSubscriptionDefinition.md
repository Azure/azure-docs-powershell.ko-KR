---
external help file: Microsoft.Azure.Commands.SubscriptionDefinition.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.subscription.preview/get-azurermsubscriptiondefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Subscription/Commands.Subscription/help/Get-AzureRmSubscriptionDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Subscription/Commands.Subscription/help/Get-AzureRmSubscriptionDefinition.md
ms.openlocfilehash: 8f9cfda051542327fdb6175da081c99e6b8b6b3e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526495"
---
# <span data-ttu-id="eeeb8-101">Get-AzureRmSubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="eeeb8-101">Get-AzureRmSubscriptionDefinition</span></span>

## <span data-ttu-id="eeeb8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eeeb8-102">SYNOPSIS</span></span>
<span data-ttu-id="eeeb8-103">구독 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eeeb8-103">Get a subscription definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eeeb8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="eeeb8-104">SYNTAX</span></span>

### <span data-ttu-id="eeeb8-105">구독 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eeeb8-105">Get subscription definitions.</span></span>
```
Get-AzureRmSubscriptionDefinition
```

## <span data-ttu-id="eeeb8-106">예제의</span><span class="sxs-lookup"><span data-stu-id="eeeb8-106">EXAMPLES</span></span>

### <span data-ttu-id="eeeb8-107">예제 1</span><span class="sxs-lookup"><span data-stu-id="eeeb8-107">Example 1</span></span>
```
PS C:\> Get-AzureRmSubscriptionDefinition

Name                    : MyProdSubscription1
SubscriptionId          : 86869d42-1782-4337-98b0-c905fb937d46
SubscriptionDisplayName : MyProdSubscription1
OfferType               : MS-AZR-0017P

Name                    : MyProdSubscription2
SubscriptionId          : 368425df-b536-4f42-b1ba-64613cfcc4b5
SubscriptionDisplayName : MyProdSubscription2
OfferType               : MS-AZR-0017P
```

<span data-ttu-id="eeeb8-108">모든 구독 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eeeb8-108">Gets all subscription definitions.</span></span>

### <span data-ttu-id="eeeb8-109">예제 2</span><span class="sxs-lookup"><span data-stu-id="eeeb8-109">Example 2</span></span>
```
PS C:\> Get-AzureRmSubscriptionDefinition -Name MyProdSubscription2

Name                    : MyProdSubscription2
SubscriptionId          : 368425df-b536-4f42-b1ba-64613cfcc4b5
SubscriptionDisplayName : MyProdSubscription2
OfferType               : MS-AZR-0017P
```

<span data-ttu-id="eeeb8-110">이름 MyProdSubscription2를 사용 하 여 구독 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="eeeb8-110">Gets a subscription definition with the name MyProdSubscription2.</span></span>

## <span data-ttu-id="eeeb8-111">변수</span><span class="sxs-lookup"><span data-stu-id="eeeb8-111">PARAMETERS</span></span>

### <span data-ttu-id="eeeb8-112">-이름</span><span class="sxs-lookup"><span data-stu-id="eeeb8-112">-Name</span></span>
<span data-ttu-id="eeeb8-113">검색할 구독 정의의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eeeb8-113">The name of the subscription definition to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eeeb8-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eeeb8-114">CommonParameters</span></span>
<span data-ttu-id="eeeb8-115">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="eeeb8-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eeeb8-116">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eeeb8-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eeeb8-117">입력</span><span class="sxs-lookup"><span data-stu-id="eeeb8-117">INPUTS</span></span>

### <span data-ttu-id="eeeb8-118">않아야</span><span class="sxs-lookup"><span data-stu-id="eeeb8-118">None</span></span>

## <span data-ttu-id="eeeb8-119">출력</span><span class="sxs-lookup"><span data-stu-id="eeeb8-119">OUTPUTS</span></span>

### <span data-ttu-id="eeeb8-120">System.webserver. List ' 1 [[Microsoft Azure.]. e n t 구독 정의, Microsoft Azure. 명령인 정의, Version = 0.1.0.0, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="eeeb8-120">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.SubscriptionDefinition.Models.PSSubscriptionDefinition, Microsoft.Azure.Commands.SubscriptionDefinition, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="eeeb8-121">상속자</span><span class="sxs-lookup"><span data-stu-id="eeeb8-121">NOTES</span></span>

## <span data-ttu-id="eeeb8-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eeeb8-122">RELATED LINKS</span></span>

