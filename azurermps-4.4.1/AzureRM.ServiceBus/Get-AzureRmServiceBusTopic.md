---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopic.md
ms.openlocfilehash: 273a8ec4bcbf5ffcc7619d3fe663d6256e4851d7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527291"
---
# <span data-ttu-id="ac23d-101">Get-AzureRmServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="ac23d-101">Get-AzureRmServiceBusTopic</span></span>

## <span data-ttu-id="ac23d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac23d-102">SYNOPSIS</span></span>
<span data-ttu-id="ac23d-103">지정 된 Service Bus 항목에 대 한 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac23d-103">Returns a description for the specified Service Bus topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac23d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ac23d-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusTopic -ResourceGroupName <String> -Namespace <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac23d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ac23d-105">DESCRIPTION</span></span>
<span data-ttu-id="ac23d-106">**AzureRmServiceBusTopic** cmdlet은 지정 된 Service Bus 네임 스페이스에 대 한 항목 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac23d-106">The **Get-AzureRmServiceBusTopic** cmdlet returns a topic description for the specified Service Bus namespace.</span></span>

## <span data-ttu-id="ac23d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ac23d-107">EXAMPLES</span></span>

### <span data-ttu-id="ac23d-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ac23d-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="ac23d-109">지정 된 Service Bus 네임 스페이스에 대 한 지정 된 항목의 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac23d-109">Returns the description of the specified topic for the given Service Bus namespace.</span></span>

## <span data-ttu-id="ac23d-110">변수</span><span class="sxs-lookup"><span data-stu-id="ac23d-110">PARAMETERS</span></span>

### <span data-ttu-id="ac23d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac23d-111">-DefaultProfile</span></span>
<span data-ttu-id="ac23d-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ac23d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac23d-113">-이름</span><span class="sxs-lookup"><span data-stu-id="ac23d-113">-Name</span></span>
<span data-ttu-id="ac23d-114">주제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ac23d-114">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac23d-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ac23d-115">-Namespace</span></span>
<span data-ttu-id="ac23d-116">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ac23d-116">Namespace Name.</span></span>

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

### <span data-ttu-id="ac23d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac23d-117">-ResourceGroupName</span></span>
<span data-ttu-id="ac23d-118">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ac23d-118">The name of the resource group</span></span>

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

### <span data-ttu-id="ac23d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac23d-119">CommonParameters</span></span>
<span data-ttu-id="ac23d-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ac23d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac23d-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac23d-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac23d-122">입력</span><span class="sxs-lookup"><span data-stu-id="ac23d-122">INPUTS</span></span>

### <span data-ttu-id="ac23d-123">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ac23d-123">-ResourceGroup</span></span>
 <span data-ttu-id="ac23d-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ac23d-124">System.String</span></span>
 

### <span data-ttu-id="ac23d-125">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="ac23d-125">-NamespaceName</span></span>
 <span data-ttu-id="ac23d-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ac23d-126">System.String</span></span>
 

### <span data-ttu-id="ac23d-127">-TopicName</span><span class="sxs-lookup"><span data-stu-id="ac23d-127">-TopicName</span></span>
 <span data-ttu-id="ac23d-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ac23d-128">System.String</span></span>

## <span data-ttu-id="ac23d-129">출력</span><span class="sxs-lookup"><span data-stu-id="ac23d-129">OUTPUTS</span></span>

### <span data-ttu-id="ac23d-130">ServiceBus. TopicAttributes/.</span><span class="sxs-lookup"><span data-stu-id="ac23d-130">Microsoft.Azure.Commands.ServiceBus.Models.TopicAttributes</span></span>
<span data-ttu-id="ac23d-131">이름: SB-Topic_exampl1 위치: 서쪽 미국 Id:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/S B-Topic_exampl1 Type: Microsoft ServiceBus/Topic AccessedAt: 1/20/2017 3:18:54 AM AutoDeleteOnIdle: 10675199.02:48:05.4775807 EntityAvailabilityStatus: CreatedAt: 1/20/2017 3:16:41 AM CountDetails: ServiceBus MessageCountDetails DefaultMessageTimeToLive: 10675199.02:05.4775807 DuplicateDetectionHistoryTimeWindow: EnableBatchedOperations: True EnableExpress: False Enableexpress: True EnableSubscriptionPartitioning: false FilteringMessagesBeforePublishing: False IsAnonymousAccessible: false IsExpress: false MaxSizeInMegabytes: 16384 RequiresDuplicateDetection: False SizeInBytes: 0 상태: 활성 구독 수: False UpdatedAt: 1/20/2017 3:16:43 AM</span><span class="sxs-lookup"><span data-stu-id="ac23d-131">Name                                : SB-Topic_exampl1 Location                            : West US Id                                  : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/S B-Topic_exampl1 Type                                : Microsoft.ServiceBus/Topic AccessedAt                          : 1/20/2017 3:18:54 AM AutoDeleteOnIdle                    : 10675199.02:48:05.4775807 EntityAvailabilityStatus            : CreatedAt                           : 1/20/2017 3:16:41 AM CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails DefaultMessageTimeToLive            : 10675199.02:48:05.4775807 DuplicateDetectionHistoryTimeWindow : EnableBatchedOperations             : True EnableExpress                       : False EnablePartitioning                  : True EnableSubscriptionPartitioning      : False FilteringMessagesBeforePublishing   : False IsAnonymousAccessible               : False IsExpress                           : False MaxSizeInMegabytes                  : 16384 RequiresDuplicateDetection          : False SizeInBytes                         : 0 Status                              : Active SubscriptionCount                   : 1 SupportOrdering                     : False UpdatedAt                           : 1/20/2017 3:16:43 AM</span></span>

## <span data-ttu-id="ac23d-132">상속자</span><span class="sxs-lookup"><span data-stu-id="ac23d-132">NOTES</span></span>

## <span data-ttu-id="ac23d-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ac23d-133">RELATED LINKS</span></span>

