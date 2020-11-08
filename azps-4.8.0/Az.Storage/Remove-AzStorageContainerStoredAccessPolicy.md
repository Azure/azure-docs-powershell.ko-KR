---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3E79EE05-7E52-4C54-B985-441BC2599925
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 1b8667d08e02c9294a18f4cbf84cb27085cbc118
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048586"
---
# <span data-ttu-id="c40e3-101">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c40e3-101">Remove-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="c40e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c40e3-102">SYNOPSIS</span></span>
<span data-ttu-id="c40e3-103">Azure 저장소 컨테이너에서 저장 된 액세스 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c40e3-103">Removes a stored access policy from an Azure storage container.</span></span>

## <span data-ttu-id="c40e3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c40e3-104">SYNTAX</span></span>

```
Remove-AzStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c40e3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c40e3-105">DESCRIPTION</span></span>
<span data-ttu-id="c40e3-106">**AzStorageContainerStoredAccessPolicy** Cmdlet은 Azure 저장소 컨테이너에서 저장 된 액세스 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c40e3-106">The **Remove-AzStorageContainerStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage container.</span></span>

## <span data-ttu-id="c40e3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c40e3-107">EXAMPLES</span></span>

### <span data-ttu-id="c40e3-108">예제 1: 저장소 컨테이너에서 저장 된 액세스 정책 제거</span><span class="sxs-lookup"><span data-stu-id="c40e3-108">Example 1: Remove a stored access policy from a storage container</span></span>
```
PS C:\>Remove-AzStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy03"
```

<span data-ttu-id="c40e3-109">이 명령은 MyContainer 라는 저장 된 컨테이너에서 Policy03 라는 액세스 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="c40e3-109">This command removes an access policy named Policy03 from the stored container named MyContainer.</span></span>

## <span data-ttu-id="c40e3-110">변수</span><span class="sxs-lookup"><span data-stu-id="c40e3-110">PARAMETERS</span></span>

### <span data-ttu-id="c40e3-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c40e3-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="c40e3-112">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c40e3-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="c40e3-113">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="c40e3-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="c40e3-114">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c40e3-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="c40e3-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="c40e3-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="c40e3-116">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c40e3-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="c40e3-117">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c40e3-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="c40e3-118">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="c40e3-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="c40e3-119">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c40e3-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="c40e3-120">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="c40e3-120">The default value is 10.</span></span>

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

### <span data-ttu-id="c40e3-121">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="c40e3-121">-Container</span></span>
<span data-ttu-id="c40e3-122">Azure 저장소 컨테이너 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c40e3-122">Specifies the Azure storage container name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c40e3-123">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="c40e3-123">-Context</span></span>
<span data-ttu-id="c40e3-124">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c40e3-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="c40e3-125">저장소 컨텍스트를 얻으려면 New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c40e3-125">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="c40e3-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c40e3-126">-DefaultProfile</span></span>
<span data-ttu-id="c40e3-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c40e3-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c40e3-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c40e3-128">-PassThru</span></span>
<span data-ttu-id="c40e3-129">이 cmdlet이 작업의 성공 여부를 반영 하는 **Boolean** 을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="c40e3-129">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="c40e3-130">기본적으로이 cmdlet은 값을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c40e3-130">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="c40e3-131">-정책</span><span class="sxs-lookup"><span data-stu-id="c40e3-131">-Policy</span></span>
<span data-ttu-id="c40e3-132">이 cmdlet이 제거 하는 저장 된 액세스 정책의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c40e3-132">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c40e3-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c40e3-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="c40e3-134">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c40e3-134">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="c40e3-135">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="c40e3-135">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="c40e3-136">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c40e3-136">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="c40e3-137">-확인</span><span class="sxs-lookup"><span data-stu-id="c40e3-137">-Confirm</span></span>
<span data-ttu-id="c40e3-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c40e3-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c40e3-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c40e3-139">-WhatIf</span></span>
<span data-ttu-id="c40e3-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c40e3-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c40e3-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c40e3-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c40e3-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c40e3-142">CommonParameters</span></span>
<span data-ttu-id="c40e3-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c40e3-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c40e3-144">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c40e3-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c40e3-145">입력</span><span class="sxs-lookup"><span data-stu-id="c40e3-145">INPUTS</span></span>

### <span data-ttu-id="c40e3-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c40e3-146">System.String</span></span>

### <span data-ttu-id="c40e3-147">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c40e3-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c40e3-148">출력</span><span class="sxs-lookup"><span data-stu-id="c40e3-148">OUTPUTS</span></span>

### <span data-ttu-id="c40e3-149">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="c40e3-149">System.Boolean</span></span>

## <span data-ttu-id="c40e3-150">상속자</span><span class="sxs-lookup"><span data-stu-id="c40e3-150">NOTES</span></span>

## <span data-ttu-id="c40e3-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c40e3-151">RELATED LINKS</span></span>

[<span data-ttu-id="c40e3-152">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c40e3-152">Get-AzStorageContainerStoredAccessPolicy</span></span>](./Get-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="c40e3-153">새로운 AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c40e3-153">New-AzStorageContainerStoredAccessPolicy</span></span>](./New-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="c40e3-154">새로운 AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="c40e3-154">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="c40e3-155">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="c40e3-155">Set-AzStorageContainerStoredAccessPolicy</span></span>](./Set-AzStorageContainerStoredAccessPolicy.md)
