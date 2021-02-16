---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
ms.openlocfilehash: b0690882cc230a92fd6e81e38832f2fc352e131c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194425"
---
# <span data-ttu-id="6ddba-101">Get-AzEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="6ddba-101">Get-AzEventGridTopicKey</span></span>

## <span data-ttu-id="6ddba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ddba-102">SYNOPSIS</span></span>
<span data-ttu-id="6ddba-103">Event Grid 토픽에 이벤트를 게시하는 데 사용되는 공유 액세스 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6ddba-103">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="6ddba-104">구문</span><span class="sxs-lookup"><span data-stu-id="6ddba-104">SYNTAX</span></span>

### <span data-ttu-id="6ddba-105">TopicNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="6ddba-105">TopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridTopicKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ddba-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ddba-106">TopicInputObjectParameterSet</span></span>
```
Get-AzEventGridTopicKey [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6ddba-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ddba-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridTopicKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ddba-108">설명</span><span class="sxs-lookup"><span data-stu-id="6ddba-108">DESCRIPTION</span></span>
<span data-ttu-id="6ddba-109">Event Grid 토픽에 이벤트를 게시하는 데 사용되는 공유 액세스 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6ddba-109">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="6ddba-110">예제</span><span class="sxs-lookup"><span data-stu-id="6ddba-110">EXAMPLES</span></span>

### <span data-ttu-id="6ddba-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="6ddba-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopicKey -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="6ddba-112">리소스 그룹 \` \` \` MyResourceGroupName에서 Event Grid 항목 Topic1의 공유 액세스 키를 \` 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6ddba-112">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="6ddba-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="6ddba-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | Get-AzEventGridTopicKey
```

<span data-ttu-id="6ddba-114">리소스 그룹 \` \` \` MyResourceGroupName에서 Event Grid 항목 Topic1의 공유 액세스 키를 \` 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6ddba-114">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="6ddba-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6ddba-115">PARAMETERS</span></span>

### <span data-ttu-id="6ddba-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ddba-116">-DefaultProfile</span></span>
<span data-ttu-id="6ddba-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="6ddba-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6ddba-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ddba-118">-InputObject</span></span>
<span data-ttu-id="6ddba-119">EventGrid 토픽 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="6ddba-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="6ddba-120">-Name</span><span class="sxs-lookup"><span data-stu-id="6ddba-120">-Name</span></span>
<span data-ttu-id="6ddba-121">EventGrid 토픽 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6ddba-121">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="6ddba-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ddba-122">-ResourceGroupName</span></span>
<span data-ttu-id="6ddba-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6ddba-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="6ddba-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ddba-124">-ResourceId</span></span>
<span data-ttu-id="6ddba-125">Event Grid 토픽을 나타내는 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="6ddba-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="6ddba-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ddba-126">CommonParameters</span></span>
<span data-ttu-id="6ddba-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6ddba-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ddba-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6ddba-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ddba-129">입력</span><span class="sxs-lookup"><span data-stu-id="6ddba-129">INPUTS</span></span>

### <span data-ttu-id="6ddba-130">System.String</span><span class="sxs-lookup"><span data-stu-id="6ddba-130">System.String</span></span>

### <span data-ttu-id="6ddba-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="6ddba-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="6ddba-132">출력</span><span class="sxs-lookup"><span data-stu-id="6ddba-132">OUTPUTS</span></span>

### <span data-ttu-id="6ddba-133">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="6ddba-133">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="6ddba-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6ddba-134">NOTES</span></span>

## <span data-ttu-id="6ddba-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6ddba-135">RELATED LINKS</span></span>
