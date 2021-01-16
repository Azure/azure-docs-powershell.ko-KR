---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 37E76360-B683-407C-9AEF-7138374562D8
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 52f1e3ce96133d0dc2e389f8eabcb18c6c7790c1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349437"
---
# <span data-ttu-id="ca4b9-101">New-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ca4b9-101">New-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="ca4b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca4b9-102">SYNOPSIS</span></span>
<span data-ttu-id="ca4b9-103">저장소 공유에 저장된 액세스 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ca4b9-103">Creates a stored access policy on a Storage share.</span></span>

## <span data-ttu-id="ca4b9-104">구문</span><span class="sxs-lookup"><span data-stu-id="ca4b9-104">SYNTAX</span></span>

```
New-AzStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="ca4b9-105">설명</span><span class="sxs-lookup"><span data-stu-id="ca4b9-105">DESCRIPTION</span></span>
<span data-ttu-id="ca4b9-106">**New-AzStorageShareStoredAccessPolicy** cmdlet은 Azure Storage 공유에 저장된 액세스 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ca4b9-106">The **New-AzStorageShareStoredAccessPolicy** cmdlet creates a stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="ca4b9-107">예제</span><span class="sxs-lookup"><span data-stu-id="ca4b9-107">EXAMPLES</span></span>

### <span data-ttu-id="ca4b9-108">예제 1: 공유에 저장된 액세스 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="ca4b9-108">Example 1: Create a stored access policy in a share</span></span>
```
PS C:\>New-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="ca4b9-109">이 명령은 공유에서 모든 권한이 있는 저장된 액세스 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ca4b9-109">This command creates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="ca4b9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca4b9-110">PARAMETERS</span></span>

### <span data-ttu-id="ca4b9-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ca4b9-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="ca4b9-112">하나의 서비스 요청에 대해 클라이언트 쪽 시간(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ca4b9-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="ca4b9-113">이전 호출이 지정된 간격에서 실패하는 경우 이 cmdlet은 요청을 다시 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="ca4b9-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="ca4b9-114">이 cmdlet이 간격이 경과하기 전에 성공적인 응답을 받지 못하면 이 cmdlet은 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ca4b9-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="ca4b9-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="ca4b9-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="ca4b9-116">최대 동시 네트워크 호출을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ca4b9-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="ca4b9-117">이 매개 변수를 사용하여 최대 동시 네트워크 호출 수를 지정하여 동시성으로 로컬 CPU 및 대역폭 사용량을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca4b9-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="ca4b9-118">지정된 값은 절대 개수로, 코어 수에 곱하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ca4b9-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="ca4b9-119">이 매개 변수는 초당 100킬로비트와 같은 낮은 대역폭 환경에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca4b9-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="ca4b9-120">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="ca4b9-120">The default value is 10.</span></span>

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

### <span data-ttu-id="ca4b9-121">-Context</span><span class="sxs-lookup"><span data-stu-id="ca4b9-121">-Context</span></span>
<span data-ttu-id="ca4b9-122">Azure 저장소 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ca4b9-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="ca4b9-123">저장소 컨텍스트를 얻습니다. [New-AzStorageContext](./New-AzStorageContext.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca4b9-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="ca4b9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca4b9-124">-DefaultProfile</span></span>
<span data-ttu-id="ca4b9-125">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ca4b9-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca4b9-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="ca4b9-126">-ExpiryTime</span></span>
<span data-ttu-id="ca4b9-127">저장된 액세스 정책이 유효하지 않은 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ca4b9-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca4b9-128">-Permission</span><span class="sxs-lookup"><span data-stu-id="ca4b9-128">-Permission</span></span>
<span data-ttu-id="ca4b9-129">저장소 공유 또는 그 아래에 있는 파일에 액세스하기 위한 저장된 액세스 정책의 사용 권한을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ca4b9-129">Specifies permissions in the stored access policy to access the Storage share or files under it.</span></span>
<span data-ttu-id="ca4b9-130">이 문자열은 읽기, 쓰기 및 삭제와 같은 `rwd` 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="ca4b9-130">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca4b9-131">-Policy</span><span class="sxs-lookup"><span data-stu-id="ca4b9-131">-Policy</span></span>
<span data-ttu-id="ca4b9-132">저장된 액세스 정책의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ca4b9-132">Specifies a name for the stored access policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca4b9-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ca4b9-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="ca4b9-134">요청의 서버 부분에 대한 시간 제한 기간의 길이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ca4b9-134">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="ca4b9-135">-ShareName</span><span class="sxs-lookup"><span data-stu-id="ca4b9-135">-ShareName</span></span>
<span data-ttu-id="ca4b9-136">저장소 공유의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ca4b9-136">Specifies the name of the Storage share.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ca4b9-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="ca4b9-137">-StartTime</span></span>
<span data-ttu-id="ca4b9-138">저장된 액세스 정책이 유효한 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ca4b9-138">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca4b9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca4b9-139">CommonParameters</span></span>
<span data-ttu-id="ca4b9-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ca4b9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca4b9-141">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ca4b9-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca4b9-142">입력</span><span class="sxs-lookup"><span data-stu-id="ca4b9-142">INPUTS</span></span>

### <span data-ttu-id="ca4b9-143">System.String</span><span class="sxs-lookup"><span data-stu-id="ca4b9-143">System.String</span></span>

### <span data-ttu-id="ca4b9-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ca4b9-144">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ca4b9-145">출력</span><span class="sxs-lookup"><span data-stu-id="ca4b9-145">OUTPUTS</span></span>

### <span data-ttu-id="ca4b9-146">System.String</span><span class="sxs-lookup"><span data-stu-id="ca4b9-146">System.String</span></span>

## <span data-ttu-id="ca4b9-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ca4b9-147">NOTES</span></span>

## <span data-ttu-id="ca4b9-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ca4b9-148">RELATED LINKS</span></span>

[<span data-ttu-id="ca4b9-149">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ca4b9-149">Get-AzStorageShareStoredAccessPolicy</span></span>](./Get-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="ca4b9-150">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="ca4b9-150">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="ca4b9-151">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ca4b9-151">Remove-AzStorageShareStoredAccessPolicy</span></span>](./Remove-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="ca4b9-152">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ca4b9-152">Set-AzStorageShareStoredAccessPolicy</span></span>](./Set-AzStorageShareStoredAccessPolicy.md)
