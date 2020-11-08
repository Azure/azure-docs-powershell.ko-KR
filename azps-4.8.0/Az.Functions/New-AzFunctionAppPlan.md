---
external help file: ''
Module Name: Az.Functions
online version: https://docs.microsoft.com/en-us/powershell/module/az.functions/new-azfunctionappplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionAppPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Functions/help/New-AzFunctionAppPlan.md
ms.openlocfilehash: 934c8ed95a31f4b953096da40b5ac480020dbc1f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212225"
---
# <span data-ttu-id="d79a0-101">New-AzFunctionAppPlan</span><span class="sxs-lookup"><span data-stu-id="d79a0-101">New-AzFunctionAppPlan</span></span>

## <span data-ttu-id="d79a0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d79a0-102">SYNOPSIS</span></span>
<span data-ttu-id="d79a0-103">함수 앱 서비스 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d79a0-103">Creates a function app service plan.</span></span>

## <span data-ttu-id="d79a0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d79a0-104">SYNTAX</span></span>

```
New-AzFunctionAppPlan -Location <String> -Name <String> -ResourceGroupName <String> -Sku <String>
 -WorkerType <String> [-SubscriptionId <String>] [-MaximumWorkerCount <Int32>] [-MinimumWorkerCount <Int32>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d79a0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d79a0-105">DESCRIPTION</span></span>
<span data-ttu-id="d79a0-106">함수 앱 서비스 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d79a0-106">Creates a function app service plan.</span></span>

## <span data-ttu-id="d79a0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d79a0-107">EXAMPLES</span></span>

### <span data-ttu-id="d79a0-108">예제 1: 서쪽 유럽에서 Windows premium 앱 계획 만들기 최대 10 개 인스턴스까지 버스트로 기능을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d79a0-108">Example 1: Create a Windows premium app plan in West Europe with burst out capability up to 10 instances.</span></span>
```powershell
PS C:\> New-AzFunctionAppPlan -ResourceGroupName MyResourceGroupName `
                              -Name MyPremiumPlan `
                              -Location WestEurope `
                              -MinimumWorkerCount 1 `
                              -MaximumWorkerCount 10 `
                              -Sku EP1 `
                              -WorkerType Windows

```

<span data-ttu-id="d79a0-109">이 명령은 서쪽에 최대 10 개의 인스턴스로 기능 하는 Windows premium 앱 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d79a0-109">This command creates a Windows premium app plan in West Europe with burst out capability up to 10 instances.</span></span>

## <span data-ttu-id="d79a0-110">변수</span><span class="sxs-lookup"><span data-stu-id="d79a0-110">PARAMETERS</span></span>

### <span data-ttu-id="d79a0-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d79a0-111">-AsJob</span></span>
<span data-ttu-id="d79a0-112">명령을 작업으로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d79a0-112">Run the command as a job.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d79a0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d79a0-113">-DefaultProfile</span></span>


```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d79a0-114">-위치</span><span class="sxs-lookup"><span data-stu-id="d79a0-114">-Location</span></span>
<span data-ttu-id="d79a0-115">소비량 계획의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="d79a0-115">The location for the consumption plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d79a0-116">-Maximum개 수</span><span class="sxs-lookup"><span data-stu-id="d79a0-116">-MaximumWorkerCount</span></span>
<span data-ttu-id="d79a0-117">App service 계획의 최대 작업자 수입니다.</span><span class="sxs-lookup"><span data-stu-id="d79a0-117">The maximum number of workers for the app service plan.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MaxBurst

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d79a0-118">-가 수</span><span class="sxs-lookup"><span data-stu-id="d79a0-118">-MinimumWorkerCount</span></span>
<span data-ttu-id="d79a0-119">App service 계획의 최소 작업자 수입니다.</span><span class="sxs-lookup"><span data-stu-id="d79a0-119">The minimum number of workers for the app service plan.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: MinInstances

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d79a0-120">-이름</span><span class="sxs-lookup"><span data-stu-id="d79a0-120">-Name</span></span>
<span data-ttu-id="d79a0-121">App Service 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d79a0-121">Name of the App Service plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d79a0-122">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d79a0-122">-NoWait</span></span>
<span data-ttu-id="d79a0-123">비동기적으로 명령을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d79a0-123">Run the command asynchronously.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d79a0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d79a0-124">-ResourceGroupName</span></span>
<span data-ttu-id="d79a0-125">자원이 속한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d79a0-125">Name of the resource group to which the resource belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d79a0-126">-Sku</span><span class="sxs-lookup"><span data-stu-id="d79a0-126">-Sku</span></span>
<span data-ttu-id="d79a0-127">계획 sku입니다.</span><span class="sxs-lookup"><span data-stu-id="d79a0-127">The plan sku.</span></span>
<span data-ttu-id="d79a0-128">유효한 입력: EP1, EP2, EP3</span><span class="sxs-lookup"><span data-stu-id="d79a0-128">Valid inputs are: EP1, EP2, EP3</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d79a0-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d79a0-129">-SubscriptionId</span></span>
<span data-ttu-id="d79a0-130">Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d79a0-130">The Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d79a0-131">태그</span><span class="sxs-lookup"><span data-stu-id="d79a0-131">-Tag</span></span>
<span data-ttu-id="d79a0-132">리소스 태그.</span><span class="sxs-lookup"><span data-stu-id="d79a0-132">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d79a0-133">-로 유형</span><span class="sxs-lookup"><span data-stu-id="d79a0-133">-WorkerType</span></span>
<span data-ttu-id="d79a0-134">계획에 대 한 작업자 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="d79a0-134">The worker type for the plan.</span></span>
<span data-ttu-id="d79a0-135">유효한 입력은 Windows 또는 Linux입니다.</span><span class="sxs-lookup"><span data-stu-id="d79a0-135">Valid inputs are: Windows or Linux.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d79a0-136">-확인</span><span class="sxs-lookup"><span data-stu-id="d79a0-136">-Confirm</span></span>
<span data-ttu-id="d79a0-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d79a0-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d79a0-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d79a0-138">-WhatIf</span></span>
<span data-ttu-id="d79a0-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d79a0-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d79a0-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d79a0-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d79a0-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d79a0-141">CommonParameters</span></span>
<span data-ttu-id="d79a0-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d79a0-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d79a0-143">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d79a0-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d79a0-144">입력</span><span class="sxs-lookup"><span data-stu-id="d79a0-144">INPUTS</span></span>

## <span data-ttu-id="d79a0-145">출력</span><span class="sxs-lookup"><span data-stu-id="d79a0-145">OUTPUTS</span></span>

### <span data-ttu-id="d79a0-146">Api20190801. i p. PowerShell. IAppServicePlan</span><span class="sxs-lookup"><span data-stu-id="d79a0-146">Microsoft.Azure.PowerShell.Cmdlets.Functions.Models.Api20190801.IAppServicePlan</span></span>

## <span data-ttu-id="d79a0-147">상속자</span><span class="sxs-lookup"><span data-stu-id="d79a0-147">NOTES</span></span>

<span data-ttu-id="d79a0-148">별칭과</span><span class="sxs-lookup"><span data-stu-id="d79a0-148">ALIASES</span></span>

## <span data-ttu-id="d79a0-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d79a0-149">RELATED LINKS</span></span>

