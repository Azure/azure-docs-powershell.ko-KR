---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlan.md
ms.openlocfilehash: 2eeaf4d4c1f0a2cf97359610d34963e32b50d1c9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386037"
---
# <span data-ttu-id="96be6-101">Get-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="96be6-101">Get-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="96be6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96be6-102">SYNOPSIS</span></span>
<span data-ttu-id="96be6-103">하나 이상의 약정 계획에 대한 요약 정보를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="96be6-103">Retrieves the summary information for one or more commitment plans.</span></span>

## <span data-ttu-id="96be6-104">구문</span><span class="sxs-lookup"><span data-stu-id="96be6-104">SYNTAX</span></span>

```
Get-AzMlCommitmentPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96be6-105">설명</span><span class="sxs-lookup"><span data-stu-id="96be6-105">DESCRIPTION</span></span>
<span data-ttu-id="96be6-106">약정 계획 정보를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="96be6-106">Retrieves commitment plan information.</span></span>
<span data-ttu-id="96be6-107">전달된 매개 변수에 따라 cmdlet은 특정 약정 계획, 현재 구독 내의 지정된 리소스 그룹에 대한 약정 계획 컬렉션 또는 현재 구독 내의 약정 계획 컬렉션을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="96be6-107">Depending on the parameters passed, the cmdlet returns the a specific commitment plan, a collection of commitment plans for a specified resource group within the current subscription, or a collection of commitment plans within the current subscription.</span></span>

## <span data-ttu-id="96be6-108">예제</span><span class="sxs-lookup"><span data-stu-id="96be6-108">EXAMPLES</span></span>

### <span data-ttu-id="96be6-109">예제 1: 특정 약정 계획 구하기</span><span class="sxs-lookup"><span data-stu-id="96be6-109">Example 1: Get a specific commitment plan</span></span>
```
Get-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

### <span data-ttu-id="96be6-110">예제 2: 현재 구독의 모든 약정 계획 리소스 얻기</span><span class="sxs-lookup"><span data-stu-id="96be6-110">Example 2: Get all commitment plan resources in current subscription</span></span>
```
Get-AzMlCommitmentPlan
```

### <span data-ttu-id="96be6-111">예제 3: 현재 구독 및 주어진 리소스 그룹의 모든 약정 계획 확인</span><span class="sxs-lookup"><span data-stu-id="96be6-111">Example 3: Get all commitment plans in the current subscription and given resource group</span></span>
```
Get-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup"
```

## <span data-ttu-id="96be6-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="96be6-112">PARAMETERS</span></span>

### <span data-ttu-id="96be6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96be6-113">-DefaultProfile</span></span>
<span data-ttu-id="96be6-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="96be6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="96be6-115">-Name</span><span class="sxs-lookup"><span data-stu-id="96be6-115">-Name</span></span>
<span data-ttu-id="96be6-116">약정 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="96be6-116">The name of the commitment plan.</span></span>

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

### <span data-ttu-id="96be6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96be6-117">-ResourceGroupName</span></span>
<span data-ttu-id="96be6-118">Azure ML 약정 계획에 대한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="96be6-118">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="96be6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96be6-119">CommonParameters</span></span>
<span data-ttu-id="96be6-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="96be6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96be6-121">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="96be6-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96be6-122">입력</span><span class="sxs-lookup"><span data-stu-id="96be6-122">INPUTS</span></span>

### <span data-ttu-id="96be6-123">없음</span><span class="sxs-lookup"><span data-stu-id="96be6-123">None</span></span>

## <span data-ttu-id="96be6-124">출력</span><span class="sxs-lookup"><span data-stu-id="96be6-124">OUTPUTS</span></span>

### <span data-ttu-id="96be6-125">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="96be6-125">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="96be6-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="96be6-126">NOTES</span></span>
<span data-ttu-id="96be6-127">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 기계, 기계 학습, azureml</span><span class="sxs-lookup"><span data-stu-id="96be6-127">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="96be6-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="96be6-128">RELATED LINKS</span></span>
