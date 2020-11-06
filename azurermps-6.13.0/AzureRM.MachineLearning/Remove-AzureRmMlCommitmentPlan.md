---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/remove-azurermmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Remove-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: d14baa5382d5d9ffeeac8efd863a17cbad279865
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534299"
---
# <span data-ttu-id="863ac-101">Remove-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="863ac-101">Remove-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="863ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="863ac-102">SYNOPSIS</span></span>
<span data-ttu-id="863ac-103">약정 계획을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="863ac-103">Deletes a commitment plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="863ac-104">구문과</span><span class="sxs-lookup"><span data-stu-id="863ac-104">SYNTAX</span></span>

### <span data-ttu-id="863ac-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="863ac-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzureRmMlCommitmentPlan -ResourceGroupName <String> -Name <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="863ac-106">RemoveByObject</span><span class="sxs-lookup"><span data-stu-id="863ac-106">RemoveByObject</span></span>
```
Remove-AzureRmMlCommitmentPlan -MlCommitmentPlan <CommitmentPlan> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="863ac-107">설명은</span><span class="sxs-lookup"><span data-stu-id="863ac-107">DESCRIPTION</span></span>
<span data-ttu-id="863ac-108">Azure 기계 학습 약정 계획을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="863ac-108">Deletes an Azure Machine Learning commitment plan.</span></span> <span data-ttu-id="863ac-109">약정 연결을 보유 하 고 있는 약정 계획은 삭제할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="863ac-109">Note that commitment plans which have commitment associations cannot be deleted.</span></span> <span data-ttu-id="863ac-110">약정 관계는 해당 대상 리소스에 의해서만 삭제 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="863ac-110">Commitment associations can only be deleted by their target resource.</span></span> <span data-ttu-id="863ac-111">예를 들어 Azure 기계 학습 웹 서비스를 삭제 하면 웹 서비스를 약정 계획과 연결 하는 약정 연결도 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="863ac-111">For example, if you delete an Azure Machine Learning web service, the commitment association which associates the web service to a commitment plan will also be deleted.</span></span>

## <span data-ttu-id="863ac-112">예제의</span><span class="sxs-lookup"><span data-stu-id="863ac-112">EXAMPLES</span></span>

### <span data-ttu-id="863ac-113">예제 1: 약정 계획 삭제</span><span class="sxs-lookup"><span data-stu-id="863ac-113">Example 1: Delete a commitment plan</span></span>
```
Remove-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="863ac-114">변수</span><span class="sxs-lookup"><span data-stu-id="863ac-114">PARAMETERS</span></span>

### <span data-ttu-id="863ac-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="863ac-115">-DefaultProfile</span></span>
<span data-ttu-id="863ac-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="863ac-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="863ac-117">-Force</span><span class="sxs-lookup"><span data-stu-id="863ac-117">-Force</span></span>
<span data-ttu-id="863ac-118">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="863ac-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="863ac-119">-MlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="863ac-119">-MlCommitmentPlan</span></span>
<span data-ttu-id="863ac-120">기계 학습 웹 서비스 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="863ac-120">The machine learning web service object.</span></span>

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

### <span data-ttu-id="863ac-121">-이름</span><span class="sxs-lookup"><span data-stu-id="863ac-121">-Name</span></span>
<span data-ttu-id="863ac-122">Azure ML 약정 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="863ac-122">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="863ac-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="863ac-123">-ResourceGroupName</span></span>
<span data-ttu-id="863ac-124">Azure ML 약정 계획에 대 한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="863ac-124">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="863ac-125">-확인</span><span class="sxs-lookup"><span data-stu-id="863ac-125">-Confirm</span></span>
<span data-ttu-id="863ac-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="863ac-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="863ac-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="863ac-127">-WhatIf</span></span>
<span data-ttu-id="863ac-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="863ac-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="863ac-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="863ac-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="863ac-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="863ac-130">CommonParameters</span></span>
<span data-ttu-id="863ac-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="863ac-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="863ac-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="863ac-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="863ac-133">입력</span><span class="sxs-lookup"><span data-stu-id="863ac-133">INPUTS</span></span>

### <span data-ttu-id="863ac-134">MachineLearning. CommitmentPlans. \ CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="863ac-134">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>
<span data-ttu-id="863ac-135">매개 변수: MlCommitmentPlan (ByValue)</span><span class="sxs-lookup"><span data-stu-id="863ac-135">Parameters: MlCommitmentPlan (ByValue)</span></span>

## <span data-ttu-id="863ac-136">출력</span><span class="sxs-lookup"><span data-stu-id="863ac-136">OUTPUTS</span></span>

### <span data-ttu-id="863ac-137">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="863ac-137">System.Void</span></span>

## <span data-ttu-id="863ac-138">상속자</span><span class="sxs-lookup"><span data-stu-id="863ac-138">NOTES</span></span>
<span data-ttu-id="863ac-139">키워드: azure, azurerm, arm, resource, 관리, manager, machine, 기계 학습, azureml</span><span class="sxs-lookup"><span data-stu-id="863ac-139">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="863ac-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="863ac-140">RELATED LINKS</span></span>
