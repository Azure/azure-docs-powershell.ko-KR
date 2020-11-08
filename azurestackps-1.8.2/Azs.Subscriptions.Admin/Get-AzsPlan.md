---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 02baf67cc13269d9d53c0adb40337adbd9929641
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94046748"
---
# <span data-ttu-id="5cc80-101">Get-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="5cc80-101">Get-AzsPlan</span></span>

## <span data-ttu-id="5cc80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5cc80-102">SYNOPSIS</span></span>
<span data-ttu-id="5cc80-103">모든 구독에 대 한 모든 계획을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cc80-103">List all plans across all subscriptions.</span></span>

## <span data-ttu-id="5cc80-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5cc80-104">SYNTAX</span></span>

### <span data-ttu-id="5cc80-105">ListAll (기본값)</span><span class="sxs-lookup"><span data-stu-id="5cc80-105">ListAll (Default)</span></span>
```
Get-AzsPlan [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="5cc80-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="5cc80-106">Get</span></span>
```
Get-AzsPlan -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="5cc80-107">목록</span><span class="sxs-lookup"><span data-stu-id="5cc80-107">List</span></span>
```
Get-AzsPlan -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="5cc80-108">리소스</span><span class="sxs-lookup"><span data-stu-id="5cc80-108">ResourceId</span></span>
```
Get-AzsPlan -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="5cc80-109">설명은</span><span class="sxs-lookup"><span data-stu-id="5cc80-109">DESCRIPTION</span></span>
<span data-ttu-id="5cc80-110">모든 구독에 대 한 모든 계획을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cc80-110">List all plans across all subscriptions.</span></span>

## <span data-ttu-id="5cc80-111">예제의</span><span class="sxs-lookup"><span data-stu-id="5cc80-111">EXAMPLES</span></span>

### <span data-ttu-id="5cc80-112">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="5cc80-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPlan -ResourceGroupName rg1 -Name plan1
```

<span data-ttu-id="5cc80-113">이 구독에서 특정 계획을 받으세요.</span><span class="sxs-lookup"><span data-stu-id="5cc80-113">Get a specifc plan under this subscriptions.</span></span>

## <span data-ttu-id="5cc80-114">변수</span><span class="sxs-lookup"><span data-stu-id="5cc80-114">PARAMETERS</span></span>

### <span data-ttu-id="5cc80-115">-이름</span><span class="sxs-lookup"><span data-stu-id="5cc80-115">-Name</span></span>
<span data-ttu-id="5cc80-116">계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5cc80-116">Name of the plan.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cc80-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cc80-117">-ResourceGroupName</span></span>
<span data-ttu-id="5cc80-118">리소스가 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5cc80-118">The name of the resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Get, List
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cc80-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5cc80-119">-ResourceId</span></span>
<span data-ttu-id="5cc80-120">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="5cc80-120">The resource id.</span></span>

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

### <span data-ttu-id="5cc80-121">-생략</span><span class="sxs-lookup"><span data-stu-id="5cc80-121">-Skip</span></span>
<span data-ttu-id="5cc80-122">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="5cc80-122">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: ListAll, List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cc80-123">-위쪽</span><span class="sxs-lookup"><span data-stu-id="5cc80-123">-Top</span></span>
<span data-ttu-id="5cc80-124">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cc80-124">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="5cc80-125">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5cc80-125">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: ListAll, List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cc80-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cc80-126">CommonParameters</span></span>
<span data-ttu-id="5cc80-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5cc80-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cc80-128">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cc80-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cc80-129">입력</span><span class="sxs-lookup"><span data-stu-id="5cc80-129">INPUTS</span></span>

## <span data-ttu-id="5cc80-130">출력</span><span class="sxs-lookup"><span data-stu-id="5cc80-130">OUTPUTS</span></span>

### <span data-ttu-id="5cc80-131">Microsoft AzureStack. 관리자. 관리. 계획</span><span class="sxs-lookup"><span data-stu-id="5cc80-131">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan</span></span>

## <span data-ttu-id="5cc80-132">상속자</span><span class="sxs-lookup"><span data-stu-id="5cc80-132">NOTES</span></span>

## <span data-ttu-id="5cc80-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5cc80-133">RELATED LINKS</span></span>

