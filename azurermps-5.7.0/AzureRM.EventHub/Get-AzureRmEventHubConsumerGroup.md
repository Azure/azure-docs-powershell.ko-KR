---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: 445d20453b9f3d99e4ff5c72e118b287f0a83898
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534820"
---
# <span data-ttu-id="7a7c9-101">Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="7a7c9-101">Get-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="7a7c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a7c9-102">SYNOPSIS</span></span>
<span data-ttu-id="7a7c9-103">지정 된 이벤트 허브 소비자 그룹의 세부 정보를 가져오거나 이벤트 허브의 소비자 그룹 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7a7c9-103">Gets the details of a specified Event Hubs consumer group, or gets a list of consumer groups in an Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a7c9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7a7c9-104">SYNTAX</span></span>

```
Get-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a7c9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7a7c9-105">DESCRIPTION</span></span>
<span data-ttu-id="7a7c9-106">Get-AzureRmEventHubConsumerGroup cmdlet은 지정 된 이벤트 허브 소비자 그룹 또는 지정 된 이벤트 허브의 소비자 그룹 목록에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7a7c9-106">The Get-AzureRmEventHubConsumerGroup cmdlet gets either the details of a specified Event Hubs consumer group, or a list of consumer groups in a given Event Hub.</span></span>
<span data-ttu-id="7a7c9-107">소비자 그룹의 이름을 제공 하는 경우 단일 소비자 그룹 세부 정보에 대 한 세부 정보가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a7c9-107">If the name of a consumer group is provided, the details of a single consumer group details are returned.</span></span>
<span data-ttu-id="7a7c9-108">소비자 그룹의 이름을 제공 하지 않으면 지정 된 이벤트 허브의 소비자 그룹 목록이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a7c9-108">If the name of a consumer group is not provided, a list of consumer groups in the specified Event Hub is returned.</span></span>

## <span data-ttu-id="7a7c9-109">예제의</span><span class="sxs-lookup"><span data-stu-id="7a7c9-109">EXAMPLES</span></span>

### <span data-ttu-id="7a7c9-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="7a7c9-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="7a7c9-111">\` \` \` \` \` \` 리소스 그룹 MyResourceGroupName를 사용 하 여 네임 스페이스 MyNamespaceName에 \` 있는 이벤트 허브 MyEventHubName에서 \` 소비자 그룹 MyConsumerGroupName를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7a7c9-111">Gets the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="7a7c9-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="7a7c9-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="7a7c9-113">\` \` \` \` 리소스 그룹 MyResourceGroupName를 사용 하 여 네임 스페이스 MyNamespaceName에 \` 있는 이벤트 허브 MyEventHubName의 소비자 그룹 목록을 가져옵니다 \` .</span><span class="sxs-lookup"><span data-stu-id="7a7c9-113">Gets a list of consumer groups in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="7a7c9-114">변수</span><span class="sxs-lookup"><span data-stu-id="7a7c9-114">PARAMETERS</span></span>

### <span data-ttu-id="7a7c9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a7c9-115">-DefaultProfile</span></span>
<span data-ttu-id="7a7c9-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7a7c9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a7c9-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="7a7c9-117">-EventHub</span></span>
<span data-ttu-id="7a7c9-118">EventHub 이름</span><span class="sxs-lookup"><span data-stu-id="7a7c9-118">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a7c9-119">-이름</span><span class="sxs-lookup"><span data-stu-id="7a7c9-119">-Name</span></span>
<span data-ttu-id="7a7c9-120">ConsumerGroup 이름</span><span class="sxs-lookup"><span data-stu-id="7a7c9-120">ConsumerGroup Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a7c9-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7a7c9-121">-Namespace</span></span>
<span data-ttu-id="7a7c9-122">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="7a7c9-122">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a7c9-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a7c9-123">-ResourceGroupName</span></span>
<span data-ttu-id="7a7c9-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="7a7c9-124">Resource Group Name</span></span>

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

### <span data-ttu-id="7a7c9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a7c9-125">CommonParameters</span></span>
<span data-ttu-id="7a7c9-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7a7c9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="7a7c9-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a7c9-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a7c9-128">입력</span><span class="sxs-lookup"><span data-stu-id="7a7c9-128">INPUTS</span></span>

### <span data-ttu-id="7a7c9-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7a7c9-129">System.String</span></span>


## <span data-ttu-id="7a7c9-130">출력</span><span class="sxs-lookup"><span data-stu-id="7a7c9-130">OUTPUTS</span></span>

### <span data-ttu-id="7a7c9-131">System.webserver. List ' 1 [[Microsoft PSConsumerGroupAttributes, Microsoft Azure. 0.5.0.0, Version =, Culture = 중립, PublicKeyToken = null]])</span><span class="sxs-lookup"><span data-stu-id="7a7c9-131">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes, Microsoft.Azure.Commands.EventHub, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="7a7c9-132">상속자</span><span class="sxs-lookup"><span data-stu-id="7a7c9-132">NOTES</span></span>

## <span data-ttu-id="7a7c9-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7a7c9-133">RELATED LINKS</span></span>
