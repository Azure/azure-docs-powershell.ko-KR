---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FD3A0013-4365-4E65-891C-5C50A9D5658C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageShare.md
ms.openlocfilehash: b6323cd751d25038ff6705cee45594796d782326
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374004"
---
# <span data-ttu-id="0738c-101">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="0738c-101">Get-AzStorageShare</span></span>

## <span data-ttu-id="0738c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0738c-102">SYNOPSIS</span></span>
<span data-ttu-id="0738c-103">파일 공유 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0738c-103">Gets a list of file shares.</span></span>

## <span data-ttu-id="0738c-104">구문</span><span class="sxs-lookup"><span data-stu-id="0738c-104">SYNTAX</span></span>

### <span data-ttu-id="0738c-105">MatchingPrefix(기본값)</span><span class="sxs-lookup"><span data-stu-id="0738c-105">MatchingPrefix (Default)</span></span>
```
Get-AzStorageShare [[-Prefix] <String>] [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="0738c-106">특정</span><span class="sxs-lookup"><span data-stu-id="0738c-106">Specific</span></span>
```
Get-AzStorageShare [-Name] <String> [[-SnapshotTime] <DateTimeOffset>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="0738c-107">설명</span><span class="sxs-lookup"><span data-stu-id="0738c-107">DESCRIPTION</span></span>
<span data-ttu-id="0738c-108">**Get-AzStorageShare** cmdlet은 저장소 계정에 대한 파일 공유 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0738c-108">The **Get-AzStorageShare** cmdlet gets a list of file shares for a storage account.</span></span>

## <span data-ttu-id="0738c-109">예제</span><span class="sxs-lookup"><span data-stu-id="0738c-109">EXAMPLES</span></span>

### <span data-ttu-id="0738c-110">예제 1: 파일 공유 다운로드</span><span class="sxs-lookup"><span data-stu-id="0738c-110">Example 1: Get a file share</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="0738c-111">이 명령은 ContosoShare06이라는 파일 공유를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0738c-111">This command gets the file share named ContosoShare06.</span></span>

### <span data-ttu-id="0738c-112">예제 2: 문자열로 시작하는 모든 파일 공유를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0738c-112">Example 2: Get all file shares that begin with a string</span></span>
```
PS C:\>Get-AzStorageShare -Prefix "Contoso"
```

<span data-ttu-id="0738c-113">이 명령은 Contoso로 시작하는 이름이 있는 모든 파일 공유를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0738c-113">This command gets all file shares that have names that begin with Contoso.</span></span>

### <span data-ttu-id="0738c-114">예제 3: 지정된 컨텍스트에서 모든 파일 공유를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0738c-114">Example 3: Get all file shares in a specified context</span></span>
```
PS C:\>$Context = New-AzStorageContext -Local
PS C:\> Get-AzStorageShare -Context $Context
```

<span data-ttu-id="0738c-115">첫 번째 명령은 **New-AzStorageContext** cmdlet을 사용하여 *로컬* 매개 변수를 사용하여 컨텍스트를 만든 다음 해당 컨텍스트 개체를 $Context 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="0738c-115">The first command uses the **New-AzStorageContext** cmdlet to create a context by using the *Local* parameter, and then stores that context object in the $Context variable.</span></span>
<span data-ttu-id="0738c-116">두 번째 명령은 로컬에 저장된 컨텍스트 개체에 대한 파일 공유를 $Context.</span><span class="sxs-lookup"><span data-stu-id="0738c-116">The second command gets the file shares for the context object stored in $Context.</span></span>

### <span data-ttu-id="0738c-117">예제 4: 특정 공유 이름 및 SnapshotTime으로 파일 공유 스냅숏 만들기</span><span class="sxs-lookup"><span data-stu-id="0738c-117">Example 4: Get a file share snapshot with specific share name and SnapshotTime</span></span>
```
PS C:\>Get-AzStorageShare -Name "ContosoShare06" -SnapshotTime "6/16/2017 9:48:41 AM +00:00"
```

<span data-ttu-id="0738c-118">이 명령은 특정 공유 이름 및 SnapshotTime을 사용하여 파일 공유 스냅숏을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0738c-118">This command gets a file share snapshot with specific share name and SnapshotTime.</span></span>

## <span data-ttu-id="0738c-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0738c-119">PARAMETERS</span></span>

### <span data-ttu-id="0738c-120">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0738c-120">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="0738c-121">하나의 서비스 요청에 대해 클라이언트 쪽 시간(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0738c-121">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="0738c-122">이전 호출이 지정된 간격에서 실패하는 경우 이 cmdlet은 요청을 다시 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="0738c-122">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="0738c-123">이 cmdlet이 간격이 경과하기 전에 성공적인 응답을 받지 못하면 이 cmdlet은 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="0738c-123">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="0738c-124">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="0738c-124">-ConcurrentTaskCount</span></span>
<span data-ttu-id="0738c-125">최대 동시 네트워크 호출을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0738c-125">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="0738c-126">이 매개 변수를 사용하여 최대 동시 네트워크 호출 수를 지정하여 동시성으로 로컬 CPU 및 대역폭 사용량을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0738c-126">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="0738c-127">지정된 값은 절대 개수로, 코어 수에 곱하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0738c-127">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="0738c-128">이 매개 변수는 초당 100킬로비트와 같은 낮은 대역폭 환경에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0738c-128">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="0738c-129">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="0738c-129">The default value is 10.</span></span>

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

### <span data-ttu-id="0738c-130">-Context</span><span class="sxs-lookup"><span data-stu-id="0738c-130">-Context</span></span>
<span data-ttu-id="0738c-131">Azure Storage 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0738c-131">Specifies an Azure Storage context.</span></span>
<span data-ttu-id="0738c-132">컨텍스트를 얻습니다. [New-AzStorageContext](./New-AzStorageContext.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0738c-132">To obtain a context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="0738c-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0738c-133">-DefaultProfile</span></span>
<span data-ttu-id="0738c-134">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0738c-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0738c-135">-Name</span><span class="sxs-lookup"><span data-stu-id="0738c-135">-Name</span></span>
<span data-ttu-id="0738c-136">파일 공유의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0738c-136">Specifies the name of the file share.</span></span>
<span data-ttu-id="0738c-137">이 cmdlet은 이 매개 변수가 지정하는 파일 공유를 얻거나 존재하지 않는 파일 공유의 이름을 지정하는 경우 아무 것도 얻지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0738c-137">This cmdlet gets the file share that this parameter specifies, or nothing if you specify the name of a file share that does not exist.</span></span>

```yaml
Type: System.String
Parameter Sets: Specific
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0738c-138">-Prefix</span><span class="sxs-lookup"><span data-stu-id="0738c-138">-Prefix</span></span>
<span data-ttu-id="0738c-139">파일 공유에 대한 prefix를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0738c-139">Specifies the prefix for file shares.</span></span>
<span data-ttu-id="0738c-140">이 cmdlet은 이 매개 변수가 지정한 사전과 일치하는 파일 공유를 얻거나, 지정된 연결과 일치하는 파일 공유가 없는 경우 파일 공유를 얻지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0738c-140">This cmdlet gets file shares that match the prefix that this parameter specifies, or no file shares if no file shares match the specified prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: MatchingPrefix
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0738c-141">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0738c-141">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="0738c-142">요청의 서버 부분에 대한 시간 제한 기간의 길이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0738c-142">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="0738c-143">-SnapshotTime</span><span class="sxs-lookup"><span data-stu-id="0738c-143">-SnapshotTime</span></span>
<span data-ttu-id="0738c-144">수신할 파일 공유 스냅숏의 SnapshotTime입니다.</span><span class="sxs-lookup"><span data-stu-id="0738c-144">SnapshotTime of the file share snapshot to be received.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: Specific
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0738c-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0738c-145">CommonParameters</span></span>
<span data-ttu-id="0738c-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0738c-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0738c-147">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0738c-147">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0738c-148">입력</span><span class="sxs-lookup"><span data-stu-id="0738c-148">INPUTS</span></span>

### <span data-ttu-id="0738c-149">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0738c-149">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0738c-150">출력</span><span class="sxs-lookup"><span data-stu-id="0738c-150">OUTPUTS</span></span>

### <span data-ttu-id="0738c-151">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span><span class="sxs-lookup"><span data-stu-id="0738c-151">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span></span>

## <span data-ttu-id="0738c-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0738c-152">NOTES</span></span>

## <span data-ttu-id="0738c-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0738c-153">RELATED LINKS</span></span>

[<span data-ttu-id="0738c-154">New-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="0738c-154">New-AzStorageShare</span></span>](./New-AzStorageShare.md)

[<span data-ttu-id="0738c-155">Remove-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="0738c-155">Remove-AzStorageShare</span></span>](./Remove-AzStorageShare.md)
