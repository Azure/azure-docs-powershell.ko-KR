---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionBudget.md
ms.openlocfilehash: dfca3033b5061116882eb68eb18fa2ff3ddd0c53
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496256"
---
# <span data-ttu-id="219f1-101">Get-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="219f1-101">Get-AzConsumptionBudget</span></span>

## <span data-ttu-id="219f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="219f1-102">SYNOPSIS</span></span>
<span data-ttu-id="219f1-103">구독 또는 리소스 그룹의 예산 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="219f1-103">Get a list of budgets in either a subscription or a resource group.</span></span>

## <span data-ttu-id="219f1-104">구문</span><span class="sxs-lookup"><span data-stu-id="219f1-104">SYNTAX</span></span>

```
Get-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] [-ResourceGroupName <String>]
 [-Name <String>] [<CommonParameters>]
```

## <span data-ttu-id="219f1-105">설명</span><span class="sxs-lookup"><span data-stu-id="219f1-105">DESCRIPTION</span></span>
<span data-ttu-id="219f1-106">Get-AzConsumptionBudget cmdlet은 구독 또는 리소스 그룹의 예산 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="219f1-106">The Get-AzConsumptionBudget cmdlet gets a list of budgets in either a subscription or a resource group.</span></span>

## <span data-ttu-id="219f1-107">예제</span><span class="sxs-lookup"><span data-stu-id="219f1-107">EXAMPLES</span></span>

### <span data-ttu-id="219f1-108">예제 1: 구독 수준에서 예산 목록 확인</span><span class="sxs-lookup"><span data-stu-id="219f1-108">Example 1: Get a list of budgets at subscription level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Consumption/budgets/PSBudget
Name:  PSBudget
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="219f1-109">예제 2: 리소스 그룹 수준에서 예산 목록 얻기</span><span class="sxs-lookup"><span data-stu-id="219f1-109">Example 2: Get a list of budgets at resource group level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget -ResourceGroupName RGBudgets
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/RGBudgets/providers/Microsoft.Consumption/budgets/PSBudgetRG
Name:  PSBudgetRG
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="219f1-110">예제 3: 구독 수준에서 예산 이름으로 예산을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="219f1-110">Example 3: Get a budget with the budget name at subscription level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget -Name PSBudget
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/providers/Microsoft.Consumption/budgets/PSBudget
Name:  PSBudget
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

### <span data-ttu-id="219f1-111">예제 4: 자원 그룹 수준에서 예산 이름을 지정한 예산을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="219f1-111">Example 4: Get a budget with the budget name at resource group level</span></span>
```powershell
PS C:\> Get-AzConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG
Amount:  60     
Category:  Cost
CurrentSpend:  null
Id:  subscriptions/1caaa5a3-2b66-438e-8ab4-bce37d518c5d/resourceGroups/RGBudgets/providers/Microsoft.Consumption/budgets/PSBudgetRG
Name:  PSBudgetRG
TimeGrain:  Monthly
TimePeriod:  EndDate:  11/1/2018 12:00:00 AM
             StartDate:  6/1/2018 12:00:00 AM
Type:  Microsoft.Consumption/budgets
```

## <span data-ttu-id="219f1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="219f1-112">PARAMETERS</span></span>

### <span data-ttu-id="219f1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="219f1-113">-DefaultProfile</span></span>
<span data-ttu-id="219f1-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="219f1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="219f1-115">-Name</span><span class="sxs-lookup"><span data-stu-id="219f1-115">-Name</span></span>
<span data-ttu-id="219f1-116">예산의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="219f1-116">Name of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="219f1-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="219f1-117">-ResourceGroupName</span></span>
<span data-ttu-id="219f1-118">예산의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="219f1-118">Resource Group of a budget.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="219f1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="219f1-119">CommonParameters</span></span>
<span data-ttu-id="219f1-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="219f1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="219f1-121">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="219f1-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="219f1-122">입력</span><span class="sxs-lookup"><span data-stu-id="219f1-122">INPUTS</span></span>

### <span data-ttu-id="219f1-123">없음</span><span class="sxs-lookup"><span data-stu-id="219f1-123">None</span></span>

## <span data-ttu-id="219f1-124">출력</span><span class="sxs-lookup"><span data-stu-id="219f1-124">OUTPUTS</span></span>

### <span data-ttu-id="219f1-125">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span><span class="sxs-lookup"><span data-stu-id="219f1-125">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="219f1-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="219f1-126">NOTES</span></span>

## <span data-ttu-id="219f1-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="219f1-127">RELATED LINKS</span></span>
