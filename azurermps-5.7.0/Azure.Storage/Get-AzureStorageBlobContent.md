---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C091D654-E113-4AE0-A6C8-24630D1294A4
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageblobcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlobContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlobContent.md
ms.openlocfilehash: 5023643ae57ab73ea625254f7b2362c947209f8d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527167"
---
# <span data-ttu-id="b6442-101">Get-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="b6442-101">Get-AzureStorageBlobContent</span></span>

## <span data-ttu-id="b6442-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6442-102">SYNOPSIS</span></span>
<span data-ttu-id="b6442-103">저장소 blob을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6442-103">Downloads a storage blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b6442-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b6442-104">SYNTAX</span></span>

### <span data-ttu-id="b6442-105">ReceiveManual (기본값)</span><span class="sxs-lookup"><span data-stu-id="b6442-105">ReceiveManual (Default)</span></span>
```
Get-AzureStorageBlobContent [-Blob] <String> [-Container] <String> [-Destination <String>] [-CheckMd5] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6442-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="b6442-106">BlobPipeline</span></span>
```
Get-AzureStorageBlobContent -CloudBlob <CloudBlob> [-Destination <String>] [-CheckMd5] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6442-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="b6442-107">ContainerPipeline</span></span>
```
Get-AzureStorageBlobContent -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Destination <String>]
 [-CheckMd5] [-Force] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6442-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b6442-108">DESCRIPTION</span></span>
<span data-ttu-id="b6442-109">**Get-AzureStorageBlobContent** cmdlet은 지정 된 저장소 blob을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6442-109">The **Get-AzureStorageBlobContent** cmdlet downloads the specified storage blob.</span></span>
<span data-ttu-id="b6442-110">Blob 이름이 로컬 컴퓨터에 대해 유효 하지 않은 경우이 cmdlet은 가능한 경우 자동으로 해결 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6442-110">If the blob name is not valid for the local computer, this cmdlet automatically resolves it if it is possible.</span></span>

## <span data-ttu-id="b6442-111">예제의</span><span class="sxs-lookup"><span data-stu-id="b6442-111">EXAMPLES</span></span>

### <span data-ttu-id="b6442-112">예제 1: 이름별로 blob 콘텐츠 다운로드</span><span class="sxs-lookup"><span data-stu-id="b6442-112">Example 1: Download blob content by name</span></span>
```
PS C:\>Get-AzureStorageBlobContent -Container "ContainerName" -Blob "Blob" -Destination "C:\test\"
```

<span data-ttu-id="b6442-113">이 명령은 이름으로 blob을 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6442-113">This command downloads a blob by name.</span></span>

### <span data-ttu-id="b6442-114">예제 2: 파이프라인을 사용 하 여 blob 콘텐츠 다운로드</span><span class="sxs-lookup"><span data-stu-id="b6442-114">Example 2: Download blob content using the pipeline</span></span>
```
PS C:\>Get-AzureStorageBlob -Container containername -Blob blobname | Get-AzureStorageBlobContent
```

<span data-ttu-id="b6442-115">이 명령은 파이프라인을 사용 하 여 blob 콘텐츠를 찾고 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6442-115">This command uses the pipeline to find and download blob content.</span></span>

### <span data-ttu-id="b6442-116">예제 3: 파이프라인 및 와일드 카드 문자를 사용 하 여 blob 콘텐츠 다운로드</span><span class="sxs-lookup"><span data-stu-id="b6442-116">Example 3: Download blob content using the pipeline and a wildcard character</span></span>
```
PS C:\>Get-AzureStorageContainer container* | Get-AzureStorageBlobContent -Blob "cbox.exe" -Destination "C:\test"
```

<span data-ttu-id="b6442-117">이 예제에서는 별표 와일드 카드 문자와 파이프라인을 사용 하 여 blob 콘텐츠를 검색 하 고 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6442-117">This example uses the asterisk wildcard character and the pipeline to find and download blob content.</span></span>

## <span data-ttu-id="b6442-118">변수</span><span class="sxs-lookup"><span data-stu-id="b6442-118">PARAMETERS</span></span>

### <span data-ttu-id="b6442-119">-Blob</span><span class="sxs-lookup"><span data-stu-id="b6442-119">-Blob</span></span>
<span data-ttu-id="b6442-120">다운로드할 blob의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6442-120">Specifies the name of the blob to be downloaded.</span></span>

```yaml
Type: String
Parameter Sets: ReceiveManual, ContainerPipeline
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6442-121">-CheckMd5</span><span class="sxs-lookup"><span data-stu-id="b6442-121">-CheckMd5</span></span>
<span data-ttu-id="b6442-122">다운로드 한 파일에 대 한 Md5 합계를 확인할 지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6442-122">Specifies whether to check the Md5 sum for the downloaded file.</span></span>

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

