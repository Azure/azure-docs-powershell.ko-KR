---
external help file: Microsoft.Azure.Commands.Scheduler.dll-Help.xml
Module Name: AzureRM.Scheduler
ms.assetid: F6B24F96-6016-4645-9F92-F584B73657D5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerServiceBusTopicJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Scheduler/Commands.Scheduler/help/Set-AzureRmSchedulerServiceBusTopicJob.md
ms.openlocfilehash: a12cf84d90ecbcc948ac13745b38438766582aaf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536188"
---
# <span data-ttu-id="11f28-101">Set-AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="11f28-101">Set-AzureRmSchedulerServiceBusTopicJob</span></span>

## <span data-ttu-id="11f28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11f28-102">SYNOPSIS</span></span>
<span data-ttu-id="11f28-103">Service bus 항목 작업을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11f28-103">Modifies a service bus topic job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="11f28-104">구문과</span><span class="sxs-lookup"><span data-stu-id="11f28-104">SYNTAX</span></span>

```
Set-AzureRmSchedulerServiceBusTopicJob -ResourceGroupName <String> -JobCollectionName <String>
 -JobName <String> -ServiceBusTopicPath <String> -ServiceBusNamespace <String>
 -ServiceBusTransportType <String> -ServiceBusMessage <String> -ServiceBusSasKeyName <String>
 -ServiceBusSasKeyValue <String> [-StartTime <DateTime>] [-Interval <Int32>] [-Frequency <String>]
 [-EndTime <DateTime>] [-ExecutionCount <Int32>] [-JobState <String>] [-ErrorActionType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11f28-105">설명은</span><span class="sxs-lookup"><span data-stu-id="11f28-105">DESCRIPTION</span></span>
<span data-ttu-id="11f28-106">**Set-AzureRmSchedulerServiceBusTopicJob** Cmdlet은 Azure Scheduler의 service bus 항목 작업을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11f28-106">The **Set-AzureRmSchedulerServiceBusTopicJob** cmdlet modifies a service bus topic job in Azure Scheduler.</span></span>

<span data-ttu-id="11f28-107">이 cmdlet은 *Erroractiontype* 매개 변수에 기반 하는 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="11f28-107">This cmdlet supports dynamic parameters based on the *ErrorActionType* parameter.</span></span>
<span data-ttu-id="11f28-108">동적 매개 변수는 다른 매개 변수 값에 따라 사용할 수 있게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="11f28-108">Dynamic parameters become available based on other parameter values.</span></span>

<span data-ttu-id="11f28-109">다른 매개 변수를 지정한 후 동적 매개 변수의 이름을 검색 하려면 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="11f28-109">To discover the names of dynamic parameters after you specify the other parameters, type a hyphen (-), and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="11f28-110">필수 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="11f28-110">If you omit a required parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="11f28-111">예제의</span><span class="sxs-lookup"><span data-stu-id="11f28-111">EXAMPLES</span></span>

## <span data-ttu-id="11f28-112">변수</span><span class="sxs-lookup"><span data-stu-id="11f28-112">PARAMETERS</span></span>

### <span data-ttu-id="11f28-113">-EndTime</span><span class="sxs-lookup"><span data-stu-id="11f28-113">-EndTime</span></span>
<span data-ttu-id="11f28-114">작업에 대 한 종료 시간을 **DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11f28-114">Specifies an end time, as a **DateTime** object, for the job.</span></span>
<span data-ttu-id="11f28-115">**DateTime** 개체를 가져오려면 Get-Date cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="11f28-115">To obtain a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="11f28-116">-ErrorActionType</span><span class="sxs-lookup"><span data-stu-id="11f28-116">-ErrorActionType</span></span>
<span data-ttu-id="11f28-117">작업에 대 한 오류 동작 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11f28-117">Specifies an error action setting for the job.</span></span>
<span data-ttu-id="11f28-118">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="11f28-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="11f28-119">Http</span><span class="sxs-lookup"><span data-stu-id="11f28-119">Http</span></span> 
- <span data-ttu-id="11f28-120">Https</span><span class="sxs-lookup"><span data-stu-id="11f28-120">Https</span></span> 
- <span data-ttu-id="11f28-121">StorageQueue</span><span class="sxs-lookup"><span data-stu-id="11f28-121">StorageQueue</span></span> 
- <span data-ttu-id="11f28-122">ServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="11f28-122">ServiceBusQueue</span></span> 
- <span data-ttu-id="11f28-123">Service<c13> Stopic</span><span class="sxs-lookup"><span data-stu-id="11f28-123">ServiceBusTopic</span></span>

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

### <span data-ttu-id="11f28-124">-ExecutionCount</span><span class="sxs-lookup"><span data-stu-id="11f28-124">-ExecutionCount</span></span>
<span data-ttu-id="11f28-125">작업이 실행 되는 횟수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11f28-125">Specifies how many times the job runs.</span></span>
<span data-ttu-id="11f28-126">기본적으로 작업이 무한정 되풀이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="11f28-126">By default, a job recurs indefinitely.</span></span>

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

### <span data-ttu-id="11f28-127">-빈도</span><span class="sxs-lookup"><span data-stu-id="11f28-127">-Frequency</span></span>
<span data-ttu-id="11f28-128">작업에 대 한 최대 빈도를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11f28-128">Specifies a maximum frequency for the job.</span></span>
<span data-ttu-id="11f28-129">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="11f28-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="11f28-130">길이의</span><span class="sxs-lookup"><span data-stu-id="11f28-130">Minute</span></span> 
- <span data-ttu-id="11f28-131">시간씩</span><span class="sxs-lookup"><span data-stu-id="11f28-131">Hour</span></span> 
- <span data-ttu-id="11f28-132">부활절</span><span class="sxs-lookup"><span data-stu-id="11f28-132">Day</span></span> 
- <span data-ttu-id="11f28-133">이번</span><span class="sxs-lookup"><span data-stu-id="11f28-133">Week</span></span> 
- <span data-ttu-id="11f28-134">달은</span><span class="sxs-lookup"><span data-stu-id="11f28-134">Month</span></span>

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

### <span data-ttu-id="11f28-135">-Interval</span><span class="sxs-lookup"><span data-stu-id="11f28-135">-Interval</span></span>
<span data-ttu-id="11f28-136">작업에 대 한 되풀이 간격을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11f28-136">Specifies an interval of recurrence for the job.</span></span>

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

### <span data-ttu-id="11f28-137">-JobCollectionName</span><span class="sxs-lookup"><span data-stu-id="11f28-137">-JobCollectionName</span></span>
<span data-ttu-id="11f28-138">작업이 속한 작업 컬렉션의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11f28-138">Specifies the name of the job collection to which the job belongs.</span></span>

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

### <span data-ttu-id="11f28-139">-JobName</span><span class="sxs-lookup"><span data-stu-id="11f28-139">-JobName</span></span>
<span data-ttu-id="11f28-140">이 cmdlet이 수정 하는 작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11f28-140">Specifies the name of the job that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="11f28-141">-JobState</span><span class="sxs-lookup"><span data-stu-id="11f28-141">-JobState</span></span>
<span data-ttu-id="11f28-142">작업의 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11f28-142">Specifies the state of the job.</span></span>
<span data-ttu-id="11f28-143">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="11f28-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="11f28-144">수</span><span class="sxs-lookup"><span data-stu-id="11f28-144">Enabled</span></span> 
- <span data-ttu-id="11f28-145">비활성화</span><span class="sxs-lookup"><span data-stu-id="11f28-145">Disabled</span></span>

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

### <span data-ttu-id="11f28-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11f28-146">-ResourceGroupName</span></span>
<span data-ttu-id="11f28-147">작업이 속한 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11f28-147">Specifies the resource group to which the job belongs.</span></span>

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

### <span data-ttu-id="11f28-148">-ServiceBusMessage</span><span class="sxs-lookup"><span data-stu-id="11f28-148">-ServiceBusMessage</span></span>
<span data-ttu-id="11f28-149">Service bus 항목 메시지를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11f28-149">Specifies a service bus topic message.</span></span>

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

### <span data-ttu-id="11f28-150">-ServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="11f28-150">-ServiceBusNamespace</span></span>
<span data-ttu-id="11f28-151">Service bus 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11f28-151">Specifies a service bus namespace.</span></span>

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

### <span data-ttu-id="11f28-152">-ServiceBusSasKeyName</span><span class="sxs-lookup"><span data-stu-id="11f28-152">-ServiceBusSasKeyName</span></span>
<span data-ttu-id="11f28-153">공유 액세스 서명 키 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11f28-153">Specifies a shared access signature key name.</span></span>

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

### <span data-ttu-id="11f28-154">-ServiceBusSasKeyValue</span><span class="sxs-lookup"><span data-stu-id="11f28-154">-ServiceBusSasKeyValue</span></span>
<span data-ttu-id="11f28-155">공유 액세스 서명 키 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11f28-155">Specifies a shared access signature key value.</span></span>

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

### <span data-ttu-id="11f28-156">-Service<c13> Stopicpath</span><span class="sxs-lookup"><span data-stu-id="11f28-156">-ServiceBusTopicPath</span></span>
<span data-ttu-id="11f28-157">Service bus 항목 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11f28-157">Specifies a service bus topic path.</span></span>

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

### <span data-ttu-id="11f28-158">-ServiceBusTransportType</span><span class="sxs-lookup"><span data-stu-id="11f28-158">-ServiceBusTransportType</span></span>
<span data-ttu-id="11f28-159">서비스 버스 전송 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11f28-159">Specifies a service bus transport type.</span></span>
<span data-ttu-id="11f28-160">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="11f28-160">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="11f28-161">NetMessaging</span><span class="sxs-lookup"><span data-stu-id="11f28-161">NetMessaging</span></span>
- <span data-ttu-id="11f28-162">AMQP</span><span class="sxs-lookup"><span data-stu-id="11f28-162">AMQP</span></span>

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

### <span data-ttu-id="11f28-163">-StartTime</span><span class="sxs-lookup"><span data-stu-id="11f28-163">-StartTime</span></span>
<span data-ttu-id="11f28-164">작업에 대 한 시작 시간을 **DateTime** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11f28-164">Specifies the start time, as a **DateTime** object, for the job.</span></span>

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

### <span data-ttu-id="11f28-165">-확인</span><span class="sxs-lookup"><span data-stu-id="11f28-165">-Confirm</span></span>
<span data-ttu-id="11f28-166">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="11f28-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11f28-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11f28-167">-WhatIf</span></span>
<span data-ttu-id="11f28-168">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="11f28-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11f28-169">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="11f28-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11f28-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11f28-170">-DefaultProfile</span></span>
<span data-ttu-id="11f28-171">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="11f28-171">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11f28-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11f28-172">CommonParameters</span></span>
<span data-ttu-id="11f28-173">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="11f28-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11f28-174">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11f28-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11f28-175">입력</span><span class="sxs-lookup"><span data-stu-id="11f28-175">INPUTS</span></span>

## <span data-ttu-id="11f28-176">출력</span><span class="sxs-lookup"><span data-stu-id="11f28-176">OUTPUTS</span></span>

### <span data-ttu-id="11f28-177">PSSchedulerJobDefinition의 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="11f28-177">Microsoft.Azure.Commands.Scheduler.Models.PSSchedulerJobDefinition</span></span>

## <span data-ttu-id="11f28-178">상속자</span><span class="sxs-lookup"><span data-stu-id="11f28-178">NOTES</span></span>

## <span data-ttu-id="11f28-179">관련 링크</span><span class="sxs-lookup"><span data-stu-id="11f28-179">RELATED LINKS</span></span>

[<span data-ttu-id="11f28-180">새로운 AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="11f28-180">New-AzureRmSchedulerHttpJob</span></span>](./New-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="11f28-181">새로운 AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="11f28-181">New-AzureRmSchedulerJobCollection</span></span>](./New-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="11f28-182">새로운 AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="11f28-182">New-AzureRmSchedulerServiceBusQueueJob</span></span>](./New-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="11f28-183">새로운 AzureRmSchedulerServiceBusTopicJob</span><span class="sxs-lookup"><span data-stu-id="11f28-183">New-AzureRmSchedulerServiceBusTopicJob</span></span>](./New-AzureRmSchedulerServiceBusTopicJob.md)

[<span data-ttu-id="11f28-184">새로운 AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="11f28-184">New-AzureRmSchedulerStorageQueueJob</span></span>](./New-AzureRmSchedulerStorageQueueJob.md)

[<span data-ttu-id="11f28-185">Set-AzureRmSchedulerHttpJob</span><span class="sxs-lookup"><span data-stu-id="11f28-185">Set-AzureRmSchedulerHttpJob</span></span>](./Set-AzureRmSchedulerHttpJob.md)

[<span data-ttu-id="11f28-186">Set-AzureRmSchedulerJobCollection</span><span class="sxs-lookup"><span data-stu-id="11f28-186">Set-AzureRmSchedulerJobCollection</span></span>](./Set-AzureRmSchedulerJobCollection.md)

[<span data-ttu-id="11f28-187">Set-AzureRmSchedulerServiceBusQueueJob</span><span class="sxs-lookup"><span data-stu-id="11f28-187">Set-AzureRmSchedulerServiceBusQueueJob</span></span>](./Set-AzureRmSchedulerServiceBusQueueJob.md)

[<span data-ttu-id="11f28-188">Set-AzureRmSchedulerStorageQueueJob</span><span class="sxs-lookup"><span data-stu-id="11f28-188">Set-AzureRmSchedulerStorageQueueJob</span></span>](./Set-AzureRmSchedulerStorageQueueJob.md)


