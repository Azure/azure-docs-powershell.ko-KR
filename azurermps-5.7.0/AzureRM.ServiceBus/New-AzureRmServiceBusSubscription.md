---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusSubscription.md
ms.openlocfilehash: 54753001be0a754cf9416e1b2ec53fd81647d8d9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703217"
---
# <span data-ttu-id="bf268-101">New-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="bf268-101">New-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="bf268-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf268-102">SYNOPSIS</span></span>
<span data-ttu-id="bf268-103">지정 된 Service Bus 항목에 대 한 구독을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bf268-103">Creates a subscription to the specified Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf268-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bf268-104">SYNTAX</span></span>

```
New-AzureRmServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DeadLetteringOnMessageExpiration <Boolean>] [-DeadLetteringOnFilterEvaluationExceptions]
 [-EnableBatchedOperations <Boolean>] [-LockDuration <String>] [-MaxDeliveryCount <Int32>]
 [-RequiresSession <Boolean>] [-ForwardTo <String>] [-ForwardDeadLetteredMessagesTo <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf268-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bf268-105">DESCRIPTION</span></span>
<span data-ttu-id="bf268-106">**AzureRmServiceBusSubscription** cmdlet은 지정 된 Service Bus 항목에 대 한 새 구독을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bf268-106">The **New-AzureRmServiceBusSubscription** cmdlet creates a new subscription to the specified Service Bus topic.</span></span>

## <span data-ttu-id="bf268-107">예제의</span><span class="sxs-lookup"><span data-stu-id="bf268-107">EXAMPLES</span></span>

### <span data-ttu-id="bf268-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="bf268-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

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
<span data-ttu-id="bf268-109">`SB-TopicSubscription-Example1`지정 된 Service Bus 항목에 대 한 구독을 만듭니다 `SB-Topic_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="bf268-109">Creates the subscription `SB-TopicSubscription-Example1` for the specified Service Bus topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="bf268-110">변수</span><span class="sxs-lookup"><span data-stu-id="bf268-110">PARAMETERS</span></span>

### <span data-ttu-id="bf268-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="bf268-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="bf268-112">구독이 자동으로 삭제 된 후의 [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) 유휴 간격을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf268-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the subscription is automatically deleted.</span></span> <span data-ttu-id="bf268-113">최소 기간은 5 분입니다.</span><span class="sxs-lookup"><span data-stu-id="bf268-113">The minimum duration is 5 minutes.</span></span>


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

### <span data-ttu-id="bf268-114">-확인</span><span class="sxs-lookup"><span data-stu-id="bf268-114">-Confirm</span></span>
<span data-ttu-id="bf268-115">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf268-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf268-116">-DeadLetteringOnFilterEvaluationExceptions</span><span class="sxs-lookup"><span data-stu-id="bf268-116">-DeadLetteringOnFilterEvaluationExceptions</span></span>
<span data-ttu-id="bf268-117">구독의 필터 평가 예외에 대 한 비활성 문자 지원이 있는지 여부를 나타내는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="bf268-117">Value that indicates whether a subscription has dead letter support on filter evaluation exceptions.</span></span>

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

### <span data-ttu-id="bf268-118">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="bf268-118">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="bf268-119">메시지 만료 시 배달 못 한 문자</span><span class="sxs-lookup"><span data-stu-id="bf268-119">Dead Lettering On Message Expiration</span></span>

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

### <span data-ttu-id="bf268-120">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="bf268-120">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="bf268-121">Timespan to live 값입니다.</span><span class="sxs-lookup"><span data-stu-id="bf268-121">Timespan to live value.</span></span>
<span data-ttu-id="bf268-122">메시지가 서비스 버스에 전송 될 때부터 메시지가 만료 되는 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="bf268-122">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span>
<span data-ttu-id="bf268-123">TimeToLive가 메시지 자체에 설정 되지 않았을 때 사용 되는 기본값입니다.</span><span class="sxs-lookup"><span data-stu-id="bf268-123">This is the default value used when TimeToLive is not set on a message itself.</span></span>
<span data-ttu-id="bf268-124">Standard = Timespan. 최대 및 기본 = 14 dyas</span><span class="sxs-lookup"><span data-stu-id="bf268-124">For Standard = Timespan.Max and Basic = 14 dyas</span></span>

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

### <span data-ttu-id="bf268-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf268-125">-DefaultProfile</span></span>
<span data-ttu-id="bf268-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bf268-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bf268-127">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="bf268-127">-EnableBatchedOperations</span></span>
<span data-ttu-id="bf268-128">일괄 처리 된 작업 사용-서버측 일괄 처리 된 작업을 사용할지 여부를 나타내는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="bf268-128">Enable Batched Operations - value that indicates whether server-side batched operations are enabled</span></span>

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

