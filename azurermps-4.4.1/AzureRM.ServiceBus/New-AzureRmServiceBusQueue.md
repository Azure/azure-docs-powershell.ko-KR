---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusQueue.md
ms.openlocfilehash: 4538bb39c085a2e7152a146d5e93e08a0c09f5de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527284"
---
# <span data-ttu-id="6eba9-101">New-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="6eba9-101">New-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="6eba9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6eba9-102">SYNOPSIS</span></span>
<span data-ttu-id="6eba9-103">지정 된 Service Bus 네임 스페이스에 Service Bus 큐를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6eba9-103">Creates a Service Bus queue in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6eba9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6eba9-104">SYNTAX</span></span>

```
New-AzureRmServiceBusQueue -ResourceGroupName <String> -Namespace <String> -Name <String>
 -EnablePartitioning <Boolean> [-LockDuration <String>] [-AutoDeleteOnIdle <String>]
 [-DefaultMessageTimeToLive <String>] [-DuplicateDetectionHistoryTimeWindow <String>]
 [-EnableBatchedOperations <Boolean>] [-DeadLetteringOnMessageExpiration <Boolean>] [-EnableExpress <Boolean>]
 [-IsAnonymousAccessible <Boolean>] [-MaxDeliveryCount <Int32>] [-MaxSizeInMegabytes <Int64>]
 [-MessageCount <Int64>] [-RequiresDuplicateDetection <Boolean>] [-RequiresSession <Boolean>]
 [-SizeInBytes <Int64>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6eba9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6eba9-105">DESCRIPTION</span></span>
<span data-ttu-id="6eba9-106">**AzureRmServiceBusQueue** cmdlet은 지정 된 service bus 네임 스페이스에 Service bus 큐를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6eba9-106">The **New-AzureRmServiceBusQueue** cmdlet creates a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="6eba9-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6eba9-107">EXAMPLES</span></span>

### <span data-ttu-id="6eba9-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="6eba9-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -EnablePartitioning $True
```

<span data-ttu-id="6eba9-109">`SB-Queue_exampl1`지정 된 Service bus 네임 스페이스에 새 Service bus 큐를 만듭니다 `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="6eba9-109">Creates a new Service Bus queue `SB-Queue_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="6eba9-110">변수</span><span class="sxs-lookup"><span data-stu-id="6eba9-110">PARAMETERS</span></span>

### <span data-ttu-id="6eba9-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="6eba9-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="6eba9-112">큐가 자동으로 삭제 되는 기준으로 사용할 [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) 유휴 간격을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eba9-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the queue is automatically deleted.</span></span> <span data-ttu-id="6eba9-113">최소 기간은 5 분입니다.</span><span class="sxs-lookup"><span data-stu-id="6eba9-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="6eba9-114">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="6eba9-114">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="6eba9-115">메시지가 만료 되는 deadlettered 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eba9-115">Specifies whether messages are deadlettered on expiration.</span></span>

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

### <span data-ttu-id="6eba9-116">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="6eba9-116">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="6eba9-117">기본 메시지 TTL (time to live)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eba9-117">Specifies the default message time-to-live (TTL).</span></span>

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

### <span data-ttu-id="6eba9-118">-DuplicateDetectionHistoryTimeWindow</span><span class="sxs-lookup"><span data-stu-id="6eba9-118">-DuplicateDetectionHistoryTimeWindow</span></span>
<span data-ttu-id="6eba9-119">중복 검색 기록의 기간을 정의 하는 [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) (중복 검색 기록 시간) 창을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eba9-119">Specifies the duplicate detection history time window, a [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) valuethat defines the duration of the duplicate detection history.</span></span> <span data-ttu-id="6eba9-120">기본값은 10 분입니다.</span><span class="sxs-lookup"><span data-stu-id="6eba9-120">The default value is 10 minutes.</span></span>

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

### <span data-ttu-id="6eba9-121">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="6eba9-121">-EnableBatchedOperations</span></span>
<span data-ttu-id="6eba9-122">서버 쪽 일괄 처리 된 작업을 사용할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eba9-122">Specifies whether server-side batched operations are enabled.</span></span>

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

