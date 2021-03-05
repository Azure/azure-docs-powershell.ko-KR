---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
ms.openlocfilehash: 33fcfabb50b0b4af73fe7111c587ac88e746598e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981515"
---
# <span data-ttu-id="f59d2-101">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f59d2-101">Get-AzStorageFileContent</span></span>

## <span data-ttu-id="f59d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f59d2-102">SYNOPSIS</span></span>
<span data-ttu-id="f59d2-103">파일의 콘텐츠를 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="f59d2-103">Downloads the contents of a file.</span></span>

## <span data-ttu-id="f59d2-104">구문</span><span class="sxs-lookup"><span data-stu-id="f59d2-104">SYNTAX</span></span>

### <span data-ttu-id="f59d2-105">ShareName(기본값)</span><span class="sxs-lookup"><span data-stu-id="f59d2-105">ShareName (Default)</span></span>
```
Get-AzStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="f59d2-106">공유</span><span class="sxs-lookup"><span data-stu-id="f59d2-106">Share</span></span>
```
Get-AzStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="f59d2-107">디렉터리</span><span class="sxs-lookup"><span data-stu-id="f59d2-107">Directory</span></span>
```
Get-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="f59d2-108">파일</span><span class="sxs-lookup"><span data-stu-id="f59d2-108">File</span></span>
```
Get-AzStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

## <span data-ttu-id="f59d2-109">설명</span><span class="sxs-lookup"><span data-stu-id="f59d2-109">DESCRIPTION</span></span>
<span data-ttu-id="f59d2-110">**Get-AzStorageFileContent** cmdlet은 파일의 내용을 다운로드한 다음 지정한 대상에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="f59d2-110">The **Get-AzStorageFileContent** cmdlet downloads the contents of a file, and then saves it to a destination that you specify.</span></span>
<span data-ttu-id="f59d2-111">이 cmdlet은 파일의 내용을 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f59d2-111">This cmdlet does not return the contents of the file.</span></span>

## <span data-ttu-id="f59d2-112">예제</span><span class="sxs-lookup"><span data-stu-id="f59d2-112">EXAMPLES</span></span>

