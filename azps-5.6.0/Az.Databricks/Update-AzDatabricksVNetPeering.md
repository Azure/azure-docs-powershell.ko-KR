---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/powershell/module/az.databricks/update-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksVNetPeering.md
ms.openlocfilehash: 60d679cf8540e39d1be293a46f9e4e441e397627
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962208"
---
# <span data-ttu-id="35f8d-101">Update-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="35f8d-101">Update-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="35f8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35f8d-102">SYNOPSIS</span></span>
<span data-ttu-id="35f8d-103">작업 영역의 vNet 피어링을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="35f8d-103">Update vNet Peering for workspace.</span></span>

## <span data-ttu-id="35f8d-104">구문</span><span class="sxs-lookup"><span data-stu-id="35f8d-104">SYNTAX</span></span>

### <span data-ttu-id="35f8d-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="35f8d-105">UpdateExpanded (Default)</span></span>
```
Update-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-AllowForwardedTraffic <Boolean>] [-AllowGatewayTransit <Boolean>]
 [-AllowVirtualNetworkAccess <Boolean>] [-UseRemoteGateway <Boolean>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="35f8d-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="35f8d-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-AllowForwardedTraffic <Boolean>]
 [-AllowGatewayTransit <Boolean>] [-AllowVirtualNetworkAccess <Boolean>] [-UseRemoteGateway <Boolean>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="35f8d-107">설명</span><span class="sxs-lookup"><span data-stu-id="35f8d-107">DESCRIPTION</span></span>
<span data-ttu-id="35f8d-108">작업 영역의 vNet 피어링을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="35f8d-108">Update vNet Peering for workspace.</span></span>

## <span data-ttu-id="35f8d-109">예제</span><span class="sxs-lookup"><span data-stu-id="35f8d-109">EXAMPLES</span></span>

### <span data-ttu-id="35f8d-110">예제 1: vnet 피어링의 AllowForwardedTraffic 업데이트</span><span class="sxs-lookup"><span data-stu-id="35f8d-110">Example 1: Update AllowForwardedTraffic of vnet peering</span></span>
```powershell
PS C:\> Update-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01 -AllowForwardedTraffic $True

Name            Type
----            ----
vnetpeering-t01
```

<span data-ttu-id="35f8d-111">이 명령은 vnet 피어링의 AllowForwardedTraffic을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="35f8d-111">This command updates AllowForwardedTraffic of vnet peering.</span></span>

### <span data-ttu-id="35f8d-112">예제 2: 개체에 따라 vnet 피어링의 AllowForwardedTraffic 업데이트</span><span class="sxs-lookup"><span data-stu-id="35f8d-112">Example 2: Update AllowForwardedTraffic of vnet peering by object</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01 | Update-AzDatabricksVNetPeering -AllowGatewayTransit $true

Name            Type
----            ----
vnetpeering-t01

```

<span data-ttu-id="35f8d-113">이 명령은 개체에 따라 vnet 피어링의 AllowForwardedTraffic을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="35f8d-113">This command updates AllowForwardedTraffic of vnet peering by object.</span></span>

## <span data-ttu-id="35f8d-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="35f8d-114">PARAMETERS</span></span>

### <span data-ttu-id="35f8d-115">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="35f8d-115">-AllowForwardedTraffic</span></span>
<span data-ttu-id="35f8d-116">[System.Management.Automation.SwitchParameter] 원격 가상 네트워크에서 로컬 가상 네트워크의 VM에서 전달된 트래픽을 허용/허용하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="35f8d-116">[System.Management.Automation.SwitchParameter] Whether the forwarded traffic from the VMs in the local virtual network will be allowed/disallowed in remote virtual network.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35f8d-117">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="35f8d-117">-AllowGatewayTransit</span></span>
<span data-ttu-id="35f8d-118">[System.Management.Automation.SwitchParameter] 이 가상 네트워크에 연결하기 위해 원격 가상 네트워킹에서 게이트웨이 링크를 사용할 수 있는 경우.</span><span class="sxs-lookup"><span data-stu-id="35f8d-118">[System.Management.Automation.SwitchParameter] If gateway links can be used in remote virtual networking to link to this virtual network.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35f8d-119">-AllowVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="35f8d-119">-AllowVirtualNetworkAccess</span></span>
<span data-ttu-id="35f8d-120">[System.Management.Automation.SwitchParameter] 로컬 가상 네트워크 공간의 VM이 원격 가상 네트워크 공간에서 VM에 액세스할 수 있는지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="35f8d-120">[System.Management.Automation.SwitchParameter] Whether the VMs in the local virtual network space would be able to access the VMs in remote virtual network space.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35f8d-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35f8d-121">-AsJob</span></span>
<span data-ttu-id="35f8d-122">작업으로 명령을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="35f8d-122">Run the command as a job</span></span>

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