### <span data-ttu-id="6eba9-123">-EnableExpress</span><span class="sxs-lookup"><span data-stu-id="6eba9-123">-EnableExpress</span></span>
<span data-ttu-id="6eba9-124">Express 엔터티를 사용할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eba9-124">Specifies whether Express Entities are enabled.</span></span> <span data-ttu-id="6eba9-125">Express 큐는 영구 저장소에 쓰기 전에 메모리의 메시지를 일시적으로 보관 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eba9-125">An express queue holds a message in memory temporarily before writing it to persistent storage.</span></span>

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

### <span data-ttu-id="6eba9-126">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="6eba9-126">-EnablePartitioning</span></span>
<span data-ttu-id="6eba9-127">EnablePartitioning을 사용할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eba9-127">Specifies whether EnablePartitioning is enabled.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 
Accepted values: TRUE, FALSE

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6eba9-128">-IsAnonymousAccessible</span><span class="sxs-lookup"><span data-stu-id="6eba9-128">-IsAnonymousAccessible</span></span>
<span data-ttu-id="6eba9-129">메시지에 익명으로 액세스할 수 있는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eba9-129">Specifies whether the message is anonymously accessible.</span></span>

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

### <span data-ttu-id="6eba9-130">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="6eba9-130">-LockDuration</span></span>
<span data-ttu-id="6eba9-131">잠금 기간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eba9-131">Specifies the lock duration.</span></span>

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

### <span data-ttu-id="6eba9-132">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="6eba9-132">-MaxDeliveryCount</span></span>
<span data-ttu-id="6eba9-133">최대 배달 횟수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eba9-133">Specifies the maximum delivery count.</span></span> <span data-ttu-id="6eba9-134">배달 횟수가 지난 후에는 메시지가 자동으로 deadlettered 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6eba9-134">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="6eba9-135">-MaxSizeInMegabytes</span><span class="sxs-lookup"><span data-stu-id="6eba9-135">-MaxSizeInMegabytes</span></span>
<span data-ttu-id="6eba9-136">큐의 최대 크기를 메가바이트 단위 (mb)로 지정 합니다 (대기열에 할당 된 메모리 크기).</span><span class="sxs-lookup"><span data-stu-id="6eba9-136">Specifies the maximum size of the queue in megabytes, which is the size of memory allocated for the queue.</span></span>

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

### <span data-ttu-id="6eba9-137">-MessageCount</span><span class="sxs-lookup"><span data-stu-id="6eba9-137">-MessageCount</span></span>
<span data-ttu-id="6eba9-138">큐의 메시지 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eba9-138">Specifies the number of messages in the queue.</span></span>

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

### <span data-ttu-id="6eba9-139">-RequiresDuplicateDetection</span><span class="sxs-lookup"><span data-stu-id="6eba9-139">-RequiresDuplicateDetection</span></span>
<span data-ttu-id="6eba9-140">큐에 중복 검색이 필요한 지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eba9-140">Specifies whether the queue requires duplicate detection.</span></span>

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

### <span data-ttu-id="6eba9-141">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="6eba9-141">-RequiresSession</span></span>
<span data-ttu-id="6eba9-142">이 대기열이 세션을 지원 하는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eba9-142">Specifies whether this queue supports sessions.</span></span>

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

### <span data-ttu-id="6eba9-143">-SizeInBytes</span><span class="sxs-lookup"><span data-stu-id="6eba9-143">-SizeInBytes</span></span>
<span data-ttu-id="6eba9-144">대기열의 크기 (바이트)입니다.</span><span class="sxs-lookup"><span data-stu-id="6eba9-144">The size of the queue in bytes.</span></span>

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

