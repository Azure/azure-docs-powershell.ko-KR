---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 268a306597fe3760e8abc7e31f980da078bf2bc2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523783"
---
# <span data-ttu-id="bd5c7-101">Get-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="bd5c7-101">Get-AzsUpdateRun</span></span>

## <span data-ttu-id="bd5c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd5c7-102">SYNOPSIS</span></span>
<span data-ttu-id="bd5c7-103">업데이트 실행 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bd5c7-103">Get the list of update runs.</span></span>

## <span data-ttu-id="bd5c7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bd5c7-104">SYNTAX</span></span>

### <span data-ttu-id="bd5c7-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="bd5c7-105">List (Default)</span></span>
```
Get-AzsUpdateRun -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>] [-Skip <Int32>]
 [-Top <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="bd5c7-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="bd5c7-106">Get</span></span>
```
Get-AzsUpdateRun -Name <String> -UpdateName <String> [-Location <String>] [-ResourceGroupName <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="bd5c7-107">리소스</span><span class="sxs-lookup"><span data-stu-id="bd5c7-107">ResourceId</span></span>
```
Get-AzsUpdateRun -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="bd5c7-108">설명은</span><span class="sxs-lookup"><span data-stu-id="bd5c7-108">DESCRIPTION</span></span>
<span data-ttu-id="bd5c7-109">업데이트 실행 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bd5c7-109">Get the list of update runs.</span></span> <span data-ttu-id="bd5c7-110">반환 되는 UpdateRun 개체의 인스턴스는 해당 되는 경우 다시 시작 하도록 파이프 될 수 있습니다 (AzsUpdateRun).</span><span class="sxs-lookup"><span data-stu-id="bd5c7-110">Instances of the UpdateRun objects returned can be piped to Restart-AzsUpdateRun, when applicable.</span></span>

## <span data-ttu-id="bd5c7-111">예제의</span><span class="sxs-lookup"><span data-stu-id="bd5c7-111">EXAMPLES</span></span>

### <span data-ttu-id="bd5c7-112">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="bd5c7-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUpdateRun -UpdateName Microsoft1.0.180302.1
```

<span data-ttu-id="bd5c7-113">특정 업데이트를 적용 하기 위한 모든 시도 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bd5c7-113">Get a list of all attempts to apply a specific update.</span></span>

## <span data-ttu-id="bd5c7-114">변수</span><span class="sxs-lookup"><span data-stu-id="bd5c7-114">PARAMETERS</span></span>

### <span data-ttu-id="bd5c7-115">-위치</span><span class="sxs-lookup"><span data-stu-id="bd5c7-115">-Location</span></span>
<span data-ttu-id="bd5c7-116">업데이트 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bd5c7-116">The name of the update location.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd5c7-117">-이름</span><span class="sxs-lookup"><span data-stu-id="bd5c7-117">-Name</span></span>
<span data-ttu-id="bd5c7-118">업데이트 실행 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="bd5c7-118">Update run identifier.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd5c7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd5c7-119">-ResourceGroupName</span></span>
<span data-ttu-id="bd5c7-120">리소스가 있는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="bd5c7-120">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd5c7-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bd5c7-121">-ResourceId</span></span>
<span data-ttu-id="bd5c7-122">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="bd5c7-122">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bd5c7-123">-생략</span><span class="sxs-lookup"><span data-stu-id="bd5c7-123">-Skip</span></span>
<span data-ttu-id="bd5c7-124">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="bd5c7-124">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd5c7-125">-위쪽</span><span class="sxs-lookup"><span data-stu-id="bd5c7-125">-Top</span></span>
<span data-ttu-id="bd5c7-126">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd5c7-126">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="bd5c7-127">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bd5c7-127">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd5c7-128">-UpdateName</span><span class="sxs-lookup"><span data-stu-id="bd5c7-128">-UpdateName</span></span>
<span data-ttu-id="bd5c7-129">업데이트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bd5c7-129">Name of the update.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd5c7-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd5c7-130">CommonParameters</span></span>
<span data-ttu-id="bd5c7-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd5c7-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd5c7-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd5c7-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd5c7-133">입력</span><span class="sxs-lookup"><span data-stu-id="bd5c7-133">INPUTS</span></span>

## <span data-ttu-id="bd5c7-134">출력</span><span class="sxs-lookup"><span data-stu-id="bd5c7-134">OUTPUTS</span></span>

### <span data-ttu-id="bd5c7-135">UpdateRun. 관리자. m m/. 관리</span><span class="sxs-lookup"><span data-stu-id="bd5c7-135">Microsoft.AzureStack.Management.Update.Admin.Models.UpdateRun</span></span>

## <span data-ttu-id="bd5c7-136">상속자</span><span class="sxs-lookup"><span data-stu-id="bd5c7-136">NOTES</span></span>

## <span data-ttu-id="bd5c7-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bd5c7-137">RELATED LINKS</span></span>

