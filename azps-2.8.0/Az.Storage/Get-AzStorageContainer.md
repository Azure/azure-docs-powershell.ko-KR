---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 90C3DF13-0010-49B6-A8CD-C6AC34BC3EFA
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainer.md
ms.openlocfilehash: afc96a48cb63e8493041b70e7450b3a2385344fd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93874129"
---
# <span data-ttu-id="88739-101">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="88739-101">Get-AzStorageContainer</span></span>

## <span data-ttu-id="88739-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88739-102">SYNOPSIS</span></span>
<span data-ttu-id="88739-103">저장소 컨테이너를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="88739-103">Lists the storage containers.</span></span>

## <span data-ttu-id="88739-104">구문과</span><span class="sxs-lookup"><span data-stu-id="88739-104">SYNTAX</span></span>

### <span data-ttu-id="88739-105">ContainerName (기본값)</span><span class="sxs-lookup"><span data-stu-id="88739-105">ContainerName (Default)</span></span>
```
Get-AzStorageContainer [[-Name] <String>] [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="88739-106">ContainerPrefix</span><span class="sxs-lookup"><span data-stu-id="88739-106">ContainerPrefix</span></span>
```
Get-AzStorageContainer -Prefix <String> [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="88739-107">설명은</span><span class="sxs-lookup"><span data-stu-id="88739-107">DESCRIPTION</span></span>
<span data-ttu-id="88739-108">**AzStorageContainer** Cmdlet은 Azure의 저장소 계정과 연결 된 저장소 컨테이너를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="88739-108">The **Get-AzStorageContainer** cmdlet lists the storage containers associated with the storage account in Azure.</span></span>

## <span data-ttu-id="88739-109">예제의</span><span class="sxs-lookup"><span data-stu-id="88739-109">EXAMPLES</span></span>

### <span data-ttu-id="88739-110">예제 1: 이름별로 Azure Storage blob 가져오기</span><span class="sxs-lookup"><span data-stu-id="88739-110">Example 1: Get Azure Storage blob by name</span></span>
```
PS C:\>Get-AzStorageContainer -Name container*
```

<span data-ttu-id="88739-111">이 예제에서는 와일드 카드 문자를 사용 하 여 container로 시작 하는 이름의 모든 컨테이너 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="88739-111">This example uses a wildcard character to return a list of all containers with a name that starts with container.</span></span>

### <span data-ttu-id="88739-112">예제 2: 컨테이너 이름 접두사를 기준으로 Azure Storage 컨테이너 가져오기</span><span class="sxs-lookup"><span data-stu-id="88739-112">Example 2: Get Azure Storage container by container name prefix</span></span>
```
PS C:\>Get-AzStorageContainer -Prefix "container"
```

<span data-ttu-id="88739-113">이 예제에서는 *Prefix* 매개 변수를 사용 하 여 container로 시작 하는 이름의 모든 컨테이너 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="88739-113">This example uses the *Prefix* parameter to return a list of all containers with a name that starts with container.</span></span>

## <span data-ttu-id="88739-114">변수</span><span class="sxs-lookup"><span data-stu-id="88739-114">PARAMETERS</span></span>

### <span data-ttu-id="88739-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="88739-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="88739-116">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88739-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="88739-117">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="88739-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="88739-118">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="88739-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="88739-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="88739-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="88739-120">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88739-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="88739-121">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="88739-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="88739-122">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="88739-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="88739-123">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="88739-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="88739-124">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="88739-124">The default value is 10.</span></span>

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

### <span data-ttu-id="88739-125">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="88739-125">-Context</span></span>
<span data-ttu-id="88739-126">저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88739-126">Specifies the storage context.</span></span>
<span data-ttu-id="88739-127">이를 만들기 위해 New-AzStorageContext cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="88739-127">To create it, you can use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="88739-128">쿼리 컨테이너 사용 권한에 저장소 계정 키 권한이 필요 하기 때문에 SAS 토큰에서 만든 저장소 컨텍스트를 사용 하는 경우 컨테이너 사용 권한이 검색 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="88739-128">The container permissions won't be retrieved when you use a storage context created from SAS Token, because query container permissions requires Storage account key permission.</span></span>

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

### <span data-ttu-id="88739-129">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="88739-129">-ContinuationToken</span></span>
<span data-ttu-id="88739-130">Blob 목록에 대 한 연속 토큰을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88739-130">Specifies a continuation token for the blob list.</span></span>

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

### <span data-ttu-id="88739-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88739-131">-DefaultProfile</span></span>
<span data-ttu-id="88739-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="88739-132">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88739-133">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="88739-133">-MaxCount</span></span>
<span data-ttu-id="88739-134">이 cmdlet이 반환 하는 최대 개체 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88739-134">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="88739-135">-이름</span><span class="sxs-lookup"><span data-stu-id="88739-135">-Name</span></span>
<span data-ttu-id="88739-136">컨테이너 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88739-136">Specifies the container name.</span></span>
<span data-ttu-id="88739-137">컨테이너 이름이 비어 있으면 cmdlet에 모든 컨테이너가 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="88739-137">If container name is empty, the cmdlet lists all the containers.</span></span>
<span data-ttu-id="88739-138">그렇지 않으면 지정 된 이름 또는 일반 이름 패턴과 일치 하는 모든 컨테이너가 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="88739-138">Otherwise, it lists all containers that match the specified name or the regular name pattern.</span></span>

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

### <span data-ttu-id="88739-139">-접두사</span><span class="sxs-lookup"><span data-stu-id="88739-139">-Prefix</span></span>
<span data-ttu-id="88739-140">가져오려는 컨테이너의 이름에 사용 되는 접두사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88739-140">Specifies a prefix used in the name of the container or containers you want to get.</span></span>
<span data-ttu-id="88739-141">이를 사용 하 여 "my" 또는 "test"와 같이 같은 문자열로 시작 하는 모든 컨테이너를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="88739-141">You can use this to find all containers that start with the same string, such as "my" or "test".</span></span>

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

### <span data-ttu-id="88739-142">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="88739-142">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="88739-143">요청에 대 한 서비스 측 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88739-143">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="88739-144">서비스가 요청을 처리 하기 전에 지정 된 간격이 경과 하면 저장소 서비스에서 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="88739-144">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="88739-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88739-145">CommonParameters</span></span>
<span data-ttu-id="88739-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="88739-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88739-147">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88739-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88739-148">입력</span><span class="sxs-lookup"><span data-stu-id="88739-148">INPUTS</span></span>

### <span data-ttu-id="88739-149">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="88739-149">System.String</span></span>

### <span data-ttu-id="88739-150">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="88739-150">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="88739-151">출력</span><span class="sxs-lookup"><span data-stu-id="88739-151">OUTPUTS</span></span>

### <span data-ttu-id="88739-152">WindowsAzure. ResourceModel를 AzureStorageContainer로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="88739-152">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="88739-153">상속자</span><span class="sxs-lookup"><span data-stu-id="88739-153">NOTES</span></span>

## <span data-ttu-id="88739-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="88739-154">RELATED LINKS</span></span>

[<span data-ttu-id="88739-155">새로운 AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="88739-155">New-AzStorageContainer</span></span>](./New-AzStorageContainer.md)

[<span data-ttu-id="88739-156">제거-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="88739-156">Remove-AzStorageContainer</span></span>](./Remove-AzStorageContainer.md)

[<span data-ttu-id="88739-157">Set-AzStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="88739-157">Set-AzStorageContainerAcl</span></span>](./Set-AzStorageContainerAcl.md)


