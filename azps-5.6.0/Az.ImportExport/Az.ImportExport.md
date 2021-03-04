---
Module Name: Az.ImportExport
Module Guid: 47cfc32b-a3bc-46e1-935e-11a63032bb86
Download Help Link: https://docs.microsoft.com/powershell/module/az.importexport
Help Version: 1.0.0.0
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Az.ImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Az.ImportExport.md
ms.openlocfilehash: cce265bc3d61f445c6843b0c1ca340ad921e1089
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975787"
---
# <span data-ttu-id="b0534-101">Az.ImportExport 모듈</span><span class="sxs-lookup"><span data-stu-id="b0534-101">Az.ImportExport Module</span></span>
## <span data-ttu-id="b0534-102">설명</span><span class="sxs-lookup"><span data-stu-id="b0534-102">Description</span></span>
<span data-ttu-id="b0534-103">Microsoft Azure PowerShell: ImportExport cmdlet</span><span class="sxs-lookup"><span data-stu-id="b0534-103">Microsoft Azure PowerShell: ImportExport cmdlets</span></span>

## <span data-ttu-id="b0534-104">Az.ImportExport Cmdlet</span><span class="sxs-lookup"><span data-stu-id="b0534-104">Az.ImportExport Cmdlets</span></span>
### [<span data-ttu-id="b0534-105">Get-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="b0534-105">Get-AzImportExport</span></span>](Get-AzImportExport.md)
<span data-ttu-id="b0534-106">기존 작업의 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b0534-106">Gets information about an existing job.</span></span>

### [<span data-ttu-id="b0534-107">Get-AzImportExportBitLockerKey</span><span class="sxs-lookup"><span data-stu-id="b0534-107">Get-AzImportExportBitLockerKey</span></span>](Get-AzImportExportBitLockerKey.md)
<span data-ttu-id="b0534-108">지정된 작업의 모든 드라이브에 대한 BitLocker 키를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="b0534-108">Returns the BitLocker Keys for all drives in the specified job.</span></span>

### [<span data-ttu-id="b0534-109">Get-AzImportExportLocation</span><span class="sxs-lookup"><span data-stu-id="b0534-109">Get-AzImportExportLocation</span></span>](Get-AzImportExportLocation.md)
<span data-ttu-id="b0534-110">가져오기 또는 내보내기 작업과 연결된 디스크를 배송할 수 있는 위치에 대한 세부 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="b0534-110">Returns the details about a location to which you can ship the disks associated with an import or export job.</span></span>
<span data-ttu-id="b0534-111">위치는 Azure 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="b0534-111">A location is an Azure region.</span></span>

### [<span data-ttu-id="b0534-112">New-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="b0534-112">New-AzImportExport</span></span>](New-AzImportExport.md)
<span data-ttu-id="b0534-113">지정된 구독에서 새 작업을 생성하거나 기존 작업을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="b0534-113">Creates a new job or updates an existing job in the specified subscription.</span></span>

### [<span data-ttu-id="b0534-114">New-AzImportExportDriveListObject</span><span class="sxs-lookup"><span data-stu-id="b0534-114">New-AzImportExportDriveListObject</span></span>](New-AzImportExportDriveListObject.md)
<span data-ttu-id="b0534-115">ImportExport용 DriverList 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b0534-115">Create a DriverList Object for ImportExport.</span></span>

### [<span data-ttu-id="b0534-116">Remove-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="b0534-116">Remove-AzImportExport</span></span>](Remove-AzImportExport.md)
<span data-ttu-id="b0534-117">기존 작업을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="b0534-117">Deletes an existing job.</span></span>
<span data-ttu-id="b0534-118">만들기 또는 완료 상태의 작업만 삭제할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b0534-118">Only jobs in the Creating or Completed states can be deleted.</span></span>

### [<span data-ttu-id="b0534-119">Update-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="b0534-119">Update-AzImportExport</span></span>](Update-AzImportExport.md)
<span data-ttu-id="b0534-120">작업의 특정 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="b0534-120">Updates specific properties of a job.</span></span>
<span data-ttu-id="b0534-121">이 작업을 호출하여 가져오기 또는 내보내기 작업을 제공하는 하드 드라이브가 Microsoft 데이터 센터로 배송된 것으로 가져오기/내보내기 서비스에 알릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b0534-121">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="b0534-122">기존 작업을 취소하는 데도 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b0534-122">It can also be used to cancel an existing job.</span></span>

