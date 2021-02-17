---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/new-AzImportExportDriveListObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExportDriveListObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExportDriveListObject.md
ms.openlocfilehash: 54252b82ecb32d26cf44b3b6f745856b755d60d9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188305"
---
# <span data-ttu-id="d72b9-101">New-AzImportExportDriveListObject</span><span class="sxs-lookup"><span data-stu-id="d72b9-101">New-AzImportExportDriveListObject</span></span>

## <span data-ttu-id="d72b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d72b9-102">SYNOPSIS</span></span>
<span data-ttu-id="d72b9-103">ImportExport에 대한 DriverList 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d72b9-103">Create a DriverList Object for ImportExport.</span></span>

## <span data-ttu-id="d72b9-104">구문</span><span class="sxs-lookup"><span data-stu-id="d72b9-104">SYNTAX</span></span>

```
New-AzImportExportDriveListObject [-BitLockerKey <String>] [-BytesSucceeded <Int64>] [-CopyStatus <String>]
 [-DriveHeaderHash <String>] [-DriveId <String>] [-ErrorLogUri <String>] [-ManifestFile <String>]
 [-ManifestHash <String>] [-ManifestUri <String>] [-PercentComplete <Int32>] [-State <DriveState>]
 [-VerboseLogUri <String>] [<CommonParameters>]
```

## <span data-ttu-id="d72b9-105">설명</span><span class="sxs-lookup"><span data-stu-id="d72b9-105">DESCRIPTION</span></span>
<span data-ttu-id="d72b9-106">ImportExport에 대한 DriverList 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d72b9-106">Create a DriverList Object for ImportExport.</span></span>

## <span data-ttu-id="d72b9-107">예제</span><span class="sxs-lookup"><span data-stu-id="d72b9-107">EXAMPLES</span></span>

### <span data-ttu-id="d72b9-108">예제 1: ImportExport 작업을 위한 새 DriveList 만들기</span><span class="sxs-lookup"><span data-stu-id="d72b9-108">Example 1: Create a new DriveList for ImportExport job</span></span>
```powershell
PS C:\> New-AzImportExportDriveListObject -DriveId "9CA995BA" -BitLockerKey "238810-662376-448998-450120-652806-203390-606320-483076" -ManifestFile "\\DriveManifest.xml" -ManifestHash "109B21108597EF36D5785F08303F3638"

BitLockerKey                                            BytesSucceeded CopyStatus DriveHeaderHash DriveId  ErrorLogUri ManifestFile        ManifestHash                     ManifestUri PercentComplete State VerboseLogUri  
------------                                            -------------- ---------- --------------- -------  ----------- ------------        ------------                     ----------- --------------- ----- ------- 
238810-662376-448998-450120-652806-203390-606320-483076 0                                         9CA995BA             \\DriveManifest.xml 109B21108597EF36D5785F08303F3638             0
```

<span data-ttu-id="d72b9-109">이러한 cmdlet은 ImportExport 작업을 위한 새 DriveList를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="d72b9-109">These cmdlets create a new DriveList for ImportExport job.</span></span>

## <span data-ttu-id="d72b9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d72b9-110">PARAMETERS</span></span>

### <span data-ttu-id="d72b9-111">-BitLockerKey</span><span class="sxs-lookup"><span data-stu-id="d72b9-111">-BitLockerKey</span></span>
<span data-ttu-id="d72b9-112">드라이브를 암호화하는 데 사용되는 BitLocker 키입니다.</span><span class="sxs-lookup"><span data-stu-id="d72b9-112">The BitLocker key used to encrypt the drive.</span></span>

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

### <span data-ttu-id="d72b9-113">-BytesSucceeded</span><span class="sxs-lookup"><span data-stu-id="d72b9-113">-BytesSucceeded</span></span>
<span data-ttu-id="d72b9-114">드라이브에 대해 성공적으로 전송된 Bytes입니다.</span><span class="sxs-lookup"><span data-stu-id="d72b9-114">Bytes successfully transferred for the drive.</span></span>

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

### <span data-ttu-id="d72b9-115">-CopyStatus</span><span class="sxs-lookup"><span data-stu-id="d72b9-115">-CopyStatus</span></span>
<span data-ttu-id="d72b9-116">데이터 전송 프로세스에 대한 자세한 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="d72b9-116">Detailed status about the data transfer process.</span></span>
<span data-ttu-id="d72b9-117">이 필드는 드라이브가 전송 중 상태가 될 때까지 응답에서 반환되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d72b9-117">This field is not returned in the response until the drive is in the Transferring state.</span></span>

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

