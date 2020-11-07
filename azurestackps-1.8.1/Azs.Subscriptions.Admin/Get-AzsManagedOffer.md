---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e30a1501cb5df34dc8f8b2ab51041f867a5ee6c1
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93875177"
---
# <span data-ttu-id="6b230-101">Get-AzsManagedOffer</span><span class="sxs-lookup"><span data-stu-id="6b230-101">Get-AzsManagedOffer</span></span>

## <span data-ttu-id="6b230-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b230-102">SYNOPSIS</span></span>
<span data-ttu-id="6b230-103">서비스 제공 목록을 관리자로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6b230-103">Get the list of offers as the administrator.</span></span>

## <span data-ttu-id="6b230-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6b230-104">SYNTAX</span></span>

### <span data-ttu-id="6b230-105">ListAll (기본값)</span><span class="sxs-lookup"><span data-stu-id="6b230-105">ListAll (Default)</span></span>
```
Get-AzsManagedOffer [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="6b230-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="6b230-106">Get</span></span>
```
Get-AzsManagedOffer -Name <String> -ResourceGroupName <String> [<CommonParameters>]
```

### <span data-ttu-id="6b230-107">목록</span><span class="sxs-lookup"><span data-stu-id="6b230-107">List</span></span>
```
Get-AzsManagedOffer -ResourceGroupName <String> [-Skip <Int32>] [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="6b230-108">리소스</span><span class="sxs-lookup"><span data-stu-id="6b230-108">ResourceId</span></span>
```
Get-AzsManagedOffer -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="6b230-109">설명은</span><span class="sxs-lookup"><span data-stu-id="6b230-109">DESCRIPTION</span></span>
<span data-ttu-id="6b230-110">행사 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="6b230-110">Get the list of offers.</span></span>

## <span data-ttu-id="6b230-111">예제의</span><span class="sxs-lookup"><span data-stu-id="6b230-111">EXAMPLES</span></span>

### <span data-ttu-id="6b230-112">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="6b230-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsManagedOffer -Name offer -ResourceGroupName offerrg
```

<span data-ttu-id="6b230-113">서비스 제공 목록을 관리자로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6b230-113">Get the list of offers as the administrator.</span></span>

## <span data-ttu-id="6b230-114">변수</span><span class="sxs-lookup"><span data-stu-id="6b230-114">PARAMETERS</span></span>

### <span data-ttu-id="6b230-115">-이름</span><span class="sxs-lookup"><span data-stu-id="6b230-115">-Name</span></span>
<span data-ttu-id="6b230-116">제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6b230-116">Name of an offer.</span></span>

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

### <span data-ttu-id="6b230-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b230-117">-ResourceGroupName</span></span>
<span data-ttu-id="6b230-118">리소스가 있는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="6b230-118">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="6b230-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6b230-119">-ResourceId</span></span>
<span data-ttu-id="6b230-120">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="6b230-120">The resource id.</span></span>

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

### <span data-ttu-id="6b230-121">-생략</span><span class="sxs-lookup"><span data-stu-id="6b230-121">-Skip</span></span>
<span data-ttu-id="6b230-122">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="6b230-122">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="6b230-123">-위쪽</span><span class="sxs-lookup"><span data-stu-id="6b230-123">-Top</span></span>
<span data-ttu-id="6b230-124">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b230-124">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="6b230-125">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b230-125">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="6b230-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b230-126">CommonParameters</span></span>
<span data-ttu-id="6b230-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b230-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b230-128">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b230-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b230-129">입력</span><span class="sxs-lookup"><span data-stu-id="6b230-129">INPUTS</span></span>

## <span data-ttu-id="6b230-130">출력</span><span class="sxs-lookup"><span data-stu-id="6b230-130">OUTPUTS</span></span>

### <span data-ttu-id="6b230-131">Microsoft AzureStack. 관리. 관리자. 제공</span><span class="sxs-lookup"><span data-stu-id="6b230-131">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Offer</span></span>

## <span data-ttu-id="6b230-132">상속자</span><span class="sxs-lookup"><span data-stu-id="6b230-132">NOTES</span></span>

## <span data-ttu-id="6b230-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6b230-133">RELATED LINKS</span></span>

