---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsslbmuxinstance
schema: 2.0.0
ms.openlocfilehash: 64e33236bbdd3f07969f6633356c98b593ee672f
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/24/2020
ms.locfileid: "94045307"
---
# <span data-ttu-id="24277-101">Get-AzsSlbMuxInstance</span><span class="sxs-lookup"><span data-stu-id="24277-101">Get-AzsSlbMuxInstance</span></span>

## <span data-ttu-id="24277-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24277-102">SYNOPSIS</span></span>
<span data-ttu-id="24277-103">요청 된 소프트웨어 부하 분산 장치 멀티플렉서 인스턴스를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="24277-103">Returns the requested software load balancer multiplexer instance.</span></span>

## <span data-ttu-id="24277-104">구문과</span><span class="sxs-lookup"><span data-stu-id="24277-104">SYNTAX</span></span>

### <span data-ttu-id="24277-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="24277-105">List (Default)</span></span>
```
Get-AzsSlbMuxInstance [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="24277-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="24277-106">Get</span></span>
```
Get-AzsSlbMuxInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="24277-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="24277-107">GetViaIdentity</span></span>
```
Get-AzsSlbMuxInstance -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="24277-108">설명은</span><span class="sxs-lookup"><span data-stu-id="24277-108">DESCRIPTION</span></span>
<span data-ttu-id="24277-109">요청 된 소프트웨어 부하 분산 장치 멀티플렉서 인스턴스를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="24277-109">Returns the requested software load balancer multiplexer instance.</span></span>

## <span data-ttu-id="24277-110">예제의</span><span class="sxs-lookup"><span data-stu-id="24277-110">EXAMPLES</span></span>

### <span data-ttu-id="24277-111">예제 1:</span><span class="sxs-lookup"><span data-stu-id="24277-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsSlbMuxInstance

A list of all software load balancer multiplexer instance at a location.
```

<span data-ttu-id="24277-112">위치에 있는 모든 소프트웨어 부하 분산 장치 멀티플렉서 인스턴스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="24277-112">Get all software load balancer multiplexer instance at a location.</span></span>

### <span data-ttu-id="24277-113">예제 2:</span><span class="sxs-lookup"><span data-stu-id="24277-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsSlbMuxInstance -Name "AzS-SLB01"

A specific software load balancer multiplexer instance at a location given a name.
```

<span data-ttu-id="24277-114">이름에 주어진 위치에 특정 소프트웨어 부하 분산 장치 멀티플렉서 인스턴스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="24277-114">Get a specific software load balancer multiplexer instance at a location given a name.</span></span>

## <span data-ttu-id="24277-115">변수</span><span class="sxs-lookup"><span data-stu-id="24277-115">PARAMETERS</span></span>

### <span data-ttu-id="24277-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24277-116">-DefaultProfile</span></span>
<span data-ttu-id="24277-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="24277-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="24277-118">-필터</span><span class="sxs-lookup"><span data-stu-id="24277-118">-Filter</span></span>
<span data-ttu-id="24277-119">OData 필터 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="24277-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="24277-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24277-120">-InputObject</span></span>
<span data-ttu-id="24277-121">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="24277-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="24277-122">-위치</span><span class="sxs-lookup"><span data-stu-id="24277-122">-Location</span></span>
<span data-ttu-id="24277-123">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="24277-123">Location of the resource.</span></span>

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

### <span data-ttu-id="24277-124">-이름</span><span class="sxs-lookup"><span data-stu-id="24277-124">-Name</span></span>
<span data-ttu-id="24277-125">SLB MUX 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24277-125">Name of a SLB MUX instance.</span></span>

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

### <span data-ttu-id="24277-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="24277-126">-PassThru</span></span>
<span data-ttu-id="24277-127">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="24277-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="24277-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24277-128">-ResourceGroupName</span></span>
<span data-ttu-id="24277-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24277-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="24277-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="24277-130">-SubscriptionId</span></span>
<span data-ttu-id="24277-131">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="24277-131">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="24277-132">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="24277-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="24277-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24277-133">CommonParameters</span></span>
<span data-ttu-id="24277-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="24277-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24277-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="24277-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24277-136">입력</span><span class="sxs-lookup"><span data-stu-id="24277-136">INPUTS</span></span>

### <span data-ttu-id="24277-137">FabricAdmin. IFabricAdminIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="24277-137">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="24277-138">출력</span><span class="sxs-lookup"><span data-stu-id="24277-138">OUTPUTS</span></span>

### <span data-ttu-id="24277-139">FabricAdmin. Api20160501. ISlbMuxInstance에 대 한</span><span class="sxs-lookup"><span data-stu-id="24277-139">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.ISlbMuxInstance</span></span>



## <span data-ttu-id="24277-140">상속자</span><span class="sxs-lookup"><span data-stu-id="24277-140">NOTES</span></span>

<span data-ttu-id="24277-141">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="24277-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="24277-142">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="24277-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="24277-143">INPUTOBJECT <IFabricAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="24277-143">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="24277-144">`[Drive <String>]`: 저장소 드라이브의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24277-144">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="24277-145">`[EdgeGateway <String>]`: Edge 게이트웨이의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24277-145">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="24277-146">`[EdgeGatewayPool <String>]`: Edge 게이트웨이 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24277-146">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="24277-147">`[FabricLocation <String>]`: 패브릭 위치.</span><span class="sxs-lookup"><span data-stu-id="24277-147">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="24277-148">`[FileShare <String>]`: 패브릭 파일 공유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24277-148">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="24277-149">`[IPPool <String>]`: IP 풀 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24277-149">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="24277-150">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="24277-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="24277-151">`[InfraRole <String>]`: 인프라 역할 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24277-151">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="24277-152">`[InfraRoleInstance <String>]`: 인프라 역할 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24277-152">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="24277-153">`[Location <String>]`: 리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="24277-153">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="24277-154">`[LogicalNetwork <String>]`: 논리 네트워크의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24277-154">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="24277-155">`[LogicalSubnet <String>]`: 논리 서브넷의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24277-155">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="24277-156">`[MacAddressPool <String>]`: MAC 주소 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24277-156">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="24277-157">`[Operation <String>]`: 작업 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="24277-157">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="24277-158">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24277-158">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="24277-159">`[ScaleUnit <String>]`: 눈금 단위 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24277-159">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="24277-160">`[ScaleUnitNode <String>]`: 배율 단위 노드의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24277-160">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="24277-161">`[SlbMuxInstance <String>]`: SLB MUX 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24277-161">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="24277-162">`[StoragePool <String>]`: 저장소 풀 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24277-162">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="24277-163">`[StorageSubSystem <String>]`: 저장소 시스템의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24277-163">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="24277-164">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="24277-164">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="24277-165">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="24277-165">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="24277-166">`[Volume <String>]`: 저장소 볼륨의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24277-166">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="24277-167">관련 링크</span><span class="sxs-lookup"><span data-stu-id="24277-167">RELATED LINKS</span></span>

