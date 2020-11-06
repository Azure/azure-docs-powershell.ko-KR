---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.InfrastructureInsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7b06ae4189b427686f4237c1a6eae841fcaba5c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523596"
---
# <span data-ttu-id="fd263-101">Repair-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="fd263-101">Repair-AzsAlert</span></span>

## <span data-ttu-id="fd263-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd263-102">SYNOPSIS</span></span>
<span data-ttu-id="fd263-103">지정 된 알림을 복구 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd263-103">Repairs the given alert.</span></span>

## <span data-ttu-id="fd263-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fd263-104">SYNTAX</span></span>

### <span data-ttu-id="fd263-105">복구 (기본값)</span><span class="sxs-lookup"><span data-stu-id="fd263-105">Repair (Default)</span></span>
```
Repair-AzsAlert -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fd263-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="fd263-106">InputObject</span></span>
```
Repair-AzsAlert -InputObject <Alert> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fd263-107">설명은</span><span class="sxs-lookup"><span data-stu-id="fd263-107">DESCRIPTION</span></span>
<span data-ttu-id="fd263-108">지정 된 알림을 복구 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd263-108">Repairs the given alert.</span></span>

## <span data-ttu-id="fd263-109">예제의</span><span class="sxs-lookup"><span data-stu-id="fd263-109">EXAMPLES</span></span>

### <span data-ttu-id="fd263-110">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="fd263-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Repair-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="fd263-111">이름으로 알림을 복구 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd263-111">Repairs an alert by Name.</span></span>

### <span data-ttu-id="fd263-112">--------------------------예제 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="fd263-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Repair-AzsAlert
```

<span data-ttu-id="fd263-113">파이핑을 통해 알림을 복구 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd263-113">Repairs an alert through piping.</span></span>

## <span data-ttu-id="fd263-114">변수</span><span class="sxs-lookup"><span data-stu-id="fd263-114">PARAMETERS</span></span>

### <span data-ttu-id="fd263-115">-Force</span><span class="sxs-lookup"><span data-stu-id="fd263-115">-Force</span></span>
<span data-ttu-id="fd263-116">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fd263-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="fd263-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd263-117">-InputObject</span></span>
<span data-ttu-id="fd263-118">Get-AzsAlert에서 반환 된 알림</span><span class="sxs-lookup"><span data-stu-id="fd263-118">An alert returned from Get-AzsAlert.</span></span>

```yaml
Type: Alert
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd263-119">-위치</span><span class="sxs-lookup"><span data-stu-id="fd263-119">-Location</span></span>
<span data-ttu-id="fd263-120">위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fd263-120">Name of the location.</span></span>

```yaml
Type: String
Parameter Sets: Repair
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd263-121">-이름</span><span class="sxs-lookup"><span data-stu-id="fd263-121">-Name</span></span>
<span data-ttu-id="fd263-122">경고 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="fd263-122">The alert identifier.</span></span>

```yaml
Type: String
Parameter Sets: Repair
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd263-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd263-123">-ResourceGroupName</span></span>
<span data-ttu-id="fd263-124">리소스가 있는 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fd263-124">Resource group name which the resource resides.</span></span>

```yaml
Type: String
Parameter Sets: Repair
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd263-125">-확인</span><span class="sxs-lookup"><span data-stu-id="fd263-125">-Confirm</span></span>
<span data-ttu-id="fd263-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd263-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd263-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd263-127">-WhatIf</span></span>
<span data-ttu-id="fd263-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fd263-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fd263-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fd263-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd263-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd263-130">CommonParameters</span></span>
<span data-ttu-id="fd263-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd263-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd263-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd263-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd263-133">입력</span><span class="sxs-lookup"><span data-stu-id="fd263-133">INPUTS</span></span>

## <span data-ttu-id="fd263-134">출력</span><span class="sxs-lookup"><span data-stu-id="fd263-134">OUTPUTS</span></span>

## <span data-ttu-id="fd263-135">상속자</span><span class="sxs-lookup"><span data-stu-id="fd263-135">NOTES</span></span>

## <span data-ttu-id="fd263-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fd263-136">RELATED LINKS</span></span>

