---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 03EC0D20-C737-4B2B-B8D9-71D06A938FAD
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageBlob.md
ms.openlocfilehash: 37ae4192e973d218bd0cb23f9ccba16367098d30
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197532"
---
# <span data-ttu-id="a5c10-101">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="a5c10-101">Remove-AzStorageBlob</span></span>

## <span data-ttu-id="a5c10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5c10-102">SYNOPSIS</span></span>
<span data-ttu-id="a5c10-103">지정된 저장소 Blob을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c10-103">Removes the specified storage blob.</span></span>

## <span data-ttu-id="a5c10-104">구문</span><span class="sxs-lookup"><span data-stu-id="a5c10-104">SYNTAX</span></span>

### <span data-ttu-id="a5c10-105">NamePipeline(기본값)</span><span class="sxs-lookup"><span data-stu-id="a5c10-105">NamePipeline (Default)</span></span>
```
Remove-AzStorageBlob [-Blob] <String> [-Container] <String> [-DeleteSnapshot] [-SnapshotTime <DateTimeOffset>]
 [-VersionId <String>] [-Force] [-PassThru] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5c10-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="a5c10-106">BlobPipeline</span></span>
```
Remove-AzStorageBlob -CloudBlob <CloudBlob> [-BlobBaseClient <BlobBaseClient>] [-DeleteSnapshot] [-Force]
 [-PassThru] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5c10-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="a5c10-107">ContainerPipeline</span></span>
```
Remove-AzStorageBlob -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-DeleteSnapshot]
 [-SnapshotTime <DateTimeOffset>] [-VersionId <String>] [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a5c10-108">설명</span><span class="sxs-lookup"><span data-stu-id="a5c10-108">DESCRIPTION</span></span>
<span data-ttu-id="a5c10-109">**Remove-AzStorageBlob** cmdlet은 Azure의 저장소 계정에서 지정된 Blob을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c10-109">The **Remove-AzStorageBlob** cmdlet removes the specified blob from a storage account in Azure.</span></span>

## <span data-ttu-id="a5c10-110">예제</span><span class="sxs-lookup"><span data-stu-id="a5c10-110">EXAMPLES</span></span>

### <span data-ttu-id="a5c10-111">예제 1: 이름으로 저장소 Blob 제거</span><span class="sxs-lookup"><span data-stu-id="a5c10-111">Example 1: Remove a storage blob by name</span></span>
```
PS C:\>Remove-AzStorageBlob -Container "ContainerName" -Blob "BlobName"
```

<span data-ttu-id="a5c10-112">이 명령은 이름으로 식별된 Blob을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c10-112">This command removes a blob identified by its name.</span></span>

### <span data-ttu-id="a5c10-113">예제 2: 파이프라인을 사용하여 저장소 Blob 제거</span><span class="sxs-lookup"><span data-stu-id="a5c10-113">Example 2: Remove a storage blob using the pipeline</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Blob "BlobName" | Remove-AzStorageBlob
```

<span data-ttu-id="a5c10-114">이 명령은 파이프라인을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c10-114">This command uses the pipeline.</span></span>

