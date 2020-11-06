---
external help file: Microsoft.Azure.Commands.Consumption.dll-Help.xml
Module Name: AzureRM.Consumption
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.consumption/remove-azurermconsumptionbudget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Remove-AzureRmConsumptionBudget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Consumption/Commands.Consumption/help/Remove-AzureRmConsumptionBudget.md
ms.openlocfilehash: b14afecc7f31f878b4ce1598f8b135265ff72249
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534400"
---
# <span data-ttu-id="6322a-101">Remove-AzureRmConsumptionBudget</span><span class="sxs-lookup"><span data-stu-id="6322a-101">Remove-AzureRmConsumptionBudget</span></span>

## <span data-ttu-id="6322a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6322a-102">SYNOPSIS</span></span>
<span data-ttu-id="6322a-103">구독 또는 리소스 그룹에서 예산을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6322a-103">Remove a budget in either a subscription or a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6322a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6322a-104">SYNTAX</span></span>

### <span data-ttu-id="6322a-105">구독 (기본값)</span><span class="sxs-lookup"><span data-stu-id="6322a-105">Subscription (Default)</span></span>
```
Remove-AzureRmConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -Name <String>
 [-ResourceGroupName <String>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6322a-106">읽어들이</span><span class="sxs-lookup"><span data-stu-id="6322a-106">Piping</span></span>
```
Remove-AzureRmConsumptionBudget [-DefaultProfile <IAzureContextContainer>] -InputObject <PSBudget> [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6322a-107">설명은</span><span class="sxs-lookup"><span data-stu-id="6322a-107">DESCRIPTION</span></span>
<span data-ttu-id="6322a-108">Remove-AzureRmConsumptionBudget cmdlet은 구독 또는 리소스 그룹에서 예산을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6322a-108">The Remove-AzureRmConsumptionBudget cmdlet removes a budget in either a subscription or a resource group.</span></span>

## <span data-ttu-id="6322a-109">예제의</span><span class="sxs-lookup"><span data-stu-id="6322a-109">EXAMPLES</span></span>

### <span data-ttu-id="6322a-110">예제 1: 구독 수준에서 예산 이름으로 예산 제거</span><span class="sxs-lookup"><span data-stu-id="6322a-110">Example 1: Remove a budget with a budget name at subscription level</span></span>
```powershell
PS C:\> Remove-AzureRmConsumptionBudget -Name PSBudget -PassThru
True
```

### <span data-ttu-id="6322a-111">예제 2: 리소스 그룹 수준에서 예산 이름으로 예산 제거</span><span class="sxs-lookup"><span data-stu-id="6322a-111">Example 2: Remove a budget with a budget name at resource group level</span></span>
```powershell
PS C:\> Remove-AzureRmConsumptionBudget -ResourceGroupName RGBudgets -Name PSBudgetRG -PassThru
True
```

### <span data-ttu-id="6322a-112">예제 3: 구독 수준에서 파이핑을 통해 예산 제거</span><span class="sxs-lookup"><span data-stu-id="6322a-112">Example 3: Remove a budget through piping at subscription level</span></span>
```powershell
PS C:\> Get-AzureRmConsumptionBudget -Name PSBudget | Remove-AzureRmConsumptionBudget -PassThru
True
```

## <span data-ttu-id="6322a-113">변수</span><span class="sxs-lookup"><span data-stu-id="6322a-113">PARAMETERS</span></span>

### <span data-ttu-id="6322a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6322a-114">-DefaultProfile</span></span>
<span data-ttu-id="6322a-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6322a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6322a-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6322a-116">-InputObject</span></span>
<span data-ttu-id="6322a-117">예산 개체</span><span class="sxs-lookup"><span data-stu-id="6322a-117">Budget object.</span></span>

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

### <span data-ttu-id="6322a-118">-이름</span><span class="sxs-lookup"><span data-stu-id="6322a-118">-Name</span></span>
<span data-ttu-id="6322a-119">예산 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6322a-119">Name of a budget.</span></span>

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

### <span data-ttu-id="6322a-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6322a-120">-PassThru</span></span>
<span data-ttu-id="6322a-121">예산이 성공적으로 제거 된 경우 Cmdlet은 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6322a-121">The Cmdlet returns true if a budget was successfully removed.</span></span>

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

### <span data-ttu-id="6322a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6322a-122">-ResourceGroupName</span></span>
<span data-ttu-id="6322a-123">예산에 대 한 자원 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="6322a-123">Resource Group of a budget.</span></span>

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

### <span data-ttu-id="6322a-124">-확인</span><span class="sxs-lookup"><span data-stu-id="6322a-124">-Confirm</span></span>
<span data-ttu-id="6322a-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6322a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6322a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6322a-126">-WhatIf</span></span>
<span data-ttu-id="6322a-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6322a-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6322a-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6322a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6322a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6322a-129">CommonParameters</span></span>
<span data-ttu-id="6322a-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6322a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6322a-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6322a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6322a-132">입력</span><span class="sxs-lookup"><span data-stu-id="6322a-132">INPUTS</span></span>

### <span data-ttu-id="6322a-133">Microsoft. a. 모든 모델에 대 한 PSBudget</span><span class="sxs-lookup"><span data-stu-id="6322a-133">Microsoft.Azure.Commands.Consumption.Models.PSBudget</span></span>
<span data-ttu-id="6322a-134">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6322a-134">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="6322a-135">출력</span><span class="sxs-lookup"><span data-stu-id="6322a-135">OUTPUTS</span></span>

### <span data-ttu-id="6322a-136">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="6322a-136">System.Boolean</span></span>

## <span data-ttu-id="6322a-137">상속자</span><span class="sxs-lookup"><span data-stu-id="6322a-137">NOTES</span></span>

## <span data-ttu-id="6322a-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6322a-138">RELATED LINKS</span></span>
