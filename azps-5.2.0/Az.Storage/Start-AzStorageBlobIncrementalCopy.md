---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/start-azstorageblobincrementalcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobIncrementalCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobIncrementalCopy.md
ms.openlocfilehash: 126d89ca600c9696a1300054c2dc82cb1d9f5d2a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329062"
---
# <span data-ttu-id="04f05-101">Start-AzStorageBlobIncrementalCopy</span><span class="sxs-lookup"><span data-stu-id="04f05-101">Start-AzStorageBlobIncrementalCopy</span></span>

## <span data-ttu-id="04f05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04f05-102">SYNOPSIS</span></span>
<span data-ttu-id="04f05-103">페이지 Blob 스냅숏에서 지정된 대상 페이지 Blob으로 증분 복사 작업을 시작하세요.</span><span class="sxs-lookup"><span data-stu-id="04f05-103">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>

## <span data-ttu-id="04f05-104">구문</span><span class="sxs-lookup"><span data-stu-id="04f05-104">SYNTAX</span></span>

### <span data-ttu-id="04f05-105">ContainerInstance(기본값)</span><span class="sxs-lookup"><span data-stu-id="04f05-105">ContainerInstance (Default)</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlobContainer <CloudBlobContainer> -SrcBlob <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04f05-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="04f05-106">BlobInstance</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04f05-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="04f05-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestCloudBlob <CloudPageBlob>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04f05-108">ContainerName</span><span class="sxs-lookup"><span data-stu-id="04f05-108">ContainerName</span></span>
```
Start-AzStorageBlobIncrementalCopy -SrcBlob <String> -SrcContainer <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04f05-109">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="04f05-109">UriPipeline</span></span>
```
Start-AzStorageBlobIncrementalCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04f05-110">설명</span><span class="sxs-lookup"><span data-stu-id="04f05-110">DESCRIPTION</span></span>
<span data-ttu-id="04f05-111">페이지 Blob 스냅숏에서 지정된 대상 페이지 Blob으로 증분 복사 작업을 시작하세요.</span><span class="sxs-lookup"><span data-stu-id="04f05-111">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>
<span data-ttu-id="04f05-112">에서 기능에 대한 자세한 내용을 https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="04f05-112">See more details of the feature in https://docs.microsoft.com/en-us/rest/api/storageservices/fileservices/incremental-copy-blob.</span></span>

## <span data-ttu-id="04f05-113">예제</span><span class="sxs-lookup"><span data-stu-id="04f05-113">EXAMPLES</span></span>

### <span data-ttu-id="04f05-114">예제 1: Blob 이름 및 스냅숏 시간으로 증분 복사 작업 시작</span><span class="sxs-lookup"><span data-stu-id="04f05-114">Example 1: Start Incremental Copy Operation by blob name and snapshot time</span></span>
```
PS C:\>Start-AzStorageBlobIncrementalCopy -SrcContainer container1 -SrcBlob blob1 -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="04f05-115">이 명령은 Blob 이름 및 스냅숏 시간으로 증분 복사 작업을 시작</span><span class="sxs-lookup"><span data-stu-id="04f05-115">This command start Incremental Copy Operation by blob name and snapshot time</span></span>

### <span data-ttu-id="04f05-116">예제 2: 원본 URI를 사용하여 증분 복사 작업 시작</span><span class="sxs-lookup"><span data-stu-id="04f05-116">Example 2: Start Incremental copy operation using source uri</span></span>
```
PS C:\>Start-AzStorageBlobIncrementalCopy -AbsoluteUri "http://www.somesite.com/somefile?snapshot=2017-04-07T10:05:40.2126635Z" -DestContainer container -DestBlob blob -DestContext $context
```

<span data-ttu-id="04f05-117">이 명령은 원본 URI를 사용하여 증분 복사 작업을 시작</span><span class="sxs-lookup"><span data-stu-id="04f05-117">This command start Incremental Copy Operation using source uri</span></span>

### <span data-ttu-id="04f05-118">예제 3: GetAzureStorageContainer에서 컨테이너 파이프라인을 사용하여 증분 복사 작업 시작</span><span class="sxs-lookup"><span data-stu-id="04f05-118">Example 3:  Start Incremental copy operation using container pipeline from GetAzureStorageContainer</span></span>
```
PS C:\>Get-AzStorageContainer -Container container1 | Start-AzStorageBlobIncrementalCopy -SrcBlob blob  -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2
```

<span data-ttu-id="04f05-119">이 명령은 GetAzureStorageContainer의 컨테이너 파이프라인을 사용하여 증분 복사 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="04f05-119">This command start Incremental Copy Operation using container pipeline from GetAzureStorageContainer</span></span>

### <span data-ttu-id="04f05-120">예제 4: Blob 이름을 통해 CloudPageBlob 개체에서 대상 Blob으로 증분 복사 작업 시작</span><span class="sxs-lookup"><span data-stu-id="04f05-120">Example 4:  start Incremental copy operation from CloudPageBlob object to destination blob with blob name</span></span>
```
PS C:\>$srcBlobSnapshot = Get-AzStorageBlob -Container container1 -prefix blob1| ?{$_.ICloudBlob.IsSnapshot})[0]
PS C:\>Start-AzStorageBlobIncrementalCopy -CloudBlob $srcBlobSnapshot.ICloudBlob -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="04f05-121">이 명령은 Blob 이름을 사용하여 CloudPageBlob 개체에서 대상 Blob으로 증분 복사 작업을 시작</span><span class="sxs-lookup"><span data-stu-id="04f05-121">This command start Incremental Copy Operation from CloudPageBlob object to destination blob with blob name</span></span>

