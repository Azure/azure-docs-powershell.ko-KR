---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E54BFD3A-CD54-4E6B-9574-92B8D3E88FF3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlob.md
ms.openlocfilehash: 44c14b1f5aa8426bfb78205fa66a53d7db7e3440
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204246"
---
# <span data-ttu-id="2fc64-101">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="2fc64-101">Get-AzStorageBlob</span></span>

## <span data-ttu-id="2fc64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2fc64-102">SYNOPSIS</span></span>
<span data-ttu-id="2fc64-103">컨테이너의 blob을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc64-103">Lists blobs in a container.</span></span>

## <span data-ttu-id="2fc64-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2fc64-104">SYNTAX</span></span>

### <span data-ttu-id="2fc64-105">BlobName (기본값)</span><span class="sxs-lookup"><span data-stu-id="2fc64-105">BlobName (Default)</span></span>
```
Get-AzStorageBlob [[-Blob] <String>] [-Container] <String> [-IncludeDeleted] [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="2fc64-106">SingleBlobSnapshotTime</span><span class="sxs-lookup"><span data-stu-id="2fc64-106">SingleBlobSnapshotTime</span></span>
```
Get-AzStorageBlob [-Blob] <String> [-Container] <String> [-IncludeDeleted] -SnapshotTime <DateTimeOffset>
 [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="2fc64-107">SingleBlobVersionID</span><span class="sxs-lookup"><span data-stu-id="2fc64-107">SingleBlobVersionID</span></span>
```
Get-AzStorageBlob [-Blob] <String> [-Container] <String> [-IncludeDeleted] -VersionId <String>
 [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="2fc64-108">BlobPrefix</span><span class="sxs-lookup"><span data-stu-id="2fc64-108">BlobPrefix</span></span>
```
Get-AzStorageBlob [-Prefix <String>] [-Container] <String> [-IncludeDeleted] [-IncludeVersion]
 [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="2fc64-109">설명은</span><span class="sxs-lookup"><span data-stu-id="2fc64-109">DESCRIPTION</span></span>
<span data-ttu-id="2fc64-110">**AzStorageBlob** Cmdlet은 Azure 저장소 계정의 지정 된 컨테이너에 blob 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc64-110">The **Get-AzStorageBlob** cmdlet lists blobs in the specified container in an Azure storage account.</span></span>

## <span data-ttu-id="2fc64-111">예제의</span><span class="sxs-lookup"><span data-stu-id="2fc64-111">EXAMPLES</span></span>

### <span data-ttu-id="2fc64-112">예제 1: blob 이름으로 blob 가져오기</span><span class="sxs-lookup"><span data-stu-id="2fc64-112">Example 1: Get a blob by blob name</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Blob blob*
```

<span data-ttu-id="2fc64-113">이 명령은 blob 이름과 와일드 카드를 사용 하 여 blob를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2fc64-113">This command uses a blob name and wildcard to get a blob.</span></span>

### <span data-ttu-id="2fc64-114">예제 2: 파이프라인을 사용 하 여 컨테이너의 blob 가져오기</span><span class="sxs-lookup"><span data-stu-id="2fc64-114">Example 2: Get blobs in a container by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Name container* | Get-AzStorageBlob -IncludeDeleted

   Container Uri: https://storageaccountname.blob.core.windows.net/container1

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime         IsDeleted 
----                 --------  ------          -----------                    ------------         ---------- ------------         --------- 
test1                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:19Z            2017-11-08 08:19:32Z True      
test1                BlockBlob 403116          application/octet-stream       2017-11-08 09:00:29Z                                 True      
test2                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:00Z                                 False
```

<span data-ttu-id="2fc64-115">이 명령은 파이프라인을 사용 하 여 컨테이너에 모든 blob (삭제 된 상태의 blob 포함)를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2fc64-115">This command uses the pipeline to get all blobs (include blobs in Deleted status) in a container.</span></span>

### <span data-ttu-id="2fc64-116">예제 3: 이름 접두사로 blob 가져오기</span><span class="sxs-lookup"><span data-stu-id="2fc64-116">Example 3: Get blobs by name prefix</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Prefix "blob"
```

<span data-ttu-id="2fc64-117">이 명령은 이름 접두사를 사용 하 여 blob를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2fc64-117">This command uses a name prefix to get blobs.</span></span>

### <span data-ttu-id="2fc64-118">예제 4: 여러 일괄 처리에 blob 나열</span><span class="sxs-lookup"><span data-stu-id="2fc64-118">Example 4: List blobs in multiple batches</span></span>
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

<span data-ttu-id="2fc64-119">이 예제에서는 *MaxCount* 및 *ContinuationToken* 매개 변수를 사용 하 여 Azure Storage blob을 여러 일괄 처리로 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc64-119">This example uses the *MaxCount* and *ContinuationToken* parameters to list Azure Storage blobs in multiple batches.</span></span>
<span data-ttu-id="2fc64-120">처음 4 개의 명령은 예제에서 사용할 변수에 값을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc64-120">The first four commands assign values to variables to use in the example.</span></span>
<span data-ttu-id="2fc64-121">다섯 번째 명령은 **AzStorageBlob** cmdlet을 사용 하 여 blob을 가져오는 **Do While** 문을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc64-121">The fifth command specifies a **Do-While** statement that uses the **Get-AzStorageBlob** cmdlet to get blobs.</span></span>
<span data-ttu-id="2fc64-122">이 문에는 $Token 변수에 저장 된 연속 토큰이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2fc64-122">The statement includes the continuation token stored in the $Token variable.</span></span>
<span data-ttu-id="2fc64-123">루프가 실행 되는 동안 값이 변경 $Token.</span><span class="sxs-lookup"><span data-stu-id="2fc64-123">$Token changes value as the loop runs.</span></span>
<span data-ttu-id="2fc64-124">자세한 내용은을 입력 `Get-Help About_Do` 하세요.</span><span class="sxs-lookup"><span data-stu-id="2fc64-124">For more information, type `Get-Help About_Do`.</span></span>
<span data-ttu-id="2fc64-125">마지막 명령은 **Echo** 명령을 사용 하 여 합계를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc64-125">The final command uses the **Echo** command to display the total.</span></span>

### <span data-ttu-id="2fc64-126">예제 5: 컨테이너의 모든 blob 가져오기 blob 버전이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2fc64-126">Example 5: Get all blobs in a container include blob version</span></span>
```
PS C:\>Get-AzStorageBlob -Container "containername"  -IncludeVersion 

   AccountName: storageaccountname, ContainerName: containername

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
blob1                BlockBlob 2097152         application/octet-stream       2020-07-06 06:56:06Z Hot                                     False      2020-07-06T06:56:06.2432658Z  
blob1                BlockBlob 2097152         application/octet-stream       2020-07-06 06:56:06Z Hot        2020-07-06T06:56:06.8588431Z False                                    
blob1                BlockBlob 2097152         application/octet-stream       2020-07-06 06:56:06Z Hot                                     False      2020-07-06T06:56:06.8598431Z *  
blob2                BlockBlob 2097152         application/octet-stream       2020-07-03 16:19:16Z Hot                                     False      2020-07-03T16:19:16.2883167Z  
blob2                BlockBlob 2097152         application/octet-stream       2020-07-03 16:19:35Z Hot                                     False      2020-07-03T16:19:35.2381110Z *
```

<span data-ttu-id="2fc64-127">이 명령은 컨테이너의 모든 blob을 가져옵니다. blob 버전을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc64-127">This command gets all blobs in a container include blob version.</span></span>

### <span data-ttu-id="2fc64-128">예제 6: 단일 blob 버전 가져오기</span><span class="sxs-lookup"><span data-stu-id="2fc64-128">Example 6: Get a single blob version</span></span>
```
PS C:\> Get-AzStorageBlob -Container "containername" -Blob blob2 -VersionId "2020-07-03T16:19:16.2883167Z" 

   AccountName: storageaccountname, ContainerName: containername

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
blob2                BlockBlob 2097152         application/octet-stream       2020-07-03 16:19:16Z Hot                                     False      2020-07-03T16:19:16.2883167Z
```

<span data-ttu-id="2fc64-129">이 명령은 verion를 사용 하 여 단일 blob을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2fc64-129">This command gets a single blobs verion with VersionId.</span></span>

### <span data-ttu-id="2fc64-130">예제 7: 단일 blob 스냅숏 가져오기</span><span class="sxs-lookup"><span data-stu-id="2fc64-130">Example 7: Get a single blob snapshot</span></span>
```
PS C:\> Get-AzStorageBlob -Container "containername" -Blob blob1 -SnapshotTime "2020-07-06T06:56:06.8588431Z"

   AccountName: storageaccountname, ContainerName: containername

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
blob1                BlockBlob 2097152         application/octet-stream       2020-07-06 06:56:06Z Hot        2020-07-06T06:56:06.8588431Z False
```

<span data-ttu-id="2fc64-131">이 명령은 SnapshotTime를 사용 하 여 단일 blob 스냅숏을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2fc64-131">This command gets a single blobs snapshot with SnapshotTime.</span></span>

## <span data-ttu-id="2fc64-132">변수</span><span class="sxs-lookup"><span data-stu-id="2fc64-132">PARAMETERS</span></span>

### <span data-ttu-id="2fc64-133">-Blob</span><span class="sxs-lookup"><span data-stu-id="2fc64-133">-Blob</span></span>
<span data-ttu-id="2fc64-134">와일드 카드 검색에 사용할 수 있는 이름 또는 이름 패턴을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc64-134">Specifies a name or name pattern, which can be used for a wildcard search.</span></span>
<span data-ttu-id="2fc64-135">Blob 이름이 지정 되지 않은 경우 cmdlet은 지정 된 컨테이너의 모든 blob을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc64-135">If no blob name is specified, the cmdlet lists all the blobs in the specified container.</span></span>
<span data-ttu-id="2fc64-136">이 매개 변수에 대 한 값이 지정 된 경우 cmdlet은 이름이이 매개 변수와 일치 하는 모든 blob를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc64-136">If a value is specified for this parameter, the cmdlet lists all blobs with names that match this parameter.</span></span> <span data-ttu-id="2fc64-137">이 매개 변수는 문자열의 모든 위치에서 와일드 카드를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc64-137">This parameter supports wildcards anywhere in the string.</span></span>

```yaml
Type: System.String
Parameter Sets: BlobName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SingleBlobSnapshotTime, SingleBlobVersionID
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fc64-138">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2fc64-138">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="2fc64-139">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc64-139">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="2fc64-140">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc64-140">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="2fc64-141">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc64-141">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="2fc64-142">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="2fc64-142">-ConcurrentTaskCount</span></span>
<span data-ttu-id="2fc64-143">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc64-143">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="2fc64-144">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2fc64-144">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="2fc64-145">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="2fc64-145">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="2fc64-146">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2fc64-146">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="2fc64-147">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="2fc64-147">The default value is 10.</span></span>

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

### <span data-ttu-id="2fc64-148">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="2fc64-148">-Container</span></span>
<span data-ttu-id="2fc64-149">컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc64-149">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="2fc64-150">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="2fc64-150">-Context</span></span>
<span data-ttu-id="2fc64-151">Blob 목록을 가져오는 데 사용할 Azure storage 계정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc64-151">Specifies the Azure storage account from which you want to get a list of blobs.</span></span>
<span data-ttu-id="2fc64-152">New-AzStorageContext cmdlet을 사용 하 여 저장소 컨텍스트를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2fc64-152">You can use the New-AzStorageContext cmdlet to create a storage context.</span></span>

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

### <span data-ttu-id="2fc64-153">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="2fc64-153">-ContinuationToken</span></span>
<span data-ttu-id="2fc64-154">Blob 목록에 대 한 연속 토큰을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc64-154">Specifies a continuation token for the blob list.</span></span>
<span data-ttu-id="2fc64-155">이 매개 변수와 *MaxCount* 매개 변수를 사용 하 여 여러 일괄 처리에 blob 목록을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc64-155">Use this parameter and the *MaxCount* parameter to list blobs in multiple batches.</span></span>

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

### <span data-ttu-id="2fc64-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fc64-156">-DefaultProfile</span></span>
<span data-ttu-id="2fc64-157">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2fc64-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2fc64-158">-IncludeDeleted</span><span class="sxs-lookup"><span data-stu-id="2fc64-158">-IncludeDeleted</span></span>
<span data-ttu-id="2fc64-159">삭제 된 Blob 포함 기본적으로 blob는 삭제 된 blob를 포함 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2fc64-159">Include Deleted Blob, by default get blob won't include deleted blob.</span></span>

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

### <span data-ttu-id="2fc64-160">-IncludeVersion</span><span class="sxs-lookup"><span data-stu-id="2fc64-160">-IncludeVersion</span></span>
<span data-ttu-id="2fc64-161">이 매개 변수가 있는 경우에만 blob 버전이 나열 됩니다. 기본적으로 blob get에는 blob 버전이 포함 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2fc64-161">Blob versions will be listed only if this parameter is present, by default get blob won't include blob versions.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BlobPrefix
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fc64-162">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="2fc64-162">-MaxCount</span></span>
<span data-ttu-id="2fc64-163">이 cmdlet이 반환 하는 최대 개체 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc64-163">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="2fc64-164">-접두사</span><span class="sxs-lookup"><span data-stu-id="2fc64-164">-Prefix</span></span>
<span data-ttu-id="2fc64-165">가져오려는 blob 이름에 대 한 접두사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc64-165">Specifies a prefix for the blob names that you want to get.</span></span>
<span data-ttu-id="2fc64-166">이 매개 변수는 정규식 또는 와일드 카드 문자를 사용 하 여 검색 하는 것을 지원 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2fc64-166">This parameter does not support using regular expressions or wildcard characters to search.</span></span>
<span data-ttu-id="2fc64-167">즉, 컨테이너에 "My", "MyBlob1", "MyBlob2" 이라는 blob만 있고 "-Prefix My \*"를 지정 하면 cmdlet은 blob을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2fc64-167">This means that if the container has only blobs named "My", "MyBlob1", and "MyBlob2" and you specify "-Prefix My\*", the cmdlet returns no blobs.</span></span>
<span data-ttu-id="2fc64-168">그러나 "-Prefix My"를 지정 하면 cmdlet은 "My", "MyBlob1", "MyBlob2"를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc64-168">However, if you specify "-Prefix My", the cmdlet returns "My", "MyBlob1", and "MyBlob2".</span></span>

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

### <span data-ttu-id="2fc64-169">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2fc64-169">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="2fc64-170">요청에 대 한 서비스 측 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc64-170">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="2fc64-171">서비스가 요청을 처리 하기 전에 지정 된 간격이 경과 하면 저장소 서비스에서 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc64-171">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="2fc64-172">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="2fc64-172">-SnapshotTime</span></span>
<span data-ttu-id="2fc64-173">Blob SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="2fc64-173">Blob SnapshotTime</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: SingleBlobSnapshotTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fc64-174">-로</span><span class="sxs-lookup"><span data-stu-id="2fc64-174">-VersionId</span></span>
<span data-ttu-id="2fc64-175">물방울</span><span class="sxs-lookup"><span data-stu-id="2fc64-175">Blob VersionId</span></span>

```yaml
Type: System.String
Parameter Sets: SingleBlobVersionID
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fc64-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fc64-176">CommonParameters</span></span>
<span data-ttu-id="2fc64-177">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fc64-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fc64-178">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fc64-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fc64-179">입력</span><span class="sxs-lookup"><span data-stu-id="2fc64-179">INPUTS</span></span>

### <span data-ttu-id="2fc64-180">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2fc64-180">System.String</span></span>

### <span data-ttu-id="2fc64-181">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2fc64-181">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2fc64-182">출력</span><span class="sxs-lookup"><span data-stu-id="2fc64-182">OUTPUTS</span></span>

### <span data-ttu-id="2fc64-183">WindowsAzure. ResourceModel. m b m.</span><span class="sxs-lookup"><span data-stu-id="2fc64-183">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="2fc64-184">상속자</span><span class="sxs-lookup"><span data-stu-id="2fc64-184">NOTES</span></span>

## <span data-ttu-id="2fc64-185">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2fc64-185">RELATED LINKS</span></span>

[<span data-ttu-id="2fc64-186">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2fc64-186">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="2fc64-187">제거-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="2fc64-187">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)

[<span data-ttu-id="2fc64-188">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="2fc64-188">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)


