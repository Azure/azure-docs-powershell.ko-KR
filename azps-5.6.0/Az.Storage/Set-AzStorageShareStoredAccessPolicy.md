---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C21CC2FA-017E-492E-96E7-B37829917FAF
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: b48c56df294e12e9c8f84b45b3bb991406338b52
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963504"
---
# <span data-ttu-id="b10c9-101">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b10c9-101">Set-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="b10c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b10c9-102">SYNOPSIS</span></span>
<span data-ttu-id="b10c9-103">Storage 공유에서 저장된 액세스 정책을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="b10c9-103">Updates a stored access policy on a Storage share.</span></span>

## <span data-ttu-id="b10c9-104">구문</span><span class="sxs-lookup"><span data-stu-id="b10c9-104">SYNTAX</span></span>

```
Set-AzStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b10c9-105">설명</span><span class="sxs-lookup"><span data-stu-id="b10c9-105">DESCRIPTION</span></span>
<span data-ttu-id="b10c9-106">**Set-AzStorageShareStoredAccessPolicy** cmdlet은 Azure Storage 공유에 저장된 액세스 정책을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="b10c9-106">The **Set-AzStorageShareStoredAccessPolicy** cmdlet updates stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="b10c9-107">예제</span><span class="sxs-lookup"><span data-stu-id="b10c9-107">EXAMPLES</span></span>

### <span data-ttu-id="b10c9-108">예제 1: Storage 공유에서 저장된 액세스 정책 업데이트</span><span class="sxs-lookup"><span data-stu-id="b10c9-108">Example 1: Update a stored access policy in Storage share</span></span>
```
PS C:\>Set-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="b10c9-109">이 명령은 공유에서 전체 권한이 있는 저장된 액세스 정책을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="b10c9-109">This command updates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="b10c9-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b10c9-110">PARAMETERS</span></span>

### <span data-ttu-id="b10c9-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b10c9-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="b10c9-112">하나의 서비스 요청에 대해 클라이언트 쪽 시간 간격(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b10c9-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="b10c9-113">지정된 간격에서 이전 호출이 실패하면 이 cmdlet에서 요청을 다시 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="b10c9-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="b10c9-114">간격이 경과하기 전에 이 cmdlet에서 성공적인 응답을 받지 못하면 이 cmdlet은 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="b10c9-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="b10c9-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="b10c9-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="b10c9-116">최대 동시 네트워크 호출을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b10c9-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="b10c9-117">이 매개 변수를 사용하여 최대 동시 네트워크 호출 수를 지정하여 로컬 CPU 및 대역폭 사용량을 제한하는 동시성 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b10c9-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="b10c9-118">지정된 값은 절대 개수로 코어 수에 곱하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b10c9-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="b10c9-119">이 매개 변수는 초당 100킬로비트와 같은 대역폭이 낮은 환경에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b10c9-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="b10c9-120">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="b10c9-120">The default value is 10.</span></span>

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

### <span data-ttu-id="b10c9-121">-Context</span><span class="sxs-lookup"><span data-stu-id="b10c9-121">-Context</span></span>
<span data-ttu-id="b10c9-122">Azure Storage 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b10c9-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="b10c9-123">저장소 컨텍스트를 구하기 위해 [New-AzStorageContext](./New-AzStorageContext.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b10c9-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="b10c9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b10c9-124">-DefaultProfile</span></span>
<span data-ttu-id="b10c9-125">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b10c9-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b10c9-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="b10c9-126">-ExpiryTime</span></span>
<span data-ttu-id="b10c9-127">저장된 액세스 정책이 유효하지 않은 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b10c9-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="b10c9-128">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="b10c9-128">-NoExpiryTime</span></span>
<span data-ttu-id="b10c9-129">이 cmdlet이 저장된 액세스 정책에서 **ExpiryTime** 속성을 지우는 경우를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b10c9-129">Indicates that this cmdlet clears the **ExpiryTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="b10c9-130">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="b10c9-130">-NoStartTime</span></span>
<span data-ttu-id="b10c9-131">이 cmdlet이 저장된 액세스 정책에서 **StartTime** 속성을 지우는 경우를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b10c9-131">Indicates that this cmdlet clears the **StartTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="b10c9-132">-권한</span><span class="sxs-lookup"><span data-stu-id="b10c9-132">-Permission</span></span>
<span data-ttu-id="b10c9-133">저장된 액세스 정책에 있는 권한을 지정하여 해당 공유 또는 파일에 액세스합니다.</span><span class="sxs-lookup"><span data-stu-id="b10c9-133">Specifies permissions in the stored access policy to access the share or files under it.</span></span>
<span data-ttu-id="b10c9-134">이 문자열은 읽기, 쓰기 및 삭제와 같은 `rwd` 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="b10c9-134">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="b10c9-135">-Policy</span><span class="sxs-lookup"><span data-stu-id="b10c9-135">-Policy</span></span>
<span data-ttu-id="b10c9-136">저장된 액세스 정책의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b10c9-136">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="b10c9-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="b10c9-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="b10c9-138">요청의 서버 부분에 대한 시간 제한 기간의 길이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b10c9-138">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="b10c9-139">-ShareName</span><span class="sxs-lookup"><span data-stu-id="b10c9-139">-ShareName</span></span>
<span data-ttu-id="b10c9-140">Storage 공유의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b10c9-140">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="b10c9-141">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b10c9-141">-StartTime</span></span>
<span data-ttu-id="b10c9-142">저장된 액세스 정책이 유효한 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b10c9-142">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="b10c9-143">-확인</span><span class="sxs-lookup"><span data-stu-id="b10c9-143">-Confirm</span></span>
<span data-ttu-id="b10c9-144">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b10c9-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b10c9-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b10c9-145">-WhatIf</span></span>
<span data-ttu-id="b10c9-146">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="b10c9-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b10c9-147">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b10c9-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b10c9-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b10c9-148">CommonParameters</span></span>
<span data-ttu-id="b10c9-149">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b10c9-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b10c9-150">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b10c9-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b10c9-151">입력</span><span class="sxs-lookup"><span data-stu-id="b10c9-151">INPUTS</span></span>

### <span data-ttu-id="b10c9-152">System.String</span><span class="sxs-lookup"><span data-stu-id="b10c9-152">System.String</span></span>

### <span data-ttu-id="b10c9-153">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b10c9-153">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="b10c9-154">출력</span><span class="sxs-lookup"><span data-stu-id="b10c9-154">OUTPUTS</span></span>

### <span data-ttu-id="b10c9-155">System.String</span><span class="sxs-lookup"><span data-stu-id="b10c9-155">System.String</span></span>

## <span data-ttu-id="b10c9-156">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b10c9-156">NOTES</span></span>

## <span data-ttu-id="b10c9-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b10c9-157">RELATED LINKS</span></span>

[<span data-ttu-id="b10c9-158">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b10c9-158">Get-AzStorageShareStoredAccessPolicy</span></span>](./Get-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="b10c9-159">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="b10c9-159">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="b10c9-160">New-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b10c9-160">New-AzStorageShareStoredAccessPolicy</span></span>](./New-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="b10c9-161">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="b10c9-161">Remove-AzStorageShareStoredAccessPolicy</span></span>](./Remove-AzStorageShareStoredAccessPolicy.md)
