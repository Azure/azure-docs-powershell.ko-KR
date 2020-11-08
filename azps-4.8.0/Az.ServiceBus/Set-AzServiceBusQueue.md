---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusQueue.md
ms.openlocfilehash: f1c3019b7d79330b1e4b0a26bd16f469eb794224
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047605"
---
# <span data-ttu-id="0754b-101">Set-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="0754b-101">Set-AzServiceBusQueue</span></span>

## <span data-ttu-id="0754b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0754b-102">SYNOPSIS</span></span>
<span data-ttu-id="0754b-103">지정 된 Service Bus 네임 스페이스의 Service Bus 큐에 대 한 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0754b-103">Updates the description of a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="0754b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0754b-104">SYNTAX</span></span>

```
Set-AzServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject] <PSQueueAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0754b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0754b-105">DESCRIPTION</span></span>
<span data-ttu-id="0754b-106">**Set-AzServiceBusQueue** cmdlet은 지정 된 service bus 네임 스페이스의 service bus 큐에 대 한 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0754b-106">The **Set-AzServiceBusQueue** cmdlet updates the description for the Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="0754b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0754b-107">EXAMPLES</span></span>

### <span data-ttu-id="0754b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="0754b-108">Example 1</span></span>
```
PS C:\> $QueueObj = Get-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1

PS C:\> $QueueObj.DeadLetteringOnMessageExpiration = $True
PS C:\> $QueueObj.SupportOrdering = $True

PS C:\> Set-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1 -QueueObj $QueueObj

Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_exampl1
Name                                : SB-Queue_exampl1
LockDuration                        : PT1M
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 1/1/0001 12:00:00 AM
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
DeadLetteringOnMessageExpiration    : True
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
UpdatedAt                           : 1/1/0001 12:00:00 AM
ForwardTo                           :
ForwardDeadLetteredMessagesTo       :
EnableBatchedOperations             : False
```

<span data-ttu-id="0754b-109">지정한 네임 스페이스의 새 설명으로 지정 된 큐를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0754b-109">Updates the specified queue with a new description in the specified namespace.</span></span> <span data-ttu-id="0754b-110">이 예제에서는 **DeadLetteringOnMessageExpiration** 속성을 **True** 로, **supportordering** 를 **true** 로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0754b-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **SupportOrdering** to **true**.</span></span>

## <span data-ttu-id="0754b-111">변수</span><span class="sxs-lookup"><span data-stu-id="0754b-111">PARAMETERS</span></span>

### <span data-ttu-id="0754b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0754b-112">-DefaultProfile</span></span>
<span data-ttu-id="0754b-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0754b-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0754b-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0754b-114">-InputObject</span></span>
<span data-ttu-id="0754b-115">ServiceBus 정의.</span><span class="sxs-lookup"><span data-stu-id="0754b-115">ServiceBus definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes
Parameter Sets: (All)
Aliases: QueueObj

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0754b-116">-이름</span><span class="sxs-lookup"><span data-stu-id="0754b-116">-Name</span></span>
<span data-ttu-id="0754b-117">큐 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0754b-117">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0754b-118">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0754b-118">-Namespace</span></span>
<span data-ttu-id="0754b-119">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0754b-119">Namespace Name.</span></span>

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

### <span data-ttu-id="0754b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0754b-120">-ResourceGroupName</span></span>
<span data-ttu-id="0754b-121">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0754b-121">The name of the resource group</span></span>

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

### <span data-ttu-id="0754b-122">-확인</span><span class="sxs-lookup"><span data-stu-id="0754b-122">-Confirm</span></span>
<span data-ttu-id="0754b-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0754b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0754b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0754b-124">-WhatIf</span></span>
<span data-ttu-id="0754b-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0754b-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0754b-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0754b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0754b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0754b-127">CommonParameters</span></span>
<span data-ttu-id="0754b-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0754b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0754b-129">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0754b-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0754b-130">입력</span><span class="sxs-lookup"><span data-stu-id="0754b-130">INPUTS</span></span>

### <span data-ttu-id="0754b-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0754b-131">System.String</span></span>

### <span data-ttu-id="0754b-132">ServiceBus. a m/.</span><span class="sxs-lookup"><span data-stu-id="0754b-132">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="0754b-133">출력</span><span class="sxs-lookup"><span data-stu-id="0754b-133">OUTPUTS</span></span>

### <span data-ttu-id="0754b-134">ServiceBus. a m/.</span><span class="sxs-lookup"><span data-stu-id="0754b-134">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="0754b-135">상속자</span><span class="sxs-lookup"><span data-stu-id="0754b-135">NOTES</span></span>

## <span data-ttu-id="0754b-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0754b-136">RELATED LINKS</span></span>
