---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SecurityInsights.dll-Help.xml
Module Name: Az.SecurityInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.securityinsights/get-azsentinelincident
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncident.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SecurityInsights/SecurityInsights/help/Get-AzSentinelIncident.md
ms.openlocfilehash: eb0854ee3a71af3bdf19d2258187c435fb0f5860
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183537"
---
# <span data-ttu-id="c4b06-101">Get-AzSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="c4b06-101">Get-AzSentinelIncident</span></span>

## <span data-ttu-id="c4b06-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4b06-102">SYNOPSIS</span></span>
<span data-ttu-id="c4b06-103">인시던트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c4b06-103">Get an Incident.</span></span>

## <span data-ttu-id="c4b06-104">구문</span><span class="sxs-lookup"><span data-stu-id="c4b06-104">SYNTAX</span></span>

### <span data-ttu-id="c4b06-105">WorkspaceScope(기본값)</span><span class="sxs-lookup"><span data-stu-id="c4b06-105">WorkspaceScope (Default)</span></span>
```
Get-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4b06-106">IncidentId</span><span class="sxs-lookup"><span data-stu-id="c4b06-106">IncidentId</span></span>
```
Get-AzSentinelIncident -ResourceGroupName <String> -WorkspaceName <String> [-IncidentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c4b06-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4b06-107">ResourceId</span></span>
```
Get-AzSentinelIncident -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c4b06-108">설명</span><span class="sxs-lookup"><span data-stu-id="c4b06-108">DESCRIPTION</span></span>
<span data-ttu-id="c4b06-109">**Get-AzSentinelIncident** cmdlet은 지정된 작업 영역의 인시던트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c4b06-109">The **Get-AzSentinelIncident** cmdlet gets an Incident from the specified workspace.</span></span>
<span data-ttu-id="c4b06-110">IncidentId 매개 변수를 *지정하면* 단일 **Incident** 개체가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="c4b06-110">If you specify the *IncidentId* parameter, a single **Incident** object is returned.</span></span>
<span data-ttu-id="c4b06-111">*IncidentId* 매개 변수를 지정하지 않으면 지정된 작업 영역의 모든 인시던트가 포함된 배열이 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="c4b06-111">If you do not specify the *IncidentId* parameter, an array containing all of the Incidents in the specified workspace are returned.</span></span>
<span data-ttu-id="c4b06-112">인시던트  개체를 사용하여 인시던트 업데이트를 할 수 있습니다. 예를 들어 인시던트 메모를 추가할 수 **있습니다.**</span><span class="sxs-lookup"><span data-stu-id="c4b06-112">You can use the **Incident** object to update the Incident, for example you can add Notes the **Incident**.</span></span>

## <span data-ttu-id="c4b06-113">예제</span><span class="sxs-lookup"><span data-stu-id="c4b06-113">EXAMPLES</span></span>

### <span data-ttu-id="c4b06-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="c4b06-114">Example 1</span></span>
```powershell
PS C:\> $Incidents = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName"
```

<span data-ttu-id="c4b06-115">이 예제에서는 지정된  작업 영역의 모든 인시던트를 인시던트와 인시던트 $Incidents 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="c4b06-115">This example gets all of the **Incidents** in the specified workspace, and then stores it in the $Incidents variable.</span></span>

### <span data-ttu-id="c4b06-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="c4b06-116">Example 2</span></span>
```powershell
PS C:\> $Incident = Get-AzSentinelIncident -ResourceGroupName "MyResourceGroup" -WorkspaceName "MyWorkspaceName" -IncidentId "MyIncidentId"
```

<span data-ttu-id="c4b06-117">이 예제에서는  지정된 작업 영역의 인시던트 및 인시던트 $Incident 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="c4b06-117">This example gets an **Incident** in the specified workspace, and then stores it in the $Incident variable.</span></span>

## <span data-ttu-id="c4b06-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4b06-118">PARAMETERS</span></span>

### <span data-ttu-id="c4b06-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4b06-119">-DefaultProfile</span></span>
<span data-ttu-id="c4b06-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c4b06-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4b06-121">-IncidentId</span><span class="sxs-lookup"><span data-stu-id="c4b06-121">-IncidentId</span></span>
<span data-ttu-id="c4b06-122">인시던트 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c4b06-122">Incident Id.</span></span>

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

### <span data-ttu-id="c4b06-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4b06-123">-ResourceGroupName</span></span>
<span data-ttu-id="c4b06-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c4b06-124">Resource group name.</span></span>

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

### <span data-ttu-id="c4b06-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c4b06-125">-ResourceId</span></span>
<span data-ttu-id="c4b06-126">리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c4b06-126">Resource Id.</span></span>

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

### <span data-ttu-id="c4b06-127">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c4b06-127">-WorkspaceName</span></span>
<span data-ttu-id="c4b06-128">작업 영역 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c4b06-128">Workspace Name.</span></span>

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

### <span data-ttu-id="c4b06-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4b06-129">CommonParameters</span></span>
<span data-ttu-id="c4b06-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c4b06-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4b06-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c4b06-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4b06-132">입력</span><span class="sxs-lookup"><span data-stu-id="c4b06-132">INPUTS</span></span>

### <span data-ttu-id="c4b06-133">System.String</span><span class="sxs-lookup"><span data-stu-id="c4b06-133">System.String</span></span>
## <span data-ttu-id="c4b06-134">출력</span><span class="sxs-lookup"><span data-stu-id="c4b06-134">OUTPUTS</span></span>

### <span data-ttu-id="c4b06-135">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span><span class="sxs-lookup"><span data-stu-id="c4b06-135">Microsoft.Azure.Commands.SecurityInsights.Models.Incidents.PSSentinelIncident</span></span>
## <span data-ttu-id="c4b06-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c4b06-136">NOTES</span></span>

## <span data-ttu-id="c4b06-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c4b06-137">RELATED LINKS</span></span>
