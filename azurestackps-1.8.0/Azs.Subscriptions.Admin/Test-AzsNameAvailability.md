---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a4bd00dc1709a3060da9777ab4755ae1c6a28ec4
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93874606"
---
# <span data-ttu-id="07d11-101">Test-AzsNameAvailability</span><span class="sxs-lookup"><span data-stu-id="07d11-101">Test-AzsNameAvailability</span></span>

## <span data-ttu-id="07d11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07d11-102">SYNOPSIS</span></span>
<span data-ttu-id="07d11-103">지정 된 구독 리소스 종류 및 이름의 avaialbility를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="07d11-103">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="07d11-104">구문과</span><span class="sxs-lookup"><span data-stu-id="07d11-104">SYNTAX</span></span>

```
Test-AzsNameAvailability -Name <String> -ResourceType <String> [<CommonParameters>]
```

## <span data-ttu-id="07d11-105">설명은</span><span class="sxs-lookup"><span data-stu-id="07d11-105">DESCRIPTION</span></span>
<span data-ttu-id="07d11-106">지정 된 구독 리소스 종류 및 이름의 avaialbility를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="07d11-106">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="07d11-107">예제의</span><span class="sxs-lookup"><span data-stu-id="07d11-107">EXAMPLES</span></span>

### <span data-ttu-id="07d11-108">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="07d11-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Test-AzsNameAvailability -ResourceType "Microsoft.Subscriptions.Admin/offers" -Name offername1
```

<span data-ttu-id="07d11-109">지정 된 구독 리소스 종류 및 이름의 avaialbility를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="07d11-109">Returns the avaialbility of the specified subscriptions resource type and name</span></span>

## <span data-ttu-id="07d11-110">변수</span><span class="sxs-lookup"><span data-stu-id="07d11-110">PARAMETERS</span></span>

### <span data-ttu-id="07d11-111">-이름</span><span class="sxs-lookup"><span data-stu-id="07d11-111">-Name</span></span>
<span data-ttu-id="07d11-112">확인할 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="07d11-112">The resource name to verify.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07d11-113">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="07d11-113">-ResourceType</span></span>
<span data-ttu-id="07d11-114">확인할 리소스 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="07d11-114">The resource type to verify.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07d11-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07d11-115">CommonParameters</span></span>
<span data-ttu-id="07d11-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="07d11-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07d11-117">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07d11-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07d11-118">입력</span><span class="sxs-lookup"><span data-stu-id="07d11-118">INPUTS</span></span>

## <span data-ttu-id="07d11-119">출력</span><span class="sxs-lookup"><span data-stu-id="07d11-119">OUTPUTS</span></span>

### <span data-ttu-id="07d11-120">CheckNameAvailabilityResponse. 관리자. m a. 관리</span><span class="sxs-lookup"><span data-stu-id="07d11-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.CheckNameAvailabilityResponse</span></span>

## <span data-ttu-id="07d11-121">상속자</span><span class="sxs-lookup"><span data-stu-id="07d11-121">NOTES</span></span>

## <span data-ttu-id="07d11-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="07d11-122">RELATED LINKS</span></span>

