---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/remove-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Remove-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Remove-AzConsumptionBudget.md
ms.openlocfilehash: b3ee807f1ae5b1af46fe2369f74da7e13f1882e6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048490"
---
# <span data-ttu-id="35635-101">Remove-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="35635-101">Remove-AzConsumptionBudget</span></span>

## <span data-ttu-id="35635-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35635-102">SYNOPSIS</span></span>
<span data-ttu-id="35635-103">구독 또는 리소스 그룹에서 예산을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="35635-103">Remove a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="35635-104">구문과</span><span class="sxs-lookup"><span data-stu-id="35635-104">SYNTAX</span></span>

### <span data-ttu-id="35635-105">구독 (기본값)</span><span class="sxs-lookup"><span data-stu-id="35635-105">Subscription (Default)</span></span>
```
Remove-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String>
 [-ResourceGroupName <String>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35635-106">읽어들이</span><span class="sxs-lookup"><span data-stu-id="35635-106">Piping</span></span>
```
Remove-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35635-107">설명은</span><span class="sxs-lookup"><span data-stu-id="35635-107">DESCRIPTION</span></span>
<span data-ttu-id="35635-108">Remove-AzConsumptionBudget cmdlet은 구독 또는 리소스 그룹에서 예산을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="35635-108">The Remove-AzConsumptionBudget cmdlet removes a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="35635-109">예제의</span><span class="sxs-lookup"><span data-stu-id="35635-109">EXAMPLES</span></span>

### <span data-ttu-id="35635-110">예제 1: 구독 수준에서 예산 이름으로 예산 제거</span><span class="sxs-lookup"><span data-stu-id="35635-110">Example 1: Remove a budget with a budget name at subscription level</span></span>
```powershell
PS C:\> Remove-AzConsumptionBudget -Name PSBudget -PassThru
True
```

### <span data-ttu-id="35635-111">예제 2: 리소스 그룹 수준에서 예산 이름으로 예산 제거</span><span class="sxs-lookup"><span data-stu-id="35635-111">Example 2: Remove a budget with a budget name at resource group level</span></span>
```powershell
PS C:\> Remove-AzConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG -PassThru
True
```

### <span data-ttu-id="35635-112">예제 3: 구독 수준에서 파이핑을 통해 예산 제거</span><span class="sxs-lookup"><span data-stu-id="35635-112">Example 3: Remove a budget through piping at subscription level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget -Name PSBudget | Remove-AzConsumptionBudget -PassThru
True
```

## <span data-ttu-id="35635-113">변수</span><span class="sxs-lookup"><span data-stu-id="35635-113">PARAMETERS</span></span>

### <span data-ttu-id="35635-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35635-114">-DefaultProfile</span></span>
<span data-ttu-id="35635-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="35635-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35635-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35635-116">-InputObject</span></span>
<span data-ttu-id="35635-117">예산 개체</span><span class="sxs-lookup"><span data-stu-id="35635-117">Budget object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Consumption.Models.PSBudget
Parameter Sets: Piping
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35635-118">-이름</span><span class="sxs-lookup"><span data-stu-id="35635-118">-Name</span></span>
<span data-ttu-id="35635-119">예산 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="35635-119">Name of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35635-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="35635-120">-PassThru</span></span>
<span data-ttu-id="35635-121">예산이 성공적으로 제거 된 경우 Cmdlet은 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="35635-121">The Cmdlet returns true if a budget was successfully removed.</span></span>

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

### <span data-ttu-id="35635-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35635-122">-ResourceGroupName</span></span>
<span data-ttu-id="35635-123">예산에 대 한 자원 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="35635-123">Resource Group of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: Subscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35635-124">-확인</span><span class="sxs-lookup"><span data-stu-id="35635-124">-Confirm</span></span>
<span data-ttu-id="35635-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="35635-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35635-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35635-126">-WhatIf</span></span>
<span data-ttu-id="35635-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="35635-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35635-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="35635-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35635-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35635-129">CommonParameters</span></span>
<span data-ttu-id="35635-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="35635-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35635-131">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35635-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35635-132">입력</span><span class="sxs-lookup"><span data-stu-id="35635-132">INPUTS</span></span>

### <span data-ttu-id="35635-133">Microsoft. a. 모든 모델에 대 한 PSBudget</span><span class="sxs-lookup"><span data-stu-id="35635-133">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="35635-134">출력</span><span class="sxs-lookup"><span data-stu-id="35635-134">OUTPUTS</span></span>

### <span data-ttu-id="35635-135">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="35635-135">System.Boolean</span></span>

## <span data-ttu-id="35635-136">상속자</span><span class="sxs-lookup"><span data-stu-id="35635-136">NOTES</span></span>

## <span data-ttu-id="35635-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="35635-137">RELATED LINKS</span></span>
