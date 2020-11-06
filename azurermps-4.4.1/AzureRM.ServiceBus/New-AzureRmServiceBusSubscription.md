---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusSubscription.md
ms.openlocfilehash: ea305b334e6efd4cb1c5af47db2a1b8817e7cab6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530667"
---
# <span data-ttu-id="3d044-101">New-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="3d044-101">New-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="3d044-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d044-102">SYNOPSIS</span></span>
<span data-ttu-id="3d044-103">지정 된 Service Bus 항목에 대 한 구독을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3d044-103">Creates a subscription to the specified Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3d044-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3d044-104">SYNTAX</span></span>

```
New-AzureRmServiceBusSubscription -ResourceGroupName <String> -Namespace <String> -Topic <String>
 -Name <String> [-AutoDeleteOnIdle <String>] [-DefaultMessageTimeToLive <String>]
 [-DeadLetteringOnFilterEvaluationExceptions <Boolean>] [-DeadLetteringOnMessageExpiration <Boolean>]
 [-EnableBatchedOperations <Boolean>] [-IsReadOnly <Boolean>] [-LockDuration <String>]
 [-MaxDeliveryCount <Int32>] [-RequiresSession <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d044-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3d044-105">DESCRIPTION</span></span>
<span data-ttu-id="3d044-106">**AzureRmServiceBusSubscription** cmdlet은 지정 된 Service Bus 항목에 대 한 새 구독을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3d044-106">The **New-AzureRmServiceBusSubscription** cmdlet creates a new subscription to the specified Service Bus topic.</span></span>

## <span data-ttu-id="3d044-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3d044-107">EXAMPLES</span></span>

### <span data-ttu-id="3d044-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="3d044-108">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="3d044-109">`SB-TopicSubscription-Example1`지정 된 Service Bus 항목에 대 한 구독을 만듭니다 `SB-Topic_exampl1` .</span><span class="sxs-lookup"><span data-stu-id="3d044-109">Creates the subscription `SB-TopicSubscription-Example1` for the specified Service Bus topic `SB-Topic_exampl1`.</span></span>

## <span data-ttu-id="3d044-110">변수</span><span class="sxs-lookup"><span data-stu-id="3d044-110">PARAMETERS</span></span>

### <span data-ttu-id="3d044-111">-AutoDeleteOnIdle</span><span class="sxs-lookup"><span data-stu-id="3d044-111">-AutoDeleteOnIdle</span></span>
<span data-ttu-id="3d044-112">구독이 자동으로 삭제 된 후의 [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) 유휴 간격을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d044-112">Specifies the [TimeSpan](https://msdn.microsoft.com/library/system.timespan.aspx) idle interval, after which the subscription is automatically deleted.</span></span> <span data-ttu-id="3d044-113">최소 기간은 5 분입니다.</span><span class="sxs-lookup"><span data-stu-id="3d044-113">The minimum duration is 5 minutes.</span></span>

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

### <span data-ttu-id="3d044-114">-DeadLetteringOnFilterEvaluationExceptions</span><span class="sxs-lookup"><span data-stu-id="3d044-114">-DeadLetteringOnFilterEvaluationExceptions</span></span>
<span data-ttu-id="3d044-115">구독에서 필터 평가 예외에 대해 무반응 문자를 지원 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3d044-115">Indicates if a subscription has dead letter support on Filter evaluation exceptions.</span></span>

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

### <span data-ttu-id="3d044-116">-DeadLetteringOnMessageExpiration</span><span class="sxs-lookup"><span data-stu-id="3d044-116">-DeadLetteringOnMessageExpiration</span></span>
<span data-ttu-id="3d044-117">메시지가 만료 되는 경우 구독에 배달 못한 시간이 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3d044-117">Indicates if a subscription has deadletter support when a message expires.</span></span>

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

### <span data-ttu-id="3d044-118">-EnableBatchedOperations</span><span class="sxs-lookup"><span data-stu-id="3d044-118">-EnableBatchedOperations</span></span>
<span data-ttu-id="3d044-119">서버 쪽 일괄 처리 된 작업을 사용할 수 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3d044-119">Indicates whether server-side batched operations are enabled.</span></span>

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

### <span data-ttu-id="3d044-120">-IsReadOnly</span><span class="sxs-lookup"><span data-stu-id="3d044-120">-IsReadOnly</span></span>
<span data-ttu-id="3d044-121">엔터티 설명이 읽기 전용인 지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3d044-121">Indicates whether the entity description is read-only</span></span>

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

### <span data-ttu-id="3d044-122">-LockDuration</span><span class="sxs-lookup"><span data-stu-id="3d044-122">-LockDuration</span></span>
<span data-ttu-id="3d044-123">구독에 대 한 잠금 기간 시간 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d044-123">Specifies the lock duration time span for the subscription.</span></span>

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

### <span data-ttu-id="3d044-124">-MaxDeliveryCount</span><span class="sxs-lookup"><span data-stu-id="3d044-124">-MaxDeliveryCount</span></span>
<span data-ttu-id="3d044-125">최대 배달 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d044-125">Specifies the number of maximum deliveries.</span></span> <span data-ttu-id="3d044-126">배달 횟수가 지난 후에는 메시지가 자동으로 deadlettered 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d044-126">A message is automatically deadlettered after this number of deliveries.</span></span>

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

### <span data-ttu-id="3d044-127">-RequiresSession</span><span class="sxs-lookup"><span data-stu-id="3d044-127">-RequiresSession</span></span>
<span data-ttu-id="3d044-128">구독이 세션 개념을 지원 하는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d044-128">Specifies whether a subscription supports the concept of sessions.</span></span>

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

### <span data-ttu-id="3d044-129">-확인</span><span class="sxs-lookup"><span data-stu-id="3d044-129">-Confirm</span></span>
<span data-ttu-id="3d044-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d044-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d044-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d044-131">-WhatIf</span></span>
<span data-ttu-id="3d044-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3d044-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d044-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3d044-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d044-134">-DefaultMessageTimeToLive</span><span class="sxs-lookup"><span data-stu-id="3d044-134">-DefaultMessageTimeToLive</span></span>
<span data-ttu-id="3d044-135">Timespan to live 값입니다.</span><span class="sxs-lookup"><span data-stu-id="3d044-135">Timespan to live value.</span></span> <span data-ttu-id="3d044-136">메시지가 서비스 버스에 전송 될 때부터 메시지가 만료 되는 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="3d044-136">This is the duration after which the message expires, starting from when the message is sent to Service Bus.</span></span> <span data-ttu-id="3d044-137">TimeToLive가 메시지 자체에 설정 되지 않았을 때 사용 되는 기본값입니다.</span><span class="sxs-lookup"><span data-stu-id="3d044-137">This is the default value used when TimeToLive is not set on a message itself.</span></span> <span data-ttu-id="3d044-138">Standard = Timespan. 최대 및 기본 = 14 dyas</span><span class="sxs-lookup"><span data-stu-id="3d044-138">For Standard = Timespan.Max and Basic = 14 dyas</span></span>

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

### <span data-ttu-id="3d044-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d044-139">-DefaultProfile</span></span>
<span data-ttu-id="3d044-140">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3d044-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d044-141">-이름</span><span class="sxs-lookup"><span data-stu-id="3d044-141">-Name</span></span>
<span data-ttu-id="3d044-142">구독 이름</span><span class="sxs-lookup"><span data-stu-id="3d044-142">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d044-143">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3d044-143">-Namespace</span></span>
<span data-ttu-id="3d044-144">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3d044-144">Namespace Name.</span></span>

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

### <span data-ttu-id="3d044-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d044-145">-ResourceGroupName</span></span>
<span data-ttu-id="3d044-146">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3d044-146">The name of the resource group</span></span>

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

### <span data-ttu-id="3d044-147">-주제</span><span class="sxs-lookup"><span data-stu-id="3d044-147">-Topic</span></span>
<span data-ttu-id="3d044-148">주제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3d044-148">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d044-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d044-149">CommonParameters</span></span>
<span data-ttu-id="3d044-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d044-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d044-151">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d044-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d044-152">입력</span><span class="sxs-lookup"><span data-stu-id="3d044-152">INPUTS</span></span>

### <span data-ttu-id="3d044-153">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="3d044-153">-ResourceGroup</span></span>
 <span data-ttu-id="3d044-154">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3d044-154">System.String</span></span>
 

### <span data-ttu-id="3d044-155">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="3d044-155">-NamespaceName</span></span>
 <span data-ttu-id="3d044-156">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3d044-156">System.String</span></span>
 

### <span data-ttu-id="3d044-157">-TopicName</span><span class="sxs-lookup"><span data-stu-id="3d044-157">-TopicName</span></span>
 <span data-ttu-id="3d044-158">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3d044-158">System.String</span></span>
 

### <span data-ttu-id="3d044-159">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="3d044-159">-SubscriptionName</span></span>
 <span data-ttu-id="3d044-160">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3d044-160">System.String</span></span>

## <span data-ttu-id="3d044-161">출력</span><span class="sxs-lookup"><span data-stu-id="3d044-161">OUTPUTS</span></span>

### <span data-ttu-id="3d044-162">ServiceBus/. i a m.</span><span class="sxs-lookup"><span data-stu-id="3d044-162">Microsoft.Azure.Commands.ServiceBus.Models.SubscriptionAttributes</span></span>
<span data-ttu-id="3d044-163">이름: SB-TopicSubscription-Example1 Location: 미국 US AccessedAt: 1/20/2017 3:18:54 AM AutoDeleteOnIdle: 10675199.02:48: MessageCountDetails CreatedAt: 1/20/2017 3:18:52 AM DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DeadLetteringOnFilterEvaluationExceptions: True DeadLetteringOnMessageExpiration: 거짓 EnableBatchedOperations: true EntityAvailabilityStatus: False ServiceBus: 00:01:00 IsReadOnly: 10 MessageCount: 0 MaxDeliveryCount: False 상태: 활성 RequiresSession: 1/20/2017 3:18:54 AM</span><span class="sxs-lookup"><span data-stu-id="3d044-163">Name                                      : SB-TopicSubscription-Example1 Location                                  : West US AccessedAt                                : 1/20/2017 3:18:54 AM AutoDeleteOnIdle                          : 10675199.02:48:05.4775807 CountDetails                              : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails CreatedAt                                 : 1/20/2017 3:18:52 AM DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807 DeadLetteringOnFilterEvaluationExceptions : True DeadLetteringOnMessageExpiration          : False EnableBatchedOperations                   : True EntityAvailabilityStatus                  : Available IsReadOnly                                : LockDuration                              : 00:01:00 MaxDeliveryCount                          : 10 MessageCount                              : 0 RequiresSession                           : False Status                                    : Active UpdatedAt                                 : 1/20/2017 3:18:54 AM</span></span>

## <span data-ttu-id="3d044-164">상속자</span><span class="sxs-lookup"><span data-stu-id="3d044-164">NOTES</span></span>

## <span data-ttu-id="3d044-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3d044-165">RELATED LINKS</span></span>

