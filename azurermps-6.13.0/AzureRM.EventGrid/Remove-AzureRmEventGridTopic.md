---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventgrid/remove-azurermeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Remove-AzureRmEventGridTopic.md
ms.openlocfilehash: d853d5d4659e41c9696ab87c3f9ab8b58c240044
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530975"
---
# <span data-ttu-id="fee6e-101">Remove-AzureRmEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="fee6e-101">Remove-AzureRmEventGridTopic</span></span>

## <span data-ttu-id="fee6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fee6e-102">SYNOPSIS</span></span>
<span data-ttu-id="fee6e-103">Azure 이벤트 그리드 항목을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fee6e-103">Removes an Azure Event Grid Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fee6e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fee6e-104">SYNTAX</span></span>

### <span data-ttu-id="fee6e-105">TopicNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="fee6e-105">TopicNameParameterSet (Default)</span></span>
```
Remove-AzureRmEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fee6e-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="fee6e-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzureRmEventGridTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fee6e-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fee6e-107">TopicInputObjectParameterSet</span></span>
```
Remove-AzureRmEventGridTopic [-InputObject] <PSTopic> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fee6e-108">설명은</span><span class="sxs-lookup"><span data-stu-id="fee6e-108">DESCRIPTION</span></span>
<span data-ttu-id="fee6e-109">Azure 이벤트 그리드 항목을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fee6e-109">Removes an Azure Event Grid Topic.</span></span>

## <span data-ttu-id="fee6e-110">예제의</span><span class="sxs-lookup"><span data-stu-id="fee6e-110">EXAMPLES</span></span>

### <span data-ttu-id="fee6e-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="fee6e-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1
```

<span data-ttu-id="fee6e-112">\` \` 리소스 그룹 MyResourceGroupName에서 이벤트 눈금 주제 Topic1를 제거 합니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="fee6e-112">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="fee6e-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="fee6e-113">Example 2</span></span>
```
PS C:\> Get-AzureRmResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/topics/Topic1" | Remove-AzureRmEventGridTopic
```

<span data-ttu-id="fee6e-114">\` \` 리소스 그룹 MyResourceGroupName에서 이벤트 눈금 주제 Topic1를 제거 합니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="fee6e-114">Removes the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="fee6e-115">변수</span><span class="sxs-lookup"><span data-stu-id="fee6e-115">PARAMETERS</span></span>

### <span data-ttu-id="fee6e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fee6e-116">-DefaultProfile</span></span>
<span data-ttu-id="fee6e-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="fee6e-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fee6e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fee6e-118">-InputObject</span></span>
<span data-ttu-id="fee6e-119">EventGrid 주제 개체</span><span class="sxs-lookup"><span data-stu-id="fee6e-119">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="fee6e-120">-이름</span><span class="sxs-lookup"><span data-stu-id="fee6e-120">-Name</span></span>
<span data-ttu-id="fee6e-121">EventGrid 주제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fee6e-121">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="fee6e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fee6e-122">-PassThru</span></span>
<span data-ttu-id="fee6e-123">제거 작업의 상태를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="fee6e-123">Returns the status of the Remove operation.</span></span> <span data-ttu-id="fee6e-124">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fee6e-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fee6e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fee6e-125">-ResourceGroupName</span></span>
<span data-ttu-id="fee6e-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fee6e-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="fee6e-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fee6e-127">-ResourceId</span></span>
<span data-ttu-id="fee6e-128">EventGrid 항목 ResourceID.</span><span class="sxs-lookup"><span data-stu-id="fee6e-128">EventGrid Topic ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fee6e-129">-확인</span><span class="sxs-lookup"><span data-stu-id="fee6e-129">-Confirm</span></span>
<span data-ttu-id="fee6e-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fee6e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fee6e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fee6e-131">-WhatIf</span></span>
<span data-ttu-id="fee6e-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fee6e-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fee6e-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fee6e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fee6e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fee6e-134">CommonParameters</span></span>
<span data-ttu-id="fee6e-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fee6e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fee6e-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fee6e-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fee6e-137">입력</span><span class="sxs-lookup"><span data-stu-id="fee6e-137">INPUTS</span></span>

### <span data-ttu-id="fee6e-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fee6e-138">System.String</span></span>

### <span data-ttu-id="fee6e-139">Microsoft. Azure. c c.</span><span class="sxs-lookup"><span data-stu-id="fee6e-139">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>
<span data-ttu-id="fee6e-140">매개 변수: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fee6e-140">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="fee6e-141">출력</span><span class="sxs-lookup"><span data-stu-id="fee6e-141">OUTPUTS</span></span>

### <span data-ttu-id="fee6e-142">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="fee6e-142">System.Boolean</span></span>

## <span data-ttu-id="fee6e-143">상속자</span><span class="sxs-lookup"><span data-stu-id="fee6e-143">NOTES</span></span>

## <span data-ttu-id="fee6e-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fee6e-144">RELATED LINKS</span></span>
