---
Module Name: AzureRM.DataMigration
Module Guid: 150d9544-6348-4373-806f-10cd0b4de4cb
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration
Help Version: 0.1.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/AzureRM.DataMigration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/AzureRM.DataMigration.md
ms.openlocfilehash: 1842bf625623e66d35adf32490a1d71315413c84
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/23/2019
ms.locfileid: "93522459"
---
# <span data-ttu-id="92d4a-101">DataMigration 모듈 AzureRM</span><span class="sxs-lookup"><span data-stu-id="92d4a-101">AzureRM.DataMigration Module</span></span>
## <span data-ttu-id="92d4a-102">설명은</span><span class="sxs-lookup"><span data-stu-id="92d4a-102">Description</span></span>
<span data-ttu-id="92d4a-103">{{Azure DataMigration Service Module}}</span><span class="sxs-lookup"><span data-stu-id="92d4a-103">{{Azure DataMigration Service Module}}</span></span>

## <span data-ttu-id="92d4a-104">DataMigration Cmdlet AzureRM</span><span class="sxs-lookup"><span data-stu-id="92d4a-104">AzureRM.DataMigration Cmdlets</span></span>
### [<span data-ttu-id="92d4a-105">Get-AzureRmDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="92d4a-105">Get-AzureRmDataMigrationProject</span></span>](Get-AzureRmDataMigrationProject.md)
<span data-ttu-id="92d4a-106">Azure 데이터베이스 마이그레이션 프로젝트의 속성을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="92d4a-106">Retrieves the properties of an Azure Database Migration project.</span></span>

### [<span data-ttu-id="92d4a-107">Get-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="92d4a-107">Get-AzureRmDataMigrationService</span></span>](Get-AzureRmDataMigrationService.md)
<span data-ttu-id="92d4a-108">Azure 데이터베이스 마이그레이션 서비스의 인스턴스와 연결 된 속성을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="92d4a-108">Retrieves the properties associated with an instance of the Azure Database Migration Service.</span></span> 

### [<span data-ttu-id="92d4a-109">Get-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="92d4a-109">Get-AzureRmDataMigrationTask</span></span>](Get-AzureRmDataMigrationTask.md)
<span data-ttu-id="92d4a-110">Azure 데이터베이스 마이그레이션 서비스 마이그레이션 작업과 연결 된 PSProjectTask 개체를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="92d4a-110">Retrieves the PSProjectTask object associated with an Azure Database Migration Service migration task.</span></span>

### <span data-ttu-id="92d4a-111">[New-AzureRmDataMigrationCommand (Get-AzureRmDataMigrationCommand.md)</span><span class="sxs-lookup"><span data-stu-id="92d4a-111">[New-AzureRmDataMigrationCommand(Get-AzureRmDataMigrationCommand.md)</span></span>
<span data-ttu-id="92d4a-112">기존 Azure 데이터베이스 마이그레이션 서비스 마이그레이션 작업에서 실행할 새 명령을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="92d4a-112">Creates a new command to be executed on an existing Azure Database Migration Service migration task.</span></span>

### [<span data-ttu-id="92d4a-113">새로운 AzureRmDataMigrationConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="92d4a-113">New-AzureRmDataMigrationConnectionInfo</span></span>](New-AzureRmDataMigrationConnectionInfo.md)
<span data-ttu-id="92d4a-114">연결에 대 한 서버 유형 및 이름을 지정 하는 새 연결 정보 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="92d4a-114">Creates a new Connection Info object specifying the server type and name for connection.</span></span>

### [<span data-ttu-id="92d4a-115">새로운 AzureRmDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="92d4a-115">New-AzureRmDataMigrationDatabaseInfo</span></span>](New-AzureRmDataMigrationDatabaseInfo.md)
<span data-ttu-id="92d4a-116">마이그레이션에 대 한 데이터베이스 원본을 지정 하는 Azure 데이터베이스 마이그레이션 서비스에 대 한 DatabaseInfo 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="92d4a-116">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

### [<span data-ttu-id="92d4a-117">새로운 AzureRmDataMigrationFileShare</span><span class="sxs-lookup"><span data-stu-id="92d4a-117">New-AzureRmDataMigrationFileShare</span></span>](New-AzureRmDataMigrationFileShare.md)
<span data-ttu-id="92d4a-118">원본 데이터베이스 백업을 수행할 로컬 네트워크 공유를 지정 하는 Azure 데이터베이스 마이그레이션 서비스에 대 한 데이터 공유 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="92d4a-118">Creates the FileShare object for the Azure Database Migration Service, which specifies the local network share to take the source database backups to.</span></span>

### [<span data-ttu-id="92d4a-119">새로운 AzureRmDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="92d4a-119">New-AzureRmDataMigrationProject</span></span>](New-AzureRmDataMigrationProject.md)
<span data-ttu-id="92d4a-120">새 Azure 데이터베이스 마이그레이션 서비스 프로젝트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="92d4a-120">Creates a new Azure Database Migration Service project.</span></span>

