---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/powershell/module/az.machinelearning/get-azmlcommitmentplanusagehistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlanUsageHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlanUsageHistory.md
ms.openlocfilehash: 8baf0e2af5ebc06e51c0f8b588fe04ff3106f892
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009627"
---
# <span data-ttu-id="c5d99-101">Get-AzMlCommitmentPlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="c5d99-101">Get-AzMlCommitmentPlanUsageHistory</span></span>

## <span data-ttu-id="c5d99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5d99-102">SYNOPSIS</span></span>
<span data-ttu-id="c5d99-103">지정된 약정 계획에 대한 사용 기록 정보를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="c5d99-103">Retrieves usage history information for a specified commitment plan.</span></span>

## <span data-ttu-id="c5d99-104">구문</span><span class="sxs-lookup"><span data-stu-id="c5d99-104">SYNTAX</span></span>

```
Get-AzMlCommitmentPlanUsageHistory -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5d99-105">설명</span><span class="sxs-lookup"><span data-stu-id="c5d99-105">DESCRIPTION</span></span>
<span data-ttu-id="c5d99-106">사용된 리소스 및 계획 내에 남아 있는 리소스를 포함하여 지정된 약정 계획에 대한 사용 기록 정보를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="c5d99-106">Retrieves usage history information for a specified commitment plan, including resources used and resources remaining within the plan.</span></span>

## <span data-ttu-id="c5d99-107">예제</span><span class="sxs-lookup"><span data-stu-id="c5d99-107">EXAMPLES</span></span>

### <span data-ttu-id="c5d99-108">예제 1: 특정 약정 계획에 대한 사용 기록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c5d99-108">Example 1: Get usage history for a specific commitment plan</span></span>
```
Get-AzMlCommitmentPlanUsageHistory -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="c5d99-109">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c5d99-109">PARAMETERS</span></span>

### <span data-ttu-id="c5d99-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5d99-110">-DefaultProfile</span></span>
<span data-ttu-id="c5d99-111">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c5d99-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c5d99-112">-Name</span><span class="sxs-lookup"><span data-stu-id="c5d99-112">-Name</span></span>
<span data-ttu-id="c5d99-113">Azure ML 약정 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c5d99-113">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="c5d99-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5d99-114">-ResourceGroupName</span></span>
<span data-ttu-id="c5d99-115">Azure ML 약정 계획에 대한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c5d99-115">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="c5d99-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5d99-116">CommonParameters</span></span>
<span data-ttu-id="c5d99-117">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c5d99-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5d99-118">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c5d99-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5d99-119">입력</span><span class="sxs-lookup"><span data-stu-id="c5d99-119">INPUTS</span></span>

### <span data-ttu-id="c5d99-120">없음</span><span class="sxs-lookup"><span data-stu-id="c5d99-120">None</span></span>

## <span data-ttu-id="c5d99-121">출력</span><span class="sxs-lookup"><span data-stu-id="c5d99-121">OUTPUTS</span></span>

### <span data-ttu-id="c5d99-122">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="c5d99-122">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory</span></span>

## <span data-ttu-id="c5d99-123">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c5d99-123">NOTES</span></span>
<span data-ttu-id="c5d99-124">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 기계, 기계 학습, azureml</span><span class="sxs-lookup"><span data-stu-id="c5d99-124">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="c5d99-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c5d99-125">RELATED LINKS</span></span>
