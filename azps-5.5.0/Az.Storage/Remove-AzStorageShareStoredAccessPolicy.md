---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E2CCDA8F-2D45-4F25-B297-337B7AB021E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: d8c9e0e49ba7a5caa9cb93290ef5e96b60fd4430
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190753"
---
# <span data-ttu-id="4fe12-101">Remove-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4fe12-101">Remove-AzStorageShareStoredAccessPolicy</span></span>

## <span data-ttu-id="4fe12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fe12-102">SYNOPSIS</span></span>
<span data-ttu-id="4fe12-103">저장소 공유에서 저장된 액세스 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4fe12-103">Removes a stored access policy from a Storage share.</span></span>

## <span data-ttu-id="4fe12-104">구문</span><span class="sxs-lookup"><span data-stu-id="4fe12-104">SYNTAX</span></span>

```
Remove-AzStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4fe12-105">설명</span><span class="sxs-lookup"><span data-stu-id="4fe12-105">DESCRIPTION</span></span>
<span data-ttu-id="4fe12-106">**Remove-AzStorageShareStoredAccessPolicy** cmdlet은 Azure Storage 공유에서 저장된 액세스 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4fe12-106">The **Remove-AzStorageShareStoredAccessPolicy** cmdlet removes a stored access policy from an Azure Storage share.</span></span>

## <span data-ttu-id="4fe12-107">예제</span><span class="sxs-lookup"><span data-stu-id="4fe12-107">EXAMPLES</span></span>

### <span data-ttu-id="4fe12-108">예제 1: Azure Storage 공유에서 저장된 액세스 정책 제거</span><span class="sxs-lookup"><span data-stu-id="4fe12-108">Example 1: Remove a stored access policy from an Azure Storage share</span></span>
```
PS C:\>Remove-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy"
```

<span data-ttu-id="4fe12-109">이 명령은 ContosoShare에서 GeneralPolicy라는 저장된 액세스 정책을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4fe12-109">This command removes a stored access policy named GeneralPolicy from ContosoShare.</span></span>

## <span data-ttu-id="4fe12-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4fe12-110">PARAMETERS</span></span>

### <span data-ttu-id="4fe12-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4fe12-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="4fe12-112">하나의 서비스 요청에 대해 클라이언트 쪽 시간(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4fe12-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="4fe12-113">이전 호출이 지정된 간격에서 실패하는 경우 이 cmdlet은 요청을 다시 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="4fe12-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="4fe12-114">이 cmdlet이 간격이 경과하기 전에 성공적인 응답을 받지 못하면 이 cmdlet은 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="4fe12-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="4fe12-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="4fe12-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="4fe12-116">최대 동시 네트워크 호출을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4fe12-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="4fe12-117">이 매개 변수를 사용하여 최대 동시 네트워크 호출 수를 지정하여 동시성으로 로컬 CPU 및 대역폭 사용량을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4fe12-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="4fe12-118">지정된 값은 절대 개수로, 코어 수에 곱하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4fe12-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="4fe12-119">이 매개 변수는 초당 100킬로비트와 같은 낮은 대역폭 환경에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4fe12-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="4fe12-120">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="4fe12-120">The default value is 10.</span></span>

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

### <span data-ttu-id="4fe12-121">-Context</span><span class="sxs-lookup"><span data-stu-id="4fe12-121">-Context</span></span>
<span data-ttu-id="4fe12-122">Azure 저장소 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4fe12-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="4fe12-123">저장소 컨텍스트를 얻습니다. [New-AzStorageContext](./New-AzStorageContext.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fe12-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="4fe12-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fe12-124">-DefaultProfile</span></span>
<span data-ttu-id="4fe12-125">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4fe12-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fe12-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4fe12-126">-PassThru</span></span>
<span data-ttu-id="4fe12-127">이 cmdlet은 작업의  성공을 반영하는 부울을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="4fe12-127">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="4fe12-128">기본적으로 이 cmdlet은 값을 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4fe12-128">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="4fe12-129">-Policy</span><span class="sxs-lookup"><span data-stu-id="4fe12-129">-Policy</span></span>
<span data-ttu-id="4fe12-130">이 cmdlet에서 제거하는 저장된 액세스 정책의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4fe12-130">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4fe12-131">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="4fe12-131">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="4fe12-132">요청의 서버 부분에 대한 시간 제한 기간의 길이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4fe12-132">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="4fe12-133">-ShareName</span><span class="sxs-lookup"><span data-stu-id="4fe12-133">-ShareName</span></span>
<span data-ttu-id="4fe12-134">이 cmdlet이 정책을 제거하는 저장소 공유 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4fe12-134">Specifies the Storage share name for which this cmdlet removes a policy.</span></span>

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

### <span data-ttu-id="4fe12-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4fe12-135">-Confirm</span></span>
<span data-ttu-id="4fe12-136">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4fe12-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4fe12-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fe12-137">-WhatIf</span></span>
<span data-ttu-id="4fe12-138">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="4fe12-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fe12-139">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4fe12-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4fe12-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fe12-140">CommonParameters</span></span>
<span data-ttu-id="4fe12-141">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4fe12-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fe12-142">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4fe12-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fe12-143">입력</span><span class="sxs-lookup"><span data-stu-id="4fe12-143">INPUTS</span></span>

### <span data-ttu-id="4fe12-144">System.String</span><span class="sxs-lookup"><span data-stu-id="4fe12-144">System.String</span></span>

### <span data-ttu-id="4fe12-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4fe12-145">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4fe12-146">출력</span><span class="sxs-lookup"><span data-stu-id="4fe12-146">OUTPUTS</span></span>

### <span data-ttu-id="4fe12-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4fe12-147">System.Boolean</span></span>

## <span data-ttu-id="4fe12-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4fe12-148">NOTES</span></span>

## <span data-ttu-id="4fe12-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4fe12-149">RELATED LINKS</span></span>

[<span data-ttu-id="4fe12-150">Get-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4fe12-150">Get-AzStorageShareStoredAccessPolicy</span></span>](./Get-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="4fe12-151">New-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4fe12-151">New-AzStorageShareStoredAccessPolicy</span></span>](./New-AzStorageShareStoredAccessPolicy.md)

[<span data-ttu-id="4fe12-152">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="4fe12-152">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="4fe12-153">Set-AzStorageShareStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4fe12-153">Set-AzStorageShareStoredAccessPolicy</span></span>](./Set-AzStorageShareStoredAccessPolicy.md)
