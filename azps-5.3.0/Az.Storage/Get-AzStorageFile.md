---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 38207027-FD76-45EE-8817-88599735C0B0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFile.md
ms.openlocfilehash: 8251c18acad2da881c3215df6a2e743b6804af6e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489295"
---
# <span data-ttu-id="62b6d-101">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="62b6d-101">Get-AzStorageFile</span></span>

## <span data-ttu-id="62b6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62b6d-102">SYNOPSIS</span></span>
<span data-ttu-id="62b6d-103">경로에 대한 폴더 및 파일을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="62b6d-103">Lists directories and files for a path.</span></span>

## <span data-ttu-id="62b6d-104">구문</span><span class="sxs-lookup"><span data-stu-id="62b6d-104">SYNTAX</span></span>

### <span data-ttu-id="62b6d-105">ShareName(기본값)</span><span class="sxs-lookup"><span data-stu-id="62b6d-105">ShareName (Default)</span></span>
```
Get-AzStorageFile [-ShareName] <String> [[-Path] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="62b6d-106">공유</span><span class="sxs-lookup"><span data-stu-id="62b6d-106">Share</span></span>
```
Get-AzStorageFile [-Share] <CloudFileShare> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="62b6d-107">디렉터리</span><span class="sxs-lookup"><span data-stu-id="62b6d-107">Directory</span></span>
```
Get-AzStorageFile [-Directory] <CloudFileDirectory> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="62b6d-108">설명</span><span class="sxs-lookup"><span data-stu-id="62b6d-108">DESCRIPTION</span></span>
<span data-ttu-id="62b6d-109">**Get-AzStorageFile** cmdlet은 사용자가 지정한 공유 또는 디렉터리에 대한 디렉터리 및 파일을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="62b6d-109">The **Get-AzStorageFile** cmdlet lists directories and files for the share or directory that you specify.</span></span>
<span data-ttu-id="62b6d-110">경로 매개 *변수를 지정하여* 지정된 경로에서 디렉터리 또는 파일의 인스턴스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="62b6d-110">Specify the *Path* parameter to get an instance of a directory or file in the specified path.</span></span>
<span data-ttu-id="62b6d-111">이 cmdlet은 **AzureStorageFile** 및 **AzureStorageDirectory 개체를 반환합니다.**</span><span class="sxs-lookup"><span data-stu-id="62b6d-111">This cmdlet returns **AzureStorageFile** and **AzureStorageDirectory** objects.</span></span>
<span data-ttu-id="62b6d-112">**IsDirectory** 속성을 사용하여 폴더와 파일을 구분할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="62b6d-112">You can use the **IsDirectory** property to distinguish between folders and files.</span></span>

## <span data-ttu-id="62b6d-113">예제</span><span class="sxs-lookup"><span data-stu-id="62b6d-113">EXAMPLES</span></span>

### <span data-ttu-id="62b6d-114">예제 1: 공유의 목록</span><span class="sxs-lookup"><span data-stu-id="62b6d-114">Example 1: List directories in a share</span></span>
```
PS C:\>Get-AzStorageFile -ShareName "ContosoShare06" | where {$_.GetType().Name -eq "AzureStorageFileDirectory"}
```

<span data-ttu-id="62b6d-115">이 명령은 ContosoShare06 공유에 있는 감독자만 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="62b6d-115">This command lists only the directories in the share ContosoShare06.</span></span>
<span data-ttu-id="62b6d-116">먼저 파일과 디렉터를 모두 검색하고, 파이프라인 연산자를 사용하여 **where** 연산자에 전달한 다음, 형식이 "AzureStorageFileDirectory"가 아닌 모든 개체를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="62b6d-116">It first retrieves both files and directories, passes them to the **where** operator by using the pipeline operator, then discards any objects whose type is not "AzureStorageFileDirectory".</span></span>

### <span data-ttu-id="62b6d-117">예제 2: 파일 디렉터리 나열</span><span class="sxs-lookup"><span data-stu-id="62b6d-117">Example 2: List a File Directory</span></span>
```
PS C:\> Get-AzStorageFile -ShareName "ContosoShare06" -Path "ContosoWorkingFolder" | Get-AzStorageFile
```

<span data-ttu-id="62b6d-118">이 명령은 ContosoShare06 공유 아래에 ContosoWorkingFolder 디렉터리의 파일 및 폴더를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="62b6d-118">This command lists the files and folders in the directory ContosoWorkingFolder under the share ContosoShare06.</span></span>
<span data-ttu-id="62b6d-119">먼저 디렉터리 인스턴스를 얻은 다음 **Get-AzStorageFile** cmdlet에 파이프라인을 추가하여 디렉터리를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="62b6d-119">It first gets the directory instance, and then pipelines it to the **Get-AzStorageFile** cmdlet to list the directory.</span></span>

## <span data-ttu-id="62b6d-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62b6d-120">PARAMETERS</span></span>

### <span data-ttu-id="62b6d-121">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="62b6d-121">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="62b6d-122">하나의 서비스 요청에 대해 클라이언트 쪽 시간 시간(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="62b6d-122">Specifies the client side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="62b6d-123">이전 호출이 지정된 간격 내에 실패하면 이 cmdlet은 요청을 다시 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="62b6d-123">If the previous call fails within the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="62b6d-124">이 cmdlet이 간격이 경과하기 전에 성공적인 응답을 받지 못하면 이 cmdlet은 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="62b6d-124">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="62b6d-125">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="62b6d-125">-ConcurrentTaskCount</span></span>
<span data-ttu-id="62b6d-126">최대 동시 네트워크 호출을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="62b6d-126">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="62b6d-127">이 매개 변수를 사용하여 최대 동시 네트워크 호출 수를 지정하여 동시성으로 로컬 CPU 및 대역폭 사용량을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="62b6d-127">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="62b6d-128">지정된 값은 절대 개수로, 코어 수에 곱하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="62b6d-128">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="62b6d-129">이 매개 변수는 초당 100킬로비트와 같은 낮은 대역폭 환경에서 네트워크 연결 문제를 완화하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="62b6d-129">This parameter can help mitigate network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="62b6d-130">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="62b6d-130">The default value is 10.</span></span>

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

### <span data-ttu-id="62b6d-131">-Context</span><span class="sxs-lookup"><span data-stu-id="62b6d-131">-Context</span></span>
<span data-ttu-id="62b6d-132">Azure Storage 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="62b6d-132">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="62b6d-133">Storage 컨텍스트를 얻습니다. New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="62b6d-133">To obtain a Storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="62b6d-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62b6d-134">-DefaultProfile</span></span>
<span data-ttu-id="62b6d-135">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="62b6d-135">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62b6d-136">-Directory</span><span class="sxs-lookup"><span data-stu-id="62b6d-136">-Directory</span></span>
<span data-ttu-id="62b6d-137">폴더를 **CloudFileDirectory 개체로 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="62b6d-137">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="62b6d-138">이 cmdlet은 이 매개 변수가 지정하는 폴더를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="62b6d-138">This cmdlet gets the folder that this parameter specifies.</span></span>
<span data-ttu-id="62b6d-139">디렉터리를 얻습니다. New-AzStorageDirectory cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="62b6d-139">To obtain a directory, use the New-AzStorageDirectory cmdlet.</span></span>
<span data-ttu-id="62b6d-140">**Get-AzStorageFile** cmdlet을 사용하여 디렉터리를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="62b6d-140">You can also use the **Get-AzStorageFile** cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="62b6d-141">-Path</span><span class="sxs-lookup"><span data-stu-id="62b6d-141">-Path</span></span>
<span data-ttu-id="62b6d-142">폴더의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="62b6d-142">Specifies the path of a folder.</span></span>
<span data-ttu-id="62b6d-143">*Path* 매개 변수를 생략하면 **Get-AzStorageFile은** 지정된 파일 공유 또는 디렉터리의 디렉터리 및 파일을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="62b6d-143">If you omit the *Path* parameter, **Get-AzStorageFile** lists the directories and files in the specified file share or directory.</span></span>
<span data-ttu-id="62b6d-144">Path 매개 *변수를 포함하면* **Get-AzStorageFile은** 지정된 경로에 디렉터리 또는 파일의 인스턴스를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="62b6d-144">If you include the *Path* parameter, **Get-AzStorageFile** returns an instance of a directory or file in the specified path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62b6d-145">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="62b6d-145">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="62b6d-146">요청에 대한 서비스 쪽 시간 제한 간격(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="62b6d-146">Specifies the service-side timeout interval, in seconds, for a request.</span></span>
<span data-ttu-id="62b6d-147">지정된 간격이 서비스에서 요청을 처리하기 전에 경과하면 Storage 서비스는 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="62b6d-147">If the specified interval elapses before the service processes the request, the Storage service returns an error.</span></span>

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

### <span data-ttu-id="62b6d-148">-공유</span><span class="sxs-lookup"><span data-stu-id="62b6d-148">-Share</span></span>
<span data-ttu-id="62b6d-149">**CloudFileShare 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="62b6d-149">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="62b6d-150">이 cmdlet은 이 매개 변수가 지정하는 파일 공유에서 파일 또는 디렉터리를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="62b6d-150">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>
<span data-ttu-id="62b6d-151">**CloudFileShare** 개체를 얻습니다. Get-AzStorageShare cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="62b6d-151">To obtain a **CloudFileShare** object, use the Get-AzStorageShare cmdlet.</span></span>
<span data-ttu-id="62b6d-152">이 개체에는 Storage 컨텍스트가 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="62b6d-152">This object contains the Storage context.</span></span>
<span data-ttu-id="62b6d-153">이 매개 변수를 지정하는 경우 Context 매개 변수를 *지정하지* 않습니다.</span><span class="sxs-lookup"><span data-stu-id="62b6d-153">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="62b6d-154">-ShareName</span><span class="sxs-lookup"><span data-stu-id="62b6d-154">-ShareName</span></span>
<span data-ttu-id="62b6d-155">파일 공유의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="62b6d-155">Specifies the name of the file share.</span></span>
<span data-ttu-id="62b6d-156">이 cmdlet은 이 매개 변수가 지정하는 파일 공유에서 파일 또는 디렉터리를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="62b6d-156">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="62b6d-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62b6d-157">CommonParameters</span></span>
<span data-ttu-id="62b6d-158">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="62b6d-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62b6d-159">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="62b6d-159">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62b6d-160">입력</span><span class="sxs-lookup"><span data-stu-id="62b6d-160">INPUTS</span></span>

### <span data-ttu-id="62b6d-161">Microsoft.Azure.Storage.File.CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="62b6d-161">Microsoft.Azure.Storage.File.CloudFileShare</span></span>

### <span data-ttu-id="62b6d-162">Microsoft.Azure.Storage.File.CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="62b6d-162">Microsoft.Azure.Storage.File.CloudFileDirectory</span></span>

### <span data-ttu-id="62b6d-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="62b6d-163">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="62b6d-164">출력</span><span class="sxs-lookup"><span data-stu-id="62b6d-164">OUTPUTS</span></span>

### <span data-ttu-id="62b6d-165">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="62b6d-165">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFile</span></span>

## <span data-ttu-id="62b6d-166">참고 사항</span><span class="sxs-lookup"><span data-stu-id="62b6d-166">NOTES</span></span>

## <span data-ttu-id="62b6d-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="62b6d-167">RELATED LINKS</span></span>

[<span data-ttu-id="62b6d-168">Get-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="62b6d-168">Get-AzStorageFileContent</span></span>](./Get-AzStorageFileContent.md)

[<span data-ttu-id="62b6d-169">New-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="62b6d-169">New-AzStorageDirectory</span></span>](./New-AzStorageDirectory.md)

[<span data-ttu-id="62b6d-170">Remove-AzStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="62b6d-170">Remove-AzStorageDirectory</span></span>](./Remove-AzStorageDirectory.md)

[<span data-ttu-id="62b6d-171">Remove-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="62b6d-171">Remove-AzStorageFile</span></span>](./Remove-AzStorageFile.md)

[<span data-ttu-id="62b6d-172">Set-AzStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="62b6d-172">Set-AzStorageFileContent</span></span>](./Set-AzStorageFileContent.md)


