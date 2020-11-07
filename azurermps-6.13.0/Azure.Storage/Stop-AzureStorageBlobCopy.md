---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: C274DFBD-6C93-4043-AF93-DAF7BEA1F11F
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/stop-azurestorageblobcopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Stop-AzureStorageBlobCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Stop-AzureStorageBlobCopy.md
ms.openlocfilehash: 67a6a9d706b8865ebca4290649a30bc8e9817569
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703195"
---
# <span data-ttu-id="10a72-101">Stop-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="10a72-101">Stop-AzureStorageBlobCopy</span></span>

## <span data-ttu-id="10a72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="10a72-102">SYNOPSIS</span></span>
<span data-ttu-id="10a72-103">복사 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="10a72-103">Stops a copy operation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10a72-104">구문과</span><span class="sxs-lookup"><span data-stu-id="10a72-104">SYNTAX</span></span>

### <span data-ttu-id="10a72-105">NamePipeline (기본값)</span><span class="sxs-lookup"><span data-stu-id="10a72-105">NamePipeline (Default)</span></span>
```
Stop-AzureStorageBlobCopy [-Blob] <String> [-Container] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="10a72-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="10a72-106">BlobPipeline</span></span>
```
Stop-AzureStorageBlobCopy -CloudBlob <CloudBlob> [-Force] [-CopyId <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="10a72-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="10a72-107">ContainerPipeline</span></span>
```
Stop-AzureStorageBlobCopy -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-Force] [-CopyId <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="10a72-108">설명은</span><span class="sxs-lookup"><span data-stu-id="10a72-108">DESCRIPTION</span></span>
<span data-ttu-id="10a72-109">**Stop-AzureStorageBlobCopy** cmdlet은 지정 된 대상 blob에 대 한 복사 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="10a72-109">The **Stop-AzureStorageBlobCopy** cmdlet stops a copy operation to the specified destination blob.</span></span>

## <span data-ttu-id="10a72-110">예제의</span><span class="sxs-lookup"><span data-stu-id="10a72-110">EXAMPLES</span></span>

### <span data-ttu-id="10a72-111">예제 1: 이름으로 복사 작업 중지</span><span class="sxs-lookup"><span data-stu-id="10a72-111">Example 1: Stop copy operation by name</span></span>
```
PS C:\>Stop-AzureStorageBlobCopy -Container "ContainerName" -Blob "BlobName" -CopyId "CopyID"
```

<span data-ttu-id="10a72-112">이 명령은 이름으로 복사 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="10a72-112">This command stops the copy operation by name.</span></span>

### <span data-ttu-id="10a72-113">예제 2: 파이프라인을 사용 하 여 복사 작업 중지</span><span class="sxs-lookup"><span data-stu-id="10a72-113">Example 2: Stop copy operation by using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer container* | Stop-AzureStorageBlobCopy -Blob "BlobName"
```

<span data-ttu-id="10a72-114">이 명령은 **AzureStorageContainer** 에서 파이프라인의 컨테이너를 전달 하 여 복사 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="10a72-114">This command stops the copy operation by passing the container on the pipeline from **Get-AzureStorageContainer**.</span></span>

### <span data-ttu-id="10a72-115">예제 3: 파이프라인 및 Get-AzureStorageBlob를 사용 하 여 복사 작업 중지</span><span class="sxs-lookup"><span data-stu-id="10a72-115">Example 3: Stop copy operation by using the pipeline and Get-AzureStorageBlob</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" | Stop-AzureStorageBlobCopy -Force
```

<span data-ttu-id="10a72-116">이 예제에서는 Get-AzureStorageBlob cmdlet에서 파이프라인에 컨테이너를 전달 하 여 복사 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="10a72-116">This example stops the copy operation by passing the container on the pipeline from the Get-AzureStorageBlob cmdlet.</span></span>

## <span data-ttu-id="10a72-117">변수</span><span class="sxs-lookup"><span data-stu-id="10a72-117">PARAMETERS</span></span>

### <span data-ttu-id="10a72-118">-Blob</span><span class="sxs-lookup"><span data-stu-id="10a72-118">-Blob</span></span>
<span data-ttu-id="10a72-119">Blob의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="10a72-119">Specifies the name of the blob.</span></span>

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

### <span data-ttu-id="10a72-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="10a72-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="10a72-121">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="10a72-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="10a72-122">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="10a72-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="10a72-123">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="10a72-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="10a72-124">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="10a72-124">-CloudBlob</span></span>
<span data-ttu-id="10a72-125">Azure Storage 클라이언트 라이브러리에서 **CloudBlob** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="10a72-125">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="10a72-126">**CloudBlob** 개체를 가져오려면 Get-AzureStorageBlob cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="10a72-126">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10a72-127">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="10a72-127">-CloudBlobContainer</span></span>
<span data-ttu-id="10a72-128">Azure Storage 클라이언트 라이브러리에서 **CloudBlobContainer** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="10a72-128">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="10a72-129">개체를 만들거나 Get-AzureStorageContainer cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="10a72-129">You can create the object or use the Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="10a72-130">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="10a72-130">-ConcurrentTaskCount</span></span>
<span data-ttu-id="10a72-131">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="10a72-131">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="10a72-132">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="10a72-132">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="10a72-133">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="10a72-133">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="10a72-134">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="10a72-134">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="10a72-135">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="10a72-135">The default value is 10.</span></span>

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

### <span data-ttu-id="10a72-136">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="10a72-136">-Container</span></span>
<span data-ttu-id="10a72-137">컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="10a72-137">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="10a72-138">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="10a72-138">-Context</span></span>
<span data-ttu-id="10a72-139">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="10a72-139">Specifies the Azure storage context.</span></span>
<span data-ttu-id="10a72-140">New-AzureStorageContext cmdlet을 사용 하 여 컨텍스트를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="10a72-140">You can create the context by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="10a72-141">-CopyId</span><span class="sxs-lookup"><span data-stu-id="10a72-141">-CopyId</span></span>
<span data-ttu-id="10a72-142">복사본 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="10a72-142">Specifies the copy ID.</span></span>

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

### <span data-ttu-id="10a72-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10a72-143">-DefaultProfile</span></span>
<span data-ttu-id="10a72-144">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="10a72-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10a72-145">-Force</span><span class="sxs-lookup"><span data-stu-id="10a72-145">-Force</span></span>
<span data-ttu-id="10a72-146">확인 메시지 없이 지정 된 blob에서 현재 복사 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="10a72-146">Stops the current copy task on the specified blob without prompting for confirmation.</span></span>

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

### <span data-ttu-id="10a72-147">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="10a72-147">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="10a72-148">요청에 대 한 서비스 측 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="10a72-148">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="10a72-149">서비스가 요청을 처리 하기 전에 지정 된 간격이 경과 하면 저장소 서비스에서 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="10a72-149">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="10a72-150">-확인</span><span class="sxs-lookup"><span data-stu-id="10a72-150">-Confirm</span></span>
<span data-ttu-id="10a72-151">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="10a72-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="10a72-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="10a72-152">-WhatIf</span></span>
<span data-ttu-id="10a72-153">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="10a72-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="10a72-154">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="10a72-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="10a72-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10a72-155">CommonParameters</span></span>
<span data-ttu-id="10a72-156">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="10a72-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10a72-157">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10a72-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10a72-158">입력</span><span class="sxs-lookup"><span data-stu-id="10a72-158">INPUTS</span></span>

### <span data-ttu-id="10a72-159">WindowsAzure. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="10a72-159">Microsoft.WindowsAzure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="10a72-160">WindowsAzure. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="10a72-160">Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="10a72-161">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="10a72-161">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="10a72-162">출력</span><span class="sxs-lookup"><span data-stu-id="10a72-162">OUTPUTS</span></span>

### <span data-ttu-id="10a72-163">WindowsAzure. ResourceModel. m b m.</span><span class="sxs-lookup"><span data-stu-id="10a72-163">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageBlob</span></span>

## <span data-ttu-id="10a72-164">상속자</span><span class="sxs-lookup"><span data-stu-id="10a72-164">NOTES</span></span>

## <span data-ttu-id="10a72-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="10a72-165">RELATED LINKS</span></span>

[<span data-ttu-id="10a72-166">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="10a72-166">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="10a72-167">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="10a72-167">Get-AzureStorageContainer</span></span>](./Get-AzureStorageContainer.md)

[<span data-ttu-id="10a72-168">시작-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="10a72-168">Start-AzureStorageBlobCopy</span></span>](./Start-AzureStorageBlobCopy.md)

[<span data-ttu-id="10a72-169">Get-AzureStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="10a72-169">Get-AzureStorageBlobCopyState</span></span>](./Get-AzureStorageBlobCopyState.md)
