---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 4a2608ee3d3f874183a35fe6b81f7cd169123416
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537260"
---
# <span data-ttu-id="d81aa-101">Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="d81aa-101">Get-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="d81aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d81aa-102">SYNOPSIS</span></span>
<span data-ttu-id="d81aa-103">지정 된 이벤트 허브 소비자 그룹의 세부 정보를 가져오거나 이벤트 허브의 소비자 그룹 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d81aa-103">Gets the details of a specified Event Hubs consumer group, or gets a list of consumer groups in an Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d81aa-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d81aa-104">SYNTAX</span></span>

```
Get-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> -Namespace <String> -EventHub <String>
 [-Name <String>]
```

## <span data-ttu-id="d81aa-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d81aa-105">DESCRIPTION</span></span>
<span data-ttu-id="d81aa-106">Get-AzureRmEventHubConsumerGroup cmdlet은 지정 된 이벤트 허브 소비자 그룹 또는 지정 된 이벤트 허브의 소비자 그룹 목록에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d81aa-106">The Get-AzureRmEventHubConsumerGroup cmdlet gets either the details of a specified Event Hubs consumer group, or a list of consumer groups in a given Event Hub.</span></span>
<span data-ttu-id="d81aa-107">소비자 그룹의 이름을 제공 하는 경우 단일 소비자 그룹 세부 정보에 대 한 세부 정보가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d81aa-107">If the name of a consumer group is provided, the details of a single consumer group details are returned.</span></span>
<span data-ttu-id="d81aa-108">소비자 그룹의 이름을 제공 하지 않으면 지정 된 이벤트 허브의 소비자 그룹 목록이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d81aa-108">If the name of a consumer group is not provided, a list of consumer groups in the specified Event Hub is returned.</span></span>

## <span data-ttu-id="d81aa-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d81aa-109">EXAMPLES</span></span>

### <span data-ttu-id="d81aa-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="d81aa-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="d81aa-111">\` \` \` \` \` \` 리소스 그룹 MyResourceGroupName를 사용 하 여 네임 스페이스 MyNamespaceName에 \` 있는 이벤트 허브 MyEventHubName에서 \` 소비자 그룹 MyConsumerGroupName를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d81aa-111">Gets the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="d81aa-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="d81aa-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="d81aa-113">\` \` \` \` 리소스 그룹 MyResourceGroupName를 사용 하 여 네임 스페이스 MyNamespaceName에 \` 있는 이벤트 허브 MyEventHubName의 소비자 그룹 목록을 가져옵니다 \` .</span><span class="sxs-lookup"><span data-stu-id="d81aa-113">Gets a list of consumer groups in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="d81aa-114">변수</span><span class="sxs-lookup"><span data-stu-id="d81aa-114">PARAMETERS</span></span>

### <span data-ttu-id="d81aa-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d81aa-115">-ResourceGroupName</span></span>
<span data-ttu-id="d81aa-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d81aa-116">Resource group name.</span></span>

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

### <span data-ttu-id="d81aa-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="d81aa-117">-EventHub</span></span>
<span data-ttu-id="d81aa-118">EventHub 이름.</span><span class="sxs-lookup"><span data-stu-id="d81aa-118">EventHub Name.</span></span>

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

### <span data-ttu-id="d81aa-119">-이름</span><span class="sxs-lookup"><span data-stu-id="d81aa-119">-Name</span></span>
<span data-ttu-id="d81aa-120">ConsumerGroup 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d81aa-120">ConsumerGroup Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d81aa-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d81aa-121">-Namespace</span></span>
<span data-ttu-id="d81aa-122">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d81aa-122">Namespace Name.</span></span>

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

## <span data-ttu-id="d81aa-123">입력</span><span class="sxs-lookup"><span data-stu-id="d81aa-123">INPUTS</span></span>

### <span data-ttu-id="d81aa-124">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d81aa-124">System.String</span></span>

## <span data-ttu-id="d81aa-125">출력</span><span class="sxs-lookup"><span data-stu-id="d81aa-125">OUTPUTS</span></span>

### <span data-ttu-id="d81aa-126">System.webserver. List ' 1 [[Microsoft ConsumerGroupAttributes, Microsoft Azure. 0.0.1.0, Version =, Culture = 중립, PublicKeyToken = null]])</span><span class="sxs-lookup"><span data-stu-id="d81aa-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.ConsumerGroupAttributes, Microsoft.Azure.Commands.EventHub, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="d81aa-127">상속자</span><span class="sxs-lookup"><span data-stu-id="d81aa-127">NOTES</span></span>

## <span data-ttu-id="d81aa-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d81aa-128">RELATED LINKS</span></span>

