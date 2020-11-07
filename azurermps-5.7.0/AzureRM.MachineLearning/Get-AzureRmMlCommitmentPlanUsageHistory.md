---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlcommitmentplanusagehistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlanUsageHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlanUsageHistory.md
ms.openlocfilehash: e92f32dab72a4a96be03f800297194711f275d70
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/21/2020
ms.locfileid: "93711927"
---
# <span data-ttu-id="3a28e-101">Get-AzureRmMlCommitmentPlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="3a28e-101">Get-AzureRmMlCommitmentPlanUsageHistory</span></span>

## <span data-ttu-id="3a28e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a28e-102">SYNOPSIS</span></span>
<span data-ttu-id="3a28e-103">지정 된 약정 계획에 대 한 사용 기록 정보를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a28e-103">Retrieves usage history information for a specified commitment plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a28e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3a28e-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentPlanUsageHistory -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a28e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3a28e-105">DESCRIPTION</span></span>
<span data-ttu-id="3a28e-106">사용 된 리소스를 비롯 하 여 계획에 남아 있는 리소스를 포함 하 여 특정 약정 계획에 대 한 사용 기록 정보를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a28e-106">Retrieves usage history information for a specified commitment plan, including resources used and resources remaining within the plan.</span></span>

## <span data-ttu-id="3a28e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3a28e-107">EXAMPLES</span></span>

### <span data-ttu-id="3a28e-108">--------------------------예제 1: 특정 약정 계획에 대 한 사용 기록 가져오기--------------------------</span><span class="sxs-lookup"><span data-stu-id="3a28e-108">--------------------------  Example 1: Get usage history for a specific commitment plan  --------------------------</span></span>
```
Get-AzureRmMlCommitmentPlanUsageHistory -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="3a28e-109">변수</span><span class="sxs-lookup"><span data-stu-id="3a28e-109">PARAMETERS</span></span>

### <span data-ttu-id="3a28e-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a28e-110">-DefaultProfile</span></span>
<span data-ttu-id="3a28e-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="3a28e-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3a28e-112">-이름</span><span class="sxs-lookup"><span data-stu-id="3a28e-112">-Name</span></span>
<span data-ttu-id="3a28e-113">Azure ML 약정 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3a28e-113">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="3a28e-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a28e-114">-ResourceGroupName</span></span>
<span data-ttu-id="3a28e-115">Azure ML 약정 계획에 대 한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3a28e-115">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="3a28e-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a28e-116">CommonParameters</span></span>
<span data-ttu-id="3a28e-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a28e-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a28e-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a28e-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a28e-119">입력</span><span class="sxs-lookup"><span data-stu-id="3a28e-119">INPUTS</span></span>

### <span data-ttu-id="3a28e-120">않아야</span><span class="sxs-lookup"><span data-stu-id="3a28e-120">None</span></span>
<span data-ttu-id="3a28e-121">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3a28e-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3a28e-122">출력</span><span class="sxs-lookup"><span data-stu-id="3a28e-122">OUTPUTS</span></span>

### <span data-ttu-id="3a28e-123">MachineLearning [] CommitmentPlans. PlanUsageHistory []</span><span class="sxs-lookup"><span data-stu-id="3a28e-123">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory[]</span></span>

## <span data-ttu-id="3a28e-124">상속자</span><span class="sxs-lookup"><span data-stu-id="3a28e-124">NOTES</span></span>
<span data-ttu-id="3a28e-125">키워드: azure, azurerm, arm, resource, 관리, manager, machine, 기계 학습, azureml</span><span class="sxs-lookup"><span data-stu-id="3a28e-125">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="3a28e-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3a28e-126">RELATED LINKS</span></span>

