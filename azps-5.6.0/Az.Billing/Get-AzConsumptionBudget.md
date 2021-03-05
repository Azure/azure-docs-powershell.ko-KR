---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Consumption.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzConsumptionBudget.md
ms.openlocfilehash: 70f7f9c43612f1fd1248e019d970d157fadab000
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986211"
---
# <span data-ttu-id="90952-101">Get-AzConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="90952-101">Get-AzConsumptionBudget</span></span>

## <span data-ttu-id="90952-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90952-102">SYNOPSIS</span></span>
<span data-ttu-id="90952-103">구독 또는 리소스 그룹에서 예산 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="90952-103">Get a list of budgets in either a subscription or a resource group.</span></span>

## <span data-ttu-id="90952-104">구문</span><span class="sxs-lookup"><span data-stu-id="90952-104">SYNTAX</span></span>

```
Get-AzConsumptionBudget [-DefaultProfile <IAzureContextContainer>] [-ResourceGroupName <String>]
 [-Name <String>] [<CommonParameters>]
```

## <span data-ttu-id="90952-105">설명</span><span class="sxs-lookup"><span data-stu-id="90952-105">DESCRIPTION</span></span>
<span data-ttu-id="90952-106">Get-AzConsumptionBudget cmdlet은 구독 또는 리소스 그룹에서 예산 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="90952-106">The Get-AzConsumptionBudget cmdlet gets a list of budgets in either a subscription or a resource group.</span></span>

## <span data-ttu-id="90952-107">예제</span><span class="sxs-lookup"><span data-stu-id="90952-107">EXAMPLES</span></span>

### <span data-ttu-id="90952-108">예제 1: 구독 수준에서 예산 목록 확인</span><span class="sxs-lookup"><span data-stu-id="90952-108">Example 1: Get a list of budgets at subscription level</span></span>
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

### <span data-ttu-id="90952-109">예제 2: 리소스 그룹 수준에서 예산 목록 표시</span><span class="sxs-lookup"><span data-stu-id="90952-109">Example 2: Get a list of budgets at resource group level</span></span>
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

### <span data-ttu-id="90952-110">예제 3: 구독 수준에서 예산 이름으로 예산을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="90952-110">Example 3: Get a budget with the budget name at subscription level</span></span>
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

### <span data-ttu-id="90952-111">예제 4: 리소스 그룹 수준에서 예산 이름으로 예산을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="90952-111">Example 4: Get a budget with the budget name at resource group level</span></span>
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

## <span data-ttu-id="90952-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="90952-112">PARAMETERS</span></span>

### <span data-ttu-id="90952-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90952-113">-DefaultProfile</span></span>
<span data-ttu-id="90952-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="90952-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90952-115">-Name</span><span class="sxs-lookup"><span data-stu-id="90952-115">-Name</span></span>
<span data-ttu-id="90952-116">예산의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="90952-116">Name of a budget.</span></span>

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

### <span data-ttu-id="90952-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90952-117">-ResourceGroupName</span></span>
<span data-ttu-id="90952-118">예산의 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="90952-118">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="90952-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90952-119">CommonParameters</span></span>
<span data-ttu-id="90952-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="90952-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90952-121">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="90952-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90952-122">입력</span><span class="sxs-lookup"><span data-stu-id="90952-122">INPUTS</span></span>

### <span data-ttu-id="90952-123">없음</span><span class="sxs-lookup"><span data-stu-id="90952-123">None</span></span>

## <span data-ttu-id="90952-124">출력</span><span class="sxs-lookup"><span data-stu-id="90952-124">OUTPUTS</span></span>

### <span data-ttu-id="90952-125">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span><span class="sxs-lookup"><span data-stu-id="90952-125">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="90952-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="90952-126">NOTES</span></span>

## <span data-ttu-id="90952-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="90952-127">RELATED LINKS</span></span>
