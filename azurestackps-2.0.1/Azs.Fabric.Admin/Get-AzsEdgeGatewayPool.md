---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsedgegatewaypool
schema: 2.0.0
ms.openlocfilehash: 79b4ae3a4bd3807b08ea45be9a9a328455f03b67
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/24/2020
ms.locfileid: "94045321"
---
# <span data-ttu-id="ea62f-101">Get-AzsEdgeGatewayPool</span><span class="sxs-lookup"><span data-stu-id="ea62f-101">Get-AzsEdgeGatewayPool</span></span>

## <span data-ttu-id="ea62f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea62f-102">SYNOPSIS</span></span>


## <span data-ttu-id="ea62f-103">구문과</span><span class="sxs-lookup"><span data-stu-id="ea62f-103">SYNTAX</span></span>

### <span data-ttu-id="ea62f-104">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="ea62f-104">List (Default)</span></span>
```
Get-AzsEdgeGatewayPool [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="ea62f-105">가져오기</span><span class="sxs-lookup"><span data-stu-id="ea62f-105">Get</span></span>
```
Get-AzsEdgeGatewayPool -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="ea62f-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ea62f-106">GetViaIdentity</span></span>
```
Get-AzsEdgeGatewayPool -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="ea62f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ea62f-107">DESCRIPTION</span></span>


## <span data-ttu-id="ea62f-108">예제의</span><span class="sxs-lookup"><span data-stu-id="ea62f-108">EXAMPLES</span></span>

### <span data-ttu-id="ea62f-109">예제 1: 모든 Edge 게이트웨이 풀 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ea62f-109">Example 1: Get a list of all Edge Gateway pools.</span></span>
```powershell
PS C:\> Get-AzsEdgeGatewayPool

Return a list of all Edge Gateway pools.
```

<span data-ttu-id="ea62f-110">모든 Edge 게이트웨이 풀의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ea62f-110">Get a list of all Edge Gateway pools.</span></span>

### <span data-ttu-id="ea62f-111">예제 2: 특정 edge 게이트웨이 풀 가져오기</span><span class="sxs-lookup"><span data-stu-id="ea62f-111">Example 2: Get a specific edge gateway pool.</span></span>
```powershell
PS C:\> Get-AzsEdgeGatewayPool

Return a specific edge gateway pool.
```

<span data-ttu-id="ea62f-112">특정 edge 게이트웨이 풀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ea62f-112">Get a specific edge gateway pool.</span></span>

## <span data-ttu-id="ea62f-113">변수</span><span class="sxs-lookup"><span data-stu-id="ea62f-113">PARAMETERS</span></span>

### <span data-ttu-id="ea62f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea62f-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="ea62f-115">-필터</span><span class="sxs-lookup"><span data-stu-id="ea62f-115">-Filter</span></span>


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

### <span data-ttu-id="ea62f-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea62f-116">-InputObject</span></span>
<span data-ttu-id="ea62f-117">생성 하려면 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ea62f-117">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="ea62f-118">-위치</span><span class="sxs-lookup"><span data-stu-id="ea62f-118">-Location</span></span>


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

### <span data-ttu-id="ea62f-119">-이름</span><span class="sxs-lookup"><span data-stu-id="ea62f-119">-Name</span></span>


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

### <span data-ttu-id="ea62f-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ea62f-120">-PassThru</span></span>


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

### <span data-ttu-id="ea62f-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea62f-121">-ResourceGroupName</span></span>


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

### <span data-ttu-id="ea62f-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ea62f-122">-SubscriptionId</span></span>


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

### <span data-ttu-id="ea62f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea62f-123">CommonParameters</span></span>
<span data-ttu-id="ea62f-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea62f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea62f-125">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ea62f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea62f-126">입력</span><span class="sxs-lookup"><span data-stu-id="ea62f-126">INPUTS</span></span>

### <span data-ttu-id="ea62f-127">FabricAdmin. IFabricAdminIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="ea62f-127">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="ea62f-128">출력</span><span class="sxs-lookup"><span data-stu-id="ea62f-128">OUTPUTS</span></span>

### <span data-ttu-id="ea62f-129">FabricAdmin. Api20160501. IEdgeGatewayPool에 대 한</span><span class="sxs-lookup"><span data-stu-id="ea62f-129">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IEdgeGatewayPool</span></span>



## <span data-ttu-id="ea62f-130">상속자</span><span class="sxs-lookup"><span data-stu-id="ea62f-130">NOTES</span></span>

<span data-ttu-id="ea62f-131">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea62f-131">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ea62f-132">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="ea62f-132">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="ea62f-133">INPUTOBJECT <IFabricAdminIdentity> :</span><span class="sxs-lookup"><span data-stu-id="ea62f-133">INPUTOBJECT <IFabricAdminIdentity>:</span></span> 
  - <span data-ttu-id="ea62f-134">`[Drive <String>]`: 저장소 드라이브의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea62f-134">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="ea62f-135">`[EdgeGateway <String>]`: Edge 게이트웨이의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea62f-135">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="ea62f-136">`[EdgeGatewayPool <String>]`: Edge 게이트웨이 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea62f-136">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="ea62f-137">`[FabricLocation <String>]`: 패브릭 위치.</span><span class="sxs-lookup"><span data-stu-id="ea62f-137">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="ea62f-138">`[FileShare <String>]`: 패브릭 파일 공유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea62f-138">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="ea62f-139">`[IPPool <String>]`: IP 풀 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea62f-139">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="ea62f-140">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="ea62f-140">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ea62f-141">`[InfraRole <String>]`: 인프라 역할 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea62f-141">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="ea62f-142">`[InfraRoleInstance <String>]`: 인프라 역할 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea62f-142">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="ea62f-143">`[Location <String>]`: 리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="ea62f-143">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="ea62f-144">`[LogicalNetwork <String>]`: 논리 네트워크의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea62f-144">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="ea62f-145">`[LogicalSubnet <String>]`: 논리 서브넷의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea62f-145">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="ea62f-146">`[MacAddressPool <String>]`: MAC 주소 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea62f-146">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="ea62f-147">`[Operation <String>]`: 작업 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="ea62f-147">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="ea62f-148">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea62f-148">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="ea62f-149">`[ScaleUnit <String>]`: 눈금 단위 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea62f-149">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="ea62f-150">`[ScaleUnitNode <String>]`: 배율 단위 노드의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea62f-150">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="ea62f-151">`[SlbMuxInstance <String>]`: SLB MUX 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea62f-151">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="ea62f-152">`[StorageSubSystem <String>]`: 저장소 시스템의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea62f-152">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="ea62f-153">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="ea62f-153">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ea62f-154">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea62f-154">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="ea62f-155">`[Volume <String>]`: 저장소 볼륨의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ea62f-155">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="ea62f-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ea62f-156">RELATED LINKS</span></span>

