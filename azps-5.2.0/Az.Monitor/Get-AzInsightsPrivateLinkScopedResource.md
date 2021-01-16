---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: f3d00ba82bbafce42cca49c60d443cd244f83df3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367620"
---
# <span data-ttu-id="e9c4e-101">Get-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="e9c4e-101">Get-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="e9c4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9c4e-102">SYNOPSIS</span></span>
<span data-ttu-id="e9c4e-103">개인 링크 범위 리소스에 대한 다운로드</span><span class="sxs-lookup"><span data-stu-id="e9c4e-103">Get for private link scoped resource</span></span>

## <span data-ttu-id="e9c4e-104">구문</span><span class="sxs-lookup"><span data-stu-id="e9c4e-104">SYNTAX</span></span>

### <span data-ttu-id="e9c4e-105">ByScopeParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="e9c4e-105">ByScopeParameterSet (Default)</span></span>
```
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName <String> -ScopeName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9c4e-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9c4e-106">ByInputObjectParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScopedResource [-Name <String>] -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e9c4e-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e9c4e-107">ByResourceIdParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScopedResource -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e9c4e-108">설명</span><span class="sxs-lookup"><span data-stu-id="e9c4e-108">DESCRIPTION</span></span>
<span data-ttu-id="e9c4e-109">개인 링크 범위 리소스에 대한 Get 또는 list, 범위가 지정된 리소스는 Log Analytics 작업 영역 또는 Application Insights 구성 요소일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e9c4e-109">Get or list for private link scoped resource, scoped resource could be Log Analytics workspace or Application Insights component</span></span>

## <span data-ttu-id="e9c4e-110">예제</span><span class="sxs-lookup"><span data-stu-id="e9c4e-110">EXAMPLES</span></span>

### <span data-ttu-id="e9c4e-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="e9c4e-111">Example 1</span></span>
```powershell
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name"
```

<span data-ttu-id="e9c4e-112">개인 링크 범위 "scope_name" 아래에 범위가 있는 리소스를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="e9c4e-112">List scoped resource under private link scope "scope_name"</span></span>

### <span data-ttu-id="e9c4e-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="e9c4e-113">Example 2</span></span>
```powershell
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="e9c4e-114">"scope_name" 이름의 개인 링크 범위 "scope_name"에서 범위가 scoped_resource_name.</span><span class="sxs-lookup"><span data-stu-id="e9c4e-114">Get scoped resource under private link scope "scope_name" with name "scoped_resource_name"</span></span>

## <span data-ttu-id="e9c4e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e9c4e-115">PARAMETERS</span></span>

### <span data-ttu-id="e9c4e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9c4e-116">-DefaultProfile</span></span>
<span data-ttu-id="e9c4e-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e9c4e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9c4e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e9c4e-118">-InputObject</span></span>
<span data-ttu-id="e9c4e-119">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="e9c4e-119">PSMonitorPrivateLinkScope</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope
Parameter Sets: ByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9c4e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="e9c4e-120">-Name</span></span>
<span data-ttu-id="e9c4e-121">범위가 지정된 리소스 이름</span><span class="sxs-lookup"><span data-stu-id="e9c4e-121">Scoped resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByScopeParameterSet, ByInputObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9c4e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9c4e-122">-ResourceGroupName</span></span>
<span data-ttu-id="e9c4e-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="e9c4e-123">Resource Group Name</span></span>

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

### <span data-ttu-id="e9c4e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e9c4e-124">-ResourceId</span></span>
<span data-ttu-id="e9c4e-125">리소스 ID</span><span class="sxs-lookup"><span data-stu-id="e9c4e-125">Resource Id</span></span>

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

### <span data-ttu-id="e9c4e-126">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="e9c4e-126">-ScopeName</span></span>
<span data-ttu-id="e9c4e-127">개인 링크 범위 이름</span><span class="sxs-lookup"><span data-stu-id="e9c4e-127">Private Link Scope Name</span></span>

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

### <span data-ttu-id="e9c4e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9c4e-128">CommonParameters</span></span>
<span data-ttu-id="e9c4e-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e9c4e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9c4e-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e9c4e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9c4e-131">입력</span><span class="sxs-lookup"><span data-stu-id="e9c4e-131">INPUTS</span></span>

### <span data-ttu-id="e9c4e-132">System.String</span><span class="sxs-lookup"><span data-stu-id="e9c4e-132">System.String</span></span>

## <span data-ttu-id="e9c4e-133">출력</span><span class="sxs-lookup"><span data-stu-id="e9c4e-133">OUTPUTS</span></span>

### <span data-ttu-id="e9c4e-134">icrosoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="e9c4e-134">icrosoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span></span>

## <span data-ttu-id="e9c4e-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e9c4e-135">NOTES</span></span>

## <span data-ttu-id="e9c4e-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e9c4e-136">RELATED LINKS</span></span>
