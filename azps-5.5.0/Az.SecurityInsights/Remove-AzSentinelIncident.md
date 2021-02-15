---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/remove-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Remove-AzSentinelIncident.md
ms.openlocfilehash: faf2c40bc43c1b42861bc93d2398d4d26731c112
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197884"
---
# <span data-ttu-id="94f24-101">Remove-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="94f24-101">Remove-AzSentinelIncident</span></span>

## <span data-ttu-id="94f24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94f24-102">SYNOPSIS</span></span>
<span data-ttu-id="94f24-103">인시던트 삭제</span><span class="sxs-lookup"><span data-stu-id="94f24-103">Delete an Incident.</span></span>

## <span data-ttu-id="94f24-104">구문</span><span class="sxs-lookup"><span data-stu-id="94f24-104">SYNTAX</span></span>

### <span data-ttu-id="94f24-105">IncidentId(기본값)</span><span class="sxs-lookup"><span data-stu-id="94f24-105">IncidentId (Default)</span></span>
```
Remove-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94f24-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="94f24-106">InputObject</span></span>
```
Remove-AzSentinelIncident -InputObject <PSSentinelIncident> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94f24-107">설명</span><span class="sxs-lookup"><span data-stu-id="94f24-107">DESCRIPTION</span></span>
<span data-ttu-id="94f24-108">**Remove-AzSentinelIncident** cmdlet은 지정된 작업 영역의 인시던트가 영구적으로 삭제됩니다.</span><span class="sxs-lookup"><span data-stu-id="94f24-108">The **Remove-AzSentinelIncident** cmdlet permanently deletes a Incident from a specified workspace.</span></span>
<span data-ttu-id="94f24-109">파이프라인 연산자를 사용하여 **Incident** 개체를 전달하거나 필요한 매개 변수를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94f24-109">You can pass an **Incident** object by using the pipeline operator, or alternatively you can specify the required parameters.</span></span>
<span data-ttu-id="94f24-110">Confirm 매개 변수 및 $ConfirmPreference Windows PowerShell cmdlet에서 확인을 요청하는지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="94f24-110">You can use the Confirm parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="94f24-111">예제</span><span class="sxs-lookup"><span data-stu-id="94f24-111">EXAMPLES</span></span>

### <span data-ttu-id="94f24-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="94f24-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
```

<span data-ttu-id="94f24-113">이 명령은 작업 영역에서 인시던트를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="94f24-113">This command removes the Incident from the workspace.</span></span>

## <span data-ttu-id="94f24-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94f24-114">PARAMETERS</span></span>

### <span data-ttu-id="94f24-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94f24-115">-DefaultProfile</span></span>
<span data-ttu-id="94f24-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="94f24-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94f24-117">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="94f24-117">-IncidentId</span></span>
<span data-ttu-id="94f24-118">인시던트 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="94f24-118">Incident Id.</span></span>

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

### <span data-ttu-id="94f24-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94f24-119">-InputObject</span></span>
<span data-ttu-id="94f24-120">InputObject.</span><span class="sxs-lookup"><span data-stu-id="94f24-120">InputObject.</span></span>

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

### <span data-ttu-id="94f24-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="94f24-121">-PassThru</span></span>
<span data-ttu-id="94f24-122">PassThru</span><span class="sxs-lookup"><span data-stu-id="94f24-122">PassThru</span></span>

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

### <span data-ttu-id="94f24-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94f24-123">-ResourceGroupName</span></span>
<span data-ttu-id="94f24-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="94f24-124">Resource group name.</span></span>

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

### <span data-ttu-id="94f24-125">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="94f24-125">-WorkspaceName</span></span>
<span data-ttu-id="94f24-126">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="94f24-126">Workspace Name.</span></span>

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

### <span data-ttu-id="94f24-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="94f24-127">-Confirm</span></span>
<span data-ttu-id="94f24-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="94f24-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94f24-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94f24-129">-WhatIf</span></span>
<span data-ttu-id="94f24-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="94f24-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94f24-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="94f24-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94f24-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94f24-132">CommonParameters</span></span>
<span data-ttu-id="94f24-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="94f24-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94f24-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="94f24-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94f24-135">입력</span><span class="sxs-lookup"><span data-stu-id="94f24-135">INPUTS</span></span>

### <span data-ttu-id="94f24-136">System.String</span><span class="sxs-lookup"><span data-stu-id="94f24-136">System.String</span></span>
### <span data-ttu-id="94f24-137">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="94f24-137">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="94f24-138">출력</span><span class="sxs-lookup"><span data-stu-id="94f24-138">OUTPUTS</span></span>

### <span data-ttu-id="94f24-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="94f24-139">System.Boolean</span></span>
## <span data-ttu-id="94f24-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="94f24-140">NOTES</span></span>

## <span data-ttu-id="94f24-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="94f24-141">RELATED LINKS</span></span>
