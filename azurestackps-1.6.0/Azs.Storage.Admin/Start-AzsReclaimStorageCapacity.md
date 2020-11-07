---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c3c7ec31ce2af23a4376f8b5f94deca302345e81
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701720"
---
# <span data-ttu-id="bfada-101">Start-AzsReclaimStorageCapacity</span><span class="sxs-lookup"><span data-stu-id="bfada-101">Start-AzsReclaimStorageCapacity</span></span>

## <span data-ttu-id="bfada-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfada-102">SYNOPSIS</span></span>
<span data-ttu-id="bfada-103">삭제 된 저장소 개체에서 가비지 수집을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfada-103">Start garbage collection on deleted storage objects.</span></span>

## <span data-ttu-id="bfada-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bfada-104">SYNTAX</span></span>

```
Start-AzsReclaimStorageCapacity [[-ResourceGroupName] <String>] [-FarmName] <String> [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bfada-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bfada-105">DESCRIPTION</span></span>
<span data-ttu-id="bfada-106">삭제 된 저장소 개체에서 가비지 수집을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfada-106">Start garbage collection on deleted storage objects.</span></span>

## <span data-ttu-id="bfada-107">예제의</span><span class="sxs-lookup"><span data-stu-id="bfada-107">EXAMPLES</span></span>

### <span data-ttu-id="bfada-108">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="bfada-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsReclaimStorageCapacity -FarmName "44263c10-13b2-4912-9b17-85c1e43b2a30"
```

<span data-ttu-id="bfada-109">가비지 수집을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfada-109">Start garbage collection.</span></span>

## <span data-ttu-id="bfada-110">변수</span><span class="sxs-lookup"><span data-stu-id="bfada-110">PARAMETERS</span></span>

### <span data-ttu-id="bfada-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bfada-111">-AsJob</span></span>
<span data-ttu-id="bfada-112">비동기를 작업으로 실행 하 고 작업 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfada-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="bfada-113">-FarmName</span><span class="sxs-lookup"><span data-stu-id="bfada-113">-FarmName</span></span>
<span data-ttu-id="bfada-114">팜 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="bfada-114">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: name

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfada-115">-Force</span><span class="sxs-lookup"><span data-stu-id="bfada-115">-Force</span></span>
<span data-ttu-id="bfada-116">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bfada-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="bfada-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfada-117">-ResourceGroupName</span></span>
<span data-ttu-id="bfada-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bfada-118">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bfada-119">-확인</span><span class="sxs-lookup"><span data-stu-id="bfada-119">-Confirm</span></span>
<span data-ttu-id="bfada-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfada-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfada-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfada-121">-WhatIf</span></span>
<span data-ttu-id="bfada-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="bfada-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfada-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bfada-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfada-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfada-124">CommonParameters</span></span>
<span data-ttu-id="bfada-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfada-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfada-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfada-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfada-127">입력</span><span class="sxs-lookup"><span data-stu-id="bfada-127">INPUTS</span></span>

## <span data-ttu-id="bfada-128">출력</span><span class="sxs-lookup"><span data-stu-id="bfada-128">OUTPUTS</span></span>

## <span data-ttu-id="bfada-129">상속자</span><span class="sxs-lookup"><span data-stu-id="bfada-129">NOTES</span></span>

## <span data-ttu-id="bfada-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bfada-130">RELATED LINKS</span></span>

