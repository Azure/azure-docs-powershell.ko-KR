---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/move-azmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Move-AzMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Move-AzMlCommitmentAssociation.md
ms.openlocfilehash: c127ff40690658a98f9d0f0fa670cddfca123f89
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192276"
---
# <span data-ttu-id="25e88-101">Move-AzMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="25e88-101">Move-AzMlCommitmentAssociation</span></span>

## <span data-ttu-id="25e88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25e88-102">SYNOPSIS</span></span>
<span data-ttu-id="25e88-103">한 약정 계획에서 다른 약정 계획으로 약정 연결 이동</span><span class="sxs-lookup"><span data-stu-id="25e88-103">Moves a commitment association from one commitment plan to another.</span></span>

## <span data-ttu-id="25e88-104">구문</span><span class="sxs-lookup"><span data-stu-id="25e88-104">SYNTAX</span></span>

```
Move-AzMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> -Name <String>
 -DestinationPlanId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="25e88-105">설명</span><span class="sxs-lookup"><span data-stu-id="25e88-105">DESCRIPTION</span></span>
<span data-ttu-id="25e88-106">상위 약정 계획에서 다른 약정 계획으로 약정 연결 리소스를 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="25e88-106">Moves a commitment association resource from its parent commitment plan to another commitment plan.</span></span>

## <span data-ttu-id="25e88-107">예제</span><span class="sxs-lookup"><span data-stu-id="25e88-107">EXAMPLES</span></span>

### <span data-ttu-id="25e88-108">예제 1: 약정 연결 이동</span><span class="sxs-lookup"><span data-stu-id="25e88-108">Example 1: Move a commitment association</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "SourceCommitmentPlanName" -Name "MyCommitmentAssociationName" -DestinationPlanId "/subscriptions/MySubscriptionId/resourceGroups/MyResourceGroup/providers/Microsoft.MachineLearning/commitmentPlans/DestinationCommitmentPlanName"
```

## <span data-ttu-id="25e88-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25e88-109">PARAMETERS</span></span>

### <span data-ttu-id="25e88-110">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="25e88-110">-CommitmentPlanName</span></span>
<span data-ttu-id="25e88-111">Azure ML 약정 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="25e88-111">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="25e88-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25e88-112">-DefaultProfile</span></span>
<span data-ttu-id="25e88-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="25e88-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="25e88-114">-DestinationPlanId</span><span class="sxs-lookup"><span data-stu-id="25e88-114">-DestinationPlanId</span></span>
<span data-ttu-id="25e88-115">대상 Azure ML 약정 계획의 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="25e88-115">The Azure resource ID of the destination Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="25e88-116">-Name</span><span class="sxs-lookup"><span data-stu-id="25e88-116">-Name</span></span>
<span data-ttu-id="25e88-117">Azure ML 약정 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="25e88-117">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="25e88-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25e88-118">-ResourceGroupName</span></span>
<span data-ttu-id="25e88-119">Azure ML 약정 연결에 대한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="25e88-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="25e88-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="25e88-120">-Confirm</span></span>
<span data-ttu-id="25e88-121">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="25e88-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25e88-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25e88-122">-WhatIf</span></span>
<span data-ttu-id="25e88-123">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="25e88-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="25e88-124">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="25e88-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25e88-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25e88-125">CommonParameters</span></span>
<span data-ttu-id="25e88-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="25e88-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25e88-127">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="25e88-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25e88-128">입력</span><span class="sxs-lookup"><span data-stu-id="25e88-128">INPUTS</span></span>

### <span data-ttu-id="25e88-129">없음</span><span class="sxs-lookup"><span data-stu-id="25e88-129">None</span></span>

## <span data-ttu-id="25e88-130">출력</span><span class="sxs-lookup"><span data-stu-id="25e88-130">OUTPUTS</span></span>

### <span data-ttu-id="25e88-131">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="25e88-131">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="25e88-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="25e88-132">NOTES</span></span>
<span data-ttu-id="25e88-133">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 기계, 기계 학습, azureml</span><span class="sxs-lookup"><span data-stu-id="25e88-133">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="25e88-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="25e88-134">RELATED LINKS</span></span>
