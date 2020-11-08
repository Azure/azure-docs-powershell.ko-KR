---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 730ECC60-72DE-46DA-A177-D5749F540710
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 577dd6cb3ca12daee1cbc4c87d5d1f619c13eea0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042014"
---
# <span data-ttu-id="ecd59-101">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ecd59-101">Set-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="ecd59-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecd59-102">SYNOPSIS</span></span>
<span data-ttu-id="ecd59-103">Azure storage 컨테이너에 대해 저장 된 액세스 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecd59-103">Sets a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="ecd59-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ecd59-104">SYNTAX</span></span>

```
Set-AzStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ecd59-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ecd59-105">DESCRIPTION</span></span>
<span data-ttu-id="ecd59-106">**AzStorageContainerStoredAccessPolicy** Cmdlet은 Azure storage 컨테이너에 대해 저장 된 액세스 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecd59-106">The **Set-AzStorageContainerStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="ecd59-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ecd59-107">EXAMPLES</span></span>

### <span data-ttu-id="ecd59-108">예제 1: 저장소 컨테이너에서 모든 권한을 사용 하 여 저장 된 액세스 정책 설정</span><span class="sxs-lookup"><span data-stu-id="ecd59-108">Example 1: Set a stored access policy in a storage container with full permission</span></span>
```
PS C:\>Set-AzStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy06" -Permission rwdl
```

<span data-ttu-id="ecd59-109">이 명령은 MyContainer 라는 저장소 컨테이너에 대 한 Policy06 라는 액세스 정책을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecd59-109">This command sets an access policy named Policy06 for storage container named MyContainer.</span></span>

## <span data-ttu-id="ecd59-110">변수</span><span class="sxs-lookup"><span data-stu-id="ecd59-110">PARAMETERS</span></span>

### <span data-ttu-id="ecd59-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ecd59-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="ecd59-112">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecd59-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="ecd59-113">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecd59-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="ecd59-114">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecd59-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="ecd59-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="ecd59-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="ecd59-116">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecd59-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="ecd59-117">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ecd59-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="ecd59-118">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="ecd59-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="ecd59-119">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ecd59-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="ecd59-120">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="ecd59-120">The default value is 10.</span></span>

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

### <span data-ttu-id="ecd59-121">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="ecd59-121">-Container</span></span>
<span data-ttu-id="ecd59-122">Azure 저장소 컨테이너 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecd59-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="ecd59-123">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="ecd59-123">-Context</span></span>
<span data-ttu-id="ecd59-124">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecd59-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="ecd59-125">저장소 컨텍스트를 얻으려면 New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecd59-125">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ecd59-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecd59-126">-DefaultProfile</span></span>
<span data-ttu-id="ecd59-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ecd59-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecd59-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="ecd59-128">-ExpiryTime</span></span>
<span data-ttu-id="ecd59-129">저장 된 액세스 정책이 무효화 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecd59-129">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="ecd59-130">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="ecd59-130">-NoExpiryTime</span></span>
<span data-ttu-id="ecd59-131">액세스 정책에 만료 날짜가 없음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ecd59-131">Indicates that the access policy has no expiration date.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecd59-132">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="ecd59-132">-NoStartTime</span></span>
<span data-ttu-id="ecd59-133">시작 시간을 $Null 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecd59-133">Sets the start time to be $Null.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecd59-134">-사용 권한</span><span class="sxs-lookup"><span data-stu-id="ecd59-134">-Permission</span></span>
<span data-ttu-id="ecd59-135">저장 된 액세스 정책에서 저장소 컨테이너에 액세스 하는 데 필요한 사용 권한을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecd59-135">Specifies permissions in the stored access policy to access the storage container.</span></span>
<span data-ttu-id="ecd59-136">이는 문자열 (예: `rwd` 읽기, 쓰기 및 삭제) 이라고 한다는 점에 유의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecd59-136">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="ecd59-137">-정책</span><span class="sxs-lookup"><span data-stu-id="ecd59-137">-Policy</span></span>
<span data-ttu-id="ecd59-138">저장 된 액세스 정책의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecd59-138">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="ecd59-139">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="ecd59-139">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="ecd59-140">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecd59-140">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="ecd59-141">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecd59-141">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="ecd59-142">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecd59-142">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="ecd59-143">-StartTime</span><span class="sxs-lookup"><span data-stu-id="ecd59-143">-StartTime</span></span>
<span data-ttu-id="ecd59-144">저장 된 액세스 정책이 유효 하 게 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecd59-144">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="ecd59-145">-확인</span><span class="sxs-lookup"><span data-stu-id="ecd59-145">-Confirm</span></span>
<span data-ttu-id="ecd59-146">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecd59-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecd59-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecd59-147">-WhatIf</span></span>
<span data-ttu-id="ecd59-148">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ecd59-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ecd59-149">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ecd59-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ecd59-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecd59-150">CommonParameters</span></span>
<span data-ttu-id="ecd59-151">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ecd59-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecd59-152">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ecd59-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecd59-153">입력</span><span class="sxs-lookup"><span data-stu-id="ecd59-153">INPUTS</span></span>

### <span data-ttu-id="ecd59-154">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ecd59-154">System.String</span></span>

### <span data-ttu-id="ecd59-155">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ecd59-155">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ecd59-156">출력</span><span class="sxs-lookup"><span data-stu-id="ecd59-156">OUTPUTS</span></span>

### <span data-ttu-id="ecd59-157">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ecd59-157">System.String</span></span>

## <span data-ttu-id="ecd59-158">상속자</span><span class="sxs-lookup"><span data-stu-id="ecd59-158">NOTES</span></span>

## <span data-ttu-id="ecd59-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ecd59-159">RELATED LINKS</span></span>

[<span data-ttu-id="ecd59-160">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ecd59-160">Get-AzStorageContainerStoredAccessPolicy</span></span>](./Get-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="ecd59-161">새로운 AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="ecd59-161">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="ecd59-162">새로운 AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ecd59-162">New-AzStorageContainerStoredAccessPolicy</span></span>](./New-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="ecd59-163">제거-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ecd59-163">Remove-AzStorageContainerStoredAccessPolicy</span></span>](./Remove-AzStorageContainerStoredAccessPolicy.md)
