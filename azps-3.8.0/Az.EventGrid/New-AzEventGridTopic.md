---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopic.md
ms.openlocfilehash: 21bad7c36b39acbfbcc438603a57f504aaa1a106
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93879286"
---
# <span data-ttu-id="aeb62-101">New-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="aeb62-101">New-AzEventGridTopic</span></span>

## <span data-ttu-id="aeb62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aeb62-102">SYNOPSIS</span></span>
<span data-ttu-id="aeb62-103">새 Azure 이벤트 그리드 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aeb62-103">Creates a new Azure Event Grid Topic.</span></span>

## <span data-ttu-id="aeb62-104">구문과</span><span class="sxs-lookup"><span data-stu-id="aeb62-104">SYNTAX</span></span>

```
New-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aeb62-105">설명은</span><span class="sxs-lookup"><span data-stu-id="aeb62-105">DESCRIPTION</span></span>
<span data-ttu-id="aeb62-106">새 Azure 이벤트 그리드 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aeb62-106">Creates a new Azure Event Grid Topic.</span></span> <span data-ttu-id="aeb62-107">항목이 만들어지면 응용 프로그램에서 항목 끝점에 이벤트를 게시할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aeb62-107">Once the topic is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="aeb62-108">예제의</span><span class="sxs-lookup"><span data-stu-id="aeb62-108">EXAMPLES</span></span>

### <span data-ttu-id="aeb62-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="aeb62-109">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2
```

<span data-ttu-id="aeb62-110">\` \` \` \` 리소스 그룹 MyResourceGroupName에서 지정 된 지리적 위치 Westus2에 Topic1 \` 이벤트 그리드 항목을 만듭니다 \` .</span><span class="sxs-lookup"><span data-stu-id="aeb62-110">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="aeb62-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="aeb62-111">Example 2</span></span>
```powershell
PS C:\> New-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="aeb62-112">지정 된 \` \` \` \` \` \` 태그 "부서" 및 "환경"이 있는 리소스 그룹 MyResourceGroupName의 지정 된 지리적 위치 westus2에 Topic1 이벤트 그리드 항목을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aeb62-112">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="aeb62-113">변수</span><span class="sxs-lookup"><span data-stu-id="aeb62-113">PARAMETERS</span></span>

### <span data-ttu-id="aeb62-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aeb62-114">-DefaultProfile</span></span>
<span data-ttu-id="aeb62-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="aeb62-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="aeb62-116">-위치</span><span class="sxs-lookup"><span data-stu-id="aeb62-116">-Location</span></span>
<span data-ttu-id="aeb62-117">주제의 위치</span><span class="sxs-lookup"><span data-stu-id="aeb62-117">The location of the topic</span></span>

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

### <span data-ttu-id="aeb62-118">-이름</span><span class="sxs-lookup"><span data-stu-id="aeb62-118">-Name</span></span>
<span data-ttu-id="aeb62-119">주제의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aeb62-119">The name of the topic.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aeb62-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aeb62-120">-ResourceGroupName</span></span>
<span data-ttu-id="aeb62-121">주제를 만들어야 하는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="aeb62-121">The resource group in which the topic should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aeb62-122">태그</span><span class="sxs-lookup"><span data-stu-id="aeb62-122">-Tag</span></span>
<span data-ttu-id="aeb62-123">리소스 태그를 나타내는 Hashtables.</span><span class="sxs-lookup"><span data-stu-id="aeb62-123">Hashtables which represents resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aeb62-124">-확인</span><span class="sxs-lookup"><span data-stu-id="aeb62-124">-Confirm</span></span>
<span data-ttu-id="aeb62-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="aeb62-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aeb62-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aeb62-126">-WhatIf</span></span>
<span data-ttu-id="aeb62-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="aeb62-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aeb62-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aeb62-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aeb62-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aeb62-129">CommonParameters</span></span>
<span data-ttu-id="aeb62-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aeb62-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aeb62-131">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aeb62-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aeb62-132">입력</span><span class="sxs-lookup"><span data-stu-id="aeb62-132">INPUTS</span></span>

### <span data-ttu-id="aeb62-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="aeb62-133">System.String</span></span>

### <span data-ttu-id="aeb62-134">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="aeb62-134">System.Collections.Hashtable</span></span>

## <span data-ttu-id="aeb62-135">출력</span><span class="sxs-lookup"><span data-stu-id="aeb62-135">OUTPUTS</span></span>

### <span data-ttu-id="aeb62-136">Microsoft. Azure. c c.</span><span class="sxs-lookup"><span data-stu-id="aeb62-136">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="aeb62-137">상속자</span><span class="sxs-lookup"><span data-stu-id="aeb62-137">NOTES</span></span>

## <span data-ttu-id="aeb62-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aeb62-138">RELATED LINKS</span></span>
