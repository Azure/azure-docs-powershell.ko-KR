---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Move-AzureRmMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Move-AzureRmMlCommitmentAssociation.md
ms.openlocfilehash: 84c1560cf4d97f7a40735d767c2c4d82fcd7d65a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537124"
---
# <span data-ttu-id="8e2c4-101">Move-AzureRmMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="8e2c4-101">Move-AzureRmMlCommitmentAssociation</span></span>

## <span data-ttu-id="8e2c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e2c4-102">SYNOPSIS</span></span>
<span data-ttu-id="8e2c4-103">한 약정 계획의 약정 관계를 전환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e2c4-103">Moves a commitment association from one commitment plan to another.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8e2c4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8e2c4-104">SYNTAX</span></span>

```
Move-AzureRmMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> -Name <String>
 -DestinationPlanId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8e2c4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="8e2c4-105">DESCRIPTION</span></span>
<span data-ttu-id="8e2c4-106">약정 연관 리소스를 해당 상위 약정 계획에서 다른 약정 계획으로 이동 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e2c4-106">Moves a commitment association resource from its parent commitment plan to another commitment plan.</span></span>

## <span data-ttu-id="8e2c4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="8e2c4-107">EXAMPLES</span></span>

### <span data-ttu-id="8e2c4-108">--------------------------예제 1: 약정 연결 이동--------------------------</span><span class="sxs-lookup"><span data-stu-id="8e2c4-108">--------------------------  Example 1: Move a commitment association  --------------------------</span></span>
<span data-ttu-id="8e2c4-109">@ {paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="8e2c4-109">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "SourceCommitmentPlanName" -Name "MyCommitmentAssociationName" -DestinationPlanId "/subscriptions/MySubscriptionId/resourceGroups/MyResourceGroup/providers/Microsoft.MachineLearning/commitmentPlans/DestinationCommitmentPlanName"
```

## <span data-ttu-id="8e2c4-110">변수</span><span class="sxs-lookup"><span data-stu-id="8e2c4-110">PARAMETERS</span></span>

### <span data-ttu-id="8e2c4-111">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="8e2c4-111">-CommitmentPlanName</span></span>
<span data-ttu-id="8e2c4-112">Azure ML 약정 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8e2c4-112">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="8e2c4-113">-DestinationPlanId</span><span class="sxs-lookup"><span data-stu-id="8e2c4-113">-DestinationPlanId</span></span>
<span data-ttu-id="8e2c4-114">대상 Azure ML 약정 계획의 Azure resource ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8e2c4-114">The Azure resource ID of the destination Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="8e2c4-115">-이름</span><span class="sxs-lookup"><span data-stu-id="8e2c4-115">-Name</span></span>
<span data-ttu-id="8e2c4-116">Azure ML 약정 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8e2c4-116">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="8e2c4-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e2c4-117">-ResourceGroupName</span></span>
<span data-ttu-id="8e2c4-118">Azure ML 약정 연결에 대 한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8e2c4-118">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="8e2c4-119">-확인</span><span class="sxs-lookup"><span data-stu-id="8e2c4-119">-Confirm</span></span>
<span data-ttu-id="8e2c4-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e2c4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e2c4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e2c4-121">-WhatIf</span></span>
<span data-ttu-id="8e2c4-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8e2c4-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8e2c4-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8e2c4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e2c4-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e2c4-124">-DefaultProfile</span></span>
<span data-ttu-id="8e2c4-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8e2c4-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e2c4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e2c4-126">CommonParameters</span></span>
<span data-ttu-id="8e2c4-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8e2c4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e2c4-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e2c4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e2c4-129">입력</span><span class="sxs-lookup"><span data-stu-id="8e2c4-129">INPUTS</span></span>

## <span data-ttu-id="8e2c4-130">출력</span><span class="sxs-lookup"><span data-stu-id="8e2c4-130">OUTPUTS</span></span>

### <span data-ttu-id="8e2c4-131">MachineLearning. CommitmentPlans. \ CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="8e2c4-131">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>
<span data-ttu-id="8e2c4-132">MachineLearning [] CommitmentPlans. CommitmentPlan []</span><span class="sxs-lookup"><span data-stu-id="8e2c4-132">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan[]</span></span>

## <span data-ttu-id="8e2c4-133">상속자</span><span class="sxs-lookup"><span data-stu-id="8e2c4-133">NOTES</span></span>
<span data-ttu-id="8e2c4-134">키워드: azure, azurerm, arm, resource, 관리, manager, machine, 기계 학습, azureml</span><span class="sxs-lookup"><span data-stu-id="8e2c4-134">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="8e2c4-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8e2c4-135">RELATED LINKS</span></span>

