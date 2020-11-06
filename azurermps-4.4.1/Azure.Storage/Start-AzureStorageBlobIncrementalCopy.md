---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Start-AzureStorageBlobIncrementalCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Start-AzureStorageBlobIncrementalCopy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/e87bc1c9e534808427b7dc77aa06eacc46663253
ms.openlocfilehash: b327db4c7054e3c841dca3310887b1d1f1201d23
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531893"
---
# <span data-ttu-id="68420-101">Start-AzureStorageBlobIncrementalCopy</span><span class="sxs-lookup"><span data-stu-id="68420-101">Start-AzureStorageBlobIncrementalCopy</span></span>

## <span data-ttu-id="68420-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68420-102">SYNOPSIS</span></span>
<span data-ttu-id="68420-103">페이지 blob 스냅숏에서 지정 된 대상 페이지 blob로 증분 복사 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="68420-103">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68420-104">구문과</span><span class="sxs-lookup"><span data-stu-id="68420-104">SYNTAX</span></span>

### <span data-ttu-id="68420-105">ContainerInstance (기본값)</span><span class="sxs-lookup"><span data-stu-id="68420-105">ContainerInstance (Default)</span></span>
```
Start-AzureStorageBlobIncrementalCopy -CloudBlobContainer <CloudBlobContainer> -SrcBlob <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68420-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="68420-106">BlobInstance</span></span>
```
Start-AzureStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68420-107">Blobinstanceetobinstance</span><span class="sxs-lookup"><span data-stu-id="68420-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzureStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestCloudBlob <CloudPageBlob>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68420-108">ContainerName</span><span class="sxs-lookup"><span data-stu-id="68420-108">ContainerName</span></span>
```
Start-AzureStorageBlobIncrementalCopy -SrcBlob <String> -SrcContainer <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="68420-109">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="68420-109">UriPipeline</span></span>
```
Start-AzureStorageBlobIncrementalCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68420-110">설명은</span><span class="sxs-lookup"><span data-stu-id="68420-110">DESCRIPTION</span></span>
<span data-ttu-id="68420-111">페이지 blob 스냅숏에서 지정 된 대상 페이지 blob로 증분 복사 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="68420-111">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>
<span data-ttu-id="68420-112">의 기능에 대 한 자세한 정보를 확인 하세요 https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob .</span><span class="sxs-lookup"><span data-stu-id="68420-112">See more details of the feature in https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob.</span></span>

## <span data-ttu-id="68420-113">예제의</span><span class="sxs-lookup"><span data-stu-id="68420-113">EXAMPLES</span></span>

### <span data-ttu-id="68420-114">예제 1: blob 이름 및 스냅숏 시간에 따라 증분 복사 작업 시작</span><span class="sxs-lookup"><span data-stu-id="68420-114">Example 1: Start Incremental Copy Operation by blob name and snapshot time</span></span>
```
PS C:\>Start-AzureStorageBlobIncrementalCopy -SrcContainer container1 -SrcBlob blob1 -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="68420-115">이 명령은 blob 이름 및 스냅숏 시간에 따라 증분 복사 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="68420-115">This command start Incremental Copy Operation by blob name and snapshot time</span></span>

### <span data-ttu-id="68420-116">예제 2: 원본 uri를 사용 하 여 증분 복사 작업 시작</span><span class="sxs-lookup"><span data-stu-id="68420-116">Example 2: Start Incremental copy operation using source uri</span></span>
```
PS C:\>Start-AzureStorageBlobIncrementalCopy -AbsoluteUri "http://www.somesite.com/somefile?snapshot=2017-04-07T10:05:40.2126635Z" -DestContainer container -DestBlob blob -DestContext $context
```

<span data-ttu-id="68420-117">이 명령은 원본 uri를 사용 하 여 증분 복사 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="68420-117">This command start Incremental Copy Operation using source uri</span></span>

### <span data-ttu-id="68420-118">예제 3: GetAzureStorageContainer에서 컨테이너 파이프라인을 사용 하 여 증분 복사 작업 시작</span><span class="sxs-lookup"><span data-stu-id="68420-118">Example 3:  Start Incremental copy operation using container pipeline from GetAzureStorageContainer</span></span>
```
PS C:\>Get-AzureStorageContainer -Container container1 | Start-AzureStorageBlobIncrementalCopy -SrcBlob blob  -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2
```

<span data-ttu-id="68420-119">이 명령은 GetAzureStorageContainer에서 컨테이너 파이프라인을 사용 하 여 증분 복사 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="68420-119">This command start Incremental Copy Operation using container pipeline from GetAzureStorageContainer</span></span>

### <span data-ttu-id="68420-120">예제 4: CloudPageBlob 개체에서 blob 이름을 사용 하 여 대상 blob로 증분 복사 작업 시작</span><span class="sxs-lookup"><span data-stu-id="68420-120">Example 4:  start Incremental copy operation from CloudPageBlob object to destination blob with blob name</span></span>
```
PS C:\>$srcBlobSnapshot = Get-AzureStorageBlob -Container container1 -prefix blob1| ?{$_.ICloudBlob.IsSnapshot})[0]
PS C:\>Start-AzureStorageBlobIncrementalCopy -CloudBlob $srcBlobSnapshot.ICloudBlob -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="68420-121">이 명령은 CloudPageBlob 개체에서 blob 이름을 사용 하는 대상 blob로 증분 복사 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="68420-121">This command start Incremental Copy Operation from CloudPageBlob object to destination blob with blob name</span></span>

