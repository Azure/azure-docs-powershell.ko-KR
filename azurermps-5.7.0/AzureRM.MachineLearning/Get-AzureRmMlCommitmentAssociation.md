---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlcommitmentassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentAssociation.md
ms.openlocfilehash: 3be16cd371543848d650711241dbcb8828a5ba32
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535971"
---
# <span data-ttu-id="e1a68-101">Get-AzureRmMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="e1a68-101">Get-AzureRmMlCommitmentAssociation</span></span>

## <span data-ttu-id="e1a68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1a68-102">SYNOPSIS</span></span>
<span data-ttu-id="e1a68-103">하나 이상의 약정 연결에 대 한 요약 정보를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1a68-103">Retrieves the summary information for one or more commitment associations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1a68-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e1a68-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1a68-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e1a68-105">DESCRIPTION</span></span>
<span data-ttu-id="e1a68-106">약정 연결 정보를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1a68-106">Retrieves commitment association information.</span></span>
<span data-ttu-id="e1a68-107">Paramenters에 따라 cmdlet은 지정 된 약정 계획에 대 한 특정 약정 연결 또는 약정 연결 컬렉션을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1a68-107">Depending on the paramenters passed, the cmdlet returns a specific commitment association or a collection of commitment associations for the specified commitment plan.</span></span>

## <span data-ttu-id="e1a68-108">예제의</span><span class="sxs-lookup"><span data-stu-id="e1a68-108">EXAMPLES</span></span>

### <span data-ttu-id="e1a68-109">--------------------------예제 1: 특정 약정 연결 가져오기--------------------------</span><span class="sxs-lookup"><span data-stu-id="e1a68-109">--------------------------  Example 1: Get a specific commitment association  --------------------------</span></span>
```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName" -Name "MyCommitmentAssociationName"
```

### <span data-ttu-id="e1a68-110">--------------------------예제 2: 지정 된 약정 계획에 대 한 모든 약정 연결 가져오기--------------------------</span><span class="sxs-lookup"><span data-stu-id="e1a68-110">--------------------------  Example 2: Get all commitment associations for the specified commitment plan  --------------------------</span></span>
```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName"
```

## <span data-ttu-id="e1a68-111">변수</span><span class="sxs-lookup"><span data-stu-id="e1a68-111">PARAMETERS</span></span>

### <span data-ttu-id="e1a68-112">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="e1a68-112">-CommitmentPlanName</span></span>
<span data-ttu-id="e1a68-113">하나 이상의 약정 연관이 있는 Azure ML 약정 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e1a68-113">The name of the Azure ML commitment plan which has one or more commitment associations.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1a68-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1a68-114">-DefaultProfile</span></span>
<span data-ttu-id="e1a68-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e1a68-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1a68-116">-이름</span><span class="sxs-lookup"><span data-stu-id="e1a68-116">-Name</span></span>
<span data-ttu-id="e1a68-117">Azure ML 약정 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e1a68-117">The name of the Azure ML commitment association.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1a68-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1a68-118">-ResourceGroupName</span></span>
<span data-ttu-id="e1a68-119">Azure ML 약정 연결에 대 한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e1a68-119">The name of the resource group for the Azure ML commitment association.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1a68-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1a68-120">CommonParameters</span></span>
<span data-ttu-id="e1a68-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1a68-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1a68-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1a68-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1a68-123">입력</span><span class="sxs-lookup"><span data-stu-id="e1a68-123">INPUTS</span></span>

### <span data-ttu-id="e1a68-124">않아야</span><span class="sxs-lookup"><span data-stu-id="e1a68-124">None</span></span>
<span data-ttu-id="e1a68-125">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e1a68-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e1a68-126">출력</span><span class="sxs-lookup"><span data-stu-id="e1a68-126">OUTPUTS</span></span>

### <span data-ttu-id="e1a68-127">MachineLearning. CommitmentPlans. \ CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="e1a68-127">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>
<span data-ttu-id="e1a68-128">MachineLearning [] CommitmentPlans. CommitmentPlan []</span><span class="sxs-lookup"><span data-stu-id="e1a68-128">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan[]</span></span>

## <span data-ttu-id="e1a68-129">상속자</span><span class="sxs-lookup"><span data-stu-id="e1a68-129">NOTES</span></span>
<span data-ttu-id="e1a68-130">키워드: azure, azurerm, arm, resource, 관리, manager, machine, 기계 학습, azureml</span><span class="sxs-lookup"><span data-stu-id="e1a68-130">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="e1a68-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e1a68-131">RELATED LINKS</span></span>

