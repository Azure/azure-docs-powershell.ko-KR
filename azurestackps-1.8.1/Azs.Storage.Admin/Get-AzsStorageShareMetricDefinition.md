---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e127b0cb9198471d237df62bfedf8d2d57ecdca2
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93875197"
---
# <span data-ttu-id="45988-101">Get-AzsStorageShareMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="45988-101">Get-AzsStorageShareMetricDefinition</span></span>

## <span data-ttu-id="45988-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45988-102">SYNOPSIS</span></span>
<span data-ttu-id="45988-103">저장소 공유에 대 한 메트릭 정의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="45988-103">Returns a list of metric definitions for a storage share.</span></span>

## <span data-ttu-id="45988-104">구문과</span><span class="sxs-lookup"><span data-stu-id="45988-104">SYNTAX</span></span>

```
Get-AzsStorageShareMetricDefinition [-FarmName] <String> [-ShareName] <String> [[-ResourceGroupName] <String>]
 [[-Skip] <Int32>] [[-Top] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="45988-105">설명은</span><span class="sxs-lookup"><span data-stu-id="45988-105">DESCRIPTION</span></span>
<span data-ttu-id="45988-106">저장소 공유에 대 한 메트릭 정의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="45988-106">Returns a list of metric definitions for a storage share.</span></span>

## <span data-ttu-id="45988-107">예제의</span><span class="sxs-lookup"><span data-stu-id="45988-107">EXAMPLES</span></span>

### <span data-ttu-id="45988-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="45988-108">EXAMPLE 1</span></span>
```
Get-AzsStorageShareMetricDefinition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -ShareName "||SU1FileServer.azurestack.local|SU1_ObjStore"
```

<span data-ttu-id="45988-109">저장소 공유에 대 한 메트릭 정의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="45988-109">Get the list of metric definitions for a storage share.</span></span>

## <span data-ttu-id="45988-110">변수</span><span class="sxs-lookup"><span data-stu-id="45988-110">PARAMETERS</span></span>

### <span data-ttu-id="45988-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="45988-111">-FarmName</span></span>
<span data-ttu-id="45988-112">팜 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="45988-112">Farm Id.</span></span>

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

### <span data-ttu-id="45988-113">-ShareName</span><span class="sxs-lookup"><span data-stu-id="45988-113">-ShareName</span></span>
<span data-ttu-id="45988-114">공유 이름.</span><span class="sxs-lookup"><span data-stu-id="45988-114">Share name.</span></span>

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

### <span data-ttu-id="45988-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45988-115">-ResourceGroupName</span></span>
<span data-ttu-id="45988-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="45988-116">Resource group name.</span></span>

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

### <span data-ttu-id="45988-117">-생략</span><span class="sxs-lookup"><span data-stu-id="45988-117">-Skip</span></span>
<span data-ttu-id="45988-118">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="45988-118">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45988-119">-위쪽</span><span class="sxs-lookup"><span data-stu-id="45988-119">-Top</span></span>
<span data-ttu-id="45988-120">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="45988-120">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="45988-121">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="45988-121">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45988-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45988-122">CommonParameters</span></span>
<span data-ttu-id="45988-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="45988-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45988-124">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45988-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45988-125">입력</span><span class="sxs-lookup"><span data-stu-id="45988-125">INPUTS</span></span>

## <span data-ttu-id="45988-126">출력</span><span class="sxs-lookup"><span data-stu-id="45988-126">OUTPUTS</span></span>

### <span data-ttu-id="45988-127">MetricDefinition. 관리자. m a 관리</span><span class="sxs-lookup"><span data-stu-id="45988-127">Microsoft.AzureStack.Management.Storage.Admin.Models.MetricDefinition</span></span>

## <span data-ttu-id="45988-128">상속자</span><span class="sxs-lookup"><span data-stu-id="45988-128">NOTES</span></span>

## <span data-ttu-id="45988-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="45988-129">RELATED LINKS</span></span>