## <span data-ttu-id="04f05-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="04f05-122">PARAMETERS</span></span>

### <span data-ttu-id="04f05-123">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="04f05-123">-AbsoluteUri</span></span>
<span data-ttu-id="04f05-124">원본에 대한 절대 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="04f05-124">Absolute Uri to the source.</span></span> <span data-ttu-id="04f05-125">원본에 필요한 경우 Uri에 자격 증명을 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="04f05-125">Be noted that the credential should be provided in the Uri, if the source requires any.</span></span>

```yaml
Type: System.String
Parameter Sets: UriPipeline
Aliases: SrcUri, SourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04f05-126">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="04f05-126">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="04f05-127">각 요청에 대한 클라이언트 쪽 최대 실행 시간(초)입니다.</span><span class="sxs-lookup"><span data-stu-id="04f05-127">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="04f05-128">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="04f05-128">-CloudBlob</span></span>
<span data-ttu-id="04f05-129">Azure Storage 클라이언트 라이브러리의 CloudBlob 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="04f05-129">CloudBlob object from Azure Storage Client library.</span></span> <span data-ttu-id="04f05-130">cmdlet을 만들거나 cmdlet을 Get-AzStorageBlob 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04f05-130">You can create it or use Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudPageBlob
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases: SrcICloudBlob, SrcCloudBlob, ICloudBlob, SourceICloudBlob, SourceCloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="04f05-131">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="04f05-131">-CloudBlobContainer</span></span>
<span data-ttu-id="04f05-132">Azure Storage 클라이언트 라이브러리의 CloudBlobContainer 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="04f05-132">CloudBlobContainer object from Azure Storage Client library.</span></span> <span data-ttu-id="04f05-133">cmdlet을 만들거나 cmdlet을 Get-AzStorageContainer 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04f05-133">You can create it or use Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases: SourceCloudBlobContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="04f05-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="04f05-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="04f05-135">동시 비동기 작업의 총 양입니다.</span><span class="sxs-lookup"><span data-stu-id="04f05-135">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="04f05-136">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="04f05-136">The default value is 10.</span></span>

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

### <span data-ttu-id="04f05-137">-Context</span><span class="sxs-lookup"><span data-stu-id="04f05-137">-Context</span></span>
<span data-ttu-id="04f05-138">원본 Azure Storage 컨텍스트입니다.</span><span class="sxs-lookup"><span data-stu-id="04f05-138">Source Azure Storage Context.</span></span> <span data-ttu-id="04f05-139">cmdlet을 사용하여 만들 New-AzStorageContext 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04f05-139">You can create it by New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ContainerInstance, BlobInstance, BlobInstanceToBlobInstance, ContainerName
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: UriPipeline
Aliases: SrcContext, SourceContext

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="04f05-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04f05-140">-DefaultProfile</span></span>
<span data-ttu-id="04f05-141">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="04f05-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04f05-142">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="04f05-142">-DestBlob</span></span>
<span data-ttu-id="04f05-143">대상 Blob 이름</span><span class="sxs-lookup"><span data-stu-id="04f05-143">Destination blob name</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerInstance, BlobInstance, ContainerName
Aliases: DestinationBlob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UriPipeline
Aliases: DestinationBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04f05-144">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="04f05-144">-DestCloudBlob</span></span>
<span data-ttu-id="04f05-145">Destination CloudBlob 개체</span><span class="sxs-lookup"><span data-stu-id="04f05-145">Destination CloudBlob object</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudPageBlob
Parameter Sets: BlobInstanceToBlobInstance
Aliases: DestICloudBlob, DestinationCloudBlob, DestinationICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04f05-146">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="04f05-146">-DestContainer</span></span>
<span data-ttu-id="04f05-147">대상 컨테이너 이름</span><span class="sxs-lookup"><span data-stu-id="04f05-147">Destination container name</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerInstance, BlobInstance, ContainerName, UriPipeline
Aliases: DestinationContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04f05-148">-DestContext</span><span class="sxs-lookup"><span data-stu-id="04f05-148">-DestContext</span></span>
<span data-ttu-id="04f05-149">대상 Azure Storage 컨텍스트입니다.</span><span class="sxs-lookup"><span data-stu-id="04f05-149">Destination Azure Storage Context.</span></span> <span data-ttu-id="04f05-150">cmdlet을 사용하여 만들 New-AzStorageContext 있습니다.</span><span class="sxs-lookup"><span data-stu-id="04f05-150">You can create it by New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases: DestinationContext

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04f05-151">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="04f05-151">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="04f05-152">각 요청에 대한 서버 시간(초)입니다.</span><span class="sxs-lookup"><span data-stu-id="04f05-152">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="04f05-153">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="04f05-153">-SrcBlob</span></span>
<span data-ttu-id="04f05-154">원본 페이지 Blob 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="04f05-154">Source page blob name.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerInstance, ContainerName
Aliases: SourceBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04f05-155">-SrcBlobSnapshotTime</span><span class="sxs-lookup"><span data-stu-id="04f05-155">-SrcBlobSnapshotTime</span></span>
<span data-ttu-id="04f05-156">원본 페이지 Blob 스냅숏 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="04f05-156">Source page blob snapshot time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ContainerInstance, ContainerName
Aliases: SourceBlobSnapshotTime

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04f05-157">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="04f05-157">-SrcContainer</span></span>
<span data-ttu-id="04f05-158">원본 컨테이너 이름</span><span class="sxs-lookup"><span data-stu-id="04f05-158">Source Container name</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName
Aliases: SourceContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04f05-159">-Confirm</span><span class="sxs-lookup"><span data-stu-id="04f05-159">-Confirm</span></span>
<span data-ttu-id="04f05-160">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="04f05-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04f05-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04f05-161">-WhatIf</span></span>
<span data-ttu-id="04f05-162">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="04f05-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04f05-163">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="04f05-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04f05-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04f05-164">CommonParameters</span></span>
<span data-ttu-id="04f05-165">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="04f05-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04f05-166">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="04f05-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04f05-167">입력</span><span class="sxs-lookup"><span data-stu-id="04f05-167">INPUTS</span></span>

### <span data-ttu-id="04f05-168">Microsoft.Azure.Storage.Blob.CloudPageBlob</span><span class="sxs-lookup"><span data-stu-id="04f05-168">Microsoft.Azure.Storage.Blob.CloudPageBlob</span></span>

### <span data-ttu-id="04f05-169">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="04f05-169">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="04f05-170">System.String</span><span class="sxs-lookup"><span data-stu-id="04f05-170">System.String</span></span>

### <span data-ttu-id="04f05-171">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="04f05-171">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="04f05-172">출력</span><span class="sxs-lookup"><span data-stu-id="04f05-172">OUTPUTS</span></span>

### <span data-ttu-id="04f05-173">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="04f05-173">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="04f05-174">참고 사항</span><span class="sxs-lookup"><span data-stu-id="04f05-174">NOTES</span></span>

## <span data-ttu-id="04f05-175">관련 링크</span><span class="sxs-lookup"><span data-stu-id="04f05-175">RELATED LINKS</span></span>