### <span data-ttu-id="b6442-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b6442-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="b6442-124">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6442-124">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="b6442-125">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6442-125">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="b6442-126">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6442-126">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="b6442-127">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="b6442-127">-CloudBlob</span></span>
<span data-ttu-id="b6442-128">클라우드 blob을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6442-128">Specifies a cloud blob.</span></span>
<span data-ttu-id="b6442-129">**CloudBlob** 개체를 가져오려면 Get-AzureStorageBlob cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6442-129">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="b6442-130">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="b6442-130">-CloudBlobContainer</span></span>
<span data-ttu-id="b6442-131">Azure storage 클라이언트 라이브러리에서 **CloudBlobContainer** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6442-131">Specifies a **CloudBlobContainer** object from the Azure storage client library.</span></span>
<span data-ttu-id="b6442-132">이를 만들거나 Get-AzureStorageContainer cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b6442-132">You can create it or use the Get-AzureStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="b6442-133">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b6442-133">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b6442-134">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6442-134">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="b6442-135">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b6442-135">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="b6442-136">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="b6442-136">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="b6442-137">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b6442-137">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="b6442-138">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="b6442-138">The default value is 10.</span></span>

<span data-ttu-id="b6442-139">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="b6442-139">The default value is 10.</span></span>

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

### <span data-ttu-id="b6442-140">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="b6442-140">-Container</span></span>
<span data-ttu-id="b6442-141">다운로드 하려는 blob이 있는 컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6442-141">Specifies the name of container that has the blob you want to download.</span></span>

```yaml
Type: String
Parameter Sets: ReceiveManual
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6442-142">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="b6442-142">-Context</span></span>
<span data-ttu-id="b6442-143">Blob 콘텐츠를 다운로드 하는 데 사용할 Azure storage 계정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6442-143">Specifies the Azure storage account from which you want to download blob content.</span></span>
<span data-ttu-id="b6442-144">New-AzureStorageContext cmdlet을 사용 하 여 저장소 컨텍스트를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b6442-144">You can use the New-AzureStorageContext cmdlet to create a storage context.</span></span>

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

### <span data-ttu-id="b6442-145">-대상</span><span class="sxs-lookup"><span data-stu-id="b6442-145">-Destination</span></span>
<span data-ttu-id="b6442-146">다운로드 한 파일을 저장할 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6442-146">Specifies the location to store the downloaded file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Path

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6442-147">-Force</span><span class="sxs-lookup"><span data-stu-id="b6442-147">-Force</span></span>
<span data-ttu-id="b6442-148">확인 하지 않고 기존 파일을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="b6442-148">Overwrites an existing file without confirmation.</span></span>

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

### <span data-ttu-id="b6442-149">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b6442-149">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="b6442-150">요청에 대 한 서비스 측 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6442-150">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="b6442-151">서비스가 요청을 처리 하기 전에 지정 된 간격이 경과 하면 저장소 서비스에서 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6442-151">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="b6442-152">-확인</span><span class="sxs-lookup"><span data-stu-id="b6442-152">-Confirm</span></span>
<span data-ttu-id="b6442-153">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6442-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b6442-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6442-154">-WhatIf</span></span>
<span data-ttu-id="b6442-155">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b6442-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6442-156">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b6442-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b6442-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6442-157">CommonParameters</span></span>
<span data-ttu-id="b6442-158">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6442-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6442-159">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6442-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6442-160">입력</span><span class="sxs-lookup"><span data-stu-id="b6442-160">INPUTS</span></span>

### <span data-ttu-id="b6442-161">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b6442-161">IStorageContext</span></span>

<span data-ttu-id="b6442-162">' Context ' 매개 변수는 파이프라인에서 ' IStorageContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6442-162">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="b6442-163">출력</span><span class="sxs-lookup"><span data-stu-id="b6442-163">OUTPUTS</span></span>

### <span data-ttu-id="b6442-164">AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="b6442-164">AzureStorageContainer</span></span>

## <span data-ttu-id="b6442-165">상속자</span><span class="sxs-lookup"><span data-stu-id="b6442-165">NOTES</span></span>
* <span data-ttu-id="b6442-166">Blob 이름이 로컬 컴퓨터에 대해 유효 하지 않은 경우 가능 하면이 cmdlet이 autoresolves를 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="b6442-166">If the blob name is invalid for local computer, this cmdlet autoresolves it, if it is possible.</span></span>

## <span data-ttu-id="b6442-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b6442-167">RELATED LINKS</span></span>

[<span data-ttu-id="b6442-168">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="b6442-168">Set-AzureStorageBlobContent</span></span>](./Set-AzureStorageBlobContent.md)

[<span data-ttu-id="b6442-169">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="b6442-169">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="b6442-170">-AzureStorageBlob 제거</span><span class="sxs-lookup"><span data-stu-id="b6442-170">Remove-AzureStorageBlob</span></span>](./Remove-AzureStorageBlob.md)
