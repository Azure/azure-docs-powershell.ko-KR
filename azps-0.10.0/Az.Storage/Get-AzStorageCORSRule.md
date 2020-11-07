---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5FA8A3F3-F52C-40BC-94C2-4CDA00C6F32F
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragecorsrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageCORSRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageCORSRule.md
ms.openlocfilehash: c32e58f2e6b8c146d1b5a01f252f1341092f86d5
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876310"
---
# <span data-ttu-id="52d1d-101">Get-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="52d1d-101">Get-AzStorageCORSRule</span></span>

## <span data-ttu-id="52d1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52d1d-102">SYNOPSIS</span></span>
<span data-ttu-id="52d1d-103">저장소 서비스 형식에 대 한 CORS 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="52d1d-103">Gets CORS rules for a Storage service type.</span></span>

## <span data-ttu-id="52d1d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="52d1d-104">SYNTAX</span></span>

```
Get-AzStorageCORSRule [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="52d1d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="52d1d-105">DESCRIPTION</span></span>
<span data-ttu-id="52d1d-106">**AzStorageCORSRule** Cmdlet은 Azure 저장소 서비스 형식에 대 한 CORS (교차 원본 리소스 공유) 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="52d1d-106">The **Get-AzStorageCORSRule** cmdlet gets Cross-Origin Resource Sharing (CORS) rules for an Azure Storage service type.</span></span>

## <span data-ttu-id="52d1d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="52d1d-107">EXAMPLES</span></span>

### <span data-ttu-id="52d1d-108">예제 1: blob 서비스의 CORS 규칙 가져오기</span><span class="sxs-lookup"><span data-stu-id="52d1d-108">Example 1: Get CORS rules of blob service</span></span>
```
PS C:\>Get-AzStorageCORSRule -ServiceType Blob
```

<span data-ttu-id="52d1d-109">이 명령은 Blob 서비스 형식에 대 한 CORS 규칙을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="52d1d-109">This command gets the CORS rules for the Blob service type.</span></span>

## <span data-ttu-id="52d1d-110">변수</span><span class="sxs-lookup"><span data-stu-id="52d1d-110">PARAMETERS</span></span>

### <span data-ttu-id="52d1d-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="52d1d-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="52d1d-112">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="52d1d-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="52d1d-113">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="52d1d-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="52d1d-114">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="52d1d-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="52d1d-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="52d1d-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="52d1d-116">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="52d1d-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="52d1d-117">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="52d1d-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="52d1d-118">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="52d1d-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="52d1d-119">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="52d1d-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="52d1d-120">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="52d1d-120">The default value is 10.</span></span>

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

### <span data-ttu-id="52d1d-121">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="52d1d-121">-Context</span></span>
<span data-ttu-id="52d1d-122">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="52d1d-122">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="52d1d-123">컨텍스트를 가져오려면 New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="52d1d-123">To obtain a context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="52d1d-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52d1d-124">-DefaultProfile</span></span>
<span data-ttu-id="52d1d-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="52d1d-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52d1d-126">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="52d1d-126">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="52d1d-127">요청에 대 한 서버 부분에 대 한 시간 초과 기간의 길이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="52d1d-127">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="52d1d-128">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="52d1d-128">-ServiceType</span></span>
<span data-ttu-id="52d1d-129">이 cmdlet이 CORS 규칙을 가져오는 Azure 저장소 서비스 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="52d1d-129">Specifies the Azure Storage service type for which this cmdlet gets CORS rules.</span></span>
<span data-ttu-id="52d1d-130">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="52d1d-130">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="52d1d-131">블</span><span class="sxs-lookup"><span data-stu-id="52d1d-131">Blob</span></span> 
- <span data-ttu-id="52d1d-132">테이블로</span><span class="sxs-lookup"><span data-stu-id="52d1d-132">Table</span></span> 
- <span data-ttu-id="52d1d-133">전담팀</span><span class="sxs-lookup"><span data-stu-id="52d1d-133">Queue</span></span> 
- <span data-ttu-id="52d1d-134">파일</span><span class="sxs-lookup"><span data-stu-id="52d1d-134">File</span></span>

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

### <span data-ttu-id="52d1d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52d1d-135">CommonParameters</span></span>
<span data-ttu-id="52d1d-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="52d1d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52d1d-137">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52d1d-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52d1d-138">입력</span><span class="sxs-lookup"><span data-stu-id="52d1d-138">INPUTS</span></span>

### <span data-ttu-id="52d1d-139">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="52d1d-139">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="52d1d-140">출력</span><span class="sxs-lookup"><span data-stu-id="52d1d-140">OUTPUTS</span></span>

### <span data-ttu-id="52d1d-141">WindowsAzure. ResourceModel를 PSCorsRule로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="52d1d-141">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSCorsRule</span></span>

## <span data-ttu-id="52d1d-142">상속자</span><span class="sxs-lookup"><span data-stu-id="52d1d-142">NOTES</span></span>

## <span data-ttu-id="52d1d-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="52d1d-143">RELATED LINKS</span></span>

[<span data-ttu-id="52d1d-144">제거-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="52d1d-144">Remove-AzStorageCORSRule</span></span>](./Remove-AzStorageCORSRule.md)

[<span data-ttu-id="52d1d-145">Set-AzStorageCORSRule</span><span class="sxs-lookup"><span data-stu-id="52d1d-145">Set-AzStorageCORSRule</span></span>](./Set-AzStorageCORSRule.md)


