---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/set-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Set-AzServiceBusRule.md
ms.openlocfilehash: 2caf2ccfe0d3428515812aa2dfeafc1237f820f5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981595"
---
# <span data-ttu-id="b0475-101">Set-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="b0475-101">Set-AzServiceBusRule</span></span>

## <span data-ttu-id="b0475-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0475-102">SYNOPSIS</span></span>
<span data-ttu-id="b0475-103">지정된 구독에 대해 지정된 규칙 설명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="b0475-103">Updates the specified rule description for the given subscription.</span></span>

## <span data-ttu-id="b0475-104">구문</span><span class="sxs-lookup"><span data-stu-id="b0475-104">SYNTAX</span></span>

```
Set-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-InputObject] <PSRulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0475-105">설명</span><span class="sxs-lookup"><span data-stu-id="b0475-105">DESCRIPTION</span></span>
<span data-ttu-id="b0475-106">**Set-AzServiceBusRule** cmdlet은 지정된 구독의 지정된 규칙에 대한 설명을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="b0475-106">The **Set-AzServiceBusRule** cmdlet updates the description for the specified rule of the given subscription.</span></span>

## <span data-ttu-id="b0475-107">예제</span><span class="sxs-lookup"><span data-stu-id="b0475-107">EXAMPLES</span></span>

### <span data-ttu-id="b0475-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b0475-108">Example 1</span></span>
```
PS C:\> $getRule = Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
PS C:\> $getRule.SqlFilter.SqlExpression = "mysqlexpression='condition'"
PS C:\> $setRule = Set-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -InputObject $getRule
```

<span data-ttu-id="b0475-109">토픽의 구독 규칙의 sql 식 **mysqlexpression='condition'** `SBRule` `SBSubscription` 업데이트 `SBTopic`</span><span class="sxs-lookup"><span data-stu-id="b0475-109">Updates the sql expression **mysqlexpression='condition'** of the rule `SBRule` of the subscription `SBSubscription` in Topic `SBTopic`</span></span>

## <span data-ttu-id="b0475-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b0475-110">PARAMETERS</span></span>

### <span data-ttu-id="b0475-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0475-111">-DefaultProfile</span></span>
<span data-ttu-id="b0475-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b0475-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0475-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0475-113">-InputObject</span></span>
<span data-ttu-id="b0475-114">ServiceBus 규칙 정의입니다.</span><span class="sxs-lookup"><span data-stu-id="b0475-114">ServiceBus Rules definition.</span></span>

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

### <span data-ttu-id="b0475-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b0475-115">-Name</span></span>
<span data-ttu-id="b0475-116">규칙 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0475-116">Rule Name.</span></span>

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

### <span data-ttu-id="b0475-117">-네임스페이스</span><span class="sxs-lookup"><span data-stu-id="b0475-117">-Namespace</span></span>
<span data-ttu-id="b0475-118">네임스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0475-118">Namespace Name.</span></span>

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

### <span data-ttu-id="b0475-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0475-119">-ResourceGroupName</span></span>
<span data-ttu-id="b0475-120">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="b0475-120">The name of the resource group</span></span>

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

### <span data-ttu-id="b0475-121">-Subscription</span><span class="sxs-lookup"><span data-stu-id="b0475-121">-Subscription</span></span>
<span data-ttu-id="b0475-122">구독 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0475-122">Subscription Name.</span></span>

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

### <span data-ttu-id="b0475-123">-Topic</span><span class="sxs-lookup"><span data-stu-id="b0475-123">-Topic</span></span>
<span data-ttu-id="b0475-124">토픽 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b0475-124">Topic Name.</span></span>

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

### <span data-ttu-id="b0475-125">-확인</span><span class="sxs-lookup"><span data-stu-id="b0475-125">-Confirm</span></span>
<span data-ttu-id="b0475-126">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b0475-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0475-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0475-127">-WhatIf</span></span>
<span data-ttu-id="b0475-128">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="b0475-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0475-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b0475-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0475-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0475-130">CommonParameters</span></span>
<span data-ttu-id="b0475-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b0475-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0475-132">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b0475-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0475-133">입력</span><span class="sxs-lookup"><span data-stu-id="b0475-133">INPUTS</span></span>

### <span data-ttu-id="b0475-134">System.String</span><span class="sxs-lookup"><span data-stu-id="b0475-134">System.String</span></span>

### <span data-ttu-id="b0475-135">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="b0475-135">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="b0475-136">출력</span><span class="sxs-lookup"><span data-stu-id="b0475-136">OUTPUTS</span></span>

### <span data-ttu-id="b0475-137">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="b0475-137">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="b0475-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b0475-138">NOTES</span></span>

## <span data-ttu-id="b0475-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b0475-139">RELATED LINKS</span></span>
