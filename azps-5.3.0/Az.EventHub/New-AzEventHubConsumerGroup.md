---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubConsumerGroup.md
ms.openlocfilehash: ef03af9c452496d198aaaa073ee9fd967d851bb4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386968"
---
# <span data-ttu-id="b8d99-101">New-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="b8d99-101">New-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="b8d99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8d99-102">SYNOPSIS</span></span>
<span data-ttu-id="b8d99-103">지정된 이벤트 허브에 대한 새 소비자 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b8d99-103">Creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="b8d99-104">구문</span><span class="sxs-lookup"><span data-stu-id="b8d99-104">SYNTAX</span></span>

```
New-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b8d99-105">설명</span><span class="sxs-lookup"><span data-stu-id="b8d99-105">DESCRIPTION</span></span>
<span data-ttu-id="b8d99-106">지정된 이벤트 허브에 대한 새 소비자 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b8d99-106">Creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="b8d99-107">예제</span><span class="sxs-lookup"><span data-stu-id="b8d99-107">EXAMPLES</span></span>

### <span data-ttu-id="b8d99-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b8d99-108">Example 1</span></span>
```
PS C:\> New-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="b8d99-109">리소스 그룹 \` MyResourceGroupName을 통해 MyNamespaceName 네임스페이스로 범위가 지정된 이벤트 허브 \` \` MyEventHubName에 소비자 그룹 \` \` \` \` MyConsumerGroupName을 \` 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b8d99-109">Creates the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, scoped to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="b8d99-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b8d99-110">PARAMETERS</span></span>

### <span data-ttu-id="b8d99-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8d99-111">-DefaultProfile</span></span>
<span data-ttu-id="b8d99-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b8d99-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8d99-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="b8d99-113">-EventHub</span></span>
<span data-ttu-id="b8d99-114">EventHub 이름</span><span class="sxs-lookup"><span data-stu-id="b8d99-114">EventHub Name</span></span>

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

### <span data-ttu-id="b8d99-115">-Name</span><span class="sxs-lookup"><span data-stu-id="b8d99-115">-Name</span></span>
<span data-ttu-id="b8d99-116">ConsumerGroup 이름</span><span class="sxs-lookup"><span data-stu-id="b8d99-116">ConsumerGroup Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8d99-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b8d99-117">-Namespace</span></span>
<span data-ttu-id="b8d99-118">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="b8d99-118">Namespace Name</span></span>

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

### <span data-ttu-id="b8d99-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8d99-119">-ResourceGroupName</span></span>
<span data-ttu-id="b8d99-120">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="b8d99-120">Resource Group Name</span></span>

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

### <span data-ttu-id="b8d99-121">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="b8d99-121">-UserMetadata</span></span>
<span data-ttu-id="b8d99-122">ConsumerGroup에 대한 사용자 메타데이터</span><span class="sxs-lookup"><span data-stu-id="b8d99-122">User Metadata for ConsumerGroup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b8d99-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b8d99-123">-Confirm</span></span>
<span data-ttu-id="b8d99-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b8d99-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8d99-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8d99-125">-WhatIf</span></span>
<span data-ttu-id="b8d99-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b8d99-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8d99-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b8d99-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8d99-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8d99-128">CommonParameters</span></span>
<span data-ttu-id="b8d99-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b8d99-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8d99-130">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b8d99-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8d99-131">입력</span><span class="sxs-lookup"><span data-stu-id="b8d99-131">INPUTS</span></span>

### <span data-ttu-id="b8d99-132">System.String</span><span class="sxs-lookup"><span data-stu-id="b8d99-132">System.String</span></span>

## <span data-ttu-id="b8d99-133">출력</span><span class="sxs-lookup"><span data-stu-id="b8d99-133">OUTPUTS</span></span>

### <span data-ttu-id="b8d99-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="b8d99-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="b8d99-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b8d99-135">NOTES</span></span>

## <span data-ttu-id="b8d99-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b8d99-136">RELATED LINKS</span></span>
