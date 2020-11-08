---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/disable-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: 532ca56646ae2cfa25f6e3480f9f924d918cfedc
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/24/2020
ms.locfileid: "94045230"
---
# <span data-ttu-id="80183-101">Disable-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="80183-101">Disable-AzsScaleUnitNode</span></span>

## <span data-ttu-id="80183-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80183-102">SYNOPSIS</span></span>


## <span data-ttu-id="80183-103">구문과</span><span class="sxs-lookup"><span data-stu-id="80183-103">SYNTAX</span></span>

### <span data-ttu-id="80183-104">중지 (기본값)</span><span class="sxs-lookup"><span data-stu-id="80183-104">Stop (Default)</span></span>
```
Disable-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="80183-105">StopViaIdentity</span><span class="sxs-lookup"><span data-stu-id="80183-105">StopViaIdentity</span></span>
```
Disable-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="80183-106">설명은</span><span class="sxs-lookup"><span data-stu-id="80183-106">DESCRIPTION</span></span>


## <span data-ttu-id="80183-107">예제의</span><span class="sxs-lookup"><span data-stu-id="80183-107">EXAMPLES</span></span>

### <span data-ttu-id="80183-108">예제 1:</span><span class="sxs-lookup"><span data-stu-id="80183-108">Example 1:</span></span>
```powershell
PS C:\> Disable-AzsScaleUnitNode -Name "HC1n25r2236"

Enable maintenance mode for a scale unit node.
```

<span data-ttu-id="80183-109">확장 단위 노드의 유지 관리 모드를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="80183-109">Start maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="80183-110">변수</span><span class="sxs-lookup"><span data-stu-id="80183-110">PARAMETERS</span></span>

### <span data-ttu-id="80183-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="80183-111">-AsJob</span></span>


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

### <span data-ttu-id="80183-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80183-112">-DefaultProfile</span></span>


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

### <span data-ttu-id="80183-113">-Force</span><span class="sxs-lookup"><span data-stu-id="80183-113">-Force</span></span>


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

### <span data-ttu-id="80183-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="80183-114">-InputObject</span></span>
<span data-ttu-id="80183-115">생성 하려면 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="80183-115">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: StopViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="80183-116">-위치</span><span class="sxs-lookup"><span data-stu-id="80183-116">-Location</span></span>


```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="80183-117">-이름</span><span class="sxs-lookup"><span data-stu-id="80183-117">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="80183-118">-NoWait</span><span class="sxs-lookup"><span data-stu-id="80183-118">-NoWait</span></span>


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

### <span data-ttu-id="80183-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="80183-119">-PassThru</span></span>


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

### <span data-ttu-id="80183-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80183-120">-ResourceGroupName</span></span>


```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="80183-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="80183-121">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: Stop
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="80183-122">-확인</span><span class="sxs-lookup"><span data-stu-id="80183-122">-Confirm</span></span>
<span data-ttu-id="80183-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="80183-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80183-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80183-124">-WhatIf</span></span>
<span data-ttu-id="80183-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="80183-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80183-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="80183-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80183-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80183-127">CommonParameters</span></span>
<span data-ttu-id="80183-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="80183-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80183-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="80183-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80183-130">입력</span><span class="sxs-lookup"><span data-stu-id="80183-130">INPUTS</span></span>

### <span data-ttu-id="80183-131">FabricAdmin. IFabricAdminIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="80183-131">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="80183-132">출력</span><span class="sxs-lookup"><span data-stu-id="80183-132">OUTPUTS</span></span>

### <span data-ttu-id="80183-133">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="80183-133">System.Boolean</span></span>



## <span data-ttu-id="80183-134">상속자</span><span class="sxs-lookup"><span data-stu-id="80183-134">NOTES</span></span>

<span data-ttu-id="80183-135">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="80183-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="80183-136">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="80183-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="80183-137">INPUTOBJECT <IFabricAdminIdentity> :</span><span class="sxs-lookup"><span data-stu-id="80183-137">INPUTOBJECT <IFabricAdminIdentity>:</span></span> 
  - <span data-ttu-id="80183-138">`[Drive <String>]`: 저장소 드라이브의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80183-138">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="80183-139">`[EdgeGateway <String>]`: Edge 게이트웨이의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80183-139">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="80183-140">`[EdgeGatewayPool <String>]`: Edge 게이트웨이 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80183-140">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="80183-141">`[FabricLocation <String>]`: 패브릭 위치.</span><span class="sxs-lookup"><span data-stu-id="80183-141">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="80183-142">`[FileShare <String>]`: 패브릭 파일 공유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80183-142">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="80183-143">`[IPPool <String>]`: IP 풀 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80183-143">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="80183-144">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="80183-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="80183-145">`[InfraRole <String>]`: 인프라 역할 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80183-145">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="80183-146">`[InfraRoleInstance <String>]`: 인프라 역할 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80183-146">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="80183-147">`[Location <String>]`: 리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="80183-147">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="80183-148">`[LogicalNetwork <String>]`: 논리 네트워크의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80183-148">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="80183-149">`[LogicalSubnet <String>]`: 논리 서브넷의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80183-149">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="80183-150">`[MacAddressPool <String>]`: MAC 주소 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80183-150">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="80183-151">`[Operation <String>]`: 작업 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="80183-151">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="80183-152">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80183-152">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="80183-153">`[ScaleUnit <String>]`: 눈금 단위 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80183-153">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="80183-154">`[ScaleUnitNode <String>]`: 배율 단위 노드의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80183-154">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="80183-155">`[SlbMuxInstance <String>]`: SLB MUX 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80183-155">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="80183-156">`[StorageSubSystem <String>]`: 저장소 시스템의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80183-156">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="80183-157">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="80183-157">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="80183-158">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="80183-158">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="80183-159">`[Volume <String>]`: 저장소 볼륨의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="80183-159">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="80183-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="80183-160">RELATED LINKS</span></span>

