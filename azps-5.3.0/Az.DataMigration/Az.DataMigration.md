---
Module Name: Az.DataMigration
Module Guid: 150d9544-6348-4373-806f-10cd0b4de4cb
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.datamigration
Help Version: 0.1.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Az.DataMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/Az.DataMigration.md
ms.openlocfilehash: 6eb1ccb692f9f57e0d686a26a7c534459118cd19
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489043"
---
# <span data-ttu-id="2a68c-101">Az.DataMigration 모듈</span><span class="sxs-lookup"><span data-stu-id="2a68c-101">Az.DataMigration Module</span></span>
## <span data-ttu-id="2a68c-102">설명</span><span class="sxs-lookup"><span data-stu-id="2a68c-102">Description</span></span>
<span data-ttu-id="2a68c-103">{{Azure DataMigration Service Module}}</span><span class="sxs-lookup"><span data-stu-id="2a68c-103">{{Azure DataMigration Service Module}}</span></span>

## <span data-ttu-id="2a68c-104">Az.DataMigration Cmdlet</span><span class="sxs-lookup"><span data-stu-id="2a68c-104">Az.DataMigration Cmdlets</span></span>
### [<span data-ttu-id="2a68c-105">Get-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="2a68c-105">Get-AzDataMigrationProject</span></span>](Get-AzDataMigrationProject.md)
<span data-ttu-id="2a68c-106">Azure Database Migration 프로젝트의 속성을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="2a68c-106">Retrieves the properties of an Azure Database Migration project.</span></span>

### [<span data-ttu-id="2a68c-107">Get-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="2a68c-107">Get-AzDataMigrationService</span></span>](Get-AzDataMigrationService.md)
<span data-ttu-id="2a68c-108">Azure Database Migration Service의 인스턴스와 연결된 속성을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="2a68c-108">Retrieves the properties associated with an instance of the Azure Database Migration Service.</span></span> 

### [<span data-ttu-id="2a68c-109">Get-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="2a68c-109">Get-AzDataMigrationTask</span></span>](Get-AzDataMigrationTask.md)
<span data-ttu-id="2a68c-110">Azure Database Migration Service 마이그레이션 작업과 연결된 PSProjectTask 개체를 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="2a68c-110">Retrieves the PSProjectTask object associated with an Azure Database Migration Service migration task.</span></span>

### [<span data-ttu-id="2a68c-111">Invoke-AzDataMigrationCommand</span><span class="sxs-lookup"><span data-stu-id="2a68c-111">Invoke-AzDataMigrationCommand</span></span>](Invoke-AzDataMigrationCommand.md)
<span data-ttu-id="2a68c-112">기존 DMS 작업에서 실행할 새 명령을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2a68c-112">Creates a new command to be executed on an existing DMS task.</span></span>

### [<span data-ttu-id="2a68c-113">New-AzDataMigrationConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="2a68c-113">New-AzDataMigrationConnectionInfo</span></span>](New-AzDataMigrationConnectionInfo.md)
<span data-ttu-id="2a68c-114">연결에 대한 서버 유형 및 이름을 지정하는 새 연결 정보 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2a68c-114">Creates a new Connection Info object specifying the server type and name for connection.</span></span>

### [<span data-ttu-id="2a68c-115">New-AzDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="2a68c-115">New-AzDataMigrationDatabaseInfo</span></span>](New-AzDataMigrationDatabaseInfo.md)
<span data-ttu-id="2a68c-116">마이그레이션을 위한 데이터베이스 원본을 지정하는 Azure Database Migration Service에 대한 DatabaseInfo 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2a68c-116">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

### [<span data-ttu-id="2a68c-117">New-AzDataMigrationFileShare</span><span class="sxs-lookup"><span data-stu-id="2a68c-117">New-AzDataMigrationFileShare</span></span>](New-AzDataMigrationFileShare.md)
<span data-ttu-id="2a68c-118">원본 데이터베이스 백업을 수행하기 위해 로컬 네트워크 공유를 지정하는 Azure Database Migration Service에 대한 FileShare 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2a68c-118">Creates the FileShare object for the Azure Database Migration Service, which specifies the local network share to take the source database backups to.</span></span>

