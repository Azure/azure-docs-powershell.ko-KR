---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4406dc4cadecd1945e82b8a90e9937df2183b4da
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689092"
---
# <span data-ttu-id="4d561-101">Install-AzsUpdate</span><span class="sxs-lookup"><span data-stu-id="4d561-101">Install-AzsUpdate</span></span>

## <span data-ttu-id="4d561-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d561-102">SYNOPSIS</span></span>
<span data-ttu-id="4d561-103">업데이트 위치에 특정 업데이트를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d561-103">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="4d561-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4d561-104">SYNTAX</span></span>

### <span data-ttu-id="4d561-105">적용 (기본값)</span><span class="sxs-lookup"><span data-stu-id="4d561-105">Apply (Default)</span></span>
```
Install-AzsUpdate -Name <String> [-ResourceGroupName <String>] [-Location <String>] [-AsJob] [-Force] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d561-106">리소스</span><span class="sxs-lookup"><span data-stu-id="4d561-106">ResourceId</span></span>
```
Install-AzsUpdate [-AsJob] -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d561-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4d561-107">DESCRIPTION</span></span>
<span data-ttu-id="4d561-108">업데이트 위치에 특정 업데이트를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d561-108">Apply a specific update at an update location.</span></span> <span data-ttu-id="4d561-109">호출 된 후 업데이트의 진행률을 수정 하는 데 사용할 수 Get-AzsUpdateRun.</span><span class="sxs-lookup"><span data-stu-id="4d561-109">After invoked, Get-AzsUpdateRun may be used to modify the progress of the update.</span></span>

## <span data-ttu-id="4d561-110">예제의</span><span class="sxs-lookup"><span data-stu-id="4d561-110">EXAMPLES</span></span>

### <span data-ttu-id="4d561-111">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="4d561-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUpdate -Name Microsoft1.0.180305.1 | Install-AzsUpdate
```

<span data-ttu-id="4d561-112">업데이트 위치에 특정 업데이트를 적용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d561-112">Apply a specific update at an update location.</span></span>

## <span data-ttu-id="4d561-113">변수</span><span class="sxs-lookup"><span data-stu-id="4d561-113">PARAMETERS</span></span>

### <span data-ttu-id="4d561-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4d561-114">-AsJob</span></span>
<span data-ttu-id="4d561-115">비동기를 작업으로 실행 하 고 작업 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d561-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="4d561-116">-Force</span><span class="sxs-lookup"><span data-stu-id="4d561-116">-Force</span></span>
<span data-ttu-id="4d561-117">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4d561-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="4d561-118">-위치</span><span class="sxs-lookup"><span data-stu-id="4d561-118">-Location</span></span>
<span data-ttu-id="4d561-119">업데이트 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4d561-119">The name of the update location.</span></span>

```yaml
Type: String
Parameter Sets: Apply
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d561-120">-이름</span><span class="sxs-lookup"><span data-stu-id="4d561-120">-Name</span></span>
<span data-ttu-id="4d561-121">업데이트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4d561-121">Name of the update.</span></span>

```yaml
Type: String
Parameter Sets: Apply
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d561-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d561-122">-ResourceGroupName</span></span>
<span data-ttu-id="4d561-123">리소스가 있는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="4d561-123">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: Apply
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d561-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4d561-124">-ResourceId</span></span>
<span data-ttu-id="4d561-125">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="4d561-125">The resource id.</span></span>

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

### <span data-ttu-id="4d561-126">-확인</span><span class="sxs-lookup"><span data-stu-id="4d561-126">-Confirm</span></span>
<span data-ttu-id="4d561-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d561-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d561-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d561-128">-WhatIf</span></span>
<span data-ttu-id="4d561-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4d561-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d561-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4d561-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d561-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d561-131">CommonParameters</span></span>
<span data-ttu-id="4d561-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d561-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d561-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d561-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d561-134">입력</span><span class="sxs-lookup"><span data-stu-id="4d561-134">INPUTS</span></span>

## <span data-ttu-id="4d561-135">출력</span><span class="sxs-lookup"><span data-stu-id="4d561-135">OUTPUTS</span></span>

### <span data-ttu-id="4d561-136">Update.exe의 업데이트. 관리자. 업데이트</span><span class="sxs-lookup"><span data-stu-id="4d561-136">Microsoft.AzureStack.Management.Update.Admin.Models.Update</span></span>

## <span data-ttu-id="4d561-137">상속자</span><span class="sxs-lookup"><span data-stu-id="4d561-137">NOTES</span></span>

## <span data-ttu-id="4d561-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4d561-138">RELATED LINKS</span></span>

