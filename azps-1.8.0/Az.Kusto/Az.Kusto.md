---
Module Name: Az.Kusto
Module Guid: 868389ce-dd36-4f57-a674-0970db085d9b
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.kusto
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Az.Kusto.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/Kusto/help/Az.Kusto.md
ms.openlocfilehash: de9b263e28983f2af4efb9ad5d4b3c06f2636033
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "93688854"
---
# <span data-ttu-id="24c87-101">A. Kusto 모듈</span><span class="sxs-lookup"><span data-stu-id="24c87-101">Az.Kusto Module</span></span>
## <span data-ttu-id="24c87-102">설명은</span><span class="sxs-lookup"><span data-stu-id="24c87-102">Description</span></span>
<span data-ttu-id="24c87-103">PowerShell에서 Kusto 리소스를 관리 하는 모듈입니다.</span><span class="sxs-lookup"><span data-stu-id="24c87-103">Module to manage Kusto resources in PowerShell.</span></span>

## <span data-ttu-id="24c87-104">A. Kusto Cmdlet</span><span class="sxs-lookup"><span data-stu-id="24c87-104">Az.Kusto Cmdlets</span></span>
### [<span data-ttu-id="24c87-105">Get-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="24c87-105">Get-AzKustoCluster</span></span>](Get-AzKustoCluster.md)
<span data-ttu-id="24c87-106">모든 Kusto 리소스 그룹의 클러스터를 나열 하거나 특정 kusto 클러스터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="24c87-106">List all Kusto clusters in a resource group or get a specific Kusto cluster.</span></span>

### [<span data-ttu-id="24c87-107">Get-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="24c87-107">Get-AzKustoDatabase</span></span>](Get-AzKustoDatabase.md)
<span data-ttu-id="24c87-108">모든 Kusto 클러스터의 데이터베이스를 나열 하거나 특정 Kusto 데이터베이스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="24c87-108">List all Kusto databases in a cluster or get a specific Kusto database.</span></span>

### [<span data-ttu-id="24c87-109">새로운 AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="24c87-109">New-AzKustoCluster</span></span>](New-AzKustoCluster.md)
<span data-ttu-id="24c87-110">새로운 Kusto를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="24c87-110">Creates a new Kusto cluster.</span></span>

### [<span data-ttu-id="24c87-111">새로운 AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="24c87-111">New-AzKustoDatabase</span></span>](New-AzKustoDatabase.md)
<span data-ttu-id="24c87-112">기존 클러스터에 새 Kusto 데이터베이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="24c87-112">Creates a new Kusto database in an existing cluster.</span></span>

### [<span data-ttu-id="24c87-113">제거-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="24c87-113">Remove-AzKustoCluster</span></span>](Remove-AzKustoCluster.md)
<span data-ttu-id="24c87-114">기존 Kusto 클러스터를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="24c87-114">Deletes an existing Kusto cluster.</span></span>

### [<span data-ttu-id="24c87-115">제거-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="24c87-115">Remove-AzKustoDatabase</span></span>](Remove-AzKustoDatabase.md)
<span data-ttu-id="24c87-116">기존 Kusto 데이터베이스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="24c87-116">Deletes an existing Kusto database.</span></span>

### [<span data-ttu-id="24c87-117">이력서-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="24c87-117">Resume-AzKustoCluster</span></span>](Resume-AzKustoCluster.md)
<span data-ttu-id="24c87-118">Suspeneded Kusto 클러스터를 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="24c87-118">Resume a suspeneded Kusto cluster.</span></span>

### [<span data-ttu-id="24c87-119">일시 중단-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="24c87-119">Suspend-AzKustoCluster</span></span>](Suspend-AzKustoCluster.md)
<span data-ttu-id="24c87-120">기존 Kusto 클러스터를 일시 중단 합니다.</span><span class="sxs-lookup"><span data-stu-id="24c87-120">Suspend an existing Kusto cluster.</span></span>

### [<span data-ttu-id="24c87-121">테스트-AzKustoClusterName</span><span class="sxs-lookup"><span data-stu-id="24c87-121">Test-AzKustoClusterName</span></span>](Test-AzKustoClusterName.md)
<span data-ttu-id="24c87-122">주어진 Kusto 클러스터 이름을 사용할 수 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="24c87-122">Check if a given Kusto cluster name is available.</span></span>

### [<span data-ttu-id="24c87-123">업데이트-AzKustoCluster</span><span class="sxs-lookup"><span data-stu-id="24c87-123">Update-AzKustoCluster</span></span>](Update-AzKustoCluster.md)
<span data-ttu-id="24c87-124">기존 Kusto 클러스터를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="24c87-124">Update an existing Kusto cluster.</span></span>

### [<span data-ttu-id="24c87-125">업데이트-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="24c87-125">Update-AzKustoDatabase</span></span>](Update-AzKustoDatabase.md)
<span data-ttu-id="24c87-126">기존 Kusto를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="24c87-126">Update an existing Kusto database.</span></span>

