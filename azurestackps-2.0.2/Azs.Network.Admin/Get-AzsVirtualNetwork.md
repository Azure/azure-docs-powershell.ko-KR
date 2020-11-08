---
external help file: ''
Module Name: Azs.Network.Admin
online version: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsvirtualnetwork
schema: 2.0.0
ms.openlocfilehash: 2f03d0599a7bfaf2b083b4a6c335b1de98b3fa73
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94046964"
---
# <span data-ttu-id="e3093-101">Get-AzsVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="e3093-101">Get-AzsVirtualNetwork</span></span>

## <span data-ttu-id="e3093-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3093-102">SYNOPSIS</span></span>
<span data-ttu-id="e3093-103">모든 가상 네트워크 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e3093-103">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="e3093-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e3093-104">SYNTAX</span></span>

```
Get-AzsVirtualNetwork [-SubscriptionId <String[]>] [-Filter <String>] [-InlineCount <String>]
 [-OrderBy <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="e3093-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e3093-105">DESCRIPTION</span></span>
<span data-ttu-id="e3093-106">모든 가상 네트워크 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e3093-106">Get a list of all virtual networks.</span></span>

## <span data-ttu-id="e3093-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e3093-107">EXAMPLES</span></span>

### <span data-ttu-id="e3093-108">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e3093-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```powershell
Get-AzsVirtualNetwork
To view examples, please use the -Online parameter with Get-Help or navigate to: https://docs.microsoft.com/powershell/module/azs.network.admin/get-azsvirtualnetwork
```

<span data-ttu-id="e3093-109">Azure 스택 스탬프에 대 한 가상 네트워크 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3093-109">Return a list of virtual networks for the Azure Stack stamp.</span></span>

## <span data-ttu-id="e3093-110">변수</span><span class="sxs-lookup"><span data-stu-id="e3093-110">PARAMETERS</span></span>

### <span data-ttu-id="e3093-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3093-111">-DefaultProfile</span></span>
<span data-ttu-id="e3093-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e3093-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3093-113">-필터</span><span class="sxs-lookup"><span data-stu-id="e3093-113">-Filter</span></span>
<span data-ttu-id="e3093-114">OData 필터 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="e3093-114">OData filter parameter.</span></span>

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

### <span data-ttu-id="e3093-115">-InlineCount</span><span class="sxs-lookup"><span data-stu-id="e3093-115">-InlineCount</span></span>
<span data-ttu-id="e3093-116">OData 인라인 개수 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="e3093-116">OData inline count parameter.</span></span>

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

### <span data-ttu-id="e3093-117">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="e3093-117">-OrderBy</span></span>
<span data-ttu-id="e3093-118">OData orderBy 매개 변수.</span><span class="sxs-lookup"><span data-stu-id="e3093-118">OData orderBy parameter.</span></span>

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

### <span data-ttu-id="e3093-119">-생략</span><span class="sxs-lookup"><span data-stu-id="e3093-119">-Skip</span></span>
<span data-ttu-id="e3093-120">OData skip 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="e3093-120">OData skip parameter.</span></span>

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

### <span data-ttu-id="e3093-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e3093-121">-SubscriptionId</span></span>
<span data-ttu-id="e3093-122">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="e3093-122">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e3093-123">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3093-123">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e3093-124">-위쪽</span><span class="sxs-lookup"><span data-stu-id="e3093-124">-Top</span></span>
<span data-ttu-id="e3093-125">OData top 매개 변수.</span><span class="sxs-lookup"><span data-stu-id="e3093-125">OData top parameter.</span></span>

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

### <span data-ttu-id="e3093-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3093-126">CommonParameters</span></span>
<span data-ttu-id="e3093-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e3093-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3093-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e3093-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3093-129">입력</span><span class="sxs-lookup"><span data-stu-id="e3093-129">INPUTS</span></span>

## <span data-ttu-id="e3093-130">출력</span><span class="sxs-lookup"><span data-stu-id="e3093-130">OUTPUTS</span></span>

### <span data-ttu-id="e3093-131">Api20150615. IVirtualNetwork에 대 한 관리자.</span><span class="sxs-lookup"><span data-stu-id="e3093-131">Microsoft.Azure.PowerShell.Cmdlets.NetworkAdmin.Models.Api20150615.IVirtualNetwork</span></span>



## <span data-ttu-id="e3093-132">상속자</span><span class="sxs-lookup"><span data-stu-id="e3093-132">NOTES</span></span>

## <span data-ttu-id="e3093-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e3093-133">RELATED LINKS</span></span>

