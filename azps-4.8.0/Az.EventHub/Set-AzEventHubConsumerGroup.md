---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubConsumerGroup.md
ms.openlocfilehash: cb898921b7fdfddddc95fc88d49dade4654c7ad2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047770"
---
# <span data-ttu-id="217b4-101">Set-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="217b4-101">Set-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="217b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="217b4-102">SYNOPSIS</span></span>
<span data-ttu-id="217b4-103">지정 된 이벤트 허브 소비자 그룹을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="217b4-103">Updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="217b4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="217b4-104">SYNTAX</span></span>

```
Set-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="217b4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="217b4-105">DESCRIPTION</span></span>
<span data-ttu-id="217b4-106">Set-AzEventHubConsumerGroup cmdlet은 지정 된 이벤트 허브 소비자 그룹을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="217b4-106">The Set-AzEventHubConsumerGroup cmdlet updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="217b4-107">예제의</span><span class="sxs-lookup"><span data-stu-id="217b4-107">EXAMPLES</span></span>

### <span data-ttu-id="217b4-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="217b4-108">Example 1</span></span>
```
PS C:\> Set-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName -UserMetadata "Testing"
```

<span data-ttu-id="217b4-109">소비자 그룹 MyConsumerGroupName의 사용자 메타 데이터 \` \` 를 "테스트"로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="217b4-109">Sets the user metadata of the consumer group \`MyConsumerGroupName\` to "Testing."</span></span>

## <span data-ttu-id="217b4-110">변수</span><span class="sxs-lookup"><span data-stu-id="217b4-110">PARAMETERS</span></span>

### <span data-ttu-id="217b4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="217b4-111">-DefaultProfile</span></span>
<span data-ttu-id="217b4-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="217b4-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="217b4-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="217b4-113">-EventHub</span></span>
<span data-ttu-id="217b4-114">EventHub 이름</span><span class="sxs-lookup"><span data-stu-id="217b4-114">EventHub Name</span></span>

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

### <span data-ttu-id="217b4-115">-이름</span><span class="sxs-lookup"><span data-stu-id="217b4-115">-Name</span></span>
<span data-ttu-id="217b4-116">ConsumerGroup 이름</span><span class="sxs-lookup"><span data-stu-id="217b4-116">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="217b4-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="217b4-117">-Namespace</span></span>
<span data-ttu-id="217b4-118">네임 스페이스 이름</span><span class="sxs-lookup"><span data-stu-id="217b4-118">Namespace Name</span></span>

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

### <span data-ttu-id="217b4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="217b4-119">-ResourceGroupName</span></span>
<span data-ttu-id="217b4-120">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="217b4-120">Resource Group Name</span></span>

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

### <span data-ttu-id="217b4-121">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="217b4-121">-UserMetadata</span></span>
<span data-ttu-id="217b4-122">ConsumerGroup에 대 한 사용자 메타 데이터</span><span class="sxs-lookup"><span data-stu-id="217b4-122">User Metadata for ConsumerGroup</span></span>

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

### <span data-ttu-id="217b4-123">-확인</span><span class="sxs-lookup"><span data-stu-id="217b4-123">-Confirm</span></span>
<span data-ttu-id="217b4-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="217b4-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="217b4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="217b4-125">-WhatIf</span></span>
<span data-ttu-id="217b4-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="217b4-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="217b4-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="217b4-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="217b4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="217b4-128">CommonParameters</span></span>
<span data-ttu-id="217b4-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="217b4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="217b4-130">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="217b4-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="217b4-131">입력</span><span class="sxs-lookup"><span data-stu-id="217b4-131">INPUTS</span></span>

### <span data-ttu-id="217b4-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="217b4-132">System.String</span></span>

## <span data-ttu-id="217b4-133">출력</span><span class="sxs-lookup"><span data-stu-id="217b4-133">OUTPUTS</span></span>

### <span data-ttu-id="217b4-134">PSConsumerGroupAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="217b4-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="217b4-135">상속자</span><span class="sxs-lookup"><span data-stu-id="217b4-135">NOTES</span></span>

## <span data-ttu-id="217b4-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="217b4-136">RELATED LINKS</span></span>