### <span data-ttu-id="d72b9-118">-DriveHeaderHash</span><span class="sxs-lookup"><span data-stu-id="d72b9-118">-DriveHeaderHash</span></span>
<span data-ttu-id="d72b9-119">드라이브 헤더 해시 값입니다.</span><span class="sxs-lookup"><span data-stu-id="d72b9-119">The drive header hash value.</span></span>

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

### <span data-ttu-id="d72b9-120">-DriveId</span><span class="sxs-lookup"><span data-stu-id="d72b9-120">-DriveId</span></span>
<span data-ttu-id="d72b9-121">드라이브의 하드웨어 일련 번호(공백 없이).</span><span class="sxs-lookup"><span data-stu-id="d72b9-121">The drive's hardware serial number, without spaces.</span></span>

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

### <span data-ttu-id="d72b9-122">-ErrorLogUri</span><span class="sxs-lookup"><span data-stu-id="d72b9-122">-ErrorLogUri</span></span>
<span data-ttu-id="d72b9-123">데이터 전송 작업에 대한 오류 로그가 포함된 Blob을 지점으로 하는 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="d72b9-123">A URI that points to the blob containing the error log for the data transfer operation.</span></span>

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

### <span data-ttu-id="d72b9-124">-ManifestFile</span><span class="sxs-lookup"><span data-stu-id="d72b9-124">-ManifestFile</span></span>
<span data-ttu-id="d72b9-125">드라이브에 있는 매니페스트 파일의 상대 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="d72b9-125">The relative path of the manifest file on the drive.</span></span>

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

### <span data-ttu-id="d72b9-126">-ManifestHash</span><span class="sxs-lookup"><span data-stu-id="d72b9-126">-ManifestHash</span></span>
<span data-ttu-id="d72b9-127">드라이브에 있는 매니페스트 파일의 Base16 인코딩 MD5 해시입니다.</span><span class="sxs-lookup"><span data-stu-id="d72b9-127">The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>

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

### <span data-ttu-id="d72b9-128">-ManifestUri</span><span class="sxs-lookup"><span data-stu-id="d72b9-128">-ManifestUri</span></span>
<span data-ttu-id="d72b9-129">드라이브 매니페스트 파일이 포함된 Blob을 지점하는 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="d72b9-129">A URI that points to the blob containing the drive manifest file.</span></span>

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

### <span data-ttu-id="d72b9-130">-PercentComplete</span><span class="sxs-lookup"><span data-stu-id="d72b9-130">-PercentComplete</span></span>
<span data-ttu-id="d72b9-131">드라이브에 대해 완료된 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="d72b9-131">Percentage completed for the drive.</span></span>

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

### <span data-ttu-id="d72b9-132">-State</span><span class="sxs-lookup"><span data-stu-id="d72b9-132">-State</span></span>
<span data-ttu-id="d72b9-133">드라이브의 현재 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="d72b9-133">The drive's current state.</span></span>

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

### <span data-ttu-id="d72b9-134">-VerboseLogUri</span><span class="sxs-lookup"><span data-stu-id="d72b9-134">-VerboseLogUri</span></span>
<span data-ttu-id="d72b9-135">데이터 전송 작업에 대한 자세한 로그가 포함된 Blob을 지점하는 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="d72b9-135">A URI that points to the blob containing the verbose log for the data transfer operation.</span></span>

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

### <span data-ttu-id="d72b9-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d72b9-136">CommonParameters</span></span>
<span data-ttu-id="d72b9-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d72b9-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d72b9-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d72b9-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d72b9-139">입력</span><span class="sxs-lookup"><span data-stu-id="d72b9-139">INPUTS</span></span>

## <span data-ttu-id="d72b9-140">출력</span><span class="sxs-lookup"><span data-stu-id="d72b9-140">OUTPUTS</span></span>

### <span data-ttu-id="d72b9-141">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveStatus</span><span class="sxs-lookup"><span data-stu-id="d72b9-141">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveStatus</span></span>

## <span data-ttu-id="d72b9-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d72b9-142">NOTES</span></span>

<span data-ttu-id="d72b9-143">별칭</span><span class="sxs-lookup"><span data-stu-id="d72b9-143">ALIASES</span></span>

## <span data-ttu-id="d72b9-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d72b9-144">RELATED LINKS</span></span>

