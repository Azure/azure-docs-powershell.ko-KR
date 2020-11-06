---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlan.md
ms.openlocfilehash: 9f9789d288773b16b2003e23b00674c12ca08738
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532244"
---
# <span data-ttu-id="21c8e-101">Get-AzureRmMlCommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="21c8e-101">Get-AzureRmMlCommitmentPlan</span></span>

## <span data-ttu-id="21c8e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21c8e-102">SYNOPSIS</span></span>
<span data-ttu-id="21c8e-103">하나 이상의 약정 계획에 대 한 요약 정보를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="21c8e-103">Retrieves the summary information for one or more commitment plans.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21c8e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="21c8e-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21c8e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="21c8e-105">DESCRIPTION</span></span>
<span data-ttu-id="21c8e-106">약정 계획 정보를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="21c8e-106">Retrieves commitment plan information.</span></span>
<span data-ttu-id="21c8e-107">Paramenters에 따라 cmdlet은 특정 약정 계획, 현재 구독 내의 지정 된 리소스 그룹에 대 한 약정 계획 모음 또는 현재 구독 내의 약정 계획 컬렉션을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="21c8e-107">Depending on the paramenters passed, the cmdlet returns the a specific commitment plan, a collection of commitment plans for a specified resource group within the current subscription, or a collection of commitment plans within the current subscription.</span></span>

## <span data-ttu-id="21c8e-108">예제의</span><span class="sxs-lookup"><span data-stu-id="21c8e-108">EXAMPLES</span></span>

### <span data-ttu-id="21c8e-109">--------------------------예제 1: 특정 약정 계획 가져오기--------------------------</span><span class="sxs-lookup"><span data-stu-id="21c8e-109">--------------------------  Example 1: Get a specific commitment plan  --------------------------</span></span>
<span data-ttu-id="21c8e-110">@ {paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="21c8e-110">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

### <span data-ttu-id="21c8e-111">--------------------------예제 2: 현재 구독에서 모든 약정 계획 리소스 가져오기--------------------------</span><span class="sxs-lookup"><span data-stu-id="21c8e-111">--------------------------  Example 2: Get all commitment plan resources in current subscription  --------------------------</span></span>
<span data-ttu-id="21c8e-112">@ {paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="21c8e-112">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlCommitmentPlan
```

### <span data-ttu-id="21c8e-113">--------------------------예제 3: 현재 구독 및 지정 된 리소스 그룹에서 모든 약정 계획 가져오기--------------------------</span><span class="sxs-lookup"><span data-stu-id="21c8e-113">--------------------------  Example 3: Get all commitment plans in the current subscription and given resource group  --------------------------</span></span>
<span data-ttu-id="21c8e-114">@ {paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="21c8e-114">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlCommitmentPlan -ResourceGroupName "MyResourceGroup"
```

## <span data-ttu-id="21c8e-115">변수</span><span class="sxs-lookup"><span data-stu-id="21c8e-115">PARAMETERS</span></span>

### <span data-ttu-id="21c8e-116">-이름</span><span class="sxs-lookup"><span data-stu-id="21c8e-116">-Name</span></span>
<span data-ttu-id="21c8e-117">약정 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="21c8e-117">The name of the commitment plan.</span></span>

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

### <span data-ttu-id="21c8e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21c8e-118">-ResourceGroupName</span></span>
<span data-ttu-id="21c8e-119">Azure ML 약정 계획에 대 한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="21c8e-119">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="21c8e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21c8e-120">-DefaultProfile</span></span>
<span data-ttu-id="21c8e-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="21c8e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21c8e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21c8e-122">CommonParameters</span></span>
<span data-ttu-id="21c8e-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="21c8e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21c8e-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21c8e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21c8e-125">입력</span><span class="sxs-lookup"><span data-stu-id="21c8e-125">INPUTS</span></span>

## <span data-ttu-id="21c8e-126">출력</span><span class="sxs-lookup"><span data-stu-id="21c8e-126">OUTPUTS</span></span>

### <span data-ttu-id="21c8e-127">MachineLearning. CommitmentPlans. \ CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="21c8e-127">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>
<span data-ttu-id="21c8e-128">MachineLearning [] CommitmentPlans. CommitmentPlan []</span><span class="sxs-lookup"><span data-stu-id="21c8e-128">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan[]</span></span>

## <span data-ttu-id="21c8e-129">상속자</span><span class="sxs-lookup"><span data-stu-id="21c8e-129">NOTES</span></span>
<span data-ttu-id="21c8e-130">키워드: azure, azurerm, arm, resource, 관리, manager, machine, 기계 학습, azureml</span><span class="sxs-lookup"><span data-stu-id="21c8e-130">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="21c8e-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="21c8e-131">RELATED LINKS</span></span>

