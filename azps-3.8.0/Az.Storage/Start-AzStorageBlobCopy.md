---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 54585346-04E2-4FB4-B5FD-833A85C46ACB
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/start-azstorageblobcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobCopy.md
ms.openlocfilehash: 36ae8a00237be287262de0cc9eac4022b9efc9d5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034966"
---
# <span data-ttu-id="71613-101">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="71613-101">Start-AzStorageBlobCopy</span></span>

## <span data-ttu-id="71613-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71613-102">SYNOPSIS</span></span>
<span data-ttu-id="71613-103">Blob 복사를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="71613-103">Starts to copy a blob.</span></span>

## <span data-ttu-id="71613-104">구문과</span><span class="sxs-lookup"><span data-stu-id="71613-104">SYNTAX</span></span>

### <span data-ttu-id="71613-105">ContainerName (기본값)</span><span class="sxs-lookup"><span data-stu-id="71613-105">ContainerName (Default)</span></span>
```
Start-AzStorageBlobCopy [-SrcBlob] <String> -SrcContainer <String> -DestContainer <String> [-DestBlob <String>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="71613-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="71613-106">BlobInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlob <CloudBlob> -DestContainer <String> [-DestBlob <String>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="71613-107">Blobinstanceetobinstance</span><span class="sxs-lookup"><span data-stu-id="71613-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlob <CloudBlob> -DestCloudBlob <CloudBlob>
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="71613-108">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="71613-108">ContainerInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-SrcBlob] <String> -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="71613-109">ShareName</span><span class="sxs-lookup"><span data-stu-id="71613-109">ShareName</span></span>
```
Start-AzStorageBlobCopy -SrcShareName <String> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71613-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="71613-110">ShareInstance</span></span>
```
Start-AzStorageBlobCopy -SrcShare <CloudFileShare> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71613-111">해당 인스턴스</span><span class="sxs-lookup"><span data-stu-id="71613-111">DirInstance</span></span>
```
Start-AzStorageBlobCopy -SrcDir <CloudFileDirectory> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71613-112">FileInstance</span><span class="sxs-lookup"><span data-stu-id="71613-112">FileInstance</span></span>
```
Start-AzStorageBlobCopy -SrcFile <CloudFile> -DestContainer <String> [-DestBlob <String>]
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71613-113">Fileinstanceetobinstance</span><span class="sxs-lookup"><span data-stu-id="71613-113">FileInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobCopy -SrcFile <CloudFile> -DestCloudBlob <CloudBlob> [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="71613-114">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="71613-114">UriPipeline</span></span>
```
Start-AzStorageBlobCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71613-115">설명은</span><span class="sxs-lookup"><span data-stu-id="71613-115">DESCRIPTION</span></span>
<span data-ttu-id="71613-116">**AzStorageBlobCopy** cmdlet을 시작 하 여 blob을 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="71613-116">The **Start-AzStorageBlobCopy** cmdlet starts to copy a blob.</span></span>

## <span data-ttu-id="71613-117">예제의</span><span class="sxs-lookup"><span data-stu-id="71613-117">EXAMPLES</span></span>

### <span data-ttu-id="71613-118">예제 1: 명명 된 blob 복사</span><span class="sxs-lookup"><span data-stu-id="71613-118">Example 1: Copy a named blob</span></span>
```
C:\PS>Start-AzStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives" -SrcContainer "ContosoUploads"
```

<span data-ttu-id="71613-119">이 명령은 ContosoUploads 이라는 컨테이너에서 ContosoPlanning2015 라는 blob의 복사 작업을 ContosoArchives 이라는 컨테이너에 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="71613-119">This command starts the copy operation of the blob named ContosoPlanning2015 from the container named ContosoUploads to the container named ContosoArchives.</span></span>

### <span data-ttu-id="71613-120">예제 2: 복사할 blob을 지정 하는 컨테이너 가져오기</span><span class="sxs-lookup"><span data-stu-id="71613-120">Example 2: Get a container to specify blobs to copy</span></span>
```
C:\PS>Get-AzStorageContainer -Name "ContosoUploads" | Start-AzStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives"
```

