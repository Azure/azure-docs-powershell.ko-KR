---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/new-azeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopicKey.md
ms.openlocfilehash: aa59b4046a775c41dd3b44142d0a407c94ff1f4c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991237"
---
# <span data-ttu-id="d3994-101">New-AzEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="d3994-101">New-AzEventGridTopicKey</span></span>

## <span data-ttu-id="d3994-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3994-102">SYNOPSIS</span></span>
<span data-ttu-id="d3994-103">Azure Event Grid 토픽에 대한 공유 액세스 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="d3994-103">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="d3994-104">구문</span><span class="sxs-lookup"><span data-stu-id="d3994-104">SYNTAX</span></span>

### <span data-ttu-id="d3994-105">TopicNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="d3994-105">TopicNameParameterSet (Default)</span></span>
```
New-AzEventGridTopicKey [-ResourceGroupName] <String> [-TopicName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3994-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3994-106">TopicInputObjectParameterSet</span></span>
```
New-AzEventGridTopicKey [-KeyName] <String> [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3994-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3994-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridTopicKey [-KeyName] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3994-108">설명</span><span class="sxs-lookup"><span data-stu-id="d3994-108">DESCRIPTION</span></span>
<span data-ttu-id="d3994-109">Azure Event Grid 토픽에 대한 공유 액세스 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="d3994-109">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="d3994-110">예제</span><span class="sxs-lookup"><span data-stu-id="d3994-110">EXAMPLES</span></span>

### <span data-ttu-id="d3994-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="d3994-111">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridTopicKey -ResourceGroup MyResourceGroupName -TopicName Topic1 -KeyName key1
```

<span data-ttu-id="d3994-112">리소스 그룹 \' \` \` \` MyResourceGroupName에서 Event Grid 항목 항목 항목1의 key key1'\에 해당하는 키를 다시 \` 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="d3994-112">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="d3994-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="d3994-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | New-AzEventGridTopicKey -KeyName "key1"
```

<span data-ttu-id="d3994-114">리소스 그룹 \' \` \` \` MyResourceGroupName에서 Event Grid 항목 항목 항목1의 key key1'\에 해당하는 키를 다시 \` 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="d3994-114">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="d3994-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d3994-115">PARAMETERS</span></span>

### <span data-ttu-id="d3994-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3994-116">-DefaultProfile</span></span>
<span data-ttu-id="d3994-117">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d3994-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d3994-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d3994-118">-InputObject</span></span>
<span data-ttu-id="d3994-119">EventGrid 토픽 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d3994-119">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3994-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="d3994-120">-KeyName</span></span>
<span data-ttu-id="d3994-121">다시 생성해야 하는 키의 이름</span><span class="sxs-lookup"><span data-stu-id="d3994-121">The name of the key that needs to be regenerated</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3994-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3994-122">-ResourceGroupName</span></span>
<span data-ttu-id="d3994-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d3994-123">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3994-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d3994-124">-ResourceId</span></span>
<span data-ttu-id="d3994-125">Event Grid 토픽을 나타내는 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="d3994-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="d3994-126">-TopicName</span><span class="sxs-lookup"><span data-stu-id="d3994-126">-TopicName</span></span>
<span data-ttu-id="d3994-127">토픽의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d3994-127">The name of the topic.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3994-128">-확인</span><span class="sxs-lookup"><span data-stu-id="d3994-128">-Confirm</span></span>
<span data-ttu-id="d3994-129">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d3994-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3994-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3994-130">-WhatIf</span></span>
<span data-ttu-id="d3994-131">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d3994-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3994-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d3994-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3994-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3994-133">CommonParameters</span></span>
<span data-ttu-id="d3994-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d3994-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3994-135">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d3994-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3994-136">입력</span><span class="sxs-lookup"><span data-stu-id="d3994-136">INPUTS</span></span>

### <span data-ttu-id="d3994-137">System.String</span><span class="sxs-lookup"><span data-stu-id="d3994-137">System.String</span></span>

### <span data-ttu-id="d3994-138">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="d3994-138">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="d3994-139">출력</span><span class="sxs-lookup"><span data-stu-id="d3994-139">OUTPUTS</span></span>

### <span data-ttu-id="d3994-140">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="d3994-140">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="d3994-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d3994-141">NOTES</span></span>

## <span data-ttu-id="d3994-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d3994-142">RELATED LINKS</span></span>
