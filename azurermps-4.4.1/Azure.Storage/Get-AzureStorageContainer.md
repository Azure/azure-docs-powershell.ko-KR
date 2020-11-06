---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 90C3DF13-0010-49B6-A8CD-C6AC34BC3EFA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageContainer.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: c94c9b9d04745fe22c8836be1858c59c253d4b63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533240"
---
# <span data-ttu-id="660ce-101">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="660ce-101">Get-AzureStorageContainer</span></span>

## <span data-ttu-id="660ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="660ce-102">SYNOPSIS</span></span>
<span data-ttu-id="660ce-103">저장소 컨테이너를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="660ce-103">Lists the storage containers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="660ce-104">구문과</span><span class="sxs-lookup"><span data-stu-id="660ce-104">SYNTAX</span></span>

### <span data-ttu-id="660ce-105">ContainerName (기본값)</span><span class="sxs-lookup"><span data-stu-id="660ce-105">ContainerName (Default)</span></span>
```
Get-AzureStorageContainer [[-Name] <String>] [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="660ce-106">ContainerPrefix</span><span class="sxs-lookup"><span data-stu-id="660ce-106">ContainerPrefix</span></span>
```
Get-AzureStorageContainer -Prefix <String> [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="660ce-107">설명은</span><span class="sxs-lookup"><span data-stu-id="660ce-107">DESCRIPTION</span></span>
<span data-ttu-id="660ce-108">**AzureStorageContainer** Cmdlet은 Azure의 저장소 계정과 연결 된 저장소 컨테이너를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="660ce-108">The **Get-AzureStorageContainer** cmdlet lists the storage containers associated with the storage account in Azure.</span></span>

## <span data-ttu-id="660ce-109">예제의</span><span class="sxs-lookup"><span data-stu-id="660ce-109">EXAMPLES</span></span>

### <span data-ttu-id="660ce-110">예제 1: 이름별로 Azure Storage blob 가져오기</span><span class="sxs-lookup"><span data-stu-id="660ce-110">Example 1: Get Azure Storage blob by name</span></span>
```
PS C:\>Get-AzureStorageContainer -Name container*
```

<span data-ttu-id="660ce-111">이 예제에서는 와일드 카드 문자를 사용 하 여 container로 시작 하는 이름의 모든 컨테이너 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="660ce-111">This example uses a wildcard character to return a list of all containers with a name that starts with container.</span></span>

### <span data-ttu-id="660ce-112">예제 2: 컨테이너 이름 접두사를 기준으로 Azure Storage 컨테이너 가져오기</span><span class="sxs-lookup"><span data-stu-id="660ce-112">Example 2: Get Azure Storage container by container name prefix</span></span>
```
PS C:\>Get-AzureStorageContainer -Prefix "container"
```

<span data-ttu-id="660ce-113">이 예제에서는 *Prefix* 매개 변수를 사용 하 여 container로 시작 하는 이름의 모든 컨테이너 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="660ce-113">This example uses the *Prefix* parameter to return a list of all containers with a name that starts with container.</span></span>

## <span data-ttu-id="660ce-114">변수</span><span class="sxs-lookup"><span data-stu-id="660ce-114">PARAMETERS</span></span>

### <span data-ttu-id="660ce-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="660ce-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="660ce-116">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="660ce-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="660ce-117">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="660ce-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="660ce-118">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="660ce-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="660ce-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="660ce-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="660ce-120">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="660ce-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="660ce-121">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="660ce-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="660ce-122">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="660ce-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="660ce-123">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="660ce-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="660ce-124">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="660ce-124">The default value is 10.</span></span>

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

### <span data-ttu-id="660ce-125">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="660ce-125">-Context</span></span>
<span data-ttu-id="660ce-126">저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="660ce-126">Specifies the storage context.</span></span>
<span data-ttu-id="660ce-127">이를 만들기 위해 New-AzureStorageContext cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="660ce-127">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="660ce-128">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="660ce-128">-ContinuationToken</span></span>
<span data-ttu-id="660ce-129">Blob 목록에 대 한 연속 토큰을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="660ce-129">Specifies a continuation token for the blob list.</span></span>

```yaml
Type: BlobContinuationToken
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="660ce-130">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="660ce-130">-MaxCount</span></span>
<span data-ttu-id="660ce-131">이 cmdlet이 반환 하는 최대 개체 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="660ce-131">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="660ce-132">-이름</span><span class="sxs-lookup"><span data-stu-id="660ce-132">-Name</span></span>
<span data-ttu-id="660ce-133">컨테이너 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="660ce-133">Specifies the container name.</span></span>
<span data-ttu-id="660ce-134">컨테이너 이름이 비어 있으면 cmdlet에 모든 컨테이너가 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="660ce-134">If container name is empty, the cmdlet lists all the containers.</span></span>
<span data-ttu-id="660ce-135">그렇지 않으면 지정 된 이름 또는 일반 이름 패턴과 일치 하는 모든 컨테이너가 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="660ce-135">Otherwise, it lists all containers that match the specified name or the regular name pattern.</span></span>

```yaml
Type: String
Parameter Sets: ContainerName
Aliases: N, Container

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: True
```

### <span data-ttu-id="660ce-136">-접두사</span><span class="sxs-lookup"><span data-stu-id="660ce-136">-Prefix</span></span>
<span data-ttu-id="660ce-137">가져오려는 컨테이너의 이름에 사용 되는 접두사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="660ce-137">Specifies a prefix used in the name of the container or containers you want to get.</span></span>
<span data-ttu-id="660ce-138">이를 사용 하 여 "my" 또는 "test"와 같이 같은 문자열로 시작 하는 모든 컨테이너를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="660ce-138">You can use this to find all containers that start with the same string, such as "my" or "test".</span></span>

```yaml
Type: String
Parameter Sets: ContainerPrefix
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="660ce-139">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="660ce-139">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="660ce-140">요청에 대 한 서비스 측 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="660ce-140">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="660ce-141">서비스가 요청을 처리 하기 전에 지정 된 간격이 경과 하면 저장소 서비스에서 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="660ce-141">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="660ce-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="660ce-142">CommonParameters</span></span>
<span data-ttu-id="660ce-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="660ce-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="660ce-144">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="660ce-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="660ce-145">입력</span><span class="sxs-lookup"><span data-stu-id="660ce-145">INPUTS</span></span>

### <span data-ttu-id="660ce-146">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="660ce-146">IStorageContext</span></span>

<span data-ttu-id="660ce-147">' Context ' 매개 변수는 파이프라인에서 ' IStorageContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="660ce-147">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="660ce-148">이름</span><span class="sxs-lookup"><span data-stu-id="660ce-148">String</span></span>

<span data-ttu-id="660ce-149">' Name ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="660ce-149">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="660ce-150">출력</span><span class="sxs-lookup"><span data-stu-id="660ce-150">OUTPUTS</span></span>

### <span data-ttu-id="660ce-151">WindowsAzure. ResourceModel를 AzureStorageContainer로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="660ce-151">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="660ce-152">상속자</span><span class="sxs-lookup"><span data-stu-id="660ce-152">NOTES</span></span>

## <span data-ttu-id="660ce-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="660ce-153">RELATED LINKS</span></span>

[<span data-ttu-id="660ce-154">새로운 AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="660ce-154">New-AzureStorageContainer</span></span>](./New-AzureStorageContainer.md)

[<span data-ttu-id="660ce-155">제거-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="660ce-155">Remove-AzureStorageContainer</span></span>](./Remove-AzureStorageContainer.md)

[<span data-ttu-id="660ce-156">Set-AzureStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="660ce-156">Set-AzureStorageContainerAcl</span></span>](./Set-AzureStorageContainerAcl.md)


