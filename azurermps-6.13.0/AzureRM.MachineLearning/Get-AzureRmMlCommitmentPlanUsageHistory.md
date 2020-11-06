---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearning/get-azurermmlcommitmentplanusagehistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlanUsageHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlanUsageHistory.md
ms.openlocfilehash: 481d1e26ad769101f06acda5573175bd06331fac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537608"
---
# <span data-ttu-id="936be-101">Get-AzureRmMlCommitmentPlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="936be-101">Get-AzureRmMlCommitmentPlanUsageHistory</span></span>

## <span data-ttu-id="936be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="936be-102">SYNOPSIS</span></span>
<span data-ttu-id="936be-103">지정 된 약정 계획에 대 한 사용 기록 정보를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="936be-103">Retrieves usage history information for a specified commitment plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="936be-104">구문과</span><span class="sxs-lookup"><span data-stu-id="936be-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentPlanUsageHistory -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="936be-105">설명은</span><span class="sxs-lookup"><span data-stu-id="936be-105">DESCRIPTION</span></span>
<span data-ttu-id="936be-106">사용 된 리소스를 비롯 하 여 계획에 남아 있는 리소스를 포함 하 여 특정 약정 계획에 대 한 사용 기록 정보를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="936be-106">Retrieves usage history information for a specified commitment plan, including resources used and resources remaining within the plan.</span></span>

## <span data-ttu-id="936be-107">예제의</span><span class="sxs-lookup"><span data-stu-id="936be-107">EXAMPLES</span></span>

### <span data-ttu-id="936be-108">예제 1: 특정 약정 계획에 대 한 사용 기록 가져오기</span><span class="sxs-lookup"><span data-stu-id="936be-108">Example 1: Get usage history for a specific commitment plan</span></span>
```
Get-AzureRmMlCommitmentPlanUsageHistory -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="936be-109">변수</span><span class="sxs-lookup"><span data-stu-id="936be-109">PARAMETERS</span></span>

### <span data-ttu-id="936be-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="936be-110">-DefaultProfile</span></span>
<span data-ttu-id="936be-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="936be-111">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="936be-112">-이름</span><span class="sxs-lookup"><span data-stu-id="936be-112">-Name</span></span>
<span data-ttu-id="936be-113">Azure ML 약정 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="936be-113">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="936be-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="936be-114">-ResourceGroupName</span></span>
<span data-ttu-id="936be-115">Azure ML 약정 계획에 대 한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="936be-115">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="936be-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="936be-116">CommonParameters</span></span>
<span data-ttu-id="936be-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="936be-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="936be-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="936be-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="936be-119">입력</span><span class="sxs-lookup"><span data-stu-id="936be-119">INPUTS</span></span>

### <span data-ttu-id="936be-120">않아야</span><span class="sxs-lookup"><span data-stu-id="936be-120">None</span></span>

## <span data-ttu-id="936be-121">출력</span><span class="sxs-lookup"><span data-stu-id="936be-121">OUTPUTS</span></span>

### <span data-ttu-id="936be-122">MachineLearning. CommitmentPlans. \ PlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="936be-122">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory</span></span>

## <span data-ttu-id="936be-123">상속자</span><span class="sxs-lookup"><span data-stu-id="936be-123">NOTES</span></span>
<span data-ttu-id="936be-124">키워드: azure, azurerm, arm, resource, 관리, manager, machine, 기계 학습, azureml</span><span class="sxs-lookup"><span data-stu-id="936be-124">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="936be-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="936be-125">RELATED LINKS</span></span>
