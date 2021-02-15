---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/update-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Update-AzSentinelIncident.md
ms.openlocfilehash: c98270b4e69d80e18ba721de0a6379d40d21fc75
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189124"
---
# <span data-ttu-id="4e372-101">Update-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="4e372-101">Update-AzSentinelIncident</span></span>

## <span data-ttu-id="4e372-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e372-102">SYNOPSIS</span></span>
<span data-ttu-id="4e372-103">인시던트 업데이트</span><span class="sxs-lookup"><span data-stu-id="4e372-103">Update an Incident.</span></span>

## <span data-ttu-id="4e372-104">구문</span><span class="sxs-lookup"><span data-stu-id="4e372-104">SYNTAX</span></span>

### <span data-ttu-id="4e372-105">IncidentId(기본값)</span><span class="sxs-lookup"><span data-stu-id="4e372-105">IncidentId (Default)</span></span>
```
Update-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> -IncidentID <String>
 [-Classification <String>] [-ClassificationComment <String>] [-ClassificationReason <String>]
 [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e372-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="4e372-106">InputObject</span></span>
```
Update-AzSentinelIncident -InputObject <PSSentinelIncident> [-Classification <String>]
 [-ClassificationComment <String>] [-ClassificationReason <String>] [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e372-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e372-107">ResourceId</span></span>
```
Update-AzSentinelIncident -ResourceId <String> [-Classification <String>] [-ClassificationComment <String>]
 [-ClassificationReason <String>] [-Description <String>]
 [-Label <System.Collections.Generic.IList`1[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel]>]
 [-Owner <PSSentinelIncidentOwner>] -Severity <String> -Status <String> -Title <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e372-108">설명</span><span class="sxs-lookup"><span data-stu-id="4e372-108">DESCRIPTION</span></span>
<span data-ttu-id="4e372-109">**Update-AzSentinelIncident** cmdlet은 지정된 작업 영역의 인시던트를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="4e372-109">The **Update-AzSentinelIncident** cmdlet updates the Incident in the specified workspace.</span></span>
<span data-ttu-id="4e372-110">인시던트  개체를 매개 변수로 전달하거나 파이프라인 연산자를 사용하여 전달하거나 필요한 매개 변수를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4e372-110">You can pass an **Incident** object as a parameter or by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="4e372-111">*Confirm* 매개 변수 및 $ConfirmPreference Windows PowerShell cmdlet에서 확인을 요청하는지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4e372-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="4e372-112">예제</span><span class="sxs-lookup"><span data-stu-id="4e372-112">EXAMPLES</span></span>

### <span data-ttu-id="4e372-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="4e372-113">Example 1</span></span>
```powershell
PS C:\> Update-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId" -Severity High
```

<span data-ttu-id="4e372-114">이 명령은 *IncidentId에* 의해 Incident를 얻게 하여 *심각도* 속성을 높음으로 *설정합니다.*</span><span class="sxs-lookup"><span data-stu-id="4e372-114">The command gets the Incident by *IncidentId* and sets the *Severity* property to *High*.</span></span>  <span data-ttu-id="4e372-115">다른 모든 속성은 동일하게 유지됩니다.</span><span class="sxs-lookup"><span data-stu-id="4e372-115">All other properties remain the same.</span></span>

## <span data-ttu-id="4e372-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e372-116">PARAMETERS</span></span>

### <span data-ttu-id="4e372-117">-Classification</span><span class="sxs-lookup"><span data-stu-id="4e372-117">-Classification</span></span>
<span data-ttu-id="4e372-118">인시던트 분류자입니다.</span><span class="sxs-lookup"><span data-stu-id="4e372-118">Incident Classificaiton.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: BenignPositive, FalsePositive, TruePositive, Undetermined

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e372-119">-ClassificationComment</span><span class="sxs-lookup"><span data-stu-id="4e372-119">-ClassificationComment</span></span>
<span data-ttu-id="4e372-120">인시던트 분류 주석입니다.</span><span class="sxs-lookup"><span data-stu-id="4e372-120">Incident Classificaiton Comment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e372-121">-ClassificationReason</span><span class="sxs-lookup"><span data-stu-id="4e372-121">-ClassificationReason</span></span>
<span data-ttu-id="4e372-122">인시던트 분류 이유.</span><span class="sxs-lookup"><span data-stu-id="4e372-122">Incident Classificaiton Reason.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: InaccurateData, IncorrectAlertLogic, SuspiciousActivity, SuspiciousButExpected

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e372-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e372-123">-DefaultProfile</span></span>
<span data-ttu-id="4e372-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4e372-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e372-125">-Description</span><span class="sxs-lookup"><span data-stu-id="4e372-125">-Description</span></span>
<span data-ttu-id="4e372-126">설명.</span><span class="sxs-lookup"><span data-stu-id="4e372-126">Description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e372-127">-IncidentID</span><span class="sxs-lookup"><span data-stu-id="4e372-127">-IncidentID</span></span>
<span data-ttu-id="4e372-128">인시던트 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4e372-128">Incident Id.</span></span>