<span data-ttu-id="71613-121">이 명령은 **AzStorageContainer** cmdlet을 사용 하 여 ContosoUploads 이라는 컨테이너를 가져온 다음 파이프라인 연산자를 사용 하 여 현재 cmdlet에 컨테이너를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="71613-121">This command gets the container named ContosoUploads, by using the **Get-AzStorageContainer** cmdlet, and then passes the container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="71613-122">해당 cmdlet은 ContosoPlanning2015 이라는 blob의 복사 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="71613-122">That cmdlet starts the copy operation of the blob named ContosoPlanning2015.</span></span>
<span data-ttu-id="71613-123">이전 cmdlet은 원본 컨테이너를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="71613-123">The previous cmdlet provides the source container.</span></span>
<span data-ttu-id="71613-124">*Destcontainer* 매개 변수는 ContosoArchives를 대상 컨테이너로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71613-124">The *DestContainer* parameter specifies ContosoArchives as the destination container.</span></span>

### <span data-ttu-id="71613-125">예제 3: 컨테이너의 모든 blob 가져오기 및 복사</span><span class="sxs-lookup"><span data-stu-id="71613-125">Example 3: Get all blobs in a container and copy them</span></span>
```
C:\PS>Get-AzStorageBlob -Container "ContosoUploads" | Start-AzStorageBlobCopy -DestContainer "ContosoArchives"
```

<span data-ttu-id="71613-126">이 명령은 **AzStorageBlob** cmdlet을 사용 하 여 ContosoUploads 이라는 컨테이너의 blob을 가져온 다음 파이프라인 연산자를 사용 하 여 현재 cmdlet에 결과를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="71613-126">This command gets the blobs in the container named ContosoUploads, by using the **Get-AzStorageBlob** cmdlet, and then passes the results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="71613-127">해당 cmdlet은 ContosoArchives 이라는 컨테이너에 대 한 blob의 복사 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="71613-127">That cmdlet starts the copy operation of the blobs to the container named ContosoArchives.</span></span>

### <span data-ttu-id="71613-128">예제 4: 개체로 지정 된 blob 복사</span><span class="sxs-lookup"><span data-stu-id="71613-128">Example 4: Copy a blob specified as an object</span></span>
```
C:\PS>$SrcBlob = Get-AzStorageBlob -Container "ContosoUploads" -Blob "ContosoPlanning2015"
C:\PS> $DestBlob = Get-AzStorageBlob -Container "ContosoArchives" -Blob "ContosoPlanning2015Archived"
C:\PS> Start-AzStorageBlobCopy -ICloudBlob $SrcBlob.ICloudBlob -DestICloudBlob $DestBlob.ICloudBlob
```

<span data-ttu-id="71613-129">첫 번째 명령은 ContosoUploads 이라는 컨테이너에서 ContosoPlanning2015 라는 blob를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="71613-129">The first command gets the blob named ContosoPlanning2015 in the container named ContosoUploads.</span></span>
<span data-ttu-id="71613-130">명령이 $SrcBlob 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="71613-130">The command stores that object in the $SrcBlob variable.</span></span>
<span data-ttu-id="71613-131">두 번째 명령은 ContosoArchives 이라는 컨테이너에서 ContosoPlanning2015Archived 라는 blob를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="71613-131">The second command gets the blob named ContosoPlanning2015Archived in the container named ContosoArchives.</span></span>
<span data-ttu-id="71613-132">명령이 $DestBlob 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="71613-132">The command stores that object in the $DestBlob variable.</span></span>
<span data-ttu-id="71613-133">마지막 명령은 원본 컨테이너에서 대상 컨테이너로 복사 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="71613-133">The last command starts the copy operation from the source container to the destination container.</span></span>
<span data-ttu-id="71613-134">명령에서는 표준 점 표기법을 사용 하 여 $SrcBlob 및 $DestBlob blob에 대 한 **ICloudBlob** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71613-134">The command uses standard dot notation to specify the **ICloudBlob** objects for the $SrcBlob and $DestBlob blobs.</span></span>

