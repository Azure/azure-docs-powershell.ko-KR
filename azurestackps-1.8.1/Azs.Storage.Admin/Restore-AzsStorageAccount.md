---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 769567562199d33116911f1f1f5e258ae2decbbe
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93875179"
---
# <span data-ttu-id="9707e-101">Restore-AzsStorageAccount</span><span class="sxs-lookup"><span data-stu-id="9707e-101">Restore-AzsStorageAccount</span></span>

## <span data-ttu-id="9707e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9707e-102">SYNOPSIS</span></span>
<span data-ttu-id="9707e-103">삭제 된 저장소 계정의 삭제를 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="9707e-103">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="9707e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9707e-104">SYNTAX</span></span>

### <span data-ttu-id="9707e-105">삭제 취소 (기본값)</span><span class="sxs-lookup"><span data-stu-id="9707e-105">Undelete (Default)</span></span>
```
Restore-AzsStorageAccount -FarmName <String> -Name <String> [-ResourceGroupName <String>] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9707e-106">리소스</span><span class="sxs-lookup"><span data-stu-id="9707e-106">ResourceId</span></span>
```
Restore-AzsStorageAccount -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9707e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="9707e-107">DESCRIPTION</span></span>
<span data-ttu-id="9707e-108">삭제 된 저장소 계정의 삭제를 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="9707e-108">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="9707e-109">예제의</span><span class="sxs-lookup"><span data-stu-id="9707e-109">EXAMPLES</span></span>

### <span data-ttu-id="9707e-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="9707e-110">EXAMPLE 1</span></span>
```
Restore-AzsStorageAccount -FarmName "90987d65-eb60-42ae-b735-18bcd7ff69da" -Name "83fe9ac0-f1e7-433e-b04c-c61ae0712093"
```

<span data-ttu-id="9707e-111">삭제 된 저장소 계정의 삭제를 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="9707e-111">Undelete a deleted storage account.</span></span>

## <span data-ttu-id="9707e-112">변수</span><span class="sxs-lookup"><span data-stu-id="9707e-112">PARAMETERS</span></span>

### <span data-ttu-id="9707e-113">-FarmName</span><span class="sxs-lookup"><span data-stu-id="9707e-113">-FarmName</span></span>
<span data-ttu-id="9707e-114">팜 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="9707e-114">Farm Id.</span></span>

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

### <span data-ttu-id="9707e-115">-이름</span><span class="sxs-lookup"><span data-stu-id="9707e-115">-Name</span></span>
<span data-ttu-id="9707e-116">테 넌 트에 표시 되지 않는 내부 저장소 계정 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="9707e-116">Internal storage account ID, which is not visible to tenant.</span></span>

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

### <span data-ttu-id="9707e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9707e-117">-ResourceGroupName</span></span>
<span data-ttu-id="9707e-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9707e-118">Resource group name.</span></span>

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

### <span data-ttu-id="9707e-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9707e-119">-ResourceId</span></span>
<span data-ttu-id="9707e-120">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="9707e-120">The resource id.</span></span>

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

### <span data-ttu-id="9707e-121">-Force</span><span class="sxs-lookup"><span data-stu-id="9707e-121">-Force</span></span>
<span data-ttu-id="9707e-122">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9707e-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9707e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9707e-123">-WhatIf</span></span>
<span data-ttu-id="9707e-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9707e-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9707e-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9707e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9707e-126">-확인</span><span class="sxs-lookup"><span data-stu-id="9707e-126">-Confirm</span></span>
<span data-ttu-id="9707e-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9707e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9707e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9707e-128">CommonParameters</span></span>
<span data-ttu-id="9707e-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9707e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9707e-130">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9707e-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9707e-131">입력</span><span class="sxs-lookup"><span data-stu-id="9707e-131">INPUTS</span></span>

## <span data-ttu-id="9707e-132">출력</span><span class="sxs-lookup"><span data-stu-id="9707e-132">OUTPUTS</span></span>

## <span data-ttu-id="9707e-133">상속자</span><span class="sxs-lookup"><span data-stu-id="9707e-133">NOTES</span></span>

## <span data-ttu-id="9707e-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9707e-134">RELATED LINKS</span></span>
