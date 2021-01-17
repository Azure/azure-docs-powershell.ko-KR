---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: cd71f1561525f166736b708caf4905fdefd443ce
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492268"
---
# <span data-ttu-id="d6fa8-101">Remove-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="d6fa8-101">Remove-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="d6fa8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6fa8-102">SYNOPSIS</span></span>
<span data-ttu-id="d6fa8-103">개인 링크 범위 리소스에 대한 삭제</span><span class="sxs-lookup"><span data-stu-id="d6fa8-103">delete for private link scoped resource</span></span>

## <span data-ttu-id="d6fa8-104">구문</span><span class="sxs-lookup"><span data-stu-id="d6fa8-104">SYNTAX</span></span>

### <span data-ttu-id="d6fa8-105">ByScopeParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="d6fa8-105">ByScopeParameterSet (Default)</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -ResourceGroupName <String> -ScopeName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6fa8-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6fa8-106">ByInputObjectParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -Name <String> -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6fa8-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6fa8-107">ByResourceIdParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6fa8-108">설명</span><span class="sxs-lookup"><span data-stu-id="d6fa8-108">DESCRIPTION</span></span>
<span data-ttu-id="d6fa8-109">개인 링크 범위 리소스에 대한 삭제</span><span class="sxs-lookup"><span data-stu-id="d6fa8-109">delete for private link scoped resource</span></span>

## <span data-ttu-id="d6fa8-110">예제</span><span class="sxs-lookup"><span data-stu-id="d6fa8-110">EXAMPLES</span></span>

### <span data-ttu-id="d6fa8-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="d6fa8-111">Example 1</span></span>
```powershell
Remove-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="d6fa8-112">개인 링크 범위 리소스 삭제</span><span class="sxs-lookup"><span data-stu-id="d6fa8-112">delete private link scoped resource</span></span>

## <span data-ttu-id="d6fa8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d6fa8-113">PARAMETERS</span></span>

### <span data-ttu-id="d6fa8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6fa8-114">-DefaultProfile</span></span>
<span data-ttu-id="d6fa8-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d6fa8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6fa8-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6fa8-116">-InputObject</span></span>
<span data-ttu-id="d6fa8-117">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="d6fa8-117">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="d6fa8-118">-Name</span><span class="sxs-lookup"><span data-stu-id="d6fa8-118">-Name</span></span>
<span data-ttu-id="d6fa8-119">범위가 지정된 리소스 이름</span><span class="sxs-lookup"><span data-stu-id="d6fa8-119">Scoped resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet, ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6fa8-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6fa8-120">-ResourceGroupName</span></span>
<span data-ttu-id="d6fa8-121">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="d6fa8-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6fa8-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6fa8-122">-ResourceId</span></span>
<span data-ttu-id="d6fa8-123">리소스 ID</span><span class="sxs-lookup"><span data-stu-id="d6fa8-123">Resource Id</span></span>

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

### <span data-ttu-id="d6fa8-124">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="d6fa8-124">-ScopeName</span></span>
<span data-ttu-id="d6fa8-125">개인 링크 범위 이름</span><span class="sxs-lookup"><span data-stu-id="d6fa8-125">Private Link Scope Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6fa8-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d6fa8-126">-Confirm</span></span>
<span data-ttu-id="d6fa8-127">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d6fa8-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6fa8-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6fa8-128">-WhatIf</span></span>
<span data-ttu-id="d6fa8-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d6fa8-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6fa8-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d6fa8-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6fa8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6fa8-131">CommonParameters</span></span>
<span data-ttu-id="d6fa8-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d6fa8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6fa8-133">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d6fa8-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6fa8-134">입력</span><span class="sxs-lookup"><span data-stu-id="d6fa8-134">INPUTS</span></span>

### <span data-ttu-id="d6fa8-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="d6fa8-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="d6fa8-136">System.String</span><span class="sxs-lookup"><span data-stu-id="d6fa8-136">System.String</span></span>

## <span data-ttu-id="d6fa8-137">출력</span><span class="sxs-lookup"><span data-stu-id="d6fa8-137">OUTPUTS</span></span>

### <span data-ttu-id="d6fa8-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d6fa8-138">System.Boolean</span></span>

## <span data-ttu-id="d6fa8-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d6fa8-139">NOTES</span></span>

## <span data-ttu-id="d6fa8-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d6fa8-140">RELATED LINKS</span></span>
