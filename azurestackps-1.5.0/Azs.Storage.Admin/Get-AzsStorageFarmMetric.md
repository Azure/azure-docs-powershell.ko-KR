---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 95ea9afa5d3dce953f4e51e84d011886e4ba5688
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523304"
---
# <span data-ttu-id="87aca-101">Get-AzsStorageFarmMetric</span><span class="sxs-lookup"><span data-stu-id="87aca-101">Get-AzsStorageFarmMetric</span></span>

## <span data-ttu-id="87aca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87aca-102">SYNOPSIS</span></span>
<span data-ttu-id="87aca-103">저장소 팜 메트릭의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="87aca-103">Returns a list of storage farm metrics.</span></span>

## <span data-ttu-id="87aca-104">구문과</span><span class="sxs-lookup"><span data-stu-id="87aca-104">SYNTAX</span></span>

```
Get-AzsStorageFarmMetric [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="87aca-105">설명은</span><span class="sxs-lookup"><span data-stu-id="87aca-105">DESCRIPTION</span></span>
<span data-ttu-id="87aca-106">저장소 팜 메트릭의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="87aca-106">Returns a list of storage farm metrics.</span></span>

## <span data-ttu-id="87aca-107">예제의</span><span class="sxs-lookup"><span data-stu-id="87aca-107">EXAMPLES</span></span>

### <span data-ttu-id="87aca-108">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="87aca-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageFarmMetric -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="87aca-109">저장소 팜 메트릭 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="87aca-109">Get the list of storage farm metrics.</span></span>

## <span data-ttu-id="87aca-110">변수</span><span class="sxs-lookup"><span data-stu-id="87aca-110">PARAMETERS</span></span>

### <span data-ttu-id="87aca-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="87aca-111">-FarmName</span></span>
<span data-ttu-id="87aca-112">팜 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="87aca-112">Farm Id.</span></span>

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

### <span data-ttu-id="87aca-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87aca-113">-ResourceGroupName</span></span>
<span data-ttu-id="87aca-114">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="87aca-114">Resource group name.</span></span>

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

### <span data-ttu-id="87aca-115">-생략</span><span class="sxs-lookup"><span data-stu-id="87aca-115">-Skip</span></span>
<span data-ttu-id="87aca-116">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="87aca-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="87aca-117">-위쪽</span><span class="sxs-lookup"><span data-stu-id="87aca-117">-Top</span></span>
<span data-ttu-id="87aca-118">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="87aca-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="87aca-119">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="87aca-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="87aca-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87aca-120">CommonParameters</span></span>
<span data-ttu-id="87aca-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="87aca-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87aca-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87aca-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87aca-123">입력</span><span class="sxs-lookup"><span data-stu-id="87aca-123">INPUTS</span></span>

## <span data-ttu-id="87aca-124">출력</span><span class="sxs-lookup"><span data-stu-id="87aca-124">OUTPUTS</span></span>

### <span data-ttu-id="87aca-125">Microsoft AzureStack. 관리 모델. 미터법</span><span class="sxs-lookup"><span data-stu-id="87aca-125">Microsoft.AzureStack.Management.Storage.Admin.Models.Metric</span></span>

## <span data-ttu-id="87aca-126">상속자</span><span class="sxs-lookup"><span data-stu-id="87aca-126">NOTES</span></span>

## <span data-ttu-id="87aca-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="87aca-127">RELATED LINKS</span></span>

