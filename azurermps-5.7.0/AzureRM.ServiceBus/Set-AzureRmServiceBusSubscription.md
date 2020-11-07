---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusSubscription.md
ms.openlocfilehash: 6bb5b6e8ea96f0852747c00ac4ef5ac11208e630
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702355"
---
# <span data-ttu-id="032ad-101">Set-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="032ad-101">Set-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="032ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="032ad-102">SYNOPSIS</span></span>
<span data-ttu-id="032ad-103">지정 된 Service Bus 네임 스페이스의 Service Bus 항목에 대 한 구독 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="032ad-103">Updates a subscription description for a Service Bus topic in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="032ad-104">구문과</span><span class="sxs-lookup"><span data-stu-id="032ad-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-InputObject] <SubscriptionAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="032ad-105">설명은</span><span class="sxs-lookup"><span data-stu-id="032ad-105">DESCRIPTION</span></span>
<span data-ttu-id="032ad-106">**AzureRmServiceBusSubscription** cmdlet은 지정 된 service bus 네임 스페이스의 service bus 항목에 대 한 구독 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="032ad-106">The **Set-AzureRmServiceBusSubscription** cmdlet updates the description of the subscription for the Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="032ad-107">예제의</span><span class="sxs-lookup"><span data-stu-id="032ad-107">EXAMPLES</span></span>

### <span data-ttu-id="032ad-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="032ad-108">Example 1</span></span>
```
PS C:\> $subscriptionObj = Get-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

PS C:\> $subscriptionObj.DeadLetteringOnMessageExpiration = $True
PS C:\> $subscriptionObj.MaxDeliveryCount = 9

Name                                      : SB-TopicSubscription-Example1
AccessedAt                                : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                          : 10675199.02:48:05.4775807
CountDetails                              : 
CreatedAt                                 : 1/20/2017 9:59:15 PM
DefaultMessageTimeToLive                  : 10675199.02:48:05.4775807
DeadLetteringOnMessageExpiration          : True
EnableBatchedOperations                   : True
LockDuration                              : 00:01:00
MaxDeliveryCount                          : 9
MessageCount                              : 0
RequiresSession                           : False
Status                                    : Active
UpdatedAt                                 : 1/20/2017 9:59:15 PM
PS C:\> Set-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionObj $subscriptionObj
```

<span data-ttu-id="032ad-109">지정 된 구독에 대 한 설명을 지정 된 항목으로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="032ad-109">Updates the description for the specified subscription to the given topic.</span></span> <span data-ttu-id="032ad-110">이 예제에서는 **DeadLetteringOnMessageExpiration** 속성을 **true** 로 업데이트 하 고 **MaxDeliveryCount** 를 9로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="032ad-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **MaxDeliveryCount** to 9.</span></span>

## <span data-ttu-id="032ad-111">변수</span><span class="sxs-lookup"><span data-stu-id="032ad-111">PARAMETERS</span></span>

### <span data-ttu-id="032ad-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="032ad-112">-DefaultProfile</span></span>
<span data-ttu-id="032ad-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="032ad-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="032ad-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="032ad-114">-InputObject</span></span>
<span data-ttu-id="032ad-115">ServiceBus 구독 정의입니다.</span><span class="sxs-lookup"><span data-stu-id="032ad-115">ServiceBus Subscription definition.</span></span>

```yaml
Type: PSSubscriptionAttributes
Parameter Sets: (All)
Aliases: SubscriptionObj

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="032ad-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="032ad-116">-Namespace</span></span>
<span data-ttu-id="032ad-117">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="032ad-117">Namespace Name.</span></span>

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

### <span data-ttu-id="032ad-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="032ad-118">-ResourceGroupName</span></span>
<span data-ttu-id="032ad-119">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="032ad-119">The name of the resource group</span></span>

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

### <span data-ttu-id="032ad-120">-주제</span><span class="sxs-lookup"><span data-stu-id="032ad-120">-Topic</span></span>
<span data-ttu-id="032ad-121">주제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="032ad-121">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="032ad-122">-확인</span><span class="sxs-lookup"><span data-stu-id="032ad-122">-Confirm</span></span>
<span data-ttu-id="032ad-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="032ad-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="032ad-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="032ad-124">-WhatIf</span></span>
<span data-ttu-id="032ad-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="032ad-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="032ad-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="032ad-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="032ad-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="032ad-127">CommonParameters</span></span>
<span data-ttu-id="032ad-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="032ad-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="032ad-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="032ad-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="032ad-130">입력</span><span class="sxs-lookup"><span data-stu-id="032ad-130">INPUTS</span></span>

### <span data-ttu-id="032ad-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="032ad-131">-ResourceGroup</span></span>
 <span data-ttu-id="032ad-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="032ad-132">System.String</span></span>

### <span data-ttu-id="032ad-133">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="032ad-133">-NamespaceName</span></span>
 <span data-ttu-id="032ad-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="032ad-134">System.String</span></span>

### <span data-ttu-id="032ad-135">-TopicName</span><span class="sxs-lookup"><span data-stu-id="032ad-135">-TopicName</span></span>
 <span data-ttu-id="032ad-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="032ad-136">System.String</span></span>

### <span data-ttu-id="032ad-137">-SubscriptionObj</span><span class="sxs-lookup"><span data-stu-id="032ad-137">-SubscriptionObj</span></span>
 <span data-ttu-id="032ad-138">ServiceBus-PSSubscriptionAttributes.</span><span class="sxs-lookup"><span data-stu-id="032ad-138">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="032ad-139">출력</span><span class="sxs-lookup"><span data-stu-id="032ad-139">OUTPUTS</span></span>

### <span data-ttu-id="032ad-140">ServiceBus-PSSubscriptionAttributes.</span><span class="sxs-lookup"><span data-stu-id="032ad-140">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="032ad-141">상속자</span><span class="sxs-lookup"><span data-stu-id="032ad-141">NOTES</span></span>

## <span data-ttu-id="032ad-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="032ad-142">RELATED LINKS</span></span>

