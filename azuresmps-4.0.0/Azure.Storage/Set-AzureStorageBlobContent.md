---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: F20A5FD3-6EC3-4EFE-988C-75F8583961A4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1caded810569225bfa269e7c0d29c60be87d4fb3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523911"
---
# <span data-ttu-id="f0299-101">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f0299-101">Set-AzureStorageBlobContent</span></span>

## <span data-ttu-id="f0299-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0299-102">SYNOPSIS</span></span>
<span data-ttu-id="f0299-103">Azure 저장소 blob에 로컬 파일을 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0299-103">Uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="f0299-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f0299-104">SYNTAX</span></span>

### <span data-ttu-id="f0299-105">SendManual (기본값)</span><span class="sxs-lookup"><span data-stu-id="f0299-105">SendManual (Default)</span></span>
```
Set-AzureStorageBlobContent [-File] <String> [-Container] <String> [-Blob <String>] [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0299-106">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="f0299-106">ContainerPipeline</span></span>
```
Set-AzureStorageBlobContent [-File] <String> [-Blob <String>] -CloudBlobContainer <CloudBlobContainer>
 [-BlobType <String>] [-Properties <Hashtable>] [-Metadata <Hashtable>] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f0299-107">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="f0299-107">BlobPipeline</span></span>
```
Set-AzureStorageBlobContent [-File] <String> -CloudBlob <CloudBlob> [-BlobType <String>]
 [-Properties <Hashtable>] [-Metadata <Hashtable>] [-Force] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0299-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f0299-108">DESCRIPTION</span></span>
<span data-ttu-id="f0299-109">**집합-AzureStorageBlobContent** cmdlet은 로컬 파일을 Azure Storage blob에 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0299-109">The **Set-AzureStorageBlobContent** cmdlet uploads a local file to an Azure Storage blob.</span></span>

## <span data-ttu-id="f0299-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f0299-110">EXAMPLES</span></span>

### <span data-ttu-id="f0299-111">예제 1: 명명 된 파일 업로드</span><span class="sxs-lookup"><span data-stu-id="f0299-111">Example 1: Upload a named file</span></span>
```
PS C:\>Set-AzureStorageBlobContent -Container "ContosoUpload" -File ".\PlanningData" -Blob "Planning2015"
```

<span data-ttu-id="f0299-112">이 명령은 PlanningData 이라는 파일을 Planning2015 라는 blob에 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0299-112">This command uploads the file that is named PlanningData to a blob named Planning2015.</span></span>

### <span data-ttu-id="f0299-113">예제 2: 현재 폴더 아래의 모든 파일 업로드</span><span class="sxs-lookup"><span data-stu-id="f0299-113">Example 2: Upload all files under the current folder</span></span>
```
PS C:\>Get-ChildItem -File -Recurse | Set-AzureStorageBlobContent -Container "ContosoUploads"
```

<span data-ttu-id="f0299-114">이 명령은 핵심 Windows PowerShell cmdlet Get-ChildItem를 사용 하 여 현재 폴더 및 하위 폴더에 있는 모든 파일을 가져오고 파이프라인 연산자를 사용 하 여 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0299-114">This command uses the core Windows PowerShell cmdlet Get-ChildItem to get all the files in the current folder and in subfolders, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="f0299-115">**Set-AzureStorageBlobContent** Cmdlet은 ContosoUploads 이라는 이름의 컨테이너에 파일을 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0299-115">The **Set-AzureStorageBlobContent** cmdlet uploads the files to the container named ContosoUploads.</span></span>

### <span data-ttu-id="f0299-116">예제 3: 기존 blob 덮어쓰기</span><span class="sxs-lookup"><span data-stu-id="f0299-116">Example 3: Overwrite an existing blob</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContosoUploads" -Blob "Planning2015" | Set-AzureStorageBlobContent -File "ContosoPlanning"
```

<span data-ttu-id="f0299-117">이 명령은 Get-AzureStorageBlob cmdlet을 사용 하 여 ContosoUploads 컨테이너의 Planning2015 라는 blob을 가져온 다음 현재 cmdlet에 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0299-117">This command gets the blob named Planning2015 in the ContosoUploads container by using the Get-AzureStorageBlob cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="f0299-118">명령이 ContosoPlanning as Planning2015 라는 파일을 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0299-118">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>
<span data-ttu-id="f0299-119">이 명령은 *Force* 매개 변수를 지정 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f0299-119">This command does not specify the *Force* parameter.</span></span>
<span data-ttu-id="f0299-120">명령에서 확인 하 라는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0299-120">The command prompts you for confirmation.</span></span>
<span data-ttu-id="f0299-121">명령을 확인 하면 cmdlet이 기존 blob을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="f0299-121">If you confirm the command, the cmdlet overwrites the existing blob.</span></span>

