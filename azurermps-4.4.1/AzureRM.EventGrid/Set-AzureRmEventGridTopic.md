---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Set-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Set-AzureRmEventGridTopic.md
ms.openlocfilehash: 509f10432139ca0f2d9aaca216f22d998b7963a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537271"
---
# <span data-ttu-id="453e2-101">Set-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="453e2-101">Set-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="453e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="453e2-102">SYNOPSIS</span></span>
<span data-ttu-id="453e2-103">이벤트 그리드 항목의 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="453e2-103">Set the properties of an Event Grid topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="453e2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="453e2-104">SYNTAX</span></span>

### <span data-ttu-id="453e2-105">TopicNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="453e2-105">TopicNameParameterSet (Default)</span></span>
```
Set-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="453e2-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="453e2-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Set-AzureRmEventGridTopic [-ResourceId] <String> [-Tag] <Hashtable> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="453e2-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="453e2-107">TopicInputObjectParameterSet</span></span>
```
Set-AzureRmEventGridTopic [-InputObject] <PSTopic> [-Tag] <Hashtable>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="453e2-108">설명은</span><span class="sxs-lookup"><span data-stu-id="453e2-108">DESCRIPTION</span></span>
<span data-ttu-id="453e2-109">이벤트 그리드 항목의 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="453e2-109">Set the properties of an Event Grid topic.</span></span> <span data-ttu-id="453e2-110">이를 사용 하 여 이벤트 그리드 항목의 태그를 바꿀 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="453e2-110">This can be used to replace the tags of an Event Grid topic.</span></span>

## <span data-ttu-id="453e2-111">예제의</span><span class="sxs-lookup"><span data-stu-id="453e2-111">EXAMPLES</span></span>

### <span data-ttu-id="453e2-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="453e2-112">Example 1</span></span>
```
PS C:\> Set-AzureRmEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="453e2-113">\` \` \` \` 태그를 지정 된 태그 "부서" 및 "환경"으로 바꾸도록 리소스 그룹 MyResourceGroupName에서 이벤트 그리드 항목 Topic1의 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="453e2-113">Sets the properties of the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` to replace the tags with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="453e2-114">변수</span><span class="sxs-lookup"><span data-stu-id="453e2-114">PARAMETERS</span></span>

### <span data-ttu-id="453e2-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="453e2-115">-InputObject</span></span>
<span data-ttu-id="453e2-116">EventGrid 주제 개체</span><span class="sxs-lookup"><span data-stu-id="453e2-116">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="453e2-117">-이름</span><span class="sxs-lookup"><span data-stu-id="453e2-117">-Name</span></span>
<span data-ttu-id="453e2-118">EventGrid 주제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="453e2-118">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="453e2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="453e2-119">-ResourceGroupName</span></span>
<span data-ttu-id="453e2-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="453e2-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="453e2-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="453e2-121">-ResourceId</span></span>
<span data-ttu-id="453e2-122">EventGrid 항목 ResourceID.</span><span class="sxs-lookup"><span data-stu-id="453e2-122">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="453e2-123">태그</span><span class="sxs-lookup"><span data-stu-id="453e2-123">-Tag</span></span>
<span data-ttu-id="453e2-124">리소스 태그를 나타내는 Hashtables입니다.</span><span class="sxs-lookup"><span data-stu-id="453e2-124">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="453e2-125">-확인</span><span class="sxs-lookup"><span data-stu-id="453e2-125">-Confirm</span></span>
<span data-ttu-id="453e2-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="453e2-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="453e2-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="453e2-127">-WhatIf</span></span>
<span data-ttu-id="453e2-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="453e2-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="453e2-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="453e2-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="453e2-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="453e2-130">-DefaultProfile</span></span>
<span data-ttu-id="453e2-131">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="453e2-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="453e2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="453e2-132">CommonParameters</span></span>
<span data-ttu-id="453e2-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="453e2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="453e2-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="453e2-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="453e2-135">입력</span><span class="sxs-lookup"><span data-stu-id="453e2-135">INPUTS</span></span>

### <span data-ttu-id="453e2-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="453e2-136">System.String</span></span>
<span data-ttu-id="453e2-137">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="453e2-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="453e2-138">출력</span><span class="sxs-lookup"><span data-stu-id="453e2-138">OUTPUTS</span></span>

### <span data-ttu-id="453e2-139">Microsoft. Azure. 관리. 항목</span><span class="sxs-lookup"><span data-stu-id="453e2-139">Microsoft.Azure.Management.EventGrid.Models.Topic</span></span>

## <span data-ttu-id="453e2-140">상속자</span><span class="sxs-lookup"><span data-stu-id="453e2-140">NOTES</span></span>

## <span data-ttu-id="453e2-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="453e2-141">RELATED LINKS</span></span>

