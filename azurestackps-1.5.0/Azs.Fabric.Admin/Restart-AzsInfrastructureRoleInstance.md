---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f6e7801a2188fe80577bc6cef9315069b0207f91
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523124"
---
# <span data-ttu-id="0db4f-101">Restart-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="0db4f-101">Restart-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="0db4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0db4f-102">SYNOPSIS</span></span>
<span data-ttu-id="0db4f-103">인프라 역할 인스턴스를 다시 부팅 합니다.</span><span class="sxs-lookup"><span data-stu-id="0db4f-103">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="0db4f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0db4f-104">SYNTAX</span></span>

### <span data-ttu-id="0db4f-105">다시 시작 (기본값)</span><span class="sxs-lookup"><span data-stu-id="0db4f-105">Restart (Default)</span></span>
```
Restart-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0db4f-106">리소스</span><span class="sxs-lookup"><span data-stu-id="0db4f-106">ResourceId</span></span>
```
Restart-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0db4f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0db4f-107">DESCRIPTION</span></span>
<span data-ttu-id="0db4f-108">인프라 역할 인스턴스를 다시 부팅 합니다.</span><span class="sxs-lookup"><span data-stu-id="0db4f-108">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="0db4f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0db4f-109">EXAMPLES</span></span>

### <span data-ttu-id="0db4f-110">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0db4f-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Restart-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="0db4f-111">인프라 역할 인스턴스를 다시 부팅 합니다.</span><span class="sxs-lookup"><span data-stu-id="0db4f-111">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="0db4f-112">변수</span><span class="sxs-lookup"><span data-stu-id="0db4f-112">PARAMETERS</span></span>

### <span data-ttu-id="0db4f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0db4f-113">-AsJob</span></span>
<span data-ttu-id="0db4f-114">비동기를 작업으로 실행 하 고 작업 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0db4f-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="0db4f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="0db4f-115">-Force</span></span>
<span data-ttu-id="0db4f-116">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0db4f-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="0db4f-117">-위치</span><span class="sxs-lookup"><span data-stu-id="0db4f-117">-Location</span></span>
<span data-ttu-id="0db4f-118">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="0db4f-118">Location of the resource.</span></span>

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

### <span data-ttu-id="0db4f-119">-이름</span><span class="sxs-lookup"><span data-stu-id="0db4f-119">-Name</span></span>
<span data-ttu-id="0db4f-120">인프라 역할 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0db4f-120">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="0db4f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0db4f-121">-ResourceGroupName</span></span>
<span data-ttu-id="0db4f-122">리소스 공급자가 등록 된 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="0db4f-122">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="0db4f-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0db4f-123">-ResourceId</span></span>
<span data-ttu-id="0db4f-124">인프라 역할 인스턴스 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0db4f-124">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="0db4f-125">-확인</span><span class="sxs-lookup"><span data-stu-id="0db4f-125">-Confirm</span></span>
<span data-ttu-id="0db4f-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0db4f-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0db4f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0db4f-127">-WhatIf</span></span>
<span data-ttu-id="0db4f-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0db4f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0db4f-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0db4f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0db4f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0db4f-130">CommonParameters</span></span>
<span data-ttu-id="0db4f-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0db4f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0db4f-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0db4f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0db4f-133">입력</span><span class="sxs-lookup"><span data-stu-id="0db4f-133">INPUTS</span></span>

## <span data-ttu-id="0db4f-134">출력</span><span class="sxs-lookup"><span data-stu-id="0db4f-134">OUTPUTS</span></span>

## <span data-ttu-id="0db4f-135">상속자</span><span class="sxs-lookup"><span data-stu-id="0db4f-135">NOTES</span></span>

## <span data-ttu-id="0db4f-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0db4f-136">RELATED LINKS</span></span>