### [<span data-ttu-id="92d4a-121">새로운 AzureRmDataMigrationSelectedDB</span><span class="sxs-lookup"><span data-stu-id="92d4a-121">New-AzureRmDataMigrationSelectedDB</span></span>](New-AzureRmDataMigrationSelectedDB.md)
<span data-ttu-id="92d4a-122">마이그레이션에 대 한 원본 및 대상 데이터베이스에 대 한 정보가 포함 된 데이터베이스 입력 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="92d4a-122">Creates a database input object that contains information about source and target databases for migration.</span></span>

### [<span data-ttu-id="92d4a-123">새로운 AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="92d4a-123">New-AzureRmDataMigrationService</span></span>](New-AzureRmDataMigrationService.md)
<span data-ttu-id="92d4a-124">Azure 데이터베이스 마이그레이션 서비스의 새 인스턴스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="92d4a-124">Creates a new instance of the Azure Database Migration Service.</span></span>

### [<span data-ttu-id="92d4a-125">새로운 AzureRmDataMigrationSyncSelectedDB</span><span class="sxs-lookup"><span data-stu-id="92d4a-125">New-AzureRmDataMigrationSyncSelectedDB</span></span>](New-AzureRmDataMigrationSyncSelectedDB.md)
<span data-ttu-id="92d4a-126">마이그레이션에 대 한 원본 및 대상 데이터베이스에 대 한 정보가 포함 된 동기화 시나리오에 대 한 데이터베이스 입력 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="92d4a-126">Creates a database input object for sync scenarios that contains information about source and target databases for migration.</span></span>

### [<span data-ttu-id="92d4a-127">새로운 AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="92d4a-127">New-AzureRmDataMigrationTask</span></span>](New-AzureRmDataMigrationTask.md)
<span data-ttu-id="92d4a-128">Azure 데이터베이스 마이그레이션 서비스에서 데이터 마이그레이션 작업을 만들고 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="92d4a-128">Creates and starts a data migration task in the Azure Database Migration Service.</span></span>

### [<span data-ttu-id="92d4a-129">제거-AzureRmDataMigrationProject</span><span class="sxs-lookup"><span data-stu-id="92d4a-129">Remove-AzureRmDataMigrationProject</span></span>](Remove-AzureRmDataMigrationProject.md)
<span data-ttu-id="92d4a-130">Azure에서 Azure 데이터베이스 마이그레이션 서비스 프로젝트를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="92d4a-130">Removes an Azure Database Migration Service project from Azure.</span></span>

### [<span data-ttu-id="92d4a-131">제거-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="92d4a-131">Remove-AzureRmDataMigrationService</span></span>](Remove-AzureRmDataMigrationService.md)
<span data-ttu-id="92d4a-132">Azure에서 Azure 데이터베이스 마이그레이션 서비스의 인스턴스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="92d4a-132">Removes an instance of the Azure Database Migration Service from Azure.</span></span>

### [<span data-ttu-id="92d4a-133">제거-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="92d4a-133">Remove-AzureRmDataMigrationTask</span></span>](Remove-AzureRmDataMigrationTask.md)
<span data-ttu-id="92d4a-134">Azure에서 Azure 데이터베이스 마이그레이션 서비스 작업을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="92d4a-134">Removes an Azure Database Migration Service task from Azure.</span></span>

### [<span data-ttu-id="92d4a-135">시작-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="92d4a-135">Start-AzureRmDataMigrationService</span></span>](Start-AzureRmDataMigrationService.md)
<span data-ttu-id="92d4a-136">Azure 데이터베이스 마이그레이션 서비스의 인스턴스를 중지 된 상태로 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="92d4a-136">Starts an instance of the Azure Database Migration Service in a stopped state.</span></span> 

### [<span data-ttu-id="92d4a-137">중지-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="92d4a-137">Stop-AzureRmDataMigrationService</span></span>](Stop-AzureRmDataMigrationService.md)
<span data-ttu-id="92d4a-138">실행 상태인 Azure 데이터베이스 마이그레이션 서비스의 인스턴스를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="92d4a-138">Stops an instance of the Azure Database Migration Service that is in a running state.</span></span>

### [<span data-ttu-id="92d4a-139">중지-AzureRmDataMigrationTask</span><span class="sxs-lookup"><span data-stu-id="92d4a-139">Stop-AzureRmDataMigrationTask</span></span>](Stop-AzureRmDataMigrationTask.md)
<span data-ttu-id="92d4a-140">실행 상태의 Azure 데이터베이스 마이그레이션 서비스 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="92d4a-140">Stops an  Azure Database Migration Service task that is in a running state.</span></span>

