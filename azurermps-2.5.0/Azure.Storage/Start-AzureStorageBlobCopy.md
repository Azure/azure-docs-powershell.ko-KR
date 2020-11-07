---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 54585346-04E2-4FB4-B5FD-833A85C46ACB
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/start-azurestorageblobcopy
schema: 2.0.0
ms.openlocfilehash: 379e86e6f6e97e1e8d70b55d972076d540654cb8
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882714"
---
# <span data-ttu-id="37cfa-101">Start-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="37cfa-101">Start-AzureStorageBlobCopy</span></span>

## <span data-ttu-id="37cfa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37cfa-102">SYNOPSIS</span></span>
<span data-ttu-id="37cfa-103">Blob 복사를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-103">Starts to copy a blob.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37cfa-104">구문과</span><span class="sxs-lookup"><span data-stu-id="37cfa-104">SYNTAX</span></span>

### <span data-ttu-id="37cfa-105">ContainerName (기본값)</span><span class="sxs-lookup"><span data-stu-id="37cfa-105">ContainerName (Default)</span></span>
```
Start-AzureStorageBlobCopy [-SrcBlob] <String> -SrcContainer <String> -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37cfa-106">BlobInstance</span><span class="sxs-lookup"><span data-stu-id="37cfa-106">BlobInstance</span></span>
```
Start-AzureStorageBlobCopy -CloudBlob <CloudBlob> -DestContainer <String> [-DestBlob <String>]
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="37cfa-107">Blobinstanceetobinstance</span><span class="sxs-lookup"><span data-stu-id="37cfa-107">BlobInstanceToBlobInstance</span></span>
```
Start-AzureStorageBlobCopy -CloudBlob <CloudBlob> -DestCloudBlob <CloudBlob>
 [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Context <IStorageContext>] [-DestContext <IStorageContext>]
 [-Force] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="37cfa-108">ContainerInstance</span><span class="sxs-lookup"><span data-stu-id="37cfa-108">ContainerInstance</span></span>
```
Start-AzureStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-SrcBlob] <String> -DestContainer <String>
 [-DestBlob <String>] [-PremiumPageBlobTier <PremiumPageBlobTier>] [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37cfa-109">ShareName</span><span class="sxs-lookup"><span data-stu-id="37cfa-109">ShareName</span></span>
```
Start-AzureStorageBlobCopy -SrcShareName <String> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="37cfa-110">ShareInstance</span><span class="sxs-lookup"><span data-stu-id="37cfa-110">ShareInstance</span></span>
```
Start-AzureStorageBlobCopy -SrcShare <CloudFileShare> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="37cfa-111">해당 인스턴스</span><span class="sxs-lookup"><span data-stu-id="37cfa-111">DirInstance</span></span>
```
Start-AzureStorageBlobCopy -SrcDir <CloudFileDirectory> -SrcFilePath <String> -DestContainer <String>
 [-DestBlob <String>] [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="37cfa-112">FileInstance</span><span class="sxs-lookup"><span data-stu-id="37cfa-112">FileInstance</span></span>
```
Start-AzureStorageBlobCopy -SrcFile <CloudFile> -DestContainer <String> [-DestBlob <String>]
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37cfa-113">Fileinstanceetobinstance</span><span class="sxs-lookup"><span data-stu-id="37cfa-113">FileInstanceToBlobInstance</span></span>
```
Start-AzureStorageBlobCopy -SrcFile <CloudFile> -DestCloudBlob <CloudBlob> [-Context <IStorageContext>]
 [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37cfa-114">UriPipeline</span><span class="sxs-lookup"><span data-stu-id="37cfa-114">UriPipeline</span></span>
```
Start-AzureStorageBlobCopy -AbsoluteUri <String> -DestContainer <String> -DestBlob <String>
 [-Context <IStorageContext>] [-DestContext <IStorageContext>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37cfa-115">설명은</span><span class="sxs-lookup"><span data-stu-id="37cfa-115">DESCRIPTION</span></span>
<span data-ttu-id="37cfa-116">**시작-AzureStorageBlobCopy** cmdlet이 시작 되어 blob을 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-116">The **Start-AzureStorageBlobCopy** cmdlet starts to copy a blob.</span></span>

## <span data-ttu-id="37cfa-117">예제의</span><span class="sxs-lookup"><span data-stu-id="37cfa-117">EXAMPLES</span></span>

### <span data-ttu-id="37cfa-118">예제 1: 명명 된 blob 복사</span><span class="sxs-lookup"><span data-stu-id="37cfa-118">Example 1: Copy a named blob</span></span>
```
C:\PS>Start-AzureStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives" -SrcContainer "ContosoUploads"
```

<span data-ttu-id="37cfa-119">이 명령은 ContosoUploads 이라는 컨테이너에서 ContosoPlanning2015 라는 blob의 복사 작업을 ContosoArchives 이라는 컨테이너에 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-119">This command starts the copy operation of the blob named ContosoPlanning2015 from the container named ContosoUploads to the container named ContosoArchives.</span></span>

### <span data-ttu-id="37cfa-120">예제 2: 복사할 blob을 지정 하는 컨테이너 가져오기</span><span class="sxs-lookup"><span data-stu-id="37cfa-120">Example 2: Get a container to specify blobs to copy</span></span>
```
C:\PS>Get-AzureStorageContainer -Name "ContosoUploads" | Start-AzureStorageBlobCopy -SrcBlob "ContosoPlanning2015" -DestContainer "ContosoArchives"
```

<span data-ttu-id="37cfa-121">이 명령은 **AzureStorageContainer** cmdlet을 사용 하 여 ContosoUploads 이라는 컨테이너를 가져온 다음 파이프라인 연산자를 사용 하 여 현재 cmdlet에 컨테이너를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-121">This command gets the container named ContosoUploads, by using the **Get-AzureStorageContainer** cmdlet, and then passes the container to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="37cfa-122">해당 cmdlet은 ContosoPlanning2015 이라는 blob의 복사 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-122">That cmdlet starts the copy operation of the blob named ContosoPlanning2015.</span></span>
<span data-ttu-id="37cfa-123">이전 cmdlet은 원본 컨테이너를 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-123">The previous cmdlet provides the source container.</span></span>
<span data-ttu-id="37cfa-124">*Destcontainer* 매개 변수는 ContosoArchives를 대상 컨테이너로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-124">The *DestContainer* parameter specifies ContosoArchives as the destination container.</span></span>

### <span data-ttu-id="37cfa-125">예제 3: 컨테이너의 모든 blob 가져오기 및 복사</span><span class="sxs-lookup"><span data-stu-id="37cfa-125">Example 3: Get all blobs in a container and copy them</span></span>
```
C:\PS>Get-AzureStorageBlob -Container "ContosoUploads" | Start-AzureStorageBlobCopy -DestContainer "ContosoArchives"
```

<span data-ttu-id="37cfa-126">이 명령은 **Get-AzureStorageBlob** cmdlet을 사용 하 여 ContosoUploads 이라는 컨테이너의 blob을 가져온 다음 파이프라인 연산자를 사용 하 여 현재 cmdlet에 결과를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-126">This command gets the blobs in the container named ContosoUploads, by using the **Get-AzureStorageBlob** cmdlet, and then passes the results to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="37cfa-127">해당 cmdlet은 ContosoArchives 이라는 컨테이너에 대 한 blob의 복사 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-127">That cmdlet starts the copy operation of the blobs to the container named ContosoArchives.</span></span>

### <span data-ttu-id="37cfa-128">예제 4: 개체로 지정 된 blob 복사</span><span class="sxs-lookup"><span data-stu-id="37cfa-128">Example 4: Copy a blob specified as an object</span></span>
```
C:\PS>$SrcBlob = Get-AzureStorageBlob -Container "ContosoUploads" -Blob "ContosoPlanning2015"
C:\PS> $DestBlob = Get-AzureStorageBlob -Container "ContosoArchives" -Blob "ContosoPlanning2015Archived"
C:\PS> Start-AzureStorageBlobCopy -ICloudBlob $SrcBlob.ICloudBlob -DestICloudBlob $DestBlob.ICloudBlob
```

<span data-ttu-id="37cfa-129">첫 번째 명령은 ContosoUploads 이라는 컨테이너에서 ContosoPlanning2015 라는 blob를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-129">The first command gets the blob named ContosoPlanning2015 in the container named ContosoUploads.</span></span>
<span data-ttu-id="37cfa-130">명령이 $SrcBlob 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-130">The command stores that object in the $SrcBlob variable.</span></span>
<span data-ttu-id="37cfa-131">두 번째 명령은 ContosoArchives 이라는 컨테이너에서 ContosoPlanning2015Archived 라는 blob를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-131">The second command gets the blob named ContosoPlanning2015Archived in the container named ContosoArchives.</span></span>
<span data-ttu-id="37cfa-132">명령이 $DestBlob 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-132">The command stores that object in the $DestBlob variable.</span></span>
<span data-ttu-id="37cfa-133">마지막 명령은 원본 컨테이너에서 대상 컨테이너로 복사 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-133">The last command starts the copy operation from the source container to the destination container.</span></span>
<span data-ttu-id="37cfa-134">명령에서는 표준 점 표기법을 사용 하 여 $SrcBlob 및 $DestBlob blob에 대 한 **ICloudBlob** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-134">The command uses standard dot notation to specify the **ICloudBlob** objects for the $SrcBlob and $DestBlob blobs.</span></span>

### <span data-ttu-id="37cfa-135">예제 5: URI에서 blob 복사</span><span class="sxs-lookup"><span data-stu-id="37cfa-135">Example 5: Copy a blob from a URI</span></span>
```
C:\PS>$Context = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
C:\PS> Start-AzureStorageBlobCopy -AbsoluteUri "http://www.contosointernal.com/planning" -DestContainer "ContosoArchive" -DestBlob "ContosoPlanning2015" -DestContext $Context
```

<span data-ttu-id="37cfa-136">이 명령은 지정 된 키를 사용 하는 ContosoGeneral 이라는 계정에 대 한 컨텍스트를 만든 다음 해당 키를 $Context 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-136">This command creates a context for the account named ContosoGeneral that uses the specified key, and then stores that key in the $Context variable.</span></span>
<span data-ttu-id="37cfa-137">두 번째 명령은 지정 된 URI의 파일을 ContosoArchive 이라는 컨테이너에 있는 ContosoPlanning 이라는 blob에 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-137">The second command copies the file from the specified URI to the blob named ContosoPlanning in the container named ContosoArchive.</span></span>
<span data-ttu-id="37cfa-138">이 명령은 $Context에 저장 된 컨텍스트에서 복사 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-138">The command starts the copy operation in the context stored in $Context.</span></span>

## <span data-ttu-id="37cfa-139">변수</span><span class="sxs-lookup"><span data-stu-id="37cfa-139">PARAMETERS</span></span>

### <span data-ttu-id="37cfa-140">-AbsoluteUri</span><span class="sxs-lookup"><span data-stu-id="37cfa-140">-AbsoluteUri</span></span>
<span data-ttu-id="37cfa-141">Azure Storage blob에 복사할 파일의 절대 URI를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-141">Specifies the absolute URI of a file to copy to an Azure Storage blob.</span></span>

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

### <span data-ttu-id="37cfa-142">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="37cfa-142">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="37cfa-143">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-143">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="37cfa-144">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-144">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="37cfa-145">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-145">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="37cfa-146">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="37cfa-146">-CloudBlob</span></span>
<span data-ttu-id="37cfa-147">Azure Storage 클라이언트 라이브러리에서 **CloudBlob** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-147">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="37cfa-148">**CloudBlob** 개체를 가져오려면 Get-AzureStorageBlob cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-148">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlob
Parameter Sets: BlobInstance, BlobInstanceToBlobInstance
Aliases: SrcICloudBlob, SrcCloudBlob, ICloudBlob, SourceICloudBlob, SourceCloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37cfa-149">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="37cfa-149">-CloudBlobContainer</span></span>
<span data-ttu-id="37cfa-150">Azure Storage 클라이언트 라이브러리에서 **CloudBlobContainer** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-150">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="37cfa-151">이 cmdlet은이 매개 변수에서 지정 하는 컨테이너에서 blob을 복사 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-151">This cmdlet copies a blob from the container that this parameter specifies.</span></span>
<span data-ttu-id="37cfa-152">**CloudBlobContainer** 개체를 가져오려면 Get-AzureStorageContainer cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-152">To obtain a **CloudBlobContainer** object, use the Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerInstance
Aliases: SourceCloudBlobContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37cfa-153">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="37cfa-153">-ConcurrentTaskCount</span></span>
<span data-ttu-id="37cfa-154">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-154">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="37cfa-155">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-155">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="37cfa-156">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-156">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="37cfa-157">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-157">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="37cfa-158">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-158">The default value is 10.</span></span>

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

### <span data-ttu-id="37cfa-159">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="37cfa-159">-Context</span></span>
<span data-ttu-id="37cfa-160">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-160">Specifies an Azure storage context.</span></span>
<span data-ttu-id="37cfa-161">저장소 컨텍스트를 얻으려면 New-AzureStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-161">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="37cfa-162">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37cfa-162">-DefaultProfile</span></span>
<span data-ttu-id="37cfa-163">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-163">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37cfa-164">-DestBlob</span><span class="sxs-lookup"><span data-stu-id="37cfa-164">-DestBlob</span></span>
<span data-ttu-id="37cfa-165">대상 blob의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-165">Specifies the name of the destination blob.</span></span>

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

### <span data-ttu-id="37cfa-166">-DestCloudBlob</span><span class="sxs-lookup"><span data-stu-id="37cfa-166">-DestCloudBlob</span></span>
<span data-ttu-id="37cfa-167">대상 **CloudBlob** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-167">Specifies a destination **CloudBlob** object</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlob
Parameter Sets: BlobInstanceToBlobInstance, FileInstanceToBlobInstance
Aliases: DestICloudBlob, DestinationCloudBlob, DestinationICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37cfa-168">-DestContainer</span><span class="sxs-lookup"><span data-stu-id="37cfa-168">-DestContainer</span></span>
<span data-ttu-id="37cfa-169">대상 컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-169">Specifies the name of the destination container.</span></span>

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

### <span data-ttu-id="37cfa-170">DestContext</span><span class="sxs-lookup"><span data-stu-id="37cfa-170">-DestContext</span></span>
<span data-ttu-id="37cfa-171">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-171">Specifies an Azure storage context.</span></span>
<span data-ttu-id="37cfa-172">저장소 컨텍스트를 얻으려면 New-AzureStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-172">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="37cfa-173">-Force</span><span class="sxs-lookup"><span data-stu-id="37cfa-173">-Force</span></span>
<span data-ttu-id="37cfa-174">이 cmdlet이 확인 메시지를 표시 하지 않고 대상 blob을 덮어씁니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-174">Indicates that this cmdlet overwrites the destination blob without prompting you for confirmation.</span></span>

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

### <span data-ttu-id="37cfa-175">-PremiumPageBlobTier</span><span class="sxs-lookup"><span data-stu-id="37cfa-175">-PremiumPageBlobTier</span></span>
<span data-ttu-id="37cfa-176">프리미엄 페이지 Blob 계층</span><span class="sxs-lookup"><span data-stu-id="37cfa-176">Premium Page Blob Tier</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.PremiumPageBlobTier
Parameter Sets: ContainerName, BlobInstance, BlobInstanceToBlobInstance, ContainerInstance
Aliases:
Accepted values: Unknown, P4, P6, P10, P20, P30, P40, P50, P60

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37cfa-177">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="37cfa-177">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="37cfa-178">요청에 대 한 서비스 측 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-178">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="37cfa-179">서비스가 요청을 처리 하기 전에 지정 된 간격이 경과 하면 저장소 서비스에서 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-179">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="37cfa-180">-SrcBlob</span><span class="sxs-lookup"><span data-stu-id="37cfa-180">-SrcBlob</span></span>
<span data-ttu-id="37cfa-181">원본 blob의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-181">Specifies the name of the source blob.</span></span>

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

### <span data-ttu-id="37cfa-182">-SrcContainer</span><span class="sxs-lookup"><span data-stu-id="37cfa-182">-SrcContainer</span></span>
<span data-ttu-id="37cfa-183">원본 컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-183">Specifies the name of the source container.</span></span>

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

### <span data-ttu-id="37cfa-184">-SrcDir</span><span class="sxs-lookup"><span data-stu-id="37cfa-184">-SrcDir</span></span>
<span data-ttu-id="37cfa-185">Azure Storage 클라이언트 라이브러리에서 **Cloudfiledirectory** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-185">Specifies a **CloudFileDirectory** object from Azure Storage Client library.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileDirectory
Parameter Sets: DirInstance
Aliases: SourceDir

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37cfa-186">-SrcFile</span><span class="sxs-lookup"><span data-stu-id="37cfa-186">-SrcFile</span></span>
<span data-ttu-id="37cfa-187">Azure Storage 클라이언트 라이브러리에서 **Cloudfile** 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-187">Specifes a **CloudFile** object from Azure Storage Client library.</span></span>
<span data-ttu-id="37cfa-188">이를 만들거나 Get-AzureStorageFile cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-188">You can create it or use Get-AzureStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
Parameter Sets: FileInstance, FileInstanceToBlobInstance
Aliases: SourceFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37cfa-189">-SrcFilePath</span><span class="sxs-lookup"><span data-stu-id="37cfa-189">-SrcFilePath</span></span>
<span data-ttu-id="37cfa-190">원본 디렉터리 또는 원본 공유의 원본 파일 상대 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-190">Specifies the source file relative path of source directory or source share.</span></span>

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

### <span data-ttu-id="37cfa-191">-SrcShare</span><span class="sxs-lookup"><span data-stu-id="37cfa-191">-SrcShare</span></span>
<span data-ttu-id="37cfa-192">Azure Storage 클라이언트 라이브러리에서 **Cloudfileshare** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-192">Specifies a **CloudFileShare** object from Azure Storage Client library.</span></span>
<span data-ttu-id="37cfa-193">이를 만들거나 Get-AzureStorageShare cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-193">You can create it or use Get-AzureStorageShare cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFileShare
Parameter Sets: ShareInstance
Aliases: SourceShare

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37cfa-194">-SrcShareName</span><span class="sxs-lookup"><span data-stu-id="37cfa-194">-SrcShareName</span></span>
<span data-ttu-id="37cfa-195">원본 공유 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-195">Specifies the source share name.</span></span>

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

### <span data-ttu-id="37cfa-196">-확인</span><span class="sxs-lookup"><span data-stu-id="37cfa-196">-Confirm</span></span>
<span data-ttu-id="37cfa-197">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-197">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37cfa-198">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37cfa-198">-WhatIf</span></span>
<span data-ttu-id="37cfa-199">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-199">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37cfa-200">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-200">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37cfa-201">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37cfa-201">CommonParameters</span></span>
<span data-ttu-id="37cfa-202">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-202">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37cfa-203">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37cfa-203">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37cfa-204">입력</span><span class="sxs-lookup"><span data-stu-id="37cfa-204">INPUTS</span></span>

### <span data-ttu-id="37cfa-205">WindowsAzure. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="37cfa-205">Microsoft.WindowsAzure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="37cfa-206">WindowsAzure. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="37cfa-206">Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="37cfa-207">WindowsAzure 파일을 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="37cfa-207">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>
<span data-ttu-id="37cfa-208">매개 변수: SrcFile (ByValue)</span><span class="sxs-lookup"><span data-stu-id="37cfa-208">Parameters: SrcFile (ByValue)</span></span>

### <span data-ttu-id="37cfa-209">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="37cfa-209">System.String</span></span>

### <span data-ttu-id="37cfa-210">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="37cfa-210">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="37cfa-211">출력</span><span class="sxs-lookup"><span data-stu-id="37cfa-211">OUTPUTS</span></span>

### <span data-ttu-id="37cfa-212">WindowsAzure. ResourceModel. m b m.</span><span class="sxs-lookup"><span data-stu-id="37cfa-212">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="37cfa-213">상속자</span><span class="sxs-lookup"><span data-stu-id="37cfa-213">NOTES</span></span>

## <span data-ttu-id="37cfa-214">관련 링크</span><span class="sxs-lookup"><span data-stu-id="37cfa-214">RELATED LINKS</span></span>

[<span data-ttu-id="37cfa-215">Get-AzureStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="37cfa-215">Get-AzureStorageBlobCopyState</span></span>](./Get-AzureStorageBlobCopyState.md)

[<span data-ttu-id="37cfa-216">중지-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="37cfa-216">Stop-AzureStorageBlobCopy</span></span>](./Stop-AzureStorageBlobCopy.md)
