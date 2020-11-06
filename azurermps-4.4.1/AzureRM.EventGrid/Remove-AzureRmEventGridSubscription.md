---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridSubscription.md
ms.openlocfilehash: a15cb222108d79544d38ce730897e03fa61066ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537280"
---
# <span data-ttu-id="3f091-101">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="3f091-101">Remove-AzureRmEventGridSubscription</span></span>

## <span data-ttu-id="3f091-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f091-102">SYNOPSIS</span></span>
<span data-ttu-id="3f091-103">Azure 이벤트 그리드 이벤트 구독을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f091-103">Removes an Azure Event Grid event subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3f091-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3f091-104">SYNTAX</span></span>

### <span data-ttu-id="3f091-105">ResourceGroupNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="3f091-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Remove-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f091-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f091-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzureRmEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f091-107">EventSubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="3f091-107">EventSubscriptionInputObjectSet</span></span>
```
Remove-AzureRmEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f091-108">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f091-108">TopicNameParameterSet</span></span>
```
Remove-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3f091-109">설명은</span><span class="sxs-lookup"><span data-stu-id="3f091-109">DESCRIPTION</span></span>
<span data-ttu-id="3f091-110">Azure 이벤트 그리드 항목, 리소스, Azure 구독 또는 리소스 그룹에 대 한 Azure 이벤트 그리드 이벤트 구독을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f091-110">Removes an Azure Event Grid event subscription for an Azure Event Grid topic, a resource, an Azure subscription or resource group.</span></span>

## <span data-ttu-id="3f091-111">예제의</span><span class="sxs-lookup"><span data-stu-id="3f091-111">EXAMPLES</span></span>

### <span data-ttu-id="3f091-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="3f091-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="3f091-113">\` \` \` 리소스 그룹 MyResourceGroupName의 Azure 이벤트 그리드 항목 Topic1에 대 한 이벤트 구독 EventSubscription1를 제거 \` \` \` 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f091-113">Removes the event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="3f091-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="3f091-114">Example 2</span></span>
```
PS C:\> Remove-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="3f091-115">\` \` 리소스 그룹 MyResourceGroupName에 대 한 이벤트 구독 EventSubscription1를 제거 합니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="3f091-115">Removes the event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="3f091-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="3f091-116">Example 3</span></span>
```
PS C:\> Remove-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="3f091-117">\` \` 기본 Azure 구독에 대 한 이벤트 구독 EventSubscription1를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f091-117">Removes the event subscription \`EventSubscription1\` to the default Azure subscription.</span></span>

### <span data-ttu-id="3f091-118">예제 4</span><span class="sxs-lookup"><span data-stu-id="3f091-118">Example 4</span></span>
```
PS C:\> Get-AzureRmResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" | Remove-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="3f091-119">이벤트 플랜 \` EventSubscription1 \` 이벤트 허브 네임 스페이스에 대 한 구독을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f091-119">Removes the event subscription \`EventSubscription1\` to an Event Hub namespace.</span></span>

### <span data-ttu-id="3f091-120">예제 5</span><span class="sxs-lookup"><span data-stu-id="3f091-120">Example 5</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroup -TopicName Topic1 | Remove-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="3f091-121">이벤트 \` \` 눈금 항목에 대 한 이벤트 구독 EventSubscription1를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f091-121">Removes the event subscription \`EventSubscription1\` to an Event Grid Topic.</span></span>

## <span data-ttu-id="3f091-122">변수</span><span class="sxs-lookup"><span data-stu-id="3f091-122">PARAMETERS</span></span>

### <span data-ttu-id="3f091-123">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="3f091-123">-EventSubscriptionName</span></span>
<span data-ttu-id="3f091-124">제거 해야 하는 이벤트 구독의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3f091-124">Name of the event subscription that needs to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSet, ResourceIdEventSubscriptionParameterSet, TopicNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f091-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f091-125">-InputObject</span></span>
<span data-ttu-id="3f091-126">EventGrid Eventgrid 개체.</span><span class="sxs-lookup"><span data-stu-id="3f091-126">EventGrid EventSubscription object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: EventSubscriptionInputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f091-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3f091-127">-PassThru</span></span>
<span data-ttu-id="3f091-128">제거 작업의 상태를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f091-128">Returns the status of the Remove operation.</span></span> <span data-ttu-id="3f091-129">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3f091-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3f091-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f091-130">-ResourceGroupName</span></span>
<span data-ttu-id="3f091-131">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3f091-131">Resource Group Name.</span></span>

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
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f091-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f091-132">-ResourceId</span></span>
<span data-ttu-id="3f091-133">이벤트 구독을 제거 해야 하는 리소스의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="3f091-133">Identifier of the resource whose event subscription needs to be removed.</span></span>

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

### <span data-ttu-id="3f091-134">-TopicName</span><span class="sxs-lookup"><span data-stu-id="3f091-134">-TopicName</span></span>
<span data-ttu-id="3f091-135">이벤트 그리드 주제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3f091-135">Event Grid Topic Name.</span></span>

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

### <span data-ttu-id="3f091-136">-확인</span><span class="sxs-lookup"><span data-stu-id="3f091-136">-Confirm</span></span>
<span data-ttu-id="3f091-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f091-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f091-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f091-138">-WhatIf</span></span>
<span data-ttu-id="3f091-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3f091-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f091-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3f091-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f091-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f091-141">-DefaultProfile</span></span>
<span data-ttu-id="3f091-142">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3f091-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f091-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f091-143">CommonParameters</span></span>
<span data-ttu-id="3f091-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3f091-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f091-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f091-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f091-146">입력</span><span class="sxs-lookup"><span data-stu-id="3f091-146">INPUTS</span></span>

### <span data-ttu-id="3f091-147">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3f091-147">System.String</span></span>
<span data-ttu-id="3f091-148">Microsoft. PSEventSubscription 표.</span><span class="sxs-lookup"><span data-stu-id="3f091-148">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="3f091-149">출력</span><span class="sxs-lookup"><span data-stu-id="3f091-149">OUTPUTS</span></span>

### <span data-ttu-id="3f091-150">System. 개체</span><span class="sxs-lookup"><span data-stu-id="3f091-150">System.Object</span></span>

## <span data-ttu-id="3f091-151">상속자</span><span class="sxs-lookup"><span data-stu-id="3f091-151">NOTES</span></span>

## <span data-ttu-id="3f091-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3f091-152">RELATED LINKS</span></span>

