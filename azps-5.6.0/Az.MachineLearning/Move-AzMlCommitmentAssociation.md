---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/move-azmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Move-AzMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Move-AzMlCommitmentAssociation.md
ms.openlocfilehash: 019ff5b50eb366947f82004d60ae38888532ac10
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952363"
---
# <span data-ttu-id="74657-101">Move-AzMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="74657-101">Move-AzMlCommitmentAssociation</span></span>

## <span data-ttu-id="74657-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74657-102">SYNOPSIS</span></span>
<span data-ttu-id="74657-103">약정 연결은 한 약정 계획에서 다른 약정 계획으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="74657-103">Moves a commitment association from one commitment plan to another.</span></span>

## <span data-ttu-id="74657-104">구문</span><span class="sxs-lookup"><span data-stu-id="74657-104">SYNTAX</span></span>

```
Move-AzMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> -Name <String>
 -DestinationPlanId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="74657-105">설명</span><span class="sxs-lookup"><span data-stu-id="74657-105">DESCRIPTION</span></span>
<span data-ttu-id="74657-106">약정 연결 리소스를 부모 약정 계획에서 다른 약정 계획으로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="74657-106">Moves a commitment association resource from its parent commitment plan to another commitment plan.</span></span>

## <span data-ttu-id="74657-107">예제</span><span class="sxs-lookup"><span data-stu-id="74657-107">EXAMPLES</span></span>

### <span data-ttu-id="74657-108">예제 1: 약정 연결 이동</span><span class="sxs-lookup"><span data-stu-id="74657-108">Example 1: Move a commitment association</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "SourceCommitmentPlanName" -Name "MyCommitmentAssociationName" -DestinationPlanId "/subscriptions/MySubscriptionId/resourceGroups/MyResourceGroup/providers/Microsoft.MachineLearning/commitmentPlans/DestinationCommitmentPlanName"
```

## <span data-ttu-id="74657-109">매개 변수</span><span class="sxs-lookup"><span data-stu-id="74657-109">PARAMETERS</span></span>

### <span data-ttu-id="74657-110">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="74657-110">-CommitmentPlanName</span></span>
<span data-ttu-id="74657-111">Azure ML 약정 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="74657-111">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="74657-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74657-112">-DefaultProfile</span></span>
<span data-ttu-id="74657-113">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="74657-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="74657-114">-DestinationPlanId</span><span class="sxs-lookup"><span data-stu-id="74657-114">-DestinationPlanId</span></span>
<span data-ttu-id="74657-115">대상 Azure ML 약정 계획의 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="74657-115">The Azure resource ID of the destination Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="74657-116">-Name</span><span class="sxs-lookup"><span data-stu-id="74657-116">-Name</span></span>
<span data-ttu-id="74657-117">Azure ML 약정 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="74657-117">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="74657-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74657-118">-ResourceGroupName</span></span>
<span data-ttu-id="74657-119">Azure ML 약정 연결에 대한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="74657-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="74657-120">-확인</span><span class="sxs-lookup"><span data-stu-id="74657-120">-Confirm</span></span>
<span data-ttu-id="74657-121">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="74657-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74657-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74657-122">-WhatIf</span></span>
<span data-ttu-id="74657-123">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="74657-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="74657-124">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="74657-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74657-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74657-125">CommonParameters</span></span>
<span data-ttu-id="74657-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="74657-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74657-127">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="74657-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74657-128">입력</span><span class="sxs-lookup"><span data-stu-id="74657-128">INPUTS</span></span>

### <span data-ttu-id="74657-129">없음</span><span class="sxs-lookup"><span data-stu-id="74657-129">None</span></span>

## <span data-ttu-id="74657-130">출력</span><span class="sxs-lookup"><span data-stu-id="74657-130">OUTPUTS</span></span>

### <span data-ttu-id="74657-131">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="74657-131">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="74657-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="74657-132">NOTES</span></span>
<span data-ttu-id="74657-133">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 기계, 기계 학습, azureml</span><span class="sxs-lookup"><span data-stu-id="74657-133">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="74657-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="74657-134">RELATED LINKS</span></span>
