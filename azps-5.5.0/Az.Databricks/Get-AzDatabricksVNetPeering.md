---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/get-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksVNetPeering.md
ms.openlocfilehash: d5078ac91627cdf9f7b57801e3b7a958b9bd776e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208640"
---
# <span data-ttu-id="2f406-101">Get-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="2f406-101">Get-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="2f406-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f406-102">SYNOPSIS</span></span>
<span data-ttu-id="2f406-103">작업 영역 vNet 피어링을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2f406-103">Gets the workspace vNet Peering.</span></span>

## <span data-ttu-id="2f406-104">구문</span><span class="sxs-lookup"><span data-stu-id="2f406-104">SYNTAX</span></span>

### <span data-ttu-id="2f406-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="2f406-105">List (Default)</span></span>
```
Get-AzDatabricksVNetPeering -ResourceGroupName <String> -WorkspaceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2f406-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="2f406-106">Get</span></span>
```
Get-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="2f406-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2f406-107">GetViaIdentity</span></span>
```
Get-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="2f406-108">설명</span><span class="sxs-lookup"><span data-stu-id="2f406-108">DESCRIPTION</span></span>
<span data-ttu-id="2f406-109">작업 영역 vNet 피어링을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2f406-109">Gets the workspace vNet Peering.</span></span>

## <span data-ttu-id="2f406-110">예제</span><span class="sxs-lookup"><span data-stu-id="2f406-110">EXAMPLES</span></span>

### <span data-ttu-id="2f406-111">예제 1: databricks 아래에 모든 vnet 피어링 나열</span><span class="sxs-lookup"><span data-stu-id="2f406-111">Example 1: List all vnet peering under a databricks</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test

Name            Type
----            ----
vnetpeering-t01
vnetpeering-t02
```

<span data-ttu-id="2f406-112">이 명령은 databricks 아래에 모든 vnet 피어링을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="2f406-112">This command lists all vnet peering under a databricks.</span></span>

### <span data-ttu-id="2f406-113">예제 2: vnet 피어링을 얻게</span><span class="sxs-lookup"><span data-stu-id="2f406-113">Example 2: Get a vnet peering</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -ResourceGroupName lucas-manual-test -WorkspaceName databricks-test01 -PeeringName MyPeering-test01

Name             Type
----             ----
MyPeering-test01
```

<span data-ttu-id="2f406-114">이 명령은 vnet 피어링을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2f406-114">This command gets a vnet peering.</span></span>

### <span data-ttu-id="2f406-115">예제 3: 개체로 vnet 피어링을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2f406-115">Example 3: Get a vnet peering by object</span></span>
```powershell
PS C:\> New-AzDatabricksVNetPeering -Name vnetpeering-t02 -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -RemoteVirtualNetworkId '/subscriptions/xxxxx-xxxx-xxx-xxxxx/resourceGroups/azure-manual-test/providers/Microsoft.Network/virtualNetworks/vnet-test02' | Get-AzDatabricksVNetPeering

Name            Type
----            ----
vnetpeering-t02
```

<span data-ttu-id="2f406-116">이 명령은 개체에 의해 vnet 피어링을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="2f406-116">This command gets a vnet peering by object.</span></span>

## <span data-ttu-id="2f406-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2f406-117">PARAMETERS</span></span>

### <span data-ttu-id="2f406-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f406-118">-DefaultProfile</span></span>
<span data-ttu-id="2f406-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2f406-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2f406-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2f406-120">-InputObject</span></span>
<span data-ttu-id="2f406-121">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="2f406-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2f406-122">-Name</span><span class="sxs-lookup"><span data-stu-id="2f406-122">-Name</span></span>
<span data-ttu-id="2f406-123">작업 영역 vNet 피어링의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2f406-123">The name of the workspace vNet peering.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f406-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f406-124">-PassThru</span></span>
<span data-ttu-id="2f406-125">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="2f406-125">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Get, GetViaIdentity
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f406-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f406-126">-ResourceGroupName</span></span>
<span data-ttu-id="2f406-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2f406-127">The name of the resource group.</span></span>
<span data-ttu-id="2f406-128">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="2f406-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="2f406-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2f406-129">-SubscriptionId</span></span>
<span data-ttu-id="2f406-130">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2f406-130">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f406-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2f406-131">-WorkspaceName</span></span>
<span data-ttu-id="2f406-132">작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2f406-132">The name of the workspace.</span></span>

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

### <span data-ttu-id="2f406-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f406-133">CommonParameters</span></span>
<span data-ttu-id="2f406-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2f406-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f406-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2f406-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f406-136">입력</span><span class="sxs-lookup"><span data-stu-id="2f406-136">INPUTS</span></span>

### <span data-ttu-id="2f406-137">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="2f406-137">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="2f406-138">출력</span><span class="sxs-lookup"><span data-stu-id="2f406-138">OUTPUTS</span></span>

### <span data-ttu-id="2f406-139">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="2f406-139">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="2f406-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2f406-140">NOTES</span></span>

<span data-ttu-id="2f406-141">별칭</span><span class="sxs-lookup"><span data-stu-id="2f406-141">ALIASES</span></span>

<span data-ttu-id="2f406-142">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="2f406-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2f406-143">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="2f406-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2f406-144">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2f406-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2f406-145">INPUTOBJECT: <IDatabricksIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="2f406-145">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2f406-146">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="2f406-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2f406-147">`[PeeringName <String>]`: 작업 영역 vNet 피어링의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2f406-147">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="2f406-148">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2f406-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="2f406-149">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="2f406-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="2f406-150">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2f406-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="2f406-151">`[WorkspaceName <String>]`: 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2f406-151">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="2f406-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2f406-152">RELATED LINKS</span></span>

