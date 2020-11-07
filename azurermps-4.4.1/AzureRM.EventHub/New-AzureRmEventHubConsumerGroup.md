---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubConsumerGroup.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: bcd20fc9c6f0c08af2ae735558a6fccc6c9814d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711573"
---
# <span data-ttu-id="e5c27-101">New-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="e5c27-101">New-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="e5c27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5c27-102">SYNOPSIS</span></span>
<span data-ttu-id="e5c27-103">지정 된 이벤트 허브에 대 한 새 소비자 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e5c27-103">Creates a new consumer group for the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e5c27-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e5c27-104">SYNTAX</span></span>

```
New-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> -Namespace <String> -EventHub <String>
 -Name <String> [[-UserMetadata] <String>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="e5c27-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e5c27-105">DESCRIPTION</span></span>
<span data-ttu-id="e5c27-106">New-AzureRmEventHubConsumerGroup cmdlet은 지정 된 이벤트 허브에 대 한 새 소비자 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e5c27-106">The New-AzureRmEventHubConsumerGroup cmdlet creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="e5c27-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e5c27-107">EXAMPLES</span></span>

### <span data-ttu-id="e5c27-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e5c27-108">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="e5c27-109">\` \` \` \` \` 리소스 그룹 MyResourceGroupName를 사용 하 여 네임 스페이스 MyNamespaceName 범위에 \` \` 있는 이벤트 허브 MyEventHubName에서 \` 소비자 그룹 MyConsumerGroupName를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e5c27-109">Creates the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, scoped to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="e5c27-110">변수</span><span class="sxs-lookup"><span data-stu-id="e5c27-110">PARAMETERS</span></span>

### <span data-ttu-id="e5c27-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5c27-111">-ResourceGroupName</span></span>
<span data-ttu-id="e5c27-112">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e5c27-112">Resource group name.</span></span>

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

### <span data-ttu-id="e5c27-113">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="e5c27-113">-UserMetadata</span></span>
<span data-ttu-id="e5c27-114">소비자 그룹의 사용자 메타 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="e5c27-114">User metadata for the consumer group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e5c27-115">-확인</span><span class="sxs-lookup"><span data-stu-id="e5c27-115">-Confirm</span></span>
<span data-ttu-id="e5c27-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e5c27-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5c27-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5c27-117">-WhatIf</span></span>
<span data-ttu-id="e5c27-118">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e5c27-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5c27-119">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e5c27-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5c27-120">-EventHub</span><span class="sxs-lookup"><span data-stu-id="e5c27-120">-EventHub</span></span>
<span data-ttu-id="e5c27-121">EventHub 이름.</span><span class="sxs-lookup"><span data-stu-id="e5c27-121">EventHub Name.</span></span>

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

### <span data-ttu-id="e5c27-122">-이름</span><span class="sxs-lookup"><span data-stu-id="e5c27-122">-Name</span></span>
<span data-ttu-id="e5c27-123">ConsumerGroup 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e5c27-123">ConsumerGroup Name.</span></span>

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

### <span data-ttu-id="e5c27-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e5c27-124">-Namespace</span></span>
<span data-ttu-id="e5c27-125">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e5c27-125">Namespace Name.</span></span>

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

## <span data-ttu-id="e5c27-126">입력</span><span class="sxs-lookup"><span data-stu-id="e5c27-126">INPUTS</span></span>

### <span data-ttu-id="e5c27-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e5c27-127">System.String</span></span>

## <span data-ttu-id="e5c27-128">출력</span><span class="sxs-lookup"><span data-stu-id="e5c27-128">OUTPUTS</span></span>

### <span data-ttu-id="e5c27-129">ConsumerGroupAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="e5c27-129">Microsoft.Azure.Commands.EventHub.Models.ConsumerGroupAttributes</span></span>

## <span data-ttu-id="e5c27-130">상속자</span><span class="sxs-lookup"><span data-stu-id="e5c27-130">NOTES</span></span>

## <span data-ttu-id="e5c27-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e5c27-131">RELATED LINKS</span></span>

