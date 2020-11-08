---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/get-azdatabricksworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksWorkspace.md
ms.openlocfilehash: 7f2bb3f1d378afec5b0774aec2977b507654b931
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212277"
---
# <span data-ttu-id="b3df8-101">Get-AzDatabricksWorkspace</span><span class="sxs-lookup"><span data-stu-id="b3df8-101">Get-AzDatabricksWorkspace</span></span>

## <span data-ttu-id="b3df8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3df8-102">SYNOPSIS</span></span>
<span data-ttu-id="b3df8-103">작업 영역을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b3df8-103">Gets the workspace.</span></span>

## <span data-ttu-id="b3df8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b3df8-104">SYNTAX</span></span>

### <span data-ttu-id="b3df8-105">List1 (기본값)</span><span class="sxs-lookup"><span data-stu-id="b3df8-105">List1 (Default)</span></span>
```
Get-AzDatabricksWorkspace [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b3df8-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="b3df8-106">Get</span></span>
```
Get-AzDatabricksWorkspace -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b3df8-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b3df8-107">GetViaIdentity</span></span>
```
Get-AzDatabricksWorkspace -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b3df8-108">목록</span><span class="sxs-lookup"><span data-stu-id="b3df8-108">List</span></span>
```
Get-AzDatabricksWorkspace -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b3df8-109">설명은</span><span class="sxs-lookup"><span data-stu-id="b3df8-109">DESCRIPTION</span></span>
<span data-ttu-id="b3df8-110">작업 영역을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b3df8-110">Gets the workspace.</span></span>

## <span data-ttu-id="b3df8-111">예제의</span><span class="sxs-lookup"><span data-stu-id="b3df8-111">EXAMPLES</span></span>

### <span data-ttu-id="b3df8-112">예제 1: 이름을 사용 하 여 Databricks 작업 영역 가져오기</span><span class="sxs-lookup"><span data-stu-id="b3df8-112">Example 1: Get a Databricks workspace with name</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace -Name databricks-test -ResourceGroupName testgroup

Location Name            Type
-------- ----            ----
eastus   databricks-test Microsoft.Databricks/workspaces
```

<span data-ttu-id="b3df8-113">이 명령은 리소스 그룹에서 Databricks 작업 영역을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b3df8-113">This command gets a Databricks workspace in a resource group.</span></span>

### <span data-ttu-id="b3df8-114">예제 2: 구독에서 모든 Databricks 작업 영역 나열</span><span class="sxs-lookup"><span data-stu-id="b3df8-114">Example 2: List all Databricks workspaces in a subscription</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace

Location Name                           Type
-------- ----                           ----
eastus   databricks-test                Microsoft.Databricks/workspaces
eastus   databricks-test-with-custom-vn Microsoft.Databricks/workspaces
```

<span data-ttu-id="b3df8-115">이 명령은 구독에 모든 Databricks 작업 영역을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3df8-115">This command lists all Databricks workspaces in a subscription.</span></span>

### <span data-ttu-id="b3df8-116">예제 3: 리소스 그룹의 모든 Databricks 작업 영역 나열</span><span class="sxs-lookup"><span data-stu-id="b3df8-116">Example 3: List all Databricks workspaces in a resource group</span></span>
```powershell
PS C:\> Get-AzDatabricksWorkspace -ResourceGroupName testgroup

Location Name                           Type
-------- ----                           ----
eastus   databricks-test                Microsoft.Databricks/workspaces
eastus   databricks-test-with-custom-vn Microsoft.Databricks/workspaces
```

<span data-ttu-id="b3df8-117">이 명령은 리소스 그룹에 모든 Databricks 작업 영역을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3df8-117">This command lists all Databricks workspaces in a resource group.</span></span>

## <span data-ttu-id="b3df8-118">변수</span><span class="sxs-lookup"><span data-stu-id="b3df8-118">PARAMETERS</span></span>

### <span data-ttu-id="b3df8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3df8-119">-DefaultProfile</span></span>
<span data-ttu-id="b3df8-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b3df8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3df8-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b3df8-121">-InputObject</span></span>
<span data-ttu-id="b3df8-122">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b3df8-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b3df8-123">-이름</span><span class="sxs-lookup"><span data-stu-id="b3df8-123">-Name</span></span>
<span data-ttu-id="b3df8-124">작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b3df8-124">The name of the workspace.</span></span>

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

### <span data-ttu-id="b3df8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3df8-125">-ResourceGroupName</span></span>
<span data-ttu-id="b3df8-126">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b3df8-126">The name of the resource group.</span></span>
<span data-ttu-id="b3df8-127">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3df8-127">The name is case insensitive.</span></span>

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

### <span data-ttu-id="b3df8-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b3df8-128">-SubscriptionId</span></span>
<span data-ttu-id="b3df8-129">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b3df8-129">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="b3df8-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3df8-130">CommonParameters</span></span>
<span data-ttu-id="b3df8-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3df8-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3df8-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b3df8-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3df8-133">입력</span><span class="sxs-lookup"><span data-stu-id="b3df8-133">INPUTS</span></span>

### <span data-ttu-id="b3df8-134">Databricks. IDatabricksIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="b3df8-134">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="b3df8-135">출력</span><span class="sxs-lookup"><span data-stu-id="b3df8-135">OUTPUTS</span></span>

### <span data-ttu-id="b3df8-136">Databricks. Api20180401에 대 한 작업 영역</span><span class="sxs-lookup"><span data-stu-id="b3df8-136">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IWorkspace</span></span>

## <span data-ttu-id="b3df8-137">상속자</span><span class="sxs-lookup"><span data-stu-id="b3df8-137">NOTES</span></span>

<span data-ttu-id="b3df8-138">별칭과</span><span class="sxs-lookup"><span data-stu-id="b3df8-138">ALIASES</span></span>

<span data-ttu-id="b3df8-139">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="b3df8-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b3df8-140">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3df8-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b3df8-141">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="b3df8-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b3df8-142">INPUTOBJECT <IDatabricksIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="b3df8-142">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b3df8-143">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="b3df8-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b3df8-144">`[PeeringName <String>]`: 작업 영역 vNet 피어 링의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b3df8-144">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="b3df8-145">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b3df8-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="b3df8-146">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="b3df8-146">The name is case insensitive.</span></span>
  - <span data-ttu-id="b3df8-147">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b3df8-147">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="b3df8-148">`[WorkspaceName <String>]`: 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b3df8-148">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="b3df8-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b3df8-149">RELATED LINKS</span></span>

