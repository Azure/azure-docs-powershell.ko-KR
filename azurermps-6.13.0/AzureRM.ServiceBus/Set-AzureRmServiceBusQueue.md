---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueue.md
ms.openlocfilehash: 8c02c596b1b1eecb8654b07a2392d2336c0b0215
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702446"
---
# <span data-ttu-id="ec943-101">Set-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="ec943-101">Set-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="ec943-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec943-102">SYNOPSIS</span></span>
<span data-ttu-id="ec943-103">지정 된 Service Bus 네임 스페이스의 Service Bus 큐에 대 한 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec943-103">Updates the description of a Service Bus queue in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec943-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ec943-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject] <PSQueueAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ec943-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ec943-105">DESCRIPTION</span></span>
<span data-ttu-id="ec943-106">**Set-AzureRmServiceBusQueue** cmdlet은 지정 된 service bus 네임 스페이스의 service bus 큐에 대 한 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec943-106">The **Set-AzureRmServiceBusQueue** cmdlet updates the description for the Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="ec943-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ec943-107">EXAMPLES</span></span>

### <span data-ttu-id="ec943-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ec943-108">Example 1</span></span>
```
PS C:\> $QueueObj = Get-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1

PS C:\> $QueueObj.DeadLetteringOnMessageExpiration = $True
PS C:\> $QueueObj.SupportOrdering = $True

PS C:\> Set-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1 -QueueObj $QueueObj

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

<span data-ttu-id="ec943-109">지정한 네임 스페이스의 새 설명으로 지정 된 큐를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec943-109">Updates the specified queue with a new description in the specified namespace.</span></span> <span data-ttu-id="ec943-110">이 예제에서는 **DeadLetteringOnMessageExpiration** 속성을 **True** 로, **supportordering** 를 **true** 로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec943-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **SupportOrdering** to **true**.</span></span>

## <span data-ttu-id="ec943-111">변수</span><span class="sxs-lookup"><span data-stu-id="ec943-111">PARAMETERS</span></span>

### <span data-ttu-id="ec943-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec943-112">-DefaultProfile</span></span>
<span data-ttu-id="ec943-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ec943-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec943-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ec943-114">-InputObject</span></span>
<span data-ttu-id="ec943-115">ServiceBus 정의.</span><span class="sxs-lookup"><span data-stu-id="ec943-115">ServiceBus definition.</span></span>

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

### <span data-ttu-id="ec943-116">-이름</span><span class="sxs-lookup"><span data-stu-id="ec943-116">-Name</span></span>
<span data-ttu-id="ec943-117">큐 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ec943-117">Queue Name.</span></span>

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

### <span data-ttu-id="ec943-118">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ec943-118">-Namespace</span></span>
<span data-ttu-id="ec943-119">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ec943-119">Namespace Name.</span></span>

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

### <span data-ttu-id="ec943-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec943-120">-ResourceGroupName</span></span>
<span data-ttu-id="ec943-121">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ec943-121">The name of the resource group</span></span>

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

### <span data-ttu-id="ec943-122">-확인</span><span class="sxs-lookup"><span data-stu-id="ec943-122">-Confirm</span></span>
<span data-ttu-id="ec943-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec943-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec943-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec943-124">-WhatIf</span></span>
<span data-ttu-id="ec943-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ec943-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec943-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ec943-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec943-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec943-127">CommonParameters</span></span>
<span data-ttu-id="ec943-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec943-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec943-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec943-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec943-130">입력</span><span class="sxs-lookup"><span data-stu-id="ec943-130">INPUTS</span></span>

### <span data-ttu-id="ec943-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ec943-131">System.String</span></span>

### <span data-ttu-id="ec943-132">ServiceBus. a m/.</span><span class="sxs-lookup"><span data-stu-id="ec943-132">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="ec943-133">출력</span><span class="sxs-lookup"><span data-stu-id="ec943-133">OUTPUTS</span></span>

### <span data-ttu-id="ec943-134">ServiceBus. a m/.</span><span class="sxs-lookup"><span data-stu-id="ec943-134">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="ec943-135">상속자</span><span class="sxs-lookup"><span data-stu-id="ec943-135">NOTES</span></span>

## <span data-ttu-id="ec943-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ec943-136">RELATED LINKS</span></span>
