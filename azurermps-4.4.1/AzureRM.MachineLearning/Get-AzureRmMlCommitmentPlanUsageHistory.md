---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlanUsageHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Get-AzureRmMlCommitmentPlanUsageHistory.md
ms.openlocfilehash: c80278e460368ca6ec78efb4f5e74e456816df47
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711543"
---
# <span data-ttu-id="2a10d-101">Get-AzureRmMlCommitmentPlanUsageHistory</span><span class="sxs-lookup"><span data-stu-id="2a10d-101">Get-AzureRmMlCommitmentPlanUsageHistory</span></span>

## <span data-ttu-id="2a10d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a10d-102">SYNOPSIS</span></span>
<span data-ttu-id="2a10d-103">지정 된 약정 계획에 대 한 사용 기록 정보를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a10d-103">Retrieves usage history information for a specified commitment plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a10d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2a10d-104">SYNTAX</span></span>

```
Get-AzureRmMlCommitmentPlanUsageHistory -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a10d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2a10d-105">DESCRIPTION</span></span>
<span data-ttu-id="2a10d-106">사용 된 리소스를 비롯 하 여 계획에 남아 있는 리소스를 포함 하 여 특정 약정 계획에 대 한 사용 기록 정보를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a10d-106">Retrieves usage history information for a specified commitment plan, including resources used and resources remaining within the plan.</span></span>

## <span data-ttu-id="2a10d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2a10d-107">EXAMPLES</span></span>

### <span data-ttu-id="2a10d-108">--------------------------예제 1: 특정 약정 계획에 대 한 사용 기록 가져오기--------------------------</span><span class="sxs-lookup"><span data-stu-id="2a10d-108">--------------------------  Example 1: Get usage history for a specific commitment plan  --------------------------</span></span>
<span data-ttu-id="2a10d-109">@ {paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="2a10d-109">@{paragraph=PS C:\\\>}</span></span>





```
Get-AzureRmMlCommitmentPlanUsageHistory -ResourceGroupName "MyResourceGroup" -Name "MyCommitmentPlanName"
```

## <span data-ttu-id="2a10d-110">변수</span><span class="sxs-lookup"><span data-stu-id="2a10d-110">PARAMETERS</span></span>

### <span data-ttu-id="2a10d-111">-이름</span><span class="sxs-lookup"><span data-stu-id="2a10d-111">-Name</span></span>
<span data-ttu-id="2a10d-112">Azure ML 약정 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2a10d-112">The name of the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="2a10d-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a10d-113">-ResourceGroupName</span></span>
<span data-ttu-id="2a10d-114">Azure ML 약정 계획에 대 한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2a10d-114">The name of the resource group for the Azure ML commitment plan.</span></span>

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

### <span data-ttu-id="2a10d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a10d-115">-DefaultProfile</span></span>
<span data-ttu-id="2a10d-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2a10d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a10d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a10d-117">CommonParameters</span></span>
<span data-ttu-id="2a10d-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2a10d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a10d-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a10d-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a10d-120">입력</span><span class="sxs-lookup"><span data-stu-id="2a10d-120">INPUTS</span></span>

## <span data-ttu-id="2a10d-121">출력</span><span class="sxs-lookup"><span data-stu-id="2a10d-121">OUTPUTS</span></span>

### <span data-ttu-id="2a10d-122">MachineLearning [] CommitmentPlans. PlanUsageHistory []</span><span class="sxs-lookup"><span data-stu-id="2a10d-122">Microsoft.Azure.Management.MachineLearning.CommitmentPlans.Models.PlanUsageHistory[]</span></span>

## <span data-ttu-id="2a10d-123">상속자</span><span class="sxs-lookup"><span data-stu-id="2a10d-123">NOTES</span></span>
<span data-ttu-id="2a10d-124">키워드: azure, azurerm, arm, resource, 관리, manager, machine, 기계 학습, azureml</span><span class="sxs-lookup"><span data-stu-id="2a10d-124">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="2a10d-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2a10d-125">RELATED LINKS</span></span>

