---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/powershell/module/az.alertsmanagement/update-azactionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzActionRule.md
ms.openlocfilehash: 7dcbf947975719a30282037d592469a986990d50
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993099"
---
# <span data-ttu-id="d4c18-101">Update-AzActionRule</span><span class="sxs-lookup"><span data-stu-id="d4c18-101">Update-AzActionRule</span></span>

## <span data-ttu-id="d4c18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4c18-102">SYNOPSIS</span></span>
<span data-ttu-id="d4c18-103">작업 규칙 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d4c18-103">Updates action rule properties.</span></span>

## <span data-ttu-id="d4c18-104">구문</span><span class="sxs-lookup"><span data-stu-id="d4c18-104">SYNTAX</span></span>

### <span data-ttu-id="d4c18-105">ByNameSimplifiedPatch(기본값)</span><span class="sxs-lookup"><span data-stu-id="d4c18-105">ByNameSimplifiedPatch (Default)</span></span>
```
Update-AzActionRule -Name <String> -ResourceGroupName <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4c18-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d4c18-106">ByResourceId</span></span>
```
Update-AzActionRule -ResourceId <String> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d4c18-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d4c18-107">ByInputObject</span></span>
```
Update-AzActionRule -InputObject <PSActionRule> [-Status <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4c18-108">설명</span><span class="sxs-lookup"><span data-stu-id="d4c18-108">DESCRIPTION</span></span>
<span data-ttu-id="d4c18-109">**Update-AzActionRule** cmdlet은 작업 규칙 속성 - 상태 및 태그를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="d4c18-109">**Update-AzActionRule** cmdlet updates action rule properties - status and tags.</span></span>

## <span data-ttu-id="d4c18-110">예제</span><span class="sxs-lookup"><span data-stu-id="d4c18-110">EXAMPLES</span></span>

### <span data-ttu-id="d4c18-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="d4c18-111">Example 1</span></span>
```powershell
PS C:\> Update-AzActionRule -ResourceGroupName "test-rg" -Name "Test-ActionRule" -Status "Disabled"
```

<span data-ttu-id="d4c18-112">이 cmdlet은 작업 규칙을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="d4c18-112">This cmdlet disables the action rule.</span></span> 

## <span data-ttu-id="d4c18-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d4c18-113">PARAMETERS</span></span>

### <span data-ttu-id="d4c18-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4c18-114">-DefaultProfile</span></span>
<span data-ttu-id="d4c18-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d4c18-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4c18-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4c18-116">-InputObject</span></span>
<span data-ttu-id="d4c18-117">작업 규칙 리소스</span><span class="sxs-lookup"><span data-stu-id="d4c18-117">The action rule resource</span></span>

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

### <span data-ttu-id="d4c18-118">-Name</span><span class="sxs-lookup"><span data-stu-id="d4c18-118">-Name</span></span>
<span data-ttu-id="d4c18-119">작업 규칙 이름</span><span class="sxs-lookup"><span data-stu-id="d4c18-119">Action rule name</span></span>

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

### <span data-ttu-id="d4c18-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4c18-120">-ResourceGroupName</span></span>
<span data-ttu-id="d4c18-121">작업 규칙 이름</span><span class="sxs-lookup"><span data-stu-id="d4c18-121">Action rule name</span></span>

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

### <span data-ttu-id="d4c18-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4c18-122">-ResourceId</span></span>
<span data-ttu-id="d4c18-123">작업 규칙의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="d4c18-123">The resource id of action rule</span></span>

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

### <span data-ttu-id="d4c18-124">-Status</span><span class="sxs-lookup"><span data-stu-id="d4c18-124">-Status</span></span>
<span data-ttu-id="d4c18-125">작업 규칙 상태</span><span class="sxs-lookup"><span data-stu-id="d4c18-125">Action rule status</span></span>

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

### <span data-ttu-id="d4c18-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="d4c18-126">-Tag</span></span>
<span data-ttu-id="d4c18-127">작업 규칙 태그</span><span class="sxs-lookup"><span data-stu-id="d4c18-127">Action rule tags</span></span>

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

### <span data-ttu-id="d4c18-128">-확인</span><span class="sxs-lookup"><span data-stu-id="d4c18-128">-Confirm</span></span>
<span data-ttu-id="d4c18-129">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d4c18-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4c18-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4c18-130">-WhatIf</span></span>
<span data-ttu-id="d4c18-131">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d4c18-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4c18-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d4c18-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4c18-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4c18-133">CommonParameters</span></span>
<span data-ttu-id="d4c18-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d4c18-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4c18-135">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d4c18-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4c18-136">입력</span><span class="sxs-lookup"><span data-stu-id="d4c18-136">INPUTS</span></span>

### <span data-ttu-id="d4c18-137">System.String</span><span class="sxs-lookup"><span data-stu-id="d4c18-137">System.String</span></span>

### <span data-ttu-id="d4c18-138">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="d4c18-138">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="d4c18-139">출력</span><span class="sxs-lookup"><span data-stu-id="d4c18-139">OUTPUTS</span></span>

### <span data-ttu-id="d4c18-140">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span><span class="sxs-lookup"><span data-stu-id="d4c18-140">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSActionRule</span></span>

## <span data-ttu-id="d4c18-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d4c18-141">NOTES</span></span>

## <span data-ttu-id="d4c18-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d4c18-142">RELATED LINKS</span></span>
