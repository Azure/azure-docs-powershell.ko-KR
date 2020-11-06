---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM
ms.assetid: 5563B6E8-805B-463B-AF78-4F5750F5CDEA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.scheduler/new-azurermschedulerstoragequeuejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerStorageQueueJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerStorageQueueJob.md
ms.openlocfilehash: eb72b64576524d85730e89f6eece094591a12158
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534672"
---
# <span data-ttu-id="0ef63-101">New-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="0ef63-101">New-AzureRmSchedulerStorageQueueJob</span></span>

## <span data-ttu-id="0ef63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ef63-102">SYNOPSIS</span></span>
<span data-ttu-id="0ef63-103">저장소 큐 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0ef63-103">Creates a storage queue job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ef63-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0ef63-104">SYNTAX</span></span>

```
New-AzureRmSchedulerStorageQueueJob -ResourceGroupName <String> -JobCollectionName <String> -JobName <String>
 -StorageQueueAccount <String> -StorageQueueName <String> -StorageSASToken <String>
 -StorageQueueMessage <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ef63-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0ef63-105">DESCRIPTION</span></span>
<span data-ttu-id="0ef63-106">**새 AzureRmSchedulerStorageQueueJob** Cmdlet은 Azure Scheduler에서 저장소 큐 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0ef63-106">The **New-AzureRmSchedulerStorageQueueJob** cmdlet creates a storage queue job in Azure Scheduler.</span></span>

<span data-ttu-id="0ef63-107">이 cmdlet은 *Erroractiontype* 매개 변수에 기반 하는 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ef63-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="0ef63-108">동적 매개 변수는 다른 매개 변수 값에 따라 사용할 수 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0ef63-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="0ef63-109">다른 매개 변수를 지정한 후 동적 매개 변수의 이름을 검색 하려면 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ef63-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="0ef63-110">필수 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ef63-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="0ef63-111">예제의</span><span class="sxs-lookup"><span data-stu-id="0ef63-111">EXAMPLES</span></span>

## <span data-ttu-id="0ef63-112">변수</span><span class="sxs-lookup"><span data-stu-id="0ef63-112">PARAMETERS</span></span>

### <span data-ttu-id="0ef63-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ef63-113">-DefaultProfile</span></span>
<span data-ttu-id="0ef63-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0ef63-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ef63-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="0ef63-115">-EndTime</span></span>
<span data-ttu-id="0ef63-116">작업에 대 한 종료 시간을 **DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ef63-116">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="0ef63-117">**DateTime** 개체를 가져오려면 Get-Date cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ef63-117">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ef63-118">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="0ef63-118">-ErrorActionType</span></span>
<span data-ttu-id="0ef63-119">작업에 대 한 오류 동작 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ef63-119">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="0ef63-120">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0ef63-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0ef63-121">Http</span><span class="sxs-lookup"><span data-stu-id="0ef63-121">Http</span></span> 
- <span data-ttu-id="0ef63-122">Https</span><span class="sxs-lookup"><span data-stu-id="0ef63-122">Https</span></span> 
- <span data-ttu-id="0ef63-123">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="0ef63-123">StorageQueue</span></span> 
- <span data-ttu-id="0ef63-124">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="0ef63-124">ServiceBusQueue</span></span> 
- <span data-ttu-id="0ef63-125">Service<c13> Stopic</span><span class="sxs-lookup"><span data-stu-id="0ef63-125">ServiceBusTopic</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https, StorageQueue, ServiceBusQueue, ServiceBusTopic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ef63-126">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="0ef63-126">-ExecutionCount</span></span>
<span data-ttu-id="0ef63-127">작업이 실행 되는 횟수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ef63-127">Specifies how many times the job runs.</span></span>
<span data-ttu-id="0ef63-128">기본적으로 작업이 무한정 되풀이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0ef63-128">By default, a job recurs indefinitely.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ef63-129">-빈도</span><span class="sxs-lookup"><span data-stu-id="0ef63-129">-Frequency</span></span>
<span data-ttu-id="0ef63-130">작업의 빈도를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ef63-130">Specifies a frequency for the job.</span></span>
<span data-ttu-id="0ef63-131">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0ef63-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0ef63-132">길이의</span><span class="sxs-lookup"><span data-stu-id="0ef63-132">Minute</span></span> 
- <span data-ttu-id="0ef63-133">시간씩</span><span class="sxs-lookup"><span data-stu-id="0ef63-133">Hour</span></span> 
- <span data-ttu-id="0ef63-134">부활절</span><span class="sxs-lookup"><span data-stu-id="0ef63-134">Day</span></span> 
- <span data-ttu-id="0ef63-135">이번</span><span class="sxs-lookup"><span data-stu-id="0ef63-135">Week</span></span> 
- <span data-ttu-id="0ef63-136">달은</span><span class="sxs-lookup"><span data-stu-id="0ef63-136">Month</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Minute, Hour, Day, Week, Month

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ef63-137">-Interval</span><span class="sxs-lookup"><span data-stu-id="0ef63-137">-Interval</span></span>
<span data-ttu-id="0ef63-138">작업에 대 한 되풀이 간격을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ef63-138">Specifies an interval of recurrence for the job.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ef63-139">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="0ef63-139">-JobCollectionName</span></span>
<span data-ttu-id="0ef63-140">작업이 속한 작업 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ef63-140">Specifies the name of the job collection to which the job belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ef63-141">-JobName</span><span class="sxs-lookup"><span data-stu-id="0ef63-141">-JobName</span></span>
<span data-ttu-id="0ef63-142">작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ef63-142">Specifies a name for the job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ef63-143">-JobState</span><span class="sxs-lookup"><span data-stu-id="0ef63-143">-JobState</span></span>
<span data-ttu-id="0ef63-144">작업의 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ef63-144">Specifies the state of the job.</span></span>
<span data-ttu-id="0ef63-145">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0ef63-145">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0ef63-146">수</span><span class="sxs-lookup"><span data-stu-id="0ef63-146">Enabled</span></span> 
- <span data-ttu-id="0ef63-147">비활성화</span><span class="sxs-lookup"><span data-stu-id="0ef63-147">Disabled</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ef63-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ef63-148">-ResourceGroupName</span></span>
<span data-ttu-id="0ef63-149">작업이 속한 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ef63-149">Specifies the resource group to which the job belongs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ef63-150">-StartTime</span><span class="sxs-lookup"><span data-stu-id="0ef63-150">-StartTime</span></span>
<span data-ttu-id="0ef63-151">작업에 대 한 시작 시간을 **DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ef63-151">Specifies the start time, as a **DateTime** object, for the job.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ef63-152">-StorageQueueAccount</span><span class="sxs-lookup"><span data-stu-id="0ef63-152">-StorageQueueAccount</span></span>
<span data-ttu-id="0ef63-153">저장소 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ef63-153">Specifies a storage account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ef63-154">-StorageQueueMessage</span><span class="sxs-lookup"><span data-stu-id="0ef63-154">-StorageQueueMessage</span></span>
<span data-ttu-id="0ef63-155">저장소 작업에 대 한 큐 메시지를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ef63-155">Specifies a queue message for the storage job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ef63-156">-StorageQueueName</span><span class="sxs-lookup"><span data-stu-id="0ef63-156">-StorageQueueName</span></span>
<span data-ttu-id="0ef63-157">저장소 큐 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ef63-157">Specifies a storage queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ef63-158">-StorageSASToken</span><span class="sxs-lookup"><span data-stu-id="0ef63-158">-StorageSASToken</span></span>
<span data-ttu-id="0ef63-159">저장소 큐에 대 한 공유 액세스 서명 토큰을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ef63-159">Specifies a shared access signature token for a storage queue.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ef63-160">-확인</span><span class="sxs-lookup"><span data-stu-id="0ef63-160">-Confirm</span></span>
<span data-ttu-id="0ef63-161">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ef63-161">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ef63-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ef63-162">-WhatIf</span></span>
<span data-ttu-id="0ef63-163">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0ef63-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ef63-164">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0ef63-164">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ef63-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ef63-165">CommonParameters</span></span>
<span data-ttu-id="0ef63-166">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ef63-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ef63-167">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ef63-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ef63-168">입력</span><span class="sxs-lookup"><span data-stu-id="0ef63-168">INPUTS</span></span>

### <span data-ttu-id="0ef63-169">않아야</span><span class="sxs-lookup"><span data-stu-id="0ef63-169">None</span></span>
<span data-ttu-id="0ef63-170">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0ef63-170">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0ef63-171">출력</span><span class="sxs-lookup"><span data-stu-id="0ef63-171">OUTPUTS</span></span>

### <span data-ttu-id="0ef63-172">PSSchedulerJobDefinition의 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="0ef63-172">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="0ef63-173">상속자</span><span class="sxs-lookup"><span data-stu-id="0ef63-173">NOTES</span></span>

## <span data-ttu-id="0ef63-174">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0ef63-174">RELATED LINKS</span></span>

[<span data-ttu-id="0ef63-175">새로운 AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="0ef63-175">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="0ef63-176">새로운 AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="0ef63-176">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="0ef63-177">새로운 AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="0ef63-177">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="0ef63-178">새로운 AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="0ef63-178">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="0ef63-179">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="0ef63-179">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="0ef63-180">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="0ef63-180">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="0ef63-181">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="0ef63-181">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="0ef63-182">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="0ef63-182">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="0ef63-183">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="0ef63-183">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


