---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/new-AzImportExportDriveListObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExportDriveListObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExportDriveListObject.md
ms.openlocfilehash: 54252b82ecb32d26cf44b3b6f745856b755d60d9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98364491"
---
# <span data-ttu-id="f6504-101">New-AzImportExportDriveListObject</span><span class="sxs-lookup"><span data-stu-id="f6504-101">New-AzImportExportDriveListObject</span></span>

## <span data-ttu-id="f6504-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6504-102">SYNOPSIS</span></span>
<span data-ttu-id="f6504-103">ImportExport에 대한 DriverList 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f6504-103">Create a DriverList Object for ImportExport.</span></span>

## <span data-ttu-id="f6504-104">구문</span><span class="sxs-lookup"><span data-stu-id="f6504-104">SYNTAX</span></span>

```
New-AzImportExportDriveListObject [-BitLockerKey <String>] [-BytesSucceeded <Int64>] [-CopyStatus <String>]
 [-DriveHeaderHash <String>] [-DriveId <String>] [-ErrorLogUri <String>] [-ManifestFile <String>]
 [-ManifestHash <String>] [-ManifestUri <String>] [-PercentComplete <Int32>] [-State <DriveState>]
 [-VerboseLogUri <String>] [<CommonParameters>]
```

## <span data-ttu-id="f6504-105">설명</span><span class="sxs-lookup"><span data-stu-id="f6504-105">DESCRIPTION</span></span>
<span data-ttu-id="f6504-106">ImportExport에 대한 DriverList 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f6504-106">Create a DriverList Object for ImportExport.</span></span>

## <span data-ttu-id="f6504-107">예제</span><span class="sxs-lookup"><span data-stu-id="f6504-107">EXAMPLES</span></span>

### <span data-ttu-id="f6504-108">예제 1: ImportExport 작업을 위한 새 DriveList 만들기</span><span class="sxs-lookup"><span data-stu-id="f6504-108">Example 1: Create a new DriveList for ImportExport job</span></span>
```powershell
PS C:\> New-AzImportExportDriveListObject -DriveId "9CA995BA" -BitLockerKey "238810-662376-448998-450120-652806-203390-606320-483076" -ManifestFile "\\DriveManifest.xml" -ManifestHash "109B21108597EF36D5785F08303F3638"

BitLockerKey                                            BytesSucceeded CopyStatus DriveHeaderHash DriveId  ErrorLogUri ManifestFile        ManifestHash                     ManifestUri PercentComplete State VerboseLogUri  
------------                                            -------------- ---------- --------------- -------  ----------- ------------        ------------                     ----------- --------------- ----- ------- 
238810-662376-448998-450120-652806-203390-606320-483076 0                                         9CA995BA             \\DriveManifest.xml 109B21108597EF36D5785F08303F3638             0
```

<span data-ttu-id="f6504-109">이러한 cmdlet은 ImportExport 작업을 위한 새 DriveList를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="f6504-109">These cmdlets create a new DriveList for ImportExport job.</span></span>

## <span data-ttu-id="f6504-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f6504-110">PARAMETERS</span></span>

