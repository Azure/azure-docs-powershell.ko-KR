---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3874c581d1d030f9c0b77abe82b5a5a289d8960d
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93874963"
---
# <span data-ttu-id="336d2-101">Get-AzsSubscriptionsQuota</span><span class="sxs-lookup"><span data-stu-id="336d2-101">Get-AzsSubscriptionsQuota</span></span>

## <span data-ttu-id="336d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="336d2-102">SYNOPSIS</span></span>
<span data-ttu-id="336d2-103">위치에서 구독 리소스 공급자 할당량 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="336d2-103">Get the list of subscription resource provider quotas at a location.</span></span>

## <span data-ttu-id="336d2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="336d2-104">SYNTAX</span></span>

### <span data-ttu-id="336d2-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="336d2-105">List (Default)</span></span>
```
Get-AzsSubscriptionsQuota [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="336d2-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="336d2-106">Get</span></span>
```
Get-AzsSubscriptionsQuota -Name <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="336d2-107">리소스</span><span class="sxs-lookup"><span data-stu-id="336d2-107">ResourceId</span></span>
```
Get-AzsSubscriptionsQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="336d2-108">설명은</span><span class="sxs-lookup"><span data-stu-id="336d2-108">DESCRIPTION</span></span>
<span data-ttu-id="336d2-109">위치에서 할당량 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="336d2-109">Get the list of quotas at a location.</span></span>

## <span data-ttu-id="336d2-110">예제의</span><span class="sxs-lookup"><span data-stu-id="336d2-110">EXAMPLES</span></span>

### <span data-ttu-id="336d2-111">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="336d2-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsSubscriptionsQuota
```

<span data-ttu-id="336d2-112">위치에서 구독 리소스 공급자 할당량 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="336d2-112">Get the list of subscription resource provider quotas at a location.</span></span>

## <span data-ttu-id="336d2-113">변수</span><span class="sxs-lookup"><span data-stu-id="336d2-113">PARAMETERS</span></span>

### <span data-ttu-id="336d2-114">-위치</span><span class="sxs-lookup"><span data-stu-id="336d2-114">-Location</span></span>
<span data-ttu-id="336d2-115">AzureStack 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="336d2-115">The AzureStack location.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: ArmLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="336d2-116">-이름</span><span class="sxs-lookup"><span data-stu-id="336d2-116">-Name</span></span>
<span data-ttu-id="336d2-117">할당량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="336d2-117">Name of the quota.</span></span>

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

### <span data-ttu-id="336d2-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="336d2-118">-ResourceId</span></span>
<span data-ttu-id="336d2-119">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="336d2-119">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="336d2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="336d2-120">CommonParameters</span></span>
<span data-ttu-id="336d2-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="336d2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="336d2-122">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="336d2-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="336d2-123">입력</span><span class="sxs-lookup"><span data-stu-id="336d2-123">INPUTS</span></span>

## <span data-ttu-id="336d2-124">출력</span><span class="sxs-lookup"><span data-stu-id="336d2-124">OUTPUTS</span></span>

### <span data-ttu-id="336d2-125">Microsoft AzureStack. 관리자. i a 관리. 할당량</span><span class="sxs-lookup"><span data-stu-id="336d2-125">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Quota</span></span>

## <span data-ttu-id="336d2-126">상속자</span><span class="sxs-lookup"><span data-stu-id="336d2-126">NOTES</span></span>

## <span data-ttu-id="336d2-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="336d2-127">RELATED LINKS</span></span>

