---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: fd4dc0dd771029951da4ae375141cc526301de34
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94033874"
---
# <span data-ttu-id="b3a63-101">New-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="b3a63-101">New-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="b3a63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3a63-102">SYNOPSIS</span></span>
<span data-ttu-id="b3a63-103">개인 링크 범위 리소스에 대해 만들기</span><span class="sxs-lookup"><span data-stu-id="b3a63-103">create for private link scoped resource</span></span>

## <span data-ttu-id="b3a63-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b3a63-104">SYNTAX</span></span>

### <span data-ttu-id="b3a63-105">ByResourceNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="b3a63-105">ByResourceNameParameterSet (Default)</span></span>
```
New-AzInsightsPrivateLinkScopedResource -LinkedResourceId <String> -ResourceGroupName <String>
 -ScopeName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b3a63-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b3a63-106">ByInputObjectParameterSet</span></span>
```
New-AzInsightsPrivateLinkScopedResource -LinkedResourceId <String> -Name <String>
 -InputObject <PSMonitorPrivateLinkScope> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b3a63-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b3a63-107">DESCRIPTION</span></span>
<span data-ttu-id="b3a63-108">개인 링크 범위 리소스에 대해 만들기, 범위 리소스는 로그 분석 작업 영역 또는 Application Insights 구성 요소 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b3a63-108">create for private link scoped resource, scoped resource could be Log Analytics workspace or Application Insights component</span></span>

## <span data-ttu-id="b3a63-109">예제의</span><span class="sxs-lookup"><span data-stu-id="b3a63-109">EXAMPLES</span></span>

### <span data-ttu-id="b3a63-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="b3a63-110">Example 1</span></span>
```powershell
$ai = Get-AzApplicationInsights -ResourceGroupName "rg_name" -Name "ai_name"

New-AzInsightsPrivateLinkScopedResource -LinkedResourceId $ai.Id -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="b3a63-111">"scoped_resource_name" 응용 프로그램 insights 구성 요소에 연결 된 범위 리소스 "ai_name" 만들기</span><span class="sxs-lookup"><span data-stu-id="b3a63-111">create scoped resource "scoped_resource_name" linked to application insights component "ai_name"</span></span>

## <span data-ttu-id="b3a63-112">변수</span><span class="sxs-lookup"><span data-stu-id="b3a63-112">PARAMETERS</span></span>

### <span data-ttu-id="b3a63-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3a63-113">-DefaultProfile</span></span>
<span data-ttu-id="b3a63-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b3a63-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3a63-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3a63-115">-InputObject</span></span>
<span data-ttu-id="b3a63-116">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="b3a63-116">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="b3a63-117">-LinkedResourceId</span><span class="sxs-lookup"><span data-stu-id="b3a63-117">-LinkedResourceId</span></span>
<span data-ttu-id="b3a63-118">연결에 대 한 LA/AI 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="b3a63-118">LA/AI Resource Id to Link</span></span>

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

### <span data-ttu-id="b3a63-119">-이름</span><span class="sxs-lookup"><span data-stu-id="b3a63-119">-Name</span></span>
<span data-ttu-id="b3a63-120">범위 리소스 이름</span><span class="sxs-lookup"><span data-stu-id="b3a63-120">Scoped resource Name</span></span>

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

### <span data-ttu-id="b3a63-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3a63-121">-ResourceGroupName</span></span>
<span data-ttu-id="b3a63-122">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="b3a63-122">Resource Group Name</span></span>

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

### <span data-ttu-id="b3a63-123">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="b3a63-123">-ScopeName</span></span>
<span data-ttu-id="b3a63-124">개인 링크 범위 이름</span><span class="sxs-lookup"><span data-stu-id="b3a63-124">Private Link Scope Name</span></span>

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

### <span data-ttu-id="b3a63-125">-확인</span><span class="sxs-lookup"><span data-stu-id="b3a63-125">-Confirm</span></span>
<span data-ttu-id="b3a63-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3a63-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3a63-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3a63-127">-WhatIf</span></span>
<span data-ttu-id="b3a63-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b3a63-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3a63-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b3a63-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3a63-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3a63-130">CommonParameters</span></span>
<span data-ttu-id="b3a63-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3a63-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3a63-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b3a63-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3a63-133">입력</span><span class="sxs-lookup"><span data-stu-id="b3a63-133">INPUTS</span></span>

### <span data-ttu-id="b3a63-134">PSMonitorPrivateLinkScope를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3a63-134">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="b3a63-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b3a63-135">System.String</span></span>

## <span data-ttu-id="b3a63-136">출력</span><span class="sxs-lookup"><span data-stu-id="b3a63-136">OUTPUTS</span></span>

### <span data-ttu-id="b3a63-137">PSMonitorPrivateLinkScopedResource를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3a63-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScopedResource</span></span>

## <span data-ttu-id="b3a63-138">상속자</span><span class="sxs-lookup"><span data-stu-id="b3a63-138">NOTES</span></span>

## <span data-ttu-id="b3a63-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b3a63-139">RELATED LINKS</span></span>
