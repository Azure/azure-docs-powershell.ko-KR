---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgriddomaintopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomainTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomainTopic.md
ms.openlocfilehash: 6f50f7e4224affb29584022ea8c61a4c0927a60d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376776"
---
# <span data-ttu-id="545e4-101">Remove-AzEventGridDomainTopic</span><span class="sxs-lookup"><span data-stu-id="545e4-101">Remove-AzEventGridDomainTopic</span></span>

## <span data-ttu-id="545e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="545e4-102">SYNOPSIS</span></span>
<span data-ttu-id="545e4-103">Azure Event Grid 도메인 토픽을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="545e4-103">Removes an Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="545e4-104">구문</span><span class="sxs-lookup"><span data-stu-id="545e4-104">SYNTAX</span></span>

### <span data-ttu-id="545e4-105">DomainTopicNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="545e4-105">DomainTopicNameParameterSet (Default)</span></span>
```
Remove-AzEventGridDomainTopic [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="545e4-106">ResourceIdDomainTopicParameterSet</span><span class="sxs-lookup"><span data-stu-id="545e4-106">ResourceIdDomainTopicParameterSet</span></span>
```
Remove-AzEventGridDomainTopic [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="545e4-107">DomainTopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="545e4-107">DomainTopicInputObjectParameterSet</span></span>
```
Remove-AzEventGridDomainTopic [-InputObject] <PSDomainTopic> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="545e4-108">설명</span><span class="sxs-lookup"><span data-stu-id="545e4-108">DESCRIPTION</span></span>
<span data-ttu-id="545e4-109">Azure Event Grid 도메인 토픽을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="545e4-109">Removes an Azure Event Grid Domain Topic.</span></span>

## <span data-ttu-id="545e4-110">예제</span><span class="sxs-lookup"><span data-stu-id="545e4-110">EXAMPLES</span></span>

### <span data-ttu-id="545e4-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="545e4-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridDomainTopic -ResourceGroupName MyResourceGroupName -DomainName Domain1 -Name Topic1
```

<span data-ttu-id="545e4-112">리소스 그룹 \` \` \` \` \` MyResourceGroupName의 Domain Domain1에서 Event Grid 도메인 항목 항목1을 \` 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="545e4-112">Removes the Event Grid Domain Topic \`Topic1\` under Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="545e4-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="545e4-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1/topics/Topic1" | Remove-AzEventGridDomainTopic
```

<span data-ttu-id="545e4-114">리소스 그룹 \` \` \` \` \` MyResourceGroupName의 Domain Domain1에서 Event Grid 도메인 항목 항목1을 \` 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="545e4-114">Removes the Event Grid Domain Topic \`Topic1\` under Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="545e4-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="545e4-115">PARAMETERS</span></span>

### <span data-ttu-id="545e4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="545e4-116">-DefaultProfile</span></span>
<span data-ttu-id="545e4-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="545e4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="545e4-118">-DomainName</span><span class="sxs-lookup"><span data-stu-id="545e4-118">-DomainName</span></span>
<span data-ttu-id="545e4-119">EventGrid 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="545e4-119">EventGrid domain name.</span></span>

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

### <span data-ttu-id="545e4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="545e4-120">-InputObject</span></span>
<span data-ttu-id="545e4-121">EventGrid 도메인 토픽 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="545e4-121">EventGrid Domain Topic object.</span></span>

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

### <span data-ttu-id="545e4-122">-Name</span><span class="sxs-lookup"><span data-stu-id="545e4-122">-Name</span></span>
<span data-ttu-id="545e4-123">EventGrid 도메인 토픽 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="545e4-123">EventGrid domain topic name.</span></span>

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

### <span data-ttu-id="545e4-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="545e4-124">-PassThru</span></span>
<span data-ttu-id="545e4-125">{{PassThru 설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="545e4-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="545e4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="545e4-126">-ResourceGroupName</span></span>
<span data-ttu-id="545e4-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="545e4-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="545e4-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="545e4-128">-ResourceId</span></span>
<span data-ttu-id="545e4-129">Event Grid 도메인 토픽을 나타내는 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="545e4-129">Resource Identifier representing the Event Grid Domain Topic.</span></span>

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

### <span data-ttu-id="545e4-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="545e4-130">-Confirm</span></span>
<span data-ttu-id="545e4-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="545e4-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="545e4-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="545e4-132">-WhatIf</span></span>
<span data-ttu-id="545e4-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="545e4-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="545e4-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="545e4-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="545e4-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="545e4-135">CommonParameters</span></span>
<span data-ttu-id="545e4-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="545e4-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="545e4-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="545e4-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="545e4-138">입력</span><span class="sxs-lookup"><span data-stu-id="545e4-138">INPUTS</span></span>

### <span data-ttu-id="545e4-139">System.String</span><span class="sxs-lookup"><span data-stu-id="545e4-139">System.String</span></span>

### <span data-ttu-id="545e4-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span><span class="sxs-lookup"><span data-stu-id="545e4-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomainTopic</span></span>

## <span data-ttu-id="545e4-141">출력</span><span class="sxs-lookup"><span data-stu-id="545e4-141">OUTPUTS</span></span>

### <span data-ttu-id="545e4-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="545e4-142">System.Boolean</span></span>

## <span data-ttu-id="545e4-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="545e4-143">NOTES</span></span>

## <span data-ttu-id="545e4-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="545e4-144">RELATED LINKS</span></span>
