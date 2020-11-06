---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 90C3DF13-0010-49B6-A8CD-C6AC34BC3EFA
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageContainer.md
ms.openlocfilehash: 45368a3abe428c65604d4ba103cf793972e50ea1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530633"
---
# <span data-ttu-id="817b4-101">Get-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="817b4-101">Get-AzureStorageContainer</span></span>

## <span data-ttu-id="817b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="817b4-102">SYNOPSIS</span></span>
<span data-ttu-id="817b4-103">저장소 컨테이너를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="817b4-103">Lists the storage containers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="817b4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="817b4-104">SYNTAX</span></span>

### <span data-ttu-id="817b4-105">ContainerName (기본값)</span><span class="sxs-lookup"><span data-stu-id="817b4-105">ContainerName (Default)</span></span>
```
Get-AzureStorageContainer [[-Name] <String>] [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="817b4-106">ContainerPrefix</span><span class="sxs-lookup"><span data-stu-id="817b4-106">ContainerPrefix</span></span>
```
Get-AzureStorageContainer -Prefix <String> [-MaxCount <Int32>] [-ContinuationToken <BlobContinuationToken>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="817b4-107">설명은</span><span class="sxs-lookup"><span data-stu-id="817b4-107">DESCRIPTION</span></span>
<span data-ttu-id="817b4-108">**AzureStorageContainer** Cmdlet은 Azure의 저장소 계정과 연결 된 저장소 컨테이너를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="817b4-108">The **Get-AzureStorageContainer** cmdlet lists the storage containers associated with the storage account in Azure.</span></span>

## <span data-ttu-id="817b4-109">예제의</span><span class="sxs-lookup"><span data-stu-id="817b4-109">EXAMPLES</span></span>

### <span data-ttu-id="817b4-110">예제 1: 이름별로 Azure Storage blob 가져오기</span><span class="sxs-lookup"><span data-stu-id="817b4-110">Example 1: Get Azure Storage blob by name</span></span>
```
PS C:\>Get-AzureStorageContainer -Name container*
```

<span data-ttu-id="817b4-111">이 예제에서는 와일드 카드 문자를 사용 하 여 container로 시작 하는 이름의 모든 컨테이너 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="817b4-111">This example uses a wildcard character to return a list of all containers with a name that starts with container.</span></span>

### <span data-ttu-id="817b4-112">예제 2: 컨테이너 이름 접두사를 기준으로 Azure Storage 컨테이너 가져오기</span><span class="sxs-lookup"><span data-stu-id="817b4-112">Example 2: Get Azure Storage container by container name prefix</span></span>
```
PS C:\>Get-AzureStorageContainer -Prefix "container"
```

<span data-ttu-id="817b4-113">이 예제에서는 *Prefix* 매개 변수를 사용 하 여 container로 시작 하는 이름의 모든 컨테이너 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="817b4-113">This example uses the *Prefix* parameter to return a list of all containers with a name that starts with container.</span></span>

## <span data-ttu-id="817b4-114">변수</span><span class="sxs-lookup"><span data-stu-id="817b4-114">PARAMETERS</span></span>

### <span data-ttu-id="817b4-115">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="817b4-115">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="817b4-116">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="817b4-116">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="817b4-117">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="817b4-117">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="817b4-118">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="817b4-118">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="817b4-119">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="817b4-119">-ConcurrentTaskCount</span></span>
<span data-ttu-id="817b4-120">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="817b4-120">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="817b4-121">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="817b4-121">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="817b4-122">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="817b4-122">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="817b4-123">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="817b4-123">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="817b4-124">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="817b4-124">The default value is 10.</span></span>

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

### <span data-ttu-id="817b4-125">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="817b4-125">-Context</span></span>
<span data-ttu-id="817b4-126">저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="817b4-126">Specifies the storage context.</span></span>
<span data-ttu-id="817b4-127">이를 만들기 위해 New-AzureStorageContext cmdlet을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="817b4-127">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>
<span data-ttu-id="817b4-128">Cmdlet이 저장소 계정 키 권한이 필요한 컨테이너 사용 권한을 쿼리 하기 때문에 SAS 토큰에서 생성 된 저장소 컨텍스트를 사용 하는 경우 cmdlet이 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="817b4-128">The cmdlet will fail when you use a storage context created from SAS Token because the cmdlet will query for container permissions which require Storage account key permission.</span></span>

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

### <span data-ttu-id="817b4-129">-ContinuationToken</span><span class="sxs-lookup"><span data-stu-id="817b4-129">-ContinuationToken</span></span>
<span data-ttu-id="817b4-130">Blob 목록에 대 한 연속 토큰을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="817b4-130">Specifies a continuation token for the blob list.</span></span>

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

### <span data-ttu-id="817b4-131">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="817b4-131">-MaxCount</span></span>
<span data-ttu-id="817b4-132">이 cmdlet이 반환 하는 최대 개체 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="817b4-132">Specifies the maximum number of objects that this cmdlet returns.</span></span>

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

### <span data-ttu-id="817b4-133">-이름</span><span class="sxs-lookup"><span data-stu-id="817b4-133">-Name</span></span>
<span data-ttu-id="817b4-134">컨테이너 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="817b4-134">Specifies the container name.</span></span>
<span data-ttu-id="817b4-135">컨테이너 이름이 비어 있으면 cmdlet에 모든 컨테이너가 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="817b4-135">If container name is empty, the cmdlet lists all the containers.</span></span>
<span data-ttu-id="817b4-136">그렇지 않으면 지정 된 이름 또는 일반 이름 패턴과 일치 하는 모든 컨테이너가 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="817b4-136">Otherwise, it lists all containers that match the specified name or the regular name pattern.</span></span>

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

### <span data-ttu-id="817b4-137">-접두사</span><span class="sxs-lookup"><span data-stu-id="817b4-137">-Prefix</span></span>
<span data-ttu-id="817b4-138">가져오려는 컨테이너의 이름에 사용 되는 접두사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="817b4-138">Specifies a prefix used in the name of the container or containers you want to get.</span></span>
<span data-ttu-id="817b4-139">이를 사용 하 여 "my" 또는 "test"와 같이 같은 문자열로 시작 하는 모든 컨테이너를 찾을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="817b4-139">You can use this to find all containers that start with the same string, such as "my" or "test".</span></span>

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

### <span data-ttu-id="817b4-140">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="817b4-140">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="817b4-141">요청에 대 한 서비스 측 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="817b4-141">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="817b4-142">서비스가 요청을 처리 하기 전에 지정 된 간격이 경과 하면 저장소 서비스에서 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="817b4-142">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="817b4-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="817b4-143">CommonParameters</span></span>
<span data-ttu-id="817b4-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="817b4-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="817b4-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="817b4-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="817b4-146">입력</span><span class="sxs-lookup"><span data-stu-id="817b4-146">INPUTS</span></span>

### <span data-ttu-id="817b4-147">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="817b4-147">IStorageContext</span></span>

<span data-ttu-id="817b4-148">' Context ' 매개 변수는 파이프라인에서 ' IStorageContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="817b4-148">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="817b4-149">이름</span><span class="sxs-lookup"><span data-stu-id="817b4-149">String</span></span>

<span data-ttu-id="817b4-150">' Name ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="817b4-150">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="817b4-151">출력</span><span class="sxs-lookup"><span data-stu-id="817b4-151">OUTPUTS</span></span>

### <span data-ttu-id="817b4-152">WindowsAzure. ResourceModel를 AzureStorageContainer로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="817b4-152">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageContainer</span></span>

## <span data-ttu-id="817b4-153">상속자</span><span class="sxs-lookup"><span data-stu-id="817b4-153">NOTES</span></span>

## <span data-ttu-id="817b4-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="817b4-154">RELATED LINKS</span></span>

[<span data-ttu-id="817b4-155">새로운 AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="817b4-155">New-AzureStorageContainer</span></span>](./New-AzureStorageContainer.md)

[<span data-ttu-id="817b4-156">제거-AzureStorageContainer</span><span class="sxs-lookup"><span data-stu-id="817b4-156">Remove-AzureStorageContainer</span></span>](./Remove-AzureStorageContainer.md)

[<span data-ttu-id="817b4-157">Set-AzureStorageContainerAcl</span><span class="sxs-lookup"><span data-stu-id="817b4-157">Set-AzureStorageContainerAcl</span></span>](./Set-AzureStorageContainerAcl.md)