```yaml
Type: String
Parameter Sets: IncidentId, ParentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e372-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e372-129">-InputObject</span></span>
<span data-ttu-id="4e372-130">InputObject.</span><span class="sxs-lookup"><span data-stu-id="4e372-130">InputObject.</span></span>

```yaml
Type: PSSentinelIncident
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e372-131">-Label</span><span class="sxs-lookup"><span data-stu-id="4e372-131">-Label</span></span>
<span data-ttu-id="4e372-132">인시던트 레이블.</span><span class="sxs-lookup"><span data-stu-id="4e372-132">Incident Labels.</span></span>

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

### <span data-ttu-id="4e372-133">-Owner</span><span class="sxs-lookup"><span data-stu-id="4e372-133">-Owner</span></span>
<span data-ttu-id="4e372-134">인시던트 소유자입니다.</span><span class="sxs-lookup"><span data-stu-id="4e372-134">Incident Owner.</span></span>

```yaml
Type: PSSentinelIncidentOwner
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e372-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e372-135">-ResourceGroupName</span></span>
<span data-ttu-id="4e372-136">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4e372-136">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e372-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4e372-137">-ResourceId</span></span>
<span data-ttu-id="4e372-138">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="4e372-138">Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e372-139">-심각도</span><span class="sxs-lookup"><span data-stu-id="4e372-139">-Severity</span></span>
<span data-ttu-id="4e372-140">인시던트 심각도입니다.</span><span class="sxs-lookup"><span data-stu-id="4e372-140">Incident Severity.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: High, Informational, Low, Medium

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e372-141">-Status</span><span class="sxs-lookup"><span data-stu-id="4e372-141">-Status</span></span>
<span data-ttu-id="4e372-142">인시던트 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="4e372-142">Incident Status.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: Active, Closed, New

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e372-143">-Title</span><span class="sxs-lookup"><span data-stu-id="4e372-143">-Title</span></span>
<span data-ttu-id="4e372-144">인시던트 제목입니다.</span><span class="sxs-lookup"><span data-stu-id="4e372-144">Incident Title.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e372-145">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4e372-145">-WorkspaceName</span></span>
<span data-ttu-id="4e372-146">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4e372-146">Workspace Name.</span></span>

```yaml
Type: String
Parameter Sets: IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e372-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e372-147">-Confirm</span></span>
<span data-ttu-id="4e372-148">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4e372-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e372-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e372-149">-WhatIf</span></span>
<span data-ttu-id="4e372-150">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="4e372-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e372-151">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4e372-151">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e372-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e372-152">CommonParameters</span></span>
<span data-ttu-id="4e372-153">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4e372-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e372-154">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4e372-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e372-155">입력</span><span class="sxs-lookup"><span data-stu-id="4e372-155">INPUTS</span></span>

### <span data-ttu-id="4e372-156">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="4e372-156">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>

### <span data-ttu-id="4e372-157">System.String</span><span class="sxs-lookup"><span data-stu-id="4e372-157">System.String</span></span>

### <span data-ttu-id="4e372-158">System.Collections.Generic.IList'1[[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel, Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="4e372-158">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentLabel, Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="4e372-159">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner</span><span class="sxs-lookup"><span data-stu-id="4e372-159">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncidentOwner</span></span>

## <span data-ttu-id="4e372-160">출력</span><span class="sxs-lookup"><span data-stu-id="4e372-160">OUTPUTS</span></span>

### <span data-ttu-id="4e372-161">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="4e372-161">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>

## <span data-ttu-id="4e372-162">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4e372-162">NOTES</span></span>

## <span data-ttu-id="4e372-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4e372-163">RELATED LINKS</span></span>
