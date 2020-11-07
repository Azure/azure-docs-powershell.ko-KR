---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: d8ef41d414d12182c15d9ec5b01138e0110dee9f
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93874964"
---
# <span data-ttu-id="0dfdb-101">Get-AzsPlanMetric</span><span class="sxs-lookup"><span data-stu-id="0dfdb-101">Get-AzsPlanMetric</span></span>

## <span data-ttu-id="0dfdb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0dfdb-102">SYNOPSIS</span></span>
<span data-ttu-id="0dfdb-103">계획 메트릭을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0dfdb-103">Get the plan metrics.</span></span>

## <span data-ttu-id="0dfdb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0dfdb-104">SYNTAX</span></span>

```
Get-AzsPlanMetric [-ResourceGroupName] <String> [-PlanName] <String> [<CommonParameters>]
```

## <span data-ttu-id="0dfdb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0dfdb-105">DESCRIPTION</span></span>
<span data-ttu-id="0dfdb-106">계획 메트릭을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0dfdb-106">Get the plan metrics.</span></span>

## <span data-ttu-id="0dfdb-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0dfdb-107">EXAMPLES</span></span>

### <span data-ttu-id="0dfdb-108">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0dfdb-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsPlanMetric -ResourceGroupName rg1 -PlanName plan1
```

<span data-ttu-id="0dfdb-109">계획의 메트릭을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0dfdb-109">Get a plan's metrics.</span></span>

## <span data-ttu-id="0dfdb-110">변수</span><span class="sxs-lookup"><span data-stu-id="0dfdb-110">PARAMETERS</span></span>

### <span data-ttu-id="0dfdb-111">-계획 이름</span><span class="sxs-lookup"><span data-stu-id="0dfdb-111">-PlanName</span></span>
<span data-ttu-id="0dfdb-112">계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0dfdb-112">Name of the plan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dfdb-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0dfdb-113">-ResourceGroupName</span></span>
<span data-ttu-id="0dfdb-114">리소스가 있는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="0dfdb-114">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dfdb-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dfdb-115">CommonParameters</span></span>
<span data-ttu-id="0dfdb-116">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0dfdb-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dfdb-117">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0dfdb-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dfdb-118">입력</span><span class="sxs-lookup"><span data-stu-id="0dfdb-118">INPUTS</span></span>

## <span data-ttu-id="0dfdb-119">출력</span><span class="sxs-lookup"><span data-stu-id="0dfdb-119">OUTPUTS</span></span>

### <span data-ttu-id="0dfdb-120">Microsoft AzureStack. 관리. 미터법</span><span class="sxs-lookup"><span data-stu-id="0dfdb-120">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Metric</span></span>

## <span data-ttu-id="0dfdb-121">상속자</span><span class="sxs-lookup"><span data-stu-id="0dfdb-121">NOTES</span></span>

## <span data-ttu-id="0dfdb-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0dfdb-122">RELATED LINKS</span></span>

