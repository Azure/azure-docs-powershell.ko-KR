---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 81bdb6a75e10af30b6febe9bbbf0989933818aec
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93874864"
---
# <span data-ttu-id="c1f53-101">Stop-AzsStorageContainerMigration</span><span class="sxs-lookup"><span data-stu-id="c1f53-101">Stop-AzsStorageContainerMigration</span></span>

## <span data-ttu-id="c1f53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1f53-102">SYNOPSIS</span></span>
<span data-ttu-id="c1f53-103">컨테이너 마이그레이션 작업을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1f53-103">Cancel a container migration job.</span></span>

## <span data-ttu-id="c1f53-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c1f53-104">SYNTAX</span></span>

```
Stop-AzsStorageContainerMigration [-JobId] <String> [[-ResourceGroupName] <String>] [-FarmName] <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1f53-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c1f53-105">DESCRIPTION</span></span>
<span data-ttu-id="c1f53-106">컨테이너 마이그레이션 작업을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1f53-106">Cancel a container migration job.</span></span>

## <span data-ttu-id="c1f53-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c1f53-107">EXAMPLES</span></span>

### <span data-ttu-id="c1f53-108">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c1f53-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Stop-AzsStorageContainerMigration -FarmName "342fccbe-e8c0-468d-a90e-cfca5fa8877c" -JobId "ac8cde1b-804f-4ace-b39b-5322106703bf"
```

<span data-ttu-id="c1f53-109">컨테이너 마이그레이션을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1f53-109">Cancel container migration.</span></span>

## <span data-ttu-id="c1f53-110">변수</span><span class="sxs-lookup"><span data-stu-id="c1f53-110">PARAMETERS</span></span>

### <span data-ttu-id="c1f53-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c1f53-111">-AsJob</span></span>
<span data-ttu-id="c1f53-112">비동기를 작업으로 실행 하 고 작업 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1f53-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="c1f53-113">-FarmName</span><span class="sxs-lookup"><span data-stu-id="c1f53-113">-FarmName</span></span>
<span data-ttu-id="c1f53-114">팜 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="c1f53-114">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1f53-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c1f53-115">-Force</span></span>
<span data-ttu-id="c1f53-116">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c1f53-116">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c1f53-117">-JobId</span><span class="sxs-lookup"><span data-stu-id="c1f53-117">-JobId</span></span>
<span data-ttu-id="c1f53-118">작업 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="c1f53-118">Operation Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1f53-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1f53-119">-ResourceGroupName</span></span>
<span data-ttu-id="c1f53-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c1f53-120">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1f53-121">-확인</span><span class="sxs-lookup"><span data-stu-id="c1f53-121">-Confirm</span></span>
<span data-ttu-id="c1f53-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1f53-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1f53-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1f53-123">-WhatIf</span></span>
<span data-ttu-id="c1f53-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c1f53-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1f53-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c1f53-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1f53-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1f53-126">CommonParameters</span></span>
<span data-ttu-id="c1f53-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1f53-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1f53-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1f53-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1f53-129">입력</span><span class="sxs-lookup"><span data-stu-id="c1f53-129">INPUTS</span></span>

## <span data-ttu-id="c1f53-130">출력</span><span class="sxs-lookup"><span data-stu-id="c1f53-130">OUTPUTS</span></span>

## <span data-ttu-id="c1f53-131">상속자</span><span class="sxs-lookup"><span data-stu-id="c1f53-131">NOTES</span></span>

## <span data-ttu-id="c1f53-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c1f53-132">RELATED LINKS</span></span>

