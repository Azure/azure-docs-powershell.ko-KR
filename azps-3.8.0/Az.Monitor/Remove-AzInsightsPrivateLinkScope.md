---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: 358eb796a156949520cf8cf0c073ee08a6537e2f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93877353"
---
# <span data-ttu-id="576ae-101">Remove-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="576ae-101">Remove-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="576ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="576ae-102">SYNOPSIS</span></span>
<span data-ttu-id="576ae-103">개인 링크 범위 삭제</span><span class="sxs-lookup"><span data-stu-id="576ae-103">delete private link scope</span></span>

## <span data-ttu-id="576ae-104">구문과</span><span class="sxs-lookup"><span data-stu-id="576ae-104">SYNTAX</span></span>

### <span data-ttu-id="576ae-105">ByResourceNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="576ae-105">ByResourceNameParameterSet (Default)</span></span>
```
Remove-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="576ae-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="576ae-106">ByResourceIdParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScope -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="576ae-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="576ae-107">ByInputObjectParameterSet</span></span>
```
Remove-AzInsightsPrivateLinkScope -InputObject <PSMonitorPrivateLinkScope>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="576ae-108">설명은</span><span class="sxs-lookup"><span data-stu-id="576ae-108">DESCRIPTION</span></span>
<span data-ttu-id="576ae-109">개인 링크 범위 삭제</span><span class="sxs-lookup"><span data-stu-id="576ae-109">delete private link scope</span></span>

## <span data-ttu-id="576ae-110">예제의</span><span class="sxs-lookup"><span data-stu-id="576ae-110">EXAMPLES</span></span>

### <span data-ttu-id="576ae-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="576ae-111">Example 1</span></span>
```powershell
Remove-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="576ae-112">리소스 그룹 "rg_name"에서 이름이 "scope_name" 인 비공개 링크 범위 삭제</span><span class="sxs-lookup"><span data-stu-id="576ae-112">delete private link scope with name "scope_name" under resource group "rg_name"</span></span>

### <span data-ttu-id="576ae-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="576ae-113">Example 2</span></span>
```powershell
Remove-AzInsightsPrivateLinkScope -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/rg_name/providers/microsoft.insights/privateLinkScopes/scope_name"
```

<span data-ttu-id="576ae-114">리소스 Id를 사용 하 여 개인 링크 범위 삭제</span><span class="sxs-lookup"><span data-stu-id="576ae-114">delete private link scope with resource Id</span></span>

### <span data-ttu-id="576ae-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="576ae-115">Example 3</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" | Remove-AzInsightsPrivateLinkScope
```

<span data-ttu-id="576ae-116">입력 개인 링크 범위 개체를 사용 하 여 개인 링크 범위 삭제</span><span class="sxs-lookup"><span data-stu-id="576ae-116">delete private link scope with input private link scope object</span></span>

## <span data-ttu-id="576ae-117">변수</span><span class="sxs-lookup"><span data-stu-id="576ae-117">PARAMETERS</span></span>

### <span data-ttu-id="576ae-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="576ae-118">-DefaultProfile</span></span>
<span data-ttu-id="576ae-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="576ae-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="576ae-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="576ae-120">-InputObject</span></span>
<span data-ttu-id="576ae-121">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="576ae-121">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="576ae-122">-이름</span><span class="sxs-lookup"><span data-stu-id="576ae-122">-Name</span></span>
<span data-ttu-id="576ae-123">개인 링크 범위 이름</span><span class="sxs-lookup"><span data-stu-id="576ae-123">Private Link Scope Name</span></span>

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

### <span data-ttu-id="576ae-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="576ae-124">-ResourceGroupName</span></span>
<span data-ttu-id="576ae-125">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="576ae-125">Resource Group Name</span></span>

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

### <span data-ttu-id="576ae-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="576ae-126">-ResourceId</span></span>
<span data-ttu-id="576ae-127">리소스 Id</span><span class="sxs-lookup"><span data-stu-id="576ae-127">Resource Id</span></span>

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

### <span data-ttu-id="576ae-128">-확인</span><span class="sxs-lookup"><span data-stu-id="576ae-128">-Confirm</span></span>
<span data-ttu-id="576ae-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="576ae-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="576ae-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="576ae-130">-WhatIf</span></span>
<span data-ttu-id="576ae-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="576ae-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="576ae-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="576ae-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="576ae-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="576ae-133">CommonParameters</span></span>
<span data-ttu-id="576ae-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="576ae-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="576ae-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="576ae-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="576ae-136">입력</span><span class="sxs-lookup"><span data-stu-id="576ae-136">INPUTS</span></span>

### <span data-ttu-id="576ae-137">PSMonitorPrivateLinkScope를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="576ae-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="576ae-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="576ae-138">System.String</span></span>

## <span data-ttu-id="576ae-139">출력</span><span class="sxs-lookup"><span data-stu-id="576ae-139">OUTPUTS</span></span>

### <span data-ttu-id="576ae-140">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="576ae-140">System.Boolean</span></span>

## <span data-ttu-id="576ae-141">상속자</span><span class="sxs-lookup"><span data-stu-id="576ae-141">NOTES</span></span>

## <span data-ttu-id="576ae-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="576ae-142">RELATED LINKS</span></span>
