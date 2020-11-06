---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 10D5B7E0-242B-4DC0-A527-8F6388E72E0A
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 19dbbe53347a06030c175f45f722bfd287863d85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530631"
---
# <span data-ttu-id="205d2-101">Get-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="205d2-101">Get-AzureStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="205d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="205d2-102">SYNOPSIS</span></span>
<span data-ttu-id="205d2-103">Azure storage 컨테이너에 대 한 저장 된 액세스 정책 또는 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="205d2-103">Gets the stored access policy or policies for an Azure storage container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="205d2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="205d2-104">SYNTAX</span></span>

```
Get-AzureStorageContainerStoredAccessPolicy [-Container] <String> [[-Policy] <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="205d2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="205d2-105">DESCRIPTION</span></span>
<span data-ttu-id="205d2-106">**AzureStorageContainerStoredAccessPolicy** Cmdlet은 Azure storage 컨테이너에 대 한 저장 된 액세스 정책 또는 정책을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="205d2-106">The **Get-AzureStorageContainerStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="205d2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="205d2-107">EXAMPLES</span></span>

### <span data-ttu-id="205d2-108">예제 1: 저장소 컨테이너에서 저장 된 액세스 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="205d2-108">Example 1: Get a stored access policy in a storage container</span></span>
```
PS C:\>Get-AzureStorageContainerStoredAccessPolicy -Container "Container07" -Policy "Policy22"
```

<span data-ttu-id="205d2-109">이 명령은 Container07 이라는 저장소 컨테이너에서 Policy22 라는 액세스 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="205d2-109">This command gets the access policy named Policy22 in the storage container named Container07.</span></span>

### <span data-ttu-id="205d2-110">예제 2: 저장소 컨테이너에 저장 된 모든 액세스 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="205d2-110">Example 2: Get all the stored access policies in a storage container</span></span>
```
PS C:\>Get-AzureStorageContainerStoredAccessPolicy -Container "Container07"
```

<span data-ttu-id="205d2-111">이 명령은 Container07 이라는 저장소 컨테이너의 모든 액세스 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="205d2-111">This command gets all access policies in the storage container named Container07.</span></span>

## <span data-ttu-id="205d2-112">변수</span><span class="sxs-lookup"><span data-stu-id="205d2-112">PARAMETERS</span></span>

### <span data-ttu-id="205d2-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="205d2-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="205d2-114">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="205d2-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="205d2-115">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="205d2-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="205d2-116">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="205d2-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="205d2-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="205d2-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="205d2-118">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="205d2-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="205d2-119">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="205d2-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="205d2-120">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="205d2-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="205d2-121">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="205d2-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="205d2-122">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="205d2-122">The default value is 10.</span></span>

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

### <span data-ttu-id="205d2-123">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="205d2-123">-Container</span></span>
<span data-ttu-id="205d2-124">Azure 저장소 컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="205d2-124">Specifies the name of your Azure storage container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="205d2-125">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="205d2-125">-Context</span></span>
<span data-ttu-id="205d2-126">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="205d2-126">Specifies the Azure storage context.</span></span>

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

### <span data-ttu-id="205d2-127">-정책</span><span class="sxs-lookup"><span data-stu-id="205d2-127">-Policy</span></span>
<span data-ttu-id="205d2-128">Azure 저장 된 액세스 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="205d2-128">Specifies the Azure stored access policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="205d2-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="205d2-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="205d2-130">요청에 대 한 서비스 측 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="205d2-130">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="205d2-131">서비스가 요청을 처리 하기 전에 지정 된 간격이 경과 하면 저장소 서비스에서 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="205d2-131">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="205d2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="205d2-132">CommonParameters</span></span>
<span data-ttu-id="205d2-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="205d2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="205d2-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="205d2-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="205d2-135">입력</span><span class="sxs-lookup"><span data-stu-id="205d2-135">INPUTS</span></span>

### <span data-ttu-id="205d2-136">이름</span><span class="sxs-lookup"><span data-stu-id="205d2-136">String</span></span>

<span data-ttu-id="205d2-137">' Container ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="205d2-137">Parameter 'Container' accepts value of type 'String' from the pipeline</span></span>

### <span data-ttu-id="205d2-138">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="205d2-138">IStorageContext</span></span>

<span data-ttu-id="205d2-139">' Context ' 매개 변수는 파이프라인에서 ' IStorageContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="205d2-139">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="205d2-140">출력</span><span class="sxs-lookup"><span data-stu-id="205d2-140">OUTPUTS</span></span>

### <span data-ttu-id="205d2-141">WindowsAzure. a. b i. SharedAccessBlobPolicy</span><span class="sxs-lookup"><span data-stu-id="205d2-141">Microsoft.WindowsAzure.Storage.Blob.SharedAccessBlobPolicy</span></span>

## <span data-ttu-id="205d2-142">상속자</span><span class="sxs-lookup"><span data-stu-id="205d2-142">NOTES</span></span>

## <span data-ttu-id="205d2-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="205d2-143">RELATED LINKS</span></span>

[<span data-ttu-id="205d2-144">새로운 AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="205d2-144">New-AzureStorageContainerStoredAccessPolicy</span></span>](./New-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="205d2-145">제거-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="205d2-145">Remove-AzureStorageContainerStoredAccessPolicy</span></span>](./Remove-AzureStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="205d2-146">Set-AzureStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="205d2-146">Set-AzureStorageContainerStoredAccessPolicy</span></span>](./Set-AzureStorageContainerStoredAccessPolicy.md)


