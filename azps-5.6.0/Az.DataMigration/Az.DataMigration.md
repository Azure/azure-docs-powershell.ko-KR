---
Module Name: Az.DataMigration
Module Guid: 150d9544-6348-4373-806f-10cd0b4de4cb
Download Help Link: https://docs.microsoft.com/powershell/module/az.datamigration
Help Version: 0.1.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Az.DataMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Az.DataMigration.md
ms.openlocfilehash: c73e82285a848c9ff6abf197eb3352cf708a2f4b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958752"
---
# <span data-ttu-id="b6b27-101">Az.DataMigration 모듈</span><span class="sxs-lookup"><span data-stu-id="b6b27-101">Az.DataMigration Module</span></span>
## <span data-ttu-id="b6b27-102">설명</span><span class="sxs-lookup"><span data-stu-id="b6b27-102">Description</span></span>
<span data-ttu-id="b6b27-103">{{Azure DataMigration Service Module}}</span><span class="sxs-lookup"><span data-stu-id="b6b27-103">{{Azure DataMigration Service Module}}</span></span>

## <span data-ttu-id="b6b27-104">Az.DataMigration Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b6b27-104">Az.DataMigration Cmdlets</span></span>
### [<span data-ttu-id="b6b27-105">Get-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="b6b27-105">Get-AzDataMigrationProject</span></span>](Get-AzDataMigrationProject.md)
<span data-ttu-id="b6b27-106">Azure Database Migration 프로젝트의 속성을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="b6b27-106">Retrieves the properties of an Azure Database Migration project.</span></span>

### [<span data-ttu-id="b6b27-107">Get-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="b6b27-107">Get-AzDataMigrationService</span></span>](Get-AzDataMigrationService.md)
<span data-ttu-id="b6b27-108">Azure Database Migration Service의 인스턴스와 연결된 속성을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="b6b27-108">Retrieves the properties associated with an instance of the Azure Database Migration Service.</span></span> 

### [<span data-ttu-id="b6b27-109">Get-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="b6b27-109">Get-AzDataMigrationTask</span></span>](Get-AzDataMigrationTask.md)
<span data-ttu-id="b6b27-110">Azure Database Migration Service 마이그레이션 작업과 연결된 PSProjectTask 개체를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="b6b27-110">Retrieves the PSProjectTask object associated with an Azure Database Migration Service migration task.</span></span>

### [<span data-ttu-id="b6b27-111">Invoke-AzDataMigrationCommand</span><span class="sxs-lookup"><span data-stu-id="b6b27-111">Invoke-AzDataMigrationCommand</span></span>](Invoke-AzDataMigrationCommand.md)
<span data-ttu-id="b6b27-112">기존 DMS 태스크에서 실행할 새 명령을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b6b27-112">Creates a new command to be executed on an existing DMS task.</span></span>

### [<span data-ttu-id="b6b27-113">New-AzDataMigrationConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="b6b27-113">New-AzDataMigrationConnectionInfo</span></span>](New-AzDataMigrationConnectionInfo.md)
<span data-ttu-id="b6b27-114">연결에 대한 서버 유형 및 이름을 지정하는 새 연결 정보 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b6b27-114">Creates a new Connection Info object specifying the server type and name for connection.</span></span>

### [<span data-ttu-id="b6b27-115">New-AzDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="b6b27-115">New-AzDataMigrationDatabaseInfo</span></span>](New-AzDataMigrationDatabaseInfo.md)
<span data-ttu-id="b6b27-116">마이그레이션을 위한 데이터베이스 원본을 지정하는 Azure Database Migration Service에 대한 DatabaseInfo 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b6b27-116">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

### [<span data-ttu-id="b6b27-117">New-AzDataMigrationFileShare</span><span class="sxs-lookup"><span data-stu-id="b6b27-117">New-AzDataMigrationFileShare</span></span>](New-AzDataMigrationFileShare.md)
<span data-ttu-id="b6b27-118">원본 데이터베이스 백업을 수행하기 위해 로컬 네트워크 공유를 지정하는 Azure Database Migration Service에 대한 FileShare 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b6b27-118">Creates the FileShare object for the Azure Database Migration Service, which specifies the local network share to take the source database backups to.</span></span>

