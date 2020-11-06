---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusRule.md
ms.openlocfilehash: cb6200156b68524119df86e24d812b97bcd250e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530063"
---
# <span data-ttu-id="74737-101">Set-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="74737-101">Set-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="74737-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74737-102">SYNOPSIS</span></span>
<span data-ttu-id="74737-103">지정 된 구독에 대해 지정 된 규칙 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="74737-103">Updates the specified rule description for the given subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="74737-104">구문과</span><span class="sxs-lookup"><span data-stu-id="74737-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-InputObject] <PSRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="74737-105">설명은</span><span class="sxs-lookup"><span data-stu-id="74737-105">DESCRIPTION</span></span>
<span data-ttu-id="74737-106">**Set-AzureRmServiceBusRule** cmdlet은 지정 된 구독에 대 한 지정 된 규칙에 대 한 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="74737-106">The **Set-AzureRmServiceBusRule** cmdlet updates the description for the specified rule of the given subscription.</span></span>

## <span data-ttu-id="74737-107">예제의</span><span class="sxs-lookup"><span data-stu-id="74737-107">EXAMPLES</span></span>

### <span data-ttu-id="74737-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="74737-108">Example 1</span></span>
```
PS C:\> $getRule = Get-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
PS C:\> $getRule.SqlFilter.SqlExpression = "mysqlexpression='condition'"
PS C:\> $setRule = Set-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -InputObject $getRule
```

<span data-ttu-id="74737-109">항목의 구독 규칙에 대 한 sqlexpression **mysqlexpression = ' condition '** 을 업데이트 합니다. `SBEule` `SBSubscription``SBTopic`</span><span class="sxs-lookup"><span data-stu-id="74737-109">updates the sqlexpression **mysqlexpression='condition'** of the rule `SBEule` of the subscription `SBSubscription` in Topic `SBTopic`</span></span>

## <span data-ttu-id="74737-110">변수</span><span class="sxs-lookup"><span data-stu-id="74737-110">PARAMETERS</span></span>

### <span data-ttu-id="74737-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74737-111">-DefaultProfile</span></span>
<span data-ttu-id="74737-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="74737-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74737-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74737-113">-InputObject</span></span>
<span data-ttu-id="74737-114">ServiceBus 규칙 정의.</span><span class="sxs-lookup"><span data-stu-id="74737-114">ServiceBus Rules definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="74737-115">-이름</span><span class="sxs-lookup"><span data-stu-id="74737-115">-Name</span></span>
<span data-ttu-id="74737-116">규칙 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="74737-116">Rule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74737-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="74737-117">-Namespace</span></span>
<span data-ttu-id="74737-118">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="74737-118">Namespace Name.</span></span>

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

### <span data-ttu-id="74737-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74737-119">-ResourceGroupName</span></span>
<span data-ttu-id="74737-120">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="74737-120">The name of the resource group</span></span>

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

### <span data-ttu-id="74737-121">-구독</span><span class="sxs-lookup"><span data-stu-id="74737-121">-Subscription</span></span>
<span data-ttu-id="74737-122">구독 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="74737-122">Subscription Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74737-123">-주제</span><span class="sxs-lookup"><span data-stu-id="74737-123">-Topic</span></span>
<span data-ttu-id="74737-124">주제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="74737-124">Topic Name.</span></span>

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

### <span data-ttu-id="74737-125">-확인</span><span class="sxs-lookup"><span data-stu-id="74737-125">-Confirm</span></span>
<span data-ttu-id="74737-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="74737-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74737-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74737-127">-WhatIf</span></span>
<span data-ttu-id="74737-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="74737-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74737-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="74737-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="74737-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74737-130">CommonParameters</span></span>
<span data-ttu-id="74737-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="74737-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74737-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74737-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74737-133">입력</span><span class="sxs-lookup"><span data-stu-id="74737-133">INPUTS</span></span>

### <span data-ttu-id="74737-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="74737-134">System.String</span></span>

### <span data-ttu-id="74737-135">ServiceBus. Ps규칙 특성을</span><span class="sxs-lookup"><span data-stu-id="74737-135">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="74737-136">출력</span><span class="sxs-lookup"><span data-stu-id="74737-136">OUTPUTS</span></span>

### <span data-ttu-id="74737-137">ServiceBus. Ps규칙 특성을</span><span class="sxs-lookup"><span data-stu-id="74737-137">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="74737-138">상속자</span><span class="sxs-lookup"><span data-stu-id="74737-138">NOTES</span></span>

## <span data-ttu-id="74737-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="74737-139">RELATED LINKS</span></span>
