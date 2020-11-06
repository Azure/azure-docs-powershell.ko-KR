---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: E54BFD3A-CD54-4E6B-9574-92B8D3E88FF3
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageBlob.md
ms.openlocfilehash: da3b5f969bfa8beafab20f256df237588ed87048
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527172"
---
# <span data-ttu-id="39e40-101">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="39e40-101">Get-AzureStorageBlob</span></span>

## <span data-ttu-id="39e40-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39e40-102">SYNOPSIS</span></span>
<span data-ttu-id="39e40-103">컨테이너의 blob을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="39e40-103">Lists blobs in a container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="39e40-104">구문과</span><span class="sxs-lookup"><span data-stu-id="39e40-104">SYNTAX</span></span>

### <span data-ttu-id="39e40-105">BlobName (기본값)</span><span class="sxs-lookup"><span data-stu-id="39e40-105">BlobName (Default)</span></span>
```
Get-AzureStorageBlob [[-Blob] <String>] [-Container] <String> [-IncludeDeleted] [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="39e40-106">BlobPrefix</span><span class="sxs-lookup"><span data-stu-id="39e40-106">BlobPrefix</span></span>
```
Get-AzureStorageBlob [-Prefix <String>] [-Container] <String> [-IncludeDeleted] [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="39e40-107">설명은</span><span class="sxs-lookup"><span data-stu-id="39e40-107">DESCRIPTION</span></span>
<span data-ttu-id="39e40-108">**Get-AzureStorageBlob** Cmdlet은 Azure 저장소 계정의 지정 된 컨테이너에 있는 blob을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="39e40-108">The **Get-AzureStorageBlob** cmdlet lists blobs in the specified container in an Azure storage account.</span></span>

## <span data-ttu-id="39e40-109">예제의</span><span class="sxs-lookup"><span data-stu-id="39e40-109">EXAMPLES</span></span>

### <span data-ttu-id="39e40-110">예제 1: blob 이름으로 blob 가져오기</span><span class="sxs-lookup"><span data-stu-id="39e40-110">Example 1: Get a blob by blob name</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" -Blob blob*
```

<span data-ttu-id="39e40-111">이 명령은 blob 이름과 와일드 카드를 사용 하 여 blob를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="39e40-111">This command uses a blob name and wildcard to get a blob.</span></span>

### <span data-ttu-id="39e40-112">예제 2: 파이프라인을 사용 하 여 컨테이너의 blob 가져오기</span><span class="sxs-lookup"><span data-stu-id="39e40-112">Example 2: Get blobs in a container by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Name container* | Get-AzureStorageBlob -IncludeDeleted

   Container Uri: https://storageaccountname.blob.core.windows.net/container1

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime         IsDeleted 
----                 --------  ------          -----------                    ------------         ---------- ------------         --------- 
test1                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:19Z            2017-11-08 08:19:32Z True      
test1                BlockBlob 403116          application/octet-stream       2017-11-08 09:00:29Z                                 True      
test2                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:00Z                                 False      
```

<span data-ttu-id="39e40-113">이 명령은 파이프라인을 사용 하 여 컨테이너에 모든 blob (삭제 된 상태의 blob 포함)를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="39e40-113">This command uses the pipeline to get all blobs (include blobs in Deleted status) in a container.</span></span>

### <span data-ttu-id="39e40-114">예제 3: 이름 접두사로 blob 가져오기</span><span class="sxs-lookup"><span data-stu-id="39e40-114">Example 3: Get blobs by name prefix</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" -Prefix "blob"
```

<span data-ttu-id="39e40-115">이 명령은 이름 접두사를 사용 하 여 blob를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="39e40-115">This command uses a name prefix to get blobs.</span></span>

### <span data-ttu-id="39e40-116">예제 4: 여러 일괄 처리에 blob 나열</span><span class="sxs-lookup"><span data-stu-id="39e40-116">Example 4: List blobs in multiple batches</span></span>
```
PS C:\>$MaxReturn = 10000
PS C:\> $ContainerName = "abc"
PS C:\> $Total = 0
PS C:\> $Token = $Null
PS C:\> do
 {
     $Blobs = Get-AzureStorageBlob -Container $ContainerName -MaxCount $MaxReturn  -ContinuationToken $Token
     $Total += $Blobs.Count
     if($Blobs.Length -le 0) { Break;}
     $Token = $Blobs[$blobs.Count -1].ContinuationToken;
 }
 While ($Token -ne $Null)
PS C:\> Echo "Total $Total blobs in container $ContainerName"
```

<span data-ttu-id="39e40-117">이 예제에서는 *MaxCount* 및 *ContinuationToken* 매개 변수를 사용 하 여 Azure Storage blob을 여러 일괄 처리로 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="39e40-117">This example uses the *MaxCount* and *ContinuationToken* parameters to list Azure Storage blobs in multiple batches.</span></span>
<span data-ttu-id="39e40-118">처음 4 개의 명령은 예제에서 사용할 변수에 값을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="39e40-118">The first four commands assign values to variables to use in the example.</span></span>

<span data-ttu-id="39e40-119">다섯 번째 명령은 **get-AzureStorageBlob** cmdlet을 사용 하 여 blob을 가져오는 **Do While** 문을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39e40-119">The fifth command specifies a **Do-While** statement that uses the **Get-AzureStorageBlob** cmdlet to get blobs.</span></span>
<span data-ttu-id="39e40-120">이 문에는 $Token 변수에 저장 된 연속 토큰이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="39e40-120">The statement includes the continuation token stored in the $Token variable.</span></span>
<span data-ttu-id="39e40-121">루프가 실행 되는 동안 값이 변경 $Token.</span><span class="sxs-lookup"><span data-stu-id="39e40-121">$Token changes value as the loop runs.</span></span>
<span data-ttu-id="39e40-122">자세한 내용은을 입력 `Get-Help About_Do` 하세요.</span><span class="sxs-lookup"><span data-stu-id="39e40-122">For more information, type `Get-Help About_Do`.</span></span>

<span data-ttu-id="39e40-123">마지막 명령은 **Echo** 명령을 사용 하 여 합계를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="39e40-123">The final command uses the **Echo** command to display the total.</span></span>

## <span data-ttu-id="39e40-124">변수</span><span class="sxs-lookup"><span data-stu-id="39e40-124">PARAMETERS</span></span>

### <span data-ttu-id="39e40-125">-Blob</span><span class="sxs-lookup"><span data-stu-id="39e40-125">-Blob</span></span>
<span data-ttu-id="39e40-126">와일드 카드 검색에 사용할 수 있는 이름 또는 이름 패턴을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39e40-126">Specifies a name or name pattern, which can be used for a wildcard search.</span></span>
<span data-ttu-id="39e40-127">Blob 이름이 지정 되지 않은 경우 cmdlet은 지정 된 컨테이너의 모든 blob을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="39e40-127">If no blob name is specified, the cmdlet lists all the blobs in the specified container.</span></span>
<span data-ttu-id="39e40-128">이 매개 변수에 대 한 값이 지정 된 경우 cmdlet은 이름이이 매개 변수와 일치 하는 모든 blob를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="39e40-128">If a value is specified for this parameter, the cmdlet lists all blobs with names that match this parameter.</span></span>

```yaml
Type: String
Parameter Sets: BlobName
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="39e40-129">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="39e40-129">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="39e40-130">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39e40-130">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="39e40-131">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="39e40-131">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="39e40-132">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="39e40-132">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="39e40-133">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="39e40-133">-ConcurrentTaskCount</span></span>
<span data-ttu-id="39e40-134">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39e40-134">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="39e40-135">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="39e40-135">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="39e40-136">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="39e40-136">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="39e40-137">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="39e40-137">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="39e40-138">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="39e40-138">The default value is 10.</span></span>

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

### <span data-ttu-id="39e40-139">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="39e40-139">-Container</span></span>
<span data-ttu-id="39e40-140">컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39e40-140">Specifies the name of the container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="39e40-141">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="39e40-141">-Context</span></span>
<span data-ttu-id="39e40-142">Blob 목록을 가져오는 데 사용할 Azure storage 계정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39e40-142">Specifies the Azure storage account from which you want to get a list of blobs.</span></span>
<span data-ttu-id="39e40-143">New-AzureStorageContext cmdlet을 사용 하 여 저장소 컨텍스트를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="39e40-143">You can use the New-AzureStorageContext cmdlet to create a storage context.</span></span>

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

### <span data-ttu-id="39e40-144">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="39e40-144">-ContinuationToken</span></span>
<span data-ttu-id="39e40-145">Blob 목록에 대 한 연속 토큰을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39e40-145">Specifies a continuation token for the blob list.</span></span>
<span data-ttu-id="39e40-146">이 매개 변수와 *MaxCount* 매개 변수를 사용 하 여 여러 일괄 처리에 blob 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="39e40-146">Use this parameter and the *MaxCount* parameter to list blobs in multiple batches.</span></span>

```yaml
Type: BlobContinuationToken
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39e40-147">-IncludeDeleted</span><span class="sxs-lookup"><span data-stu-id="39e40-147">-IncludeDeleted</span></span>
<span data-ttu-id="39e40-148">삭제 된 Blob 포함 기본적으로 blob는 삭제 된 blob를 포함 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="39e40-148">Include Deleted Blob, by default get blob won't include deleted blob.</span></span>

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

### <span data-ttu-id="39e40-149">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="39e40-149">-MaxCount</span></span>
<span data-ttu-id="39e40-150">이 cmdlet이 반환 하는 최대 개체 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39e40-150">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="39e40-151">-접두사</span><span class="sxs-lookup"><span data-stu-id="39e40-151">-Prefix</span></span>
<span data-ttu-id="39e40-152">가져오려는 blob 이름에 대 한 접두사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39e40-152">Specifies a prefix for the blob names that you want to get.</span></span>
<span data-ttu-id="39e40-153">이 매개 변수는 정규식 또는 와일드 카드 문자를 사용 하 여 검색 하는 것을 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="39e40-153">This parameter does not support using regular expressions or wildcard characters to search.</span></span>
<span data-ttu-id="39e40-154">즉, 컨테이너에 "My", "MyBlob1", "MyBlob2" 이라는 blob만 있고 "-Prefix My \*"를 지정 하면 cmdlet은 blob을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="39e40-154">This means that if the container has only blobs named "My", "MyBlob1", and "MyBlob2" and you specify "-Prefix My\*", the cmdlet returns no blobs.</span></span>
<span data-ttu-id="39e40-155">그러나 "-Prefix My"를 지정 하면 cmdlet은 "My", "MyBlob1", "MyBlob2"를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="39e40-155">However, if you specify "-Prefix My", the cmdlet returns "My", "MyBlob1", and "MyBlob2".</span></span>

```yaml
Type: String
Parameter Sets: BlobPrefix
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="39e40-156">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="39e40-156">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="39e40-157">요청에 대 한 서비스 측 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39e40-157">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="39e40-158">서비스가 요청을 처리 하기 전에 지정 된 간격이 경과 하면 저장소 서비스에서 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="39e40-158">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="39e40-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39e40-159">CommonParameters</span></span>
<span data-ttu-id="39e40-160">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="39e40-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39e40-161">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39e40-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39e40-162">입력</span><span class="sxs-lookup"><span data-stu-id="39e40-162">INPUTS</span></span>

### <span data-ttu-id="39e40-163">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="39e40-163">IStorageContext</span></span>
<span data-ttu-id="39e40-164">' Context ' 매개 변수는 파이프라인에서 ' IStorageContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="39e40-164">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="39e40-165">출력</span><span class="sxs-lookup"><span data-stu-id="39e40-165">OUTPUTS</span></span>

### <span data-ttu-id="39e40-166">AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="39e40-166">AzureStorageBlob</span></span>

## <span data-ttu-id="39e40-167">상속자</span><span class="sxs-lookup"><span data-stu-id="39e40-167">NOTES</span></span>

## <span data-ttu-id="39e40-168">관련 링크</span><span class="sxs-lookup"><span data-stu-id="39e40-168">RELATED LINKS</span></span>

[<span data-ttu-id="39e40-169">가져오기-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="39e40-169">Get-AzureStorageBlobContent</span></span>](./Get-AzureStorageBlobContent.md)

[<span data-ttu-id="39e40-170">-AzureStorageBlob 제거</span><span class="sxs-lookup"><span data-stu-id="39e40-170">Remove-AzureStorageBlob</span></span>](./Remove-AzureStorageBlob.md)

[<span data-ttu-id="39e40-171">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="39e40-171">Set-AzureStorageBlobContent</span></span>](./Set-AzureStorageBlobContent.md)

