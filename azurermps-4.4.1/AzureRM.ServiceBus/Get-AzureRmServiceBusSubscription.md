---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusSubscription.md
ms.openlocfilehash: 0e0f6a824571ab529daa576e5f3f9a4cbff08264
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527299"
---
# <span data-ttu-id="920fb-101">Get-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="920fb-101">Get-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="920fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="920fb-102">SYNOPSIS</span></span>
<span data-ttu-id="920fb-103">지정 된 항목에 대 한 구독 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="920fb-103">Returns a subscription description for the specified topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="920fb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="920fb-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusSubscription -ResourceGroupName <String> -Namespace <String> -Topic <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="920fb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="920fb-105">DESCRIPTION</span></span>
<span data-ttu-id="920fb-106">**AzureRmServiceBusSubscription** cmdlet은 지정 된 Service Bus 항목에 대 한 구독 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="920fb-106">The **Get-AzureRmServiceBusSubscription** cmdlet returns a subscription description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="920fb-107">예제의</span><span class="sxs-lookup"><span data-stu-id="920fb-107">EXAMPLES</span></span>

### <span data-ttu-id="920fb-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="920fb-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="920fb-109">지정 된 Service Bus 항목에 대 한 구독 설명을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="920fb-109">Returns a subscription description for the specified Service Bus topic.</span></span>

## <span data-ttu-id="920fb-110">변수</span><span class="sxs-lookup"><span data-stu-id="920fb-110">PARAMETERS</span></span>

### <span data-ttu-id="920fb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="920fb-111">-DefaultProfile</span></span>
<span data-ttu-id="920fb-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="920fb-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="920fb-113">-이름</span><span class="sxs-lookup"><span data-stu-id="920fb-113">-Name</span></span>
<span data-ttu-id="920fb-114">구독 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="920fb-114">Subscription Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="920fb-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="920fb-115">-Namespace</span></span>
<span data-ttu-id="920fb-116">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="920fb-116">Namespace Name.</span></span>

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

### <span data-ttu-id="920fb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="920fb-117">-ResourceGroupName</span></span>
<span data-ttu-id="920fb-118">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="920fb-118">The name of the resource group</span></span>

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

### <span data-ttu-id="920fb-119">-주제</span><span class="sxs-lookup"><span data-stu-id="920fb-119">-Topic</span></span>
<span data-ttu-id="920fb-120">주제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="920fb-120">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="920fb-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="920fb-121">CommonParameters</span></span>
<span data-ttu-id="920fb-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="920fb-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="920fb-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="920fb-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="920fb-124">입력</span><span class="sxs-lookup"><span data-stu-id="920fb-124">INPUTS</span></span>

### <span data-ttu-id="920fb-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="920fb-125">-ResourceGroup</span></span>
 <span data-ttu-id="920fb-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="920fb-126">System.String</span></span>
 

### <span data-ttu-id="920fb-127">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="920fb-127">-NamespaceName</span></span>
 <span data-ttu-id="920fb-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="920fb-128">System.String</span></span>
 

### <span data-ttu-id="920fb-129">-TopicName</span><span class="sxs-lookup"><span data-stu-id="920fb-129">-TopicName</span></span>
 <span data-ttu-id="920fb-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="920fb-130">System.String</span></span>
 

### <span data-ttu-id="920fb-131">-SubscriptionName</span><span class="sxs-lookup"><span data-stu-id="920fb-131">-SubscriptionName</span></span>
 <span data-ttu-id="920fb-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="920fb-132">System.String</span></span>
 

## <span data-ttu-id="920fb-133">출력</span><span class="sxs-lookup"><span data-stu-id="920fb-133">OUTPUTS</span></span>

### <span data-ttu-id="920fb-134">ServiceBus/. i a m.</span><span class="sxs-lookup"><span data-stu-id="920fb-134">Microsoft.Azure.Commands.ServiceBus.Models.SubscriptionAttributes</span></span>
<span data-ttu-id="920fb-135">이름: SB-TopicSubscription-Example1 Location: 미국 US AccessedAt: 1/20/2017 3:18:54 AM AutoDeleteOnIdle: 10675199.02:48: MessageCountDetails CreatedAt: 1/20/2017 3:18:52 AM DefaultMessageTimeToLive: 10675199.02:48:05.4775807 DeadLetteringOnFilterEvaluationExceptions: True DeadLetteringOnMessageExpiration: 거짓 EnableBatchedOperations: true EntityAvailabilityStatus: False ServiceBus: 00:01:00 IsReadOnly: 10 MessageCount: 0 MaxDeliveryCount: False 상태: 활성 RequiresSession: 1/20/2017 3:18:54 AM</span><span class="sxs-lookup"><span data-stu-id="920fb-135">Name                                      : SB-TopicSubscription-Example1 Location                                  : West US AccessedAt                                : 1/20/2017 3:18:54 AM AutoDeleteOnIdle                          : 10675199.02:48:05.4775807 CountDetails                              : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails CreatedAt                                 : 1/20/2017 3:18:52 AM DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807 DeadLetteringOnFilterEvaluationExceptions : True DeadLetteringOnMessageExpiration          : False EnableBatchedOperations                   : True EntityAvailabilityStatus                  : Available IsReadOnly                                : LockDuration                              : 00:01:00 MaxDeliveryCount                          : 10 MessageCount                              : 0 RequiresSession                           : False Status                                    : Active UpdatedAt                                 : 1/20/2017 3:18:54 AM</span></span>

## <span data-ttu-id="920fb-136">상속자</span><span class="sxs-lookup"><span data-stu-id="920fb-136">NOTES</span></span>

## <span data-ttu-id="920fb-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="920fb-137">RELATED LINKS</span></span>

