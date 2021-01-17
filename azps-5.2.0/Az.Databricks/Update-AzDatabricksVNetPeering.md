---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/update-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksVNetPeering.md
ms.openlocfilehash: d53b45b67aa0843ddbdd8c5b063ff9295661a495
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98362237"
---
# <span data-ttu-id="5aa45-101">Update-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="5aa45-101">Update-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="5aa45-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5aa45-102">SYNOPSIS</span></span>
<span data-ttu-id="5aa45-103">작업 영역의 vNet 피어링을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5aa45-103">Update vNet Peering for workspace.</span></span>

## <span data-ttu-id="5aa45-104">구문</span><span class="sxs-lookup"><span data-stu-id="5aa45-104">SYNTAX</span></span>

### <span data-ttu-id="5aa45-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="5aa45-105">UpdateExpanded (Default)</span></span>
```
Update-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-AllowForwardedTraffic <Boolean>] [-AllowGatewayTransit <Boolean>]
 [-AllowVirtualNetworkAccess <Boolean>] [-UseRemoteGateway <Boolean>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5aa45-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="5aa45-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-AllowForwardedTraffic <Boolean>]
 [-AllowGatewayTransit <Boolean>] [-AllowVirtualNetworkAccess <Boolean>] [-UseRemoteGateway <Boolean>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5aa45-107">설명</span><span class="sxs-lookup"><span data-stu-id="5aa45-107">DESCRIPTION</span></span>
<span data-ttu-id="5aa45-108">작업 영역의 vNet 피어링을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5aa45-108">Update vNet Peering for workspace.</span></span>

## <span data-ttu-id="5aa45-109">예제</span><span class="sxs-lookup"><span data-stu-id="5aa45-109">EXAMPLES</span></span>

### <span data-ttu-id="5aa45-110">예제 1: vnet 피어링의 AllowForwardedTraffic 업데이트</span><span class="sxs-lookup"><span data-stu-id="5aa45-110">Example 1: Update AllowForwardedTraffic of vnet peering</span></span>
```powershell
PS C:\> Update-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01 -AllowForwardedTraffic $True

Name            Type
----            ----
vnetpeering-t01
```

<span data-ttu-id="5aa45-111">이 명령은 vnet 피어링의 AllowForwardedTraffic을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5aa45-111">This command updates AllowForwardedTraffic of vnet peering.</span></span>

### <span data-ttu-id="5aa45-112">예제 2: 개체에 따라 vnet 피어링의 AllowForwardedTraffic 업데이트</span><span class="sxs-lookup"><span data-stu-id="5aa45-112">Example 2: Update AllowForwardedTraffic of vnet peering by object</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01 | Update-AzDatabricksVNetPeering -AllowGatewayTransit $true

Name            Type
----            ----
vnetpeering-t01

```

<span data-ttu-id="5aa45-113">이 명령은 개체에 의해 vnet 피어링의 AllowForwardedTraffic을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="5aa45-113">This command updates AllowForwardedTraffic of vnet peering by object.</span></span>

## <span data-ttu-id="5aa45-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5aa45-114">PARAMETERS</span></span>

### <span data-ttu-id="5aa45-115">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="5aa45-115">-AllowForwardedTraffic</span></span>
<span data-ttu-id="5aa45-116">[System.Management.Automation.SwitchParameter] 로컬 가상 네트워크의 VM에서 전달된 트래픽이 원격 가상 네트워크에서 허용/허용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5aa45-116">[System.Management.Automation.SwitchParameter] Whether the forwarded traffic from the VMs in the local virtual network will be allowed/disallowed in remote virtual network.</span></span>

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

### <span data-ttu-id="5aa45-117">-AllowGatewayTransit</span><span class="sxs-lookup"><span data-stu-id="5aa45-117">-AllowGatewayTransit</span></span>
<span data-ttu-id="5aa45-118">[System.Management.Automation.SwitchParameter] 게이트웨이 링크를 원격 가상 네트워킹에서 사용하여 이 가상 네트워크에 연결하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5aa45-118">[System.Management.Automation.SwitchParameter] If gateway links can be used in remote virtual networking to link to this virtual network.</span></span>

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

### <span data-ttu-id="5aa45-119">-AllowVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="5aa45-119">-AllowVirtualNetworkAccess</span></span>
<span data-ttu-id="5aa45-120">[System.Management.Automation.SwitchParameter] 로컬 가상 네트워크 공간의 VM이 원격 가상 네트워크 공간의 VM에 액세스할 수 있는지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="5aa45-120">[System.Management.Automation.SwitchParameter] Whether the VMs in the local virtual network space would be able to access the VMs in remote virtual network space.</span></span>

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

### <span data-ttu-id="5aa45-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5aa45-121">-AsJob</span></span>
<span data-ttu-id="5aa45-122">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="5aa45-122">Run the command as a job</span></span>

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

