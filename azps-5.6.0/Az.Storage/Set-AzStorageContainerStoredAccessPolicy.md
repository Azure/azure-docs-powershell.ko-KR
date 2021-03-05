---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 730ECC60-72DE-46DA-A177-D5749F540710
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: e195b4844b35e5ab10d41ed505d619edf3f13515
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002251"
---
# <span data-ttu-id="aaaa4-101">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="aaaa4-101">Set-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="aaaa4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aaaa4-102">SYNOPSIS</span></span>
<span data-ttu-id="aaaa4-103">Azure 저장소 컨테이너에 대한 저장된 액세스 정책을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="aaaa4-103">Sets a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="aaaa4-104">구문</span><span class="sxs-lookup"><span data-stu-id="aaaa4-104">SYNTAX</span></span>

```
Set-AzStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aaaa4-105">설명</span><span class="sxs-lookup"><span data-stu-id="aaaa4-105">DESCRIPTION</span></span>
<span data-ttu-id="aaaa4-106">**Set-AzStorageContainerStoredAccessPolicy** cmdlet은 Azure Storage 컨테이너에 대한 저장된 액세스 정책을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="aaaa4-106">The **Set-AzStorageContainerStoredAccessPolicy** cmdlet sets a stored access policy for an Azure storage container.</span></span>

## <span data-ttu-id="aaaa4-107">예제</span><span class="sxs-lookup"><span data-stu-id="aaaa4-107">EXAMPLES</span></span>

### <span data-ttu-id="aaaa4-108">예제 1: 전체 권한으로 저장소 컨테이너에 저장된 액세스 정책 설정</span><span class="sxs-lookup"><span data-stu-id="aaaa4-108">Example 1: Set a stored access policy in a storage container with full permission</span></span>
```
PS C:\>Set-AzStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy06" -Permission rwdl
```

<span data-ttu-id="aaaa4-109">이 명령은 MyContainer라는 저장소 컨테이너에 대해 Policy06이라는 액세스 정책을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="aaaa4-109">This command sets an access policy named Policy06 for storage container named MyContainer.</span></span>

## <span data-ttu-id="aaaa4-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="aaaa4-110">PARAMETERS</span></span>

### <span data-ttu-id="aaaa4-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="aaaa4-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="aaaa4-112">하나의 서비스 요청에 대해 클라이언트 쪽 시간 간격(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aaaa4-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="aaaa4-113">지정된 간격에서 이전 호출이 실패하면 이 cmdlet에서 요청을 다시 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="aaaa4-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="aaaa4-114">간격이 경과하기 전에 이 cmdlet에서 성공적인 응답을 받지 못하면 이 cmdlet은 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="aaaa4-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="aaaa4-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="aaaa4-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="aaaa4-116">최대 동시 네트워크 호출을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aaaa4-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="aaaa4-117">이 매개 변수를 사용하여 최대 동시 네트워크 호출 수를 지정하여 로컬 CPU 및 대역폭 사용량을 제한하는 동시성 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aaaa4-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="aaaa4-118">지정된 값은 절대 개수로 코어 수에 곱하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aaaa4-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="aaaa4-119">이 매개 변수는 초당 100킬로비트와 같은 대역폭이 낮은 환경에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aaaa4-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="aaaa4-120">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="aaaa4-120">The default value is 10.</span></span>

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

### <span data-ttu-id="aaaa4-121">-Container</span><span class="sxs-lookup"><span data-stu-id="aaaa4-121">-Container</span></span>
<span data-ttu-id="aaaa4-122">Azure Storage 컨테이너 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aaaa4-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="aaaa4-123">-Context</span><span class="sxs-lookup"><span data-stu-id="aaaa4-123">-Context</span></span>
<span data-ttu-id="aaaa4-124">Azure Storage 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aaaa4-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="aaaa4-125">저장소 컨텍스트를 구하기 위해 New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="aaaa4-125">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="aaaa4-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaaa4-126">-DefaultProfile</span></span>
<span data-ttu-id="aaaa4-127">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aaaa4-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aaaa4-128">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="aaaa4-128">-ExpiryTime</span></span>
<span data-ttu-id="aaaa4-129">저장된 액세스 정책이 유효하지 않은 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aaaa4-129">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="aaaa4-130">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="aaaa4-130">-NoExpiryTime</span></span>
<span data-ttu-id="aaaa4-131">액세스 정책에 만료 날짜가 없음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="aaaa4-131">Indicates that the access policy has no expiration date.</span></span>

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

### <span data-ttu-id="aaaa4-132">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="aaaa4-132">-NoStartTime</span></span>
<span data-ttu-id="aaaa4-133">시작 시간을 $Null.</span><span class="sxs-lookup"><span data-stu-id="aaaa4-133">Sets the start time to be $Null.</span></span>

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

### <span data-ttu-id="aaaa4-134">-권한</span><span class="sxs-lookup"><span data-stu-id="aaaa4-134">-Permission</span></span>
<span data-ttu-id="aaaa4-135">저장소 컨테이너에 액세스하기 위해 저장된 액세스 정책에서 권한을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aaaa4-135">Specifies permissions in the stored access policy to access the storage container.</span></span>
<span data-ttu-id="aaaa4-136">이 문자열은 읽기, 쓰기 및 삭제와 같은 `rwd` 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="aaaa4-136">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="aaaa4-137">-Policy</span><span class="sxs-lookup"><span data-stu-id="aaaa4-137">-Policy</span></span>
<span data-ttu-id="aaaa4-138">저장된 액세스 정책의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aaaa4-138">Specifies the name for the stored access policy.</span></span>

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

### <span data-ttu-id="aaaa4-139">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="aaaa4-139">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="aaaa4-140">하나의 서비스 요청에 대해 클라이언트 쪽 시간 간격(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aaaa4-140">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="aaaa4-141">지정된 간격에서 이전 호출이 실패하면 이 cmdlet에서 요청을 다시 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="aaaa4-141">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="aaaa4-142">간격이 경과하기 전에 이 cmdlet에서 성공적인 응답을 받지 못하면 이 cmdlet은 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="aaaa4-142">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="aaaa4-143">-StartTime</span><span class="sxs-lookup"><span data-stu-id="aaaa4-143">-StartTime</span></span>
<span data-ttu-id="aaaa4-144">저장된 액세스 정책이 유효한 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="aaaa4-144">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="aaaa4-145">-확인</span><span class="sxs-lookup"><span data-stu-id="aaaa4-145">-Confirm</span></span>
<span data-ttu-id="aaaa4-146">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="aaaa4-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aaaa4-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aaaa4-147">-WhatIf</span></span>
<span data-ttu-id="aaaa4-148">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="aaaa4-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aaaa4-149">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aaaa4-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aaaa4-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaaa4-150">CommonParameters</span></span>
<span data-ttu-id="aaaa4-151">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="aaaa4-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaaa4-152">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="aaaa4-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaaa4-153">입력</span><span class="sxs-lookup"><span data-stu-id="aaaa4-153">INPUTS</span></span>

### <span data-ttu-id="aaaa4-154">System.String</span><span class="sxs-lookup"><span data-stu-id="aaaa4-154">System.String</span></span>

### <span data-ttu-id="aaaa4-155">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="aaaa4-155">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="aaaa4-156">출력</span><span class="sxs-lookup"><span data-stu-id="aaaa4-156">OUTPUTS</span></span>

### <span data-ttu-id="aaaa4-157">System.String</span><span class="sxs-lookup"><span data-stu-id="aaaa4-157">System.String</span></span>

## <span data-ttu-id="aaaa4-158">참고 사항</span><span class="sxs-lookup"><span data-stu-id="aaaa4-158">NOTES</span></span>

## <span data-ttu-id="aaaa4-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aaaa4-159">RELATED LINKS</span></span>

[<span data-ttu-id="aaaa4-160">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="aaaa4-160">Get-AzStorageContainerStoredAccessPolicy</span></span>](./Get-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="aaaa4-161">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="aaaa4-161">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="aaaa4-162">New-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="aaaa4-162">New-AzStorageContainerStoredAccessPolicy</span></span>](./New-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="aaaa4-163">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="aaaa4-163">Remove-AzStorageContainerStoredAccessPolicy</span></span>](./Remove-AzStorageContainerStoredAccessPolicy.md)
