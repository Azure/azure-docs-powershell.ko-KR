---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubConsumerGroup.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: c8684e9af0bca55dca52f336a458f4c428ca67a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532280"
---
# <span data-ttu-id="27a07-101">Remove-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="27a07-101">Remove-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="27a07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27a07-102">SYNOPSIS</span></span>
<span data-ttu-id="27a07-103">지정 된 이벤트 허브 소비자 그룹을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="27a07-103">Deletes the specified Event Hubs consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27a07-104">구문과</span><span class="sxs-lookup"><span data-stu-id="27a07-104">SYNTAX</span></span>

```
Remove-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> -Namespace <String> -EventHub <String>
 -Name <String> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="27a07-105">설명은</span><span class="sxs-lookup"><span data-stu-id="27a07-105">DESCRIPTION</span></span>
<span data-ttu-id="27a07-106">Remove-AzureRmEventHubConsumerGroup cmdlet은 지정 된 이벤트 허브에서 지정한 소비자 그룹을 제거 하 고 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="27a07-106">The Remove-AzureRmEventHubConsumerGroup cmdlet removes and deletes the specified consumer group from the given Event Hub.</span></span>

## <span data-ttu-id="27a07-107">예제의</span><span class="sxs-lookup"><span data-stu-id="27a07-107">EXAMPLES</span></span>

### <span data-ttu-id="27a07-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="27a07-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyConsumerGroupName
```

<span data-ttu-id="27a07-109">\` \` \` \` MyNamespaceName 네임 스페이스로 범위가 지정 된 이벤트 허브 MyEventHubName에서 소비자 그룹 MyConsumerGroupName를 \` 삭제 \` 합니다.</span><span class="sxs-lookup"><span data-stu-id="27a07-109">Deletes the consumer group \`MyConsumerGroupName\` from the Event Hub \`MyEventHubName\`, scoped to the \`MyNamespaceName\` namespace.</span></span>

## <span data-ttu-id="27a07-110">변수</span><span class="sxs-lookup"><span data-stu-id="27a07-110">PARAMETERS</span></span>

### <span data-ttu-id="27a07-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27a07-111">-ResourceGroupName</span></span>
<span data-ttu-id="27a07-112">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="27a07-112">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27a07-113">-확인</span><span class="sxs-lookup"><span data-stu-id="27a07-113">-Confirm</span></span>
<span data-ttu-id="27a07-114">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="27a07-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27a07-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27a07-115">-WhatIf</span></span>
<span data-ttu-id="27a07-116">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="27a07-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27a07-117">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="27a07-117">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27a07-118">-EventHub</span><span class="sxs-lookup"><span data-stu-id="27a07-118">-EventHub</span></span>
<span data-ttu-id="27a07-119">EventHub 이름.</span><span class="sxs-lookup"><span data-stu-id="27a07-119">EventHub Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27a07-120">-이름</span><span class="sxs-lookup"><span data-stu-id="27a07-120">-Name</span></span>
<span data-ttu-id="27a07-121">ConsumerGroup 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="27a07-121">ConsumerGroup Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27a07-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="27a07-122">-Namespace</span></span>
<span data-ttu-id="27a07-123">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="27a07-123">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="27a07-124">입력</span><span class="sxs-lookup"><span data-stu-id="27a07-124">INPUTS</span></span>

### <span data-ttu-id="27a07-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="27a07-125">System.String</span></span>

## <span data-ttu-id="27a07-126">출력</span><span class="sxs-lookup"><span data-stu-id="27a07-126">OUTPUTS</span></span>

### <span data-ttu-id="27a07-127">System. 개체</span><span class="sxs-lookup"><span data-stu-id="27a07-127">System.Object</span></span>

## <span data-ttu-id="27a07-128">상속자</span><span class="sxs-lookup"><span data-stu-id="27a07-128">NOTES</span></span>

## <span data-ttu-id="27a07-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="27a07-129">RELATED LINKS</span></span>

