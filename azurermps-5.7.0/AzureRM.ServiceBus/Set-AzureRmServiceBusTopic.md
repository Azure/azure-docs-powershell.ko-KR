---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusTopic.md
ms.openlocfilehash: 92c26b2b92257de7cdd3bbbb0d602d45d8ea1d1c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528799"
---
# <span data-ttu-id="c66c5-101">Set-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="c66c5-101">Set-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="c66c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c66c5-102">SYNOPSIS</span></span>
<span data-ttu-id="c66c5-103">지정 된 Service Bus 네임 스페이스의 Service Bus 항목에 대 한 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c66c5-103">Updates the description of a Service Bus topic in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c66c5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c66c5-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject] <TopicAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c66c5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c66c5-105">DESCRIPTION</span></span>
<span data-ttu-id="c66c5-106">**AzureRmServiceBusTopic** cmdlet은 지정 된 service bus 네임 스페이스의 service bus 항목에 대 한 description 개체를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c66c5-106">The **Set-AzureRmServiceBusTopic** cmdlet updates a description object for a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="c66c5-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c66c5-107">EXAMPLES</span></span>

### <span data-ttu-id="c66c5-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="c66c5-108">Example 1</span></span>
```
PS C:\> $topicObj = Get-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1

PS C:\> $topicObj.EnableExpress = $True

PS C:\> Set-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -TopicObj $topicObj

Name                                : SB-Topic_exampl1
Id                                  : /subscriptions/{subscription id}d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-
                                      Topic_exampl1
Type                                : Microsoft.ServiceBus/Topic
AccessedAt                          : 1/20/2017 3:18:54 AM
AutoDeleteOnIdle                    : 10675199.02:48:05.4775807
CreatedAt                           : 1/20/2017 3:16:41 AM
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
DefaultMessageTimeToLive            : 10675199.02:48:05.4775807
DuplicateDetectionHistoryTimeWindow : 
EnableBatchedOperations             : True
EnableExpress                       : True
EnablePartitioning                  : True
MaxSizeInMegabytes                  : 16384
RequiresDuplicateDetection          : False
SizeInBytes                         : 0
Status                              : Active
SubscriptionCount                   : 1
SupportOrdering                     : False
UpdatedAt                           : 1/20/2017 7:12:16 PM
```
<span data-ttu-id="c66c5-109">지정 된 네임 스페이스에 대 한 새 설명으로 지정한 항목을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c66c5-109">Updates the specified topic with a new description in the specified namespace.</span></span> <span data-ttu-id="c66c5-110">이 예제에서는 **Enableexpress** 속성을 **true** 로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c66c5-110">This example updates the **EnableExpress** property to **true**.</span></span> 

## <span data-ttu-id="c66c5-111">변수</span><span class="sxs-lookup"><span data-stu-id="c66c5-111">PARAMETERS</span></span>

### <span data-ttu-id="c66c5-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c66c5-112">-DefaultProfile</span></span>
<span data-ttu-id="c66c5-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c66c5-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c66c5-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c66c5-114">-InputObject</span></span>
<span data-ttu-id="c66c5-115">ServiceBus 주제 정의.</span><span class="sxs-lookup"><span data-stu-id="c66c5-115">ServiceBus Topic definition.</span></span>

```yaml
Type: PSTopicAttributes
Parameter Sets: (All)
Aliases: TopicObj

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c66c5-116">-이름</span><span class="sxs-lookup"><span data-stu-id="c66c5-116">-Name</span></span>
<span data-ttu-id="c66c5-117">주제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c66c5-117">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c66c5-118">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c66c5-118">-Namespace</span></span>
<span data-ttu-id="c66c5-119">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c66c5-119">Namespace Name.</span></span>

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

### <span data-ttu-id="c66c5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c66c5-120">-ResourceGroupName</span></span>
<span data-ttu-id="c66c5-121">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c66c5-121">The name of the resource group</span></span>

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

### <span data-ttu-id="c66c5-122">-확인</span><span class="sxs-lookup"><span data-stu-id="c66c5-122">-Confirm</span></span>
<span data-ttu-id="c66c5-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c66c5-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c66c5-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c66c5-124">-WhatIf</span></span>
<span data-ttu-id="c66c5-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c66c5-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c66c5-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c66c5-126">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c66c5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c66c5-127">CommonParameters</span></span>
<span data-ttu-id="c66c5-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c66c5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c66c5-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c66c5-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c66c5-130">입력</span><span class="sxs-lookup"><span data-stu-id="c66c5-130">INPUTS</span></span>

### <span data-ttu-id="c66c5-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c66c5-131">-ResourceGroup</span></span>
 <span data-ttu-id="c66c5-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c66c5-132">System.String</span></span>

### <span data-ttu-id="c66c5-133">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="c66c5-133">-NamespaceName</span></span>
 <span data-ttu-id="c66c5-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c66c5-134">System.String</span></span>

### <span data-ttu-id="c66c5-135">-TopicName</span><span class="sxs-lookup"><span data-stu-id="c66c5-135">-TopicName</span></span>
 <span data-ttu-id="c66c5-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c66c5-136">System.String</span></span>

### <span data-ttu-id="c66c5-137">-TopicObj</span><span class="sxs-lookup"><span data-stu-id="c66c5-137">-TopicObj</span></span>
 <span data-ttu-id="c66c5-138">ServiceBus. a. m/.Ppstop특성</span><span class="sxs-lookup"><span data-stu-id="c66c5-138">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="c66c5-139">출력</span><span class="sxs-lookup"><span data-stu-id="c66c5-139">OUTPUTS</span></span>

### <span data-ttu-id="c66c5-140">ServiceBus. a. m/.Ppstop특성</span><span class="sxs-lookup"><span data-stu-id="c66c5-140">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="c66c5-141">상속자</span><span class="sxs-lookup"><span data-stu-id="c66c5-141">NOTES</span></span>

## <span data-ttu-id="c66c5-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c66c5-142">RELATED LINKS</span></span>

