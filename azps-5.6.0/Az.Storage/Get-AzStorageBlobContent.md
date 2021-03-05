---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C091D654-E113-4AE0-A6C8-24630D1294A4
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobContent.md
ms.openlocfilehash: b3c2e5809cf2f9aa13a11600351c64a825caf5d9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002752"
---
# <span data-ttu-id="63210-101">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="63210-101">Get-AzStorageBlobContent</span></span>

## <span data-ttu-id="63210-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63210-102">SYNOPSIS</span></span>
<span data-ttu-id="63210-103">저장소 Blob을 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="63210-103">Downloads a storage blob.</span></span>

## <span data-ttu-id="63210-104">구문</span><span class="sxs-lookup"><span data-stu-id="63210-104">SYNTAX</span></span>

### <span data-ttu-id="63210-105">ReceiveManual(기본값)</span><span class="sxs-lookup"><span data-stu-id="63210-105">ReceiveManual (Default)</span></span>
```
Get-AzStorageBlobContent [-Blob] <String> [-Container] <String> [-Destination <String>] [-CheckMd5] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="63210-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="63210-106">BlobPipeline</span></span>
```
Get-AzStorageBlobContent -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] [-Destination <String>]
 [-CheckMd5] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63210-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="63210-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobContent -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Destination <String>]
 [-CheckMd5] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63210-108">설명</span><span class="sxs-lookup"><span data-stu-id="63210-108">DESCRIPTION</span></span>
<span data-ttu-id="63210-109">**Get-AzStorageBlobContent** cmdlet은 지정된 저장소 Blob을 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="63210-109">The **Get-AzStorageBlobContent** cmdlet downloads the specified storage blob.</span></span>
<span data-ttu-id="63210-110">Blob 이름이 로컬 컴퓨터에 유효하지 않은 경우 이 cmdlet은 가능한 경우 자동으로 해결됩니다.</span><span class="sxs-lookup"><span data-stu-id="63210-110">If the blob name is not valid for the local computer, this cmdlet automatically resolves it if it is possible.</span></span>

## <span data-ttu-id="63210-111">예제</span><span class="sxs-lookup"><span data-stu-id="63210-111">EXAMPLES</span></span>

### <span data-ttu-id="63210-112">예제 1: 이름으로 Blob 콘텐츠 다운로드</span><span class="sxs-lookup"><span data-stu-id="63210-112">Example 1: Download blob content by name</span></span>
```
PS C:\>Get-AzStorageBlobContent -Container "ContainerName" -Blob "Blob" -Destination "C:\test\"
```

<span data-ttu-id="63210-113">이 명령은 이름으로 Blob을 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="63210-113">This command downloads a blob by name.</span></span>

### <span data-ttu-id="63210-114">예제 2: 파이프라인을 사용하여 Blob 콘텐츠 다운로드</span><span class="sxs-lookup"><span data-stu-id="63210-114">Example 2: Download blob content using the pipeline</span></span>
```
PS C:\>Get-AzStorageBlob -Container containername -Blob blobname | Get-AzStorageBlobContent
```

<span data-ttu-id="63210-115">이 명령은 파이프라인을 사용하여 Blob 콘텐츠를 찾고 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="63210-115">This command uses the pipeline to find and download blob content.</span></span>

### <span data-ttu-id="63210-116">예제 3: 파이프라인 및 와일드카드 문자를 사용하여 Blob 콘텐츠 다운로드</span><span class="sxs-lookup"><span data-stu-id="63210-116">Example 3: Download blob content using the pipeline and a wildcard character</span></span>
```
PS C:\>Get-AzStorageContainer container* | Get-AzStorageBlobContent -Blob "cbox.exe" -Destination "C:\test"
```

<span data-ttu-id="63210-117">이 예제에서는 Asterisk 와일드카드 문자 및 파이프라인을 사용하여 Blob 콘텐츠를 찾고 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="63210-117">This example uses the asterisk wildcard character and the pipeline to find and download blob content.</span></span>

### <span data-ttu-id="63210-118">예제 4: Blob 개체를 다운로드하고 변수에 저장한 다음 Blob 개체로 Blob 콘텐츠를 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="63210-118">Example 4: Get a blob object and save it in a variable, then download blob content with the blob object</span></span>
```
PS C:\>$blob = Get-AzStorageBlob -Container containername -Blob blobname 
PS C:\>Get-AzStorageBlobContent -CloudBlob $blob.ICloudBlob -Destination "C:\test"
```

<span data-ttu-id="63210-119">이 예제에서는 먼저 Blob 개체를 구하고 변수에 저장한 다음 Blob 개체로 Blob 콘텐츠를 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="63210-119">This example first get a blob object and save it in a variable, then download blob content with the blob object.</span></span> 

## <span data-ttu-id="63210-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="63210-120">PARAMETERS</span></span>

### <span data-ttu-id="63210-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="63210-121">-AsJob</span></span>
<span data-ttu-id="63210-122">백그라운드에서 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="63210-122">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="63210-123">-Blob</span><span class="sxs-lookup"><span data-stu-id="63210-123">-Blob</span></span>
<span data-ttu-id="63210-124">다운로드할 Blob의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="63210-124">Specifies the name of the blob to be downloaded.</span></span>

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

### <span data-ttu-id="63210-125">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="63210-125">-BlobBaseClient</span></span>
<span data-ttu-id="63210-126">BlobBaseClient 개체</span><span class="sxs-lookup"><span data-stu-id="63210-126">BlobBaseClient Object</span></span>

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

