---
Module Name: Az.StorageSync
Module Guid: 001b4bbc-9d7d-43b2-9e95-7a70325e9509
Download Help Link: https://docs.microsoft.com/powershell/module/az.storagesync
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
ms.openlocfilehash: 9acaa8a562ffe88631a587703a3300ac13f73224
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973179"
---
# <span data-ttu-id="0b1b7-101">Az.StorageSync 모듈</span><span class="sxs-lookup"><span data-stu-id="0b1b7-101">Az.StorageSync Module</span></span>
## <span data-ttu-id="0b1b7-102">설명</span><span class="sxs-lookup"><span data-stu-id="0b1b7-102">Description</span></span>
<span data-ttu-id="0b1b7-103">Storage 동기화 모듈의 cmdlet을 사용하면 PowerShell의 Azure 파일 동기화에 대한 작업을 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0b1b7-103">The cmdlets in the Storage Sync module enable you to manage operations pertaining to Azure File Sync in PowerShell.</span></span>

## <span data-ttu-id="0b1b7-104">Az.StorageSync Cmdlet</span><span class="sxs-lookup"><span data-stu-id="0b1b7-104">Az.StorageSync Cmdlets</span></span>
### [<span data-ttu-id="0b1b7-105">Get-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="0b1b7-105">Get-AzStorageSyncCloudEndpoint</span></span>](Get-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="0b1b7-106">이 명령은 주어진 동기화 그룹 내의 모든 클라우드 엔드포인트를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="0b1b7-106">This command lists all cloud endpoints within a given sync group.</span></span>

### [<span data-ttu-id="0b1b7-107">Get-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="0b1b7-107">Get-AzStorageSyncGroup</span></span>](Get-AzStorageSyncGroup.md)
<span data-ttu-id="0b1b7-108">이 명령은 주어진 저장소 동기화 서비스 내의 모든 동기화 그룹을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="0b1b7-108">This command lists all sync groups within a given storage sync service.</span></span>

### [<span data-ttu-id="0b1b7-109">Get-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="0b1b7-109">Get-AzStorageSyncServer</span></span>](Get-AzStorageSyncServer.md)
<span data-ttu-id="0b1b7-110">이 명령은 주어진 저장소 동기화 서비스에 등록된 모든 서버를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="0b1b7-110">This command lists all servers registered to a given storage sync service.</span></span>

### [<span data-ttu-id="0b1b7-111">Get-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0b1b7-111">Get-AzStorageSyncServerEndpoint</span></span>](Get-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="0b1b7-112">이 명령은 주어진 동기화 그룹 내의 모든 서버 엔드포인트를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="0b1b7-112">This command lists all server endpoints within a given sync group.</span></span>

### [<span data-ttu-id="0b1b7-113">Get-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="0b1b7-113">Get-AzStorageSyncService</span></span>](Get-AzStorageSyncService.md)
<span data-ttu-id="0b1b7-114">이 명령은 구독/리소스 그룹의 주어진 범위 내의 모든 저장소 동기화 서비스를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="0b1b7-114">This command lists all storage sync services within a given scope of subscription/resource group.</span></span>

### [<span data-ttu-id="0b1b7-115">Invoke-AzStorageSyncChangeDetection</span><span class="sxs-lookup"><span data-stu-id="0b1b7-115">Invoke-AzStorageSyncChangeDetection</span></span>](Invoke-AzStorageSyncChangeDetection.md)
<span data-ttu-id="0b1b7-116">이 명령을 사용하여 네임스페이스 변경 내용 검색을 수동으로 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0b1b7-116">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="0b1b7-117">전체 공유, 하위 폴더 또는 파일 집합을 대상으로 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0b1b7-117">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="0b1b7-118">최대 10,000개 변경 내용을 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0b1b7-118">A maximum of 10,000 changes can be detected.</span></span> <span data-ttu-id="0b1b7-119">변경 범위를 알 수 있는 경우 이 명령의 실행을 네임스페이스의 일부로 제한하여 변경 검색이 10,000개 변경 한도 내에서 빠르게 완료될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0b1b7-119">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within a 10,000 changes limit.</span></span>

### [<span data-ttu-id="0b1b7-120">Invoke-AzStorageSyncCompatibilityCheck</span><span class="sxs-lookup"><span data-stu-id="0b1b7-120">Invoke-AzStorageSyncCompatibilityCheck</span></span>](Invoke-AzStorageSyncCompatibilityCheck.md)
<span data-ttu-id="0b1b7-121">시스템과 Azure 파일 동기화 간에 잠재적인 호환성 문제가 확인됩니다.</span><span class="sxs-lookup"><span data-stu-id="0b1b7-121">Checks for potential compatibility issues between your system and Azure File Sync.</span></span>

### [<span data-ttu-id="0b1b7-122">Invoke-AzStorageSyncFileRecall</span><span class="sxs-lookup"><span data-stu-id="0b1b7-122">Invoke-AzStorageSyncFileRecall</span></span>](Invoke-AzStorageSyncFileRecall.md)
<span data-ttu-id="0b1b7-123">이 명령은 계층화된 모든 파일을 로컬 디스크로 다시 회수합니다.</span><span class="sxs-lookup"><span data-stu-id="0b1b7-123">This command recalls all tiered files back to local disk.</span></span>

### [<span data-ttu-id="0b1b7-124">New-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="0b1b7-124">New-AzStorageSyncCloudEndpoint</span></span>](New-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="0b1b7-125">이 명령은 동기화 그룹에 Azure 파일 동기화 클라우드 엔드포인트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0b1b7-125">This command creates an Azure File Sync cloud endpoint in a sync group.</span></span>

