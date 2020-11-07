---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlcommitmentplanusagehistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlanUsageHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentPlanUsageHistory.md
ms.openlocfilehash: 4d78d6e6a1b0ae5ea9f8815d537bca1496e24bbb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689447"
---
# <span data-ttu-id="6e5f3-101">Get-AzMlCommitmentPlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="6e5f3-101">Get-AzMlCommitmentPlanUsageHistory</span></span>

## <span data-ttu-id="6e5f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e5f3-102">SYNOPSIS</span></span>
<span data-ttu-id="6e5f3-103">지정 된 약정 계획에 대 한 사용 기록 정보를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e5f3-103">Retrieves usage history information for a specified commitment plan.</span></span>

## <span data-ttu-id="6e5f3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6e5f3-104">SYNTAX</span></span>

```
Get-AzMlCommitmentPlanUsageHistory -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e5f3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6e5f3-105">DESCRIPTION</span></span>
<span data-ttu-id="6e5f3-106">사용 된 리소스를 비롯 하 여 계획에 남아 있는 리소스를 포함 하 여 특정 약정 계획에 대 한 사용 기록 정보를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e5f3-106">Retrieves usage history information for a specified commitment plan, including resources used and resources remaining within the plan.</span></span>

## <span data-ttu-id="6e5f3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6e5f3-107">EXAMPLES</span></span>

### <span data-ttu-id="6e5f3-108">예제 1: 특정 약정 계획에 대 한 사용 기록 가져오기</span><span class="sxs-lookup"><span data-stu-id="6e5f3-108">Example 1: Get usage history for a specific commitment plan</span></span>
```
Get-AzMlCommitmentPlanUsageHistory -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="6e5f3-109">변수</span><span class="sxs-lookup"><span data-stu-id="6e5f3-109">PARAMETERS</span></span>

### <span data-ttu-id="6e5f3-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e5f3-110">-DefaultProfile</span></span>
<span data-ttu-id="6e5f3-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="6e5f3-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6e5f3-112">-이름</span><span class="sxs-lookup"><span data-stu-id="6e5f3-112">-Name</span></span>
<span data-ttu-id="6e5f3-113">Azure ML 약정 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6e5f3-113">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="6e5f3-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e5f3-114">-ResourceGroupName</span></span>
<span data-ttu-id="6e5f3-115">Azure ML 약정 계획에 대 한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6e5f3-115">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="6e5f3-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e5f3-116">CommonParameters</span></span>
<span data-ttu-id="6e5f3-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e5f3-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e5f3-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e5f3-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e5f3-119">입력</span><span class="sxs-lookup"><span data-stu-id="6e5f3-119">INPUTS</span></span>

### <span data-ttu-id="6e5f3-120">않아야</span><span class="sxs-lookup"><span data-stu-id="6e5f3-120">None</span></span>

## <span data-ttu-id="6e5f3-121">출력</span><span class="sxs-lookup"><span data-stu-id="6e5f3-121">OUTPUTS</span></span>

### <span data-ttu-id="6e5f3-122">MachineLearning. CommitmentPlans. \ PlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="6e5f3-122">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory</span></span>

## <span data-ttu-id="6e5f3-123">상속자</span><span class="sxs-lookup"><span data-stu-id="6e5f3-123">NOTES</span></span>
<span data-ttu-id="6e5f3-124">키워드: azure, azurerm, arm, resource, 관리, manager, machine, 기계 학습, azureml</span><span class="sxs-lookup"><span data-stu-id="6e5f3-124">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="6e5f3-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6e5f3-125">RELATED LINKS</span></span>
