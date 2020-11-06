---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentAssociation.md
ms.openlocfilehash: 63c0184b9104b939073c4d58313777e8940d0f93
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532245"
---
# <span data-ttu-id="ebb2a-101">Get-AzureRmMlCommitmentAssociation</span><span class="sxs-lookup"><span data-stu-id="ebb2a-101">Get-AzureRmMlCommitmentAssociation</span></span>

## <span data-ttu-id="ebb2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ebb2a-102">SYNOPSIS</span></span>
<span data-ttu-id="ebb2a-103">하나 이상의 약정 연결에 대 한 요약 정보를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb2a-103">Retrieves the summary information for one or more commitment associations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ebb2a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ebb2a-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName <String> -CommitmentPlanName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ebb2a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ebb2a-105">DESCRIPTION</span></span>
<span data-ttu-id="ebb2a-106">약정 연결 정보를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb2a-106">Retrieves commitment association information.</span></span>
<span data-ttu-id="ebb2a-107">Paramenters에 따라 cmdlet은 지정 된 약정 계획에 대 한 특정 약정 연결 또는 약정 연결 컬렉션을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb2a-107">Depending on the paramenters passed, the cmdlet returns a specific commitment association or a collection of commitment associations for the specified commitment plan.</span></span>

## <span data-ttu-id="ebb2a-108">예제의</span><span class="sxs-lookup"><span data-stu-id="ebb2a-108">EXAMPLES</span></span>

### <span data-ttu-id="ebb2a-109">--------------------------예제 1: 특정 약정 연결 가져오기--------------------------</span><span class="sxs-lookup"><span data-stu-id="ebb2a-109">--------------------------  Example 1: Get a specific commitment association  --------------------------</span></span>
<span data-ttu-id="ebb2a-110">@ {paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="ebb2a-110">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName" -Name "MyCommitmentAssociationName"
```

### <span data-ttu-id="ebb2a-111">--------------------------예제 2: 지정 된 약정 계획에 대 한 모든 약정 연결 가져오기--------------------------</span><span class="sxs-lookup"><span data-stu-id="ebb2a-111">--------------------------  Example 2: Get all commitment associations for the specified commitment plan  --------------------------</span></span>
<span data-ttu-id="ebb2a-112">@ {paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="ebb2a-112">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlCommitmentAssociation -ResourceGroupName "MyResourceGroup" -CommitmentPlanName "MyCommitmentPlanName"
```

## <span data-ttu-id="ebb2a-113">변수</span><span class="sxs-lookup"><span data-stu-id="ebb2a-113">PARAMETERS</span></span>

### <span data-ttu-id="ebb2a-114">-CommitmentPlanName</span><span class="sxs-lookup"><span data-stu-id="ebb2a-114">-CommitmentPlanName</span></span>
<span data-ttu-id="ebb2a-115">하나 이상의 약정 연관이 있는 Azure ML 약정 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ebb2a-115">The name of the Azure ML commitment plan which has one or more commitment associations.</span></span>

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

### <span data-ttu-id="ebb2a-116">-이름</span><span class="sxs-lookup"><span data-stu-id="ebb2a-116">-Name</span></span>
<span data-ttu-id="ebb2a-117">Azure ML 약정 연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ebb2a-117">The name of the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="ebb2a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebb2a-118">-ResourceGroupName</span></span>
<span data-ttu-id="ebb2a-119">Azure ML 약정 연결에 대 한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ebb2a-119">The name of the resource group for the Azure ML commitment association.</span></span>

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

### <span data-ttu-id="ebb2a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebb2a-120">-DefaultProfile</span></span>
<span data-ttu-id="ebb2a-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ebb2a-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ebb2a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebb2a-122">CommonParameters</span></span>
<span data-ttu-id="ebb2a-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ebb2a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebb2a-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebb2a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebb2a-125">입력</span><span class="sxs-lookup"><span data-stu-id="ebb2a-125">INPUTS</span></span>

## <span data-ttu-id="ebb2a-126">출력</span><span class="sxs-lookup"><span data-stu-id="ebb2a-126">OUTPUTS</span></span>

### <span data-ttu-id="ebb2a-127">MachineLearning. CommitmentPlans. \ CommitmentPlan</span><span class="sxs-lookup"><span data-stu-id="ebb2a-127">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan</span></span>
<span data-ttu-id="ebb2a-128">MachineLearning [] CommitmentPlans. CommitmentPlan []</span><span class="sxs-lookup"><span data-stu-id="ebb2a-128">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.CommitmentPlan[]</span></span>

## <span data-ttu-id="ebb2a-129">상속자</span><span class="sxs-lookup"><span data-stu-id="ebb2a-129">NOTES</span></span>
<span data-ttu-id="ebb2a-130">키워드: azure, azurerm, arm, resource, 관리, manager, machine, 기계 학습, azureml</span><span class="sxs-lookup"><span data-stu-id="ebb2a-130">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="ebb2a-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ebb2a-131">RELATED LINKS</span></span>

