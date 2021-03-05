---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/powershell/module/az.importexport/new-AzImportExportDriveListObject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExportDriveListObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExportDriveListObject.md
ms.openlocfilehash: 4b3907e71dd8d457b1ab38ecd5cdc82b38d7b772
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970827"
---
# <span data-ttu-id="a3cd7-101">New-AzImportExportDriveListObject</span><span class="sxs-lookup"><span data-stu-id="a3cd7-101">New-AzImportExportDriveListObject</span></span>

## <span data-ttu-id="a3cd7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3cd7-102">SYNOPSIS</span></span>
<span data-ttu-id="a3cd7-103">ImportExport용 DriverList 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a3cd7-103">Create a DriverList Object for ImportExport.</span></span>

## <span data-ttu-id="a3cd7-104">구문</span><span class="sxs-lookup"><span data-stu-id="a3cd7-104">SYNTAX</span></span>

```
New-AzImportExportDriveListObject [-BitLockerKey <String>] [-BytesSucceeded <Int64>] [-CopyStatus <String>]
 [-DriveHeaderHash <String>] [-DriveId <String>] [-ErrorLogUri <String>] [-ManifestFile <String>]
 [-ManifestHash <String>] [-ManifestUri <String>] [-PercentComplete <Int32>] [-State <DriveState>]
 [-VerboseLogUri <String>] [<CommonParameters>]
```

## <span data-ttu-id="a3cd7-105">설명</span><span class="sxs-lookup"><span data-stu-id="a3cd7-105">DESCRIPTION</span></span>
<span data-ttu-id="a3cd7-106">ImportExport용 DriverList 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a3cd7-106">Create a DriverList Object for ImportExport.</span></span>

## <span data-ttu-id="a3cd7-107">예제</span><span class="sxs-lookup"><span data-stu-id="a3cd7-107">EXAMPLES</span></span>

### <span data-ttu-id="a3cd7-108">예제 1: ImportExport 작업용 새 DriveList 만들기</span><span class="sxs-lookup"><span data-stu-id="a3cd7-108">Example 1: Create a new DriveList for ImportExport job</span></span>
```powershell
PS C:\> New-AzImportExportDriveListObject -DriveId "9CA995BA" -BitLockerKey "238810-662376-448998-450120-652806-203390-606320-483076" -ManifestFile "\\DriveManifest.xml" -ManifestHash "109B21108597EF36D5785F08303F3638"

BitLockerKey                                            BytesSucceeded CopyStatus DriveHeaderHash DriveId  ErrorLogUri ManifestFile        ManifestHash                     ManifestUri PercentComplete State VerboseLogUri  
------------                                            -------------- ---------- --------------- -------  ----------- ------------        ------------                     ----------- --------------- ----- ------- 
238810-662376-448998-450120-652806-203390-606320-483076 0                                         9CA995BA             \\DriveManifest.xml 109B21108597EF36D5785F08303F3638             0
```

<span data-ttu-id="a3cd7-109">이러한 cmdlet은 ImportExport 작업을 위한 새 DriveList를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="a3cd7-109">These cmdlets create a new DriveList for ImportExport job.</span></span>

## <span data-ttu-id="a3cd7-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a3cd7-110">PARAMETERS</span></span>

### <span data-ttu-id="a3cd7-111">-BitLockerKey</span><span class="sxs-lookup"><span data-stu-id="a3cd7-111">-BitLockerKey</span></span>
<span data-ttu-id="a3cd7-112">드라이브를 암호화하는 데 사용되는 BitLocker 키입니다.</span><span class="sxs-lookup"><span data-stu-id="a3cd7-112">The BitLocker key used to encrypt the drive.</span></span>

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

### <span data-ttu-id="a3cd7-113">-BytesSucceeded</span><span class="sxs-lookup"><span data-stu-id="a3cd7-113">-BytesSucceeded</span></span>
<span data-ttu-id="a3cd7-114">드라이브에 대해 성공적으로 전송된 Bytes입니다.</span><span class="sxs-lookup"><span data-stu-id="a3cd7-114">Bytes successfully transferred for the drive.</span></span>

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

### <span data-ttu-id="a3cd7-115">-CopyStatus</span><span class="sxs-lookup"><span data-stu-id="a3cd7-115">-CopyStatus</span></span>
<span data-ttu-id="a3cd7-116">데이터 전송 프로세스에 대한 자세한 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="a3cd7-116">Detailed status about the data transfer process.</span></span>
<span data-ttu-id="a3cd7-117">이 필드는 드라이브가 전송 상태일 때까지 응답에서 반환되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a3cd7-117">This field is not returned in the response until the drive is in the Transferring state.</span></span>

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

