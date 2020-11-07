---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8c9a27b1722c1c7f08d9daeab0205dd20d9ba8b9
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93874932"
---
# <span data-ttu-id="d885e-101">Stop-AzsStorageContainerMigration</span><span class="sxs-lookup"><span data-stu-id="d885e-101">Stop-AzsStorageContainerMigration</span></span>

## <span data-ttu-id="d885e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d885e-102">SYNOPSIS</span></span>
<span data-ttu-id="d885e-103">컨테이너 마이그레이션 작업을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="d885e-103">Cancel a container migration job.</span></span>

## <span data-ttu-id="d885e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d885e-104">SYNTAX</span></span>

```
Stop-AzsStorageContainerMigration [-JobId] <String> [[-ResourceGroupName] <String>] [-FarmName] <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d885e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d885e-105">DESCRIPTION</span></span>
<span data-ttu-id="d885e-106">컨테이너 마이그레이션 작업을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="d885e-106">Cancel a container migration job.</span></span>

## <span data-ttu-id="d885e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d885e-107">EXAMPLES</span></span>

### <span data-ttu-id="d885e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="d885e-108">EXAMPLE 1</span></span>
```
Stop-AzsStorageContainerMigration -FarmName "342fccbe-e8c0-468d-a90e-cfca5fa8877c" -JobId "ac8cde1b-804f-4ace-b39b-5322106703bf"
```

<span data-ttu-id="d885e-109">컨테이너 마이그레이션을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="d885e-109">Cancel container migration.</span></span>

## <span data-ttu-id="d885e-110">변수</span><span class="sxs-lookup"><span data-stu-id="d885e-110">PARAMETERS</span></span>

### <span data-ttu-id="d885e-111">-JobId</span><span class="sxs-lookup"><span data-stu-id="d885e-111">-JobId</span></span>
<span data-ttu-id="d885e-112">작업 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="d885e-112">Operation Id.</span></span>

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

### <span data-ttu-id="d885e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d885e-113">-ResourceGroupName</span></span>
<span data-ttu-id="d885e-114">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d885e-114">Resource group name.</span></span>

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

### <span data-ttu-id="d885e-115">-FarmName</span><span class="sxs-lookup"><span data-stu-id="d885e-115">-FarmName</span></span>
<span data-ttu-id="d885e-116">팜 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="d885e-116">Farm Id.</span></span>

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

### <span data-ttu-id="d885e-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d885e-117">-AsJob</span></span>
<span data-ttu-id="d885e-118">비동기를 작업으로 실행 하 고 작업 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d885e-118">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="d885e-119">-Force</span><span class="sxs-lookup"><span data-stu-id="d885e-119">-Force</span></span>
<span data-ttu-id="d885e-120">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d885e-120">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d885e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d885e-121">-WhatIf</span></span>
<span data-ttu-id="d885e-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d885e-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d885e-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d885e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d885e-124">-확인</span><span class="sxs-lookup"><span data-stu-id="d885e-124">-Confirm</span></span>
<span data-ttu-id="d885e-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d885e-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d885e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d885e-126">CommonParameters</span></span>
<span data-ttu-id="d885e-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d885e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d885e-128">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d885e-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d885e-129">입력</span><span class="sxs-lookup"><span data-stu-id="d885e-129">INPUTS</span></span>

## <span data-ttu-id="d885e-130">출력</span><span class="sxs-lookup"><span data-stu-id="d885e-130">OUTPUTS</span></span>

## <span data-ttu-id="d885e-131">상속자</span><span class="sxs-lookup"><span data-stu-id="d885e-131">NOTES</span></span>

## <span data-ttu-id="d885e-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d885e-132">RELATED LINKS</span></span>
