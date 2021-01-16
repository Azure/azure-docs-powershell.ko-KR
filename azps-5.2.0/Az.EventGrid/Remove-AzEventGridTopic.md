---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridTopic.md
ms.openlocfilehash: bd60a5c57f72fd6fd5eae9dffbbdb7bea0752343
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341414"
---
# <span data-ttu-id="ee1a5-101">Remove-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="ee1a5-101">Remove-AzEventGridTopic</span></span>

## <span data-ttu-id="ee1a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee1a5-102">SYNOPSIS</span></span>
<span data-ttu-id="ee1a5-103">Azure Event Grid 토픽을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ee1a5-103">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="ee1a5-104">구문</span><span class="sxs-lookup"><span data-stu-id="ee1a5-104">SYNTAX</span></span>

### <span data-ttu-id="ee1a5-105">TopicNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="ee1a5-105">TopicNameParameterSet (Default)</span></span>
```
Remove-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee1a5-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee1a5-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee1a5-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee1a5-107">TopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridTopic [-InputObject] <PSTopic> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee1a5-108">설명</span><span class="sxs-lookup"><span data-stu-id="ee1a5-108">DESCRIPTION</span></span>
<span data-ttu-id="ee1a5-109">Azure Event Grid 토픽을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ee1a5-109">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="ee1a5-110">예제</span><span class="sxs-lookup"><span data-stu-id="ee1a5-110">EXAMPLES</span></span>

### <span data-ttu-id="ee1a5-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="ee1a5-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1
```

<span data-ttu-id="ee1a5-112">리소스 그룹 \` \` \` MyResourceGroupName에서 Event Grid 항목 Topic1을 \` 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ee1a5-112">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="ee1a5-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="ee1a5-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1" | Remove-AzEventGridTopic
```

<span data-ttu-id="ee1a5-114">리소스 그룹 \` \` \` MyResourceGroupName에서 Event Grid 항목 Topic1을 \` 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ee1a5-114">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="ee1a5-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee1a5-115">PARAMETERS</span></span>

### <span data-ttu-id="ee1a5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee1a5-116">-DefaultProfile</span></span>
<span data-ttu-id="ee1a5-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ee1a5-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ee1a5-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee1a5-118">-InputObject</span></span>
<span data-ttu-id="ee1a5-119">EventGrid 토픽 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ee1a5-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="ee1a5-120">-Name</span><span class="sxs-lookup"><span data-stu-id="ee1a5-120">-Name</span></span>
<span data-ttu-id="ee1a5-121">EventGrid 토픽 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ee1a5-121">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee1a5-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ee1a5-122">-PassThru</span></span>
<span data-ttu-id="ee1a5-123">제거 작업의 상태를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ee1a5-123">Returns the status of the Remove operation.</span></span> <span data-ttu-id="ee1a5-124">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ee1a5-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ee1a5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee1a5-125">-ResourceGroupName</span></span>
<span data-ttu-id="ee1a5-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ee1a5-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="ee1a5-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee1a5-127">-ResourceId</span></span>
<span data-ttu-id="ee1a5-128">EventGrid 토픽 ResourceID.</span><span class="sxs-lookup"><span data-stu-id="ee1a5-128">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="ee1a5-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ee1a5-129">-Confirm</span></span>
<span data-ttu-id="ee1a5-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ee1a5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee1a5-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee1a5-131">-WhatIf</span></span>
<span data-ttu-id="ee1a5-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ee1a5-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee1a5-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ee1a5-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee1a5-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee1a5-134">CommonParameters</span></span>
<span data-ttu-id="ee1a5-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ee1a5-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee1a5-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ee1a5-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee1a5-137">입력</span><span class="sxs-lookup"><span data-stu-id="ee1a5-137">INPUTS</span></span>

### <span data-ttu-id="ee1a5-138">System.String</span><span class="sxs-lookup"><span data-stu-id="ee1a5-138">System.String</span></span>

### <span data-ttu-id="ee1a5-139">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="ee1a5-139">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="ee1a5-140">출력</span><span class="sxs-lookup"><span data-stu-id="ee1a5-140">OUTPUTS</span></span>

### <span data-ttu-id="ee1a5-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ee1a5-141">System.Boolean</span></span>

## <span data-ttu-id="ee1a5-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ee1a5-142">NOTES</span></span>

## <span data-ttu-id="ee1a5-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ee1a5-143">RELATED LINKS</span></span>