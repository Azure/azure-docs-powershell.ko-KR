---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/remove-azurermeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridSubscription.md
ms.openlocfilehash: 82d386fb0834db3de03d5692ad8b7a241b6eed90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530977"
---
# <span data-ttu-id="bfe4b-101">Remove-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="bfe4b-101">Remove-AzureRmEventGridSubscription</span></span>

## <span data-ttu-id="bfe4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfe4b-102">SYNOPSIS</span></span>
<span data-ttu-id="bfe4b-103">Azure 이벤트 그리드 이벤트 구독을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfe4b-103">Removes an Azure Event Grid event subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bfe4b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bfe4b-104">SYNTAX</span></span>

### <span data-ttu-id="bfe4b-105">ResourceGroupNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="bfe4b-105">ResourceGroupNameParameterSet (Default)</span></span>
```
Remove-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [[-ResourceGroupName] <String>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfe4b-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="bfe4b-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzureRmEventGridSubscription [-ResourceId] <String> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfe4b-107">EventSubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="bfe4b-107">EventSubscriptionInputObjectSet</span></span>
```
Remove-AzureRmEventGridSubscription [-InputObject] <PSTopic> [-EventSubscriptionName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bfe4b-108">TopicNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="bfe4b-108">TopicNameParameterSet</span></span>
```
Remove-AzureRmEventGridSubscription [-EventSubscriptionName] <String> [-ResourceGroupName] <String>
 [-TopicName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bfe4b-109">설명은</span><span class="sxs-lookup"><span data-stu-id="bfe4b-109">DESCRIPTION</span></span>
<span data-ttu-id="bfe4b-110">Azure 이벤트 그리드 항목, 리소스, Azure 구독 또는 리소스 그룹에 대 한 Azure 이벤트 그리드 이벤트 구독을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfe4b-110">Removes an Azure Event Grid event subscription for an Azure Event Grid topic, a resource, an Azure subscription or resource group.</span></span>

## <span data-ttu-id="bfe4b-111">예제의</span><span class="sxs-lookup"><span data-stu-id="bfe4b-111">EXAMPLES</span></span>

### <span data-ttu-id="bfe4b-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="bfe4b-112">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventGridSubscription -ResourceGroup MyResourceGroup -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="bfe4b-113">\` \` \` 리소스 그룹 MyResourceGroupName의 Azure 이벤트 그리드 항목 Topic1에 대 한 이벤트 구독 EventSubscription1를 제거 \` \` \` 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfe4b-113">Removes the event subscription \`EventSubscription1\` to an Azure Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="bfe4b-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="bfe4b-114">Example 2</span></span>
```
PS C:\> Remove-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="bfe4b-115">\` \` 리소스 그룹 MyResourceGroupName에 대 한 이벤트 구독 EventSubscription1를 제거 합니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="bfe4b-115">Removes the event subscription \`EventSubscription1\` to a resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="bfe4b-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="bfe4b-116">Example 3</span></span>
```
PS C:\> Remove-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="bfe4b-117">\` \` 기본 Azure 구독에 대 한 이벤트 구독 EventSubscription1를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfe4b-117">Removes the event subscription \`EventSubscription1\` to the default Azure subscription.</span></span>

### <span data-ttu-id="bfe4b-118">예제 4</span><span class="sxs-lookup"><span data-stu-id="bfe4b-118">Example 4</span></span>
```
PS C:\> Get-AzureRmResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName" | Remove-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="bfe4b-119">이벤트 플랜 \` EventSubscription1 \` 이벤트 허브 네임 스페이스에 대 한 구독을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfe4b-119">Removes the event subscription \`EventSubscription1\` to an Event Hub namespace.</span></span>

### <span data-ttu-id="bfe4b-120">예제 5</span><span class="sxs-lookup"><span data-stu-id="bfe4b-120">Example 5</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroup -TopicName Topic1 | Remove-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="bfe4b-121">이벤트 \` \` 눈금 항목에 대 한 이벤트 구독 EventSubscription1를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfe4b-121">Removes the event subscription \`EventSubscription1\` to an Event Grid Topic.</span></span>

## <span data-ttu-id="bfe4b-122">변수</span><span class="sxs-lookup"><span data-stu-id="bfe4b-122">PARAMETERS</span></span>

### <span data-ttu-id="bfe4b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfe4b-123">-DefaultProfile</span></span>
<span data-ttu-id="bfe4b-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="bfe4b-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bfe4b-125">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="bfe4b-125">-EventSubscriptionName</span></span>
<span data-ttu-id="bfe4b-126">제거 해야 하는 이벤트 구독의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bfe4b-126">Name of the event subscription that needs to be removed.</span></span>

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

### <span data-ttu-id="bfe4b-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bfe4b-127">-InputObject</span></span>
<span data-ttu-id="bfe4b-128">EventGrid Eventgrid 개체.</span><span class="sxs-lookup"><span data-stu-id="bfe4b-128">EventGrid EventSubscription object.</span></span>

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

### <span data-ttu-id="bfe4b-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bfe4b-129">-PassThru</span></span>
<span data-ttu-id="bfe4b-130">제거 작업의 상태를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfe4b-130">Returns the status of the Remove operation.</span></span> <span data-ttu-id="bfe4b-131">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bfe4b-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="bfe4b-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfe4b-132">-ResourceGroupName</span></span>
<span data-ttu-id="bfe4b-133">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bfe4b-133">Resource Group Name.</span></span>

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

### <span data-ttu-id="bfe4b-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bfe4b-134">-ResourceId</span></span>
<span data-ttu-id="bfe4b-135">이벤트 구독을 제거 해야 하는 리소스의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="bfe4b-135">Identifier of the resource whose event subscription needs to be removed.</span></span>

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

### <span data-ttu-id="bfe4b-136">-TopicName</span><span class="sxs-lookup"><span data-stu-id="bfe4b-136">-TopicName</span></span>
<span data-ttu-id="bfe4b-137">이벤트 그리드 주제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bfe4b-137">Event Grid Topic Name.</span></span>

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

### <span data-ttu-id="bfe4b-138">-확인</span><span class="sxs-lookup"><span data-stu-id="bfe4b-138">-Confirm</span></span>
<span data-ttu-id="bfe4b-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfe4b-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bfe4b-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bfe4b-140">-WhatIf</span></span>
<span data-ttu-id="bfe4b-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="bfe4b-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bfe4b-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bfe4b-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bfe4b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfe4b-143">CommonParameters</span></span>
<span data-ttu-id="bfe4b-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bfe4b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfe4b-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfe4b-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfe4b-146">입력</span><span class="sxs-lookup"><span data-stu-id="bfe4b-146">INPUTS</span></span>

### <span data-ttu-id="bfe4b-147">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="bfe4b-147">System.String</span></span>

### <span data-ttu-id="bfe4b-148">Microsoft. Azure. c c.</span><span class="sxs-lookup"><span data-stu-id="bfe4b-148">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>
<span data-ttu-id="bfe4b-149">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bfe4b-149">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="bfe4b-150">출력</span><span class="sxs-lookup"><span data-stu-id="bfe4b-150">OUTPUTS</span></span>

### <span data-ttu-id="bfe4b-151">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="bfe4b-151">System.Boolean</span></span>

## <span data-ttu-id="bfe4b-152">상속자</span><span class="sxs-lookup"><span data-stu-id="bfe4b-152">NOTES</span></span>

## <span data-ttu-id="bfe4b-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bfe4b-153">RELATED LINKS</span></span>