### <span data-ttu-id="bf268-129">-ForwardDeadLetteredMessagesTo</span><span class="sxs-lookup"><span data-stu-id="bf268-129">-ForwardDeadLetteredMessagesTo</span></span>
<span data-ttu-id="bf268-130">배달 못한 편지 메시지를 전달 하기 위한 큐/항목 이름</span><span class="sxs-lookup"><span data-stu-id="bf268-130">Queue/Topic name to forward the Dead Letter message</span></span>

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

### <span data-ttu-id="bf268-131">-ForwardTo</span><span class="sxs-lookup"><span data-stu-id="bf268-131">-ForwardTo</span></span>
<span data-ttu-id="bf268-132">메시지를 전달 하기 위한 큐/항목 이름</span><span class="sxs-lookup"><span data-stu-id="bf268-132">Queue/Topic name to forward the messages</span></span>

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

### <span data-ttu-id="bf268-133">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="bf268-133">-LockDuration</span></span>
<span data-ttu-id="bf268-134">잠금 기간</span><span class="sxs-lookup"><span data-stu-id="bf268-134">Lock Duration</span></span>

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

### <span data-ttu-id="bf268-135">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="bf268-135">-MaxDeliveryCount</span></span>
<span data-ttu-id="bf268-136">MaxDeliveryCount-최대 배달 수입니다.</span><span class="sxs-lookup"><span data-stu-id="bf268-136">MaxDeliveryCount - the maximum delivery count.</span></span>
<span data-ttu-id="bf268-137">배달 횟수가 지난 후에는 메시지가 자동으로 deadlettered 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bf268-137">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="bf268-138">-이름</span><span class="sxs-lookup"><span data-stu-id="bf268-138">-Name</span></span>
<span data-ttu-id="bf268-139">구독 이름</span><span class="sxs-lookup"><span data-stu-id="bf268-139">Subscription Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf268-140">-Namespace</span><span class="sxs-lookup"><span data-stu-id="bf268-140">-Namespace</span></span>
<span data-ttu-id="bf268-141">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="bf268-141">Namespace Name</span></span>

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

### <span data-ttu-id="bf268-142">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="bf268-142">-RequiresSession</span></span>
<span data-ttu-id="bf268-143">RequiresSession-이 대기열이 중복 검색을 요구 하는지 여부를 나타내는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="bf268-143">RequiresSession - the value indicating if this queue requires duplicate detection.</span></span>

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

### <span data-ttu-id="bf268-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf268-144">-ResourceGroupName</span></span>
<span data-ttu-id="bf268-145">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bf268-145">The name of the resource group</span></span>

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

### <span data-ttu-id="bf268-146">-주제</span><span class="sxs-lookup"><span data-stu-id="bf268-146">-Topic</span></span>
<span data-ttu-id="bf268-147">주제 이름</span><span class="sxs-lookup"><span data-stu-id="bf268-147">Topic Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf268-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf268-148">-WhatIf</span></span>
<span data-ttu-id="bf268-149">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="bf268-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf268-150">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bf268-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf268-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf268-151">CommonParameters</span></span>
<span data-ttu-id="bf268-152">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf268-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="bf268-153">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf268-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf268-154">입력</span><span class="sxs-lookup"><span data-stu-id="bf268-154">INPUTS</span></span>

### <span data-ttu-id="bf268-155">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="bf268-155">-ResourceGroup</span></span>
 <span data-ttu-id="bf268-156">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="bf268-156">System.String</span></span>
 

### <span data-ttu-id="bf268-157">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="bf268-157">-NamespaceName</span></span>
 <span data-ttu-id="bf268-158">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="bf268-158">System.String</span></span>
 

### <span data-ttu-id="bf268-159">-TopicName</span><span class="sxs-lookup"><span data-stu-id="bf268-159">-TopicName</span></span>
 <span data-ttu-id="bf268-160">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="bf268-160">System.String</span></span>
 

### <span data-ttu-id="bf268-161">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="bf268-161">-SubscriptionName</span></span>
 <span data-ttu-id="bf268-162">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="bf268-162">System.String</span></span>


## <span data-ttu-id="bf268-163">출력</span><span class="sxs-lookup"><span data-stu-id="bf268-163">OUTPUTS</span></span>

### <span data-ttu-id="bf268-164">ServiceBus-PSSubscriptionAttributes.</span><span class="sxs-lookup"><span data-stu-id="bf268-164">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>


## <span data-ttu-id="bf268-165">상속자</span><span class="sxs-lookup"><span data-stu-id="bf268-165">NOTES</span></span>

## <span data-ttu-id="bf268-166">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bf268-166">RELATED LINKS</span></span>
