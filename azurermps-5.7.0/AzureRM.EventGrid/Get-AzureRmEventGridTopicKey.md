---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/get-azurermeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicKey.md
ms.openlocfilehash: 741a888287ba7fcb4a9b54c1281a6a27be5fbb0a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93704030"
---
# <span data-ttu-id="7d107-101">Get-AzureRmEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="7d107-101">Get-AzureRmEventGridTopicKey</span></span>

## <span data-ttu-id="7d107-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d107-102">SYNOPSIS</span></span>
<span data-ttu-id="7d107-103">이벤트 그리드 항목에 이벤트를 게시 하는 데 사용 되는 공유 된 선택 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7d107-103">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d107-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7d107-104">SYNTAX</span></span>

### <span data-ttu-id="7d107-105">TopicNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="7d107-105">TopicNameParameterSet (Default)</span></span>
```
Get-AzureRmEventGridTopicKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d107-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d107-106">TopicInputObjectParameterSet</span></span>
```
Get-AzureRmEventGridTopicKey [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7d107-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d107-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzureRmEventGridTopicKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7d107-108">설명은</span><span class="sxs-lookup"><span data-stu-id="7d107-108">DESCRIPTION</span></span>
<span data-ttu-id="7d107-109">이벤트 그리드 항목에 이벤트를 게시 하는 데 사용 되는 공유 된 선택 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7d107-109">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="7d107-110">예제의</span><span class="sxs-lookup"><span data-stu-id="7d107-110">EXAMPLES</span></span>

### <span data-ttu-id="7d107-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="7d107-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridTopicKey -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="7d107-112">\` \` 리소스 그룹 MyResourceGroupName에서 이벤트 그리드 Topic1에 대 한 공유 된 액세스 키를 가져옵니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="7d107-112">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="7d107-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="7d107-113">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | Get-AzureRmEventGridTopicKey
```

<span data-ttu-id="7d107-114">\` \` 리소스 그룹 MyResourceGroupName에서 이벤트 그리드 Topic1에 대 한 공유 된 액세스 키를 가져옵니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="7d107-114">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="7d107-115">변수</span><span class="sxs-lookup"><span data-stu-id="7d107-115">PARAMETERS</span></span>

### <span data-ttu-id="7d107-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d107-116">-DefaultProfile</span></span>
<span data-ttu-id="7d107-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7d107-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d107-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7d107-118">-InputObject</span></span>
<span data-ttu-id="7d107-119">EventGrid 주제 개체</span><span class="sxs-lookup"><span data-stu-id="7d107-119">EventGrid Topic object.</span></span>

```yaml
Type: PSTopic
Parameter Sets: TopicInputObjectParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d107-120">-이름</span><span class="sxs-lookup"><span data-stu-id="7d107-120">-Name</span></span>
<span data-ttu-id="7d107-121">EventGrid 주제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7d107-121">EventGrid Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d107-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d107-122">-ResourceGroupName</span></span>
<span data-ttu-id="7d107-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7d107-123">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d107-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d107-124">-ResourceId</span></span>
<span data-ttu-id="7d107-125">이벤트 그리드 항목을 나타내는 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="7d107-125">Resource Identifier representing the Event Grid Topic.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d107-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d107-126">CommonParameters</span></span>
<span data-ttu-id="7d107-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7d107-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d107-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d107-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d107-129">입력</span><span class="sxs-lookup"><span data-stu-id="7d107-129">INPUTS</span></span>

### <span data-ttu-id="7d107-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7d107-130">System.String</span></span>

## <span data-ttu-id="7d107-131">출력</span><span class="sxs-lookup"><span data-stu-id="7d107-131">OUTPUTS</span></span>

### <span data-ttu-id="7d107-132">TopicSharedAccessKeys (Microsoft. 관리.</span><span class="sxs-lookup"><span data-stu-id="7d107-132">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="7d107-133">상속자</span><span class="sxs-lookup"><span data-stu-id="7d107-133">NOTES</span></span>

## <span data-ttu-id="7d107-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7d107-134">RELATED LINKS</span></span>

