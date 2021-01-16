---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/update-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: 93e97906fc7e985d522f5af9d678392741a9022b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334101"
---
# <span data-ttu-id="9bcea-101">Update-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="9bcea-101">Update-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="9bcea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9bcea-102">SYNOPSIS</span></span>
<span data-ttu-id="9bcea-103">개인 링크 범위에 대한 업데이트</span><span class="sxs-lookup"><span data-stu-id="9bcea-103">Update for private link scope</span></span>

## <span data-ttu-id="9bcea-104">구문</span><span class="sxs-lookup"><span data-stu-id="9bcea-104">SYNTAX</span></span>

### <span data-ttu-id="9bcea-105">ByResourceNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="9bcea-105">ByResourceNameParameterSet (Default)</span></span>
```
Update-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bcea-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9bcea-106">ByResourceIdParameterSet</span></span>
```
Update-AzInsightsPrivateLinkScope -ResourceId <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bcea-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9bcea-107">ByInputObjectParameterSet</span></span>
```
Update-AzInsightsPrivateLinkScope -InputObject <PSMonitorPrivateLinkScope> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9bcea-108">설명</span><span class="sxs-lookup"><span data-stu-id="9bcea-108">DESCRIPTION</span></span>
<span data-ttu-id="9bcea-109">개인 링크 범위에 대한 업데이트</span><span class="sxs-lookup"><span data-stu-id="9bcea-109">Update for private link scope</span></span>

## <span data-ttu-id="9bcea-110">예제</span><span class="sxs-lookup"><span data-stu-id="9bcea-110">EXAMPLES</span></span>

### <span data-ttu-id="9bcea-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="9bcea-111">Example 1</span></span>
```powershell
Update-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" -Tags "key:value"
```

<span data-ttu-id="9bcea-112">리소스 그룹 "scope_name"에서 "rg_name"라는 이름으로 개인 링크 범위를 업데이트하여 "key:value" 태그를 사용</span><span class="sxs-lookup"><span data-stu-id="9bcea-112">update private link scope with name "scope_name" under resource group "rg_name" to use tag "key:value"</span></span>

### <span data-ttu-id="9bcea-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="9bcea-113">Example 2</span></span>
```powershell
Update-AzInsightsPrivateLinkScope -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/rg_name/providers/microsoft.insights/privateLinkScopes/scope_name" -Tags "key:value"
```

<span data-ttu-id="9bcea-114">"key:value" 태그를 사용하기 위해 리소스 ID로 개인 링크 범위를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="9bcea-114">update private link scope with resource Id to use tag "key:value"</span></span>

### <span data-ttu-id="9bcea-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="9bcea-115">Example 3</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" | Update-AzInsightsPrivateLinkScope -Tags "key:value"
```

<span data-ttu-id="9bcea-116">"key:value" 태그를 사용하기 위해 입력 개인 링크 범위 개체를 사용하여 개인 링크 범위를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="9bcea-116">update private link scope with input private link scope object to use tag "key:value"</span></span>

## <span data-ttu-id="9bcea-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9bcea-117">PARAMETERS</span></span>

### <span data-ttu-id="9bcea-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bcea-118">-DefaultProfile</span></span>
<span data-ttu-id="9bcea-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9bcea-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9bcea-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9bcea-120">-InputObject</span></span>
<span data-ttu-id="9bcea-121">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="9bcea-121">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="9bcea-122">-Name</span><span class="sxs-lookup"><span data-stu-id="9bcea-122">-Name</span></span>
<span data-ttu-id="9bcea-123">개인 링크 범위 이름</span><span class="sxs-lookup"><span data-stu-id="9bcea-123">Private Link Scope Name</span></span>

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

### <span data-ttu-id="9bcea-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bcea-124">-ResourceGroupName</span></span>
<span data-ttu-id="9bcea-125">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="9bcea-125">Resource Group Name</span></span>

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

### <span data-ttu-id="9bcea-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9bcea-126">-ResourceId</span></span>
<span data-ttu-id="9bcea-127">리소스 ID</span><span class="sxs-lookup"><span data-stu-id="9bcea-127">Resource Id</span></span>

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

### <span data-ttu-id="9bcea-128">-Tags</span><span class="sxs-lookup"><span data-stu-id="9bcea-128">-Tags</span></span>
<span data-ttu-id="9bcea-129">태그</span><span class="sxs-lookup"><span data-stu-id="9bcea-129">Tags</span></span>

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

### <span data-ttu-id="9bcea-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9bcea-130">-Confirm</span></span>
<span data-ttu-id="9bcea-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9bcea-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bcea-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bcea-132">-WhatIf</span></span>
<span data-ttu-id="9bcea-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="9bcea-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9bcea-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9bcea-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bcea-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bcea-135">CommonParameters</span></span>
<span data-ttu-id="9bcea-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9bcea-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bcea-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9bcea-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bcea-138">입력</span><span class="sxs-lookup"><span data-stu-id="9bcea-138">INPUTS</span></span>

### <span data-ttu-id="9bcea-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="9bcea-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="9bcea-140">System.String</span><span class="sxs-lookup"><span data-stu-id="9bcea-140">System.String</span></span>

## <span data-ttu-id="9bcea-141">출력</span><span class="sxs-lookup"><span data-stu-id="9bcea-141">OUTPUTS</span></span>

### <span data-ttu-id="9bcea-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="9bcea-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="9bcea-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9bcea-143">NOTES</span></span>

## <span data-ttu-id="9bcea-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9bcea-144">RELATED LINKS</span></span>