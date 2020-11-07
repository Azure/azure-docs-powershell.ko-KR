---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: d1534c7cfacbcc70c2fe822676d67142401f9ff9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876063"
---
# <span data-ttu-id="7c47a-101">Get-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="7c47a-101">Get-AzsScaleUnitNode</span></span>

## <span data-ttu-id="7c47a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c47a-102">SYNOPSIS</span></span>


## <span data-ttu-id="7c47a-103">구문과</span><span class="sxs-lookup"><span data-stu-id="7c47a-103">SYNTAX</span></span>

### <span data-ttu-id="7c47a-104">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="7c47a-104">List (Default)</span></span>
```
Get-AzsScaleUnitNode [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="7c47a-105">가져오기</span><span class="sxs-lookup"><span data-stu-id="7c47a-105">Get</span></span>
```
Get-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="7c47a-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7c47a-106">GetViaIdentity</span></span>
```
Get-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="7c47a-107">설명은</span><span class="sxs-lookup"><span data-stu-id="7c47a-107">DESCRIPTION</span></span>


## <span data-ttu-id="7c47a-108">예제의</span><span class="sxs-lookup"><span data-stu-id="7c47a-108">EXAMPLES</span></span>

### <span data-ttu-id="7c47a-109">예제 1:</span><span class="sxs-lookup"><span data-stu-id="7c47a-109">Example 1:</span></span>
```powershell
PS C:\> Get-AzsScaleUnitNode

A list of all scale unit nodes at a location.
```

<span data-ttu-id="7c47a-110">위치에서 모든 배율 단위 노드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7c47a-110">Get all scale unit nodes at a location.</span></span>

### <span data-ttu-id="7c47a-111">예제 2:</span><span class="sxs-lookup"><span data-stu-id="7c47a-111">Example 2:</span></span>
```powershell
PS C:\> Get-AzsScaleUnitNode -Name "HC1n25r2231"

A specific scale unit node at a location given a name.
```

<span data-ttu-id="7c47a-112">이름이 지정 된 위치에서 특정 배율 단위 노드를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7c47a-112">Get a specific scale unit node at a location given a name.</span></span>

## <span data-ttu-id="7c47a-113">변수</span><span class="sxs-lookup"><span data-stu-id="7c47a-113">PARAMETERS</span></span>

### <span data-ttu-id="7c47a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c47a-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="7c47a-115">-필터</span><span class="sxs-lookup"><span data-stu-id="7c47a-115">-Filter</span></span>


```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7c47a-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7c47a-116">-InputObject</span></span>
<span data-ttu-id="7c47a-117">생성 하려면 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7c47a-117">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="7c47a-118">-위치</span><span class="sxs-lookup"><span data-stu-id="7c47a-118">-Location</span></span>


```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7c47a-119">-이름</span><span class="sxs-lookup"><span data-stu-id="7c47a-119">-Name</span></span>


```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7c47a-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7c47a-120">-PassThru</span></span>


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

### <span data-ttu-id="7c47a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c47a-121">-ResourceGroupName</span></span>


```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7c47a-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7c47a-122">-SubscriptionId</span></span>


```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="7c47a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c47a-123">CommonParameters</span></span>
<span data-ttu-id="7c47a-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c47a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c47a-125">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7c47a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c47a-126">입력</span><span class="sxs-lookup"><span data-stu-id="7c47a-126">INPUTS</span></span>

### <span data-ttu-id="7c47a-127">FabricAdmin. IFabricAdminIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="7c47a-127">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="7c47a-128">출력</span><span class="sxs-lookup"><span data-stu-id="7c47a-128">OUTPUTS</span></span>

### <span data-ttu-id="7c47a-129">FabricAdmin. Api20160501. IScaleUnitNode에 대 한</span><span class="sxs-lookup"><span data-stu-id="7c47a-129">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IScaleUnitNode</span></span>



## <span data-ttu-id="7c47a-130">상속자</span><span class="sxs-lookup"><span data-stu-id="7c47a-130">NOTES</span></span>

<span data-ttu-id="7c47a-131">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c47a-131">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7c47a-132">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="7c47a-132">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="7c47a-133">INPUTOBJECT <IFabricAdminIdentity> :</span><span class="sxs-lookup"><span data-stu-id="7c47a-133">INPUTOBJECT <IFabricAdminIdentity>:</span></span> 
  - <span data-ttu-id="7c47a-134">`[Drive <String>]`: 저장소 드라이브의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c47a-134">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="7c47a-135">`[EdgeGateway <String>]`: Edge 게이트웨이의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c47a-135">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="7c47a-136">`[EdgeGatewayPool <String>]`: Edge 게이트웨이 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c47a-136">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="7c47a-137">`[FabricLocation <String>]`: 패브릭 위치.</span><span class="sxs-lookup"><span data-stu-id="7c47a-137">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="7c47a-138">`[FileShare <String>]`: 패브릭 파일 공유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c47a-138">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="7c47a-139">`[IPPool <String>]`: IP 풀 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c47a-139">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="7c47a-140">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="7c47a-140">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7c47a-141">`[InfraRole <String>]`: 인프라 역할 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c47a-141">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="7c47a-142">`[InfraRoleInstance <String>]`: 인프라 역할 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c47a-142">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="7c47a-143">`[Location <String>]`: 리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="7c47a-143">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="7c47a-144">`[LogicalNetwork <String>]`: 논리 네트워크의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c47a-144">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="7c47a-145">`[LogicalSubnet <String>]`: 논리 서브넷의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c47a-145">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="7c47a-146">`[MacAddressPool <String>]`: MAC 주소 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c47a-146">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="7c47a-147">`[Operation <String>]`: 작업 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="7c47a-147">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="7c47a-148">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c47a-148">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="7c47a-149">`[ScaleUnit <String>]`: 눈금 단위 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c47a-149">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="7c47a-150">`[ScaleUnitNode <String>]`: 배율 단위 노드의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c47a-150">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="7c47a-151">`[SlbMuxInstance <String>]`: SLB MUX 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c47a-151">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="7c47a-152">`[StorageSubSystem <String>]`: 저장소 시스템의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c47a-152">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="7c47a-153">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="7c47a-153">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="7c47a-154">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="7c47a-154">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="7c47a-155">`[Volume <String>]`: 저장소 볼륨의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7c47a-155">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="7c47a-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7c47a-156">RELATED LINKS</span></span>

