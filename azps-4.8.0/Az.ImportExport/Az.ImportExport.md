---
Module Name: Az.ImportExport
Module Guid: 47cfc32b-a3bc-46e1-935e-11a63032bb86
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.importexport
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Az.ImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Az.ImportExport.md
ms.openlocfilehash: 2da6d45b7bc8107e70a672962a6bc57ccb9f17a0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212753"
---
# <span data-ttu-id="6a7d4-101">Az 내보내기 모듈</span><span class="sxs-lookup"><span data-stu-id="6a7d4-101">Az.ImportExport Module</span></span>
## <span data-ttu-id="6a7d4-102">설명은</span><span class="sxs-lookup"><span data-stu-id="6a7d4-102">Description</span></span>
<span data-ttu-id="6a7d4-103">Microsoft Azure PowerShell: ImportExport cmdlet</span><span class="sxs-lookup"><span data-stu-id="6a7d4-103">Microsoft Azure PowerShell: ImportExport cmdlets</span></span>

## <span data-ttu-id="6a7d4-104">Az 내보내기 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="6a7d4-104">Az.ImportExport Cmdlets</span></span>
### [<span data-ttu-id="6a7d4-105">Get-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="6a7d4-105">Get-AzImportExport</span></span>](Get-AzImportExport.md)
<span data-ttu-id="6a7d4-106">기존 작업에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6a7d4-106">Gets information about an existing job.</span></span>

### [<span data-ttu-id="6a7d4-107">Get-AzImportExportBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="6a7d4-107">Get-AzImportExportBitLockerKey</span></span>](Get-AzImportExportBitLockerKey.md)
<span data-ttu-id="6a7d4-108">지정 된 작업의 모든 드라이브에 대 한 BitLocker 키를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a7d4-108">Returns the BitLocker Keys for all drives in the specified job.</span></span>

### [<span data-ttu-id="6a7d4-109">Get-AzImportExportLocation</span><span class="sxs-lookup"><span data-stu-id="6a7d4-109">Get-AzImportExportLocation</span></span>](Get-AzImportExportLocation.md)
<span data-ttu-id="6a7d4-110">가져오기 또는 내보내기 작업과 연결 된 디스크를 제공할 수 있는 위치에 대 한 세부 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a7d4-110">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="6a7d4-111">위치는 Azure 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="6a7d4-111">A location is an Azure region.</span></span>

### [<span data-ttu-id="6a7d4-112">새로운 AzImportExport</span><span class="sxs-lookup"><span data-stu-id="6a7d4-112">New-AzImportExport</span></span>](New-AzImportExport.md)
<span data-ttu-id="6a7d4-113">지정 된 구독에서 새 작업을 만들거나 기존 작업을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a7d4-113">Creates a new job or updates an existing job in the specified subscription.</span></span>

### [<span data-ttu-id="6a7d4-114">새로운 AzImportExportDriveListObject</span><span class="sxs-lookup"><span data-stu-id="6a7d4-114">New-AzImportExportDriveListObject</span></span>](New-AzImportExportDriveListObject.md)
<span data-ttu-id="6a7d4-115">ImportExport에 대 한 DriverList 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6a7d4-115">Create a DriverList Object for ImportExport.</span></span>

### [<span data-ttu-id="6a7d4-116">제거-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="6a7d4-116">Remove-AzImportExport</span></span>](Remove-AzImportExport.md)
<span data-ttu-id="6a7d4-117">기존 작업을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a7d4-117">Deletes an existing job.</span></span>
<span data-ttu-id="6a7d4-118">만들기 또는 완료 상태의 작업만 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6a7d4-118">Only jobs in the Creating or Completed states can be deleted.</span></span>

### [<span data-ttu-id="6a7d4-119">업데이트-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="6a7d4-119">Update-AzImportExport</span></span>](Update-AzImportExport.md)
<span data-ttu-id="6a7d4-120">작업의 특정 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a7d4-120">Updates specific properties of a job.</span></span>
<span data-ttu-id="6a7d4-121">이 작업을 호출 하 여 가져오기/내보내기 서비스에 가져오거나 내보내기 작업을 수행 하는 하드 드라이브가 Microsoft 데이터 센터로 제공 되었음을 알릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6a7d4-121">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="6a7d4-122">이를 사용 하 여 기존 작업을 취소할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6a7d4-122">It can also be used to cancel an existing job.</span></span>

