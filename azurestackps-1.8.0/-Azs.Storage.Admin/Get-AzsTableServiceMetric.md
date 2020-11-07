---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 007f5116c17e9bf2c1df742e0f11c9a86844134b
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93874735"
---
# <span data-ttu-id="1f737-101">Get-AzsTableServiceMetric</span><span class="sxs-lookup"><span data-stu-id="1f737-101">Get-AzsTableServiceMetric</span></span>

## <span data-ttu-id="1f737-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f737-102">SYNOPSIS</span></span>
<span data-ttu-id="1f737-103">테이블 서비스에 대 한 메트릭 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f737-103">Returns a list of metrics for table service.</span></span>

## <span data-ttu-id="1f737-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1f737-104">SYNTAX</span></span>

```
Get-AzsTableServiceMetric [-FarmName] <String> [-ResourceGroupName <String>] [-Skip <Int32>] [-Top <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="1f737-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1f737-105">DESCRIPTION</span></span>
<span data-ttu-id="1f737-106">테이블 서비스에 대 한 메트릭 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f737-106">Returns a list of metrics for table service.</span></span>

## <span data-ttu-id="1f737-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1f737-107">EXAMPLES</span></span>

### <span data-ttu-id="1f737-108">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="1f737-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsTableServiceMetric -FarmName f9b8e2e2-e4b4-44e0-9d92-6a848b1a5376
```

<span data-ttu-id="1f737-109">테이블 서비스에 대 한 메트릭 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1f737-109">Get the list of metrics for table service.</span></span>

## <span data-ttu-id="1f737-110">변수</span><span class="sxs-lookup"><span data-stu-id="1f737-110">PARAMETERS</span></span>

### <span data-ttu-id="1f737-111">-FarmName</span><span class="sxs-lookup"><span data-stu-id="1f737-111">-FarmName</span></span>
<span data-ttu-id="1f737-112">팜 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="1f737-112">Farm Id.</span></span>

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

### <span data-ttu-id="1f737-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f737-113">-ResourceGroupName</span></span>
<span data-ttu-id="1f737-114">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1f737-114">Resource group name.</span></span>

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

### <span data-ttu-id="1f737-115">-생략</span><span class="sxs-lookup"><span data-stu-id="1f737-115">-Skip</span></span>
<span data-ttu-id="1f737-116">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="1f737-116">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="1f737-117">-위쪽</span><span class="sxs-lookup"><span data-stu-id="1f737-117">-Top</span></span>
<span data-ttu-id="1f737-118">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f737-118">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="1f737-119">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f737-119">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="1f737-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f737-120">CommonParameters</span></span>
<span data-ttu-id="1f737-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1f737-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f737-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f737-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f737-123">입력</span><span class="sxs-lookup"><span data-stu-id="1f737-123">INPUTS</span></span>

## <span data-ttu-id="1f737-124">출력</span><span class="sxs-lookup"><span data-stu-id="1f737-124">OUTPUTS</span></span>

### <span data-ttu-id="1f737-125">Microsoft AzureStack. 관리 모델. 미터법</span><span class="sxs-lookup"><span data-stu-id="1f737-125">Microsoft.AzureStack.Management.Storage.Admin.Models.Metric</span></span>

## <span data-ttu-id="1f737-126">상속자</span><span class="sxs-lookup"><span data-stu-id="1f737-126">NOTES</span></span>

## <span data-ttu-id="1f737-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1f737-127">RELATED LINKS</span></span>