### [<span data-ttu-id="2a68c-119">New-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="2a68c-119">New-AzDataMigrationProject</span></span>](New-AzDataMigrationProject.md)
<span data-ttu-id="2a68c-120">새 Azure Database Migration Service 프로젝트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2a68c-120">Creates a new Azure Database Migration Service project.</span></span>

### [<span data-ttu-id="2a68c-121">New-AzDataMigrationSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="2a68c-121">New-AzDataMigrationSelectedDBObject</span></span>](New-AzDataMigrationSelectedDBObject.md)
<span data-ttu-id="2a68c-122">마이그레이션을 위한 원본 및 대상 데이터베이스에 대한 정보를 포함하는 데이터베이스 입력 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2a68c-122">Creates a database input object that contains information about source and target databases for migration.</span></span>

### [<span data-ttu-id="2a68c-123">New-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="2a68c-123">New-AzDataMigrationService</span></span>](New-AzDataMigrationService.md)
<span data-ttu-id="2a68c-124">Azure Database Migration Service의 새 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2a68c-124">Creates a new instance of the Azure Database Migration Service.</span></span>

### [<span data-ttu-id="2a68c-125">New-AzDataMigrationSyncSelectedDBObject</span><span class="sxs-lookup"><span data-stu-id="2a68c-125">New-AzDataMigrationSyncSelectedDBObject</span></span>](New-AzDataMigrationSyncSelectedDBObject.md)
<span data-ttu-id="2a68c-126">마이그레이션 작업에 사용할 동기화 시나리오에 특정된 데이터베이스 정보 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2a68c-126">Creates a database info object specific to the sync scenario to be used for a migration task.</span></span>

### [<span data-ttu-id="2a68c-127">New-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="2a68c-127">New-AzDataMigrationTask</span></span>](New-AzDataMigrationTask.md)
<span data-ttu-id="2a68c-128">Azure Database Migration Service에서 데이터 마이그레이션 작업을 만들고 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="2a68c-128">Creates and starts a data migration task in the Azure Database Migration Service.</span></span>

### [<span data-ttu-id="2a68c-129">Remove-AzDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="2a68c-129">Remove-AzDataMigrationProject</span></span>](Remove-AzDataMigrationProject.md)
<span data-ttu-id="2a68c-130">Azure에서 Azure Database Migration Service 프로젝트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2a68c-130">Removes an Azure Database Migration Service project from Azure.</span></span>

### [<span data-ttu-id="2a68c-131">Remove-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="2a68c-131">Remove-AzDataMigrationService</span></span>](Remove-AzDataMigrationService.md)
<span data-ttu-id="2a68c-132">Azure에서 Azure Database Migration Service의 인스턴스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2a68c-132">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

### [<span data-ttu-id="2a68c-133">Remove-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="2a68c-133">Remove-AzDataMigrationTask</span></span>](Remove-AzDataMigrationTask.md)
<span data-ttu-id="2a68c-134">Azure에서 Azure Database Migration Service 작업을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="2a68c-134">Removes an Azure Database Migration Service task from Azure.</span></span>

### [<span data-ttu-id="2a68c-135">Start-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="2a68c-135">Start-AzDataMigrationService</span></span>](Start-AzDataMigrationService.md)
<span data-ttu-id="2a68c-136">중지된 상태로 Azure Database Migration Service의 인스턴스를 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="2a68c-136">Starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

### [<span data-ttu-id="2a68c-137">Stop-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="2a68c-137">Stop-AzDataMigrationService</span></span>](Stop-AzDataMigrationService.md)
<span data-ttu-id="2a68c-138">실행 중인 상태인 Azure Database Migration Service의 인스턴스를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="2a68c-138">Stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

### [<span data-ttu-id="2a68c-139">Stop-AzDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="2a68c-139">Stop-AzDataMigrationTask</span></span>](Stop-AzDataMigrationTask.md)
<span data-ttu-id="2a68c-140">실행 중인 상태인 Azure Database Migration Service 작업을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="2a68c-140">Stops an  Azure Database Migration Service task that is in a running state.</span></span>

