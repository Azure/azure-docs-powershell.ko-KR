---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
ms.openlocfilehash: a2e2b27023e9af9f08db6446d6d2808402ca27cc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218700"
---
# <span data-ttu-id="19768-101">Remove-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="19768-101">Remove-AzEventGridSubscription</span></span>

## <span data-ttu-id="19768-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19768-102">SYNOPSIS</span></span>
<span data-ttu-id="19768-103">Azure 이벤트 그리드 이벤트 구독을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="19768-103">Removes an Azure Event Grid event subscription.</span></span>

## <span data-ttu-id="19768-104">구문과</span><span class="sxs-lookup"><span data-stu-id="19768-104">SYNTAX</span></span>

### <span data-ttu-id="19768-105">ResourceGroupNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="19768-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19768-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="19768-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19768-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="19768-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19768-108">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="19768-108">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19768-109">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="19768-109">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-EventSubscriptionName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19768-110">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="19768-110">TopicNameParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="19768-111">DomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="19768-111">DomainNameParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-DomainTopicName <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19768-112">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="19768-112">DomainEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19768-113">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="19768-113">DomainTopicEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19768-114">설명은</span><span class="sxs-lookup"><span data-stu-id="19768-114">DESCRIPTION</span></span>
<span data-ttu-id="19768-115">Azure 이벤트 그리드 항목, 리소스, Azure 구독 또는 리소스 그룹에 대 한 Azure 이벤트 그리드 이벤트 구독을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="19768-115">Removes an Azure Event Grid event subscription for an Azure Event Grid topic, a resource, an Azure subscription or resource group.</span></span>

## <span data-ttu-id="19768-116">예제의</span><span class="sxs-lookup"><span data-stu-id="19768-116">EXAMPLES</span></span>

### <span data-ttu-id="19768-117">예제 1</span><span class="sxs-lookup"><span data-stu-id="19768-117">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="19768-118">\` \` \` 리소스 그룹 MyResourceGroupName의 Azure 이벤트 그리드 항목 Topic1에 대 한 이벤트 구독 EventSubscription1를 제거 \` \` \` 합니다.</span><span class="sxs-lookup"><span data-stu-id="19768-118">Removes the event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="19768-119">예제 2</span><span class="sxs-lookup"><span data-stu-id="19768-119">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="19768-120">\` \` 리소스 그룹 MyResourceGroupName에 대 한 이벤트 구독 EventSubscription1를 제거 합니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="19768-120">Removes the event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="19768-121">예제 3</span><span class="sxs-lookup"><span data-stu-id="19768-121">Example 3</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="19768-122">\` \` 기본 Azure 구독에 대 한 이벤트 구독 EventSubscription1를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="19768-122">Removes the event subscription \`EventSubscription1\` to the default Azure subscription.</span></span>

### <span data-ttu-id="19768-123">예제 4</span><span class="sxs-lookup"><span data-stu-id="19768-123">Example 4</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="19768-124">이벤트 플랜 \` EventSubscription1 \` 이벤트 허브 네임 스페이스에 대 한 구독을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="19768-124">Removes the event subscription \`EventSubscription1\` to an Event Hub namespace.</span></span>

### <span data-ttu-id="19768-125">예제 5</span><span class="sxs-lookup"><span data-stu-id="19768-125">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroup -TopicName Topic1 | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="19768-126">이벤트 \` \` 눈금 항목에 대 한 이벤트 구독 EventSubscription1를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="19768-126">Removes the event subscription \`EventSubscription1\` to an Event Grid Topic.</span></span>

## <span data-ttu-id="19768-127">변수</span><span class="sxs-lookup"><span data-stu-id="19768-127">PARAMETERS</span></span>

### <span data-ttu-id="19768-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19768-128">-DefaultProfile</span></span>
<span data-ttu-id="19768-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="19768-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19768-130">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="19768-130">-DomainInputObject</span></span>
<span data-ttu-id="19768-131">EventGrid 도메인 개체.</span><span class="sxs-lookup"><span data-stu-id="19768-131">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="19768-132">-DomainName</span><span class="sxs-lookup"><span data-stu-id="19768-132">-DomainName</span></span>
<span data-ttu-id="19768-133">EventGrid 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="19768-133">EventGrid domain name.</span></span>

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

### <span data-ttu-id="19768-134">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="19768-134">-DomainTopicInputObject</span></span>
<span data-ttu-id="19768-135">EventGrid 도메인 주제 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="19768-135">EventGrid Domain Topic object.</span></span>

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

### <span data-ttu-id="19768-136">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="19768-136">-DomainTopicName</span></span>
<span data-ttu-id="19768-137">EventGrid 도메인 주제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="19768-137">EventGrid domain topic name.</span></span>

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

### <span data-ttu-id="19768-138">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="19768-138">-EventSubscriptionName</span></span>
<span data-ttu-id="19768-139">제거 해야 하는 이벤트 구독의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="19768-139">Name of the event subscription that needs to be removed.</span></span>

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

### <span data-ttu-id="19768-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="19768-140">-InputObject</span></span>
<span data-ttu-id="19768-141">EventGrid 주제 개체</span><span class="sxs-lookup"><span data-stu-id="19768-141">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="19768-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="19768-142">-PassThru</span></span>
<span data-ttu-id="19768-143">제거 작업의 상태를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="19768-143">Returns the status of the Remove operation.</span></span> <span data-ttu-id="19768-144">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="19768-144">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="19768-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19768-145">-ResourceGroupName</span></span>
<span data-ttu-id="19768-146">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="19768-146">Resource Group Name.</span></span>

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

### <span data-ttu-id="19768-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="19768-147">-ResourceId</span></span>
<span data-ttu-id="19768-148">이벤트 구독을 제거 해야 하는 리소스의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="19768-148">Identifier of the resource whose event subscription needs to be removed.</span></span>

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

### <span data-ttu-id="19768-149">-TopicName</span><span class="sxs-lookup"><span data-stu-id="19768-149">-TopicName</span></span>
<span data-ttu-id="19768-150">이벤트 그리드 주제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="19768-150">Event Grid Topic Name.</span></span>

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

### <span data-ttu-id="19768-151">-확인</span><span class="sxs-lookup"><span data-stu-id="19768-151">-Confirm</span></span>
<span data-ttu-id="19768-152">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="19768-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19768-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19768-153">-WhatIf</span></span>
<span data-ttu-id="19768-154">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="19768-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19768-155">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="19768-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19768-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19768-156">CommonParameters</span></span>
<span data-ttu-id="19768-157">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="19768-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19768-158">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="19768-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19768-159">입력</span><span class="sxs-lookup"><span data-stu-id="19768-159">INPUTS</span></span>

### <span data-ttu-id="19768-160">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="19768-160">System.String</span></span>

### <span data-ttu-id="19768-161">Microsoft. Azure. c c.</span><span class="sxs-lookup"><span data-stu-id="19768-161">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="19768-162">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="19768-162">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="19768-163">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="19768-163">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="19768-164">출력</span><span class="sxs-lookup"><span data-stu-id="19768-164">OUTPUTS</span></span>

### <span data-ttu-id="19768-165">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="19768-165">System.Boolean</span></span>

## <span data-ttu-id="19768-166">상속자</span><span class="sxs-lookup"><span data-stu-id="19768-166">NOTES</span></span>

## <span data-ttu-id="19768-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="19768-167">RELATED LINKS</span></span>
