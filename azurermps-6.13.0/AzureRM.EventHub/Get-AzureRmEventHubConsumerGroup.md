---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: 205dc883f8f6e0481f88438137ca45ad7a99c4ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702939"
---
# <span data-ttu-id="277ae-101">Get-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="277ae-101">Get-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="277ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="277ae-102">SYNOPSIS</span></span>
<span data-ttu-id="277ae-103">지정 된 이벤트 허브 소비자 그룹의 세부 정보를 가져오거나 이벤트 허브의 소비자 그룹 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="277ae-103">Gets the details of a specified Event Hubs consumer group, or gets a list of consumer groups in an Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="277ae-104">구문과</span><span class="sxs-lookup"><span data-stu-id="277ae-104">SYNTAX</span></span>

```
Get-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="277ae-105">설명은</span><span class="sxs-lookup"><span data-stu-id="277ae-105">DESCRIPTION</span></span>
<span data-ttu-id="277ae-106">Get-AzureRmEventHubConsumerGroup cmdlet은 지정 된 이벤트 허브 소비자 그룹 또는 지정 된 이벤트 허브의 소비자 그룹 목록에 대 한 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="277ae-106">The Get-AzureRmEventHubConsumerGroup cmdlet gets either the details of a specified Event Hubs consumer group, or a list of consumer groups in a given Event Hub.</span></span>
<span data-ttu-id="277ae-107">소비자 그룹의 이름을 제공 하는 경우 단일 소비자 그룹 세부 정보에 대 한 세부 정보가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="277ae-107">If the name of a consumer group is provided, the details of a single consumer group details are returned.</span></span>
<span data-ttu-id="277ae-108">소비자 그룹의 이름을 제공 하지 않으면 지정 된 이벤트 허브의 소비자 그룹 목록이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="277ae-108">If the name of a consumer group is not provided, a list of consumer groups in the specified Event Hub is returned.</span></span>

## <span data-ttu-id="277ae-109">예제의</span><span class="sxs-lookup"><span data-stu-id="277ae-109">EXAMPLES</span></span>

### <span data-ttu-id="277ae-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="277ae-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="277ae-111">\` \` \` \` \` \` 리소스 그룹 MyResourceGroupName를 사용 하 여 네임 스페이스 MyNamespaceName에 \` 있는 이벤트 허브 MyEventHubName에서 \` 소비자 그룹 MyConsumerGroupName를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="277ae-111">Gets the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="277ae-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="277ae-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="277ae-113">\` \` \` \` 리소스 그룹 MyResourceGroupName를 사용 하 여 네임 스페이스 MyNamespaceName에 \` 있는 이벤트 허브 MyEventHubName의 소비자 그룹 목록을 가져옵니다 \` .</span><span class="sxs-lookup"><span data-stu-id="277ae-113">Gets a list of consumer groups in the Event Hub \`MyEventHubName\`, which exists in the namespace \`MyNamespaceName\` with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="277ae-114">변수</span><span class="sxs-lookup"><span data-stu-id="277ae-114">PARAMETERS</span></span>

### <span data-ttu-id="277ae-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="277ae-115">-DefaultProfile</span></span>
<span data-ttu-id="277ae-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="277ae-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="277ae-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="277ae-117">-EventHub</span></span>
<span data-ttu-id="277ae-118">EventHub 이름</span><span class="sxs-lookup"><span data-stu-id="277ae-118">EventHub Name</span></span>

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

### <span data-ttu-id="277ae-119">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="277ae-119">-MaxCount</span></span>
<span data-ttu-id="277ae-120">반환할 최대 ConsumerGroups 수를 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="277ae-120">Determine the maximum number of ConsumerGroups  to return.</span></span>

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

### <span data-ttu-id="277ae-121">-이름</span><span class="sxs-lookup"><span data-stu-id="277ae-121">-Name</span></span>
<span data-ttu-id="277ae-122">ConsumerGroup 이름</span><span class="sxs-lookup"><span data-stu-id="277ae-122">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="277ae-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="277ae-123">-Namespace</span></span>
<span data-ttu-id="277ae-124">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="277ae-124">Namespace Name</span></span>

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

### <span data-ttu-id="277ae-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="277ae-125">-ResourceGroupName</span></span>
<span data-ttu-id="277ae-126">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="277ae-126">Resource Group Name</span></span>

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

### <span data-ttu-id="277ae-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="277ae-127">CommonParameters</span></span>
<span data-ttu-id="277ae-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="277ae-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="277ae-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="277ae-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="277ae-130">입력</span><span class="sxs-lookup"><span data-stu-id="277ae-130">INPUTS</span></span>

### <span data-ttu-id="277ae-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="277ae-131">System.String</span></span>

## <span data-ttu-id="277ae-132">출력</span><span class="sxs-lookup"><span data-stu-id="277ae-132">OUTPUTS</span></span>

### <span data-ttu-id="277ae-133">PSConsumerGroupAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="277ae-133">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="277ae-134">상속자</span><span class="sxs-lookup"><span data-stu-id="277ae-134">NOTES</span></span>

## <span data-ttu-id="277ae-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="277ae-135">RELATED LINKS</span></span>
