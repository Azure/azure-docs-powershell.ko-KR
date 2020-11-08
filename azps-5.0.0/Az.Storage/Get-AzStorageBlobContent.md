---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C091D654-E113-4AE0-A6C8-24630D1294A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobContent.md
ms.openlocfilehash: eec7d4b29f752d3bf302dc9f5c35fa5c6da51c6f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216017"
---
# <span data-ttu-id="a4360-101">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a4360-101">Get-AzStorageBlobContent</span></span>

## <span data-ttu-id="a4360-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4360-102">SYNOPSIS</span></span>
<span data-ttu-id="a4360-103">저장소 blob을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4360-103">Downloads a storage blob.</span></span>

## <span data-ttu-id="a4360-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a4360-104">SYNTAX</span></span>

### <span data-ttu-id="a4360-105">ReceiveManual (기본값)</span><span class="sxs-lookup"><span data-stu-id="a4360-105">ReceiveManual (Default)</span></span>
```
Get-AzStorageBlobContent [-Blob] <String> [-Container] <String> [-Destination <String>] [-CheckMd5] [-Force]
 [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a4360-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="a4360-106">BlobPipeline</span></span>
```
Get-AzStorageBlobContent -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] [-Destination <String>]
 [-CheckMd5] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4360-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="a4360-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobContent -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Destination <String>]
 [-CheckMd5] [-Force] [-AsJob] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4360-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a4360-108">DESCRIPTION</span></span>
<span data-ttu-id="a4360-109">**AzStorageBlobContent** cmdlet은 지정 된 저장소 blob을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4360-109">The **Get-AzStorageBlobContent** cmdlet downloads the specified storage blob.</span></span>
<span data-ttu-id="a4360-110">Blob 이름이 로컬 컴퓨터에 대해 유효 하지 않은 경우이 cmdlet은 가능한 경우 자동으로 해결 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4360-110">If the blob name is not valid for the local computer, this cmdlet automatically resolves it if it is possible.</span></span>

## <span data-ttu-id="a4360-111">예제의</span><span class="sxs-lookup"><span data-stu-id="a4360-111">EXAMPLES</span></span>

### <span data-ttu-id="a4360-112">예제 1: 이름별로 blob 콘텐츠 다운로드</span><span class="sxs-lookup"><span data-stu-id="a4360-112">Example 1: Download blob content by name</span></span>
```
PS C:\>Get-AzStorageBlobContent -Container "ContainerName" -Blob "Blob" -Destination "C:\test\"
```

<span data-ttu-id="a4360-113">이 명령은 이름으로 blob을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4360-113">This command downloads a blob by name.</span></span>

### <span data-ttu-id="a4360-114">예제 2: 파이프라인을 사용 하 여 blob 콘텐츠 다운로드</span><span class="sxs-lookup"><span data-stu-id="a4360-114">Example 2: Download blob content using the pipeline</span></span>
```
PS C:\>Get-AzStorageBlob -Container containername -Blob blobname | Get-AzStorageBlobContent
```

<span data-ttu-id="a4360-115">이 명령은 파이프라인을 사용 하 여 blob 콘텐츠를 찾고 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4360-115">This command uses the pipeline to find and download blob content.</span></span>

### <span data-ttu-id="a4360-116">예제 3: 파이프라인 및 와일드 카드 문자를 사용 하 여 blob 콘텐츠 다운로드</span><span class="sxs-lookup"><span data-stu-id="a4360-116">Example 3: Download blob content using the pipeline and a wildcard character</span></span>
```
PS C:\>Get-AzStorageContainer container* | Get-AzStorageBlobContent -Blob "cbox.exe" -Destination "C:\test"
```

<span data-ttu-id="a4360-117">이 예제에서는 별표 와일드 카드 문자와 파이프라인을 사용 하 여 blob 콘텐츠를 검색 하 고 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4360-117">This example uses the asterisk wildcard character and the pipeline to find and download blob content.</span></span>

### <span data-ttu-id="a4360-118">예제 4: blob 개체를 가져오고이를 변수에 저장 한 다음 blob 개체와 함께 blob 콘텐츠를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4360-118">Example 4: Get a blob object and save it in a variable, then download blob content with the blob object</span></span>
```
PS C:\>$blob = Get-AzStorageBlob -Container containername -Blob blobname 
PS C:\>Get-AzStorageBlobContent -CloudBlob $blob.ICloudBlob -Destination "C:\test"
```

<span data-ttu-id="a4360-119">이 예제에서는 먼저 blob 개체를 가져오고이를 변수에 저장 한 다음 blob 개체와 함께 blob 콘텐츠를 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4360-119">This example first get a blob object and save it in a variable, then download blob content with the blob object.</span></span> 

## <span data-ttu-id="a4360-120">변수</span><span class="sxs-lookup"><span data-stu-id="a4360-120">PARAMETERS</span></span>

### <span data-ttu-id="a4360-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a4360-121">-AsJob</span></span>
<span data-ttu-id="a4360-122">백그라운드에서 cmdlet을 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4360-122">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="a4360-123">-Blob</span><span class="sxs-lookup"><span data-stu-id="a4360-123">-Blob</span></span>
<span data-ttu-id="a4360-124">다운로드할 blob의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4360-124">Specifies the name of the blob to be downloaded.</span></span>

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

