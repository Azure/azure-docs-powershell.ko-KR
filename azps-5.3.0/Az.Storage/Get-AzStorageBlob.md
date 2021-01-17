---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E54BFD3A-CD54-4E6B-9574-92B8D3E88FF3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlob.md
ms.openlocfilehash: 44c14b1f5aa8426bfb78205fa66a53d7db7e3440
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489304"
---
# <span data-ttu-id="66347-101">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="66347-101">Get-AzStorageBlob</span></span>

## <span data-ttu-id="66347-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66347-102">SYNOPSIS</span></span>
<span data-ttu-id="66347-103">컨테이너의 Blob을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="66347-103">Lists blobs in a container.</span></span>

## <span data-ttu-id="66347-104">구문</span><span class="sxs-lookup"><span data-stu-id="66347-104">SYNTAX</span></span>

### <span data-ttu-id="66347-105">BlobName(기본값)</span><span class="sxs-lookup"><span data-stu-id="66347-105">BlobName (Default)</span></span>
```
Get-AzStorageBlob [[-Blob] <String>] [-Container] <String> [-IncludeDeleted] [-MaxCount <Int32>]
 [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="66347-106">SingleBlobSnapshotTime</span><span class="sxs-lookup"><span data-stu-id="66347-106">SingleBlobSnapshotTime</span></span>
```
Get-AzStorageBlob [-Blob] <String> [-Container] <String> [-IncludeDeleted] -SnapshotTime <DateTimeOffset>
 [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="66347-107">SingleBlobVersionID</span><span class="sxs-lookup"><span data-stu-id="66347-107">SingleBlobVersionID</span></span>
```
Get-AzStorageBlob [-Blob] <String> [-Container] <String> [-IncludeDeleted] -VersionId <String>
 [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="66347-108">BlobPrefix</span><span class="sxs-lookup"><span data-stu-id="66347-108">BlobPrefix</span></span>
```
Get-AzStorageBlob [-Prefix <String>] [-Container] <String> [-IncludeDeleted] [-IncludeVersion]
 [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="66347-109">설명</span><span class="sxs-lookup"><span data-stu-id="66347-109">DESCRIPTION</span></span>
<span data-ttu-id="66347-110">**Get-AzStorageBlob** cmdlet은 Azure Storage 계정의 지정된 컨테이너에 Blob을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="66347-110">The **Get-AzStorageBlob** cmdlet lists blobs in the specified container in an Azure storage account.</span></span>

## <span data-ttu-id="66347-111">예제</span><span class="sxs-lookup"><span data-stu-id="66347-111">EXAMPLES</span></span>

### <span data-ttu-id="66347-112">예제 1: Blob 이름으로 Blob을 얻게</span><span class="sxs-lookup"><span data-stu-id="66347-112">Example 1: Get a blob by blob name</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Blob blob*
```

<span data-ttu-id="66347-113">이 명령은 Blob 이름 및 와일드카드를 사용하여 Blob을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="66347-113">This command uses a blob name and wildcard to get a blob.</span></span>

### <span data-ttu-id="66347-114">예제 2: 파이프라인을 사용하여 컨테이너에서 Blob을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="66347-114">Example 2: Get blobs in a container by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Name container* | Get-AzStorageBlob -IncludeDeleted

   Container Uri: https://storageaccountname.blob.core.windows.net/container1

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime         IsDeleted 
----                 --------  ------          -----------                    ------------         ---------- ------------         --------- 
test1                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:19Z            2017-11-08 08:19:32Z True      
test1                BlockBlob 403116          application/octet-stream       2017-11-08 09:00:29Z                                 True      
test2                BlockBlob 403116          application/octet-stream       2017-11-08 07:53:00Z                                 False
```

<span data-ttu-id="66347-115">이 명령은 파이프라인을 사용하여 컨테이너의 모든 Blob(삭제된 상태에 Blob 포함)을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="66347-115">This command uses the pipeline to get all blobs (include blobs in Deleted status) in a container.</span></span>

### <span data-ttu-id="66347-116">예제 3: 이름에 의해 Blob을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="66347-116">Example 3: Get blobs by name prefix</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Prefix "blob"
```

<span data-ttu-id="66347-117">이 명령은 이름 사전을 사용하여 Blob을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="66347-117">This command uses a name prefix to get blobs.</span></span>

### <span data-ttu-id="66347-118">예제 4: 여러 배치에 Blob 나열</span><span class="sxs-lookup"><span data-stu-id="66347-118">Example 4: List blobs in multiple batches</span></span>
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

<span data-ttu-id="66347-119">이 예제에서는 *MaxCount* 및 *ContinuationToken* 매개 변수를 사용하여 여러 배치에서 Azure Storage Blob을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="66347-119">This example uses the *MaxCount* and *ContinuationToken* parameters to list Azure Storage blobs in multiple batches.</span></span>
<span data-ttu-id="66347-120">처음 4개의 명령은 예제에서 사용할 변수에 값을 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="66347-120">The first four commands assign values to variables to use in the example.</span></span>
<span data-ttu-id="66347-121">다섯 번째 명령은 **Get-AzStorageBlob** cmdlet을 사용하여 Blob을 얻게 하는 **Do-While** 문을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="66347-121">The fifth command specifies a **Do-While** statement that uses the **Get-AzStorageBlob** cmdlet to get blobs.</span></span>
<span data-ttu-id="66347-122">이 문에는 다음 변수에 저장된 연속 토큰이 $Token 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="66347-122">The statement includes the continuation token stored in the $Token variable.</span></span>
<span data-ttu-id="66347-123">$Token 실행될 때 값을 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="66347-123">$Token changes value as the loop runs.</span></span>
<span data-ttu-id="66347-124">자세한 내용은 `Get-Help About_Do` .를 입력합니다.</span><span class="sxs-lookup"><span data-stu-id="66347-124">For more information, type `Get-Help About_Do`.</span></span>
<span data-ttu-id="66347-125">마지막 명령은 **Echo** 명령을 사용하여 합계를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="66347-125">The final command uses the **Echo** command to display the total.</span></span>

### <span data-ttu-id="66347-126">예제 5: 컨테이너의 모든 Blob에 Blob 버전 포함</span><span class="sxs-lookup"><span data-stu-id="66347-126">Example 5: Get all blobs in a container include blob version</span></span>
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

<span data-ttu-id="66347-127">이 명령은 컨테이너의 모든 Blob에 Blob 버전이 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="66347-127">This command gets all blobs in a container include blob version.</span></span>

### <span data-ttu-id="66347-128">예제 6: 단일 Blob 버전 다운로드</span><span class="sxs-lookup"><span data-stu-id="66347-128">Example 6: Get a single blob version</span></span>
```
PS C:\> Get-AzStorageBlob -Container "containername" -Blob blob2 -VersionId "2020-07-03T16:19:16.2883167Z" 

   AccountName: storageaccountname, ContainerName: containername

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
blob2                BlockBlob 2097152         application/octet-stream       2020-07-03 16:19:16Z Hot                                     False      2020-07-03T16:19:16.2883167Z
```

<span data-ttu-id="66347-129">이 명령은 VersionId를 사용하여 단일 Blob verion을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="66347-129">This command gets a single blobs verion with VersionId.</span></span>

### <span data-ttu-id="66347-130">예제 7: 단일 Blob 스냅숏 만들기</span><span class="sxs-lookup"><span data-stu-id="66347-130">Example 7: Get a single blob snapshot</span></span>
```
PS C:\> Get-AzStorageBlob -Container "containername" -Blob blob1 -SnapshotTime "2020-07-06T06:56:06.8588431Z"

   AccountName: storageaccountname, ContainerName: containername

Name                 BlobType  Length          ContentType                    LastModified         AccessTier SnapshotTime                 IsDeleted  VersionId                     
----                 --------  ------          -----------                    ------------         ---------- ------------                 ---------  ---------                     
blob1                BlockBlob 2097152         application/octet-stream       2020-07-06 06:56:06Z Hot        2020-07-06T06:56:06.8588431Z False
```

<span data-ttu-id="66347-131">이 명령은 SnapshotTime을 사용하여 단일 Blob 스냅숏을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="66347-131">This command gets a single blobs snapshot with SnapshotTime.</span></span>

## <span data-ttu-id="66347-132">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="66347-132">PARAMETERS</span></span>

### <span data-ttu-id="66347-133">-Blob</span><span class="sxs-lookup"><span data-stu-id="66347-133">-Blob</span></span>
<span data-ttu-id="66347-134">와일드카드 검색에 사용할 수 있는 이름 또는 이름 패턴을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="66347-134">Specifies a name or name pattern, which can be used for a wildcard search.</span></span>
<span data-ttu-id="66347-135">Blob 이름이 지정되지 않은 경우 cmdlet은 지정된 컨테이너의 모든 Blob을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="66347-135">If no blob name is specified, the cmdlet lists all the blobs in the specified container.</span></span>
<span data-ttu-id="66347-136">이 매개 변수에 값을 지정하면 cmdlet에 이 매개 변수와 일치하는 이름이 있는 모든 Blob이 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="66347-136">If a value is specified for this parameter, the cmdlet lists all blobs with names that match this parameter.</span></span> <span data-ttu-id="66347-137">이 매개 변수는 문자열의 어디에서나 와일드카드를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="66347-137">This parameter supports wildcards anywhere in the string.</span></span>

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

### <span data-ttu-id="66347-138">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="66347-138">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="66347-139">하나의 서비스 요청에 대해 클라이언트 쪽 시간(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="66347-139">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="66347-140">이전 호출이 지정된 간격에서 실패하는 경우 이 cmdlet은 요청을 다시 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="66347-140">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="66347-141">이 cmdlet이 간격이 경과하기 전에 성공적인 응답을 받지 못하면 이 cmdlet은 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="66347-141">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="66347-142">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="66347-142">-ConcurrentTaskCount</span></span>
<span data-ttu-id="66347-143">최대 동시 네트워크 호출을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="66347-143">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="66347-144">이 매개 변수를 사용하여 최대 동시 네트워크 호출 수를 지정하여 동시성으로 로컬 CPU 및 대역폭 사용량을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="66347-144">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="66347-145">지정된 값은 절대 개수로, 코어 수에 곱하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="66347-145">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="66347-146">이 매개 변수는 초당 100킬로비트와 같은 낮은 대역폭 환경에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="66347-146">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="66347-147">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="66347-147">The default value is 10.</span></span>

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

### <span data-ttu-id="66347-148">-Container</span><span class="sxs-lookup"><span data-stu-id="66347-148">-Container</span></span>
<span data-ttu-id="66347-149">컨테이너의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="66347-149">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="66347-150">-Context</span><span class="sxs-lookup"><span data-stu-id="66347-150">-Context</span></span>
<span data-ttu-id="66347-151">Blob 목록을 얻을 Azure Storage 계정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="66347-151">Specifies the Azure storage account from which you want to get a list of blobs.</span></span>
<span data-ttu-id="66347-152">New-AzStorageContext cmdlet을 사용하여 저장소 컨텍스트를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="66347-152">You can use the New-AzStorageContext cmdlet to create a storage context.</span></span>

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

### <span data-ttu-id="66347-153">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="66347-153">-ContinuationToken</span></span>
<span data-ttu-id="66347-154">Blob 목록에 대한 연속 토큰을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="66347-154">Specifies a continuation token for the blob list.</span></span>
<span data-ttu-id="66347-155">이 매개 변수와 *MaxCount* 매개 변수를 사용하여 여러 배치에 Blob을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="66347-155">Use this parameter and the *MaxCount* parameter to list blobs in multiple batches.</span></span>

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

### <span data-ttu-id="66347-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66347-156">-DefaultProfile</span></span>
<span data-ttu-id="66347-157">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="66347-157">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66347-158">-IncludeDeleted</span><span class="sxs-lookup"><span data-stu-id="66347-158">-IncludeDeleted</span></span>
<span data-ttu-id="66347-159">삭제된 Blob을 포함하면 기본적으로 Blob get은 삭제된 Blob을 포함하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="66347-159">Include Deleted Blob, by default get blob won't include deleted blob.</span></span>

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

### <span data-ttu-id="66347-160">-IncludeVersion</span><span class="sxs-lookup"><span data-stu-id="66347-160">-IncludeVersion</span></span>
<span data-ttu-id="66347-161">Blob 버전은 이 매개 변수가 있는 경우만 나열됩니다. 기본적으로 blob get blob 버전은 포함하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="66347-161">Blob versions will be listed only if this parameter is present, by default get blob won't include blob versions.</span></span>

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

### <span data-ttu-id="66347-162">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="66347-162">-MaxCount</span></span>
<span data-ttu-id="66347-163">이 cmdlet이 반환하는 개체의 최대 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="66347-163">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="66347-164">-Prefix</span><span class="sxs-lookup"><span data-stu-id="66347-164">-Prefix</span></span>
<span data-ttu-id="66347-165">얻게 할 Blob 이름에 대한 prefix를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="66347-165">Specifies a prefix for the blob names that you want to get.</span></span>
<span data-ttu-id="66347-166">이 매개 변수는 정규식 또는 와일드카드 문자를 사용하여 검색을 지원하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="66347-166">This parameter does not support using regular expressions or wildcard characters to search.</span></span>
<span data-ttu-id="66347-167">즉, 컨테이너에 "My", "MyBlob1" 및 "MyBlob2"라는 Blob만 있는 경우 "-Prefix My\*"를 지정하면 cmdlet은 Blob이 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="66347-167">This means that if the container has only blobs named "My", "MyBlob1", and "MyBlob2" and you specify "-Prefix My\*", the cmdlet returns no blobs.</span></span>
<span data-ttu-id="66347-168">그러나 "-Prefix My"를 지정하면 cmdlet은 "My", "MyBlob1" 및 "MyBlob2"를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="66347-168">However, if you specify "-Prefix My", the cmdlet returns "My", "MyBlob1", and "MyBlob2".</span></span>

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

### <span data-ttu-id="66347-169">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="66347-169">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="66347-170">요청에 대한 서비스 쪽 시간제한 간격(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="66347-170">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="66347-171">지정된 간격이 서비스에서 요청을 처리하기 전에 경과하면 저장소 서비스가 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="66347-171">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="66347-172">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="66347-172">-SnapshotTime</span></span>
<span data-ttu-id="66347-173">Blob SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="66347-173">Blob SnapshotTime</span></span>

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

### <span data-ttu-id="66347-174">-VersionId</span><span class="sxs-lookup"><span data-stu-id="66347-174">-VersionId</span></span>
<span data-ttu-id="66347-175">Blob VersionId</span><span class="sxs-lookup"><span data-stu-id="66347-175">Blob VersionId</span></span>

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

### <span data-ttu-id="66347-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66347-176">CommonParameters</span></span>
<span data-ttu-id="66347-177">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="66347-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66347-178">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="66347-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66347-179">입력</span><span class="sxs-lookup"><span data-stu-id="66347-179">INPUTS</span></span>

### <span data-ttu-id="66347-180">System.String</span><span class="sxs-lookup"><span data-stu-id="66347-180">System.String</span></span>

### <span data-ttu-id="66347-181">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="66347-181">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="66347-182">출력</span><span class="sxs-lookup"><span data-stu-id="66347-182">OUTPUTS</span></span>

### <span data-ttu-id="66347-183">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="66347-183">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="66347-184">참고 사항</span><span class="sxs-lookup"><span data-stu-id="66347-184">NOTES</span></span>

## <span data-ttu-id="66347-185">관련 링크</span><span class="sxs-lookup"><span data-stu-id="66347-185">RELATED LINKS</span></span>

[<span data-ttu-id="66347-186">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="66347-186">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="66347-187">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="66347-187">Remove-AzStorageBlob</span></span>](./Remove-AzStorageBlob.md)

[<span data-ttu-id="66347-188">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="66347-188">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)


