---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 730ECC60-72DE-46DA-A177-D5749F540710
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 577dd6cb3ca12daee1cbc4c87d5d1f619c13eea0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348278"
---
# <span data-ttu-id="0b5e9-101">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0b5e9-101">Set-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="0b5e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b5e9-102">SYNOPSIS</span></span>
<span data-ttu-id="0b5e9-103">Azure 저장소 컨테이너에 대해 저장된 액세스 정책을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="0b5e9-103">Sets a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="0b5e9-104">구문</span><span class="sxs-lookup"><span data-stu-id="0b5e9-104">SYNTAX</span></span>

```
Set-AzStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0b5e9-105">설명</span><span class="sxs-lookup"><span data-stu-id="0b5e9-105">DESCRIPTION</span></span>
<span data-ttu-id="0b5e9-106">**Set-AzStorageContainerStoredAccessPolicy** cmdlet은 Azure 저장소 컨테이너에 대해 저장된 액세스 정책을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="0b5e9-106">The **Set-AzStorageContainerStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="0b5e9-107">예제</span><span class="sxs-lookup"><span data-stu-id="0b5e9-107">EXAMPLES</span></span>

### <span data-ttu-id="0b5e9-108">예제 1: 모든 권한이 있는 저장소 컨테이너에 저장된 액세스 정책 설정</span><span class="sxs-lookup"><span data-stu-id="0b5e9-108">Example 1: Set a stored access policy in a storage container with full permission</span></span>
```
PS C:\>Set-AzStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy06" -Permission rwdl
```

<span data-ttu-id="0b5e9-109">이 명령은 MyContainer라는 저장소 컨테이너에 대해 Policy06이라는 액세스 정책을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="0b5e9-109">This command sets an access policy named Policy06 for storage container named MyContainer.</span></span>

## <span data-ttu-id="0b5e9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0b5e9-110">PARAMETERS</span></span>

### <span data-ttu-id="0b5e9-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0b5e9-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="0b5e9-112">하나의 서비스 요청에 대해 클라이언트 쪽 시간(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0b5e9-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="0b5e9-113">이전 호출이 지정된 간격에서 실패하는 경우 이 cmdlet은 요청을 다시 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="0b5e9-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="0b5e9-114">이 cmdlet이 간격이 경과하기 전에 성공적인 응답을 받지 못하면 이 cmdlet은 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="0b5e9-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="0b5e9-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="0b5e9-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="0b5e9-116">최대 동시 네트워크 호출을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0b5e9-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="0b5e9-117">이 매개 변수를 사용하여 최대 동시 네트워크 호출 수를 지정하여 동시성으로 로컬 CPU 및 대역폭 사용량을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0b5e9-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="0b5e9-118">지정된 값은 절대 개수로, 코어 수에 곱하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0b5e9-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="0b5e9-119">이 매개 변수는 초당 100킬로비트와 같은 낮은 대역폭 환경에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0b5e9-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="0b5e9-120">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="0b5e9-120">The default value is 10.</span></span>

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

### <span data-ttu-id="0b5e9-121">-Container</span><span class="sxs-lookup"><span data-stu-id="0b5e9-121">-Container</span></span>
<span data-ttu-id="0b5e9-122">Azure 저장소 컨테이너 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0b5e9-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="0b5e9-123">-Context</span><span class="sxs-lookup"><span data-stu-id="0b5e9-123">-Context</span></span>
<span data-ttu-id="0b5e9-124">Azure 저장소 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0b5e9-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="0b5e9-125">저장소 컨텍스트를 얻습니다. New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b5e9-125">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="0b5e9-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b5e9-126">-DefaultProfile</span></span>
<span data-ttu-id="0b5e9-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0b5e9-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b5e9-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="0b5e9-128">-ExpiryTime</span></span>
<span data-ttu-id="0b5e9-129">저장된 액세스 정책이 유효하지 않은 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0b5e9-129">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="0b5e9-130">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="0b5e9-130">-NoExpiryTime</span></span>
<span data-ttu-id="0b5e9-131">액세스 정책에 만료 날짜가 없음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="0b5e9-131">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="0b5e9-132">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="0b5e9-132">-NoStartTime</span></span>
<span data-ttu-id="0b5e9-133">시작 시간을 설정하여 $Null.</span><span class="sxs-lookup"><span data-stu-id="0b5e9-133">Sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="0b5e9-134">-Permission</span><span class="sxs-lookup"><span data-stu-id="0b5e9-134">-Permission</span></span>
<span data-ttu-id="0b5e9-135">저장소 컨테이너에 액세스하기 위한 저장된 액세스 정책의 사용 권한을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0b5e9-135">Specifies permissions in the stored access policy to access the storage container.</span></span>
<span data-ttu-id="0b5e9-136">이 문자열은 읽기, 쓰기 및 삭제와 같은 `rwd` 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="0b5e9-136">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="0b5e9-137">-Policy</span><span class="sxs-lookup"><span data-stu-id="0b5e9-137">-Policy</span></span>
<span data-ttu-id="0b5e9-138">저장된 액세스 정책의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0b5e9-138">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="0b5e9-139">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="0b5e9-139">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="0b5e9-140">하나의 서비스 요청에 대해 클라이언트 쪽 시간(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0b5e9-140">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="0b5e9-141">이전 호출이 지정된 간격에서 실패하는 경우 이 cmdlet은 요청을 다시 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="0b5e9-141">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="0b5e9-142">이 cmdlet이 간격이 경과하기 전에 성공적인 응답을 받지 못하면 이 cmdlet은 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="0b5e9-142">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="0b5e9-143">-StartTime</span><span class="sxs-lookup"><span data-stu-id="0b5e9-143">-StartTime</span></span>
<span data-ttu-id="0b5e9-144">저장된 액세스 정책이 유효한 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0b5e9-144">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="0b5e9-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0b5e9-145">-Confirm</span></span>
<span data-ttu-id="0b5e9-146">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0b5e9-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b5e9-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b5e9-147">-WhatIf</span></span>
<span data-ttu-id="0b5e9-148">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="0b5e9-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0b5e9-149">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0b5e9-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b5e9-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b5e9-150">CommonParameters</span></span>
<span data-ttu-id="0b5e9-151">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0b5e9-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b5e9-152">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0b5e9-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b5e9-153">입력</span><span class="sxs-lookup"><span data-stu-id="0b5e9-153">INPUTS</span></span>

### <span data-ttu-id="0b5e9-154">System.String</span><span class="sxs-lookup"><span data-stu-id="0b5e9-154">System.String</span></span>

### <span data-ttu-id="0b5e9-155">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0b5e9-155">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0b5e9-156">출력</span><span class="sxs-lookup"><span data-stu-id="0b5e9-156">OUTPUTS</span></span>

### <span data-ttu-id="0b5e9-157">System.String</span><span class="sxs-lookup"><span data-stu-id="0b5e9-157">System.String</span></span>

## <span data-ttu-id="0b5e9-158">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0b5e9-158">NOTES</span></span>

## <span data-ttu-id="0b5e9-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0b5e9-159">RELATED LINKS</span></span>

[<span data-ttu-id="0b5e9-160">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0b5e9-160">Get-AzStorageContainerStoredAccessPolicy</span></span>](./Get-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="0b5e9-161">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="0b5e9-161">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="0b5e9-162">New-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0b5e9-162">New-AzStorageContainerStoredAccessPolicy</span></span>](./New-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="0b5e9-163">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0b5e9-163">Remove-AzStorageContainerStoredAccessPolicy</span></span>](./Remove-AzStorageContainerStoredAccessPolicy.md)
