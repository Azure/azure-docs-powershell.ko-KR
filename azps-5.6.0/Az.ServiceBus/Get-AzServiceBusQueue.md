---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/get-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusQueue.md
ms.openlocfilehash: 6236fc36980226900182dcc673c320052ba6b2bd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993379"
---
# <span data-ttu-id="327f8-101">Get-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="327f8-101">Get-AzServiceBusQueue</span></span>

## <span data-ttu-id="327f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="327f8-102">SYNOPSIS</span></span>
<span data-ttu-id="327f8-103">지정된 Service Bus 큐에 대한 설명을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="327f8-103">Returns a description for the specified Service Bus queue.</span></span>

## <span data-ttu-id="327f8-104">구문</span><span class="sxs-lookup"><span data-stu-id="327f8-104">SYNTAX</span></span>

```
Get-AzServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="327f8-105">설명</span><span class="sxs-lookup"><span data-stu-id="327f8-105">DESCRIPTION</span></span>
<span data-ttu-id="327f8-106">지정된 Service Bus 큐에 대한 설명을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="327f8-106">Returns a description for the specified Service Bus queue.</span></span>

## <span data-ttu-id="327f8-107">예제</span><span class="sxs-lookup"><span data-stu-id="327f8-107">EXAMPLES</span></span>

### <span data-ttu-id="327f8-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="327f8-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1

Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_example1
Name                                : SB-Queue_example1
LockDuration                        : PT1M
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 10/11/2018 12:37:11 AM
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
DeadLetteringOnMessageExpiration    : False
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
UpdatedAt                           : 10/11/2018 12:37:11 AM
ForwardTo                           :
ForwardDeadLetteredMessagesTo       :
EnableBatchedOperations             : False
```

<span data-ttu-id="327f8-109">큐에 대한 설명을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="327f8-109">Returns the description of the queue.</span></span>

### <span data-ttu-id="327f8-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="327f8-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="327f8-111">주어진 네임스페이스에 대한 큐 목록을 반환합니다. 기본적으로 100개 이상의 큐가 반환되는 경우 -MaxCount 매개 변수를 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="327f8-111">Returns list of queues for given namespace, By default 100 queues will be returned, if more than 100 queues to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="327f8-112">예제 3</span><span class="sxs-lookup"><span data-stu-id="327f8-112">Example 3</span></span>
```
PS C:\> Get-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -MaxCount 150
```

<span data-ttu-id="327f8-113">주어진 네임스페이스에 대한 처음 150개 큐 목록을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="327f8-113">Returns list of first 150 queues for given namespace</span></span>

## <span data-ttu-id="327f8-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="327f8-114">PARAMETERS</span></span>

### <span data-ttu-id="327f8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="327f8-115">-DefaultProfile</span></span>
<span data-ttu-id="327f8-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="327f8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="327f8-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="327f8-117">-MaxCount</span></span>
<span data-ttu-id="327f8-118">반환할 최대 큐 수를 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="327f8-118">Determine the maximum number of Queues to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="327f8-119">-Name</span><span class="sxs-lookup"><span data-stu-id="327f8-119">-Name</span></span>
<span data-ttu-id="327f8-120">큐 이름</span><span class="sxs-lookup"><span data-stu-id="327f8-120">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="327f8-121">-네임스페이스</span><span class="sxs-lookup"><span data-stu-id="327f8-121">-Namespace</span></span>
<span data-ttu-id="327f8-122">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="327f8-122">Namespace Name</span></span>

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

### <span data-ttu-id="327f8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="327f8-123">-ResourceGroupName</span></span>
<span data-ttu-id="327f8-124">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="327f8-124">The name of the resource group</span></span>

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

### <span data-ttu-id="327f8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="327f8-125">CommonParameters</span></span>
<span data-ttu-id="327f8-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="327f8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="327f8-127">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="327f8-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="327f8-128">입력</span><span class="sxs-lookup"><span data-stu-id="327f8-128">INPUTS</span></span>

### <span data-ttu-id="327f8-129">System.String</span><span class="sxs-lookup"><span data-stu-id="327f8-129">System.String</span></span>

## <span data-ttu-id="327f8-130">출력</span><span class="sxs-lookup"><span data-stu-id="327f8-130">OUTPUTS</span></span>

### <span data-ttu-id="327f8-131">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="327f8-131">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="327f8-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="327f8-132">NOTES</span></span>

## <span data-ttu-id="327f8-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="327f8-133">RELATED LINKS</span></span>
