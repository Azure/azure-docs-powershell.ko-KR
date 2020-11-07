---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: afc99afebed095da96d826918cc6912f197d1899
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93874829"
---
# <span data-ttu-id="0a88d-101">Get-AzsDelegatedProvider</span><span class="sxs-lookup"><span data-stu-id="0a88d-101">Get-AzsDelegatedProvider</span></span>

## <span data-ttu-id="0a88d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a88d-102">SYNOPSIS</span></span>
<span data-ttu-id="0a88d-103">DelegatedProviders 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0a88d-103">Get the list of delegatedProviders.</span></span>

## <span data-ttu-id="0a88d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0a88d-104">SYNTAX</span></span>

### <span data-ttu-id="0a88d-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="0a88d-105">List (Default)</span></span>
```
Get-AzsDelegatedProvider [<CommonParameters>]
```

### <span data-ttu-id="0a88d-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="0a88d-106">Get</span></span>
```
Get-AzsDelegatedProvider [-DelegatedProviderId] <Guid> [<CommonParameters>]
```

## <span data-ttu-id="0a88d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0a88d-107">DESCRIPTION</span></span>
<span data-ttu-id="0a88d-108">DelegatedProviders 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0a88d-108">Get the list of delegatedProviders.</span></span>

## <span data-ttu-id="0a88d-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0a88d-109">EXAMPLES</span></span>

### <span data-ttu-id="0a88d-110">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0a88d-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDelegatedProvider
```

<span data-ttu-id="0a88d-111">위임 된 공급자 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="0a88d-111">Get a list of delegated providers.</span></span>

### <span data-ttu-id="0a88d-112">--------------------------예제 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="0a88d-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsDelegatedProvider -DelegatedProviderId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="0a88d-113">위임 된 특정 공급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0a88d-113">Get the a specific delegated provider.</span></span>

## <span data-ttu-id="0a88d-114">변수</span><span class="sxs-lookup"><span data-stu-id="0a88d-114">PARAMETERS</span></span>

### <span data-ttu-id="0a88d-115">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="0a88d-115">-DelegatedProviderId</span></span>
<span data-ttu-id="0a88d-116">{{Fill DelegatedProviderId Description}}</span><span class="sxs-lookup"><span data-stu-id="0a88d-116">{{Fill DelegatedProviderId Description}}</span></span>

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

### <span data-ttu-id="0a88d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a88d-117">CommonParameters</span></span>
<span data-ttu-id="0a88d-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a88d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a88d-119">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a88d-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a88d-120">입력</span><span class="sxs-lookup"><span data-stu-id="0a88d-120">INPUTS</span></span>

## <span data-ttu-id="0a88d-121">출력</span><span class="sxs-lookup"><span data-stu-id="0a88d-121">OUTPUTS</span></span>

### <span data-ttu-id="0a88d-122">Microsoft AzureStack. 관리. 구독</span><span class="sxs-lookup"><span data-stu-id="0a88d-122">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="0a88d-123">상속자</span><span class="sxs-lookup"><span data-stu-id="0a88d-123">NOTES</span></span>

## <span data-ttu-id="0a88d-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0a88d-124">RELATED LINKS</span></span>

