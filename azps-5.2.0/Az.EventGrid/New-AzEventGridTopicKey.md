---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopicKey.md
ms.openlocfilehash: ab9c9401b0f8d929be1a4aa244f407957d886e4c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363714"
---
# <span data-ttu-id="98e48-101">New-AzEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="98e48-101">New-AzEventGridTopicKey</span></span>

## <span data-ttu-id="98e48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98e48-102">SYNOPSIS</span></span>
<span data-ttu-id="98e48-103">Azure Event Grid 토픽에 대한 공유 액세스 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="98e48-103">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="98e48-104">구문</span><span class="sxs-lookup"><span data-stu-id="98e48-104">SYNTAX</span></span>

### <span data-ttu-id="98e48-105">TopicNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="98e48-105">TopicNameParameterSet (Default)</span></span>
```
New-AzEventGridTopicKey [-ResourceGroupName] <String> [-TopicName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98e48-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="98e48-106">TopicInputObjectParameterSet</span></span>
```
New-AzEventGridTopicKey [-KeyName] <String> [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98e48-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="98e48-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridTopicKey [-KeyName] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98e48-108">설명</span><span class="sxs-lookup"><span data-stu-id="98e48-108">DESCRIPTION</span></span>
<span data-ttu-id="98e48-109">Azure Event Grid 토픽에 대한 공유 액세스 키를 다시 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="98e48-109">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="98e48-110">예제</span><span class="sxs-lookup"><span data-stu-id="98e48-110">EXAMPLES</span></span>

### <span data-ttu-id="98e48-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="98e48-111">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridTopicKey -ResourceGroup MyResourceGroupName -TopicName Topic1 -KeyName key1
```

<span data-ttu-id="98e48-112">리소스 그룹 \' \` \` \` MyResourceGroupName에서 Event Grid 항목 Topic1의 key key1'\에 해당하는 키를 다시 \` 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="98e48-112">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="98e48-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="98e48-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | New-AzEventGridTopicKey -KeyName "key1"
```

<span data-ttu-id="98e48-114">리소스 그룹 \' \` \` \` MyResourceGroupName에서 Event Grid 항목 Topic1의 key key1'\에 해당하는 키를 다시 \` 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="98e48-114">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="98e48-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="98e48-115">PARAMETERS</span></span>

### <span data-ttu-id="98e48-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98e48-116">-DefaultProfile</span></span>
<span data-ttu-id="98e48-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="98e48-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="98e48-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="98e48-118">-InputObject</span></span>
<span data-ttu-id="98e48-119">EventGrid 토픽 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="98e48-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="98e48-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="98e48-120">-KeyName</span></span>
<span data-ttu-id="98e48-121">다시 생성해야 하는 키의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="98e48-121">The name of the key that needs to be regenerated</span></span>

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

### <span data-ttu-id="98e48-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98e48-122">-ResourceGroupName</span></span>
<span data-ttu-id="98e48-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="98e48-123">Resource group name.</span></span>

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

### <span data-ttu-id="98e48-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98e48-124">-ResourceId</span></span>
<span data-ttu-id="98e48-125">Event Grid 토픽을 나타내는 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="98e48-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="98e48-126">-TopicName</span><span class="sxs-lookup"><span data-stu-id="98e48-126">-TopicName</span></span>
<span data-ttu-id="98e48-127">항목의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="98e48-127">The name of the topic.</span></span>

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

### <span data-ttu-id="98e48-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="98e48-128">-Confirm</span></span>
<span data-ttu-id="98e48-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="98e48-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98e48-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98e48-130">-WhatIf</span></span>
<span data-ttu-id="98e48-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="98e48-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98e48-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="98e48-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98e48-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98e48-133">CommonParameters</span></span>
<span data-ttu-id="98e48-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="98e48-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98e48-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="98e48-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98e48-136">입력</span><span class="sxs-lookup"><span data-stu-id="98e48-136">INPUTS</span></span>

### <span data-ttu-id="98e48-137">System.String</span><span class="sxs-lookup"><span data-stu-id="98e48-137">System.String</span></span>

### <span data-ttu-id="98e48-138">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="98e48-138">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="98e48-139">출력</span><span class="sxs-lookup"><span data-stu-id="98e48-139">OUTPUTS</span></span>

### <span data-ttu-id="98e48-140">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="98e48-140">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="98e48-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="98e48-141">NOTES</span></span>

## <span data-ttu-id="98e48-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="98e48-142">RELATED LINKS</span></span>
