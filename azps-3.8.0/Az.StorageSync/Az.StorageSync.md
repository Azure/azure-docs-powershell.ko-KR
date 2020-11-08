---
Module Name: Az.StorageSync
Module Guid: 001b4bbc-9d7d-43b2-9e95-7a70325e9509
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.storagesync
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Az.StorageSync.md
ms.openlocfilehash: 3bfdc9c488f02794e82388741e7103417878c9f6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042451"
---
# <span data-ttu-id="20454-101">Az StorageSync 모듈</span><span class="sxs-lookup"><span data-stu-id="20454-101">Az.StorageSync Module</span></span>
## <span data-ttu-id="20454-102">설명은</span><span class="sxs-lookup"><span data-stu-id="20454-102">Description</span></span>
<span data-ttu-id="20454-103">저장소 동기화 모듈의 cmdlet을 사용 하면 PowerShell의 Azure 파일 동기화와 관련 된 작업을 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="20454-103">The cmdlets in the Storage Sync module enable you to manage operations pertaining to Azure File Sync in PowerShell.</span></span>

## <span data-ttu-id="20454-104">Az StorageSync Cmdlet</span><span class="sxs-lookup"><span data-stu-id="20454-104">Az.StorageSync Cmdlets</span></span>
### [<span data-ttu-id="20454-105">Get-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="20454-105">Get-AzStorageSyncCloudEndpoint</span></span>](Get-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="20454-106">이 명령은 지정 된 동기화 그룹 내의 모든 클라우드 끝점을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="20454-106">This command lists all cloud endpoints within a given sync group.</span></span>

### [<span data-ttu-id="20454-107">Get-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="20454-107">Get-AzStorageSyncGroup</span></span>](Get-AzStorageSyncGroup.md)
<span data-ttu-id="20454-108">이 명령은 지정 된 저장소 동기화 서비스 내의 모든 동기화 그룹을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="20454-108">This command lists all sync groups within a given storage sync service.</span></span>

### [<span data-ttu-id="20454-109">Get-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="20454-109">Get-AzStorageSyncServer</span></span>](Get-AzStorageSyncServer.md)
<span data-ttu-id="20454-110">이 명령은 지정 된 저장소 동기화 서비스에 등록 된 모든 서버를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="20454-110">This command lists all servers registered to a given storage sync service.</span></span>

### [<span data-ttu-id="20454-111">Get-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="20454-111">Get-AzStorageSyncServerEndpoint</span></span>](Get-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="20454-112">이 명령은 지정 된 동기화 그룹 내의 모든 서버 끝점을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="20454-112">This command lists all server endpoints within a given sync group.</span></span>

### [<span data-ttu-id="20454-113">Get-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="20454-113">Get-AzStorageSyncService</span></span>](Get-AzStorageSyncService.md)
<span data-ttu-id="20454-114">이 명령은 구독/리소스 그룹의 지정 된 범위 내에 있는 모든 저장소 동기화 서비스를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="20454-114">This command lists all storage sync services within a given scope of subscription/resource group.</span></span>

### [<span data-ttu-id="20454-115">AzStorageSyncChangeDetection-호출</span><span class="sxs-lookup"><span data-stu-id="20454-115">Invoke-AzStorageSyncChangeDetection</span></span>](Invoke-AzStorageSyncChangeDetection.md)
<span data-ttu-id="20454-116">이 명령을 사용 하 여 네임 스페이스 변경 감지를 수동으로 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="20454-116">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="20454-117">전체 공유, 하위 폴더 또는 파일 집합을 대상으로 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="20454-117">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="20454-118">최대 1만 개의 변경 내용을 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="20454-118">A maximum of 10,000 changes can be detected.</span></span> <span data-ttu-id="20454-119">변경의 범위가 사용자에 게 알려진 경우이 명령의 실행을 네임 스페이스의 부분으로 제한 하 여 변경 내용이 1만 변경 제한 내에서 신속 하 게 완료 될 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="20454-119">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within a 10,000 changes limit.</span></span>

### [<span data-ttu-id="20454-120">AzStorageSyncCompatibilityCheck-호출</span><span class="sxs-lookup"><span data-stu-id="20454-120">Invoke-AzStorageSyncCompatibilityCheck</span></span>](Invoke-AzStorageSyncCompatibilityCheck.md)
<span data-ttu-id="20454-121">시스템 및 Azure 파일 동기화 간에 발생할 수 있는 호환성 문제가 있는지 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="20454-121">Checks for potential compatibility issues between your system and Azure File Sync.</span></span>

### [<span data-ttu-id="20454-122">AzStorageSyncFileRecall-호출</span><span class="sxs-lookup"><span data-stu-id="20454-122">Invoke-AzStorageSyncFileRecall</span></span>](Invoke-AzStorageSyncFileRecall.md)
<span data-ttu-id="20454-123">이 명령은 모든 계층화 파일을 다시 로컬 디스크로 회수 합니다.</span><span class="sxs-lookup"><span data-stu-id="20454-123">This command recalls all tiered files back to local disk.</span></span>

### [<span data-ttu-id="20454-124">새로운 AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="20454-124">New-AzStorageSyncCloudEndpoint</span></span>](New-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="20454-125">이 명령은 동기화 그룹에 Azure 파일 동기화 클라우드 끝점을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="20454-125">This command creates an Azure File Sync cloud endpoint in a sync group.</span></span>

