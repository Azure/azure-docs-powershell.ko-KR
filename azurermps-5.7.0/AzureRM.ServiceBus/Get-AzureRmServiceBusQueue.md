---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueue.md
ms.openlocfilehash: 967bc5c3126a0976096b6c9d9b6b76af8f0ef43e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528803"
---
# <span data-ttu-id="75fee-101">Get-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="75fee-101">Get-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="75fee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="75fee-102">SYNOPSIS</span></span>
<span data-ttu-id="75fee-103">지정 된 Service Bus 큐에 대 한 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="75fee-103">Returns a description for the specified Service Bus queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75fee-104">구문과</span><span class="sxs-lookup"><span data-stu-id="75fee-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75fee-105">설명은</span><span class="sxs-lookup"><span data-stu-id="75fee-105">DESCRIPTION</span></span>
<span data-ttu-id="75fee-106">**AzureRmServiceBusQueue** cmdlet은 지정 된 Service Bus 큐에 대 한 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="75fee-106">The **Get-AzureRmServiceBusQueue** cmdlet returns a description of the specified Service Bus queue.</span></span>

## <span data-ttu-id="75fee-107">예제의</span><span class="sxs-lookup"><span data-stu-id="75fee-107">EXAMPLES</span></span>

### <span data-ttu-id="75fee-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="75fee-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_example1

LockDuration                        : 
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : 10675199.02:48:05.4775807
CreatedAt                           : 1/20/2017 2:51:35 AM
DefaultMessageTimeToLive            : 10675199.02:48:05.4775807
DuplicateDetectionHistoryTimeWindow : 
DeadLetteringOnMessageExpiration    : False
EnableExpress                       : False
EnablePartitioning                  : True
MaxDeliveryCount                    : 
MaxSizeInMegabytes                  : 16384
MessageCount                        : 
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
RequiresDuplicateDetection          : False
RequiresSession                     : False
SizeInBytes                         : 
Status                              : Active
UpdatedAt                           : 1/20/2017 2:51:37 AM
Id                                  : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/S
                                      B-Queue_example1
Name                                : SB-Queue_example1
Type                                : Microsoft.ServiceBus/Queues

```

<span data-ttu-id="75fee-109">큐에 대 한 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="75fee-109">Returns the description of the queue.</span></span>

## <span data-ttu-id="75fee-110">변수</span><span class="sxs-lookup"><span data-stu-id="75fee-110">PARAMETERS</span></span>

### <span data-ttu-id="75fee-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75fee-111">-DefaultProfile</span></span>
<span data-ttu-id="75fee-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="75fee-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75fee-113">-이름</span><span class="sxs-lookup"><span data-stu-id="75fee-113">-Name</span></span>
<span data-ttu-id="75fee-114">큐 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="75fee-114">Queue Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueueName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="75fee-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="75fee-115">-Namespace</span></span>
<span data-ttu-id="75fee-116">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="75fee-116">Namespace Name.</span></span>

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

### <span data-ttu-id="75fee-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75fee-117">-ResourceGroupName</span></span>
<span data-ttu-id="75fee-118">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="75fee-118">The name of the resource group</span></span>

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

### <span data-ttu-id="75fee-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75fee-119">CommonParameters</span></span>
<span data-ttu-id="75fee-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="75fee-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75fee-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75fee-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75fee-122">입력</span><span class="sxs-lookup"><span data-stu-id="75fee-122">INPUTS</span></span>

### <span data-ttu-id="75fee-123">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="75fee-123">-ResourceGroup</span></span>
 <span data-ttu-id="75fee-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="75fee-124">System.String</span></span>
 

### <span data-ttu-id="75fee-125">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="75fee-125">-NamespaceName</span></span>
 <span data-ttu-id="75fee-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="75fee-126">System.String</span></span>
 

### <span data-ttu-id="75fee-127">-QueueName</span><span class="sxs-lookup"><span data-stu-id="75fee-127">-QueueName</span></span>
 <span data-ttu-id="75fee-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="75fee-128">System.String</span></span> 

## <span data-ttu-id="75fee-129">출력</span><span class="sxs-lookup"><span data-stu-id="75fee-129">OUTPUTS</span></span>

### <span data-ttu-id="75fee-130">ServiceBus. a m/.</span><span class="sxs-lookup"><span data-stu-id="75fee-130">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="75fee-131">상속자</span><span class="sxs-lookup"><span data-stu-id="75fee-131">NOTES</span></span>

## <span data-ttu-id="75fee-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="75fee-132">RELATED LINKS</span></span>