### <span data-ttu-id="f59d2-113">예제 1: 폴더에서 파일 다운로드</span><span class="sxs-lookup"><span data-stu-id="f59d2-113">Example 1: Download a file from a folder</span></span>
```
PS C:\>Get-AzStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="f59d2-114">이 명령은 ContosoShare06 파일 공유에서 현재 폴더로 ContosoWorkingFolder 폴더에 CurrentDataFile이라는 파일을 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="f59d2-114">This command downloads a file that is named CurrentDataFile in the folder ContosoWorkingFolder from the file share ContosoShare06 to current folder.</span></span>

### <span data-ttu-id="f59d2-115">예제 2: 샘플 파일 공유에서 파일 다운로드</span><span class="sxs-lookup"><span data-stu-id="f59d2-115">Example 2: Downloads the files under sample file share</span></span>
```
PS C:\>Get-AzStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzStorageFileContent
```

<span data-ttu-id="f59d2-116">이 예제에서는 샘플 파일 공유에서 파일을 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="f59d2-116">This example downloads the files under sample file share</span></span>

### <span data-ttu-id="f59d2-117">예제 3: 로컬 파일에 Azure 파일을 다운로드하고 로컬 파일에서 Azure 파일 SMB 속성(파일 속성, 파일 만들기 시간, 파일 마지막 쓰기 시간)을 보존합니다.</span><span class="sxs-lookup"><span data-stu-id="f59d2-117">Example 3: Download an Azure file to a local file, and perserve the Azure File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the local file.</span></span>
```
PS C:\>Get-AzStorageFileContent -ShareName sample -Path "dir1/file1" -Destination $localFilePath -PreserveSMBAttribute
```

<span data-ttu-id="f59d2-118">이 예제에서는 Azure 파일을 로컬 파일에 다운로드하고 로컬 파일에서 Azure 파일 SMB 속성(File Attributtes, 파일 만들기 시간, 파일 마지막 쓰기 시간)을 보존합니다.</span><span class="sxs-lookup"><span data-stu-id="f59d2-118">This example downloads an Azure file to a local file, and perserves the Azure File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the local file.</span></span>

## <span data-ttu-id="f59d2-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f59d2-119">PARAMETERS</span></span>

### <span data-ttu-id="f59d2-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f59d2-120">-AsJob</span></span>
<span data-ttu-id="f59d2-121">백그라운드에서 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="f59d2-121">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="f59d2-122">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="f59d2-122">-CheckMd5</span></span>
<span data-ttu-id="f59d2-123">다운로드한 파일에 대한 Md5 합계를 확인할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f59d2-123">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

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

### <span data-ttu-id="f59d2-124">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f59d2-124">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="f59d2-125">하나의 서비스 요청에 대해 클라이언트 쪽 시간 간격(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f59d2-125">Specifies the client-side time-out interval, in seconds, for one service request.</span></span> <span data-ttu-id="f59d2-126">지정된 간격에서 이전 호출이 실패하면 이 cmdlet에서 요청을 다시 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="f59d2-126">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span> <span data-ttu-id="f59d2-127">간격이 경과하기 전에 이 cmdlet에서 성공적인 응답을 받지 못하면 이 cmdlet은 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f59d2-127">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="f59d2-128">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="f59d2-128">-ConcurrentTaskCount</span></span>
<span data-ttu-id="f59d2-129">최대 동시 네트워크 호출을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f59d2-129">Specifies the maximum concurrent network calls.</span></span> <span data-ttu-id="f59d2-130">이 매개 변수를 사용하여 최대 동시 네트워크 호출 수를 지정하여 로컬 CPU 및 대역폭 사용량을 제한하는 동시성 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f59d2-130">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span> <span data-ttu-id="f59d2-131">지정된 값은 절대 개수로 코어 수에 곱하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f59d2-131">The specified value is an absolute count and is not multiplied by the core count.</span></span> <span data-ttu-id="f59d2-132">이 매개 변수는 초당 100킬로비트와 같은 대역폭이 낮은 환경에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f59d2-132">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span> <span data-ttu-id="f59d2-133">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="f59d2-133">The default value is 10.</span></span>

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

### <span data-ttu-id="f59d2-134">-Context</span><span class="sxs-lookup"><span data-stu-id="f59d2-134">-Context</span></span>
<span data-ttu-id="f59d2-135">Azure Storage 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f59d2-135">Specifies an Azure Storage context.</span></span> <span data-ttu-id="f59d2-136">컨텍스트를 얻지 위해 New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f59d2-136">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f59d2-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f59d2-137">-DefaultProfile</span></span>
<span data-ttu-id="f59d2-138">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f59d2-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f59d2-139">-대상</span><span class="sxs-lookup"><span data-stu-id="f59d2-139">-Destination</span></span>
<span data-ttu-id="f59d2-140">대상 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f59d2-140">Specifies the destination path.</span></span>
<span data-ttu-id="f59d2-141">이 cmdlet은 이 매개 변수가 지정한 위치로 파일 콘텐츠를 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="f59d2-141">This cmdlet downloads the file contents to the location that this parameter specifies.</span></span>
<span data-ttu-id="f59d2-142">존재하지 않는 파일의 경로를 지정하는 경우 이 cmdlet은 해당 파일을 만들고 내용을 새 파일에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="f59d2-142">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="f59d2-143">이미 존재하는 파일의 경로를 지정하고 *Force* 매개 변수를 지정하면 cmdlet이 파일을 덮어 써 놨습니다.</span><span class="sxs-lookup"><span data-stu-id="f59d2-143">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="f59d2-144">기존 파일의 경로를 지정하고 *Force를* 지정하지 않으면 cmdlet이 계속되기 전에 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="f59d2-144">If you specify a path of an existing file and you do not specify *Force*, the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="f59d2-145">폴더의 경로를 지정하는 경우 이 cmdlet은 Azure Storage 파일의 이름이 있는 파일을 만들기 위해 시도합니다.</span><span class="sxs-lookup"><span data-stu-id="f59d2-145">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f59d2-146">-Directory</span><span class="sxs-lookup"><span data-stu-id="f59d2-146">-Directory</span></span>
<span data-ttu-id="f59d2-147">폴더를 **CloudFileDirectory 개체로 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="f59d2-147">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="f59d2-148">이 cmdlet은 이 매개 변수가 지정하는 폴더의 파일에 대한 콘텐츠를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f59d2-148">This cmdlet gets content for a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="f59d2-149">디렉터리를 구하기 위해 New-AzStorageDirectory cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f59d2-149">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="f59d2-150">또한 Get-AzStorageFile cmdlet을 사용하여 디렉터리를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f59d2-150">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases: CloudFileDirectory

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f59d2-151">-File</span><span class="sxs-lookup"><span data-stu-id="f59d2-151">-File</span></span>
<span data-ttu-id="f59d2-152">파일을 **CloudFile 개체로 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="f59d2-152">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="f59d2-153">이 cmdlet은 이 매개 변수가 지정하는 파일을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f59d2-153">This cmdlet gets the file that this parameter specifies.</span></span>
<span data-ttu-id="f59d2-154">**CloudFile** 개체를 얻은 경우 Get-AzStorageFile cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="f59d2-154">To obtain a **CloudFile** object, use the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: File
Aliases: CloudFile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f59d2-155">-Force</span><span class="sxs-lookup"><span data-stu-id="f59d2-155">-Force</span></span>
<span data-ttu-id="f59d2-156">존재하지 않는 파일의 경로를 지정하는 경우 이 cmdlet은 해당 파일을 만들고 내용을 새 파일에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="f59d2-156">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="f59d2-157">이미 존재하는 파일의 경로를 지정하고 *Force* 매개 변수를 지정하면 cmdlet이 파일을 덮어 써 놨습니다.</span><span class="sxs-lookup"><span data-stu-id="f59d2-157">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="f59d2-158">기존 파일의 경로를 지정하고 *Force를* 지정하지 않으면 cmdlet이 계속되기 전에 메시지를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="f59d2-158">If you specify a path of an existing file and you do not specify *Force*, the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="f59d2-159">폴더의 경로를 지정하는 경우 이 cmdlet은 Azure Storage 파일의 이름이 있는 파일을 만들기 위해 시도합니다.</span><span class="sxs-lookup"><span data-stu-id="f59d2-159">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="f59d2-160">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f59d2-160">-PassThru</span></span>
<span data-ttu-id="f59d2-161">이 cmdlet은 **다운로드하는 AzureStorageFile** 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f59d2-161">Indicates that this cmdlet returns the **AzureStorageFile** object that it downloads.</span></span>

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

### <span data-ttu-id="f59d2-162">-Path</span><span class="sxs-lookup"><span data-stu-id="f59d2-162">-Path</span></span>
<span data-ttu-id="f59d2-163">파일의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f59d2-163">Specifies the path of a file.</span></span>
<span data-ttu-id="f59d2-164">이 cmdlet은 이 매개 변수가 지정하는 파일을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="f59d2-164">This cmdlet gets the contents the file that this parameter specifies.</span></span>
<span data-ttu-id="f59d2-165">파일이 없는 경우 이 cmdlet은 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f59d2-165">If the file does not exist, this cmdlet returns an error.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, Share, Directory
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f59d2-166">-PreserveSMBAttribute</span><span class="sxs-lookup"><span data-stu-id="f59d2-166">-PreserveSMBAttribute</span></span>
<span data-ttu-id="f59d2-167">원본 파일 SMB 속성(File Attributtes, 파일 만들기 시간, 파일 마지막 쓰기 시간)을 대상 파일에 보관합니다.</span><span class="sxs-lookup"><span data-stu-id="f59d2-167">Keep the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in destination File.</span></span> <span data-ttu-id="f59d2-168">이 매개 변수는 Windows에서만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f59d2-168">This parameter is only available on Windows.</span></span>

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

### <span data-ttu-id="f59d2-169">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f59d2-169">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="f59d2-170">요청에 대해 서비스 쪽 시간 시간 간격(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f59d2-170">Specifies the service side time-out interval, in seconds, for a request.</span></span> <span data-ttu-id="f59d2-171">서비스가 요청을 처리하기 전에 지정된 간격이 경과하면 저장소 서비스가 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f59d2-171">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="f59d2-172">-Share</span><span class="sxs-lookup"><span data-stu-id="f59d2-172">-Share</span></span>
<span data-ttu-id="f59d2-173">**CloudFileShare 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="f59d2-173">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="f59d2-174">이 cmdlet은 이 매개 변수가 지정하는 공유에서 파일의 내용을 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="f59d2-174">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>
<span data-ttu-id="f59d2-175">**CloudFileShare** 개체를 얻은 경우 Get-AzStorageShare cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="f59d2-175">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="f59d2-176">이 개체에는 저장소 컨텍스트가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f59d2-176">This object contains the storage context.</span></span>
<span data-ttu-id="f59d2-177">이 매개 변수를 지정하는 경우 Context 매개 변수를 *지정하지* 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f59d2-177">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases: CloudFileShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f59d2-178">-ShareName</span><span class="sxs-lookup"><span data-stu-id="f59d2-178">-ShareName</span></span>
<span data-ttu-id="f59d2-179">파일 공유의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f59d2-179">Specifies the name of the file share.</span></span>
<span data-ttu-id="f59d2-180">이 cmdlet은 이 매개 변수가 지정하는 공유에서 파일의 내용을 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="f59d2-180">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f59d2-181">-확인</span><span class="sxs-lookup"><span data-stu-id="f59d2-181">-Confirm</span></span>
<span data-ttu-id="f59d2-182">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f59d2-182">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f59d2-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f59d2-183">-WhatIf</span></span>
<span data-ttu-id="f59d2-184">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="f59d2-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f59d2-185">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f59d2-185">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f59d2-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f59d2-186">CommonParameters</span></span>
<span data-ttu-id="f59d2-187">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f59d2-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f59d2-188">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f59d2-188">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f59d2-189">입력</span><span class="sxs-lookup"><span data-stu-id="f59d2-189">INPUTS</span></span>

### <span data-ttu-id="f59d2-190">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="f59d2-190">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="f59d2-191">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="f59d2-191">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="f59d2-192">Microsoft.Azure.Storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="f59d2-192">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="f59d2-193">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f59d2-193">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f59d2-194">출력</span><span class="sxs-lookup"><span data-stu-id="f59d2-194">OUTPUTS</span></span>

### <span data-ttu-id="f59d2-195">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="f59d2-195">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="f59d2-196">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f59d2-196">NOTES</span></span>

## <span data-ttu-id="f59d2-197">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f59d2-197">RELATED LINKS</span></span>

[<span data-ttu-id="f59d2-198">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="f59d2-198">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="f59d2-199">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="f59d2-199">Set-AzStorageFileContent</span></span>](./Set-AzStorageFileContent.md)


