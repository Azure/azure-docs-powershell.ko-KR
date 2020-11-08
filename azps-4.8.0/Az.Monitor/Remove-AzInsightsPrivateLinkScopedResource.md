---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azinsightsprivatelinkscopedresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScopedResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScopedResource.md
ms.openlocfilehash: cd71f1561525f166736b708caf4905fdefd443ce
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94211617"
---
# <span data-ttu-id="2e5e1-101">Remove-AzInsightsPrivateLinkScopedResource</span><span class="sxs-lookup"><span data-stu-id="2e5e1-101">Remove-AzInsightsPrivateLinkScopedResource</span></span>

## <span data-ttu-id="2e5e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e5e1-102">SYNOPSIS</span></span>
<span data-ttu-id="2e5e1-103">비공개 링크 범위 리소스에 대 한 삭제</span><span class="sxs-lookup"><span data-stu-id="2e5e1-103">delete for private link scoped resource</span></span>

## <span data-ttu-id="2e5e1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2e5e1-104">SYNTAX</span></span>

### <span data-ttu-id="2e5e1-105">ByScopeParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="2e5e1-105">ByScopeParameterSet (Default)</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -ResourceGroupName <String> -ScopeName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e5e1-106">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e5e1-106">ByInputObjectParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -Name <String> -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e5e1-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e5e1-107">ByResourceIdParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScopedResource -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2e5e1-108">설명은</span><span class="sxs-lookup"><span data-stu-id="2e5e1-108">DESCRIPTION</span></span>
<span data-ttu-id="2e5e1-109">비공개 링크 범위 리소스에 대 한 삭제</span><span class="sxs-lookup"><span data-stu-id="2e5e1-109">delete for private link scoped resource</span></span>

## <span data-ttu-id="2e5e1-110">예제의</span><span class="sxs-lookup"><span data-stu-id="2e5e1-110">EXAMPLES</span></span>

### <span data-ttu-id="2e5e1-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="2e5e1-111">Example 1</span></span>
```powershell
Remove-AzInsightsPrivateLinkScopedResource -ResourceGroupName "rg_name" -ScopeName "scope_name" -Name "scoped_resource_name"
```

<span data-ttu-id="2e5e1-112">개인 링크 범위 리소스 삭제</span><span class="sxs-lookup"><span data-stu-id="2e5e1-112">delete private link scoped resource</span></span>

## <span data-ttu-id="2e5e1-113">변수</span><span class="sxs-lookup"><span data-stu-id="2e5e1-113">PARAMETERS</span></span>

### <span data-ttu-id="2e5e1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e5e1-114">-DefaultProfile</span></span>
<span data-ttu-id="2e5e1-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2e5e1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e5e1-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e5e1-116">-InputObject</span></span>
<span data-ttu-id="2e5e1-117">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="2e5e1-117">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="2e5e1-118">-이름</span><span class="sxs-lookup"><span data-stu-id="2e5e1-118">-Name</span></span>
<span data-ttu-id="2e5e1-119">범위 리소스 이름</span><span class="sxs-lookup"><span data-stu-id="2e5e1-119">Scoped resource Name</span></span>

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

### <span data-ttu-id="2e5e1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e5e1-120">-ResourceGroupName</span></span>
<span data-ttu-id="2e5e1-121">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="2e5e1-121">Resource Group Name</span></span>

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

### <span data-ttu-id="2e5e1-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e5e1-122">-ResourceId</span></span>
<span data-ttu-id="2e5e1-123">리소스 Id</span><span class="sxs-lookup"><span data-stu-id="2e5e1-123">Resource Id</span></span>

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

### <span data-ttu-id="2e5e1-124">-ScopeName</span><span class="sxs-lookup"><span data-stu-id="2e5e1-124">-ScopeName</span></span>
<span data-ttu-id="2e5e1-125">개인 링크 범위 이름</span><span class="sxs-lookup"><span data-stu-id="2e5e1-125">Private Link Scope Name</span></span>

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

### <span data-ttu-id="2e5e1-126">-확인</span><span class="sxs-lookup"><span data-stu-id="2e5e1-126">-Confirm</span></span>
<span data-ttu-id="2e5e1-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e5e1-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e5e1-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e5e1-128">-WhatIf</span></span>
<span data-ttu-id="2e5e1-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2e5e1-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e5e1-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2e5e1-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e5e1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e5e1-131">CommonParameters</span></span>
<span data-ttu-id="2e5e1-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e5e1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e5e1-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2e5e1-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e5e1-134">입력</span><span class="sxs-lookup"><span data-stu-id="2e5e1-134">INPUTS</span></span>

### <span data-ttu-id="2e5e1-135">PSMonitorPrivateLinkScope를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e5e1-135">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="2e5e1-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2e5e1-136">System.String</span></span>

## <span data-ttu-id="2e5e1-137">출력</span><span class="sxs-lookup"><span data-stu-id="2e5e1-137">OUTPUTS</span></span>

### <span data-ttu-id="2e5e1-138">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="2e5e1-138">System.Boolean</span></span>

## <span data-ttu-id="2e5e1-139">상속자</span><span class="sxs-lookup"><span data-stu-id="2e5e1-139">NOTES</span></span>

## <span data-ttu-id="2e5e1-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2e5e1-140">RELATED LINKS</span></span>
