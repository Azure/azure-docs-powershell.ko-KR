---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubConsumerGroup.md
ms.openlocfilehash: fc108c633b70cc1eed32bcc0574ad25109a065fc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185945"
---
# <span data-ttu-id="3bbba-101">Get-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="3bbba-101">Get-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="3bbba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3bbba-102">SYNOPSIS</span></span>
<span data-ttu-id="3bbba-103">지정된 Event Hubs 소비자 그룹의 세부 정보를 얻거나 이벤트 허브에서 소비자 그룹 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3bbba-103">Gets the details of a specified Event Hubs consumer group, or gets a list of consumer groups in an Event Hub.</span></span>

## <span data-ttu-id="3bbba-104">구문</span><span class="sxs-lookup"><span data-stu-id="3bbba-104">SYNTAX</span></span>

```
Get-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3bbba-105">설명</span><span class="sxs-lookup"><span data-stu-id="3bbba-105">DESCRIPTION</span></span>
<span data-ttu-id="3bbba-106">Get-AzEventHubConsumerGroup cmdlet은 지정된 Event Hubs 소비자 그룹의 세부 정보 또는 지정된 이벤트 허브의 소비자 그룹 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3bbba-106">The Get-AzEventHubConsumerGroup cmdlet gets either the details of a specified Event Hubs consumer group, or a list of consumer groups in a given Event Hub.</span></span>
<span data-ttu-id="3bbba-107">소비자 그룹의 이름이 제공된 경우 단일 소비자 그룹 세부 정보의 세부 정보가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="3bbba-107">If the name of a consumer group is provided, the details of a single consumer group details are returned.</span></span>
<span data-ttu-id="3bbba-108">소비자 그룹의 이름이 제공되지 않으면 지정된 이벤트 허브의 소비자 그룹 목록이 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="3bbba-108">If the name of a consumer group is not provided, a list of consumer groups in the specified Event Hub is returned.</span></span>

## <span data-ttu-id="3bbba-109">예제</span><span class="sxs-lookup"><span data-stu-id="3bbba-109">EXAMPLES</span></span>

### <span data-ttu-id="3bbba-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="3bbba-110">Example 1</span></span>
```
PS C:\> Get-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="3bbba-111">리소스 그룹 \` \` \` MyResourceGroupName이 있는 MyNamespaceName 네임스페이스에 있는 이벤트 허브 MyEventHubName에서 소비자 그룹 \` \` \` \` MyConsumerGroupName을 \` 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3bbba-111">Gets the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="3bbba-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="3bbba-112">Example 2</span></span>
```
PS C:\> Get-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="3bbba-113">리소스 그룹 \` \` \` \` \` MyResourceGroupName이 있는 MyNamespaceName 네임스페이스에 있는 이벤트 허브 MyEventHubName의 소비자 그룹 목록을 \` 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="3bbba-113">Gets a list of consumer groups in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="3bbba-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3bbba-114">PARAMETERS</span></span>

### <span data-ttu-id="3bbba-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bbba-115">-DefaultProfile</span></span>
<span data-ttu-id="3bbba-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3bbba-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bbba-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="3bbba-117">-EventHub</span></span>
<span data-ttu-id="3bbba-118">EventHub 이름</span><span class="sxs-lookup"><span data-stu-id="3bbba-118">EventHub Name</span></span>

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

### <span data-ttu-id="3bbba-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="3bbba-119">-MaxCount</span></span>
<span data-ttu-id="3bbba-120">반환할 ConsumerGroup의 최대 수를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3bbba-120">Determine the maximum number of ConsumerGroups  to return.</span></span>

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

### <span data-ttu-id="3bbba-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3bbba-121">-Name</span></span>
<span data-ttu-id="3bbba-122">ConsumerGroup 이름</span><span class="sxs-lookup"><span data-stu-id="3bbba-122">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="3bbba-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3bbba-123">-Namespace</span></span>
<span data-ttu-id="3bbba-124">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="3bbba-124">Namespace Name</span></span>

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

### <span data-ttu-id="3bbba-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bbba-125">-ResourceGroupName</span></span>
<span data-ttu-id="3bbba-126">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="3bbba-126">Resource Group Name</span></span>

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

### <span data-ttu-id="3bbba-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bbba-127">CommonParameters</span></span>
<span data-ttu-id="3bbba-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3bbba-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bbba-129">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="3bbba-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bbba-130">입력</span><span class="sxs-lookup"><span data-stu-id="3bbba-130">INPUTS</span></span>

### <span data-ttu-id="3bbba-131">System.String</span><span class="sxs-lookup"><span data-stu-id="3bbba-131">System.String</span></span>

## <span data-ttu-id="3bbba-132">출력</span><span class="sxs-lookup"><span data-stu-id="3bbba-132">OUTPUTS</span></span>

### <span data-ttu-id="3bbba-133">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="3bbba-133">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="3bbba-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3bbba-134">NOTES</span></span>

## <span data-ttu-id="3bbba-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3bbba-135">RELATED LINKS</span></span>
