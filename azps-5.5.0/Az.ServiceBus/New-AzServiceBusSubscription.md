---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusSubscription.md
ms.openlocfilehash: 53f91cb6904cb8c481a5379d5499805ffe82ce33
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208128"
---
# <span data-ttu-id="b301e-101">New-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="b301e-101">New-AzServiceBusSubscription</span></span>

## <span data-ttu-id="b301e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b301e-102">SYNOPSIS</span></span>
<span data-ttu-id="b301e-103">지정된 Service Bus 토픽에 대한 구독을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b301e-103">Creates a subscription to the specified Service Bus topic.</span></span>

## <span data-ttu-id="b301e-104">구문</span><span class="sxs-lookup"><span data-stu-id="b301e-104">SYNTAX</span></span>

```
New-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DeadLetteringOnMessageExpiration <Boolean>] [-DeadLetteringOnFilterEvaluationExceptions]
 [-EnableBatchedOperations <Boolean>] [-LockDuration <String>] [-MaxDeliveryCount <Int32>]
 [-RequiresSession <Boolean>] [-ForwardTo <String>] [-ForwardDeadLetteredMessagesTo <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b301e-105">설명</span><span class="sxs-lookup"><span data-stu-id="b301e-105">DESCRIPTION</span></span>
<span data-ttu-id="b301e-106">**New-AzServiceBusSubscription** cmdlet은 지정된 Service Bus 토픽에 대한 새 구독을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b301e-106">The **New-AzServiceBusSubscription** cmdlet creates a new subscription to the specified Service Bus topic.</span></span>

## <span data-ttu-id="b301e-107">예제</span><span class="sxs-lookup"><span data-stu-id="b301e-107">EXAMPLES</span></span>

### <span data-ttu-id="b301e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b301e-108">Example 1</span></span>
```
PS C:\> New-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

