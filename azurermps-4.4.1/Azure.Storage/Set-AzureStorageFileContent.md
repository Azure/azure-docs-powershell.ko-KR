---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FA98E64B-D589-4653-9ACC-86573FAF4550
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageFileContent.md
gitcommit: https://github.com/Azure/azure-powershell/blob/173e94aec59d7f539b72e43e90e5e7f8ba5f62bc
ms.openlocfilehash: 6f0421c9b442bfc92dc693326542882ba2b0e8d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535576"
---
# <span data-ttu-id="ff9be-101">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ff9be-101">Set-AzureStorageFileContent</span></span>

## <span data-ttu-id="ff9be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff9be-102">SYNOPSIS</span></span>
<span data-ttu-id="ff9be-103">파일의 내용을 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff9be-103">Uploads the contents of a file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff9be-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ff9be-104">SYNTAX</span></span>

### <span data-ttu-id="ff9be-105">ShareName (기본값)</span><span class="sxs-lookup"><span data-stu-id="ff9be-105">ShareName (Default)</span></span>
```
Set-AzureStorageFileContent [-ShareName] <String> [-Source] <String> [[-Path] <String>] [-PassThru] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff9be-106">공유</span><span class="sxs-lookup"><span data-stu-id="ff9be-106">Share</span></span>
```
Set-AzureStorageFileContent [-Share] <CloudFileShare> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff9be-107">디렉토리로</span><span class="sxs-lookup"><span data-stu-id="ff9be-107">Directory</span></span>
```
Set-AzureStorageFileContent [-Directory] <CloudFileDirectory> [-Source] <String> [[-Path] <String>] [-PassThru]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff9be-108">설명은</span><span class="sxs-lookup"><span data-stu-id="ff9be-108">DESCRIPTION</span></span>
<span data-ttu-id="ff9be-109">**AzureStorageFileContent** cmdlet은 지정 된 공유에서 파일의 콘텐츠를 파일에 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff9be-109">The **Set-AzureStorageFileContent** cmdlet uploads the contents of a file to a file on a specified share.</span></span>

## <span data-ttu-id="ff9be-110">예제의</span><span class="sxs-lookup"><span data-stu-id="ff9be-110">EXAMPLES</span></span>

### <span data-ttu-id="ff9be-111">예제 1: 현재 폴더에 파일 업로드</span><span class="sxs-lookup"><span data-stu-id="ff9be-111">Example 1: Upload a file in the current folder</span></span>
```
PS C:\>Set-AzureStorageFileContent -ShareName "ContosoShare06" -Source "DataFile37" -Path "ContosoWorkingFolder/CurrentDataFile"
```

<span data-ttu-id="ff9be-112">이 명령은 현재 폴더에 DataFile37 이라는 파일을 ContosoWorkingFolder 이라는 폴더에 있는 CurrentDataFile 파일 이라는 파일로 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff9be-112">This command uploads a file that is named DataFile37 in the current folder as a file that is named CurrentDataFile in the folder named ContosoWorkingFolder.</span></span>

### <span data-ttu-id="ff9be-113">예제 2: 현재 폴더의 모든 파일 업로드</span><span class="sxs-lookup"><span data-stu-id="ff9be-113">Example 2: Upload all the files in the current folder</span></span>
```
PS C:\>$CurrentFolder = (Get-Item .).FullName
PS C:\> $Container = Get-AzureStorageShare -Name "ContosoShare06"
PS C:\> Get-ChildItem -Recurse | Where-Object { $_.GetType().Name -eq "FileInfo"} | ForEach-Object {
    $path=$_.FullName.Substring($Currentfolder.Length+1).Replace("\","/")
    Set-AzureStorageFileContent -Share $Container -Source $_.FullName -Path $path -Force
}
```

<span data-ttu-id="ff9be-114">이 예제에서는 여러 가지 일반적인 Windows PowerShell cmdlet 및 현재 cmdlet을 사용 하 여 현재 폴더의 모든 파일을 컨테이너 ContosoShare06의 루트 폴더에 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff9be-114">This example uses several common Windows PowerShell cmdlets and the current cmdlet to upload all files from the current folder to the root folder of container ContosoShare06.</span></span>

<span data-ttu-id="ff9be-115">첫 번째 명령은 현재 폴더의 이름을 가져와 $CurrentFolder 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff9be-115">The first command gets the name of the current folder and stores it in the $CurrentFolder variable.</span></span>

<span data-ttu-id="ff9be-116">두 번째 명령은 **AzureStorageShare** cmdlet을 사용 하 여 ContosoShare06 이라는 이름의 파일 공유를 가져오고이를 $Container 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff9be-116">The second command uses the **Get-AzureStorageShare** cmdlet to get the file share named ContosoShare06, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="ff9be-117">마지막 명령은 파이프라인 연산자를 사용 하 여 현재 폴더의 콘텐츠를 가져와 각 항목을 Where-Object cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff9be-117">The final command gets the contents of the current folder and passes each one to the Where-Object cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ff9be-118">해당 cmdlet은 파일이 아닌 개체를 필터링 한 다음 파일을 ForEach-Object cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff9be-118">That cmdlet filters out objects that are not files, and then passes the files to the ForEach-Object cmdlet.</span></span>
<span data-ttu-id="ff9be-119">해당 cmdlet은 해당 경로를 만드는 각 파일에 대해 스크립트 블록을 실행 한 다음 현재 cmdlet을 사용 하 여 파일을 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff9be-119">That cmdlet runs a script block for each file that creates the appropriate path for it and then uses the current cmdlet to upload the file.</span></span>
<span data-ttu-id="ff9be-120">결과는이 예제에서 업로드 하는 다른 파일과 관련 하 여 동일한 이름과 상대 위치를 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="ff9be-120">The result has the same name and same relative position with regard to the other files that this example uploads.</span></span>
<span data-ttu-id="ff9be-121">스크립트 블록에 대 한 자세한 내용을 보려면을 입력 `Get-Help about_Script_Blocks` 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff9be-121">For more information about script blocks, type `Get-Help about_Script_Blocks`.</span></span>

## <span data-ttu-id="ff9be-122">변수</span><span class="sxs-lookup"><span data-stu-id="ff9be-122">PARAMETERS</span></span>

### <span data-ttu-id="ff9be-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ff9be-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="ff9be-124">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff9be-124">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="ff9be-125">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff9be-125">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="ff9be-126">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff9be-126">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff9be-127">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="ff9be-127">-ConcurrentTaskCount</span></span>
<span data-ttu-id="ff9be-128">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff9be-128">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="ff9be-129">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ff9be-129">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="ff9be-130">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="ff9be-130">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="ff9be-131">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ff9be-131">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="ff9be-132">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="ff9be-132">The default value is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff9be-133">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="ff9be-133">-Context</span></span>
<span data-ttu-id="ff9be-134">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff9be-134">Specifies an Azure storage context.</span></span>
<span data-ttu-id="ff9be-135">저장소 컨텍스트를 얻으려면 [새로운-AzureStorageContext](./New-AzureStorageContext.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff9be-135">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ShareName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff9be-136">-디렉터리</span><span class="sxs-lookup"><span data-stu-id="ff9be-136">-Directory</span></span>
<span data-ttu-id="ff9be-137">폴더를 **Cloudfiledirectory** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff9be-137">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="ff9be-138">이 cmdlet은이 매개 변수에서 지정 하는 폴더에 파일을 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff9be-138">This cmdlet uploads the file to the folder that this parameter specifies.</span></span>
<span data-ttu-id="ff9be-139">디렉터리를 가져오려면 New-AzureStorageDirectory cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff9be-139">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="ff9be-140">또한 Get-AzureStorageFile cmdlet을 사용 하 여 디렉터리를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ff9be-140">You can also use the Get-AzureStorageFile cmdlet to obtain a directory.</span></span>

```yaml
Type: CloudFileDirectory
Parameter Sets: Directory
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff9be-141">-Force</span><span class="sxs-lookup"><span data-stu-id="ff9be-141">-Force</span></span>
<span data-ttu-id="ff9be-142">이 cmdlet이 기존 Azure 저장소 파일을 덮어쓴다는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ff9be-142">Indicates that this cmdlet overwrites an existing Azure storage file.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff9be-143">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ff9be-143">-PassThru</span></span>
<span data-ttu-id="ff9be-144">이 cmdlet이 생성 또는 업로드 하는 **AzureStorageFile** 개체를 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ff9be-144">Indicates that this cmdlet returns the **AzureStorageFile** object that it creates or uploads.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff9be-145">-Path</span><span class="sxs-lookup"><span data-stu-id="ff9be-145">-Path</span></span>
<span data-ttu-id="ff9be-146">파일 또는 폴더의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff9be-146">Specifies the path of a file or folder.</span></span>
<span data-ttu-id="ff9be-147">이 cmdlet은이 매개 변수에서 지정 하는 파일 또는이 매개 변수에서 지정 하는 폴더의 파일에 콘텐츠를 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff9be-147">This cmdlet uploads contents to the file that this parameter specifies, or to a file in the folder that this parameter specifies.</span></span>
<span data-ttu-id="ff9be-148">폴더를 지정 하는 경우이 cmdlet은 원본 파일과 동일한 이름을 가진 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ff9be-148">If you specify a folder, this cmdlet creates a file that has the same name as the source file.</span></span>

<span data-ttu-id="ff9be-149">존재 하지 않는 파일의 경로를 지정 하면이 cmdlet이 해당 파일을 만들고 해당 파일에 콘텐츠를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff9be-149">If you specify a path of a file that does not exist, this cmdlet creates that file and saves the contents to that file.</span></span>
<span data-ttu-id="ff9be-150">이미 존재 하는 파일을 지정 하 고 _Force_ 매개 변수를 지정 하면이 cmdlet이 파일의 내용을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="ff9be-150">If you specify a file that already exists, and you specify the _Force_ parameter, this cmdlet overwrites the contents of the file.</span></span>
<span data-ttu-id="ff9be-151">이미 존재 하 고 _Force_ 를 지정 하지 않은 파일을 지정 하면이 cmdlet은 아무런 변화가 없으며 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff9be-151">If you specify a file that already exists and you do not specify _Force_ , this cmdlet makes no change, and returns an error.</span></span>

<span data-ttu-id="ff9be-152">존재 하지 않는 폴더의 경로를 지정 하면이 cmdlet은 아무런 변화가 없으며 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff9be-152">If you specify a path of a folder that does not exist, this cmdlet makes no change, and returns an error.</span></span>


```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff9be-153">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ff9be-153">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="ff9be-154">요청에 대 한 서버 부분에 대 한 시간 초과 기간의 길이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff9be-154">Specifies the length of the time-out period for the server part of a request.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff9be-155">-공유</span><span class="sxs-lookup"><span data-stu-id="ff9be-155">-Share</span></span>
<span data-ttu-id="ff9be-156">**Cloudfileshare** 되지 않는 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff9be-156">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="ff9be-157">이 cmdlet은이 매개 변수에서 지정 하는 파일 공유의 파일에 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff9be-157">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>
<span data-ttu-id="ff9be-158">**Cloudfileshare** 되지 않는 개체를 가져오려면 Get-AzureStorageShare cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff9be-158">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="ff9be-159">이 개체는 저장소 컨텍스트를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff9be-159">This object contains the storage context.</span></span>
<span data-ttu-id="ff9be-160">이 매개 변수를 지정 하는 경우 *컨텍스트* 매개 변수를 지정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="ff9be-160">If you specify this parameter, do not specify the *Context* parameter.</span></span>

```yaml
Type: CloudFileShare
Parameter Sets: Share
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ff9be-161">-ShareName</span><span class="sxs-lookup"><span data-stu-id="ff9be-161">-ShareName</span></span>
<span data-ttu-id="ff9be-162">파일 공유의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff9be-162">Specifies the name of the file share.</span></span>
<span data-ttu-id="ff9be-163">이 cmdlet은이 매개 변수에서 지정 하는 파일 공유의 파일에 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff9be-163">This cmdlet uploads to a file in the file share this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff9be-164">-원본</span><span class="sxs-lookup"><span data-stu-id="ff9be-164">-Source</span></span>
<span data-ttu-id="ff9be-165">이 cmdlet이 업로드 하는 원본 파일을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff9be-165">Specifies the source file that this cmdlet uploads.</span></span>
<span data-ttu-id="ff9be-166">존재 하지 않는 파일을 지정 하면이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff9be-166">If you specify a file that does not exist, this cmdlet returns an error.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: FullName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff9be-167">-확인</span><span class="sxs-lookup"><span data-stu-id="ff9be-167">-Confirm</span></span>
<span data-ttu-id="ff9be-168">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff9be-168">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff9be-169">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff9be-169">-WhatIf</span></span>
<span data-ttu-id="ff9be-170">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ff9be-170">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff9be-171">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ff9be-171">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ff9be-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff9be-172">CommonParameters</span></span>
<span data-ttu-id="ff9be-173">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff9be-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff9be-174">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff9be-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff9be-175">입력</span><span class="sxs-lookup"><span data-stu-id="ff9be-175">INPUTS</span></span>

### <span data-ttu-id="ff9be-176">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ff9be-176">IStorageContext</span></span>

<span data-ttu-id="ff9be-177">' Context ' 매개 변수는 파이프라인에서 ' IStorageContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff9be-177">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="ff9be-178">CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="ff9be-178">CloudFileDirectory</span></span>

<span data-ttu-id="ff9be-179">' Directory ' 매개 변수는 파이프라인에서 ' CloudFileDirectory ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff9be-179">Parameter 'Directory' accepts value of type 'CloudFileDirectory' from the pipeline</span></span>

### <span data-ttu-id="ff9be-180">CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="ff9be-180">CloudFileShare</span></span>

<span data-ttu-id="ff9be-181">' Share ' 매개 변수는 파이프라인에서 ' CloudFileShare 범위 ' 형식의 값을 받아들입니다.</span><span class="sxs-lookup"><span data-stu-id="ff9be-181">Parameter 'Share' accepts value of type 'CloudFileShare' from the pipeline</span></span>

## <span data-ttu-id="ff9be-182">출력</span><span class="sxs-lookup"><span data-stu-id="ff9be-182">OUTPUTS</span></span>

## <span data-ttu-id="ff9be-183">상속자</span><span class="sxs-lookup"><span data-stu-id="ff9be-183">NOTES</span></span>

## <span data-ttu-id="ff9be-184">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ff9be-184">RELATED LINKS</span></span>

[<span data-ttu-id="ff9be-185">-AzureStorageDirectory 제거</span><span class="sxs-lookup"><span data-stu-id="ff9be-185">Remove-AzureStorageDirectory</span></span>](./Remove-AzureStorageDirectory.md)

[<span data-ttu-id="ff9be-186">새-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="ff9be-186">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)

[<span data-ttu-id="ff9be-187">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="ff9be-187">Get-AzureStorageFileContent</span></span>](./Get-AzureStorageFileContent.md)
