---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomainTopic.md
ms.openlocfilehash: 04bed413aca213a558ab1e0afaf5e6badcf238c2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696514"
---
# <span data-ttu-id="845a6-101">Remove-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="845a6-101">Remove-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="845a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="845a6-102">SYNOPSIS</span></span>
<span data-ttu-id="845a6-103">Azure 이벤트 그리드 도메인 항목을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="845a6-103">Removes an Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="845a6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="845a6-104">SYNTAX</span></span>

### <span data-ttu-id="845a6-105">DomainTopicNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="845a6-105">DomainTopicNameParameterSet (Default)</span></span>
```
Remove-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="845a6-106">ResourceIdDomainTopicParameterSet</span><span class="sxs-lookup"><span data-stu-id="845a6-106">ResourceIdDomainTopicParameterSet</span></span>
```
Remove-AzEventGridDomainTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="845a6-107">DomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="845a6-107">DomainTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridDomainTopic [-InputObject] <PSDomainTopic> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="845a6-108">설명은</span><span class="sxs-lookup"><span data-stu-id="845a6-108">DESCRIPTION</span></span>
<span data-ttu-id="845a6-109">Azure 이벤트 그리드 도메인 항목을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="845a6-109">Removes an Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="845a6-110">예제의</span><span class="sxs-lookup"><span data-stu-id="845a6-110">EXAMPLES</span></span>

### <span data-ttu-id="845a6-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="845a6-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridDomainTopic -ResourceGroupName MyResourceGroupName -DomainName Domain1 -Name Topic1
```

<span data-ttu-id="845a6-112">\` \` \` 리소스 그룹 MyResourceGroupName의 도메인 Domain1 아래 Topic1 이벤트 그리드 도메인 항목을 제거 \` \` \` 합니다.</span><span class="sxs-lookup"><span data-stu-id="845a6-112">Removes the Event Grid Domain Topic \`Topic1\` under Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="845a6-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="845a6-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/Topic1" | Remove-AzEventGridDomainTopic
```

<span data-ttu-id="845a6-114">\` \` \` 리소스 그룹 MyResourceGroupName의 도메인 Domain1 아래 Topic1 이벤트 그리드 도메인 항목을 제거 \` \` \` 합니다.</span><span class="sxs-lookup"><span data-stu-id="845a6-114">Removes the Event Grid Domain Topic \`Topic1\` under Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="845a6-115">변수</span><span class="sxs-lookup"><span data-stu-id="845a6-115">PARAMETERS</span></span>

### <span data-ttu-id="845a6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="845a6-116">-DefaultProfile</span></span>
<span data-ttu-id="845a6-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="845a6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="845a6-118">-DomainName</span><span class="sxs-lookup"><span data-stu-id="845a6-118">-DomainName</span></span>
<span data-ttu-id="845a6-119">EventGrid 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="845a6-119">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="845a6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="845a6-120">-InputObject</span></span>
<span data-ttu-id="845a6-121">EventGrid 도메인 주제 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="845a6-121">EventGrid Domain Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic
Parameter Sets: DomainTopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="845a6-122">-이름</span><span class="sxs-lookup"><span data-stu-id="845a6-122">-Name</span></span>
<span data-ttu-id="845a6-123">EventGrid 도메인 주제 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="845a6-123">EventGrid domain topic name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: DomainTopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="845a6-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="845a6-124">-PassThru</span></span>
<span data-ttu-id="845a6-125">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="845a6-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="845a6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="845a6-126">-ResourceGroupName</span></span>
<span data-ttu-id="845a6-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="845a6-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainTopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="845a6-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="845a6-128">-ResourceId</span></span>
<span data-ttu-id="845a6-129">이벤트 그리드 도메인 항목을 나타내는 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="845a6-129">Resource Identifier representing the Event Grid Domain Topic.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdDomainTopicParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="845a6-130">-확인</span><span class="sxs-lookup"><span data-stu-id="845a6-130">-Confirm</span></span>
<span data-ttu-id="845a6-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="845a6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="845a6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="845a6-132">-WhatIf</span></span>
<span data-ttu-id="845a6-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="845a6-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="845a6-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="845a6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="845a6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="845a6-135">CommonParameters</span></span>
<span data-ttu-id="845a6-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="845a6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="845a6-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="845a6-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="845a6-138">입력</span><span class="sxs-lookup"><span data-stu-id="845a6-138">INPUTS</span></span>

### <span data-ttu-id="845a6-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="845a6-139">System.String</span></span>

### <span data-ttu-id="845a6-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="845a6-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="845a6-141">출력</span><span class="sxs-lookup"><span data-stu-id="845a6-141">OUTPUTS</span></span>

### <span data-ttu-id="845a6-142">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="845a6-142">System.Boolean</span></span>

## <span data-ttu-id="845a6-143">상속자</span><span class="sxs-lookup"><span data-stu-id="845a6-143">NOTES</span></span>

## <span data-ttu-id="845a6-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="845a6-144">RELATED LINKS</span></span>