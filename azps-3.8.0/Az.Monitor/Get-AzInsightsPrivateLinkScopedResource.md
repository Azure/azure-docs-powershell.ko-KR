---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: f3d00ba82bbafce42cca49c60d443cd244f83df3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041870"
---
# <span data-ttu-id="7fb3a-101">Get-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="7fb3a-101">Get-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="7fb3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7fb3a-102">SYNOPSIS</span></span>
<span data-ttu-id="7fb3a-103">개인 링크 범위 리소스 가져오기</span><span class="sxs-lookup"><span data-stu-id="7fb3a-103">Get for private link scoped resource</span></span>

## <span data-ttu-id="7fb3a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7fb3a-104">SYNTAX</span></span>

### <span data-ttu-id="7fb3a-105">ByScopeParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="7fb3a-105">ByScopeParameterSet (Default)</span></span>
```
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName <String> -ScopeName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7fb3a-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fb3a-106">ByInputObjectParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScopedResource [-Name <String>] -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7fb3a-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fb3a-107">ByResourceIdParameterSet</span></span>
```
Get-AzInsightsPrivateLinkScopedResource -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7fb3a-108">설명은</span><span class="sxs-lookup"><span data-stu-id="7fb3a-108">DESCRIPTION</span></span>
<span data-ttu-id="7fb3a-109">개인 링크 범위 리소스에 대 한 가져오기 또는 목록, 범위 리소스는 로그 분석 작업 영역 또는 Application Insights 구성 요소 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7fb3a-109">Get or list for private link scoped resource, scoped resource could be Log Analytics workspace or Application Insights component</span></span>

## <span data-ttu-id="7fb3a-110">예제의</span><span class="sxs-lookup"><span data-stu-id="7fb3a-110">EXAMPLES</span></span>

### <span data-ttu-id="7fb3a-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="7fb3a-111">Example 1</span></span>
```powershell
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name"
```

<span data-ttu-id="7fb3a-112">개인 링크 범위 "scope_name"의 범위 리소스 목록</span><span class="sxs-lookup"><span data-stu-id="7fb3a-112">List scoped resource under private link scope "scope_name"</span></span>

### <span data-ttu-id="7fb3a-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="7fb3a-113">Example 2</span></span>
```powershell
Get-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="7fb3a-114">개인 링크 범위에서 "scope_name" (이름이 "scoped_resource_name") 인 범위 리소스 가져오기</span><span class="sxs-lookup"><span data-stu-id="7fb3a-114">Get scoped resource under private link scope "scope_name" with name "scoped_resource_name"</span></span>

## <span data-ttu-id="7fb3a-115">변수</span><span class="sxs-lookup"><span data-stu-id="7fb3a-115">PARAMETERS</span></span>

### <span data-ttu-id="7fb3a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fb3a-116">-DefaultProfile</span></span>
<span data-ttu-id="7fb3a-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7fb3a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fb3a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7fb3a-118">-InputObject</span></span>
<span data-ttu-id="7fb3a-119">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="7fb3a-119">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="7fb3a-120">-이름</span><span class="sxs-lookup"><span data-stu-id="7fb3a-120">-Name</span></span>
<span data-ttu-id="7fb3a-121">범위 리소스 이름</span><span class="sxs-lookup"><span data-stu-id="7fb3a-121">Scoped resource Name</span></span>

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

### <span data-ttu-id="7fb3a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fb3a-122">-ResourceGroupName</span></span>
<span data-ttu-id="7fb3a-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="7fb3a-123">Resource Group Name</span></span>

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

### <span data-ttu-id="7fb3a-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7fb3a-124">-ResourceId</span></span>
<span data-ttu-id="7fb3a-125">리소스 Id</span><span class="sxs-lookup"><span data-stu-id="7fb3a-125">Resource Id</span></span>

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

### <span data-ttu-id="7fb3a-126">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="7fb3a-126">-ScopeName</span></span>
<span data-ttu-id="7fb3a-127">개인 링크 범위 이름</span><span class="sxs-lookup"><span data-stu-id="7fb3a-127">Private Link Scope Name</span></span>

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

### <span data-ttu-id="7fb3a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fb3a-128">CommonParameters</span></span>
<span data-ttu-id="7fb3a-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7fb3a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fb3a-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7fb3a-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fb3a-131">입력</span><span class="sxs-lookup"><span data-stu-id="7fb3a-131">INPUTS</span></span>

### <span data-ttu-id="7fb3a-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7fb3a-132">System.String</span></span>

## <span data-ttu-id="7fb3a-133">출력</span><span class="sxs-lookup"><span data-stu-id="7fb3a-133">OUTPUTS</span></span>

### <span data-ttu-id="7fb3a-134">icrosoft. PSMonitorPrivateLinkScopedResource에 대 한 정보</span><span class="sxs-lookup"><span data-stu-id="7fb3a-134">icrosoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span></span>

## <span data-ttu-id="7fb3a-135">상속자</span><span class="sxs-lookup"><span data-stu-id="7fb3a-135">NOTES</span></span>

## <span data-ttu-id="7fb3a-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7fb3a-136">RELATED LINKS</span></span>
