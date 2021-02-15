---
Module Name: Az.CostManagement
Module Guid: 4cd9af10-559e-4fb9-8dcd-d3e8eb9e03b7
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.costmanagement
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Az.CostManagement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CostManagement/help/Az.CostManagement.md
ms.openlocfilehash: 0bfac4d12c15bef8b16e9ba239423b1443a9f5b7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196708"
---
# <span data-ttu-id="52d04-101">Az.CostManagement 모듈</span><span class="sxs-lookup"><span data-stu-id="52d04-101">Az.CostManagement Module</span></span>
## <span data-ttu-id="52d04-102">설명</span><span class="sxs-lookup"><span data-stu-id="52d04-102">Description</span></span>
<span data-ttu-id="52d04-103">Microsoft Azure PowerShell: 비용 cmdlet</span><span class="sxs-lookup"><span data-stu-id="52d04-103">Microsoft Azure PowerShell: Cost cmdlets</span></span>

## <span data-ttu-id="52d04-104">Az.CostManagement Cmdlet</span><span class="sxs-lookup"><span data-stu-id="52d04-104">Az.CostManagement Cmdlets</span></span>
### [<span data-ttu-id="52d04-105">Get-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="52d04-105">Get-AzCostManagementExport</span></span>](Get-AzCostManagementExport.md)
<span data-ttu-id="52d04-106">내보내기 이름으로 정의된 범위에 대한 내보내기 작업을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="52d04-106">The operation to get the export for the defined scope by export name.</span></span>

### [<span data-ttu-id="52d04-107">Get-AzCostManagementExportExecutionHistory</span><span class="sxs-lookup"><span data-stu-id="52d04-107">Get-AzCostManagementExportExecutionHistory</span></span>](Get-AzCostManagementExportExecutionHistory.md)
<span data-ttu-id="52d04-108">정의된 범위 및 내보내기 이름에 대한 내보내기 실행 기록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="52d04-108">The operation to get the execution history of an export for the defined scope and export name.</span></span>

### [<span data-ttu-id="52d04-109">Invoke-AzCostManagementExecuteExport</span><span class="sxs-lookup"><span data-stu-id="52d04-109">Invoke-AzCostManagementExecuteExport</span></span>](Invoke-AzCostManagementExecuteExport.md)
<span data-ttu-id="52d04-110">내보내기 실행 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="52d04-110">The operation to execute an export.</span></span>

### [<span data-ttu-id="52d04-111">Invoke-AzCostManagementQuery</span><span class="sxs-lookup"><span data-stu-id="52d04-111">Invoke-AzCostManagementQuery</span></span>](Invoke-AzCostManagementQuery.md)
<span data-ttu-id="52d04-112">정의된 범위에 대한 사용 데이터를 쿼리합니다.</span><span class="sxs-lookup"><span data-stu-id="52d04-112">Query the usage data for scope defined.</span></span>

### [<span data-ttu-id="52d04-113">New-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="52d04-113">New-AzCostManagementExport</span></span>](New-AzCostManagementExport.md)
<span data-ttu-id="52d04-114">내보내기 만들기 또는 업데이트 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="52d04-114">The operation to create or update a export.</span></span>
<span data-ttu-id="52d04-115">업데이트 작업을 수행하려면 요청에서 최신 eTag를 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="52d04-115">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="52d04-116">get 작업을 수행하여 최신 eTag를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="52d04-116">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="52d04-117">만들기 작업에는 eTag가 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="52d04-117">Create operation does not require eTag.</span></span>

### [<span data-ttu-id="52d04-118">New-AzCostManagementQueryComparisonExpressionObject</span><span class="sxs-lookup"><span data-stu-id="52d04-118">New-AzCostManagementQueryComparisonExpressionObject</span></span>](New-AzCostManagementQueryComparisonExpressionObject.md)
<span data-ttu-id="52d04-119">QueryComparisonExpression에 대한 메모리 내 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="52d04-119">Create a in-memory object for QueryComparisonExpression</span></span>

### [<span data-ttu-id="52d04-120">New-AzCostManagementQueryFilterObject</span><span class="sxs-lookup"><span data-stu-id="52d04-120">New-AzCostManagementQueryFilterObject</span></span>](New-AzCostManagementQueryFilterObject.md)
<span data-ttu-id="52d04-121">QueryFilter에 대한 메모리 내 개체 만들기</span><span class="sxs-lookup"><span data-stu-id="52d04-121">Create a in-memory object for QueryFilter</span></span>

### [<span data-ttu-id="52d04-122">Remove-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="52d04-122">Remove-AzCostManagementExport</span></span>](Remove-AzCostManagementExport.md)
<span data-ttu-id="52d04-123">내보내기 삭제 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="52d04-123">The operation to delete a export.</span></span>

### [<span data-ttu-id="52d04-124">Update-AzCostManagementExport</span><span class="sxs-lookup"><span data-stu-id="52d04-124">Update-AzCostManagementExport</span></span>](Update-AzCostManagementExport.md)
<span data-ttu-id="52d04-125">내보내기 만들기 또는 업데이트 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="52d04-125">The operation to create or update a export.</span></span>
<span data-ttu-id="52d04-126">업데이트 작업을 수행하려면 요청에서 최신 eTag를 설정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="52d04-126">Update operation requires latest eTag to be set in the request.</span></span>
<span data-ttu-id="52d04-127">get 작업을 수행하여 최신 eTag를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="52d04-127">You may obtain the latest eTag by performing a get operation.</span></span>
<span data-ttu-id="52d04-128">만들기 작업에는 eTag가 필요하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="52d04-128">Create operation does not require eTag.</span></span>

