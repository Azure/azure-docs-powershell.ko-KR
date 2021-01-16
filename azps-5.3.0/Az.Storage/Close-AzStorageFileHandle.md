---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/close-azstoragefilehandle
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Close-AzStorageFileHandle.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Close-AzStorageFileHandle.md
ms.openlocfilehash: 0ac029d4fbe0ab632671f024ff90ebeca9717d50
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376384"
---
# <span data-ttu-id="0f468-101">Close-AzStorageFileHandle</span><span class="sxs-lookup"><span data-stu-id="0f468-101">Close-AzStorageFileHandle</span></span>

## <span data-ttu-id="0f468-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f468-102">SYNOPSIS</span></span>
<span data-ttu-id="0f468-103">파일 공유, 파일 디렉터리 또는 파일의 파일 핸들을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="0f468-103">Closes file handles of a file share, a file directory or a file.</span></span>

## <span data-ttu-id="0f468-104">구문</span><span class="sxs-lookup"><span data-stu-id="0f468-104">SYNTAX</span></span>

### <span data-ttu-id="0f468-105">ShareNameCloseAll(기본값)</span><span class="sxs-lookup"><span data-stu-id="0f468-105">ShareNameCloseAll (Default)</span></span>
```
Close-AzStorageFileHandle [-ShareName] <String> [[-Path] <String>] [-Recursive] [-CloseAll]
 [-Context <IStorageContext>] [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f468-106">ShareNameCloseSingle</span><span class="sxs-lookup"><span data-stu-id="0f468-106">ShareNameCloseSingle</span></span>
```
Close-AzStorageFileHandle [-ShareName] <String> -FileHandle <PSFileHandle> [-Context <IStorageContext>]
 [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0f468-107">ShareCloseAll</span><span class="sxs-lookup"><span data-stu-id="0f468-107">ShareCloseAll</span></span>
```
Close-AzStorageFileHandle [-Share] <CloudFileShare> [[-Path] <String>] [-Recursive] [-CloseAll] [-PassThru]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0f468-108">ShareCloseSingle</span><span class="sxs-lookup"><span data-stu-id="0f468-108">ShareCloseSingle</span></span>
```
Close-AzStorageFileHandle [-Share] <CloudFileShare> -FileHandle <PSFileHandle> [-PassThru] [-AsJob]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0f468-109">DirectoryCloseAll</span><span class="sxs-lookup"><span data-stu-id="0f468-109">DirectoryCloseAll</span></span>
```
Close-AzStorageFileHandle [-Directory] <CloudFileDirectory> [[-Path] <String>] [-Recursive] [-CloseAll]
 [-PassThru] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0f468-110">FileCloseAll</span><span class="sxs-lookup"><span data-stu-id="0f468-110">FileCloseAll</span></span>
```
Close-AzStorageFileHandle [-File] <CloudFile> [-CloseAll] [-PassThru] [-AsJob]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0f468-111">설명</span><span class="sxs-lookup"><span data-stu-id="0f468-111">DESCRIPTION</span></span>
<span data-ttu-id="0f468-112">**Close-AzStorageFileHandle cmdlet은** 파일 공유 또는 파일 디렉터리 또는 파일의 파일 핸들을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="0f468-112">The **Close-AzStorageFileHandle** cmdlet closes file handles of a  file share, or file directory or a file.</span></span>

## <span data-ttu-id="0f468-113">예제</span><span class="sxs-lookup"><span data-stu-id="0f468-113">EXAMPLES</span></span>

### <span data-ttu-id="0f468-114">예제 1: 현재 Storage 계정의 모든 파일 공유를 나열하고 파일 공유의 모든 파일 핸들을 재발적으로 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="0f468-114">Example 1: Lists all file shares of current Storage Account, and close all file handles of the file shares recursively.</span></span>
```
PS C:\>Get-AzStorageShare | Close-AzStorageFileHandle -CloseAll -Recursive
```

<span data-ttu-id="0f468-115">이 명령은 현재 Storage 계정의 모든 파일 공유를 나열하고 파일 공유의 모든 파일 핸들을 재발적으로 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="0f468-115">This command lists all file shares of current Storage Account, and close all file handles of the file shares recursively..</span></span>

### <span data-ttu-id="0f468-116">예제 2: 파일 디렉터리의 모든 파일 핸들을 재발적으로 닫고 닫힌 파일 핸들 수 표시</span><span class="sxs-lookup"><span data-stu-id="0f468-116">Example 2: Close all file handles on a file directory recursively and show the closed file handle count</span></span>
```
PS C:\>Close-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2' -Recursive -CloseAll -PassThru
10
```

<span data-ttu-id="0f468-117">이 명령은 파일 디렉터리의 모든 파일 핸들을 닫고 닫힌 파일 핸들 수를 보여 주며,</span><span class="sxs-lookup"><span data-stu-id="0f468-117">This command closes all file handles on a file directory and show the closed file handle count.</span></span>

### <span data-ttu-id="0f468-118">예제 3: 파일 디렉터리에서 1일 전에 열리며 모든 파일 핸들 닫기</span><span class="sxs-lookup"><span data-stu-id="0f468-118">Example 3: Close all file handles which is opened 1 day ago on a file directory</span></span>
```
PS C:\>Get-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2' -Recursive | ? {$_.OpenTime.DateTime.AddDays(1) -lt (Get-Date)} | Close-AzStorageFileHandle -ShareName "mysharename"
```

<span data-ttu-id="0f468-119">이 명령은 파일 디렉터리의 모든 파일 핸들을 재발적으로 나열하고, 1일 전에 연 핸들을 필터로 처리한 다음, 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="0f468-119">This command lists all file handles on a file directory recursively, filters out the handles which are opened 1 day ago, and then close them.</span></span>

### <span data-ttu-id="0f468-120">예제 4: 파일의 모든 파일 핸들 닫기</span><span class="sxs-lookup"><span data-stu-id="0f468-120">Example 4: Close all file handles on a file</span></span>
```
PS C:\>Close-AzStorageFileHandle -ShareName "mysharename" -Path 'dir1/dir2/test.txt' -CloseAll
```

<span data-ttu-id="0f468-121">이 명령은 파일의 모든 파일 핸들을 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="0f468-121">This command closes all file handles on a file.</span></span>

## <span data-ttu-id="0f468-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f468-122">PARAMETERS</span></span>

### <span data-ttu-id="0f468-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0f468-123">-AsJob</span></span>
<span data-ttu-id="0f468-124">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="0f468-124">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f468-125">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0f468-125">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="0f468-126">각 요청에 대한 클라이언트 쪽 최대 실행 시간(초)입니다.</span><span class="sxs-lookup"><span data-stu-id="0f468-126">The client side maximum execution time for each request in seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f468-127">-CloseAll</span><span class="sxs-lookup"><span data-stu-id="0f468-127">-CloseAll</span></span>
<span data-ttu-id="0f468-128">모든 파일 핸들을 강제로 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="0f468-128">Force close all File handles.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ShareNameCloseAll, ShareCloseAll, DirectoryCloseAll, FileCloseAll
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f468-129">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="0f468-129">-ConcurrentTaskCount</span></span>
<span data-ttu-id="0f468-130">동시 비동기 작업의 총 양입니다.</span><span class="sxs-lookup"><span data-stu-id="0f468-130">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="0f468-131">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="0f468-131">The default value is 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f468-132">-Context</span><span class="sxs-lookup"><span data-stu-id="0f468-132">-Context</span></span>
<span data-ttu-id="0f468-133">Azure Storage 컨텍스트 개체</span><span class="sxs-lookup"><span data-stu-id="0f468-133">Azure Storage Context Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareNameCloseAll, ShareNameCloseSingle
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f468-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f468-134">-DefaultProfile</span></span>
<span data-ttu-id="0f468-135">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0f468-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f468-136">-Directory</span><span class="sxs-lookup"><span data-stu-id="0f468-136">-Directory</span></span>
<span data-ttu-id="0f468-137">CloudFileDirectory 개체는 파일/directories가 나열되는 기본 폴더를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0f468-137">CloudFileDirectory object indicated the base folder where the files/directories would be listed.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: DirectoryCloseAll
Aliases: CloudFileDirectory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f468-138">-File</span><span class="sxs-lookup"><span data-stu-id="0f468-138">-File</span></span>
<span data-ttu-id="0f468-139">CloudFile 개체는 핸들을 닫을 파일을 표시했습니다.</span><span class="sxs-lookup"><span data-stu-id="0f468-139">CloudFile object indicated the file to close handle.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: FileCloseAll
Aliases: CloudFile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f468-140">-FileHandle</span><span class="sxs-lookup"><span data-stu-id="0f468-140">-FileHandle</span></span>
<span data-ttu-id="0f468-141">닫을 파일 핸들입니다.</span><span class="sxs-lookup"><span data-stu-id="0f468-141">The File Handle to close.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSFileHandle
Parameter Sets: ShareNameCloseSingle, ShareCloseSingle
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f468-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0f468-142">-PassThru</span></span>
<span data-ttu-id="0f468-143">닫힌 파일 핸들 수를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="0f468-143">Return the count of closed file handles.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f468-144">-Path</span><span class="sxs-lookup"><span data-stu-id="0f468-144">-Path</span></span>
<span data-ttu-id="0f468-145">기존 파일/디렉터리에 대한 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="0f468-145">Path to an existing file/directory.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareNameCloseAll, ShareCloseAll, DirectoryCloseAll
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f468-146">-Recursive</span><span class="sxs-lookup"><span data-stu-id="0f468-146">-Recursive</span></span>
<span data-ttu-id="0f468-147">목록은 재발적으로 처리합니다.</span><span class="sxs-lookup"><span data-stu-id="0f468-147">List handles Recursively.</span></span>
<span data-ttu-id="0f468-148">파일 디렉터리에서만 작동합니다.</span><span class="sxs-lookup"><span data-stu-id="0f468-148">Only works on File Directory.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ShareNameCloseAll, ShareCloseAll, DirectoryCloseAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f468-149">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0f468-149">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="0f468-150">각 요청에 대한 서버 시간(초)입니다.</span><span class="sxs-lookup"><span data-stu-id="0f468-150">The server time out for each request in seconds.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f468-151">-공유</span><span class="sxs-lookup"><span data-stu-id="0f468-151">-Share</span></span>
<span data-ttu-id="0f468-152">CloudFileShare 개체는 파일/감독이 나열될 공유를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0f468-152">CloudFileShare object indicated the share where the files/directories would be listed.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: ShareCloseAll, ShareCloseSingle
Aliases: CloudFileShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f468-153">-ShareName</span><span class="sxs-lookup"><span data-stu-id="0f468-153">-ShareName</span></span>
<span data-ttu-id="0f468-154">파일/폴더가 나열될 파일 공유의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0f468-154">Name of the file share where the files/directories would be listed.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareNameCloseAll, ShareNameCloseSingle
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f468-155">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0f468-155">-Confirm</span></span>
<span data-ttu-id="0f468-156">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0f468-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f468-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f468-157">-WhatIf</span></span>
<span data-ttu-id="0f468-158">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="0f468-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f468-159">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0f468-159">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f468-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f468-160">CommonParameters</span></span>
<span data-ttu-id="0f468-161">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0f468-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f468-162">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0f468-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f468-163">입력</span><span class="sxs-lookup"><span data-stu-id="0f468-163">INPUTS</span></span>

### <span data-ttu-id="0f468-164">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="0f468-164">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="0f468-165">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="0f468-165">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="0f468-166">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0f468-166">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0f468-167">출력</span><span class="sxs-lookup"><span data-stu-id="0f468-167">OUTPUTS</span></span>

### <span data-ttu-id="0f468-168">Microsoft.Azure.Storage.File.CloseFileHandleResultSegment</span><span class="sxs-lookup"><span data-stu-id="0f468-168">Microsoft.Azure.Storage.File.CloseFileHandleResultSegment</span></span>

## <span data-ttu-id="0f468-169">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0f468-169">NOTES</span></span>

## <span data-ttu-id="0f468-170">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0f468-170">RELATED LINKS</span></span>
