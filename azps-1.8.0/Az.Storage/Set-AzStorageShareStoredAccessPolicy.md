---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C21CC2FA-017E-492E-96E7-B37829917FAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 58fc0ef20300f57407d7df35f1732830dbc4c5d4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698527"
---
# <span data-ttu-id="4fbd5-101">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4fbd5-101">Set-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="4fbd5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fbd5-102">SYNOPSIS</span></span>
<span data-ttu-id="4fbd5-103">저장소 공유에 저장 된 액세스 정책을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fbd5-103">Updates a stored access policy on a Storage share.</span></span>

## <span data-ttu-id="4fbd5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4fbd5-104">SYNTAX</span></span>

```
Set-AzStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-NoStartTime] [-NoExpiryTime] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4fbd5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4fbd5-105">DESCRIPTION</span></span>
<span data-ttu-id="4fbd5-106">**AzStorageShareStoredAccessPolicy** Cmdlet은 Azure 저장소 공유에 저장 된 액세스 정책을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fbd5-106">The **Set-AzStorageShareStoredAccessPolicy** cmdlet updates stored access policy on an Azure Storage share.</span></span>

## <span data-ttu-id="4fbd5-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4fbd5-107">EXAMPLES</span></span>

### <span data-ttu-id="4fbd5-108">예제 1: 저장소 공유에 저장 된 액세스 정책 업데이트</span><span class="sxs-lookup"><span data-stu-id="4fbd5-108">Example 1: Update a stored access policy in Storage share</span></span>
```
PS C:\>Set-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

<span data-ttu-id="4fbd5-109">이 명령은 공유에 모든 권한이 있는 저장 된 액세스 정책을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fbd5-109">This command updates a stored access policy that has full permission in a share.</span></span>

## <span data-ttu-id="4fbd5-110">변수</span><span class="sxs-lookup"><span data-stu-id="4fbd5-110">PARAMETERS</span></span>

### <span data-ttu-id="4fbd5-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4fbd5-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="4fbd5-112">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fbd5-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="4fbd5-113">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fbd5-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="4fbd5-114">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fbd5-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="4fbd5-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="4fbd5-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="4fbd5-116">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fbd5-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="4fbd5-117">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4fbd5-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="4fbd5-118">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="4fbd5-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="4fbd5-119">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4fbd5-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="4fbd5-120">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="4fbd5-120">The default value is 10.</span></span>

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

### <span data-ttu-id="4fbd5-121">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="4fbd5-121">-Context</span></span>
<span data-ttu-id="4fbd5-122">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fbd5-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="4fbd5-123">저장소 컨텍스트를 얻으려면 [New AzStorageContext](./New-AzStorageContext.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fbd5-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="4fbd5-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fbd5-124">-DefaultProfile</span></span>
<span data-ttu-id="4fbd5-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4fbd5-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fbd5-126">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="4fbd5-126">-ExpiryTime</span></span>
<span data-ttu-id="4fbd5-127">저장 된 액세스 정책이 무효화 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fbd5-127">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="4fbd5-128">-NoExpiryTime</span><span class="sxs-lookup"><span data-stu-id="4fbd5-128">-NoExpiryTime</span></span>
<span data-ttu-id="4fbd5-129">이 cmdlet이 저장 된 액세스 정책에서 **ExpiryTime** 속성을 지우도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fbd5-129">Indicates that this cmdlet clears the **ExpiryTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="4fbd5-130">-NoStartTime</span><span class="sxs-lookup"><span data-stu-id="4fbd5-130">-NoStartTime</span></span>
<span data-ttu-id="4fbd5-131">이 cmdlet이 저장 된 액세스 정책에서 **StartTime** 속성을 지우는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4fbd5-131">Indicates that this cmdlet clears the **StartTime** property in the stored access policy.</span></span>

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

### <span data-ttu-id="4fbd5-132">-사용 권한</span><span class="sxs-lookup"><span data-stu-id="4fbd5-132">-Permission</span></span>
<span data-ttu-id="4fbd5-133">공유 또는 그 아래에 있는 파일에 액세스 하기 위해 저장 된 액세스 정책에서 사용 권한을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fbd5-133">Specifies permissions in the stored access policy to access the share or files under it.</span></span>
<span data-ttu-id="4fbd5-134">이는 문자열 (예: `rwd` 읽기, 쓰기 및 삭제) 이라고 한다는 점에 유의 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fbd5-134">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="4fbd5-135">-정책</span><span class="sxs-lookup"><span data-stu-id="4fbd5-135">-Policy</span></span>
<span data-ttu-id="4fbd5-136">저장 된 액세스 정책의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fbd5-136">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="4fbd5-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4fbd5-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="4fbd5-138">요청에 대 한 서버 부분에 대 한 시간 초과 기간의 길이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fbd5-138">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="4fbd5-139">-ShareName</span><span class="sxs-lookup"><span data-stu-id="4fbd5-139">-ShareName</span></span>
<span data-ttu-id="4fbd5-140">저장소 공유의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fbd5-140">Specifies the name of the Storage share.</span></span>

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

### <span data-ttu-id="4fbd5-141">-StartTime</span><span class="sxs-lookup"><span data-stu-id="4fbd5-141">-StartTime</span></span>
<span data-ttu-id="4fbd5-142">저장 된 액세스 정책이 유효 하 게 되는 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fbd5-142">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="4fbd5-143">-확인</span><span class="sxs-lookup"><span data-stu-id="4fbd5-143">-Confirm</span></span>
<span data-ttu-id="4fbd5-144">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fbd5-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fbd5-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fbd5-145">-WhatIf</span></span>
<span data-ttu-id="4fbd5-146">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4fbd5-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4fbd5-147">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4fbd5-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fbd5-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fbd5-148">CommonParameters</span></span>
<span data-ttu-id="4fbd5-149">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fbd5-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fbd5-150">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fbd5-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fbd5-151">입력</span><span class="sxs-lookup"><span data-stu-id="4fbd5-151">INPUTS</span></span>

### <span data-ttu-id="4fbd5-152">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4fbd5-152">System.String</span></span>

### <span data-ttu-id="4fbd5-153">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4fbd5-153">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4fbd5-154">출력</span><span class="sxs-lookup"><span data-stu-id="4fbd5-154">OUTPUTS</span></span>

### <span data-ttu-id="4fbd5-155">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4fbd5-155">System.String</span></span>

## <span data-ttu-id="4fbd5-156">상속자</span><span class="sxs-lookup"><span data-stu-id="4fbd5-156">NOTES</span></span>

## <span data-ttu-id="4fbd5-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4fbd5-157">RELATED LINKS</span></span>

[<span data-ttu-id="4fbd5-158">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4fbd5-158">Get-AzStorageShareStoredAccessPolicy</span></span>](./Get-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="4fbd5-159">새로운 AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="4fbd5-159">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="4fbd5-160">새로운 AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4fbd5-160">New-AzStorageShareStoredAccessPolicy</span></span>](./New-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="4fbd5-161">제거-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4fbd5-161">Remove-AzStorageShareStoredAccessPolicy</span></span>](./Remove-AzStorageShareStoredAccessPolicy.md)
