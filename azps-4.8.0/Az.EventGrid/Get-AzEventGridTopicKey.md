---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
ms.openlocfilehash: b0690882cc230a92fd6e81e38832f2fc352e131c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056357"
---
# <span data-ttu-id="976d3-101">Get-AzEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="976d3-101">Get-AzEventGridTopicKey</span></span>

## <span data-ttu-id="976d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="976d3-102">SYNOPSIS</span></span>
<span data-ttu-id="976d3-103">이벤트 그리드 항목에 이벤트를 게시 하는 데 사용 되는 공유 된 선택 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="976d3-103">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="976d3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="976d3-104">SYNTAX</span></span>

### <span data-ttu-id="976d3-105">TopicNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="976d3-105">TopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridTopicKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="976d3-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="976d3-106">TopicInputObjectParameterSet</span></span>
```
Get-AzEventGridTopicKey [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="976d3-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="976d3-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridTopicKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="976d3-108">설명은</span><span class="sxs-lookup"><span data-stu-id="976d3-108">DESCRIPTION</span></span>
<span data-ttu-id="976d3-109">이벤트 그리드 항목에 이벤트를 게시 하는 데 사용 되는 공유 된 선택 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="976d3-109">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="976d3-110">예제의</span><span class="sxs-lookup"><span data-stu-id="976d3-110">EXAMPLES</span></span>

### <span data-ttu-id="976d3-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="976d3-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopicKey -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="976d3-112">\` \` 리소스 그룹 MyResourceGroupName에서 이벤트 그리드 Topic1에 대 한 공유 된 액세스 키를 가져옵니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="976d3-112">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="976d3-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="976d3-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | Get-AzEventGridTopicKey
```

<span data-ttu-id="976d3-114">\` \` 리소스 그룹 MyResourceGroupName에서 이벤트 그리드 Topic1에 대 한 공유 된 액세스 키를 가져옵니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="976d3-114">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="976d3-115">변수</span><span class="sxs-lookup"><span data-stu-id="976d3-115">PARAMETERS</span></span>

### <span data-ttu-id="976d3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="976d3-116">-DefaultProfile</span></span>
<span data-ttu-id="976d3-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="976d3-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="976d3-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="976d3-118">-InputObject</span></span>
<span data-ttu-id="976d3-119">EventGrid 주제 개체</span><span class="sxs-lookup"><span data-stu-id="976d3-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="976d3-120">-이름</span><span class="sxs-lookup"><span data-stu-id="976d3-120">-Name</span></span>
<span data-ttu-id="976d3-121">EventGrid 주제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="976d3-121">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="976d3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="976d3-122">-ResourceGroupName</span></span>
<span data-ttu-id="976d3-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="976d3-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="976d3-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="976d3-124">-ResourceId</span></span>
<span data-ttu-id="976d3-125">이벤트 그리드 항목을 나타내는 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="976d3-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="976d3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="976d3-126">CommonParameters</span></span>
<span data-ttu-id="976d3-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="976d3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="976d3-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="976d3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="976d3-129">입력</span><span class="sxs-lookup"><span data-stu-id="976d3-129">INPUTS</span></span>

### <span data-ttu-id="976d3-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="976d3-130">System.String</span></span>

### <span data-ttu-id="976d3-131">Microsoft. Azure. c c.</span><span class="sxs-lookup"><span data-stu-id="976d3-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="976d3-132">출력</span><span class="sxs-lookup"><span data-stu-id="976d3-132">OUTPUTS</span></span>

### <span data-ttu-id="976d3-133">TopicSharedAccessKeys (Microsoft. 관리.</span><span class="sxs-lookup"><span data-stu-id="976d3-133">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="976d3-134">상속자</span><span class="sxs-lookup"><span data-stu-id="976d3-134">NOTES</span></span>

## <span data-ttu-id="976d3-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="976d3-135">RELATED LINKS</span></span>
