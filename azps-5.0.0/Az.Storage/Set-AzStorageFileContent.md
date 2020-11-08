---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FA98E64B-D589-4653-9ACC-86573FAF4550
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageFileContent.md
ms.openlocfilehash: 3fed30a260532378274e2df815d6e4b252c018f6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215765"
---
# <span data-ttu-id="6ea12-101">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="6ea12-101">Set-AzStorageFileContent</span></span>

## <span data-ttu-id="6ea12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ea12-102">SYNOPSIS</span></span>
<span data-ttu-id="6ea12-103">파일의 내용을 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ea12-103">Uploads the contents of a file.</span></span>

## <span data-ttu-id="6ea12-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6ea12-104">SYNTAX</span></span>

### <span data-ttu-id="6ea12-105">ShareName (기본값)</span><span class="sxs-lookup"><span data-stu-id="6ea12-105">ShareName (Default)</span></span>
```
Set-AzStorageFileContent [-ShareName] <String> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="6ea12-106">공유</span><span class="sxs-lookup"><span data-stu-id="6ea12-106">Share</span></span>
```
Set-AzStorageFileContent [-Share] <CloudFileShare> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="6ea12-107">디렉토리로</span><span class="sxs-lookup"><span data-stu-id="6ea12-107">Directory</span></span>
```
Set-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

## <span data-ttu-id="6ea12-108">설명은</span><span class="sxs-lookup"><span data-stu-id="6ea12-108">DESCRIPTION</span></span>
<span data-ttu-id="6ea12-109">**AzStorageFileContent** cmdlet은 지정 된 공유에서 파일의 콘텐츠를 파일에 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ea12-109">The **Set-AzStorageFileContent** cmdlet uploads the contents of a file to a file on a specified share.</span></span>

## <span data-ttu-id="6ea12-110">예제의</span><span class="sxs-lookup"><span data-stu-id="6ea12-110">EXAMPLES</span></span>

### <span data-ttu-id="6ea12-111">예제 1: 현재 폴더에 파일 업로드</span><span class="sxs-lookup"><span data-stu-id="6ea12-111">Example 1: Upload a file in the current folder</span></span>
```
PS C:\>Set-AzStorageFileContent -ShareName "ContosoShare06" -Source "DataFile37" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="6ea12-112">이 명령은 현재 폴더에 DataFile37 이라는 파일을 ContosoWorkingFolder 이라는 폴더에 있는 CurrentDataFile 파일 이라는 파일로 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ea12-112">This command uploads a file that is named DataFile37 in the current folder as a file that is named CurrentDataFile in the folder named ContosoWorkingFolder.</span></span>

### <span data-ttu-id="6ea12-113">예제 2: 현재 폴더의 모든 파일 업로드</span><span class="sxs-lookup"><span data-stu-id="6ea12-113">Example 2: Upload all the files in the current folder</span></span>
```
PS C:\>$CurrentFolder = (Get-Item .).FullName
PS C:\> $Container = Get-AzStorageShare -Name "ContosoShare06"
PS C:\> Get-ChildItem -Recurse | Where-Object { $_.GetType().Name -eq "FileInfo"} | ForEach-Object {
    $path=$_.FullName.Substring($Currentfolder.Length+1).Replace("\","/")
    Set-AzStorageFileContent -Share $Container -Source $_.FullName -Path $path -Force
}
```

