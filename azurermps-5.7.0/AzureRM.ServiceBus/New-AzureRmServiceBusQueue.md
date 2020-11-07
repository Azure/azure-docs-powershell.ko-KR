---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueue.md
ms.openlocfilehash: 8e1b1cd39e30bcbe2ccc9f46b5ab39511e4de58f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703218"
---
# <span data-ttu-id="ece6c-101">New-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="ece6c-101">New-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="ece6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ece6c-102">SYNOPSIS</span></span>
<span data-ttu-id="ece6c-103">지정 된 Service Bus 네임 스페이스에 Service Bus 큐를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ece6c-103">Creates a Service Bus queue in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ece6c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ece6c-104">SYNTAX</span></span>

```
New-AzureRmServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-EnablePartitioning <Boolean>] [-LockDuration <String>] [-AutoDeleteOnIdle <String>]
 [-DefaultMessageTimeToLive <String>] [-DuplicateDetectionHistoryTimeWindow <String>]
 [-DeadLetteringOnMessageExpiration <Boolean>] [-EnableBatchedOperations] [-EnableExpress <Boolean>]
 [-MaxDeliveryCount <Int32>] [-MaxSizeInMegabytes <Int64>] [-MessageCount <Int64>]
 [-RequiresDuplicateDetection <Boolean>] [-RequiresSession <Boolean>] [-SizeInBytes <Int64>]
 [-ForwardTo <String>] [-ForwardDeadLetteredMessagesTo <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ece6c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ece6c-105">DESCRIPTION</span></span>
<span data-ttu-id="ece6c-106">**AzureRmServiceBusQueue** cmdlet은 지정 된 service bus 네임 스페이스에 Service bus 큐를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ece6c-106">The **New-AzureRmServiceBusQueue** cmdlet creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="ece6c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ece6c-107">EXAMPLES</span></span>

### <span data-ttu-id="ece6c-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ece6c-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -EnablePartitioning $True

Name                                : SB-Queue_exampl1
LockDuration                        : 
AccessedAt                          : 
AutoDeleteOnIdle                    : 10675199.02:48:05.4775807
CreatedAt                           : 1/20/2017 2:51:36 AM
DefaultMessageTimeToLive            : 10675199.02:48:05.4775807
DuplicateDetectionHistoryTimeWindow : 
DeadLetteringOnMessageExpiration    : False
EnableExpress                       : False
EnablePartitioning                  : True
MaxDeliveryCount                    : 
MaxSizeInMegabytes                  : 16384
MessageCount                        : 
CountDetails                        : 
RequiresDuplicateDetection          : False
RequiresSession                     : False
SizeInBytes                         : 
Status                              : Active
UpdatedAt                           : 1/20/2017 2:51:37 AM
```
<span data-ttu-id="ece6c-109">`SB-Queue_exampl1`지정 된 Service bus 네임 스페이스에 새 Service bus 큐를 만듭니다 `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="ece6c-109">Creates a new Service Bus queue `SB-Queue_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="ece6c-110">변수</span><span class="sxs-lookup"><span data-stu-id="ece6c-110">PARAMETERS</span></span>

