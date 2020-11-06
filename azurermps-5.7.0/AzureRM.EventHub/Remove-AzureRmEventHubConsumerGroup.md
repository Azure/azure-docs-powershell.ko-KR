---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/remove-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: 5b88ce6edc92cb6483b8d6df95599fcea854f805
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530534"
---
# <span data-ttu-id="34938-101">Remove-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="34938-101">Remove-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="34938-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34938-102">SYNOPSIS</span></span>
<span data-ttu-id="34938-103">지정 된 이벤트 허브 소비자 그룹을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="34938-103">Deletes the specified Event Hubs consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="34938-104">구문과</span><span class="sxs-lookup"><span data-stu-id="34938-104">SYNTAX</span></span>

```
Remove-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34938-105">설명은</span><span class="sxs-lookup"><span data-stu-id="34938-105">DESCRIPTION</span></span>
<span data-ttu-id="34938-106">Remove-AzureRmEventHubConsumerGroup cmdlet은 지정 된 이벤트 허브에서 지정한 소비자 그룹을 제거 하 고 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="34938-106">The Remove-AzureRmEventHubConsumerGroup cmdlet removes and deletes the specified consumer group from the given Event Hub.</span></span>

## <span data-ttu-id="34938-107">예제의</span><span class="sxs-lookup"><span data-stu-id="34938-107">EXAMPLES</span></span>

### <span data-ttu-id="34938-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="34938-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyConsumerGroupName
```

<span data-ttu-id="34938-109">\` \` \` \` MyNamespaceName 네임 스페이스로 범위가 지정 된 이벤트 허브 MyEventHubName에서 소비자 그룹 MyConsumerGroupName를 \` 삭제 \` 합니다.</span><span class="sxs-lookup"><span data-stu-id="34938-109">Deletes the consumer group \`MyConsumerGroupName\` from the Event Hub \`MyEventHubName\`, scoped to the \`MyNamespaceName\` namespace.</span></span>

## <span data-ttu-id="34938-110">변수</span><span class="sxs-lookup"><span data-stu-id="34938-110">PARAMETERS</span></span>

### <span data-ttu-id="34938-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34938-111">-DefaultProfile</span></span>
<span data-ttu-id="34938-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="34938-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34938-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="34938-113">-EventHub</span></span>
<span data-ttu-id="34938-114">EventHub 이름</span><span class="sxs-lookup"><span data-stu-id="34938-114">EventHub Name</span></span>

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

### <span data-ttu-id="34938-115">-이름</span><span class="sxs-lookup"><span data-stu-id="34938-115">-Name</span></span>
<span data-ttu-id="34938-116">ConsumerGroup 이름</span><span class="sxs-lookup"><span data-stu-id="34938-116">ConsumerGroup Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="34938-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="34938-117">-Namespace</span></span>
<span data-ttu-id="34938-118">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="34938-118">Namespace Name</span></span>

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

### <span data-ttu-id="34938-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34938-119">-ResourceGroupName</span></span>
<span data-ttu-id="34938-120">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="34938-120">Resource Group Name</span></span>

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

### <span data-ttu-id="34938-121">-확인</span><span class="sxs-lookup"><span data-stu-id="34938-121">-Confirm</span></span>
<span data-ttu-id="34938-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="34938-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34938-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34938-123">-WhatIf</span></span>
<span data-ttu-id="34938-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="34938-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34938-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="34938-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34938-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34938-126">CommonParameters</span></span>
<span data-ttu-id="34938-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="34938-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="34938-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="34938-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34938-129">입력</span><span class="sxs-lookup"><span data-stu-id="34938-129">INPUTS</span></span>

### <span data-ttu-id="34938-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="34938-130">System.String</span></span>


## <span data-ttu-id="34938-131">출력</span><span class="sxs-lookup"><span data-stu-id="34938-131">OUTPUTS</span></span>

### <span data-ttu-id="34938-132">System. 개체</span><span class="sxs-lookup"><span data-stu-id="34938-132">System.Object</span></span>

## <span data-ttu-id="34938-133">상속자</span><span class="sxs-lookup"><span data-stu-id="34938-133">NOTES</span></span>

## <span data-ttu-id="34938-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="34938-134">RELATED LINKS</span></span>
