---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C274DFBD-6C93-4043-AF93-DAF7BEA1F11F
online version: https://docs.microsoft.com/powershell/module/az.storage/stop-azstorageblobcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageBlobCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageBlobCopy.md
ms.openlocfilehash: 1be012a9a9c5a62cbd08451849f8d50e9a5d52a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960064"
---
# <span data-ttu-id="65f52-101">Stop-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="65f52-101">Stop-AzStorageBlobCopy</span></span>

## <span data-ttu-id="65f52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65f52-102">SYNOPSIS</span></span>
<span data-ttu-id="65f52-103">복사 작업을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="65f52-103">Stops a copy operation.</span></span>

## <span data-ttu-id="65f52-104">구문</span><span class="sxs-lookup"><span data-stu-id="65f52-104">SYNTAX</span></span>

### <span data-ttu-id="65f52-105">NamePipeline(기본값)</span><span class="sxs-lookup"><span data-stu-id="65f52-105">NamePipeline (Default)</span></span>
```
Stop-AzStorageBlobCopy [-Blob] <String> [-Container] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="65f52-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="65f52-106">BlobPipeline</span></span>
```
Stop-AzStorageBlobCopy -CloudBlob <CloudBlob> [-Force] [-CopyId <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="65f52-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="65f52-107">ContainerPipeline</span></span>
```
Stop-AzStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="65f52-108">설명</span><span class="sxs-lookup"><span data-stu-id="65f52-108">DESCRIPTION</span></span>
<span data-ttu-id="65f52-109">**Stop-AzStorageBlobCopy** cmdlet은 지정된 대상 Blob에 대한 복사 작업을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="65f52-109">The **Stop-AzStorageBlobCopy** cmdlet stops a copy operation to the specified destination blob.</span></span>

## <span data-ttu-id="65f52-110">예제</span><span class="sxs-lookup"><span data-stu-id="65f52-110">EXAMPLES</span></span>

### <span data-ttu-id="65f52-111">예제 1: 이름으로 복사 작업 중지</span><span class="sxs-lookup"><span data-stu-id="65f52-111">Example 1: Stop copy operation by name</span></span>
```
PS C:\>Stop-AzStorageBlobCopy -Container "ContainerName" -Blob "BlobName" -CopyId "CopyID"
```

<span data-ttu-id="65f52-112">이 명령은 이름으로 복사 작업을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="65f52-112">This command stops the copy operation by name.</span></span>

### <span data-ttu-id="65f52-113">예제 2: 파이프라인을 사용하여 복사 작업 중지</span><span class="sxs-lookup"><span data-stu-id="65f52-113">Example 2: Stop copy operation by using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer container* | Stop-AzStorageBlobCopy -Blob "BlobName"
```

<span data-ttu-id="65f52-114">이 명령은 **Get-AzStorageContainer에서** 파이프라인의 컨테이너를 전달하여 복사 작업을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="65f52-114">This command stops the copy operation by passing the container on the pipeline from **Get-AzStorageContainer**.</span></span>

### <span data-ttu-id="65f52-115">예제 3: 파이프라인을 사용하여 복사 작업을 중지하고 Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="65f52-115">Example 3: Stop copy operation by using the pipeline and Get-AzStorageBlob</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" | Stop-AzStorageBlobCopy -Force
```

<span data-ttu-id="65f52-116">이 예제에서는 파이프라인의 컨테이너를 cmdlet에서 전달하여 복사 Get-AzStorageBlob 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="65f52-116">This example stops the copy operation by passing the container on the pipeline from the Get-AzStorageBlob cmdlet.</span></span>

## <span data-ttu-id="65f52-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="65f52-117">PARAMETERS</span></span>

### <span data-ttu-id="65f52-118">-Blob</span><span class="sxs-lookup"><span data-stu-id="65f52-118">-Blob</span></span>
<span data-ttu-id="65f52-119">Blob의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="65f52-119">Specifies the name of the blob.</span></span>

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

### <span data-ttu-id="65f52-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="65f52-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="65f52-121">하나의 서비스 요청에 대해 클라이언트 쪽 시간 간격(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="65f52-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="65f52-122">지정된 간격에서 이전 호출이 실패하면 이 cmdlet에서 요청을 다시 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="65f52-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="65f52-123">간격이 경과하기 전에 이 cmdlet에서 성공적인 응답을 받지 못하면 이 cmdlet은 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="65f52-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="65f52-124">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="65f52-124">-CloudBlob</span></span>
<span data-ttu-id="65f52-125">Azure Storage 클라이언트 라이브러리에서 **CloudBlob** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="65f52-125">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="65f52-126">**CloudBlob** 개체를 얻으면 Get-AzStorageBlob cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="65f52-126">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="65f52-127">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="65f52-127">-CloudBlobContainer</span></span>
<span data-ttu-id="65f52-128">Azure Storage 클라이언트 라이브러리에서 **CloudBlobContainer** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="65f52-128">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="65f52-129">개체를 만들거나 cmdlet을 Get-AzStorageContainer 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="65f52-129">You can create the object or use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="65f52-130">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="65f52-130">-ConcurrentTaskCount</span></span>
<span data-ttu-id="65f52-131">최대 동시 네트워크 호출을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="65f52-131">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="65f52-132">이 매개 변수를 사용하여 최대 동시 네트워크 호출 수를 지정하여 로컬 CPU 및 대역폭 사용량을 제한하는 동시성 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="65f52-132">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="65f52-133">지정된 값은 절대 개수로 코어 수에 곱하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="65f52-133">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="65f52-134">이 매개 변수는 초당 100킬로비트와 같은 대역폭이 낮은 환경에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="65f52-134">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="65f52-135">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="65f52-135">The default value is 10.</span></span>

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

### <span data-ttu-id="65f52-136">-Container</span><span class="sxs-lookup"><span data-stu-id="65f52-136">-Container</span></span>
<span data-ttu-id="65f52-137">컨테이너의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="65f52-137">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="65f52-138">-Context</span><span class="sxs-lookup"><span data-stu-id="65f52-138">-Context</span></span>
<span data-ttu-id="65f52-139">Azure Storage 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="65f52-139">Specifies the Azure storage context.</span></span>
<span data-ttu-id="65f52-140">New-AzStorageContext cmdlet을 사용하여 컨텍스트를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="65f52-140">You can create the context by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="65f52-141">-CopyId</span><span class="sxs-lookup"><span data-stu-id="65f52-141">-CopyId</span></span>
<span data-ttu-id="65f52-142">복사 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="65f52-142">Specifies the copy ID.</span></span>

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

### <span data-ttu-id="65f52-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65f52-143">-DefaultProfile</span></span>
<span data-ttu-id="65f52-144">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="65f52-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65f52-145">-Force</span><span class="sxs-lookup"><span data-stu-id="65f52-145">-Force</span></span>
<span data-ttu-id="65f52-146">확인을 요청하지 않고 지정된 Blob의 현재 복사 작업을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="65f52-146">Stops the current copy task on the specified blob without prompting for confirmation.</span></span>

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

### <span data-ttu-id="65f52-147">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="65f52-147">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="65f52-148">요청에 대해 서비스 쪽 시간 시간 간격(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="65f52-148">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="65f52-149">서비스가 요청을 처리하기 전에 지정된 간격이 경과하면 저장소 서비스가 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="65f52-149">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="65f52-150">-확인</span><span class="sxs-lookup"><span data-stu-id="65f52-150">-Confirm</span></span>
<span data-ttu-id="65f52-151">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="65f52-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65f52-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65f52-152">-WhatIf</span></span>
<span data-ttu-id="65f52-153">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="65f52-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65f52-154">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="65f52-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65f52-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65f52-155">CommonParameters</span></span>
<span data-ttu-id="65f52-156">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="65f52-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65f52-157">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="65f52-157">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65f52-158">입력</span><span class="sxs-lookup"><span data-stu-id="65f52-158">INPUTS</span></span>

### <span data-ttu-id="65f52-159">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="65f52-159">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="65f52-160">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="65f52-160">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="65f52-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="65f52-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="65f52-162">출력</span><span class="sxs-lookup"><span data-stu-id="65f52-162">OUTPUTS</span></span>

### <span data-ttu-id="65f52-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="65f52-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="65f52-164">참고 사항</span><span class="sxs-lookup"><span data-stu-id="65f52-164">NOTES</span></span>

## <span data-ttu-id="65f52-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="65f52-165">RELATED LINKS</span></span>

[<span data-ttu-id="65f52-166">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="65f52-166">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="65f52-167">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="65f52-167">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="65f52-168">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="65f52-168">Start-AzStorageBlobCopy</span></span>](./Start-AzStorageBlobCopy.md)

[<span data-ttu-id="65f52-169">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="65f52-169">Get-AzStorageBlobCopyState</span></span>](./Get-AzStorageBlobCopyState.md)
