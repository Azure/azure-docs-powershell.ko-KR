---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.fabric.admin/start-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: c8b1ed8ea0be65e92022cf1ac759024a07fc76c4
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94046698"
---
# <span data-ttu-id="59268-101">Start-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="59268-101">Start-AzsScaleUnitNode</span></span>

## <span data-ttu-id="59268-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59268-102">SYNOPSIS</span></span>
<span data-ttu-id="59268-103">배율 단위 노드의 전원을 켭니다.</span><span class="sxs-lookup"><span data-stu-id="59268-103">Power on a scale unit node.</span></span>

## <span data-ttu-id="59268-104">구문과</span><span class="sxs-lookup"><span data-stu-id="59268-104">SYNTAX</span></span>

### <span data-ttu-id="59268-105">PowerOn (기본값)</span><span class="sxs-lookup"><span data-stu-id="59268-105">PowerOn (Default)</span></span>
```
Start-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="59268-106">PowerOnViaIdentity</span><span class="sxs-lookup"><span data-stu-id="59268-106">PowerOnViaIdentity</span></span>
```
Start-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="59268-107">설명은</span><span class="sxs-lookup"><span data-stu-id="59268-107">DESCRIPTION</span></span>
<span data-ttu-id="59268-108">배율 단위 노드의 전원을 켭니다.</span><span class="sxs-lookup"><span data-stu-id="59268-108">Power on a scale unit node.</span></span>

## <span data-ttu-id="59268-109">예제의</span><span class="sxs-lookup"><span data-stu-id="59268-109">EXAMPLES</span></span>

### <span data-ttu-id="59268-110">예제 1:</span><span class="sxs-lookup"><span data-stu-id="59268-110">Example 1:</span></span>
```powershell
PS C:\> Start-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="59268-111">배율 단위 노드의 전원을 켭니다.</span><span class="sxs-lookup"><span data-stu-id="59268-111">Power on a scale unit node.</span></span>

### <span data-ttu-id="59268-112">예제 2:</span><span class="sxs-lookup"><span data-stu-id="59268-112">Example 2:</span></span>
```powershell
PS C:\> Start-AzsScaleUnitNode -Name "HC1n25r2236" -AsJob
```

<span data-ttu-id="59268-113">배율 단위 노드의 전원을 켭니다.</span><span class="sxs-lookup"><span data-stu-id="59268-113">Power on a scale unit node.</span></span> <span data-ttu-id="59268-114">작업으로</span><span class="sxs-lookup"><span data-stu-id="59268-114">As a job.</span></span>

## <span data-ttu-id="59268-115">변수</span><span class="sxs-lookup"><span data-stu-id="59268-115">PARAMETERS</span></span>

### <span data-ttu-id="59268-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="59268-116">-AsJob</span></span>
<span data-ttu-id="59268-117">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="59268-117">Run the command as a job</span></span>

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

### <span data-ttu-id="59268-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59268-118">-DefaultProfile</span></span>
<span data-ttu-id="59268-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="59268-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59268-120">-Force</span><span class="sxs-lookup"><span data-stu-id="59268-120">-Force</span></span>
<span data-ttu-id="59268-121">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="59268-121">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="59268-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59268-122">-InputObject</span></span>
<span data-ttu-id="59268-123">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="59268-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: PowerOnViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="59268-124">-위치</span><span class="sxs-lookup"><span data-stu-id="59268-124">-Location</span></span>
<span data-ttu-id="59268-125">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="59268-125">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="59268-126">-이름</span><span class="sxs-lookup"><span data-stu-id="59268-126">-Name</span></span>
<span data-ttu-id="59268-127">배율 단위 노드의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59268-127">Name of the scale unit node.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="59268-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="59268-128">-NoWait</span></span>
<span data-ttu-id="59268-129">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="59268-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="59268-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="59268-130">-PassThru</span></span>
<span data-ttu-id="59268-131">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="59268-131">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="59268-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59268-132">-ResourceGroupName</span></span>
<span data-ttu-id="59268-133">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59268-133">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="59268-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="59268-134">-SubscriptionId</span></span>
<span data-ttu-id="59268-135">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="59268-135">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="59268-136">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="59268-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="59268-137">-확인</span><span class="sxs-lookup"><span data-stu-id="59268-137">-Confirm</span></span>
<span data-ttu-id="59268-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="59268-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59268-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59268-139">-WhatIf</span></span>
<span data-ttu-id="59268-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="59268-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59268-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="59268-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59268-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59268-142">CommonParameters</span></span>
<span data-ttu-id="59268-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="59268-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59268-144">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="59268-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59268-145">입력</span><span class="sxs-lookup"><span data-stu-id="59268-145">INPUTS</span></span>

### <span data-ttu-id="59268-146">FabricAdmin. IFabricAdminIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="59268-146">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="59268-147">출력</span><span class="sxs-lookup"><span data-stu-id="59268-147">OUTPUTS</span></span>

### <span data-ttu-id="59268-148">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="59268-148">System.Boolean</span></span>

## <span data-ttu-id="59268-149">상속자</span><span class="sxs-lookup"><span data-stu-id="59268-149">NOTES</span></span>

<span data-ttu-id="59268-150">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="59268-150">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="59268-151">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="59268-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="59268-152">INPUTOBJECT <IFabricAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="59268-152">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="59268-153">`[Drive <String>]`: 저장소 드라이브의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59268-153">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="59268-154">`[EdgeGateway <String>]`: Edge 게이트웨이의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59268-154">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="59268-155">`[EdgeGatewayPool <String>]`: Edge 게이트웨이 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59268-155">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="59268-156">`[FabricLocation <String>]`: 패브릭 위치.</span><span class="sxs-lookup"><span data-stu-id="59268-156">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="59268-157">`[FileShare <String>]`: 패브릭 파일 공유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59268-157">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="59268-158">`[IPPool <String>]`: IP 풀 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59268-158">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="59268-159">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="59268-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="59268-160">`[InfraRole <String>]`: 인프라 역할 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59268-160">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="59268-161">`[InfraRoleInstance <String>]`: 인프라 역할 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59268-161">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="59268-162">`[Location <String>]`: 리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="59268-162">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="59268-163">`[LogicalNetwork <String>]`: 논리 네트워크의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59268-163">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="59268-164">`[LogicalSubnet <String>]`: 논리 서브넷의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59268-164">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="59268-165">`[MacAddressPool <String>]`: MAC 주소 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59268-165">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="59268-166">`[Operation <String>]`: 작업 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="59268-166">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="59268-167">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59268-167">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="59268-168">`[ScaleUnit <String>]`: 눈금 단위 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59268-168">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="59268-169">`[ScaleUnitNode <String>]`: 배율 단위 노드의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59268-169">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="59268-170">`[SlbMuxInstance <String>]`: SLB MUX 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59268-170">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="59268-171">`[StoragePool <String>]`: 저장소 풀 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59268-171">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="59268-172">`[StorageSubSystem <String>]`: 저장소 시스템의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59268-172">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="59268-173">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="59268-173">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="59268-174">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="59268-174">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="59268-175">`[Volume <String>]`: 저장소 볼륨의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59268-175">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="59268-176">관련 링크</span><span class="sxs-lookup"><span data-stu-id="59268-176">RELATED LINKS</span></span>
