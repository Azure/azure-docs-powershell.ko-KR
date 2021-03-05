---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: ff4e75e2301ef9ae2ccd6f2e5064e06aedc2dbd4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980043"
---
# <span data-ttu-id="b7475-101">Get-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="b7475-101">Get-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="b7475-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7475-102">SYNOPSIS</span></span>
<span data-ttu-id="b7475-103">개인 링크 범위가 지정된 리소스에 대한 다운로드</span><span class="sxs-lookup"><span data-stu-id="b7475-103">Get for private link scoped resource</span></span>

## <span data-ttu-id="b7475-104">구문</span><span class="sxs-lookup"><span data-stu-id="b7475-104">SYNTAX</span></span>

### <span data-ttu-id="b7475-105">ByScopeParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="b7475-105">ByScopeParameterSet (Default)</span></span>
```
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName <String> -ScopeName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7475-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7475-106">ByInputObjectParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScopedResource [-Name <String>] -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7475-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7475-107">ByResourceIdParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScopedResource -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b7475-108">설명</span><span class="sxs-lookup"><span data-stu-id="b7475-108">DESCRIPTION</span></span>
<span data-ttu-id="b7475-109">개인 링크 범위 리소스에 대한 Get 또는 list, 범위가 지정된 리소스는 Log Analytics 작업 영역 또는 Application Insights 구성 요소일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7475-109">Get or list for private link scoped resource, scoped resource could be Log Analytics workspace or Application Insights component</span></span>

## <span data-ttu-id="b7475-110">예제</span><span class="sxs-lookup"><span data-stu-id="b7475-110">EXAMPLES</span></span>

### <span data-ttu-id="b7475-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="b7475-111">Example 1</span></span>
```powershell
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name"
```

<span data-ttu-id="b7475-112">개인 링크 범위 "scope_name" 아래에 범위가 지정된 리소스 나열</span><span class="sxs-lookup"><span data-stu-id="b7475-112">List scoped resource under private link scope "scope_name"</span></span>

### <span data-ttu-id="b7475-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="b7475-113">Example 2</span></span>
```powershell
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="b7475-114">이름 "scope_name"를 사용하여 개인 링크 범위 "scope_name" 범위의 리소스 scoped_resource_name</span><span class="sxs-lookup"><span data-stu-id="b7475-114">Get scoped resource under private link scope "scope_name" with name "scoped_resource_name"</span></span>

## <span data-ttu-id="b7475-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b7475-115">PARAMETERS</span></span>

### <span data-ttu-id="b7475-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7475-116">-DefaultProfile</span></span>
<span data-ttu-id="b7475-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b7475-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7475-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7475-118">-InputObject</span></span>
<span data-ttu-id="b7475-119">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="b7475-119">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="b7475-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b7475-120">-Name</span></span>
<span data-ttu-id="b7475-121">범위가 지정된 리소스 이름</span><span class="sxs-lookup"><span data-stu-id="b7475-121">Scoped resource Name</span></span>

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

### <span data-ttu-id="b7475-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7475-122">-ResourceGroupName</span></span>
<span data-ttu-id="b7475-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="b7475-123">Resource Group Name</span></span>

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

### <span data-ttu-id="b7475-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b7475-124">-ResourceId</span></span>
<span data-ttu-id="b7475-125">리소스 ID</span><span class="sxs-lookup"><span data-stu-id="b7475-125">Resource Id</span></span>

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

### <span data-ttu-id="b7475-126">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="b7475-126">-ScopeName</span></span>
<span data-ttu-id="b7475-127">개인 링크 범위 이름</span><span class="sxs-lookup"><span data-stu-id="b7475-127">Private Link Scope Name</span></span>

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

### <span data-ttu-id="b7475-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7475-128">CommonParameters</span></span>
<span data-ttu-id="b7475-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b7475-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7475-130">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b7475-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7475-131">입력</span><span class="sxs-lookup"><span data-stu-id="b7475-131">INPUTS</span></span>

### <span data-ttu-id="b7475-132">System.String</span><span class="sxs-lookup"><span data-stu-id="b7475-132">System.String</span></span>

## <span data-ttu-id="b7475-133">출력</span><span class="sxs-lookup"><span data-stu-id="b7475-133">OUTPUTS</span></span>

### <span data-ttu-id="b7475-134">icrosoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="b7475-134">icrosoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span></span>

## <span data-ttu-id="b7475-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b7475-135">NOTES</span></span>

## <span data-ttu-id="b7475-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b7475-136">RELATED LINKS</span></span>
