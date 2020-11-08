---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopicKey.md
ms.openlocfilehash: ab9c9401b0f8d929be1a4aa244f407957d886e4c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213593"
---
# <span data-ttu-id="d5236-101">New-AzEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="d5236-101">New-AzEventGridTopicKey</span></span>

## <span data-ttu-id="d5236-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5236-102">SYNOPSIS</span></span>
<span data-ttu-id="d5236-103">Azure 이벤트 그리드 항목에 대 한 공유 된 선택 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5236-103">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="d5236-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d5236-104">SYNTAX</span></span>

### <span data-ttu-id="d5236-105">TopicNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="d5236-105">TopicNameParameterSet (Default)</span></span>
```
New-AzEventGridTopicKey [-ResourceGroupName] <String> [-TopicName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5236-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5236-106">TopicInputObjectParameterSet</span></span>
```
New-AzEventGridTopicKey [-KeyName] <String> [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5236-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="d5236-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridTopicKey [-KeyName] <String> [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5236-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d5236-108">DESCRIPTION</span></span>
<span data-ttu-id="d5236-109">Azure 이벤트 그리드 항목에 대 한 공유 된 선택 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5236-109">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="d5236-110">예제의</span><span class="sxs-lookup"><span data-stu-id="d5236-110">EXAMPLES</span></span>

### <span data-ttu-id="d5236-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="d5236-111">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridTopicKey -ResourceGroup MyResourceGroupName -TopicName Topic1 -KeyName key1
```

<span data-ttu-id="d5236-112">\' \` 리소스 그룹 MyResourceGroupName에서 이벤트 그리드 Topic1의 키 key1 항목에 해당 하는 키를 다시 생성 \` \` \` 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5236-112">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="d5236-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="d5236-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | New-AzEventGridTopicKey -KeyName "key1"
```

<span data-ttu-id="d5236-114">\' \` 리소스 그룹 MyResourceGroupName에서 이벤트 그리드 Topic1의 키 key1 항목에 해당 하는 키를 다시 생성 \` \` \` 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5236-114">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="d5236-115">변수</span><span class="sxs-lookup"><span data-stu-id="d5236-115">PARAMETERS</span></span>

### <span data-ttu-id="d5236-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5236-116">-DefaultProfile</span></span>
<span data-ttu-id="d5236-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d5236-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d5236-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d5236-118">-InputObject</span></span>
<span data-ttu-id="d5236-119">EventGrid 주제 개체</span><span class="sxs-lookup"><span data-stu-id="d5236-119">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5236-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="d5236-120">-KeyName</span></span>
<span data-ttu-id="d5236-121">다시 생성 해야 하는 키의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d5236-121">The name of the key that needs to be regenerated</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5236-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5236-122">-ResourceGroupName</span></span>
<span data-ttu-id="d5236-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d5236-123">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5236-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d5236-124">-ResourceId</span></span>
<span data-ttu-id="d5236-125">이벤트 그리드 항목을 나타내는 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="d5236-125">Resource Identifier representing the Event Grid Topic.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5236-126">-TopicName</span><span class="sxs-lookup"><span data-stu-id="d5236-126">-TopicName</span></span>
<span data-ttu-id="d5236-127">주제의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d5236-127">The name of the topic.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5236-128">-확인</span><span class="sxs-lookup"><span data-stu-id="d5236-128">-Confirm</span></span>
<span data-ttu-id="d5236-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5236-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5236-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5236-130">-WhatIf</span></span>
<span data-ttu-id="d5236-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d5236-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5236-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d5236-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5236-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5236-133">CommonParameters</span></span>
<span data-ttu-id="d5236-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5236-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5236-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d5236-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5236-136">입력</span><span class="sxs-lookup"><span data-stu-id="d5236-136">INPUTS</span></span>

### <span data-ttu-id="d5236-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d5236-137">System.String</span></span>

### <span data-ttu-id="d5236-138">Microsoft. Azure. c c.</span><span class="sxs-lookup"><span data-stu-id="d5236-138">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="d5236-139">출력</span><span class="sxs-lookup"><span data-stu-id="d5236-139">OUTPUTS</span></span>

### <span data-ttu-id="d5236-140">TopicSharedAccessKeys (Microsoft. 관리.</span><span class="sxs-lookup"><span data-stu-id="d5236-140">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="d5236-141">상속자</span><span class="sxs-lookup"><span data-stu-id="d5236-141">NOTES</span></span>

## <span data-ttu-id="d5236-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d5236-142">RELATED LINKS</span></span>