### <span data-ttu-id="5aa45-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5aa45-123">-DefaultProfile</span></span>
<span data-ttu-id="5aa45-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5aa45-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5aa45-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5aa45-125">-InputObject</span></span>
<span data-ttu-id="5aa45-126">ID 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="5aa45-126">Identity parameter.</span></span>
<span data-ttu-id="5aa45-127">생성을 위해 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="5aa45-127">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5aa45-128">-Name</span><span class="sxs-lookup"><span data-stu-id="5aa45-128">-Name</span></span>
<span data-ttu-id="5aa45-129">VNetPeering의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5aa45-129">The name of the VNetPeering.</span></span>

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

### <span data-ttu-id="5aa45-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5aa45-130">-NoWait</span></span>
<span data-ttu-id="5aa45-131">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="5aa45-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5aa45-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5aa45-132">-ResourceGroupName</span></span>
<span data-ttu-id="5aa45-133">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5aa45-133">The name of the resource group.</span></span>
<span data-ttu-id="5aa45-134">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="5aa45-134">The name is case insensitive.</span></span>

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

### <span data-ttu-id="5aa45-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5aa45-135">-SubscriptionId</span></span>
<span data-ttu-id="5aa45-136">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5aa45-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="5aa45-137">-UseRemoteGateway</span><span class="sxs-lookup"><span data-stu-id="5aa45-137">-UseRemoteGateway</span></span>
<span data-ttu-id="5aa45-138">[System.Management.Automation.SwitchParameter] 이 가상 네트워크에서 원격 게이트웨이를 사용할 수 있는 경우</span><span class="sxs-lookup"><span data-stu-id="5aa45-138">[System.Management.Automation.SwitchParameter] If remote gateways can be used on this virtual network.</span></span>
<span data-ttu-id="5aa45-139">플래그가 true로 설정되어 있으며 원격 피어링의 allowGatewayTransit도 true이면 가상 네트워크는 전송을 위해 원격 가상 네트워크의 게이트웨이를 사용하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5aa45-139">If the flag is set to true, and allowGatewayTransit on remote peering is also true, virtual network will use gateways of remote virtual network for transit.</span></span>
<span data-ttu-id="5aa45-140">한 피어링만 이 플래그를 true로 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5aa45-140">Only one peering can have this flag set to true.</span></span>
<span data-ttu-id="5aa45-141">가상 네트워크에 게이트웨이가 이미 있는 경우 이 플래그를 설정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="5aa45-141">This flag cannot be set if virtual network already has a gateway.</span></span>

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

### <span data-ttu-id="5aa45-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5aa45-142">-WorkspaceName</span></span>
<span data-ttu-id="5aa45-143">작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5aa45-143">The name of the workspace.</span></span>

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

### <span data-ttu-id="5aa45-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5aa45-144">-Confirm</span></span>
<span data-ttu-id="5aa45-145">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5aa45-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5aa45-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5aa45-146">-WhatIf</span></span>
<span data-ttu-id="5aa45-147">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5aa45-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5aa45-148">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5aa45-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5aa45-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5aa45-149">CommonParameters</span></span>
<span data-ttu-id="5aa45-150">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5aa45-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5aa45-151">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5aa45-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5aa45-152">입력</span><span class="sxs-lookup"><span data-stu-id="5aa45-152">INPUTS</span></span>

### <span data-ttu-id="5aa45-153">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="5aa45-153">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="5aa45-154">출력</span><span class="sxs-lookup"><span data-stu-id="5aa45-154">OUTPUTS</span></span>

### <span data-ttu-id="5aa45-155">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="5aa45-155">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="5aa45-156">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5aa45-156">NOTES</span></span>

<span data-ttu-id="5aa45-157">별칭</span><span class="sxs-lookup"><span data-stu-id="5aa45-157">ALIASES</span></span>

<span data-ttu-id="5aa45-158">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="5aa45-158">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5aa45-159">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="5aa45-159">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5aa45-160">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5aa45-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5aa45-161">INPUTOBJECT: <IDatabricksIdentity> ID 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="5aa45-161">INPUTOBJECT <IDatabricksIdentity>: Identity parameter.</span></span>
  - <span data-ttu-id="5aa45-162">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="5aa45-162">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5aa45-163">`[PeeringName <String>]`: 작업 영역 vNet 피어링의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5aa45-163">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="5aa45-164">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5aa45-164">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="5aa45-165">이름은 대소문자 무관합니다.</span><span class="sxs-lookup"><span data-stu-id="5aa45-165">The name is case insensitive.</span></span>
  - <span data-ttu-id="5aa45-166">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5aa45-166">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="5aa45-167">`[WorkspaceName <String>]`: 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5aa45-167">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="5aa45-168">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5aa45-168">RELATED LINKS</span></span>

