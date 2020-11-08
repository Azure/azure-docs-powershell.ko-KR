---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsedgegateway
schema: 2.0.0
ms.openlocfilehash: a9c883fab422252aad167d92da3adf55edd9a78b
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94046625"
---
# <span data-ttu-id="afd58-101">Get-AzsEdgeGateway</span><span class="sxs-lookup"><span data-stu-id="afd58-101">Get-AzsEdgeGateway</span></span>

## <span data-ttu-id="afd58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afd58-102">SYNOPSIS</span></span>
<span data-ttu-id="afd58-103">요청 된 edge 게이트웨이를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="afd58-103">Returns the requested edge gateway.</span></span>

## <span data-ttu-id="afd58-104">구문과</span><span class="sxs-lookup"><span data-stu-id="afd58-104">SYNTAX</span></span>

### <span data-ttu-id="afd58-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="afd58-105">List (Default)</span></span>
```
Get-AzsEdgeGateway [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="afd58-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="afd58-106">Get</span></span>
```
Get-AzsEdgeGateway -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="afd58-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="afd58-107">GetViaIdentity</span></span>
```
Get-AzsEdgeGateway -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="afd58-108">설명은</span><span class="sxs-lookup"><span data-stu-id="afd58-108">DESCRIPTION</span></span>
<span data-ttu-id="afd58-109">요청 된 edge 게이트웨이를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="afd58-109">Returns the requested edge gateway.</span></span>

## <span data-ttu-id="afd58-110">예제의</span><span class="sxs-lookup"><span data-stu-id="afd58-110">EXAMPLES</span></span>

### <span data-ttu-id="afd58-111">예제 1:</span><span class="sxs-lookup"><span data-stu-id="afd58-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsEdgeGateway

Get a list of all edge gateways.
```

<span data-ttu-id="afd58-112">특정 위치에 있는 모든 edge 게이트웨이의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="afd58-112">Returns the list of all edge gateways at a certain location.</span></span>


## <span data-ttu-id="afd58-113">변수</span><span class="sxs-lookup"><span data-stu-id="afd58-113">PARAMETERS</span></span>

### <span data-ttu-id="afd58-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afd58-114">-DefaultProfile</span></span>
<span data-ttu-id="afd58-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="afd58-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="afd58-116">-필터</span><span class="sxs-lookup"><span data-stu-id="afd58-116">-Filter</span></span>
<span data-ttu-id="afd58-117">OData 필터 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="afd58-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="afd58-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="afd58-118">-InputObject</span></span>
<span data-ttu-id="afd58-119">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="afd58-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="afd58-120">-위치</span><span class="sxs-lookup"><span data-stu-id="afd58-120">-Location</span></span>
<span data-ttu-id="afd58-121">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="afd58-121">Location of the resource.</span></span>

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

### <span data-ttu-id="afd58-122">-이름</span><span class="sxs-lookup"><span data-stu-id="afd58-122">-Name</span></span>
<span data-ttu-id="afd58-123">Edge 게이트웨이의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afd58-123">Name of the edge gateway.</span></span>

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

### <span data-ttu-id="afd58-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="afd58-124">-PassThru</span></span>
<span data-ttu-id="afd58-125">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="afd58-125">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="afd58-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afd58-126">-ResourceGroupName</span></span>
<span data-ttu-id="afd58-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afd58-127">Name of the resource group.</span></span>

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

### <span data-ttu-id="afd58-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="afd58-128">-SubscriptionId</span></span>
<span data-ttu-id="afd58-129">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="afd58-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="afd58-130">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="afd58-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="afd58-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afd58-131">CommonParameters</span></span>
<span data-ttu-id="afd58-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="afd58-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afd58-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="afd58-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afd58-134">입력</span><span class="sxs-lookup"><span data-stu-id="afd58-134">INPUTS</span></span>

### <span data-ttu-id="afd58-135">FabricAdmin. IFabricAdminIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="afd58-135">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="afd58-136">출력</span><span class="sxs-lookup"><span data-stu-id="afd58-136">OUTPUTS</span></span>

### <span data-ttu-id="afd58-137">FabricAdmin. Api20160501. IEdgeGateway에 대 한</span><span class="sxs-lookup"><span data-stu-id="afd58-137">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IEdgeGateway</span></span>



## <span data-ttu-id="afd58-138">상속자</span><span class="sxs-lookup"><span data-stu-id="afd58-138">NOTES</span></span>

<span data-ttu-id="afd58-139">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="afd58-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="afd58-140">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="afd58-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="afd58-141">INPUTOBJECT <IFabricAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="afd58-141">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="afd58-142">`[Drive <String>]`: 저장소 드라이브의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afd58-142">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="afd58-143">`[EdgeGateway <String>]`: Edge 게이트웨이의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afd58-143">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="afd58-144">`[EdgeGatewayPool <String>]`: Edge 게이트웨이 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afd58-144">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="afd58-145">`[FabricLocation <String>]`: 패브릭 위치.</span><span class="sxs-lookup"><span data-stu-id="afd58-145">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="afd58-146">`[FileShare <String>]`: 패브릭 파일 공유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afd58-146">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="afd58-147">`[IPPool <String>]`: IP 풀 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afd58-147">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="afd58-148">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="afd58-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="afd58-149">`[InfraRole <String>]`: 인프라 역할 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afd58-149">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="afd58-150">`[InfraRoleInstance <String>]`: 인프라 역할 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afd58-150">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="afd58-151">`[Location <String>]`: 리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="afd58-151">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="afd58-152">`[LogicalNetwork <String>]`: 논리 네트워크의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afd58-152">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="afd58-153">`[LogicalSubnet <String>]`: 논리 서브넷의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afd58-153">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="afd58-154">`[MacAddressPool <String>]`: MAC 주소 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afd58-154">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="afd58-155">`[Operation <String>]`: 작업 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="afd58-155">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="afd58-156">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afd58-156">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="afd58-157">`[ScaleUnit <String>]`: 눈금 단위 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afd58-157">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="afd58-158">`[ScaleUnitNode <String>]`: 배율 단위 노드의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afd58-158">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="afd58-159">`[SlbMuxInstance <String>]`: SLB MUX 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afd58-159">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="afd58-160">`[StoragePool <String>]`: 저장소 풀 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afd58-160">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="afd58-161">`[StorageSubSystem <String>]`: 저장소 시스템의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afd58-161">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="afd58-162">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="afd58-162">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="afd58-163">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="afd58-163">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="afd58-164">`[Volume <String>]`: 저장소 볼륨의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="afd58-164">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="afd58-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="afd58-165">RELATED LINKS</span></span>

