---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
ms.openlocfilehash: a2e2b27023e9af9f08db6446d6d2808402ca27cc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188484"
---
# <span data-ttu-id="44efa-101">Remove-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="44efa-101">Remove-AzEventGridSubscription</span></span>

## <span data-ttu-id="44efa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44efa-102">SYNOPSIS</span></span>
<span data-ttu-id="44efa-103">Azure Event Grid 이벤트 구독을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="44efa-103">Removes an Azure Event Grid event subscription.</span></span>

## <span data-ttu-id="44efa-104">구문</span><span class="sxs-lookup"><span data-stu-id="44efa-104">SYNTAX</span></span>

### <span data-ttu-id="44efa-105">ResourceGroupNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="44efa-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44efa-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="44efa-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44efa-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="44efa-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44efa-108">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="44efa-108">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44efa-109">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="44efa-109">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-EventSubscriptionName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44efa-110">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="44efa-110">TopicNameParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="44efa-111">DomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="44efa-111">DomainNameParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-DomainTopicName <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44efa-112">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="44efa-112">DomainEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44efa-113">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="44efa-113">DomainTopicEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44efa-114">설명</span><span class="sxs-lookup"><span data-stu-id="44efa-114">DESCRIPTION</span></span>
<span data-ttu-id="44efa-115">Azure Event Grid 토픽, 리소스, Azure 구독 또는 리소스 그룹에 대한 Azure Event Grid 이벤트 구독을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="44efa-115">Removes an Azure Event Grid event subscription for an Azure Event Grid topic, a resource, an Azure subscription or resource group.</span></span>

## <span data-ttu-id="44efa-116">예제</span><span class="sxs-lookup"><span data-stu-id="44efa-116">EXAMPLES</span></span>

### <span data-ttu-id="44efa-117">예제 1</span><span class="sxs-lookup"><span data-stu-id="44efa-117">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="44efa-118">리소스 그룹 \` \` \` \` \` MyResourceGroupName의 Azure Event Grid 토픽 Topic1에 대한 이벤트 구독 EventSubscription1을 \` 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="44efa-118">Removes the event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="44efa-119">예제 2</span><span class="sxs-lookup"><span data-stu-id="44efa-119">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="44efa-120">이벤트 구독 \` EventSubscription1을 리소스 그룹 \` \` MyResourceGroupName으로 \` 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="44efa-120">Removes the event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="44efa-121">예제 3</span><span class="sxs-lookup"><span data-stu-id="44efa-121">Example 3</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="44efa-122">이벤트 구독 \` EventSubscription1을 기본 \` Azure 구독으로 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="44efa-122">Removes the event subscription \`EventSubscription1\` to the default Azure subscription.</span></span>

### <span data-ttu-id="44efa-123">예제 4</span><span class="sxs-lookup"><span data-stu-id="44efa-123">Example 4</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="44efa-124">Event Hub 네임스페이스에 대한 이벤트 구독 \` EventSubscription1을 \` 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="44efa-124">Removes the event subscription \`EventSubscription1\` to an Event Hub namespace.</span></span>

### <span data-ttu-id="44efa-125">예제 5</span><span class="sxs-lookup"><span data-stu-id="44efa-125">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroup -TopicName Topic1 | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="44efa-126">Event Grid 토픽에 대한 이벤트 구독 \` \` EventSubscription1을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="44efa-126">Removes the event subscription \`EventSubscription1\` to an Event Grid Topic.</span></span>

## <span data-ttu-id="44efa-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="44efa-127">PARAMETERS</span></span>

### <span data-ttu-id="44efa-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44efa-128">-DefaultProfile</span></span>
<span data-ttu-id="44efa-129">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="44efa-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="44efa-130">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="44efa-130">-DomainInputObject</span></span>
<span data-ttu-id="44efa-131">EventGrid 도메인 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="44efa-131">EventGrid Domain object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomain
Parameter Sets: EventSubscriptionDomainInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44efa-132">-DomainName</span><span class="sxs-lookup"><span data-stu-id="44efa-132">-DomainName</span></span>
<span data-ttu-id="44efa-133">EventGrid 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="44efa-133">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44efa-134">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="44efa-134">-DomainTopicInputObject</span></span>
<span data-ttu-id="44efa-135">EventGrid 도메인 토픽 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="44efa-135">EventGrid Domain Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic
Parameter Sets: EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44efa-136">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="44efa-136">-DomainTopicName</span></span>
<span data-ttu-id="44efa-137">EventGrid 도메인 토픽 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="44efa-137">EventGrid domain topic name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44efa-138">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="44efa-138">-EventSubscriptionName</span></span>
<span data-ttu-id="44efa-139">제거해야 하는 이벤트 구독의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="44efa-139">Name of the event subscription that needs to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, TopicNameParameterSet, DomainNameParameterSet, DomainEventSubscriptionParameterSet, DomainTopicEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet, EventSubscriptionDomainInputObjectParameterSet, EventSubscriptionDomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44efa-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44efa-140">-InputObject</span></span>
<span data-ttu-id="44efa-141">EventGrid 토픽 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="44efa-141">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: EventSubscriptionCustomTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44efa-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="44efa-142">-PassThru</span></span>
<span data-ttu-id="44efa-143">제거 작업의 상태를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="44efa-143">Returns the status of the Remove operation.</span></span> <span data-ttu-id="44efa-144">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="44efa-144">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44efa-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44efa-145">-ResourceGroupName</span></span>
<span data-ttu-id="44efa-146">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="44efa-146">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet, DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44efa-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="44efa-147">-ResourceId</span></span>
<span data-ttu-id="44efa-148">이벤트 구독을 제거해야 하는 리소스의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="44efa-148">Identifier of the resource whose event subscription needs to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44efa-149">-TopicName</span><span class="sxs-lookup"><span data-stu-id="44efa-149">-TopicName</span></span>
<span data-ttu-id="44efa-150">Event Grid 토픽 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="44efa-150">Event Grid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="44efa-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="44efa-151">-Confirm</span></span>
<span data-ttu-id="44efa-152">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="44efa-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44efa-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44efa-153">-WhatIf</span></span>
<span data-ttu-id="44efa-154">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="44efa-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44efa-155">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="44efa-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44efa-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44efa-156">CommonParameters</span></span>
<span data-ttu-id="44efa-157">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="44efa-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44efa-158">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="44efa-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44efa-159">입력</span><span class="sxs-lookup"><span data-stu-id="44efa-159">INPUTS</span></span>

### <span data-ttu-id="44efa-160">System.String</span><span class="sxs-lookup"><span data-stu-id="44efa-160">System.String</span></span>

### <span data-ttu-id="44efa-161">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="44efa-161">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="44efa-162">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="44efa-162">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="44efa-163">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="44efa-163">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="44efa-164">출력</span><span class="sxs-lookup"><span data-stu-id="44efa-164">OUTPUTS</span></span>

### <span data-ttu-id="44efa-165">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="44efa-165">System.Boolean</span></span>

## <span data-ttu-id="44efa-166">참고 사항</span><span class="sxs-lookup"><span data-stu-id="44efa-166">NOTES</span></span>

## <span data-ttu-id="44efa-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="44efa-167">RELATED LINKS</span></span>
