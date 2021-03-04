---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/powershell/module/az.securityinsights/remove-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelIncident.md
ms.openlocfilehash: 80badb2e73aa00fd9a221c20372ab42499c1cb0e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969899"
---
# <span data-ttu-id="64444-101">Remove-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="64444-101">Remove-AzSentinelIncident</span></span>

## <span data-ttu-id="64444-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64444-102">SYNOPSIS</span></span>
<span data-ttu-id="64444-103">인시던트 삭제</span><span class="sxs-lookup"><span data-stu-id="64444-103">Delete an Incident.</span></span>

## <span data-ttu-id="64444-104">구문</span><span class="sxs-lookup"><span data-stu-id="64444-104">SYNTAX</span></span>

### <span data-ttu-id="64444-105">incidentId(기본값)</span><span class="sxs-lookup"><span data-stu-id="64444-105">IncidentId (Default)</span></span>
```
Remove-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64444-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="64444-106">InputObject</span></span>
```
Remove-AzSentinelIncident -InputObject <PSSentinelIncident> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64444-107">설명</span><span class="sxs-lookup"><span data-stu-id="64444-107">DESCRIPTION</span></span>
<span data-ttu-id="64444-108">**Remove-AzSentinelIncident** cmdlet은 지정된 작업 영역의 인시던트를 영구적으로 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="64444-108">The **Remove-AzSentinelIncident** cmdlet permanently deletes a Incident from a specified workspace.</span></span>
<span data-ttu-id="64444-109">파이프라인 연산자를  사용하여 인시던트 개체를 전달하거나 필요한 매개 변수를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64444-109">You can pass an **Incident** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="64444-110">확인 매개 변수 및 $ConfirmPreference Windows PowerShell 변수를 사용하여 cmdlet에서 확인을 묻는 메시지를 표시하는지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="64444-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="64444-111">예제</span><span class="sxs-lookup"><span data-stu-id="64444-111">EXAMPLES</span></span>

### <span data-ttu-id="64444-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="64444-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
```

<span data-ttu-id="64444-113">이 명령은 작업 영역에서 인시던트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="64444-113">This command removes the Incident from the workspace.</span></span>

## <span data-ttu-id="64444-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="64444-114">PARAMETERS</span></span>

### <span data-ttu-id="64444-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64444-115">-DefaultProfile</span></span>
<span data-ttu-id="64444-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="64444-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64444-117">-incidentId</span><span class="sxs-lookup"><span data-stu-id="64444-117">-IncidentId</span></span>
<span data-ttu-id="64444-118">인시던트 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="64444-118">Incident Id.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64444-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="64444-119">-InputObject</span></span>
<span data-ttu-id="64444-120">InputObject.</span><span class="sxs-lookup"><span data-stu-id="64444-120">InputObject.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="64444-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="64444-121">-PassThru</span></span>
<span data-ttu-id="64444-122">PassThru</span><span class="sxs-lookup"><span data-stu-id="64444-122">PassThru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="64444-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64444-123">-ResourceGroupName</span></span>
<span data-ttu-id="64444-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="64444-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64444-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="64444-125">-WorkspaceName</span></span>
<span data-ttu-id="64444-126">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="64444-126">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64444-127">-확인</span><span class="sxs-lookup"><span data-stu-id="64444-127">-Confirm</span></span>
<span data-ttu-id="64444-128">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="64444-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64444-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64444-129">-WhatIf</span></span>
<span data-ttu-id="64444-130">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="64444-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="64444-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="64444-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="64444-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64444-132">CommonParameters</span></span>
<span data-ttu-id="64444-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="64444-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64444-134">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="64444-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64444-135">입력</span><span class="sxs-lookup"><span data-stu-id="64444-135">INPUTS</span></span>

### <span data-ttu-id="64444-136">System.String</span><span class="sxs-lookup"><span data-stu-id="64444-136">System.String</span></span>
### <span data-ttu-id="64444-137">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="64444-137">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="64444-138">출력</span><span class="sxs-lookup"><span data-stu-id="64444-138">OUTPUTS</span></span>

### <span data-ttu-id="64444-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="64444-139">System.Boolean</span></span>
## <span data-ttu-id="64444-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="64444-140">NOTES</span></span>

## <span data-ttu-id="64444-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="64444-141">RELATED LINKS</span></span>
