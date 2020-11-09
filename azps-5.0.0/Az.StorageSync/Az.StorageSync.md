---
Module Name: Az.StorageSync
Module Guid: 001b4bbc-9d7d-43b2-9e95-7a70325e9509
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.storagesync
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
ms.openlocfilehash: bc3704c3594826f19399c1967bbe86ed7f1e8773
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310553"
---
# <span data-ttu-id="377d3-101">Az StorageSync 모듈</span><span class="sxs-lookup"><span data-stu-id="377d3-101">Az.StorageSync Module</span></span>
## <span data-ttu-id="377d3-102">설명은</span><span class="sxs-lookup"><span data-stu-id="377d3-102">Description</span></span>
<span data-ttu-id="377d3-103">저장소 동기화 모듈의 cmdlet을 사용 하면 PowerShell의 Azure 파일 동기화와 관련 된 작업을 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="377d3-103">The cmdlets in the Storage Sync module enable you to manage operations pertaining to Azure File Sync in PowerShell.</span></span>

## <span data-ttu-id="377d3-104">Az StorageSync Cmdlet</span><span class="sxs-lookup"><span data-stu-id="377d3-104">Az.StorageSync Cmdlets</span></span>
### [<span data-ttu-id="377d3-105">Get-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="377d3-105">Get-AzStorageSyncCloudEndpoint</span></span>](Get-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="377d3-106">이 명령은 지정 된 동기화 그룹 내의 모든 클라우드 끝점을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="377d3-106">This command lists all cloud endpoints within a given sync group.</span></span>

### [<span data-ttu-id="377d3-107">Get-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="377d3-107">Get-AzStorageSyncGroup</span></span>](Get-AzStorageSyncGroup.md)
<span data-ttu-id="377d3-108">이 명령은 지정 된 저장소 동기화 서비스 내의 모든 동기화 그룹을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="377d3-108">This command lists all sync groups within a given storage sync service.</span></span>

### [<span data-ttu-id="377d3-109">Get-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="377d3-109">Get-AzStorageSyncServer</span></span>](Get-AzStorageSyncServer.md)
<span data-ttu-id="377d3-110">이 명령은 지정 된 저장소 동기화 서비스에 등록 된 모든 서버를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="377d3-110">This command lists all servers registered to a given storage sync service.</span></span>

### [<span data-ttu-id="377d3-111">Get-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="377d3-111">Get-AzStorageSyncServerEndpoint</span></span>](Get-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="377d3-112">이 명령은 지정 된 동기화 그룹 내의 모든 서버 끝점을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="377d3-112">This command lists all server endpoints within a given sync group.</span></span>

### [<span data-ttu-id="377d3-113">Get-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="377d3-113">Get-AzStorageSyncService</span></span>](Get-AzStorageSyncService.md)
<span data-ttu-id="377d3-114">이 명령은 구독/리소스 그룹의 지정 된 범위 내에 있는 모든 저장소 동기화 서비스를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="377d3-114">This command lists all storage sync services within a given scope of subscription/resource group.</span></span>

### [<span data-ttu-id="377d3-115">AzStorageSyncChangeDetection-호출</span><span class="sxs-lookup"><span data-stu-id="377d3-115">Invoke-AzStorageSyncChangeDetection</span></span>](Invoke-AzStorageSyncChangeDetection.md)
<span data-ttu-id="377d3-116">이 명령을 사용 하 여 네임 스페이스 변경 감지를 수동으로 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="377d3-116">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="377d3-117">전체 공유, 하위 폴더 또는 파일 집합을 대상으로 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="377d3-117">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="377d3-118">최대 1만 개의 변경 내용을 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="377d3-118">A maximum of 10,000 changes can be detected.</span></span> <span data-ttu-id="377d3-119">변경의 범위가 사용자에 게 알려진 경우이 명령의 실행을 네임 스페이스의 부분으로 제한 하 여 변경 내용이 1만 변경 제한 내에서 신속 하 게 완료 될 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="377d3-119">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within a 10,000 changes limit.</span></span>

### [<span data-ttu-id="377d3-120">AzStorageSyncCompatibilityCheck-호출</span><span class="sxs-lookup"><span data-stu-id="377d3-120">Invoke-AzStorageSyncCompatibilityCheck</span></span>](Invoke-AzStorageSyncCompatibilityCheck.md)
<span data-ttu-id="377d3-121">시스템 및 Azure 파일 동기화 간에 발생할 수 있는 호환성 문제가 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="377d3-121">Checks for potential compatibility issues between your system and Azure File Sync.</span></span>

### [<span data-ttu-id="377d3-122">AzStorageSyncFileRecall-호출</span><span class="sxs-lookup"><span data-stu-id="377d3-122">Invoke-AzStorageSyncFileRecall</span></span>](Invoke-AzStorageSyncFileRecall.md)
<span data-ttu-id="377d3-123">이 명령은 모든 계층화 파일을 다시 로컬 디스크로 회수 합니다.</span><span class="sxs-lookup"><span data-stu-id="377d3-123">This command recalls all tiered files back to local disk.</span></span>

### [<span data-ttu-id="377d3-124">새로운 AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="377d3-124">New-AzStorageSyncCloudEndpoint</span></span>](New-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="377d3-125">이 명령은 동기화 그룹에 Azure 파일 동기화 클라우드 끝점을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="377d3-125">This command creates an Azure File Sync cloud endpoint in a sync group.</span></span>

