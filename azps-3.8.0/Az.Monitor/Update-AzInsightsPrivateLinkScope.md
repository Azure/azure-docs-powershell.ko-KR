---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/update-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: 93e97906fc7e985d522f5af9d678392741a9022b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93877313"
---
# <span data-ttu-id="87ef9-101">Update-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="87ef9-101">Update-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="87ef9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87ef9-102">SYNOPSIS</span></span>
<span data-ttu-id="87ef9-103">개인 링크 범위 업데이트</span><span class="sxs-lookup"><span data-stu-id="87ef9-103">Update for private link scope</span></span>

## <span data-ttu-id="87ef9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="87ef9-104">SYNTAX</span></span>

### <span data-ttu-id="87ef9-105">ByResourceNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="87ef9-105">ByResourceNameParameterSet (Default)</span></span>
```
Update-AzInsightsPrivateLinkScope -ResourceGroupName <String> -Name <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87ef9-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="87ef9-106">ByResourceIdParameterSet</span></span>
```
Update-AzInsightsPrivateLinkScope -ResourceId <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87ef9-107">ByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="87ef9-107">ByInputObjectParameterSet</span></span>
```
Update-AzInsightsPrivateLinkScope -InputObject <PSMonitorPrivateLinkScope> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87ef9-108">설명은</span><span class="sxs-lookup"><span data-stu-id="87ef9-108">DESCRIPTION</span></span>
<span data-ttu-id="87ef9-109">개인 링크 범위 업데이트</span><span class="sxs-lookup"><span data-stu-id="87ef9-109">Update for private link scope</span></span>

## <span data-ttu-id="87ef9-110">예제의</span><span class="sxs-lookup"><span data-stu-id="87ef9-110">EXAMPLES</span></span>

### <span data-ttu-id="87ef9-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="87ef9-111">Example 1</span></span>
```powershell
Update-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" -Tags "key:value"
```

<span data-ttu-id="87ef9-112">"rg_name" 리소스 그룹의 이름이 "scope_name" 인 개인 링크 범위를 업데이트 하 여 "key: value" 태그를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="87ef9-112">update private link scope with name "scope_name" under resource group "rg_name" to use tag "key:value"</span></span>

### <span data-ttu-id="87ef9-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="87ef9-113">Example 2</span></span>
```powershell
Update-AzInsightsPrivateLinkScope -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/rg_name/providers/microsoft.insights/privateLinkScopes/scope_name" -Tags "key:value"
```

<span data-ttu-id="87ef9-114">"key: value" 태그를 사용 하기 위해 리소스 Id와 함께 개인 링크 범위 업데이트</span><span class="sxs-lookup"><span data-stu-id="87ef9-114">update private link scope with resource Id to use tag "key:value"</span></span>

### <span data-ttu-id="87ef9-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="87ef9-115">Example 3</span></span>
```powershell
Get-AzInsightsPrivateLinkScope -ResourceGroupName "rg_name" -Name "scope_name" | Update-AzInsightsPrivateLinkScope -Tags "key:value"
```

<span data-ttu-id="87ef9-116">"key: value" 태그를 사용 하기 위한 입력 비공개 링크 범위 개체를 사용 하 여 개인 링크 범위 업데이트</span><span class="sxs-lookup"><span data-stu-id="87ef9-116">update private link scope with input private link scope object to use tag "key:value"</span></span>

## <span data-ttu-id="87ef9-117">변수</span><span class="sxs-lookup"><span data-stu-id="87ef9-117">PARAMETERS</span></span>

### <span data-ttu-id="87ef9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87ef9-118">-DefaultProfile</span></span>
<span data-ttu-id="87ef9-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="87ef9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87ef9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="87ef9-120">-InputObject</span></span>
<span data-ttu-id="87ef9-121">PSMonitorPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="87ef9-121">PSMonitorPrivateLinkScope</span></span>

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

### <span data-ttu-id="87ef9-122">-이름</span><span class="sxs-lookup"><span data-stu-id="87ef9-122">-Name</span></span>
<span data-ttu-id="87ef9-123">개인 링크 범위 이름</span><span class="sxs-lookup"><span data-stu-id="87ef9-123">Private Link Scope Name</span></span>

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

### <span data-ttu-id="87ef9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87ef9-124">-ResourceGroupName</span></span>
<span data-ttu-id="87ef9-125">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="87ef9-125">Resource Group Name</span></span>

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

### <span data-ttu-id="87ef9-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="87ef9-126">-ResourceId</span></span>
<span data-ttu-id="87ef9-127">리소스 Id</span><span class="sxs-lookup"><span data-stu-id="87ef9-127">Resource Id</span></span>

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

### <span data-ttu-id="87ef9-128">태그</span><span class="sxs-lookup"><span data-stu-id="87ef9-128">-Tags</span></span>
<span data-ttu-id="87ef9-129">태그도</span><span class="sxs-lookup"><span data-stu-id="87ef9-129">Tags</span></span>

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

### <span data-ttu-id="87ef9-130">-확인</span><span class="sxs-lookup"><span data-stu-id="87ef9-130">-Confirm</span></span>
<span data-ttu-id="87ef9-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="87ef9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87ef9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87ef9-132">-WhatIf</span></span>
<span data-ttu-id="87ef9-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="87ef9-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87ef9-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="87ef9-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87ef9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87ef9-135">CommonParameters</span></span>
<span data-ttu-id="87ef9-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="87ef9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87ef9-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="87ef9-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87ef9-138">입력</span><span class="sxs-lookup"><span data-stu-id="87ef9-138">INPUTS</span></span>

### <span data-ttu-id="87ef9-139">PSMonitorPrivateLinkScope를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="87ef9-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

### <span data-ttu-id="87ef9-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="87ef9-140">System.String</span></span>

## <span data-ttu-id="87ef9-141">출력</span><span class="sxs-lookup"><span data-stu-id="87ef9-141">OUTPUTS</span></span>

### <span data-ttu-id="87ef9-142">PSMonitorPrivateLinkScope를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="87ef9-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="87ef9-143">상속자</span><span class="sxs-lookup"><span data-stu-id="87ef9-143">NOTES</span></span>

## <span data-ttu-id="87ef9-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="87ef9-144">RELATED LINKS</span></span>
