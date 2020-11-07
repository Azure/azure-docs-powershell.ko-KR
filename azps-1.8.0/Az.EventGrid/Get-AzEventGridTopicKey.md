---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
ms.openlocfilehash: 3454a3aad2276384588c0ccc550a1b0ef6df7cfc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700877"
---
# <span data-ttu-id="f0663-101">Get-AzEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="f0663-101">Get-AzEventGridTopicKey</span></span>

## <span data-ttu-id="f0663-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0663-102">SYNOPSIS</span></span>
<span data-ttu-id="f0663-103">이벤트 그리드 항목에 이벤트를 게시 하는 데 사용 되는 공유 된 선택 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f0663-103">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="f0663-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f0663-104">SYNTAX</span></span>

### <span data-ttu-id="f0663-105">TopicNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="f0663-105">TopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridTopicKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0663-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0663-106">TopicInputObjectParameterSet</span></span>
```
Get-AzEventGridTopicKey [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f0663-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="f0663-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridTopicKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0663-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f0663-108">DESCRIPTION</span></span>
<span data-ttu-id="f0663-109">이벤트 그리드 항목에 이벤트를 게시 하는 데 사용 되는 공유 된 선택 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f0663-109">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="f0663-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f0663-110">EXAMPLES</span></span>

### <span data-ttu-id="f0663-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="f0663-111">Example 1</span></span>
```
PS C:\> Get-AzEventGridTopicKey -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="f0663-112">\` \` 리소스 그룹 MyResourceGroupName에서 이벤트 그리드 Topic1에 대 한 공유 된 액세스 키를 가져옵니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="f0663-112">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="f0663-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="f0663-113">Example 2</span></span>
```
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | Get-AzEventGridTopicKey
```

<span data-ttu-id="f0663-114">\` \` 리소스 그룹 MyResourceGroupName에서 이벤트 그리드 Topic1에 대 한 공유 된 액세스 키를 가져옵니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="f0663-114">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="f0663-115">변수</span><span class="sxs-lookup"><span data-stu-id="f0663-115">PARAMETERS</span></span>

### <span data-ttu-id="f0663-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0663-116">-DefaultProfile</span></span>
<span data-ttu-id="f0663-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f0663-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f0663-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f0663-118">-InputObject</span></span>
<span data-ttu-id="f0663-119">EventGrid 주제 개체</span><span class="sxs-lookup"><span data-stu-id="f0663-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="f0663-120">-이름</span><span class="sxs-lookup"><span data-stu-id="f0663-120">-Name</span></span>
<span data-ttu-id="f0663-121">EventGrid 주제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f0663-121">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0663-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0663-122">-ResourceGroupName</span></span>
<span data-ttu-id="f0663-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f0663-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="f0663-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f0663-124">-ResourceId</span></span>
<span data-ttu-id="f0663-125">이벤트 그리드 항목을 나타내는 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="f0663-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="f0663-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0663-126">CommonParameters</span></span>
<span data-ttu-id="f0663-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0663-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0663-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0663-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0663-129">입력</span><span class="sxs-lookup"><span data-stu-id="f0663-129">INPUTS</span></span>

### <span data-ttu-id="f0663-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f0663-130">System.String</span></span>

### <span data-ttu-id="f0663-131">Microsoft. Azure. c c.</span><span class="sxs-lookup"><span data-stu-id="f0663-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="f0663-132">출력</span><span class="sxs-lookup"><span data-stu-id="f0663-132">OUTPUTS</span></span>

### <span data-ttu-id="f0663-133">TopicSharedAccessKeys (Microsoft. 관리.</span><span class="sxs-lookup"><span data-stu-id="f0663-133">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="f0663-134">상속자</span><span class="sxs-lookup"><span data-stu-id="f0663-134">NOTES</span></span>

## <span data-ttu-id="f0663-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f0663-135">RELATED LINKS</span></span>
