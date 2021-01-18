---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/remove-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Remove-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Remove-AzConsumptionBudget.md
ms.openlocfilehash: b3ee807f1ae5b1af46fe2369f74da7e13f1882e6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496243"
---
# <span data-ttu-id="8d8a7-101">Remove-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="8d8a7-101">Remove-AzConsumptionBudget</span></span>

## <span data-ttu-id="8d8a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d8a7-102">SYNOPSIS</span></span>
<span data-ttu-id="8d8a7-103">구독 또는 리소스 그룹에서 예산을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="8d8a7-103">Remove a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="8d8a7-104">구문</span><span class="sxs-lookup"><span data-stu-id="8d8a7-104">SYNTAX</span></span>

### <span data-ttu-id="8d8a7-105">구독(기본값)</span><span class="sxs-lookup"><span data-stu-id="8d8a7-105">Subscription (Default)</span></span>
```
Remove-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String>
 [-ResourceGroupName <String>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d8a7-106">파이핑</span><span class="sxs-lookup"><span data-stu-id="8d8a7-106">Piping</span></span>
```
Remove-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d8a7-107">설명</span><span class="sxs-lookup"><span data-stu-id="8d8a7-107">DESCRIPTION</span></span>
<span data-ttu-id="8d8a7-108">이 Remove-AzConsumptionBudget cmdlet은 구독 또는 리소스 그룹에서 예산을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="8d8a7-108">The Remove-AzConsumptionBudget cmdlet removes a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="8d8a7-109">예제</span><span class="sxs-lookup"><span data-stu-id="8d8a7-109">EXAMPLES</span></span>

### <span data-ttu-id="8d8a7-110">예제 1: 구독 수준에서 예산 이름을 사용하여 예산 제거</span><span class="sxs-lookup"><span data-stu-id="8d8a7-110">Example 1: Remove a budget with a budget name at subscription level</span></span>
```powershell
PS C:\> Remove-AzConsumptionBudget -Name PSBudget -PassThru
True
```

### <span data-ttu-id="8d8a7-111">예제 2: 리소스 그룹 수준에서 예산 이름을 사용하여 예산 제거</span><span class="sxs-lookup"><span data-stu-id="8d8a7-111">Example 2: Remove a budget with a budget name at resource group level</span></span>
```powershell
PS C:\> Remove-AzConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG -PassThru
True
```

### <span data-ttu-id="8d8a7-112">예제 3: 구독 수준에서 파이핑을 통해 예산 제거</span><span class="sxs-lookup"><span data-stu-id="8d8a7-112">Example 3: Remove a budget through piping at subscription level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget -Name PSBudget | Remove-AzConsumptionBudget -PassThru
True
```

## <span data-ttu-id="8d8a7-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d8a7-113">PARAMETERS</span></span>

### <span data-ttu-id="8d8a7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d8a7-114">-DefaultProfile</span></span>
<span data-ttu-id="8d8a7-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8d8a7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d8a7-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8d8a7-116">-InputObject</span></span>
<span data-ttu-id="8d8a7-117">예산 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="8d8a7-117">Budget object.</span></span>

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

### <span data-ttu-id="8d8a7-118">-Name</span><span class="sxs-lookup"><span data-stu-id="8d8a7-118">-Name</span></span>
<span data-ttu-id="8d8a7-119">예산의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8d8a7-119">Name of a budget.</span></span>

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

### <span data-ttu-id="8d8a7-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8d8a7-120">-PassThru</span></span>
<span data-ttu-id="8d8a7-121">예산이 성공적으로 제거된 경우 Cmdlet은 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="8d8a7-121">The Cmdlet returns true if a budget was successfully removed.</span></span>

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

### <span data-ttu-id="8d8a7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d8a7-122">-ResourceGroupName</span></span>
<span data-ttu-id="8d8a7-123">예산의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="8d8a7-123">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="8d8a7-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8d8a7-124">-Confirm</span></span>
<span data-ttu-id="8d8a7-125">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8d8a7-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d8a7-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d8a7-126">-WhatIf</span></span>
<span data-ttu-id="8d8a7-127">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="8d8a7-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d8a7-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8d8a7-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d8a7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d8a7-129">CommonParameters</span></span>
<span data-ttu-id="8d8a7-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8d8a7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d8a7-131">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8d8a7-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d8a7-132">입력</span><span class="sxs-lookup"><span data-stu-id="8d8a7-132">INPUTS</span></span>

### <span data-ttu-id="8d8a7-133">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span><span class="sxs-lookup"><span data-stu-id="8d8a7-133">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="8d8a7-134">출력</span><span class="sxs-lookup"><span data-stu-id="8d8a7-134">OUTPUTS</span></span>

### <span data-ttu-id="8d8a7-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8d8a7-135">System.Boolean</span></span>

## <span data-ttu-id="8d8a7-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8d8a7-136">NOTES</span></span>

## <span data-ttu-id="8d8a7-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8d8a7-137">RELATED LINKS</span></span>