### <span data-ttu-id="a4360-125">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="a4360-125">-BlobBaseClient</span></span>
<span data-ttu-id="a4360-126">BlobBaseClient 개체</span><span class="sxs-lookup"><span data-stu-id="a4360-126">BlobBaseClient Object</span></span>

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

### <span data-ttu-id="a4360-127">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="a4360-127">-CheckMd5</span></span>
<span data-ttu-id="a4360-128">다운로드 한 파일에 대 한 Md5 합계를 확인할 지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4360-128">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

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

### <span data-ttu-id="a4360-129">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a4360-129">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="a4360-130">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4360-130">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="a4360-131">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4360-131">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="a4360-132">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4360-132">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="a4360-133">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="a4360-133">-CloudBlob</span></span>
<span data-ttu-id="a4360-134">클라우드 blob을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4360-134">Specifies a cloud blob.</span></span>
<span data-ttu-id="a4360-135">**CloudBlob** 개체를 가져오려면 Get-AzStorageBlob cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4360-135">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="a4360-136">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="a4360-136">-CloudBlobContainer</span></span>
<span data-ttu-id="a4360-137">Azure storage 클라이언트 라이브러리에서 **CloudBlobContainer** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4360-137">Specifies a **CloudBlobContainer** object from the Azure storage client library.</span></span>
<span data-ttu-id="a4360-138">이를 만들거나 Get-AzStorageContainer cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a4360-138">You can create it or use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="a4360-139">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="a4360-139">-ConcurrentTaskCount</span></span>
<span data-ttu-id="a4360-140">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4360-140">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="a4360-141">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a4360-141">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="a4360-142">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="a4360-142">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="a4360-143">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a4360-143">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="a4360-144">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="a4360-144">The default value is 10.</span></span>

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

### <span data-ttu-id="a4360-145">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="a4360-145">-Container</span></span>
<span data-ttu-id="a4360-146">다운로드 하려는 blob이 있는 컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4360-146">Specifies the name of container that has the blob you want to download.</span></span>

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

### <span data-ttu-id="a4360-147">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="a4360-147">-Context</span></span>
<span data-ttu-id="a4360-148">Blob 콘텐츠를 다운로드 하는 데 사용할 Azure storage 계정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4360-148">Specifies the Azure storage account from which you want to download blob content.</span></span>
<span data-ttu-id="a4360-149">New-AzStorageContext cmdlet을 사용 하 여 저장소 컨텍스트를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a4360-149">You can use the New-AzStorageContext cmdlet to create a storage context.</span></span>

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

### <span data-ttu-id="a4360-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4360-150">-DefaultProfile</span></span>
<span data-ttu-id="a4360-151">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a4360-151">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4360-152">-대상</span><span class="sxs-lookup"><span data-stu-id="a4360-152">-Destination</span></span>
<span data-ttu-id="a4360-153">다운로드 한 파일을 저장할 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4360-153">Specifies the location to store the downloaded file.</span></span>

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

### <span data-ttu-id="a4360-154">-Force</span><span class="sxs-lookup"><span data-stu-id="a4360-154">-Force</span></span>
<span data-ttu-id="a4360-155">확인 하지 않고 기존 파일을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="a4360-155">Overwrites an existing file without confirmation.</span></span>

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

### <span data-ttu-id="a4360-156">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a4360-156">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="a4360-157">요청에 대 한 서비스 측 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4360-157">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="a4360-158">서비스가 요청을 처리 하기 전에 지정 된 간격이 경과 하면 저장소 서비스에서 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4360-158">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="a4360-159">-확인</span><span class="sxs-lookup"><span data-stu-id="a4360-159">-Confirm</span></span>
<span data-ttu-id="a4360-160">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4360-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4360-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4360-161">-WhatIf</span></span>
<span data-ttu-id="a4360-162">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a4360-162">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4360-163">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a4360-163">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4360-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4360-164">CommonParameters</span></span>
<span data-ttu-id="a4360-165">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4360-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4360-166">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4360-166">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4360-167">입력</span><span class="sxs-lookup"><span data-stu-id="a4360-167">INPUTS</span></span>

### <span data-ttu-id="a4360-168">CloudBlob를 통해 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4360-168">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="a4360-169">CloudBlobContainer를 통해 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4360-169">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="a4360-170">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a4360-170">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a4360-171">출력</span><span class="sxs-lookup"><span data-stu-id="a4360-171">OUTPUTS</span></span>

### <span data-ttu-id="a4360-172">WindowsAzure. ResourceModel. m b m.</span><span class="sxs-lookup"><span data-stu-id="a4360-172">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="a4360-173">상속자</span><span class="sxs-lookup"><span data-stu-id="a4360-173">NOTES</span></span>
* <span data-ttu-id="a4360-174">Blob 이름이 로컬 컴퓨터에 대해 유효 하지 않은 경우 가능 하면이 cmdlet이 autoresolves를 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4360-174">If the blob name is invalid for local computer, this cmdlet autoresolves it, if it is possible.</span></span>

## <span data-ttu-id="a4360-175">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a4360-175">RELATED LINKS</span></span>

[<span data-ttu-id="a4360-176">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a4360-176">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)

[<span data-ttu-id="a4360-177">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="a4360-177">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="a4360-178">제거-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="a4360-178">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)