### [<span data-ttu-id="377d3-126">새로운 AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="377d3-126">New-AzStorageSyncGroup</span></span>](New-AzStorageSyncGroup.md)
<span data-ttu-id="377d3-127">이 명령은 지정 된 저장소 동기화 서비스 내에 새 동기화 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="377d3-127">This command creates a new sync group within a specified storage sync service.</span></span>

### [<span data-ttu-id="377d3-128">새로운 AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="377d3-128">New-AzStorageSyncServerEndpoint</span></span>](New-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="377d3-129">이 명령은 등록 된 서버에서 새 서버 끝점을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="377d3-129">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="377d3-130">이렇게 하면 서버의 지정 된 경로가 동기화 그룹의 다른 끝점과 파일 동기화를 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="377d3-130">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span>

### [<span data-ttu-id="377d3-131">새로운 AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="377d3-131">New-AzStorageSyncService</span></span>](New-AzStorageSyncService.md)
<span data-ttu-id="377d3-132">이 명령은 리소스 그룹에 새 저장소 동기화 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="377d3-132">This command creates a new storage sync service in a resource group.</span></span>

### [<span data-ttu-id="377d3-133">Set-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="377d3-133">Set-AzStorageSyncService</span></span>](New-AzStorageSyncService.md)
<span data-ttu-id="377d3-134">이 명령은 리소스 그룹에 저장소 동기화 서비스를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="377d3-134">This command sets a storage sync service in a resource group.</span></span>

### [<span data-ttu-id="377d3-135">Register-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="377d3-135">Register-AzStorageSyncServer</span></span>](Register-AzStorageSyncServer.md)
<span data-ttu-id="377d3-136">이 명령은 신뢰 관계를 만드는 저장소 동기화 서비스에 서버를 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="377d3-136">This command registers a server to a storage sync service which creates a trust relationship.</span></span> <span data-ttu-id="377d3-137">그러면 PowerShell 또는 Azure 포털을 사용 하 여이 서버에서 동기화를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="377d3-137">PowerShell or the Azure portal can then be used to configure sync on this server.</span></span>

### [<span data-ttu-id="377d3-138">제거-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="377d3-138">Remove-AzStorageSyncCloudEndpoint</span></span>](Remove-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="377d3-139">이 명령은 동기화 그룹에서 지정 된 클라우드 끝점을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="377d3-139">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="377d3-140">하나 이상의 클라우드 끝점이 없으면이 동기화 그룹의 다른 서버 끝점을 동기화 할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="377d3-140">Without at least one cloud endpoint, no other server endpoints in this sync group can sync.</span></span>

### [<span data-ttu-id="377d3-141">제거-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="377d3-141">Remove-AzStorageSyncGroup</span></span>](Remove-AzStorageSyncGroup.md)
<span data-ttu-id="377d3-142">이 명령은 지정 된 동기화 그룹을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="377d3-142">This command will delete the specified sync group.</span></span>

### [<span data-ttu-id="377d3-143">제거-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="377d3-143">Remove-AzStorageSyncServerEndpoint</span></span>](Remove-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="377d3-144">이 명령은 지정 된 서버 종점을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="377d3-144">This command will delete the specified server endpoint.</span></span> <span data-ttu-id="377d3-145">이 위치와 동기화가 즉시 중지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="377d3-145">Sync to this location will stop immediately.</span></span>

### [<span data-ttu-id="377d3-146">제거-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="377d3-146">Remove-AzStorageSyncService</span></span>](Remove-AzStorageSyncService.md)
<span data-ttu-id="377d3-147">이 명령은 지정 된 저장소 동기화 서비스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="377d3-147">This command will delete the specified storage sync service.</span></span>

### [<span data-ttu-id="377d3-148">다시 설정-AzStorageSyncServerCertificate</span><span class="sxs-lookup"><span data-stu-id="377d3-148">Reset-AzStorageSyncServerCertificate</span></span>](Reset-AzStorageSyncServerCertificate.md)
<span data-ttu-id="377d3-149">문제 해결에만 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="377d3-149">Use for troubleshooting only.</span></span> <span data-ttu-id="377d3-150">이 명령은 저장소 동기화 서비스에 대 한 서버 id를 설명 하는 데 사용 되는 저장소 동기화 서버 인증서를 롤백합니다.</span><span class="sxs-lookup"><span data-stu-id="377d3-150">This command will roll the storage sync server certificate used to describe the server identity to the storage sync service.</span></span>

### [<span data-ttu-id="377d3-151">Set-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="377d3-151">Set-AzStorageSyncServerEndpoint</span></span>](Set-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="377d3-152">이 명령을 사용 하 여 서버 끝점의 조정 가능한 매개 변수를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="377d3-152">This command allows for changes on the adjustable parameters of a server endpoint.</span></span>

### [<span data-ttu-id="377d3-153">등록 취소-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="377d3-153">Unregister-AzStorageSyncServer</span></span>](Unregister-AzStorageSyncServer.md)
<span data-ttu-id="377d3-154">경고: 서버의 등록을 취소 하면이 서버의 모든 서버 끝점에 대 한 연계 삭제가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="377d3-154">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="377d3-155">이 명령은 저장소 동기화 서비스에서 서버의 등록을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="377d3-155">This command will unregister a server from it's storage sync service.</span></span>

