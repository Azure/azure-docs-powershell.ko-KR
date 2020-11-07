---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/enable-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: 4a7140d5162f046377e37b92d4e6931abdbb4cf4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876080"
---
# <span data-ttu-id="c81a1-101">Enable-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="c81a1-101">Enable-AzsScaleUnitNode</span></span>

## <span data-ttu-id="c81a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c81a1-102">SYNOPSIS</span></span>


## <span data-ttu-id="c81a1-103">구문과</span><span class="sxs-lookup"><span data-stu-id="c81a1-103">SYNTAX</span></span>

### <span data-ttu-id="c81a1-104">시작 (기본값)</span><span class="sxs-lookup"><span data-stu-id="c81a1-104">Start (Default)</span></span>
```
Enable-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c81a1-105">StartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c81a1-105">StartViaIdentity</span></span>
```
Enable-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c81a1-106">설명은</span><span class="sxs-lookup"><span data-stu-id="c81a1-106">DESCRIPTION</span></span>


## <span data-ttu-id="c81a1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c81a1-107">EXAMPLES</span></span>

### <span data-ttu-id="c81a1-108">예제 1:</span><span class="sxs-lookup"><span data-stu-id="c81a1-108">Example 1:</span></span>
```powershell
PS C:\> Enable-AzsScaleUnitNode -Name "HC1n25r2236"

Stop maintenance mode on a scale unit node.
```

<span data-ttu-id="c81a1-109">확장 단위 노드의 유지 관리 모드를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="c81a1-109">Stop maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="c81a1-110">변수</span><span class="sxs-lookup"><span data-stu-id="c81a1-110">PARAMETERS</span></span>

### <span data-ttu-id="c81a1-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c81a1-111">-AsJob</span></span>


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

### <span data-ttu-id="c81a1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c81a1-112">-DefaultProfile</span></span>


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

### <span data-ttu-id="c81a1-113">-Force</span><span class="sxs-lookup"><span data-stu-id="c81a1-113">-Force</span></span>


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

### <span data-ttu-id="c81a1-114">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c81a1-114">-InputObject</span></span>
<span data-ttu-id="c81a1-115">생성 하려면 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c81a1-115">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: StartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="c81a1-116">-위치</span><span class="sxs-lookup"><span data-stu-id="c81a1-116">-Location</span></span>


```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c81a1-117">-이름</span><span class="sxs-lookup"><span data-stu-id="c81a1-117">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c81a1-118">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c81a1-118">-NoWait</span></span>


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

### <span data-ttu-id="c81a1-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c81a1-119">-PassThru</span></span>


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

### <span data-ttu-id="c81a1-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c81a1-120">-ResourceGroupName</span></span>


```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c81a1-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c81a1-121">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c81a1-122">-확인</span><span class="sxs-lookup"><span data-stu-id="c81a1-122">-Confirm</span></span>
<span data-ttu-id="c81a1-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c81a1-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c81a1-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c81a1-124">-WhatIf</span></span>
<span data-ttu-id="c81a1-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c81a1-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c81a1-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c81a1-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c81a1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c81a1-127">CommonParameters</span></span>
<span data-ttu-id="c81a1-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c81a1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c81a1-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c81a1-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c81a1-130">입력</span><span class="sxs-lookup"><span data-stu-id="c81a1-130">INPUTS</span></span>

### <span data-ttu-id="c81a1-131">FabricAdmin. IFabricAdminIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="c81a1-131">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="c81a1-132">출력</span><span class="sxs-lookup"><span data-stu-id="c81a1-132">OUTPUTS</span></span>

### <span data-ttu-id="c81a1-133">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="c81a1-133">System.Boolean</span></span>



## <span data-ttu-id="c81a1-134">상속자</span><span class="sxs-lookup"><span data-stu-id="c81a1-134">NOTES</span></span>

<span data-ttu-id="c81a1-135">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c81a1-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c81a1-136">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="c81a1-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="c81a1-137">INPUTOBJECT <IFabricAdminIdentity> :</span><span class="sxs-lookup"><span data-stu-id="c81a1-137">INPUTOBJECT <IFabricAdminIdentity>:</span></span> 
  - <span data-ttu-id="c81a1-138">`[Drive <String>]`: 저장소 드라이브의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c81a1-138">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="c81a1-139">`[EdgeGateway <String>]`: Edge 게이트웨이의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c81a1-139">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="c81a1-140">`[EdgeGatewayPool <String>]`: Edge 게이트웨이 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c81a1-140">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="c81a1-141">`[FabricLocation <String>]`: 패브릭 위치.</span><span class="sxs-lookup"><span data-stu-id="c81a1-141">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="c81a1-142">`[FileShare <String>]`: 패브릭 파일 공유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c81a1-142">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="c81a1-143">`[IPPool <String>]`: IP 풀 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c81a1-143">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="c81a1-144">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="c81a1-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c81a1-145">`[InfraRole <String>]`: 인프라 역할 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c81a1-145">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="c81a1-146">`[InfraRoleInstance <String>]`: 인프라 역할 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c81a1-146">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="c81a1-147">`[Location <String>]`: 리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="c81a1-147">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="c81a1-148">`[LogicalNetwork <String>]`: 논리 네트워크의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c81a1-148">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="c81a1-149">`[LogicalSubnet <String>]`: 논리 서브넷의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c81a1-149">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="c81a1-150">`[MacAddressPool <String>]`: MAC 주소 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c81a1-150">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="c81a1-151">`[Operation <String>]`: 작업 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="c81a1-151">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="c81a1-152">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c81a1-152">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="c81a1-153">`[ScaleUnit <String>]`: 눈금 단위 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c81a1-153">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="c81a1-154">`[ScaleUnitNode <String>]`: 배율 단위 노드의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c81a1-154">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="c81a1-155">`[SlbMuxInstance <String>]`: SLB MUX 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c81a1-155">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="c81a1-156">`[StorageSubSystem <String>]`: 저장소 시스템의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c81a1-156">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="c81a1-157">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="c81a1-157">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="c81a1-158">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="c81a1-158">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="c81a1-159">`[Volume <String>]`: 저장소 볼륨의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c81a1-159">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="c81a1-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c81a1-160">RELATED LINKS</span></span>

