---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f5d91226a4762c5f1429d8d05b48defd83b4e2df
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93875182"
---
# <span data-ttu-id="574ce-101">Get-AzsTableServiceMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="574ce-101">Get-AzsTableServiceMetricDefinition</span></span>

## <span data-ttu-id="574ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="574ce-102">SYNOPSIS</span></span>
<span data-ttu-id="574ce-103">테이블 서비스에 대 한 메트릭 정의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="574ce-103">Returns a list of metric definitions for table service.</span></span>

## <span data-ttu-id="574ce-104">구문과</span><span class="sxs-lookup"><span data-stu-id="574ce-104">SYNTAX</span></span>

```
Get-AzsTableServiceMetricDefinition [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="574ce-105">설명은</span><span class="sxs-lookup"><span data-stu-id="574ce-105">DESCRIPTION</span></span>
<span data-ttu-id="574ce-106">테이블 서비스에 대 한 메트릭 정의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="574ce-106">Returns a list of metric definitions for table service.</span></span>

## <span data-ttu-id="574ce-107">예제의</span><span class="sxs-lookup"><span data-stu-id="574ce-107">EXAMPLES</span></span>

### <span data-ttu-id="574ce-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="574ce-108">EXAMPLE 1</span></span>
```
Get-AzsTableServiceMetricDefinition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="574ce-109">테이블 서비스에 대 한 메트릭 정의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="574ce-109">Get the list of metric definitions for table service.</span></span>

## <span data-ttu-id="574ce-110">변수</span><span class="sxs-lookup"><span data-stu-id="574ce-110">PARAMETERS</span></span>

### <span data-ttu-id="574ce-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="574ce-111">-FarmName</span></span>
<span data-ttu-id="574ce-112">팜 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="574ce-112">Farm Id.</span></span>

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

### <span data-ttu-id="574ce-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="574ce-113">-ResourceGroupName</span></span>
<span data-ttu-id="574ce-114">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="574ce-114">Resource group name.</span></span>

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

### <span data-ttu-id="574ce-115">-생략</span><span class="sxs-lookup"><span data-stu-id="574ce-115">-Skip</span></span>
<span data-ttu-id="574ce-116">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="574ce-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="574ce-117">-위쪽</span><span class="sxs-lookup"><span data-stu-id="574ce-117">-Top</span></span>
<span data-ttu-id="574ce-118">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="574ce-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="574ce-119">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="574ce-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="574ce-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="574ce-120">CommonParameters</span></span>
<span data-ttu-id="574ce-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="574ce-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="574ce-122">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="574ce-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="574ce-123">입력</span><span class="sxs-lookup"><span data-stu-id="574ce-123">INPUTS</span></span>

## <span data-ttu-id="574ce-124">출력</span><span class="sxs-lookup"><span data-stu-id="574ce-124">OUTPUTS</span></span>

### <span data-ttu-id="574ce-125">MetricDefinition. 관리자. m a 관리</span><span class="sxs-lookup"><span data-stu-id="574ce-125">Microsoft.AzureStack.Management.Storage.Admin.Models.MetricDefinition</span></span>

## <span data-ttu-id="574ce-126">상속자</span><span class="sxs-lookup"><span data-stu-id="574ce-126">NOTES</span></span>

## <span data-ttu-id="574ce-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="574ce-127">RELATED LINKS</span></span>
