---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 26E06BA3-C550-40A5-B8E3-FEC8E9BF3867
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageCORSRule.md
ms.openlocfilehash: aeae25ab3a8ff0b1fa3eb91db90497b44555631f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494672"
---
# <span data-ttu-id="ce90a-101">Remove-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="ce90a-101">Remove-AzStorageCORSRule</span></span>

## <span data-ttu-id="ce90a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce90a-102">SYNOPSIS</span></span>
<span data-ttu-id="ce90a-103">Storage 서비스에 대한 CORS를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ce90a-103">Removes CORS for a Storage service.</span></span>

## <span data-ttu-id="ce90a-104">구문</span><span class="sxs-lookup"><span data-stu-id="ce90a-104">SYNTAX</span></span>

```
Remove-AzStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="ce90a-105">설명</span><span class="sxs-lookup"><span data-stu-id="ce90a-105">DESCRIPTION</span></span>
<span data-ttu-id="ce90a-106">**Remove-AzStorageCORSRule** cmdlet은 Azure Storage 서비스에 대한 CORS(원본 간 리소스 공유)를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ce90a-106">The **Remove-AzStorageCORSRule** cmdlet removes Cross-Origin Resource Sharing (CORS) for an Azure Storage service.</span></span>
<span data-ttu-id="ce90a-107">이 cmdlet은 Storage 서비스 형식의 모든 CORS 규칙을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="ce90a-107">This cmdlet deletes all CORS rules in a Storage service type.</span></span>
<span data-ttu-id="ce90a-108">이 cmdlet에 대한 저장소 서비스의 유형은 Blob, 테이블, 큐 및 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="ce90a-108">The types of storage services for this cmdlet are Blob, Table, Queue, and File.</span></span>

## <span data-ttu-id="ce90a-109">예제</span><span class="sxs-lookup"><span data-stu-id="ce90a-109">EXAMPLES</span></span>

### <span data-ttu-id="ce90a-110">예제 1: Blob service에 대한 CORS 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="ce90a-110">Example 1: Remove CORS rules for the blob service</span></span>
```
PS C:\>Remove-AzStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="ce90a-111">이 명령은 Blob service 형식에 대한 CORS 규칙을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ce90a-111">This command removes CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="ce90a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ce90a-112">PARAMETERS</span></span>

### <span data-ttu-id="ce90a-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ce90a-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="ce90a-114">하나의 서비스 요청에 대해 클라이언트 쪽 시간(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ce90a-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="ce90a-115">이전 호출이 지정된 간격에서 실패하는 경우 이 cmdlet은 요청을 다시 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="ce90a-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="ce90a-116">이 cmdlet이 간격이 경과하기 전에 성공적인 응답을 받지 못하면 이 cmdlet은 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ce90a-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="ce90a-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="ce90a-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="ce90a-118">최대 동시 네트워크 호출을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ce90a-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="ce90a-119">이 매개 변수를 사용하여 최대 동시 네트워크 호출 수를 지정하여 동시성으로 로컬 CPU 및 대역폭 사용량을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ce90a-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="ce90a-120">지정된 값은 절대 개수로, 코어 수에 곱하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ce90a-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="ce90a-121">이 매개 변수는 초당 100킬로비트와 같은 낮은 대역폭 환경에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ce90a-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="ce90a-122">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="ce90a-122">The default value is 10.</span></span>

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

### <span data-ttu-id="ce90a-123">-Context</span><span class="sxs-lookup"><span data-stu-id="ce90a-123">-Context</span></span>
<span data-ttu-id="ce90a-124">Azure 저장소 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ce90a-124">Specifies the Azure storage context.</span></span>
<span data-ttu-id="ce90a-125">저장소 컨텍스트를 얻기 위해 New-AzStorageContext cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="ce90a-125">To obtain the storage context, the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ce90a-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce90a-126">-DefaultProfile</span></span>
<span data-ttu-id="ce90a-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ce90a-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce90a-128">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ce90a-128">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="ce90a-129">요청의 서버 부분에 대한 시간 제한 기간의 길이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ce90a-129">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="ce90a-130">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="ce90a-130">-ServiceType</span></span>
<span data-ttu-id="ce90a-131">이 cmdlet에서 규칙을 제거하는 Azure Storage 서비스 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ce90a-131">Specifies the Azure Storage service type for which this cmdlet removes rules.</span></span>
<span data-ttu-id="ce90a-132">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="ce90a-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="ce90a-133">Blob</span><span class="sxs-lookup"><span data-stu-id="ce90a-133">Blob</span></span> 
- <span data-ttu-id="ce90a-134">표</span><span class="sxs-lookup"><span data-stu-id="ce90a-134">Table</span></span> 
- <span data-ttu-id="ce90a-135">큐</span><span class="sxs-lookup"><span data-stu-id="ce90a-135">Queue</span></span> 
- <span data-ttu-id="ce90a-136">파일</span><span class="sxs-lookup"><span data-stu-id="ce90a-136">File</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.StorageServiceType
Parameter Sets: (All)
Aliases:
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce90a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce90a-137">CommonParameters</span></span>
<span data-ttu-id="ce90a-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ce90a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce90a-139">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ce90a-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce90a-140">입력</span><span class="sxs-lookup"><span data-stu-id="ce90a-140">INPUTS</span></span>

### <span data-ttu-id="ce90a-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ce90a-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ce90a-142">출력</span><span class="sxs-lookup"><span data-stu-id="ce90a-142">OUTPUTS</span></span>

### <span data-ttu-id="ce90a-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="ce90a-143">System.Void</span></span>

## <span data-ttu-id="ce90a-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ce90a-144">NOTES</span></span>

## <span data-ttu-id="ce90a-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ce90a-145">RELATED LINKS</span></span>

[<span data-ttu-id="ce90a-146">Get-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="ce90a-146">Get-AzStorageCORSRule</span></span>](./Get-AzStorageCORSRule.md)

[<span data-ttu-id="ce90a-147">Set-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="ce90a-147">Set-AzStorageCORSRule</span></span>](./Set-AzStorageCORSRule.md)


