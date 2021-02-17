---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusQueue.md
ms.openlocfilehash: 367d5b9184e98b9559d0f2f09696c2cf9905a854
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178588"
---
# <span data-ttu-id="ec8e7-101">Get-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="ec8e7-101">Get-AzServiceBusQueue</span></span>

## <span data-ttu-id="ec8e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec8e7-102">SYNOPSIS</span></span>
<span data-ttu-id="ec8e7-103">지정된 Service Bus 큐에 대한 설명을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ec8e7-103">Returns a description for the specified Service Bus queue.</span></span>

## <span data-ttu-id="ec8e7-104">구문</span><span class="sxs-lookup"><span data-stu-id="ec8e7-104">SYNTAX</span></span>

```
Get-AzServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec8e7-105">설명</span><span class="sxs-lookup"><span data-stu-id="ec8e7-105">DESCRIPTION</span></span>
<span data-ttu-id="ec8e7-106">지정된 Service Bus 큐에 대한 설명을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ec8e7-106">Returns a description for the specified Service Bus queue.</span></span>

## <span data-ttu-id="ec8e7-107">예제</span><span class="sxs-lookup"><span data-stu-id="ec8e7-107">EXAMPLES</span></span>

### <span data-ttu-id="ec8e7-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ec8e7-108">Example 1</span></span>
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

<span data-ttu-id="ec8e7-109">큐에 대한 설명을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ec8e7-109">Returns the description of the queue.</span></span>

### <span data-ttu-id="ec8e7-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="ec8e7-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="ec8e7-111">주어진 네임스페이스에 대한 큐 목록을 반환합니다. 기본적으로 100개 이상의 큐가 반환됩니다. 100개 이상의 큐가 반환되는 경우 -MaxCount 매개 변수를 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="ec8e7-111">Returns list of queues for given namespace, By default 100 queues will be returned, if more than 100 queues to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="ec8e7-112">예제 3</span><span class="sxs-lookup"><span data-stu-id="ec8e7-112">Example 3</span></span>
```
PS C:\> Get-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -MaxCount 150
```

<span data-ttu-id="ec8e7-113">주어진 네임스페이스에 대한 처음 150개 큐 목록을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ec8e7-113">Returns list of first 150 queues for given namespace</span></span>

## <span data-ttu-id="ec8e7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ec8e7-114">PARAMETERS</span></span>

### <span data-ttu-id="ec8e7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec8e7-115">-DefaultProfile</span></span>
<span data-ttu-id="ec8e7-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ec8e7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec8e7-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="ec8e7-117">-MaxCount</span></span>
<span data-ttu-id="ec8e7-118">반환할 최대 큐 수를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec8e7-118">Determine the maximum number of Queues to return.</span></span>

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

### <span data-ttu-id="ec8e7-119">-Name</span><span class="sxs-lookup"><span data-stu-id="ec8e7-119">-Name</span></span>
<span data-ttu-id="ec8e7-120">큐 이름</span><span class="sxs-lookup"><span data-stu-id="ec8e7-120">Queue Name</span></span>

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

### <span data-ttu-id="ec8e7-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ec8e7-121">-Namespace</span></span>
<span data-ttu-id="ec8e7-122">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="ec8e7-122">Namespace Name</span></span>

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

### <span data-ttu-id="ec8e7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec8e7-123">-ResourceGroupName</span></span>
<span data-ttu-id="ec8e7-124">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="ec8e7-124">The name of the resource group</span></span>

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

### <span data-ttu-id="ec8e7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec8e7-125">CommonParameters</span></span>
<span data-ttu-id="ec8e7-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ec8e7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec8e7-127">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ec8e7-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec8e7-128">입력</span><span class="sxs-lookup"><span data-stu-id="ec8e7-128">INPUTS</span></span>

### <span data-ttu-id="ec8e7-129">System.String</span><span class="sxs-lookup"><span data-stu-id="ec8e7-129">System.String</span></span>

## <span data-ttu-id="ec8e7-130">출력</span><span class="sxs-lookup"><span data-stu-id="ec8e7-130">OUTPUTS</span></span>

### <span data-ttu-id="ec8e7-131">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="ec8e7-131">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="ec8e7-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ec8e7-132">NOTES</span></span>

## <span data-ttu-id="ec8e7-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ec8e7-133">RELATED LINKS</span></span>
