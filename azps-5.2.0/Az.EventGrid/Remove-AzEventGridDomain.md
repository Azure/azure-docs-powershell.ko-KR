---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/remove-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Remove-AzEventGridDomain.md
ms.openlocfilehash: 88d5e0baadaa625a2cd33a795b66d7484d496330
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363707"
---
# <span data-ttu-id="67ef4-101">Remove-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="67ef4-101">Remove-AzEventGridDomain</span></span>

## <span data-ttu-id="67ef4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67ef4-102">SYNOPSIS</span></span>
<span data-ttu-id="67ef4-103">Azure Event Grid 도메인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="67ef4-103">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="67ef4-104">구문</span><span class="sxs-lookup"><span data-stu-id="67ef4-104">SYNTAX</span></span>

### <span data-ttu-id="67ef4-105">DomainNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="67ef4-105">DomainNameParameterSet (Default)</span></span>
```
Remove-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67ef4-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="67ef4-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Remove-AzEventGridDomain [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67ef4-107">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="67ef4-107">DomainInputObjectParameterSet</span></span>
```
Remove-AzEventGridDomain [-InputObject] <PSDomain> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67ef4-108">설명</span><span class="sxs-lookup"><span data-stu-id="67ef4-108">DESCRIPTION</span></span>
<span data-ttu-id="67ef4-109">Azure Event Grid 도메인을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="67ef4-109">Removes an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="67ef4-110">예제</span><span class="sxs-lookup"><span data-stu-id="67ef4-110">EXAMPLES</span></span>

### <span data-ttu-id="67ef4-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="67ef4-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1
```

<span data-ttu-id="67ef4-112">리소스 그룹 \` \` \` MyResourceGroupName에서 Event Grid 도메인 도메인 1을 \` 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="67ef4-112">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="67ef4-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="67ef4-113">Example 2</span></span>
```powershell
PS C:\> Get-AzResource -ResourceId "/subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/Domains/Domain1" | Remove-AzEventGridDomain
```

<span data-ttu-id="67ef4-114">리소스 그룹 \` \` \` MyResourceGroupName에서 Event Grid 도메인 도메인 1을 \` 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="67ef4-114">Removes the Event Grid Domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="67ef4-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67ef4-115">PARAMETERS</span></span>

### <span data-ttu-id="67ef4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67ef4-116">-DefaultProfile</span></span>
<span data-ttu-id="67ef4-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="67ef4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67ef4-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="67ef4-118">-InputObject</span></span>
<span data-ttu-id="67ef4-119">EventGrid 도메인 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="67ef4-119">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="67ef4-120">-Name</span><span class="sxs-lookup"><span data-stu-id="67ef4-120">-Name</span></span>
<span data-ttu-id="67ef4-121">EventGrid 도메인 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="67ef4-121">EventGrid domain name.</span></span>

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

### <span data-ttu-id="67ef4-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="67ef4-122">-PassThru</span></span>
<span data-ttu-id="67ef4-123">{{PassThru 설명 채우기}}</span><span class="sxs-lookup"><span data-stu-id="67ef4-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="67ef4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67ef4-124">-ResourceGroupName</span></span>
<span data-ttu-id="67ef4-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="67ef4-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="67ef4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="67ef4-126">-ResourceId</span></span>
<span data-ttu-id="67ef4-127">Event Grid 도메인을 나타내는 리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="67ef4-127">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="67ef4-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="67ef4-128">-Confirm</span></span>
<span data-ttu-id="67ef4-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="67ef4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67ef4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67ef4-130">-WhatIf</span></span>
<span data-ttu-id="67ef4-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="67ef4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67ef4-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="67ef4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67ef4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67ef4-133">CommonParameters</span></span>
<span data-ttu-id="67ef4-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="67ef4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67ef4-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="67ef4-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67ef4-136">입력</span><span class="sxs-lookup"><span data-stu-id="67ef4-136">INPUTS</span></span>

### <span data-ttu-id="67ef4-137">System.String</span><span class="sxs-lookup"><span data-stu-id="67ef4-137">System.String</span></span>

### <span data-ttu-id="67ef4-138">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="67ef4-138">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="67ef4-139">출력</span><span class="sxs-lookup"><span data-stu-id="67ef4-139">OUTPUTS</span></span>

### <span data-ttu-id="67ef4-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="67ef4-140">System.Boolean</span></span>

## <span data-ttu-id="67ef4-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="67ef4-141">NOTES</span></span>

## <span data-ttu-id="67ef4-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="67ef4-142">RELATED LINKS</span></span>
