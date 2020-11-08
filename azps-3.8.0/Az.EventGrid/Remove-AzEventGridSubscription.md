---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
ms.openlocfilehash: 59cf723d976d8f16d2e810ba2a8fbb924c822137
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034404"
---
# <span data-ttu-id="bbf36-101">Remove-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="bbf36-101">Remove-AzEventGridSubscription</span></span>

## <span data-ttu-id="bbf36-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbf36-102">SYNOPSIS</span></span>
<span data-ttu-id="bbf36-103">Azure 이벤트 그리드 이벤트 구독을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbf36-103">Removes an Azure Event Grid event subscription.</span></span>

## <span data-ttu-id="bbf36-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bbf36-104">SYNTAX</span></span>

### <span data-ttu-id="bbf36-105">ResourceGroupNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="bbf36-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbf36-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="bbf36-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbf36-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bbf36-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbf36-108">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bbf36-108">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbf36-109">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bbf36-109">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-EventSubscriptionName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbf36-110">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bbf36-110">TopicNameParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bbf36-111">DomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bbf36-111">DomainNameParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-DomainTopicName <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbf36-112">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="bbf36-112">DomainEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bbf36-113">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="bbf36-113">DomainTopicEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bbf36-114">설명은</span><span class="sxs-lookup"><span data-stu-id="bbf36-114">DESCRIPTION</span></span>
<span data-ttu-id="bbf36-115">Azure 이벤트 그리드 항목, 리소스, Azure 구독 또는 리소스 그룹에 대 한 Azure 이벤트 그리드 이벤트 구독을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbf36-115">Removes an Azure Event Grid event subscription for an Azure Event Grid topic, a resource, an Azure subscription or resource group.</span></span>

## <span data-ttu-id="bbf36-116">예제의</span><span class="sxs-lookup"><span data-stu-id="bbf36-116">EXAMPLES</span></span>

### <span data-ttu-id="bbf36-117">예제 1</span><span class="sxs-lookup"><span data-stu-id="bbf36-117">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="bbf36-118">\` \` \` 리소스 그룹 MyResourceGroupName의 Azure 이벤트 그리드 항목 Topic1에 대 한 이벤트 구독 EventSubscription1를 제거 \` \` \` 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbf36-118">Removes the event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="bbf36-119">예제 2</span><span class="sxs-lookup"><span data-stu-id="bbf36-119">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="bbf36-120">\` \` 리소스 그룹 MyResourceGroupName에 대 한 이벤트 구독 EventSubscription1를 제거 합니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="bbf36-120">Removes the event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="bbf36-121">예제 3</span><span class="sxs-lookup"><span data-stu-id="bbf36-121">Example 3</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="bbf36-122">\` \` 기본 Azure 구독에 대 한 이벤트 구독 EventSubscription1를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbf36-122">Removes the event subscription \`EventSubscription1\` to the default Azure subscription.</span></span>

### <span data-ttu-id="bbf36-123">예제 4</span><span class="sxs-lookup"><span data-stu-id="bbf36-123">Example 4</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="bbf36-124">이벤트 플랜 \` EventSubscription1 \` 이벤트 허브 네임 스페이스에 대 한 구독을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbf36-124">Removes the event subscription \`EventSubscription1\` to an Event Hub namespace.</span></span>

### <span data-ttu-id="bbf36-125">예제 5</span><span class="sxs-lookup"><span data-stu-id="bbf36-125">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroup -TopicName Topic1 | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="bbf36-126">이벤트 \` \` 눈금 항목에 대 한 이벤트 구독 EventSubscription1를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbf36-126">Removes the event subscription \`EventSubscription1\` to an Event Grid Topic.</span></span>

## <span data-ttu-id="bbf36-127">변수</span><span class="sxs-lookup"><span data-stu-id="bbf36-127">PARAMETERS</span></span>

