---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/new-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubConsumerGroup.md
ms.openlocfilehash: 2a11ab0ec68ee01864f1255953121b91f1b27ebf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957120"
---
# <span data-ttu-id="6c079-101">New-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="6c079-101">New-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="6c079-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c079-102">SYNOPSIS</span></span>
<span data-ttu-id="6c079-103">지정된 Event Hub에 대한 새 소비자 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6c079-103">Creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="6c079-104">구문</span><span class="sxs-lookup"><span data-stu-id="6c079-104">SYNTAX</span></span>

```
New-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6c079-105">설명</span><span class="sxs-lookup"><span data-stu-id="6c079-105">DESCRIPTION</span></span>
<span data-ttu-id="6c079-106">지정된 Event Hub에 대한 새 소비자 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6c079-106">Creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="6c079-107">예제</span><span class="sxs-lookup"><span data-stu-id="6c079-107">EXAMPLES</span></span>

### <span data-ttu-id="6c079-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="6c079-108">Example 1</span></span>
```
PS C:\> New-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="6c079-109">리소스 그룹 \` \` \` \` \` MyResourceGroupName이 있는 네임스페이스 MyNamespaceName로 범위가 지정된 Event Hub MyEventHubName에서 소비자 그룹 \` \` MyConsumerGroupName을 \` 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6c079-109">Creates the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, scoped to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="6c079-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6c079-110">PARAMETERS</span></span>

### <span data-ttu-id="6c079-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c079-111">-DefaultProfile</span></span>
<span data-ttu-id="6c079-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6c079-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c079-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="6c079-113">-EventHub</span></span>
<span data-ttu-id="6c079-114">EventHub 이름</span><span class="sxs-lookup"><span data-stu-id="6c079-114">EventHub Name</span></span>

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

### <span data-ttu-id="6c079-115">-Name</span><span class="sxs-lookup"><span data-stu-id="6c079-115">-Name</span></span>
<span data-ttu-id="6c079-116">ConsumerGroup 이름</span><span class="sxs-lookup"><span data-stu-id="6c079-116">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="6c079-117">-네임스페이스</span><span class="sxs-lookup"><span data-stu-id="6c079-117">-Namespace</span></span>
<span data-ttu-id="6c079-118">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="6c079-118">Namespace Name</span></span>

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

### <span data-ttu-id="6c079-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c079-119">-ResourceGroupName</span></span>
<span data-ttu-id="6c079-120">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="6c079-120">Resource Group Name</span></span>

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

### <span data-ttu-id="6c079-121">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="6c079-121">-UserMetadata</span></span>
<span data-ttu-id="6c079-122">ConsumerGroup에 대한 사용자 메타데이터</span><span class="sxs-lookup"><span data-stu-id="6c079-122">User Metadata for ConsumerGroup</span></span>

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

### <span data-ttu-id="6c079-123">-확인</span><span class="sxs-lookup"><span data-stu-id="6c079-123">-Confirm</span></span>
<span data-ttu-id="6c079-124">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6c079-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c079-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c079-125">-WhatIf</span></span>
<span data-ttu-id="6c079-126">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="6c079-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c079-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6c079-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c079-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c079-128">CommonParameters</span></span>
<span data-ttu-id="6c079-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6c079-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c079-130">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6c079-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c079-131">입력</span><span class="sxs-lookup"><span data-stu-id="6c079-131">INPUTS</span></span>

### <span data-ttu-id="6c079-132">System.String</span><span class="sxs-lookup"><span data-stu-id="6c079-132">System.String</span></span>

## <span data-ttu-id="6c079-133">출력</span><span class="sxs-lookup"><span data-stu-id="6c079-133">OUTPUTS</span></span>

### <span data-ttu-id="6c079-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="6c079-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="6c079-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6c079-135">NOTES</span></span>

## <span data-ttu-id="6c079-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6c079-136">RELATED LINKS</span></span>