### <span data-ttu-id="f0299-122">예제 4: 파이프라인을 사용 하 여 컨테이너에 파일 업로드</span><span class="sxs-lookup"><span data-stu-id="f0299-122">Example 4: Upload a file to a container by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Container "ContosoUpload*" | Set-AzureStorageBlobContent -File "ContosoPlanning" -Blob "Planning2015"
```

<span data-ttu-id="f0299-123">이 명령은 **AzureStorageContainer** cmdlet을 사용 하 여 ContosoUpload 문자열로 시작 하는 컨테이너를 가져온 다음 현재 cmdlet에 해당 blob을 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0299-123">This command gets the container that starts with the string ContosoUpload by using the **Get-AzureStorageContainer** cmdlet, and then passes that blob to the current cmdlet.</span></span>
<span data-ttu-id="f0299-124">명령이 ContosoPlanning as Planning2015 라는 파일을 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0299-124">The command uploads the file that is named ContosoPlanning as Planning2015.</span></span>

### <span data-ttu-id="f0299-125">예제 5: 파일 및 메타 데이터 업로드</span><span class="sxs-lookup"><span data-stu-id="f0299-125">Example 5: Upload a file and metadata</span></span>
```
PS C:\>$Metadata = @{"key" = "value"; "name" = "test"}
PS C:\> Set-AzureStorageBlobContent -File "ContosoPlanning" -Container "ContosoUploads" -Metadata $Metadata
```

<span data-ttu-id="f0299-126">첫 번째 명령은 blob에 대 한 메타 데이터를 포함 하는 해시 테이블을 만들고이 해시 테이블을 $Metadata 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0299-126">The first command creates a hash table that contains metadata for a blob, and stores that hash table in the $Metadata variable.</span></span>

<span data-ttu-id="f0299-127">두 번째 명령은 ContosoPlanning 이라는 파일을 ContosoUploads 이라는 컨테이너에 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0299-127">The second command uploads the file that is named ContosoPlanning to the container named ContosoUploads.</span></span>
<span data-ttu-id="f0299-128">Blob에는 $Metadata에 저장 된 메타 데이터가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f0299-128">The blob includes the metadata stored in $Metadata.</span></span>

## <span data-ttu-id="f0299-129">변수</span><span class="sxs-lookup"><span data-stu-id="f0299-129">PARAMETERS</span></span>

### <span data-ttu-id="f0299-130">-Blob</span><span class="sxs-lookup"><span data-stu-id="f0299-130">-Blob</span></span>
<span data-ttu-id="f0299-131">Blob의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0299-131">Specifies the name of a blob.</span></span>
<span data-ttu-id="f0299-132">이 cmdlet은이 매개 변수에서 지정 하는 Azure 저장소 blob에 파일을 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0299-132">This cmdlet uploads a file to the Azure Storage blob that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: SendManual, ContainerPipeline
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0299-133">-BlobType</span><span class="sxs-lookup"><span data-stu-id="f0299-133">-BlobType</span></span>
<span data-ttu-id="f0299-134">이 cmdlet이 업로드 하는 blob의 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0299-134">Specifies the type for the blob that this cmdlet uploads.</span></span>
<span data-ttu-id="f0299-135">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="f0299-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f0299-136">않도록</span><span class="sxs-lookup"><span data-stu-id="f0299-136">Block</span></span>
- <span data-ttu-id="f0299-137">쪽</span><span class="sxs-lookup"><span data-stu-id="f0299-137">Page</span></span>

<span data-ttu-id="f0299-138">기본값은 블록입니다.</span><span class="sxs-lookup"><span data-stu-id="f0299-138">The default value is Block.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Block, Page, Append

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0299-139">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f0299-139">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="f0299-140">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0299-140">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="f0299-141">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0299-141">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="f0299-142">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0299-142">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="f0299-143">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="f0299-143">-CloudBlob</span></span>
<span data-ttu-id="f0299-144">**CloudBlob** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0299-144">Specifies a **CloudBlob** object.</span></span>
<span data-ttu-id="f0299-145">**CloudBlob** 개체를 가져오려면 Get-AzureStorageBlob cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0299-145">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0299-146">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="f0299-146">-CloudBlobContainer</span></span>
<span data-ttu-id="f0299-147">Azure Storage 클라이언트 라이브러리에서 **CloudBlobContainer** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0299-147">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="f0299-148">이 cmdlet은이 매개 변수에서 지정 하는 컨테이너의 blob에 콘텐츠를 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0299-148">This cmdlet uploads content to a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="f0299-149">**CloudBlobContainer** 개체를 가져오려면 Get-AzureStorageContainer cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0299-149">To obtain a **CloudBlobContainer** object, use the Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0299-150">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="f0299-150">-ConcurrentTaskCount</span></span>
<span data-ttu-id="f0299-151">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0299-151">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="f0299-152">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0299-152">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="f0299-153">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="f0299-153">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="f0299-154">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0299-154">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="f0299-155">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="f0299-155">The default value is 10.</span></span>

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

### <span data-ttu-id="f0299-156">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="f0299-156">-Container</span></span>
<span data-ttu-id="f0299-157">컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0299-157">Specifies the name of a container.</span></span>
<span data-ttu-id="f0299-158">이 cmdlet은이 매개 변수에서 지정 하는 컨테이너의 blob에 파일을 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0299-158">This cmdlet uploads a file to a blob in the container that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: SendManual
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0299-159">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="f0299-159">-Context</span></span>
<span data-ttu-id="f0299-160">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0299-160">Specifies an Azure storage context.</span></span>
<span data-ttu-id="f0299-161">저장소 컨텍스트를 얻으려면 New-AzureStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0299-161">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0299-162">-파일</span><span class="sxs-lookup"><span data-stu-id="f0299-162">-File</span></span>
<span data-ttu-id="f0299-163">Blob content로 업로드할 파일의 로컬 파일 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0299-163">Specifies a local file path for a file to upload as blob content.</span></span>

```yaml
Type: String
Parameter Sets: SendManual
Aliases: FullName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ContainerPipeline, BlobPipeline
Aliases: FullName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0299-164">-Force</span><span class="sxs-lookup"><span data-stu-id="f0299-164">-Force</span></span>
<span data-ttu-id="f0299-165">이 cmdlet이 확인 메시지를 표시 하지 않고 기존 blob을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="f0299-165">Indicates that this cmdlet overwrites an existing blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="f0299-166">-Metadata</span><span class="sxs-lookup"><span data-stu-id="f0299-166">-Metadata</span></span>
<span data-ttu-id="f0299-167">업로드 된 blob에 대 한 메타 데이터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0299-167">Specifies metadata for the uploaded blob.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0299-168">-속성</span><span class="sxs-lookup"><span data-stu-id="f0299-168">-Properties</span></span>
<span data-ttu-id="f0299-169">업로드 된 blob에 대 한 속성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0299-169">Specifies properties for the uploaded blob.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0299-170">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="f0299-170">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="f0299-171">요청에 대 한 서비스 측 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0299-171">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="f0299-172">서비스가 요청을 처리 하기 전에 지정 된 간격이 경과 하면 저장소 서비스에서 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0299-172">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="f0299-173">-확인</span><span class="sxs-lookup"><span data-stu-id="f0299-173">-Confirm</span></span>
<span data-ttu-id="f0299-174">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0299-174">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0299-175">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0299-175">-WhatIf</span></span>
<span data-ttu-id="f0299-176">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f0299-176">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0299-177">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f0299-177">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0299-178">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0299-178">CommonParameters</span></span>
<span data-ttu-id="f0299-179">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0299-179">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0299-180">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0299-180">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0299-181">입력</span><span class="sxs-lookup"><span data-stu-id="f0299-181">INPUTS</span></span>

## <span data-ttu-id="f0299-182">출력</span><span class="sxs-lookup"><span data-stu-id="f0299-182">OUTPUTS</span></span>

## <span data-ttu-id="f0299-183">상속자</span><span class="sxs-lookup"><span data-stu-id="f0299-183">NOTES</span></span>

## <span data-ttu-id="f0299-184">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f0299-184">RELATED LINKS</span></span>

[<span data-ttu-id="f0299-185">가져오기-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="f0299-185">Get-AzureStorageBlobContent</span></span>](./Get-AzureStorageBlobContent.md)

[<span data-ttu-id="f0299-186">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="f0299-186">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="f0299-187">-AzureStorageBlob 제거</span><span class="sxs-lookup"><span data-stu-id="f0299-187">Remove-AzureStorageBlob</span></span>](./Remove-AzureStorageBlob.md)