### <span data-ttu-id="35f8d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35f8d-123">-DefaultProfile</span></span>
<span data-ttu-id="35f8d-124">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="35f8d-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35f8d-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35f8d-125">-InputObject</span></span>
<span data-ttu-id="35f8d-126">ID 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="35f8d-126">Identity parameter.</span></span>
<span data-ttu-id="35f8d-127">생성을 위해 INPUTOBJECT 속성에 대한 노트 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="35f8d-127">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35f8d-128">-Name</span><span class="sxs-lookup"><span data-stu-id="35f8d-128">-Name</span></span>
<span data-ttu-id="35f8d-129">VNetPeering의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="35f8d-129">The name of the VNetPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: PeeringName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35f8d-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="35f8d-130">-NoWait</span></span>
<span data-ttu-id="35f8d-131">명령 비동기 실행</span><span class="sxs-lookup"><span data-stu-id="35f8d-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="35f8d-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35f8d-132">-ResourceGroupName</span></span>
<span data-ttu-id="35f8d-133">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="35f8d-133">The name of the resource group.</span></span>
<span data-ttu-id="35f8d-134">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="35f8d-134">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35f8d-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="35f8d-135">-SubscriptionId</span></span>
<span data-ttu-id="35f8d-136">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="35f8d-136">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35f8d-137">-UseRemoteGateway</span><span class="sxs-lookup"><span data-stu-id="35f8d-137">-UseRemoteGateway</span></span>
<span data-ttu-id="35f8d-138">[System.Management.Automation.SwitchParameter] 이 가상 네트워크에서 원격 게이트웨이를 사용할 수 있는 경우.</span><span class="sxs-lookup"><span data-stu-id="35f8d-138">[System.Management.Automation.SwitchParameter] If remote gateways can be used on this virtual network.</span></span>
<span data-ttu-id="35f8d-139">플래그가 true로 설정되어 있으며 원격 피어링에서 AllowGatewayTransit도 true인 경우 가상 네트워크는 전송을 위해 원격 가상 네트워크의 게이트웨이를 사용하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="35f8d-139">If the flag is set to true, and allowGatewayTransit on remote peering is also true, virtual network will use gateways of remote virtual network for transit.</span></span>
<span data-ttu-id="35f8d-140">하나의 피어링만 이 플래그를 true로 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="35f8d-140">Only one peering can have this flag set to true.</span></span>
<span data-ttu-id="35f8d-141">가상 네트워크에 게이트웨이가 이미 있는 경우 이 플래그를 설정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="35f8d-141">This flag cannot be set if virtual network already has a gateway.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35f8d-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="35f8d-142">-WorkspaceName</span></span>
<span data-ttu-id="35f8d-143">작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="35f8d-143">The name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="35f8d-144">-확인</span><span class="sxs-lookup"><span data-stu-id="35f8d-144">-Confirm</span></span>
<span data-ttu-id="35f8d-145">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="35f8d-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35f8d-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35f8d-146">-WhatIf</span></span>
<span data-ttu-id="35f8d-147">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="35f8d-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35f8d-148">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="35f8d-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35f8d-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35f8d-149">CommonParameters</span></span>
<span data-ttu-id="35f8d-150">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="35f8d-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35f8d-151">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="35f8d-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35f8d-152">입력</span><span class="sxs-lookup"><span data-stu-id="35f8d-152">INPUTS</span></span>

### <span data-ttu-id="35f8d-153">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="35f8d-153">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="35f8d-154">출력</span><span class="sxs-lookup"><span data-stu-id="35f8d-154">OUTPUTS</span></span>

### <span data-ttu-id="35f8d-155">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="35f8d-155">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="35f8d-156">참고 사항</span><span class="sxs-lookup"><span data-stu-id="35f8d-156">NOTES</span></span>

<span data-ttu-id="35f8d-157">별칭</span><span class="sxs-lookup"><span data-stu-id="35f8d-157">ALIASES</span></span>

<span data-ttu-id="35f8d-158">복잡한 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="35f8d-158">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="35f8d-159">아래에 설명된 매개 변수를 만들 경우 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="35f8d-159">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="35f8d-160">해시 테이블에 대한 자세한 내용은 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="35f8d-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="35f8d-161">INPUTOBJECT <IDatabricksIdentity> : ID 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="35f8d-161">INPUTOBJECT <IDatabricksIdentity>: Identity parameter.</span></span>
  - <span data-ttu-id="35f8d-162">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="35f8d-162">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="35f8d-163">`[PeeringName <String>]`: 작업 영역 vNet 피어링의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="35f8d-163">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="35f8d-164">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="35f8d-164">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="35f8d-165">이름은 대소문자와 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="35f8d-165">The name is case insensitive.</span></span>
  - <span data-ttu-id="35f8d-166">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="35f8d-166">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="35f8d-167">`[WorkspaceName <String>]`: 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="35f8d-167">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="35f8d-168">관련 링크</span><span class="sxs-lookup"><span data-stu-id="35f8d-168">RELATED LINKS</span></span>