### <span data-ttu-id="a5c10-115">예제 3: 파이프라인을 사용하여 저장소 Blob 제거</span><span class="sxs-lookup"><span data-stu-id="a5c10-115">Example 3: Remove storage blobs using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container container* | Remove-AzStorageBlob -Blob "BlobName"
```

<span data-ttu-id="a5c10-116">이 명령은 추가(\*) 와일드카드 문자 및 파이프라인을 사용하여 Blob 또는 Blob을 검색한 다음 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c10-116">This command uses the asterisk (\*) wildcard character and the pipeline to retrieve the blob or blobs and then removes them.</span></span>

### <span data-ttu-id="a5c10-117">예제 4: 단일 Blob 버전 제거</span><span class="sxs-lookup"><span data-stu-id="a5c10-117">Example 4: Remove a single blob version</span></span>
```
PS C:\> Remove-AzStorageBlob -Container "containername" -Blob blob2 -VersionId "2020-07-03T16:19:16.2883167Z"
```

<span data-ttu-id="a5c10-118">이 명령은 VersionId를 사용하여 단일 Blob verion을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c10-118">This command removes a single blobs verion with VersionId.</span></span>

### <span data-ttu-id="a5c10-119">예제 5: 단일 Blob 스냅숏 제거</span><span class="sxs-lookup"><span data-stu-id="a5c10-119">Example 5: Remove a single blob snapshot</span></span>
```
PS C:\> Remove-AzStorageBlob -Container "containername" -Blob blob1 -SnapshotTime "2020-07-06T06:56:06.8588431Z"
```

<span data-ttu-id="a5c10-120">이 명령은 SnapshotTime을 사용하여 단일 Blob 스냅숏을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c10-120">This command removes a single blobs snapshot with SnapshotTime.</span></span>

## <span data-ttu-id="a5c10-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5c10-121">PARAMETERS</span></span>

### <span data-ttu-id="a5c10-122">-Blob</span><span class="sxs-lookup"><span data-stu-id="a5c10-122">-Blob</span></span>
<span data-ttu-id="a5c10-123">제거할 Blob의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c10-123">Specifies the name of the blob you want to remove.</span></span>

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

### <span data-ttu-id="a5c10-124">-BlobBaseClient</span><span class="sxs-lookup"><span data-stu-id="a5c10-124">-BlobBaseClient</span></span>
<span data-ttu-id="a5c10-125">BlobBaseClient 개체</span><span class="sxs-lookup"><span data-stu-id="a5c10-125">BlobBaseClient Object</span></span>

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

### <span data-ttu-id="a5c10-126">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a5c10-126">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="a5c10-127">하나의 서비스 요청에 대해 클라이언트 쪽 시간(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c10-127">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="a5c10-128">이전 호출이 지정된 간격에서 실패하는 경우 이 cmdlet은 요청을 다시 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c10-128">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="a5c10-129">이 cmdlet이 간격이 경과하기 전에 성공적인 응답을 받지 못하면 이 cmdlet은 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c10-129">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="a5c10-130">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="a5c10-130">-CloudBlob</span></span>
<span data-ttu-id="a5c10-131">클라우드 Blob을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c10-131">Specifies a cloud blob.</span></span>
<span data-ttu-id="a5c10-132">**CloudBlob 개체를 얻습니다.** Get-AzStorageBlob cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c10-132">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="a5c10-133">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="a5c10-133">-CloudBlobContainer</span></span>
<span data-ttu-id="a5c10-134">Azure Storage 클라이언트 라이브러리에서 **CloudBlobContainer** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c10-134">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="a5c10-135">Get-AzStorageContainer cmdlet을 사용하여 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5c10-135">You can use the Get-AzStorageContainer cmdlet to get it.</span></span>

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

### <span data-ttu-id="a5c10-136">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="a5c10-136">-ConcurrentTaskCount</span></span>
<span data-ttu-id="a5c10-137">최대 동시 네트워크 호출을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c10-137">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="a5c10-138">이 매개 변수를 사용하면 최대 동시 네트워크 호출 수를 지정하여 동시성으로 로컬 CPU 및 대역폭 사용량을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5c10-138">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="a5c10-139">지정된 값은 절대 개수로, 코어 수에 곱하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5c10-139">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="a5c10-140">이 매개 변수는 초당 100킬로비트와 같은 낮은 대역폭 환경에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5c10-140">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="a5c10-141">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="a5c10-141">The default value is 10.</span></span>

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

### <span data-ttu-id="a5c10-142">-Container</span><span class="sxs-lookup"><span data-stu-id="a5c10-142">-Container</span></span>
<span data-ttu-id="a5c10-143">컨테이너의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c10-143">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="a5c10-144">-Context</span><span class="sxs-lookup"><span data-stu-id="a5c10-144">-Context</span></span>
<span data-ttu-id="a5c10-145">Azure 저장소 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c10-145">Specifies the Azure storage context.</span></span>
<span data-ttu-id="a5c10-146">New-AzStorageContext cmdlet을 사용하여 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5c10-146">You can use the New-AzStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="a5c10-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5c10-147">-DefaultProfile</span></span>
<span data-ttu-id="a5c10-148">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a5c10-148">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5c10-149">-DeleteSnapshot</span><span class="sxs-lookup"><span data-stu-id="a5c10-149">-DeleteSnapshot</span></span>
<span data-ttu-id="a5c10-150">모든 스냅숏이 삭제되지만 기본 Blob은 삭제하지 못하게 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c10-150">Specifies that all snapshots be deleted, but not the base blob.</span></span>
<span data-ttu-id="a5c10-151">이 매개 변수를 지정하지 않으면 기본 Blob 및 해당 스냅숏이 함께 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5c10-151">If this parameter is not specified, the base blob and its snapshots are deleted together.</span></span>
<span data-ttu-id="a5c10-152">사용자에게 삭제 작업을 확인하라는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5c10-152">The user is prompted to confirm the delete operation.</span></span>

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

### <span data-ttu-id="a5c10-153">-Force</span><span class="sxs-lookup"><span data-stu-id="a5c10-153">-Force</span></span>
<span data-ttu-id="a5c10-154">이 cmdlet이 확인 없이 Blob 및 해당 스냅숏을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c10-154">Indicates that this cmdlet removes the blob and its snapshot without confirmation.</span></span>

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

### <span data-ttu-id="a5c10-155">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a5c10-155">-PassThru</span></span>
<span data-ttu-id="a5c10-156">이 cmdlet은 작업의  성공을 반영하는 부울을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c10-156">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="a5c10-157">기본적으로 이 cmdlet은 값을 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5c10-157">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="a5c10-158">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a5c10-158">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="a5c10-159">cmdlet에서 읽을 Azure 프로필을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c10-159">Specifies the Azure profile for the cmdlet to read.</span></span>
<span data-ttu-id="a5c10-160">지정하지 않으면 cmdlet이 기본 프로필에서 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="a5c10-160">If not specified, the cmdlet reads from the default profile.</span></span>

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

### <span data-ttu-id="a5c10-161">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="a5c10-161">-SnapshotTime</span></span>
<span data-ttu-id="a5c10-162">Blob SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="a5c10-162">Blob SnapshotTime</span></span>

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

### <span data-ttu-id="a5c10-163">-VersionId</span><span class="sxs-lookup"><span data-stu-id="a5c10-163">-VersionId</span></span>
<span data-ttu-id="a5c10-164">Blob VersionId</span><span class="sxs-lookup"><span data-stu-id="a5c10-164">Blob VersionId</span></span>

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

### <span data-ttu-id="a5c10-165">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a5c10-165">-Confirm</span></span>
<span data-ttu-id="a5c10-166">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5c10-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5c10-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5c10-167">-WhatIf</span></span>
<span data-ttu-id="a5c10-168">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a5c10-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5c10-169">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5c10-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5c10-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5c10-170">CommonParameters</span></span>
<span data-ttu-id="a5c10-171">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a5c10-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5c10-172">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a5c10-172">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5c10-173">입력</span><span class="sxs-lookup"><span data-stu-id="a5c10-173">INPUTS</span></span>

### <span data-ttu-id="a5c10-174">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="a5c10-174">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="a5c10-175">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="a5c10-175">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="a5c10-176">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a5c10-176">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a5c10-177">출력</span><span class="sxs-lookup"><span data-stu-id="a5c10-177">OUTPUTS</span></span>

### <span data-ttu-id="a5c10-178">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a5c10-178">System.Boolean</span></span>

## <span data-ttu-id="a5c10-179">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a5c10-179">NOTES</span></span>

## <span data-ttu-id="a5c10-180">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a5c10-180">RELATED LINKS</span></span>

[<span data-ttu-id="a5c10-181">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="a5c10-181">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="a5c10-182">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a5c10-182">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="a5c10-183">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="a5c10-183">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)
