---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: 358eb796a156949520cf8cf0c073ee08a6537e2f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184913"
---
# <span data-ttu-id="cab10-101">Remove-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="cab10-101">Remove-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="cab10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cab10-102">SYNOPSIS</span></span>
<span data-ttu-id="cab10-103">개인 링크 범위 삭제</span><span class="sxs-lookup"><span data-stu-id="cab10-103">delete private link scope</span></span>

## <span data-ttu-id="cab10-104">구문</span><span class="sxs-lookup"><span data-stu-id="cab10-104">SYNTAX</span></span>

### <span data-ttu-id="cab10-105">ByResourceNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="cab10-105">ByResourceNameParameterSet (Default)</span></span>
```
Remove-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cab10-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cab10-106">ByResourceIdParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScope -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cab10-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cab10-107">ByInputObjectParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScope -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cab10-108">설명</span><span class="sxs-lookup"><span data-stu-id="cab10-108">DESCRIPTION</span></span>
<span data-ttu-id="cab10-109">개인 링크 범위 삭제</span><span class="sxs-lookup"><span data-stu-id="cab10-109">delete private link scope</span></span>

## <span data-ttu-id="cab10-110">예제</span><span class="sxs-lookup"><span data-stu-id="cab10-110">EXAMPLES</span></span>

### <span data-ttu-id="cab10-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="cab10-111">Example 1</span></span>
```powershell
Remove-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="cab10-112">리소스 그룹 "scope_name"에서 이름이 "rg_name" 개인 링크 범위를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="cab10-112">delete private link scope with name "scope_name" under resource group "rg_name"</span></span>

### <span data-ttu-id="cab10-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="cab10-113">Example 2</span></span>
```powershell
Remove-AzInsightsPrivateLinkScope -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/rg_name/providers/microsoft.insights/privateLinkScopes/scope_name"
```

<span data-ttu-id="cab10-114">리소스 ID를 사용하여 개인 링크 범위 삭제</span><span class="sxs-lookup"><span data-stu-id="cab10-114">delete private link scope with resource Id</span></span>

### <span data-ttu-id="cab10-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="cab10-115">Example 3</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" | Remove-AzInsightsPrivateLinkScope
```

<span data-ttu-id="cab10-116">입력 개인 링크 범위 개체를 사용하여 개인 링크 범위 삭제</span><span class="sxs-lookup"><span data-stu-id="cab10-116">delete private link scope with input private link scope object</span></span>

## <span data-ttu-id="cab10-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cab10-117">PARAMETERS</span></span>

### <span data-ttu-id="cab10-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cab10-118">-DefaultProfile</span></span>
<span data-ttu-id="cab10-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cab10-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cab10-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cab10-120">-InputObject</span></span>
<span data-ttu-id="cab10-121">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="cab10-121">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="cab10-122">-Name</span><span class="sxs-lookup"><span data-stu-id="cab10-122">-Name</span></span>
<span data-ttu-id="cab10-123">개인 링크 범위 이름</span><span class="sxs-lookup"><span data-stu-id="cab10-123">Private Link Scope Name</span></span>

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

### <span data-ttu-id="cab10-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cab10-124">-ResourceGroupName</span></span>
<span data-ttu-id="cab10-125">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="cab10-125">Resource Group Name</span></span>

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

### <span data-ttu-id="cab10-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cab10-126">-ResourceId</span></span>
<span data-ttu-id="cab10-127">리소스 ID</span><span class="sxs-lookup"><span data-stu-id="cab10-127">Resource Id</span></span>

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

### <span data-ttu-id="cab10-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cab10-128">-Confirm</span></span>
<span data-ttu-id="cab10-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="cab10-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cab10-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cab10-130">-WhatIf</span></span>
<span data-ttu-id="cab10-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="cab10-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cab10-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cab10-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cab10-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cab10-133">CommonParameters</span></span>
<span data-ttu-id="cab10-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cab10-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cab10-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cab10-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cab10-136">입력</span><span class="sxs-lookup"><span data-stu-id="cab10-136">INPUTS</span></span>

### <span data-ttu-id="cab10-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="cab10-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="cab10-138">System.String</span><span class="sxs-lookup"><span data-stu-id="cab10-138">System.String</span></span>

## <span data-ttu-id="cab10-139">출력</span><span class="sxs-lookup"><span data-stu-id="cab10-139">OUTPUTS</span></span>

### <span data-ttu-id="cab10-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cab10-140">System.Boolean</span></span>

## <span data-ttu-id="cab10-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cab10-141">NOTES</span></span>

## <span data-ttu-id="cab10-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cab10-142">RELATED LINKS</span></span>
