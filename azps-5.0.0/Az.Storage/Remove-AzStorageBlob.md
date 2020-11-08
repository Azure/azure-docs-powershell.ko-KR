---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 03EC0D20-C737-4B2B-B8D9-71D06A938FAD
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageBlob.md
ms.openlocfilehash: 37ae4192e973d218bd0cb23f9ccba16367098d30
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226040"
---
# <span data-ttu-id="6d6b9-101">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="6d6b9-101">Remove-AzStorageBlob</span></span>

## <span data-ttu-id="6d6b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d6b9-102">SYNOPSIS</span></span>
<span data-ttu-id="6d6b9-103">지정 된 저장소 blob을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d6b9-103">Removes the specified storage blob.</span></span>

## <span data-ttu-id="6d6b9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6d6b9-104">SYNTAX</span></span>

### <span data-ttu-id="6d6b9-105">NamePipeline (기본값)</span><span class="sxs-lookup"><span data-stu-id="6d6b9-105">NamePipeline (Default)</span></span>
```
Remove-AzStorageBlob [-Blob] <String> [-Container] <String> [-DeleteSnapshot] [-SnapshotTime <DateTimeOffset>]
 [-VersionId <String>] [-Force] [-PassThru] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d6b9-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="6d6b9-106">BlobPipeline</span></span>
```
Remove-AzStorageBlob -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] [-DeleteSnapshot] [-Force]
 [-PassThru] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6d6b9-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="6d6b9-107">ContainerPipeline</span></span>
```
Remove-AzStorageBlob -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-DeleteSnapshot]
 [-SnapshotTime <DateTimeOffset>] [-VersionId <String>] [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6d6b9-108">설명은</span><span class="sxs-lookup"><span data-stu-id="6d6b9-108">DESCRIPTION</span></span>
<span data-ttu-id="6d6b9-109">**AzStorageBlob** Cmdlet은 Azure의 저장소 계정에서 지정 된 blob을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d6b9-109">The **Remove-AzStorageBlob** cmdlet removes the specified blob from a storage account in Azure.</span></span>

## <span data-ttu-id="6d6b9-110">예제의</span><span class="sxs-lookup"><span data-stu-id="6d6b9-110">EXAMPLES</span></span>

### <span data-ttu-id="6d6b9-111">예제 1: 이름으로 저장소 blob 제거</span><span class="sxs-lookup"><span data-stu-id="6d6b9-111">Example 1: Remove a storage blob by name</span></span>
```
PS C:\>Remove-AzStorageBlob -Container "ContainerName" -Blob "BlobName"
```

<span data-ttu-id="6d6b9-112">이 명령은 이름으로 식별 되는 blob을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d6b9-112">This command removes a blob identified by its name.</span></span>

### <span data-ttu-id="6d6b9-113">예제 2: 파이프라인을 사용 하 여 저장소 blob 제거</span><span class="sxs-lookup"><span data-stu-id="6d6b9-113">Example 2: Remove a storage blob using the pipeline</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Blob "BlobName" | Remove-AzStorageBlob
```

<span data-ttu-id="6d6b9-114">이 명령은 파이프라인을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d6b9-114">This command uses the pipeline.</span></span>

