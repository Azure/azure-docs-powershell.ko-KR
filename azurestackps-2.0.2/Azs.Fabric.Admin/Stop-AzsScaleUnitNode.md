---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.fabric.admin/stop-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: 3f5adef6382038fdaf8c17620508b4a450ff74bc
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94046809"
---
# <span data-ttu-id="90398-101">Stop-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="90398-101">Stop-AzsScaleUnitNode</span></span>

## <span data-ttu-id="90398-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90398-102">SYNOPSIS</span></span>
<span data-ttu-id="90398-103">배율 단위 노드의 전원을 끕니다.</span><span class="sxs-lookup"><span data-stu-id="90398-103">Power off a scale unit node.</span></span>

## <span data-ttu-id="90398-104">구문과</span><span class="sxs-lookup"><span data-stu-id="90398-104">SYNTAX</span></span>

### <span data-ttu-id="90398-105">PowerOff (기본값)</span><span class="sxs-lookup"><span data-stu-id="90398-105">PowerOff (Default)</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="90398-106">PowerOffViaIdentity</span><span class="sxs-lookup"><span data-stu-id="90398-106">PowerOffViaIdentity</span></span>
```
Stop-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="90398-107">셧다운</span><span class="sxs-lookup"><span data-stu-id="90398-107">Shutdown</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="90398-108">ShutdownViaIdentity</span><span class="sxs-lookup"><span data-stu-id="90398-108">ShutdownViaIdentity</span></span>
```
Stop-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="90398-109">설명은</span><span class="sxs-lookup"><span data-stu-id="90398-109">DESCRIPTION</span></span>
<span data-ttu-id="90398-110">배율 단위 노드의 전원을 끕니다.</span><span class="sxs-lookup"><span data-stu-id="90398-110">Power off a scale unit node.</span></span>

## <span data-ttu-id="90398-111">예제의</span><span class="sxs-lookup"><span data-stu-id="90398-111">EXAMPLES</span></span>

