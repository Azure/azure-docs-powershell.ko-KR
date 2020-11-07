---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusQueue.md
ms.openlocfilehash: b9ad7c729395115845349c1e39f8d90666a4fcb8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699182"
---
# <span data-ttu-id="bf336-101">New-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="bf336-101">New-AzServiceBusQueue</span></span>

## <span data-ttu-id="bf336-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf336-102">SYNOPSIS</span></span>
<span data-ttu-id="bf336-103">지정 된 Service Bus 네임 스페이스에 Service Bus 큐를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bf336-103">Creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="bf336-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bf336-104">SYNTAX</span></span>

```
New-AzServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-EnablePartitioning <Boolean>] [-LockDuration <String>] [-AutoDeleteOnIdle <String>]
 [-DefaultMessageTimeToLive <String>] [-DuplicateDetectionHistoryTimeWindow <String>]
 [-DeadLetteringOnMessageExpiration <Boolean>] [-EnableBatchedOperations] [-EnableExpress <Boolean>]
 [-MaxDeliveryCount <Int32>] [-MaxSizeInMegabytes <Int64>] [-MessageCount <Int64>]
 [-RequiresDuplicateDetection <Boolean>] [-RequiresSession <Boolean>] [-SizeInBytes <Int64>]
 [-ForwardTo <String>] [-ForwardDeadLetteredMessagesTo <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf336-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bf336-105">DESCRIPTION</span></span>
<span data-ttu-id="bf336-106">**AzServiceBusQueue** cmdlet은 지정 된 service bus 네임 스페이스에 Service bus 큐를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bf336-106">The **New-AzServiceBusQueue** cmdlet creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="bf336-107">예제의</span><span class="sxs-lookup"><span data-stu-id="bf336-107">EXAMPLES</span></span>

### <span data-ttu-id="bf336-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="bf336-108">Example 1</span></span>
```
PS C:\> New-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1 -EnablePartitioning $True

Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_example1
Name                                : SB-Queue_example1
LockDuration                        : PT1M
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 10/11/2018 12:37:11 AM
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
DeadLetteringOnMessageExpiration    : False
EnableExpress                       : False
EnablePartitioning                  : False
MaxDeliveryCount                    : 10
MaxSizeInMegabytes                  : 81920
MessageCount                        : 0
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
RequiresDuplicateDetection          : False
RequiresSession                     : False
SizeInBytes                         : 0
Status                              : Active
UpdatedAt                           : 10/11/2018 12:37:12 AM
ForwardTo                           :
ForwardDeadLetteredMessagesTo       :
EnableBatchedOperations             : False
```

<span data-ttu-id="bf336-109">`SB-Queue_example1`지정 된 Service bus 네임 스페이스에 새 Service bus 큐를 만듭니다 `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="bf336-109">Creates a new Service Bus queue `SB-Queue_example1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="bf336-110">변수</span><span class="sxs-lookup"><span data-stu-id="bf336-110">PARAMETERS</span></span>

### <span data-ttu-id="bf336-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="bf336-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="bf336-112">큐가 자동으로 삭제 되는 기준으로 사용할 [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) 유휴 간격을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf336-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the queue is automatically deleted.</span></span> <span data-ttu-id="bf336-113">최소 기간은 5 분입니다.</span><span class="sxs-lookup"><span data-stu-id="bf336-113">The minimum duration is 5 minutes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf336-114">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="bf336-114">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="bf336-115">메시지 만료 시 배달 못 한 문자</span><span class="sxs-lookup"><span data-stu-id="bf336-115">Dead Lettering On Message Expiration</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf336-116">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="bf336-116">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="bf336-117">Timespan to live 값입니다.</span><span class="sxs-lookup"><span data-stu-id="bf336-117">Timespan to live value.</span></span>
<span data-ttu-id="bf336-118">메시지가 서비스 버스에 전송 될 때부터 메시지가 만료 되는 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="bf336-118">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="bf336-119">TimeToLive가 메시지 자체에 설정 되지 않았을 때 사용 되는 기본값입니다.</span><span class="sxs-lookup"><span data-stu-id="bf336-119">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="bf336-120">Standard = Timespan. 최대 및 기본 = 14 dyas</span><span class="sxs-lookup"><span data-stu-id="bf336-120">For Standard = Timespan.Max and Basic = 14 dyas</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf336-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf336-121">-DefaultProfile</span></span>
<span data-ttu-id="bf336-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bf336-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf336-123">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="bf336-123">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="bf336-124">중복 검색 기록의 기간을 정의 하는 [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) (중복 검색 기록 시간) 창을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf336-124">Specifies the duplicate detection history time window, a [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) valuethat defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="bf336-125">기본값은 10 분입니다.</span><span class="sxs-lookup"><span data-stu-id="bf336-125">The default value is 10 minutes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf336-126">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="bf336-126">-EnableBatchedOperations</span></span>
<span data-ttu-id="bf336-127">일괄 처리 된 작업 사용-서버측 일괄 처리 된 작업을 사용할지 여부를 나타내는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="bf336-127">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

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

### <span data-ttu-id="bf336-128">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="bf336-128">-EnableExpress</span></span>
<span data-ttu-id="bf336-129">EnableExpress-Express 엔터티를 사용할 수 있는지 여부를 나타내는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="bf336-129">EnableExpress - a value that indicates whether Express Entities are enabled.</span></span>
<span data-ttu-id="bf336-130">Express 큐는 영구 저장소에 쓰기 전에 메모리의 메시지를 일시적으로 보관 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf336-130">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf336-131">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="bf336-131">-EnablePartitioning</span></span>
<span data-ttu-id="bf336-132">EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="bf336-132">EnablePartitioning</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf336-133">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="bf336-133">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="bf336-134">배달 못한 편지 메시지를 전달 하기 위한 큐/항목 이름</span><span class="sxs-lookup"><span data-stu-id="bf336-134">Queue/Topic name to forward the Dead Letter message</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf336-135">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="bf336-135">-ForwardTo</span></span>
<span data-ttu-id="bf336-136">메시지를 전달 하기 위한 큐/항목 이름</span><span class="sxs-lookup"><span data-stu-id="bf336-136">Queue/Topic name to forward the messages</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf336-137">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="bf336-137">-LockDuration</span></span>
<span data-ttu-id="bf336-138">잠금 기간</span><span class="sxs-lookup"><span data-stu-id="bf336-138">Lock Duration</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf336-139">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="bf336-139">-MaxDeliveryCount</span></span>
<span data-ttu-id="bf336-140">MaxDeliveryCount-최대 배달 수입니다.</span><span class="sxs-lookup"><span data-stu-id="bf336-140">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="bf336-141">배달 횟수가 지난 후에는 메시지가 자동으로 deadlettered 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bf336-141">A message is automatically deadlettered after this number of deliveries.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf336-142">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="bf336-142">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="bf336-143">MaxSizeInMegabytes-대기열의 최대 크기 (mb)로, 대기열에 할당 된 메모리 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="bf336-143">MaxSizeInMegabytes - the maximum size of the queue in megabytes, which is the size of memory allocated for the queue.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf336-144">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="bf336-144">-MessageCount</span></span>
<span data-ttu-id="bf336-145">MessageCount-대기열에 있는 메시지 수</span><span class="sxs-lookup"><span data-stu-id="bf336-145">MessageCount - the number of messages in the queue</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf336-146">-이름</span><span class="sxs-lookup"><span data-stu-id="bf336-146">-Name</span></span>
<span data-ttu-id="bf336-147">큐 이름</span><span class="sxs-lookup"><span data-stu-id="bf336-147">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf336-148">-Namespace</span><span class="sxs-lookup"><span data-stu-id="bf336-148">-Namespace</span></span>
<span data-ttu-id="bf336-149">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="bf336-149">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf336-150">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="bf336-150">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="bf336-151">RequiresDuplicateDetection-대기열이 세션의 개념을 지원 하는지 여부를 나타내는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="bf336-151">RequiresDuplicateDetection - a value that indicates whether the queue supports the concept of session</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf336-152">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="bf336-152">-RequiresSession</span></span>
<span data-ttu-id="bf336-153">RequiresSession-이 대기열이 중복 검색을 요구 하는지 여부를 나타내는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="bf336-153">RequiresSession - the value indicating if this queue requires duplicate detection</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf336-154">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf336-154">-ResourceGroupName</span></span>
<span data-ttu-id="bf336-155">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bf336-155">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf336-156">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="bf336-156">-SizeInBytes</span></span>
<span data-ttu-id="bf336-157">SizeInBytes-대기열의 크기 (바이트)입니다.</span><span class="sxs-lookup"><span data-stu-id="bf336-157">SizeInBytes - the size of the queue in bytes</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf336-158">-확인</span><span class="sxs-lookup"><span data-stu-id="bf336-158">-Confirm</span></span>
<span data-ttu-id="bf336-159">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf336-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf336-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf336-160">-WhatIf</span></span>
<span data-ttu-id="bf336-161">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="bf336-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf336-162">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bf336-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf336-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf336-163">CommonParameters</span></span>
<span data-ttu-id="bf336-164">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf336-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf336-165">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf336-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf336-166">입력</span><span class="sxs-lookup"><span data-stu-id="bf336-166">INPUTS</span></span>

### <span data-ttu-id="bf336-167">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="bf336-167">System.String</span></span>

### <span data-ttu-id="bf336-168">시스템 Null 허용 ' 1 [[CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="bf336-168">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="bf336-169">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e])</span><span class="sxs-lookup"><span data-stu-id="bf336-169">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="bf336-170">시스템 Null 허용 ' 1 [[System.webserver, System.webserver, CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="bf336-170">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="bf336-171">출력</span><span class="sxs-lookup"><span data-stu-id="bf336-171">OUTPUTS</span></span>

### <span data-ttu-id="bf336-172">ServiceBus. a m/.</span><span class="sxs-lookup"><span data-stu-id="bf336-172">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="bf336-173">상속자</span><span class="sxs-lookup"><span data-stu-id="bf336-173">NOTES</span></span>

## <span data-ttu-id="bf336-174">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bf336-174">RELATED LINKS</span></span>