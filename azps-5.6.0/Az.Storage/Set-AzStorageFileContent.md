---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FA98E64B-D589-4653-9ACC-86573FAF4550
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azstoragefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageFileContent.md
ms.openlocfilehash: 597728b1b327da28495574ca865a2e75a1a774a3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974160"
---
# <span data-ttu-id="e921a-101">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e921a-101">Set-AzStorageFileContent</span></span>

## <span data-ttu-id="e921a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e921a-102">SYNOPSIS</span></span>
<span data-ttu-id="e921a-103">파일의 내용을 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="e921a-103">Uploads the contents of a file.</span></span>

## <span data-ttu-id="e921a-104">구문</span><span class="sxs-lookup"><span data-stu-id="e921a-104">SYNTAX</span></span>

### <span data-ttu-id="e921a-105">ShareName(기본값)</span><span class="sxs-lookup"><span data-stu-id="e921a-105">ShareName (Default)</span></span>
```
Set-AzStorageFileContent [-ShareName] <String> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="e921a-106">공유</span><span class="sxs-lookup"><span data-stu-id="e921a-106">Share</span></span>
```
Set-AzStorageFileContent [-Share] <CloudFileShare> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

### <span data-ttu-id="e921a-107">디렉터리</span><span class="sxs-lookup"><span data-stu-id="e921a-107">Directory</span></span>
```
Set-AzStorageFileContent [-Directory] <CloudFileDirectory> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-AsJob] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [-PreserveSMBAttribute] [<CommonParameters>]
```

## <span data-ttu-id="e921a-108">설명</span><span class="sxs-lookup"><span data-stu-id="e921a-108">DESCRIPTION</span></span>
<span data-ttu-id="e921a-109">**Set-AzStorageFileContent** cmdlet은 파일의 내용을 지정된 공유의 파일에 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="e921a-109">The **Set-AzStorageFileContent** cmdlet uploads the contents of a file to a file on a specified share.</span></span>

## <span data-ttu-id="e921a-110">예제</span><span class="sxs-lookup"><span data-stu-id="e921a-110">EXAMPLES</span></span>