## <span data-ttu-id="68420-122">변수</span><span class="sxs-lookup"><span data-stu-id="68420-122">PARAMETERS</span></span>

### <span data-ttu-id="68420-123">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="68420-123">-AbsoluteUri</span></span>
<span data-ttu-id="68420-124">원본에 대 한 절대 Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="68420-124">Absolute Uri to the source.</span></span> <span data-ttu-id="68420-125">원본에 필요한 경우 자격 증명을 Uri에 제공 해야 한다는 점에 유의 하세요.</span><span class="sxs-lookup"><span data-stu-id="68420-125">Be noted that the credential should be provided in the Uri, if the source requires any.</span></span>

```yaml
Type: String
Parameter Sets: UriPipeline
Aliases: SrcUri, SourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68420-126">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="68420-126">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="68420-127">각 요청에 대 한 클라이언트 쪽 최대 실행 시간 (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="68420-127">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="68420-128">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="68420-128">-CloudBlob</span></span>
<span data-ttu-id="68420-129">Azure Storage 클라이언트 라이브러리의 CloudBlob 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="68420-129">CloudBlob object from Azure Storage Client library.</span></span> <span data-ttu-id="68420-130">이를 만들거나 Get-AzureStorageBlob cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="68420-130">You can create it or use Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: CloudPageBlob
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases: SrcICloudBlob, SrcCloudBlob, ICloudBlob, SourceICloudBlob, SourceCloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68420-131">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="68420-131">-CloudBlobContainer</span></span>
<span data-ttu-id="68420-132">Azure Storage 클라이언트 라이브러리의 CloudBlobContainer 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="68420-132">CloudBlobContainer object from Azure Storage Client library.</span></span> <span data-ttu-id="68420-133">이를 만들거나 Get-AzureStorageContainer cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="68420-133">You can create it or use Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases: SourceCloudBlobContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68420-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="68420-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="68420-135">동시 비동기 작업의 전체 양입니다.</span><span class="sxs-lookup"><span data-stu-id="68420-135">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="68420-136">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="68420-136">The default value is 10.</span></span>

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

### <span data-ttu-id="68420-137">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="68420-137">-Context</span></span>
<span data-ttu-id="68420-138">원본 Azure 저장소 컨텍스트입니다.</span><span class="sxs-lookup"><span data-stu-id="68420-138">Source Azure Storage Context.</span></span> <span data-ttu-id="68420-139">New-AzureStorageContext cmdlet을 통해 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="68420-139">You can create it by New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ContainerInstance, BlobInstance, BlobInstanceToBlobInstance, ContainerName
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

```yaml
Type: IStorageContext
Parameter Sets: UriPipeline
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="68420-140">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="68420-140">-DestBlob</span></span>
<span data-ttu-id="68420-141">대상 blob 이름</span><span class="sxs-lookup"><span data-stu-id="68420-141">Destination blob name</span></span>

