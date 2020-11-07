---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 02baf67cc13269d9d53c0adb40337adbd9929641
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93874965"
---
# <span data-ttu-id="36038-101">Get-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="36038-101">Get-AzsPlan</span></span>

## <span data-ttu-id="36038-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36038-102">SYNOPSIS</span></span>
<span data-ttu-id="36038-103">모든 구독에 대 한 모든 계획을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="36038-103">List all plans across all subscriptions.</span></span>

## <span data-ttu-id="36038-104">구문과</span><span class="sxs-lookup"><span data-stu-id="36038-104">SYNTAX</span></span>

### <span data-ttu-id="36038-105">ListAll (기본값)</span><span class="sxs-lookup"><span data-stu-id="36038-105">ListAll (Default)</span></span>
```
Get-AzsPlan [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="36038-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="36038-106">Get</span></span>
```
Get-AzsPlan -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="36038-107">목록</span><span class="sxs-lookup"><span data-stu-id="36038-107">List</span></span>
```
Get-AzsPlan -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="36038-108">리소스</span><span class="sxs-lookup"><span data-stu-id="36038-108">ResourceId</span></span>
```
Get-AzsPlan -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="36038-109">설명은</span><span class="sxs-lookup"><span data-stu-id="36038-109">DESCRIPTION</span></span>
<span data-ttu-id="36038-110">모든 구독에 대 한 모든 계획을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="36038-110">List all plans across all subscriptions.</span></span>

## <span data-ttu-id="36038-111">예제의</span><span class="sxs-lookup"><span data-stu-id="36038-111">EXAMPLES</span></span>

### <span data-ttu-id="36038-112">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="36038-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPlan -ResourceGroupName rg1 -Name plan1
```

<span data-ttu-id="36038-113">이 구독에서 특정 계획을 받으세요.</span><span class="sxs-lookup"><span data-stu-id="36038-113">Get a specifc plan under this subscriptions.</span></span>

## <span data-ttu-id="36038-114">변수</span><span class="sxs-lookup"><span data-stu-id="36038-114">PARAMETERS</span></span>

### <span data-ttu-id="36038-115">-이름</span><span class="sxs-lookup"><span data-stu-id="36038-115">-Name</span></span>
<span data-ttu-id="36038-116">계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="36038-116">Name of the plan.</span></span>

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

### <span data-ttu-id="36038-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36038-117">-ResourceGroupName</span></span>
<span data-ttu-id="36038-118">리소스가 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="36038-118">The name of the resource group the resource is located under.</span></span>

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

### <span data-ttu-id="36038-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="36038-119">-ResourceId</span></span>
<span data-ttu-id="36038-120">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="36038-120">The resource id.</span></span>

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

### <span data-ttu-id="36038-121">-생략</span><span class="sxs-lookup"><span data-stu-id="36038-121">-Skip</span></span>
<span data-ttu-id="36038-122">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="36038-122">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="36038-123">-위쪽</span><span class="sxs-lookup"><span data-stu-id="36038-123">-Top</span></span>
<span data-ttu-id="36038-124">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="36038-124">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="36038-125">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="36038-125">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="36038-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36038-126">CommonParameters</span></span>
<span data-ttu-id="36038-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="36038-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36038-128">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36038-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36038-129">입력</span><span class="sxs-lookup"><span data-stu-id="36038-129">INPUTS</span></span>

## <span data-ttu-id="36038-130">출력</span><span class="sxs-lookup"><span data-stu-id="36038-130">OUTPUTS</span></span>

### <span data-ttu-id="36038-131">Microsoft AzureStack. 관리자. 관리. 계획</span><span class="sxs-lookup"><span data-stu-id="36038-131">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Plan</span></span>

## <span data-ttu-id="36038-132">상속자</span><span class="sxs-lookup"><span data-stu-id="36038-132">NOTES</span></span>

## <span data-ttu-id="36038-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="36038-133">RELATED LINKS</span></span>

