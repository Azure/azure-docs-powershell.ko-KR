---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 88c19285ee7188dab272eeab7a668f5f5dfe22a4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523800"
---
# <span data-ttu-id="ecb50-101">Get-AzsDelegatedProvider</span><span class="sxs-lookup"><span data-stu-id="ecb50-101">Get-AzsDelegatedProvider</span></span>

## <span data-ttu-id="ecb50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecb50-102">SYNOPSIS</span></span>
<span data-ttu-id="ecb50-103">DelegatedProviders 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ecb50-103">Get the list of delegatedProviders.</span></span>

## <span data-ttu-id="ecb50-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ecb50-104">SYNTAX</span></span>

### <span data-ttu-id="ecb50-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="ecb50-105">List (Default)</span></span>
```
Get-AzsDelegatedProvider [<CommonParameters>]
```

### <span data-ttu-id="ecb50-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="ecb50-106">Get</span></span>
```
Get-AzsDelegatedProvider [-DelegatedProviderId] <Guid> [<CommonParameters>]
```

## <span data-ttu-id="ecb50-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ecb50-107">DESCRIPTION</span></span>
<span data-ttu-id="ecb50-108">DelegatedProviders 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ecb50-108">Get the list of delegatedProviders.</span></span>

## <span data-ttu-id="ecb50-109">예제의</span><span class="sxs-lookup"><span data-stu-id="ecb50-109">EXAMPLES</span></span>

### <span data-ttu-id="ecb50-110">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ecb50-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsDelegatedProvider
```

<span data-ttu-id="ecb50-111">위임 된 공급자 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="ecb50-111">Get a list of delegated providers.</span></span>

### <span data-ttu-id="ecb50-112">--------------------------예제 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="ecb50-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsDelegatedProvider -DelegatedProviderId "c90173b1-de7a-4b1d-8600-b832b0e65946"
```

<span data-ttu-id="ecb50-113">위임 된 특정 공급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ecb50-113">Get the a specific delegated provider.</span></span>

## <span data-ttu-id="ecb50-114">변수</span><span class="sxs-lookup"><span data-stu-id="ecb50-114">PARAMETERS</span></span>

### <span data-ttu-id="ecb50-115">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="ecb50-115">-DelegatedProviderId</span></span>
<span data-ttu-id="ecb50-116">DelegatedProvider 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="ecb50-116">DelegatedProvider identifier.</span></span>

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

### <span data-ttu-id="ecb50-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecb50-117">CommonParameters</span></span>
<span data-ttu-id="ecb50-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecb50-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecb50-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecb50-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecb50-120">입력</span><span class="sxs-lookup"><span data-stu-id="ecb50-120">INPUTS</span></span>

## <span data-ttu-id="ecb50-121">출력</span><span class="sxs-lookup"><span data-stu-id="ecb50-121">OUTPUTS</span></span>

### <span data-ttu-id="ecb50-122">Microsoft AzureStack. 관리. 구독</span><span class="sxs-lookup"><span data-stu-id="ecb50-122">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="ecb50-123">상속자</span><span class="sxs-lookup"><span data-stu-id="ecb50-123">NOTES</span></span>

## <span data-ttu-id="ecb50-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ecb50-124">RELATED LINKS</span></span>

