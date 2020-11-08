---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusSubscription.md
ms.openlocfilehash: 53f91cb6904cb8c481a5379d5499805ffe82ce33
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217025"
---
# <span data-ttu-id="d4e2d-101">New-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="d4e2d-101">New-AzServiceBusSubscription</span></span>

## <span data-ttu-id="d4e2d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4e2d-102">SYNOPSIS</span></span>
<span data-ttu-id="d4e2d-103">지정 된 Service Bus 항목에 대 한 구독을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d4e2d-103">Creates a subscription to the specified Service Bus topic.</span></span>

## <span data-ttu-id="d4e2d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d4e2d-104">SYNTAX</span></span>

```
New-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DeadLetteringOnMessageExpiration <Boolean>] [-DeadLetteringOnFilterEvaluationExceptions]
 [-EnableBatchedOperations <Boolean>] [-LockDuration <String>] [-MaxDeliveryCount <Int32>]
 [-RequiresSession <Boolean>] [-ForwardTo <String>] [-ForwardDeadLetteredMessagesTo <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4e2d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d4e2d-105">DESCRIPTION</span></span>
<span data-ttu-id="d4e2d-106">**AzServiceBusSubscription** cmdlet은 지정 된 Service Bus 항목에 대 한 새 구독을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d4e2d-106">The **New-AzServiceBusSubscription** cmdlet creates a new subscription to the specified Service Bus topic.</span></span>

## <span data-ttu-id="d4e2d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d4e2d-107">EXAMPLES</span></span>

### <span data-ttu-id="d4e2d-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="d4e2d-108">Example 1</span></span>
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

<span data-ttu-id="d4e2d-109">`SB-TopicSubscription-Example1`지정 된 Service Bus 항목에 대 한 구독을 만듭니다 `SB-Topic_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="d4e2d-109">Creates the subscription `SB-TopicSubscription-Example1` for the specified Service Bus topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="d4e2d-110">변수</span><span class="sxs-lookup"><span data-stu-id="d4e2d-110">PARAMETERS</span></span>

### <span data-ttu-id="d4e2d-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="d4e2d-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="d4e2d-112">구독이 자동으로 삭제 된 후의 [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) 유휴 간격을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4e2d-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the subscription is automatically deleted.</span></span> <span data-ttu-id="d4e2d-113">최소 기간은 5 분입니다.</span><span class="sxs-lookup"><span data-stu-id="d4e2d-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="d4e2d-114">-DeadLetteringOnFilterEvaluationExceptions</span><span class="sxs-lookup"><span data-stu-id="d4e2d-114">-DeadLetteringOnFilterEvaluationExceptions</span></span>
<span data-ttu-id="d4e2d-115">구독의 필터 평가 예외에 대 한 비활성 문자 지원이 있는지 여부를 나타내는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="d4e2d-115">Value that indicates whether a subscription has dead letter support on filter evaluation exceptions.</span></span>

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

### <span data-ttu-id="d4e2d-116">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="d4e2d-116">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="d4e2d-117">메시지 만료 시 배달 못 한 문자</span><span class="sxs-lookup"><span data-stu-id="d4e2d-117">Dead Lettering On Message Expiration</span></span>

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

### <span data-ttu-id="d4e2d-118">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="d4e2d-118">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="d4e2d-119">Timespan to live 값입니다.</span><span class="sxs-lookup"><span data-stu-id="d4e2d-119">Timespan to live value.</span></span>
<span data-ttu-id="d4e2d-120">메시지가 서비스 버스에 전송 될 때부터 메시지가 만료 되는 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="d4e2d-120">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="d4e2d-121">TimeToLive가 메시지 자체에 설정 되지 않았을 때 사용 되는 기본값입니다.</span><span class="sxs-lookup"><span data-stu-id="d4e2d-121">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="d4e2d-122">Standard = Timespan. 최대 및 기본 = 14 일</span><span class="sxs-lookup"><span data-stu-id="d4e2d-122">For Standard = Timespan.Max and Basic = 14 days</span></span>

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

### <span data-ttu-id="d4e2d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4e2d-123">-DefaultProfile</span></span>
<span data-ttu-id="d4e2d-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d4e2d-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4e2d-125">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="d4e2d-125">-EnableBatchedOperations</span></span>
<span data-ttu-id="d4e2d-126">일괄 처리 된 작업 사용-서버측 일괄 처리 된 작업을 사용할지 여부를 나타내는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="d4e2d-126">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

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

