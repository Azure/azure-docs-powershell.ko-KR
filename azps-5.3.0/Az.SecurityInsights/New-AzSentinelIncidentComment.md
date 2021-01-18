---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/new-azsentinelincidentcomment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentComment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/New-AzSentinelIncidentComment.md
ms.openlocfilehash: 8824832b1b3d09a24998891ad4636e3a3e0f1e19
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494927"
---
# <span data-ttu-id="1f741-101">New-AzSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="1f741-101">New-AzSentinelIncidentComment</span></span>

## <span data-ttu-id="1f741-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1f741-102">SYNOPSIS</span></span>
<span data-ttu-id="1f741-103">인시던트에 인시던트 주석을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="1f741-103">Add an Incident Comment to an Incident.</span></span>

## <span data-ttu-id="1f741-104">구문</span><span class="sxs-lookup"><span data-stu-id="1f741-104">SYNTAX</span></span>

```
New-AzSentinelIncidentComment -ResourceGroupName <String> -WorkspaceName <String> -IncidentId <String>
 [-IncidentCommentId <String>] -Message <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f741-105">설명</span><span class="sxs-lookup"><span data-stu-id="1f741-105">DESCRIPTION</span></span>
<span data-ttu-id="1f741-106">**New-AzSentinelIncidentComment** cmdlet은 지정된 작업 영역의 인시던트 주석을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1f741-106">The **New-AzSentinelIncidentComment** cmdlet creates a Incident Comment from the specified workspace.</span></span>
<span data-ttu-id="1f741-107">*Confirm* 매개 변수 및 $ConfirmPreference Windows PowerShell cmdlet에서 확인을 요청하는지 여부를 제어할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1f741-107">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="1f741-108">예제</span><span class="sxs-lookup"><span data-stu-id="1f741-108">EXAMPLES</span></span>

### <span data-ttu-id="1f741-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="1f741-109">Example 1</span></span>
```powershell
PS C:\> $Incident = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
PS C:\> $IncidentComment = New-AzSentinelIncidentComment -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId ($Incident.Name) -Message "Still needs investigation"
```

<span data-ttu-id="1f741-110">이 예제에서는 지정된 작업 영역의 **IncidentComment를** 만든 다음, 해당 변수에 $IncidentComment 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="1f741-110">This example creates an **IncidentComment** in the specified workspace, and then stores it in the $IncidentComment variable.</span></span>

## <span data-ttu-id="1f741-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1f741-111">PARAMETERS</span></span>

### <span data-ttu-id="1f741-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f741-112">-DefaultProfile</span></span>
<span data-ttu-id="1f741-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1f741-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f741-114">-IncidentCommentId</span><span class="sxs-lookup"><span data-stu-id="1f741-114">-IncidentCommentId</span></span>
<span data-ttu-id="1f741-115">인시던트 주석 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1f741-115">Incident Comment Id.</span></span>

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

### <span data-ttu-id="1f741-116">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="1f741-116">-IncidentId</span></span>
<span data-ttu-id="1f741-117">인시던트 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="1f741-117">Incident Id.</span></span>

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

### <span data-ttu-id="1f741-118">-Message</span><span class="sxs-lookup"><span data-stu-id="1f741-118">-Message</span></span>
<span data-ttu-id="1f741-119">인시던트 메시지입니다.</span><span class="sxs-lookup"><span data-stu-id="1f741-119">Incident Message.</span></span>

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

### <span data-ttu-id="1f741-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f741-120">-ResourceGroupName</span></span>
<span data-ttu-id="1f741-121">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1f741-121">Resource group name.</span></span>

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

### <span data-ttu-id="1f741-122">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1f741-122">-WorkspaceName</span></span>
<span data-ttu-id="1f741-123">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1f741-123">Workspace Name.</span></span>

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

### <span data-ttu-id="1f741-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1f741-124">-Confirm</span></span>
<span data-ttu-id="1f741-125">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1f741-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f741-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f741-126">-WhatIf</span></span>
<span data-ttu-id="1f741-127">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1f741-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1f741-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1f741-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f741-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f741-129">CommonParameters</span></span>
<span data-ttu-id="1f741-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1f741-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f741-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1f741-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f741-132">입력</span><span class="sxs-lookup"><span data-stu-id="1f741-132">INPUTS</span></span>

### <span data-ttu-id="1f741-133">없음</span><span class="sxs-lookup"><span data-stu-id="1f741-133">None</span></span>
## <span data-ttu-id="1f741-134">출력</span><span class="sxs-lookup"><span data-stu-id="1f741-134">OUTPUTS</span></span>

### <span data-ttu-id="1f741-135">Microsoft.Azure.Commands.SecurityInsights.Models.IncidentComments.PSSentinelIncidentComment</span><span class="sxs-lookup"><span data-stu-id="1f741-135">Microsoft.Azure.Commands.SecurityInsights.Models.IncidentComments.PSSentinelIncidentComment</span></span>
## <span data-ttu-id="1f741-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1f741-136">NOTES</span></span>

## <span data-ttu-id="1f741-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1f741-137">RELATED LINKS</span></span>
