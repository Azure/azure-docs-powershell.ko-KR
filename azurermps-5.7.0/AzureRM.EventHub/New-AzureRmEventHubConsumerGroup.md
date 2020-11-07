---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: a9447c745ddf60c4a2adcb2a55c824b65d96efd8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93704024"
---
# <span data-ttu-id="89734-101">New-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="89734-101">New-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="89734-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89734-102">SYNOPSIS</span></span>
<span data-ttu-id="89734-103">지정 된 이벤트 허브에 대 한 새 소비자 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="89734-103">Creates a new consumer group for the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89734-104">구문과</span><span class="sxs-lookup"><span data-stu-id="89734-104">SYNTAX</span></span>

```
New-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="89734-105">예제의</span><span class="sxs-lookup"><span data-stu-id="89734-105">EXAMPLES</span></span>

### <span data-ttu-id="89734-106">예제 1</span><span class="sxs-lookup"><span data-stu-id="89734-106">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="89734-107">\` \` \` \` \` 리소스 그룹 MyResourceGroupName를 사용 하 여 네임 스페이스 MyNamespaceName 범위에 \` \` 있는 이벤트 허브 MyEventHubName에서 \` 소비자 그룹 MyConsumerGroupName를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="89734-107">Creates the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, scoped to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="89734-108">변수</span><span class="sxs-lookup"><span data-stu-id="89734-108">PARAMETERS</span></span>

### <span data-ttu-id="89734-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89734-109">-DefaultProfile</span></span>
<span data-ttu-id="89734-110">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="89734-110">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89734-111">-EventHub</span><span class="sxs-lookup"><span data-stu-id="89734-111">-EventHub</span></span>
<span data-ttu-id="89734-112">EventHub 이름</span><span class="sxs-lookup"><span data-stu-id="89734-112">EventHub Name</span></span>

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

### <span data-ttu-id="89734-113">-이름</span><span class="sxs-lookup"><span data-stu-id="89734-113">-Name</span></span>
<span data-ttu-id="89734-114">ConsumerGroup 이름</span><span class="sxs-lookup"><span data-stu-id="89734-114">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="89734-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="89734-115">-Namespace</span></span>
<span data-ttu-id="89734-116">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="89734-116">Namespace Name</span></span>

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

### <span data-ttu-id="89734-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="89734-117">-ResourceGroupName</span></span>
<span data-ttu-id="89734-118">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="89734-118">Resource Group Name</span></span>

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

### <span data-ttu-id="89734-119">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="89734-119">-UserMetadata</span></span>
<span data-ttu-id="89734-120">ConsumerGroup에 대 한 사용자 메타 데이터</span><span class="sxs-lookup"><span data-stu-id="89734-120">User Metadata for ConsumerGroup</span></span>

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

### <span data-ttu-id="89734-121">-확인</span><span class="sxs-lookup"><span data-stu-id="89734-121">-Confirm</span></span>
<span data-ttu-id="89734-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="89734-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89734-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89734-123">-WhatIf</span></span>
<span data-ttu-id="89734-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="89734-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="89734-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="89734-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="89734-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89734-126">CommonParameters</span></span>
<span data-ttu-id="89734-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="89734-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="89734-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89734-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89734-129">입력</span><span class="sxs-lookup"><span data-stu-id="89734-129">INPUTS</span></span>

### <span data-ttu-id="89734-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="89734-130">System.String</span></span>


## <span data-ttu-id="89734-131">출력</span><span class="sxs-lookup"><span data-stu-id="89734-131">OUTPUTS</span></span>

### <span data-ttu-id="89734-132">PSConsumerGroupAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="89734-132">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>


## <span data-ttu-id="89734-133">상속자</span><span class="sxs-lookup"><span data-stu-id="89734-133">NOTES</span></span>

## <span data-ttu-id="89734-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="89734-134">RELATED LINKS</span></span>