### <span data-ttu-id="e921a-111">예제 1: 현재 폴더에 파일 업로드</span><span class="sxs-lookup"><span data-stu-id="e921a-111">Example 1: Upload a file in the current folder</span></span>
```
PS C:\>Set-AzStorageFileContent -ShareName "ContosoShare06" -Source "DataFile37" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="e921a-112">이 명령은 현재 폴더에 DataFile37이라는 파일을 ContosoWorkingFolder라는 폴더의 CurrentDataFile이라는 파일로 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="e921a-112">This command uploads a file that is named DataFile37 in the current folder as a file that is named CurrentDataFile in the folder named ContosoWorkingFolder.</span></span>

### <span data-ttu-id="e921a-113">예제 2: 현재 폴더에 있는 모든 파일 업로드</span><span class="sxs-lookup"><span data-stu-id="e921a-113">Example 2: Upload all the files in the current folder</span></span>
```
PS C:\>$CurrentFolder = (Get-Item .).FullName
PS C:\> $Container = Get-AzStorageShare -Name "ContosoShare06"
PS C:\> Get-ChildItem -Recurse | Where-Object { $_.GetType().Name -eq "FileInfo"} | ForEach-Object {
    $path=$_.FullName.Substring($Currentfolder.Length+1).Replace("\","/")
    Set-AzStorageFileContent -Share $Container -Source $_.FullName -Path $path -Force
}
```

<span data-ttu-id="e921a-114">이 예제에서는 여러 Windows PowerShell cmdlet 및 현재 cmdlet을 사용하여 현재 폴더의 모든 파일을 ContosoShare06의 루트 폴더로 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="e921a-114">This example uses several common Windows PowerShell cmdlets and the current cmdlet to upload all files from the current folder to the root folder of container ContosoShare06.</span></span>
<span data-ttu-id="e921a-115">첫 번째 명령은 현재 폴더의 이름을 얻게 하여 $CurrentFolder 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="e921a-115">The first command gets the name of the current folder and stores it in the $CurrentFolder variable.</span></span>
<span data-ttu-id="e921a-116">두 번째 명령은 **Get-AzStorageShare** cmdlet을 사용하여 ContosoShare06이라는 파일 공유를 얻은 다음, $Container 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="e921a-116">The second command uses the **Get-AzStorageShare** cmdlet to get the file share named ContosoShare06, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="e921a-117">최종 명령은 현재 폴더의 내용을 얻게 하여 파이프라인 연산자를 사용하여 각 폴더를 Where-Object cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="e921a-117">The final command gets the contents of the current folder and passes each one to the Where-Object cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="e921a-118">해당 cmdlet은 파일이 아닌 개체를 필터한 다음 파일을 ForEach-Object cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="e921a-118">That cmdlet filters out objects that are not files, and then passes the files to the ForEach-Object cmdlet.</span></span>
<span data-ttu-id="e921a-119">해당 cmdlet은 해당 파일에 대한 적절한 경로를 만든 다음 현재 cmdlet을 사용하여 파일을 업로드하는 각 파일에 대한 스크립트 블록을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e921a-119">That cmdlet runs a script block for each file that creates the appropriate path for it and then uses the current cmdlet to upload the file.</span></span>
<span data-ttu-id="e921a-120">결과는 이 예제에서 업로드하는 다른 파일에 대해 이름과 상대 위치가 동일합니다.</span><span class="sxs-lookup"><span data-stu-id="e921a-120">The result has the same name and same relative position with regard to the other files that this example uploads.</span></span>
<span data-ttu-id="e921a-121">스크립트 블록에 대한 자세한 내용은 `Get-Help about_Script_Blocks` 를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="e921a-121">For more information about script blocks, type `Get-Help about_Script_Blocks`.</span></span>

### <span data-ttu-id="e921a-122">예제 3: Azure 파일에 로컬 파일을 업로드하고 Azure 파일에서 로컬 파일 SMB 속성(파일 속성, 파일 만들기 시간, 파일 마지막 쓰기 시간)을 보존합니다.</span><span class="sxs-lookup"><span data-stu-id="e921a-122">Example 3: Upload a local file to an Azure file, and perserve the local File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the Azure file.</span></span>
```
PS C:\>Get-AzStorageFileContent -source $localFilePath -ShareName sample -Path "dir1/file1" -PreserveSMBAttribute
```

<span data-ttu-id="e921a-123">이 예제에서는 로컬 파일을 Azure 파일에 업로드하고 Azure 파일에서 로컬 파일 SMB 속성(파일 속성, 파일 만들기 시간, 파일 마지막 쓰기 시간)을 보존합니다.</span><span class="sxs-lookup"><span data-stu-id="e921a-123">This example uploads a local file to an Azure file, and perserves the local File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in the Azure file.</span></span>

## <span data-ttu-id="e921a-124">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e921a-124">PARAMETERS</span></span>

### <span data-ttu-id="e921a-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e921a-125">-AsJob</span></span>
<span data-ttu-id="e921a-126">백그라운드에서 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e921a-126">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="e921a-127">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e921a-127">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="e921a-128">하나의 서비스 요청에 대해 클라이언트 쪽 시간 간격(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e921a-128">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="e921a-129">지정된 간격에서 이전 호출이 실패하면 이 cmdlet에서 요청을 다시 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="e921a-129">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="e921a-130">간격이 경과하기 전에 이 cmdlet에서 성공적인 응답을 받지 못하면 이 cmdlet은 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="e921a-130">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="e921a-131">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="e921a-131">-ConcurrentTaskCount</span></span>
<span data-ttu-id="e921a-132">최대 동시 네트워크 호출을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e921a-132">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="e921a-133">이 매개 변수를 사용하여 최대 동시 네트워크 호출 수를 지정하여 로컬 CPU 및 대역폭 사용량을 제한하는 동시성 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e921a-133">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="e921a-134">지정된 값은 절대 개수로 코어 수에 곱하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e921a-134">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="e921a-135">이 매개 변수는 초당 100킬로비트와 같은 대역폭이 낮은 환경에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e921a-135">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="e921a-136">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="e921a-136">The default value is 10.</span></span>

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

### <span data-ttu-id="e921a-137">-Context</span><span class="sxs-lookup"><span data-stu-id="e921a-137">-Context</span></span>
<span data-ttu-id="e921a-138">Azure Storage 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e921a-138">Specifies an Azure storage context.</span></span>
<span data-ttu-id="e921a-139">저장소 컨텍스트를 구하기 위해 [New-AzStorageContext](./New-AzStorageContext.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e921a-139">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="e921a-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e921a-140">-DefaultProfile</span></span>
<span data-ttu-id="e921a-141">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e921a-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e921a-142">-Directory</span><span class="sxs-lookup"><span data-stu-id="e921a-142">-Directory</span></span>
<span data-ttu-id="e921a-143">폴더를 **CloudFileDirectory 개체로 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="e921a-143">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="e921a-144">이 cmdlet은 이 매개 변수가 지정하는 폴더에 파일을 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="e921a-144">This cmdlet uploads the file to the folder that this parameter specifies.</span></span>
<span data-ttu-id="e921a-145">디렉터리를 구하기 위해 New-AzStorageDirectory cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e921a-145">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="e921a-146">또한 Get-AzStorageFile cmdlet을 사용하여 디렉터리를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e921a-146">You can also use the Get-AzStorageFile cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="e921a-147">-Force</span><span class="sxs-lookup"><span data-stu-id="e921a-147">-Force</span></span>
<span data-ttu-id="e921a-148">이 cmdlet이 기존 Azure Storage 파일을 덮어 사용 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e921a-148">Indicates that this cmdlet overwrites an existing Azure storage file.</span></span>

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

### <span data-ttu-id="e921a-149">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e921a-149">-PassThru</span></span>
<span data-ttu-id="e921a-150">이 cmdlet은 만들거나 업로드하는 **AzureStorageFile** 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="e921a-150">Indicates that this cmdlet returns the **AzureStorageFile** object that it creates or uploads.</span></span>

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

### <span data-ttu-id="e921a-151">-Path</span><span class="sxs-lookup"><span data-stu-id="e921a-151">-Path</span></span>
<span data-ttu-id="e921a-152">파일 또는 폴더의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e921a-152">Specifies the path of a file or folder.</span></span>
<span data-ttu-id="e921a-153">이 cmdlet은 이 매개 변수가 지정하는 파일 또는 이 매개 변수가 지정하는 폴더의 파일에 콘텐츠를 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="e921a-153">This cmdlet uploads contents to the file that this parameter specifies, or to a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="e921a-154">폴더를 지정하는 경우 이 cmdlet은 원본 파일과 이름이 같은 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e921a-154">If you specify a folder, this cmdlet creates a file that has the same name as the source file.</span></span>
<span data-ttu-id="e921a-155">존재하지 않는 파일의 경로를 지정하는 경우 이 cmdlet은 해당 파일을 만들고 해당 파일에 콘텐츠를 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="e921a-155">If you specify a path of a file that does not exist, this cmdlet creates that file and saves the contents to that file.</span></span>
<span data-ttu-id="e921a-156">이미 존재하는 파일을 지정하고 _Force_ 매개 변수를 지정하는 경우 이 cmdlet은 파일의 내용을 덮어 써</span><span class="sxs-lookup"><span data-stu-id="e921a-156">If you specify a file that already exists, and you specify the _Force_ parameter, this cmdlet overwrites the contents of the file.</span></span>
<span data-ttu-id="e921a-157">이미 존재하는 파일을 지정하고 _Force를_ 지정하지 않는 경우 이 cmdlet은 변경되지 않습니다. 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="e921a-157">If you specify a file that already exists and you do not specify _Force_, this cmdlet makes no change, and returns an error.</span></span>
<span data-ttu-id="e921a-158">존재하지 않는 폴더의 경로를 지정하는 경우 이 cmdlet은 변경되지 않습니다. 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="e921a-158">If you specify a path of a folder that does not exist, this cmdlet makes no change, and returns an error.</span></span>

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

### <span data-ttu-id="e921a-159">-PreserveSMBAttribute</span><span class="sxs-lookup"><span data-stu-id="e921a-159">-PreserveSMBAttribute</span></span>
<span data-ttu-id="e921a-160">원본 파일 SMB 속성(File Attributtes, 파일 만들기 시간, 파일 마지막 쓰기 시간)을 대상 파일에 보관합니다.</span><span class="sxs-lookup"><span data-stu-id="e921a-160">Keep the source File SMB properties (File Attributtes, File Creation Time, File Last Write Time) in destination File.</span></span> <span data-ttu-id="e921a-161">이 매개 변수는 Windows에서만 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e921a-161">This parameter is only available on Windows.</span></span>

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

### <span data-ttu-id="e921a-162">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="e921a-162">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="e921a-163">요청의 서버 부분에 대한 시간 제한 기간의 길이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e921a-163">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="e921a-164">-Share</span><span class="sxs-lookup"><span data-stu-id="e921a-164">-Share</span></span>
<span data-ttu-id="e921a-165">**CloudFileShare 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="e921a-165">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="e921a-166">이 cmdlet은 이 매개 변수를 지정하여 파일 공유의 파일에 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="e921a-166">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>
<span data-ttu-id="e921a-167">**CloudFileShare** 개체를 얻은 경우 Get-AzStorageShare cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="e921a-167">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="e921a-168">이 개체에는 저장소 컨텍스트가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e921a-168">This object contains the storage context.</span></span>
<span data-ttu-id="e921a-169">이 매개 변수를 지정하는 경우 Context 매개 변수를 *지정하지* 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e921a-169">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="e921a-170">-ShareName</span><span class="sxs-lookup"><span data-stu-id="e921a-170">-ShareName</span></span>
<span data-ttu-id="e921a-171">파일 공유의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e921a-171">Specifies the name of the file share.</span></span>
<span data-ttu-id="e921a-172">이 cmdlet은 이 매개 변수를 지정하여 파일 공유의 파일에 업로드합니다.</span><span class="sxs-lookup"><span data-stu-id="e921a-172">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>

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

### <span data-ttu-id="e921a-173">-Source</span><span class="sxs-lookup"><span data-stu-id="e921a-173">-Source</span></span>
<span data-ttu-id="e921a-174">이 cmdlet이 업로드하는 원본 파일을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e921a-174">Specifies the source file that this cmdlet uploads.</span></span>
<span data-ttu-id="e921a-175">존재하지 않는 파일을 지정하면 이 cmdlet에서 오류가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="e921a-175">If you specify a file that does not exist, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="e921a-176">-확인</span><span class="sxs-lookup"><span data-stu-id="e921a-176">-Confirm</span></span>
<span data-ttu-id="e921a-177">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e921a-177">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e921a-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e921a-178">-WhatIf</span></span>
<span data-ttu-id="e921a-179">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e921a-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e921a-180">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e921a-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e921a-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e921a-181">CommonParameters</span></span>
<span data-ttu-id="e921a-182">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e921a-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e921a-183">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e921a-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e921a-184">입력</span><span class="sxs-lookup"><span data-stu-id="e921a-184">INPUTS</span></span>

### <span data-ttu-id="e921a-185">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="e921a-185">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="e921a-186">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="e921a-186">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="e921a-187">System.String</span><span class="sxs-lookup"><span data-stu-id="e921a-187">System.String</span></span>

### <span data-ttu-id="e921a-188">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="e921a-188">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="e921a-189">출력</span><span class="sxs-lookup"><span data-stu-id="e921a-189">OUTPUTS</span></span>

### <span data-ttu-id="e921a-190">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="e921a-190">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="e921a-191">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e921a-191">NOTES</span></span>

## <span data-ttu-id="e921a-192">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e921a-192">RELATED LINKS</span></span>

[<span data-ttu-id="e921a-193">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="e921a-193">Remove-AzStorageDirectory</span></span>](./Remove-AzStorageDirectory.md)

[<span data-ttu-id="e921a-194">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="e921a-194">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)

[<span data-ttu-id="e921a-195">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="e921a-195">Get-AzStorageFileContent</span></span>](./Get-AzStorageFileContent.md)