### [<span data-ttu-id="20454-126">새로운 AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="20454-126">New-AzStorageSyncGroup</span></span>](New-AzStorageSyncGroup.md)
<span data-ttu-id="20454-127">이 명령은 지정 된 저장소 동기화 서비스 내에 새 동기화 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="20454-127">This command creates a new sync group within a specified storage sync service.</span></span>

### [<span data-ttu-id="20454-128">새로운 AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="20454-128">New-AzStorageSyncServerEndpoint</span></span>](New-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="20454-129">이 명령은 등록 된 서버에서 새 서버 끝점을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="20454-129">This command creates a new server endpoint on a registered server.</span></span> <span data-ttu-id="20454-130">이렇게 하면 서버의 지정 된 경로가 동기화 그룹의 다른 끝점과 파일 동기화를 시작할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="20454-130">This enables the specified path on the server to start syncing the files with other endpoints in the sync group.</span></span>

### [<span data-ttu-id="20454-131">새로운 AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="20454-131">New-AzStorageSyncService</span></span>](New-AzStorageSyncService.md)
<span data-ttu-id="20454-132">이 명령은 리소스 그룹에 새 저장소 동기화 서비스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="20454-132">This command creates a new storage sync service in a resource group.</span></span>

### [<span data-ttu-id="20454-133">Register-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="20454-133">Register-AzStorageSyncServer</span></span>](Register-AzStorageSyncServer.md)
<span data-ttu-id="20454-134">이 명령은 신뢰 관계를 만드는 저장소 동기화 서비스에 서버를 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="20454-134">This command registers a server to a storage sync service which creates a trust relationship.</span></span> <span data-ttu-id="20454-135">그러면 PowerShell 또는 Azure 포털을 사용 하 여이 서버에서 동기화를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="20454-135">PowerShell or the Azure portal can then be used to configure sync on this server.</span></span>

### [<span data-ttu-id="20454-136">제거-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="20454-136">Remove-AzStorageSyncCloudEndpoint</span></span>](Remove-AzStorageSyncCloudEndpoint.md)
<span data-ttu-id="20454-137">이 명령은 동기화 그룹에서 지정 된 클라우드 끝점을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="20454-137">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="20454-138">하나 이상의 클라우드 끝점이 없으면이 동기화 그룹의 다른 서버 끝점을 동기화 할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="20454-138">Without at least one cloud endpoint, no other server endpoints in this sync group can sync.</span></span>

### [<span data-ttu-id="20454-139">제거-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="20454-139">Remove-AzStorageSyncGroup</span></span>](Remove-AzStorageSyncGroup.md)
<span data-ttu-id="20454-140">이 명령은 지정 된 동기화 그룹을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="20454-140">This command will delete the specified sync group.</span></span>

### [<span data-ttu-id="20454-141">제거-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="20454-141">Remove-AzStorageSyncServerEndpoint</span></span>](Remove-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="20454-142">이 명령은 지정 된 서버 종점을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="20454-142">This command will delete the specified server endpoint.</span></span> <span data-ttu-id="20454-143">이 위치와 동기화가 즉시 중지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="20454-143">Sync to this location will stop immediately.</span></span>

### [<span data-ttu-id="20454-144">제거-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="20454-144">Remove-AzStorageSyncService</span></span>](Remove-AzStorageSyncService.md)
<span data-ttu-id="20454-145">이 명령은 지정 된 저장소 동기화 서비스를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="20454-145">This command will delete the specified storage sync service.</span></span>

### [<span data-ttu-id="20454-146">다시 설정-AzStorageSyncServerCertificate</span><span class="sxs-lookup"><span data-stu-id="20454-146">Reset-AzStorageSyncServerCertificate</span></span>](Reset-AzStorageSyncServerCertificate.md)
<span data-ttu-id="20454-147">문제 해결에만 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="20454-147">Use for troubleshooting only.</span></span> <span data-ttu-id="20454-148">이 명령은 저장소 동기화 서비스에 대 한 서버 id를 설명 하는 데 사용 되는 저장소 동기화 서버 인증서를 롤백합니다.</span><span class="sxs-lookup"><span data-stu-id="20454-148">This command will roll the storage sync server certificate used to describe the server identity to the storage sync service.</span></span>

### [<span data-ttu-id="20454-149">Set-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="20454-149">Set-AzStorageSyncServerEndpoint</span></span>](Set-AzStorageSyncServerEndpoint.md)
<span data-ttu-id="20454-150">이 명령을 사용 하 여 서버 끝점의 조정 가능한 매개 변수를 변경할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="20454-150">This command allows for changes on the adjustable parameters of a server endpoint.</span></span>

### [<span data-ttu-id="20454-151">등록 취소-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="20454-151">Unregister-AzStorageSyncServer</span></span>](Unregister-AzStorageSyncServer.md)
<span data-ttu-id="20454-152">경고: 서버의 등록을 취소 하면이 서버의 모든 서버 끝점에 대 한 연계 삭제가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="20454-152">Warning: Unregistering a server will result in cascading deletes of all server endpoints on this server.</span></span> <span data-ttu-id="20454-153">이 명령은 저장소 동기화 서비스에서 서버의 등록을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="20454-153">This command will unregister a server from it's storage sync service.</span></span>

