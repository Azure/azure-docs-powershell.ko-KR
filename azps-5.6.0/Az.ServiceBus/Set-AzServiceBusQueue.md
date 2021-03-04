---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/set-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusQueue.md
ms.openlocfilehash: 3fdd10ea83efb68b33d6936a84d32e940df71e29
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981643"
---
# <span data-ttu-id="17210-101">Set-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="17210-101">Set-AzServiceBusQueue</span></span>

## <span data-ttu-id="17210-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17210-102">SYNOPSIS</span></span>
<span data-ttu-id="17210-103">지정된 Service Bus 네임스페이스에서 Service Bus 큐에 대한 설명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="17210-103">Updates the description of a Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="17210-104">구문</span><span class="sxs-lookup"><span data-stu-id="17210-104">SYNTAX</span></span>

```
Set-AzServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject] <PSQueueAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="17210-105">설명</span><span class="sxs-lookup"><span data-stu-id="17210-105">DESCRIPTION</span></span>
<span data-ttu-id="17210-106">**Set-AzServiceBusQueue** cmdlet은 지정된 Service Bus 네임스페이스에서 Service Bus 큐에 대한 설명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="17210-106">The **Set-AzServiceBusQueue** cmdlet updates the description for the Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="17210-107">예제</span><span class="sxs-lookup"><span data-stu-id="17210-107">EXAMPLES</span></span>

### <span data-ttu-id="17210-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="17210-108">Example 1</span></span>
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

<span data-ttu-id="17210-109">지정된 네임스페이스에서 새 설명으로 지정된 큐를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="17210-109">Updates the specified queue with a new description in the specified namespace.</span></span> <span data-ttu-id="17210-110">이 예제에서는 **DeadLetteringOnMessageExpiration** 속성을 **true로** 업데이트하고 **SupportOrdering을** true로 **업데이트합니다.**</span><span class="sxs-lookup"><span data-stu-id="17210-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **SupportOrdering** to **true**.</span></span>

## <span data-ttu-id="17210-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="17210-111">PARAMETERS</span></span>

### <span data-ttu-id="17210-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17210-112">-DefaultProfile</span></span>
<span data-ttu-id="17210-113">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="17210-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17210-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="17210-114">-InputObject</span></span>
<span data-ttu-id="17210-115">ServiceBus 정의입니다.</span><span class="sxs-lookup"><span data-stu-id="17210-115">ServiceBus definition.</span></span>

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

### <span data-ttu-id="17210-116">-Name</span><span class="sxs-lookup"><span data-stu-id="17210-116">-Name</span></span>
<span data-ttu-id="17210-117">큐 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="17210-117">Queue Name.</span></span>

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

### <span data-ttu-id="17210-118">-네임스페이스</span><span class="sxs-lookup"><span data-stu-id="17210-118">-Namespace</span></span>
<span data-ttu-id="17210-119">네임스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="17210-119">Namespace Name.</span></span>

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

### <span data-ttu-id="17210-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17210-120">-ResourceGroupName</span></span>
<span data-ttu-id="17210-121">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="17210-121">The name of the resource group</span></span>

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

### <span data-ttu-id="17210-122">-확인</span><span class="sxs-lookup"><span data-stu-id="17210-122">-Confirm</span></span>
<span data-ttu-id="17210-123">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="17210-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17210-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17210-124">-WhatIf</span></span>
<span data-ttu-id="17210-125">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="17210-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17210-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="17210-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17210-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17210-127">CommonParameters</span></span>
<span data-ttu-id="17210-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="17210-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17210-129">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="17210-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17210-130">입력</span><span class="sxs-lookup"><span data-stu-id="17210-130">INPUTS</span></span>

### <span data-ttu-id="17210-131">System.String</span><span class="sxs-lookup"><span data-stu-id="17210-131">System.String</span></span>

### <span data-ttu-id="17210-132">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="17210-132">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="17210-133">출력</span><span class="sxs-lookup"><span data-stu-id="17210-133">OUTPUTS</span></span>

### <span data-ttu-id="17210-134">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="17210-134">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="17210-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="17210-135">NOTES</span></span>

## <span data-ttu-id="17210-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="17210-136">RELATED LINKS</span></span>
