---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 03EC0D20-C737-4B2B-B8D9-71D06A938FAD
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageblob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageBlob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageBlob.md
ms.openlocfilehash: 7d2363f0fc9955ac75444c18da137dcfee345664
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698580"
---
# <span data-ttu-id="eaa59-101">Remove-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="eaa59-101">Remove-AzStorageBlob</span></span>

## <span data-ttu-id="eaa59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eaa59-102">SYNOPSIS</span></span>
<span data-ttu-id="eaa59-103">지정 된 저장소 blob을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="eaa59-103">Removes the specified storage blob.</span></span>

## <span data-ttu-id="eaa59-104">구문과</span><span class="sxs-lookup"><span data-stu-id="eaa59-104">SYNTAX</span></span>

### <span data-ttu-id="eaa59-105">NamePipeline (기본값)</span><span class="sxs-lookup"><span data-stu-id="eaa59-105">NamePipeline (Default)</span></span>
```
Remove-AzStorageBlob [-Blob] <String> [-Container] <String> [-DeleteSnapshot] [-Force] [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eaa59-106">BlobPipeline</span><span class="sxs-lookup"><span data-stu-id="eaa59-106">BlobPipeline</span></span>
```
Remove-AzStorageBlob -CloudBlob <CloudBlob> [-DeleteSnapshot] [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="eaa59-107">ContainerPipeline</span><span class="sxs-lookup"><span data-stu-id="eaa59-107">ContainerPipeline</span></span>
```
Remove-AzStorageBlob -CloudBlobContainer <CloudBlobContainer> [-Blob] <String> [-DeleteSnapshot] [-Force]
 [-PassThru] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="eaa59-108">설명은</span><span class="sxs-lookup"><span data-stu-id="eaa59-108">DESCRIPTION</span></span>
<span data-ttu-id="eaa59-109">**AzStorageBlob** Cmdlet은 Azure의 저장소 계정에서 지정 된 blob을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="eaa59-109">The **Remove-AzStorageBlob** cmdlet removes the specified blob from a storage account in Azure.</span></span>

## <span data-ttu-id="eaa59-110">예제의</span><span class="sxs-lookup"><span data-stu-id="eaa59-110">EXAMPLES</span></span>

### <span data-ttu-id="eaa59-111">예제 1: 이름으로 저장소 blob 제거</span><span class="sxs-lookup"><span data-stu-id="eaa59-111">Example 1: Remove a storage blob by name</span></span>
```
PS C:\>Remove-AzStorageBlob -Container "ContainerName" -Blob "BlobName"
```

<span data-ttu-id="eaa59-112">이 명령은 이름으로 식별 되는 blob을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="eaa59-112">This command removes a blob identified by its name.</span></span>

### <span data-ttu-id="eaa59-113">예제 2: 파이프라인을 사용 하 여 저장소 blob 제거</span><span class="sxs-lookup"><span data-stu-id="eaa59-113">Example 2: Remove a storage blob using the pipeline</span></span>
```
PS C:\>Get-AzStorageBlob -Container "ContainerName" -Blob "BlobName" | Remove-AzStorageBlob
```

<span data-ttu-id="eaa59-114">이 명령은 파이프라인을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="eaa59-114">This command uses the pipeline.</span></span>

### <span data-ttu-id="eaa59-115">예제 3: 파이프라인을 사용 하 여 저장소 blob 제거</span><span class="sxs-lookup"><span data-stu-id="eaa59-115">Example 3: Remove storage blobs using the pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -Container container* | Remove-AzStorageBlob -Blob "BlobName"
```

<span data-ttu-id="eaa59-116">이 명령은 별표 (\*) 와일드 카드 문자 및 파이프라인을 사용 하 여 blob 또는 blob을 검색 한 다음 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="eaa59-116">This command uses the asterisk (\*) wildcard character and the pipeline to retrieve the blob or blobs and then removes them.</span></span>

## <span data-ttu-id="eaa59-117">변수</span><span class="sxs-lookup"><span data-stu-id="eaa59-117">PARAMETERS</span></span>

### <span data-ttu-id="eaa59-118">-Blob</span><span class="sxs-lookup"><span data-stu-id="eaa59-118">-Blob</span></span>
<span data-ttu-id="eaa59-119">제거 하려는 blob의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eaa59-119">Specifies the name of the blob you want to remove.</span></span>

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

### <span data-ttu-id="eaa59-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="eaa59-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="eaa59-121">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eaa59-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="eaa59-122">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="eaa59-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="eaa59-123">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="eaa59-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="eaa59-124">-CloudBlob</span><span class="sxs-lookup"><span data-stu-id="eaa59-124">-CloudBlob</span></span>
<span data-ttu-id="eaa59-125">클라우드 blob을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eaa59-125">Specifies a cloud blob.</span></span>
<span data-ttu-id="eaa59-126">**CloudBlob** 개체를 가져오려면 Get-AzStorageBlob cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="eaa59-126">To obtain a **CloudBlob** object, use the Get-AzStorageBlob cmdlet.</span></span>

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

### <span data-ttu-id="eaa59-127">-CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="eaa59-127">-CloudBlobContainer</span></span>
<span data-ttu-id="eaa59-128">Azure Storage 클라이언트 라이브러리에서 **CloudBlobContainer** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eaa59-128">Specifies a **CloudBlobContainer** object from the Azure Storage Client library.</span></span>
<span data-ttu-id="eaa59-129">Get-AzStorageContainer cmdlet을 사용 하 여 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eaa59-129">You can use the Get-AzStorageContainer cmdlet to get it.</span></span>

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

### <span data-ttu-id="eaa59-130">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="eaa59-130">-ConcurrentTaskCount</span></span>
<span data-ttu-id="eaa59-131">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eaa59-131">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="eaa59-132">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eaa59-132">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="eaa59-133">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="eaa59-133">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="eaa59-134">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eaa59-134">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="eaa59-135">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="eaa59-135">The default value is 10.</span></span>

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

### <span data-ttu-id="eaa59-136">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="eaa59-136">-Container</span></span>
<span data-ttu-id="eaa59-137">컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eaa59-137">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="eaa59-138">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="eaa59-138">-Context</span></span>
<span data-ttu-id="eaa59-139">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eaa59-139">Specifies the Azure storage context.</span></span>
<span data-ttu-id="eaa59-140">New-AzStorageContext cmdlet을 사용 하 여 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eaa59-140">You can use the New-AzStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="eaa59-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaa59-141">-DefaultProfile</span></span>
<span data-ttu-id="eaa59-142">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="eaa59-142">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eaa59-143">-DeleteSnapshot</span><span class="sxs-lookup"><span data-stu-id="eaa59-143">-DeleteSnapshot</span></span>
<span data-ttu-id="eaa59-144">기본 blob이 아닌 모든 스냅숏을 삭제 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eaa59-144">Specifies that all snapshots be deleted, but not the base blob.</span></span>
<span data-ttu-id="eaa59-145">이 매개 변수를 지정 하지 않으면 기본 blob 및 해당 스냅샷이 함께 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eaa59-145">If this parameter is not specified, the base blob and its snapshots are deleted together.</span></span>
<span data-ttu-id="eaa59-146">사용자에 게 삭제 작업을 확인 하는 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="eaa59-146">The user is prompted to confirm the delete operation.</span></span>

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

### <span data-ttu-id="eaa59-147">-Force</span><span class="sxs-lookup"><span data-stu-id="eaa59-147">-Force</span></span>
<span data-ttu-id="eaa59-148">이 cmdlet이 확인 없이 blob 및 해당 스냅샷을 제거 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="eaa59-148">Indicates that this cmdlet removes the blob and its snapshot without confirmation.</span></span>

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

### <span data-ttu-id="eaa59-149">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eaa59-149">-PassThru</span></span>
<span data-ttu-id="eaa59-150">이 cmdlet이 작업의 성공 여부를 반영 하는 **Boolean** 을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="eaa59-150">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="eaa59-151">기본적으로이 cmdlet은 값을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eaa59-151">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="eaa59-152">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="eaa59-152">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="eaa59-153">읽을 cmdlet에 대 한 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eaa59-153">Specifies the Azure profile for the cmdlet to read.</span></span>
<span data-ttu-id="eaa59-154">지정 하지 않으면 cmdlet은 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="eaa59-154">If not specified, the cmdlet reads from the default profile.</span></span>

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

### <span data-ttu-id="eaa59-155">-확인</span><span class="sxs-lookup"><span data-stu-id="eaa59-155">-Confirm</span></span>
<span data-ttu-id="eaa59-156">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="eaa59-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eaa59-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eaa59-157">-WhatIf</span></span>
<span data-ttu-id="eaa59-158">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="eaa59-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eaa59-159">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eaa59-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eaa59-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaa59-160">CommonParameters</span></span>
<span data-ttu-id="eaa59-161">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="eaa59-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaa59-162">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eaa59-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaa59-163">입력</span><span class="sxs-lookup"><span data-stu-id="eaa59-163">INPUTS</span></span>

### <span data-ttu-id="eaa59-164">WindowsAzure. CloudBlob</span><span class="sxs-lookup"><span data-stu-id="eaa59-164">Microsoft.WindowsAzure.Storage.Blob.CloudBlob</span></span>

### <span data-ttu-id="eaa59-165">WindowsAzure. CloudBlobContainer</span><span class="sxs-lookup"><span data-stu-id="eaa59-165">Microsoft.WindowsAzure.Storage.Blob.CloudBlobContainer</span></span>

### <span data-ttu-id="eaa59-166">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="eaa59-166">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="eaa59-167">출력</span><span class="sxs-lookup"><span data-stu-id="eaa59-167">OUTPUTS</span></span>

### <span data-ttu-id="eaa59-168">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="eaa59-168">System.Boolean</span></span>

## <span data-ttu-id="eaa59-169">상속자</span><span class="sxs-lookup"><span data-stu-id="eaa59-169">NOTES</span></span>

## <span data-ttu-id="eaa59-170">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eaa59-170">RELATED LINKS</span></span>

[<span data-ttu-id="eaa59-171">Get-AzStorageBlob</span><span class="sxs-lookup"><span data-stu-id="eaa59-171">Get-AzStorageBlob</span></span>](./Get-AzStorageBlob.md)

[<span data-ttu-id="eaa59-172">Get-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="eaa59-172">Get-AzStorageBlobContent</span></span>](./Get-AzStorageBlobContent.md)

[<span data-ttu-id="eaa59-173">Set-AzStorageBlobContent</span><span class="sxs-lookup"><span data-stu-id="eaa59-173">Set-AzStorageBlobContent</span></span>](./Set-AzStorageBlobContent.md)