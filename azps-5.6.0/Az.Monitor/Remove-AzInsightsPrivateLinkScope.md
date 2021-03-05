---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/remove-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: af33bf23e6cd488f98e38c9bd2696029b5510aca
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984508"
---
# <span data-ttu-id="bca89-101">Remove-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="bca89-101">Remove-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="bca89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bca89-102">SYNOPSIS</span></span>
<span data-ttu-id="bca89-103">개인 링크 범위 삭제</span><span class="sxs-lookup"><span data-stu-id="bca89-103">delete private link scope</span></span>

## <span data-ttu-id="bca89-104">구문</span><span class="sxs-lookup"><span data-stu-id="bca89-104">SYNTAX</span></span>

### <span data-ttu-id="bca89-105">ByResourceNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="bca89-105">ByResourceNameParameterSet (Default)</span></span>
```
Remove-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bca89-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="bca89-106">ByResourceIdParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScope -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bca89-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bca89-107">ByInputObjectParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScope -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bca89-108">설명</span><span class="sxs-lookup"><span data-stu-id="bca89-108">DESCRIPTION</span></span>
<span data-ttu-id="bca89-109">개인 링크 범위 삭제</span><span class="sxs-lookup"><span data-stu-id="bca89-109">delete private link scope</span></span>

## <span data-ttu-id="bca89-110">예제</span><span class="sxs-lookup"><span data-stu-id="bca89-110">EXAMPLES</span></span>

### <span data-ttu-id="bca89-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="bca89-111">Example 1</span></span>
```powershell
Remove-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="bca89-112">리소스 그룹 "scope_name"에서 이름 "scope_name"가 있는 개인 링크 rg_name</span><span class="sxs-lookup"><span data-stu-id="bca89-112">delete private link scope with name "scope_name" under resource group "rg_name"</span></span>

### <span data-ttu-id="bca89-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="bca89-113">Example 2</span></span>
```powershell
Remove-AzInsightsPrivateLinkScope -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/rg_name/providers/microsoft.insights/privateLinkScopes/scope_name"
```

<span data-ttu-id="bca89-114">리소스 ID를 사용하여 개인 링크 범위 삭제</span><span class="sxs-lookup"><span data-stu-id="bca89-114">delete private link scope with resource Id</span></span>

### <span data-ttu-id="bca89-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="bca89-115">Example 3</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" | Remove-AzInsightsPrivateLinkScope
```

<span data-ttu-id="bca89-116">입력 개인 링크 범위 개체가 있는 개인 링크 범위 삭제</span><span class="sxs-lookup"><span data-stu-id="bca89-116">delete private link scope with input private link scope object</span></span>

## <span data-ttu-id="bca89-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="bca89-117">PARAMETERS</span></span>

### <span data-ttu-id="bca89-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bca89-118">-DefaultProfile</span></span>
<span data-ttu-id="bca89-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bca89-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bca89-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bca89-120">-InputObject</span></span>
<span data-ttu-id="bca89-121">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="bca89-121">PSMonitorPrivateLinkScope</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bca89-122">-Name</span><span class="sxs-lookup"><span data-stu-id="bca89-122">-Name</span></span>
<span data-ttu-id="bca89-123">개인 링크 범위 이름</span><span class="sxs-lookup"><span data-stu-id="bca89-123">Private Link Scope Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bca89-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bca89-124">-ResourceGroupName</span></span>
<span data-ttu-id="bca89-125">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="bca89-125">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bca89-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bca89-126">-ResourceId</span></span>
<span data-ttu-id="bca89-127">리소스 ID</span><span class="sxs-lookup"><span data-stu-id="bca89-127">Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bca89-128">-확인</span><span class="sxs-lookup"><span data-stu-id="bca89-128">-Confirm</span></span>
<span data-ttu-id="bca89-129">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bca89-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bca89-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bca89-130">-WhatIf</span></span>
<span data-ttu-id="bca89-131">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="bca89-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bca89-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bca89-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bca89-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bca89-133">CommonParameters</span></span>
<span data-ttu-id="bca89-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bca89-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bca89-135">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bca89-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bca89-136">입력</span><span class="sxs-lookup"><span data-stu-id="bca89-136">INPUTS</span></span>

### <span data-ttu-id="bca89-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="bca89-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="bca89-138">System.String</span><span class="sxs-lookup"><span data-stu-id="bca89-138">System.String</span></span>

## <span data-ttu-id="bca89-139">출력</span><span class="sxs-lookup"><span data-stu-id="bca89-139">OUTPUTS</span></span>

### <span data-ttu-id="bca89-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bca89-140">System.Boolean</span></span>

## <span data-ttu-id="bca89-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bca89-141">NOTES</span></span>

## <span data-ttu-id="bca89-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bca89-142">RELATED LINKS</span></span>
