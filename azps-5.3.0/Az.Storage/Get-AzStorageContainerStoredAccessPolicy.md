---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 10D5B7E0-242B-4DC0-A527-8F6388E72E0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 5a0f976d561396bc93facfeedcbb1c89c768e5b2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374067"
---
# <span data-ttu-id="ac3aa-101">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ac3aa-101">Get-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="ac3aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac3aa-102">SYNOPSIS</span></span>
<span data-ttu-id="ac3aa-103">Azure 저장소 컨테이너에 대한 저장된 액세스 정책 또는 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ac3aa-103">Gets the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="ac3aa-104">구문</span><span class="sxs-lookup"><span data-stu-id="ac3aa-104">SYNTAX</span></span>

```
Get-AzStorageContainerStoredAccessPolicy [-Container] <String> [[-Policy] <String>]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="ac3aa-105">설명</span><span class="sxs-lookup"><span data-stu-id="ac3aa-105">DESCRIPTION</span></span>
<span data-ttu-id="ac3aa-106">**Get-AzStorageContainerStoredAccessPolicy** cmdlet은 Azure 저장소 컨테이너에 대한 저장된 액세스 정책 또는 정책을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="ac3aa-106">The **Get-AzStorageContainerStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage container.</span></span>

## <span data-ttu-id="ac3aa-107">예제</span><span class="sxs-lookup"><span data-stu-id="ac3aa-107">EXAMPLES</span></span>

### <span data-ttu-id="ac3aa-108">예제 1: 저장소 컨테이너에 저장된 액세스 정책 얻기</span><span class="sxs-lookup"><span data-stu-id="ac3aa-108">Example 1: Get a stored access policy in a storage container</span></span>
```
PS C:\>Get-AzStorageContainerStoredAccessPolicy -Container "Container07" -Policy "Policy22"
```

<span data-ttu-id="ac3aa-109">이 명령은 Container07이라는 저장소 컨테이너에서 Policy22라는 액세스 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ac3aa-109">This command gets the access policy named Policy22 in the storage container named Container07.</span></span>

### <span data-ttu-id="ac3aa-110">예제 2: 저장소 컨테이너에 저장된 모든 액세스 정책 얻기</span><span class="sxs-lookup"><span data-stu-id="ac3aa-110">Example 2: Get all the stored access policies in a storage container</span></span>
```
PS C:\>Get-AzStorageContainerStoredAccessPolicy -Container "Container07"
```

<span data-ttu-id="ac3aa-111">이 명령은 Container07이라는 저장소 컨테이너의 모든 액세스 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ac3aa-111">This command gets all access policies in the storage container named Container07.</span></span>

## <span data-ttu-id="ac3aa-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac3aa-112">PARAMETERS</span></span>

### <span data-ttu-id="ac3aa-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ac3aa-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="ac3aa-114">하나의 서비스 요청에 대해 클라이언트 쪽 시간(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ac3aa-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="ac3aa-115">이전 호출이 지정된 간격에서 실패하는 경우 이 cmdlet은 요청을 다시 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="ac3aa-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="ac3aa-116">이 cmdlet이 간격이 경과하기 전에 성공적인 응답을 받지 못하면 이 cmdlet은 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ac3aa-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="ac3aa-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="ac3aa-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="ac3aa-118">최대 동시 네트워크 호출을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ac3aa-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="ac3aa-119">이 매개 변수를 사용하여 최대 동시 네트워크 호출 수를 지정하여 동시성으로 로컬 CPU 및 대역폭 사용량을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac3aa-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="ac3aa-120">지정된 값은 절대 개수로, 코어 수에 곱하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ac3aa-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="ac3aa-121">이 매개 변수는 초당 100킬로비트와 같은 낮은 대역폭 환경에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ac3aa-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="ac3aa-122">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="ac3aa-122">The default value is 10.</span></span>

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

### <span data-ttu-id="ac3aa-123">-Container</span><span class="sxs-lookup"><span data-stu-id="ac3aa-123">-Container</span></span>
<span data-ttu-id="ac3aa-124">Azure 저장소 컨테이너의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ac3aa-124">Specifies the name of your Azure storage container.</span></span>

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

### <span data-ttu-id="ac3aa-125">-Context</span><span class="sxs-lookup"><span data-stu-id="ac3aa-125">-Context</span></span>
<span data-ttu-id="ac3aa-126">Azure 저장소 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ac3aa-126">Specifies the Azure storage context.</span></span>

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

### <span data-ttu-id="ac3aa-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac3aa-127">-DefaultProfile</span></span>
<span data-ttu-id="ac3aa-128">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ac3aa-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac3aa-129">-Policy</span><span class="sxs-lookup"><span data-stu-id="ac3aa-129">-Policy</span></span>
<span data-ttu-id="ac3aa-130">Azure에 저장된 액세스 정책을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ac3aa-130">Specifies the Azure stored access policy.</span></span>

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

### <span data-ttu-id="ac3aa-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ac3aa-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="ac3aa-132">요청에 대한 서비스 쪽 시간제한 간격(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ac3aa-132">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="ac3aa-133">지정된 간격이 서비스에서 요청을 처리하기 전에 경과하면 저장소 서비스가 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ac3aa-133">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="ac3aa-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac3aa-134">CommonParameters</span></span>
<span data-ttu-id="ac3aa-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ac3aa-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac3aa-136">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ac3aa-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac3aa-137">입력</span><span class="sxs-lookup"><span data-stu-id="ac3aa-137">INPUTS</span></span>

### <span data-ttu-id="ac3aa-138">System.String</span><span class="sxs-lookup"><span data-stu-id="ac3aa-138">System.String</span></span>

### <span data-ttu-id="ac3aa-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ac3aa-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ac3aa-140">출력</span><span class="sxs-lookup"><span data-stu-id="ac3aa-140">OUTPUTS</span></span>

### <span data-ttu-id="ac3aa-141">Microsoft.Azure.Storage.Blob.SharedAccessBlobPolicy</span><span class="sxs-lookup"><span data-stu-id="ac3aa-141">Microsoft.Azure.Storage.Blob.SharedAccessBlobPolicy</span></span>

## <span data-ttu-id="ac3aa-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ac3aa-142">NOTES</span></span>

## <span data-ttu-id="ac3aa-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ac3aa-143">RELATED LINKS</span></span>

[<span data-ttu-id="ac3aa-144">New-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ac3aa-144">New-AzStorageContainerStoredAccessPolicy</span></span>](./New-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="ac3aa-145">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ac3aa-145">Remove-AzStorageContainerStoredAccessPolicy</span></span>](./Remove-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="ac3aa-146">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ac3aa-146">Set-AzStorageContainerStoredAccessPolicy</span></span>](./Set-AzStorageContainerStoredAccessPolicy.md)