### <span data-ttu-id="71613-135">예제 5: URI에서 blob 복사</span><span class="sxs-lookup"><span data-stu-id="71613-135">Example 5: Copy a blob from a URI</span></span>
```
C:\PS>$Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
C:\PS> Start-AzStorageBlobCopy -AbsoluteUri "http://www.contosointernal.com/planning" -DestContainer "ContosoArchive" -DestBlob "ContosoPlanning2015" -DestContext $Context
```

<span data-ttu-id="71613-136">이 명령은 지정 된 키를 사용 하는 ContosoGeneral 이라는 계정에 대 한 컨텍스트를 만든 다음 해당 키를 $Context 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="71613-136">This command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that key in the $Context variable.</span></span>
<span data-ttu-id="71613-137">두 번째 명령은 지정 된 URI의 파일을 ContosoArchive 이라는 컨테이너에 있는 ContosoPlanning 이라는 blob에 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="71613-137">The second command copies the file from the specified URI to the blob named ContosoPlanning in the container named ContosoArchive.</span></span>
<span data-ttu-id="71613-138">이 명령은 $Context에 저장 된 컨텍스트에서 복사 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="71613-138">The command starts the copy operation in the context stored in $Context.</span></span>

### <span data-ttu-id="71613-139">예제 6: 블록 blob을 새 blob 이름으로 대상 컨테이너에 복사 하 고 대상 blob StandardBlobTier Hot로 RehydratePriority를 높게 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71613-139">Example 6: Copy a block blob to destination container with a new blob name, and set destination blob StandardBlobTier as Hot, RehydratePriority as High</span></span>
```
C:\PS>Start-AzStorageBlobCopy -SrcContainer "ContosoUploads" -SrcBlob "BlockBlobName" -DestContainer "ContosoArchives" -DestBlob "NewBlockBlobName" -StandardBlobTier Hot -RehydratePriority High
```

<span data-ttu-id="71613-140">이 명령은 블록 blob의 복사 작업을 새 blob 이름으로 대상 컨테이너로 시작 하 고, 대상 blob StandardBlobTier Hot로 RehydratePriority를 높게 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71613-140">This command starts the copy operation of a block blob to destination container with a new blob name, and set destination blob StandardBlobTier as Hot, RehydratePriority as High</span></span>

## <span data-ttu-id="71613-141">변수</span><span class="sxs-lookup"><span data-stu-id="71613-141">PARAMETERS</span></span>

### <span data-ttu-id="71613-142">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="71613-142">-AbsoluteUri</span></span>
<span data-ttu-id="71613-143">Azure Storage blob에 복사할 파일의 절대 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71613-143">Specifies the absolute URI of a file to copy to an Azure Storage blob.</span></span>

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

### <span data-ttu-id="71613-144">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="71613-144">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="71613-145">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71613-145">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="71613-146">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="71613-146">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="71613-147">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="71613-147">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="71613-148">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="71613-148">-CloudBlob</span></span>
<span data-ttu-id="71613-149">Azure Storage 클라이언트 라이브러리에서 **CloudBlob** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71613-149">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="71613-150">**CloudBlob** 개체를 가져오려면 Get-AzStorageBlob cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="71613-150">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases: SrcICloudBlob, SrcCloudBlob, ICloudBlob, SourceICloudBlob, SourceCloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71613-151">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="71613-151">-CloudBlobContainer</span></span>
<span data-ttu-id="71613-152">Azure Storage 클라이언트 라이브러리에서 **CloudBlobContainer** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71613-152">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="71613-153">이 cmdlet은이 매개 변수에서 지정 하는 컨테이너에서 blob을 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="71613-153">This cmdlet copies a blob from the container that this parameter specifies.</span></span>
<span data-ttu-id="71613-154">**CloudBlobContainer** 개체를 가져오려면 Get-AzStorageContainer cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="71613-154">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="71613-155">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="71613-155">-ConcurrentTaskCount</span></span>
<span data-ttu-id="71613-156">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71613-156">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="71613-157">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="71613-157">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="71613-158">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="71613-158">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="71613-159">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="71613-159">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="71613-160">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="71613-160">The default value is 10.</span></span>

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

