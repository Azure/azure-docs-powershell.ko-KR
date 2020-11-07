---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridSubscription.md
ms.openlocfilehash: 2e2abe03d0df4ccf662f99945c45e837669a1de9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696512"
---
# <span data-ttu-id="8dbfb-101">Remove-AzEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="8dbfb-101">Remove-AzEventGridSubscription</span></span>

## <span data-ttu-id="8dbfb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8dbfb-102">SYNOPSIS</span></span>
<span data-ttu-id="8dbfb-103">Azure 이벤트 그리드 이벤트 구독을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8dbfb-103">Removes an Azure Event Grid event subscription.</span></span>

## <span data-ttu-id="8dbfb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8dbfb-104">SYNTAX</span></span>

### <span data-ttu-id="8dbfb-105">ResourceGroupNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="8dbfb-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8dbfb-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="8dbfb-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8dbfb-107">EventSubscriptionCustomTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8dbfb-107">EventSubscriptionCustomTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8dbfb-108">EventSubscriptionDomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8dbfb-108">EventSubscriptionDomainInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-DomainInputObject] <PSDomain> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8dbfb-109">EventSubscriptionDomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8dbfb-109">EventSubscriptionDomainTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridSubscription [-DomainTopicInputObject] <PSDomainTopic> [-EventSubscriptionName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8dbfb-110">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8dbfb-110">TopicNameParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8dbfb-111">DomainNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8dbfb-111">DomainNameParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-DomainName] <String> [-DomainTopicName <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8dbfb-112">DomainEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="8dbfb-112">DomainEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8dbfb-113">DomainTopicEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="8dbfb-113">DomainTopicEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridSubscription [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8dbfb-114">설명은</span><span class="sxs-lookup"><span data-stu-id="8dbfb-114">DESCRIPTION</span></span>
<span data-ttu-id="8dbfb-115">Azure 이벤트 그리드 항목, 리소스, Azure 구독 또는 리소스 그룹에 대 한 Azure 이벤트 그리드 이벤트 구독을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8dbfb-115">Removes an Azure Event Grid event subscription for an Azure Event Grid topic, a resource, an Azure subscription or resource group.</span></span>

## <span data-ttu-id="8dbfb-116">예제의</span><span class="sxs-lookup"><span data-stu-id="8dbfb-116">EXAMPLES</span></span>

