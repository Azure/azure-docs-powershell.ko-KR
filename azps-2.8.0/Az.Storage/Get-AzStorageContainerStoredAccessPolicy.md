---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 10D5B7E0-242B-4DC0-A527-8F6388E72E0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 71f00e9e1842eef237a7128d5e20e2ac2116e8a9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93874130"
---
# <span data-ttu-id="35fa9-101">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="35fa9-101">Get-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="35fa9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35fa9-102">SYNOPSIS</span></span>
<span data-ttu-id="35fa9-103">Azure storage 컨테이너에 대 한 저장 된 액세스 정책 또는 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="35fa9-103">Gets the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="35fa9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="35fa9-104">SYNTAX</span></span>

```
Get-AzStorageContainerStoredAccessPolicy [-Container] <String> [[-Policy] <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="35fa9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="35fa9-105">DESCRIPTION</span></span>
<span data-ttu-id="35fa9-106">**AzStorageContainerStoredAccessPolicy** Cmdlet은 Azure storage 컨테이너에 대 한 저장 된 액세스 정책 또는 정책을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="35fa9-106">The **Get-AzStorageContainerStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="35fa9-107">예제의</span><span class="sxs-lookup"><span data-stu-id="35fa9-107">EXAMPLES</span></span>

### <span data-ttu-id="35fa9-108">예제 1: 저장소 컨테이너에서 저장 된 액세스 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="35fa9-108">Example 1: Get a stored access policy in a storage container</span></span>
```
PS C:\>Get-AzStorageContainerStoredAccessPolicy -Container "Container07" -Policy "Policy22"
```

<span data-ttu-id="35fa9-109">이 명령은 Container07 이라는 저장소 컨테이너에서 Policy22 라는 액세스 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="35fa9-109">This command gets the access policy named Policy22 in the storage container named Container07.</span></span>

### <span data-ttu-id="35fa9-110">예제 2: 저장소 컨테이너에 저장 된 모든 액세스 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="35fa9-110">Example 2: Get all the stored access policies in a storage container</span></span>
```
PS C:\>Get-AzStorageContainerStoredAccessPolicy -Container "Container07"
```

<span data-ttu-id="35fa9-111">이 명령은 Container07 이라는 저장소 컨테이너의 모든 액세스 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="35fa9-111">This command gets all access policies in the storage container named Container07.</span></span>

## <span data-ttu-id="35fa9-112">변수</span><span class="sxs-lookup"><span data-stu-id="35fa9-112">PARAMETERS</span></span>

### <span data-ttu-id="35fa9-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="35fa9-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="35fa9-114">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35fa9-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="35fa9-115">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="35fa9-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="35fa9-116">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="35fa9-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="35fa9-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="35fa9-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="35fa9-118">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35fa9-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="35fa9-119">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35fa9-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="35fa9-120">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="35fa9-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="35fa9-121">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35fa9-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="35fa9-122">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="35fa9-122">The default value is 10.</span></span>

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

### <span data-ttu-id="35fa9-123">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="35fa9-123">-Container</span></span>
<span data-ttu-id="35fa9-124">Azure 저장소 컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35fa9-124">Specifies the name of your Azure storage container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35fa9-125">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="35fa9-125">-Context</span></span>
<span data-ttu-id="35fa9-126">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35fa9-126">Specifies the Azure storage context.</span></span>

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

### <span data-ttu-id="35fa9-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35fa9-127">-DefaultProfile</span></span>
<span data-ttu-id="35fa9-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="35fa9-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35fa9-129">-정책</span><span class="sxs-lookup"><span data-stu-id="35fa9-129">-Policy</span></span>
<span data-ttu-id="35fa9-130">Azure 저장 된 액세스 정책을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35fa9-130">Specifies the Azure stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35fa9-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="35fa9-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="35fa9-132">요청에 대 한 서비스 측 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="35fa9-132">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="35fa9-133">서비스가 요청을 처리 하기 전에 지정 된 간격이 경과 하면 저장소 서비스에서 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="35fa9-133">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="35fa9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35fa9-134">CommonParameters</span></span>
<span data-ttu-id="35fa9-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="35fa9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35fa9-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35fa9-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35fa9-137">입력</span><span class="sxs-lookup"><span data-stu-id="35fa9-137">INPUTS</span></span>

### <span data-ttu-id="35fa9-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="35fa9-138">System.String</span></span>

### <span data-ttu-id="35fa9-139">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="35fa9-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="35fa9-140">출력</span><span class="sxs-lookup"><span data-stu-id="35fa9-140">OUTPUTS</span></span>

### <span data-ttu-id="35fa9-141">Microsoft Azure. SharedAccessBlobPolicy</span><span class="sxs-lookup"><span data-stu-id="35fa9-141">Microsoft.Azure.Storage.Blob.SharedAccessBlobPolicy</span></span>

## <span data-ttu-id="35fa9-142">상속자</span><span class="sxs-lookup"><span data-stu-id="35fa9-142">NOTES</span></span>

## <span data-ttu-id="35fa9-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="35fa9-143">RELATED LINKS</span></span>

[<span data-ttu-id="35fa9-144">새로운 AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="35fa9-144">New-AzStorageContainerStoredAccessPolicy</span></span>](./New-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="35fa9-145">제거-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="35fa9-145">Remove-AzStorageContainerStoredAccessPolicy</span></span>](./Remove-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="35fa9-146">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="35fa9-146">Set-AzStorageContainerStoredAccessPolicy</span></span>](./Set-AzStorageContainerStoredAccessPolicy.md)


