---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubConsumerGroup.md
ms.openlocfilehash: cb898921b7fdfddddc95fc88d49dade4654c7ad2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489771"
---
# <span data-ttu-id="db881-101">Set-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="db881-101">Set-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="db881-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db881-102">SYNOPSIS</span></span>
<span data-ttu-id="db881-103">지정된 Event Hubs 소비자 그룹을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="db881-103">Updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="db881-104">구문</span><span class="sxs-lookup"><span data-stu-id="db881-104">SYNTAX</span></span>

```
Set-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="db881-105">설명</span><span class="sxs-lookup"><span data-stu-id="db881-105">DESCRIPTION</span></span>
<span data-ttu-id="db881-106">이 Set-AzEventHubConsumerGroup cmdlet은 지정된 Event Hubs 소비자 그룹을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="db881-106">The Set-AzEventHubConsumerGroup cmdlet updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="db881-107">예제</span><span class="sxs-lookup"><span data-stu-id="db881-107">EXAMPLES</span></span>

### <span data-ttu-id="db881-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="db881-108">Example 1</span></span>
```
PS C:\> Set-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName -UserMetadata "Testing"
```

<span data-ttu-id="db881-109">소비자 그룹 \` MyConsumerGroupName의 사용자 메타데이터를 \` "테스트"로 설정</span><span class="sxs-lookup"><span data-stu-id="db881-109">Sets the user metadata of the consumer group \`MyConsumerGroupName\` to "Testing."</span></span>

## <span data-ttu-id="db881-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db881-110">PARAMETERS</span></span>

### <span data-ttu-id="db881-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db881-111">-DefaultProfile</span></span>
<span data-ttu-id="db881-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="db881-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db881-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="db881-113">-EventHub</span></span>
<span data-ttu-id="db881-114">EventHub 이름</span><span class="sxs-lookup"><span data-stu-id="db881-114">EventHub Name</span></span>

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

### <span data-ttu-id="db881-115">-Name</span><span class="sxs-lookup"><span data-stu-id="db881-115">-Name</span></span>
<span data-ttu-id="db881-116">ConsumerGroup 이름</span><span class="sxs-lookup"><span data-stu-id="db881-116">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="db881-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="db881-117">-Namespace</span></span>
<span data-ttu-id="db881-118">네임스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="db881-118">Namespace Name</span></span>

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

### <span data-ttu-id="db881-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db881-119">-ResourceGroupName</span></span>
<span data-ttu-id="db881-120">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="db881-120">Resource Group Name</span></span>

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

### <span data-ttu-id="db881-121">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="db881-121">-UserMetadata</span></span>
<span data-ttu-id="db881-122">ConsumerGroup에 대한 사용자 메타데이터</span><span class="sxs-lookup"><span data-stu-id="db881-122">User Metadata for ConsumerGroup</span></span>

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

### <span data-ttu-id="db881-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db881-123">-Confirm</span></span>
<span data-ttu-id="db881-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="db881-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db881-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db881-125">-WhatIf</span></span>
<span data-ttu-id="db881-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="db881-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db881-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="db881-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db881-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db881-128">CommonParameters</span></span>
<span data-ttu-id="db881-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="db881-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db881-130">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="db881-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db881-131">입력</span><span class="sxs-lookup"><span data-stu-id="db881-131">INPUTS</span></span>

### <span data-ttu-id="db881-132">System.String</span><span class="sxs-lookup"><span data-stu-id="db881-132">System.String</span></span>

## <span data-ttu-id="db881-133">출력</span><span class="sxs-lookup"><span data-stu-id="db881-133">OUTPUTS</span></span>

### <span data-ttu-id="db881-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="db881-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="db881-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="db881-135">NOTES</span></span>

## <span data-ttu-id="db881-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="db881-136">RELATED LINKS</span></span>
