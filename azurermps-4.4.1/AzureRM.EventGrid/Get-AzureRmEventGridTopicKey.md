---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicKey.md
ms.openlocfilehash: 91e3acd227acd8a83dcd5ccb0beb2ed12d1cca99
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711580"
---
# <span data-ttu-id="d2dc2-101">Get-AzureRmEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="d2dc2-101">Get-AzureRmEventGridTopicKey</span></span>

## <span data-ttu-id="d2dc2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2dc2-102">SYNOPSIS</span></span>
<span data-ttu-id="d2dc2-103">이벤트 그리드 항목에 이벤트를 게시 하는 데 사용 되는 공유 된 선택 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d2dc2-103">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2dc2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d2dc2-104">SYNTAX</span></span>

### <span data-ttu-id="d2dc2-105">TopicNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="d2dc2-105">TopicNameParameterSet (Default)</span></span>
```
Get-AzureRmEventGridTopicKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d2dc2-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2dc2-106">TopicInputObjectParameterSet</span></span>
```
Get-AzureRmEventGridTopicKey [-InputObject] <PSTopic> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d2dc2-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2dc2-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzureRmEventGridTopicKey [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d2dc2-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d2dc2-108">DESCRIPTION</span></span>
<span data-ttu-id="d2dc2-109">이벤트 그리드 항목에 이벤트를 게시 하는 데 사용 되는 공유 된 선택 키를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d2dc2-109">Gets the shared access keys used to publish events to an Event Grid topic.</span></span>

## <span data-ttu-id="d2dc2-110">예제의</span><span class="sxs-lookup"><span data-stu-id="d2dc2-110">EXAMPLES</span></span>

### <span data-ttu-id="d2dc2-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="d2dc2-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridTopicKey -ResourceGroup MyResourceGroupName -Name Topic1
```

<span data-ttu-id="d2dc2-112">\` \` 리소스 그룹 MyResourceGroupName에서 이벤트 그리드 Topic1에 대 한 공유 된 액세스 키를 가져옵니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="d2dc2-112">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="d2dc2-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="d2dc2-113">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | Get-AzureRmEventGridTopicKey
```

<span data-ttu-id="d2dc2-114">\` \` 리소스 그룹 MyResourceGroupName에서 이벤트 그리드 Topic1에 대 한 공유 된 액세스 키를 가져옵니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="d2dc2-114">Gets the shared access keys of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="d2dc2-115">변수</span><span class="sxs-lookup"><span data-stu-id="d2dc2-115">PARAMETERS</span></span>

### <span data-ttu-id="d2dc2-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2dc2-116">-InputObject</span></span>
<span data-ttu-id="d2dc2-117">EventGrid 주제 개체</span><span class="sxs-lookup"><span data-stu-id="d2dc2-117">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="d2dc2-118">-이름</span><span class="sxs-lookup"><span data-stu-id="d2dc2-118">-Name</span></span>
<span data-ttu-id="d2dc2-119">EventGrid 주제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d2dc2-119">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="d2dc2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2dc2-120">-ResourceGroupName</span></span>
<span data-ttu-id="d2dc2-121">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d2dc2-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="d2dc2-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2dc2-122">-ResourceId</span></span>
<span data-ttu-id="d2dc2-123">이벤트 그리드 항목을 나타내는 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="d2dc2-123">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="d2dc2-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2dc2-124">-DefaultProfile</span></span>
<span data-ttu-id="d2dc2-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d2dc2-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2dc2-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2dc2-126">CommonParameters</span></span>
<span data-ttu-id="d2dc2-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2dc2-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2dc2-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2dc2-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2dc2-129">입력</span><span class="sxs-lookup"><span data-stu-id="d2dc2-129">INPUTS</span></span>

### <span data-ttu-id="d2dc2-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d2dc2-130">System.String</span></span>

## <span data-ttu-id="d2dc2-131">출력</span><span class="sxs-lookup"><span data-stu-id="d2dc2-131">OUTPUTS</span></span>

### <span data-ttu-id="d2dc2-132">TopicSharedAccessKeys (Microsoft. 관리.</span><span class="sxs-lookup"><span data-stu-id="d2dc2-132">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="d2dc2-133">상속자</span><span class="sxs-lookup"><span data-stu-id="d2dc2-133">NOTES</span></span>

## <span data-ttu-id="d2dc2-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d2dc2-134">RELATED LINKS</span></span>

