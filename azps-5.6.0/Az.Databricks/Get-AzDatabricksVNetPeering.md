---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/powershell/module/az.databricks/get-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksVNetPeering.md
ms.openlocfilehash: a5654fa0974accf4319df4cbbd08ef220fa7ad9e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966475"
---
# <span data-ttu-id="ca2e9-101">Get-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="ca2e9-101">Get-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="ca2e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca2e9-102">SYNOPSIS</span></span>
<span data-ttu-id="ca2e9-103">작업 영역 vNet 피어링을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ca2e9-103">Gets the workspace vNet Peering.</span></span>

## <span data-ttu-id="ca2e9-104">구문</span><span class="sxs-lookup"><span data-stu-id="ca2e9-104">SYNTAX</span></span>

### <span data-ttu-id="ca2e9-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="ca2e9-105">List (Default)</span></span>
```
Get-AzDatabricksVNetPeering -ResourceGroupName <String> -WorkspaceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ca2e9-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="ca2e9-106">Get</span></span>
```
Get-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="ca2e9-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ca2e9-107">GetViaIdentity</span></span>
```
Get-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="ca2e9-108">설명</span><span class="sxs-lookup"><span data-stu-id="ca2e9-108">DESCRIPTION</span></span>
<span data-ttu-id="ca2e9-109">작업 영역 vNet 피어링을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ca2e9-109">Gets the workspace vNet Peering.</span></span>

## <span data-ttu-id="ca2e9-110">예제</span><span class="sxs-lookup"><span data-stu-id="ca2e9-110">EXAMPLES</span></span>

### <span data-ttu-id="ca2e9-111">예제 1: 데이터 브릭 아래에 모든 vnet 피어링 나열</span><span class="sxs-lookup"><span data-stu-id="ca2e9-111">Example 1: List all vnet peering under a databricks</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test

Name            Type
----            ----
vnetpeering-t01
vnetpeering-t02
```

<span data-ttu-id="ca2e9-112">이 명령은 데이터 브릭 아래에 모든 vnet 피어링을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="ca2e9-112">This command lists all vnet peering under a databricks.</span></span>

### <span data-ttu-id="ca2e9-113">예제 2: vnet 피어링하기</span><span class="sxs-lookup"><span data-stu-id="ca2e9-113">Example 2: Get a vnet peering</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -ResourceGroupName lucas-manual-test -WorkspaceName databricks-test01 -PeeringName MyPeering-test01

Name             Type
----             ----
MyPeering-test01
```

<span data-ttu-id="ca2e9-114">이 명령은 vnet 피어링을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ca2e9-114">This command gets a vnet peering.</span></span>

### <span data-ttu-id="ca2e9-115">예제 3: 개체에 따라 vnet 피어링을 얻다</span><span class="sxs-lookup"><span data-stu-id="ca2e9-115">Example 3: Get a vnet peering by object</span></span>
```powershell
PS C:\> New-AzDatabricksVNetPeering -Name vnetpeering-t02 -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -RemoteVirtualNetworkId '/subscriptions/xxxxx-xxxx-xxx-xxxxx/resourceGroups/azure-manual-test/providers/Microsoft.Network/virtualNetworks/vnet-test02' | Get-AzDatabricksVNetPeering

Name            Type
----            ----
vnetpeering-t02
```

<span data-ttu-id="ca2e9-116">이 명령은 개체에 따라 vnet 피어링을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ca2e9-116">This command gets a vnet peering by object.</span></span>

## <span data-ttu-id="ca2e9-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ca2e9-117">PARAMETERS</span></span>

### <span data-ttu-id="ca2e9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca2e9-118">-DefaultProfile</span></span>
<span data-ttu-id="ca2e9-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ca2e9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca2e9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ca2e9-120">-InputObject</span></span>
<span data-ttu-id="ca2e9-121">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="ca2e9-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ca2e9-122">-Name</span><span class="sxs-lookup"><span data-stu-id="ca2e9-122">-Name</span></span>
<span data-ttu-id="ca2e9-123">작업 영역 vNet 피어링의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ca2e9-123">The name of the workspace vNet peering.</span></span>

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

### <span data-ttu-id="ca2e9-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ca2e9-124">-PassThru</span></span>
<span data-ttu-id="ca2e9-125">명령이 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="ca2e9-125">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ca2e9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca2e9-126">-ResourceGroupName</span></span>
<span data-ttu-id="ca2e9-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ca2e9-127">The name of the resource group.</span></span>
<span data-ttu-id="ca2e9-128">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="ca2e9-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="ca2e9-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ca2e9-129">-SubscriptionId</span></span>
<span data-ttu-id="ca2e9-130">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ca2e9-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="ca2e9-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ca2e9-131">-WorkspaceName</span></span>
<span data-ttu-id="ca2e9-132">작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ca2e9-132">The name of the workspace.</span></span>

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

### <span data-ttu-id="ca2e9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca2e9-133">CommonParameters</span></span>
<span data-ttu-id="ca2e9-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ca2e9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca2e9-135">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ca2e9-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca2e9-136">입력</span><span class="sxs-lookup"><span data-stu-id="ca2e9-136">INPUTS</span></span>

### <span data-ttu-id="ca2e9-137">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="ca2e9-137">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="ca2e9-138">출력</span><span class="sxs-lookup"><span data-stu-id="ca2e9-138">OUTPUTS</span></span>

### <span data-ttu-id="ca2e9-139">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="ca2e9-139">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="ca2e9-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ca2e9-140">NOTES</span></span>

<span data-ttu-id="ca2e9-141">별칭</span><span class="sxs-lookup"><span data-stu-id="ca2e9-141">ALIASES</span></span>

<span data-ttu-id="ca2e9-142">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="ca2e9-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ca2e9-143">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="ca2e9-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ca2e9-144">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ca2e9-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ca2e9-145">INPUTOBJECT <IDatabricksIdentity> : ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="ca2e9-145">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ca2e9-146">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="ca2e9-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ca2e9-147">`[PeeringName <String>]`: 작업 영역 vNet 피어링의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ca2e9-147">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="ca2e9-148">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ca2e9-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="ca2e9-149">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="ca2e9-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="ca2e9-150">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ca2e9-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="ca2e9-151">`[WorkspaceName <String>]`: 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ca2e9-151">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="ca2e9-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ca2e9-152">RELATED LINKS</span></span>

