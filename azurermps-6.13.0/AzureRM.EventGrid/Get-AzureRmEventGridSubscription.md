---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/get-azurermeventgridsubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridSubscription.md
ms.openlocfilehash: 3117433c677330eba4585d45337c44658225ee0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530984"
---
# <span data-ttu-id="4285a-101">Get-AzureRmEventGridSubscription</span><span class="sxs-lookup"><span data-stu-id="4285a-101">Get-AzureRmEventGridSubscription</span></span>

## <span data-ttu-id="4285a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4285a-102">SYNOPSIS</span></span>
<span data-ttu-id="4285a-103">이벤트 구독에 대 한 세부 정보를 가져오거나 현재 Azure 구독에 있는 모든 이벤트 구독의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4285a-103">Gets the details of an event subscription, or gets a list of all event subscriptions in the current Azure subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4285a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4285a-104">SYNTAX</span></span>

### <span data-ttu-id="4285a-105">EventSubscriptionTopicNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="4285a-105">EventSubscriptionTopicNameParameterSet (Default)</span></span>
```
Get-AzureRmEventGridSubscription [[-EventSubscriptionName] <String>] [[-ResourceGroupName] <String>]
 [[-TopicName] <String>] [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4285a-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="4285a-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzureRmEventGridSubscription [[-EventSubscriptionName] <String>] [-ResourceId] <String>
 [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4285a-107">EventSubscriptionTopicTypeNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4285a-107">EventSubscriptionTopicTypeNameParameterSet</span></span>
```
Get-AzureRmEventGridSubscription [[-ResourceGroupName] <String>] [[-TopicTypeName] <String>]
 [[-Location] <String>] [-IncludeFullEndpointUrl] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4285a-108">EventSubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4285a-108">EventSubscriptionInputObjectSet</span></span>
```
Get-AzureRmEventGridSubscription [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4285a-109">설명은</span><span class="sxs-lookup"><span data-stu-id="4285a-109">DESCRIPTION</span></span>
<span data-ttu-id="4285a-110">Get-AzureRmEventGridSubscription cmdlet은 지정 된 이벤트 그리드 구독에 대 한 세부 정보 또는 현재 Azure 구독 또는 리소스 그룹에 있는 모든 이벤트 그리드 구독 목록 중 하나를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4285a-110">The Get-AzureRmEventGridSubscription cmdlet gets either the details of a specified Event Grid subscription, or a list of all Event Grid subscriptions in the current Azure subscription or resource group.</span></span>
<span data-ttu-id="4285a-111">이벤트 구독 이름을 제공 하는 경우 단일 이벤트 그리드 구독에 대 한 세부 정보가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4285a-111">If the event subscription name is provided, the details of a single Event Grid subscription is returned.</span></span>
<span data-ttu-id="4285a-112">이벤트 구독 이름을 제공 하지 않으면 모든 이벤트 구독 목록이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4285a-112">If the event subscription name is not provided, a list of all event subscriptions is returned.</span></span>

## <span data-ttu-id="4285a-113">예제의</span><span class="sxs-lookup"><span data-stu-id="4285a-113">EXAMPLES</span></span>

### <span data-ttu-id="4285a-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="4285a-114">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="4285a-115">\` \` \` \` 리소스 그룹 MyResourceGroupName의 주제 Topic1에 대해 생성 \` 된 이벤트 구독 EventSubscription1의 세부 정보를 가져옵니다 \` .</span><span class="sxs-lookup"><span data-stu-id="4285a-115">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="4285a-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="4285a-116">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1 -EventSubscriptionName EventSubscription1 -IncludeFullEndpointUrl
```

<span data-ttu-id="4285a-117">\` \` \` \` \` \` Webhook 기반 이벤트 구독 인 경우 전체 끝점 URL을 포함 하 여 리소스 그룹 MyResourceGroupName의 주제 Topic1에 대해 생성 된 이벤트 구독 EventSubscription1의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4285a-117">Gets the details of event subscription \`EventSubscription1\` created for topic \`Topic1\` in resource group \`MyResourceGroupName\`, including the full endpoint URL if it is a webhook based event subscription.</span></span>

### <span data-ttu-id="4285a-118">예제 3</span><span class="sxs-lookup"><span data-stu-id="4285a-118">Example 3</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -TopicName Topic1
```

