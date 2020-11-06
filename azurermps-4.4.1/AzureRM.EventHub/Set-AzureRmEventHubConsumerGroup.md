---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubConsumerGroup.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: c871036c6f3113bd40e17fb5bbc201fa6297573c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534096"
---
# <span data-ttu-id="a7f70-101">Set-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="a7f70-101">Set-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="a7f70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7f70-102">SYNOPSIS</span></span>
<span data-ttu-id="a7f70-103">지정 된 이벤트 허브 소비자 그룹을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7f70-103">Updates the specified Event Hubs consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a7f70-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a7f70-104">SYNTAX</span></span>

```
Set-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> -Namespace <String> -EventHub <String>
 -Name <String> [[-UserMetadata] <String>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="a7f70-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a7f70-105">DESCRIPTION</span></span>
<span data-ttu-id="a7f70-106">Set-AzureRmEventHubConsumerGroup cmdlet은 지정 된 이벤트 허브 소비자 그룹을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7f70-106">The Set-AzureRmEventHubConsumerGroup cmdlet updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="a7f70-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a7f70-107">EXAMPLES</span></span>

### <span data-ttu-id="a7f70-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="a7f70-108">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName -UserMetadata "Testing"
```

<span data-ttu-id="a7f70-109">소비자 그룹 MyConsumerGroupName의 사용자 메타 데이터 \` \` 를 "테스트"로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7f70-109">Sets the user metadata of the consumer group \`MyConsumerGroupName\` to "Testing."</span></span>

## <span data-ttu-id="a7f70-110">변수</span><span class="sxs-lookup"><span data-stu-id="a7f70-110">PARAMETERS</span></span>

### <span data-ttu-id="a7f70-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7f70-111">-ResourceGroupName</span></span>
<span data-ttu-id="a7f70-112">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a7f70-112">Resource group name.</span></span>

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

### <span data-ttu-id="a7f70-113">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="a7f70-113">-UserMetadata</span></span>
<span data-ttu-id="a7f70-114">소비자 그룹에 대 한 사용자 메타 데이터입니다 (선택 사항).</span><span class="sxs-lookup"><span data-stu-id="a7f70-114">User metadata for the consumer group (optional).</span></span>

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

### <span data-ttu-id="a7f70-115">-확인</span><span class="sxs-lookup"><span data-stu-id="a7f70-115">-Confirm</span></span>
<span data-ttu-id="a7f70-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a7f70-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f70-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7f70-117">-WhatIf</span></span>
<span data-ttu-id="a7f70-118">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a7f70-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7f70-119">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a7f70-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7f70-120">-EventHub</span><span class="sxs-lookup"><span data-stu-id="a7f70-120">-EventHub</span></span>
<span data-ttu-id="a7f70-121">EventHub 이름.</span><span class="sxs-lookup"><span data-stu-id="a7f70-121">EventHub Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7f70-122">-이름</span><span class="sxs-lookup"><span data-stu-id="a7f70-122">-Name</span></span>
<span data-ttu-id="a7f70-123">ConsumerGroup 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a7f70-123">ConsumerGroup Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7f70-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a7f70-124">-Namespace</span></span>
<span data-ttu-id="a7f70-125">네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a7f70-125">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="a7f70-126">입력</span><span class="sxs-lookup"><span data-stu-id="a7f70-126">INPUTS</span></span>

### <span data-ttu-id="a7f70-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a7f70-127">System.String</span></span>

## <span data-ttu-id="a7f70-128">출력</span><span class="sxs-lookup"><span data-stu-id="a7f70-128">OUTPUTS</span></span>

### <span data-ttu-id="a7f70-129">ConsumerGroupAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="a7f70-129">Microsoft.Azure.Commands.EventHub.Models.ConsumerGroupAttributes</span></span>

## <span data-ttu-id="a7f70-130">상속자</span><span class="sxs-lookup"><span data-stu-id="a7f70-130">NOTES</span></span>

## <span data-ttu-id="a7f70-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a7f70-131">RELATED LINKS</span></span>

