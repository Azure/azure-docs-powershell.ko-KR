---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6A46DA60-2ACF-4842-B5B3-58944264854A
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageContainer.md
ms.openlocfilehash: d1de24650c2e40b05f708885c2c9a017105dabb2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93874271"
---
# <span data-ttu-id="7201a-101">Remove-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="7201a-101">Remove-AzStorageContainer</span></span>

## <span data-ttu-id="7201a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7201a-102">SYNOPSIS</span></span>
<span data-ttu-id="7201a-103">지정 된 저장소 컨테이너를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7201a-103">Removes the specified storage container.</span></span>

## <span data-ttu-id="7201a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7201a-104">SYNTAX</span></span>

```
Remove-AzStorageContainer [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7201a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7201a-105">DESCRIPTION</span></span>
<span data-ttu-id="7201a-106">**AzStorageContainer** Cmdlet은 Azure에서 지정 된 저장소 컨테이너를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7201a-106">The **Remove-AzStorageContainer** cmdlet removes the specified storage container in Azure.</span></span>

## <span data-ttu-id="7201a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7201a-107">EXAMPLES</span></span>

### <span data-ttu-id="7201a-108">예제 1: 컨테이너 제거</span><span class="sxs-lookup"><span data-stu-id="7201a-108">Example 1: Remove a container</span></span>
```
PS C:\>Remove-AzStorageContainer -Name "MyTestContainer"
```

<span data-ttu-id="7201a-109">이 예제에서는 MyTestContainer 이라는 컨테이너를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7201a-109">This example removes a container named MyTestContainer.</span></span>

## <span data-ttu-id="7201a-110">변수</span><span class="sxs-lookup"><span data-stu-id="7201a-110">PARAMETERS</span></span>

### <span data-ttu-id="7201a-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7201a-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="7201a-112">한 서비스 요청에 대 한 클라이언트 쪽 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7201a-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="7201a-113">이전 호출이 지정 된 간격으로 실행 되지 않는 경우이 cmdlet은 요청을 다시 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="7201a-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="7201a-114">이 cmdlet이 간격이 경과할 때까지 성공적인 응답을 받지 못하는 경우이 cmdlet은 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7201a-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="7201a-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="7201a-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="7201a-116">최대 동시 네트워크 통화를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7201a-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="7201a-117">이 매개 변수를 사용 하 여 최대 동시 네트워크 호출 수를 지정 하 여 로컬 CPU 및 대역폭 사용량을 스로틀 하도록 병행성을 제한할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7201a-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="7201a-118">지정 된 값이 절대 수 이며 코어 개수로 곱해집니다.</span><span class="sxs-lookup"><span data-stu-id="7201a-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="7201a-119">이 매개 변수는 낮은 대역폭 환경 (예: 초당 100 킬로 비트)에서 네트워크 연결 문제를 줄이는 데 도움이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7201a-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="7201a-120">기본값은 10입니다.</span><span class="sxs-lookup"><span data-stu-id="7201a-120">The default value is 10.</span></span>

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

### <span data-ttu-id="7201a-121">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="7201a-121">-Context</span></span>
<span data-ttu-id="7201a-122">제거 하려는 컨테이너에 대 한 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7201a-122">Specifies a context for the container you want to remove.</span></span>
<span data-ttu-id="7201a-123">New-AzStorageContext cmdlet을 사용 하 여 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7201a-123">You can use the New-AzStorageContext cmdlet to create it.</span></span>

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

### <span data-ttu-id="7201a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7201a-124">-DefaultProfile</span></span>
<span data-ttu-id="7201a-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7201a-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7201a-126">-Force</span><span class="sxs-lookup"><span data-stu-id="7201a-126">-Force</span></span>
<span data-ttu-id="7201a-127">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="7201a-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7201a-128">-이름</span><span class="sxs-lookup"><span data-stu-id="7201a-128">-Name</span></span>
<span data-ttu-id="7201a-129">제거할 컨테이너의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7201a-129">Specifies the name of the container to remove.</span></span>

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

### <span data-ttu-id="7201a-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7201a-130">-PassThru</span></span>
<span data-ttu-id="7201a-131">이 cmdlet이 작업의 성공 여부를 반영 하는 **Boolean** 을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7201a-131">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="7201a-132">기본적으로이 cmdlet은 값을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7201a-132">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="7201a-133">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="7201a-133">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="7201a-134">요청에 대 한 서비스 측 시간 제한 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7201a-134">Specifies the service side time-out interval, in seconds, for a request.</span></span>
<span data-ttu-id="7201a-135">서비스가 요청을 처리 하기 전에 지정 된 간격이 경과 하면 저장소 서비스에서 오류를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7201a-135">If the specified interval elapses before the service processes the request, the storage service returns an error.</span></span>

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

### <span data-ttu-id="7201a-136">-확인</span><span class="sxs-lookup"><span data-stu-id="7201a-136">-Confirm</span></span>
<span data-ttu-id="7201a-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7201a-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7201a-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7201a-138">-WhatIf</span></span>
<span data-ttu-id="7201a-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7201a-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7201a-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7201a-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7201a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7201a-141">CommonParameters</span></span>
<span data-ttu-id="7201a-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7201a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7201a-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7201a-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7201a-144">입력</span><span class="sxs-lookup"><span data-stu-id="7201a-144">INPUTS</span></span>

### <span data-ttu-id="7201a-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7201a-145">System.String</span></span>

### <span data-ttu-id="7201a-146">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7201a-146">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7201a-147">출력</span><span class="sxs-lookup"><span data-stu-id="7201a-147">OUTPUTS</span></span>

### <span data-ttu-id="7201a-148">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="7201a-148">System.Boolean</span></span>

## <span data-ttu-id="7201a-149">상속자</span><span class="sxs-lookup"><span data-stu-id="7201a-149">NOTES</span></span>

## <span data-ttu-id="7201a-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7201a-150">RELATED LINKS</span></span>

[<span data-ttu-id="7201a-151">Get-AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="7201a-151">Get-AzStorageContainer</span></span>](./Get-AzStorageContainer.md)

[<span data-ttu-id="7201a-152">새로운 AzStorageContainer</span><span class="sxs-lookup"><span data-stu-id="7201a-152">New-AzStorageContainer</span></span>](./New-AzStorageContainer.md)
