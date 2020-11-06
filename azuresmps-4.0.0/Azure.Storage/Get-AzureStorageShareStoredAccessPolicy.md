---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 73BB521B-20F2-4F2B-AA88-2B128F36A9EF
online version: ''
schema: 2.0.0
ms.openlocfilehash: cbc7268d3d7d233f6a3fafeb92540e23ae3eaa6c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523999"
---
# <span data-ttu-id="a01e0-101">Get-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a01e0-101">Get-AzureStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="a01e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a01e0-102">SYNOPSIS</span></span>
<span data-ttu-id="a01e0-103">저장소 공유에 대 한 저장 된 액세스 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a01e0-103">Gets stored access policies for a Storage share.</span></span>

## <span data-ttu-id="a01e0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a01e0-104">SYNTAX</span></span>

```
Get-AzureStorageShareStoredAccessPolicy [-ShareName] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="a01e0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a01e0-105">DESCRIPTION</span></span>
<span data-ttu-id="a01e0-106">**AzureStorageShareStoredAccessPolicy** Cmdlet은 Azure 저장소 공유에 대 한 저장 된 액세스 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a01e0-106">The **Get-AzureStorageShareStoredAccessPolicy** cmdlet gets stored access policies for an Azure Storage share.</span></span>
<span data-ttu-id="a01e0-107">특정 정책을 가져오려면 name을 기준으로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a01e0-107">To get a particular policy, specify it by name.</span></span>

## <span data-ttu-id="a01e0-108">예제의</span><span class="sxs-lookup"><span data-stu-id="a01e0-108">EXAMPLES</span></span>

### <span data-ttu-id="a01e0-109">예제 1: 공유에 저장 된 액세스 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="a01e0-109">Example 1: Get a stored access policy in a share</span></span>
```
PS C:\>Get-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="a01e0-110">이 명령은 ContosoShare의 일반 Policy (저장 된 액세스 정책)를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a01e0-110">This command gets a stored access policy named GeneralPolicy in ContosoShare.</span></span>

### <span data-ttu-id="a01e0-111">예제 2: 공유에 저장 된 모든 액세스 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="a01e0-111">Example 2: Get all the stored access policies in share</span></span>
```
PS C:\>Get-AzureStorageShareStoredAccessPolicy -ShareName "ContosoShare"
```

<span data-ttu-id="a01e0-112">이 명령은 ContosoShare에 저장 된 모든 액세스 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a01e0-112">This command gets all stored access policies in ContosoShare.</span></span>

## <span data-ttu-id="a01e0-113">변수</span><span class="sxs-lookup"><span data-stu-id="a01e0-113">PARAMETERS</span></span>

### <span data-ttu-id="a01e0-114">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a01e0-114">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="a01e0-115">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a01e0-115">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="a01e0-116">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="a01e0-116">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="a01e0-117">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a01e0-117">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="a01e0-118">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="a01e0-118">-ConcurrentTaskCount</span></span>
<span data-ttu-id="a01e0-119">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a01e0-119">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="a01e0-120">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a01e0-120">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="a01e0-121">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="a01e0-121">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="a01e0-122">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a01e0-122">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="a01e0-123">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="a01e0-123">The default value is 10.</span></span>

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

### <span data-ttu-id="a01e0-124">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="a01e0-124">-Context</span></span>
<span data-ttu-id="a01e0-125">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a01e0-125">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="a01e0-126">컨텍스트를 가져오려면 [새로운-AzureStorageContext](./New-AzureStorageContext.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a01e0-126">To obtain a context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="a01e0-127">-정책</span><span class="sxs-lookup"><span data-stu-id="a01e0-127">-Policy</span></span>
<span data-ttu-id="a01e0-128">이 cmdlet이 가져오는 저장 된 액세스 정책의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a01e0-128">Specifies the name of the stored access policy that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a01e0-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="a01e0-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="a01e0-130">요청에 대 한 서버 부분에 대 한 시간 초과 기간의 길이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a01e0-130">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="a01e0-131">-ShareName</span><span class="sxs-lookup"><span data-stu-id="a01e0-131">-ShareName</span></span>
<span data-ttu-id="a01e0-132">이 cmdlet에서 정책을 가져오는 저장소 공유 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a01e0-132">Specifies the Storage share name for which this cmdlet gets policies.</span></span>

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

### <span data-ttu-id="a01e0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a01e0-133">CommonParameters</span></span>
<span data-ttu-id="a01e0-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a01e0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a01e0-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a01e0-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a01e0-136">입력</span><span class="sxs-lookup"><span data-stu-id="a01e0-136">INPUTS</span></span>

## <span data-ttu-id="a01e0-137">출력</span><span class="sxs-lookup"><span data-stu-id="a01e0-137">OUTPUTS</span></span>

## <span data-ttu-id="a01e0-138">상속자</span><span class="sxs-lookup"><span data-stu-id="a01e0-138">NOTES</span></span>

## <span data-ttu-id="a01e0-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a01e0-139">RELATED LINKS</span></span>

[<span data-ttu-id="a01e0-140">새로운 AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="a01e0-140">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="a01e0-141">새로운 AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a01e0-141">New-AzureStorageShareStoredAccessPolicy</span></span>](./New-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="a01e0-142">제거-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a01e0-142">Remove-AzureStorageShareStoredAccessPolicy</span></span>](./Remove-AzureStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="a01e0-143">Set-AzureStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a01e0-143">Set-AzureStorageShareStoredAccessPolicy</span></span>](./Set-AzureStorageShareStoredAccessPolicy.md)