### <span data-ttu-id="ece6c-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="ece6c-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="ece6c-112">큐가 자동으로 삭제 되는 기준으로 사용할 [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) 유휴 간격을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ece6c-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the queue is automatically deleted.</span></span> <span data-ttu-id="ece6c-113">최소 기간은 5 분입니다.</span><span class="sxs-lookup"><span data-stu-id="ece6c-113">The minimum duration is 5 minutes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ece6c-114">-확인</span><span class="sxs-lookup"><span data-stu-id="ece6c-114">-Confirm</span></span>
<span data-ttu-id="ece6c-115">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ece6c-115">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ece6c-116">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="ece6c-116">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="ece6c-117">메시지 만료 시 배달 못 한 문자</span><span class="sxs-lookup"><span data-stu-id="ece6c-117">Dead Lettering On Message Expiration</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ece6c-118">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="ece6c-118">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="ece6c-119">Timespan to live 값입니다.</span><span class="sxs-lookup"><span data-stu-id="ece6c-119">Timespan to live value.</span></span>
<span data-ttu-id="ece6c-120">메시지가 서비스 버스에 전송 될 때부터 메시지가 만료 되는 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="ece6c-120">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="ece6c-121">TimeToLive가 메시지 자체에 설정 되지 않았을 때 사용 되는 기본값입니다.</span><span class="sxs-lookup"><span data-stu-id="ece6c-121">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="ece6c-122">Standard = Timespan. 최대 및 기본 = 14 dyas</span><span class="sxs-lookup"><span data-stu-id="ece6c-122">For Standard = Timespan.Max and Basic = 14 dyas</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ece6c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ece6c-123">-DefaultProfile</span></span>
<span data-ttu-id="ece6c-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ece6c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ece6c-125">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="ece6c-125">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="ece6c-126">중복 검색 기록의 기간을 정의 하는 [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) (중복 검색 기록 시간) 창을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ece6c-126">Specifies the duplicate detection history time window, a [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) valuethat defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="ece6c-127">기본값은 10 분입니다.</span><span class="sxs-lookup"><span data-stu-id="ece6c-127">The default value is 10 minutes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ece6c-128">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="ece6c-128">-EnableBatchedOperations</span></span>
<span data-ttu-id="ece6c-129">일괄 처리 된 작업 사용-서버측 일괄 처리 된 작업을 사용할지 여부를 나타내는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="ece6c-129">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ece6c-130">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="ece6c-130">-EnableExpress</span></span>
<span data-ttu-id="ece6c-131">EnableExpress-Express 엔터티를 사용할 수 있는지 여부를 나타내는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="ece6c-131">EnableExpress - a value that indicates whether Express Entities are enabled.</span></span>
<span data-ttu-id="ece6c-132">Express 큐는 영구 저장소에 쓰기 전에 메모리의 메시지를 일시적으로 보관 합니다.</span><span class="sxs-lookup"><span data-stu-id="ece6c-132">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ece6c-133">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="ece6c-133">-EnablePartitioning</span></span>
<span data-ttu-id="ece6c-134">EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="ece6c-134">EnablePartitioning</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ece6c-135">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="ece6c-135">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="ece6c-136">배달 못한 편지 메시지를 전달 하기 위한 큐/항목 이름</span><span class="sxs-lookup"><span data-stu-id="ece6c-136">Queue/Topic name to forward the Dead Letter message</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ece6c-137">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="ece6c-137">-ForwardTo</span></span>
<span data-ttu-id="ece6c-138">메시지를 전달 하기 위한 큐/항목 이름</span><span class="sxs-lookup"><span data-stu-id="ece6c-138">Queue/Topic name to forward the messages</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ece6c-139">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="ece6c-139">-LockDuration</span></span>
<span data-ttu-id="ece6c-140">잠금 기간</span><span class="sxs-lookup"><span data-stu-id="ece6c-140">Lock Duration</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ece6c-141">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="ece6c-141">-MaxDeliveryCount</span></span>
<span data-ttu-id="ece6c-142">MaxDeliveryCount-최대 배달 수입니다.</span><span class="sxs-lookup"><span data-stu-id="ece6c-142">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="ece6c-143">배달 횟수가 지난 후에는 메시지가 자동으로 deadlettered 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ece6c-143">A message is automatically deadlettered after this number of deliveries.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ece6c-144">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="ece6c-144">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="ece6c-145">MaxSizeInMegabytes-대기열의 최대 크기 (mb)로, 대기열에 할당 된 메모리 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="ece6c-145">MaxSizeInMegabytes - the maximum size of the queue in megabytes, which is the size of memory allocated for the queue.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ece6c-146">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="ece6c-146">-MessageCount</span></span>
<span data-ttu-id="ece6c-147">MessageCount-대기열에 있는 메시지 수</span><span class="sxs-lookup"><span data-stu-id="ece6c-147">MessageCount - the number of messages in the queue</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ece6c-148">-이름</span><span class="sxs-lookup"><span data-stu-id="ece6c-148">-Name</span></span>
<span data-ttu-id="ece6c-149">큐 이름</span><span class="sxs-lookup"><span data-stu-id="ece6c-149">Queue Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ece6c-150">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ece6c-150">-Namespace</span></span>
<span data-ttu-id="ece6c-151">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="ece6c-151">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ece6c-152">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="ece6c-152">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="ece6c-153">RequiresDuplicateDetection-대기열이 세션의 개념을 지원 하는지 여부를 나타내는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="ece6c-153">RequiresDuplicateDetection - a value that indicates whether the queue supports the concept of session</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ece6c-154">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="ece6c-154">-RequiresSession</span></span>
<span data-ttu-id="ece6c-155">RequiresSession-이 대기열이 중복 검색을 요구 하는지 여부를 나타내는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="ece6c-155">RequiresSession - the value indicating if this queue requires duplicate detection</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:
Accepted values: TRUE, FALSE

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ece6c-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ece6c-156">-ResourceGroupName</span></span>
<span data-ttu-id="ece6c-157">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ece6c-157">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ece6c-158">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="ece6c-158">-SizeInBytes</span></span>
<span data-ttu-id="ece6c-159">SizeInBytes-대기열의 크기 (바이트)입니다.</span><span class="sxs-lookup"><span data-stu-id="ece6c-159">SizeInBytes - the size of the queue in bytes</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ece6c-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ece6c-160">-WhatIf</span></span>
<span data-ttu-id="ece6c-161">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ece6c-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ece6c-162">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ece6c-162">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ece6c-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ece6c-163">CommonParameters</span></span>
<span data-ttu-id="ece6c-164">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ece6c-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ece6c-165">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ece6c-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ece6c-166">입력</span><span class="sxs-lookup"><span data-stu-id="ece6c-166">INPUTS</span></span>

### <span data-ttu-id="ece6c-167">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ece6c-167">-ResourceGroup</span></span>
 <span data-ttu-id="ece6c-168">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ece6c-168">System.String</span></span>

### <span data-ttu-id="ece6c-169">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="ece6c-169">-NamespaceName</span></span>
 <span data-ttu-id="ece6c-170">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ece6c-170">System.String</span></span>

### <span data-ttu-id="ece6c-171">-QueueName</span><span class="sxs-lookup"><span data-stu-id="ece6c-171">-QueueName</span></span>
 <span data-ttu-id="ece6c-172">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ece6c-172">System.String</span></span>

### <span data-ttu-id="ece6c-173">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="ece6c-173">-EnablePartitioning</span></span>
 <span data-ttu-id="ece6c-174">시스템 부울 인가요?</span><span class="sxs-lookup"><span data-stu-id="ece6c-174">System.Boolean?</span></span>


## <span data-ttu-id="ece6c-175">출력</span><span class="sxs-lookup"><span data-stu-id="ece6c-175">OUTPUTS</span></span>

### <span data-ttu-id="ece6c-176">ServiceBus. a m/.</span><span class="sxs-lookup"><span data-stu-id="ece6c-176">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>


## <span data-ttu-id="ece6c-177">상속자</span><span class="sxs-lookup"><span data-stu-id="ece6c-177">NOTES</span></span>

## <span data-ttu-id="ece6c-178">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ece6c-178">RELATED LINKS</span></span>
