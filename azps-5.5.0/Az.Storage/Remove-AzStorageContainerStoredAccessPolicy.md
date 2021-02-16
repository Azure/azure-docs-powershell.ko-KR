---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3E79EE05-7E52-4C54-B985-441BC2599925
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragecontainerstoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainerStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainerStoredAccessPolicy.md
ms.openlocfilehash: 1b8667d08e02c9294a18f4cbf84cb27085cbc118
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197516"
---
# <span data-ttu-id="3db85-101">Remove-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3db85-101">Remove-AzStorageContainerStoredAccessPolicy</span></span>

## <span data-ttu-id="3db85-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3db85-102">SYNOPSIS</span></span>
<span data-ttu-id="3db85-103">Azure 저장소 컨테이너에서 저장된 액세스 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3db85-103">Removes a stored access policy from an Azure storage container.</span></span>

## <span data-ttu-id="3db85-104">구문</span><span class="sxs-lookup"><span data-stu-id="3db85-104">SYNTAX</span></span>

```
Remove-AzStorageContainerStoredAccessPolicy [-Container] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3db85-105">설명</span><span class="sxs-lookup"><span data-stu-id="3db85-105">DESCRIPTION</span></span>
<span data-ttu-id="3db85-106">**Remove-AzStorageContainerStoredAccessPolicy** cmdlet은 Azure 저장소 컨테이너에서 저장된 액세스 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3db85-106">The **Remove-AzStorageContainerStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage container.</span></span>

## <span data-ttu-id="3db85-107">예제</span><span class="sxs-lookup"><span data-stu-id="3db85-107">EXAMPLES</span></span>

### <span data-ttu-id="3db85-108">예제 1: 저장소 컨테이너에서 저장된 액세스 정책 제거</span><span class="sxs-lookup"><span data-stu-id="3db85-108">Example 1: Remove a stored access policy from a storage container</span></span>
```
PS C:\>Remove-AzStorageContainerStoredAccessPolicy -Container "MyContainer" -Policy "Policy03"
```

<span data-ttu-id="3db85-109">이 명령은 MyContainer라는 저장된 컨테이너에서 Policy03이라는 액세스 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="3db85-109">This command removes an access policy named Policy03 from the stored container named MyContainer.</span></span>

## <span data-ttu-id="3db85-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3db85-110">PARAMETERS</span></span>

### <span data-ttu-id="3db85-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3db85-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="3db85-112">하나의 서비스 요청에 대해 클라이언트 쪽 시간(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3db85-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="3db85-113">이전 호출이 지정된 간격에서 실패하는 경우 이 cmdlet은 요청을 다시 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="3db85-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="3db85-114">이 cmdlet이 간격이 경과하기 전에 성공적인 응답을 받지 못하면 이 cmdlet은 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="3db85-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="3db85-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="3db85-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="3db85-116">최대 동시 네트워크 호출을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3db85-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="3db85-117">이 매개 변수를 사용하면 최대 동시 네트워크 호출 수를 지정하여 동시성으로 로컬 CPU 및 대역폭 사용량을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3db85-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="3db85-118">지정된 값은 절대 개수로, 코어 수에 곱하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3db85-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="3db85-119">이 매개 변수는 초당 100킬로비트와 같은 낮은 대역폭 환경에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3db85-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="3db85-120">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="3db85-120">The default value is 10.</span></span>

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

### <span data-ttu-id="3db85-121">-Container</span><span class="sxs-lookup"><span data-stu-id="3db85-121">-Container</span></span>
<span data-ttu-id="3db85-122">Azure 저장소 컨테이너 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3db85-122">Specifies the Azure storage container name.</span></span>

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

### <span data-ttu-id="3db85-123">-Context</span><span class="sxs-lookup"><span data-stu-id="3db85-123">-Context</span></span>
<span data-ttu-id="3db85-124">Azure 저장소 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3db85-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="3db85-125">저장소 컨텍스트를 얻습니다. New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3db85-125">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="3db85-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3db85-126">-DefaultProfile</span></span>
<span data-ttu-id="3db85-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3db85-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3db85-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3db85-128">-PassThru</span></span>
<span data-ttu-id="3db85-129">이 cmdlet은 작업의  성공을 반영하는 부울을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="3db85-129">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="3db85-130">기본적으로 이 cmdlet은 값을 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3db85-130">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="3db85-131">-Policy</span><span class="sxs-lookup"><span data-stu-id="3db85-131">-Policy</span></span>
<span data-ttu-id="3db85-132">이 cmdlet에서 제거하는 저장된 액세스 정책의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3db85-132">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3db85-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="3db85-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="3db85-134">하나의 서비스 요청에 대해 클라이언트 쪽 시간(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3db85-134">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="3db85-135">이전 호출이 지정된 간격에서 실패하는 경우 이 cmdlet은 요청을 다시 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="3db85-135">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="3db85-136">이 cmdlet이 간격이 경과하기 전에 성공적인 응답을 받지 못하면 이 cmdlet은 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="3db85-136">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="3db85-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3db85-137">-Confirm</span></span>
<span data-ttu-id="3db85-138">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3db85-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3db85-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3db85-139">-WhatIf</span></span>
<span data-ttu-id="3db85-140">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="3db85-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3db85-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3db85-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3db85-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3db85-142">CommonParameters</span></span>
<span data-ttu-id="3db85-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3db85-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3db85-144">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="3db85-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3db85-145">입력</span><span class="sxs-lookup"><span data-stu-id="3db85-145">INPUTS</span></span>

### <span data-ttu-id="3db85-146">System.String</span><span class="sxs-lookup"><span data-stu-id="3db85-146">System.String</span></span>

### <span data-ttu-id="3db85-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3db85-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3db85-148">출력</span><span class="sxs-lookup"><span data-stu-id="3db85-148">OUTPUTS</span></span>

### <span data-ttu-id="3db85-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3db85-149">System.Boolean</span></span>

## <span data-ttu-id="3db85-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3db85-150">NOTES</span></span>

## <span data-ttu-id="3db85-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3db85-151">RELATED LINKS</span></span>

[<span data-ttu-id="3db85-152">Get-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3db85-152">Get-AzStorageContainerStoredAccessPolicy</span></span>](./Get-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="3db85-153">New-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3db85-153">New-AzStorageContainerStoredAccessPolicy</span></span>](./New-AzStorageContainerStoredAccessPolicy.md)

[<span data-ttu-id="3db85-154">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="3db85-154">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="3db85-155">Set-AzStorageContainerStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="3db85-155">Set-AzStorageContainerStoredAccessPolicy</span></span>](./Set-AzStorageContainerStoredAccessPolicy.md)
