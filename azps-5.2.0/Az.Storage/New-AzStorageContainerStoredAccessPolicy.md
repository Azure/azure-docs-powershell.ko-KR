---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C324F28A-7215-4F10-A012-92B4F6544BC0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: eb51b8c4e33f45d637354f85be049295626afdd6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324778"
---
# <span data-ttu-id="141e3-101">New-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="141e3-101">New-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="141e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="141e3-102">SYNOPSIS</span></span>
<span data-ttu-id="141e3-103">Azure 저장소 컨테이너에 대해 저장된 액세스 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="141e3-103">Creates a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="141e3-104">구문</span><span class="sxs-lookup"><span data-stu-id="141e3-104">SYNTAX</span></span>

```
New-AzStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="141e3-105">설명</span><span class="sxs-lookup"><span data-stu-id="141e3-105">DESCRIPTION</span></span>
<span data-ttu-id="141e3-106">**New-AzStorageContainerStoredAccessPolicy** cmdlet은 Azure 저장소 컨테이너에 대해 저장된 액세스 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="141e3-106">The **New-AzStorageContainerStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="141e3-107">예제</span><span class="sxs-lookup"><span data-stu-id="141e3-107">EXAMPLES</span></span>

### <span data-ttu-id="141e3-108">예제 1: 저장소 컨테이너에 저장된 액세스 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="141e3-108">Example 1: Create a stored access policy in a storage container</span></span>
```
PS C:\>New-AzStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy01"
```

<span data-ttu-id="141e3-109">이 명령은 MyContainer라는 저장소 컨테이너에 Policy01이라는 액세스 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="141e3-109">This command creates an access policy named Policy01 in the storage container named MyContainer.</span></span>

## <span data-ttu-id="141e3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="141e3-110">PARAMETERS</span></span>

### <span data-ttu-id="141e3-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="141e3-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="141e3-112">하나의 서비스 요청에 대해 클라이언트 쪽 시간(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="141e3-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="141e3-113">이전 호출이 지정된 간격에서 실패하는 경우 이 cmdlet은 요청을 다시 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="141e3-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="141e3-114">이 cmdlet이 간격이 경과하기 전에 성공적인 응답을 받지 못하면 이 cmdlet은 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="141e3-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="141e3-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="141e3-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="141e3-116">최대 동시 네트워크 호출을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="141e3-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="141e3-117">이 매개 변수를 사용하여 최대 동시 네트워크 호출 수를 지정하여 동시성으로 로컬 CPU 및 대역폭 사용량을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="141e3-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="141e3-118">지정된 값은 절대 개수로, 코어 수에 곱하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="141e3-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="141e3-119">이 매개 변수는 초당 100킬로비트와 같은 낮은 대역폭 환경에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="141e3-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="141e3-120">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="141e3-120">The default value is 10.</span></span>

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

### <span data-ttu-id="141e3-121">-Container</span><span class="sxs-lookup"><span data-stu-id="141e3-121">-Container</span></span>
<span data-ttu-id="141e3-122">Azure 저장소 컨테이너 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="141e3-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="141e3-123">-Context</span><span class="sxs-lookup"><span data-stu-id="141e3-123">-Context</span></span>
<span data-ttu-id="141e3-124">Azure 저장소 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="141e3-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="141e3-125">저장소 컨텍스트를 얻습니다. New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="141e3-125">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="141e3-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="141e3-126">-DefaultProfile</span></span>
<span data-ttu-id="141e3-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="141e3-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="141e3-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="141e3-128">-ExpiryTime</span></span>
<span data-ttu-id="141e3-129">저장된 액세스 정책이 유효하지 않은 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="141e3-129">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="141e3-130">-Permission</span><span class="sxs-lookup"><span data-stu-id="141e3-130">-Permission</span></span>
<span data-ttu-id="141e3-131">컨테이너에 액세스하기 위한 저장된 액세스 정책의 사용 권한을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="141e3-131">Specifies permissions in the stored access policy to access the container.</span></span>
<span data-ttu-id="141e3-132">이 문자열은 읽기, 쓰기 및 삭제와 같은 `rwd` 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="141e3-132">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="141e3-133">-Policy</span><span class="sxs-lookup"><span data-stu-id="141e3-133">-Policy</span></span>
<span data-ttu-id="141e3-134">이 SAS 토큰에 대한 사용 권한을 포함하는 저장된 액세스 정책을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="141e3-134">Specifies a stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="141e3-135">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="141e3-135">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="141e3-136">하나의 서비스 요청에 대해 클라이언트 쪽 시간(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="141e3-136">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="141e3-137">이전 호출이 지정된 간격에서 실패하는 경우 이 cmdlet은 요청을 다시 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="141e3-137">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="141e3-138">이 cmdlet이 간격이 경과하기 전에 성공적인 응답을 받지 못하면 이 cmdlet은 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="141e3-138">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="141e3-139">-StartTime</span><span class="sxs-lookup"><span data-stu-id="141e3-139">-StartTime</span></span>
<span data-ttu-id="141e3-140">저장된 액세스 정책이 유효한 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="141e3-140">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="141e3-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="141e3-141">CommonParameters</span></span>
<span data-ttu-id="141e3-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="141e3-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="141e3-143">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="141e3-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="141e3-144">입력</span><span class="sxs-lookup"><span data-stu-id="141e3-144">INPUTS</span></span>

### <span data-ttu-id="141e3-145">System.String</span><span class="sxs-lookup"><span data-stu-id="141e3-145">System.String</span></span>

### <span data-ttu-id="141e3-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="141e3-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="141e3-147">출력</span><span class="sxs-lookup"><span data-stu-id="141e3-147">OUTPUTS</span></span>

### <span data-ttu-id="141e3-148">System.String</span><span class="sxs-lookup"><span data-stu-id="141e3-148">System.String</span></span>

## <span data-ttu-id="141e3-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="141e3-149">NOTES</span></span>

## <span data-ttu-id="141e3-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="141e3-150">RELATED LINKS</span></span>

[<span data-ttu-id="141e3-151">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="141e3-151">Get-AzStorageContainerStoredAccessPolicy</span></span>](./Get-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="141e3-152">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="141e3-152">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="141e3-153">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="141e3-153">Remove-AzStorageContainerStoredAccessPolicy</span></span>](./Remove-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="141e3-154">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="141e3-154">Set-AzStorageContainerStoredAccessPolicy</span></span>](./Set-AzStorageContainerStoredAccessPolicy.md)


