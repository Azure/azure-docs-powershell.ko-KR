---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
ms.openlocfilehash: 2af687a79255d5e5ab4b49135bf8a8f7b8f819f1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205893"
---
# <span data-ttu-id="7a10b-101">Update-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="7a10b-101">Update-AzActionRule</span></span>

## <span data-ttu-id="7a10b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a10b-102">SYNOPSIS</span></span>
<span data-ttu-id="7a10b-103">작업 규칙 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="7a10b-103">Updates action rule properties.</span></span>

## <span data-ttu-id="7a10b-104">구문</span><span class="sxs-lookup"><span data-stu-id="7a10b-104">SYNTAX</span></span>

### <span data-ttu-id="7a10b-105">ByNameSimplifiedPatch(기본값)</span><span class="sxs-lookup"><span data-stu-id="7a10b-105">ByNameSimplifiedPatch (Default)</span></span>
```
Update-AzActionRule -Name <String> -ResourceGroupName <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a10b-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7a10b-106">ByResourceId</span></span>
```
Update-AzActionRule -ResourceId <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7a10b-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7a10b-107">ByInputObject</span></span>
```
Update-AzActionRule -InputObject <PSActionRule> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a10b-108">설명</span><span class="sxs-lookup"><span data-stu-id="7a10b-108">DESCRIPTION</span></span>
<span data-ttu-id="7a10b-109">**Update-AzActionRule** cmdlet은 작업 규칙 속성(상태 및 태그)을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="7a10b-109">**Update-AzActionRule** cmdlet updates action rule properties - status and tags.</span></span>

## <span data-ttu-id="7a10b-110">예제</span><span class="sxs-lookup"><span data-stu-id="7a10b-110">EXAMPLES</span></span>

### <span data-ttu-id="7a10b-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="7a10b-111">Example 1</span></span>
```powershell
PS C:\> Update-AzActionRule -ResourceGroupName "test-rg" -Name "Test-ActionRule" -Status "Disabled"
```

<span data-ttu-id="7a10b-112">이 cmdlet은 작업 규칙을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7a10b-112">This cmdlet disables the action rule.</span></span> 

## <span data-ttu-id="7a10b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a10b-113">PARAMETERS</span></span>

### <span data-ttu-id="7a10b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a10b-114">-DefaultProfile</span></span>
<span data-ttu-id="7a10b-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7a10b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a10b-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7a10b-116">-InputObject</span></span>
<span data-ttu-id="7a10b-117">작업 규칙 리소스</span><span class="sxs-lookup"><span data-stu-id="7a10b-117">The action rule resource</span></span>

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

### <span data-ttu-id="7a10b-118">-Name</span><span class="sxs-lookup"><span data-stu-id="7a10b-118">-Name</span></span>
<span data-ttu-id="7a10b-119">작업 규칙 이름</span><span class="sxs-lookup"><span data-stu-id="7a10b-119">Action rule name</span></span>

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

### <span data-ttu-id="7a10b-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a10b-120">-ResourceGroupName</span></span>
<span data-ttu-id="7a10b-121">작업 규칙 이름</span><span class="sxs-lookup"><span data-stu-id="7a10b-121">Action rule name</span></span>

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

### <span data-ttu-id="7a10b-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7a10b-122">-ResourceId</span></span>
<span data-ttu-id="7a10b-123">작업 규칙의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="7a10b-123">The resource id of action rule</span></span>

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

### <span data-ttu-id="7a10b-124">-Status</span><span class="sxs-lookup"><span data-stu-id="7a10b-124">-Status</span></span>
<span data-ttu-id="7a10b-125">작업 규칙 상태</span><span class="sxs-lookup"><span data-stu-id="7a10b-125">Action rule status</span></span>

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

### <span data-ttu-id="7a10b-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="7a10b-126">-Tag</span></span>
<span data-ttu-id="7a10b-127">작업 규칙 태그</span><span class="sxs-lookup"><span data-stu-id="7a10b-127">Action rule tags</span></span>

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

### <span data-ttu-id="7a10b-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7a10b-128">-Confirm</span></span>
<span data-ttu-id="7a10b-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a10b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a10b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a10b-130">-WhatIf</span></span>
<span data-ttu-id="7a10b-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7a10b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a10b-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7a10b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a10b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a10b-133">CommonParameters</span></span>
<span data-ttu-id="7a10b-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7a10b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a10b-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7a10b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a10b-136">입력</span><span class="sxs-lookup"><span data-stu-id="7a10b-136">INPUTS</span></span>

### <span data-ttu-id="7a10b-137">System.String</span><span class="sxs-lookup"><span data-stu-id="7a10b-137">System.String</span></span>

### <span data-ttu-id="7a10b-138">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="7a10b-138">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="7a10b-139">출력</span><span class="sxs-lookup"><span data-stu-id="7a10b-139">OUTPUTS</span></span>

### <span data-ttu-id="7a10b-140">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="7a10b-140">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="7a10b-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7a10b-141">NOTES</span></span>

## <span data-ttu-id="7a10b-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7a10b-142">RELATED LINKS</span></span>
