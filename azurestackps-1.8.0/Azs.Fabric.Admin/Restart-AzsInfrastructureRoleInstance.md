---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 03dfddb3ec666df5096184c5e00692862e091626
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93874649"
---
# <span data-ttu-id="e7826-101">Restart-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="e7826-101">Restart-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="e7826-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7826-102">SYNOPSIS</span></span>
<span data-ttu-id="e7826-103">인프라 역할 인스턴스를 다시 부팅 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7826-103">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="e7826-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e7826-104">SYNTAX</span></span>

### <span data-ttu-id="e7826-105">다시 시작 (기본값)</span><span class="sxs-lookup"><span data-stu-id="e7826-105">Restart (Default)</span></span>
```
Restart-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7826-106">리소스</span><span class="sxs-lookup"><span data-stu-id="e7826-106">ResourceId</span></span>
```
Restart-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e7826-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e7826-107">DESCRIPTION</span></span>
<span data-ttu-id="e7826-108">인프라 역할 인스턴스를 다시 부팅 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7826-108">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="e7826-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e7826-109">EXAMPLES</span></span>

### <span data-ttu-id="e7826-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="e7826-110">EXAMPLE 1</span></span>
```
Restart-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="e7826-111">인프라 역할 인스턴스를 다시 부팅 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7826-111">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="e7826-112">변수</span><span class="sxs-lookup"><span data-stu-id="e7826-112">PARAMETERS</span></span>

### <span data-ttu-id="e7826-113">-이름</span><span class="sxs-lookup"><span data-stu-id="e7826-113">-Name</span></span>
<span data-ttu-id="e7826-114">인프라 역할 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e7826-114">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="e7826-115">-위치</span><span class="sxs-lookup"><span data-stu-id="e7826-115">-Location</span></span>
<span data-ttu-id="e7826-116">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="e7826-116">Location of the resource.</span></span>

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

### <span data-ttu-id="e7826-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7826-117">-ResourceGroupName</span></span>
<span data-ttu-id="e7826-118">리소스 공급자가 등록 된 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="e7826-118">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="e7826-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7826-119">-ResourceId</span></span>
<span data-ttu-id="e7826-120">인프라 역할 인스턴스 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e7826-120">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="e7826-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e7826-121">-AsJob</span></span>
<span data-ttu-id="e7826-122">비동기를 작업으로 실행 하 고 작업 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7826-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="e7826-123">-Force</span><span class="sxs-lookup"><span data-stu-id="e7826-123">-Force</span></span>
<span data-ttu-id="e7826-124">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e7826-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="e7826-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7826-125">-WhatIf</span></span>
<span data-ttu-id="e7826-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e7826-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7826-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e7826-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7826-128">-확인</span><span class="sxs-lookup"><span data-stu-id="e7826-128">-Confirm</span></span>
<span data-ttu-id="e7826-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7826-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7826-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7826-130">CommonParameters</span></span>
<span data-ttu-id="e7826-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7826-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7826-132">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7826-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7826-133">입력</span><span class="sxs-lookup"><span data-stu-id="e7826-133">INPUTS</span></span>

## <span data-ttu-id="e7826-134">출력</span><span class="sxs-lookup"><span data-stu-id="e7826-134">OUTPUTS</span></span>

## <span data-ttu-id="e7826-135">상속자</span><span class="sxs-lookup"><span data-stu-id="e7826-135">NOTES</span></span>

## <span data-ttu-id="e7826-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e7826-136">RELATED LINKS</span></span>
