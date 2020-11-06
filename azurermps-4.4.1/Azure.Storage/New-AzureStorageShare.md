---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FCDCEF0B-6E2C-480E-9841-EF4E64D61D54
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShare.md
gitcommit: https://github.com/Azure/azure-powershell/blob/173e94aec59d7f539b72e43e90e5e7f8ba5f62bc
ms.openlocfilehash: a1be5816427ac1aa91b9daa98701abaec044c20f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537936"
---
# <span data-ttu-id="dcd92-101">New-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="dcd92-101">New-AzureStorageShare</span></span>

## <span data-ttu-id="dcd92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dcd92-102">SYNOPSIS</span></span>
<span data-ttu-id="dcd92-103">파일 공유를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dcd92-103">Creates a file share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dcd92-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dcd92-104">SYNTAX</span></span>

```
New-AzureStorageShare [-Name] <String> [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="dcd92-105">설명은</span><span class="sxs-lookup"><span data-stu-id="dcd92-105">DESCRIPTION</span></span>
<span data-ttu-id="dcd92-106">**새 AzureStorageShare** cmdlet은 파일 공유를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dcd92-106">The **New-AzureStorageShare** cmdlet creates a file share.</span></span>

## <span data-ttu-id="dcd92-107">예제의</span><span class="sxs-lookup"><span data-stu-id="dcd92-107">EXAMPLES</span></span>

### <span data-ttu-id="dcd92-108">예제 1: 파일 공유 만들기</span><span class="sxs-lookup"><span data-stu-id="dcd92-108">Example 1: Create a file share</span></span>
```
PS C:\>New-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="dcd92-109">이 명령은 ContosoShare06 이라는 파일 공유를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dcd92-109">This command creates a file share named ContosoShare06.</span></span>

## <span data-ttu-id="dcd92-110">변수</span><span class="sxs-lookup"><span data-stu-id="dcd92-110">PARAMETERS</span></span>

### <span data-ttu-id="dcd92-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="dcd92-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="dcd92-112">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd92-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="dcd92-113">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd92-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="dcd92-114">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd92-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="dcd92-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="dcd92-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="dcd92-116">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd92-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="dcd92-117">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcd92-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="dcd92-118">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="dcd92-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="dcd92-119">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcd92-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="dcd92-120">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="dcd92-120">The default value is 10.</span></span>

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

### <span data-ttu-id="dcd92-121">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="dcd92-121">-Context</span></span>
<span data-ttu-id="dcd92-122">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd92-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="dcd92-123">저장소 컨텍스트를 얻으려면 [새로운-AzureStorageContext](./New-AzureStorageContext.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd92-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="dcd92-124">-이름</span><span class="sxs-lookup"><span data-stu-id="dcd92-124">-Name</span></span>
<span data-ttu-id="dcd92-125">파일 공유의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd92-125">Specifies the name of a file share.</span></span>
<span data-ttu-id="dcd92-126">이 cmdlet은이 매개 변수에서 지정 하는 이름의 파일 공유를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dcd92-126">This cmdlet creates a file share that has the name that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dcd92-127">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="dcd92-127">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="dcd92-128">요청에 대 한 서버 부분에 대 한 시간 초과 기간의 길이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd92-128">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="dcd92-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcd92-129">CommonParameters</span></span>
<span data-ttu-id="dcd92-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd92-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcd92-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcd92-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcd92-132">입력</span><span class="sxs-lookup"><span data-stu-id="dcd92-132">INPUTS</span></span>

### <span data-ttu-id="dcd92-133">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="dcd92-133">IStorageContext</span></span>

<span data-ttu-id="dcd92-134">' Context ' 매개 변수는 파이프라인에서 ' IStorageContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd92-134">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="dcd92-135">이름</span><span class="sxs-lookup"><span data-stu-id="dcd92-135">String</span></span>

<span data-ttu-id="dcd92-136">' Name ' 매개 변수는 파이프라인에서 ' String ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcd92-136">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="dcd92-137">출력</span><span class="sxs-lookup"><span data-stu-id="dcd92-137">OUTPUTS</span></span>

## <span data-ttu-id="dcd92-138">상속자</span><span class="sxs-lookup"><span data-stu-id="dcd92-138">NOTES</span></span>

## <span data-ttu-id="dcd92-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dcd92-139">RELATED LINKS</span></span>

[<span data-ttu-id="dcd92-140">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="dcd92-140">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="dcd92-141">새로운 AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="dcd92-141">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="dcd92-142">제거-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="dcd92-142">Remove-AzureStorageShare</span></span>](./Remove-AzureStorageShare.md)
