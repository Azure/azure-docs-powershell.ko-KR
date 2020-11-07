---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsinfrastructurelocation
schema: 2.0.0
ms.openlocfilehash: 0d0f2856503943d19653dd09a8cb1c125fec9517
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876066"
---
# <span data-ttu-id="a9bae-101">Get-AzsInfrastructureLocation</span><span class="sxs-lookup"><span data-stu-id="a9bae-101">Get-AzsInfrastructureLocation</span></span>

## <span data-ttu-id="a9bae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9bae-102">SYNOPSIS</span></span>
<span data-ttu-id="a9bae-103">요청 된 패브릭 위치를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9bae-103">Returns the requested fabric location.</span></span>

## <span data-ttu-id="a9bae-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a9bae-104">SYNTAX</span></span>

### <span data-ttu-id="a9bae-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="a9bae-105">List (Default)</span></span>
```
Get-AzsInfrastructureLocation [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a9bae-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="a9bae-106">Get</span></span>
```
Get-AzsInfrastructureLocation -FabricLocation <String> [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="a9bae-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a9bae-107">GetViaIdentity</span></span>
```
Get-AzsInfrastructureLocation -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="a9bae-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a9bae-108">DESCRIPTION</span></span>
<span data-ttu-id="a9bae-109">요청 된 패브릭 위치를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9bae-109">Returns the requested fabric location.</span></span>

## <span data-ttu-id="a9bae-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a9bae-110">EXAMPLES</span></span>

### <span data-ttu-id="a9bae-111">예제 1:</span><span class="sxs-lookup"><span data-stu-id="a9bae-111">Example 1:</span></span> 
```powershell
PS C:\> Get-AzsInfrastructureLocation

Return a list of all fabric locations.
```

<span data-ttu-id="a9bae-112">모든 패브릭 위치 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a9bae-112">Get a list of all fabric locations.</span></span>

### <span data-ttu-id="a9bae-113">예제 2:</span><span class="sxs-lookup"><span data-stu-id="a9bae-113">Example 2:</span></span> 
```powershell
PS C:\> Get-AzsInfrastructureLocation -Location "local"

Return a location based on the name.
```

<span data-ttu-id="a9bae-114">이름을 기준으로 위치를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a9bae-114">Get a location based on the name.</span></span>

## <span data-ttu-id="a9bae-115">변수</span><span class="sxs-lookup"><span data-stu-id="a9bae-115">PARAMETERS</span></span>

### <span data-ttu-id="a9bae-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9bae-116">-DefaultProfile</span></span>
<span data-ttu-id="a9bae-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a9bae-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9bae-118">-FabricLocation</span><span class="sxs-lookup"><span data-stu-id="a9bae-118">-FabricLocation</span></span>
<span data-ttu-id="a9bae-119">패브릭 위치.</span><span class="sxs-lookup"><span data-stu-id="a9bae-119">Fabric location.</span></span>

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

### <span data-ttu-id="a9bae-120">-필터</span><span class="sxs-lookup"><span data-stu-id="a9bae-120">-Filter</span></span>
<span data-ttu-id="a9bae-121">OData 필터 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="a9bae-121">OData filter parameter.</span></span>

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

### <span data-ttu-id="a9bae-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a9bae-122">-InputObject</span></span>
<span data-ttu-id="a9bae-123">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a9bae-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a9bae-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a9bae-124">-PassThru</span></span>
<span data-ttu-id="a9bae-125">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9bae-125">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Get, GetViaIdentity
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a9bae-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9bae-126">-ResourceGroupName</span></span>
<span data-ttu-id="a9bae-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a9bae-127">Name of the resource group.</span></span>

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

### <span data-ttu-id="a9bae-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a9bae-128">-SubscriptionId</span></span>
<span data-ttu-id="a9bae-129">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="a9bae-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a9bae-130">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9bae-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a9bae-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9bae-131">CommonParameters</span></span>
<span data-ttu-id="a9bae-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9bae-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9bae-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a9bae-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9bae-134">입력</span><span class="sxs-lookup"><span data-stu-id="a9bae-134">INPUTS</span></span>

### <span data-ttu-id="a9bae-135">FabricAdmin. IFabricAdminIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="a9bae-135">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="a9bae-136">출력</span><span class="sxs-lookup"><span data-stu-id="a9bae-136">OUTPUTS</span></span>

### <span data-ttu-id="a9bae-137">FabricAdmin. Api20160501. IFabricLocation에 대 한</span><span class="sxs-lookup"><span data-stu-id="a9bae-137">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IFabricLocation</span></span>



## <span data-ttu-id="a9bae-138">상속자</span><span class="sxs-lookup"><span data-stu-id="a9bae-138">NOTES</span></span>

<span data-ttu-id="a9bae-139">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9bae-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a9bae-140">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="a9bae-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="a9bae-141">INPUTOBJECT <IFabricAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="a9bae-141">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a9bae-142">`[Drive <String>]`: 저장소 드라이브의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a9bae-142">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="a9bae-143">`[EdgeGateway <String>]`: Edge 게이트웨이의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a9bae-143">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="a9bae-144">`[EdgeGatewayPool <String>]`: Edge 게이트웨이 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a9bae-144">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="a9bae-145">`[FabricLocation <String>]`: 패브릭 위치.</span><span class="sxs-lookup"><span data-stu-id="a9bae-145">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="a9bae-146">`[FileShare <String>]`: 패브릭 파일 공유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a9bae-146">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="a9bae-147">`[IPPool <String>]`: IP 풀 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a9bae-147">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="a9bae-148">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="a9bae-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a9bae-149">`[InfraRole <String>]`: 인프라 역할 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a9bae-149">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="a9bae-150">`[InfraRoleInstance <String>]`: 인프라 역할 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a9bae-150">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="a9bae-151">`[Location <String>]`: 리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="a9bae-151">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="a9bae-152">`[LogicalNetwork <String>]`: 논리 네트워크의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a9bae-152">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="a9bae-153">`[LogicalSubnet <String>]`: 논리 서브넷의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a9bae-153">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="a9bae-154">`[MacAddressPool <String>]`: MAC 주소 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a9bae-154">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="a9bae-155">`[Operation <String>]`: 작업 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="a9bae-155">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="a9bae-156">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a9bae-156">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="a9bae-157">`[ScaleUnit <String>]`: 눈금 단위 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a9bae-157">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="a9bae-158">`[ScaleUnitNode <String>]`: 배율 단위 노드의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a9bae-158">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="a9bae-159">`[SlbMuxInstance <String>]`: SLB MUX 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a9bae-159">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="a9bae-160">`[StorageSubSystem <String>]`: 저장소 시스템의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a9bae-160">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="a9bae-161">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="a9bae-161">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a9bae-162">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9bae-162">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="a9bae-163">`[Volume <String>]`: 저장소 볼륨의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a9bae-163">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="a9bae-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a9bae-164">RELATED LINKS</span></span>

