---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5FA8A3F3-F52C-40BC-94C2-4CDA00C6F32F
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageCORSRule.md
ms.openlocfilehash: 1eb5803c65739c2e202d042efbf6ba4dff815394
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349670"
---
# <span data-ttu-id="c6efe-101">Get-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="c6efe-101">Get-AzStorageCORSRule</span></span>

## <span data-ttu-id="c6efe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6efe-102">SYNOPSIS</span></span>
<span data-ttu-id="c6efe-103">Storage 서비스 유형에 대한 CORS 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c6efe-103">Gets CORS rules for a Storage service type.</span></span>

## <span data-ttu-id="c6efe-104">구문</span><span class="sxs-lookup"><span data-stu-id="c6efe-104">SYNTAX</span></span>

```
Get-AzStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="c6efe-105">설명</span><span class="sxs-lookup"><span data-stu-id="c6efe-105">DESCRIPTION</span></span>
<span data-ttu-id="c6efe-106">**Get-AzStorageCORSRule** cmdlet은 Azure Storage 서비스 유형에 대한 CORS(원본 간 리소스 공유) 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c6efe-106">The **Get-AzStorageCORSRule** cmdlet gets Cross-Origin Resource Sharing (CORS) rules for an Azure Storage service type.</span></span>

## <span data-ttu-id="c6efe-107">예제</span><span class="sxs-lookup"><span data-stu-id="c6efe-107">EXAMPLES</span></span>

### <span data-ttu-id="c6efe-108">예제 1: Blob service의 CORS 규칙 얻기</span><span class="sxs-lookup"><span data-stu-id="c6efe-108">Example 1: Get CORS rules of blob service</span></span>
```
PS C:\>Get-AzStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="c6efe-109">이 명령은 Blob service 형식에 대한 CORS 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c6efe-109">This command gets the CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="c6efe-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c6efe-110">PARAMETERS</span></span>

### <span data-ttu-id="c6efe-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c6efe-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="c6efe-112">하나의 서비스 요청에 대해 클라이언트 쪽 시간(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c6efe-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="c6efe-113">이전 호출이 지정된 간격에서 실패하는 경우 이 cmdlet은 요청을 다시 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="c6efe-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="c6efe-114">이 cmdlet이 간격이 경과하기 전에 성공적인 응답을 받지 못하면 이 cmdlet은 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="c6efe-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="c6efe-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="c6efe-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="c6efe-116">최대 동시 네트워크 호출을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c6efe-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="c6efe-117">이 매개 변수를 사용하여 최대 동시 네트워크 호출 수를 지정하여 동시성으로 로컬 CPU 및 대역폭 사용량을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c6efe-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="c6efe-118">지정된 값은 절대 개수로, 코어 수에 곱하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c6efe-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="c6efe-119">이 매개 변수는 초당 100킬로비트와 같은 낮은 대역폭 환경에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c6efe-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="c6efe-120">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="c6efe-120">The default value is 10.</span></span>

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

### <span data-ttu-id="c6efe-121">-Context</span><span class="sxs-lookup"><span data-stu-id="c6efe-121">-Context</span></span>
<span data-ttu-id="c6efe-122">Azure Storage 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c6efe-122">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="c6efe-123">컨텍스트를 얻습니다. New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6efe-123">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="c6efe-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6efe-124">-DefaultProfile</span></span>
<span data-ttu-id="c6efe-125">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c6efe-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6efe-126">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c6efe-126">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="c6efe-127">요청의 서버 부분에 대한 시간 제한 기간의 길이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c6efe-127">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="c6efe-128">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="c6efe-128">-ServiceType</span></span>
<span data-ttu-id="c6efe-129">이 cmdlet이 CORS 규칙을 받을 Azure Storage 서비스 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c6efe-129">Specifies the Azure Storage service type for which this cmdlet gets CORS rules.</span></span>
<span data-ttu-id="c6efe-130">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="c6efe-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="c6efe-131">Blob</span><span class="sxs-lookup"><span data-stu-id="c6efe-131">Blob</span></span> 
- <span data-ttu-id="c6efe-132">표</span><span class="sxs-lookup"><span data-stu-id="c6efe-132">Table</span></span> 
- <span data-ttu-id="c6efe-133">큐</span><span class="sxs-lookup"><span data-stu-id="c6efe-133">Queue</span></span> 
- <span data-ttu-id="c6efe-134">파일</span><span class="sxs-lookup"><span data-stu-id="c6efe-134">File</span></span>

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

### <span data-ttu-id="c6efe-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6efe-135">CommonParameters</span></span>
<span data-ttu-id="c6efe-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c6efe-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6efe-137">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c6efe-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6efe-138">입력</span><span class="sxs-lookup"><span data-stu-id="c6efe-138">INPUTS</span></span>

### <span data-ttu-id="c6efe-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c6efe-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c6efe-140">출력</span><span class="sxs-lookup"><span data-stu-id="c6efe-140">OUTPUTS</span></span>

### <span data-ttu-id="c6efe-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span><span class="sxs-lookup"><span data-stu-id="c6efe-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span></span>

## <span data-ttu-id="c6efe-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c6efe-142">NOTES</span></span>

## <span data-ttu-id="c6efe-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c6efe-143">RELATED LINKS</span></span>

[<span data-ttu-id="c6efe-144">Remove-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="c6efe-144">Remove-AzStorageCORSRule</span></span>](./Remove-AzStorageCORSRule.md)

[<span data-ttu-id="c6efe-145">Set-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="c6efe-145">Set-AzStorageCORSRule</span></span>](./Set-AzStorageCORSRule.md)


