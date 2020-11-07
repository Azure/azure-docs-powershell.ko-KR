---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 48f7fd6280596e70810d330f3fe69b37059e15cd
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93874928"
---
# <span data-ttu-id="c7ef3-101">Start-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="c7ef3-101">Start-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="c7ef3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7ef3-102">SYNOPSIS</span></span>
<span data-ttu-id="c7ef3-103">인프라 역할 인스턴스의 기능을 켭니다.</span><span class="sxs-lookup"><span data-stu-id="c7ef3-103">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="c7ef3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c7ef3-104">SYNTAX</span></span>

### <span data-ttu-id="c7ef3-105">PowerOn (기본값)</span><span class="sxs-lookup"><span data-stu-id="c7ef3-105">PowerOn (Default)</span></span>
```
Start-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7ef3-106">리소스</span><span class="sxs-lookup"><span data-stu-id="c7ef3-106">ResourceId</span></span>
```
Start-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c7ef3-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c7ef3-107">DESCRIPTION</span></span>
<span data-ttu-id="c7ef3-108">인프라 역할 인스턴스의 기능을 켭니다.</span><span class="sxs-lookup"><span data-stu-id="c7ef3-108">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="c7ef3-109">예제의</span><span class="sxs-lookup"><span data-stu-id="c7ef3-109">EXAMPLES</span></span>

### <span data-ttu-id="c7ef3-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="c7ef3-110">EXAMPLE 1</span></span>
```
Start-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="c7ef3-111">인프라 역할 인스턴스의 기능을 켭니다.</span><span class="sxs-lookup"><span data-stu-id="c7ef3-111">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="c7ef3-112">변수</span><span class="sxs-lookup"><span data-stu-id="c7ef3-112">PARAMETERS</span></span>

### <span data-ttu-id="c7ef3-113">-이름</span><span class="sxs-lookup"><span data-stu-id="c7ef3-113">-Name</span></span>
<span data-ttu-id="c7ef3-114">인프라 역할 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c7ef3-114">Name of the infrastructure role instance.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7ef3-115">-위치</span><span class="sxs-lookup"><span data-stu-id="c7ef3-115">-Location</span></span>
<span data-ttu-id="c7ef3-116">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="c7ef3-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7ef3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7ef3-117">-ResourceGroupName</span></span>
<span data-ttu-id="c7ef3-118">리소스 공급자가 등록 된 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="c7ef3-118">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7ef3-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7ef3-119">-ResourceId</span></span>
<span data-ttu-id="c7ef3-120">인프라 역할 인스턴스 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c7ef3-120">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="c7ef3-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c7ef3-121">-AsJob</span></span>
<span data-ttu-id="c7ef3-122">비동기를 작업으로 실행 하 고 작업 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7ef3-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="c7ef3-123">-Force</span><span class="sxs-lookup"><span data-stu-id="c7ef3-123">-Force</span></span>
<span data-ttu-id="c7ef3-124">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c7ef3-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="c7ef3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7ef3-125">-WhatIf</span></span>
<span data-ttu-id="c7ef3-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c7ef3-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7ef3-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c7ef3-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7ef3-128">-확인</span><span class="sxs-lookup"><span data-stu-id="c7ef3-128">-Confirm</span></span>
<span data-ttu-id="c7ef3-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7ef3-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7ef3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7ef3-130">CommonParameters</span></span>
<span data-ttu-id="c7ef3-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c7ef3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7ef3-132">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7ef3-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7ef3-133">입력</span><span class="sxs-lookup"><span data-stu-id="c7ef3-133">INPUTS</span></span>

## <span data-ttu-id="c7ef3-134">출력</span><span class="sxs-lookup"><span data-stu-id="c7ef3-134">OUTPUTS</span></span>

## <span data-ttu-id="c7ef3-135">상속자</span><span class="sxs-lookup"><span data-stu-id="c7ef3-135">NOTES</span></span>

## <span data-ttu-id="c7ef3-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c7ef3-136">RELATED LINKS</span></span>
