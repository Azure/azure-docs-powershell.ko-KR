---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusSubscription.md
ms.openlocfilehash: a2a535dd9607b3018b7fe215f152bbeeb01b8858
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341265"
---
# <span data-ttu-id="ccd27-101">Get-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="ccd27-101">Get-AzServiceBusSubscription</span></span>

## <span data-ttu-id="ccd27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ccd27-102">SYNOPSIS</span></span>
<span data-ttu-id="ccd27-103">지정된 토픽에 대한 구독 설명을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd27-103">Returns a subscription description for the specified topic.</span></span>

## <span data-ttu-id="ccd27-104">구문</span><span class="sxs-lookup"><span data-stu-id="ccd27-104">SYNTAX</span></span>

```
Get-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ccd27-105">설명</span><span class="sxs-lookup"><span data-stu-id="ccd27-105">DESCRIPTION</span></span>
<span data-ttu-id="ccd27-106">**Get-AzServiceBusSubscription** cmdlet은 지정된 Service Bus 항목에 대한 구독 설명을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd27-106">The **Get-AzServiceBusSubscription** cmdlet returns a subscription description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="ccd27-107">예제</span><span class="sxs-lookup"><span data-stu-id="ccd27-107">EXAMPLES</span></span>

### <span data-ttu-id="ccd27-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ccd27-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

Name                                      : SB-TopicSubscription-Example1
AccessedAt                                : 1/20/2017 3:18:54 AM
AutoDeleteOnIdle                          : 10675199.02:48:05.4775807
CountDetails                              : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
CreatedAt                                 : 1/20/2017 3:18:52 AM
DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807
DeadLetteringOnMessageExpiration          : False
EnableBatchedOperations                   : True
LockDuration                              : 00:01:00
MaxDeliveryCount                          : 10
MessageCount                              : 0
RequiresSession                           : False
Status                                    : Active
UpdatedAt                                 : 1/20/2017 3:18:54 AM
```

<span data-ttu-id="ccd27-109">지정된 Service Bus 항목에 대한 구독 설명을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd27-109">Returns a subscription description for the specified Service Bus topic.</span></span>

### <span data-ttu-id="ccd27-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="ccd27-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="ccd27-111">지정된 Service Bus 토픽에 대한 구독 목록을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd27-111">Returns list of subscriptions for specified Service Bus topic.</span></span> <span data-ttu-id="ccd27-112">기본적으로 100개 구독이 반환됩니다. 구독 수에 대해 -MaxCount 매개 변수를 사용하세요.</span><span class="sxs-lookup"><span data-stu-id="ccd27-112">By default 100 subscriptions will be returned, for number of subscriptions please use -MaxCount Parameter</span></span>

### <span data-ttu-id="ccd27-113">예제 3</span><span class="sxs-lookup"><span data-stu-id="ccd27-113">Example 3</span></span>
```
PS C:\> Get-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -MaxCount 150
```

<span data-ttu-id="ccd27-114">지정된 Service Bus 토픽에 대한 처음 150개 구독 목록을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd27-114">Returns list of first 150 subscriptions for specified Service Bus topic.</span></span>

## <span data-ttu-id="ccd27-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ccd27-115">PARAMETERS</span></span>

### <span data-ttu-id="ccd27-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccd27-116">-DefaultProfile</span></span>
<span data-ttu-id="ccd27-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ccd27-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ccd27-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="ccd27-118">-MaxCount</span></span>
<span data-ttu-id="ccd27-119">반환할 구독의 최대 수를 결정하세요.</span><span class="sxs-lookup"><span data-stu-id="ccd27-119">Determine the maximum number of Subscriptions to return.</span></span>

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

### <span data-ttu-id="ccd27-120">-Name</span><span class="sxs-lookup"><span data-stu-id="ccd27-120">-Name</span></span>
<span data-ttu-id="ccd27-121">구독 이름</span><span class="sxs-lookup"><span data-stu-id="ccd27-121">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccd27-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ccd27-122">-Namespace</span></span>
<span data-ttu-id="ccd27-123">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="ccd27-123">Namespace Name</span></span>

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

### <span data-ttu-id="ccd27-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccd27-124">-ResourceGroupName</span></span>
<span data-ttu-id="ccd27-125">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="ccd27-125">The name of the resource group</span></span>

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

### <span data-ttu-id="ccd27-126">-Topic</span><span class="sxs-lookup"><span data-stu-id="ccd27-126">-Topic</span></span>
<span data-ttu-id="ccd27-127">토픽 이름</span><span class="sxs-lookup"><span data-stu-id="ccd27-127">Topic Name</span></span>

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

### <span data-ttu-id="ccd27-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccd27-128">CommonParameters</span></span>
<span data-ttu-id="ccd27-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ccd27-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccd27-130">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ccd27-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccd27-131">입력</span><span class="sxs-lookup"><span data-stu-id="ccd27-131">INPUTS</span></span>

### <span data-ttu-id="ccd27-132">System.String</span><span class="sxs-lookup"><span data-stu-id="ccd27-132">System.String</span></span>

## <span data-ttu-id="ccd27-133">출력</span><span class="sxs-lookup"><span data-stu-id="ccd27-133">OUTPUTS</span></span>

### <span data-ttu-id="ccd27-134">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="ccd27-134">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="ccd27-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ccd27-135">NOTES</span></span>

## <span data-ttu-id="ccd27-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ccd27-136">RELATED LINKS</span></span>
