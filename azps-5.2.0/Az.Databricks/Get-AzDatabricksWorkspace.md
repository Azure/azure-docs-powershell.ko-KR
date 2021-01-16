---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/get-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksWorkspace.md
ms.openlocfilehash: 7f2bb3f1d378afec5b0774aec2977b507654b931
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368803"
---
# <span data-ttu-id="bc328-101">Get-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="bc328-101">Get-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="bc328-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc328-102">SYNOPSIS</span></span>
<span data-ttu-id="bc328-103">작업 영역이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bc328-103">Gets the workspace.</span></span>

## <span data-ttu-id="bc328-104">구문</span><span class="sxs-lookup"><span data-stu-id="bc328-104">SYNTAX</span></span>

### <span data-ttu-id="bc328-105">List1(기본값)</span><span class="sxs-lookup"><span data-stu-id="bc328-105">List1 (Default)</span></span>
```
Get-AzDatabricksWorkspace [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bc328-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="bc328-106">Get</span></span>
```
Get-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bc328-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bc328-107">GetViaIdentity</span></span>
```
Get-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bc328-108">목록</span><span class="sxs-lookup"><span data-stu-id="bc328-108">List</span></span>
```
Get-AzDatabricksWorkspace -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="bc328-109">설명</span><span class="sxs-lookup"><span data-stu-id="bc328-109">DESCRIPTION</span></span>
<span data-ttu-id="bc328-110">작업 영역이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bc328-110">Gets the workspace.</span></span>

## <span data-ttu-id="bc328-111">예제</span><span class="sxs-lookup"><span data-stu-id="bc328-111">EXAMPLES</span></span>

### <span data-ttu-id="bc328-112">예제 1: 이름으로 Databricks 작업 영역 얻기</span><span class="sxs-lookup"><span data-stu-id="bc328-112">Example 1: Get a Databricks workspace with name</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace -Name databricks-test -ResourceGroupName testgroup

Location Name            Type
-------- ----            ----
eastus   databricks-test Microsoft.Databricks/workspaces
```

<span data-ttu-id="bc328-113">이 명령은 리소스 그룹에 Databricks 작업 영역이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bc328-113">This command gets a Databricks workspace in a resource group.</span></span>

### <span data-ttu-id="bc328-114">예제 2: 구독의 모든 Databricks 작업 영역 나열</span><span class="sxs-lookup"><span data-stu-id="bc328-114">Example 2: List all Databricks workspaces in a subscription</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace

Location Name                           Type
-------- ----                           ----
eastus   databricks-test                Microsoft.Databricks/workspaces
eastus   databricks-test-with-custom-vn Microsoft.Databricks/workspaces
```

<span data-ttu-id="bc328-115">이 명령은 구독의 모든 Databricks 작업 영역이 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="bc328-115">This command lists all Databricks workspaces in a subscription.</span></span>

### <span data-ttu-id="bc328-116">예제 3: 리소스 그룹의 모든 Databricks 작업 영역 나열</span><span class="sxs-lookup"><span data-stu-id="bc328-116">Example 3: List all Databricks workspaces in a resource group</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace -ResourceGroupName testgroup

Location Name                           Type
-------- ----                           ----
eastus   databricks-test                Microsoft.Databricks/workspaces
eastus   databricks-test-with-custom-vn Microsoft.Databricks/workspaces
```

<span data-ttu-id="bc328-117">이 명령은 리소스 그룹의 모든 Databricks 작업 영역이 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="bc328-117">This command lists all Databricks workspaces in a resource group.</span></span>

## <span data-ttu-id="bc328-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bc328-118">PARAMETERS</span></span>

### <span data-ttu-id="bc328-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc328-119">-DefaultProfile</span></span>
<span data-ttu-id="bc328-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bc328-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bc328-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bc328-121">-InputObject</span></span>
<span data-ttu-id="bc328-122">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="bc328-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="bc328-123">-Name</span><span class="sxs-lookup"><span data-stu-id="bc328-123">-Name</span></span>
<span data-ttu-id="bc328-124">작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bc328-124">The name of the workspace.</span></span>

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

### <span data-ttu-id="bc328-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc328-125">-ResourceGroupName</span></span>
<span data-ttu-id="bc328-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bc328-126">The name of the resource group.</span></span>
<span data-ttu-id="bc328-127">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="bc328-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="bc328-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bc328-128">-SubscriptionId</span></span>
<span data-ttu-id="bc328-129">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="bc328-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="bc328-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc328-130">CommonParameters</span></span>
<span data-ttu-id="bc328-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bc328-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc328-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="bc328-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc328-133">입력</span><span class="sxs-lookup"><span data-stu-id="bc328-133">INPUTS</span></span>

### <span data-ttu-id="bc328-134">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="bc328-134">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="bc328-135">출력</span><span class="sxs-lookup"><span data-stu-id="bc328-135">OUTPUTS</span></span>

### <span data-ttu-id="bc328-136">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span><span class="sxs-lookup"><span data-stu-id="bc328-136">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="bc328-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bc328-137">NOTES</span></span>

<span data-ttu-id="bc328-138">별칭</span><span class="sxs-lookup"><span data-stu-id="bc328-138">ALIASES</span></span>

<span data-ttu-id="bc328-139">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="bc328-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bc328-140">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="bc328-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bc328-141">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bc328-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bc328-142">INPUTOBJECT: <IDatabricksIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="bc328-142">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bc328-143">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="bc328-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bc328-144">`[PeeringName <String>]`: 작업 영역 vNet 피어링의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bc328-144">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="bc328-145">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bc328-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="bc328-146">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="bc328-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="bc328-147">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="bc328-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="bc328-148">`[WorkspaceName <String>]`: 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bc328-148">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="bc328-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bc328-149">RELATED LINKS</span></span>