<span data-ttu-id="4285a-119">\` \` 리소스 그룹 MyResourceGroupName에서 항목 Topic1에 대해 생성 된 모든 이벤트 구독 목록을 가져옵니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="4285a-119">Get a list of all the event subscriptions created for topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="4285a-120">예제 4</span><span class="sxs-lookup"><span data-stu-id="4285a-120">Example 4</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="4285a-121">\` \` 리소스 그룹 MyResourceGroupName에 대해 생성 된 이벤트 구독 EventSubscription1의 세부 정보를 가져옵니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="4285a-121">Gets the details of event subscription \`EventSubscription1\` created for resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="4285a-122">예제 5</span><span class="sxs-lookup"><span data-stu-id="4285a-122">Example 5</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -EventSubscriptionName EventSubscription1
```

<span data-ttu-id="4285a-123">\` \` 현재 선택 된 Azure 구독에 대해 생성 된 이벤트 구독 EventSubscription1의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4285a-123">Gets the details of event subscription \`EventSubscription1\` created for the currently selected Azure subscription.</span></span>

### <span data-ttu-id="4285a-124">예제 6</span><span class="sxs-lookup"><span data-stu-id="4285a-124">Example 6</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="4285a-125">리소스 그룹 MyResourceGroupName에서 만든 모든 전역 이벤트 구독의 목록을 가져옵니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="4285a-125">Gets the list of all global event subscriptions created under the resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="4285a-126">예제 7</span><span class="sxs-lookup"><span data-stu-id="4285a-126">Example 7</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription
```

<span data-ttu-id="4285a-127">현재 선택 된 Azure 구독에서 만들어진 모든 전역 이벤트 구독의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4285a-127">Gets the list of all global event subscriptions created under the currently selected Azure subscription.</span></span>

### <span data-ttu-id="4285a-128">예제 8</span><span class="sxs-lookup"><span data-stu-id="4285a-128">Example 8</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceGroupName MyResourceGroupName -Location westus2
```

<span data-ttu-id="4285a-129">\` \` 지정 된 위치 westus2에서 리소스 그룹 MyResourceGroupName에 만든 모든 국가별 이벤트 구독의 목록을 가져옵니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="4285a-129">Gets the list of all regional event subscriptions created under resource group \`MyResourceGroupName\` in the specified location \`westus2\`.</span></span>

### <span data-ttu-id="4285a-130">예제 9</span><span class="sxs-lookup"><span data-stu-id="4285a-130">Example 9</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -ResourceId "/subscriptions/$subscriptionId/resourceGroups/$resourceGroupName/providers/Microsoft.EventHub/namespaces/$namespaceName"
```

<span data-ttu-id="4285a-131">지정 된 EventHub 네임 스페이스에 대해 만들어진 모든 이벤트 구독의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4285a-131">Gets the list of all event subscriptions created for the specified EventHub namespace.</span></span>