### <span data-ttu-id="71613-161">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="71613-161">-Context</span></span>
<span data-ttu-id="71613-162">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71613-162">Specifies an Azure storage context.</span></span>
<span data-ttu-id="71613-163">저장소 컨텍스트를 얻으려면 New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="71613-163">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ContainerName, BlobInstance, BlobInstanceToBlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance, FileInstanceToBlobInstance
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

### <span data-ttu-id="71613-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71613-164">-DefaultProfile</span></span>
<span data-ttu-id="71613-165">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="71613-165">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="71613-166">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="71613-166">-DestBlob</span></span>
<span data-ttu-id="71613-167">대상 blob의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71613-167">Specifies the name of the destination blob.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, BlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance
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

### <span data-ttu-id="71613-168">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="71613-168">-DestCloudBlob</span></span>
<span data-ttu-id="71613-169">대상 **CloudBlob** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71613-169">Specifies a destination **CloudBlob** object</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.CloudBlob
Parameter Sets: BlobInstanceToBlobInstance, FileInstanceToBlobInstance
Aliases: DestICloudBlob, DestinationCloudBlob, DestinationICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71613-170">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="71613-170">-DestContainer</span></span>
<span data-ttu-id="71613-171">대상 컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71613-171">Specifies the name of the destination container.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, BlobInstance, ContainerInstance, ShareName, ShareInstance, DirInstance, FileInstance, UriPipeline
Aliases: DestinationContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71613-172">DestContext</span><span class="sxs-lookup"><span data-stu-id="71613-172">-DestContext</span></span>
<span data-ttu-id="71613-173">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71613-173">Specifies an Azure storage context.</span></span>
<span data-ttu-id="71613-174">저장소 컨텍스트를 얻으려면 New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="71613-174">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="71613-175">-Force</span><span class="sxs-lookup"><span data-stu-id="71613-175">-Force</span></span>
<span data-ttu-id="71613-176">이 cmdlet이 확인 메시지를 표시 하지 않고 대상 blob을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="71613-176">Indicates that this cmdlet overwrites the destination blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="71613-177">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="71613-177">-PremiumPageBlobTier</span></span>
<span data-ttu-id="71613-178">프리미엄 페이지 Blob 계층</span><span class="sxs-lookup"><span data-stu-id="71613-178">Premium Page Blob Tier</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.PremiumPageBlobTier
Parameter Sets: ContainerName, BlobInstance, BlobInstanceToBlobInstance, ContainerInstance
Aliases:
Accepted values: Unknown, P4, P6, P10, P20, P30, P40, P50, P60

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71613-179">-RehydratePriority</span><span class="sxs-lookup"><span data-stu-id="71613-179">-RehydratePriority</span></span>
<span data-ttu-id="71613-180">Block Blob RehydratePriority.</span><span class="sxs-lookup"><span data-stu-id="71613-180">Block Blob RehydratePriority.</span></span> <span data-ttu-id="71613-181">보관 된 blob을 rehydrate 하는 우선 순위를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="71613-181">Indicates the priority with which to rehydrate an archived blob.</span></span> <span data-ttu-id="71613-182">유효한 값은 높음/표준입니다.</span><span class="sxs-lookup"><span data-stu-id="71613-182">Valid values are High/Standard.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.RehydratePriority
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71613-183">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="71613-183">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="71613-184">요청에 대 한 서비스 측 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71613-184">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="71613-185">서비스가 요청을 처리 하기 전에 지정 된 간격이 경과 하면 저장소 서비스에서 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="71613-185">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="71613-186">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="71613-186">-SrcBlob</span></span>
<span data-ttu-id="71613-187">원본 blob의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71613-187">Specifies the name of the source blob.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName, ContainerInstance
Aliases: SourceBlob

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71613-188">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="71613-188">-SrcContainer</span></span>
<span data-ttu-id="71613-189">원본 컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71613-189">Specifies the name of the source container.</span></span>

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

