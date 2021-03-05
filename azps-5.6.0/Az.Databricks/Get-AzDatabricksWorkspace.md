---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/powershell/module/az.databricks/get-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksWorkspace.md
ms.openlocfilehash: ec44b1ace55a36ebaa56c8b0242db485581c5e10
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966464"
---
# <span data-ttu-id="86d69-101">Get-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="86d69-101">Get-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="86d69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86d69-102">SYNOPSIS</span></span>
<span data-ttu-id="86d69-103">작업 영역이 도착합니다.</span><span class="sxs-lookup"><span data-stu-id="86d69-103">Gets the workspace.</span></span>

## <span data-ttu-id="86d69-104">구문</span><span class="sxs-lookup"><span data-stu-id="86d69-104">SYNTAX</span></span>

### <span data-ttu-id="86d69-105">List1(기본값)</span><span class="sxs-lookup"><span data-stu-id="86d69-105">List1 (Default)</span></span>
```
Get-AzDatabricksWorkspace [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="86d69-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="86d69-106">Get</span></span>
```
Get-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="86d69-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="86d69-107">GetViaIdentity</span></span>
```
Get-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="86d69-108">목록</span><span class="sxs-lookup"><span data-stu-id="86d69-108">List</span></span>
```
Get-AzDatabricksWorkspace -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="86d69-109">설명</span><span class="sxs-lookup"><span data-stu-id="86d69-109">DESCRIPTION</span></span>
<span data-ttu-id="86d69-110">작업 영역이 도착합니다.</span><span class="sxs-lookup"><span data-stu-id="86d69-110">Gets the workspace.</span></span>

## <span data-ttu-id="86d69-111">예제</span><span class="sxs-lookup"><span data-stu-id="86d69-111">EXAMPLES</span></span>

### <span data-ttu-id="86d69-112">예제 1: 이름으로 Databricks 작업 영역 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="86d69-112">Example 1: Get a Databricks workspace with name</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace -Name databricks-test -ResourceGroupName testgroup

Location Name            Type
-------- ----            ----
eastus   databricks-test Microsoft.Databricks/workspaces
```

<span data-ttu-id="86d69-113">이 명령은 리소스 그룹에 Databricks 작업 영역이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="86d69-113">This command gets a Databricks workspace in a resource group.</span></span>

### <span data-ttu-id="86d69-114">예제 2: 구독의 모든 Databricks 작업 영역 나열</span><span class="sxs-lookup"><span data-stu-id="86d69-114">Example 2: List all Databricks workspaces in a subscription</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace

Location Name                           Type
-------- ----                           ----
eastus   databricks-test                Microsoft.Databricks/workspaces
eastus   databricks-test-with-custom-vn Microsoft.Databricks/workspaces
```

<span data-ttu-id="86d69-115">이 명령은 구독의 모든 Databricks 작업 영역이 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="86d69-115">This command lists all Databricks workspaces in a subscription.</span></span>

### <span data-ttu-id="86d69-116">예제 3: 리소스 그룹에 모든 Databricks 작업 영역 나열</span><span class="sxs-lookup"><span data-stu-id="86d69-116">Example 3: List all Databricks workspaces in a resource group</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace -ResourceGroupName testgroup

Location Name                           Type
-------- ----                           ----
eastus   databricks-test                Microsoft.Databricks/workspaces
eastus   databricks-test-with-custom-vn Microsoft.Databricks/workspaces
```

<span data-ttu-id="86d69-117">이 명령은 리소스 그룹의 모든 Databricks 작업 영역이 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="86d69-117">This command lists all Databricks workspaces in a resource group.</span></span>

## <span data-ttu-id="86d69-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="86d69-118">PARAMETERS</span></span>

### <span data-ttu-id="86d69-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86d69-119">-DefaultProfile</span></span>
<span data-ttu-id="86d69-120">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="86d69-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86d69-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="86d69-121">-InputObject</span></span>
<span data-ttu-id="86d69-122">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="86d69-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86d69-123">-Name</span><span class="sxs-lookup"><span data-stu-id="86d69-123">-Name</span></span>
<span data-ttu-id="86d69-124">작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="86d69-124">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: WorkspaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86d69-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86d69-125">-ResourceGroupName</span></span>
<span data-ttu-id="86d69-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="86d69-126">The name of the resource group.</span></span>
<span data-ttu-id="86d69-127">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="86d69-127">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86d69-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="86d69-128">-SubscriptionId</span></span>
<span data-ttu-id="86d69-129">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="86d69-129">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86d69-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86d69-130">CommonParameters</span></span>
<span data-ttu-id="86d69-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="86d69-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86d69-132">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="86d69-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86d69-133">입력</span><span class="sxs-lookup"><span data-stu-id="86d69-133">INPUTS</span></span>

### <span data-ttu-id="86d69-134">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="86d69-134">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="86d69-135">출력</span><span class="sxs-lookup"><span data-stu-id="86d69-135">OUTPUTS</span></span>

### <span data-ttu-id="86d69-136">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="86d69-136">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="86d69-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="86d69-137">NOTES</span></span>

<span data-ttu-id="86d69-138">별칭</span><span class="sxs-lookup"><span data-stu-id="86d69-138">ALIASES</span></span>

<span data-ttu-id="86d69-139">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="86d69-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="86d69-140">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="86d69-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="86d69-141">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="86d69-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="86d69-142">INPUTOBJECT <IDatabricksIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="86d69-142">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="86d69-143">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="86d69-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="86d69-144">`[PeeringName <String>]`: 작업 영역 vNet 피어링의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="86d69-144">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="86d69-145">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="86d69-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="86d69-146">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="86d69-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="86d69-147">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="86d69-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="86d69-148">`[WorkspaceName <String>]`: 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="86d69-148">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="86d69-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="86d69-149">RELATED LINKS</span></span>

