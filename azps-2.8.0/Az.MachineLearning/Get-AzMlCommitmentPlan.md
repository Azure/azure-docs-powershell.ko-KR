---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlan.md
ms.openlocfilehash: e8c3fbb6f3d5f9ca3592546f4039c484003811f9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689451"
---
# <span data-ttu-id="59beb-101">Get-AzMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="59beb-101">Get-AzMlCommitmentPlan</span></span>

## <span data-ttu-id="59beb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59beb-102">SYNOPSIS</span></span>
<span data-ttu-id="59beb-103">하나 이상의 약정 계획에 대 한 요약 정보를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="59beb-103">Retrieves the summary information for one or more commitment plans.</span></span>

## <span data-ttu-id="59beb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="59beb-104">SYNTAX</span></span>

```
Get-AzMlCommitmentPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59beb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="59beb-105">DESCRIPTION</span></span>
<span data-ttu-id="59beb-106">약정 계획 정보를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="59beb-106">Retrieves commitment plan information.</span></span>
<span data-ttu-id="59beb-107">전달 된 매개 변수에 따라 cmdlet은 특정 약정 계획, 현재 구독 내의 지정 된 리소스 그룹에 대 한 약정 계획 모음 또는 현재 구독 내의 약정 계획 컬렉션을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="59beb-107">Depending on the parameters passed, the cmdlet returns the a specific commitment plan, a collection of commitment plans for a specified resource group within the current subscription, or a collection of commitment plans within the current subscription.</span></span>

## <span data-ttu-id="59beb-108">예제의</span><span class="sxs-lookup"><span data-stu-id="59beb-108">EXAMPLES</span></span>

### <span data-ttu-id="59beb-109">예제 1: 특정 약정 계획 가져오기</span><span class="sxs-lookup"><span data-stu-id="59beb-109">Example 1: Get a specific commitment plan</span></span>
```
Get-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

### <span data-ttu-id="59beb-110">예제 2: 현재 구독에서 모든 약정 계획 리소스 가져오기</span><span class="sxs-lookup"><span data-stu-id="59beb-110">Example 2: Get all commitment plan resources in current subscription</span></span>
```
Get-AzMlCommitmentPlan
```

### <span data-ttu-id="59beb-111">예제 3: 현재 구독 및 지정 된 리소스 그룹에서 모든 약정 계획 가져오기</span><span class="sxs-lookup"><span data-stu-id="59beb-111">Example 3: Get all commitment plans in the current subscription and given resource group</span></span>
```
Get-AzMlCommitmentPlan -ResourceGroupName "MyResourceGroup"
```

## <span data-ttu-id="59beb-112">변수</span><span class="sxs-lookup"><span data-stu-id="59beb-112">PARAMETERS</span></span>

### <span data-ttu-id="59beb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59beb-113">-DefaultProfile</span></span>
<span data-ttu-id="59beb-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="59beb-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="59beb-115">-이름</span><span class="sxs-lookup"><span data-stu-id="59beb-115">-Name</span></span>
<span data-ttu-id="59beb-116">약정 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59beb-116">The name of the commitment plan.</span></span>

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

### <span data-ttu-id="59beb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59beb-117">-ResourceGroupName</span></span>
<span data-ttu-id="59beb-118">Azure ML 약정 계획에 대 한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59beb-118">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="59beb-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59beb-119">CommonParameters</span></span>
<span data-ttu-id="59beb-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="59beb-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59beb-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59beb-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59beb-122">입력</span><span class="sxs-lookup"><span data-stu-id="59beb-122">INPUTS</span></span>

### <span data-ttu-id="59beb-123">않아야</span><span class="sxs-lookup"><span data-stu-id="59beb-123">None</span></span>

## <span data-ttu-id="59beb-124">출력</span><span class="sxs-lookup"><span data-stu-id="59beb-124">OUTPUTS</span></span>

### <span data-ttu-id="59beb-125">MachineLearning. CommitmentPlans. \ CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="59beb-125">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="59beb-126">상속자</span><span class="sxs-lookup"><span data-stu-id="59beb-126">NOTES</span></span>
<span data-ttu-id="59beb-127">키워드: azure, azurerm, arm, resource, 관리, manager, machine, 기계 학습, azureml</span><span class="sxs-lookup"><span data-stu-id="59beb-127">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="59beb-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="59beb-128">RELATED LINKS</span></span>
