---
Module Name: Az.Blueprint
Module Guid: ef36c942-4a71-4e19-9450-05a35843deb6
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.blueprint
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Az.Blueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Az.Blueprint.md
ms.openlocfilehash: 1722032406a81253ebf580f79172be85aa23c55f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363175"
---
# <span data-ttu-id="85181-101">Az.Blueprint 모듈</span><span class="sxs-lookup"><span data-stu-id="85181-101">Az.Blueprint Module</span></span>
## <span data-ttu-id="85181-102">설명</span><span class="sxs-lookup"><span data-stu-id="85181-102">Description</span></span>
<span data-ttu-id="85181-103">이 섹션의 항목에서는 Azure Resource Manager 프레임워크의 Azure Blueprints에 대한 Azure PowerShell cmdlet을 설명합니다.</span><span class="sxs-lookup"><span data-stu-id="85181-103">The topics in this section document the Azure PowerShell cmdlets for Azure Blueprints in the Azure Resource Manager framework.</span></span> <span data-ttu-id="85181-104">cmdlet은 Microsoft.Azure.PowerShell.Cmdlets.Blueprint 네임스페이스에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="85181-104">The cmdlets exist in the Microsoft.Azure.PowerShell.Cmdlets.Blueprint namespace.</span></span>

## <span data-ttu-id="85181-105">Az.Blueprint Cmdlet</span><span class="sxs-lookup"><span data-stu-id="85181-105">Az.Blueprint Cmdlets</span></span>
### [<span data-ttu-id="85181-106">Export-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="85181-106">Export-AzBlueprintWithArtifact</span></span>](Export-AzBlueprintWithArtifact.md)
<span data-ttu-id="85181-107">지정된 청사진 정의를 JSON 파일로 지정된 출력 위치로 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="85181-107">Export specified blueprint definition to the specified output location as a JSON file.</span></span> 

### [<span data-ttu-id="85181-108">Get-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="85181-108">Get-AzBlueprint</span></span>](Get-AzBlueprint.md)
<span data-ttu-id="85181-109">하나 이상의 청사진 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="85181-109">Get one or more blueprint definitions.</span></span>

### [<span data-ttu-id="85181-110">Get-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="85181-110">Get-AzBlueprintArtifact</span></span>](Get-AzBlueprintArtifact.md)
<span data-ttu-id="85181-111">청사진 정의에서 아티팩트를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="85181-111">Retrieve artifacts from a blueprint definition.</span></span>

### [<span data-ttu-id="85181-112">Get-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="85181-112">Get-AzBlueprintAssignment</span></span>](Get-AzBlueprintAssignment.md)
<span data-ttu-id="85181-113">하나 이상의 청사진 할당을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="85181-113">Get one or more blueprint assignments.</span></span>

### [<span data-ttu-id="85181-114">Import-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="85181-114">Import-AzBlueprintWithArtifact</span></span>](Import-AzBlueprintWithArtifact.md)
<span data-ttu-id="85181-115">JSON 형식으로 청사진 파일을 청사진 개체로 가져오고 지정된 구독 또는 관리 그룹 내에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="85181-115">Import a blueprint file in JSON format to a blueprint object and save it within the specified subscription or management group.</span></span>

### [<span data-ttu-id="85181-116">New-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="85181-116">New-AzBlueprint</span></span>](New-AzBlueprint.md)
<span data-ttu-id="85181-117">새 청사진 정의를 만들고 지정된 구독 또는 관리 그룹 내에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="85181-117">Create a new blueprint definition and save it within the specified subscription or management group.</span></span>

### [<span data-ttu-id="85181-118">New-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="85181-118">New-AzBlueprintArtifact</span></span>](New-AzBlueprintArtifact.md)
<span data-ttu-id="85181-119">새 아티팩트를 만들고 청사진 정의 내에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="85181-119">Create a new artifact and save it within a blueprint definition.</span></span>

### [<span data-ttu-id="85181-120">New-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="85181-120">New-AzBlueprintAssignment</span></span>](New-AzBlueprintAssignment.md)
<span data-ttu-id="85181-121">구독 또는 관리 그룹에 청사진 정의를 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="85181-121">Assign a blueprint definition to a subscription or a management group.</span></span>

### [<span data-ttu-id="85181-122">Publish-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="85181-122">Publish-AzBlueprint</span></span>](Publish-AzBlueprint.md)
<span data-ttu-id="85181-123">새 버전의 청사진을 게시합니다.</span><span class="sxs-lookup"><span data-stu-id="85181-123">Publish a new version of a blueprint.</span></span>

### [<span data-ttu-id="85181-124">Remove-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="85181-124">Remove-AzBlueprintAssignment</span></span>](Remove-AzBlueprintAssignment.md)
<span data-ttu-id="85181-125">구독 또는 관리 그룹에서 청사진 할당을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="85181-125">Remove a blueprint assignment from a subscription or a management group.</span></span>

### [<span data-ttu-id="85181-126">Set-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="85181-126">Set-AzBlueprint</span></span>](Set-AzBlueprint.md)
<span data-ttu-id="85181-127">청사진 정의를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="85181-127">Update a blueprint definition.</span></span>

### [<span data-ttu-id="85181-128">Set-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="85181-128">Set-AzBlueprintArtifact</span></span>](Set-AzBlueprintArtifact.md)
<span data-ttu-id="85181-129">청사진 정의에서 아티팩트를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="85181-129">Update an artifact in a blueprint definition.</span></span>

### [<span data-ttu-id="85181-130">Set-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="85181-130">Set-AzBlueprintAssignment</span></span>](Set-AzBlueprintAssignment.md)
<span data-ttu-id="85181-131">기존 청사진 할당을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="85181-131">Update an existing blueprint assignment.</span></span>

