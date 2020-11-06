---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FD3A0013-4365-4E65-891C-5C50A9D5658C
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageShare.md
ms.openlocfilehash: c0c3aedf6c92df8b81beed92ef4ea779dd8ff131
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530615"
---
# <span data-ttu-id="c6320-101">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="c6320-101">Get-AzureStorageShare</span></span>

## <span data-ttu-id="c6320-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6320-102">SYNOPSIS</span></span>
<span data-ttu-id="c6320-103">파일 공유 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c6320-103">Gets a list of file shares.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6320-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c6320-104">SYNTAX</span></span>

### <span data-ttu-id="c6320-105">MatchingPrefix (기본값)</span><span class="sxs-lookup"><span data-stu-id="c6320-105">MatchingPrefix (Default)</span></span>
```
Get-AzureStorageShare [[-Prefix] <String>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="c6320-106">만</span><span class="sxs-lookup"><span data-stu-id="c6320-106">Specific</span></span>
```
Get-AzureStorageShare [-Name] <String> [-SnapshotTime <DateTimeOffset>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="c6320-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c6320-107">DESCRIPTION</span></span>
<span data-ttu-id="c6320-108">**AzureStorageShare** cmdlet은 저장소 계정의 파일 공유 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c6320-108">The **Get-AzureStorageShare** cmdlet gets a list of file shares for a storage account.</span></span>

## <span data-ttu-id="c6320-109">예제의</span><span class="sxs-lookup"><span data-stu-id="c6320-109">EXAMPLES</span></span>

### <span data-ttu-id="c6320-110">예제 1: 파일 공유 가져오기</span><span class="sxs-lookup"><span data-stu-id="c6320-110">Example 1: Get a file share</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="c6320-111">이 명령은 ContosoShare06 이라는 파일 공유를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c6320-111">This command gets the file share named ContosoShare06.</span></span>

### <span data-ttu-id="c6320-112">예제 2: 문자열로 시작 하는 모든 파일 공유 가져오기</span><span class="sxs-lookup"><span data-stu-id="c6320-112">Example 2: Get all file shares that begin with a string</span></span>
```
PS C:\>Get-AzureStorageShare -Prefix "Contoso"
```

<span data-ttu-id="c6320-113">이 명령은 Contoso로 시작 하는 이름의 모든 파일 공유를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c6320-113">This command gets all file shares that have names that begin with Contoso.</span></span>

### <span data-ttu-id="c6320-114">예제 3: 지정 된 컨텍스트에서 모든 파일 공유 가져오기</span><span class="sxs-lookup"><span data-stu-id="c6320-114">Example 3: Get all file shares in a specified context</span></span>
```
PS C:\>$Context = New-AzureStorageContext -Local
PS C:\> Get-AzureStorageShare -Context $Context
```

<span data-ttu-id="c6320-115">첫 번째 명령은 **New AzureStorageContext** cmdlet을 사용 하 여 *Local* 매개 변수를 사용 하 여 컨텍스트를 만든 다음 해당 컨텍스트 개체를 $Context 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6320-115">The first command uses the **New-AzureStorageContext** cmdlet to create a context by using the *Local* parameter, and then stores that context object in the $Context variable.</span></span>

<span data-ttu-id="c6320-116">두 번째 명령은 $Context에 저장 된 컨텍스트 개체에 대 한 파일 공유를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c6320-116">The second command gets the file shares for the context object stored in $Context.</span></span>

### <span data-ttu-id="c6320-117">예제 4: 특정 공유 이름 및 SnapshotTime을 사용 하 여 파일 공유 스냅숏 가져오기</span><span class="sxs-lookup"><span data-stu-id="c6320-117">Example 4: Get a file share snapshot with specific share name and SnapshotTime</span></span>
```
PS C:\>Get-AzureStorageShare -Name "ContosoShare06" -SnapshotTime "6/16/2017 9:48:41 AM +00:00"
```

<span data-ttu-id="c6320-118">이 명령은 특정 공유 이름 및 SnapshotTime을 사용 하 여 파일 공유 스냅숏을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c6320-118">This command gets a file share snapshot with specific share name and SnapshotTime.</span></span>

## <span data-ttu-id="c6320-119">변수</span><span class="sxs-lookup"><span data-stu-id="c6320-119">PARAMETERS</span></span>

### <span data-ttu-id="c6320-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c6320-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="c6320-121">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6320-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="c6320-122">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6320-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="c6320-123">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6320-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="c6320-124">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="c6320-124">-ConcurrentTaskCount</span></span>
<span data-ttu-id="c6320-125">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6320-125">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="c6320-126">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c6320-126">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="c6320-127">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="c6320-127">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="c6320-128">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c6320-128">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="c6320-129">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="c6320-129">The default value is 10.</span></span>

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

### <span data-ttu-id="c6320-130">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="c6320-130">-Context</span></span>
<span data-ttu-id="c6320-131">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6320-131">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="c6320-132">컨텍스트를 가져오려면 [새로운-AzureStorageContext](./New-AzureStorageContext.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6320-132">To obtain a context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="c6320-133">-이름</span><span class="sxs-lookup"><span data-stu-id="c6320-133">-Name</span></span>
<span data-ttu-id="c6320-134">파일 공유의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6320-134">Specifies the name of the file share.</span></span>
<span data-ttu-id="c6320-135">이 cmdlet은이 매개 변수에서 지정 하는 파일 공유를 가져오거나 존재 하지 않는 파일 공유의 이름을 지정 하는 경우 아무 작업도 수행 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c6320-135">This cmdlet gets the file share that this parameter specifies, or nothing if you specify the name of a file share that does not exist.</span></span>

```yaml
Type: String
Parameter Sets: Specific
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6320-136">-접두사</span><span class="sxs-lookup"><span data-stu-id="c6320-136">-Prefix</span></span>
<span data-ttu-id="c6320-137">파일 공유에 대 한 접두사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6320-137">Specifies the prefix for file shares.</span></span>
<span data-ttu-id="c6320-138">이 cmdlet은이 매개 변수에서 지정 하는 접두사와 일치 하는 파일 공유를 가져오거나 지정 된 접두사와 일치 하는 파일 공유가 없는 경우 파일 공유를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c6320-138">This cmdlet gets file shares that match the prefix that this parameter specifies, or no file shares if no file shares match the specified prefix.</span></span>

```yaml
Type: String
Parameter Sets: MatchingPrefix
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6320-139">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c6320-139">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="c6320-140">요청에 대 한 서버 부분에 대 한 시간 초과 기간의 길이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6320-140">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="c6320-141">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="c6320-141">-SnapshotTime</span></span>
<span data-ttu-id="c6320-142">수신할 파일 공유 스냅숏의 SnapshotTime.</span><span class="sxs-lookup"><span data-stu-id="c6320-142">SnapshotTime of the file share snapshot to be received.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: Specific
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6320-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6320-143">CommonParameters</span></span>
<span data-ttu-id="c6320-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6320-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6320-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6320-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6320-146">입력</span><span class="sxs-lookup"><span data-stu-id="c6320-146">INPUTS</span></span>

### <span data-ttu-id="c6320-147">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c6320-147">IStorageContext</span></span>

<span data-ttu-id="c6320-148">' Context ' 매개 변수는 파이프라인에서 ' IStorageContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c6320-148">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="c6320-149">출력</span><span class="sxs-lookup"><span data-stu-id="c6320-149">OUTPUTS</span></span>

## <span data-ttu-id="c6320-150">상속자</span><span class="sxs-lookup"><span data-stu-id="c6320-150">NOTES</span></span>

## <span data-ttu-id="c6320-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c6320-151">RELATED LINKS</span></span>

[<span data-ttu-id="c6320-152">새로운 AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="c6320-152">New-AzureStorageShare</span></span>](./New-AzureStorageShare.md)

[<span data-ttu-id="c6320-153">제거-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="c6320-153">Remove-AzureStorageShare</span></span>](./Remove-AzureStorageShare.md)