### <span data-ttu-id="71613-190">-SrcDir</span><span class="sxs-lookup"><span data-stu-id="71613-190">-SrcDir</span></span>
<span data-ttu-id="71613-191">Azure Storage 클라이언트 라이브러리에서 **Cloudfiledirectory** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71613-191">Specifies a **CloudFileDirectory** object from Azure Storage Client library.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileDirectory
Parameter Sets: DirInstance
Aliases: SourceDir

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71613-192">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="71613-192">-SrcFile</span></span>
<span data-ttu-id="71613-193">Azure Storage 클라이언트 라이브러리에서 **Cloudfile** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71613-193">Specifies a **CloudFile** object from Azure Storage Client library.</span></span>
<span data-ttu-id="71613-194">이를 만들거나 Get-AzStorageFile cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="71613-194">You can create it or use Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFile
Parameter Sets: FileInstance, FileInstanceToBlobInstance
Aliases: SourceFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="71613-195">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="71613-195">-SrcFilePath</span></span>
<span data-ttu-id="71613-196">원본 디렉터리 또는 원본 공유의 원본 파일 상대 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71613-196">Specifies the source file relative path of source directory or source share.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName, ShareInstance, DirInstance
Aliases: SourceFilePath

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71613-197">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="71613-197">-SrcShare</span></span>
<span data-ttu-id="71613-198">Azure Storage 클라이언트 라이브러리에서 **Cloudfileshare** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71613-198">Specifies a **CloudFileShare** object from Azure Storage Client library.</span></span>
<span data-ttu-id="71613-199">이를 만들거나 Get-AzStorageShare cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="71613-199">You can create it or use Get-AzStorageShare cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Storage.File.CloudFileShare
Parameter Sets: ShareInstance
Aliases: SourceShare

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71613-200">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="71613-200">-SrcShareName</span></span>
<span data-ttu-id="71613-201">원본 공유 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71613-201">Specifies the source share name.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases: SourceShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71613-202">-StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="71613-202">-StandardBlobTier</span></span>
<span data-ttu-id="71613-203">Block Blob 계층, 유효한 값은 Hot/Archive입니다.</span><span class="sxs-lookup"><span data-stu-id="71613-203">Block Blob Tier, valid values are Hot/Cool/Archive.</span></span>
<span data-ttu-id="71613-204">세부 정보 참조 https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span><span class="sxs-lookup"><span data-stu-id="71613-204">See detail in https://docs.microsoft.com/en-us/azure/storage/blobs/storage-blob-storage-tiers</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71613-205">-확인</span><span class="sxs-lookup"><span data-stu-id="71613-205">-Confirm</span></span>
<span data-ttu-id="71613-206">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="71613-206">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71613-207">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71613-207">-WhatIf</span></span>
<span data-ttu-id="71613-208">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="71613-208">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71613-209">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="71613-209">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71613-210">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71613-210">CommonParameters</span></span>
<span data-ttu-id="71613-211">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="71613-211">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71613-212">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71613-212">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71613-213">입력</span><span class="sxs-lookup"><span data-stu-id="71613-213">INPUTS</span></span>

### <span data-ttu-id="71613-214">CloudBlob를 통해 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="71613-214">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="71613-215">CloudBlobContainer를 통해 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="71613-215">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="71613-216">Microsoft. c c. | 파일</span><span class="sxs-lookup"><span data-stu-id="71613-216">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="71613-217">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="71613-217">System.String</span></span>

### <span data-ttu-id="71613-218">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="71613-218">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="71613-219">출력</span><span class="sxs-lookup"><span data-stu-id="71613-219">OUTPUTS</span></span>

### <span data-ttu-id="71613-220">WindowsAzure. ResourceModel. m b m.</span><span class="sxs-lookup"><span data-stu-id="71613-220">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="71613-221">상속자</span><span class="sxs-lookup"><span data-stu-id="71613-221">NOTES</span></span>

## <span data-ttu-id="71613-222">관련 링크</span><span class="sxs-lookup"><span data-stu-id="71613-222">RELATED LINKS</span></span>

[<span data-ttu-id="71613-223">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="71613-223">Get-AzStorageBlobCopyState</span></span>](./Get-AzStorageBlobCopyState.md)

[<span data-ttu-id="71613-224">중지-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="71613-224">Stop-AzStorageBlobCopy</span></span>](./Stop-AzStorageBlobCopy.md)
