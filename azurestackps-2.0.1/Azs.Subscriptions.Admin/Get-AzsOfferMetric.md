---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsoffermetric
schema: 2.0.0
ms.openlocfilehash: 515cf3d9c26c9ca4ed59178e49854e23edfea84c
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/24/2020
ms.locfileid: "94045325"
---
# <span data-ttu-id="4c330-101">Get-AzsOfferMetric</span><span class="sxs-lookup"><span data-stu-id="4c330-101">Get-AzsOfferMetric</span></span>

## <span data-ttu-id="4c330-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c330-102">SYNOPSIS</span></span>
<span data-ttu-id="4c330-103">제공 지표를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4c330-103">Get the offer metrics.</span></span>

## <span data-ttu-id="4c330-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4c330-104">SYNTAX</span></span>

```
Get-AzsOfferMetric -OfferName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="4c330-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4c330-105">DESCRIPTION</span></span>
<span data-ttu-id="4c330-106">제공 지표를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4c330-106">Get the offer metrics.</span></span>

## <span data-ttu-id="4c330-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4c330-107">EXAMPLES</span></span>

### <span data-ttu-id="4c330-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="4c330-108">Example 1</span></span>
```powershell
PS C:\> Get-AzsOfferMetric -OfferName "testoffer" -ResourceGroupName "testrg"

EndTime               MetricUnit StartTime            TimeGrain
-------               ---------- ---------            ---------
3/13/2020 12:04:33 AM Count      3/6/2020 12:00:00 AM P1D      
3/13/2020 12:04:33 AM Count      3/6/2020 12:00:00 AM P1D
```

<span data-ttu-id="4c330-109">제공 지표를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4c330-109">Get the offer metrics.</span></span>

## <span data-ttu-id="4c330-110">변수</span><span class="sxs-lookup"><span data-stu-id="4c330-110">PARAMETERS</span></span>

### <span data-ttu-id="4c330-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c330-111">-DefaultProfile</span></span>
<span data-ttu-id="4c330-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4c330-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4c330-113">-OfferName</span><span class="sxs-lookup"><span data-stu-id="4c330-113">-OfferName</span></span>
<span data-ttu-id="4c330-114">제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4c330-114">Name of an offer.</span></span>

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

### <span data-ttu-id="4c330-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c330-115">-ResourceGroupName</span></span>
<span data-ttu-id="4c330-116">리소스가 있는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="4c330-116">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="4c330-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4c330-117">-SubscriptionId</span></span>
<span data-ttu-id="4c330-118">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다. 구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c330-118">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4c330-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c330-119">CommonParameters</span></span>
<span data-ttu-id="4c330-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4c330-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c330-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4c330-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c330-122">입력</span><span class="sxs-lookup"><span data-stu-id="4c330-122">INPUTS</span></span>

## <span data-ttu-id="4c330-123">출력</span><span class="sxs-lookup"><span data-stu-id="4c330-123">OUTPUTS</span></span>

### <span data-ttu-id="4c330-124">SubscriptionsAdmin. Api20151101. IMetricList에 대 한</span><span class="sxs-lookup"><span data-stu-id="4c330-124">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IMetricList</span></span>

<span data-ttu-id="4c330-125">별칭과</span><span class="sxs-lookup"><span data-stu-id="4c330-125">ALIASES</span></span>

## <span data-ttu-id="4c330-126">상속자</span><span class="sxs-lookup"><span data-stu-id="4c330-126">NOTES</span></span>

## <span data-ttu-id="4c330-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4c330-127">RELATED LINKS</span></span>

