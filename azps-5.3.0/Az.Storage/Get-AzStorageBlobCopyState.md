---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: CBD157D2-37C5-491F-A806-6B39F1D0415A
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageblobcopystate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobCopyState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageBlobCopyState.md
ms.openlocfilehash: 319463dfb80cddbbffe5b7d1652a04f98e285768
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489308"
---
# <span data-ttu-id="364c4-101">Get-AzStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="364c4-101">Get-AzStorageBlobCopyState</span></span>

## <span data-ttu-id="364c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="364c4-102">SYNOPSIS</span></span>
<span data-ttu-id="364c4-103">Azure Storage Blob의 복사 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="364c4-103">Gets the copy status of an Azure Storage blob.</span></span>

## <span data-ttu-id="364c4-104">구문</span><span class="sxs-lookup"><span data-stu-id="364c4-104">SYNTAX</span></span>

### <span data-ttu-id="364c4-105">NamePipeline(기본값)</span><span class="sxs-lookup"><span data-stu-id="364c4-105">NamePipeline (Default)</span></span>
```
Get-AzStorageBlobCopyState [-Blob] <String> [-Container] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="364c4-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="364c4-106">BlobPipeline</span></span>
```
Get-AzStorageBlobCopyState -CloudBlob <CloudBlob> [-WaitForComplete] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="364c4-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="364c4-107">ContainerPipeline</span></span>
```
Get-AzStorageBlobCopyState -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="364c4-108">설명</span><span class="sxs-lookup"><span data-stu-id="364c4-108">DESCRIPTION</span></span>
<span data-ttu-id="364c4-109">**Get-AzStorageBlobCopyState** cmdlet은 Azure Storage Blob의 복사 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="364c4-109">The **Get-AzStorageBlobCopyState** cmdlet gets the copy status of an Azure Storage blob.</span></span>
<span data-ttu-id="364c4-110">복사 대상 Blob에서 실행해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="364c4-110">It should run on the copy destination blob.</span></span>

## <span data-ttu-id="364c4-111">예제</span><span class="sxs-lookup"><span data-stu-id="364c4-111">EXAMPLES</span></span>

### <span data-ttu-id="364c4-112">예제 1: Blob의 복사 상태 확인</span><span class="sxs-lookup"><span data-stu-id="364c4-112">Example 1: Get the copy status of a blob</span></span>
```
C:\PS>Get-AzStorageBlobCopyState -Blob "ContosoPlanning2015" -Container "ContosoUploads"
```

<span data-ttu-id="364c4-113">이 명령은 ContosoUploads 컨테이너에서 ContosoPlanning2015라는 Blob의 복사 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="364c4-113">This command gets the copy status of the blob named ContosoPlanning2015 in the container ContosoUploads.</span></span>

### <span data-ttu-id="364c4-114">예제 2: 파이프라인을 사용하여 Blob의 복사 상태 얻기</span><span class="sxs-lookup"><span data-stu-id="364c4-114">Example 2: Get the copy status for of a blob by using the pipeline</span></span>
```
C:\PS>Get-AzStorageBlob -Blob "ContosoPlanning2015" -Container "ContosoUploads" | Get-AzStorageBlobCopyState
```

<span data-ttu-id="364c4-115">이 명령은 **Get-AzStorageBlob** cmdlet을 사용하여 ContosoUploads라는 컨테이너에서 ContosoPlanning2015라는 Blob을 얻은 다음 파이프라인 연산자를 사용하여 현재 cmdlet에 결과를 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="364c4-115">This command gets the blob named ContosoPlanning2015 in the container named ContosoUploads by using the **Get-AzStorageBlob** cmdlet, and then passes the result to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="364c4-116">**Get-AzStorageBlobCopyState** cmdlet은 해당 Blob에 대한 복사 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="364c4-116">The **Get-AzStorageBlobCopyState** cmdlet gets the copy status for that blob.</span></span>

### <span data-ttu-id="364c4-117">예제 3: 파이프라인을 사용하여 컨테이너의 Blob에 대한 복사 상태 확인</span><span class="sxs-lookup"><span data-stu-id="364c4-117">Example 3: Get the copy status for a blob in a container by using the pipeline</span></span>
```
C:\PS>Get-AzStorageContainer -Name "ContosoUploads" | Get-AzStorageBlobCopyState -Blob "ContosoPlanning2015"
```

<span data-ttu-id="364c4-118">이 명령은 **Get-AzStorageBlob** cmdlet을 사용하여 컨테이너 이름을 지정한 다음 결과를 현재 cmdlet에 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="364c4-118">This command gets the container named by using the **Get-AzStorageBlob** cmdlet, and then passes the result to the current cmdlet.</span></span>
<span data-ttu-id="364c4-119">**Get-AzStorageContainer** cmdlet은 해당 컨테이너에서 ContosoPlanning2015라는 Blob에 대한 복사 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="364c4-119">The **Get-AzStorageContainer** cmdlet gets the copy status for the blob named ContosoPlanning2015 in that container.</span></span>

### <span data-ttu-id="364c4-120">예제 4: 복사 및 파이프라인을 시작하여 복사 상태 얻기</span><span class="sxs-lookup"><span data-stu-id="364c4-120">Example 4: Start Copy and pipeline to get the copy status</span></span>
```
C:\PS> $destBlob = Start-AzStorageBlobCopy -SrcContainer "contosouploads" -SrcBlob "ContosoPlanning2015" -DestContainer "contosouploads2" -DestBlob "ContosoPlanning2015_copy"

