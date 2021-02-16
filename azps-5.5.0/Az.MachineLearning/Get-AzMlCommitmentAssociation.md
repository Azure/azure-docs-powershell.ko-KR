---
external help file: Microsoft.Azure.PowerShell.Cmdlets.MachineLearning.dll-Help.xml
Module Name: Az.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/az.machinelearning/get-azmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MachineLearning/MachineLearning/help/Get-AzMlCommitmentAssociation.md
ms.openlocfilehash: 415645b1b4c1d0094b1466d833a29aa10b2b83b8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194169"
---
# <span data-ttu-id="f92df-101">Get-AzMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="f92df-101">Get-AzMlCommitmentAssociation</span></span>

## <span data-ttu-id="f92df-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f92df-102">SYNOPSIS</span></span>
<span data-ttu-id="f92df-103">하나 이상의 약정 연결에 대한 요약 정보를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="f92df-103">Retrieves the summary information for one or more commitment associations.</span></span>

## <span data-ttu-id="f92df-104">구문</span><span class="sxs-lookup"><span data-stu-id="f92df-104">SYNTAX</span></span>

```
Get-AzMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f92df-105">설명</span><span class="sxs-lookup"><span data-stu-id="f92df-105">DESCRIPTION</span></span>
<span data-ttu-id="f92df-106">약정 연결 정보를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="f92df-106">Retrieves commitment association information.</span></span>
<span data-ttu-id="f92df-107">전달된 매개 변수에 따라 cmdlet은 지정된 약정 계획에 대한 특정 약정 연결 또는 약정 연결 컬렉션을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f92df-107">Depending on the parameters passed, the cmdlet returns a specific commitment association or a collection of commitment associations for the specified commitment plan.</span></span>

## <span data-ttu-id="f92df-108">예제</span><span class="sxs-lookup"><span data-stu-id="f92df-108">EXAMPLES</span></span>

### <span data-ttu-id="f92df-109">예제 1: 특정 약정 연결 구하기</span><span class="sxs-lookup"><span data-stu-id="f92df-109">Example 1: Get a specific commitment association</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName" -Name "MyCommitmentAssociationName"
```

### <span data-ttu-id="f92df-110">예제 2: 지정된 약정 계획에 대한 모든 약정 연결 얻기</span><span class="sxs-lookup"><span data-stu-id="f92df-110">Example 2: Get all commitment associations for the specified commitment plan</span></span>
```
Get-AzMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName"
```

## <span data-ttu-id="f92df-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f92df-111">PARAMETERS</span></span>

### <span data-ttu-id="f92df-112">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="f92df-112">-CommitmentPlanName</span></span>
<span data-ttu-id="f92df-113">하나 이상의 약정 연결로 연결되는 Azure ML 약정 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f92df-113">The name of the Azure ML commitment plan which has one or more commitment associations.</span></span>

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

### <span data-ttu-id="f92df-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f92df-114">-DefaultProfile</span></span>
<span data-ttu-id="f92df-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f92df-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f92df-116">-Name</span><span class="sxs-lookup"><span data-stu-id="f92df-116">-Name</span></span>
<span data-ttu-id="f92df-117">Azure ML 약정 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f92df-117">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="f92df-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f92df-118">-ResourceGroupName</span></span>
<span data-ttu-id="f92df-119">Azure ML 약정 연결에 대한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f92df-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="f92df-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f92df-120">CommonParameters</span></span>
<span data-ttu-id="f92df-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f92df-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f92df-122">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f92df-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f92df-123">입력</span><span class="sxs-lookup"><span data-stu-id="f92df-123">INPUTS</span></span>

### <span data-ttu-id="f92df-124">없음</span><span class="sxs-lookup"><span data-stu-id="f92df-124">None</span></span>

## <span data-ttu-id="f92df-125">출력</span><span class="sxs-lookup"><span data-stu-id="f92df-125">OUTPUTS</span></span>

### <span data-ttu-id="f92df-126">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="f92df-126">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>

## <span data-ttu-id="f92df-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f92df-127">NOTES</span></span>
<span data-ttu-id="f92df-128">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 기계, 기계 학습, azureml</span><span class="sxs-lookup"><span data-stu-id="f92df-128">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="f92df-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f92df-129">RELATED LINKS</span></span>