### <span data-ttu-id="f6504-111">-BitLockerKey</span><span class="sxs-lookup"><span data-stu-id="f6504-111">-BitLockerKey</span></span>
<span data-ttu-id="f6504-112">드라이브를 암호화하는 데 사용되는 BitLocker 키입니다.</span><span class="sxs-lookup"><span data-stu-id="f6504-112">The BitLocker key used to encrypt the drive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6504-113">-BytesSucceeded</span><span class="sxs-lookup"><span data-stu-id="f6504-113">-BytesSucceeded</span></span>
<span data-ttu-id="f6504-114">드라이브에 대해 성공적으로 전송된 Bytes입니다.</span><span class="sxs-lookup"><span data-stu-id="f6504-114">Bytes successfully transferred for the drive.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6504-115">-CopyStatus</span><span class="sxs-lookup"><span data-stu-id="f6504-115">-CopyStatus</span></span>
<span data-ttu-id="f6504-116">데이터 전송 프로세스에 대한 자세한 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="f6504-116">Detailed status about the data transfer process.</span></span>
<span data-ttu-id="f6504-117">이 필드는 드라이브가 전송 중 상태가 될 때까지 응답에서 반환되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f6504-117">This field is not returned in the response until the drive is in the Transferring state.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6504-118">-DriveHeaderHash</span><span class="sxs-lookup"><span data-stu-id="f6504-118">-DriveHeaderHash</span></span>
<span data-ttu-id="f6504-119">드라이브 헤더 해시 값입니다.</span><span class="sxs-lookup"><span data-stu-id="f6504-119">The drive header hash value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6504-120">-DriveId</span><span class="sxs-lookup"><span data-stu-id="f6504-120">-DriveId</span></span>
<span data-ttu-id="f6504-121">드라이브의 하드웨어 일련 번호(공백 없이).</span><span class="sxs-lookup"><span data-stu-id="f6504-121">The drive's hardware serial number, without spaces.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6504-122">-ErrorLogUri</span><span class="sxs-lookup"><span data-stu-id="f6504-122">-ErrorLogUri</span></span>
<span data-ttu-id="f6504-123">데이터 전송 작업에 대한 오류 로그가 포함된 Blob을 지점으로 하는 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="f6504-123">A URI that points to the blob containing the error log for the data transfer operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6504-124">-ManifestFile</span><span class="sxs-lookup"><span data-stu-id="f6504-124">-ManifestFile</span></span>
<span data-ttu-id="f6504-125">드라이브에 있는 매니페스트 파일의 상대 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="f6504-125">The relative path of the manifest file on the drive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6504-126">-ManifestHash</span><span class="sxs-lookup"><span data-stu-id="f6504-126">-ManifestHash</span></span>
<span data-ttu-id="f6504-127">드라이브에 있는 매니페스트 파일의 Base16 인코딩 MD5 해시입니다.</span><span class="sxs-lookup"><span data-stu-id="f6504-127">The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6504-128">-ManifestUri</span><span class="sxs-lookup"><span data-stu-id="f6504-128">-ManifestUri</span></span>
<span data-ttu-id="f6504-129">드라이브 매니페스트 파일이 포함된 Blob을 지점하는 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="f6504-129">A URI that points to the blob containing the drive manifest file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6504-130">-PercentComplete</span><span class="sxs-lookup"><span data-stu-id="f6504-130">-PercentComplete</span></span>
<span data-ttu-id="f6504-131">드라이브에 대해 완료된 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="f6504-131">Percentage completed for the drive.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6504-132">-State</span><span class="sxs-lookup"><span data-stu-id="f6504-132">-State</span></span>
<span data-ttu-id="f6504-133">드라이브의 현재 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="f6504-133">The drive's current state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Support.DriveState
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6504-134">-VerboseLogUri</span><span class="sxs-lookup"><span data-stu-id="f6504-134">-VerboseLogUri</span></span>
<span data-ttu-id="f6504-135">데이터 전송 작업에 대한 자세한 로그가 포함된 Blob을 지점하는 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="f6504-135">A URI that points to the blob containing the verbose log for the data transfer operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6504-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6504-136">CommonParameters</span></span>
<span data-ttu-id="f6504-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f6504-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6504-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f6504-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6504-139">입력</span><span class="sxs-lookup"><span data-stu-id="f6504-139">INPUTS</span></span>

## <span data-ttu-id="f6504-140">출력</span><span class="sxs-lookup"><span data-stu-id="f6504-140">OUTPUTS</span></span>

### <span data-ttu-id="f6504-141">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveStatus</span><span class="sxs-lookup"><span data-stu-id="f6504-141">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveStatus</span></span>

## <span data-ttu-id="f6504-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f6504-142">NOTES</span></span>

<span data-ttu-id="f6504-143">별칭</span><span class="sxs-lookup"><span data-stu-id="f6504-143">ALIASES</span></span>

## <span data-ttu-id="f6504-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f6504-144">RELATED LINKS</span></span>

