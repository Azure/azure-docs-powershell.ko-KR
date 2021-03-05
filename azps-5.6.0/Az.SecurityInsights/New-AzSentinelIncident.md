---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/new-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncident.md
ms.openlocfilehash: 6cb65832484c7038f5740c481836d8fe889ebc94
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005648"
---
# <span data-ttu-id="f8c48-101">New-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="f8c48-101">New-AzSentinelIncident</span></span>

## <span data-ttu-id="f8c48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8c48-102">SYNOPSIS</span></span>
<span data-ttu-id="f8c48-103">인시던트 만들기</span><span class="sxs-lookup"><span data-stu-id="f8c48-103">Create an Incident.</span></span>

## <span data-ttu-id="f8c48-104">구문</span><span class="sxs-lookup"><span data-stu-id="f8c48-104">SYNTAX</span></span>

```
New-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> [-IncidentId <String>]
 [-Classificaton <String>] [-ClassificationComment <String>] [-ClassificationReason <String>]
 [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8c48-105">설명</span><span class="sxs-lookup"><span data-stu-id="f8c48-105">DESCRIPTION</span></span>
<span data-ttu-id="f8c48-106">**New-AzSentinelIncident** cmdlet은 지정된 작업 영역의 인시던트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f8c48-106">The **New-AzSentinelIncident** cmdlet creates a Incident from the specified workspace.</span></span>
<span data-ttu-id="f8c48-107">확인 매개  변수 및 $ConfirmPreference Windows PowerShell 변수를 사용하여 cmdlet에서 확인을 묻는 메시지를 표시하는지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f8c48-107">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="f8c48-108">예제</span><span class="sxs-lookup"><span data-stu-id="f8c48-108">EXAMPLES</span></span>

### <span data-ttu-id="f8c48-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="f8c48-109">Example 1</span></span>
```powershell
PS C:\> $Incident = New-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -Title "NewIncident" -Severity Low -Status New
```

<span data-ttu-id="f8c48-110">이 예제에서는  지정된 작업 영역의 인시던트를 만든 다음, 인시던트 $Incident 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="f8c48-110">This example creates an **Incident** in the specified workspace, and then stores it in the $Incident variable.</span></span>

## <span data-ttu-id="f8c48-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f8c48-111">PARAMETERS</span></span>

### <span data-ttu-id="f8c48-112">-ClassificationComment</span><span class="sxs-lookup"><span data-stu-id="f8c48-112">-ClassificationComment</span></span>
<span data-ttu-id="f8c48-113">인시던트 분류자 주석입니다.</span><span class="sxs-lookup"><span data-stu-id="f8c48-113">Incident Classificaiton Comment.</span></span>

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

### <span data-ttu-id="f8c48-114">-ClassificationReason</span><span class="sxs-lookup"><span data-stu-id="f8c48-114">-ClassificationReason</span></span>
<span data-ttu-id="f8c48-115">인시던트 분류자이톤 이유입니다.</span><span class="sxs-lookup"><span data-stu-id="f8c48-115">Incident Classificaiton Reason.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: InaccurateData, IncorrectAlertLogic, SuspiciousActivity, SuspiciousButExpected

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8c48-116">-Classificaton</span><span class="sxs-lookup"><span data-stu-id="f8c48-116">-Classificaton</span></span>
<span data-ttu-id="f8c48-117">인시던트 분류.</span><span class="sxs-lookup"><span data-stu-id="f8c48-117">Incident Classificaiton.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: BenignPositive, FalsePositive, TruePositive, Undetermined

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8c48-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8c48-118">-DefaultProfile</span></span>
<span data-ttu-id="f8c48-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f8c48-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8c48-120">-Description</span><span class="sxs-lookup"><span data-stu-id="f8c48-120">-Description</span></span>
<span data-ttu-id="f8c48-121">설명입니다.</span><span class="sxs-lookup"><span data-stu-id="f8c48-121">Description.</span></span>

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

### <span data-ttu-id="f8c48-122">-incidentId</span><span class="sxs-lookup"><span data-stu-id="f8c48-122">-IncidentId</span></span>
<span data-ttu-id="f8c48-123">인시던트 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f8c48-123">Incident Id.</span></span>

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

### <span data-ttu-id="f8c48-124">-Label</span><span class="sxs-lookup"><span data-stu-id="f8c48-124">-Label</span></span>
<span data-ttu-id="f8c48-125">인시던트 레이블입니다.</span><span class="sxs-lookup"><span data-stu-id="f8c48-125">Incident Labels.</span></span>

```yaml
Type: System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8c48-126">-소유자</span><span class="sxs-lookup"><span data-stu-id="f8c48-126">-Owner</span></span>
<span data-ttu-id="f8c48-127">인시던트 소유자입니다.</span><span class="sxs-lookup"><span data-stu-id="f8c48-127">Incident Owner.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f8c48-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8c48-128">-ResourceGroupName</span></span>
<span data-ttu-id="f8c48-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f8c48-129">Resource group name.</span></span>

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

### <span data-ttu-id="f8c48-130">-심각도</span><span class="sxs-lookup"><span data-stu-id="f8c48-130">-Severity</span></span>
<span data-ttu-id="f8c48-131">인시던트 심각도입니다.</span><span class="sxs-lookup"><span data-stu-id="f8c48-131">Incident Severity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: High, Informational, Low, Medium

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8c48-132">-Status</span><span class="sxs-lookup"><span data-stu-id="f8c48-132">-Status</span></span>
<span data-ttu-id="f8c48-133">인시던트 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="f8c48-133">Incident Status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Active, Closed, New

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8c48-134">-Title</span><span class="sxs-lookup"><span data-stu-id="f8c48-134">-Title</span></span>
<span data-ttu-id="f8c48-135">인시던트 타이틀입니다.</span><span class="sxs-lookup"><span data-stu-id="f8c48-135">Incident Title.</span></span>

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

### <span data-ttu-id="f8c48-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f8c48-136">-WorkspaceName</span></span>
<span data-ttu-id="f8c48-137">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f8c48-137">Workspace Name.</span></span>

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

### <span data-ttu-id="f8c48-138">-확인</span><span class="sxs-lookup"><span data-stu-id="f8c48-138">-Confirm</span></span>
<span data-ttu-id="f8c48-139">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f8c48-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8c48-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8c48-140">-WhatIf</span></span>
<span data-ttu-id="f8c48-141">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="f8c48-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f8c48-142">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f8c48-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8c48-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8c48-143">CommonParameters</span></span>
<span data-ttu-id="f8c48-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f8c48-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8c48-145">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f8c48-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8c48-146">입력</span><span class="sxs-lookup"><span data-stu-id="f8c48-146">INPUTS</span></span>

### <span data-ttu-id="f8c48-147">System.Collections.Generic.IList'1[[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentincidentLabel, Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="f8c48-147">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel, Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
### <span data-ttu-id="f8c48-148">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentincidentOwner</span><span class="sxs-lookup"><span data-stu-id="f8c48-148">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner</span></span>
## <span data-ttu-id="f8c48-149">출력</span><span class="sxs-lookup"><span data-stu-id="f8c48-149">OUTPUTS</span></span>

### <span data-ttu-id="f8c48-150">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="f8c48-150">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="f8c48-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f8c48-151">NOTES</span></span>

## <span data-ttu-id="f8c48-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f8c48-152">RELATED LINKS</span></span>
