---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C091D654-E113-4AE0-A6C8-24630D1294A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobContent.md
ms.openlocfilehash: eec7d4b29f752d3bf302dc9f5c35fa5c6da51c6f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349682"
---
# <span data-ttu-id="ec3ff-101">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ec3ff-101">Get-AzStorageBlobContent</span></span>

## <span data-ttu-id="ec3ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec3ff-102">SYNOPSIS</span></span>
<span data-ttu-id="ec3ff-103">저장소 Blob을 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="ec3ff-103">Downloads a storage blob.</span></span>

## <span data-ttu-id="ec3ff-104">구문</span><span class="sxs-lookup"><span data-stu-id="ec3ff-104">SYNTAX</span></span>

### <span data-ttu-id="ec3ff-105">ReceiveManual(기본값)</span><span class="sxs-lookup"><span data-stu-id="ec3ff-105">ReceiveManual (Default)</span></span>
```
Get-AzStorageBlobContent [-Blob] <String> [-Container] <String> [-Destination <String>] [-CheckMd5] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ec3ff-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="ec3ff-106">BlobPipeline</span></span>
```
Get-AzStorageBlobContent -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] [-Destination <String>]
 [-CheckMd5] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec3ff-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="ec3ff-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobContent -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Destination <String>]
 [-CheckMd5] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec3ff-108">설명</span><span class="sxs-lookup"><span data-stu-id="ec3ff-108">DESCRIPTION</span></span>
<span data-ttu-id="ec3ff-109">**Get-AzStorageBlobContent** cmdlet은 지정된 저장소 Blob을 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="ec3ff-109">The **Get-AzStorageBlobContent** cmdlet downloads the specified storage blob.</span></span>
<span data-ttu-id="ec3ff-110">Blob 이름이 로컬 컴퓨터에 유효하지 않은 경우 이 cmdlet은 가능한 경우 자동으로 해결합니다.</span><span class="sxs-lookup"><span data-stu-id="ec3ff-110">If the blob name is not valid for the local computer, this cmdlet automatically resolves it if it is possible.</span></span>

## <span data-ttu-id="ec3ff-111">예제</span><span class="sxs-lookup"><span data-stu-id="ec3ff-111">EXAMPLES</span></span>

### <span data-ttu-id="ec3ff-112">예제 1: 이름으로 Blob 콘텐츠 다운로드</span><span class="sxs-lookup"><span data-stu-id="ec3ff-112">Example 1: Download blob content by name</span></span>
```
PS C:\>Get-AzStorageBlobContent -Container "ContainerName" -Blob "Blob" -Destination "C:\test\"
```

<span data-ttu-id="ec3ff-113">이 명령은 이름으로 Blob을 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="ec3ff-113">This command downloads a blob by name.</span></span>

### <span data-ttu-id="ec3ff-114">예제 2: 파이프라인을 사용하여 Blob 콘텐츠 다운로드</span><span class="sxs-lookup"><span data-stu-id="ec3ff-114">Example 2: Download blob content using the pipeline</span></span>
```
PS C:\>Get-AzStorageBlob -Container containername -Blob blobname | Get-AzStorageBlobContent
```

<span data-ttu-id="ec3ff-115">이 명령은 파이프라인을 사용하여 Blob 콘텐츠를 찾아 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="ec3ff-115">This command uses the pipeline to find and download blob content.</span></span>

### <span data-ttu-id="ec3ff-116">예제 3: 파이프라인 및 와일드카드 문자를 사용하여 Blob 콘텐츠 다운로드</span><span class="sxs-lookup"><span data-stu-id="ec3ff-116">Example 3: Download blob content using the pipeline and a wildcard character</span></span>
```
PS C:\>Get-AzStorageContainer container* | Get-AzStorageBlobContent -Blob "cbox.exe" -Destination "C:\test"
```

<span data-ttu-id="ec3ff-117">이 예제에서는 추가 와일드카드 문자와 파이프라인을 사용하여 Blob 콘텐츠를 찾아 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="ec3ff-117">This example uses the asterisk wildcard character and the pipeline to find and download blob content.</span></span>

