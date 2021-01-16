---
Module Name: Az.ImportExport
Module Guid: 47cfc32b-a3bc-46e1-935e-11a63032bb86
Download Help Link: https://docs.microsoft.com/en-us/powershell/module/az.importexport
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Az.ImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Az.ImportExport.md
ms.openlocfilehash: 2da6d45b7bc8107e70a672962a6bc57ccb9f17a0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339009"
---
# <span data-ttu-id="9b4de-101">Az.ImportExport 모듈</span><span class="sxs-lookup"><span data-stu-id="9b4de-101">Az.ImportExport Module</span></span>
## <span data-ttu-id="9b4de-102">설명</span><span class="sxs-lookup"><span data-stu-id="9b4de-102">Description</span></span>
<span data-ttu-id="9b4de-103">Microsoft Azure PowerShell: ImportExport cmdlet</span><span class="sxs-lookup"><span data-stu-id="9b4de-103">Microsoft Azure PowerShell: ImportExport cmdlets</span></span>

## <span data-ttu-id="9b4de-104">Az.ImportExport Cmdlet</span><span class="sxs-lookup"><span data-stu-id="9b4de-104">Az.ImportExport Cmdlets</span></span>
### [<span data-ttu-id="9b4de-105">Get-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="9b4de-105">Get-AzImportExport</span></span>](Get-AzImportExport.md)
<span data-ttu-id="9b4de-106">기존 작업 관련 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9b4de-106">Gets information about an existing job.</span></span>

### [<span data-ttu-id="9b4de-107">Get-AzImportExportBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="9b4de-107">Get-AzImportExportBitLockerKey</span></span>](Get-AzImportExportBitLockerKey.md)
<span data-ttu-id="9b4de-108">지정된 작업의 모든 드라이브에 대한 BitLocker 키를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="9b4de-108">Returns the BitLocker Keys for all drives in the specified job.</span></span>

### [<span data-ttu-id="9b4de-109">Get-AzImportExportLocation</span><span class="sxs-lookup"><span data-stu-id="9b4de-109">Get-AzImportExportLocation</span></span>](Get-AzImportExportLocation.md)
<span data-ttu-id="9b4de-110">가져오기 또는 내보내기 작업과 연결된 디스크를 배송할 수 있는 위치에 대한 세부 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="9b4de-110">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="9b4de-111">위치는 Azure 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="9b4de-111">A location is an Azure region.</span></span>

### [<span data-ttu-id="9b4de-112">New-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="9b4de-112">New-AzImportExport</span></span>](New-AzImportExport.md)
<span data-ttu-id="9b4de-113">새 작업을 생성하거나 지정된 구독에서 기존 작업을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="9b4de-113">Creates a new job or updates an existing job in the specified subscription.</span></span>

### [<span data-ttu-id="9b4de-114">New-AzImportExportDriveListObject</span><span class="sxs-lookup"><span data-stu-id="9b4de-114">New-AzImportExportDriveListObject</span></span>](New-AzImportExportDriveListObject.md)
<span data-ttu-id="9b4de-115">ImportExport에 대한 DriverList 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9b4de-115">Create a DriverList Object for ImportExport.</span></span>

### [<span data-ttu-id="9b4de-116">Remove-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="9b4de-116">Remove-AzImportExport</span></span>](Remove-AzImportExport.md)
<span data-ttu-id="9b4de-117">기존 작업을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="9b4de-117">Deletes an existing job.</span></span>
<span data-ttu-id="9b4de-118">만들기 또는 완료 상태의 작업만 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b4de-118">Only jobs in the Creating or Completed states can be deleted.</span></span>

### [<span data-ttu-id="9b4de-119">Update-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="9b4de-119">Update-AzImportExport</span></span>](Update-AzImportExport.md)
<span data-ttu-id="9b4de-120">작업의 특정 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="9b4de-120">Updates specific properties of a job.</span></span>
<span data-ttu-id="9b4de-121">이 작업을 호출하여 Import/Export 서비스에 가져오기 또는 내보내기 작업이 있는 하드 드라이브가 Microsoft 데이터 센터로 배송된 경우를 알릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b4de-121">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="9b4de-122">기존 작업을 취소하는 데 사용할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b4de-122">It can also be used to cancel an existing job.</span></span>

