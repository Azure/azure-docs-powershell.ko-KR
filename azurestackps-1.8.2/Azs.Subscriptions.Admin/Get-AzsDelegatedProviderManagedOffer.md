---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: edf7b9135bc1f2d614f9fc516acadbc31821c45e
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94046909"
---
# <span data-ttu-id="940df-101">Get-AzsDelegatedProviderManagedOffer</span><span class="sxs-lookup"><span data-stu-id="940df-101">Get-AzsDelegatedProviderManagedOffer</span></span>

## <span data-ttu-id="940df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="940df-102">SYNOPSIS</span></span>
<span data-ttu-id="940df-103">위임 된 공급자 제공 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="940df-103">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="940df-104">구문과</span><span class="sxs-lookup"><span data-stu-id="940df-104">SYNTAX</span></span>

### <span data-ttu-id="940df-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="940df-105">List (Default)</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProviderId <String> [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="940df-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="940df-106">Get</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProviderId <String> -Name <String> [<CommonParameters>]
```

### <span data-ttu-id="940df-107">리소스</span><span class="sxs-lookup"><span data-stu-id="940df-107">ResourceId</span></span>
```
Get-AzsDelegatedProviderManagedOffer -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="940df-108">설명은</span><span class="sxs-lookup"><span data-stu-id="940df-108">DESCRIPTION</span></span>
<span data-ttu-id="940df-109">위임 된 공급자 제공 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="940df-109">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="940df-110">예제의</span><span class="sxs-lookup"><span data-stu-id="940df-110">EXAMPLES</span></span>

### <span data-ttu-id="940df-111">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="940df-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProvider "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="940df-112">위임 된 공급자 제공 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="940df-112">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="940df-113">변수</span><span class="sxs-lookup"><span data-stu-id="940df-113">PARAMETERS</span></span>

### <span data-ttu-id="940df-114">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="940df-114">-DelegatedProviderId</span></span>
<span data-ttu-id="940df-115">DelegatedProvider 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="940df-115">DelegatedProvider identifier.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: DelegatedProvider

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="940df-116">-이름</span><span class="sxs-lookup"><span data-stu-id="940df-116">-Name</span></span>
<span data-ttu-id="940df-117">제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="940df-117">Name of an offer.</span></span>

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

### <span data-ttu-id="940df-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="940df-118">-ResourceId</span></span>
<span data-ttu-id="940df-119">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="940df-119">The resource id.</span></span>

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

### <span data-ttu-id="940df-120">-생략</span><span class="sxs-lookup"><span data-stu-id="940df-120">-Skip</span></span>
<span data-ttu-id="940df-121">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="940df-121">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="940df-122">-위쪽</span><span class="sxs-lookup"><span data-stu-id="940df-122">-Top</span></span>
<span data-ttu-id="940df-123">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="940df-123">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="940df-124">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="940df-124">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="940df-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="940df-125">CommonParameters</span></span>
<span data-ttu-id="940df-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="940df-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="940df-127">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="940df-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="940df-128">입력</span><span class="sxs-lookup"><span data-stu-id="940df-128">INPUTS</span></span>

## <span data-ttu-id="940df-129">출력</span><span class="sxs-lookup"><span data-stu-id="940df-129">OUTPUTS</span></span>

### <span data-ttu-id="940df-130">DelegatedProviderOffer. 관리자. m a. 관리</span><span class="sxs-lookup"><span data-stu-id="940df-130">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.DelegatedProviderOffer</span></span>

## <span data-ttu-id="940df-131">상속자</span><span class="sxs-lookup"><span data-stu-id="940df-131">NOTES</span></span>

## <span data-ttu-id="940df-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="940df-132">RELATED LINKS</span></span>