### <span data-ttu-id="63210-127">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="63210-127">-CheckMd5</span></span>
<span data-ttu-id="63210-128">다운로드한 파일에 대한 Md5 합계를 확인할지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="63210-128">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

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

### <span data-ttu-id="63210-129">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="63210-129">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="63210-130">하나의 서비스 요청에 대해 클라이언트 쪽 시간 간격(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="63210-130">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="63210-131">지정된 간격에서 이전 호출이 실패하면 이 cmdlet에서 요청을 다시 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="63210-131">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="63210-132">간격이 경과하기 전에 이 cmdlet에서 성공적인 응답을 받지 못하면 이 cmdlet은 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="63210-132">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="63210-133">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="63210-133">-CloudBlob</span></span>
<span data-ttu-id="63210-134">클라우드 Blob을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="63210-134">Specifies a cloud blob.</span></span>
<span data-ttu-id="63210-135">**CloudBlob** 개체를 얻으면 Get-AzStorageBlob cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="63210-135">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="63210-136">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="63210-136">-CloudBlobContainer</span></span>
<span data-ttu-id="63210-137">Azure Storage 클라이언트 라이브러리에서 **CloudBlobContainer** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="63210-137">Specifies a **CloudBlobContainer** object from the Azure storage client library.</span></span>
<span data-ttu-id="63210-138">cmdlet을 만들거나 Get-AzStorageContainer 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="63210-138">You can create it or use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="63210-139">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="63210-139">-ConcurrentTaskCount</span></span>
<span data-ttu-id="63210-140">최대 동시 네트워크 호출을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="63210-140">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="63210-141">이 매개 변수를 사용하여 최대 동시 네트워크 호출 수를 지정하여 로컬 CPU 및 대역폭 사용량을 제한하는 동시성 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="63210-141">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="63210-142">지정된 값은 절대 개수로 코어 수에 곱하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="63210-142">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="63210-143">이 매개 변수는 초당 100킬로비트와 같은 대역폭이 낮은 환경에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="63210-143">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="63210-144">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="63210-144">The default value is 10.</span></span>

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

### <span data-ttu-id="63210-145">-Container</span><span class="sxs-lookup"><span data-stu-id="63210-145">-Container</span></span>
<span data-ttu-id="63210-146">다운로드할 Blob이 있는 컨테이너의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="63210-146">Specifies the name of container that has the blob you want to download.</span></span>

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

### <span data-ttu-id="63210-147">-Context</span><span class="sxs-lookup"><span data-stu-id="63210-147">-Context</span></span>
<span data-ttu-id="63210-148">Blob 콘텐츠를 다운로드할 Azure Storage 계정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="63210-148">Specifies the Azure storage account from which you want to download blob content.</span></span>
<span data-ttu-id="63210-149">저장소 컨텍스트를 New-AzStorageContext cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="63210-149">You can use the New-AzStorageContext cmdlet to create a storage context.</span></span>

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

### <span data-ttu-id="63210-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63210-150">-DefaultProfile</span></span>
<span data-ttu-id="63210-151">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="63210-151">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63210-152">-대상</span><span class="sxs-lookup"><span data-stu-id="63210-152">-Destination</span></span>
<span data-ttu-id="63210-153">다운로드한 파일을 저장할 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="63210-153">Specifies the location to store the downloaded file.</span></span>

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

### <span data-ttu-id="63210-154">-Force</span><span class="sxs-lookup"><span data-stu-id="63210-154">-Force</span></span>
<span data-ttu-id="63210-155">확인 없이 기존 파일을 덮어 덮어 덮습니다.</span><span class="sxs-lookup"><span data-stu-id="63210-155">Overwrites an existing file without confirmation.</span></span>

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

### <span data-ttu-id="63210-156">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="63210-156">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="63210-157">요청에 대해 서비스 쪽 시간 시간 간격(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="63210-157">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="63210-158">서비스가 요청을 처리하기 전에 지정된 간격이 경과하면 저장소 서비스가 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="63210-158">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="63210-159">-확인</span><span class="sxs-lookup"><span data-stu-id="63210-159">-Confirm</span></span>
<span data-ttu-id="63210-160">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="63210-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63210-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63210-161">-WhatIf</span></span>
<span data-ttu-id="63210-162">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="63210-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63210-163">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="63210-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63210-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63210-164">CommonParameters</span></span>
<span data-ttu-id="63210-165">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="63210-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63210-166">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="63210-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63210-167">입력</span><span class="sxs-lookup"><span data-stu-id="63210-167">INPUTS</span></span>

### <span data-ttu-id="63210-168">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="63210-168">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="63210-169">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="63210-169">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="63210-170">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="63210-170">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="63210-171">출력</span><span class="sxs-lookup"><span data-stu-id="63210-171">OUTPUTS</span></span>

### <span data-ttu-id="63210-172">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="63210-172">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="63210-173">참고 사항</span><span class="sxs-lookup"><span data-stu-id="63210-173">NOTES</span></span>
* <span data-ttu-id="63210-174">로컬 컴퓨터에 Blob 이름이 올바르지 않은 경우 이 cmdlet은 가능한 경우 자동으로 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="63210-174">If the blob name is invalid for local computer, this cmdlet autoresolves it, if it is possible.</span></span>

## <span data-ttu-id="63210-175">관련 링크</span><span class="sxs-lookup"><span data-stu-id="63210-175">RELATED LINKS</span></span>

[<span data-ttu-id="63210-176">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="63210-176">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)

[<span data-ttu-id="63210-177">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="63210-177">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="63210-178">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="63210-178">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)
