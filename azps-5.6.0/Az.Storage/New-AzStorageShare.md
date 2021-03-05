---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FCDCEF0B-6E2C-480E-9841-EF4E64D61D54
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShare.md
ms.openlocfilehash: 492ad3713bafa692d0ddf969540b8cab89fc05a2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002363"
---
# <span data-ttu-id="158a9-101">New-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="158a9-101">New-AzStorageShare</span></span>

## <span data-ttu-id="158a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="158a9-102">SYNOPSIS</span></span>
<span data-ttu-id="158a9-103">파일 공유를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="158a9-103">Creates a file share.</span></span>

## <span data-ttu-id="158a9-104">구문</span><span class="sxs-lookup"><span data-stu-id="158a9-104">SYNTAX</span></span>

```
New-AzStorageShare [-Name] <String> [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="158a9-105">설명</span><span class="sxs-lookup"><span data-stu-id="158a9-105">DESCRIPTION</span></span>
<span data-ttu-id="158a9-106">**New-AzStorageShare** cmdlet은 파일 공유를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="158a9-106">The **New-AzStorageShare** cmdlet creates a file share.</span></span>

## <span data-ttu-id="158a9-107">예제</span><span class="sxs-lookup"><span data-stu-id="158a9-107">EXAMPLES</span></span>

### <span data-ttu-id="158a9-108">예제 1: 파일 공유 만들기</span><span class="sxs-lookup"><span data-stu-id="158a9-108">Example 1: Create a file share</span></span>
```
PS C:\>New-AzStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="158a9-109">이 명령은 ContosoShare06이라는 파일 공유를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="158a9-109">This command creates a file share named ContosoShare06.</span></span>

## <span data-ttu-id="158a9-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="158a9-110">PARAMETERS</span></span>

### <span data-ttu-id="158a9-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="158a9-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="158a9-112">하나의 서비스 요청에 대해 클라이언트 쪽 시간 간격(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="158a9-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="158a9-113">지정된 간격에서 이전 호출이 실패하면 이 cmdlet에서 요청을 다시 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="158a9-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="158a9-114">간격이 경과하기 전에 이 cmdlet에서 성공적인 응답을 받지 못하면 이 cmdlet은 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="158a9-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="158a9-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="158a9-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="158a9-116">최대 동시 네트워크 호출을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="158a9-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="158a9-117">이 매개 변수를 사용하여 최대 동시 네트워크 호출 수를 지정하여 로컬 CPU 및 대역폭 사용량을 제한하는 동시성 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="158a9-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="158a9-118">지정된 값은 절대 개수로 코어 수에 곱하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="158a9-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="158a9-119">이 매개 변수는 초당 100킬로비트와 같은 대역폭이 낮은 환경에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="158a9-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="158a9-120">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="158a9-120">The default value is 10.</span></span>

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

### <span data-ttu-id="158a9-121">-Context</span><span class="sxs-lookup"><span data-stu-id="158a9-121">-Context</span></span>
<span data-ttu-id="158a9-122">Azure Storage 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="158a9-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="158a9-123">저장소 컨텍스트를 구하기 위해 [New-AzStorageContext](./New-AzStorageContext.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="158a9-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="158a9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="158a9-124">-DefaultProfile</span></span>
<span data-ttu-id="158a9-125">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="158a9-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="158a9-126">-Name</span><span class="sxs-lookup"><span data-stu-id="158a9-126">-Name</span></span>
<span data-ttu-id="158a9-127">파일 공유의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="158a9-127">Specifies the name of a file share.</span></span>
<span data-ttu-id="158a9-128">이 cmdlet은 이 매개 변수가 지정하는 이름이 있는 파일 공유를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="158a9-128">This cmdlet creates a file share that has the name that this parameter specifies.</span></span>

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

### <span data-ttu-id="158a9-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="158a9-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="158a9-130">요청의 서버 부분에 대한 시간 제한 기간의 길이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="158a9-130">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="158a9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="158a9-131">CommonParameters</span></span>
<span data-ttu-id="158a9-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="158a9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="158a9-133">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="158a9-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="158a9-134">입력</span><span class="sxs-lookup"><span data-stu-id="158a9-134">INPUTS</span></span>

### <span data-ttu-id="158a9-135">System.String</span><span class="sxs-lookup"><span data-stu-id="158a9-135">System.String</span></span>

### <span data-ttu-id="158a9-136">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="158a9-136">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="158a9-137">출력</span><span class="sxs-lookup"><span data-stu-id="158a9-137">OUTPUTS</span></span>

### <span data-ttu-id="158a9-138">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span><span class="sxs-lookup"><span data-stu-id="158a9-138">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span></span>

## <span data-ttu-id="158a9-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="158a9-139">NOTES</span></span>

## <span data-ttu-id="158a9-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="158a9-140">RELATED LINKS</span></span>

[<span data-ttu-id="158a9-141">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="158a9-141">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="158a9-142">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="158a9-142">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="158a9-143">Remove-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="158a9-143">Remove-AzStorageShare</span></span>](./Remove-AzStorageShare.md)
