---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 03EC0D20-C737-4B2B-B8D9-71D06A938FAD
online version: ''
schema: 2.0.0
ms.openlocfilehash: b40585f584cc8c2634acab54e6862e4163c6b7a7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523744"
---
# <span data-ttu-id="37d36-101">Remove-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="37d36-101">Remove-AzureStorageBlob</span></span>

## <span data-ttu-id="37d36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37d36-102">SYNOPSIS</span></span>
<span data-ttu-id="37d36-103">지정 된 저장소 blob을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="37d36-103">Removes the specified storage blob.</span></span>

## <span data-ttu-id="37d36-104">구문과</span><span class="sxs-lookup"><span data-stu-id="37d36-104">SYNTAX</span></span>

### <span data-ttu-id="37d36-105">NamePipeline (기본값)</span><span class="sxs-lookup"><span data-stu-id="37d36-105">NamePipeline (Default)</span></span>
```
Remove-AzureStorageBlob [-Blob] <String> [-Container] <String> [-DeleteSnapshot] [-Force] [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37d36-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="37d36-106">BlobPipeline</span></span>
```
Remove-AzureStorageBlob -CloudBlob <CloudBlob> [-DeleteSnapshot] [-Force] [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37d36-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="37d36-107">ContainerPipeline</span></span>
```
Remove-AzureStorageBlob -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-DeleteSnapshot] [-Force]
 [-PassThru] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37d36-108">설명은</span><span class="sxs-lookup"><span data-stu-id="37d36-108">DESCRIPTION</span></span>
<span data-ttu-id="37d36-109">**제거-AzureStorageBlob** Cmdlet은 Azure의 저장소 계정에서 지정 된 blob을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="37d36-109">The **Remove-AzureStorageBlob** cmdlet removes the specified blob from a storage account in Azure.</span></span>

## <span data-ttu-id="37d36-110">예제의</span><span class="sxs-lookup"><span data-stu-id="37d36-110">EXAMPLES</span></span>

### <span data-ttu-id="37d36-111">예제 1: 이름으로 저장소 blob 제거</span><span class="sxs-lookup"><span data-stu-id="37d36-111">Example 1: Remove a storage blob by name</span></span>
```
PS C:\>Remove-AzureStorageBlob -Container "ContainerName" -Blob "BlobName"
```

<span data-ttu-id="37d36-112">이 명령은 이름으로 식별 되는 blob을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="37d36-112">This command removes a blob identified by its name.</span></span>

### <span data-ttu-id="37d36-113">예제 2: 파이프라인을 사용 하 여 저장소 blob 제거</span><span class="sxs-lookup"><span data-stu-id="37d36-113">Example 2: Remove a storage blob using the pipeline</span></span>
```
PS C:\>Get-AzureStorageBlob -Container "ContainerName" -Blob "BlobName" | Remove-AzureStorageBlob
```

<span data-ttu-id="37d36-114">이 명령은 파이프라인을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="37d36-114">This command uses the pipeline.</span></span>

### <span data-ttu-id="37d36-115">예제 3: 파이프라인을 사용 하 여 저장소 blob 제거</span><span class="sxs-lookup"><span data-stu-id="37d36-115">Example 3: Remove storage blobs using the pipeline</span></span>
```
PS C:\>Get-AzureStorageContainer -Container container* | Remove-AzureStorageBlob -Blob "BlobName"
```

<span data-ttu-id="37d36-116">이 명령은 별표 (\*) 와일드 카드 문자 및 파이프라인을 사용 하 여 blob 또는 blob을 검색 한 다음 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="37d36-116">This command uses the asterisk (\*) wildcard character and the pipeline to retrieve the blob or blobs and then removes them.</span></span>

## <span data-ttu-id="37d36-117">변수</span><span class="sxs-lookup"><span data-stu-id="37d36-117">PARAMETERS</span></span>

### <span data-ttu-id="37d36-118">-Blob</span><span class="sxs-lookup"><span data-stu-id="37d36-118">-Blob</span></span>
<span data-ttu-id="37d36-119">제거 하려는 blob의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37d36-119">Specifies the name of the blob you want to remove.</span></span>

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

### <span data-ttu-id="37d36-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="37d36-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="37d36-121">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37d36-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="37d36-122">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="37d36-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="37d36-123">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="37d36-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="37d36-124">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="37d36-124">-CloudBlob</span></span>
<span data-ttu-id="37d36-125">클라우드 blob을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37d36-125">Specifies a cloud blob.</span></span>
<span data-ttu-id="37d36-126">**CloudBlob** 개체를 가져오려면 Get-AzureStorageBlob cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="37d36-126">To obtain a **CloudBlob** object, use the Get-AzureStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="37d36-127">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="37d36-127">-CloudBlobContainer</span></span>
<span data-ttu-id="37d36-128">Azure Storage 클라이언트 라이브러리에서 **CloudBlobContainer** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37d36-128">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="37d36-129">Get-AzureStorageContainer cmdlet을 사용 하 여 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37d36-129">You can use the Get-AzureStorageContainer cmdlet to get it.</span></span>

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

### <span data-ttu-id="37d36-130">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="37d36-130">-ConcurrentTaskCount</span></span>
<span data-ttu-id="37d36-131">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37d36-131">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="37d36-132">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37d36-132">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="37d36-133">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="37d36-133">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="37d36-134">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37d36-134">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="37d36-135">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="37d36-135">The default value is 10.</span></span>

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

### <span data-ttu-id="37d36-136">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="37d36-136">-Container</span></span>
<span data-ttu-id="37d36-137">컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37d36-137">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="37d36-138">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="37d36-138">-Context</span></span>
<span data-ttu-id="37d36-139">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37d36-139">Specifies the Azure storage context.</span></span>
<span data-ttu-id="37d36-140">New-AzureStorageContext cmdlet을 사용 하 여 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="37d36-140">You can use the New-AzureStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="37d36-141">-DeleteSnapshot</span><span class="sxs-lookup"><span data-stu-id="37d36-141">-DeleteSnapshot</span></span>
<span data-ttu-id="37d36-142">기본 blob이 아닌 모든 스냅숏을 삭제 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37d36-142">Specifies that all snapshots be deleted, but not the base blob.</span></span>
<span data-ttu-id="37d36-143">이 매개 변수를 지정 하지 않으면 기본 blob 및 해당 스냅샷이 함께 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="37d36-143">If this parameter is not specified, the base blob and its snapshots are deleted together.</span></span>
<span data-ttu-id="37d36-144">사용자에 게 삭제 작업을 확인 하는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="37d36-144">The user is prompted to confirm the delete operation.</span></span>

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

### <span data-ttu-id="37d36-145">-Force</span><span class="sxs-lookup"><span data-stu-id="37d36-145">-Force</span></span>
<span data-ttu-id="37d36-146">이 cmdlet이 확인 없이 blob 및 해당 스냅샷을 제거 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="37d36-146">Indicates that this cmdlet removes the blob and its snapshot without confirmation.</span></span>

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

### <span data-ttu-id="37d36-147">-PassThru</span><span class="sxs-lookup"><span data-stu-id="37d36-147">-PassThru</span></span>
<span data-ttu-id="37d36-148">이 cmdlet이 작업의 성공 여부를 반영 하는 **Boolean** 을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="37d36-148">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="37d36-149">기본적으로이 cmdlet은 값을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="37d36-149">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="37d36-150">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="37d36-150">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="37d36-151">읽을 cmdlet에 대 한 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="37d36-151">Specifies the Azure profile for the cmdlet to read.</span></span>
<span data-ttu-id="37d36-152">지정 하지 않으면 cmdlet은 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="37d36-152">If not specified, the cmdlet reads from the default profile.</span></span>

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

### <span data-ttu-id="37d36-153">-확인</span><span class="sxs-lookup"><span data-stu-id="37d36-153">-Confirm</span></span>
<span data-ttu-id="37d36-154">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="37d36-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37d36-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37d36-155">-WhatIf</span></span>
<span data-ttu-id="37d36-156">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="37d36-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37d36-157">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="37d36-157">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37d36-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37d36-158">CommonParameters</span></span>
<span data-ttu-id="37d36-159">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="37d36-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37d36-160">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37d36-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37d36-161">입력</span><span class="sxs-lookup"><span data-stu-id="37d36-161">INPUTS</span></span>

## <span data-ttu-id="37d36-162">출력</span><span class="sxs-lookup"><span data-stu-id="37d36-162">OUTPUTS</span></span>

## <span data-ttu-id="37d36-163">상속자</span><span class="sxs-lookup"><span data-stu-id="37d36-163">NOTES</span></span>

## <span data-ttu-id="37d36-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="37d36-164">RELATED LINKS</span></span>

[<span data-ttu-id="37d36-165">Get-AzureStorageBlob</span><span class="sxs-lookup"><span data-stu-id="37d36-165">Get-AzureStorageBlob</span></span>](./Get-AzureStorageBlob.md)

[<span data-ttu-id="37d36-166">가져오기-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="37d36-166">Get-AzureStorageBlobContent</span></span>](./Get-AzureStorageBlobContent.md)

[<span data-ttu-id="37d36-167">Set-AzureStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="37d36-167">Set-AzureStorageBlobContent</span></span>](./Set-AzureStorageBlobContent.md)