### <span data-ttu-id="4285a-132">예제 10</span><span class="sxs-lookup"><span data-stu-id="4285a-132">Example 10</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -TopicTypeName "Microsoft.EventHub.Namespaces" -Location $location
```

<span data-ttu-id="4285a-133">지정 된 항목 형식 (EventHub 네임 스페이스)에 대해 생성 된 모든 이벤트 구독의 목록을 해당 위치에 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4285a-133">Gets the list of all event subscriptions created for the specified topic type (EventHub namespaces) in the specified location.</span></span>

### <span data-ttu-id="4285a-134">예제 11</span><span class="sxs-lookup"><span data-stu-id="4285a-134">Example 11</span></span>
```
PS C:\> Get-AzureRmEventGridSubscription -TopicTypeName "Microsoft.Resources.ResourceGroups" -ResourceGroupName MyResourceGroupName
```

<span data-ttu-id="4285a-135">특정 리소스 그룹에 대해 생성 된 모든 이벤트 구독의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4285a-135">Gets the list of all event subscriptions created for the specific resource group.</span></span>

## <span data-ttu-id="4285a-136">변수</span><span class="sxs-lookup"><span data-stu-id="4285a-136">PARAMETERS</span></span>

### <span data-ttu-id="4285a-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4285a-137">-DefaultProfile</span></span>
<span data-ttu-id="4285a-138">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4285a-138">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4285a-139">-EventSubscriptionName</span><span class="sxs-lookup"><span data-stu-id="4285a-139">-EventSubscriptionName</span></span>
<span data-ttu-id="4285a-140">이벤트 구독의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4285a-140">The name of the event subscription</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4285a-141">-IncludeFullEndpointUrl</span><span class="sxs-lookup"><span data-stu-id="4285a-141">-IncludeFullEndpointUrl</span></span>
<span data-ttu-id="4285a-142">이벤트 구독 대상의 전체 끝점 URL을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="4285a-142">Include the full endpoint URL of the event subscription destination.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EventSubscriptionTopicNameParameterSet, ResourceIdEventSubscriptionParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4285a-143">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4285a-143">-InputObject</span></span>
<span data-ttu-id="4285a-144">EventGrid 이벤트 구독 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="4285a-144">EventGrid Event Subscription object.</span></span>

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

### <span data-ttu-id="4285a-145">-위치</span><span class="sxs-lookup"><span data-stu-id="4285a-145">-Location</span></span>
<span data-ttu-id="4285a-146">Location</span><span class="sxs-lookup"><span data-stu-id="4285a-146">Location</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4285a-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4285a-147">-ResourceGroupName</span></span>
<span data-ttu-id="4285a-148">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4285a-148">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet, EventSubscriptionTopicTypeNameParameterSet
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4285a-149">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4285a-149">-ResourceId</span></span>
<span data-ttu-id="4285a-150">이벤트 구독이 생성 된 리소스의 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="4285a-150">Identifier of the resource to which event subscriptions have been created.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4285a-151">-TopicName</span><span class="sxs-lookup"><span data-stu-id="4285a-151">-TopicName</span></span>
<span data-ttu-id="4285a-152">EventGrid 주제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4285a-152">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicNameParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4285a-153">-TopicTypeName</span><span class="sxs-lookup"><span data-stu-id="4285a-153">-TopicTypeName</span></span>
<span data-ttu-id="4285a-154">TopicType 이름</span><span class="sxs-lookup"><span data-stu-id="4285a-154">TopicType name</span></span>

```yaml
Type: System.String
Parameter Sets: EventSubscriptionTopicTypeNameParameterSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4285a-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4285a-155">CommonParameters</span></span>
<span data-ttu-id="4285a-156">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4285a-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4285a-157">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4285a-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4285a-158">입력</span><span class="sxs-lookup"><span data-stu-id="4285a-158">INPUTS</span></span>

### <span data-ttu-id="4285a-159">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4285a-159">System.String</span></span>

### <span data-ttu-id="4285a-160">Microsoft. Azure. c c.</span><span class="sxs-lookup"><span data-stu-id="4285a-160">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>
<span data-ttu-id="4285a-161">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4285a-161">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="4285a-162">출력</span><span class="sxs-lookup"><span data-stu-id="4285a-162">OUTPUTS</span></span>

### <span data-ttu-id="4285a-163">Microsoft. PSEventSubscription 표.</span><span class="sxs-lookup"><span data-stu-id="4285a-163">Microsoft.Azure.Commands.EventGrid.Models.PSEventSubscription</span></span>

## <span data-ttu-id="4285a-164">상속자</span><span class="sxs-lookup"><span data-stu-id="4285a-164">NOTES</span></span>

## <span data-ttu-id="4285a-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4285a-165">RELATED LINKS</span></span>
