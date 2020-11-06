---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/set-azurermeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Set-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Set-AzureRmEventGridTopic.md
ms.openlocfilehash: 384c05e6424ab7b8d4fbb01a0c4822b73702c419
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530974"
---
# <span data-ttu-id="eebcb-101">Set-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="eebcb-101">Set-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="eebcb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="eebcb-102">SYNOPSIS</span></span>
<span data-ttu-id="eebcb-103">이벤트 그리드 항목의 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eebcb-103">Sets the properties of an Event Grid topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eebcb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="eebcb-104">SYNTAX</span></span>

### <span data-ttu-id="eebcb-105">TopicNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="eebcb-105">TopicNameParameterSet (Default)</span></span>
```
Set-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eebcb-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="eebcb-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Set-AzureRmEventGridTopic [-ResourceId] <String> [-Tag] <Hashtable> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eebcb-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eebcb-107">TopicInputObjectParameterSet</span></span>
```
Set-AzureRmEventGridTopic [-InputObject] <PSTopic> [-Tag] <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eebcb-108">설명은</span><span class="sxs-lookup"><span data-stu-id="eebcb-108">DESCRIPTION</span></span>
<span data-ttu-id="eebcb-109">이벤트 그리드 항목의 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eebcb-109">Sets the properties of an Event Grid topic.</span></span> <span data-ttu-id="eebcb-110">이를 사용 하 여 이벤트 그리드 항목의 태그를 바꿀 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="eebcb-110">This can be used to replace the tags of an Event Grid topic.</span></span>

## <span data-ttu-id="eebcb-111">예제의</span><span class="sxs-lookup"><span data-stu-id="eebcb-111">EXAMPLES</span></span>

### <span data-ttu-id="eebcb-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="eebcb-112">Example 1</span></span>
```
PS C:\> Set-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="eebcb-113">\` \` \` \` 태그를 지정 된 태그 "부서" 및 "환경"으로 바꾸도록 리소스 그룹 MyResourceGroupName에서 이벤트 그리드 항목 Topic1의 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="eebcb-113">Sets the properties of the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` to replace the tags with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="eebcb-114">변수</span><span class="sxs-lookup"><span data-stu-id="eebcb-114">PARAMETERS</span></span>

### <span data-ttu-id="eebcb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eebcb-115">-DefaultProfile</span></span>
<span data-ttu-id="eebcb-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="eebcb-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eebcb-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="eebcb-117">-InputObject</span></span>
<span data-ttu-id="eebcb-118">EventGrid 주제 개체</span><span class="sxs-lookup"><span data-stu-id="eebcb-118">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="eebcb-119">-이름</span><span class="sxs-lookup"><span data-stu-id="eebcb-119">-Name</span></span>
<span data-ttu-id="eebcb-120">EventGrid 주제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eebcb-120">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="eebcb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eebcb-121">-ResourceGroupName</span></span>
<span data-ttu-id="eebcb-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="eebcb-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="eebcb-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="eebcb-123">-ResourceId</span></span>
<span data-ttu-id="eebcb-124">EventGrid 항목 ResourceID.</span><span class="sxs-lookup"><span data-stu-id="eebcb-124">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="eebcb-125">태그</span><span class="sxs-lookup"><span data-stu-id="eebcb-125">-Tag</span></span>
<span data-ttu-id="eebcb-126">리소스 태그를 나타내는 Hashtables입니다.</span><span class="sxs-lookup"><span data-stu-id="eebcb-126">Hashtables which represents resource Tag.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eebcb-127">-확인</span><span class="sxs-lookup"><span data-stu-id="eebcb-127">-Confirm</span></span>
<span data-ttu-id="eebcb-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="eebcb-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eebcb-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eebcb-129">-WhatIf</span></span>
<span data-ttu-id="eebcb-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="eebcb-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eebcb-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="eebcb-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eebcb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eebcb-132">CommonParameters</span></span>
<span data-ttu-id="eebcb-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="eebcb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eebcb-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eebcb-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eebcb-135">입력</span><span class="sxs-lookup"><span data-stu-id="eebcb-135">INPUTS</span></span>

### <span data-ttu-id="eebcb-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="eebcb-136">System.String</span></span>

### <span data-ttu-id="eebcb-137">Microsoft. Azure. c c.</span><span class="sxs-lookup"><span data-stu-id="eebcb-137">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>
<span data-ttu-id="eebcb-138">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="eebcb-138">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="eebcb-139">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="eebcb-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="eebcb-140">출력</span><span class="sxs-lookup"><span data-stu-id="eebcb-140">OUTPUTS</span></span>

### <span data-ttu-id="eebcb-141">Microsoft. Azure. c c.</span><span class="sxs-lookup"><span data-stu-id="eebcb-141">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="eebcb-142">상속자</span><span class="sxs-lookup"><span data-stu-id="eebcb-142">NOTES</span></span>

## <span data-ttu-id="eebcb-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="eebcb-143">RELATED LINKS</span></span>
