---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.fabric.admin/add-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: fe7726c25ee9dd83ca940b4ac6e47b3cc26a6457
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94046713"
---
# <span data-ttu-id="e1118-101">Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="e1118-101">Add-AzsScaleUnitNode</span></span>

## <span data-ttu-id="e1118-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1118-102">SYNOPSIS</span></span>
<span data-ttu-id="e1118-103">배율 단위를 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1118-103">Scales out a scale unit.</span></span>

## <span data-ttu-id="e1118-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e1118-104">SYNTAX</span></span>

### <span data-ttu-id="e1118-105">ScaleExpanded (기본값)</span><span class="sxs-lookup"><span data-stu-id="e1118-105">ScaleExpanded (Default)</span></span>
```
Add-AzsScaleUnitNode -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-AwaitStorageConvergence] [-BmciPv4Address <String>] [-ComputerName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e1118-106">크기가</span><span class="sxs-lookup"><span data-stu-id="e1118-106">Scale</span></span>
```
Add-AzsScaleUnitNode -ScaleUnit <String> -ScaleUnitNodeParameter <IScaleOutScaleUnitParametersList>
 [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e1118-107">ScaleViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e1118-107">ScaleViaIdentity</span></span>
```
Add-AzsScaleUnitNode -InputObject <IFabricAdminIdentity>
 -ScaleUnitNodeParameter <IScaleOutScaleUnitParametersList> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="e1118-108">ScaleViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="e1118-108">ScaleViaIdentityExpanded</span></span>
```
Add-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-AwaitStorageConvergence]
 [-BmciPv4Address <String>] [-ComputerName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e1118-109">설명은</span><span class="sxs-lookup"><span data-stu-id="e1118-109">DESCRIPTION</span></span>
<span data-ttu-id="e1118-110">배율 단위를 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1118-110">Scales out a scale unit.</span></span>

## <span data-ttu-id="e1118-111">예제의</span><span class="sxs-lookup"><span data-stu-id="e1118-111">EXAMPLES</span></span>

### <span data-ttu-id="e1118-112">예제 1: Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="e1118-112">Example 1: Add-AzsScaleUnitNode</span></span>
```powershell
PS C:\> Add-AzsScaleUnitNode -BmciPv4Address $BmciPv4Address -ComputerName $ComputerName -ScaleUnit $ScaleUnitName

Adds a list of nodes to the scale unit.
```

<span data-ttu-id="e1118-113">확장 단위 클러스터에 새 배율 단위 노드를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1118-113">Add a new scale unit node to your scale unit cluster.</span></span>

## <span data-ttu-id="e1118-114">변수</span><span class="sxs-lookup"><span data-stu-id="e1118-114">PARAMETERS</span></span>

### <span data-ttu-id="e1118-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e1118-115">-AsJob</span></span>
<span data-ttu-id="e1118-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="e1118-116">Run the command as a job</span></span>

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

### <span data-ttu-id="e1118-117">-AwaitStorageConvergence</span><span class="sxs-lookup"><span data-stu-id="e1118-117">-AwaitStorageConvergence</span></span>
<span data-ttu-id="e1118-118">플래그는 작업이 반환 되기 전에 저장소가 수렴 될 때까지 대기 해야 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e1118-118">Flag indicates if the operation should wait for storage to converge before returning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ScaleExpanded, ScaleViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e1118-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1118-119">-DefaultProfile</span></span>
<span data-ttu-id="e1118-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e1118-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1118-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e1118-121">-InputObject</span></span>
<span data-ttu-id="e1118-122">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e1118-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: ScaleViaIdentity, ScaleViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="e1118-123">-위치</span><span class="sxs-lookup"><span data-stu-id="e1118-123">-Location</span></span>
<span data-ttu-id="e1118-124">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="e1118-124">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Scale, ScaleExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e1118-125">-BmciPv4Address</span><span class="sxs-lookup"><span data-stu-id="e1118-125">-BmciPv4Address</span></span> 
<span data-ttu-id="e1118-126">물리적 컴퓨터의 BMC 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="e1118-126">BMC address of the physical machine.</span></span>

### <span data-ttu-id="e1118-127">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="e1118-127">-ComputerName</span></span> 
<span data-ttu-id="e1118-128">물리적 컴퓨터의 컴퓨터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e1118-128">Computer name of the physical machine.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IScaleOutScaleUnitParameters[]
Parameter Sets: ScaleExpanded, ScaleViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e1118-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e1118-129">-NoWait</span></span>
<span data-ttu-id="e1118-130">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="e1118-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e1118-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e1118-131">-PassThru</span></span>
<span data-ttu-id="e1118-132">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1118-132">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e1118-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1118-133">-ResourceGroupName</span></span>
<span data-ttu-id="e1118-134">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e1118-134">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Scale, ScaleExpanded
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e1118-135">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="e1118-135">-ScaleUnit</span></span>
<span data-ttu-id="e1118-136">눈금 단위의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e1118-136">Name of the scale units.</span></span>

```yaml
Type: System.String
Parameter Sets: Scale, ScaleExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e1118-137">-ScaleUnitNodeParameter</span><span class="sxs-lookup"><span data-stu-id="e1118-137">-ScaleUnitNodeParameter</span></span>
<span data-ttu-id="e1118-138">배율 단위 노드 집합을 추가 하는 데 사용할 수 있는 입력 데이터 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="e1118-138">A list of input data that allows for adding a set of scale unit nodes.</span></span>
<span data-ttu-id="e1118-139">생성 하려면 SCALEUNITNODEPARAMETER 속성에 대 한 메모 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e1118-139">To construct, see NOTES section for SCALEUNITNODEPARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IScaleOutScaleUnitParametersList
Parameter Sets: Scale, ScaleViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="e1118-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e1118-140">-SubscriptionId</span></span>
<span data-ttu-id="e1118-141">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="e1118-141">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e1118-142">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1118-142">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Scale, ScaleExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e1118-143">-확인</span><span class="sxs-lookup"><span data-stu-id="e1118-143">-Confirm</span></span>
<span data-ttu-id="e1118-144">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1118-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1118-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1118-145">-WhatIf</span></span>
<span data-ttu-id="e1118-146">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e1118-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1118-147">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e1118-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1118-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1118-148">CommonParameters</span></span>
<span data-ttu-id="e1118-149">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1118-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1118-150">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e1118-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1118-151">입력</span><span class="sxs-lookup"><span data-stu-id="e1118-151">INPUTS</span></span>

### <span data-ttu-id="e1118-152">FabricAdmin. Api20160501. IScaleOutScaleUnitParametersList에 대 한</span><span class="sxs-lookup"><span data-stu-id="e1118-152">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IScaleOutScaleUnitParametersList</span></span>

### <span data-ttu-id="e1118-153">FabricAdmin. IFabricAdminIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="e1118-153">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="e1118-154">출력</span><span class="sxs-lookup"><span data-stu-id="e1118-154">OUTPUTS</span></span>

### <span data-ttu-id="e1118-155">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="e1118-155">System.Boolean</span></span>

## <span data-ttu-id="e1118-156">상속자</span><span class="sxs-lookup"><span data-stu-id="e1118-156">NOTES</span></span>

<span data-ttu-id="e1118-157">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1118-157">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e1118-158">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="e1118-158">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="e1118-159">INPUTOBJECT <IFabricAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="e1118-159">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e1118-160">`[Drive <String>]`: 저장소 드라이브의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e1118-160">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="e1118-161">`[EdgeGateway <String>]`: Edge 게이트웨이의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e1118-161">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="e1118-162">`[EdgeGatewayPool <String>]`: Edge 게이트웨이 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e1118-162">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="e1118-163">`[FabricLocation <String>]`: 패브릭 위치.</span><span class="sxs-lookup"><span data-stu-id="e1118-163">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="e1118-164">`[FileShare <String>]`: 패브릭 파일 공유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e1118-164">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="e1118-165">`[IPPool <String>]`: IP 풀 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e1118-165">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="e1118-166">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="e1118-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e1118-167">`[InfraRole <String>]`: 인프라 역할 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e1118-167">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="e1118-168">`[InfraRoleInstance <String>]`: 인프라 역할 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e1118-168">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="e1118-169">`[Location <String>]`: 리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="e1118-169">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="e1118-170">`[LogicalNetwork <String>]`: 논리 네트워크의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e1118-170">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="e1118-171">`[LogicalSubnet <String>]`: 논리 서브넷의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e1118-171">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="e1118-172">`[MacAddressPool <String>]`: MAC 주소 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e1118-172">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="e1118-173">`[Operation <String>]`: 작업 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="e1118-173">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="e1118-174">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e1118-174">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="e1118-175">`[ScaleUnit <String>]`: 눈금 단위 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e1118-175">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="e1118-176">`[ScaleUnitNode <String>]`: 배율 단위 노드의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e1118-176">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="e1118-177">`[SlbMuxInstance <String>]`: SLB MUX 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e1118-177">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="e1118-178">`[StorageSubSystem <String>]`: 저장소 시스템의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e1118-178">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="e1118-179">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="e1118-179">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e1118-180">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e1118-180">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="e1118-181">`[Volume <String>]`: 저장소 볼륨의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e1118-181">`[Volume <String>]`: Name of the storage volume.</span></span>

<span data-ttu-id="e1118-182">NODELIST <IScaleOutScaleUnitParameters [] >: 배율 단위 노드의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="e1118-182">NODELIST <IScaleOutScaleUnitParameters[]>: List of nodes in the scale unit.</span></span>
  - <span data-ttu-id="e1118-183">`[BmciPv4Address <String>]`: 물리적 컴퓨터의 BMC 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="e1118-183">`[BmciPv4Address <String>]`: BMC address of the physical machine.</span></span>
  - <span data-ttu-id="e1118-184">`[ComputerName <String>]`: 물리적 컴퓨터의 컴퓨터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e1118-184">`[ComputerName <String>]`: Computer name of the physical machine.</span></span>

<span data-ttu-id="e1118-185">SCALEUNITNODEPARAMETER <IScaleOutScaleUnitParametersList> : 배율 단위 노드 집합을 추가 하는 데 사용할 수 있는 입력 데이터 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="e1118-185">SCALEUNITNODEPARAMETER <IScaleOutScaleUnitParametersList>: A list of input data that allows for adding a set of scale unit nodes.</span></span>
  - <span data-ttu-id="e1118-186">`[AwaitStorageConvergence <Boolean?>]`: 플래그 반환 하기 전에 작업이 저장소를 대기 해야 하는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e1118-186">`[AwaitStorageConvergence <Boolean?>]`: Flag indicates if the operation should wait for storage to converge before returning.</span></span>
  - <span data-ttu-id="e1118-187">`[NodeList <IScaleOutScaleUnitParameters[]>]`: 배율 단위 노드의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="e1118-187">`[NodeList <IScaleOutScaleUnitParameters[]>]`: List of nodes in the scale unit.</span></span>
    - <span data-ttu-id="e1118-188">`[BmciPv4Address <String>]`: 물리적 컴퓨터의 BMC 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="e1118-188">`[BmciPv4Address <String>]`: BMC address of the physical machine.</span></span>
    - <span data-ttu-id="e1118-189">`[ComputerName <String>]`: 물리적 컴퓨터의 컴퓨터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e1118-189">`[ComputerName <String>]`: Computer name of the physical machine.</span></span>

## <span data-ttu-id="e1118-190">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e1118-190">RELATED LINKS</span></span>
