---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: FCDCEF0B-6E2C-480E-9841-EF4E64D61D54
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestorageshare
schema: 2.0.0
ms.openlocfilehash: 55ee72941f49954bcc56f9558bc7ffb444ae9e6b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882038"
---
# <span data-ttu-id="4486b-101">New-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="4486b-101">New-AzureStorageShare</span></span>

## <span data-ttu-id="4486b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4486b-102">SYNOPSIS</span></span>
<span data-ttu-id="4486b-103">파일 공유를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4486b-103">Creates a file share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4486b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4486b-104">SYNTAX</span></span>

```
New-AzureStorageShare [-Name] <String> [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="4486b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4486b-105">DESCRIPTION</span></span>
<span data-ttu-id="4486b-106">**새 AzureStorageShare** cmdlet은 파일 공유를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4486b-106">The **New-AzureStorageShare** cmdlet creates a file share.</span></span>

## <span data-ttu-id="4486b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4486b-107">EXAMPLES</span></span>

### <span data-ttu-id="4486b-108">예제 1: 파일 공유 만들기</span><span class="sxs-lookup"><span data-stu-id="4486b-108">Example 1: Create a file share</span></span>
```
PS C:\>New-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="4486b-109">이 명령은 ContosoShare06 이라는 파일 공유를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4486b-109">This command creates a file share named ContosoShare06.</span></span>

## <span data-ttu-id="4486b-110">변수</span><span class="sxs-lookup"><span data-stu-id="4486b-110">PARAMETERS</span></span>

### <span data-ttu-id="4486b-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4486b-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="4486b-112">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4486b-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="4486b-113">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="4486b-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="4486b-114">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4486b-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="4486b-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="4486b-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="4486b-116">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4486b-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="4486b-117">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4486b-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="4486b-118">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="4486b-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="4486b-119">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4486b-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="4486b-120">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="4486b-120">The default value is 10.</span></span>

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

### <span data-ttu-id="4486b-121">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="4486b-121">-Context</span></span>
<span data-ttu-id="4486b-122">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4486b-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="4486b-123">저장소 컨텍스트를 얻으려면 [새로운-AzureStorageContext](./New-AzureStorageContext.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4486b-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="4486b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4486b-124">-DefaultProfile</span></span>
<span data-ttu-id="4486b-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4486b-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4486b-126">-이름</span><span class="sxs-lookup"><span data-stu-id="4486b-126">-Name</span></span>
<span data-ttu-id="4486b-127">파일 공유의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4486b-127">Specifies the name of a file share.</span></span>
<span data-ttu-id="4486b-128">이 cmdlet은이 매개 변수에서 지정 하는 이름의 파일 공유를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4486b-128">This cmdlet creates a file share that has the name that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4486b-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4486b-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="4486b-130">요청에 대 한 서버 부분에 대 한 시간 초과 기간의 길이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4486b-130">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="4486b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4486b-131">CommonParameters</span></span>
<span data-ttu-id="4486b-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4486b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4486b-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4486b-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4486b-134">입력</span><span class="sxs-lookup"><span data-stu-id="4486b-134">INPUTS</span></span>

### <span data-ttu-id="4486b-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4486b-135">System.String</span></span>

### <span data-ttu-id="4486b-136">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4486b-136">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4486b-137">출력</span><span class="sxs-lookup"><span data-stu-id="4486b-137">OUTPUTS</span></span>

### <span data-ttu-id="4486b-138">WindowsAzure 파일. c a c 공유</span><span class="sxs-lookup"><span data-stu-id="4486b-138">Microsoft.WindowsAzure.Storage.File.CloudFileShare</span></span>

## <span data-ttu-id="4486b-139">상속자</span><span class="sxs-lookup"><span data-stu-id="4486b-139">NOTES</span></span>

## <span data-ttu-id="4486b-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4486b-140">RELATED LINKS</span></span>

[<span data-ttu-id="4486b-141">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="4486b-141">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="4486b-142">새로운 AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="4486b-142">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="4486b-143">제거-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="4486b-143">Remove-AzureStorageShare</span></span>](./Remove-AzureStorageShare.md)