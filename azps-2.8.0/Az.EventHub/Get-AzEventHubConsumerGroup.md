---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubConsumerGroup.md
ms.openlocfilehash: 7f10df478851679afeb73157252d954f756f0c4c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696496"
---
# <span data-ttu-id="b96e4-101">Get-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="b96e4-101">Get-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="b96e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b96e4-102">SYNOPSIS</span></span>
<span data-ttu-id="b96e4-103">지정 된 이벤트 허브 소비자 그룹의 세부 정보를 가져오거나 이벤트 허브의 소비자 그룹 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b96e4-103">Gets the details of a specified Event Hubs consumer group, or gets a list of consumer groups in an Event Hub.</span></span>

## <span data-ttu-id="b96e4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b96e4-104">SYNTAX</span></span>

```
Get-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b96e4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b96e4-105">DESCRIPTION</span></span>
<span data-ttu-id="b96e4-106">Get-AzEventHubConsumerGroup cmdlet은 지정 된 이벤트 허브 소비자 그룹 또는 지정 된 이벤트 허브의 소비자 그룹 목록에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b96e4-106">The Get-AzEventHubConsumerGroup cmdlet gets either the details of a specified Event Hubs consumer group, or a list of consumer groups in a given Event Hub.</span></span>
<span data-ttu-id="b96e4-107">소비자 그룹의 이름을 제공 하는 경우 단일 소비자 그룹 세부 정보에 대 한 세부 정보가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b96e4-107">If the name of a consumer group is provided, the details of a single consumer group details are returned.</span></span>
<span data-ttu-id="b96e4-108">소비자 그룹의 이름을 제공 하지 않으면 지정 된 이벤트 허브의 소비자 그룹 목록이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b96e4-108">If the name of a consumer group is not provided, a list of consumer groups in the specified Event Hub is returned.</span></span>

## <span data-ttu-id="b96e4-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b96e4-109">EXAMPLES</span></span>

### <span data-ttu-id="b96e4-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="b96e4-110">Example 1</span></span>
```
PS C:\> Get-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="b96e4-111">\` \` \` \` \` \` 리소스 그룹 MyResourceGroupName를 사용 하 여 네임 스페이스 MyNamespaceName에 \` 있는 이벤트 허브 MyEventHubName에서 \` 소비자 그룹 MyConsumerGroupName를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b96e4-111">Gets the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="b96e4-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="b96e4-112">Example 2</span></span>
```
PS C:\> Get-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="b96e4-113">\` \` \` \` 리소스 그룹 MyResourceGroupName를 사용 하 여 네임 스페이스 MyNamespaceName에 \` 있는 이벤트 허브 MyEventHubName의 소비자 그룹 목록을 가져옵니다 \` .</span><span class="sxs-lookup"><span data-stu-id="b96e4-113">Gets a list of consumer groups in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="b96e4-114">변수</span><span class="sxs-lookup"><span data-stu-id="b96e4-114">PARAMETERS</span></span>

### <span data-ttu-id="b96e4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b96e4-115">-DefaultProfile</span></span>
<span data-ttu-id="b96e4-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b96e4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b96e4-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="b96e4-117">-EventHub</span></span>
<span data-ttu-id="b96e4-118">EventHub 이름</span><span class="sxs-lookup"><span data-stu-id="b96e4-118">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b96e4-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="b96e4-119">-MaxCount</span></span>
<span data-ttu-id="b96e4-120">반환할 최대 ConsumerGroups 수를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b96e4-120">Determine the maximum number of ConsumerGroups  to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b96e4-121">-이름</span><span class="sxs-lookup"><span data-stu-id="b96e4-121">-Name</span></span>
<span data-ttu-id="b96e4-122">ConsumerGroup 이름</span><span class="sxs-lookup"><span data-stu-id="b96e4-122">ConsumerGroup Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b96e4-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b96e4-123">-Namespace</span></span>
<span data-ttu-id="b96e4-124">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="b96e4-124">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b96e4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b96e4-125">-ResourceGroupName</span></span>
<span data-ttu-id="b96e4-126">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="b96e4-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b96e4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b96e4-127">CommonParameters</span></span>
<span data-ttu-id="b96e4-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b96e4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b96e4-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b96e4-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b96e4-130">입력</span><span class="sxs-lookup"><span data-stu-id="b96e4-130">INPUTS</span></span>

### <span data-ttu-id="b96e4-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b96e4-131">System.String</span></span>

## <span data-ttu-id="b96e4-132">출력</span><span class="sxs-lookup"><span data-stu-id="b96e4-132">OUTPUTS</span></span>

### <span data-ttu-id="b96e4-133">PSConsumerGroupAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="b96e4-133">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="b96e4-134">상속자</span><span class="sxs-lookup"><span data-stu-id="b96e4-134">NOTES</span></span>

## <span data-ttu-id="b96e4-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b96e4-135">RELATED LINKS</span></span>
