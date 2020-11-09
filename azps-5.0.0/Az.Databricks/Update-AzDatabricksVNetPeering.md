---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/update-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Update-AzDatabricksVNetPeering.md
ms.openlocfilehash: d53b45b67aa0843ddbdd8c5b063ff9295661a495
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305054"
---
# <span data-ttu-id="c0758-101">Update-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="c0758-101">Update-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="c0758-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0758-102">SYNOPSIS</span></span>
<span data-ttu-id="c0758-103">작업 영역에 대 한 vNet 피어 링 업데이트</span><span class="sxs-lookup"><span data-stu-id="c0758-103">Update vNet Peering for workspace.</span></span>

## <span data-ttu-id="c0758-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c0758-104">SYNTAX</span></span>

### <span data-ttu-id="c0758-105">UpdateExpanded 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="c0758-105">UpdateExpanded (Default)</span></span>
```
Update-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String>] [-AllowForwardedTraffic <Boolean>] [-AllowGatewayTransit <Boolean>]
 [-AllowVirtualNetworkAccess <Boolean>] [-UseRemoteGateway <Boolean>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c0758-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="c0758-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-AllowForwardedTraffic <Boolean>]
 [-AllowGatewayTransit <Boolean>] [-AllowVirtualNetworkAccess <Boolean>] [-UseRemoteGateway <Boolean>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c0758-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c0758-107">DESCRIPTION</span></span>
<span data-ttu-id="c0758-108">작업 영역에 대 한 vNet 피어 링 업데이트</span><span class="sxs-lookup"><span data-stu-id="c0758-108">Update vNet Peering for workspace.</span></span>

## <span data-ttu-id="c0758-109">예제의</span><span class="sxs-lookup"><span data-stu-id="c0758-109">EXAMPLES</span></span>

### <span data-ttu-id="c0758-110">예제 1: vnet 피어 링 업데이트 AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="c0758-110">Example 1: Update AllowForwardedTraffic of vnet peering</span></span>
```powershell
PS C:\> Update-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01 -AllowForwardedTraffic $True

Name            Type
----            ----
vnetpeering-t01
```

<span data-ttu-id="c0758-111">이 명령은 vnet 피어 링의 AllowForwardedTraffic를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0758-111">This command updates AllowForwardedTraffic of vnet peering.</span></span>

### <span data-ttu-id="c0758-112">예제 2: 개체에의 한 vnet 피어 링 업데이트 AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="c0758-112">Example 2: Update AllowForwardedTraffic of vnet peering by object</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -Name vnetpeering-t01 | Update-AzDatabricksVNetPeering -AllowGatewayTransit $true

Name            Type
----            ----
vnetpeering-t01

```

<span data-ttu-id="c0758-113">이 명령은 개체에의 한 vnet 피어 링의 AllowForwardedTraffic를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0758-113">This command updates AllowForwardedTraffic of vnet peering by object.</span></span>

## <span data-ttu-id="c0758-114">변수</span><span class="sxs-lookup"><span data-stu-id="c0758-114">PARAMETERS</span></span>

### <span data-ttu-id="c0758-115">-AllowForwardedTraffic</span><span class="sxs-lookup"><span data-stu-id="c0758-115">-AllowForwardedTraffic</span></span>
<span data-ttu-id="c0758-116">[System.webserver 매개 변수] 로컬 가상 네트워크의 Vm 으로부터 전달 된 트래픽이 원격 가상 네트워크에서 허용/허용 되지 않을 지 여부</span><span class="sxs-lookup"><span data-stu-id="c0758-116">[System.Management.Automation.SwitchParameter] Whether the forwarded traffic from the VMs in the local virtual network will be allowed/disallowed in remote virtual network.</span></span>

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

### <span data-ttu-id="c0758-117">-Allow게이트웨이 전송</span><span class="sxs-lookup"><span data-stu-id="c0758-117">-AllowGatewayTransit</span></span>
<span data-ttu-id="c0758-118">원격 가상 네트워킹에서 게이트웨이 링크를 사용 하 여이 가상 네트워크에 연결할 수 있는 경우 [system.webserver]. e \ 스위치 매개 변수</span><span class="sxs-lookup"><span data-stu-id="c0758-118">[System.Management.Automation.SwitchParameter] If gateway links can be used in remote virtual networking to link to this virtual network.</span></span>

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

### <span data-ttu-id="c0758-119">-AllowVirtualNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="c0758-119">-AllowVirtualNetworkAccess</span></span>
<span data-ttu-id="c0758-120">[System.webserver 매개 변수] 로컬 가상 네트워크 공간의 Vm이 원격 가상 네트워크 공간에서 Vm에 액세스할 수 있는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0758-120">[System.Management.Automation.SwitchParameter] Whether the VMs in the local virtual network space would be able to access the VMs in remote virtual network space.</span></span>

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

