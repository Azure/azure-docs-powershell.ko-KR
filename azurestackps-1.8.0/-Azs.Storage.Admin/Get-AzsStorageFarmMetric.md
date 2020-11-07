---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 95ea9afa5d3dce953f4e51e84d011886e4ba5688
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93874871"
---
# <span data-ttu-id="4fb5d-101">Get-AzsStorageFarmMetric</span><span class="sxs-lookup"><span data-stu-id="4fb5d-101">Get-AzsStorageFarmMetric</span></span>

## <span data-ttu-id="4fb5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fb5d-102">SYNOPSIS</span></span>
<span data-ttu-id="4fb5d-103">저장소 팜 메트릭의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fb5d-103">Returns a list of storage farm metrics.</span></span>

## <span data-ttu-id="4fb5d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4fb5d-104">SYNTAX</span></span>

```
Get-AzsStorageFarmMetric [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="4fb5d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4fb5d-105">DESCRIPTION</span></span>
<span data-ttu-id="4fb5d-106">저장소 팜 메트릭의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fb5d-106">Returns a list of storage farm metrics.</span></span>

## <span data-ttu-id="4fb5d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4fb5d-107">EXAMPLES</span></span>

### <span data-ttu-id="4fb5d-108">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="4fb5d-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageFarmMetric -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="4fb5d-109">저장소 팜 메트릭 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4fb5d-109">Get the list of storage farm metrics.</span></span>

## <span data-ttu-id="4fb5d-110">변수</span><span class="sxs-lookup"><span data-stu-id="4fb5d-110">PARAMETERS</span></span>

### <span data-ttu-id="4fb5d-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="4fb5d-111">-FarmName</span></span>
<span data-ttu-id="4fb5d-112">팜 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="4fb5d-112">Farm Id.</span></span>

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

### <span data-ttu-id="4fb5d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fb5d-113">-ResourceGroupName</span></span>
<span data-ttu-id="4fb5d-114">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4fb5d-114">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fb5d-115">-생략</span><span class="sxs-lookup"><span data-stu-id="4fb5d-115">-Skip</span></span>
<span data-ttu-id="4fb5d-116">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="4fb5d-116">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fb5d-117">-위쪽</span><span class="sxs-lookup"><span data-stu-id="4fb5d-117">-Top</span></span>
<span data-ttu-id="4fb5d-118">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fb5d-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="4fb5d-119">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4fb5d-119">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fb5d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fb5d-120">CommonParameters</span></span>
<span data-ttu-id="4fb5d-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fb5d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fb5d-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fb5d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fb5d-123">입력</span><span class="sxs-lookup"><span data-stu-id="4fb5d-123">INPUTS</span></span>

## <span data-ttu-id="4fb5d-124">출력</span><span class="sxs-lookup"><span data-stu-id="4fb5d-124">OUTPUTS</span></span>

### <span data-ttu-id="4fb5d-125">Microsoft AzureStack. 관리 모델. 미터법</span><span class="sxs-lookup"><span data-stu-id="4fb5d-125">Microsoft.AzureStack.Management.Storage.Admin.Models.Metric</span></span>

## <span data-ttu-id="4fb5d-126">상속자</span><span class="sxs-lookup"><span data-stu-id="4fb5d-126">NOTES</span></span>

## <span data-ttu-id="4fb5d-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4fb5d-127">RELATED LINKS</span></span>

