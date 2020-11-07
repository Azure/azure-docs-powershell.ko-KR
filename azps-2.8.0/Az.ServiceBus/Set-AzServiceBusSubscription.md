---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/set-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusSubscription.md
ms.openlocfilehash: d05a8bb98910a478790581b21a0f4ee7be710ea1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873094"
---
# <span data-ttu-id="2c5e6-101">Set-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="2c5e6-101">Set-AzServiceBusSubscription</span></span>

## <span data-ttu-id="2c5e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c5e6-102">SYNOPSIS</span></span>
<span data-ttu-id="2c5e6-103">지정 된 Service Bus 네임 스페이스의 Service Bus 항목에 대 한 구독 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c5e6-103">Updates a subscription description for a Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="2c5e6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2c5e6-104">SYNTAX</span></span>

```
Set-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-InputObject] <PSSubscriptionAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2c5e6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2c5e6-105">DESCRIPTION</span></span>
<span data-ttu-id="2c5e6-106">**AzServiceBusSubscription** cmdlet은 지정 된 service bus 네임 스페이스의 service bus 항목에 대 한 구독 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c5e6-106">The **Set-AzServiceBusSubscription** cmdlet updates the description of the subscription for the Service Bus topic in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="2c5e6-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2c5e6-107">EXAMPLES</span></span>

### <span data-ttu-id="2c5e6-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="2c5e6-108">Example 1</span></span>
```
PS C:\> $subscriptionObj = Get-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1

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
PS C:\> Set-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionObj $subscriptionObj
```

<span data-ttu-id="2c5e6-109">지정 된 구독에 대 한 설명을 지정 된 항목으로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c5e6-109">Updates the description for the specified subscription to the given topic.</span></span> <span data-ttu-id="2c5e6-110">이 예제에서는 **DeadLetteringOnMessageExpiration** 속성을 **true** 로 업데이트 하 고 **MaxDeliveryCount** 를 9로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c5e6-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **MaxDeliveryCount** to 9.</span></span>

## <span data-ttu-id="2c5e6-111">변수</span><span class="sxs-lookup"><span data-stu-id="2c5e6-111">PARAMETERS</span></span>

### <span data-ttu-id="2c5e6-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c5e6-112">-DefaultProfile</span></span>
<span data-ttu-id="2c5e6-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2c5e6-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c5e6-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2c5e6-114">-InputObject</span></span>
<span data-ttu-id="2c5e6-115">ServiceBus 구독 정의입니다.</span><span class="sxs-lookup"><span data-stu-id="2c5e6-115">ServiceBus Subscription definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes
Parameter Sets: (All)
Aliases: SubscriptionObj

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c5e6-116">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2c5e6-116">-Namespace</span></span>
<span data-ttu-id="2c5e6-117">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2c5e6-117">Namespace Name.</span></span>

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

### <span data-ttu-id="2c5e6-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c5e6-118">-ResourceGroupName</span></span>
<span data-ttu-id="2c5e6-119">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2c5e6-119">The name of the resource group</span></span>

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

### <span data-ttu-id="2c5e6-120">-주제</span><span class="sxs-lookup"><span data-stu-id="2c5e6-120">-Topic</span></span>
<span data-ttu-id="2c5e6-121">주제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2c5e6-121">Topic Name.</span></span>

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

### <span data-ttu-id="2c5e6-122">-확인</span><span class="sxs-lookup"><span data-stu-id="2c5e6-122">-Confirm</span></span>
<span data-ttu-id="2c5e6-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c5e6-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c5e6-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c5e6-124">-WhatIf</span></span>
<span data-ttu-id="2c5e6-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2c5e6-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c5e6-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2c5e6-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c5e6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c5e6-127">CommonParameters</span></span>
<span data-ttu-id="2c5e6-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c5e6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c5e6-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c5e6-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c5e6-130">입력</span><span class="sxs-lookup"><span data-stu-id="2c5e6-130">INPUTS</span></span>

### <span data-ttu-id="2c5e6-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2c5e6-131">System.String</span></span>

### <span data-ttu-id="2c5e6-132">ServiceBus-PSSubscriptionAttributes.</span><span class="sxs-lookup"><span data-stu-id="2c5e6-132">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="2c5e6-133">출력</span><span class="sxs-lookup"><span data-stu-id="2c5e6-133">OUTPUTS</span></span>

### <span data-ttu-id="2c5e6-134">ServiceBus-PSSubscriptionAttributes.</span><span class="sxs-lookup"><span data-stu-id="2c5e6-134">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="2c5e6-135">상속자</span><span class="sxs-lookup"><span data-stu-id="2c5e6-135">NOTES</span></span>

## <span data-ttu-id="2c5e6-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2c5e6-136">RELATED LINKS</span></span>
