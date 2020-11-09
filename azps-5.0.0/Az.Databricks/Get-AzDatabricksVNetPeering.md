---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/get-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksVNetPeering.md
ms.openlocfilehash: d5078ac91627cdf9f7b57801e3b7a958b9bd776e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305096"
---
# <span data-ttu-id="92feb-101">Get-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="92feb-101">Get-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="92feb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92feb-102">SYNOPSIS</span></span>
<span data-ttu-id="92feb-103">작업 영역 vNet 피어 링을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="92feb-103">Gets the workspace vNet Peering.</span></span>

## <span data-ttu-id="92feb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="92feb-104">SYNTAX</span></span>

### <span data-ttu-id="92feb-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="92feb-105">List (Default)</span></span>
```
Get-AzDatabricksVNetPeering -ResourceGroupName <String> -WorkspaceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="92feb-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="92feb-106">Get</span></span>
```
Get-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="92feb-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="92feb-107">GetViaIdentity</span></span>
```
Get-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="92feb-108">설명은</span><span class="sxs-lookup"><span data-stu-id="92feb-108">DESCRIPTION</span></span>
<span data-ttu-id="92feb-109">작업 영역 vNet 피어 링을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="92feb-109">Gets the workspace vNet Peering.</span></span>

## <span data-ttu-id="92feb-110">예제의</span><span class="sxs-lookup"><span data-stu-id="92feb-110">EXAMPLES</span></span>

### <span data-ttu-id="92feb-111">예제 1: databricks에서 모든 vnet 피어 링 나열</span><span class="sxs-lookup"><span data-stu-id="92feb-111">Example 1: List all vnet peering under a databricks</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test

Name            Type
----            ----
vnetpeering-t01
vnetpeering-t02
```

<span data-ttu-id="92feb-112">이 명령은 databricks에 있는 모든 vnet 피어 링을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="92feb-112">This command lists all vnet peering under a databricks.</span></span>

### <span data-ttu-id="92feb-113">예제 2: vnet 피어 링 가져오기</span><span class="sxs-lookup"><span data-stu-id="92feb-113">Example 2: Get a vnet peering</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -ResourceGroupName lucas-manual-test -WorkspaceName databricks-test01 -PeeringName MyPeering-test01

Name             Type
----             ----
MyPeering-test01
```

<span data-ttu-id="92feb-114">이 명령은 vnet 피어 링을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="92feb-114">This command gets a vnet peering.</span></span>

### <span data-ttu-id="92feb-115">예제 3: 개체에의 한 vnet 피어 링 가져오기</span><span class="sxs-lookup"><span data-stu-id="92feb-115">Example 3: Get a vnet peering by object</span></span>
```powershell
PS C:\> New-AzDatabricksVNetPeering -Name vnetpeering-t02 -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -RemoteVirtualNetworkId '/subscriptions/xxxxx-xxxx-xxx-xxxxx/resourceGroups/azure-manual-test/providers/Microsoft.Network/virtualNetworks/vnet-test02' | Get-AzDatabricksVNetPeering

Name            Type
----            ----
vnetpeering-t02
```

<span data-ttu-id="92feb-116">이 명령은 개체에의 한 vnet 피어 링을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="92feb-116">This command gets a vnet peering by object.</span></span>

## <span data-ttu-id="92feb-117">변수</span><span class="sxs-lookup"><span data-stu-id="92feb-117">PARAMETERS</span></span>

### <span data-ttu-id="92feb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92feb-118">-DefaultProfile</span></span>
<span data-ttu-id="92feb-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="92feb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92feb-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="92feb-120">-InputObject</span></span>
<span data-ttu-id="92feb-121">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="92feb-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="92feb-122">-이름</span><span class="sxs-lookup"><span data-stu-id="92feb-122">-Name</span></span>
<span data-ttu-id="92feb-123">작업 영역 vNet 피어 링의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="92feb-123">The name of the workspace vNet peering.</span></span>

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

### <span data-ttu-id="92feb-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="92feb-124">-PassThru</span></span>
<span data-ttu-id="92feb-125">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="92feb-125">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="92feb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92feb-126">-ResourceGroupName</span></span>
<span data-ttu-id="92feb-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="92feb-127">The name of the resource group.</span></span>
<span data-ttu-id="92feb-128">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="92feb-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="92feb-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="92feb-129">-SubscriptionId</span></span>
<span data-ttu-id="92feb-130">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="92feb-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="92feb-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="92feb-131">-WorkspaceName</span></span>
<span data-ttu-id="92feb-132">작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="92feb-132">The name of the workspace.</span></span>

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

### <span data-ttu-id="92feb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92feb-133">CommonParameters</span></span>
<span data-ttu-id="92feb-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="92feb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92feb-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="92feb-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92feb-136">입력</span><span class="sxs-lookup"><span data-stu-id="92feb-136">INPUTS</span></span>

### <span data-ttu-id="92feb-137">Databricks. IDatabricksIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="92feb-137">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="92feb-138">출력</span><span class="sxs-lookup"><span data-stu-id="92feb-138">OUTPUTS</span></span>

### <span data-ttu-id="92feb-139">Databricks. Api20180401. IVirtualNetworkPeering에 대 한</span><span class="sxs-lookup"><span data-stu-id="92feb-139">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="92feb-140">상속자</span><span class="sxs-lookup"><span data-stu-id="92feb-140">NOTES</span></span>

<span data-ttu-id="92feb-141">별칭과</span><span class="sxs-lookup"><span data-stu-id="92feb-141">ALIASES</span></span>

<span data-ttu-id="92feb-142">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="92feb-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="92feb-143">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="92feb-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="92feb-144">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="92feb-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="92feb-145">INPUTOBJECT <IDatabricksIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="92feb-145">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="92feb-146">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="92feb-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="92feb-147">`[PeeringName <String>]`: 작업 영역 vNet 피어 링의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="92feb-147">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="92feb-148">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="92feb-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="92feb-149">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="92feb-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="92feb-150">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="92feb-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="92feb-151">`[WorkspaceName <String>]`: 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="92feb-151">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="92feb-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="92feb-152">RELATED LINKS</span></span>