### [<span data-ttu-id="0b1b7-126">New-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="0b1b7-126">New-AzStorageSyncGroup</span></span>](New-AzStorageSyncGroup.md)
<span data-ttu-id="0b1b7-127">이 명령은 지정된 저장소 동기화 서비스 내에서 새 동기화 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0b1b7-127">This command creates a new sync group within a specified storage sync service.</span></span>

### [<span data-ttu-id="0b1b7-128">New-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0b1b7-128">New-AzStorageSyncServerEndpoint</span></span>](New-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="0b1b7-129">이 명령은 등록된 서버에 새 서버 엔드포인트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0b1b7-129">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="0b1b7-130">이렇게 하면 서버의 지정된 경로가 동기화 그룹의 다른 엔드포인트와 파일을 동기화하기 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0b1b7-130">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span>

### [<span data-ttu-id="0b1b7-131">New-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="0b1b7-131">New-AzStorageSyncService</span></span>](New-AzStorageSyncService.md)
<span data-ttu-id="0b1b7-132">이 명령은 리소스 그룹에 새 저장소 동기화 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0b1b7-132">This command creates a new storage sync service in a resource group.</span></span>

### [<span data-ttu-id="0b1b7-133">Set-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="0b1b7-133">Set-AzStorageSyncService</span></span>](New-AzStorageSyncService.md)
<span data-ttu-id="0b1b7-134">이 명령은 리소스 그룹에 저장소 동기화 서비스를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="0b1b7-134">This command sets a storage sync service in a resource group.</span></span>

### [<span data-ttu-id="0b1b7-135">Register-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="0b1b7-135">Register-AzStorageSyncServer</span></span>](Register-AzStorageSyncServer.md)
<span data-ttu-id="0b1b7-136">이 명령은 신뢰 관계를 만드는 저장소 동기화 서비스에 서버를 등록합니다.</span><span class="sxs-lookup"><span data-stu-id="0b1b7-136">This command registers a server to a storage sync service which creates a trust relationship.</span></span> <span data-ttu-id="0b1b7-137">그런 다음 PowerShell 또는 Azure Portal을 사용하여 이 서버에서 동기화를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0b1b7-137">PowerShell or the Azure portal can then be used to configure sync on this server.</span></span>

### [<span data-ttu-id="0b1b7-138">Remove-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="0b1b7-138">Remove-AzStorageSyncCloudEndpoint</span></span>](Remove-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="0b1b7-139">이 명령은 동기화 그룹에서 지정된 클라우드 엔드포인트를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="0b1b7-139">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="0b1b7-140">하나 이상의 클라우드 엔드포인트가 없는 경우 이 동기화 그룹의 다른 서버 엔드포인트는 동기화할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="0b1b7-140">Without at least one cloud endpoint, no other server endpoints in this sync group can sync.</span></span>

### [<span data-ttu-id="0b1b7-141">Remove-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="0b1b7-141">Remove-AzStorageSyncGroup</span></span>](Remove-AzStorageSyncGroup.md)
<span data-ttu-id="0b1b7-142">이 명령은 지정된 동기화 그룹을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="0b1b7-142">This command will delete the specified sync group.</span></span>

### [<span data-ttu-id="0b1b7-143">Remove-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0b1b7-143">Remove-AzStorageSyncServerEndpoint</span></span>](Remove-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="0b1b7-144">이 명령은 지정된 서버 엔드포인트를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="0b1b7-144">This command will delete the specified server endpoint.</span></span> <span data-ttu-id="0b1b7-145">이 위치에 동기화하면 즉시 중지됩니다.</span><span class="sxs-lookup"><span data-stu-id="0b1b7-145">Sync to this location will stop immediately.</span></span>

### [<span data-ttu-id="0b1b7-146">Remove-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="0b1b7-146">Remove-AzStorageSyncService</span></span>](Remove-AzStorageSyncService.md)
<span data-ttu-id="0b1b7-147">이 명령은 지정된 저장소 동기화 서비스를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="0b1b7-147">This command will delete the specified storage sync service.</span></span>

### [<span data-ttu-id="0b1b7-148">Reset-AzStorageSyncServerCertificate</span><span class="sxs-lookup"><span data-stu-id="0b1b7-148">Reset-AzStorageSyncServerCertificate</span></span>](Reset-AzStorageSyncServerCertificate.md)
<span data-ttu-id="0b1b7-149">문제 해결에만 사용.</span><span class="sxs-lookup"><span data-stu-id="0b1b7-149">Use for troubleshooting only.</span></span> <span data-ttu-id="0b1b7-150">이 명령은 저장소 동기화 서비스에 서버 ID를 설명하는 데 사용되는 저장소 동기화 서버 인증서를 롤링합니다.</span><span class="sxs-lookup"><span data-stu-id="0b1b7-150">This command will roll the storage sync server certificate used to describe the server identity to the storage sync service.</span></span>

### [<span data-ttu-id="0b1b7-151">Set-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0b1b7-151">Set-AzStorageSyncServerEndpoint</span></span>](Set-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="0b1b7-152">이 명령을 사용하면 서버 엔드포인트의 조정 가능한 매개 변수를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0b1b7-152">This command allows for changes on the adjustable parameters of a server endpoint.</span></span>

### [<span data-ttu-id="0b1b7-153">Unregister-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="0b1b7-153">Unregister-AzStorageSyncServer</span></span>](Unregister-AzStorageSyncServer.md)
<span data-ttu-id="0b1b7-154">경고: 서버를 등록하지 않은 경우 이 서버의 모든 서버 엔드포인트가 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="0b1b7-154">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="0b1b7-155">이 명령은 저장소 동기화 서비스에서 서버를 등록을 등록하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0b1b7-155">This command will unregister a server from it's storage sync service.</span></span>

