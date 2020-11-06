---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/New-AzureRmEventGridTopicKey.md
ms.openlocfilehash: bb9cd92ff614a944c144f056d8d59aa1d4239b25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537283"
---
# <span data-ttu-id="d8662-101">New-AzureRmEventGridTopicKey</span><span class="sxs-lookup"><span data-stu-id="d8662-101">New-AzureRmEventGridTopicKey</span></span>

## <span data-ttu-id="d8662-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8662-102">SYNOPSIS</span></span>
<span data-ttu-id="d8662-103">Azure 이벤트 그리드 항목에 대 한 공유 된 선택 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8662-103">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8662-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d8662-104">SYNTAX</span></span>

### <span data-ttu-id="d8662-105">TopicNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="d8662-105">TopicNameParameterSet (Default)</span></span>
```
New-AzureRmEventGridTopicKey [-ResourceGroupName] <String> [-TopicName] <String> [-KeyName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8662-106">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8662-106">TopicInputObjectParameterSet</span></span>
```
New-AzureRmEventGridTopicKey [-KeyName] <String> [-InputObject] <PSTopic>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8662-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8662-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzureRmEventGridTopicKey [-KeyName] <String> [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8662-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d8662-108">DESCRIPTION</span></span>
<span data-ttu-id="d8662-109">Azure 이벤트 그리드 항목에 대 한 공유 된 선택 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8662-109">Regenerates the shared access key for an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="d8662-110">예제의</span><span class="sxs-lookup"><span data-stu-id="d8662-110">EXAMPLES</span></span>

### <span data-ttu-id="d8662-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="d8662-111">Example 1</span></span>
```
PS C:\> New-AzureRmEventGridTopicKey -ResourceGroup MyResourceGroupName -TopicName Topic1 -KeyName key1
```

<span data-ttu-id="d8662-112">\' \` 리소스 그룹 MyResourceGroupName에서 이벤트 그리드 Topic1의 키 key1 항목에 해당 하는 키를 다시 생성 \` \` \` 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8662-112">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="d8662-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="d8662-113">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 | New-AzureRmEventGridTopicKey -KeyName "key1"
```

<span data-ttu-id="d8662-114">\' \` 리소스 그룹 MyResourceGroupName에서 이벤트 그리드 Topic1의 키 key1 항목에 해당 하는 키를 다시 생성 \` \` \` 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8662-114">Regenerate the key corresponding to key \'key1'\ of Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="d8662-115">변수</span><span class="sxs-lookup"><span data-stu-id="d8662-115">PARAMETERS</span></span>

### <span data-ttu-id="d8662-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8662-116">-InputObject</span></span>
<span data-ttu-id="d8662-117">EventGrid 주제 개체</span><span class="sxs-lookup"><span data-stu-id="d8662-117">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="d8662-118">-KeyName</span><span class="sxs-lookup"><span data-stu-id="d8662-118">-KeyName</span></span>
<span data-ttu-id="d8662-119">다시 생성 해야 하는 키의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d8662-119">The name of the key that needs to be regenerated</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicInputObjectParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8662-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8662-120">-ResourceGroupName</span></span>
<span data-ttu-id="d8662-121">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d8662-121">Resource group name.</span></span>

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

### <span data-ttu-id="d8662-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d8662-122">-ResourceId</span></span>
<span data-ttu-id="d8662-123">이벤트 그리드 항목을 나타내는 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="d8662-123">Resource Identifier representing the Event Grid Topic.</span></span>

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

### <span data-ttu-id="d8662-124">-TopicName</span><span class="sxs-lookup"><span data-stu-id="d8662-124">-TopicName</span></span>
<span data-ttu-id="d8662-125">주제의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d8662-125">The name of the topic.</span></span>

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

### <span data-ttu-id="d8662-126">-확인</span><span class="sxs-lookup"><span data-stu-id="d8662-126">-Confirm</span></span>
<span data-ttu-id="d8662-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8662-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8662-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8662-128">-WhatIf</span></span>
<span data-ttu-id="d8662-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d8662-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8662-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d8662-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8662-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8662-131">-DefaultProfile</span></span>
<span data-ttu-id="d8662-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d8662-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8662-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8662-133">CommonParameters</span></span>
<span data-ttu-id="d8662-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d8662-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8662-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8662-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8662-136">입력</span><span class="sxs-lookup"><span data-stu-id="d8662-136">INPUTS</span></span>

### <span data-ttu-id="d8662-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d8662-137">System.String</span></span>

## <span data-ttu-id="d8662-138">출력</span><span class="sxs-lookup"><span data-stu-id="d8662-138">OUTPUTS</span></span>

### <span data-ttu-id="d8662-139">TopicSharedAccessKeys (Microsoft. 관리.</span><span class="sxs-lookup"><span data-stu-id="d8662-139">Microsoft.Azure.Management.EventGrid.Models.TopicSharedAccessKeys</span></span>

## <span data-ttu-id="d8662-140">상속자</span><span class="sxs-lookup"><span data-stu-id="d8662-140">NOTES</span></span>

## <span data-ttu-id="d8662-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d8662-141">RELATED LINKS</span></span>

