---
Module Name: Az.Kusto
Module Guid: 868389ce-dd36-4f57-a674-0970db085d9b
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.kusto
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Az.Kusto.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Az.Kusto.md
ms.openlocfilehash: be3a0f654c1b7120b82f1dc386b845f69771717f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034598"
---
# <span data-ttu-id="8b3af-101">A. Kusto 모듈</span><span class="sxs-lookup"><span data-stu-id="8b3af-101">Az.Kusto Module</span></span>
## <span data-ttu-id="8b3af-102">설명은</span><span class="sxs-lookup"><span data-stu-id="8b3af-102">Description</span></span>
<span data-ttu-id="8b3af-103">PowerShell에서 Kusto 리소스를 관리 하는 모듈입니다.</span><span class="sxs-lookup"><span data-stu-id="8b3af-103">Module to manage Kusto resources in PowerShell.</span></span>

## <span data-ttu-id="8b3af-104">A. Kusto Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8b3af-104">Az.Kusto Cmdlets</span></span>
### [<span data-ttu-id="8b3af-105">Get-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="8b3af-105">Get-AzKustoCluster</span></span>](Get-AzKustoCluster.md)
<span data-ttu-id="8b3af-106">모든 Kusto 리소스 그룹의 클러스터를 나열 하거나 특정 kusto 클러스터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8b3af-106">List all Kusto clusters in a resource group or get a specific Kusto cluster.</span></span>

### [<span data-ttu-id="8b3af-107">Get-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="8b3af-107">Get-AzKustoDatabase</span></span>](Get-AzKustoDatabase.md)
<span data-ttu-id="8b3af-108">모든 Kusto 클러스터의 데이터베이스를 나열 하거나 특정 Kusto 데이터베이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8b3af-108">List all Kusto databases in a cluster or get a specific Kusto database.</span></span>

### [<span data-ttu-id="8b3af-109">새로운 AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="8b3af-109">New-AzKustoCluster</span></span>](New-AzKustoCluster.md)
<span data-ttu-id="8b3af-110">새로운 Kusto를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8b3af-110">Creates a new Kusto cluster.</span></span>

### [<span data-ttu-id="8b3af-111">새로운 AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="8b3af-111">New-AzKustoDatabase</span></span>](New-AzKustoDatabase.md)
<span data-ttu-id="8b3af-112">기존 클러스터에 새 Kusto 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8b3af-112">Creates a new Kusto database in an existing cluster.</span></span>

### [<span data-ttu-id="8b3af-113">제거-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="8b3af-113">Remove-AzKustoCluster</span></span>](Remove-AzKustoCluster.md)
<span data-ttu-id="8b3af-114">기존 Kusto 클러스터를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b3af-114">Deletes an existing Kusto cluster.</span></span>

### [<span data-ttu-id="8b3af-115">제거-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="8b3af-115">Remove-AzKustoDatabase</span></span>](Remove-AzKustoDatabase.md)
<span data-ttu-id="8b3af-116">기존 Kusto 데이터베이스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b3af-116">Deletes an existing Kusto database.</span></span>

### [<span data-ttu-id="8b3af-117">이력서-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="8b3af-117">Resume-AzKustoCluster</span></span>](Resume-AzKustoCluster.md)
<span data-ttu-id="8b3af-118">일시 중단 된 Kusto 클러스터를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b3af-118">Resume a suspended Kusto cluster.</span></span>

### [<span data-ttu-id="8b3af-119">일시 중단-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="8b3af-119">Suspend-AzKustoCluster</span></span>](Suspend-AzKustoCluster.md)
<span data-ttu-id="8b3af-120">기존 Kusto 클러스터를 일시 중단 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b3af-120">Suspend an existing Kusto cluster.</span></span>

### [<span data-ttu-id="8b3af-121">테스트-AzKustoClusterName</span><span class="sxs-lookup"><span data-stu-id="8b3af-121">Test-AzKustoClusterName</span></span>](Test-AzKustoClusterName.md)
<span data-ttu-id="8b3af-122">주어진 Kusto 클러스터 이름을 사용할 수 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b3af-122">Check if a given Kusto cluster name is available.</span></span>

### [<span data-ttu-id="8b3af-123">업데이트-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="8b3af-123">Update-AzKustoCluster</span></span>](Update-AzKustoCluster.md)
<span data-ttu-id="8b3af-124">기존 Kusto 클러스터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b3af-124">Update an existing Kusto cluster.</span></span>

### [<span data-ttu-id="8b3af-125">업데이트-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="8b3af-125">Update-AzKustoDatabase</span></span>](Update-AzKustoDatabase.md)
<span data-ttu-id="8b3af-126">기존 Kusto를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8b3af-126">Update an existing Kusto database.</span></span>

