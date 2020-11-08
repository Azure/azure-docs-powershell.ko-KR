---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2e80ea57424b350a1255a2a19c7bea8c22c34c71
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94047053"
---
# <span data-ttu-id="fe899-101">Get-AzsBlobServiceMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="fe899-101">Get-AzsBlobServiceMetricDefinition</span></span>

## <span data-ttu-id="fe899-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe899-102">SYNOPSIS</span></span>
<span data-ttu-id="fe899-103">Blob 서비스에 대 한 메트릭 정의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe899-103">Returns the list of metric definitions for blob service.</span></span>

## <span data-ttu-id="fe899-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fe899-104">SYNTAX</span></span>

```
Get-AzsBlobServiceMetricDefinition [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="fe899-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fe899-105">DESCRIPTION</span></span>
<span data-ttu-id="fe899-106">Blob 서비스에 대 한 메트릭 정의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe899-106">Returns the list of metric definitions for blob service.</span></span>

## <span data-ttu-id="fe899-107">예제의</span><span class="sxs-lookup"><span data-stu-id="fe899-107">EXAMPLES</span></span>

### <span data-ttu-id="fe899-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="fe899-108">EXAMPLE 1</span></span>
```
Get-AzsBlobServiceMetricDefinition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="fe899-109">Blob 서비스에 대 한 메트릭 정의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fe899-109">Get a list of metric definitions for the blob service.</span></span>

## <span data-ttu-id="fe899-110">변수</span><span class="sxs-lookup"><span data-stu-id="fe899-110">PARAMETERS</span></span>

### <span data-ttu-id="fe899-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="fe899-111">-FarmName</span></span>
<span data-ttu-id="fe899-112">팜 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="fe899-112">Farm Id.</span></span>

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

### <span data-ttu-id="fe899-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe899-113">-ResourceGroupName</span></span>
<span data-ttu-id="fe899-114">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fe899-114">Resource group name.</span></span>

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

### <span data-ttu-id="fe899-115">-생략</span><span class="sxs-lookup"><span data-stu-id="fe899-115">-Skip</span></span>
<span data-ttu-id="fe899-116">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="fe899-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="fe899-117">-위쪽</span><span class="sxs-lookup"><span data-stu-id="fe899-117">-Top</span></span>
<span data-ttu-id="fe899-118">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe899-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="fe899-119">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fe899-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="fe899-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe899-120">CommonParameters</span></span>
<span data-ttu-id="fe899-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe899-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe899-122">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe899-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe899-123">입력</span><span class="sxs-lookup"><span data-stu-id="fe899-123">INPUTS</span></span>

## <span data-ttu-id="fe899-124">출력</span><span class="sxs-lookup"><span data-stu-id="fe899-124">OUTPUTS</span></span>

### <span data-ttu-id="fe899-125">MetricDefinition. 관리자. m a 관리</span><span class="sxs-lookup"><span data-stu-id="fe899-125">Microsoft.AzureStack.Management.Storage.Admin.Models.MetricDefinition</span></span>

## <span data-ttu-id="fe899-126">상속자</span><span class="sxs-lookup"><span data-stu-id="fe899-126">NOTES</span></span>

## <span data-ttu-id="fe899-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fe899-127">RELATED LINKS</span></span>