### <span data-ttu-id="6d6b9-115">예제 3: 파이프라인을 사용 하 여 저장소 blob 제거</span><span class="sxs-lookup"><span data-stu-id="6d6b9-115">Example 3: Remove storage blobs using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container container* | Remove-AzStorageBlob -Blob "BlobName"
```

<span data-ttu-id="6d6b9-116">이 명령은 별표 (\*) 와일드 카드 문자 및 파이프라인을 사용 하 여 blob 또는 blob을 검색 한 다음 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d6b9-116">This command uses the asterisk (\*) wildcard character and the pipeline to retrieve the blob or blobs and then removes them.</span></span>

### <span data-ttu-id="6d6b9-117">예제 4: 단일 blob 버전 제거</span><span class="sxs-lookup"><span data-stu-id="6d6b9-117">Example 4: Remove a single blob version</span></span>
```
PS C:\> Remove-AzStorageBlob -Container "containername" -Blob blob2 -VersionId "2020-07-03T16:19:16.2883167Z"
```

<span data-ttu-id="6d6b9-118">이 명령은 verion를 사용 하 여 단일 blob을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d6b9-118">This command removes a single blobs verion with VersionId.</span></span>

### <span data-ttu-id="6d6b9-119">예제 5: 단일 blob 스냅숏 제거</span><span class="sxs-lookup"><span data-stu-id="6d6b9-119">Example 5: Remove a single blob snapshot</span></span>
```
PS C:\> Remove-AzStorageBlob -Container "containername" -Blob blob1 -SnapshotTime "2020-07-06T06:56:06.8588431Z"
```

<span data-ttu-id="6d6b9-120">이 명령은 SnapshotTime를 사용 하 여 단일 blob 스냅숏을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d6b9-120">This command removes a single blobs snapshot with SnapshotTime.</span></span>

## <span data-ttu-id="6d6b9-121">변수</span><span class="sxs-lookup"><span data-stu-id="6d6b9-121">PARAMETERS</span></span>

### <span data-ttu-id="6d6b9-122">-Blob</span><span class="sxs-lookup"><span data-stu-id="6d6b9-122">-Blob</span></span>
<span data-ttu-id="6d6b9-123">제거 하려는 blob의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d6b9-123">Specifies the name of the blob you want to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d6b9-124">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="6d6b9-124">-BlobBaseClient</span></span>
<span data-ttu-id="6d6b9-125">BlobBaseClient 개체</span><span class="sxs-lookup"><span data-stu-id="6d6b9-125">BlobBaseClient Object</span></span>

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

### <span data-ttu-id="6d6b9-126">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6d6b9-126">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="6d6b9-127">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d6b9-127">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="6d6b9-128">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d6b9-128">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="6d6b9-129">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d6b9-129">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="6d6b9-130">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="6d6b9-130">-CloudBlob</span></span>
<span data-ttu-id="6d6b9-131">클라우드 blob을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d6b9-131">Specifies a cloud blob.</span></span>
<span data-ttu-id="6d6b9-132">**CloudBlob** 개체를 가져오려면 Get-AzStorageBlob cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d6b9-132">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="6d6b9-133">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="6d6b9-133">-CloudBlobContainer</span></span>
<span data-ttu-id="6d6b9-134">Azure Storage 클라이언트 라이브러리에서 **CloudBlobContainer** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d6b9-134">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="6d6b9-135">Get-AzStorageContainer cmdlet을 사용 하 여 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6d6b9-135">You can use the Get-AzStorageContainer cmdlet to get it.</span></span>

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

### <span data-ttu-id="6d6b9-136">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="6d6b9-136">-ConcurrentTaskCount</span></span>
<span data-ttu-id="6d6b9-137">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d6b9-137">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="6d6b9-138">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6d6b9-138">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="6d6b9-139">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="6d6b9-139">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="6d6b9-140">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6d6b9-140">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="6d6b9-141">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="6d6b9-141">The default value is 10.</span></span>

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

### <span data-ttu-id="6d6b9-142">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="6d6b9-142">-Container</span></span>
<span data-ttu-id="6d6b9-143">컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d6b9-143">Specifies the name of the container.</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d6b9-144">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="6d6b9-144">-Context</span></span>
<span data-ttu-id="6d6b9-145">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d6b9-145">Specifies the Azure storage context.</span></span>
<span data-ttu-id="6d6b9-146">New-AzStorageContext cmdlet을 사용 하 여 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6d6b9-146">You can use the New-AzStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="6d6b9-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d6b9-147">-DefaultProfile</span></span>
<span data-ttu-id="6d6b9-148">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6d6b9-148">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d6b9-149">-DeleteSnapshot</span><span class="sxs-lookup"><span data-stu-id="6d6b9-149">-DeleteSnapshot</span></span>
<span data-ttu-id="6d6b9-150">기본 blob이 아닌 모든 스냅숏을 삭제 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d6b9-150">Specifies that all snapshots be deleted, but not the base blob.</span></span>
<span data-ttu-id="6d6b9-151">이 매개 변수를 지정 하지 않으면 기본 blob 및 해당 스냅샷이 함께 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6d6b9-151">If this parameter is not specified, the base blob and its snapshots are deleted together.</span></span>
<span data-ttu-id="6d6b9-152">사용자에 게 삭제 작업을 확인 하는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6d6b9-152">The user is prompted to confirm the delete operation.</span></span>

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

### <span data-ttu-id="6d6b9-153">-Force</span><span class="sxs-lookup"><span data-stu-id="6d6b9-153">-Force</span></span>
<span data-ttu-id="6d6b9-154">이 cmdlet이 확인 없이 blob 및 해당 스냅샷을 제거 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6d6b9-154">Indicates that this cmdlet removes the blob and its snapshot without confirmation.</span></span>

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

### <span data-ttu-id="6d6b9-155">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6d6b9-155">-PassThru</span></span>
<span data-ttu-id="6d6b9-156">이 cmdlet이 작업의 성공 여부를 반영 하는 **Boolean** 을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6d6b9-156">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="6d6b9-157">기본적으로이 cmdlet은 값을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6d6b9-157">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="6d6b9-158">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="6d6b9-158">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="6d6b9-159">읽을 cmdlet에 대 한 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d6b9-159">Specifies the Azure profile for the cmdlet to read.</span></span>
<span data-ttu-id="6d6b9-160">지정 하지 않으면 cmdlet은 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="6d6b9-160">If not specified, the cmdlet reads from the default profile.</span></span>

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

### <span data-ttu-id="6d6b9-161">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="6d6b9-161">-SnapshotTime</span></span>
<span data-ttu-id="6d6b9-162">Blob SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="6d6b9-162">Blob SnapshotTime</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d6b9-163">-로</span><span class="sxs-lookup"><span data-stu-id="6d6b9-163">-VersionId</span></span>
<span data-ttu-id="6d6b9-164">물방울</span><span class="sxs-lookup"><span data-stu-id="6d6b9-164">Blob VersionId</span></span>

```yaml
Type: System.String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d6b9-165">-확인</span><span class="sxs-lookup"><span data-stu-id="6d6b9-165">-Confirm</span></span>
<span data-ttu-id="6d6b9-166">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d6b9-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d6b9-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d6b9-167">-WhatIf</span></span>
<span data-ttu-id="6d6b9-168">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6d6b9-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d6b9-169">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6d6b9-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d6b9-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d6b9-170">CommonParameters</span></span>
<span data-ttu-id="6d6b9-171">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d6b9-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d6b9-172">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d6b9-172">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d6b9-173">입력</span><span class="sxs-lookup"><span data-stu-id="6d6b9-173">INPUTS</span></span>

### <span data-ttu-id="6d6b9-174">CloudBlob를 통해 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d6b9-174">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="6d6b9-175">CloudBlobContainer를 통해 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d6b9-175">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="6d6b9-176">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6d6b9-176">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6d6b9-177">출력</span><span class="sxs-lookup"><span data-stu-id="6d6b9-177">OUTPUTS</span></span>

### <span data-ttu-id="6d6b9-178">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="6d6b9-178">System.Boolean</span></span>

## <span data-ttu-id="6d6b9-179">상속자</span><span class="sxs-lookup"><span data-stu-id="6d6b9-179">NOTES</span></span>

## <span data-ttu-id="6d6b9-180">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6d6b9-180">RELATED LINKS</span></span>

[<span data-ttu-id="6d6b9-181">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="6d6b9-181">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="6d6b9-182">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6d6b9-182">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="6d6b9-183">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="6d6b9-183">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)
