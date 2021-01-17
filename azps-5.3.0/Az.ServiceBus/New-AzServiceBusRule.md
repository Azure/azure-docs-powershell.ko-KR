---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusRule.md
ms.openlocfilehash: d667049fb512545aebfd9681b3ad3d9f44651951
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494861"
---
# <span data-ttu-id="38510-101">New-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="38510-101">New-AzServiceBusRule</span></span>

## <span data-ttu-id="38510-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38510-102">SYNOPSIS</span></span>
<span data-ttu-id="38510-103">주어진 토픽 구독에 대한 새 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="38510-103">Creates a new rule for a given Subscription of Topic.</span></span> 

## <span data-ttu-id="38510-104">구문</span><span class="sxs-lookup"><span data-stu-id="38510-104">SYNTAX</span></span>

### <span data-ttu-id="38510-105">RulePropertiesSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="38510-105">RulePropertiesSet (Default)</span></span>
```
New-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38510-106">RuleActionPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="38510-106">RuleActionPropertiesSet</span></span>
```
New-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [-Name] <String> [-SqlExpression] <String> -ActionSqlExpression <String>
 [-RequiresPreprocessing] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38510-107">설명</span><span class="sxs-lookup"><span data-stu-id="38510-107">DESCRIPTION</span></span>
<span data-ttu-id="38510-108">**New-AzServiceBusRule** cmdlet은 주어진 구독에 대한 새 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="38510-108">The **New-AzServiceBusRule** cmdlet Creates a new rule for given subscription.</span></span>

## <span data-ttu-id="38510-109">예제</span><span class="sxs-lookup"><span data-stu-id="38510-109">EXAMPLES</span></span>

### <span data-ttu-id="38510-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="38510-110">Example 1</span></span>
```
PS C:\> New-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'"
```

<span data-ttu-id="38510-111">New-AzServiceBusRule cmdlet은 지정된 구독에 대한 새 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="38510-111">The New-AzServiceBusRule cmdlet creates a new rule for the specified Subscription.</span></span>

### <span data-ttu-id="38510-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="38510-112">Example 2</span></span>
```
PS C:\> New-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule -SqlExpression "mysqlexpression='test'" -ActionSqlExpression "SET myAction='test'" -RequiresPreprocessing
```

<span data-ttu-id="38510-113">New-AzServiceBusRule cmdlet은 ActionFilter를 통해 지정된 구독에 대한 새 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="38510-113">The New-AzServiceBusRule cmdlet creates a new rule for the specified Subscription with ActionFilter.</span></span>

## <span data-ttu-id="38510-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38510-114">PARAMETERS</span></span>

### <span data-ttu-id="38510-115">-ActionSqlExpression</span><span class="sxs-lookup"><span data-stu-id="38510-115">-ActionSqlExpression</span></span>
<span data-ttu-id="38510-116">작업 SqlFilter 식</span><span class="sxs-lookup"><span data-stu-id="38510-116">Action SqlFilter Expression</span></span>

```yaml
Type: System.String
Parameter Sets: RuleActionPropertiesSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38510-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38510-117">-DefaultProfile</span></span>
<span data-ttu-id="38510-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="38510-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38510-119">-Name</span><span class="sxs-lookup"><span data-stu-id="38510-119">-Name</span></span>
<span data-ttu-id="38510-120">규칙 이름</span><span class="sxs-lookup"><span data-stu-id="38510-120">Rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38510-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="38510-121">-Namespace</span></span>
<span data-ttu-id="38510-122">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="38510-122">Namespace Name</span></span>

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

### <span data-ttu-id="38510-123">-RequiresPreprocessing</span><span class="sxs-lookup"><span data-stu-id="38510-123">-RequiresPreprocessing</span></span>
<span data-ttu-id="38510-124">전 처리가 필요한 작업</span><span class="sxs-lookup"><span data-stu-id="38510-124">Action Requires Preprocessing</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RuleActionPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38510-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38510-125">-ResourceGroupName</span></span>
<span data-ttu-id="38510-126">리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="38510-126">The name of the resource group</span></span>

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

### <span data-ttu-id="38510-127">-SqlExpression</span><span class="sxs-lookup"><span data-stu-id="38510-127">-SqlExpression</span></span>
<span data-ttu-id="38510-128">Sql 필터 식</span><span class="sxs-lookup"><span data-stu-id="38510-128">Sql Filter Expression</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38510-129">-Subscription</span><span class="sxs-lookup"><span data-stu-id="38510-129">-Subscription</span></span>
<span data-ttu-id="38510-130">구독 이름</span><span class="sxs-lookup"><span data-stu-id="38510-130">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38510-131">-Topic</span><span class="sxs-lookup"><span data-stu-id="38510-131">-Topic</span></span>
<span data-ttu-id="38510-132">토픽 이름</span><span class="sxs-lookup"><span data-stu-id="38510-132">Topic Name</span></span>

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

### <span data-ttu-id="38510-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38510-133">-Confirm</span></span>
<span data-ttu-id="38510-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="38510-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38510-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38510-135">-WhatIf</span></span>
<span data-ttu-id="38510-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="38510-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38510-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="38510-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38510-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38510-138">CommonParameters</span></span>
<span data-ttu-id="38510-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="38510-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38510-140">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="38510-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38510-141">입력</span><span class="sxs-lookup"><span data-stu-id="38510-141">INPUTS</span></span>

### <span data-ttu-id="38510-142">System.String</span><span class="sxs-lookup"><span data-stu-id="38510-142">System.String</span></span>

## <span data-ttu-id="38510-143">출력</span><span class="sxs-lookup"><span data-stu-id="38510-143">OUTPUTS</span></span>

### <span data-ttu-id="38510-144">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="38510-144">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="38510-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="38510-145">NOTES</span></span>

## <span data-ttu-id="38510-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="38510-146">RELATED LINKS</span></span>