<span data-ttu-id="6ea12-114">이 예제에서는 여러 가지 일반적인 Windows PowerShell cmdlet 및 현재 cmdlet을 사용 하 여 현재 폴더의 모든 파일을 컨테이너 ContosoShare06의 루트 폴더에 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ea12-114">This example uses several common Windows PowerShell cmdlets and the current cmdlet to upload all files from the current folder to the root folder of container ContosoShare06.</span></span>
<span data-ttu-id="6ea12-115">첫 번째 명령은 현재 폴더의 이름을 가져와 $CurrentFolder 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ea12-115">The first command gets the name of the current folder and stores it in the $CurrentFolder variable.</span></span>
<span data-ttu-id="6ea12-116">두 번째 명령은 **AzStorageShare** cmdlet을 사용 하 여 ContosoShare06 이라는 이름의 파일 공유를 가져오고이를 $Container 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ea12-116">The second command uses the **Get-AzStorageShare** cmdlet to get the file share named ContosoShare06, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="6ea12-117">마지막 명령은 파이프라인 연산자를 사용 하 여 현재 폴더의 콘텐츠를 가져와 각 항목을 Where-Object cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ea12-117">The final command gets the contents of the current folder and passes each one to the Where-Object cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6ea12-118">해당 cmdlet은 파일이 아닌 개체를 필터링 한 다음 파일을 ForEach-Object cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ea12-118">That cmdlet filters out objects that are not files, and then passes the files to the ForEach-Object cmdlet.</span></span>
<span data-ttu-id="6ea12-119">해당 cmdlet은 해당 경로를 만드는 각 파일에 대해 스크립트 블록을 실행 한 다음 현재 cmdlet을 사용 하 여 파일을 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ea12-119">That cmdlet runs a script block for each file that creates the appropriate path for it and then uses the current cmdlet to upload the file.</span></span>
<span data-ttu-id="6ea12-120">결과는이 예제에서 업로드 하는 다른 파일과 관련 하 여 동일한 이름과 상대 위치를 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="6ea12-120">The result has the same name and same relative position with regard to the other files that this example uploads.</span></span>
<span data-ttu-id="6ea12-121">스크립트 블록에 대 한 자세한 내용을 보려면을 입력 `Get-Help about_Script_Blocks` 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ea12-121">For more information about script blocks, type `Get-Help about_Script_Blocks`.</span></span>

### <span data-ttu-id="6ea12-122">예제 3: Azure 파일에 로컬 파일을 업로드 하 고 Azure 파일의 로컬 파일 SMB 속성 (파일 특성 기술 전달자, 파일 만든 시간, 파일의 마지막 쓰기 시간)을 처리 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ea12-122">Example 3: Upload a local file to an Azure file, and perserve the local File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the Azure file.</span></span>
```
PS C:\>Get-AzStorageFileContent -source $localFilePath -ShareName sample -Path "dir1/file1" -PreserveSMBAttribute
```

<span data-ttu-id="6ea12-123">이 예제에서는 azure 파일에 로컬 파일을 업로드 하 고 Azure 파일의 로컬 파일 SMB 속성 (파일 특성 기술 전달자, 파일 생성 시간, 파일 마지막 쓰기 시간)을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ea12-123">This example uploads a local file to an Azure file, and perserves the local File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the Azure file.</span></span>

## <span data-ttu-id="6ea12-124">변수</span><span class="sxs-lookup"><span data-stu-id="6ea12-124">PARAMETERS</span></span>

### <span data-ttu-id="6ea12-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6ea12-125">-AsJob</span></span>
<span data-ttu-id="6ea12-126">백그라운드에서 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ea12-126">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="6ea12-127">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6ea12-127">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="6ea12-128">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ea12-128">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="6ea12-129">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ea12-129">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="6ea12-130">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ea12-130">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="6ea12-131">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="6ea12-131">-ConcurrentTaskCount</span></span>
<span data-ttu-id="6ea12-132">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ea12-132">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="6ea12-133">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6ea12-133">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="6ea12-134">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="6ea12-134">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="6ea12-135">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6ea12-135">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="6ea12-136">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="6ea12-136">The default value is 10.</span></span>

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

