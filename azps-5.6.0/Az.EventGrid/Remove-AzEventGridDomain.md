---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/remove-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
ms.openlocfilehash: 703b01ef012f77126e0db3d425cd892fa7256317
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964720"
---
# <span data-ttu-id="84339-101">Remove-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="84339-101">Remove-AzEventGridDomain</span></span>

## <span data-ttu-id="84339-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84339-102">SYNOPSIS</span></span>
<span data-ttu-id="84339-103">Azure Event Grid 도메인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="84339-103">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="84339-104">구문</span><span class="sxs-lookup"><span data-stu-id="84339-104">SYNTAX</span></span>

### <span data-ttu-id="84339-105">DomainNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="84339-105">DomainNameParameterSet (Default)</span></span>
```
Remove-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84339-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="84339-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridDomain [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84339-107">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="84339-107">DomainInputObjectParameterSet</span></span>
```
Remove-AzEventGridDomain [-InputObject] <PSDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84339-108">설명</span><span class="sxs-lookup"><span data-stu-id="84339-108">DESCRIPTION</span></span>
<span data-ttu-id="84339-109">Azure Event Grid 도메인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="84339-109">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="84339-110">예제</span><span class="sxs-lookup"><span data-stu-id="84339-110">EXAMPLES</span></span>

### <span data-ttu-id="84339-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="84339-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1
```

<span data-ttu-id="84339-112">리소스 그룹 \` \` \` MyResourceGroupName에서 Event Grid Domain1을 \` 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="84339-112">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="84339-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="84339-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/Domains/Domain1" | Remove-AzEventGridDomain
```

<span data-ttu-id="84339-114">리소스 그룹 \` \` \` MyResourceGroupName에서 Event Grid Domain1을 \` 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="84339-114">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="84339-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="84339-115">PARAMETERS</span></span>

### <span data-ttu-id="84339-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84339-116">-DefaultProfile</span></span>
<span data-ttu-id="84339-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="84339-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84339-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="84339-118">-InputObject</span></span>
<span data-ttu-id="84339-119">EventGrid 도메인 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="84339-119">EventGrid Domain object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomain
Parameter Sets: DomainInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84339-120">-Name</span><span class="sxs-lookup"><span data-stu-id="84339-120">-Name</span></span>
<span data-ttu-id="84339-121">EventGrid 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="84339-121">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84339-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="84339-122">-PassThru</span></span>
<span data-ttu-id="84339-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="84339-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="84339-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84339-124">-ResourceGroupName</span></span>
<span data-ttu-id="84339-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="84339-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84339-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="84339-126">-ResourceId</span></span>
<span data-ttu-id="84339-127">Event Grid 도메인을 나타내는 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="84339-127">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="84339-128">-확인</span><span class="sxs-lookup"><span data-stu-id="84339-128">-Confirm</span></span>
<span data-ttu-id="84339-129">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="84339-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84339-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84339-130">-WhatIf</span></span>
<span data-ttu-id="84339-131">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="84339-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84339-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="84339-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84339-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84339-133">CommonParameters</span></span>
<span data-ttu-id="84339-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="84339-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84339-135">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="84339-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84339-136">입력</span><span class="sxs-lookup"><span data-stu-id="84339-136">INPUTS</span></span>

### <span data-ttu-id="84339-137">System.String</span><span class="sxs-lookup"><span data-stu-id="84339-137">System.String</span></span>

### <span data-ttu-id="84339-138">Microsoft.Azure.Commands.EventGrid.Models.PSD오마인</span><span class="sxs-lookup"><span data-stu-id="84339-138">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="84339-139">출력</span><span class="sxs-lookup"><span data-stu-id="84339-139">OUTPUTS</span></span>

### <span data-ttu-id="84339-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="84339-140">System.Boolean</span></span>

## <span data-ttu-id="84339-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="84339-141">NOTES</span></span>

## <span data-ttu-id="84339-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="84339-142">RELATED LINKS</span></span>