### <span data-ttu-id="c0758-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c0758-121">-AsJob</span></span>
<span data-ttu-id="c0758-122">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="c0758-122">Run the command as a job</span></span>

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

### <span data-ttu-id="c0758-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0758-123">-DefaultProfile</span></span>
<span data-ttu-id="c0758-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c0758-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0758-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0758-125">-InputObject</span></span>
<span data-ttu-id="c0758-126">Id 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="c0758-126">Identity parameter.</span></span>
<span data-ttu-id="c0758-127">생성 하려면 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c0758-127">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c0758-128">-이름</span><span class="sxs-lookup"><span data-stu-id="c0758-128">-Name</span></span>
<span data-ttu-id="c0758-129">VNetPeering 링의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c0758-129">The name of the VNetPeering.</span></span>

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

### <span data-ttu-id="c0758-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c0758-130">-NoWait</span></span>
<span data-ttu-id="c0758-131">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="c0758-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c0758-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0758-132">-ResourceGroupName</span></span>
<span data-ttu-id="c0758-133">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c0758-133">The name of the resource group.</span></span>
<span data-ttu-id="c0758-134">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0758-134">The name is case insensitive.</span></span>

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

### <span data-ttu-id="c0758-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c0758-135">-SubscriptionId</span></span>
<span data-ttu-id="c0758-136">대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c0758-136">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="c0758-137">-UseRemoteGateway</span><span class="sxs-lookup"><span data-stu-id="c0758-137">-UseRemoteGateway</span></span>
<span data-ttu-id="c0758-138">이 가상 네트워크에서 원격 게이트웨이를 사용할 수 있는 경우 [system.webserver] 스위치 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0758-138">[System.Management.Automation.SwitchParameter] If remote gateways can be used on this virtual network.</span></span>
<span data-ttu-id="c0758-139">플래그를 true로 설정 하 고 원격 피어 링에 대 한 Allow네트워크도 참이 면 가상 네트워크는 전송에 원격 가상 네트워크 게이트웨이를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0758-139">If the flag is set to true, and allowGatewayTransit on remote peering is also true, virtual network will use gateways of remote virtual network for transit.</span></span>
<span data-ttu-id="c0758-140">한 번만 피어 링이이 플래그를 true로 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c0758-140">Only one peering can have this flag set to true.</span></span>
<span data-ttu-id="c0758-141">가상 네트워크에 이미 게이트웨이가 있는 경우이 플래그를 설정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c0758-141">This flag cannot be set if virtual network already has a gateway.</span></span>

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

### <span data-ttu-id="c0758-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c0758-142">-WorkspaceName</span></span>
<span data-ttu-id="c0758-143">작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c0758-143">The name of the workspace.</span></span>

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

### <span data-ttu-id="c0758-144">-확인</span><span class="sxs-lookup"><span data-stu-id="c0758-144">-Confirm</span></span>
<span data-ttu-id="c0758-145">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0758-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0758-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0758-146">-WhatIf</span></span>
<span data-ttu-id="c0758-147">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c0758-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0758-148">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c0758-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0758-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0758-149">CommonParameters</span></span>
<span data-ttu-id="c0758-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0758-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0758-151">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c0758-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0758-152">입력</span><span class="sxs-lookup"><span data-stu-id="c0758-152">INPUTS</span></span>

### <span data-ttu-id="c0758-153">Databricks. IDatabricksIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="c0758-153">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="c0758-154">출력</span><span class="sxs-lookup"><span data-stu-id="c0758-154">OUTPUTS</span></span>

### <span data-ttu-id="c0758-155">Databricks. Api20180401. IVirtualNetworkPeering에 대 한</span><span class="sxs-lookup"><span data-stu-id="c0758-155">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="c0758-156">상속자</span><span class="sxs-lookup"><span data-stu-id="c0758-156">NOTES</span></span>

<span data-ttu-id="c0758-157">별칭과</span><span class="sxs-lookup"><span data-stu-id="c0758-157">ALIASES</span></span>

<span data-ttu-id="c0758-158">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="c0758-158">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c0758-159">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0758-159">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c0758-160">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="c0758-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c0758-161">INPUTOBJECT <IDatabricksIdentity> : Identity 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="c0758-161">INPUTOBJECT <IDatabricksIdentity>: Identity parameter.</span></span>
  - <span data-ttu-id="c0758-162">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="c0758-162">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c0758-163">`[PeeringName <String>]`: 작업 영역 vNet 피어 링의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c0758-163">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="c0758-164">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c0758-164">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="c0758-165">이름은 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0758-165">The name is case insensitive.</span></span>
  - <span data-ttu-id="c0758-166">`[SubscriptionId <String>]`: 대상 구독의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c0758-166">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="c0758-167">`[WorkspaceName <String>]`: 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c0758-167">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="c0758-168">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c0758-168">RELATED LINKS</span></span>