C:\PS> $destBlob | Get-AzStorageBlobCopyState
```

<span data-ttu-id="364c4-121">첫 번째 명령은 Blob "ContosoPlanning2015"를 "ContosoPlanning2015_copy"로 복사하고 destiantion Blob 개체를 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="364c4-121">The first command starts copy blob "ContosoPlanning2015" to "ContosoPlanning2015_copy", and output the destiantion blob object.</span></span> <span data-ttu-id="364c4-122">두 번째 명령 파이프라인은 Destiantion Blob 개체를 Get-AzStorageBlobCopyState로 파이프라인하여 Blob 복사 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="364c4-122">The second command pipeline the destiantion blob object to Get-AzStorageBlobCopyState, to get blob copy state.</span></span> 

## <span data-ttu-id="364c4-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="364c4-123">PARAMETERS</span></span>

### <span data-ttu-id="364c4-124">-Blob</span><span class="sxs-lookup"><span data-stu-id="364c4-124">-Blob</span></span>
<span data-ttu-id="364c4-125">Blob의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="364c4-125">Specifies the name of a blob.</span></span>
<span data-ttu-id="364c4-126">이 cmdlet은 이 매개 변수가 지정하는 Azure Storage Blob에 대한 Blob 복사 작업의 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="364c4-126">This cmdlet gets the state of the blob copy operation for the Azure Storage blob that this parameter specifies.</span></span>

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

### <span data-ttu-id="364c4-127">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="364c4-127">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="364c4-128">하나의 서비스 요청에 대해 클라이언트 쪽 시간(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="364c4-128">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="364c4-129">이전 호출이 지정된 간격에서 실패하는 경우 이 cmdlet은 요청을 다시 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="364c4-129">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="364c4-130">이 cmdlet이 간격이 경과하기 전에 성공적인 응답을 받지 못하면 이 cmdlet은 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="364c4-130">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="364c4-131">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="364c4-131">-CloudBlob</span></span>
<span data-ttu-id="364c4-132">Azure Storage 클라이언트 라이브러리의 **CloudBlob** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="364c4-132">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="364c4-133">**CloudBlob 개체를 얻으면** Get-AzStorageBlob cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="364c4-133">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="364c4-134">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="364c4-134">-CloudBlobContainer</span></span>
<span data-ttu-id="364c4-135">Azure Storage 클라이언트 라이브러리에서 **CloudBlobContainer** 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="364c4-135">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="364c4-136">이 cmdlet은 이 매개 변수가 지정하는 컨테이너에 있는 Blob의 복사 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="364c4-136">This cmdlet gets the copy status of a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="364c4-137">**CloudBlobContainer** 개체를 얻습니다. Get-AzStorageContainer cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="364c4-137">To obtain a **CloudBlobContainer** object, use the Get-AzStorageContainer cmdlet.</span></span>

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

### <span data-ttu-id="364c4-138">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="364c4-138">-ConcurrentTaskCount</span></span>
<span data-ttu-id="364c4-139">최대 동시 네트워크 호출을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="364c4-139">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="364c4-140">이 매개 변수를 사용하여 최대 동시 네트워크 호출 수를 지정하여 동시성으로 로컬 CPU 및 대역폭 사용량을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="364c4-140">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="364c4-141">지정된 값은 절대 개수로, 코어 수에 곱하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="364c4-141">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="364c4-142">이 매개 변수는 초당 100킬로비트와 같은 낮은 대역폭 환경에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="364c4-142">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="364c4-143">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="364c4-143">The default value is 10.</span></span>

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

### <span data-ttu-id="364c4-144">-Container</span><span class="sxs-lookup"><span data-stu-id="364c4-144">-Container</span></span>
<span data-ttu-id="364c4-145">컨테이너의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="364c4-145">Specifies the name of a container.</span></span>
<span data-ttu-id="364c4-146">이 cmdlet은 이 매개 변수가 지정하는 컨테이너의 Blob에 대한 복사 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="364c4-146">This cmdlet gets the copy status for a blob in the container that this parameter specifies.</span></span>

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

### <span data-ttu-id="364c4-147">-Context</span><span class="sxs-lookup"><span data-stu-id="364c4-147">-Context</span></span>
<span data-ttu-id="364c4-148">Azure 저장소 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="364c4-148">Specifies an Azure storage context.</span></span>
<span data-ttu-id="364c4-149">저장소 컨텍스트를 얻습니다. New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="364c4-149">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="364c4-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="364c4-150">-DefaultProfile</span></span>
<span data-ttu-id="364c4-151">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="364c4-151">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="364c4-152">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="364c4-152">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="364c4-153">요청에 대한 서비스 쪽 시간제한 간격(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="364c4-153">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="364c4-154">지정된 간격이 서비스에서 요청을 처리하기 전에 경과하면 저장소 서비스가 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="364c4-154">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="364c4-155">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="364c4-155">-WaitForComplete</span></span>
<span data-ttu-id="364c4-156">이 cmdlet이 복사본이 완료될 때까지 기다렸다는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="364c4-156">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="364c4-157">이 매개 변수를 지정하지 않으면 이 cmdlet은 결과를 즉시 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="364c4-157">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

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

### <span data-ttu-id="364c4-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="364c4-158">CommonParameters</span></span>
<span data-ttu-id="364c4-159">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="364c4-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="364c4-160">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="364c4-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="364c4-161">입력</span><span class="sxs-lookup"><span data-stu-id="364c4-161">INPUTS</span></span>

### <span data-ttu-id="364c4-162">Microsoft.Azure.Storage.Blob.CloudBlob</span><span class="sxs-lookup"><span data-stu-id="364c4-162">Microsoft.Azure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="364c4-163">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="364c4-163">Microsoft.Azure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="364c4-164">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="364c4-164">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="364c4-165">출력</span><span class="sxs-lookup"><span data-stu-id="364c4-165">OUTPUTS</span></span>

### <span data-ttu-id="364c4-166">Microsoft.Azure.Storage.Blob.CopyState</span><span class="sxs-lookup"><span data-stu-id="364c4-166">Microsoft.Azure.Storage.Blob.CopyState</span></span>

## <span data-ttu-id="364c4-167">참고 사항</span><span class="sxs-lookup"><span data-stu-id="364c4-167">NOTES</span></span>

## <span data-ttu-id="364c4-168">관련 링크</span><span class="sxs-lookup"><span data-stu-id="364c4-168">RELATED LINKS</span></span>

[<span data-ttu-id="364c4-169">Start-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="364c4-169">Start-AzStorageBlobCopy</span></span>](./Start-AzStorageBlobCopy.md)

[<span data-ttu-id="364c4-170">Stop-AzStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="364c4-170">Stop-AzStorageBlobCopy</span></span>](./Stop-AzStorageBlobCopy.md)


