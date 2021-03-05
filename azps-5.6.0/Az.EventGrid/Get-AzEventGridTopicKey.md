---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/get-azeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicKey.md
ms.openlocfilehash: 92a70d16f8cd1db2c37c1247c994a3c406df5a54
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991312"
---
# <span data-ttu-id="dba2f-101">Get-AzEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="dba2f-101">Get-AzEventGridTopicKey</span></span>

## <span data-ttu-id="dba2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dba2f-102">SYNOPSIS</span></span>
<span data-ttu-id="dba2f-103">Event Grid 토픽에 이벤트를 게시하는 데 사용되는 공유 액세스 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dba2f-103">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="dba2f-104">구문</span><span class="sxs-lookup"><span data-stu-id="dba2f-104">SYNTAX</span></span>

### <span data-ttu-id="dba2f-105">TopicNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="dba2f-105">TopicNameParameterSet (Default)</span></span>
```
Get-AzEventGridTopicKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dba2f-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dba2f-106">TopicInputObjectParameterSet</span></span>
```
Get-AzEventGridTopicKey [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="dba2f-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="dba2f-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridTopicKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dba2f-108">설명</span><span class="sxs-lookup"><span data-stu-id="dba2f-108">DESCRIPTION</span></span>
<span data-ttu-id="dba2f-109">Event Grid 토픽에 이벤트를 게시하는 데 사용되는 공유 액세스 키를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dba2f-109">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="dba2f-110">예제</span><span class="sxs-lookup"><span data-stu-id="dba2f-110">EXAMPLES</span></span>

### <span data-ttu-id="dba2f-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="dba2f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopicKey -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="dba2f-112">리소스 그룹 \` \` \` MyResourceGroupName 에서 Event Grid 항목 항목1의 공유 액세스 키를 \` 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dba2f-112">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="dba2f-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="dba2f-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | Get-AzEventGridTopicKey
```

<span data-ttu-id="dba2f-114">리소스 그룹 \` \` \` MyResourceGroupName 에서 Event Grid 항목 항목1의 공유 액세스 키를 \` 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dba2f-114">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="dba2f-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="dba2f-115">PARAMETERS</span></span>

### <span data-ttu-id="dba2f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dba2f-116">-DefaultProfile</span></span>
<span data-ttu-id="dba2f-117">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="dba2f-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dba2f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dba2f-118">-InputObject</span></span>
<span data-ttu-id="dba2f-119">EventGrid 토픽 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="dba2f-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="dba2f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="dba2f-120">-Name</span></span>
<span data-ttu-id="dba2f-121">EventGrid 토픽 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dba2f-121">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="dba2f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dba2f-122">-ResourceGroupName</span></span>
<span data-ttu-id="dba2f-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dba2f-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="dba2f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dba2f-124">-ResourceId</span></span>
<span data-ttu-id="dba2f-125">Event Grid 토픽을 나타내는 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="dba2f-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="dba2f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dba2f-126">CommonParameters</span></span>
<span data-ttu-id="dba2f-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="dba2f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dba2f-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dba2f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dba2f-129">입력</span><span class="sxs-lookup"><span data-stu-id="dba2f-129">INPUTS</span></span>

### <span data-ttu-id="dba2f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="dba2f-130">System.String</span></span>

### <span data-ttu-id="dba2f-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="dba2f-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="dba2f-132">출력</span><span class="sxs-lookup"><span data-stu-id="dba2f-132">OUTPUTS</span></span>

### <span data-ttu-id="dba2f-133">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="dba2f-133">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="dba2f-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="dba2f-134">NOTES</span></span>

## <span data-ttu-id="dba2f-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dba2f-135">RELATED LINKS</span></span>
