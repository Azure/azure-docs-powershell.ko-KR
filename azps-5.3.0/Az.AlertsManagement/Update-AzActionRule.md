---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
ms.openlocfilehash: 2af687a79255d5e5ab4b49135bf8a8f7b8f819f1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494527"
---
# <span data-ttu-id="c2523-101">Update-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="c2523-101">Update-AzActionRule</span></span>

## <span data-ttu-id="c2523-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2523-102">SYNOPSIS</span></span>
<span data-ttu-id="c2523-103">작업 규칙 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c2523-103">Updates action rule properties.</span></span>

## <span data-ttu-id="c2523-104">구문</span><span class="sxs-lookup"><span data-stu-id="c2523-104">SYNTAX</span></span>

### <span data-ttu-id="c2523-105">ByNameSimplifiedPatch(기본값)</span><span class="sxs-lookup"><span data-stu-id="c2523-105">ByNameSimplifiedPatch (Default)</span></span>
```
Update-AzActionRule -Name <String> -ResourceGroupName <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2523-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c2523-106">ByResourceId</span></span>
```
Update-AzActionRule -ResourceId <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2523-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c2523-107">ByInputObject</span></span>
```
Update-AzActionRule -InputObject <PSActionRule> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2523-108">설명</span><span class="sxs-lookup"><span data-stu-id="c2523-108">DESCRIPTION</span></span>
<span data-ttu-id="c2523-109">**Update-AzActionRule** cmdlet은 작업 규칙 속성(상태 및 태그)을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c2523-109">**Update-AzActionRule** cmdlet updates action rule properties - status and tags.</span></span>

## <span data-ttu-id="c2523-110">예제</span><span class="sxs-lookup"><span data-stu-id="c2523-110">EXAMPLES</span></span>

### <span data-ttu-id="c2523-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="c2523-111">Example 1</span></span>
```powershell
PS C:\> Update-AzActionRule -ResourceGroupName "test-rg" -Name "Test-ActionRule" -Status "Disabled"
```

<span data-ttu-id="c2523-112">이 cmdlet은 작업 규칙을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="c2523-112">This cmdlet disables the action rule.</span></span> 

## <span data-ttu-id="c2523-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2523-113">PARAMETERS</span></span>

### <span data-ttu-id="c2523-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2523-114">-DefaultProfile</span></span>
<span data-ttu-id="c2523-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c2523-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2523-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2523-116">-InputObject</span></span>
<span data-ttu-id="c2523-117">작업 규칙 리소스</span><span class="sxs-lookup"><span data-stu-id="c2523-117">The action rule resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2523-118">-Name</span><span class="sxs-lookup"><span data-stu-id="c2523-118">-Name</span></span>
<span data-ttu-id="c2523-119">작업 규칙 이름</span><span class="sxs-lookup"><span data-stu-id="c2523-119">Action rule name</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameSimplifiedPatch
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2523-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2523-120">-ResourceGroupName</span></span>
<span data-ttu-id="c2523-121">작업 규칙 이름</span><span class="sxs-lookup"><span data-stu-id="c2523-121">Action rule name</span></span>

```yaml
Type: System.String
Parameter Sets: ByNameSimplifiedPatch
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2523-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2523-122">-ResourceId</span></span>
<span data-ttu-id="c2523-123">작업 규칙의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="c2523-123">The resource id of action rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2523-124">-Status</span><span class="sxs-lookup"><span data-stu-id="c2523-124">-Status</span></span>
<span data-ttu-id="c2523-125">작업 규칙 상태</span><span class="sxs-lookup"><span data-stu-id="c2523-125">Action rule status</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2523-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="c2523-126">-Tag</span></span>
<span data-ttu-id="c2523-127">작업 규칙 태그</span><span class="sxs-lookup"><span data-stu-id="c2523-127">Action rule tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2523-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c2523-128">-Confirm</span></span>
<span data-ttu-id="c2523-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2523-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2523-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2523-130">-WhatIf</span></span>
<span data-ttu-id="c2523-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c2523-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2523-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c2523-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2523-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2523-133">CommonParameters</span></span>
<span data-ttu-id="c2523-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c2523-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2523-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c2523-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2523-136">입력</span><span class="sxs-lookup"><span data-stu-id="c2523-136">INPUTS</span></span>

### <span data-ttu-id="c2523-137">System.String</span><span class="sxs-lookup"><span data-stu-id="c2523-137">System.String</span></span>

### <span data-ttu-id="c2523-138">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="c2523-138">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="c2523-139">출력</span><span class="sxs-lookup"><span data-stu-id="c2523-139">OUTPUTS</span></span>

### <span data-ttu-id="c2523-140">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="c2523-140">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="c2523-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c2523-141">NOTES</span></span>

## <span data-ttu-id="c2523-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c2523-142">RELATED LINKS</span></span>