Name                                      : SB-TopicSubscription-Example1
AccessedAt                                : 1/20/2017 3:18:54 AM
AutoDeleteOnIdle                          : 10675199.02:48:05.4775807
CountDetails                              : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
CreatedAt                                 : 1/20/2017 3:18:52 AM
DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807
DeadLetteringOnMessageExpiration          : False
EnableBatchedOperations                   : True
LockDuration                              : 00:01:00
MaxDeliveryCount                          : 10
MessageCount                              : 0
RequiresSession                           : False
Status                                    : Active
UpdatedAt                                 : 1/20/2017 3:18:54 AM
```

<span data-ttu-id="b301e-109">지정된 `SB-TopicSubscription-Example1` Service Bus 토픽에 대한 구독을 `SB-Topic_exampl1` 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b301e-109">Creates the subscription `SB-TopicSubscription-Example1` for the specified Service Bus topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="b301e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b301e-110">PARAMETERS</span></span>

### <span data-ttu-id="b301e-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="b301e-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="b301e-112">구독이 자동으로 삭제되는 [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) 유휴 간격을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b301e-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the subscription is automatically deleted.</span></span> <span data-ttu-id="b301e-113">최소 기간은 5분입니다.</span><span class="sxs-lookup"><span data-stu-id="b301e-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="b301e-114">-DeadLetteringOnFilterEvaluationExceptions</span><span class="sxs-lookup"><span data-stu-id="b301e-114">-DeadLetteringOnFilterEvaluationExceptions</span></span>
<span data-ttu-id="b301e-115">구독에 필터 평가 예외에 대한 dead letter 지원이 있는지 여부를 나타내는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="b301e-115">Value that indicates whether a subscription has dead letter support on filter evaluation exceptions.</span></span>

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

### <span data-ttu-id="b301e-116">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="b301e-116">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="b301e-117">메시지 만료 시 Dead Lettering</span><span class="sxs-lookup"><span data-stu-id="b301e-117">Dead Lettering On Message Expiration</span></span>

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

### <span data-ttu-id="b301e-118">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="b301e-118">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="b301e-119">Timespan to live 값입니다.</span><span class="sxs-lookup"><span data-stu-id="b301e-119">Timespan to live value.</span></span>
<span data-ttu-id="b301e-120">메시지가 Service Bus로 전송될 때부터 메시지가 만료되는 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="b301e-120">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="b301e-121">TimeToLive가 메시지 자체에 설정되지 않은 경우 사용되는 기본값입니다.</span><span class="sxs-lookup"><span data-stu-id="b301e-121">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="b301e-122">Standard = Timespan.Max 및 Basic = 14일</span><span class="sxs-lookup"><span data-stu-id="b301e-122">For Standard = Timespan.Max and Basic = 14 days</span></span>

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

### <span data-ttu-id="b301e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b301e-123">-DefaultProfile</span></span>
<span data-ttu-id="b301e-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b301e-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b301e-125">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="b301e-125">-EnableBatchedOperations</span></span>
<span data-ttu-id="b301e-126">일괄 처리 작업 사용 - 서버 쪽 일괄 처리 작업이 사용하도록 설정되어 있는지 여부를 나타내는 값</span><span class="sxs-lookup"><span data-stu-id="b301e-126">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

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

### <span data-ttu-id="b301e-127">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="b301e-127">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="b301e-128">Dead Letter 메시지를 전달할 큐/토픽 이름</span><span class="sxs-lookup"><span data-stu-id="b301e-128">Queue/Topic name to forward the Dead Letter message</span></span>

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

### <span data-ttu-id="b301e-129">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="b301e-129">-ForwardTo</span></span>
<span data-ttu-id="b301e-130">메시지를 전달할 큐/토픽 이름</span><span class="sxs-lookup"><span data-stu-id="b301e-130">Queue/Topic name to forward the messages</span></span>

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

### <span data-ttu-id="b301e-131">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="b301e-131">-LockDuration</span></span>
<span data-ttu-id="b301e-132">잠금 기간</span><span class="sxs-lookup"><span data-stu-id="b301e-132">Lock Duration</span></span>

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

### <span data-ttu-id="b301e-133">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="b301e-133">-MaxDeliveryCount</span></span>
<span data-ttu-id="b301e-134">MaxDeliveryCount - 최대 배달 수입니다.</span><span class="sxs-lookup"><span data-stu-id="b301e-134">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="b301e-135">이 수의 배달 후에 메시지가 자동으로 배달되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b301e-135">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="b301e-136">-Name</span><span class="sxs-lookup"><span data-stu-id="b301e-136">-Name</span></span>
<span data-ttu-id="b301e-137">구독 이름</span><span class="sxs-lookup"><span data-stu-id="b301e-137">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b301e-138">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b301e-138">-Namespace</span></span>
<span data-ttu-id="b301e-139">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="b301e-139">Namespace Name</span></span>

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

### <span data-ttu-id="b301e-140">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="b301e-140">-RequiresSession</span></span>
<span data-ttu-id="b301e-141">RequiresSession - 이 큐에 중복 검색이 필요한지 나타내는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="b301e-141">RequiresSession - the value indicating if this queue requires duplicate detection.</span></span>

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

### <span data-ttu-id="b301e-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b301e-142">-ResourceGroupName</span></span>
<span data-ttu-id="b301e-143">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="b301e-143">The name of the resource group</span></span>

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

### <span data-ttu-id="b301e-144">-Topic</span><span class="sxs-lookup"><span data-stu-id="b301e-144">-Topic</span></span>
<span data-ttu-id="b301e-145">토픽 이름</span><span class="sxs-lookup"><span data-stu-id="b301e-145">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b301e-146">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b301e-146">-Confirm</span></span>
<span data-ttu-id="b301e-147">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b301e-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b301e-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b301e-148">-WhatIf</span></span>
<span data-ttu-id="b301e-149">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b301e-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b301e-150">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b301e-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b301e-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b301e-151">CommonParameters</span></span>
<span data-ttu-id="b301e-152">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b301e-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b301e-153">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b301e-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b301e-154">입력</span><span class="sxs-lookup"><span data-stu-id="b301e-154">INPUTS</span></span>

### <span data-ttu-id="b301e-155">System.String</span><span class="sxs-lookup"><span data-stu-id="b301e-155">System.String</span></span>

### <span data-ttu-id="b301e-156">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b301e-156">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b301e-157">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b301e-157">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="b301e-158">출력</span><span class="sxs-lookup"><span data-stu-id="b301e-158">OUTPUTS</span></span>

### <span data-ttu-id="b301e-159">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="b301e-159">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="b301e-160">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b301e-160">NOTES</span></span>

## <span data-ttu-id="b301e-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b301e-161">RELATED LINKS</span></span>
