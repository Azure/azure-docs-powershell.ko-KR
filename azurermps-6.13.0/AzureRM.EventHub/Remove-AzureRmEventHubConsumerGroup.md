---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: 2ef6227acf398b228d6ca5ffe4fad3d39ec75723
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530345"
---
# <span data-ttu-id="24b87-101">Remove-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="24b87-101">Remove-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="24b87-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24b87-102">SYNOPSIS</span></span>
<span data-ttu-id="24b87-103">지정 된 이벤트 허브 소비자 그룹을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="24b87-103">Deletes the specified Event Hubs consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24b87-104">구문과</span><span class="sxs-lookup"><span data-stu-id="24b87-104">SYNTAX</span></span>

### <span data-ttu-id="24b87-105">ConsumergroupPropertiesSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="24b87-105">ConsumergroupPropertiesSet (Default)</span></span>
```
Remove-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="24b87-106">ConsumergroupInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="24b87-106">ConsumergroupInputObjectSet</span></span>
```
Remove-AzureRmEventHubConsumerGroup [-InputObject] <PSConsumerGroupAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24b87-107">ConsumergroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="24b87-107">ConsumergroupResourceIdParameterSet</span></span>
```
Remove-AzureRmEventHubConsumerGroup [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24b87-108">설명은</span><span class="sxs-lookup"><span data-stu-id="24b87-108">DESCRIPTION</span></span>
<span data-ttu-id="24b87-109">Remove-AzureRmEventHubConsumerGroup cmdlet은 지정 된 이벤트 허브에서 지정한 소비자 그룹을 제거 하 고 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="24b87-109">The Remove-AzureRmEventHubConsumerGroup cmdlet removes and deletes the specified consumer group from the given Event Hub.</span></span>

## <span data-ttu-id="24b87-110">예제의</span><span class="sxs-lookup"><span data-stu-id="24b87-110">EXAMPLES</span></span>

### <span data-ttu-id="24b87-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="24b87-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyConsumerGroupName
```

<span data-ttu-id="24b87-112">\` \` \` \` MyNamespaceName 네임 스페이스로 범위가 지정 된 이벤트 허브 MyEventHubName에서 소비자 그룹 MyConsumerGroupName를 \` 삭제 \` 합니다.</span><span class="sxs-lookup"><span data-stu-id="24b87-112">Deletes the consumer group \`MyConsumerGroupName\` from the Event Hub \`MyEventHubName\`, scoped to the \`MyNamespaceName\` namespace.</span></span>

### <span data-ttu-id="24b87-113">예제 2.1-InputObject-Using 변수</span><span class="sxs-lookup"><span data-stu-id="24b87-113">Example 2.1 - InputObject - Using Variable</span></span>
```
PS C:\> $inputobject = Get-AzureRmEventHubConsumerGroup <params>
PS C:\> Remove-AzureRmEventHubConsumerGroup -InputObject $inputobject
```

### <span data-ttu-id="24b87-114">예제 2.2-InputObject-Using 파이핑</span><span class="sxs-lookup"><span data-stu-id="24b87-114">Example 2.2 - InputObject - Using Piping</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup <params> | Remove-AzureRmEventHubConsumerGroup
```

### <span data-ttu-id="24b87-115">예제 3.1-Vairable를 사용 하는 ResourceId</span><span class="sxs-lookup"><span data-stu-id="24b87-115">Example 3.1 - ResourceId Using Vairable</span></span>
```
PS C:\> $resourceid = Get-AzureRmEventHubConsumerGroup <params>
PS C:\> Remove-AzureRmEventHubConsumerGroup -ResourceId $resourceid.Id
```

### <span data-ttu-id="24b87-116">예제 3.2-문자열을 사용 하는 ResourceId</span><span class="sxs-lookup"><span data-stu-id="24b87-116">Example 3.2 - ResourceId Using string</span></span>
```
PS C:\> Remove-AzureRmEventHubConsumerGroup -ResourceId "/subscriptions/xxx-xxxx-xxxxx-xxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.EventHub/namespaces/NamespaceName/eventhubs/EventHubName/consumergroups/ConsumerGroupName"
```

## <span data-ttu-id="24b87-117">변수</span><span class="sxs-lookup"><span data-stu-id="24b87-117">PARAMETERS</span></span>

### <span data-ttu-id="24b87-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="24b87-118">-AsJob</span></span>
<span data-ttu-id="24b87-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="24b87-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="24b87-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24b87-120">-DefaultProfile</span></span>
<span data-ttu-id="24b87-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="24b87-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24b87-122">-EventHub</span><span class="sxs-lookup"><span data-stu-id="24b87-122">-EventHub</span></span>
<span data-ttu-id="24b87-123">EventHub 이름</span><span class="sxs-lookup"><span data-stu-id="24b87-123">EventHub Name</span></span>

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

### <span data-ttu-id="24b87-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24b87-124">-InputObject</span></span>
<span data-ttu-id="24b87-125">ConsumerGroup 개체</span><span class="sxs-lookup"><span data-stu-id="24b87-125">ConsumerGroup Object</span></span>

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

### <span data-ttu-id="24b87-126">-이름</span><span class="sxs-lookup"><span data-stu-id="24b87-126">-Name</span></span>
<span data-ttu-id="24b87-127">ConsumerGroup 이름</span><span class="sxs-lookup"><span data-stu-id="24b87-127">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="24b87-128">-Namespace</span><span class="sxs-lookup"><span data-stu-id="24b87-128">-Namespace</span></span>
<span data-ttu-id="24b87-129">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="24b87-129">Namespace Name</span></span>

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

### <span data-ttu-id="24b87-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="24b87-130">-PassThru</span></span>
<span data-ttu-id="24b87-131">명령이 성공적으로 실행 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="24b87-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="24b87-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24b87-132">-ResourceGroupName</span></span>
<span data-ttu-id="24b87-133">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="24b87-133">Resource Group Name</span></span>

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

### <span data-ttu-id="24b87-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="24b87-134">-ResourceId</span></span>
<span data-ttu-id="24b87-135">ConsumerGroup 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="24b87-135">ConsumerGroup Resource Id</span></span>

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

### <span data-ttu-id="24b87-136">-확인</span><span class="sxs-lookup"><span data-stu-id="24b87-136">-Confirm</span></span>
<span data-ttu-id="24b87-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="24b87-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24b87-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24b87-138">-WhatIf</span></span>
<span data-ttu-id="24b87-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="24b87-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24b87-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="24b87-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24b87-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24b87-141">CommonParameters</span></span>
<span data-ttu-id="24b87-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="24b87-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24b87-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24b87-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24b87-144">입력</span><span class="sxs-lookup"><span data-stu-id="24b87-144">INPUTS</span></span>

### <span data-ttu-id="24b87-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="24b87-145">System.String</span></span>

### <span data-ttu-id="24b87-146">PSConsumerGroupAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="24b87-146">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>
<span data-ttu-id="24b87-147">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="24b87-147">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="24b87-148">출력</span><span class="sxs-lookup"><span data-stu-id="24b87-148">OUTPUTS</span></span>

### <span data-ttu-id="24b87-149">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="24b87-149">System.Void</span></span>

## <span data-ttu-id="24b87-150">상속자</span><span class="sxs-lookup"><span data-stu-id="24b87-150">NOTES</span></span>

## <span data-ttu-id="24b87-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="24b87-151">RELATED LINKS</span></span>
