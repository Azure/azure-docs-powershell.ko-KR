---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 199d9fb2ce88c149965d488b55bce669f364a615
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93874945"
---
# <span data-ttu-id="8a7b6-101">New-PlanAcquisitionPropertiesObject</span><span class="sxs-lookup"><span data-stu-id="8a7b6-101">New-PlanAcquisitionPropertiesObject</span></span>

## <span data-ttu-id="8a7b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a7b6-102">SYNOPSIS</span></span>
<span data-ttu-id="8a7b6-103">구독에 대 한 추가 기능 계획의 획득을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8a7b6-103">Represents the acquisition of an add-on plan for a subscription.</span></span>

## <span data-ttu-id="8a7b6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8a7b6-104">SYNTAX</span></span>

```
New-PlanAcquisitionPropertiesObject [[-ProvisioningState] <String>] [[-AcquisitionTime] <String>]
 [[-Id] <String>] [[-PlanId] <String>] [[-AcquisitionId] <String>] [[-ExternalReferenceId] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="8a7b6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8a7b6-105">DESCRIPTION</span></span>
<span data-ttu-id="8a7b6-106">구독에 대 한 추가 기능 계획의 획득을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8a7b6-106">Represents the acquisition of an add-on plan for a subscription.</span></span>

## <span data-ttu-id="8a7b6-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8a7b6-107">EXAMPLES</span></span>

### <span data-ttu-id="8a7b6-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="8a7b6-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="8a7b6-109">{{여기에 예제 설명 추가}}</span><span class="sxs-lookup"><span data-stu-id="8a7b6-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="8a7b6-110">변수</span><span class="sxs-lookup"><span data-stu-id="8a7b6-110">PARAMETERS</span></span>

### <span data-ttu-id="8a7b6-111">-AcquisitionId</span><span class="sxs-lookup"><span data-stu-id="8a7b6-111">-AcquisitionId</span></span>
<span data-ttu-id="8a7b6-112">취득 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="8a7b6-112">Acquisition identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a7b6-113">-AcquisitionTime</span><span class="sxs-lookup"><span data-stu-id="8a7b6-113">-AcquisitionTime</span></span>
<span data-ttu-id="8a7b6-114">구입 시간.</span><span class="sxs-lookup"><span data-stu-id="8a7b6-114">Acquisition time.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a7b6-115">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="8a7b6-115">-ExternalReferenceId</span></span>
<span data-ttu-id="8a7b6-116">외부 참조 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="8a7b6-116">External reference identifier.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a7b6-117">-Id</span><span class="sxs-lookup"><span data-stu-id="8a7b6-117">-Id</span></span>
<span data-ttu-id="8a7b6-118">테 넌 트 구독 컨텍스트에 있는 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="8a7b6-118">Identifier in the tenant subscription context.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a7b6-119">-PlanId</span><span class="sxs-lookup"><span data-stu-id="8a7b6-119">-PlanId</span></span>
<span data-ttu-id="8a7b6-120">테 넌 트 구독 컨텍스트에서 id를 계획 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a7b6-120">Plan identifier in the tenant subscription context.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a7b6-121">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="8a7b6-121">-ProvisioningState</span></span>
<span data-ttu-id="8a7b6-122">프로 비전의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="8a7b6-122">State of the provisioning.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a7b6-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a7b6-123">CommonParameters</span></span>
<span data-ttu-id="8a7b6-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a7b6-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a7b6-125">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a7b6-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a7b6-126">입력</span><span class="sxs-lookup"><span data-stu-id="8a7b6-126">INPUTS</span></span>

## <span data-ttu-id="8a7b6-127">출력</span><span class="sxs-lookup"><span data-stu-id="8a7b6-127">OUTPUTS</span></span>

## <span data-ttu-id="8a7b6-128">상속자</span><span class="sxs-lookup"><span data-stu-id="8a7b6-128">NOTES</span></span>

## <span data-ttu-id="8a7b6-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8a7b6-129">RELATED LINKS</span></span>