### <span data-ttu-id="6eba9-145">-확인</span><span class="sxs-lookup"><span data-stu-id="6eba9-145">-Confirm</span></span>
<span data-ttu-id="6eba9-146">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eba9-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6eba9-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6eba9-147">-WhatIf</span></span>
<span data-ttu-id="6eba9-148">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6eba9-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6eba9-149">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6eba9-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6eba9-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6eba9-150">-DefaultProfile</span></span>
<span data-ttu-id="6eba9-151">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6eba9-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6eba9-152">-이름</span><span class="sxs-lookup"><span data-stu-id="6eba9-152">-Name</span></span>
<span data-ttu-id="6eba9-153">큐 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6eba9-153">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6eba9-154">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6eba9-154">-Namespace</span></span>
<span data-ttu-id="6eba9-155">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6eba9-155">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6eba9-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6eba9-156">-ResourceGroupName</span></span>
<span data-ttu-id="6eba9-157">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6eba9-157">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6eba9-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6eba9-158">CommonParameters</span></span>
<span data-ttu-id="6eba9-159">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6eba9-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6eba9-160">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6eba9-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6eba9-161">입력</span><span class="sxs-lookup"><span data-stu-id="6eba9-161">INPUTS</span></span>

### <span data-ttu-id="6eba9-162">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6eba9-162">-ResourceGroup</span></span>
 <span data-ttu-id="6eba9-163">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6eba9-163">System.String</span></span>

### <span data-ttu-id="6eba9-164">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="6eba9-164">-NamespaceName</span></span>
 <span data-ttu-id="6eba9-165">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6eba9-165">System.String</span></span>

### <span data-ttu-id="6eba9-166">-QueueName</span><span class="sxs-lookup"><span data-stu-id="6eba9-166">-QueueName</span></span>
 <span data-ttu-id="6eba9-167">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6eba9-167">System.String</span></span>

### <span data-ttu-id="6eba9-168">-EnablePartitioning</span><span class="sxs-lookup"><span data-stu-id="6eba9-168">-EnablePartitioning</span></span>
 <span data-ttu-id="6eba9-169">시스템 부울 인가요?</span><span class="sxs-lookup"><span data-stu-id="6eba9-169">System.Boolean?</span></span>

## <span data-ttu-id="6eba9-170">출력</span><span class="sxs-lookup"><span data-stu-id="6eba9-170">OUTPUTS</span></span>

### <span data-ttu-id="6eba9-171">ServiceBus 특성이 있는 경우.</span><span class="sxs-lookup"><span data-stu-id="6eba9-171">Microsoft.Azure.Commands.ServiceBus.Models.QueueAttributes</span></span>
<span data-ttu-id="6eba9-172">이름: SB-Queue_exampl1 위치: 서쪽 미국 LockDuration: AccessedAt: AutoDeleteOnIdle: 10675199.02:48:05.4775807 EntityAvailabilityStatus: CreatedAt: 1/20/2017 2:51:36 AM DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow: EnableBatchedOperations: True DeadLetteringOnMessageExpiration: False EnableExpress: False Enableexpress: True IsAnonymousAccessible: false MaxDeliveryCount: MaxSizeInMegabytes: 16384 MessageCount: RequiresDuplicateDetection: False RequiresSession: False SizeInBytes: Status: 활성 지원 순서: False UpdatedAt: 1/20/2017 2:51:37 AM</span><span class="sxs-lookup"><span data-stu-id="6eba9-172">Name                                : SB-Queue_exampl1 Location                            : West US LockDuration                        : AccessedAt                          : AutoDeleteOnIdle                    : 10675199.02:48:05.4775807 EntityAvailabilityStatus            : CreatedAt                           : 1/20/2017 2:51:36 AM DefaultMessageTimeToLive            : 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow : EnableBatchedOperations             : True DeadLetteringOnMessageExpiration    : False EnableExpress                       : False EnablePartitioning                  : True IsAnonymousAccessible               : False MaxDeliveryCount                    : MaxSizeInMegabytes                  : 16384 MessageCount                        : CountDetails                        : RequiresDuplicateDetection          : False RequiresSession                     : False SizeInBytes                         : Status                              : Active SupportOrdering                     : False UpdatedAt                           : 1/20/2017 2:51:37 AM</span></span>

## <span data-ttu-id="6eba9-173">상속자</span><span class="sxs-lookup"><span data-stu-id="6eba9-173">NOTES</span></span>

## <span data-ttu-id="6eba9-174">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6eba9-174">RELATED LINKS</span></span>