### <span data-ttu-id="6ea12-137">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="6ea12-137">-Context</span></span>
<span data-ttu-id="6ea12-138">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ea12-138">Specifies an Azure storage context.</span></span>
<span data-ttu-id="6ea12-139">저장소 컨텍스트를 얻으려면 [New AzStorageContext](./New-AzStorageContext.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ea12-139">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="6ea12-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ea12-140">-DefaultProfile</span></span>
<span data-ttu-id="6ea12-141">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6ea12-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ea12-142">-디렉터리</span><span class="sxs-lookup"><span data-stu-id="6ea12-142">-Directory</span></span>
<span data-ttu-id="6ea12-143">폴더를 **Cloudfiledirectory** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ea12-143">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="6ea12-144">이 cmdlet은이 매개 변수에서 지정 하는 폴더에 파일을 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ea12-144">This cmdlet uploads the file to the folder that this parameter specifies.</span></span>
<span data-ttu-id="6ea12-145">디렉터리를 가져오려면 New-AzStorageDirectory cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ea12-145">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="6ea12-146">또한 Get-AzStorageFile cmdlet을 사용 하 여 디렉터리를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6ea12-146">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="6ea12-147">-Force</span><span class="sxs-lookup"><span data-stu-id="6ea12-147">-Force</span></span>
<span data-ttu-id="6ea12-148">이 cmdlet이 기존 Azure 저장소 파일을 덮어쓴다는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6ea12-148">Indicates that this cmdlet overwrites an existing Azure storage file.</span></span>

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

### <span data-ttu-id="6ea12-149">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6ea12-149">-PassThru</span></span>
<span data-ttu-id="6ea12-150">이 cmdlet이 생성 또는 업로드 하는 **AzureStorageFile** 개체를 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6ea12-150">Indicates that this cmdlet returns the **AzureStorageFile** object that it creates or uploads.</span></span>

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

### <span data-ttu-id="6ea12-151">-Path</span><span class="sxs-lookup"><span data-stu-id="6ea12-151">-Path</span></span>
<span data-ttu-id="6ea12-152">파일 또는 폴더의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ea12-152">Specifies the path of a file or folder.</span></span>
<span data-ttu-id="6ea12-153">이 cmdlet은이 매개 변수에서 지정 하는 파일 또는이 매개 변수에서 지정 하는 폴더의 파일에 콘텐츠를 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ea12-153">This cmdlet uploads contents to the file that this parameter specifies, or to a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="6ea12-154">폴더를 지정 하는 경우이 cmdlet은 원본 파일과 동일한 이름을 가진 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6ea12-154">If you specify a folder, this cmdlet creates a file that has the same name as the source file.</span></span>
<span data-ttu-id="6ea12-155">존재 하지 않는 파일의 경로를 지정 하면이 cmdlet이 해당 파일을 만들고 해당 파일에 콘텐츠를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ea12-155">If you specify a path of a file that does not exist, this cmdlet creates that file and saves the contents to that file.</span></span>
<span data-ttu-id="6ea12-156">이미 존재 하는 파일을 지정 하 고 _Force_ 매개 변수를 지정 하면이 cmdlet이 파일의 내용을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="6ea12-156">If you specify a file that already exists, and you specify the _Force_ parameter, this cmdlet overwrites the contents of the file.</span></span>
<span data-ttu-id="6ea12-157">이미 존재 하 고 _Force_ 를 지정 하지 않은 파일을 지정 하면이 cmdlet은 아무런 변화가 없으며 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ea12-157">If you specify a file that already exists and you do not specify _Force_ , this cmdlet makes no change, and returns an error.</span></span>
<span data-ttu-id="6ea12-158">존재 하지 않는 폴더의 경로를 지정 하면이 cmdlet은 아무런 변화가 없으며 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ea12-158">If you specify a path of a folder that does not exist, this cmdlet makes no change, and returns an error.</span></span>

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

### <span data-ttu-id="6ea12-159">-PreserveSMBAttribute</span><span class="sxs-lookup"><span data-stu-id="6ea12-159">-PreserveSMBAttribute</span></span>
<span data-ttu-id="6ea12-160">원본 파일의 SMB 속성 (파일 특성 기술 전달자, 파일 생성 시간, 파일의 마지막 쓰기 시간)을 대상 파일에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ea12-160">Keep the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in destination File.</span></span> <span data-ttu-id="6ea12-161">이 매개 변수는 Windows 에서만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6ea12-161">This parameter is only available on Windows.</span></span>

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

### <span data-ttu-id="6ea12-162">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6ea12-162">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="6ea12-163">요청에 대 한 서버 부분에 대 한 시간 초과 기간의 길이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ea12-163">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="6ea12-164">-공유</span><span class="sxs-lookup"><span data-stu-id="6ea12-164">-Share</span></span>
<span data-ttu-id="6ea12-165">**Cloudfileshare** 되지 않는 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ea12-165">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="6ea12-166">이 cmdlet은이 매개 변수에서 지정 하는 파일 공유의 파일에 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ea12-166">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>
<span data-ttu-id="6ea12-167">**Cloudfileshare** 되지 않는 개체를 가져오려면 Get-AzStorageShare cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ea12-167">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="6ea12-168">이 개체는 저장소 컨텍스트를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ea12-168">This object contains the storage context.</span></span>
<span data-ttu-id="6ea12-169">이 매개 변수를 지정 하는 경우 *컨텍스트* 매개 변수를 지정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="6ea12-169">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="6ea12-170">-ShareName</span><span class="sxs-lookup"><span data-stu-id="6ea12-170">-ShareName</span></span>
<span data-ttu-id="6ea12-171">파일 공유의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ea12-171">Specifies the name of the file share.</span></span>
<span data-ttu-id="6ea12-172">이 cmdlet은이 매개 변수에서 지정 하는 파일 공유의 파일에 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ea12-172">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>

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

### <span data-ttu-id="6ea12-173">-원본</span><span class="sxs-lookup"><span data-stu-id="6ea12-173">-Source</span></span>
<span data-ttu-id="6ea12-174">이 cmdlet이 업로드 하는 원본 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ea12-174">Specifies the source file that this cmdlet uploads.</span></span>
<span data-ttu-id="6ea12-175">존재 하지 않는 파일을 지정 하면이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ea12-175">If you specify a file that does not exist, this cmdlet returns an error.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: FullName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ea12-176">-확인</span><span class="sxs-lookup"><span data-stu-id="6ea12-176">-Confirm</span></span>
<span data-ttu-id="6ea12-177">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ea12-177">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ea12-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ea12-178">-WhatIf</span></span>
<span data-ttu-id="6ea12-179">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6ea12-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ea12-180">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6ea12-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ea12-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ea12-181">CommonParameters</span></span>
<span data-ttu-id="6ea12-182">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ea12-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ea12-183">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ea12-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ea12-184">입력</span><span class="sxs-lookup"><span data-stu-id="6ea12-184">INPUTS</span></span>

### <span data-ttu-id="6ea12-185">Microsoft. c m m. c a c 파일 공유</span><span class="sxs-lookup"><span data-stu-id="6ea12-185">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="6ea12-186">Microsoft. c l i 파일 디렉터리</span><span class="sxs-lookup"><span data-stu-id="6ea12-186">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="6ea12-187">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6ea12-187">System.String</span></span>

### <span data-ttu-id="6ea12-188">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6ea12-188">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6ea12-189">출력</span><span class="sxs-lookup"><span data-stu-id="6ea12-189">OUTPUTS</span></span>

### <span data-ttu-id="6ea12-190">WindowsAzure. ResourceModel를 AzureStorageFile로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="6ea12-190">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="6ea12-191">상속자</span><span class="sxs-lookup"><span data-stu-id="6ea12-191">NOTES</span></span>

## <span data-ttu-id="6ea12-192">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6ea12-192">RELATED LINKS</span></span>

[<span data-ttu-id="6ea12-193">제거-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="6ea12-193">Remove-AzStorageDirectory</span></span>](./Remove-AzStorageDirectory.md)

[<span data-ttu-id="6ea12-194">새로운 AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="6ea12-194">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)

[<span data-ttu-id="6ea12-195">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="6ea12-195">Get-AzStorageFileContent</span></span>](./Get-AzStorageFileContent.md)