### [<span data-ttu-id="b6b27-119">New-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="b6b27-119">New-AzDataMigrationProject</span></span>](New-AzDataMigrationProject.md)
<span data-ttu-id="b6b27-120">새 Azure Database Migration Service 프로젝트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b6b27-120">Creates a new Azure Database Migration Service project.</span></span>

### [<span data-ttu-id="b6b27-121">New-AzDataMigrationSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="b6b27-121">New-AzDataMigrationSelectedDBObject</span></span>](New-AzDataMigrationSelectedDBObject.md)
<span data-ttu-id="b6b27-122">마이그레이션을 위한 원본 및 대상 데이터베이스에 대한 정보가 포함된 데이터베이스 입력 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b6b27-122">Creates a database input object that contains information about source and target databases for migration.</span></span>

### [<span data-ttu-id="b6b27-123">New-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="b6b27-123">New-AzDataMigrationService</span></span>](New-AzDataMigrationService.md)
<span data-ttu-id="b6b27-124">Azure Database Migration Service의 새 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b6b27-124">Creates a new instance of the Azure Database Migration Service.</span></span>

### [<span data-ttu-id="b6b27-125">New-AzDataMigrationSyncSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="b6b27-125">New-AzDataMigrationSyncSelectedDBObject</span></span>](New-AzDataMigrationSyncSelectedDBObject.md)
<span data-ttu-id="b6b27-126">마이그레이션 작업에 사용할 동기화 시나리오에 특정 데이터베이스 정보 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b6b27-126">Creates a database info object specific to the sync scenario to be used for a migration task.</span></span>

### [<span data-ttu-id="b6b27-127">New-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="b6b27-127">New-AzDataMigrationTask</span></span>](New-AzDataMigrationTask.md)
<span data-ttu-id="b6b27-128">Azure Database Migration Service에서 데이터 마이그레이션 작업을 만들고 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="b6b27-128">Creates and starts a data migration task in the Azure Database Migration Service.</span></span>

### [<span data-ttu-id="b6b27-129">Remove-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="b6b27-129">Remove-AzDataMigrationProject</span></span>](Remove-AzDataMigrationProject.md)
<span data-ttu-id="b6b27-130">Azure에서 Azure Database Migration Service 프로젝트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b6b27-130">Removes an Azure Database Migration Service project from Azure.</span></span>

### [<span data-ttu-id="b6b27-131">Remove-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="b6b27-131">Remove-AzDataMigrationService</span></span>](Remove-AzDataMigrationService.md)
<span data-ttu-id="b6b27-132">Azure에서 Azure Database Migration Service의 인스턴스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b6b27-132">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

### [<span data-ttu-id="b6b27-133">Remove-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="b6b27-133">Remove-AzDataMigrationTask</span></span>](Remove-AzDataMigrationTask.md)
<span data-ttu-id="b6b27-134">Azure에서 Azure Database Migration Service 작업을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b6b27-134">Removes an Azure Database Migration Service task from Azure.</span></span>

### [<span data-ttu-id="b6b27-135">Start-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="b6b27-135">Start-AzDataMigrationService</span></span>](Start-AzDataMigrationService.md)
<span data-ttu-id="b6b27-136">중지된 상태로 Azure Database Migration Service의 인스턴스를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="b6b27-136">Starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

### [<span data-ttu-id="b6b27-137">Stop-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="b6b27-137">Stop-AzDataMigrationService</span></span>](Stop-AzDataMigrationService.md)
<span data-ttu-id="b6b27-138">실행 중인 상태인 Azure Database Migration Service의 인스턴스를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="b6b27-138">Stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

### [<span data-ttu-id="b6b27-139">Stop-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="b6b27-139">Stop-AzDataMigrationTask</span></span>](Stop-AzDataMigrationTask.md)
<span data-ttu-id="b6b27-140">실행 중인 상태인 Azure Database Migration Service 작업을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="b6b27-140">Stops an  Azure Database Migration Service task that is in a running state.</span></span>

