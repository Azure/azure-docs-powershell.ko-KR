---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/start-azstorageblobincrementalcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobIncrementalCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobIncrementalCopy.md
ms.openlocfilehash: 772e97611d81362ffb3becea8875826110e822a9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002224"
---
# <span data-ttu-id="af832-101">Start-AzStorageBlobIncrementalCopy</span><span class="sxs-lookup"><span data-stu-id="af832-101">Start-AzStorageBlobIncrementalCopy</span></span>

## <span data-ttu-id="af832-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af832-102">SYNOPSIS</span></span>
<span data-ttu-id="af832-103">페이지 Blob 스냅숏에서 지정된 대상 페이지 Blob으로 증분 복사 작업을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="af832-103">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>

## <span data-ttu-id="af832-104">구문</span><span class="sxs-lookup"><span data-stu-id="af832-104">SYNTAX</span></span>

### <span data-ttu-id="af832-105">ContainerInstance(기본값)</span><span class="sxs-lookup"><span data-stu-id="af832-105">ContainerInstance (Default)</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlobContainer <CloudBlobContainer> -SrcBlob <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af832-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="af832-106">BlobInstance</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af832-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="af832-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobIncrementalCopy -CloudBlob <CloudPageBlob> -DestCloudBlob <CloudPageBlob>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af832-108">ContainerName</span><span class="sxs-lookup"><span data-stu-id="af832-108">ContainerName</span></span>
```
Start-AzStorageBlobIncrementalCopy -SrcBlob <String> -SrcContainer <String>
 -SrcBlobSnapshotTime <DateTimeOffset> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af832-109">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="af832-109">UriPipeline</span></span>
```
Start-AzStorageBlobIncrementalCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af832-110">설명</span><span class="sxs-lookup"><span data-stu-id="af832-110">DESCRIPTION</span></span>
<span data-ttu-id="af832-111">페이지 Blob 스냅숏에서 지정된 대상 페이지 Blob으로 증분 복사 작업을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="af832-111">Start an Incremental copy operation from a Page blob snapshot to the specified destination Page blob.</span></span>
<span data-ttu-id="af832-112">에서 기능에 대한 자세한 내용을 https://docs.microsoft.com/rest/api/storageservices/fileservices/incremental-copy-blob 참조합니다.</span><span class="sxs-lookup"><span data-stu-id="af832-112">See more details of the feature in https://docs.microsoft.com/rest/api/storageservices/fileservices/incremental-copy-blob.</span></span>

## <span data-ttu-id="af832-113">예제</span><span class="sxs-lookup"><span data-stu-id="af832-113">EXAMPLES</span></span>

