---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/repair-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: b9a285e650f0ed47dd0144a460b324ecdae49f7d
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94047147"
---
# <span data-ttu-id="9c2f4-101">Repair-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="9c2f4-101">Repair-AzsScaleUnitNode</span></span>

## <span data-ttu-id="9c2f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c2f4-102">SYNOPSIS</span></span>
<span data-ttu-id="9c2f4-103">클러스터의 노드를 복구 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-103">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="9c2f4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9c2f4-104">SYNTAX</span></span>

### <span data-ttu-id="9c2f4-105">RepairExpanded (기본값)</span><span class="sxs-lookup"><span data-stu-id="9c2f4-105">RepairExpanded (Default)</span></span>
```
Repair-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-BiosVersion <String>] [-BmciPv4Address <String>] [-ClusterName <String>]
 [-ComputerName <String>] [-Force] [-MacAddress <String>] [-Model <String>] [-SerialNumber <String>]
 [-Vendor <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="9c2f4-106">복구</span><span class="sxs-lookup"><span data-stu-id="9c2f4-106">Repair</span></span>
```
Repair-AzsScaleUnitNode -Name <String> -BareMetalNode <IBareMetalNodeDescription> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9c2f4-107">RepairViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9c2f4-107">RepairViaIdentity</span></span>
```
Repair-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> -BareMetalNode <IBareMetalNodeDescription>
 [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="9c2f4-108">RepairViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="9c2f4-108">RepairViaIdentityExpanded</span></span>
```
Repair-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-BiosVersion <String>] [-BmciPv4Address <String>]
 [-ClusterName <String>] [-ComputerName <String>] [-Force] [-MacAddress <String>] [-Model <String>]
 [-SerialNumber <String>] [-Vendor <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9c2f4-109">설명은</span><span class="sxs-lookup"><span data-stu-id="9c2f4-109">DESCRIPTION</span></span>
<span data-ttu-id="9c2f4-110">클러스터의 노드를 복구 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-110">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="9c2f4-111">예제의</span><span class="sxs-lookup"><span data-stu-id="9c2f4-111">EXAMPLES</span></span>

### <span data-ttu-id="9c2f4-112">예제 1:</span><span class="sxs-lookup"><span data-stu-id="9c2f4-112">Example 1:</span></span>
```powershell
PS C:\> Repair-AzsScaleUnitNode -Name "AZS-ERCO03" -BMCIPv4Address ***.***.***.***

```

<span data-ttu-id="9c2f4-113">배율 단위 노드를 복구 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-113">Repair a scale unit node.</span></span>


## <span data-ttu-id="9c2f4-114">변수</span><span class="sxs-lookup"><span data-stu-id="9c2f4-114">PARAMETERS</span></span>

### <span data-ttu-id="9c2f4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9c2f4-115">-AsJob</span></span>
<span data-ttu-id="9c2f4-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="9c2f4-116">Run the command as a job</span></span>

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

### <span data-ttu-id="9c2f4-117">-BareMetalNode</span><span class="sxs-lookup"><span data-stu-id="9c2f4-117">-BareMetalNode</span></span>
<span data-ttu-id="9c2f4-118">클러스터에서 ScaleOut 작업에 사용 되는 완전 한 메탈 노드에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-118">Description of a bare metal node used for ScaleOut operation on a cluster.</span></span>
<span data-ttu-id="9c2f4-119">생성 하려면 BAREMETALNODE 속성에 대 한 메모 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-119">To construct, see NOTES section for BAREMETALNODE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IBareMetalNodeDescription
Parameter Sets: Repair, RepairViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="9c2f4-120">-BiosVersion</span><span class="sxs-lookup"><span data-stu-id="9c2f4-120">-BiosVersion</span></span>
<span data-ttu-id="9c2f4-121">물리적 컴퓨터의 Bios 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-121">Bios version of the physical machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9c2f4-122">-BmciPv4Address</span><span class="sxs-lookup"><span data-stu-id="9c2f4-122">-BmciPv4Address</span></span>
<span data-ttu-id="9c2f4-123">물리적 컴퓨터의 BMC 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-123">BMC address of the physical machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9c2f4-124">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="9c2f4-124">-ClusterName</span></span>
<span data-ttu-id="9c2f4-125">클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-125">Name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9c2f4-126">-ComputerName</span><span class="sxs-lookup"><span data-stu-id="9c2f4-126">-ComputerName</span></span>
<span data-ttu-id="9c2f4-127">컴퓨터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-127">Name of the computer.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9c2f4-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c2f4-128">-DefaultProfile</span></span>
<span data-ttu-id="9c2f4-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c2f4-130">-Force</span><span class="sxs-lookup"><span data-stu-id="9c2f4-130">-Force</span></span>
<span data-ttu-id="9c2f4-131">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-131">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="9c2f4-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c2f4-132">-InputObject</span></span>
<span data-ttu-id="9c2f4-133">생성 하려면 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-133">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: RepairViaIdentity, RepairViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="9c2f4-134">-위치</span><span class="sxs-lookup"><span data-stu-id="9c2f4-134">-Location</span></span>
<span data-ttu-id="9c2f4-135">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-135">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair, RepairExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9c2f4-136">-(.)</span><span class="sxs-lookup"><span data-stu-id="9c2f4-136">-MacAddress</span></span>
<span data-ttu-id="9c2f4-137">완전 노드의 MAC 주소 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-137">Name of the MAC address of the bare metal node.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9c2f4-138">-모델</span><span class="sxs-lookup"><span data-stu-id="9c2f4-138">-Model</span></span>
<span data-ttu-id="9c2f4-139">물리적 컴퓨터의 모델입니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-139">Model of the physical machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9c2f4-140">-이름</span><span class="sxs-lookup"><span data-stu-id="9c2f4-140">-Name</span></span>
<span data-ttu-id="9c2f4-141">배율 단위 노드의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-141">Name of the scale unit node.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair, RepairExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9c2f4-142">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9c2f4-142">-NoWait</span></span>
<span data-ttu-id="9c2f4-143">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="9c2f4-143">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9c2f4-144">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9c2f4-144">-PassThru</span></span>
<span data-ttu-id="9c2f4-145">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-145">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9c2f4-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c2f4-146">-ResourceGroupName</span></span>
<span data-ttu-id="9c2f4-147">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-147">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair, RepairExpanded
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9c2f4-148">-일련 번호</span><span class="sxs-lookup"><span data-stu-id="9c2f4-148">-SerialNumber</span></span>
<span data-ttu-id="9c2f4-149">물리적 컴퓨터의 일련 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-149">Serial number of the physical machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9c2f4-150">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9c2f4-150">-SubscriptionId</span></span>
<span data-ttu-id="9c2f4-151">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-151">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="9c2f4-152">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-152">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair, RepairExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9c2f4-153">-공급 업체</span><span class="sxs-lookup"><span data-stu-id="9c2f4-153">-Vendor</span></span>
<span data-ttu-id="9c2f4-154">물리적 컴퓨터의 공급 업체입니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-154">Vendor of the physical machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9c2f4-155">-확인</span><span class="sxs-lookup"><span data-stu-id="9c2f4-155">-Confirm</span></span>
<span data-ttu-id="9c2f4-156">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c2f4-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c2f4-157">-WhatIf</span></span>
<span data-ttu-id="9c2f4-158">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c2f4-159">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c2f4-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c2f4-160">CommonParameters</span></span>
<span data-ttu-id="9c2f4-161">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c2f4-162">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c2f4-163">입력</span><span class="sxs-lookup"><span data-stu-id="9c2f4-163">INPUTS</span></span>

### <span data-ttu-id="9c2f4-164">FabricAdmin. Api20160501. IBareMetalNodeDescription에 대 한</span><span class="sxs-lookup"><span data-stu-id="9c2f4-164">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IBareMetalNodeDescription</span></span>

### <span data-ttu-id="9c2f4-165">FabricAdmin. IFabricAdminIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="9c2f4-165">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="9c2f4-166">출력</span><span class="sxs-lookup"><span data-stu-id="9c2f4-166">OUTPUTS</span></span>

### <span data-ttu-id="9c2f4-167">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="9c2f4-167">System.Boolean</span></span>



## <span data-ttu-id="9c2f4-168">상속자</span><span class="sxs-lookup"><span data-stu-id="9c2f4-168">NOTES</span></span>

<span data-ttu-id="9c2f4-169">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-169">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9c2f4-170">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-170">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="9c2f4-171">BAREMETALNODE <IBareMetalNodeDescription> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="9c2f4-171">BAREMETALNODE <IBareMetalNodeDescription>: Identity Parameter</span></span>
  - <span data-ttu-id="9c2f4-172">`[BiosVersion <String>]`: 물리적 컴퓨터의 Bios 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-172">`[BiosVersion <String>]`: Bios version of the physical machine.</span></span>
  - <span data-ttu-id="9c2f4-173">`[BmciPv4Address <String>]`: 물리적 컴퓨터의 BMC 주소입니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-173">`[BmciPv4Address <String>]`: BMC address of the physical machine.</span></span>
  - <span data-ttu-id="9c2f4-174">`[ClusterName <String>]`: 클러스터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-174">`[ClusterName <String>]`: Name of the cluster.</span></span>
  - <span data-ttu-id="9c2f4-175">`[ComputerName <String>]`: 컴퓨터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-175">`[ComputerName <String>]`: Name of the computer.</span></span>
  - <span data-ttu-id="9c2f4-176">`[MacAddress <String>]`: 완전 한 금속 노드의 MAC 주소 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-176">`[MacAddress <String>]`: Name of the MAC address of the bare metal node.</span></span>
  - <span data-ttu-id="9c2f4-177">`[Model <String>]`: 물리적 컴퓨터의 모델입니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-177">`[Model <String>]`: Model of the physical machine.</span></span>
  - <span data-ttu-id="9c2f4-178">`[SerialNumber <String>]`: 물리적 컴퓨터의 일련 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-178">`[SerialNumber <String>]`: Serial number of the physical machine.</span></span>
  - <span data-ttu-id="9c2f4-179">`[Vendor <String>]`: 물리적 컴퓨터의 공급 업체입니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-179">`[Vendor <String>]`: Vendor of the physical machine.</span></span>

<span data-ttu-id="9c2f4-180">INPUTOBJECT <IFabricAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="9c2f4-180">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9c2f4-181">`[Drive <String>]`: 저장소 드라이브의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-181">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="9c2f4-182">`[EdgeGateway <String>]`: Edge 게이트웨이의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-182">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="9c2f4-183">`[EdgeGatewayPool <String>]`: Edge 게이트웨이 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-183">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="9c2f4-184">`[FabricLocation <String>]`: 패브릭 위치.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-184">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="9c2f4-185">`[FileShare <String>]`: 패브릭 파일 공유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-185">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="9c2f4-186">`[IPPool <String>]`: IP 풀 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-186">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="9c2f4-187">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="9c2f4-187">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9c2f4-188">`[InfraRole <String>]`: 인프라 역할 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-188">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="9c2f4-189">`[InfraRoleInstance <String>]`: 인프라 역할 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-189">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="9c2f4-190">`[Location <String>]`: 리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-190">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="9c2f4-191">`[LogicalNetwork <String>]`: 논리 네트워크의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-191">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="9c2f4-192">`[LogicalSubnet <String>]`: 논리 서브넷의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-192">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="9c2f4-193">`[MacAddressPool <String>]`: MAC 주소 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-193">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="9c2f4-194">`[Operation <String>]`: 작업 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-194">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="9c2f4-195">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-195">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="9c2f4-196">`[ScaleUnit <String>]`: 눈금 단위 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-196">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="9c2f4-197">`[ScaleUnitNode <String>]`: 배율 단위 노드의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-197">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="9c2f4-198">`[SlbMuxInstance <String>]`: SLB MUX 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-198">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="9c2f4-199">`[StoragePool <String>]`: 저장소 풀 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-199">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="9c2f4-200">`[StorageSubSystem <String>]`: 저장소 시스템의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-200">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="9c2f4-201">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-201">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="9c2f4-202">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-202">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="9c2f4-203">`[Volume <String>]`: 저장소 볼륨의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9c2f4-203">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="9c2f4-204">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9c2f4-204">RELATED LINKS</span></span>

