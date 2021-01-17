---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: d5986694ad0064265bbd4bad6e1efc378683ce97
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385694"
---
# <span data-ttu-id="d3995-101">Get-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="d3995-101">Get-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="d3995-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3995-102">SYNOPSIS</span></span>
<span data-ttu-id="d3995-103">개인 링크 범위 다운로드</span><span class="sxs-lookup"><span data-stu-id="d3995-103">Get private link scope</span></span>

## <span data-ttu-id="d3995-104">구문</span><span class="sxs-lookup"><span data-stu-id="d3995-104">SYNTAX</span></span>

### <span data-ttu-id="d3995-105">ByResourceGroupParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="d3995-105">ByResourceGroupParameterSet (Default)</span></span>
```
Get-AzInsightsPrivateLinkScope [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d3995-106">ByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3995-106">ByResourceNameParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3995-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3995-107">ByResourceIdParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScope -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d3995-108">설명</span><span class="sxs-lookup"><span data-stu-id="d3995-108">DESCRIPTION</span></span>
<span data-ttu-id="d3995-109">개인 링크 범위 나열 또는 다운로드</span><span class="sxs-lookup"><span data-stu-id="d3995-109">List or get private link scope</span></span> 

## <span data-ttu-id="d3995-110">예제</span><span class="sxs-lookup"><span data-stu-id="d3995-110">EXAMPLES</span></span>

### <span data-ttu-id="d3995-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="d3995-111">Example 1</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name"
```

<span data-ttu-id="d3995-112">리소스 그룹 "rg_name" 아래에 개인 링크 범위를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="d3995-112">List private link scopes under resource group "rg_name"</span></span>

### <span data-ttu-id="d3995-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="d3995-113">Example 2</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="d3995-114">리소스 그룹 "scope_name"에서 이름이 "rg_name"인 개인 링크 범위를 얻음</span><span class="sxs-lookup"><span data-stu-id="d3995-114">Get private link scope with name "scope_name" under resource group "rg_name"</span></span>

## <span data-ttu-id="d3995-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3995-115">PARAMETERS</span></span>

### <span data-ttu-id="d3995-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3995-116">-DefaultProfile</span></span>
<span data-ttu-id="d3995-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d3995-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3995-118">-Name</span><span class="sxs-lookup"><span data-stu-id="d3995-118">-Name</span></span>
<span data-ttu-id="d3995-119">개인 링크 범위 이름</span><span class="sxs-lookup"><span data-stu-id="d3995-119">Private Link Scope Name</span></span>

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

### <span data-ttu-id="d3995-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3995-120">-ResourceGroupName</span></span>
<span data-ttu-id="d3995-121">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="d3995-121">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="d3995-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d3995-122">-ResourceId</span></span>
<span data-ttu-id="d3995-123">리소스 ID</span><span class="sxs-lookup"><span data-stu-id="d3995-123">Resource Id</span></span>

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

### <span data-ttu-id="d3995-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3995-124">CommonParameters</span></span>
<span data-ttu-id="d3995-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d3995-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3995-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d3995-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3995-127">입력</span><span class="sxs-lookup"><span data-stu-id="d3995-127">INPUTS</span></span>

### <span data-ttu-id="d3995-128">System.String</span><span class="sxs-lookup"><span data-stu-id="d3995-128">System.String</span></span>

## <span data-ttu-id="d3995-129">출력</span><span class="sxs-lookup"><span data-stu-id="d3995-129">OUTPUTS</span></span>

### <span data-ttu-id="d3995-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="d3995-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="d3995-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d3995-131">NOTES</span></span>

## <span data-ttu-id="d3995-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d3995-132">RELATED LINKS</span></span>
