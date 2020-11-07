---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 646ee96dec361ac6318b4cfe48b80ec4c3686321
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93874862"
---
# <span data-ttu-id="0a44b-101">Get-AzsStorageShareMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="0a44b-101">Get-AzsStorageShareMetricDefinition</span></span>

## <span data-ttu-id="0a44b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a44b-102">SYNOPSIS</span></span>
<span data-ttu-id="0a44b-103">저장소 공유에 대 한 메트릭 정의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a44b-103">Returns a list of metric definitions for a storage share.</span></span>

## <span data-ttu-id="0a44b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0a44b-104">SYNTAX</span></span>

```
Get-AzsStorageShareMetricDefinition [-FarmName] <String> [-Name] <String> [[-ResourceGroupName] <String>]
 [[-Skip] <Int32>] [[-Top] <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="0a44b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0a44b-105">DESCRIPTION</span></span>
<span data-ttu-id="0a44b-106">저장소 공유에 대 한 메트릭 정의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a44b-106">Returns a list of metric definitions for a storage share.</span></span>

## <span data-ttu-id="0a44b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0a44b-107">EXAMPLES</span></span>

### <span data-ttu-id="0a44b-108">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0a44b-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsStorageShareMetricDefinition -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376 -Name "||SU1FileServer.azurestack.local|SU1_ObjStore"
```

<span data-ttu-id="0a44b-109">저장소 공유에 대 한 메트릭 정의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0a44b-109">Get the list of metric definitions for a storage share.</span></span>

## <span data-ttu-id="0a44b-110">변수</span><span class="sxs-lookup"><span data-stu-id="0a44b-110">PARAMETERS</span></span>

### <span data-ttu-id="0a44b-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="0a44b-111">-FarmName</span></span>
<span data-ttu-id="0a44b-112">팜 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="0a44b-112">Farm Id.</span></span>

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

### <span data-ttu-id="0a44b-113">-이름</span><span class="sxs-lookup"><span data-stu-id="0a44b-113">-Name</span></span>
<span data-ttu-id="0a44b-114">공유 이름.</span><span class="sxs-lookup"><span data-stu-id="0a44b-114">Share name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a44b-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a44b-115">-ResourceGroupName</span></span>
<span data-ttu-id="0a44b-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0a44b-116">Resource group name.</span></span>

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

### <span data-ttu-id="0a44b-117">-생략</span><span class="sxs-lookup"><span data-stu-id="0a44b-117">-Skip</span></span>
<span data-ttu-id="0a44b-118">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="0a44b-118">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="0a44b-119">-위쪽</span><span class="sxs-lookup"><span data-stu-id="0a44b-119">-Top</span></span>
<span data-ttu-id="0a44b-120">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a44b-120">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="0a44b-121">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0a44b-121">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="0a44b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a44b-122">CommonParameters</span></span>
<span data-ttu-id="0a44b-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a44b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a44b-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a44b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a44b-125">입력</span><span class="sxs-lookup"><span data-stu-id="0a44b-125">INPUTS</span></span>

## <span data-ttu-id="0a44b-126">출력</span><span class="sxs-lookup"><span data-stu-id="0a44b-126">OUTPUTS</span></span>

### <span data-ttu-id="0a44b-127">MetricDefinition. 관리자. m a 관리</span><span class="sxs-lookup"><span data-stu-id="0a44b-127">Microsoft.AzureStack.Management.Storage.Admin.Models.MetricDefinition</span></span>

## <span data-ttu-id="0a44b-128">상속자</span><span class="sxs-lookup"><span data-stu-id="0a44b-128">NOTES</span></span>

## <span data-ttu-id="0a44b-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0a44b-129">RELATED LINKS</span></span>