### <span data-ttu-id="90398-112">예제 1:</span><span class="sxs-lookup"><span data-stu-id="90398-112">Example 1:</span></span>
```powershell
PS C:\> Stop-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="90398-113">배율 단위 노드 전원을 차단 합니다.</span><span class="sxs-lookup"><span data-stu-id="90398-113">Power down a scale unit node.</span></span>

### <span data-ttu-id="90398-114">예제 2:</span><span class="sxs-lookup"><span data-stu-id="90398-114">Example 2:</span></span>
```powershell
PS C:\> Stop-AzsScaleUnitNode -Name "HC1n25r2236" -AsJob
```

<span data-ttu-id="90398-115">배율 단위 노드 전원을 차단 합니다.</span><span class="sxs-lookup"><span data-stu-id="90398-115">Power down a scale unit node.</span></span> <span data-ttu-id="90398-116">작업으로</span><span class="sxs-lookup"><span data-stu-id="90398-116">As a job.</span></span>

## <span data-ttu-id="90398-117">변수</span><span class="sxs-lookup"><span data-stu-id="90398-117">PARAMETERS</span></span>

### <span data-ttu-id="90398-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="90398-118">-AsJob</span></span>
<span data-ttu-id="90398-119">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="90398-119">Run the command as a job</span></span>

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

### <span data-ttu-id="90398-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90398-120">-DefaultProfile</span></span>
<span data-ttu-id="90398-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="90398-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90398-122">-Force</span><span class="sxs-lookup"><span data-stu-id="90398-122">-Force</span></span>
<span data-ttu-id="90398-123">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="90398-123">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="90398-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="90398-124">-InputObject</span></span>
<span data-ttu-id="90398-125">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="90398-125">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="90398-126">-위치</span><span class="sxs-lookup"><span data-stu-id="90398-126">-Location</span></span>
<span data-ttu-id="90398-127">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="90398-127">Location of the resource.</span></span>

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

### <span data-ttu-id="90398-128">-이름</span><span class="sxs-lookup"><span data-stu-id="90398-128">-Name</span></span>
<span data-ttu-id="90398-129">인프라 역할 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="90398-129">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="90398-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="90398-130">-NoWait</span></span>
<span data-ttu-id="90398-131">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="90398-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="90398-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="90398-132">-PassThru</span></span>
<span data-ttu-id="90398-133">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="90398-133">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="90398-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90398-134">-ResourceGroupName</span></span>
<span data-ttu-id="90398-135">배율 단위 노드의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="90398-135">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="90398-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="90398-136">-SubscriptionId</span></span>
<span data-ttu-id="90398-137">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="90398-137">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="90398-138">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="90398-138">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="90398-139">-확인</span><span class="sxs-lookup"><span data-stu-id="90398-139">-Confirm</span></span>
<span data-ttu-id="90398-140">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="90398-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90398-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90398-141">-WhatIf</span></span>
<span data-ttu-id="90398-142">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="90398-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90398-143">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="90398-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90398-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90398-144">CommonParameters</span></span>
<span data-ttu-id="90398-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="90398-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90398-146">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="90398-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90398-147">입력</span><span class="sxs-lookup"><span data-stu-id="90398-147">INPUTS</span></span>

### <span data-ttu-id="90398-148">FabricAdmin. IFabricAdminIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="90398-148">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="90398-149">출력</span><span class="sxs-lookup"><span data-stu-id="90398-149">OUTPUTS</span></span>

### <span data-ttu-id="90398-150">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="90398-150">System.Boolean</span></span>

## <span data-ttu-id="90398-151">상속자</span><span class="sxs-lookup"><span data-stu-id="90398-151">NOTES</span></span>

<span data-ttu-id="90398-152">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="90398-152">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="90398-153">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="90398-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="90398-154">INPUTOBJECT <IFabricAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="90398-154">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="90398-155">`[Drive <String>]`: 저장소 드라이브의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="90398-155">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="90398-156">`[EdgeGateway <String>]`: Edge 게이트웨이의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="90398-156">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="90398-157">`[EdgeGatewayPool <String>]`: Edge 게이트웨이 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="90398-157">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="90398-158">`[FabricLocation <String>]`: 패브릭 위치.</span><span class="sxs-lookup"><span data-stu-id="90398-158">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="90398-159">`[FileShare <String>]`: 패브릭 파일 공유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="90398-159">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="90398-160">`[IPPool <String>]`: IP 풀 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="90398-160">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="90398-161">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="90398-161">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="90398-162">`[InfraRole <String>]`: 인프라 역할 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="90398-162">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="90398-163">`[InfraRoleInstance <String>]`: 인프라 역할 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="90398-163">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="90398-164">`[Location <String>]`: 리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="90398-164">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="90398-165">`[LogicalNetwork <String>]`: 논리 네트워크의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="90398-165">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="90398-166">`[LogicalSubnet <String>]`: 논리 서브넷의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="90398-166">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="90398-167">`[MacAddressPool <String>]`: MAC 주소 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="90398-167">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="90398-168">`[Operation <String>]`: 작업 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="90398-168">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="90398-169">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="90398-169">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="90398-170">`[ScaleUnit <String>]`: 눈금 단위 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="90398-170">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="90398-171">`[ScaleUnitNode <String>]`: 배율 단위 노드의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="90398-171">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="90398-172">`[SlbMuxInstance <String>]`: SLB MUX 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="90398-172">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="90398-173">`[StoragePool <String>]`: 저장소 풀 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="90398-173">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="90398-174">`[StorageSubSystem <String>]`: 저장소 시스템의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="90398-174">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="90398-175">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="90398-175">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="90398-176">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="90398-176">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="90398-177">`[Volume <String>]`: 저장소 볼륨의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="90398-177">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="90398-178">관련 링크</span><span class="sxs-lookup"><span data-stu-id="90398-178">RELATED LINKS</span></span>
