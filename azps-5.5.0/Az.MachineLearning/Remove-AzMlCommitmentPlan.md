---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/remove-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Remove-AzMlCommitmentPlan.md
ms.openlocfilehash: 8593853817739438176b70424ab529f0811d90de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190292"
---
# <span data-ttu-id="7bd7c-101">Remove-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="7bd7c-101">Remove-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="7bd7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7bd7c-102">SYNOPSIS</span></span>
<span data-ttu-id="7bd7c-103">약정 계획을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd7c-103">Deletes a commitment plan.</span></span>

## <span data-ttu-id="7bd7c-104">구문</span><span class="sxs-lookup"><span data-stu-id="7bd7c-104">SYNTAX</span></span>

### <span data-ttu-id="7bd7c-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="7bd7c-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzMlCommitmentPlan -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bd7c-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="7bd7c-106">RemoveByObject</span></span>
```
Remove-AzMlCommitmentPlan -MlCommitmentPlan <CommitmentPlan> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bd7c-107">설명</span><span class="sxs-lookup"><span data-stu-id="7bd7c-107">DESCRIPTION</span></span>
<span data-ttu-id="7bd7c-108">Azure Machine Learning 약정 계획을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd7c-108">Deletes an Azure Machine Learning commitment plan.</span></span> <span data-ttu-id="7bd7c-109">약정 연결로 된 약정 요금제는 삭제할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd7c-109">Note that commitment plans which have commitment associations cannot be deleted.</span></span> <span data-ttu-id="7bd7c-110">약정 연결은 대상 리소스에서만 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd7c-110">Commitment associations can only be deleted by their target resource.</span></span> <span data-ttu-id="7bd7c-111">예를 들어 Azure Machine Learning 웹 서비스를 삭제하면 웹 서비스를 약정 계획에 연결한 약정 연결도 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="7bd7c-111">For example, if you delete an Azure Machine Learning web service, the commitment association which associates the web service to a commitment plan will also be deleted.</span></span>

## <span data-ttu-id="7bd7c-112">예제</span><span class="sxs-lookup"><span data-stu-id="7bd7c-112">EXAMPLES</span></span>

### <span data-ttu-id="7bd7c-113">예제 1: 약정 계획 삭제</span><span class="sxs-lookup"><span data-stu-id="7bd7c-113">Example 1: Delete a commitment plan</span></span>
```
Remove-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="7bd7c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7bd7c-114">PARAMETERS</span></span>

### <span data-ttu-id="7bd7c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bd7c-115">-DefaultProfile</span></span>
<span data-ttu-id="7bd7c-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7bd7c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7bd7c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="7bd7c-117">-Force</span></span>
<span data-ttu-id="7bd7c-118">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd7c-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="7bd7c-119">-MlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="7bd7c-119">-MlCommitmentPlan</span></span>
<span data-ttu-id="7bd7c-120">기계 학습 웹 서비스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd7c-120">The machine learning web service object.</span></span>

```yaml
Type: Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan
Parameter Sets: RemoveByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7bd7c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="7bd7c-121">-Name</span></span>
<span data-ttu-id="7bd7c-122">Azure ML 약정 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd7c-122">The name of the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bd7c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bd7c-123">-ResourceGroupName</span></span>
<span data-ttu-id="7bd7c-124">Azure ML 약정 계획에 대한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7bd7c-124">The name of the resource group for the Azure ML commitment plan.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7bd7c-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7bd7c-125">-Confirm</span></span>
<span data-ttu-id="7bd7c-126">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7bd7c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bd7c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bd7c-127">-WhatIf</span></span>
<span data-ttu-id="7bd7c-128">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7bd7c-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7bd7c-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7bd7c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bd7c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bd7c-130">CommonParameters</span></span>
<span data-ttu-id="7bd7c-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7bd7c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bd7c-132">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7bd7c-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bd7c-133">입력</span><span class="sxs-lookup"><span data-stu-id="7bd7c-133">INPUTS</span></span>

### <span data-ttu-id="7bd7c-134">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="7bd7c-134">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="7bd7c-135">출력</span><span class="sxs-lookup"><span data-stu-id="7bd7c-135">OUTPUTS</span></span>

### <span data-ttu-id="7bd7c-136">System.Void</span><span class="sxs-lookup"><span data-stu-id="7bd7c-136">System.Void</span></span>

## <span data-ttu-id="7bd7c-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7bd7c-137">NOTES</span></span>
<span data-ttu-id="7bd7c-138">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 기계, 기계 학습, azureml</span><span class="sxs-lookup"><span data-stu-id="7bd7c-138">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="7bd7c-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7bd7c-139">RELATED LINKS</span></span>
