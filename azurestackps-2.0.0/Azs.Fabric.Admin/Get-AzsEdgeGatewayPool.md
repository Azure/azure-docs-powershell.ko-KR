---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsedgegatewaypool
schema: 2.0.0
ms.openlocfilehash: 79b4ae3a4bd3807b08ea45be9a9a328455f03b67
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876077"
---
# <span data-ttu-id="e181b-101">Get-AzsEdgeGatewayPool</span><span class="sxs-lookup"><span data-stu-id="e181b-101">Get-AzsEdgeGatewayPool</span></span>

## <span data-ttu-id="e181b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e181b-102">SYNOPSIS</span></span>


## <span data-ttu-id="e181b-103">구문과</span><span class="sxs-lookup"><span data-stu-id="e181b-103">SYNTAX</span></span>

### <span data-ttu-id="e181b-104">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="e181b-104">List (Default)</span></span>
```
Get-AzsEdgeGatewayPool [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="e181b-105">가져오기</span><span class="sxs-lookup"><span data-stu-id="e181b-105">Get</span></span>
```
Get-AzsEdgeGatewayPool -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="e181b-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e181b-106">GetViaIdentity</span></span>
```
Get-AzsEdgeGatewayPool -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="e181b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e181b-107">DESCRIPTION</span></span>


## <span data-ttu-id="e181b-108">예제의</span><span class="sxs-lookup"><span data-stu-id="e181b-108">EXAMPLES</span></span>

### <span data-ttu-id="e181b-109">예제 1: 모든 Edge 게이트웨이 풀 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e181b-109">Example 1: Get a list of all Edge Gateway pools.</span></span>
```powershell
PS C:\> Get-AzsEdgeGatewayPool

Return a list of all Edge Gateway pools.
```

<span data-ttu-id="e181b-110">모든 Edge 게이트웨이 풀의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e181b-110">Get a list of all Edge Gateway pools.</span></span>

### <span data-ttu-id="e181b-111">예제 2: 특정 edge 게이트웨이 풀 가져오기</span><span class="sxs-lookup"><span data-stu-id="e181b-111">Example 2: Get a specific edge gateway pool.</span></span>
```powershell
PS C:\> Get-AzsEdgeGatewayPool

Return a specific edge gateway pool.
```

<span data-ttu-id="e181b-112">특정 edge 게이트웨이 풀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e181b-112">Get a specific edge gateway pool.</span></span>

## <span data-ttu-id="e181b-113">변수</span><span class="sxs-lookup"><span data-stu-id="e181b-113">PARAMETERS</span></span>

### <span data-ttu-id="e181b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e181b-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="e181b-115">-필터</span><span class="sxs-lookup"><span data-stu-id="e181b-115">-Filter</span></span>


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

### <span data-ttu-id="e181b-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e181b-116">-InputObject</span></span>
<span data-ttu-id="e181b-117">생성 하려면 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e181b-117">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e181b-118">-위치</span><span class="sxs-lookup"><span data-stu-id="e181b-118">-Location</span></span>


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

### <span data-ttu-id="e181b-119">-이름</span><span class="sxs-lookup"><span data-stu-id="e181b-119">-Name</span></span>


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

### <span data-ttu-id="e181b-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e181b-120">-PassThru</span></span>


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

### <span data-ttu-id="e181b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e181b-121">-ResourceGroupName</span></span>


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

### <span data-ttu-id="e181b-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e181b-122">-SubscriptionId</span></span>


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

### <span data-ttu-id="e181b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e181b-123">CommonParameters</span></span>
<span data-ttu-id="e181b-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e181b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e181b-125">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e181b-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e181b-126">입력</span><span class="sxs-lookup"><span data-stu-id="e181b-126">INPUTS</span></span>

### <span data-ttu-id="e181b-127">FabricAdmin. IFabricAdminIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="e181b-127">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="e181b-128">출력</span><span class="sxs-lookup"><span data-stu-id="e181b-128">OUTPUTS</span></span>

### <span data-ttu-id="e181b-129">FabricAdmin. Api20160501. IEdgeGatewayPool에 대 한</span><span class="sxs-lookup"><span data-stu-id="e181b-129">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IEdgeGatewayPool</span></span>



## <span data-ttu-id="e181b-130">상속자</span><span class="sxs-lookup"><span data-stu-id="e181b-130">NOTES</span></span>

<span data-ttu-id="e181b-131">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e181b-131">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e181b-132">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="e181b-132">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="e181b-133">INPUTOBJECT <IFabricAdminIdentity> :</span><span class="sxs-lookup"><span data-stu-id="e181b-133">INPUTOBJECT <IFabricAdminIdentity>:</span></span> 
  - <span data-ttu-id="e181b-134">`[Drive <String>]`: 저장소 드라이브의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e181b-134">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="e181b-135">`[EdgeGateway <String>]`: Edge 게이트웨이의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e181b-135">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="e181b-136">`[EdgeGatewayPool <String>]`: Edge 게이트웨이 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e181b-136">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="e181b-137">`[FabricLocation <String>]`: 패브릭 위치.</span><span class="sxs-lookup"><span data-stu-id="e181b-137">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="e181b-138">`[FileShare <String>]`: 패브릭 파일 공유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e181b-138">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="e181b-139">`[IPPool <String>]`: IP 풀 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e181b-139">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="e181b-140">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="e181b-140">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e181b-141">`[InfraRole <String>]`: 인프라 역할 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e181b-141">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="e181b-142">`[InfraRoleInstance <String>]`: 인프라 역할 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e181b-142">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="e181b-143">`[Location <String>]`: 리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="e181b-143">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="e181b-144">`[LogicalNetwork <String>]`: 논리 네트워크의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e181b-144">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="e181b-145">`[LogicalSubnet <String>]`: 논리 서브넷의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e181b-145">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="e181b-146">`[MacAddressPool <String>]`: MAC 주소 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e181b-146">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="e181b-147">`[Operation <String>]`: 작업 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="e181b-147">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="e181b-148">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e181b-148">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="e181b-149">`[ScaleUnit <String>]`: 눈금 단위 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e181b-149">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="e181b-150">`[ScaleUnitNode <String>]`: 배율 단위 노드의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e181b-150">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="e181b-151">`[SlbMuxInstance <String>]`: SLB MUX 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e181b-151">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="e181b-152">`[StorageSubSystem <String>]`: 저장소 시스템의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e181b-152">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="e181b-153">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="e181b-153">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e181b-154">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e181b-154">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="e181b-155">`[Volume <String>]`: 저장소 볼륨의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e181b-155">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="e181b-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e181b-156">RELATED LINKS</span></span>

