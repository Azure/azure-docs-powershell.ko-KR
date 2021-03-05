---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6A46DA60-2ACF-4842-B5B3-58944264854A
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainer.md
ms.openlocfilehash: e2d408e54aa4b4e2de766d4f4e058d2edd22cb22
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970144"
---
# <span data-ttu-id="c5958-101">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c5958-101">Remove-AzStorageContainer</span></span>

## <span data-ttu-id="c5958-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5958-102">SYNOPSIS</span></span>
<span data-ttu-id="c5958-103">지정된 저장소 컨테이너를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c5958-103">Removes the specified storage container.</span></span>

## <span data-ttu-id="c5958-104">구문</span><span class="sxs-lookup"><span data-stu-id="c5958-104">SYNTAX</span></span>

```
Remove-AzStorageContainer [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c5958-105">설명</span><span class="sxs-lookup"><span data-stu-id="c5958-105">DESCRIPTION</span></span>
<span data-ttu-id="c5958-106">**Remove-AzStorageContainer** cmdlet은 Azure에서 지정된 저장소 컨테이너를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c5958-106">The **Remove-AzStorageContainer** cmdlet removes the specified storage container in Azure.</span></span>

## <span data-ttu-id="c5958-107">예제</span><span class="sxs-lookup"><span data-stu-id="c5958-107">EXAMPLES</span></span>

### <span data-ttu-id="c5958-108">예제 1: 컨테이너 제거</span><span class="sxs-lookup"><span data-stu-id="c5958-108">Example 1: Remove a container</span></span>
```
PS C:\>Remove-AzStorageContainer -Name "MyTestContainer"
```

<span data-ttu-id="c5958-109">이 예제에서는 MyTestContainer라는 컨테이너를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="c5958-109">This example removes a container named MyTestContainer.</span></span>

## <span data-ttu-id="c5958-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c5958-110">PARAMETERS</span></span>

### <span data-ttu-id="c5958-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c5958-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="c5958-112">하나의 서비스 요청에 대해 클라이언트 쪽 시간 간격(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c5958-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="c5958-113">지정된 간격에서 이전 호출이 실패하면 이 cmdlet에서 요청을 다시 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="c5958-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="c5958-114">간격이 경과하기 전에 이 cmdlet에서 성공적인 응답을 받지 못하면 이 cmdlet은 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="c5958-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="c5958-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="c5958-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="c5958-116">최대 동시 네트워크 호출을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c5958-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="c5958-117">이 매개 변수를 사용하여 최대 동시 네트워크 호출 수를 지정하여 로컬 CPU 및 대역폭 사용량을 제한하는 동시성 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c5958-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="c5958-118">지정된 값은 절대 개수로 코어 수에 곱하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c5958-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="c5958-119">이 매개 변수는 초당 100킬로비트와 같은 대역폭이 낮은 환경에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c5958-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="c5958-120">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="c5958-120">The default value is 10.</span></span>

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

### <span data-ttu-id="c5958-121">-Context</span><span class="sxs-lookup"><span data-stu-id="c5958-121">-Context</span></span>
<span data-ttu-id="c5958-122">제거할 컨테이너에 대한 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c5958-122">Specifies a context for the container you want to remove.</span></span>
<span data-ttu-id="c5958-123">New-AzStorageContext cmdlet을 사용하여 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c5958-123">You can use the New-AzStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="c5958-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5958-124">-DefaultProfile</span></span>
<span data-ttu-id="c5958-125">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c5958-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5958-126">-Force</span><span class="sxs-lookup"><span data-stu-id="c5958-126">-Force</span></span>
<span data-ttu-id="c5958-127">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="c5958-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c5958-128">-Name</span><span class="sxs-lookup"><span data-stu-id="c5958-128">-Name</span></span>
<span data-ttu-id="c5958-129">제거할 컨테이너의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c5958-129">Specifies the name of the container to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c5958-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c5958-130">-PassThru</span></span>
<span data-ttu-id="c5958-131">이 cmdlet은 작업의 성공을 반영하는 **부울을** 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="c5958-131">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="c5958-132">기본적으로 이 cmdlet은 값을 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c5958-132">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="c5958-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="c5958-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="c5958-134">요청에 대해 서비스 쪽 시간 시간 간격(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c5958-134">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="c5958-135">서비스가 요청을 처리하기 전에 지정된 간격이 경과하면 저장소 서비스가 오류를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="c5958-135">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="c5958-136">-확인</span><span class="sxs-lookup"><span data-stu-id="c5958-136">-Confirm</span></span>
<span data-ttu-id="c5958-137">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c5958-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5958-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5958-138">-WhatIf</span></span>
<span data-ttu-id="c5958-139">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c5958-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5958-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c5958-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5958-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5958-141">CommonParameters</span></span>
<span data-ttu-id="c5958-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c5958-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5958-143">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c5958-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5958-144">입력</span><span class="sxs-lookup"><span data-stu-id="c5958-144">INPUTS</span></span>

### <span data-ttu-id="c5958-145">System.String</span><span class="sxs-lookup"><span data-stu-id="c5958-145">System.String</span></span>

### <span data-ttu-id="c5958-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c5958-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="c5958-147">출력</span><span class="sxs-lookup"><span data-stu-id="c5958-147">OUTPUTS</span></span>

### <span data-ttu-id="c5958-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c5958-148">System.Boolean</span></span>

## <span data-ttu-id="c5958-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c5958-149">NOTES</span></span>

## <span data-ttu-id="c5958-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c5958-150">RELATED LINKS</span></span>

[<span data-ttu-id="c5958-151">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c5958-151">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="c5958-152">New-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="c5958-152">New-AzStorageContainer</span></span>](./New-AzStorageContainer.md)
