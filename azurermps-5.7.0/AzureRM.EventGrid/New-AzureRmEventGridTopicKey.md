---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/new-azurermeventgridtopickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopicKey.md
ms.openlocfilehash: 3600d7523e95b937f20d9d0b97d677c5cf02ca0f
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/21/2020
ms.locfileid: "93538251"
---
# <span data-ttu-id="47dbb-101">New-AzureRmEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="47dbb-101">New-AzureRmEventGridTopicKey</span></span>

## <span data-ttu-id="47dbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47dbb-102">SYNOPSIS</span></span>
<span data-ttu-id="47dbb-103">Azure 이벤트 그리드 항목에 대 한 공유 된 선택 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="47dbb-103">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="47dbb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="47dbb-104">SYNTAX</span></span>

### <span data-ttu-id="47dbb-105">TopicNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="47dbb-105">TopicNameParameterSet (Default)</span></span>
```
New-AzureRmEventGridTopicKey [-ResourceGroupName] <String> [-TopicName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47dbb-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="47dbb-106">TopicInputObjectParameterSet</span></span>
```
New-AzureRmEventGridTopicKey [-KeyName] <String> [-InputObject] <PSTopic>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47dbb-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="47dbb-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzureRmEventGridTopicKey [-KeyName] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47dbb-108">설명은</span><span class="sxs-lookup"><span data-stu-id="47dbb-108">DESCRIPTION</span></span>
<span data-ttu-id="47dbb-109">Azure 이벤트 그리드 항목에 대 한 공유 된 선택 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="47dbb-109">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="47dbb-110">예제의</span><span class="sxs-lookup"><span data-stu-id="47dbb-110">EXAMPLES</span></span>

### <span data-ttu-id="47dbb-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="47dbb-111">Example 1</span></span>
```
PS C:\> New-AzureRmEventGridTopicKey -ResourceGroup MyResourceGroupName -TopicName Topic1 -KeyName key1
```

<span data-ttu-id="47dbb-112">\' \` 리소스 그룹 MyResourceGroupName에서 이벤트 그리드 Topic1의 키 key1 항목에 해당 하는 키를 다시 생성 \` \` \` 합니다.</span><span class="sxs-lookup"><span data-stu-id="47dbb-112">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="47dbb-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="47dbb-113">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | New-AzureRmEventGridTopicKey -KeyName "key1"
```

<span data-ttu-id="47dbb-114">\' \` 리소스 그룹 MyResourceGroupName에서 이벤트 그리드 Topic1의 키 key1 항목에 해당 하는 키를 다시 생성 \` \` \` 합니다.</span><span class="sxs-lookup"><span data-stu-id="47dbb-114">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="47dbb-115">변수</span><span class="sxs-lookup"><span data-stu-id="47dbb-115">PARAMETERS</span></span>

### <span data-ttu-id="47dbb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47dbb-116">-DefaultProfile</span></span>
<span data-ttu-id="47dbb-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="47dbb-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="47dbb-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47dbb-118">-InputObject</span></span>
<span data-ttu-id="47dbb-119">EventGrid 주제 개체</span><span class="sxs-lookup"><span data-stu-id="47dbb-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="47dbb-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="47dbb-120">-KeyName</span></span>
<span data-ttu-id="47dbb-121">다시 생성 해야 하는 키의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="47dbb-121">The name of the key that needs to be regenerated</span></span>

```yaml
Type: String
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: TopicInputObjectParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47dbb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47dbb-122">-ResourceGroupName</span></span>
<span data-ttu-id="47dbb-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="47dbb-123">Resource group name.</span></span>

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

### <span data-ttu-id="47dbb-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="47dbb-124">-ResourceId</span></span>
<span data-ttu-id="47dbb-125">이벤트 그리드 항목을 나타내는 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="47dbb-125">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="47dbb-126">-TopicName</span><span class="sxs-lookup"><span data-stu-id="47dbb-126">-TopicName</span></span>
<span data-ttu-id="47dbb-127">주제의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="47dbb-127">The name of the topic.</span></span>

```yaml
Type: String
Parameter Sets: TopicNameParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47dbb-128">-확인</span><span class="sxs-lookup"><span data-stu-id="47dbb-128">-Confirm</span></span>
<span data-ttu-id="47dbb-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="47dbb-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47dbb-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47dbb-130">-WhatIf</span></span>
<span data-ttu-id="47dbb-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="47dbb-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47dbb-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="47dbb-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47dbb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47dbb-133">CommonParameters</span></span>
<span data-ttu-id="47dbb-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="47dbb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47dbb-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="47dbb-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47dbb-136">입력</span><span class="sxs-lookup"><span data-stu-id="47dbb-136">INPUTS</span></span>

### <span data-ttu-id="47dbb-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="47dbb-137">System.String</span></span>

## <span data-ttu-id="47dbb-138">출력</span><span class="sxs-lookup"><span data-stu-id="47dbb-138">OUTPUTS</span></span>

### <span data-ttu-id="47dbb-139">TopicSharedAccessKeys (Microsoft. 관리.</span><span class="sxs-lookup"><span data-stu-id="47dbb-139">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="47dbb-140">상속자</span><span class="sxs-lookup"><span data-stu-id="47dbb-140">NOTES</span></span>

## <span data-ttu-id="47dbb-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="47dbb-141">RELATED LINKS</span></span>

