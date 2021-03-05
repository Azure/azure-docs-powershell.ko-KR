---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/update-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: ef53c93669faea2e9f952c0887e6cb0b105cf19b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965760"
---
# <span data-ttu-id="93bfb-101">Update-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="93bfb-101">Update-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="93bfb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93bfb-102">SYNOPSIS</span></span>
<span data-ttu-id="93bfb-103">비공개 링크 범위에 대한 업데이트</span><span class="sxs-lookup"><span data-stu-id="93bfb-103">Update for private link scope</span></span>

## <span data-ttu-id="93bfb-104">구문</span><span class="sxs-lookup"><span data-stu-id="93bfb-104">SYNTAX</span></span>

### <span data-ttu-id="93bfb-105">ByResourceNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="93bfb-105">ByResourceNameParameterSet (Default)</span></span>
```
Update-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93bfb-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="93bfb-106">ByResourceIdParameterSet</span></span>
```
Update-AzInsightsPrivateLinkScope -ResourceId <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93bfb-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="93bfb-107">ByInputObjectParameterSet</span></span>
```
Update-AzInsightsPrivateLinkScope -InputObject <PSMonitorPrivateLinkScope> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93bfb-108">설명</span><span class="sxs-lookup"><span data-stu-id="93bfb-108">DESCRIPTION</span></span>
<span data-ttu-id="93bfb-109">비공개 링크 범위에 대한 업데이트</span><span class="sxs-lookup"><span data-stu-id="93bfb-109">Update for private link scope</span></span>

## <span data-ttu-id="93bfb-110">예제</span><span class="sxs-lookup"><span data-stu-id="93bfb-110">EXAMPLES</span></span>

### <span data-ttu-id="93bfb-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="93bfb-111">Example 1</span></span>
```powershell
Update-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" -Tags "key:value"
```

<span data-ttu-id="93bfb-112">태그 "key:value"를 scope_name "rg_name" 이름으로 개인 링크 범위를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="93bfb-112">update private link scope with name "scope_name" under resource group "rg_name" to use tag "key:value"</span></span>

### <span data-ttu-id="93bfb-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="93bfb-113">Example 2</span></span>
```powershell
Update-AzInsightsPrivateLinkScope -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/rg_name/providers/microsoft.insights/privateLinkScopes/scope_name" -Tags "key:value"
```

<span data-ttu-id="93bfb-114">태그 "key:value"를 사용하여 리소스 ID로 개인 링크 범위를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="93bfb-114">update private link scope with resource Id to use tag "key:value"</span></span>

### <span data-ttu-id="93bfb-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="93bfb-115">Example 3</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" | Update-AzInsightsPrivateLinkScope -Tags "key:value"
```

<span data-ttu-id="93bfb-116">태그 "key:value"를 사용할 수 있는 입력 개인 링크 범위 개체로 개인 링크 범위를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="93bfb-116">update private link scope with input private link scope object to use tag "key:value"</span></span>

## <span data-ttu-id="93bfb-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="93bfb-117">PARAMETERS</span></span>

### <span data-ttu-id="93bfb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93bfb-118">-DefaultProfile</span></span>
<span data-ttu-id="93bfb-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="93bfb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93bfb-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="93bfb-120">-InputObject</span></span>
<span data-ttu-id="93bfb-121">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="93bfb-121">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="93bfb-122">-Name</span><span class="sxs-lookup"><span data-stu-id="93bfb-122">-Name</span></span>
<span data-ttu-id="93bfb-123">개인 링크 범위 이름</span><span class="sxs-lookup"><span data-stu-id="93bfb-123">Private Link Scope Name</span></span>

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

### <span data-ttu-id="93bfb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93bfb-124">-ResourceGroupName</span></span>
<span data-ttu-id="93bfb-125">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="93bfb-125">Resource Group Name</span></span>

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

### <span data-ttu-id="93bfb-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="93bfb-126">-ResourceId</span></span>
<span data-ttu-id="93bfb-127">리소스 ID</span><span class="sxs-lookup"><span data-stu-id="93bfb-127">Resource Id</span></span>

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

### <span data-ttu-id="93bfb-128">-Tags</span><span class="sxs-lookup"><span data-stu-id="93bfb-128">-Tags</span></span>
<span data-ttu-id="93bfb-129">태그</span><span class="sxs-lookup"><span data-stu-id="93bfb-129">Tags</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93bfb-130">-확인</span><span class="sxs-lookup"><span data-stu-id="93bfb-130">-Confirm</span></span>
<span data-ttu-id="93bfb-131">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="93bfb-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93bfb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93bfb-132">-WhatIf</span></span>
<span data-ttu-id="93bfb-133">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="93bfb-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93bfb-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="93bfb-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93bfb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93bfb-135">CommonParameters</span></span>
<span data-ttu-id="93bfb-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="93bfb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93bfb-137">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="93bfb-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93bfb-138">입력</span><span class="sxs-lookup"><span data-stu-id="93bfb-138">INPUTS</span></span>

### <span data-ttu-id="93bfb-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="93bfb-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="93bfb-140">System.String</span><span class="sxs-lookup"><span data-stu-id="93bfb-140">System.String</span></span>

## <span data-ttu-id="93bfb-141">출력</span><span class="sxs-lookup"><span data-stu-id="93bfb-141">OUTPUTS</span></span>

### <span data-ttu-id="93bfb-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="93bfb-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="93bfb-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="93bfb-143">NOTES</span></span>

## <span data-ttu-id="93bfb-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="93bfb-144">RELATED LINKS</span></span>