### <span data-ttu-id="ec3ff-118">예제 4: Blob 개체를 다운로드하고 변수에 저장한 다음 Blob 개체가 있는 Blob 콘텐츠를 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="ec3ff-118">Example 4: Get a blob object and save it in a variable, then download blob content with the blob object</span></span>
```
PS C:\>$blob = Get-AzStorageBlob -Container containername -Blob blobname 
PS C:\>Get-AzStorageBlobContent -CloudBlob $blob.ICloudBlob -Destination "C:\test"
```

<span data-ttu-id="ec3ff-119">이 예제에서는 먼저 Blob 개체를 다운로드하고 변수에 저장한 다음 Blob 개체가 있는 Blob 콘텐츠를 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="ec3ff-119">This example first get a blob object and save it in a variable, then download blob content with the blob object.</span></span> 

## <span data-ttu-id="ec3ff-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ec3ff-120">PARAMETERS</span></span>

### <span data-ttu-id="ec3ff-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ec3ff-121">-AsJob</span></span>
<span data-ttu-id="ec3ff-122">백그라운드에서 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="ec3ff-122">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="ec3ff-123">-Blob</span><span class="sxs-lookup"><span data-stu-id="ec3ff-123">-Blob</span></span>
<span data-ttu-id="ec3ff-124">다운로드할 Blob의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ec3ff-124">Specifies the name of the blob to be downloaded.</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual, ContainerPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec3ff-125">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="ec3ff-125">-BlobBaseClient</span></span>
<span data-ttu-id="ec3ff-126">BlobBaseClient 개체</span><span class="sxs-lookup"><span data-stu-id="ec3ff-126">BlobBaseClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.Specialized.BlobBaseClient
Parameter Sets: BlobPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec3ff-127">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="ec3ff-127">-CheckMd5</span></span>
<span data-ttu-id="ec3ff-128">다운로드한 파일의 Md5 합계를 확인할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ec3ff-128">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

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

### <span data-ttu-id="ec3ff-129">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ec3ff-129">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="ec3ff-130">하나의 서비스 요청에 대해 클라이언트 쪽 시간(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ec3ff-130">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="ec3ff-131">이전 호출이 지정된 간격에서 실패하는 경우 이 cmdlet은 요청을 다시 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="ec3ff-131">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="ec3ff-132">이 cmdlet이 간격이 경과하기 전에 성공적인 응답을 받지 못하면 이 cmdlet은 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ec3ff-132">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="ec3ff-133">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="ec3ff-133">-CloudBlob</span></span>
<span data-ttu-id="ec3ff-134">클라우드 Blob을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ec3ff-134">Specifies a cloud blob.</span></span>
<span data-ttu-id="ec3ff-135">**CloudBlob 개체를 얻으면** Get-AzStorageBlob cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="ec3ff-135">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec3ff-136">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="ec3ff-136">-CloudBlobContainer</span></span>
<span data-ttu-id="ec3ff-137">Azure Storage 클라이언트 라이브러리에서 **CloudBlobContainer** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ec3ff-137">Specifies a **CloudBlobContainer** object from the Azure storage client library.</span></span>
<span data-ttu-id="ec3ff-138">cmdlet을 만들거나 Get-AzStorageContainer 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec3ff-138">You can create it or use the Get-AzStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec3ff-139">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="ec3ff-139">-ConcurrentTaskCount</span></span>
<span data-ttu-id="ec3ff-140">최대 동시 네트워크 호출을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ec3ff-140">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="ec3ff-141">이 매개 변수를 사용하여 최대 동시 네트워크 호출 수를 지정하여 동시성으로 로컬 CPU 및 대역폭 사용량을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec3ff-141">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="ec3ff-142">지정된 값은 절대 개수로, 코어 수에 곱하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ec3ff-142">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="ec3ff-143">이 매개 변수는 초당 100킬로비트와 같은 낮은 대역폭 환경에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec3ff-143">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="ec3ff-144">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="ec3ff-144">The default value is 10.</span></span>

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

