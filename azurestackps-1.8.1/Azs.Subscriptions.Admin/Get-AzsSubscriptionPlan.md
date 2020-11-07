---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b2cb2886e84b42d499fb04693757cee333458f9b
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93874973"
---
# <span data-ttu-id="059dc-101">Get-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="059dc-101">Get-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="059dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="059dc-102">SYNOPSIS</span></span>
<span data-ttu-id="059dc-103">구독에서 액세스할 수 있는 모든 확보 된 계획의 컬렉션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="059dc-103">Get a collection of all acquired plans that subscription has access to.</span></span>

## <span data-ttu-id="059dc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="059dc-104">SYNTAX</span></span>

### <span data-ttu-id="059dc-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="059dc-105">List (Default)</span></span>
```
Get-AzsSubscriptionPlan -TargetSubscriptionId <Guid> [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="059dc-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="059dc-106">Get</span></span>
```
Get-AzsSubscriptionPlan -AcquisitionId <Guid> -TargetSubscriptionId <Guid> [<CommonParameters>]
```

### <span data-ttu-id="059dc-107">리소스</span><span class="sxs-lookup"><span data-stu-id="059dc-107">ResourceId</span></span>
```
Get-AzsSubscriptionPlan -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="059dc-108">설명은</span><span class="sxs-lookup"><span data-stu-id="059dc-108">DESCRIPTION</span></span>
<span data-ttu-id="059dc-109">구독에서 액세스할 수 있는 모든 확보 된 계획의 컬렉션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="059dc-109">Get a collection of all acquired plans that subscription has access to.</span></span>

## <span data-ttu-id="059dc-110">예제의</span><span class="sxs-lookup"><span data-stu-id="059dc-110">EXAMPLES</span></span>

### <span data-ttu-id="059dc-111">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="059dc-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsSubscriptionPlan -TargetSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="059dc-112">구독에서 액세스할 수 있는 모든 확보 된 계획의 컬렉션을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="059dc-112">Get a collection of all acquired plans that subscription has access to.</span></span>

## <span data-ttu-id="059dc-113">변수</span><span class="sxs-lookup"><span data-stu-id="059dc-113">PARAMETERS</span></span>

### <span data-ttu-id="059dc-114">-AcquisitionId</span><span class="sxs-lookup"><span data-stu-id="059dc-114">-AcquisitionId</span></span>
<span data-ttu-id="059dc-115">계획 획득 식별자</span><span class="sxs-lookup"><span data-stu-id="059dc-115">The plan acquisition Identifier</span></span>

```yaml
Type: Guid
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="059dc-116">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="059dc-116">-ResourceId</span></span>
<span data-ttu-id="059dc-117">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="059dc-117">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="059dc-118">-생략</span><span class="sxs-lookup"><span data-stu-id="059dc-118">-Skip</span></span>
<span data-ttu-id="059dc-119">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="059dc-119">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="059dc-120">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="059dc-120">-TargetSubscriptionId</span></span>
<span data-ttu-id="059dc-121">대상 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="059dc-121">The target subscription ID.</span></span>

```yaml
Type: Guid
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="059dc-122">-위쪽</span><span class="sxs-lookup"><span data-stu-id="059dc-122">-Top</span></span>
<span data-ttu-id="059dc-123">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="059dc-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="059dc-124">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="059dc-124">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="059dc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="059dc-125">CommonParameters</span></span>
<span data-ttu-id="059dc-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="059dc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="059dc-127">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="059dc-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="059dc-128">입력</span><span class="sxs-lookup"><span data-stu-id="059dc-128">INPUTS</span></span>

## <span data-ttu-id="059dc-129">출력</span><span class="sxs-lookup"><span data-stu-id="059dc-129">OUTPUTS</span></span>

### <span data-ttu-id="059dc-130">Microsoft AzureStack. 경영진. 관리. 모델 취득</span><span class="sxs-lookup"><span data-stu-id="059dc-130">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.PlanAcquisition</span></span>

## <span data-ttu-id="059dc-131">상속자</span><span class="sxs-lookup"><span data-stu-id="059dc-131">NOTES</span></span>

## <span data-ttu-id="059dc-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="059dc-132">RELATED LINKS</span></span>