### <span data-ttu-id="bbf36-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbf36-128">-DefaultProfile</span></span>
<span data-ttu-id="bbf36-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="bbf36-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bbf36-130">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="bbf36-130">-DomainInputObject</span></span>
<span data-ttu-id="bbf36-131">EventGrid 도메인 개체.</span><span class="sxs-lookup"><span data-stu-id="bbf36-131">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="bbf36-132">-DomainName</span><span class="sxs-lookup"><span data-stu-id="bbf36-132">-DomainName</span></span>
<span data-ttu-id="bbf36-133">EventGrid 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bbf36-133">EventGrid domain name.</span></span>

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

### <span data-ttu-id="bbf36-134">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="bbf36-134">-DomainTopicInputObject</span></span>
<span data-ttu-id="bbf36-135">EventGrid 도메인 주제 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="bbf36-135">EventGrid Domain Topic object.</span></span>

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

### <span data-ttu-id="bbf36-136">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="bbf36-136">-DomainTopicName</span></span>
<span data-ttu-id="bbf36-137">EventGrid 도메인 주제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bbf36-137">EventGrid domain topic name.</span></span>

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

### <span data-ttu-id="bbf36-138">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="bbf36-138">-EventSubscriptionName</span></span>
<span data-ttu-id="bbf36-139">제거 해야 하는 이벤트 구독의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bbf36-139">Name of the event subscription that needs to be removed.</span></span>

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

### <span data-ttu-id="bbf36-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bbf36-140">-InputObject</span></span>
<span data-ttu-id="bbf36-141">EventGrid 주제 개체</span><span class="sxs-lookup"><span data-stu-id="bbf36-141">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="bbf36-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bbf36-142">-PassThru</span></span>
<span data-ttu-id="bbf36-143">제거 작업의 상태를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbf36-143">Returns the status of the Remove operation.</span></span> <span data-ttu-id="bbf36-144">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bbf36-144">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="bbf36-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbf36-145">-ResourceGroupName</span></span>
<span data-ttu-id="bbf36-146">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bbf36-146">Resource Group Name.</span></span>

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

### <span data-ttu-id="bbf36-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bbf36-147">-ResourceId</span></span>
<span data-ttu-id="bbf36-148">이벤트 구독을 제거 해야 하는 리소스의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="bbf36-148">Identifier of the resource whose event subscription needs to be removed.</span></span>

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

### <span data-ttu-id="bbf36-149">-TopicName</span><span class="sxs-lookup"><span data-stu-id="bbf36-149">-TopicName</span></span>
<span data-ttu-id="bbf36-150">이벤트 그리드 주제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bbf36-150">Event Grid Topic Name.</span></span>

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

### <span data-ttu-id="bbf36-151">-확인</span><span class="sxs-lookup"><span data-stu-id="bbf36-151">-Confirm</span></span>
<span data-ttu-id="bbf36-152">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbf36-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bbf36-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bbf36-153">-WhatIf</span></span>
<span data-ttu-id="bbf36-154">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="bbf36-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bbf36-155">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bbf36-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bbf36-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbf36-156">CommonParameters</span></span>
<span data-ttu-id="bbf36-157">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbf36-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbf36-158">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbf36-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbf36-159">입력</span><span class="sxs-lookup"><span data-stu-id="bbf36-159">INPUTS</span></span>

### <span data-ttu-id="bbf36-160">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="bbf36-160">System.String</span></span>

### <span data-ttu-id="bbf36-161">Microsoft. Azure. c c.</span><span class="sxs-lookup"><span data-stu-id="bbf36-161">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="bbf36-162">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="bbf36-162">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="bbf36-163">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="bbf36-163">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="bbf36-164">출력</span><span class="sxs-lookup"><span data-stu-id="bbf36-164">OUTPUTS</span></span>

### <span data-ttu-id="bbf36-165">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="bbf36-165">System.Boolean</span></span>

## <span data-ttu-id="bbf36-166">상속자</span><span class="sxs-lookup"><span data-stu-id="bbf36-166">NOTES</span></span>

## <span data-ttu-id="bbf36-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bbf36-167">RELATED LINKS</span></span>