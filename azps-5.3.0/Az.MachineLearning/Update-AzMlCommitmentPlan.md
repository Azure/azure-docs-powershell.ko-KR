---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/update-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Update-AzMlCommitmentPlan.md
ms.openlocfilehash: 733f473ed09807c33355ac6bc22491a160e5481a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385904"
---
# <span data-ttu-id="c16e0-101">Update-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="c16e0-101">Update-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="c16e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c16e0-102">SYNOPSIS</span></span>
<span data-ttu-id="c16e0-103">기존 약정 계획 리소스의 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c16e0-103">Updates properties of an existing commitment plan resource.</span></span>

## <span data-ttu-id="c16e0-104">구문</span><span class="sxs-lookup"><span data-stu-id="c16e0-104">SYNTAX</span></span>

```
Update-AzMlCommitmentPlan -ResourceGroupName <String> -Name <String> -SkuName <String> -SkuTier <String>
 [-SkuCapacity <Int32>] [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c16e0-105">설명</span><span class="sxs-lookup"><span data-stu-id="c16e0-105">DESCRIPTION</span></span>
<span data-ttu-id="c16e0-106">기존 약정 계획 리소스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c16e0-106">Updates an existing commitment plan resource.</span></span> <span data-ttu-id="c16e0-107">약정 계획의 대부분의 속성은 변경할 수 있으며 수정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c16e0-107">Note that most properties of the commitment plan are immutable and cannot be modified.</span></span> <span data-ttu-id="c16e0-108">수정할 수 있는 속성에는 SKU(한 SKU에서 다른 SKU로 약정 계획을 마이그레이션할 수 있도록 허용) 및 태그가 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="c16e0-108">Properties which can be modified include Sku (allowing you to migrate the commitment plan from one SKU to another) and Tags.</span></span>

## <span data-ttu-id="c16e0-109">예제</span><span class="sxs-lookup"><span data-stu-id="c16e0-109">EXAMPLES</span></span>

### <span data-ttu-id="c16e0-110">예제 1: 약정 계획 업데이트</span><span class="sxs-lookup"><span data-stu-id="c16e0-110">Example 1: Update a commitment plan</span></span>
```
Update-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName" -Tags @{'MyTagKey'='MyTagValue'}
```

## <span data-ttu-id="c16e0-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c16e0-111">PARAMETERS</span></span>

### <span data-ttu-id="c16e0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c16e0-112">-DefaultProfile</span></span>
<span data-ttu-id="c16e0-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c16e0-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c16e0-114">-Force</span><span class="sxs-lookup"><span data-stu-id="c16e0-114">-Force</span></span>
<span data-ttu-id="c16e0-115">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c16e0-115">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c16e0-116">-Name</span><span class="sxs-lookup"><span data-stu-id="c16e0-116">-Name</span></span>
<span data-ttu-id="c16e0-117">Azure ML 약정 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c16e0-117">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="c16e0-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c16e0-118">-ResourceGroupName</span></span>
<span data-ttu-id="c16e0-119">Azure ML 약정 계획에 대한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c16e0-119">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="c16e0-120">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="c16e0-120">-SkuCapacity</span></span>
<span data-ttu-id="c16e0-121">Azure ML 약정 계획을 업데이트할 때 사용할 SKU의 용량입니다.</span><span class="sxs-lookup"><span data-stu-id="c16e0-121">The capacity of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="c16e0-122">-SkuName</span><span class="sxs-lookup"><span data-stu-id="c16e0-122">-SkuName</span></span>
<span data-ttu-id="c16e0-123">Azure ML 약정 계획을 업데이트할 때 사용할 SKU의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c16e0-123">The name of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="c16e0-124">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="c16e0-124">-SkuTier</span></span>
<span data-ttu-id="c16e0-125">Azure ML 약정 계획을 업데이트할 때 사용할 SKU의 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="c16e0-125">The tier of the SKU to use when updating the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="c16e0-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="c16e0-126">-Tag</span></span>
<span data-ttu-id="c16e0-127">약정 계획 리소스에 대한 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="c16e0-127">Tags for the commitment plan resource.</span></span>

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

### <span data-ttu-id="c16e0-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c16e0-128">-Confirm</span></span>
<span data-ttu-id="c16e0-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c16e0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c16e0-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c16e0-130">-WhatIf</span></span>
<span data-ttu-id="c16e0-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c16e0-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c16e0-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c16e0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c16e0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c16e0-133">CommonParameters</span></span>
<span data-ttu-id="c16e0-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c16e0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c16e0-135">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c16e0-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c16e0-136">입력</span><span class="sxs-lookup"><span data-stu-id="c16e0-136">INPUTS</span></span>

### <span data-ttu-id="c16e0-137">없음</span><span class="sxs-lookup"><span data-stu-id="c16e0-137">None</span></span>

## <span data-ttu-id="c16e0-138">출력</span><span class="sxs-lookup"><span data-stu-id="c16e0-138">OUTPUTS</span></span>

### <span data-ttu-id="c16e0-139">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="c16e0-139">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="c16e0-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c16e0-140">NOTES</span></span>
<span data-ttu-id="c16e0-141">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 기계, 기계 학습, azureml</span><span class="sxs-lookup"><span data-stu-id="c16e0-141">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="c16e0-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c16e0-142">RELATED LINKS</span></span>
