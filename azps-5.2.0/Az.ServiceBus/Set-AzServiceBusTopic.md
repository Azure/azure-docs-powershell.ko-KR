---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusTopic.md
ms.openlocfilehash: 8e8fe04476e66db6b45372879ac3176f9d492acc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360935"
---
# <span data-ttu-id="fc505-101">Set-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="fc505-101">Set-AzServiceBusTopic</span></span>

## <span data-ttu-id="fc505-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc505-102">SYNOPSIS</span></span>
<span data-ttu-id="fc505-103">지정된 Service Bus 네임스페이스에서 Service Bus 토픽에 대한 설명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="fc505-103">Updates the description of a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="fc505-104">구문</span><span class="sxs-lookup"><span data-stu-id="fc505-104">SYNTAX</span></span>

```
Set-AzServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject] <PSTopicAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fc505-105">설명</span><span class="sxs-lookup"><span data-stu-id="fc505-105">DESCRIPTION</span></span>
<span data-ttu-id="fc505-106">**Set-AzServiceBusTopic** cmdlet은 지정된 Service Bus 네임스페이스에서 Service Bus 토픽에 대한 설명 개체를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="fc505-106">The **Set-AzServiceBusTopic** cmdlet updates a description object for a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="fc505-107">예제</span><span class="sxs-lookup"><span data-stu-id="fc505-107">EXAMPLES</span></span>

### <span data-ttu-id="fc505-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="fc505-108">Example 1</span></span>
```
PS C:\> $topicObj = Get-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-ExampleStandard -TopicName SB-Topic_exampl1

PS C:\> $topicObj.EnableExpress = $True

PS C:\> Set-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-ExampleStandard -TopicName SB-Topic_exampl1 -TopicObj $topicObj

Name                                : SB-Topic_example1
Id                                  : /subscriptions/{subscriptionId}/resourceGroups/{ResourceGroupName}/providers/Microsoft.ServiceBus/namespaces/SB-ExampleStandard/topics/SB-Topic_example1
Type                                : Microsoft.ServiceBus/Namespaces/Topics
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : P10675199DT2H48M5.4775807S
CreatedAt                           : 10/12/2018 12:01:28 AM
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
DefaultMessageTimeToLive            : P10675199DT2H48M5.4775807S
DuplicateDetectionHistoryTimeWindow : PT10M
EnableBatchedOperations             : True
EnableExpress                       : False
EnablePartitioning                  : True
MaxSizeInMegabytes                  : 81920
RequiresDuplicateDetection          : False
SizeInBytes                         : 0
Status                              : Active
SubscriptionCount                   : 0
SupportOrdering                     : False
UpdatedAt                           : 10/12/2018 12:01:29 AM
```

<span data-ttu-id="fc505-109">지정된 네임스페이스에서 새 설명으로 지정된 토픽을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="fc505-109">Updates the specified topic with a new description in the specified namespace.</span></span> <span data-ttu-id="fc505-110">이 예제에서는 **EnableExpress 속성을 true로** **업데이트합니다.**</span><span class="sxs-lookup"><span data-stu-id="fc505-110">This example updates the **EnableExpress** property to **true**.</span></span> 

## <span data-ttu-id="fc505-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc505-111">PARAMETERS</span></span>

### <span data-ttu-id="fc505-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc505-112">-DefaultProfile</span></span>
<span data-ttu-id="fc505-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fc505-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc505-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc505-114">-InputObject</span></span>
<span data-ttu-id="fc505-115">ServiceBus 토픽 정의입니다.</span><span class="sxs-lookup"><span data-stu-id="fc505-115">ServiceBus Topic definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes
Parameter Sets: (All)
Aliases: TopicObj

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc505-116">-Name</span><span class="sxs-lookup"><span data-stu-id="fc505-116">-Name</span></span>
<span data-ttu-id="fc505-117">토픽 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fc505-117">Topic Name.</span></span>

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

### <span data-ttu-id="fc505-118">-Namespace</span><span class="sxs-lookup"><span data-stu-id="fc505-118">-Namespace</span></span>
<span data-ttu-id="fc505-119">네임스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fc505-119">Namespace Name.</span></span>

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

### <span data-ttu-id="fc505-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc505-120">-ResourceGroupName</span></span>
<span data-ttu-id="fc505-121">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="fc505-121">The name of the resource group</span></span>

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

### <span data-ttu-id="fc505-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fc505-122">-Confirm</span></span>
<span data-ttu-id="fc505-123">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fc505-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc505-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc505-124">-WhatIf</span></span>
<span data-ttu-id="fc505-125">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="fc505-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc505-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fc505-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc505-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc505-127">CommonParameters</span></span>
<span data-ttu-id="fc505-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fc505-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc505-129">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fc505-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc505-130">입력</span><span class="sxs-lookup"><span data-stu-id="fc505-130">INPUTS</span></span>

### <span data-ttu-id="fc505-131">System.String</span><span class="sxs-lookup"><span data-stu-id="fc505-131">System.String</span></span>

### <span data-ttu-id="fc505-132">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="fc505-132">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="fc505-133">출력</span><span class="sxs-lookup"><span data-stu-id="fc505-133">OUTPUTS</span></span>

### <span data-ttu-id="fc505-134">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="fc505-134">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="fc505-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fc505-135">NOTES</span></span>

## <span data-ttu-id="fc505-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fc505-136">RELATED LINKS</span></span>
