---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 38207027-FD76-45EE-8817-88599735C0B0
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragefile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageFile.md
ms.openlocfilehash: a66b84586693052a2e6279c0cd56d8b091ae4230
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530629"
---
# <span data-ttu-id="26e4c-101">Get-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="26e4c-101">Get-AzureStorageFile</span></span>

## <span data-ttu-id="26e4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26e4c-102">SYNOPSIS</span></span>
<span data-ttu-id="26e4c-103">경로에 대 한 디렉터리 및 파일을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="26e4c-103">Lists directories and files for a path.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="26e4c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="26e4c-104">SYNTAX</span></span>

### <span data-ttu-id="26e4c-105">ShareName (기본값)</span><span class="sxs-lookup"><span data-stu-id="26e4c-105">ShareName (Default)</span></span>
```
Get-AzureStorageFile [-ShareName] <String> [[-Path] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="26e4c-106">공유</span><span class="sxs-lookup"><span data-stu-id="26e4c-106">Share</span></span>
```
Get-AzureStorageFile [-Share] <CloudFileShare> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="26e4c-107">디렉토리로</span><span class="sxs-lookup"><span data-stu-id="26e4c-107">Directory</span></span>
```
Get-AzureStorageFile [-Directory] <CloudFileDirectory> [[-Path] <String>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="26e4c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="26e4c-108">DESCRIPTION</span></span>
<span data-ttu-id="26e4c-109">**AzureStorageFile** cmdlet은 사용자가 지정 하는 공유 또는 디렉터리에 대 한 디렉터리 및 파일을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="26e4c-109">The **Get-AzureStorageFile** cmdlet lists directories and files for the share or directory that you specify.</span></span>
<span data-ttu-id="26e4c-110">*Path* 매개 변수를 지정 하 여 지정 된 경로에 있는 디렉터리 또는 파일의 인스턴스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="26e4c-110">Specify the *Path* parameter to get an instance of a directory or file in the specified path.</span></span>

<span data-ttu-id="26e4c-111">이 cmdlet은 **AzureStorageFile** 및 **azurestoragedirectory** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="26e4c-111">This cmdlet returns **AzureStorageFile** and **AzureStorageDirectory** objects.</span></span>
<span data-ttu-id="26e4c-112">**Isdirectory** 속성을 사용 하 여 폴더와 파일을 구별할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26e4c-112">You can use the **IsDirectory** property to distinguish between folders and files.</span></span>

## <span data-ttu-id="26e4c-113">예제의</span><span class="sxs-lookup"><span data-stu-id="26e4c-113">EXAMPLES</span></span>

### <span data-ttu-id="26e4c-114">예제 1: 공유의 디렉터리 나열</span><span class="sxs-lookup"><span data-stu-id="26e4c-114">Example 1: List directories in a share</span></span>
```
PS C:\>Get-AzureStorageFile -ShareName "ContosoShare06" | where {$_.GetType().Name -eq "CloudFileDirectory"}
```

<span data-ttu-id="26e4c-115">이 명령은 공유 ContosoShare06의 디렉터리만 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="26e4c-115">This command lists only the directories in the share ContosoShare06.</span></span>
<span data-ttu-id="26e4c-116">먼저 파일과 디렉터리를 모두 검색 하 고 파이프라인 연산자를 사용 하 여 **where** 연산자에 전달한 다음 형식이 "CloudFileDirectory"가 아닌 개체를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="26e4c-116">It first retrieves both files and directories, passes them to the **where** operator by using the pipeline operator, then discards any objects whose type is not "CloudFileDirectory".</span></span>

### <span data-ttu-id="26e4c-117">예제 2: 파일 디렉터리 나열</span><span class="sxs-lookup"><span data-stu-id="26e4c-117">Example 2: List a File Directory</span></span>
```
PS C:\> Get-AzureStorageFile -ShareName "ContosoShare06" -Path "ContosoWorkingFolder" | Get-AzureStorageFile
```

<span data-ttu-id="26e4c-118">이 명령은 디렉터리 ContosoWorkingFolder의 share ContosoShare06에 있는 파일 및 폴더를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="26e4c-118">This command lists the files and folders in the directory ContosoWorkingFolder under the share ContosoShare06.</span></span>
<span data-ttu-id="26e4c-119">먼저 디렉터리 인스턴스를 가져온 다음 **AzureStorageFile** cmdlet으로이를 파이프라인 하 여 디렉터리를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="26e4c-119">It first gets the directory instance, and then pipelines it to the **Get-AzureStorageFile** cmdlet to list the directory.</span></span>

## <span data-ttu-id="26e4c-120">변수</span><span class="sxs-lookup"><span data-stu-id="26e4c-120">PARAMETERS</span></span>

### <span data-ttu-id="26e4c-121">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="26e4c-121">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="26e4c-122">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26e4c-122">Specifies the client side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="26e4c-123">이전 호출이 지정 된 간격 내에 실패 하는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="26e4c-123">If the previous call fails within the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="26e4c-124">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="26e4c-124">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="26e4c-125">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="26e4c-125">-ConcurrentTaskCount</span></span>
<span data-ttu-id="26e4c-126">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26e4c-126">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="26e4c-127">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26e4c-127">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="26e4c-128">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="26e4c-128">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="26e4c-129">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 완화 하는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26e4c-129">This parameter can help mitigate network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="26e4c-130">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="26e4c-130">The default value is 10.</span></span>

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

### <span data-ttu-id="26e4c-131">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="26e4c-131">-Context</span></span>
<span data-ttu-id="26e4c-132">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26e4c-132">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="26e4c-133">저장소 컨텍스트를 얻으려면 New-AzureStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="26e4c-133">To obtain a Storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="26e4c-134">-디렉터리</span><span class="sxs-lookup"><span data-stu-id="26e4c-134">-Directory</span></span>
<span data-ttu-id="26e4c-135">폴더를 **Cloudfiledirectory** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26e4c-135">Specifies a folder as a **CloudFileDirectory** object.</span></span>
<span data-ttu-id="26e4c-136">이 cmdlet은이 매개 변수에서 지정 하는 폴더를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="26e4c-136">This cmdlet gets the folder that this parameter specifies.</span></span>
<span data-ttu-id="26e4c-137">디렉터리를 가져오려면 New-AzureStorageDirectory cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="26e4c-137">To obtain a directory, use the New-AzureStorageDirectory cmdlet.</span></span>
<span data-ttu-id="26e4c-138">**Get-AzureStorageFile** cmdlet을 사용 하 여 디렉터리를 가져올 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="26e4c-138">You can also use the **Get-AzureStorageFile** cmdlet to obtain a directory.</span></span>

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

### <span data-ttu-id="26e4c-139">-Path</span><span class="sxs-lookup"><span data-stu-id="26e4c-139">-Path</span></span>
<span data-ttu-id="26e4c-140">폴더의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26e4c-140">Specifies the path of a folder.</span></span>

<span data-ttu-id="26e4c-141">*Path* 매개 변수를 생략 하면 **AzureStorageFile** 에서 지정 된 파일 공유 또는 디렉터리의 디렉터리와 파일을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="26e4c-141">If you omit the *Path* parameter, **Get-AzureStorageFile** lists the directories and files in the specified file share or directory.</span></span>
<span data-ttu-id="26e4c-142">*Path* 매개 변수를 포함 하는 경우 **AzureStorageFile** 는 지정 된 경로에 있는 디렉터리 또는 파일의 인스턴스를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="26e4c-142">If you include the *Path* parameter, **Get-AzureStorageFile** returns an instance of a directory or file in the specified path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26e4c-143">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="26e4c-143">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="26e4c-144">요청에 대 한 서비스 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26e4c-144">Specifies the service-side timeout interval, in seconds, for a request.</span></span>
<span data-ttu-id="26e4c-145">서비스가 요청을 처리 하기 전에 지정 된 간격이 경과 하면 저장소 서비스에서 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="26e4c-145">If the specified interval elapses before the service processes the request, the Storage service returns an error.</span></span>

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

### <span data-ttu-id="26e4c-146">-공유</span><span class="sxs-lookup"><span data-stu-id="26e4c-146">-Share</span></span>
<span data-ttu-id="26e4c-147">**Cloudfileshare** 되지 않는 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26e4c-147">Specifies a **CloudFileShare** object.</span></span>
<span data-ttu-id="26e4c-148">이 cmdlet은이 매개 변수에서 지정 하는 파일 공유에서 파일 또는 디렉터리를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="26e4c-148">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>
<span data-ttu-id="26e4c-149">**Cloudfileshare** 되지 않는 개체를 가져오려면 Get-AzureStorageShare cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="26e4c-149">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>
<span data-ttu-id="26e4c-150">이 개체는 저장소 컨텍스트를 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="26e4c-150">This object contains the Storage context.</span></span>
<span data-ttu-id="26e4c-151">이 매개 변수를 지정 하는 경우 *컨텍스트* 매개 변수를 지정 하지 마세요.</span><span class="sxs-lookup"><span data-stu-id="26e4c-151">If you specify this parameter, do not specify the *Context* parameter.</span></span>

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

### <span data-ttu-id="26e4c-152">-ShareName</span><span class="sxs-lookup"><span data-stu-id="26e4c-152">-ShareName</span></span>
<span data-ttu-id="26e4c-153">파일 공유의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26e4c-153">Specifies the name of the file share.</span></span>
<span data-ttu-id="26e4c-154">이 cmdlet은이 매개 변수에서 지정 하는 파일 공유에서 파일 또는 디렉터리를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="26e4c-154">This cmdlet gets a file or directory from the file share that this parameter specifies.</span></span>

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

### <span data-ttu-id="26e4c-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26e4c-155">CommonParameters</span></span>
<span data-ttu-id="26e4c-156">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="26e4c-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26e4c-157">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26e4c-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26e4c-158">입력</span><span class="sxs-lookup"><span data-stu-id="26e4c-158">INPUTS</span></span>

### <span data-ttu-id="26e4c-159">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="26e4c-159">IStorageContext</span></span>

<span data-ttu-id="26e4c-160">' Context ' 매개 변수는 파이프라인에서 ' IStorageContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="26e4c-160">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="26e4c-161">CloudFileDirectory</span><span class="sxs-lookup"><span data-stu-id="26e4c-161">CloudFileDirectory</span></span>

<span data-ttu-id="26e4c-162">' Directory ' 매개 변수는 파이프라인에서 ' CloudFileDirectory ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="26e4c-162">Parameter 'Directory' accepts value of type 'CloudFileDirectory' from the pipeline</span></span>

### <span data-ttu-id="26e4c-163">CloudFileShare</span><span class="sxs-lookup"><span data-stu-id="26e4c-163">CloudFileShare</span></span>

<span data-ttu-id="26e4c-164">' Share ' 매개 변수는 파이프라인에서 ' CloudFileShare 범위 ' 형식의 값을 받아들입니다.</span><span class="sxs-lookup"><span data-stu-id="26e4c-164">Parameter 'Share' accepts value of type 'CloudFileShare' from the pipeline</span></span>

## <span data-ttu-id="26e4c-165">출력</span><span class="sxs-lookup"><span data-stu-id="26e4c-165">OUTPUTS</span></span>

## <span data-ttu-id="26e4c-166">상속자</span><span class="sxs-lookup"><span data-stu-id="26e4c-166">NOTES</span></span>

## <span data-ttu-id="26e4c-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="26e4c-167">RELATED LINKS</span></span>

[<span data-ttu-id="26e4c-168">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="26e4c-168">Get-AzureStorageFileContent</span></span>](./Get-AzureStorageFileContent.md)

[<span data-ttu-id="26e4c-169">새-AzureStorageDirectory</span><span class="sxs-lookup"><span data-stu-id="26e4c-169">New-AzureStorageDirectory</span></span>](./New-AzureStorageDirectory.md)

[<span data-ttu-id="26e4c-170">-AzureStorageDirectory 제거</span><span class="sxs-lookup"><span data-stu-id="26e4c-170">Remove-AzureStorageDirectory</span></span>](./Remove-AzureStorageDirectory.md)

[<span data-ttu-id="26e4c-171">제거-AzureStorageFile</span><span class="sxs-lookup"><span data-stu-id="26e4c-171">Remove-AzureStorageFile</span></span>](./Remove-AzureStorageFile.md)

[<span data-ttu-id="26e4c-172">Set-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="26e4c-172">Set-AzureStorageFileContent</span></span>](./Set-AzureStorageFileContent.md)


