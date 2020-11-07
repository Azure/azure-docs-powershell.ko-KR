---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentAssociation.md
ms.openlocfilehash: d22632f830c40cd992f874d4f09c05b8a3fd9a5d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867565"
---
# <span data-ttu-id="e10dd-101">Get-AzMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="e10dd-101">Get-AzMlCommitmentAssociation</span></span>

## <span data-ttu-id="e10dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e10dd-102">SYNOPSIS</span></span>
<span data-ttu-id="e10dd-103">하나 이상의 약정 연결에 대 한 요약 정보를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="e10dd-103">Retrieves the summary information for one or more commitment associations.</span></span>

## <span data-ttu-id="e10dd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e10dd-104">SYNTAX</span></span>

```
Get-AzMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e10dd-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e10dd-105">DESCRIPTION</span></span>
<span data-ttu-id="e10dd-106">약정 연결 정보를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="e10dd-106">Retrieves commitment association information.</span></span>
<span data-ttu-id="e10dd-107">Paramenters에 따라 cmdlet은 지정 된 약정 계획에 대 한 특정 약정 연결 또는 약정 연결 컬렉션을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e10dd-107">Depending on the paramenters passed, the cmdlet returns a specific commitment association or a collection of commitment associations for the specified commitment plan.</span></span>

## <span data-ttu-id="e10dd-108">예제의</span><span class="sxs-lookup"><span data-stu-id="e10dd-108">EXAMPLES</span></span>

### <span data-ttu-id="e10dd-109">예제 1: 특정 약정 연결 가져오기</span><span class="sxs-lookup"><span data-stu-id="e10dd-109">Example 1: Get a specific commitment association</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName" -Name "MyCommitmentAssociationName"
```

### <span data-ttu-id="e10dd-110">예제 2: 지정 된 약정 계획에 대 한 모든 약정 연결 가져오기</span><span class="sxs-lookup"><span data-stu-id="e10dd-110">Example 2: Get all commitment associations for the specified commitment plan</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName"
```

## <span data-ttu-id="e10dd-111">변수</span><span class="sxs-lookup"><span data-stu-id="e10dd-111">PARAMETERS</span></span>

### <span data-ttu-id="e10dd-112">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="e10dd-112">-CommitmentPlanName</span></span>
<span data-ttu-id="e10dd-113">하나 이상의 약정 연관이 있는 Azure ML 약정 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e10dd-113">The name of the Azure ML commitment plan which has one or more commitment associations.</span></span>

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

### <span data-ttu-id="e10dd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e10dd-114">-DefaultProfile</span></span>
<span data-ttu-id="e10dd-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e10dd-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e10dd-116">-이름</span><span class="sxs-lookup"><span data-stu-id="e10dd-116">-Name</span></span>
<span data-ttu-id="e10dd-117">Azure ML 약정 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e10dd-117">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="e10dd-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e10dd-118">-ResourceGroupName</span></span>
<span data-ttu-id="e10dd-119">Azure ML 약정 연결에 대 한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e10dd-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="e10dd-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e10dd-120">CommonParameters</span></span>
<span data-ttu-id="e10dd-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e10dd-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e10dd-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e10dd-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e10dd-123">입력</span><span class="sxs-lookup"><span data-stu-id="e10dd-123">INPUTS</span></span>

### <span data-ttu-id="e10dd-124">않아야</span><span class="sxs-lookup"><span data-stu-id="e10dd-124">None</span></span>

## <span data-ttu-id="e10dd-125">출력</span><span class="sxs-lookup"><span data-stu-id="e10dd-125">OUTPUTS</span></span>

### <span data-ttu-id="e10dd-126">MachineLearning. CommitmentPlans. \ CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="e10dd-126">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="e10dd-127">상속자</span><span class="sxs-lookup"><span data-stu-id="e10dd-127">NOTES</span></span>
<span data-ttu-id="e10dd-128">키워드: azure, azurerm, arm, resource, 관리, manager, machine, 기계 학습, azureml</span><span class="sxs-lookup"><span data-stu-id="e10dd-128">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="e10dd-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e10dd-129">RELATED LINKS</span></span>
