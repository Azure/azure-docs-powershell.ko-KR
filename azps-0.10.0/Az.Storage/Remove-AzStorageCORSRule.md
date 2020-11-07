---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 26E06BA3-C550-40A5-B8E3-FEC8E9BF3867
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Remove-AzStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Remove-AzStorageCORSRule.md
ms.openlocfilehash: f134d554e02c2067f51107faf0f5001bb133eb88
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876236"
---
# <span data-ttu-id="d9aac-101">Remove-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="d9aac-101">Remove-AzStorageCORSRule</span></span>

## <span data-ttu-id="d9aac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9aac-102">SYNOPSIS</span></span>
<span data-ttu-id="d9aac-103">저장소 서비스의 CORS를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9aac-103">Removes CORS for a Storage service.</span></span>

## <span data-ttu-id="d9aac-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d9aac-104">SYNTAX</span></span>

```
Remove-AzStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="d9aac-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d9aac-105">DESCRIPTION</span></span>
<span data-ttu-id="d9aac-106">**AzStorageCORSRule** Cmdlet은 Azure 저장소 서비스의 CORS (교차 원본 리소스 공유)를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9aac-106">The **Remove-AzStorageCORSRule** cmdlet removes Cross-Origin Resource Sharing (CORS) for an Azure Storage service.</span></span>
<span data-ttu-id="d9aac-107">이 cmdlet은 저장소 서비스 유형에 서 모든 CORS 규칙을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9aac-107">This cmdlet deletes all CORS rules in a Storage service type.</span></span>
<span data-ttu-id="d9aac-108">이 cmdlet에 대 한 저장소 서비스의 유형은 Blob, 테이블, 큐 및 파일입니다.</span><span class="sxs-lookup"><span data-stu-id="d9aac-108">The types of storage services for this cmdlet are Blob, Table, Queue, and File.</span></span>

## <span data-ttu-id="d9aac-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d9aac-109">EXAMPLES</span></span>

### <span data-ttu-id="d9aac-110">예제 1: blob 서비스에 대 한 CORS 규칙 제거</span><span class="sxs-lookup"><span data-stu-id="d9aac-110">Example 1: Remove CORS rules for the blob service</span></span>
```
PS C:\>Remove-AzStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="d9aac-111">이 명령은 Blob 서비스 형식에 대 한 CORS 규칙을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9aac-111">This command removes CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="d9aac-112">변수</span><span class="sxs-lookup"><span data-stu-id="d9aac-112">PARAMETERS</span></span>

### <span data-ttu-id="d9aac-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d9aac-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="d9aac-114">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9aac-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="d9aac-115">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9aac-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="d9aac-116">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9aac-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="d9aac-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="d9aac-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="d9aac-118">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9aac-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="d9aac-119">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9aac-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="d9aac-120">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="d9aac-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="d9aac-121">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d9aac-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="d9aac-122">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="d9aac-122">The default value is 10.</span></span>

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

### <span data-ttu-id="d9aac-123">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="d9aac-123">-Context</span></span>
<span data-ttu-id="d9aac-124">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9aac-124">Specifies the Azure storage context.</span></span>
<span data-ttu-id="d9aac-125">저장소 컨텍스트를 얻으려면 New-AzStorageContext cmdlet을 제공 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9aac-125">To obtain the storage context, the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="d9aac-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9aac-126">-DefaultProfile</span></span>
<span data-ttu-id="d9aac-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d9aac-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9aac-128">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="d9aac-128">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="d9aac-129">요청에 대 한 서버 부분에 대 한 시간 초과 기간의 길이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9aac-129">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="d9aac-130">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="d9aac-130">-ServiceType</span></span>
<span data-ttu-id="d9aac-131">이 cmdlet이 규칙을 제거할 Azure 저장소 서비스 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9aac-131">Specifies the Azure Storage service type for which this cmdlet removes rules.</span></span>
<span data-ttu-id="d9aac-132">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="d9aac-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d9aac-133">블</span><span class="sxs-lookup"><span data-stu-id="d9aac-133">Blob</span></span> 
- <span data-ttu-id="d9aac-134">테이블로</span><span class="sxs-lookup"><span data-stu-id="d9aac-134">Table</span></span> 
- <span data-ttu-id="d9aac-135">전담팀</span><span class="sxs-lookup"><span data-stu-id="d9aac-135">Queue</span></span> 
- <span data-ttu-id="d9aac-136">파일</span><span class="sxs-lookup"><span data-stu-id="d9aac-136">File</span></span>

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

### <span data-ttu-id="d9aac-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9aac-137">CommonParameters</span></span>
<span data-ttu-id="d9aac-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9aac-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9aac-139">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9aac-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9aac-140">입력</span><span class="sxs-lookup"><span data-stu-id="d9aac-140">INPUTS</span></span>

### <span data-ttu-id="d9aac-141">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d9aac-141">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="d9aac-142">출력</span><span class="sxs-lookup"><span data-stu-id="d9aac-142">OUTPUTS</span></span>

### <span data-ttu-id="d9aac-143">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="d9aac-143">System.Void</span></span>

## <span data-ttu-id="d9aac-144">상속자</span><span class="sxs-lookup"><span data-stu-id="d9aac-144">NOTES</span></span>

## <span data-ttu-id="d9aac-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d9aac-145">RELATED LINKS</span></span>

[<span data-ttu-id="d9aac-146">Get-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="d9aac-146">Get-AzStorageCORSRule</span></span>](./Get-AzStorageCORSRule.md)

[<span data-ttu-id="d9aac-147">Set-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="d9aac-147">Set-AzStorageCORSRule</span></span>](./Set-AzStorageCORSRule.md)