### <span data-ttu-id="8dbfb-117">예제 1</span><span class="sxs-lookup"><span data-stu-id="8dbfb-117">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="8dbfb-118">\` \` \` 리소스 그룹 MyResourceGroupName의 Azure 이벤트 그리드 항목 Topic1에 대 한 이벤트 구독 EventSubscription1를 제거 \` \` \` 합니다.</span><span class="sxs-lookup"><span data-stu-id="8dbfb-118">Removes the event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="8dbfb-119">예제 2</span><span class="sxs-lookup"><span data-stu-id="8dbfb-119">Example 2</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="8dbfb-120">\` \` 리소스 그룹 MyResourceGroupName에 대 한 이벤트 구독 EventSubscription1를 제거 합니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="8dbfb-120">Removes the event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="8dbfb-121">예제 3</span><span class="sxs-lookup"><span data-stu-id="8dbfb-121">Example 3</span></span>
```powershell
PS C:\> Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="8dbfb-122">\` \` 기본 Azure 구독에 대 한 이벤트 구독 EventSubscription1를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8dbfb-122">Removes the event subscription \`EventSubscription1\` to the default Azure subscription.</span></span>

### <span data-ttu-id="8dbfb-123">예제 4</span><span class="sxs-lookup"><span data-stu-id="8dbfb-123">Example 4</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="8dbfb-124">이벤트 플랜 \` EventSubscription1 \` 이벤트 허브 네임 스페이스에 대 한 구독을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8dbfb-124">Removes the event subscription \`EventSubscription1\` to an Event Hub namespace.</span></span>

### <span data-ttu-id="8dbfb-125">예제 5</span><span class="sxs-lookup"><span data-stu-id="8dbfb-125">Example 5</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroup -TopicName Topic1 | Remove-AzEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="8dbfb-126">이벤트 \` \` 눈금 항목에 대 한 이벤트 구독 EventSubscription1를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="8dbfb-126">Removes the event subscription \`EventSubscription1\` to an Event Grid Topic.</span></span>

## <span data-ttu-id="8dbfb-127">변수</span><span class="sxs-lookup"><span data-stu-id="8dbfb-127">PARAMETERS</span></span>

### <span data-ttu-id="8dbfb-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8dbfb-128">-DefaultProfile</span></span>
<span data-ttu-id="8dbfb-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8dbfb-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8dbfb-130">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="8dbfb-130">-DomainInputObject</span></span>
<span data-ttu-id="8dbfb-131">EventGrid 도메인 개체.</span><span class="sxs-lookup"><span data-stu-id="8dbfb-131">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="8dbfb-132">-DomainName</span><span class="sxs-lookup"><span data-stu-id="8dbfb-132">-DomainName</span></span>
<span data-ttu-id="8dbfb-133">EventGrid 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8dbfb-133">EventGrid domain name.</span></span>

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

### <span data-ttu-id="8dbfb-134">-DomainTopicInputObject</span><span class="sxs-lookup"><span data-stu-id="8dbfb-134">-DomainTopicInputObject</span></span>
<span data-ttu-id="8dbfb-135">EventGrid 도메인 주제 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="8dbfb-135">EventGrid Domain Topic object.</span></span>

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

### <span data-ttu-id="8dbfb-136">-DomainTopicName</span><span class="sxs-lookup"><span data-stu-id="8dbfb-136">-DomainTopicName</span></span>
<span data-ttu-id="8dbfb-137">EventGrid 도메인 주제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8dbfb-137">EventGrid domain topic name.</span></span>

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

### <span data-ttu-id="8dbfb-138">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="8dbfb-138">-EventSubscriptionName</span></span>
<span data-ttu-id="8dbfb-139">제거 해야 하는 이벤트 구독의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8dbfb-139">Name of the event subscription that needs to be removed.</span></span>

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

### <span data-ttu-id="8dbfb-140">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8dbfb-140">-InputObject</span></span>
<span data-ttu-id="8dbfb-141">EventGrid 주제 개체</span><span class="sxs-lookup"><span data-stu-id="8dbfb-141">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="8dbfb-142">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8dbfb-142">-PassThru</span></span>
<span data-ttu-id="8dbfb-143">제거 작업의 상태를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="8dbfb-143">Returns the status of the Remove operation.</span></span> <span data-ttu-id="8dbfb-144">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8dbfb-144">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8dbfb-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8dbfb-145">-ResourceGroupName</span></span>
<span data-ttu-id="8dbfb-146">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8dbfb-146">Resource Group Name.</span></span>

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

### <span data-ttu-id="8dbfb-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8dbfb-147">-ResourceId</span></span>
<span data-ttu-id="8dbfb-148">이벤트 구독을 제거 해야 하는 리소스의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="8dbfb-148">Identifier of the resource whose event subscription needs to be removed.</span></span>

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

### <span data-ttu-id="8dbfb-149">-TopicName</span><span class="sxs-lookup"><span data-stu-id="8dbfb-149">-TopicName</span></span>
<span data-ttu-id="8dbfb-150">이벤트 그리드 주제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8dbfb-150">Event Grid Topic Name.</span></span>

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

### <span data-ttu-id="8dbfb-151">-확인</span><span class="sxs-lookup"><span data-stu-id="8dbfb-151">-Confirm</span></span>
<span data-ttu-id="8dbfb-152">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8dbfb-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8dbfb-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8dbfb-153">-WhatIf</span></span>
<span data-ttu-id="8dbfb-154">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8dbfb-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8dbfb-155">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8dbfb-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8dbfb-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8dbfb-156">CommonParameters</span></span>
<span data-ttu-id="8dbfb-157">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8dbfb-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8dbfb-158">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8dbfb-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8dbfb-159">입력</span><span class="sxs-lookup"><span data-stu-id="8dbfb-159">INPUTS</span></span>

### <span data-ttu-id="8dbfb-160">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8dbfb-160">System.String</span></span>

### <span data-ttu-id="8dbfb-161">Microsoft. Azure. c c.</span><span class="sxs-lookup"><span data-stu-id="8dbfb-161">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="8dbfb-162">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="8dbfb-162">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

### <span data-ttu-id="8dbfb-163">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="8dbfb-163">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="8dbfb-164">출력</span><span class="sxs-lookup"><span data-stu-id="8dbfb-164">OUTPUTS</span></span>

### <span data-ttu-id="8dbfb-165">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="8dbfb-165">System.Boolean</span></span>

## <span data-ttu-id="8dbfb-166">상속자</span><span class="sxs-lookup"><span data-stu-id="8dbfb-166">NOTES</span></span>

## <span data-ttu-id="8dbfb-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8dbfb-167">RELATED LINKS</span></span>
