---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: b4e3e69a0c55188514a31dbe7377f8336784b114
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93874731"
---
# <span data-ttu-id="b579a-101">Restore-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="b579a-101">Restore-AzsStorageAccount</span></span>

## <span data-ttu-id="b579a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b579a-102">SYNOPSIS</span></span>
<span data-ttu-id="b579a-103">삭제 된 저장소 계정의 삭제를 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="b579a-103">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="b579a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b579a-104">SYNTAX</span></span>

### <span data-ttu-id="b579a-105">삭제 취소 (기본값)</span><span class="sxs-lookup"><span data-stu-id="b579a-105">Undelete (Default)</span></span>
```
Restore-AzsStorageAccount -FarmName <String> -Name <String> [-ResourceGroupName <String>] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b579a-106">리소스</span><span class="sxs-lookup"><span data-stu-id="b579a-106">ResourceId</span></span>
```
Restore-AzsStorageAccount -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b579a-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b579a-107">DESCRIPTION</span></span>
<span data-ttu-id="b579a-108">삭제 된 저장소 계정의 삭제를 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="b579a-108">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="b579a-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b579a-109">EXAMPLES</span></span>

### <span data-ttu-id="b579a-110">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b579a-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Restore-AzsStorageAccount -FarmName "90987d65-eb60-42ae-b735-18bcd7ff69da" -Name "83fe9ac0-f1e7-433e-b04c-c61ae0712093"
```

<span data-ttu-id="b579a-111">삭제 된 저장소 계정의 삭제를 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="b579a-111">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="b579a-112">변수</span><span class="sxs-lookup"><span data-stu-id="b579a-112">PARAMETERS</span></span>

### <span data-ttu-id="b579a-113">-FarmName</span><span class="sxs-lookup"><span data-stu-id="b579a-113">-FarmName</span></span>
<span data-ttu-id="b579a-114">팜 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="b579a-114">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: Undelete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b579a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b579a-115">-Force</span></span>
<span data-ttu-id="b579a-116">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b579a-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b579a-117">-이름</span><span class="sxs-lookup"><span data-stu-id="b579a-117">-Name</span></span>
<span data-ttu-id="b579a-118">테 넌 트에 표시 되지 않는 내부 저장소 계정 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b579a-118">Internal storage account ID, which is not visible to tenant.</span></span>

```yaml
Type: String
Parameter Sets: Undelete
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b579a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b579a-119">-ResourceGroupName</span></span>
<span data-ttu-id="b579a-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b579a-120">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: Undelete
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b579a-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b579a-121">-ResourceId</span></span>
<span data-ttu-id="b579a-122">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="b579a-122">The resource id.</span></span>

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

### <span data-ttu-id="b579a-123">-확인</span><span class="sxs-lookup"><span data-stu-id="b579a-123">-Confirm</span></span>
<span data-ttu-id="b579a-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b579a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b579a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b579a-125">-WhatIf</span></span>
<span data-ttu-id="b579a-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b579a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b579a-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b579a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b579a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b579a-128">CommonParameters</span></span>
<span data-ttu-id="b579a-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b579a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b579a-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b579a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b579a-131">입력</span><span class="sxs-lookup"><span data-stu-id="b579a-131">INPUTS</span></span>

## <span data-ttu-id="b579a-132">출력</span><span class="sxs-lookup"><span data-stu-id="b579a-132">OUTPUTS</span></span>

## <span data-ttu-id="b579a-133">상속자</span><span class="sxs-lookup"><span data-stu-id="b579a-133">NOTES</span></span>

## <span data-ttu-id="b579a-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b579a-134">RELATED LINKS</span></span>

