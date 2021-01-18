---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncident.md
ms.openlocfilehash: eb0854ee3a71af3bdf19d2258187c435fb0f5860
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494943"
---
# <span data-ttu-id="d91a4-101">Get-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="d91a4-101">Get-AzSentinelIncident</span></span>

## <span data-ttu-id="d91a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d91a4-102">SYNOPSIS</span></span>
<span data-ttu-id="d91a4-103">인시던트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d91a4-103">Get an Incident.</span></span>

## <span data-ttu-id="d91a4-104">구문</span><span class="sxs-lookup"><span data-stu-id="d91a4-104">SYNTAX</span></span>

### <span data-ttu-id="d91a4-105">WorkspaceScope(기본값)</span><span class="sxs-lookup"><span data-stu-id="d91a4-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d91a4-106">IncidentId</span><span class="sxs-lookup"><span data-stu-id="d91a4-106">IncidentId</span></span>
```
Get-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> [-IncidentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d91a4-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="d91a4-107">ResourceId</span></span>
```
Get-AzSentinelIncident -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d91a4-108">설명</span><span class="sxs-lookup"><span data-stu-id="d91a4-108">DESCRIPTION</span></span>
<span data-ttu-id="d91a4-109">**Get-AzSentinelIncident** cmdlet은 지정된 작업 영역의 인시던트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d91a4-109">The **Get-AzSentinelIncident** cmdlet gets an Incident from the specified workspace.</span></span>
<span data-ttu-id="d91a4-110">IncidentId 매개 변수를 *지정하면* 단일 **Incident** 개체가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="d91a4-110">If you specify the *IncidentId* parameter, a single **Incident** object is returned.</span></span>
<span data-ttu-id="d91a4-111">*IncidentId* 매개 변수를 지정하지 않으면 지정된 작업 영역의 모든 인시던트가 포함된 배열이 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="d91a4-111">If you do not specify the *IncidentId* parameter, an array containing all of the Incidents in the specified workspace are returned.</span></span>
<span data-ttu-id="d91a4-112">인시던트  개체를 사용하여 인시던트 업데이트를 할 수 있습니다. 예를 들어 인시던트 메모를 추가할 수 **있습니다.**</span><span class="sxs-lookup"><span data-stu-id="d91a4-112">You can use the **Incident** object to update the Incident, for example you can add Notes the **Incident**.</span></span>

## <span data-ttu-id="d91a4-113">예제</span><span class="sxs-lookup"><span data-stu-id="d91a4-113">EXAMPLES</span></span>

### <span data-ttu-id="d91a4-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="d91a4-114">Example 1</span></span>
```powershell
PS C:\> $Incidents = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="d91a4-115">이 예제에서는 지정된  작업 영역의 모든 인시던트를 인시던트와 인시던트 $Incidents 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="d91a4-115">This example gets all of the **Incidents** in the specified workspace, and then stores it in the $Incidents variable.</span></span>

### <span data-ttu-id="d91a4-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="d91a4-116">Example 2</span></span>
```powershell
PS C:\> $Incident = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
```

<span data-ttu-id="d91a4-117">이 예제에서는  지정된 작업 영역의 인시던트 및 인시던트 $Incident 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="d91a4-117">This example gets an **Incident** in the specified workspace, and then stores it in the $Incident variable.</span></span>

## <span data-ttu-id="d91a4-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d91a4-118">PARAMETERS</span></span>

### <span data-ttu-id="d91a4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d91a4-119">-DefaultProfile</span></span>
<span data-ttu-id="d91a4-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d91a4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d91a4-121">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="d91a4-121">-IncidentId</span></span>
<span data-ttu-id="d91a4-122">인시던트 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d91a4-122">Incident Id.</span></span>

```yaml
Type: System.String
Parameter Sets: IncidentId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d91a4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d91a4-123">-ResourceGroupName</span></span>
<span data-ttu-id="d91a4-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d91a4-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d91a4-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d91a4-125">-ResourceId</span></span>
<span data-ttu-id="d91a4-126">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d91a4-126">Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d91a4-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d91a4-127">-WorkspaceName</span></span>
<span data-ttu-id="d91a4-128">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d91a4-128">Workspace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WorkspaceScope, IncidentId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d91a4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d91a4-129">CommonParameters</span></span>
<span data-ttu-id="d91a4-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d91a4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d91a4-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d91a4-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d91a4-132">입력</span><span class="sxs-lookup"><span data-stu-id="d91a4-132">INPUTS</span></span>

### <span data-ttu-id="d91a4-133">System.String</span><span class="sxs-lookup"><span data-stu-id="d91a4-133">System.String</span></span>
## <span data-ttu-id="d91a4-134">출력</span><span class="sxs-lookup"><span data-stu-id="d91a4-134">OUTPUTS</span></span>

### <span data-ttu-id="d91a4-135">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="d91a4-135">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="d91a4-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d91a4-136">NOTES</span></span>

## <span data-ttu-id="d91a4-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d91a4-137">RELATED LINKS</span></span>
