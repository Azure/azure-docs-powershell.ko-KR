---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/stop-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: d413d7da00fe18de804306d0cfaa1ccade0e2650
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/24/2020
ms.locfileid: "94045209"
---
# <span data-ttu-id="014dd-101">Stop-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="014dd-101">Stop-AzsScaleUnitNode</span></span>

## <span data-ttu-id="014dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="014dd-102">SYNOPSIS</span></span>
<span data-ttu-id="014dd-103">배율 단위 노드의 전원을 끕니다.</span><span class="sxs-lookup"><span data-stu-id="014dd-103">Power off a scale unit node.</span></span>

## <span data-ttu-id="014dd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="014dd-104">SYNTAX</span></span>

### <span data-ttu-id="014dd-105">PowerOff (기본값)</span><span class="sxs-lookup"><span data-stu-id="014dd-105">PowerOff (Default)</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="014dd-106">PowerOffViaIdentity</span><span class="sxs-lookup"><span data-stu-id="014dd-106">PowerOffViaIdentity</span></span>
```
Stop-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="014dd-107">셧다운</span><span class="sxs-lookup"><span data-stu-id="014dd-107">Shutdown</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="014dd-108">ShutdownViaIdentity</span><span class="sxs-lookup"><span data-stu-id="014dd-108">ShutdownViaIdentity</span></span>
```
Stop-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="014dd-109">설명은</span><span class="sxs-lookup"><span data-stu-id="014dd-109">DESCRIPTION</span></span>
<span data-ttu-id="014dd-110">배율 단위 노드의 전원을 끕니다.</span><span class="sxs-lookup"><span data-stu-id="014dd-110">Power off a scale unit node.</span></span>

## <span data-ttu-id="014dd-111">예제의</span><span class="sxs-lookup"><span data-stu-id="014dd-111">EXAMPLES</span></span>

### <span data-ttu-id="014dd-112">예제 1: {{여기에 제목 추가}}</span><span class="sxs-lookup"><span data-stu-id="014dd-112">Example 1: {{ Add title here }}</span></span>
```powershell
PS C:\> Stop-AzsInfrastructureRoleInstancef -Name "AzS-ACS01"

```

<span data-ttu-id="014dd-113">인프라 역할 인스턴스의 기능을 해제 합니다.</span><span class="sxs-lookup"><span data-stu-id="014dd-113">Power off a infrastructure role instance.</span></span>

## <span data-ttu-id="014dd-114">변수</span><span class="sxs-lookup"><span data-stu-id="014dd-114">PARAMETERS</span></span>

### <span data-ttu-id="014dd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="014dd-115">-AsJob</span></span>
<span data-ttu-id="014dd-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="014dd-116">Run the command as a job</span></span>

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

### <span data-ttu-id="014dd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="014dd-117">-DefaultProfile</span></span>
<span data-ttu-id="014dd-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="014dd-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="014dd-119">-Force</span><span class="sxs-lookup"><span data-stu-id="014dd-119">-Force</span></span>
<span data-ttu-id="014dd-120">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="014dd-120">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="014dd-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="014dd-121">-InputObject</span></span>
<span data-ttu-id="014dd-122">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="014dd-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: PowerOffViaIdentity, ShutdownViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="014dd-123">-위치</span><span class="sxs-lookup"><span data-stu-id="014dd-123">-Location</span></span>
<span data-ttu-id="014dd-124">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="014dd-124">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff, Shutdown
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="014dd-125">-이름</span><span class="sxs-lookup"><span data-stu-id="014dd-125">-Name</span></span>
<span data-ttu-id="014dd-126">인프라 역할 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="014dd-126">Name of an infrastructure role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff, Shutdown
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="014dd-127">-NoWait</span><span class="sxs-lookup"><span data-stu-id="014dd-127">-NoWait</span></span>
<span data-ttu-id="014dd-128">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="014dd-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="014dd-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="014dd-129">-PassThru</span></span>
<span data-ttu-id="014dd-130">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="014dd-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="014dd-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="014dd-131">-ResourceGroupName</span></span>
<span data-ttu-id="014dd-132">배율 단위 노드의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="014dd-132">Name of the scale unit node.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff, Shutdown
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="014dd-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="014dd-133">-SubscriptionId</span></span>
<span data-ttu-id="014dd-134">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="014dd-134">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="014dd-135">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="014dd-135">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff, Shutdown
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="014dd-136">-확인</span><span class="sxs-lookup"><span data-stu-id="014dd-136">-Confirm</span></span>
<span data-ttu-id="014dd-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="014dd-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="014dd-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="014dd-138">-WhatIf</span></span>
<span data-ttu-id="014dd-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="014dd-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="014dd-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="014dd-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="014dd-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="014dd-141">CommonParameters</span></span>
<span data-ttu-id="014dd-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="014dd-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="014dd-143">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="014dd-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="014dd-144">입력</span><span class="sxs-lookup"><span data-stu-id="014dd-144">INPUTS</span></span>

