---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 176294FA-BB08-4A63-AD45-1E6C6D67A5D8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 778c5020dc47bc8db7bda664b2e352045d851dfd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93524127"
---
# <span data-ttu-id="09bbe-101">Set-AzureStorageShareQuota</span><span class="sxs-lookup"><span data-stu-id="09bbe-101">Set-AzureStorageShareQuota</span></span>

## <span data-ttu-id="09bbe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09bbe-102">SYNOPSIS</span></span>
<span data-ttu-id="09bbe-103">공유에 대 한 저장소 용량을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="09bbe-103">Sets the storage capacity for a share.</span></span>

## <span data-ttu-id="09bbe-104">구문과</span><span class="sxs-lookup"><span data-stu-id="09bbe-104">SYNTAX</span></span>

### <span data-ttu-id="09bbe-105">ShareName</span><span class="sxs-lookup"><span data-stu-id="09bbe-105">ShareName</span></span>
```
Set-AzureStorageShareQuota [-ShareName] <String> [-Quota] <Int32> [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="09bbe-106">공유</span><span class="sxs-lookup"><span data-stu-id="09bbe-106">Share</span></span>
```
Set-AzureStorageShareQuota [-Share] <CloudFileShare> [-Quota] <Int32> [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="09bbe-107">설명은</span><span class="sxs-lookup"><span data-stu-id="09bbe-107">DESCRIPTION</span></span>
<span data-ttu-id="09bbe-108">**AzureStorageShareQuota** cmdlet은 지정 된 공유에 대 한 저장소 용량을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="09bbe-108">The **Set-AzureStorageShareQuota** cmdlet sets the storage capacity for a specified share.</span></span>

## <span data-ttu-id="09bbe-109">예제의</span><span class="sxs-lookup"><span data-stu-id="09bbe-109">EXAMPLES</span></span>

### <span data-ttu-id="09bbe-110">예제 1: 공유 저장소 용량 설정</span><span class="sxs-lookup"><span data-stu-id="09bbe-110">Example 1: Set the storage capacity of a share</span></span>
```
PS C:\>Set-AzureStorageShareQuota -ShareName "ContosoShare01" -Quota 1024
```

<span data-ttu-id="09bbe-111">이 명령은 ContosoShare01 이라는 공유에 대 한 저장소 용량을 1024 GB로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="09bbe-111">This command sets the storage capacity for a share named ContosoShare01 to 1024 GB.</span></span>

## <span data-ttu-id="09bbe-112">변수</span><span class="sxs-lookup"><span data-stu-id="09bbe-112">PARAMETERS</span></span>

### <span data-ttu-id="09bbe-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="09bbe-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="09bbe-114">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="09bbe-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="09bbe-115">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="09bbe-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="09bbe-116">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="09bbe-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="09bbe-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="09bbe-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="09bbe-118">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="09bbe-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="09bbe-119">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="09bbe-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="09bbe-120">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="09bbe-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="09bbe-121">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="09bbe-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="09bbe-122">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="09bbe-122">The default value is 10.</span></span>

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

### <span data-ttu-id="09bbe-123">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="09bbe-123">-Context</span></span>
<span data-ttu-id="09bbe-124">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="09bbe-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="09bbe-125">저장소 컨텍스트를 얻으려면 [새로운-AzureStorageContext](./New-AzureStorageContext.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="09bbe-125">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: ShareName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09bbe-126">-할당량</span><span class="sxs-lookup"><span data-stu-id="09bbe-126">-Quota</span></span>
<span data-ttu-id="09bbe-127">할당량 값을 기가바이트 (GB)로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="09bbe-127">Specifies the quota value in gigabytes (GB).</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09bbe-128">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="09bbe-128">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="09bbe-129">요청에 대 한 서버 부분에 대 한 시간 초과 기간의 길이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="09bbe-129">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="09bbe-130">-공유</span><span class="sxs-lookup"><span data-stu-id="09bbe-130">-Share</span></span>
<span data-ttu-id="09bbe-131">이 cmdlet이 할당량을 설정 하는 공유를 나타내기 위해 **cloudfileshare** 되지 않는 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="09bbe-131">Specifies a **CloudFileShare** object to represent the share for which this cmdlets sets a quota.</span></span>
<span data-ttu-id="09bbe-132">**Cloudfileshare** 되지 않는 개체를 가져오려면 Get-AzureStorageShare cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="09bbe-132">To obtain a **CloudFileShare** object, use the Get-AzureStorageShare cmdlet.</span></span>

```yaml
Type: CloudFileShare
Parameter Sets: Share
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09bbe-133">-ShareName</span><span class="sxs-lookup"><span data-stu-id="09bbe-133">-ShareName</span></span>
<span data-ttu-id="09bbe-134">할당량을 설정할 파일 공유의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="09bbe-134">Specifies the name of the file share for which to set a quota.</span></span>

```yaml
Type: String
Parameter Sets: ShareName
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09bbe-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09bbe-135">CommonParameters</span></span>
<span data-ttu-id="09bbe-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="09bbe-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09bbe-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09bbe-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09bbe-138">입력</span><span class="sxs-lookup"><span data-stu-id="09bbe-138">INPUTS</span></span>

## <span data-ttu-id="09bbe-139">출력</span><span class="sxs-lookup"><span data-stu-id="09bbe-139">OUTPUTS</span></span>

## <span data-ttu-id="09bbe-140">상속자</span><span class="sxs-lookup"><span data-stu-id="09bbe-140">NOTES</span></span>

## <span data-ttu-id="09bbe-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="09bbe-141">RELATED LINKS</span></span>

[<span data-ttu-id="09bbe-142">Get-AzureStorageFileContent</span><span class="sxs-lookup"><span data-stu-id="09bbe-142">Get-AzureStorageFileContent</span></span>](./Get-AzureStorageFileContent.md)

[<span data-ttu-id="09bbe-143">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="09bbe-143">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="09bbe-144">새로운 AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="09bbe-144">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)
