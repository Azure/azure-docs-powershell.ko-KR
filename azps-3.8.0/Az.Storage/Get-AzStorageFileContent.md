---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6420CBE1-BF9D-493D-BCA8-E8C6688FAF3B
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileContent.md
ms.openlocfilehash: 986b882e867051f1736b47da1cc89960cc89492c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034688"
---
# <span data-ttu-id="ba5f1-101">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ba5f1-101">Get-AzStorageFileContent</span></span>

## <span data-ttu-id="ba5f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba5f1-102">SYNOPSIS</span></span>
<span data-ttu-id="ba5f1-103">파일의 내용을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-103">Downloads the contents of a file.</span></span>

## <span data-ttu-id="ba5f1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ba5f1-104">SYNTAX</span></span>

### <span data-ttu-id="ba5f1-105">ShareName (기본값)</span><span class="sxs-lookup"><span data-stu-id="ba5f1-105">ShareName (Default)</span></span>
```
Get-AzStorageFileContent [-ShareName] <String> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="ba5f1-106">공유</span><span class="sxs-lookup"><span data-stu-id="ba5f1-106">Share</span></span>
```
Get-AzStorageFileContent [-Share] <CloudFileShare> [-Path] <String> [[-Destination] <String>] [-CheckMd5]
 [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="ba5f1-107">디렉토리로</span><span class="sxs-lookup"><span data-stu-id="ba5f1-107">Directory</span></span>
```
Get-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Path] <String> [[-Destination] <String>]
 [-CheckMd5] [-PassThru] [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="ba5f1-108">파일</span><span class="sxs-lookup"><span data-stu-id="ba5f1-108">File</span></span>
```
Get-AzStorageFileContent [-File] <CloudFile> [[-Destination] <String>] [-CheckMd5] [-PassThru] [-Force]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

## <span data-ttu-id="ba5f1-109">설명은</span><span class="sxs-lookup"><span data-stu-id="ba5f1-109">DESCRIPTION</span></span>
<span data-ttu-id="ba5f1-110">**AzStorageFileContent** cmdlet은 파일의 콘텐츠를 다운로드 한 다음 지정 된 대상에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-110">The **Get-AzStorageFileContent** cmdlet downloads the contents of a file, and then saves it to a destination that you specify.</span></span>
<span data-ttu-id="ba5f1-111">이 cmdlet은 파일의 내용을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-111">This cmdlet does not return the contents of the file.</span></span>

## <span data-ttu-id="ba5f1-112">예제의</span><span class="sxs-lookup"><span data-stu-id="ba5f1-112">EXAMPLES</span></span>

### <span data-ttu-id="ba5f1-113">예제 1: 폴더에서 파일 다운로드</span><span class="sxs-lookup"><span data-stu-id="ba5f1-113">Example 1: Download a file from a folder</span></span>
```
PS C:\>Get-AzStorageFileContent -ShareName "ContosoShare06" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="ba5f1-114">이 명령은 파일 공유 ContosoShare06에서 현재 폴더로 ContosoWorkingFolder 폴더의 CurrentDataFile 파일을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-114">This command downloads a file that is named CurrentDataFile in the folder ContosoWorkingFolder from the file share ContosoShare06 to current folder.</span></span>

### <span data-ttu-id="ba5f1-115">예제 2: 샘플 파일 공유 아래에서 파일을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-115">Example 2: Downloads the files under sample file share</span></span>
```
PS C:\>Get-AzStorageFile -ShareName sample | ? {$_.GetType().Name -eq "CloudFile"} | Get-AzStorageFileContent
```

<span data-ttu-id="ba5f1-116">이 예제에서는 예제 파일 공유 아래에 있는 파일을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-116">This example downloads the files under sample file share</span></span>

### <span data-ttu-id="ba5f1-117">예제 3: 로컬 파일에 Azure 파일을 다운로드 하 고, 로컬 파일에서 Azure 파일 SMB 속성 (파일 특성 기술 전달자, 파일 만든 시간, 파일 마지막 쓰기 시간)을 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-117">Example 3: Download an Azure file to a local file, and perserve the Azure File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the local file.</span></span>
```
PS C:\>Get-AzStorageFileContent -ShareName sample -Path "dir1/file1" -Destination $localFilePath -PreserveSMBAttribute
```

<span data-ttu-id="ba5f1-118">이 예제에서는 Azure 파일을 로컬 파일에 다운로드 하 고, 로컬 파일에서 Azure 파일 SMB 속성 (파일 특성 기술 전달자, 파일 만든 시간, 파일 마지막 쓰기 시간)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-118">This example downloads an Azure file to a local file, and perserves the Azure File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the local file.</span></span>

## <span data-ttu-id="ba5f1-119">변수</span><span class="sxs-lookup"><span data-stu-id="ba5f1-119">PARAMETERS</span></span>

### <span data-ttu-id="ba5f1-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ba5f1-120">-AsJob</span></span>
<span data-ttu-id="ba5f1-121">백그라운드에서 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-121">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="ba5f1-122">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="ba5f1-122">-CheckMd5</span></span>
<span data-ttu-id="ba5f1-123">다운로드 한 파일에 대 한 Md5 합계를 확인할 지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-123">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

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

### <span data-ttu-id="ba5f1-124">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ba5f1-124">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="ba5f1-125">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-125">Specifies the client-side time-out interval, in seconds, for one service request.</span></span> <span data-ttu-id="ba5f1-126">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-126">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span> <span data-ttu-id="ba5f1-127">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-127">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="ba5f1-128">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="ba5f1-128">-ConcurrentTaskCount</span></span>
<span data-ttu-id="ba5f1-129">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-129">Specifies the maximum concurrent network calls.</span></span> <span data-ttu-id="ba5f1-130">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-130">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span> <span data-ttu-id="ba5f1-131">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-131">The specified value is an absolute count and is not multiplied by the core count.</span></span> <span data-ttu-id="ba5f1-132">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-132">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span> <span data-ttu-id="ba5f1-133">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-133">The default value is 10.</span></span>

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

### <span data-ttu-id="ba5f1-134">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="ba5f1-134">-Context</span></span>
<span data-ttu-id="ba5f1-135">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-135">Specifies an Azure Storage context.</span></span> <span data-ttu-id="ba5f1-136">컨텍스트를 가져오려면 New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-136">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ba5f1-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba5f1-137">-DefaultProfile</span></span>
<span data-ttu-id="ba5f1-138">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-138">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba5f1-139">-대상</span><span class="sxs-lookup"><span data-stu-id="ba5f1-139">-Destination</span></span>
<span data-ttu-id="ba5f1-140">대상 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-140">Specifies the destination path.</span></span>
<span data-ttu-id="ba5f1-141">이 cmdlet은이 매개 변수에서 지정 하는 위치에 파일 콘텐츠를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-141">This cmdlet downloads the file contents to the location that this parameter specifies.</span></span>
<span data-ttu-id="ba5f1-142">존재 하지 않는 파일의 경로를 지정 하면이 cmdlet이 해당 파일을 만들고 새 파일에 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-142">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="ba5f1-143">이미 존재 하는 파일의 경로를 지정 하 고 *Force* 매개 변수를 지정 하면 cmdlet이 파일을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-143">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="ba5f1-144">기존 파일의 경로를 지정 하 고 *Force* 를 지정 하지 않으면 계속 하기 전에 cmdlet에서 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-144">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="ba5f1-145">폴더의 경로를 지정 하는 경우이 cmdlet은 Azure 저장소 파일의 이름을 가진 파일을 만들려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-145">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="ba5f1-146">-디렉터리</span><span class="sxs-lookup"><span data-stu-id="ba5f1-146">-Directory</span></span>
<span data-ttu-id="ba5f1-147">폴더를 **Cloudfiledirectory** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-147">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="ba5f1-148">이 cmdlet은이 매개 변수에서 지정 하는 폴더의 파일에 대 한 콘텐츠를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-148">This cmdlet gets content for a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="ba5f1-149">디렉터리를 가져오려면 New-AzStorageDirectory cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-149">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="ba5f1-150">또한 Get-AzStorageFile cmdlet을 사용 하 여 디렉터리를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-150">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: Directory
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba5f1-151">-파일</span><span class="sxs-lookup"><span data-stu-id="ba5f1-151">-File</span></span>
<span data-ttu-id="ba5f1-152">파일을 **cloudfile** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-152">Specifies a file as a **CloudFile** object.</span></span>
<span data-ttu-id="ba5f1-153">이 cmdlet은이 매개 변수에서 지정 하는 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-153">This cmdlet gets the file that this parameter specifies.</span></span>
<span data-ttu-id="ba5f1-154">**Cloudfile** 개체를 얻으려면 Get-AzStorageFile cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-154">To obtain a **CloudFile** object, use the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: File
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba5f1-155">-Force</span><span class="sxs-lookup"><span data-stu-id="ba5f1-155">-Force</span></span>
<span data-ttu-id="ba5f1-156">존재 하지 않는 파일의 경로를 지정 하면이 cmdlet이 해당 파일을 만들고 새 파일에 내용을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-156">If you specify the path of a file that does not exist, this cmdlet creates that file, and saves the contents in the new file.</span></span>
<span data-ttu-id="ba5f1-157">이미 존재 하는 파일의 경로를 지정 하 고 *Force* 매개 변수를 지정 하면 cmdlet이 파일을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-157">If you specify a path of a file that already exists and you specify the *Force* parameter, the cmdlet overwrites the file.</span></span>
<span data-ttu-id="ba5f1-158">기존 파일의 경로를 지정 하 고 *Force* 를 지정 하지 않으면 계속 하기 전에 cmdlet에서 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-158">If you specify a path of an existing file and you do not specify *Force* , the cmdlet prompts you before it continues.</span></span>
<span data-ttu-id="ba5f1-159">폴더의 경로를 지정 하는 경우이 cmdlet은 Azure 저장소 파일의 이름을 가진 파일을 만들려고 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-159">If you specify the path of a folder, this cmdlet attempts to create a file that has the name of the Azure storage file.</span></span>

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

### <span data-ttu-id="ba5f1-160">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ba5f1-160">-PassThru</span></span>
<span data-ttu-id="ba5f1-161">이 cmdlet이 다운로드 하는 **AzureStorageFile** 개체를 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-161">Indicates that this cmdlet returns the **AzureStorageFile** object that it downloads.</span></span>

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

### <span data-ttu-id="ba5f1-162">-Path</span><span class="sxs-lookup"><span data-stu-id="ba5f1-162">-Path</span></span>
<span data-ttu-id="ba5f1-163">파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-163">Specifies the path of a file.</span></span>
<span data-ttu-id="ba5f1-164">이 cmdlet은이 매개 변수에서 지정 하는 파일의 콘텐츠를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-164">This cmdlet gets the contents the file that this parameter specifies.</span></span>
<span data-ttu-id="ba5f1-165">파일이 없는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-165">If the file does not exist, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="ba5f1-166">-PreserveSMBAttribute</span><span class="sxs-lookup"><span data-stu-id="ba5f1-166">-PreserveSMBAttribute</span></span>
<span data-ttu-id="ba5f1-167">원본 파일의 SMB 속성 (파일 특성 기술 전달자, 파일 생성 시간, 파일의 마지막 쓰기 시간)을 대상 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-167">Keep the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in destination File.</span></span> <span data-ttu-id="ba5f1-168">이 매개 변수는 Windows 에서만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-168">This parameter is only available on Windows.</span></span>

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

### <span data-ttu-id="ba5f1-169">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ba5f1-169">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="ba5f1-170">요청에 대 한 서비스 측 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-170">Specifies the service side time-out interval, in seconds, for a request.</span></span> <span data-ttu-id="ba5f1-171">서비스가 요청을 처리 하기 전에 지정 된 간격이 경과 하면 저장소 서비스에서 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-171">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="ba5f1-172">-공유</span><span class="sxs-lookup"><span data-stu-id="ba5f1-172">-Share</span></span>
<span data-ttu-id="ba5f1-173">**Cloudfileshare** 되지 않는 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-173">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="ba5f1-174">이 cmdlet은이 매개 변수에서 지정 하는 공유에서 파일의 콘텐츠를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-174">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>
<span data-ttu-id="ba5f1-175">**Cloudfileshare** 되지 않는 개체를 가져오려면 Get-AzStorageShare cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-175">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="ba5f1-176">이 개체는 저장소 컨텍스트를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-176">This object contains the storage context.</span></span>
<span data-ttu-id="ba5f1-177">이 매개 변수를 지정 하는 경우 *컨텍스트* 매개 변수를 지정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-177">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: Share
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba5f1-178">-ShareName</span><span class="sxs-lookup"><span data-stu-id="ba5f1-178">-ShareName</span></span>
<span data-ttu-id="ba5f1-179">파일 공유의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-179">Specifies the name of the file share.</span></span>
<span data-ttu-id="ba5f1-180">이 cmdlet은이 매개 변수에서 지정 하는 공유에서 파일의 콘텐츠를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-180">This cmdlet downloads the contents of the file in the share this parameter specifies.</span></span>

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

### <span data-ttu-id="ba5f1-181">-확인</span><span class="sxs-lookup"><span data-stu-id="ba5f1-181">-Confirm</span></span>
<span data-ttu-id="ba5f1-182">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-182">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba5f1-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba5f1-183">-WhatIf</span></span>
<span data-ttu-id="ba5f1-184">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba5f1-185">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-185">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba5f1-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba5f1-186">CommonParameters</span></span>
<span data-ttu-id="ba5f1-187">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ba5f1-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba5f1-188">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ba5f1-188">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba5f1-189">입력</span><span class="sxs-lookup"><span data-stu-id="ba5f1-189">INPUTS</span></span>

### <span data-ttu-id="ba5f1-190">Microsoft. c m m. c a c 파일 공유</span><span class="sxs-lookup"><span data-stu-id="ba5f1-190">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="ba5f1-191">Microsoft. c l i 파일 디렉터리</span><span class="sxs-lookup"><span data-stu-id="ba5f1-191">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="ba5f1-192">Microsoft. c c. | 파일</span><span class="sxs-lookup"><span data-stu-id="ba5f1-192">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="ba5f1-193">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ba5f1-193">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ba5f1-194">출력</span><span class="sxs-lookup"><span data-stu-id="ba5f1-194">OUTPUTS</span></span>

### <span data-ttu-id="ba5f1-195">Microsoft. c c. | 파일</span><span class="sxs-lookup"><span data-stu-id="ba5f1-195">Microsoft.Azure.Storage.File.CloudFile</span></span>

## <span data-ttu-id="ba5f1-196">상속자</span><span class="sxs-lookup"><span data-stu-id="ba5f1-196">NOTES</span></span>

## <span data-ttu-id="ba5f1-197">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ba5f1-197">RELATED LINKS</span></span>

[<span data-ttu-id="ba5f1-198">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="ba5f1-198">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="ba5f1-199">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ba5f1-199">Set-AzStorageFileContent</span></span>](./Set-AzStorageFileContent.md)


