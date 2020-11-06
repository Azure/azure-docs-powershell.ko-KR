---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueue.md
ms.openlocfilehash: d90d93548e46f3586319b0acf96319fe24e298af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93536191"
---
# <span data-ttu-id="e1bc5-101">Get-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="e1bc5-101">Get-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="e1bc5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1bc5-102">SYNOPSIS</span></span>
<span data-ttu-id="e1bc5-103">지정 된 Service Bus 큐에 대 한 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1bc5-103">Returns a description for the specified Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1bc5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e1bc5-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusQueue -ResourceGroupName <String> -Namespace <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1bc5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e1bc5-105">DESCRIPTION</span></span>
<span data-ttu-id="e1bc5-106">**AzureRmServiceBusQueue** cmdlet은 지정 된 Service Bus 큐에 대 한 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1bc5-106">The **Get-AzureRmServiceBusQueue** cmdlet returns a description of the specified Service Bus queue.</span></span>

## <span data-ttu-id="e1bc5-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e1bc5-107">EXAMPLES</span></span>

### <span data-ttu-id="e1bc5-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e1bc5-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1
```

<span data-ttu-id="e1bc5-109">큐에 대 한 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1bc5-109">Returns the description of the queue.</span></span> 

## <span data-ttu-id="e1bc5-110">변수</span><span class="sxs-lookup"><span data-stu-id="e1bc5-110">PARAMETERS</span></span>

### <span data-ttu-id="e1bc5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1bc5-111">-DefaultProfile</span></span>
<span data-ttu-id="e1bc5-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e1bc5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1bc5-113">-이름</span><span class="sxs-lookup"><span data-stu-id="e1bc5-113">-Name</span></span>
<span data-ttu-id="e1bc5-114">큐 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e1bc5-114">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1bc5-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e1bc5-115">-Namespace</span></span>
<span data-ttu-id="e1bc5-116">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e1bc5-116">Namespace Name.</span></span>

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

### <span data-ttu-id="e1bc5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1bc5-117">-ResourceGroupName</span></span>
<span data-ttu-id="e1bc5-118">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e1bc5-118">The name of the resource group</span></span>

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

### <span data-ttu-id="e1bc5-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1bc5-119">CommonParameters</span></span>
<span data-ttu-id="e1bc5-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1bc5-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1bc5-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1bc5-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1bc5-122">입력</span><span class="sxs-lookup"><span data-stu-id="e1bc5-122">INPUTS</span></span>

### <span data-ttu-id="e1bc5-123">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="e1bc5-123">-ResourceGroup</span></span>
 <span data-ttu-id="e1bc5-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e1bc5-124">System.String</span></span>
 

### <span data-ttu-id="e1bc5-125">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="e1bc5-125">-NamespaceName</span></span>
 <span data-ttu-id="e1bc5-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e1bc5-126">System.String</span></span>
 

### <span data-ttu-id="e1bc5-127">-QueueName</span><span class="sxs-lookup"><span data-stu-id="e1bc5-127">-QueueName</span></span>
 <span data-ttu-id="e1bc5-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e1bc5-128">System.String</span></span> 

## <span data-ttu-id="e1bc5-129">출력</span><span class="sxs-lookup"><span data-stu-id="e1bc5-129">OUTPUTS</span></span>

### <span data-ttu-id="e1bc5-130">ServiceBus 특성이 있는 경우.</span><span class="sxs-lookup"><span data-stu-id="e1bc5-130">Microsoft.Azure.Commands.ServiceBus.Models.QueueAttributes</span></span>
<span data-ttu-id="e1bc5-131">LockDuration: AccessedAt: 1/1/0001 12:00:00 AM AutoDeleteOnIdle: 10675199.02:48:05.4775807 EntityAvailabilityStatus: CreatedAt: 1/20/2017 2:51:35 AM DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow: EnableBatchedOperations: True DeadLetteringOnMessageExpiration: False EnableExpress: False Enableexpress: True IsAnonymousAccessible: False MaxDeliveryCount: MaxSizeInMegabytes: 16384 MessageCount: RequiresDuplicateDetection: False RequiresSession: false SizeInBytes: Status: 활성 지원 순서: False UpdatedAt: 1/20/2017 2:51:37 AM Id:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/S B-Queue_example1 이름: SB-Queue_example1 유형: Microsoft의 ServiceBus/대기열 위치: 서쪽 미국</span><span class="sxs-lookup"><span data-stu-id="e1bc5-131">LockDuration                        : AccessedAt                          : 1/1/0001 12:00:00 AM AutoDeleteOnIdle                    : 10675199.02:48:05.4775807 EntityAvailabilityStatus            : CreatedAt                           : 1/20/2017 2:51:35 AM DefaultMessageTimeToLive            : 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow : EnableBatchedOperations             : True DeadLetteringOnMessageExpiration    : False EnableExpress                       : False EnablePartitioning                  : True IsAnonymousAccessible               : False MaxDeliveryCount                    : MaxSizeInMegabytes                  : 16384 MessageCount                        : CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails RequiresDuplicateDetection          : False RequiresSession                     : False SizeInBytes                         : Status                              : Active SupportOrdering                     : False UpdatedAt                           : 1/20/2017 2:51:37 AM Id                                  : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/S B-Queue_example1 Name                                : SB-Queue_example1 Type                                : Microsoft.ServiceBus/Queues Location                            : West US</span></span>

## <span data-ttu-id="e1bc5-132">상속자</span><span class="sxs-lookup"><span data-stu-id="e1bc5-132">NOTES</span></span>

## <span data-ttu-id="e1bc5-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e1bc5-133">RELATED LINKS</span></span>