### <span data-ttu-id="a3cd7-118">-DriveHeaderHash</span><span class="sxs-lookup"><span data-stu-id="a3cd7-118">-DriveHeaderHash</span></span>
<span data-ttu-id="a3cd7-119">드라이브 헤더 해시 값입니다.</span><span class="sxs-lookup"><span data-stu-id="a3cd7-119">The drive header hash value.</span></span>

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

### <span data-ttu-id="a3cd7-120">-DriveId</span><span class="sxs-lookup"><span data-stu-id="a3cd7-120">-DriveId</span></span>
<span data-ttu-id="a3cd7-121">공백이 없는 드라이브의 하드웨어 일련 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="a3cd7-121">The drive's hardware serial number, without spaces.</span></span>

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

### <span data-ttu-id="a3cd7-122">-ErrorLogUri</span><span class="sxs-lookup"><span data-stu-id="a3cd7-122">-ErrorLogUri</span></span>
<span data-ttu-id="a3cd7-123">데이터 전송 작업에 대한 오류 로그가 포함된 Blob을 지적하는 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="a3cd7-123">A URI that points to the blob containing the error log for the data transfer operation.</span></span>

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

### <span data-ttu-id="a3cd7-124">-ManifestFile</span><span class="sxs-lookup"><span data-stu-id="a3cd7-124">-ManifestFile</span></span>
<span data-ttu-id="a3cd7-125">드라이브의 매니페스트 파일의 상대 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="a3cd7-125">The relative path of the manifest file on the drive.</span></span>

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

### <span data-ttu-id="a3cd7-126">-ManifestHash</span><span class="sxs-lookup"><span data-stu-id="a3cd7-126">-ManifestHash</span></span>
<span data-ttu-id="a3cd7-127">드라이브의 매니페스트 파일의 Base16 인코딩 MD5 해시입니다.</span><span class="sxs-lookup"><span data-stu-id="a3cd7-127">The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>

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

### <span data-ttu-id="a3cd7-128">-ManifestUri</span><span class="sxs-lookup"><span data-stu-id="a3cd7-128">-ManifestUri</span></span>
<span data-ttu-id="a3cd7-129">드라이브 매니페스트 파일이 포함된 Blob을 지적하는 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="a3cd7-129">A URI that points to the blob containing the drive manifest file.</span></span>

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

### <span data-ttu-id="a3cd7-130">-PercentComplete</span><span class="sxs-lookup"><span data-stu-id="a3cd7-130">-PercentComplete</span></span>
<span data-ttu-id="a3cd7-131">드라이브에 대해 완료된 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="a3cd7-131">Percentage completed for the drive.</span></span>

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

### <span data-ttu-id="a3cd7-132">-State</span><span class="sxs-lookup"><span data-stu-id="a3cd7-132">-State</span></span>
<span data-ttu-id="a3cd7-133">드라이브의 현재 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="a3cd7-133">The drive's current state.</span></span>

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

### <span data-ttu-id="a3cd7-134">-VerboseLogUri</span><span class="sxs-lookup"><span data-stu-id="a3cd7-134">-VerboseLogUri</span></span>
<span data-ttu-id="a3cd7-135">데이터 전송 작업에 대한 자세한 로그가 포함된 Blob을 지적하는 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="a3cd7-135">A URI that points to the blob containing the verbose log for the data transfer operation.</span></span>

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

### <span data-ttu-id="a3cd7-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3cd7-136">CommonParameters</span></span>
<span data-ttu-id="a3cd7-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a3cd7-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3cd7-138">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a3cd7-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3cd7-139">입력</span><span class="sxs-lookup"><span data-stu-id="a3cd7-139">INPUTS</span></span>

## <span data-ttu-id="a3cd7-140">출력</span><span class="sxs-lookup"><span data-stu-id="a3cd7-140">OUTPUTS</span></span>

### <span data-ttu-id="a3cd7-141">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveStatus</span><span class="sxs-lookup"><span data-stu-id="a3cd7-141">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveStatus</span></span>

## <span data-ttu-id="a3cd7-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a3cd7-142">NOTES</span></span>

<span data-ttu-id="a3cd7-143">별칭</span><span class="sxs-lookup"><span data-stu-id="a3cd7-143">ALIASES</span></span>

## <span data-ttu-id="a3cd7-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a3cd7-144">RELATED LINKS</span></span>

