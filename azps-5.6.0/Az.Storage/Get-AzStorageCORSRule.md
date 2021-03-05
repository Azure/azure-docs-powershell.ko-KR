---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5FA8A3F3-F52C-40BC-94C2-4CDA00C6F32F
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageCORSRule.md
ms.openlocfilehash: e4313dda57632fbc2a5381b1f92067da85c1a905
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002651"
---
# <span data-ttu-id="7ec4a-101">Get-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="7ec4a-101">Get-AzStorageCORSRule</span></span>

## <span data-ttu-id="7ec4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ec4a-102">SYNOPSIS</span></span>
<span data-ttu-id="7ec4a-103">Storage 서비스 형식에 대한 CORS 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7ec4a-103">Gets CORS rules for a Storage service type.</span></span>

## <span data-ttu-id="7ec4a-104">구문</span><span class="sxs-lookup"><span data-stu-id="7ec4a-104">SYNTAX</span></span>

```
Get-AzStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="7ec4a-105">설명</span><span class="sxs-lookup"><span data-stu-id="7ec4a-105">DESCRIPTION</span></span>
<span data-ttu-id="7ec4a-106">**Get-AzStorageCORSRule** cmdlet은 Azure Storage 서비스 유형에 대한 CORS(원본 간 리소스 공유) 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7ec4a-106">The **Get-AzStorageCORSRule** cmdlet gets Cross-Origin Resource Sharing (CORS) rules for an Azure Storage service type.</span></span>

## <span data-ttu-id="7ec4a-107">예제</span><span class="sxs-lookup"><span data-stu-id="7ec4a-107">EXAMPLES</span></span>

### <span data-ttu-id="7ec4a-108">예제 1: Blob 서비스의 CORS 규칙 얻기</span><span class="sxs-lookup"><span data-stu-id="7ec4a-108">Example 1: Get CORS rules of blob service</span></span>
```
PS C:\>Get-AzStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="7ec4a-109">이 명령은 Blob 서비스 형식에 대한 CORS 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7ec4a-109">This command gets the CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="7ec4a-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7ec4a-110">PARAMETERS</span></span>

### <span data-ttu-id="7ec4a-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7ec4a-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="7ec4a-112">하나의 서비스 요청에 대해 클라이언트 쪽 시간 간격(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7ec4a-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="7ec4a-113">지정된 간격에서 이전 호출이 실패하면 이 cmdlet에서 요청을 다시 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="7ec4a-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="7ec4a-114">간격이 경과하기 전에 이 cmdlet에서 성공적인 응답을 받지 못하면 이 cmdlet은 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="7ec4a-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="7ec4a-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="7ec4a-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="7ec4a-116">최대 동시 네트워크 호출을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7ec4a-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="7ec4a-117">이 매개 변수를 사용하여 최대 동시 네트워크 호출 수를 지정하여 로컬 CPU 및 대역폭 사용량을 제한하는 동시성 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ec4a-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="7ec4a-118">지정된 값은 절대 개수로 코어 수에 곱하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7ec4a-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="7ec4a-119">이 매개 변수는 초당 100킬로비트와 같은 대역폭이 낮은 환경에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7ec4a-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="7ec4a-120">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="7ec4a-120">The default value is 10.</span></span>

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

### <span data-ttu-id="7ec4a-121">-Context</span><span class="sxs-lookup"><span data-stu-id="7ec4a-121">-Context</span></span>
<span data-ttu-id="7ec4a-122">Azure Storage 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7ec4a-122">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="7ec4a-123">컨텍스트를 얻지 위해 New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7ec4a-123">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="7ec4a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ec4a-124">-DefaultProfile</span></span>
<span data-ttu-id="7ec4a-125">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7ec4a-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ec4a-126">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7ec4a-126">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="7ec4a-127">요청의 서버 부분에 대한 시간 제한 기간의 길이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7ec4a-127">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="7ec4a-128">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="7ec4a-128">-ServiceType</span></span>
<span data-ttu-id="7ec4a-129">이 cmdlet에서 CORS 규칙을 제공하는 Azure Storage 서비스 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7ec4a-129">Specifies the Azure Storage service type for which this cmdlet gets CORS rules.</span></span>
<span data-ttu-id="7ec4a-130">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="7ec4a-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7ec4a-131">Blob</span><span class="sxs-lookup"><span data-stu-id="7ec4a-131">Blob</span></span> 
- <span data-ttu-id="7ec4a-132">표</span><span class="sxs-lookup"><span data-stu-id="7ec4a-132">Table</span></span> 
- <span data-ttu-id="7ec4a-133">큐</span><span class="sxs-lookup"><span data-stu-id="7ec4a-133">Queue</span></span> 
- <span data-ttu-id="7ec4a-134">파일</span><span class="sxs-lookup"><span data-stu-id="7ec4a-134">File</span></span>

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

### <span data-ttu-id="7ec4a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ec4a-135">CommonParameters</span></span>
<span data-ttu-id="7ec4a-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7ec4a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ec4a-137">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7ec4a-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ec4a-138">입력</span><span class="sxs-lookup"><span data-stu-id="7ec4a-138">INPUTS</span></span>

### <span data-ttu-id="7ec4a-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7ec4a-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7ec4a-140">출력</span><span class="sxs-lookup"><span data-stu-id="7ec4a-140">OUTPUTS</span></span>

### <span data-ttu-id="7ec4a-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span><span class="sxs-lookup"><span data-stu-id="7ec4a-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span></span>

## <span data-ttu-id="7ec4a-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7ec4a-142">NOTES</span></span>

## <span data-ttu-id="7ec4a-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7ec4a-143">RELATED LINKS</span></span>

[<span data-ttu-id="7ec4a-144">Remove-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="7ec4a-144">Remove-AzStorageCORSRule</span></span>](./Remove-AzStorageCORSRule.md)

[<span data-ttu-id="7ec4a-145">Set-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="7ec4a-145">Set-AzStorageCORSRule</span></span>](./Set-AzStorageCORSRule.md)


