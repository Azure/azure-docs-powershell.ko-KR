---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: CBD157D2-37C5-491F-A806-6B39F1D0415A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3191d7369597fbfb0781b550a57f0032f9aaad4f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93524047"
---
# <span data-ttu-id="2c33b-101">Get-AzureStorageBlobCopyState</span><span class="sxs-lookup"><span data-stu-id="2c33b-101">Get-AzureStorageBlobCopyState</span></span>

## <span data-ttu-id="2c33b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c33b-102">SYNOPSIS</span></span>
<span data-ttu-id="2c33b-103">Azure 저장소 blob의 복사 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2c33b-103">Gets the copy status of an Azure Storage blob.</span></span>

## <span data-ttu-id="2c33b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2c33b-104">SYNTAX</span></span>

### <span data-ttu-id="2c33b-105">NamePipeline (기본값)</span><span class="sxs-lookup"><span data-stu-id="2c33b-105">NamePipeline (Default)</span></span>
```
Get-AzureStorageBlobCopyState [-Blob] <String> [-Container] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="2c33b-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="2c33b-106">BlobPipeline</span></span>
```
Get-AzureStorageBlobCopyState -CloudBlob <CloudBlob> [-WaitForComplete] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="2c33b-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="2c33b-107">ContainerPipeline</span></span>
```
Get-AzureStorageBlobCopyState -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-WaitForComplete]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="2c33b-108">설명은</span><span class="sxs-lookup"><span data-stu-id="2c33b-108">DESCRIPTION</span></span>
<span data-ttu-id="2c33b-109">**Get-AzureStorageBlobCopyState** Cmdlet은 Azure Storage blob의 복사 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2c33b-109">The **Get-AzureStorageBlobCopyState** cmdlet gets the copy status of an Azure Storage blob.</span></span>

## <span data-ttu-id="2c33b-110">예제의</span><span class="sxs-lookup"><span data-stu-id="2c33b-110">EXAMPLES</span></span>

### <span data-ttu-id="2c33b-111">예제 1: blob의 복사 상태 가져오기</span><span class="sxs-lookup"><span data-stu-id="2c33b-111">Example 1: Get the copy status of a blob</span></span>
```
C:\PS>Get-AzureStorageBlobCopyState -Blob "ContosoPlanning2015" -Container "ContosoUploads"
```

<span data-ttu-id="2c33b-112">이 명령은 컨테이너 ContosoUploads에서 ContosoPlanning2015 라는 blob의 복사 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2c33b-112">This command gets the copy status of the blob named ContosoPlanning2015 in the container ContosoUploads.</span></span>

### <span data-ttu-id="2c33b-113">예제 2: 파이프라인을 사용 하 여 blob의 복사 상태 가져오기</span><span class="sxs-lookup"><span data-stu-id="2c33b-113">Example 2: Get the copy status for of a blob by using the pipeline</span></span>
```
C:\PS>Get-AzureStorageBlob -Blob "ContosoPlanning2015" -Container "ContosoUploads" | Get-AzureStorageBlobCopyState
```

<span data-ttu-id="2c33b-114">이 명령은 **Get-AzureStorageBlob** cmdlet을 사용 하 여 ContosoUploads 이라는 컨테이너에서 ContosoPlanning2015 라는 blob을 가져온 다음 파이프라인 연산자를 사용 하 여 현재 cmdlet에 결과를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c33b-114">This command gets the blob named ContosoPlanning2015 in the container named ContosoUploads by using the **Get-AzureStorageBlob** cmdlet, and then passes the result to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="2c33b-115">**Get-AzureStorageBlobCopyState** cmdlet은 해당 blob에 대 한 복사 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2c33b-115">The **Get-AzureStorageBlobCopyState** cmdlet gets the copy status for that blob.</span></span>

### <span data-ttu-id="2c33b-116">예제 3: 파이프라인을 사용 하 여 컨테이너의 blob에 대 한 복사 상태 가져오기</span><span class="sxs-lookup"><span data-stu-id="2c33b-116">Example 3: Get the copy status for a blob in a container by using the pipeline</span></span>
```
C:\PS>Get-AzureStorageContainer -Name "ContosoUploads" | Get-AzureStorageBlobCopyState -Blob "ContosoPlanning2015"
```

<span data-ttu-id="2c33b-117">이 명령은 **Get-AzureStorageBlob** cmdlet을 사용 하 여 명명 된 컨테이너를 가져온 다음 결과를 현재 cmdlet으로 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c33b-117">This command gets the container named by using the **Get-AzureStorageBlob** cmdlet, and then passes the result to the current cmdlet.</span></span>
<span data-ttu-id="2c33b-118">**AzureStorageContainer** cmdlet은 해당 컨테이너의 ContosoPlanning2015 라는 blob에 대 한 복사 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2c33b-118">The **Get-AzureStorageContainer** cmdlet gets the copy status for the blob named ContosoPlanning2015 in that container.</span></span>

## <span data-ttu-id="2c33b-119">변수</span><span class="sxs-lookup"><span data-stu-id="2c33b-119">PARAMETERS</span></span>

### <span data-ttu-id="2c33b-120">-Blob</span><span class="sxs-lookup"><span data-stu-id="2c33b-120">-Blob</span></span>
<span data-ttu-id="2c33b-121">Blob의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c33b-121">Specifies the name of a blob.</span></span>
<span data-ttu-id="2c33b-122">이 cmdlet은이 매개 변수에서 지정 하는 Azure 저장소 blob에 대 한 blob 복사 작업의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2c33b-122">This cmdlet gets the state of the blob copy operation for the Azure Storage blob that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: NamePipeline, ContainerPipeline
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c33b-123">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2c33b-123">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="2c33b-124">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c33b-124">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="2c33b-125">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c33b-125">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="2c33b-126">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c33b-126">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c33b-127">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="2c33b-127">-CloudBlob</span></span>
<span data-ttu-id="2c33b-128">Azure Storage 클라이언트 라이브러리에서 **CloudBlob** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c33b-128">Specifies a **CloudBlob** object from Azure Storage Client library.</span></span>
<span data-ttu-id="2c33b-129">**CloudBlob** 개체를 가져오려면 Get-AzureStorageBlob cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c33b-129">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

```yaml
Type: CloudBlob
Parameter Sets: BlobPipeline
Aliases: ICloudBlob

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c33b-130">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="2c33b-130">-CloudBlobContainer</span></span>
<span data-ttu-id="2c33b-131">Azure Storage 클라이언트 라이브러리에서 **CloudBlobContainer** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c33b-131">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="2c33b-132">이 cmdlet은이 매개 변수에서 지정 하는 컨테이너의 blob에 대 한 복사본 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2c33b-132">This cmdlet gets the copy status of a blob in the container that this parameter specifies.</span></span>
<span data-ttu-id="2c33b-133">**CloudBlobContainer** 개체를 가져오려면 Get-AzureStorageContainer cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c33b-133">To obtain a **CloudBlobContainer** object, use the Get-AzureStorageContainer cmdlet.</span></span>

