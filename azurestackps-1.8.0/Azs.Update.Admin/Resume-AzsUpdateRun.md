---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb3b784d079d1de3cec1d4fe3ec50a2853a4b054
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93874592"
---
# <span data-ttu-id="7c48c-101">Resume-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="7c48c-101">Resume-AzsUpdateRun</span></span>

## <span data-ttu-id="7c48c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c48c-102">SYNOPSIS</span></span>
<span data-ttu-id="7c48c-103">이전에 시작 된 업데이트 실행이 실패 한 경우 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c48c-103">Resumes a previously started update run that failed.</span></span>

## <span data-ttu-id="7c48c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7c48c-104">SYNTAX</span></span>

### <span data-ttu-id="7c48c-105">UpdateRuns_Rerun (기본값)</span><span class="sxs-lookup"><span data-stu-id="7c48c-105">UpdateRuns_Rerun (Default)</span></span>
```
Resume-AzsUpdateRun -Name <String> [-Location <String>] [-ResourceGroupName <String>] -UpdateName <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c48c-106">리소스</span><span class="sxs-lookup"><span data-stu-id="7c48c-106">ResourceId</span></span>
```
Resume-AzsUpdateRun [-AsJob] -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c48c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7c48c-107">DESCRIPTION</span></span>
<span data-ttu-id="7c48c-108">이전에 시작 된 업데이트 실행이 실패 한 경우 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c48c-108">Resumes a previously started update run that failed.</span></span> <span data-ttu-id="7c48c-109">Resumeed update 실행은 마지막으로 실패 한 시점에 다시 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7c48c-109">Resumeed update runs will resume at the point they last failed.</span></span>

## <span data-ttu-id="7c48c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="7c48c-110">EXAMPLES</span></span>

### <span data-ttu-id="7c48c-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="7c48c-111">EXAMPLE 1</span></span>
```
Get-AzsUpdateRun -Name 5173e9f4-3040-494f-b7a7-738a6331d55c -UpdateName Microsoft1.0.180305.1 | Resume-AzsUpdateRun
```

<span data-ttu-id="7c48c-112">이전에 시작 된 업데이트 실행이 실패 한 경우 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c48c-112">Resumes a previously started update run that failed.</span></span>

## <span data-ttu-id="7c48c-113">변수</span><span class="sxs-lookup"><span data-stu-id="7c48c-113">PARAMETERS</span></span>

### <span data-ttu-id="7c48c-114">-이름</span><span class="sxs-lookup"><span data-stu-id="7c48c-114">-Name</span></span>
<span data-ttu-id="7c48c-115">업데이트 실행 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="7c48c-115">Update run identifier.</span></span>

```yaml
Type: String
Parameter Sets: UpdateRuns_Rerun
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c48c-116">-위치</span><span class="sxs-lookup"><span data-stu-id="7c48c-116">-Location</span></span>
<span data-ttu-id="7c48c-117">업데이트 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c48c-117">The name of the update location.</span></span>

```yaml
Type: String
Parameter Sets: UpdateRuns_Rerun
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c48c-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c48c-118">-ResourceGroupName</span></span>
<span data-ttu-id="7c48c-119">리소스가 있는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="7c48c-119">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: UpdateRuns_Rerun
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c48c-120">-UpdateName</span><span class="sxs-lookup"><span data-stu-id="7c48c-120">-UpdateName</span></span>
<span data-ttu-id="7c48c-121">업데이트의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c48c-121">Display name of the update.</span></span>

```yaml
Type: String
Parameter Sets: UpdateRuns_Rerun
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c48c-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7c48c-122">-AsJob</span></span>
<span data-ttu-id="7c48c-123">비동기를 작업으로 실행 하 고 작업 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c48c-123">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c48c-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c48c-124">-ResourceId</span></span>
<span data-ttu-id="7c48c-125">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="7c48c-125">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c48c-126">-Force</span><span class="sxs-lookup"><span data-stu-id="7c48c-126">-Force</span></span>
<span data-ttu-id="7c48c-127">확인 하지 않고 항목을 제거 하는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="7c48c-127">Flag to remove the item without confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c48c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c48c-128">-WhatIf</span></span>
<span data-ttu-id="7c48c-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7c48c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c48c-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7c48c-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c48c-131">-확인</span><span class="sxs-lookup"><span data-stu-id="7c48c-131">-Confirm</span></span>
<span data-ttu-id="7c48c-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c48c-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c48c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c48c-133">CommonParameters</span></span>
<span data-ttu-id="7c48c-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c48c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c48c-135">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c48c-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c48c-136">입력</span><span class="sxs-lookup"><span data-stu-id="7c48c-136">INPUTS</span></span>

## <span data-ttu-id="7c48c-137">출력</span><span class="sxs-lookup"><span data-stu-id="7c48c-137">OUTPUTS</span></span>

## <span data-ttu-id="7c48c-138">상속자</span><span class="sxs-lookup"><span data-stu-id="7c48c-138">NOTES</span></span>

## <span data-ttu-id="7c48c-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7c48c-139">RELATED LINKS</span></span>
