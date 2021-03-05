---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 90C3DF13-0010-49B6-A8CD-C6AC34BC3EFA
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainer.md
ms.openlocfilehash: 15aefebea30e829371c57c3c1cd575a604b81eaf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981531"
---
# <span data-ttu-id="9b3bd-101">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="9b3bd-101">Get-AzStorageContainer</span></span>

## <span data-ttu-id="9b3bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b3bd-102">SYNOPSIS</span></span>
<span data-ttu-id="9b3bd-103">저장소 컨테이너를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="9b3bd-103">Lists the storage containers.</span></span>

## <span data-ttu-id="9b3bd-104">구문</span><span class="sxs-lookup"><span data-stu-id="9b3bd-104">SYNTAX</span></span>

### <span data-ttu-id="9b3bd-105">ContainerName(기본값)</span><span class="sxs-lookup"><span data-stu-id="9b3bd-105">ContainerName (Default)</span></span>
```
Get-AzStorageContainer [[-Name] <String>] [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="9b3bd-106">ContainerPrefix</span><span class="sxs-lookup"><span data-stu-id="9b3bd-106">ContainerPrefix</span></span>
```
Get-AzStorageContainer -Prefix <String> [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="9b3bd-107">설명</span><span class="sxs-lookup"><span data-stu-id="9b3bd-107">DESCRIPTION</span></span>
<span data-ttu-id="9b3bd-108">**Get-AzStorageContainer** cmdlet에는 Azure의 저장소 계정과 연결된 저장소 컨테이너가 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b3bd-108">The **Get-AzStorageContainer** cmdlet lists the storage containers associated with the storage account in Azure.</span></span>

## <span data-ttu-id="9b3bd-109">예제</span><span class="sxs-lookup"><span data-stu-id="9b3bd-109">EXAMPLES</span></span>

### <span data-ttu-id="9b3bd-110">예제 1: 이름에 의해 Azure Storage Blob을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b3bd-110">Example 1: Get Azure Storage blob by name</span></span>
```
PS C:\>Get-AzStorageContainer -Name container*
```

<span data-ttu-id="9b3bd-111">이 예제에서는 와일드카드 문자를 사용하여 컨테이너로 시작하는 이름이 있는 모든 컨테이너 목록을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="9b3bd-111">This example uses a wildcard character to return a list of all containers with a name that starts with container.</span></span>

### <span data-ttu-id="9b3bd-112">예제 2: 컨테이너 이름에 의해 Azure Storage 컨테이너를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9b3bd-112">Example 2: Get Azure Storage container by container name prefix</span></span>
```
PS C:\>Get-AzStorageContainer -Prefix "container"
```

<span data-ttu-id="9b3bd-113">이 예제에서는 *Prefix* 매개 변수를 사용하여 컨테이너로 시작하는 이름이 있는 모든 컨테이너 목록을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="9b3bd-113">This example uses the *Prefix* parameter to return a list of all containers with a name that starts with container.</span></span>

## <span data-ttu-id="9b3bd-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="9b3bd-114">PARAMETERS</span></span>

### <span data-ttu-id="9b3bd-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9b3bd-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="9b3bd-116">하나의 서비스 요청에 대해 클라이언트 쪽 시간 간격(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9b3bd-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="9b3bd-117">지정된 간격에서 이전 호출이 실패하면 이 cmdlet에서 요청을 다시 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="9b3bd-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="9b3bd-118">간격이 경과하기 전에 이 cmdlet에서 성공적인 응답을 받지 못하면 이 cmdlet은 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="9b3bd-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="9b3bd-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="9b3bd-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="9b3bd-120">최대 동시 네트워크 호출을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9b3bd-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="9b3bd-121">이 매개 변수를 사용하여 최대 동시 네트워크 호출 수를 지정하여 로컬 CPU 및 대역폭 사용량을 제한하는 동시성 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b3bd-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="9b3bd-122">지정된 값은 절대 개수로 코어 수에 곱하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9b3bd-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="9b3bd-123">이 매개 변수는 초당 100킬로비트와 같은 대역폭이 낮은 환경에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b3bd-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="9b3bd-124">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="9b3bd-124">The default value is 10.</span></span>

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

### <span data-ttu-id="9b3bd-125">-Context</span><span class="sxs-lookup"><span data-stu-id="9b3bd-125">-Context</span></span>
<span data-ttu-id="9b3bd-126">저장소 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9b3bd-126">Specifies the storage context.</span></span>
<span data-ttu-id="9b3bd-127">만들기 위해 New-AzStorageContext cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b3bd-127">To create it, you can use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="9b3bd-128">쿼리 컨테이너 사용 권한에는 Storage 계정 키 권한이 필요하기 때문에 SAS 토큰에서 만든 저장소 컨텍스트를 사용할 때 컨테이너 사용 권한이 검색되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9b3bd-128">The container permissions won't be retrieved when you use a storage context created from SAS Token, because query container permissions requires Storage account key permission.</span></span>

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

### <span data-ttu-id="9b3bd-129">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="9b3bd-129">-ContinuationToken</span></span>
<span data-ttu-id="9b3bd-130">Blob 목록에 대한 연속 토큰을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9b3bd-130">Specifies a continuation token for the blob list.</span></span>

```yaml
Type: Microsoft.Azure.Storage.Blob.BlobContinuationToken
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b3bd-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b3bd-131">-DefaultProfile</span></span>
<span data-ttu-id="9b3bd-132">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9b3bd-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b3bd-133">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="9b3bd-133">-MaxCount</span></span>
<span data-ttu-id="9b3bd-134">이 cmdlet이 반환하는 최대 개체 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9b3bd-134">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="9b3bd-135">-Name</span><span class="sxs-lookup"><span data-stu-id="9b3bd-135">-Name</span></span>
<span data-ttu-id="9b3bd-136">컨테이너 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9b3bd-136">Specifies the container name.</span></span>
<span data-ttu-id="9b3bd-137">컨테이너 이름이 비어 있는 경우 cmdlet에는 모든 컨테이너가 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b3bd-137">If container name is empty, the cmdlet lists all the containers.</span></span>
<span data-ttu-id="9b3bd-138">그렇지 않으면 지정된 이름 또는 일반 이름 패턴과 일치하는 모든 컨테이너가 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="9b3bd-138">Otherwise, it lists all containers that match the specified name or the regular name pattern.</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerName
Aliases: N, Container

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9b3bd-139">-Prefix</span><span class="sxs-lookup"><span data-stu-id="9b3bd-139">-Prefix</span></span>
<span data-ttu-id="9b3bd-140">얻을 컨테이너 또는 컨테이너의 이름에 사용되는 도두를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9b3bd-140">Specifies a prefix used in the name of the container or containers you want to get.</span></span>
<span data-ttu-id="9b3bd-141">이 기능을 사용하여 "my" 또는 "test"와 같은 동일한 문자열로 시작하는 모든 컨테이너를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9b3bd-141">You can use this to find all containers that start with the same string, such as "my" or "test".</span></span>

```yaml
Type: System.String
Parameter Sets: ContainerPrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b3bd-142">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="9b3bd-142">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="9b3bd-143">요청에 대해 서비스 쪽 시간 시간 간격(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="9b3bd-143">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="9b3bd-144">서비스가 요청을 처리하기 전에 지정된 간격이 경과하면 저장소 서비스가 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="9b3bd-144">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="9b3bd-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b3bd-145">CommonParameters</span></span>
<span data-ttu-id="9b3bd-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9b3bd-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b3bd-147">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9b3bd-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b3bd-148">입력</span><span class="sxs-lookup"><span data-stu-id="9b3bd-148">INPUTS</span></span>

### <span data-ttu-id="9b3bd-149">System.String</span><span class="sxs-lookup"><span data-stu-id="9b3bd-149">System.String</span></span>

### <span data-ttu-id="9b3bd-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="9b3bd-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="9b3bd-151">출력</span><span class="sxs-lookup"><span data-stu-id="9b3bd-151">OUTPUTS</span></span>

### <span data-ttu-id="9b3bd-152">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="9b3bd-152">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="9b3bd-153">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9b3bd-153">NOTES</span></span>

## <span data-ttu-id="9b3bd-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9b3bd-154">RELATED LINKS</span></span>

[<span data-ttu-id="9b3bd-155">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="9b3bd-155">New-AzStorageContainer</span></span>](./New-AzStorageContainer.md)

[<span data-ttu-id="9b3bd-156">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="9b3bd-156">Remove-AzStorageContainer</span></span>](./Remove-AzStorageContainer.md)

[<span data-ttu-id="9b3bd-157">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="9b3bd-157">Set-AzStorageContainerAcl</span></span>](./Set-AzStorageContainerAcl.md)


