---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsippool
schema: 2.0.0
ms.openlocfilehash: 532dcd2a91591b639b93b5b67851a4118457068b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876069"
---
# <span data-ttu-id="05acb-101">Get-AzsIPPool</span><span class="sxs-lookup"><span data-stu-id="05acb-101">Get-AzsIPPool</span></span>

## <span data-ttu-id="05acb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05acb-102">SYNOPSIS</span></span>
<span data-ttu-id="05acb-103">요청 된 IP 풀을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="05acb-103">Return the requested IP pool.</span></span>

## <span data-ttu-id="05acb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="05acb-104">SYNTAX</span></span>

### <span data-ttu-id="05acb-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="05acb-105">List (Default)</span></span>
```
Get-AzsIPPool [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="05acb-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="05acb-106">Get</span></span>
```
Get-AzsIPPool -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="05acb-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="05acb-107">GetViaIdentity</span></span>
```
Get-AzsIPPool -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="05acb-108">설명은</span><span class="sxs-lookup"><span data-stu-id="05acb-108">DESCRIPTION</span></span>
<span data-ttu-id="05acb-109">요청 된 IP 풀을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="05acb-109">Return the requested IP pool.</span></span>

## <span data-ttu-id="05acb-110">예제의</span><span class="sxs-lookup"><span data-stu-id="05acb-110">EXAMPLES</span></span>

### <span data-ttu-id="05acb-111">예제 1:</span><span class="sxs-lookup"><span data-stu-id="05acb-111">Example 1:</span></span> 
```powershell
PS C:\> Get-AzsIpPool

Return an all infrastructure ip pools.
```

<span data-ttu-id="05acb-112">모든 인프라 ip 풀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="05acb-112">Get an all infrastructure ip pools.</span></span>

### <span data-ttu-id="05acb-113">예제 2:</span><span class="sxs-lookup"><span data-stu-id="05acb-113">Example 2:</span></span> 
```powershell
PS C:\> Get-AzsIpPool -Name "08786a0f-ad8c-43aa-a154-06083abfc1ac"

Get an infrastructure ip pool based on name.
```

<span data-ttu-id="05acb-114">이름을 기반으로 하는 인프라 ip 풀을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="05acb-114">Get an infrastructure ip pool based on name.</span></span>

## <span data-ttu-id="05acb-115">변수</span><span class="sxs-lookup"><span data-stu-id="05acb-115">PARAMETERS</span></span>

### <span data-ttu-id="05acb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05acb-116">-DefaultProfile</span></span>


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

### <span data-ttu-id="05acb-117">-필터</span><span class="sxs-lookup"><span data-stu-id="05acb-117">-Filter</span></span>
<span data-ttu-id="05acb-118">OData 필터 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="05acb-118">OData filter parameter.</span></span>

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

### <span data-ttu-id="05acb-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05acb-119">-InputObject</span></span>
<span data-ttu-id="05acb-120">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="05acb-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="05acb-121">-위치</span><span class="sxs-lookup"><span data-stu-id="05acb-121">-Location</span></span>
<span data-ttu-id="05acb-122">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="05acb-122">Location of the resource.</span></span>

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

### <span data-ttu-id="05acb-123">-이름</span><span class="sxs-lookup"><span data-stu-id="05acb-123">-Name</span></span>
<span data-ttu-id="05acb-124">IP 풀 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="05acb-124">IP pool name.</span></span>

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

### <span data-ttu-id="05acb-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="05acb-125">-PassThru</span></span>
<span data-ttu-id="05acb-126">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="05acb-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="05acb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05acb-127">-ResourceGroupName</span></span>
<span data-ttu-id="05acb-128">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="05acb-128">Name of the resource group.</span></span>

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

### <span data-ttu-id="05acb-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="05acb-129">-SubscriptionId</span></span>
<span data-ttu-id="05acb-130">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="05acb-130">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="05acb-131">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="05acb-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="05acb-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05acb-132">CommonParameters</span></span>
<span data-ttu-id="05acb-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="05acb-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05acb-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="05acb-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05acb-135">입력</span><span class="sxs-lookup"><span data-stu-id="05acb-135">INPUTS</span></span>

### <span data-ttu-id="05acb-136">FabricAdmin. IFabricAdminIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="05acb-136">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="05acb-137">출력</span><span class="sxs-lookup"><span data-stu-id="05acb-137">OUTPUTS</span></span>

### <span data-ttu-id="05acb-138">FabricAdmin. PowerShell. Api20160501. IIPPool</span><span class="sxs-lookup"><span data-stu-id="05acb-138">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IIPPool</span></span>



## <span data-ttu-id="05acb-139">상속자</span><span class="sxs-lookup"><span data-stu-id="05acb-139">NOTES</span></span>

<span data-ttu-id="05acb-140">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="05acb-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="05acb-141">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="05acb-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="05acb-142">INPUTOBJECT <IFabricAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="05acb-142">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="05acb-143">`[Drive <String>]`: 저장소 드라이브의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="05acb-143">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="05acb-144">`[EdgeGateway <String>]`: Edge 게이트웨이의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="05acb-144">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="05acb-145">`[EdgeGatewayPool <String>]`: Edge 게이트웨이 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="05acb-145">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="05acb-146">`[FabricLocation <String>]`: 패브릭 위치.</span><span class="sxs-lookup"><span data-stu-id="05acb-146">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="05acb-147">`[FileShare <String>]`: 패브릭 파일 공유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="05acb-147">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="05acb-148">`[IPPool <String>]`: IP 풀 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="05acb-148">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="05acb-149">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="05acb-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="05acb-150">`[InfraRole <String>]`: 인프라 역할 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="05acb-150">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="05acb-151">`[InfraRoleInstance <String>]`: 인프라 역할 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="05acb-151">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="05acb-152">`[Location <String>]`: 리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="05acb-152">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="05acb-153">`[LogicalNetwork <String>]`: 논리 네트워크의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="05acb-153">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="05acb-154">`[LogicalSubnet <String>]`: 논리 서브넷의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="05acb-154">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="05acb-155">`[MacAddressPool <String>]`: MAC 주소 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="05acb-155">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="05acb-156">`[Operation <String>]`: 작업 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="05acb-156">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="05acb-157">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="05acb-157">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="05acb-158">`[ScaleUnit <String>]`: 눈금 단위 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="05acb-158">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="05acb-159">`[ScaleUnitNode <String>]`: 배율 단위 노드의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="05acb-159">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="05acb-160">`[SlbMuxInstance <String>]`: SLB MUX 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="05acb-160">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="05acb-161">`[StoragePool <String>]`: 저장소 풀 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="05acb-161">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="05acb-162">`[StorageSubSystem <String>]`: 저장소 시스템의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="05acb-162">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="05acb-163">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="05acb-163">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="05acb-164">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="05acb-164">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="05acb-165">`[Volume <String>]`: 저장소 볼륨의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="05acb-165">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="05acb-166">관련 링크</span><span class="sxs-lookup"><span data-stu-id="05acb-166">RELATED LINKS</span></span>

