---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: afc99afebed095da96d826918cc6912f197d1899
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93875199"
---
# <span data-ttu-id="e629f-101">Get-AzsDelegatedProvider</span><span class="sxs-lookup"><span data-stu-id="e629f-101">Get-AzsDelegatedProvider</span></span>

## <span data-ttu-id="e629f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e629f-102">SYNOPSIS</span></span>
<span data-ttu-id="e629f-103">DelegatedProviders 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e629f-103">Get the list of delegatedProviders.</span></span>

## <span data-ttu-id="e629f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e629f-104">SYNTAX</span></span>

### <span data-ttu-id="e629f-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="e629f-105">List (Default)</span></span>
```
Get-AzsDelegatedProvider [<CommonParameters>]
```

### <span data-ttu-id="e629f-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="e629f-106">Get</span></span>
```
Get-AzsDelegatedProvider [-DelegatedProviderId] <Guid> [<CommonParameters>]
```

## <span data-ttu-id="e629f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e629f-107">DESCRIPTION</span></span>
<span data-ttu-id="e629f-108">DelegatedProviders 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e629f-108">Get the list of delegatedProviders.</span></span>

## <span data-ttu-id="e629f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e629f-109">EXAMPLES</span></span>

### <span data-ttu-id="e629f-110">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e629f-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDelegatedProvider
```

<span data-ttu-id="e629f-111">위임 된 공급자 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="e629f-111">Get a list of delegated providers.</span></span>

### <span data-ttu-id="e629f-112">--------------------------예제 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="e629f-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsDelegatedProvider -DelegatedProviderId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="e629f-113">위임 된 특정 공급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e629f-113">Get the a specific delegated provider.</span></span>

## <span data-ttu-id="e629f-114">변수</span><span class="sxs-lookup"><span data-stu-id="e629f-114">PARAMETERS</span></span>

### <span data-ttu-id="e629f-115">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="e629f-115">-DelegatedProviderId</span></span>
<span data-ttu-id="e629f-116">{{Fill DelegatedProviderId Description}}</span><span class="sxs-lookup"><span data-stu-id="e629f-116">{{Fill DelegatedProviderId Description}}</span></span>

```yaml
Type: Guid
Parameter Sets: Get
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e629f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e629f-117">CommonParameters</span></span>
<span data-ttu-id="e629f-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e629f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e629f-119">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e629f-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e629f-120">입력</span><span class="sxs-lookup"><span data-stu-id="e629f-120">INPUTS</span></span>

## <span data-ttu-id="e629f-121">출력</span><span class="sxs-lookup"><span data-stu-id="e629f-121">OUTPUTS</span></span>

### <span data-ttu-id="e629f-122">Microsoft AzureStack. 관리. 구독</span><span class="sxs-lookup"><span data-stu-id="e629f-122">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="e629f-123">상속자</span><span class="sxs-lookup"><span data-stu-id="e629f-123">NOTES</span></span>

## <span data-ttu-id="e629f-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e629f-124">RELATED LINKS</span></span>

