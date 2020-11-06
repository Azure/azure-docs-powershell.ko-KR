---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: 52987702-D101-4D5D-852D-2809374292F4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerServiceBusQueueJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/New-AzureRmSchedulerServiceBusQueueJob.md
ms.openlocfilehash: a61d745cb748d27baf7b07b6b4389077e50aaa24
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533855"
---
# <span data-ttu-id="ccf1c-101">New-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="ccf1c-101">New-AzureRmSchedulerServiceBusQueueJob</span></span>

## <span data-ttu-id="ccf1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ccf1c-102">SYNOPSIS</span></span>
<span data-ttu-id="ccf1c-103">Service bus 큐 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ccf1c-103">Creates a service bus queue job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ccf1c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ccf1c-104">SYNTAX</span></span>

```
New-AzureRmSchedulerServiceBusQueueJob -ResourceGroupName <String> -JobCollectionName <String>
 -JobName <String> -ServiceBusQueueName <String> -ServiceBusNamespace <String>
 -ServiceBusTransportType <String> -ServiceBusMessage <String> -ServiceBusSasKeyName <String>
 -ServiceBusSasKeyValue <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccf1c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ccf1c-105">DESCRIPTION</span></span>
<span data-ttu-id="ccf1c-106">**AzureRmSchedulerServiceBusQueueJob** Cmdlet은 Azure Scheduler에서 service bus 큐 작업을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ccf1c-106">The **New-AzureRmSchedulerServiceBusQueueJob** cmdlet creates a service bus queue job in Azure Scheduler.</span></span>

<span data-ttu-id="ccf1c-107">이 cmdlet은 *Erroractiontype* 매개 변수에 기반 하는 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccf1c-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="ccf1c-108">동적 매개 변수는 다른 매개 변수 값에 따라 사용할 수 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ccf1c-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="ccf1c-109">다른 매개 변수를 지정한 후 동적 매개 변수의 이름을 검색 하려면 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccf1c-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="ccf1c-110">필수 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccf1c-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="ccf1c-111">예제의</span><span class="sxs-lookup"><span data-stu-id="ccf1c-111">EXAMPLES</span></span>

## <span data-ttu-id="ccf1c-112">변수</span><span class="sxs-lookup"><span data-stu-id="ccf1c-112">PARAMETERS</span></span>

### <span data-ttu-id="ccf1c-113">-EndTime</span><span class="sxs-lookup"><span data-stu-id="ccf1c-113">-EndTime</span></span>
<span data-ttu-id="ccf1c-114">작업에 대 한 종료 시간을 **DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccf1c-114">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="ccf1c-115">**DateTime** 개체를 가져오려면 Get-Date cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccf1c-115">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="ccf1c-116">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="ccf1c-116">-ErrorActionType</span></span>
<span data-ttu-id="ccf1c-117">작업에 대 한 오류 동작 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccf1c-117">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="ccf1c-118">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ccf1c-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ccf1c-119">Http</span><span class="sxs-lookup"><span data-stu-id="ccf1c-119">Http</span></span> 
- <span data-ttu-id="ccf1c-120">Https</span><span class="sxs-lookup"><span data-stu-id="ccf1c-120">Https</span></span> 
- <span data-ttu-id="ccf1c-121">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="ccf1c-121">StorageQueue</span></span> 
- <span data-ttu-id="ccf1c-122">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="ccf1c-122">ServiceBusQueue</span></span> 
- <span data-ttu-id="ccf1c-123">Service<c13> Stopic</span><span class="sxs-lookup"><span data-stu-id="ccf1c-123">ServiceBusTopic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https, StorageQueue, ServiceBusQueue, ServiceBusTopic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccf1c-124">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="ccf1c-124">-ExecutionCount</span></span>
<span data-ttu-id="ccf1c-125">작업이 실행 되는 횟수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccf1c-125">Specifies how many times the job runs.</span></span>
<span data-ttu-id="ccf1c-126">기본적으로 작업이 무한정 되풀이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ccf1c-126">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="ccf1c-127">-빈도</span><span class="sxs-lookup"><span data-stu-id="ccf1c-127">-Frequency</span></span>
<span data-ttu-id="ccf1c-128">작업의 빈도를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccf1c-128">Specifies a frequency for the job.</span></span>
<span data-ttu-id="ccf1c-129">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ccf1c-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ccf1c-130">길이의</span><span class="sxs-lookup"><span data-stu-id="ccf1c-130">Minute</span></span> 
- <span data-ttu-id="ccf1c-131">시간씩</span><span class="sxs-lookup"><span data-stu-id="ccf1c-131">Hour</span></span> 
- <span data-ttu-id="ccf1c-132">부활절</span><span class="sxs-lookup"><span data-stu-id="ccf1c-132">Day</span></span> 
- <span data-ttu-id="ccf1c-133">이번</span><span class="sxs-lookup"><span data-stu-id="ccf1c-133">Week</span></span> 
- <span data-ttu-id="ccf1c-134">달은</span><span class="sxs-lookup"><span data-stu-id="ccf1c-134">Month</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Minute, Hour, Day, Week, Month

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf1c-135">-Interval</span><span class="sxs-lookup"><span data-stu-id="ccf1c-135">-Interval</span></span>
<span data-ttu-id="ccf1c-136">작업에 대 한 되풀이 간격을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccf1c-136">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="ccf1c-137">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="ccf1c-137">-JobCollectionName</span></span>
<span data-ttu-id="ccf1c-138">작업이 속한 작업 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccf1c-138">Specifies the name of the job collection to which the job belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccf1c-139">-JobName</span><span class="sxs-lookup"><span data-stu-id="ccf1c-139">-JobName</span></span>
<span data-ttu-id="ccf1c-140">작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccf1c-140">Specifies a name for the job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccf1c-141">-JobState</span><span class="sxs-lookup"><span data-stu-id="ccf1c-141">-JobState</span></span>
<span data-ttu-id="ccf1c-142">작업의 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccf1c-142">Specifies the state of the job.</span></span>
<span data-ttu-id="ccf1c-143">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ccf1c-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ccf1c-144">수</span><span class="sxs-lookup"><span data-stu-id="ccf1c-144">Enabled</span></span> 
- <span data-ttu-id="ccf1c-145">비활성화</span><span class="sxs-lookup"><span data-stu-id="ccf1c-145">Disabled</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccf1c-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccf1c-146">-ResourceGroupName</span></span>
<span data-ttu-id="ccf1c-147">작업이 속한 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccf1c-147">Specifies the resource group to which the job belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccf1c-148">-ServiceBusMessage</span><span class="sxs-lookup"><span data-stu-id="ccf1c-148">-ServiceBusMessage</span></span>
<span data-ttu-id="ccf1c-149">Service bus 큐 메시지를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccf1c-149">Specifies a service bus queue message.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf1c-150">-ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="ccf1c-150">-ServiceBusNamespace</span></span>
<span data-ttu-id="ccf1c-151">Service bus 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccf1c-151">Specifies a service bus namespace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf1c-152">-ServiceBusQueueName</span><span class="sxs-lookup"><span data-stu-id="ccf1c-152">-ServiceBusQueueName</span></span>
<span data-ttu-id="ccf1c-153">서비스 버스 큐 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccf1c-153">Specifies a service bus queue name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf1c-154">-ServiceBusSasKeyName</span><span class="sxs-lookup"><span data-stu-id="ccf1c-154">-ServiceBusSasKeyName</span></span>
<span data-ttu-id="ccf1c-155">공유 액세스 서명 키 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccf1c-155">Specifies a shared access signature key name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf1c-156">-ServiceBusSasKeyValue</span><span class="sxs-lookup"><span data-stu-id="ccf1c-156">-ServiceBusSasKeyValue</span></span>
<span data-ttu-id="ccf1c-157">공유 액세스 서명 키 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccf1c-157">Specifies a shared access signature key value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf1c-158">-ServiceBusTransportType</span><span class="sxs-lookup"><span data-stu-id="ccf1c-158">-ServiceBusTransportType</span></span>
<span data-ttu-id="ccf1c-159">서비스 버스 전송 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccf1c-159">Specifies a service bus transport type.</span></span>
<span data-ttu-id="ccf1c-160">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="ccf1c-160">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ccf1c-161">NetMessaging</span><span class="sxs-lookup"><span data-stu-id="ccf1c-161">NetMessaging</span></span> 
- <span data-ttu-id="ccf1c-162">AMQP</span><span class="sxs-lookup"><span data-stu-id="ccf1c-162">AMQP</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: NetMessaging, AMQP

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf1c-163">-StartTime</span><span class="sxs-lookup"><span data-stu-id="ccf1c-163">-StartTime</span></span>
<span data-ttu-id="ccf1c-164">작업에 대 한 시작 시간을 **DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccf1c-164">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="ccf1c-165">-확인</span><span class="sxs-lookup"><span data-stu-id="ccf1c-165">-Confirm</span></span>
<span data-ttu-id="ccf1c-166">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccf1c-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccf1c-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccf1c-167">-WhatIf</span></span>
<span data-ttu-id="ccf1c-168">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ccf1c-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ccf1c-169">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ccf1c-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccf1c-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccf1c-170">-DefaultProfile</span></span>
<span data-ttu-id="ccf1c-171">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ccf1c-171">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccf1c-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccf1c-172">CommonParameters</span></span>
<span data-ttu-id="ccf1c-173">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ccf1c-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccf1c-174">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccf1c-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccf1c-175">입력</span><span class="sxs-lookup"><span data-stu-id="ccf1c-175">INPUTS</span></span>

## <span data-ttu-id="ccf1c-176">출력</span><span class="sxs-lookup"><span data-stu-id="ccf1c-176">OUTPUTS</span></span>

### <span data-ttu-id="ccf1c-177">PSSchedulerJobDefinition의 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="ccf1c-177">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="ccf1c-178">상속자</span><span class="sxs-lookup"><span data-stu-id="ccf1c-178">NOTES</span></span>

## <span data-ttu-id="ccf1c-179">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ccf1c-179">RELATED LINKS</span></span>

[<span data-ttu-id="ccf1c-180">새로운 AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="ccf1c-180">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="ccf1c-181">새로운 AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="ccf1c-181">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="ccf1c-182">새로운 AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="ccf1c-182">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="ccf1c-183">새로운 AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="ccf1c-183">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="ccf1c-184">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="ccf1c-184">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="ccf1c-185">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="ccf1c-185">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="ccf1c-186">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="ccf1c-186">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="ccf1c-187">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="ccf1c-187">Set-AzureRmSchedulerServiceBusTopicJob</span></span>](./Set-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="ccf1c-188">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="ccf1c-188">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