```yaml
Type: String
Parameter Sets: ContainerInstance, BlobInstance, ContainerName
Aliases: DestinationBlob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: UriPipeline
Aliases: DestinationBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68420-142">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="68420-142">-DestCloudBlob</span></span>
<span data-ttu-id="68420-143">Destination CloudBlob 개체</span><span class="sxs-lookup"><span data-stu-id="68420-143">Destination CloudBlob object</span></span>

```yaml
Type: CloudPageBlob
Parameter Sets: BlobInstanceToBlobInstance
Aliases: DestICloudBlob, DestinationCloudBlob, DestinationICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68420-144">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="68420-144">-DestContainer</span></span>
<span data-ttu-id="68420-145">대상 컨테이너 이름</span><span class="sxs-lookup"><span data-stu-id="68420-145">Destination container name</span></span>

```yaml
Type: String
Parameter Sets: ContainerInstance, BlobInstance, ContainerName, UriPipeline
Aliases: DestinationContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68420-146">DestContext</span><span class="sxs-lookup"><span data-stu-id="68420-146">-DestContext</span></span>
<span data-ttu-id="68420-147">대상 Azure 저장소 컨텍스트입니다.</span><span class="sxs-lookup"><span data-stu-id="68420-147">Destination Azure Storage Context.</span></span> <span data-ttu-id="68420-148">New-AzureStorageContext cmdlet을 통해 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="68420-148">You can create it by New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: DestinationContext

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68420-149">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="68420-149">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="68420-150">각 요청에 대 한 서버 시간 제한 (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="68420-150">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="68420-151">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="68420-151">-SrcBlob</span></span>
<span data-ttu-id="68420-152">원본 페이지 blob 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="68420-152">Source page blob name.</span></span>

```yaml
Type: String
Parameter Sets: ContainerInstance, ContainerName
Aliases: SourceBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68420-153">-SrcBlobSnapshotTime</span><span class="sxs-lookup"><span data-stu-id="68420-153">-SrcBlobSnapshotTime</span></span>
<span data-ttu-id="68420-154">원본 페이지 blob 스냅숏 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="68420-154">Source page blob snapshot time.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ContainerInstance, ContainerName
Aliases: SourceBlobSnapshotTime

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68420-155">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="68420-155">-SrcContainer</span></span>
<span data-ttu-id="68420-156">원본 컨테이너 이름</span><span class="sxs-lookup"><span data-stu-id="68420-156">Source Container name</span></span>

```yaml
Type: String
Parameter Sets: ContainerName
Aliases: SourceContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68420-157">-확인</span><span class="sxs-lookup"><span data-stu-id="68420-157">-Confirm</span></span>
<span data-ttu-id="68420-158">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="68420-158">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68420-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68420-159">-WhatIf</span></span>
<span data-ttu-id="68420-160">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="68420-160">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="68420-161">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="68420-161">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68420-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68420-162">CommonParameters</span></span>
<span data-ttu-id="68420-163">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="68420-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68420-164">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68420-164">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68420-165">입력</span><span class="sxs-lookup"><span data-stu-id="68420-165">INPUTS</span></span>

### <span data-ttu-id="68420-166">WindowsAzure. c c a Blob</span><span class="sxs-lookup"><span data-stu-id="68420-166">Microsoft.WindowsAzure.Storage.Blob.CloudPageBlob</span></span>
<span data-ttu-id="68420-167">WindowsAzure. CloudBlobContainer. WindowsAzure. m a. 저장소. AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="68420-167">Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer System.String Microsoft.WindowsAzure.Commands.Common.Storage.AzureStorageContext</span></span>

## <span data-ttu-id="68420-168">출력</span><span class="sxs-lookup"><span data-stu-id="68420-168">OUTPUTS</span></span>

### <span data-ttu-id="68420-169">WindowsAzure. ResourceModel. m b m.</span><span class="sxs-lookup"><span data-stu-id="68420-169">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="68420-170">상속자</span><span class="sxs-lookup"><span data-stu-id="68420-170">NOTES</span></span>

## <span data-ttu-id="68420-171">관련 링크</span><span class="sxs-lookup"><span data-stu-id="68420-171">RELATED LINKS</span></span>

