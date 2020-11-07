---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusQueue.md
ms.openlocfilehash: 099e86e8ed085169823c40d51de376085f768753
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699197"
---
# <span data-ttu-id="07102-101">Get-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="07102-101">Get-AzServiceBusQueue</span></span>

## <span data-ttu-id="07102-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07102-102">SYNOPSIS</span></span>
<span data-ttu-id="07102-103">지정 된 Service Bus 큐에 대 한 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="07102-103">Returns a description for the specified Service Bus queue.</span></span>

## <span data-ttu-id="07102-104">구문과</span><span class="sxs-lookup"><span data-stu-id="07102-104">SYNTAX</span></span>

```
Get-AzServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07102-105">설명은</span><span class="sxs-lookup"><span data-stu-id="07102-105">DESCRIPTION</span></span>
<span data-ttu-id="07102-106">지정 된 Service Bus 큐에 대 한 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="07102-106">Returns a description for the specified Service Bus queue.</span></span>

## <span data-ttu-id="07102-107">예제의</span><span class="sxs-lookup"><span data-stu-id="07102-107">EXAMPLES</span></span>

### <span data-ttu-id="07102-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="07102-108">Example 1</span></span>
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

<span data-ttu-id="07102-109">큐에 대 한 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="07102-109">Returns the description of the queue.</span></span>

### <span data-ttu-id="07102-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="07102-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="07102-111">지정 된 네임 스페이스에 대 한 큐의 목록을 반환 합니다. 100 개 이상의 큐가 반환 되는 경우에는 기본적으로 100 큐가 반환 되 고,-MaxCount 매개 변수를 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="07102-111">Returns list of queues for given namespace, By default 100 queues will be returned, if more than 100 queues to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="07102-112">예제 3</span><span class="sxs-lookup"><span data-stu-id="07102-112">Example 3</span></span>
```
PS C:\> Get-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -MaxCount 150
```

<span data-ttu-id="07102-113">지정 된 네임 스페이스에 대 한 첫 번째 150 큐의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="07102-113">Returns list of first 150 queues for given namespace</span></span>

## <span data-ttu-id="07102-114">변수</span><span class="sxs-lookup"><span data-stu-id="07102-114">PARAMETERS</span></span>

### <span data-ttu-id="07102-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07102-115">-DefaultProfile</span></span>
<span data-ttu-id="07102-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="07102-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07102-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="07102-117">-MaxCount</span></span>
<span data-ttu-id="07102-118">반환할 최대 큐 수를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07102-118">Determine the maximum number of Queues to return.</span></span>

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

### <span data-ttu-id="07102-119">-이름</span><span class="sxs-lookup"><span data-stu-id="07102-119">-Name</span></span>
<span data-ttu-id="07102-120">큐 이름</span><span class="sxs-lookup"><span data-stu-id="07102-120">Queue Name</span></span>

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

### <span data-ttu-id="07102-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="07102-121">-Namespace</span></span>
<span data-ttu-id="07102-122">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="07102-122">Namespace Name</span></span>

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

### <span data-ttu-id="07102-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07102-123">-ResourceGroupName</span></span>
<span data-ttu-id="07102-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="07102-124">The name of the resource group</span></span>

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

### <span data-ttu-id="07102-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07102-125">CommonParameters</span></span>
<span data-ttu-id="07102-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="07102-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07102-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07102-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07102-128">입력</span><span class="sxs-lookup"><span data-stu-id="07102-128">INPUTS</span></span>

### <span data-ttu-id="07102-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="07102-129">System.String</span></span>

## <span data-ttu-id="07102-130">출력</span><span class="sxs-lookup"><span data-stu-id="07102-130">OUTPUTS</span></span>

### <span data-ttu-id="07102-131">ServiceBus. a m/.</span><span class="sxs-lookup"><span data-stu-id="07102-131">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="07102-132">상속자</span><span class="sxs-lookup"><span data-stu-id="07102-132">NOTES</span></span>

## <span data-ttu-id="07102-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="07102-133">RELATED LINKS</span></span>
