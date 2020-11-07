---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 781b920bf955a84554b9152f54c9847a00a8b160
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93874641"
---
# <span data-ttu-id="cd0c8-101">Restart-AzsInfrastructureRole</span><span class="sxs-lookup"><span data-stu-id="cd0c8-101">Restart-AzsInfrastructureRole</span></span>

## <span data-ttu-id="cd0c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd0c8-102">SYNOPSIS</span></span>
<span data-ttu-id="cd0c8-103">Requestd 인프라 역할을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd0c8-103">Restarts the requestd infrastructure role.</span></span>

## <span data-ttu-id="cd0c8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cd0c8-104">SYNTAX</span></span>

### <span data-ttu-id="cd0c8-105">다시 시작 (기본값)</span><span class="sxs-lookup"><span data-stu-id="cd0c8-105">Restart (Default)</span></span>
```
Restart-AzsInfrastructureRole -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd0c8-106">리소스</span><span class="sxs-lookup"><span data-stu-id="cd0c8-106">ResourceId</span></span>
```
Restart-AzsInfrastructureRole -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd0c8-107">설명은</span><span class="sxs-lookup"><span data-stu-id="cd0c8-107">DESCRIPTION</span></span>
<span data-ttu-id="cd0c8-108">Requestd 인프라 역할을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd0c8-108">Restarts the requestd infrastructure role.</span></span>

## <span data-ttu-id="cd0c8-109">예제의</span><span class="sxs-lookup"><span data-stu-id="cd0c8-109">EXAMPLES</span></span>

### <span data-ttu-id="cd0c8-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="cd0c8-110">EXAMPLE 1</span></span>
```
Restart-AzsInfrastructureRole -Name "Active Directory Federation Services"
```

<span data-ttu-id="cd0c8-111">충돌 하는 인프라 역할을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd0c8-111">Restart an infrastructure role which has crashed.</span></span>

## <span data-ttu-id="cd0c8-112">변수</span><span class="sxs-lookup"><span data-stu-id="cd0c8-112">PARAMETERS</span></span>

### <span data-ttu-id="cd0c8-113">-이름</span><span class="sxs-lookup"><span data-stu-id="cd0c8-113">-Name</span></span>
<span data-ttu-id="cd0c8-114">인프라 역할 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="cd0c8-114">Infrastructure role name.</span></span>

```yaml
Type: String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd0c8-115">-위치</span><span class="sxs-lookup"><span data-stu-id="cd0c8-115">-Location</span></span>
<span data-ttu-id="cd0c8-116">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="cd0c8-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Restart
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd0c8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd0c8-117">-ResourceGroupName</span></span>
<span data-ttu-id="cd0c8-118">리소스 공급자가 등록 된 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="cd0c8-118">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Restart
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd0c8-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd0c8-119">-ResourceId</span></span>
<span data-ttu-id="cd0c8-120">인프라 역할 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="cd0c8-120">Infrastructure role resource ID.</span></span>

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

### <span data-ttu-id="cd0c8-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd0c8-121">-AsJob</span></span>
<span data-ttu-id="cd0c8-122">비동기를 작업으로 실행 하 고 작업 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd0c8-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="cd0c8-123">-Force</span><span class="sxs-lookup"><span data-stu-id="cd0c8-123">-Force</span></span>
<span data-ttu-id="cd0c8-124">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cd0c8-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="cd0c8-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd0c8-125">-WhatIf</span></span>
<span data-ttu-id="cd0c8-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cd0c8-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd0c8-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cd0c8-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd0c8-128">-확인</span><span class="sxs-lookup"><span data-stu-id="cd0c8-128">-Confirm</span></span>
<span data-ttu-id="cd0c8-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd0c8-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd0c8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd0c8-130">CommonParameters</span></span>
<span data-ttu-id="cd0c8-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cd0c8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd0c8-132">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd0c8-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd0c8-133">입력</span><span class="sxs-lookup"><span data-stu-id="cd0c8-133">INPUTS</span></span>

## <span data-ttu-id="cd0c8-134">출력</span><span class="sxs-lookup"><span data-stu-id="cd0c8-134">OUTPUTS</span></span>

## <span data-ttu-id="cd0c8-135">상속자</span><span class="sxs-lookup"><span data-stu-id="cd0c8-135">NOTES</span></span>

## <span data-ttu-id="cd0c8-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cd0c8-136">RELATED LINKS</span></span>