### <span data-ttu-id="014dd-145">FabricAdmin. IFabricAdminIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="014dd-145">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="014dd-146">출력</span><span class="sxs-lookup"><span data-stu-id="014dd-146">OUTPUTS</span></span>

### <span data-ttu-id="014dd-147">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="014dd-147">System.Boolean</span></span>



## <span data-ttu-id="014dd-148">상속자</span><span class="sxs-lookup"><span data-stu-id="014dd-148">NOTES</span></span>

<span data-ttu-id="014dd-149">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="014dd-149">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="014dd-150">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="014dd-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="014dd-151">INPUTOBJECT <IFabricAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="014dd-151">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="014dd-152">`[Drive <String>]`: 저장소 드라이브의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="014dd-152">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="014dd-153">`[EdgeGateway <String>]`: Edge 게이트웨이의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="014dd-153">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="014dd-154">`[EdgeGatewayPool <String>]`: Edge 게이트웨이 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="014dd-154">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="014dd-155">`[FabricLocation <String>]`: 패브릭 위치.</span><span class="sxs-lookup"><span data-stu-id="014dd-155">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="014dd-156">`[FileShare <String>]`: 패브릭 파일 공유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="014dd-156">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="014dd-157">`[IPPool <String>]`: IP 풀 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="014dd-157">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="014dd-158">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="014dd-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="014dd-159">`[InfraRole <String>]`: 인프라 역할 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="014dd-159">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="014dd-160">`[InfraRoleInstance <String>]`: 인프라 역할 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="014dd-160">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="014dd-161">`[Location <String>]`: 리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="014dd-161">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="014dd-162">`[LogicalNetwork <String>]`: 논리 네트워크의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="014dd-162">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="014dd-163">`[LogicalSubnet <String>]`: 논리 서브넷의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="014dd-163">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="014dd-164">`[MacAddressPool <String>]`: MAC 주소 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="014dd-164">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="014dd-165">`[Operation <String>]`: 작업 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="014dd-165">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="014dd-166">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="014dd-166">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="014dd-167">`[ScaleUnit <String>]`: 눈금 단위 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="014dd-167">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="014dd-168">`[ScaleUnitNode <String>]`: 배율 단위 노드의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="014dd-168">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="014dd-169">`[SlbMuxInstance <String>]`: SLB MUX 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="014dd-169">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="014dd-170">`[StoragePool <String>]`: 저장소 풀 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="014dd-170">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="014dd-171">`[StorageSubSystem <String>]`: 저장소 시스템의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="014dd-171">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="014dd-172">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="014dd-172">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="014dd-173">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="014dd-173">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="014dd-174">`[Volume <String>]`: 저장소 볼륨의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="014dd-174">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="014dd-175">관련 링크</span><span class="sxs-lookup"><span data-stu-id="014dd-175">RELATED LINKS</span></span>

