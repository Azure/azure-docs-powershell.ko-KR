---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E54BFD3A-CD54-4E6B-9574-92B8D3E88FF3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlob.md
ms.openlocfilehash: 9f4c20c29012609c773d176fb2f80c585bd9a851
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034706"
---
# <span data-ttu-id="41e1c-101">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="41e1c-101">Get-AzStorageBlob</span></span>

## <span data-ttu-id="41e1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="41e1c-102">SYNOPSIS</span></span>
<span data-ttu-id="41e1c-103">컨테이너의 blob을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="41e1c-103">Lists blobs in a container.</span></span>

## <span data-ttu-id="41e1c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="41e1c-104">SYNTAX</span></span>

### <span data-ttu-id="41e1c-105">BlobName (기본값)</span><span class="sxs-lookup"><span data-stu-id="41e1c-105">BlobName (Default)</span></span>
```
Get-AzStorageBlob [[-Blob] <String>] [-Container] <String> [-IncludeDeleted] [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="41e1c-106">BlobPrefix</span><span class="sxs-lookup"><span data-stu-id="41e1c-106">BlobPrefix</span></span>
```
Get-AzStorageBlob [-Prefix <String>] [-Container] <String> [-IncludeDeleted] [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="41e1c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="41e1c-107">DESCRIPTION</span></span>
<span data-ttu-id="41e1c-108">**AzStorageBlob** Cmdlet은 Azure 저장소 계정의 지정 된 컨테이너에 blob 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="41e1c-108">The **Get-AzStorageBlob** cmdlet lists blobs in the specified container in an Azure storage account.</span></span>

## <span data-ttu-id="41e1c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="41e1c-109">EXAMPLES</span></span>

### <span data-ttu-id="41e1c-110">예제 1: blob 이름으로 blob 가져오기</span><span class="sxs-lookup"><span data-stu-id="41e1c-110">Example 1: Get a blob by blob name</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Blob blob*
```

<span data-ttu-id="41e1c-111">이 명령은 blob 이름과 와일드 카드를 사용 하 여 blob를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="41e1c-111">This command uses a blob name and wildcard to get a blob.</span></span>

### <span data-ttu-id="41e1c-112">예제 2: 파이프라인을 사용 하 여 컨테이너의 blob 가져오기</span><span class="sxs-lookup"><span data-stu-id="41e1c-112">Example 2: Get blobs in a container by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Name container* | Get-AzStorageBlob -IncludeDeleted

   Container Uri: https://storageaccountname.blob.core.windows.net/container1

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime         IsDeleted 
----                 --------  ------          -----------                    ------------         ---------- ------------         --------- 
test1                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:19Z            2017-11-08 08:19:32Z True      
test1                BlockBlob 403116          application/octet-stream       2017-11-08 09:00:29Z                                 True      
test2                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:00Z                                 False
```

<span data-ttu-id="41e1c-113">이 명령은 파이프라인을 사용 하 여 컨테이너에 모든 blob (삭제 된 상태의 blob 포함)를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="41e1c-113">This command uses the pipeline to get all blobs (include blobs in Deleted status) in a container.</span></span>

### <span data-ttu-id="41e1c-114">예제 3: 이름 접두사로 blob 가져오기</span><span class="sxs-lookup"><span data-stu-id="41e1c-114">Example 3: Get blobs by name prefix</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Prefix "blob"
```

<span data-ttu-id="41e1c-115">이 명령은 이름 접두사를 사용 하 여 blob를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="41e1c-115">This command uses a name prefix to get blobs.</span></span>

### <span data-ttu-id="41e1c-116">예제 4: 여러 일괄 처리에 blob 나열</span><span class="sxs-lookup"><span data-stu-id="41e1c-116">Example 4: List blobs in multiple batches</span></span>
```
PS C:\>$MaxReturn = 10000
PS C:\> $ContainerName = "abc"
PS C:\> $Total = 0
PS C:\> $Token = $Null
PS C:\> do
 {
     $Blobs = Get-AzStorageBlob -Container $ContainerName -MaxCount $MaxReturn  -ContinuationToken $Token
     $Total += $Blobs.Count
     if($Blobs.Length -le 0) { Break;}
     $Token = $Blobs[$blobs.Count -1].ContinuationToken;
 }
 While ($Token -ne $Null)
PS C:\> Echo "Total $Total blobs in container $ContainerName"
```

<span data-ttu-id="41e1c-117">이 예제에서는 *MaxCount* 및 *ContinuationToken* 매개 변수를 사용 하 여 Azure Storage blob을 여러 일괄 처리로 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="41e1c-117">This example uses the *MaxCount* and *ContinuationToken* parameters to list Azure Storage blobs in multiple batches.</span></span>
<span data-ttu-id="41e1c-118">처음 4 개의 명령은 예제에서 사용할 변수에 값을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="41e1c-118">The first four commands assign values to variables to use in the example.</span></span>
<span data-ttu-id="41e1c-119">다섯 번째 명령은 **AzStorageBlob** cmdlet을 사용 하 여 blob을 가져오는 **Do While** 문을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41e1c-119">The fifth command specifies a **Do-While** statement that uses the **Get-AzStorageBlob** cmdlet to get blobs.</span></span>
<span data-ttu-id="41e1c-120">이 문에는 $Token 변수에 저장 된 연속 토큰이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="41e1c-120">The statement includes the continuation token stored in the $Token variable.</span></span>
<span data-ttu-id="41e1c-121">루프가 실행 되는 동안 값이 변경 $Token.</span><span class="sxs-lookup"><span data-stu-id="41e1c-121">$Token changes value as the loop runs.</span></span>
<span data-ttu-id="41e1c-122">자세한 내용은을 입력 `Get-Help About_Do` 하세요.</span><span class="sxs-lookup"><span data-stu-id="41e1c-122">For more information, type `Get-Help About_Do`.</span></span>
<span data-ttu-id="41e1c-123">마지막 명령은 **Echo** 명령을 사용 하 여 합계를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="41e1c-123">The final command uses the **Echo** command to display the total.</span></span>

## <span data-ttu-id="41e1c-124">변수</span><span class="sxs-lookup"><span data-stu-id="41e1c-124">PARAMETERS</span></span>

### <span data-ttu-id="41e1c-125">-Blob</span><span class="sxs-lookup"><span data-stu-id="41e1c-125">-Blob</span></span>
<span data-ttu-id="41e1c-126">와일드 카드 검색에 사용할 수 있는 이름 또는 이름 패턴을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41e1c-126">Specifies a name or name pattern, which can be used for a wildcard search.</span></span>
<span data-ttu-id="41e1c-127">Blob 이름이 지정 되지 않은 경우 cmdlet은 지정 된 컨테이너의 모든 blob을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="41e1c-127">If no blob name is specified, the cmdlet lists all the blobs in the specified container.</span></span>
<span data-ttu-id="41e1c-128">이 매개 변수에 대 한 값이 지정 된 경우 cmdlet은 이름이이 매개 변수와 일치 하는 모든 blob를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="41e1c-128">If a value is specified for this parameter, the cmdlet lists all blobs with names that match this parameter.</span></span> <span data-ttu-id="41e1c-129">이 매개 변수는 문자열의 모든 위치에서 와일드 카드를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="41e1c-129">This parameter supports wildcards anywhere in the string.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="41e1c-130">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="41e1c-130">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="41e1c-131">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41e1c-131">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="41e1c-132">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="41e1c-132">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="41e1c-133">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="41e1c-133">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="41e1c-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="41e1c-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="41e1c-135">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41e1c-135">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="41e1c-136">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="41e1c-136">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="41e1c-137">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="41e1c-137">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="41e1c-138">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="41e1c-138">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="41e1c-139">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="41e1c-139">The default value is 10.</span></span>

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

### <span data-ttu-id="41e1c-140">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="41e1c-140">-Container</span></span>
<span data-ttu-id="41e1c-141">컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41e1c-141">Specifies the name of the container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="41e1c-142">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="41e1c-142">-Context</span></span>
<span data-ttu-id="41e1c-143">Blob 목록을 가져오는 데 사용할 Azure storage 계정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41e1c-143">Specifies the Azure storage account from which you want to get a list of blobs.</span></span>
<span data-ttu-id="41e1c-144">New-AzStorageContext cmdlet을 사용 하 여 저장소 컨텍스트를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="41e1c-144">You can use the New-AzStorageContext cmdlet to create a storage context.</span></span>

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

### <span data-ttu-id="41e1c-145">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="41e1c-145">-ContinuationToken</span></span>
<span data-ttu-id="41e1c-146">Blob 목록에 대 한 연속 토큰을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41e1c-146">Specifies a continuation token for the blob list.</span></span>
<span data-ttu-id="41e1c-147">이 매개 변수와 *MaxCount* 매개 변수를 사용 하 여 여러 일괄 처리에 blob 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="41e1c-147">Use this parameter and the *MaxCount* parameter to list blobs in multiple batches.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.BlobContinuationToken
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41e1c-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41e1c-148">-DefaultProfile</span></span>
<span data-ttu-id="41e1c-149">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="41e1c-149">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="41e1c-150">-IncludeDeleted</span><span class="sxs-lookup"><span data-stu-id="41e1c-150">-IncludeDeleted</span></span>
<span data-ttu-id="41e1c-151">삭제 된 Blob 포함 기본적으로 blob는 삭제 된 blob를 포함 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="41e1c-151">Include Deleted Blob, by default get blob won't include deleted blob.</span></span>

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

### <span data-ttu-id="41e1c-152">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="41e1c-152">-MaxCount</span></span>
<span data-ttu-id="41e1c-153">이 cmdlet이 반환 하는 최대 개체 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41e1c-153">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="41e1c-154">-접두사</span><span class="sxs-lookup"><span data-stu-id="41e1c-154">-Prefix</span></span>
<span data-ttu-id="41e1c-155">가져오려는 blob 이름에 대 한 접두사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41e1c-155">Specifies a prefix for the blob names that you want to get.</span></span>
<span data-ttu-id="41e1c-156">이 매개 변수는 정규식 또는 와일드 카드 문자를 사용 하 여 검색 하는 것을 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="41e1c-156">This parameter does not support using regular expressions or wildcard characters to search.</span></span>
<span data-ttu-id="41e1c-157">즉, 컨테이너에 "My", "MyBlob1", "MyBlob2" 이라는 blob만 있고 "-Prefix My \*"를 지정 하면 cmdlet은 blob을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="41e1c-157">This means that if the container has only blobs named "My", "MyBlob1", and "MyBlob2" and you specify "-Prefix My\*", the cmdlet returns no blobs.</span></span>
<span data-ttu-id="41e1c-158">그러나 "-Prefix My"를 지정 하면 cmdlet은 "My", "MyBlob1", "MyBlob2"를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="41e1c-158">However, if you specify "-Prefix My", the cmdlet returns "My", "MyBlob1", and "MyBlob2".</span></span>

```yaml
Type: System.String
Parameter Sets: BlobPrefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41e1c-159">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="41e1c-159">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="41e1c-160">요청에 대 한 서비스 측 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="41e1c-160">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="41e1c-161">서비스가 요청을 처리 하기 전에 지정 된 간격이 경과 하면 저장소 서비스에서 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="41e1c-161">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="41e1c-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41e1c-162">CommonParameters</span></span>
<span data-ttu-id="41e1c-163">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="41e1c-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41e1c-164">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41e1c-164">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41e1c-165">입력</span><span class="sxs-lookup"><span data-stu-id="41e1c-165">INPUTS</span></span>

### <span data-ttu-id="41e1c-166">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="41e1c-166">System.String</span></span>

### <span data-ttu-id="41e1c-167">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="41e1c-167">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="41e1c-168">출력</span><span class="sxs-lookup"><span data-stu-id="41e1c-168">OUTPUTS</span></span>

### <span data-ttu-id="41e1c-169">WindowsAzure. ResourceModel. m b m.</span><span class="sxs-lookup"><span data-stu-id="41e1c-169">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="41e1c-170">상속자</span><span class="sxs-lookup"><span data-stu-id="41e1c-170">NOTES</span></span>

## <span data-ttu-id="41e1c-171">관련 링크</span><span class="sxs-lookup"><span data-stu-id="41e1c-171">RELATED LINKS</span></span>

[<span data-ttu-id="41e1c-172">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="41e1c-172">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="41e1c-173">제거-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="41e1c-173">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)

[<span data-ttu-id="41e1c-174">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="41e1c-174">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)