```yaml
Type: CloudBlobContainer
Parameter Sets: ContainerPipeline
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c33b-134">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="2c33b-134">-ConcurrentTaskCount</span></span>
<span data-ttu-id="2c33b-135">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c33b-135">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="2c33b-136">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2c33b-136">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="2c33b-137">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="2c33b-137">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="2c33b-138">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2c33b-138">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="2c33b-139">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="2c33b-139">The default value is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c33b-140">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="2c33b-140">-Container</span></span>
<span data-ttu-id="2c33b-141">컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c33b-141">Specifies the name of a container.</span></span>
<span data-ttu-id="2c33b-142">이 cmdlet은이 매개 변수에서 지정 하는 컨테이너의 blob에 대 한 복사 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="2c33b-142">This cmdlet gets the copy status for a blob in the container that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: NamePipeline
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c33b-143">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="2c33b-143">-Context</span></span>
<span data-ttu-id="2c33b-144">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c33b-144">Specifies an Azure storage context.</span></span>
<span data-ttu-id="2c33b-145">저장소 컨텍스트를 얻으려면 New-AzureStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c33b-145">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c33b-146">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="2c33b-146">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="2c33b-147">요청에 대 한 서비스 측 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c33b-147">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="2c33b-148">서비스가 요청을 처리 하기 전에 지정 된 간격이 경과 하면 저장소 서비스에서 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c33b-148">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c33b-149">-WaitForComplete</span><span class="sxs-lookup"><span data-stu-id="2c33b-149">-WaitForComplete</span></span>
<span data-ttu-id="2c33b-150">이 cmdlet이 복사가 완료 될 때까지 대기 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2c33b-150">Indicates that this cmdlet waits for the copy to finish.</span></span>
<span data-ttu-id="2c33b-151">이 매개 변수를 지정 하지 않으면이 cmdlet은 결과를 즉시 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c33b-151">If you do not specify this parameter, this cmdlet returns a result immediately.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c33b-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c33b-152">CommonParameters</span></span>
<span data-ttu-id="2c33b-153">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c33b-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c33b-154">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c33b-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c33b-155">입력</span><span class="sxs-lookup"><span data-stu-id="2c33b-155">INPUTS</span></span>

## <span data-ttu-id="2c33b-156">출력</span><span class="sxs-lookup"><span data-stu-id="2c33b-156">OUTPUTS</span></span>

### <span data-ttu-id="2c33b-157">CopyState</span><span class="sxs-lookup"><span data-stu-id="2c33b-157">CopyState</span></span>

## <span data-ttu-id="2c33b-158">상속자</span><span class="sxs-lookup"><span data-stu-id="2c33b-158">NOTES</span></span>

## <span data-ttu-id="2c33b-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2c33b-159">RELATED LINKS</span></span>

[<span data-ttu-id="2c33b-160">시작-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="2c33b-160">Start-AzureStorageBlobCopy</span></span>](./Start-AzureStorageBlobCopy.md)

[<span data-ttu-id="2c33b-161">중지-AzureStorageBlobCopy</span><span class="sxs-lookup"><span data-stu-id="2c33b-161">Stop-AzureStorageBlobCopy</span></span>](./Stop-AzureStorageBlobCopy.md)


