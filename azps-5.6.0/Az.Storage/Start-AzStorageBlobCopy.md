---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 54585346-04E2-4FB4-B5FD-833A85C46ACB
online version: https://docs.microsoft.com/powershell/module/az.storage/start-azstorageblobcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Start-AzStorageBlobCopy.md
ms.openlocfilehash: 754ac7657561ba52e28f90d951c0843a8c206484
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002235"
---
# <span data-ttu-id="3546a-101">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="3546a-101">Start-AzStorageBlobCopy</span></span>

## <span data-ttu-id="3546a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3546a-102">SYNOPSIS</span></span>
<span data-ttu-id="3546a-103">Blob을 복사하기 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-103">Starts to copy a blob.</span></span>

## <span data-ttu-id="3546a-104">구문</span><span class="sxs-lookup"><span data-stu-id="3546a-104">SYNTAX</span></span>

### <span data-ttu-id="3546a-105">ContainerName(기본값)</span><span class="sxs-lookup"><span data-stu-id="3546a-105">ContainerName (Default)</span></span>
```
Start-AzStorageBlobCopy [-SrcBlob] <String> -SrcContainer <String> -DestContainer <String> [-DestBlob <String>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3546a-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="3546a-106">BlobInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3546a-107">BlobInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="3546a-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] -DestCloudBlob <CloudBlob>
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3546a-108">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="3546a-108">ContainerInstance</span></span>
```
Start-AzStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-SrcBlob] <String> -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3546a-109">ShareName</span><span class="sxs-lookup"><span data-stu-id="3546a-109">ShareName</span></span>
```
Start-AzStorageBlobCopy -SrcShareName <String> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3546a-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="3546a-110">ShareInstance</span></span>
```
Start-AzStorageBlobCopy -SrcShare <CloudFileShare> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3546a-111">DirInstance</span><span class="sxs-lookup"><span data-stu-id="3546a-111">DirInstance</span></span>
```
Start-AzStorageBlobCopy -SrcDir <CloudFileDirectory> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3546a-112">FileInstance</span><span class="sxs-lookup"><span data-stu-id="3546a-112">FileInstance</span></span>
```
Start-AzStorageBlobCopy -SrcFile <CloudFile> -DestContainer <String> [-DestBlob <String>]
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3546a-113">FileInstanceToBlobInstance</span><span class="sxs-lookup"><span data-stu-id="3546a-113">FileInstanceToBlobInstance</span></span>
```
Start-AzStorageBlobCopy -SrcFile <CloudFile> -DestCloudBlob <CloudBlob> [-StandardBlobTier <String>]
 [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3546a-114">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="3546a-114">UriPipeline</span></span>
```
Start-AzStorageBlobCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-StandardBlobTier <String>] [-RehydratePriority <RehydratePriority>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3546a-115">설명</span><span class="sxs-lookup"><span data-stu-id="3546a-115">DESCRIPTION</span></span>
<span data-ttu-id="3546a-116">**Start-AzStorageBlobCopy** cmdlet은 Blob을 복사하기 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-116">The **Start-AzStorageBlobCopy** cmdlet starts to copy a blob.</span></span>

## <span data-ttu-id="3546a-117">예제</span><span class="sxs-lookup"><span data-stu-id="3546a-117">EXAMPLES</span></span>

### <span data-ttu-id="3546a-118">예제 1: 명명된 Blob 복사</span><span class="sxs-lookup"><span data-stu-id="3546a-118">Example 1: Copy a named blob</span></span>
```
C:\PS>Start-AzStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives" -SrcContainer "ContosoUploads"
```

<span data-ttu-id="3546a-119">이 명령은 ContosoUploads라는 컨테이너에서 ContosoArchives라는 컨테이너로 ContosoPlanning2015라는 Blob의 복사 작업을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-119">This command starts the copy operation of the blob named ContosoPlanning2015 from the container named ContosoUploads to the container named ContosoArchives.</span></span>

### <span data-ttu-id="3546a-120">예제 2: 복사할 Blob을 지정하는 컨테이너를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-120">Example 2: Get a container to specify blobs to copy</span></span>
```
C:\PS>Get-AzStorageContainer -Name "ContosoUploads" | Start-AzStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives"
```

<span data-ttu-id="3546a-121">이 명령은 **Get-AzStorageContainer** cmdlet을 사용하여 ContosoUploads라는 컨테이너를 얻은 다음 파이프라인 연산자를 사용하여 컨테이너를 현재 cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-121">This command gets the container named ContosoUploads, by using the **Get-AzStorageContainer** cmdlet, and then passes the container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3546a-122">해당 cmdlet은 ContosoPlanning2015라는 Blob의 복사 작업을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-122">That cmdlet starts the copy operation of the blob named ContosoPlanning2015.</span></span>
<span data-ttu-id="3546a-123">이전 cmdlet은 원본 컨테이너를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-123">The previous cmdlet provides the source container.</span></span>
<span data-ttu-id="3546a-124">*DestContainer 매개* 변수는 ContosoArchives를 대상 컨테이너로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-124">The *DestContainer* parameter specifies ContosoArchives as the destination container.</span></span>

### <span data-ttu-id="3546a-125">예제 3: 컨테이너의 모든 Blob을 다운로드하고 복사합니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-125">Example 3: Get all blobs in a container and copy them</span></span>
```
C:\PS>Get-AzStorageBlob -Container "ContosoUploads" | Start-AzStorageBlobCopy -DestContainer "ContosoArchives"
```

<span data-ttu-id="3546a-126">이 명령은 **Get-AzStorageBlob** cmdlet을 사용하여 ContosoUploads라는 컨테이너의 Blob을 얻은 다음 파이프라인 연산자를 사용하여 현재 cmdlet에 결과를 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-126">This command gets the blobs in the container named ContosoUploads, by using the **Get-AzStorageBlob** cmdlet, and then passes the results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="3546a-127">해당 cmdlet은 ContosoArchives라는 컨테이너에 Blob의 복사 작업을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-127">That cmdlet starts the copy operation of the blobs to the container named ContosoArchives.</span></span>

### <span data-ttu-id="3546a-128">예제 4: 개체로 지정된 Blob 복사</span><span class="sxs-lookup"><span data-stu-id="3546a-128">Example 4: Copy a blob specified as an object</span></span>
```
C:\PS>$SrcBlob = Get-AzStorageBlob -Container "ContosoUploads" -Blob "ContosoPlanning2015"
C:\PS> $DestBlob = Get-AzStorageBlob -Container "ContosoArchives" -Blob "ContosoPlanning2015Archived"
C:\PS> Start-AzStorageBlobCopy -ICloudBlob $SrcBlob.ICloudBlob -DestICloudBlob $DestBlob.ICloudBlob
```

<span data-ttu-id="3546a-129">첫 번째 명령은 ContosoUploads라는 컨테이너에서 ContosoPlanning2015라는 Blob을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-129">The first command gets the blob named ContosoPlanning2015 in the container named ContosoUploads.</span></span>
<span data-ttu-id="3546a-130">명령은 해당 개체를 $SrcBlob 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-130">The command stores that object in the $SrcBlob variable.</span></span>
<span data-ttu-id="3546a-131">두 번째 명령은 ContosoArchives라는 컨테이너에서 ContosoPlanning2015Archived라는 Blob을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-131">The second command gets the blob named ContosoPlanning2015Archived in the container named ContosoArchives.</span></span>
<span data-ttu-id="3546a-132">명령은 해당 개체를 $DestBlob 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-132">The command stores that object in the $DestBlob variable.</span></span>
<span data-ttu-id="3546a-133">마지막 명령은 원본 컨테이너에서 대상 컨테이너로 복사 작업을 시작합니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-133">The last command starts the copy operation from the source container to the destination container.</span></span>
<span data-ttu-id="3546a-134">명령은 표준 점표를 사용하여 **blob** 및 $SrcBlob $DestBlob 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-134">The command uses standard dot notation to specify the **ICloudBlob** objects for the $SrcBlob and $DestBlob blobs.</span></span>

### <span data-ttu-id="3546a-135">예제 5: URI에서 Blob 복사</span><span class="sxs-lookup"><span data-stu-id="3546a-135">Example 5: Copy a blob from a URI</span></span>
```
C:\PS>$Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
C:\PS> Start-AzStorageBlobCopy -AbsoluteUri "http://www.contosointernal.com/planning" -DestContainer "ContosoArchive" -DestBlob "ContosoPlanning2015" -DestContext $Context
```

<span data-ttu-id="3546a-136">이 명령은 지정된 키를 사용하는 ContosoGeneral이라는 계정에 대한 컨텍스트를 만든 다음 해당 $Context 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-136">This command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that key in the $Context variable.</span></span>
<span data-ttu-id="3546a-137">두 번째 명령은 ContosoArchive라는 컨테이너에서 ContosoPlanning이라는 Blob에 지정된 URI에서 파일을 복사합니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-137">The second command copies the file from the specified URI to the blob named ContosoPlanning in the container named ContosoArchive.</span></span>
<span data-ttu-id="3546a-138">명령은 에 저장된 대상 컨텍스트로 복사 작업을 $Context.</span><span class="sxs-lookup"><span data-stu-id="3546a-138">The command starts the copy operation to the destination context stored in $Context.</span></span>
<span data-ttu-id="3546a-139">원본 저장소 컨텍스트가 없습니다. 따라서 원본 Uri는 원본 개체에 대한 액세스 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-139">There are no source storage context, so the source Uri must have access to the source object.</span></span> <span data-ttu-id="3546a-140">예: 원본이 공용 Azure Blob이 없는 경우 Uri에는 Blob에 대한 읽기 액세스 권한이 있는 SAS 토큰이 포함되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-140">E.g: if the source is a none public Azure blob, the Uri should contain SAS token which has read access to the blob.</span></span>

### <span data-ttu-id="3546a-141">예제 6: 새 Blob 이름으로 대상 컨테이너에 블록 Blob을 복사하고 대상 Blob StandardBlobTier를 핫으로 설정하고 높음으로 다시 하이하이드레이트Priority</span><span class="sxs-lookup"><span data-stu-id="3546a-141">Example 6: Copy a block blob to destination container with a new blob name, and set destination blob StandardBlobTier as Hot, RehydratePriority as High</span></span>
```
C:\PS>Start-AzStorageBlobCopy -SrcContainer "ContosoUploads" -SrcBlob "BlockBlobName" -DestContainer "ContosoArchives" -DestBlob "NewBlockBlobName" -StandardBlobTier Hot -RehydratePriority High
```

<span data-ttu-id="3546a-142">이 명령은 새 Blob 이름으로 대상 컨테이너에 대한 블록 Blob의 복사 작업을 시작하고 대상 Blob StandardBlobTier를 Hot, RehydratePriority로 높음으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-142">This command starts the copy operation of a block blob to destination container with a new blob name, and set destination blob StandardBlobTier as Hot, RehydratePriority as High</span></span>

## <span data-ttu-id="3546a-143">매개 변수</span><span class="sxs-lookup"><span data-stu-id="3546a-143">PARAMETERS</span></span>

### <span data-ttu-id="3546a-144">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="3546a-144">-AbsoluteUri</span></span>
<span data-ttu-id="3546a-145">Azure Storage Blob에 복사할 파일의 절대 URI를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-145">Specifies the absolute URI of a file to copy to an Azure Storage blob.</span></span>

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

### <span data-ttu-id="3546a-146">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="3546a-146">-BlobBaseClient</span></span>
<span data-ttu-id="3546a-147">BlobBaseClient 개체</span><span class="sxs-lookup"><span data-stu-id="3546a-147">BlobBaseClient Object</span></span>

```yaml
Type: Azure.Storage.Blobs.Specialized.BlobBaseClient
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3546a-148">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3546a-148">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="3546a-149">하나의 서비스 요청에 대해 클라이언트 쪽 시간 간격(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-149">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="3546a-150">지정된 간격에서 이전 호출이 실패하면 이 cmdlet에서 요청을 다시 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-150">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="3546a-151">간격이 경과하기 전에 이 cmdlet에서 성공적인 응답을 받지 못하면 이 cmdlet은 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-151">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="3546a-152">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="3546a-152">-CloudBlob</span></span>
<span data-ttu-id="3546a-153">Azure Storage 클라이언트 라이브러리에서 **CloudBlob** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-153">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="3546a-154">**CloudBlob** 개체를 얻으면 Get-AzStorageBlob cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-154">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="3546a-155">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="3546a-155">-CloudBlobContainer</span></span>
<span data-ttu-id="3546a-156">Azure Storage 클라이언트 라이브러리에서 **CloudBlobContainer** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-156">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="3546a-157">이 cmdlet은 이 매개 변수가 지정하는 컨테이너에서 Blob을 복사합니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-157">This cmdlet copies a blob from the container that this parameter specifies.</span></span>
<span data-ttu-id="3546a-158">**CloudBlobContainer** 개체를 얻은 경우 Get-AzStorageContainer cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-158">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="3546a-159">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="3546a-159">-ConcurrentTaskCount</span></span>
<span data-ttu-id="3546a-160">최대 동시 네트워크 호출을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-160">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="3546a-161">이 매개 변수를 사용하여 최대 동시 네트워크 호출 수를 지정하여 로컬 CPU 및 대역폭 사용량을 제한하는 동시성 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-161">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="3546a-162">지정된 값은 절대 개수로 코어 수에 곱하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-162">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="3546a-163">이 매개 변수는 초당 100킬로비트와 같은 대역폭이 낮은 환경에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-163">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="3546a-164">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-164">The default value is 10.</span></span>

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

### <span data-ttu-id="3546a-165">-Context</span><span class="sxs-lookup"><span data-stu-id="3546a-165">-Context</span></span>
<span data-ttu-id="3546a-166">Azure Storage 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-166">Specifies an Azure storage context.</span></span>
<span data-ttu-id="3546a-167">저장소 컨텍스트를 구하기 위해 New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-167">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="3546a-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3546a-168">-DefaultProfile</span></span>
<span data-ttu-id="3546a-169">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-169">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3546a-170">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="3546a-170">-DestBlob</span></span>
<span data-ttu-id="3546a-171">대상 Blob의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-171">Specifies the name of the destination blob.</span></span>

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

### <span data-ttu-id="3546a-172">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="3546a-172">-DestCloudBlob</span></span>
<span data-ttu-id="3546a-173">대상 **CloudBlob 개체를 지정합니다.**</span><span class="sxs-lookup"><span data-stu-id="3546a-173">Specifies a destination **CloudBlob** object</span></span>

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

### <span data-ttu-id="3546a-174">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="3546a-174">-DestContainer</span></span>
<span data-ttu-id="3546a-175">대상 컨테이너의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-175">Specifies the name of the destination container.</span></span>

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

### <span data-ttu-id="3546a-176">-DestContext</span><span class="sxs-lookup"><span data-stu-id="3546a-176">-DestContext</span></span>
<span data-ttu-id="3546a-177">Azure Storage 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-177">Specifies an Azure storage context.</span></span>
<span data-ttu-id="3546a-178">저장소 컨텍스트를 구하기 위해 New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-178">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="3546a-179">-Force</span><span class="sxs-lookup"><span data-stu-id="3546a-179">-Force</span></span>
<span data-ttu-id="3546a-180">이 cmdlet이 확인을 요청하지 않고 대상 Blob을 덮어 묻는 메시지를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-180">Indicates that this cmdlet overwrites the destination blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="3546a-181">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="3546a-181">-PremiumPageBlobTier</span></span>
<span data-ttu-id="3546a-182">프리미엄 페이지 Blob 계층</span><span class="sxs-lookup"><span data-stu-id="3546a-182">Premium Page Blob Tier</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.PremiumPageBlobTier
Parameter Sets: ContainerName, BlobInstance, BlobInstanceToBlobInstance, ContainerInstance
Aliases:
Accepted values: Unknown, P4, P6, P10, P20, P30, P40, P50, P60, P70, P80

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3546a-183">-RehydratePriority</span><span class="sxs-lookup"><span data-stu-id="3546a-183">-RehydratePriority</span></span>
<span data-ttu-id="3546a-184">Blob RehydratePriority를 차단합니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-184">Block Blob RehydratePriority.</span></span> <span data-ttu-id="3546a-185">보관된 Blob을 다시하이드레이션할 우선 순위를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-185">Indicates the priority with which to rehydrate an archived blob.</span></span> <span data-ttu-id="3546a-186">유효한 값은 높음/표준입니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-186">Valid values are High/Standard.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.RehydratePriority
Parameter Sets: (All)
Aliases:
Accepted values: Standard, High

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3546a-187">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3546a-187">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="3546a-188">요청에 대해 서비스 쪽 시간 시간 간격(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-188">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="3546a-189">서비스가 요청을 처리하기 전에 지정된 간격이 경과하면 저장소 서비스가 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-189">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="3546a-190">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="3546a-190">-SrcBlob</span></span>
<span data-ttu-id="3546a-191">원본 Blob의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-191">Specifies the name of the source blob.</span></span>

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

### <span data-ttu-id="3546a-192">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="3546a-192">-SrcContainer</span></span>
<span data-ttu-id="3546a-193">원본 컨테이너의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-193">Specifies the name of the source container.</span></span>

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

### <span data-ttu-id="3546a-194">-SrcDir</span><span class="sxs-lookup"><span data-stu-id="3546a-194">-SrcDir</span></span>
<span data-ttu-id="3546a-195">Azure Storage 클라이언트 라이브러리에서 **CloudFileDirectory** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-195">Specifies a **CloudFileDirectory** object from Azure Storage Client library.</span></span>

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

### <span data-ttu-id="3546a-196">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="3546a-196">-SrcFile</span></span>
<span data-ttu-id="3546a-197">Azure Storage 클라이언트 라이브러리에서 **CloudFile** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-197">Specifies a **CloudFile** object from Azure Storage Client library.</span></span>
<span data-ttu-id="3546a-198">cmdlet을 만들거나 Get-AzStorageFile 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-198">You can create it or use Get-AzStorageFile cmdlet.</span></span>

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

### <span data-ttu-id="3546a-199">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="3546a-199">-SrcFilePath</span></span>
<span data-ttu-id="3546a-200">원본 디렉터리 또는 원본 공유의 원본 파일 상대 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-200">Specifies the source file relative path of source directory or source share.</span></span>

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

### <span data-ttu-id="3546a-201">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="3546a-201">-SrcShare</span></span>
<span data-ttu-id="3546a-202">Azure Storage 클라이언트 라이브러리에서 **CloudFileShare** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-202">Specifies a **CloudFileShare** object from Azure Storage Client library.</span></span>
<span data-ttu-id="3546a-203">cmdlet을 만들거나 Get-AzStorageShare 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-203">You can create it or use Get-AzStorageShare cmdlet.</span></span>

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

### <span data-ttu-id="3546a-204">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="3546a-204">-SrcShareName</span></span>
<span data-ttu-id="3546a-205">원본 공유 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-205">Specifies the source share name.</span></span>

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

### <span data-ttu-id="3546a-206">-StandardBlobTier</span><span class="sxs-lookup"><span data-stu-id="3546a-206">-StandardBlobTier</span></span>
<span data-ttu-id="3546a-207">블록 Blob 계층, 유효한 값은 Hot/Cool/Archive입니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-207">Block Blob Tier, valid values are Hot/Cool/Archive.</span></span>
<span data-ttu-id="3546a-208">자세한 정보 보기 https://docs.microsoft.com/azure/storage/blobs/storage-blob-storage-tiers</span><span class="sxs-lookup"><span data-stu-id="3546a-208">See detail in https://docs.microsoft.com/azure/storage/blobs/storage-blob-storage-tiers</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hot, Cool, Archive

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3546a-209">-확인</span><span class="sxs-lookup"><span data-stu-id="3546a-209">-Confirm</span></span>
<span data-ttu-id="3546a-210">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-210">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3546a-211">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3546a-211">-WhatIf</span></span>
<span data-ttu-id="3546a-212">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-212">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3546a-213">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-213">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3546a-214">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3546a-214">CommonParameters</span></span>
<span data-ttu-id="3546a-215">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3546a-215">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3546a-216">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="3546a-216">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3546a-217">입력</span><span class="sxs-lookup"><span data-stu-id="3546a-217">INPUTS</span></span>

### <span data-ttu-id="3546a-218">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="3546a-218">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="3546a-219">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="3546a-219">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="3546a-220">Microsoft.Azure.Storage.File.CloudFile</span><span class="sxs-lookup"><span data-stu-id="3546a-220">Microsoft.Azure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="3546a-221">System.String</span><span class="sxs-lookup"><span data-stu-id="3546a-221">System.String</span></span>

### <span data-ttu-id="3546a-222">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3546a-222">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3546a-223">출력</span><span class="sxs-lookup"><span data-stu-id="3546a-223">OUTPUTS</span></span>

### <span data-ttu-id="3546a-224">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="3546a-224">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="3546a-225">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3546a-225">NOTES</span></span>

## <span data-ttu-id="3546a-226">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3546a-226">RELATED LINKS</span></span>

[<span data-ttu-id="3546a-227">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="3546a-227">Get-AzStorageBlobCopyState</span></span>](./Get-AzStorageBlobCopyState.md)

[<span data-ttu-id="3546a-228">Stop-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="3546a-228">Stop-AzStorageBlobCopy</span></span>](./Stop-AzStorageBlobCopy.md)
