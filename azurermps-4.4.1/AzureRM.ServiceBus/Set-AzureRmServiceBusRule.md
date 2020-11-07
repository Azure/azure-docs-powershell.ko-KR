---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusRule.md
ms.openlocfilehash: 4fb10e2bb438cbc4f40936f9f9ead5c0bb36d861
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711233"
---
# <span data-ttu-id="eeadd-101">Set-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="eeadd-101">Set-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="eeadd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eeadd-102">SYNOPSIS</span></span>
<span data-ttu-id="eeadd-103">지정 된 구독에 대해 지정 된 규칙 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="eeadd-103">Updates the specified rule description for the given subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eeadd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="eeadd-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-InputObject] <RulesAttributes>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eeadd-105">설명은</span><span class="sxs-lookup"><span data-stu-id="eeadd-105">DESCRIPTION</span></span>
<span data-ttu-id="eeadd-106">**Set-AzureRmServiceBusRule** cmdlet은 지정 된 구독에 대 한 지정 된 규칙에 대 한 설명을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="eeadd-106">The **Set-AzureRmServiceBusRule** cmdlet updates the description for the specified rule of the given subscription.</span></span>

## <span data-ttu-id="eeadd-107">예제의</span><span class="sxs-lookup"><span data-stu-id="eeadd-107">EXAMPLES</span></span>

### <span data-ttu-id="eeadd-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="eeadd-108">Example 1</span></span>
```
PS C:\> $getRule = Get-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
PS C:\> $getRule.SqlFilter.SqlExpression = "mysqlexpression='condition'"
PS C:\> $setRule = Set-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -InputObject $getRule
```

<span data-ttu-id="eeadd-109">항목의 구독 규칙에 대 한 sqlexpression **mysqlexpression = ' condition '** 을 업데이트 합니다. `SBEule` `SBSubscription``SBTopic`</span><span class="sxs-lookup"><span data-stu-id="eeadd-109">updates the sqlexpression **mysqlexpression='condition'** of the rule `SBEule` of the subscription `SBSubscription` in Topic `SBTopic`</span></span>

## <span data-ttu-id="eeadd-110">변수</span><span class="sxs-lookup"><span data-stu-id="eeadd-110">PARAMETERS</span></span>

### <span data-ttu-id="eeadd-111">-확인</span><span class="sxs-lookup"><span data-stu-id="eeadd-111">-Confirm</span></span>
<span data-ttu-id="eeadd-112">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="eeadd-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eeadd-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eeadd-113">-InputObject</span></span>
<span data-ttu-id="eeadd-114">ServiceBus 규칙 정의.</span><span class="sxs-lookup"><span data-stu-id="eeadd-114">ServiceBus Rules definition.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.RulesAttributes
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eeadd-115">-이름</span><span class="sxs-lookup"><span data-stu-id="eeadd-115">-Name</span></span>
<span data-ttu-id="eeadd-116">규칙 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eeadd-116">Rule Name.</span></span>

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

### <span data-ttu-id="eeadd-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="eeadd-117">-Namespace</span></span>
<span data-ttu-id="eeadd-118">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eeadd-118">Namespace Name.</span></span>

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

### <span data-ttu-id="eeadd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eeadd-119">-ResourceGroupName</span></span>
<span data-ttu-id="eeadd-120">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eeadd-120">The name of the resource group</span></span>

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

### <span data-ttu-id="eeadd-121">-구독</span><span class="sxs-lookup"><span data-stu-id="eeadd-121">-Subscription</span></span>
<span data-ttu-id="eeadd-122">구독 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eeadd-122">Subscription Name.</span></span>

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

### <span data-ttu-id="eeadd-123">-주제</span><span class="sxs-lookup"><span data-stu-id="eeadd-123">-Topic</span></span>
<span data-ttu-id="eeadd-124">주제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eeadd-124">Topic Name.</span></span>

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

### <span data-ttu-id="eeadd-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eeadd-125">-WhatIf</span></span>
<span data-ttu-id="eeadd-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="eeadd-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eeadd-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eeadd-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eeadd-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eeadd-128">-DefaultProfile</span></span>
<span data-ttu-id="eeadd-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="eeadd-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="eeadd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eeadd-130">CommonParameters</span></span>
<span data-ttu-id="eeadd-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="eeadd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eeadd-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eeadd-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eeadd-133">입력</span><span class="sxs-lookup"><span data-stu-id="eeadd-133">INPUTS</span></span>

### <span data-ttu-id="eeadd-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="eeadd-134">System.String</span></span>
<span data-ttu-id="eeadd-135">ServiceBus.-\*.</span><span class="sxs-lookup"><span data-stu-id="eeadd-135">Microsoft.Azure.Commands.ServiceBus.Models.RulesAttributes</span></span>

## <span data-ttu-id="eeadd-136">출력</span><span class="sxs-lookup"><span data-stu-id="eeadd-136">OUTPUTS</span></span>

### <span data-ttu-id="eeadd-137">ServiceBus.-\*.</span><span class="sxs-lookup"><span data-stu-id="eeadd-137">Microsoft.Azure.Commands.ServiceBus.Models.RulesAttributes</span></span>

## <span data-ttu-id="eeadd-138">상속자</span><span class="sxs-lookup"><span data-stu-id="eeadd-138">NOTES</span></span>

## <span data-ttu-id="eeadd-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eeadd-139">RELATED LINKS</span></span>

