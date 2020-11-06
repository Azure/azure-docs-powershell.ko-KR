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
ms.locfileid: "93523888"
---
# <span data-ttu-id="67d83-101">Start-AzsReclaimStorageCapacity</span><span class="sxs-lookup"><span data-stu-id="67d83-101">Start-AzsReclaimStorageCapacity</span></span>

## <span data-ttu-id="67d83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67d83-102">SYNOPSIS</span></span>
<span data-ttu-id="67d83-103">삭제 된 저장소 개체에서 가비지 수집을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="67d83-103">Start garbage collection on deleted storage objects.</span></span>

## <span data-ttu-id="67d83-104">구문과</span><span class="sxs-lookup"><span data-stu-id="67d83-104">SYNTAX</span></span>

```
Start-AzsReclaimStorageCapacity [[-ResourceGroupName] <String>] [-FarmName] <String> [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67d83-105">설명은</span><span class="sxs-lookup"><span data-stu-id="67d83-105">DESCRIPTION</span></span>
<span data-ttu-id="67d83-106">삭제 된 저장소 개체에서 가비지 수집을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="67d83-106">Start garbage collection on deleted storage objects.</span></span>

## <span data-ttu-id="67d83-107">예제의</span><span class="sxs-lookup"><span data-stu-id="67d83-107">EXAMPLES</span></span>

### <span data-ttu-id="67d83-108">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="67d83-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsReclaimStorageCapacity -FarmName "44263c10-13b2-4912-9b17-85c1e43b2a30"
```

<span data-ttu-id="67d83-109">가비지 수집을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="67d83-109">Start garbage collection.</span></span>

## <span data-ttu-id="67d83-110">변수</span><span class="sxs-lookup"><span data-stu-id="67d83-110">PARAMETERS</span></span>

### <span data-ttu-id="67d83-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="67d83-111">-AsJob</span></span>
<span data-ttu-id="67d83-112">비동기를 작업으로 실행 하 고 작업 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="67d83-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="67d83-113">-FarmName</span><span class="sxs-lookup"><span data-stu-id="67d83-113">-FarmName</span></span>
<span data-ttu-id="67d83-114">팜 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="67d83-114">Farm Id.</span></span>

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

### <span data-ttu-id="67d83-115">-Force</span><span class="sxs-lookup"><span data-stu-id="67d83-115">-Force</span></span>
<span data-ttu-id="67d83-116">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="67d83-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="67d83-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67d83-117">-ResourceGroupName</span></span>
<span data-ttu-id="67d83-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="67d83-118">Resource group name.</span></span>

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

### <span data-ttu-id="67d83-119">-확인</span><span class="sxs-lookup"><span data-stu-id="67d83-119">-Confirm</span></span>
<span data-ttu-id="67d83-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="67d83-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67d83-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67d83-121">-WhatIf</span></span>
<span data-ttu-id="67d83-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="67d83-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67d83-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="67d83-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67d83-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67d83-124">CommonParameters</span></span>
<span data-ttu-id="67d83-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="67d83-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67d83-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67d83-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67d83-127">입력</span><span class="sxs-lookup"><span data-stu-id="67d83-127">INPUTS</span></span>

## <span data-ttu-id="67d83-128">출력</span><span class="sxs-lookup"><span data-stu-id="67d83-128">OUTPUTS</span></span>

## <span data-ttu-id="67d83-129">상속자</span><span class="sxs-lookup"><span data-stu-id="67d83-129">NOTES</span></span>

## <span data-ttu-id="67d83-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="67d83-130">RELATED LINKS</span></span>

