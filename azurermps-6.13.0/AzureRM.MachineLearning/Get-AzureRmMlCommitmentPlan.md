---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlcommitmentplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: f0b081911d1bcd2a2b195d3185eb3b36505060c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702716"
---
# <span data-ttu-id="70825-101">Get-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="70825-101">Get-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="70825-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="70825-102">SYNOPSIS</span></span>
<span data-ttu-id="70825-103">하나 이상의 약정 계획에 대 한 요약 정보를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="70825-103">Retrieves the summary information for one or more commitment plans.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70825-104">구문과</span><span class="sxs-lookup"><span data-stu-id="70825-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="70825-105">설명은</span><span class="sxs-lookup"><span data-stu-id="70825-105">DESCRIPTION</span></span>
<span data-ttu-id="70825-106">약정 계획 정보를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="70825-106">Retrieves commitment plan information.</span></span>
<span data-ttu-id="70825-107">Paramenters에 따라 cmdlet은 특정 약정 계획, 현재 구독 내의 지정 된 리소스 그룹에 대 한 약정 계획 모음 또는 현재 구독 내의 약정 계획 컬렉션을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="70825-107">Depending on the paramenters passed, the cmdlet returns the a specific commitment plan, a collection of commitment plans for a specified resource group within the current subscription, or a collection of commitment plans within the current subscription.</span></span>

## <span data-ttu-id="70825-108">예제의</span><span class="sxs-lookup"><span data-stu-id="70825-108">EXAMPLES</span></span>

### <span data-ttu-id="70825-109">예제 1: 특정 약정 계획 가져오기</span><span class="sxs-lookup"><span data-stu-id="70825-109">Example 1: Get a specific commitment plan</span></span>
```
Get-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

### <span data-ttu-id="70825-110">예제 2: 현재 구독에서 모든 약정 계획 리소스 가져오기</span><span class="sxs-lookup"><span data-stu-id="70825-110">Example 2: Get all commitment plan resources in current subscription</span></span>
```
Get-AzureRmMlCommitmentPlan
```

### <span data-ttu-id="70825-111">예제 3: 현재 구독 및 지정 된 리소스 그룹에서 모든 약정 계획 가져오기</span><span class="sxs-lookup"><span data-stu-id="70825-111">Example 3: Get all commitment plans in the current subscription and given resource group</span></span>
```
Get-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup"
```

## <span data-ttu-id="70825-112">변수</span><span class="sxs-lookup"><span data-stu-id="70825-112">PARAMETERS</span></span>

### <span data-ttu-id="70825-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70825-113">-DefaultProfile</span></span>
<span data-ttu-id="70825-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="70825-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="70825-115">-이름</span><span class="sxs-lookup"><span data-stu-id="70825-115">-Name</span></span>
<span data-ttu-id="70825-116">약정 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="70825-116">The name of the commitment plan.</span></span>

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

### <span data-ttu-id="70825-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70825-117">-ResourceGroupName</span></span>
<span data-ttu-id="70825-118">Azure ML 약정 계획에 대 한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="70825-118">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="70825-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70825-119">CommonParameters</span></span>
<span data-ttu-id="70825-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="70825-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70825-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70825-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70825-122">입력</span><span class="sxs-lookup"><span data-stu-id="70825-122">INPUTS</span></span>

### <span data-ttu-id="70825-123">않아야</span><span class="sxs-lookup"><span data-stu-id="70825-123">None</span></span>

## <span data-ttu-id="70825-124">출력</span><span class="sxs-lookup"><span data-stu-id="70825-124">OUTPUTS</span></span>

### <span data-ttu-id="70825-125">MachineLearning. CommitmentPlans. \ CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="70825-125">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="70825-126">상속자</span><span class="sxs-lookup"><span data-stu-id="70825-126">NOTES</span></span>
<span data-ttu-id="70825-127">키워드: azure, azurerm, arm, resource, 관리, manager, machine, 기계 학습, azureml</span><span class="sxs-lookup"><span data-stu-id="70825-127">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="70825-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="70825-128">RELATED LINKS</span></span>
