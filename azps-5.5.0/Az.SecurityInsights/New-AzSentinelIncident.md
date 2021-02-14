---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncident.md
ms.openlocfilehash: b3618f178ea5dee54991c037da78ac51f2ed4502
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201724"
---
# <span data-ttu-id="d4222-101">New-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="d4222-101">New-AzSentinelIncident</span></span>

## <span data-ttu-id="d4222-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4222-102">SYNOPSIS</span></span>
<span data-ttu-id="d4222-103">인시던트 만들기</span><span class="sxs-lookup"><span data-stu-id="d4222-103">Create an Incident.</span></span>

## <span data-ttu-id="d4222-104">구문</span><span class="sxs-lookup"><span data-stu-id="d4222-104">SYNTAX</span></span>

```
New-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> [-IncidentId <String>]
 [-Classificaton <String>] [-ClassificationComment <String>] [-ClassificationReason <String>]
 [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4222-105">설명</span><span class="sxs-lookup"><span data-stu-id="d4222-105">DESCRIPTION</span></span>
<span data-ttu-id="d4222-106">**New-AzSentinelIncident** cmdlet은 지정된 작업 영역의 인시던트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d4222-106">The **New-AzSentinelIncident** cmdlet creates a Incident from the specified workspace.</span></span>
<span data-ttu-id="d4222-107">*Confirm* 매개 변수 및 $ConfirmPreference Windows PowerShell cmdlet에서 확인을 요청하는지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d4222-107">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="d4222-108">예제</span><span class="sxs-lookup"><span data-stu-id="d4222-108">EXAMPLES</span></span>

### <span data-ttu-id="d4222-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="d4222-109">Example 1</span></span>
```powershell
PS C:\> $Incident = New-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -Title "NewIncident" -Severity Low -Status New
```

<span data-ttu-id="d4222-110">이 예제에서는  지정된 작업 영역의 인시던트를 만든 다음 인시던트 $Incident 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="d4222-110">This example creates an **Incident** in the specified workspace, and then stores it in the $Incident variable.</span></span>

## <span data-ttu-id="d4222-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4222-111">PARAMETERS</span></span>

### <span data-ttu-id="d4222-112">-ClassificationComment</span><span class="sxs-lookup"><span data-stu-id="d4222-112">-ClassificationComment</span></span>
<span data-ttu-id="d4222-113">인시던트 분류 주석입니다.</span><span class="sxs-lookup"><span data-stu-id="d4222-113">Incident Classificaiton Comment.</span></span>

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

### <span data-ttu-id="d4222-114">-ClassificationReason</span><span class="sxs-lookup"><span data-stu-id="d4222-114">-ClassificationReason</span></span>
<span data-ttu-id="d4222-115">인시던트 분류 이유.</span><span class="sxs-lookup"><span data-stu-id="d4222-115">Incident Classificaiton Reason.</span></span>

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

### <span data-ttu-id="d4222-116">-Classificaton</span><span class="sxs-lookup"><span data-stu-id="d4222-116">-Classificaton</span></span>
<span data-ttu-id="d4222-117">인시던트 분류자입니다.</span><span class="sxs-lookup"><span data-stu-id="d4222-117">Incident Classificaiton.</span></span>

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

### <span data-ttu-id="d4222-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4222-118">-DefaultProfile</span></span>
<span data-ttu-id="d4222-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d4222-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4222-120">-Description</span><span class="sxs-lookup"><span data-stu-id="d4222-120">-Description</span></span>
<span data-ttu-id="d4222-121">설명.</span><span class="sxs-lookup"><span data-stu-id="d4222-121">Description.</span></span>

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

### <span data-ttu-id="d4222-122">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="d4222-122">-IncidentId</span></span>
<span data-ttu-id="d4222-123">인시던트 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d4222-123">Incident Id.</span></span>

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

### <span data-ttu-id="d4222-124">-Label</span><span class="sxs-lookup"><span data-stu-id="d4222-124">-Label</span></span>
<span data-ttu-id="d4222-125">인시던트 레이블.</span><span class="sxs-lookup"><span data-stu-id="d4222-125">Incident Labels.</span></span>

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

### <span data-ttu-id="d4222-126">-Owner</span><span class="sxs-lookup"><span data-stu-id="d4222-126">-Owner</span></span>
<span data-ttu-id="d4222-127">인시던트 소유자입니다.</span><span class="sxs-lookup"><span data-stu-id="d4222-127">Incident Owner.</span></span>

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

### <span data-ttu-id="d4222-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4222-128">-ResourceGroupName</span></span>
<span data-ttu-id="d4222-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d4222-129">Resource group name.</span></span>

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

### <span data-ttu-id="d4222-130">-심각도</span><span class="sxs-lookup"><span data-stu-id="d4222-130">-Severity</span></span>
<span data-ttu-id="d4222-131">인시던트 심각도입니다.</span><span class="sxs-lookup"><span data-stu-id="d4222-131">Incident Severity.</span></span>

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

### <span data-ttu-id="d4222-132">-Status</span><span class="sxs-lookup"><span data-stu-id="d4222-132">-Status</span></span>
<span data-ttu-id="d4222-133">인시던트 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="d4222-133">Incident Status.</span></span>

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

### <span data-ttu-id="d4222-134">-Title</span><span class="sxs-lookup"><span data-stu-id="d4222-134">-Title</span></span>
<span data-ttu-id="d4222-135">인시던트 제목입니다.</span><span class="sxs-lookup"><span data-stu-id="d4222-135">Incident Title.</span></span>

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

### <span data-ttu-id="d4222-136">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d4222-136">-WorkspaceName</span></span>
<span data-ttu-id="d4222-137">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d4222-137">Workspace Name.</span></span>

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

### <span data-ttu-id="d4222-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d4222-138">-Confirm</span></span>
<span data-ttu-id="d4222-139">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d4222-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4222-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4222-140">-WhatIf</span></span>
<span data-ttu-id="d4222-141">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="d4222-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d4222-142">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d4222-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4222-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4222-143">CommonParameters</span></span>
<span data-ttu-id="d4222-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d4222-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4222-145">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d4222-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4222-146">입력</span><span class="sxs-lookup"><span data-stu-id="d4222-146">INPUTS</span></span>

### <span data-ttu-id="d4222-147">System.Collections.Generic.IList'1[[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel, Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="d4222-147">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel, Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
### <span data-ttu-id="d4222-148">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner</span><span class="sxs-lookup"><span data-stu-id="d4222-148">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner</span></span>
## <span data-ttu-id="d4222-149">출력</span><span class="sxs-lookup"><span data-stu-id="d4222-149">OUTPUTS</span></span>

### <span data-ttu-id="d4222-150">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="d4222-150">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="d4222-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d4222-151">NOTES</span></span>

## <span data-ttu-id="d4222-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d4222-152">RELATED LINKS</span></span>
