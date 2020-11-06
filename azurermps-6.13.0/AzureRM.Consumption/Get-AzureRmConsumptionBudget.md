---
external help file: Microsoft.Azure.Commands.Consumption.dll-Help.xml
Module Name: AzureRM.Consumption
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.consumption/get-azurermconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Get-AzureRmConsumptionBudget.md
ms.openlocfilehash: 7793dfe2f5d83e0975a5a8c200d19b48d8c4d9f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528560"
---
# <span data-ttu-id="8ee60-101">Get-AzureRmConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="8ee60-101">Get-AzureRmConsumptionBudget</span></span>

## <span data-ttu-id="8ee60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ee60-102">SYNOPSIS</span></span>
<span data-ttu-id="8ee60-103">구독 또는 리소스 그룹의 예산 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8ee60-103">Get a list of budgets in either a subscription or a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8ee60-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8ee60-104">SYNTAX</span></span>

```
Get-AzureRmConsumptionBudget [-DefaultProfile <IAzureContextContainer>] [-ResourceGroupName <String>]
 [-Name <String>] [<CommonParameters>]
```

## <span data-ttu-id="8ee60-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8ee60-105">DESCRIPTION</span></span>
<span data-ttu-id="8ee60-106">Get-AzureRmConsumptionBudget cmdlet은 구독 또는 리소스 그룹의 예산 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8ee60-106">The Get-AzureRmConsumptionBudget cmdlet gets a list of budgets in either a subscription or a resource group.</span></span>

## <span data-ttu-id="8ee60-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8ee60-107">EXAMPLES</span></span>

### <span data-ttu-id="8ee60-108">예제 1: 구독 수준에서 예산 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="8ee60-108">Example 1: Get a list of budgets at subscription level</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionBudget
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

### <span data-ttu-id="8ee60-109">예제 2: 리소스 그룹 수준에서 예산 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="8ee60-109">Example 2: Get a list of budgets at resource group level</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionBudget -ResourceGroupName RGBudgets
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

### <span data-ttu-id="8ee60-110">예제 3: 구독 수준에서 예산 이름으로 예산 가져오기</span><span class="sxs-lookup"><span data-stu-id="8ee60-110">Example 3: Get a budget with the budget name at subscription level</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionBudget -Name PSBudget
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

### <span data-ttu-id="8ee60-111">예제 4: 리소스 그룹 수준에서 예산 이름으로 예산 가져오기</span><span class="sxs-lookup"><span data-stu-id="8ee60-111">Example 4: Get a budget with the budget name at resource group level</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG
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

## <span data-ttu-id="8ee60-112">변수</span><span class="sxs-lookup"><span data-stu-id="8ee60-112">PARAMETERS</span></span>

### <span data-ttu-id="8ee60-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ee60-113">-DefaultProfile</span></span>
<span data-ttu-id="8ee60-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8ee60-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8ee60-115">-이름</span><span class="sxs-lookup"><span data-stu-id="8ee60-115">-Name</span></span>
<span data-ttu-id="8ee60-116">예산 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8ee60-116">Name of a budget.</span></span>

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

### <span data-ttu-id="8ee60-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ee60-117">-ResourceGroupName</span></span>
<span data-ttu-id="8ee60-118">예산에 대 한 자원 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="8ee60-118">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="8ee60-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ee60-119">CommonParameters</span></span>
<span data-ttu-id="8ee60-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ee60-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ee60-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ee60-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ee60-122">입력</span><span class="sxs-lookup"><span data-stu-id="8ee60-122">INPUTS</span></span>

### <span data-ttu-id="8ee60-123">않아야</span><span class="sxs-lookup"><span data-stu-id="8ee60-123">None</span></span>

## <span data-ttu-id="8ee60-124">출력</span><span class="sxs-lookup"><span data-stu-id="8ee60-124">OUTPUTS</span></span>

### <span data-ttu-id="8ee60-125">Microsoft. a. 모든 모델에 대 한 PSBudget</span><span class="sxs-lookup"><span data-stu-id="8ee60-125">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>

## <span data-ttu-id="8ee60-126">상속자</span><span class="sxs-lookup"><span data-stu-id="8ee60-126">NOTES</span></span>

## <span data-ttu-id="8ee60-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8ee60-127">RELATED LINKS</span></span>
