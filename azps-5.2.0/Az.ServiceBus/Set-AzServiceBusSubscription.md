---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusSubscription.md
ms.openlocfilehash: 2bff80a8f04dada3625eaa5b0a16287bb37c6a13
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98339309"
---
# <span data-ttu-id="32618-101">Set-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="32618-101">Set-AzServiceBusSubscription</span></span>

## <span data-ttu-id="32618-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32618-102">SYNOPSIS</span></span>
<span data-ttu-id="32618-103">지정된 Service Bus 네임스페이스에서 Service Bus 토픽에 대한 구독 설명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="32618-103">Updates a subscription description for a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="32618-104">구문</span><span class="sxs-lookup"><span data-stu-id="32618-104">SYNTAX</span></span>

```
Set-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-InputObject] <PSSubscriptionAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="32618-105">설명</span><span class="sxs-lookup"><span data-stu-id="32618-105">DESCRIPTION</span></span>
<span data-ttu-id="32618-106">**Set-AzServiceBusSubscription** cmdlet은 지정된 Service Bus 네임스페이스에서 Service Bus 토픽에 대한 구독에 대한 설명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="32618-106">The **Set-AzServiceBusSubscription** cmdlet updates the description of the subscription for the Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="32618-107">예제</span><span class="sxs-lookup"><span data-stu-id="32618-107">EXAMPLES</span></span>

### <span data-ttu-id="32618-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="32618-108">Example 1</span></span>
```
PS C:\> $subscriptionObj = Get-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

PS C:\> $subscriptionObj.DeadLetteringOnMessageExpiration = $True
PS C:\> $subscriptionObj.MaxDeliveryCount = 9

Name                                      : SB-TopicSubscription-Example1
AccessedAt                                : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                          : 10675199.02:48:05.4775807
CountDetails                              : 
CreatedAt                                 : 1/20/2017 9:59:15 PM
DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807
DeadLetteringOnMessageExpiration          : True
EnableBatchedOperations                   : True
LockDuration                              : 00:01:00
MaxDeliveryCount                          : 9
MessageCount                              : 0
RequiresSession                           : False
Status                                    : Active
UpdatedAt                                 : 1/20/2017 9:59:15 PM
PS C:\> Set-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionObj $subscriptionObj
```

<span data-ttu-id="32618-109">지정된 구독에 대한 설명을 지정된 토픽으로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="32618-109">Updates the description for the specified subscription to the given topic.</span></span> <span data-ttu-id="32618-110">이 예제에서는 **DeadLetteringOnMessageExpiration** 속성을 **true로,** **MaxDeliveryCount를** 9로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="32618-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **MaxDeliveryCount** to 9.</span></span>

## <span data-ttu-id="32618-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="32618-111">PARAMETERS</span></span>

### <span data-ttu-id="32618-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32618-112">-DefaultProfile</span></span>
<span data-ttu-id="32618-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="32618-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32618-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="32618-114">-InputObject</span></span>
<span data-ttu-id="32618-115">ServiceBus 구독 정의입니다.</span><span class="sxs-lookup"><span data-stu-id="32618-115">ServiceBus Subscription definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes
Parameter Sets: (All)
Aliases: SubscriptionObj

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32618-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="32618-116">-Namespace</span></span>
<span data-ttu-id="32618-117">네임스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="32618-117">Namespace Name.</span></span>

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

### <span data-ttu-id="32618-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32618-118">-ResourceGroupName</span></span>
<span data-ttu-id="32618-119">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="32618-119">The name of the resource group</span></span>

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

### <span data-ttu-id="32618-120">-Topic</span><span class="sxs-lookup"><span data-stu-id="32618-120">-Topic</span></span>
<span data-ttu-id="32618-121">토픽 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="32618-121">Topic Name.</span></span>

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

### <span data-ttu-id="32618-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="32618-122">-Confirm</span></span>
<span data-ttu-id="32618-123">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="32618-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32618-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32618-124">-WhatIf</span></span>
<span data-ttu-id="32618-125">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="32618-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32618-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="32618-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32618-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32618-127">CommonParameters</span></span>
<span data-ttu-id="32618-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="32618-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32618-129">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="32618-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32618-130">입력</span><span class="sxs-lookup"><span data-stu-id="32618-130">INPUTS</span></span>

### <span data-ttu-id="32618-131">System.String</span><span class="sxs-lookup"><span data-stu-id="32618-131">System.String</span></span>

### <span data-ttu-id="32618-132">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="32618-132">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="32618-133">출력</span><span class="sxs-lookup"><span data-stu-id="32618-133">OUTPUTS</span></span>

### <span data-ttu-id="32618-134">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="32618-134">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="32618-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="32618-135">NOTES</span></span>

## <span data-ttu-id="32618-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="32618-136">RELATED LINKS</span></span>
