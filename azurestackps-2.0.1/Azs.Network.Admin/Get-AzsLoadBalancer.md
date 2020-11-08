---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsloadbalancer
schema: 2.0.0
ms.openlocfilehash: 1450a35252a3bd5e749a8ebdb60fda0e8ad35f88
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/24/2020
ms.locfileid: "94045215"
---
# <span data-ttu-id="3deb6-101">Get-AzsLoadBalancer</span><span class="sxs-lookup"><span data-stu-id="3deb6-101">Get-AzsLoadBalancer</span></span>

## <span data-ttu-id="3deb6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3deb6-102">SYNOPSIS</span></span>
<span data-ttu-id="3deb6-103">모든 부하 분산 장치 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3deb6-103">Get a list of all load balancers.</span></span>

## <span data-ttu-id="3deb6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3deb6-104">SYNTAX</span></span>

```
Get-AzsLoadBalancer [-SubscriptionId <String[]>] [-Filter <String>] [-InlineCount <String>]
 [-OrderBy <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="3deb6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3deb6-105">DESCRIPTION</span></span>
<span data-ttu-id="3deb6-106">모든 부하 분산 장치 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3deb6-106">Get a list of all load balancers.</span></span>

## <span data-ttu-id="3deb6-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3deb6-107">EXAMPLES</span></span>

### <span data-ttu-id="3deb6-108">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3deb6-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```powershell
Get-AzsLoadBalancer
To view examples, please use the -Online parameter with Get-Help or navigate to: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsloadbalancer
```



## <span data-ttu-id="3deb6-109">변수</span><span class="sxs-lookup"><span data-stu-id="3deb6-109">PARAMETERS</span></span>

### <span data-ttu-id="3deb6-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3deb6-110">-DefaultProfile</span></span>
<span data-ttu-id="3deb6-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3deb6-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3deb6-112">-필터</span><span class="sxs-lookup"><span data-stu-id="3deb6-112">-Filter</span></span>
<span data-ttu-id="3deb6-113">OData 필터 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="3deb6-113">OData filter parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3deb6-114">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="3deb6-114">-InlineCount</span></span>
<span data-ttu-id="3deb6-115">OData 인라인 개수 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="3deb6-115">OData inline count parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3deb6-116">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="3deb6-116">-OrderBy</span></span>
<span data-ttu-id="3deb6-117">OData orderBy 매개 변수.</span><span class="sxs-lookup"><span data-stu-id="3deb6-117">OData orderBy parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3deb6-118">-생략</span><span class="sxs-lookup"><span data-stu-id="3deb6-118">-Skip</span></span>
<span data-ttu-id="3deb6-119">OData skip 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="3deb6-119">OData skip parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3deb6-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3deb6-120">-SubscriptionId</span></span>
<span data-ttu-id="3deb6-121">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="3deb6-121">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="3deb6-122">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="3deb6-122">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3deb6-123">-위쪽</span><span class="sxs-lookup"><span data-stu-id="3deb6-123">-Top</span></span>
<span data-ttu-id="3deb6-124">OData top 매개 변수.</span><span class="sxs-lookup"><span data-stu-id="3deb6-124">OData top parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="3deb6-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3deb6-125">CommonParameters</span></span>
<span data-ttu-id="3deb6-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3deb6-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3deb6-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3deb6-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3deb6-128">입력</span><span class="sxs-lookup"><span data-stu-id="3deb6-128">INPUTS</span></span>

## <span data-ttu-id="3deb6-129">출력</span><span class="sxs-lookup"><span data-stu-id="3deb6-129">OUTPUTS</span></span>

### <span data-ttu-id="3deb6-130">Api20150615. ILoadBalancer에 대 한 관리자.</span><span class="sxs-lookup"><span data-stu-id="3deb6-130">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.ILoadBalancer</span></span>



## <span data-ttu-id="3deb6-131">상속자</span><span class="sxs-lookup"><span data-stu-id="3deb6-131">NOTES</span></span>

## <span data-ttu-id="3deb6-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3deb6-132">RELATED LINKS</span></span>
