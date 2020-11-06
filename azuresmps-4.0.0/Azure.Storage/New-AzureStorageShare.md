---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FCDCEF0B-6E2C-480E-9841-EF4E64D61D54
online version: ''
schema: 2.0.0
ms.openlocfilehash: 381bfc62ed3a80b650b61b11790a87658a75ee9d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523567"
---
# <span data-ttu-id="bf997-101">New-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="bf997-101">New-AzureStorageShare</span></span>

## <span data-ttu-id="bf997-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf997-102">SYNOPSIS</span></span>
<span data-ttu-id="bf997-103">파일 공유를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bf997-103">Creates a file share.</span></span>

## <span data-ttu-id="bf997-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bf997-104">SYNTAX</span></span>

```
New-AzureStorageShare [-Name] <String> [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="bf997-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bf997-105">DESCRIPTION</span></span>
<span data-ttu-id="bf997-106">**새 AzureStorageShare** cmdlet은 파일 공유를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bf997-106">The **New-AzureStorageShare** cmdlet creates a file share.</span></span>

## <span data-ttu-id="bf997-107">예제의</span><span class="sxs-lookup"><span data-stu-id="bf997-107">EXAMPLES</span></span>

### <span data-ttu-id="bf997-108">예제 1: 파일 공유 만들기</span><span class="sxs-lookup"><span data-stu-id="bf997-108">Example 1: Create a file share</span></span>
```
PS C:\>New-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="bf997-109">이 명령은 ContosoShare06 이라는 파일 공유를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bf997-109">This command creates a file share named ContosoShare06.</span></span>

## <span data-ttu-id="bf997-110">변수</span><span class="sxs-lookup"><span data-stu-id="bf997-110">PARAMETERS</span></span>

### <span data-ttu-id="bf997-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="bf997-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="bf997-112">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf997-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="bf997-113">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf997-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="bf997-114">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf997-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="bf997-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="bf997-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="bf997-116">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf997-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="bf997-117">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bf997-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="bf997-118">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="bf997-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="bf997-119">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bf997-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="bf997-120">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="bf997-120">The default value is 10.</span></span>

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

### <span data-ttu-id="bf997-121">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="bf997-121">-Context</span></span>
<span data-ttu-id="bf997-122">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf997-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="bf997-123">저장소 컨텍스트를 얻으려면 [새로운-AzureStorageContext](./New-AzureStorageContext.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf997-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="bf997-124">-이름</span><span class="sxs-lookup"><span data-stu-id="bf997-124">-Name</span></span>
<span data-ttu-id="bf997-125">파일 공유의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf997-125">Specifies the name of a file share.</span></span>
<span data-ttu-id="bf997-126">이 cmdlet은이 매개 변수에서 지정 하는 이름의 파일 공유를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bf997-126">This cmdlet creates a file share that has the name that this parameter specifies.</span></span>

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

### <span data-ttu-id="bf997-127">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="bf997-127">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="bf997-128">요청에 대 한 서버 부분에 대 한 시간 초과 기간의 길이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf997-128">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="bf997-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf997-129">CommonParameters</span></span>
<span data-ttu-id="bf997-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf997-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf997-131">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf997-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf997-132">입력</span><span class="sxs-lookup"><span data-stu-id="bf997-132">INPUTS</span></span>

## <span data-ttu-id="bf997-133">출력</span><span class="sxs-lookup"><span data-stu-id="bf997-133">OUTPUTS</span></span>

## <span data-ttu-id="bf997-134">상속자</span><span class="sxs-lookup"><span data-stu-id="bf997-134">NOTES</span></span>

## <span data-ttu-id="bf997-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bf997-135">RELATED LINKS</span></span>

[<span data-ttu-id="bf997-136">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="bf997-136">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="bf997-137">새로운 AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="bf997-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="bf997-138">제거-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="bf997-138">Remove-AzureStorageShare</span></span>](./Remove-AzureStorageShare.md)