### <span data-ttu-id="d4e2d-127">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="d4e2d-127">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="d4e2d-128">배달 못한 편지 메시지를 전달 하기 위한 큐/항목 이름</span><span class="sxs-lookup"><span data-stu-id="d4e2d-128">Queue/Topic name to forward the Dead Letter message</span></span>

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

### <span data-ttu-id="d4e2d-129">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="d4e2d-129">-ForwardTo</span></span>
<span data-ttu-id="d4e2d-130">메시지를 전달 하기 위한 큐/항목 이름</span><span class="sxs-lookup"><span data-stu-id="d4e2d-130">Queue/Topic name to forward the messages</span></span>

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

### <span data-ttu-id="d4e2d-131">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="d4e2d-131">-LockDuration</span></span>
<span data-ttu-id="d4e2d-132">잠금 기간</span><span class="sxs-lookup"><span data-stu-id="d4e2d-132">Lock Duration</span></span>

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

### <span data-ttu-id="d4e2d-133">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="d4e2d-133">-MaxDeliveryCount</span></span>
<span data-ttu-id="d4e2d-134">MaxDeliveryCount-최대 배달 수입니다.</span><span class="sxs-lookup"><span data-stu-id="d4e2d-134">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="d4e2d-135">배달 횟수가 지난 후에는 메시지가 자동으로 deadlettered 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d4e2d-135">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="d4e2d-136">-이름</span><span class="sxs-lookup"><span data-stu-id="d4e2d-136">-Name</span></span>
<span data-ttu-id="d4e2d-137">구독 이름</span><span class="sxs-lookup"><span data-stu-id="d4e2d-137">Subscription Name</span></span>

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

### <span data-ttu-id="d4e2d-138">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d4e2d-138">-Namespace</span></span>
<span data-ttu-id="d4e2d-139">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="d4e2d-139">Namespace Name</span></span>

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

### <span data-ttu-id="d4e2d-140">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="d4e2d-140">-RequiresSession</span></span>
<span data-ttu-id="d4e2d-141">RequiresSession-이 대기열이 중복 검색을 요구 하는지 여부를 나타내는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="d4e2d-141">RequiresSession - the value indicating if this queue requires duplicate detection.</span></span>

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

### <span data-ttu-id="d4e2d-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4e2d-142">-ResourceGroupName</span></span>
<span data-ttu-id="d4e2d-143">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d4e2d-143">The name of the resource group</span></span>

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

### <span data-ttu-id="d4e2d-144">-주제</span><span class="sxs-lookup"><span data-stu-id="d4e2d-144">-Topic</span></span>
<span data-ttu-id="d4e2d-145">주제 이름</span><span class="sxs-lookup"><span data-stu-id="d4e2d-145">Topic Name</span></span>

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

### <span data-ttu-id="d4e2d-146">-확인</span><span class="sxs-lookup"><span data-stu-id="d4e2d-146">-Confirm</span></span>
<span data-ttu-id="d4e2d-147">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4e2d-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4e2d-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4e2d-148">-WhatIf</span></span>
<span data-ttu-id="d4e2d-149">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d4e2d-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4e2d-150">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d4e2d-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4e2d-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4e2d-151">CommonParameters</span></span>
<span data-ttu-id="d4e2d-152">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4e2d-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4e2d-153">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4e2d-153">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4e2d-154">입력</span><span class="sxs-lookup"><span data-stu-id="d4e2d-154">INPUTS</span></span>

### <span data-ttu-id="d4e2d-155">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d4e2d-155">System.String</span></span>

### <span data-ttu-id="d4e2d-156">시스템 Null 허용 ' 1 [[CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d4e2d-156">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="d4e2d-157">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e])</span><span class="sxs-lookup"><span data-stu-id="d4e2d-157">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="d4e2d-158">출력</span><span class="sxs-lookup"><span data-stu-id="d4e2d-158">OUTPUTS</span></span>

### <span data-ttu-id="d4e2d-159">ServiceBus-PSSubscriptionAttributes.</span><span class="sxs-lookup"><span data-stu-id="d4e2d-159">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="d4e2d-160">상속자</span><span class="sxs-lookup"><span data-stu-id="d4e2d-160">NOTES</span></span>

## <span data-ttu-id="d4e2d-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d4e2d-161">RELATED LINKS</span></span>