### <span data-ttu-id="ec3ff-145">-Container</span><span class="sxs-lookup"><span data-stu-id="ec3ff-145">-Container</span></span>
<span data-ttu-id="ec3ff-146">다운로드하려는 Blob이 있는 컨테이너의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ec3ff-146">Specifies the name of container that has the blob you want to download.</span></span>

```yaml
Type: System.String
Parameter Sets: ReceiveManual
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec3ff-147">-Context</span><span class="sxs-lookup"><span data-stu-id="ec3ff-147">-Context</span></span>
<span data-ttu-id="ec3ff-148">Blob 콘텐츠를 다운로드하려는 Azure Storage 계정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ec3ff-148">Specifies the Azure storage account from which you want to download blob content.</span></span>
<span data-ttu-id="ec3ff-149">New-AzStorageContext cmdlet을 사용하여 저장소 컨텍스트를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ec3ff-149">You can use the New-AzStorageContext cmdlet to create a storage context.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec3ff-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec3ff-150">-DefaultProfile</span></span>
<span data-ttu-id="ec3ff-151">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ec3ff-151">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec3ff-152">-Destination</span><span class="sxs-lookup"><span data-stu-id="ec3ff-152">-Destination</span></span>
<span data-ttu-id="ec3ff-153">다운로드한 파일을 저장할 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ec3ff-153">Specifies the location to store the downloaded file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Path

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec3ff-154">-Force</span><span class="sxs-lookup"><span data-stu-id="ec3ff-154">-Force</span></span>
<span data-ttu-id="ec3ff-155">확인 없이 기존 파일을 덮어 덮어 습니다.</span><span class="sxs-lookup"><span data-stu-id="ec3ff-155">Overwrites an existing file without confirmation.</span></span>

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

### <span data-ttu-id="ec3ff-156">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ec3ff-156">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="ec3ff-157">요청에 대한 서비스 쪽 시간제한 간격(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ec3ff-157">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="ec3ff-158">지정된 간격이 서비스에서 요청을 처리하기 전에 경과하면 저장소 서비스가 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ec3ff-158">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="ec3ff-159">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ec3ff-159">-Confirm</span></span>
<span data-ttu-id="ec3ff-160">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec3ff-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec3ff-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec3ff-161">-WhatIf</span></span>
<span data-ttu-id="ec3ff-162">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ec3ff-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec3ff-163">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ec3ff-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec3ff-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec3ff-164">CommonParameters</span></span>
<span data-ttu-id="ec3ff-165">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ec3ff-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec3ff-166">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ec3ff-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec3ff-167">입력</span><span class="sxs-lookup"><span data-stu-id="ec3ff-167">INPUTS</span></span>

### <span data-ttu-id="ec3ff-168">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="ec3ff-168">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="ec3ff-169">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="ec3ff-169">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="ec3ff-170">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ec3ff-170">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ec3ff-171">출력</span><span class="sxs-lookup"><span data-stu-id="ec3ff-171">OUTPUTS</span></span>

### <span data-ttu-id="ec3ff-172">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="ec3ff-172">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="ec3ff-173">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ec3ff-173">NOTES</span></span>
* <span data-ttu-id="ec3ff-174">로컬 컴퓨터에 Blob 이름이 올바르지 않은 경우 이 cmdlet은 가능한 경우 자동으로 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="ec3ff-174">If the blob name is invalid for local computer, this cmdlet autoresolves it, if it is possible.</span></span>

## <span data-ttu-id="ec3ff-175">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ec3ff-175">RELATED LINKS</span></span>

[<span data-ttu-id="ec3ff-176">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="ec3ff-176">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)

[<span data-ttu-id="ec3ff-177">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="ec3ff-177">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="ec3ff-178">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="ec3ff-178">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)
