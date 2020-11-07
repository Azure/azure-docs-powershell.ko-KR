---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 94609250696a99a337153e9e0d3a1d092e380c40
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93874833"
---
# <span data-ttu-id="797a2-101">Remove-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="797a2-101">Remove-AzsNetworkQuota</span></span>

## <span data-ttu-id="797a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="797a2-102">SYNOPSIS</span></span>
<span data-ttu-id="797a2-103">이름으로 할당량을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="797a2-103">Delete a quota by name.</span></span>

## <span data-ttu-id="797a2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="797a2-104">SYNTAX</span></span>

### <span data-ttu-id="797a2-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="797a2-105">Delete (Default)</span></span>
```
Remove-AzsNetworkQuota -Name <String> [-Location <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="797a2-106">리소스</span><span class="sxs-lookup"><span data-stu-id="797a2-106">ResourceId</span></span>
```
Remove-AzsNetworkQuota -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="797a2-107">설명은</span><span class="sxs-lookup"><span data-stu-id="797a2-107">DESCRIPTION</span></span>
<span data-ttu-id="797a2-108">이름으로 할당량을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="797a2-108">Delete a quota by name.</span></span>

## <span data-ttu-id="797a2-109">예제의</span><span class="sxs-lookup"><span data-stu-id="797a2-109">EXAMPLES</span></span>

### <span data-ttu-id="797a2-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="797a2-110">EXAMPLE 1</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="797a2-111">이름으로 네트워크 할당량을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="797a2-111">Remove a network quota by name.</span></span>

### <span data-ttu-id="797a2-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="797a2-112">EXAMPLE 2</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1 | Remove-AzsNetworkQuota
```

<span data-ttu-id="797a2-113">파이프를 사용 하 여 네트워크 할당량을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="797a2-113">Remove a network quota using a pipe.</span></span>

### <span data-ttu-id="797a2-114">예제 3</span><span class="sxs-lookup"><span data-stu-id="797a2-114">EXAMPLE 3</span></span>
```
Remove-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="797a2-115">네트워크 할당량을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="797a2-115">Remove a network quota.</span></span>

## <span data-ttu-id="797a2-116">변수</span><span class="sxs-lookup"><span data-stu-id="797a2-116">PARAMETERS</span></span>

### <span data-ttu-id="797a2-117">-이름</span><span class="sxs-lookup"><span data-stu-id="797a2-117">-Name</span></span>
<span data-ttu-id="797a2-118">리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="797a2-118">Name of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="797a2-119">-위치</span><span class="sxs-lookup"><span data-stu-id="797a2-119">-Location</span></span>
<span data-ttu-id="797a2-120">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="797a2-120">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="797a2-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="797a2-121">-ResourceId</span></span>
<span data-ttu-id="797a2-122">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="797a2-122">The resource id.</span></span>

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

### <span data-ttu-id="797a2-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="797a2-123">-AsJob</span></span>
<span data-ttu-id="797a2-124">비동기를 작업으로 실행 하 고 작업 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="797a2-124">Run asynchronous as a job and return the job object.</span></span>


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

### <span data-ttu-id="797a2-125">-Force</span><span class="sxs-lookup"><span data-stu-id="797a2-125">-Force</span></span>
<span data-ttu-id="797a2-126">확인을 묻지 않도록 매개 변수를 전환 합니다.</span><span class="sxs-lookup"><span data-stu-id="797a2-126">Switch parameter for not asking confirmation.</span></span>

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

### <span data-ttu-id="797a2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="797a2-127">-WhatIf</span></span>
<span data-ttu-id="797a2-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="797a2-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="797a2-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="797a2-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="797a2-130">-확인</span><span class="sxs-lookup"><span data-stu-id="797a2-130">-Confirm</span></span>
<span data-ttu-id="797a2-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="797a2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="797a2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="797a2-132">CommonParameters</span></span>
<span data-ttu-id="797a2-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="797a2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="797a2-134">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="797a2-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="797a2-135">입력</span><span class="sxs-lookup"><span data-stu-id="797a2-135">INPUTS</span></span>

## <span data-ttu-id="797a2-136">출력</span><span class="sxs-lookup"><span data-stu-id="797a2-136">OUTPUTS</span></span>

## <span data-ttu-id="797a2-137">상속자</span><span class="sxs-lookup"><span data-stu-id="797a2-137">NOTES</span></span>

## <span data-ttu-id="797a2-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="797a2-138">RELATED LINKS</span></span>
