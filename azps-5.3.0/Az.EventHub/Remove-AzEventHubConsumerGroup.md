---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/remove-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Remove-AzEventHubConsumerGroup.md
ms.openlocfilehash: f84464d366ae84cf0a83ecc616a80b90475af8d7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493035"
---
# <span data-ttu-id="b82bd-101">Remove-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="b82bd-101">Remove-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="b82bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b82bd-102">SYNOPSIS</span></span>
<span data-ttu-id="b82bd-103">지정된 Event Hubs 소비자 그룹을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="b82bd-103">Deletes the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="b82bd-104">구문</span><span class="sxs-lookup"><span data-stu-id="b82bd-104">SYNTAX</span></span>

### <span data-ttu-id="b82bd-105">ConsumergroupPropertiesSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="b82bd-105">ConsumergroupPropertiesSet (Default)</span></span>
```
Remove-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b82bd-106">ConsumergroupInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b82bd-106">ConsumergroupInputObjectSet</span></span>
```
Remove-AzEventHubConsumerGroup [-InputObject] <PSConsumerGroupAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b82bd-107">ConsumergroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b82bd-107">ConsumergroupResourceIdParameterSet</span></span>
```
Remove-AzEventHubConsumerGroup [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b82bd-108">설명</span><span class="sxs-lookup"><span data-stu-id="b82bd-108">DESCRIPTION</span></span>
<span data-ttu-id="b82bd-109">이 Remove-AzEventHubConsumerGroup cmdlet은 지정된 이벤트 허브에서 지정된 소비자 그룹을 제거하고 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="b82bd-109">The Remove-AzEventHubConsumerGroup cmdlet removes and deletes the specified consumer group from the given Event Hub.</span></span>

## <span data-ttu-id="b82bd-110">예제</span><span class="sxs-lookup"><span data-stu-id="b82bd-110">EXAMPLES</span></span>

### <span data-ttu-id="b82bd-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="b82bd-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyConsumerGroupName
```

<span data-ttu-id="b82bd-112">MyNamespaceName 네임스페이스로 범위가 지정되는 이벤트 허브 \` \` \` MyEventHubName에서 소비자 그룹 \` MyConsumerGroupName을 \` \` 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="b82bd-112">Deletes the consumer group \`MyConsumerGroupName\` from the Event Hub \`MyEventHubName\`, scoped to the \`MyNamespaceName\` namespace.</span></span>

### <span data-ttu-id="b82bd-113">예제 2: InputObject - 변수 사용</span><span class="sxs-lookup"><span data-stu-id="b82bd-113">Example 2: InputObject - Using Variable</span></span>
```powershell
PS C:\> $inputobject = Get-AzEventHubConsumerGroup <params>
PS C:\> Remove-AzEventHubConsumerGroup -InputObject $inputobject
```

### <span data-ttu-id="b82bd-114">예제 3: InputObject - 파이핑 사용</span><span class="sxs-lookup"><span data-stu-id="b82bd-114">Example 3: InputObject - Using Piping</span></span>
```powershell
PS C:\> Get-AzEventHubConsumerGroup <params> | Remove-AzEventHubConsumerGroup
```

### <span data-ttu-id="b82bd-115">예제 4: 변수를 사용하는 ResourceId</span><span class="sxs-lookup"><span data-stu-id="b82bd-115">Example 4: ResourceId Using Variable</span></span>
```powershell
PS C:\> $resourceid = Get-AzEventHubConsumerGroup <params>
PS C:\> Remove-AzEventHubConsumerGroup -ResourceId $resourceid.Id
```

### <span data-ttu-id="b82bd-116">예제 5: 문자열을 사용하는 ResourceId</span><span class="sxs-lookup"><span data-stu-id="b82bd-116">Example 5: ResourceId Using string</span></span>
```powershell
PS C:\> Remove-AzEventHubConsumerGroup -ResourceId "/subscriptions/xxx-xxxx-xxxxx-xxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName/consumergroups/ConsumerGroupName"
```

## <span data-ttu-id="b82bd-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b82bd-117">PARAMETERS</span></span>

### <span data-ttu-id="b82bd-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b82bd-118">-AsJob</span></span>
<span data-ttu-id="b82bd-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="b82bd-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b82bd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b82bd-120">-DefaultProfile</span></span>
<span data-ttu-id="b82bd-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b82bd-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b82bd-122">-EventHub</span><span class="sxs-lookup"><span data-stu-id="b82bd-122">-EventHub</span></span>
<span data-ttu-id="b82bd-123">EventHub 이름</span><span class="sxs-lookup"><span data-stu-id="b82bd-123">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: ConsumergroupPropertiesSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b82bd-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b82bd-124">-InputObject</span></span>
<span data-ttu-id="b82bd-125">ConsumerGroup 개체</span><span class="sxs-lookup"><span data-stu-id="b82bd-125">ConsumerGroup Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes
Parameter Sets: ConsumergroupInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b82bd-126">-Name</span><span class="sxs-lookup"><span data-stu-id="b82bd-126">-Name</span></span>
<span data-ttu-id="b82bd-127">ConsumerGroup 이름</span><span class="sxs-lookup"><span data-stu-id="b82bd-127">ConsumerGroup Name</span></span>

```yaml
Type: System.String
Parameter Sets: ConsumergroupPropertiesSet
Aliases: ConsumerGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b82bd-128">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b82bd-128">-Namespace</span></span>
<span data-ttu-id="b82bd-129">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="b82bd-129">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: ConsumergroupPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b82bd-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b82bd-130">-PassThru</span></span>
<span data-ttu-id="b82bd-131">명령이 성공하면 이를 지정하면 true가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="b82bd-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="b82bd-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b82bd-132">-ResourceGroupName</span></span>
<span data-ttu-id="b82bd-133">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="b82bd-133">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ConsumergroupPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b82bd-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b82bd-134">-ResourceId</span></span>
<span data-ttu-id="b82bd-135">ConsumerGroup 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="b82bd-135">ConsumerGroup Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ConsumergroupResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b82bd-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b82bd-136">-Confirm</span></span>
<span data-ttu-id="b82bd-137">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b82bd-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b82bd-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b82bd-138">-WhatIf</span></span>
<span data-ttu-id="b82bd-139">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b82bd-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b82bd-140">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b82bd-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b82bd-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b82bd-141">CommonParameters</span></span>
<span data-ttu-id="b82bd-142">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b82bd-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b82bd-143">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b82bd-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b82bd-144">입력</span><span class="sxs-lookup"><span data-stu-id="b82bd-144">INPUTS</span></span>

### <span data-ttu-id="b82bd-145">System.String</span><span class="sxs-lookup"><span data-stu-id="b82bd-145">System.String</span></span>

### <span data-ttu-id="b82bd-146">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="b82bd-146">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="b82bd-147">출력</span><span class="sxs-lookup"><span data-stu-id="b82bd-147">OUTPUTS</span></span>

### <span data-ttu-id="b82bd-148">System.Void</span><span class="sxs-lookup"><span data-stu-id="b82bd-148">System.Void</span></span>

## <span data-ttu-id="b82bd-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b82bd-149">NOTES</span></span>

## <span data-ttu-id="b82bd-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b82bd-150">RELATED LINKS</span></span>