### <span data-ttu-id="af832-114">예제 1: Blob 이름 및 스냅숏 시간으로 증분 복사 작업 시작</span><span class="sxs-lookup"><span data-stu-id="af832-114">Example 1: Start Incremental Copy Operation by blob name and snapshot time</span></span>
```
PS C:\>Start-AzStorageBlobIncrementalCopy -SrcContainer container1 -SrcBlob blob1 -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="af832-115">이 명령은 Blob 이름 및 스냅숏 시간으로 증분 복사 작업을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="af832-115">This command start Incremental Copy Operation by blob name and snapshot time</span></span>

### <span data-ttu-id="af832-116">예제 2: 원본 uri를 사용하여 증분 복사 작업 시작</span><span class="sxs-lookup"><span data-stu-id="af832-116">Example 2: Start Incremental copy operation using source uri</span></span>
```
PS C:\>Start-AzStorageBlobIncrementalCopy -AbsoluteUri "http://www.somesite.com/somefile?snapshot=2017-04-07T10:05:40.2126635Z" -DestContainer container -DestBlob blob -DestContext $context
```

<span data-ttu-id="af832-117">이 명령은 원본 uri를 사용하여 증분 복사 작업을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="af832-117">This command start Incremental Copy Operation using source uri</span></span>

### <span data-ttu-id="af832-118">예제 3: GetAzureStorageContainer에서 컨테이너 파이프라인을 사용하여 증분 복사 작업 시작</span><span class="sxs-lookup"><span data-stu-id="af832-118">Example 3:  Start Incremental copy operation using container pipeline from GetAzureStorageContainer</span></span>
```
PS C:\>Get-AzStorageContainer -Container container1 | Start-AzStorageBlobIncrementalCopy -SrcBlob blob  -SrcBlobSnapshotTime "04/07/2017 09:55:36.1190229 AM +00:00" -DestContainer container2
```

<span data-ttu-id="af832-119">이 명령은 GetAzureStorageContainer에서 컨테이너 파이프라인을 사용하여 증분 복사 작업을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="af832-119">This command start Incremental Copy Operation using container pipeline from GetAzureStorageContainer</span></span>

### <span data-ttu-id="af832-120">예제 4: Blob 이름으로 CloudPageBlob 개체에서 대상 Blob으로 증분 복사 작업 시작</span><span class="sxs-lookup"><span data-stu-id="af832-120">Example 4:  start Incremental copy operation from CloudPageBlob object to destination blob with blob name</span></span>
```
PS C:\>$srcBlobSnapshot = Get-AzStorageBlob -Container container1 -prefix blob1| ?{$_.ICloudBlob.IsSnapshot})[0]
PS C:\>Start-AzStorageBlobIncrementalCopy -CloudBlob $srcBlobSnapshot.ICloudBlob -DestContainer container2 -DestBlob blob2
```

<span data-ttu-id="af832-121">이 명령은 CloudPageBlob 개체에서 Blob 이름으로 대상 Blob으로 증분 복사 작업을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="af832-121">This command start Incremental Copy Operation from CloudPageBlob object to destination blob with blob name</span></span>

## <span data-ttu-id="af832-122">매개 변수</span><span class="sxs-lookup"><span data-stu-id="af832-122">PARAMETERS</span></span>

### <span data-ttu-id="af832-123">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="af832-123">-AbsoluteUri</span></span>
<span data-ttu-id="af832-124">원본에 대한 절대 Uri입니다.</span><span class="sxs-lookup"><span data-stu-id="af832-124">Absolute Uri to the source.</span></span> <span data-ttu-id="af832-125">원본에 자격 증명이 필요한 경우 Uri에 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="af832-125">Be noted that the credential should be provided in the Uri, if the source requires any.</span></span>

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

### <span data-ttu-id="af832-126">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="af832-126">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="af832-127">클라이언트 쪽에서 각 요청에 대한 최대 실행 시간(초)입니다.</span><span class="sxs-lookup"><span data-stu-id="af832-127">The client side maximum execution time for each request in seconds.</span></span>

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

### <span data-ttu-id="af832-128">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="af832-128">-CloudBlob</span></span>
<span data-ttu-id="af832-129">Azure Storage 클라이언트 라이브러리의 CloudBlob 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="af832-129">CloudBlob object from Azure Storage Client library.</span></span> <span data-ttu-id="af832-130">cmdlet을 만들거나 Get-AzStorageBlob 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af832-130">You can create it or use Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="af832-131">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="af832-131">-CloudBlobContainer</span></span>
<span data-ttu-id="af832-132">Azure Storage 클라이언트 라이브러리의 CloudBlobContainer 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="af832-132">CloudBlobContainer object from Azure Storage Client library.</span></span> <span data-ttu-id="af832-133">cmdlet을 만들거나 Get-AzStorageContainer 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af832-133">You can create it or use Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="af832-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="af832-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="af832-135">동시 비동기 작업의 총 양입니다.</span><span class="sxs-lookup"><span data-stu-id="af832-135">The total amount of concurrent async tasks.</span></span>
<span data-ttu-id="af832-136">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="af832-136">The default value is 10.</span></span>

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

### <span data-ttu-id="af832-137">-Context</span><span class="sxs-lookup"><span data-stu-id="af832-137">-Context</span></span>
<span data-ttu-id="af832-138">원본 Azure Storage 컨텍스트입니다.</span><span class="sxs-lookup"><span data-stu-id="af832-138">Source Azure Storage Context.</span></span> <span data-ttu-id="af832-139">cmdlet을 사용하여 New-AzStorageContext 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af832-139">You can create it by New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="af832-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af832-140">-DefaultProfile</span></span>
<span data-ttu-id="af832-141">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="af832-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af832-142">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="af832-142">-DestBlob</span></span>
<span data-ttu-id="af832-143">대상 Blob 이름</span><span class="sxs-lookup"><span data-stu-id="af832-143">Destination blob name</span></span>

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

### <span data-ttu-id="af832-144">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="af832-144">-DestCloudBlob</span></span>
<span data-ttu-id="af832-145">대상 CloudBlob 개체</span><span class="sxs-lookup"><span data-stu-id="af832-145">Destination CloudBlob object</span></span>

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

### <span data-ttu-id="af832-146">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="af832-146">-DestContainer</span></span>
<span data-ttu-id="af832-147">대상 컨테이너 이름</span><span class="sxs-lookup"><span data-stu-id="af832-147">Destination container name</span></span>

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

### <span data-ttu-id="af832-148">-DestContext</span><span class="sxs-lookup"><span data-stu-id="af832-148">-DestContext</span></span>
<span data-ttu-id="af832-149">대상 Azure Storage 컨텍스트입니다.</span><span class="sxs-lookup"><span data-stu-id="af832-149">Destination Azure Storage Context.</span></span> <span data-ttu-id="af832-150">cmdlet을 사용하여 New-AzStorageContext 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="af832-150">You can create it by New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="af832-151">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="af832-151">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="af832-152">각 요청에 대한 서버 시간(초)입니다.</span><span class="sxs-lookup"><span data-stu-id="af832-152">The server time out for each request in seconds.</span></span>

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

### <span data-ttu-id="af832-153">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="af832-153">-SrcBlob</span></span>
<span data-ttu-id="af832-154">원본 페이지 Blob 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="af832-154">Source page blob name.</span></span>

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

### <span data-ttu-id="af832-155">-SrcBlobSnapshotTime</span><span class="sxs-lookup"><span data-stu-id="af832-155">-SrcBlobSnapshotTime</span></span>
<span data-ttu-id="af832-156">원본 페이지 Blob 스냅숏 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="af832-156">Source page blob snapshot time.</span></span>

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

### <span data-ttu-id="af832-157">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="af832-157">-SrcContainer</span></span>
<span data-ttu-id="af832-158">원본 컨테이너 이름</span><span class="sxs-lookup"><span data-stu-id="af832-158">Source Container name</span></span>

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

### <span data-ttu-id="af832-159">-확인</span><span class="sxs-lookup"><span data-stu-id="af832-159">-Confirm</span></span>
<span data-ttu-id="af832-160">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="af832-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af832-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af832-161">-WhatIf</span></span>
<span data-ttu-id="af832-162">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="af832-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af832-163">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="af832-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af832-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af832-164">CommonParameters</span></span>
<span data-ttu-id="af832-165">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="af832-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af832-166">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="af832-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af832-167">입력</span><span class="sxs-lookup"><span data-stu-id="af832-167">INPUTS</span></span>

### <span data-ttu-id="af832-168">Microsoft.Azure.Storage.Blob.CloudPageBlob</span><span class="sxs-lookup"><span data-stu-id="af832-168">Microsoft.Azure.Storage.Blob.CloudPageBlob</span></span>

### <span data-ttu-id="af832-169">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="af832-169">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="af832-170">System.String</span><span class="sxs-lookup"><span data-stu-id="af832-170">System.String</span></span>

### <span data-ttu-id="af832-171">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="af832-171">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="af832-172">출력</span><span class="sxs-lookup"><span data-stu-id="af832-172">OUTPUTS</span></span>

### <span data-ttu-id="af832-173">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="af832-173">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="af832-174">참고 사항</span><span class="sxs-lookup"><span data-stu-id="af832-174">NOTES</span></span>

## <span data-ttu-id="af832-175">관련 링크</span><span class="sxs-lookup"><span data-stu-id="af832-175">RELATED LINKS</span></span>
