---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/new-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/New-AzMlCommitmentPlan.md
ms.openlocfilehash: 7d3d65e10864848cb1564b7137321c911c153ce0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344553"
---
# <span data-ttu-id="718c7-101">New-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="718c7-101">New-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="718c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="718c7-102">SYNOPSIS</span></span>
<span data-ttu-id="718c7-103">새 약정 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="718c7-103">Creates a new commitment plan.</span></span>

## <span data-ttu-id="718c7-104">구문</span><span class="sxs-lookup"><span data-stu-id="718c7-104">SYNTAX</span></span>

```
New-AzMlCommitmentPlan -ResourceGroupName <String> -Location <String> -Name <String> -SkuName <String>
 -SkuTier <String> [-SkuCapacity <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="718c7-105">설명</span><span class="sxs-lookup"><span data-stu-id="718c7-105">DESCRIPTION</span></span>
<span data-ttu-id="718c7-106">기존 리소스 그룹에 Azure Machine Learning 약정 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="718c7-106">Creates an Azure Machine Learning commitment plan in an existing resource group.</span></span>
<span data-ttu-id="718c7-107">리소스 그룹에 동일한 이름의 약정 계획이 있는 경우 호출은 업데이트 작업으로 작동하고 기존 약정 계획을 덮어 덮어 습니다.</span><span class="sxs-lookup"><span data-stu-id="718c7-107">If a commitment plan with the same name exists in the resource group, the call acts as an update operation and the existing commitment plan is overwritten.</span></span>

## <span data-ttu-id="718c7-108">예제</span><span class="sxs-lookup"><span data-stu-id="718c7-108">EXAMPLES</span></span>

### <span data-ttu-id="718c7-109">예제 1: 새 약정 계획 만들기</span><span class="sxs-lookup"><span data-stu-id="718c7-109">Example 1: Create a new commitment plan</span></span>
```
New-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Location "South Central US" -SkuName DevTest -SkuTier Standard -SkuCapacity 1
```

<span data-ttu-id="718c7-110">"MyResourceGroup" 그룹 및 미국 중남부 지역에 "MyCommitmentPlanName"이라는 새 Azure Machine Learning 약정 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="718c7-110">Creates a new Azure Machine Learning commitment plan named "MyCommitmentPlanName" in the "MyResourceGroup" group and South Central US region.</span></span> <span data-ttu-id="718c7-111">이 예제에서는 SKU DevTest/Standard가 사용됩니다. 즉, 약정 계획에서 제공하는 리소스는 DevTest/Standard의 제한으로 정의됩니다.</span><span class="sxs-lookup"><span data-stu-id="718c7-111">In this example, the SKU DevTest/Standard is used, meaning the resources provided by the commitment plan will be defined by the limits of DevTest/Standard.</span></span> <span data-ttu-id="718c7-112">이 예제의 SkuCapacity는 1입니다. 즉, 계획 비용은 DevTest의 비용의 1배가 며 계획에 포함된 리소스는 DevTest에서 제공하는 리소스의 1배가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="718c7-112">The SkuCapacity in this example is 1, meaning the cost of the plan will be 1x the cost of DevTest, and the resources the plan contains will be 1x what DevTest provides.</span></span>

## <span data-ttu-id="718c7-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="718c7-113">PARAMETERS</span></span>

### <span data-ttu-id="718c7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="718c7-114">-DefaultProfile</span></span>
<span data-ttu-id="718c7-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="718c7-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="718c7-116">-Force</span><span class="sxs-lookup"><span data-stu-id="718c7-116">-Force</span></span>
<span data-ttu-id="718c7-117">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="718c7-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="718c7-118">-Location</span><span class="sxs-lookup"><span data-stu-id="718c7-118">-Location</span></span>
<span data-ttu-id="718c7-119">Azure ML 약정 계획의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="718c7-119">The location of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="718c7-120">-Name</span><span class="sxs-lookup"><span data-stu-id="718c7-120">-Name</span></span>
<span data-ttu-id="718c7-121">Azure ML 약정 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="718c7-121">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="718c7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="718c7-122">-ResourceGroupName</span></span>
<span data-ttu-id="718c7-123">Azure ML 약정 계획에 대한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="718c7-123">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="718c7-124">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="718c7-124">-SkuCapacity</span></span>
<span data-ttu-id="718c7-125">Azure ML 약정 계획을 프로비전할 때 사용할 SKU의 용량입니다.</span><span class="sxs-lookup"><span data-stu-id="718c7-125">The capacity of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="718c7-126">-SkuName</span><span class="sxs-lookup"><span data-stu-id="718c7-126">-SkuName</span></span>
<span data-ttu-id="718c7-127">Azure ML 약정 계획을 프로비전할 때 사용할 SKU의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="718c7-127">The name of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="718c7-128">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="718c7-128">-SkuTier</span></span>
<span data-ttu-id="718c7-129">Azure ML 약정 계획을 프로비전할 때 사용할 SKU의 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="718c7-129">The tier of the SKU to use when provisioning the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="718c7-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="718c7-130">-Confirm</span></span>
<span data-ttu-id="718c7-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="718c7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="718c7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="718c7-132">-WhatIf</span></span>
<span data-ttu-id="718c7-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="718c7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="718c7-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="718c7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="718c7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="718c7-135">CommonParameters</span></span>
<span data-ttu-id="718c7-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="718c7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="718c7-137">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="718c7-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="718c7-138">입력</span><span class="sxs-lookup"><span data-stu-id="718c7-138">INPUTS</span></span>

### <span data-ttu-id="718c7-139">없음</span><span class="sxs-lookup"><span data-stu-id="718c7-139">None</span></span>

## <span data-ttu-id="718c7-140">출력</span><span class="sxs-lookup"><span data-stu-id="718c7-140">OUTPUTS</span></span>

### <span data-ttu-id="718c7-141">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="718c7-141">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="718c7-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="718c7-142">NOTES</span></span>
<span data-ttu-id="718c7-143">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 기계, 기계 학습, azureml</span><span class="sxs-lookup"><span data-stu-id="718c7-143">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="718c7-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="718c7-144">RELATED LINKS</span></span>
