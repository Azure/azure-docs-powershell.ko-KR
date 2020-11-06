---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 37E76360-B683-407C-9AEF-7138374562D8
online version: ''
schema: 2.0.0
ms.openlocfilehash: f76cd56055e800dc5d7d5ac15e66be23621ffbe2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523324"
---
# <span data-ttu-id="03369-101">New-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="03369-101">New-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="03369-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03369-102">SYNOPSIS</span></span>
<span data-ttu-id="03369-103">저장소 공유에 저장 된 액세스 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="03369-103">Creates a stored access policy on a Storage share.</span></span>

## <span data-ttu-id="03369-104">구문과</span><span class="sxs-lookup"><span data-stu-id="03369-104">SYNTAX</span></span>

```
New-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="03369-105">설명은</span><span class="sxs-lookup"><span data-stu-id="03369-105">DESCRIPTION</span></span>
<span data-ttu-id="03369-106">**AzureStorageShareStoredAccessPolicy** Cmdlet은 Azure 저장소 공유에 저장 된 액세스 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="03369-106">The **New-AzureStorageShareStoredAccessPolicy** cmdlet creates a stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="03369-107">예제의</span><span class="sxs-lookup"><span data-stu-id="03369-107">EXAMPLES</span></span>

### <span data-ttu-id="03369-108">예제 1: 공유에 저장 된 액세스 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="03369-108">Example 1: Create a stored access policy in a share</span></span>
```
PS C:\>New-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="03369-109">이 명령은 공유에 모든 권한이 있는 저장 된 액세스 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="03369-109">This command creates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="03369-110">변수</span><span class="sxs-lookup"><span data-stu-id="03369-110">PARAMETERS</span></span>

### <span data-ttu-id="03369-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="03369-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="03369-112">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="03369-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="03369-113">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="03369-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="03369-114">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="03369-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="03369-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="03369-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="03369-116">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="03369-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="03369-117">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03369-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="03369-118">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="03369-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="03369-119">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="03369-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="03369-120">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="03369-120">The default value is 10.</span></span>

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

### <span data-ttu-id="03369-121">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="03369-121">-Context</span></span>
<span data-ttu-id="03369-122">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="03369-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="03369-123">저장소 컨텍스트를 얻으려면 [새로운-AzureStorageContext](./New-AzureStorageContext.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="03369-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="03369-124">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="03369-124">-ExpiryTime</span></span>
<span data-ttu-id="03369-125">저장 된 액세스 정책이 무효화 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="03369-125">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03369-126">-사용 권한</span><span class="sxs-lookup"><span data-stu-id="03369-126">-Permission</span></span>
<span data-ttu-id="03369-127">저장 된 액세스 정책에서 저장소 공유 또는 그 아래에 있는 파일에 액세스 하는 데 필요한 사용 권한을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="03369-127">Specifies permissions in the stored access policy to access the Storage share or files under it.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03369-128">-정책</span><span class="sxs-lookup"><span data-stu-id="03369-128">-Policy</span></span>
<span data-ttu-id="03369-129">저장 된 액세스 정책의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="03369-129">Specifies a name for the stored access policy.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03369-130">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="03369-130">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="03369-131">요청에 대 한 서버 부분에 대 한 시간 초과 기간의 길이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="03369-131">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="03369-132">-ShareName</span><span class="sxs-lookup"><span data-stu-id="03369-132">-ShareName</span></span>
<span data-ttu-id="03369-133">저장소 공유의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="03369-133">Specifies the name of the Storage share.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="03369-134">-StartTime</span><span class="sxs-lookup"><span data-stu-id="03369-134">-StartTime</span></span>
<span data-ttu-id="03369-135">저장 된 액세스 정책이 유효 하 게 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="03369-135">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="03369-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03369-136">CommonParameters</span></span>
<span data-ttu-id="03369-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="03369-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03369-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03369-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03369-139">입력</span><span class="sxs-lookup"><span data-stu-id="03369-139">INPUTS</span></span>

## <span data-ttu-id="03369-140">출력</span><span class="sxs-lookup"><span data-stu-id="03369-140">OUTPUTS</span></span>

## <span data-ttu-id="03369-141">상속자</span><span class="sxs-lookup"><span data-stu-id="03369-141">NOTES</span></span>

## <span data-ttu-id="03369-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="03369-142">RELATED LINKS</span></span>

[<span data-ttu-id="03369-143">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="03369-143">Get-AzureStorageShareStoredAccessPolicy</span></span>](./Get-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="03369-144">새로운 AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="03369-144">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="03369-145">제거-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="03369-145">Remove-AzureStorageShareStoredAccessPolicy</span></span>](./Remove-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="03369-146">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="03369-146">Set-AzureStorageShareStoredAccessPolicy</span></span>](./Set-AzureStorageShareStoredAccessPolicy.md)
