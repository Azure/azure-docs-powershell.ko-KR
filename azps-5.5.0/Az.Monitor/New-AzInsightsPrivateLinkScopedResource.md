---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: fd4dc0dd771029951da4ae375141cc526301de34
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192177"
---
# <span data-ttu-id="4db21-101">New-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="4db21-101">New-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="4db21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4db21-102">SYNOPSIS</span></span>
<span data-ttu-id="4db21-103">개인 링크 범위 리소스 만들기</span><span class="sxs-lookup"><span data-stu-id="4db21-103">create for private link scoped resource</span></span>

## <span data-ttu-id="4db21-104">구문</span><span class="sxs-lookup"><span data-stu-id="4db21-104">SYNTAX</span></span>

### <span data-ttu-id="4db21-105">ByResourceNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="4db21-105">ByResourceNameParameterSet (Default)</span></span>
```
New-AzInsightsPrivateLinkScopedResource -LinkedResourceId <String> -ResourceGroupName <String>
 -ScopeName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4db21-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4db21-106">ByInputObjectParameterSet</span></span>
```
New-AzInsightsPrivateLinkScopedResource -LinkedResourceId <String> -Name <String>
 -InputObject <PSMonitorPrivateLinkScope> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4db21-107">설명</span><span class="sxs-lookup"><span data-stu-id="4db21-107">DESCRIPTION</span></span>
<span data-ttu-id="4db21-108">개인 링크 범위 리소스에 대한 만들기, 범위가 지정한 리소스는 Log Analytics 작업 영역 또는 Application Insights 구성 요소일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4db21-108">create for private link scoped resource, scoped resource could be Log Analytics workspace or Application Insights component</span></span>

## <span data-ttu-id="4db21-109">예제</span><span class="sxs-lookup"><span data-stu-id="4db21-109">EXAMPLES</span></span>

### <span data-ttu-id="4db21-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="4db21-110">Example 1</span></span>
```powershell
$ai = Get-AzApplicationInsights -ResourceGroupName "rg_name" -Name "ai_name"

New-AzInsightsPrivateLinkScopedResource -LinkedResourceId $ai.Id -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="4db21-111">Application Insights 구성 요소 "scoped_resource_name"에 연결된 범위가 있는 리소스 "ai_name" 만들기</span><span class="sxs-lookup"><span data-stu-id="4db21-111">create scoped resource "scoped_resource_name" linked to application insights component "ai_name"</span></span>

## <span data-ttu-id="4db21-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4db21-112">PARAMETERS</span></span>

### <span data-ttu-id="4db21-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4db21-113">-DefaultProfile</span></span>
<span data-ttu-id="4db21-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4db21-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4db21-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4db21-115">-InputObject</span></span>
<span data-ttu-id="4db21-116">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="4db21-116">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="4db21-117">-LinkedResourceId</span><span class="sxs-lookup"><span data-stu-id="4db21-117">-LinkedResourceId</span></span>
<span data-ttu-id="4db21-118">LA/AI 리소스 ID를 연결</span><span class="sxs-lookup"><span data-stu-id="4db21-118">LA/AI Resource Id to Link</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4db21-119">-Name</span><span class="sxs-lookup"><span data-stu-id="4db21-119">-Name</span></span>
<span data-ttu-id="4db21-120">범위가 지정된 리소스 이름</span><span class="sxs-lookup"><span data-stu-id="4db21-120">Scoped resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4db21-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4db21-121">-ResourceGroupName</span></span>
<span data-ttu-id="4db21-122">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="4db21-122">Resource Group Name</span></span>

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

### <span data-ttu-id="4db21-123">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="4db21-123">-ScopeName</span></span>
<span data-ttu-id="4db21-124">개인 링크 범위 이름</span><span class="sxs-lookup"><span data-stu-id="4db21-124">Private Link Scope Name</span></span>

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

### <span data-ttu-id="4db21-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4db21-125">-Confirm</span></span>
<span data-ttu-id="4db21-126">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4db21-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4db21-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4db21-127">-WhatIf</span></span>
<span data-ttu-id="4db21-128">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="4db21-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4db21-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4db21-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4db21-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4db21-130">CommonParameters</span></span>
<span data-ttu-id="4db21-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4db21-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4db21-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4db21-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4db21-133">입력</span><span class="sxs-lookup"><span data-stu-id="4db21-133">INPUTS</span></span>

### <span data-ttu-id="4db21-134">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="4db21-134">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="4db21-135">System.String</span><span class="sxs-lookup"><span data-stu-id="4db21-135">System.String</span></span>

## <span data-ttu-id="4db21-136">출력</span><span class="sxs-lookup"><span data-stu-id="4db21-136">OUTPUTS</span></span>

### <span data-ttu-id="4db21-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="4db21-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span></span>

## <span data-ttu-id="4db21-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4db21-138">NOTES</span></span>

## <span data-ttu-id="4db21-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4db21-139">RELATED LINKS</span></span>
