---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsinfrastructureshare
schema: 2.0.0
ms.openlocfilehash: e5fce1490b27bb569ce493a66a1c2646b73466a4
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94046673"
---
# <span data-ttu-id="2e3ed-101">Get-AzsInfrastructureShare</span><span class="sxs-lookup"><span data-stu-id="2e3ed-101">Get-AzsInfrastructureShare</span></span>

## <span data-ttu-id="2e3ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2e3ed-102">SYNOPSIS</span></span>
<span data-ttu-id="2e3ed-103">요청 된 패브릭 파일 공유를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-103">Returns the requested fabric file share.</span></span>

## <span data-ttu-id="2e3ed-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2e3ed-104">SYNTAX</span></span>

### <span data-ttu-id="2e3ed-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="2e3ed-105">List (Default)</span></span>
```
Get-AzsInfrastructureShare [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

### <span data-ttu-id="2e3ed-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="2e3ed-106">Get</span></span>
```
Get-AzsInfrastructureShare -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="2e3ed-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2e3ed-107">GetViaIdentity</span></span>
```
Get-AzsInfrastructureShare -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="2e3ed-108">설명은</span><span class="sxs-lookup"><span data-stu-id="2e3ed-108">DESCRIPTION</span></span>
<span data-ttu-id="2e3ed-109">요청 된 패브릭 파일 공유를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-109">Returns the requested fabric file share.</span></span>

## <span data-ttu-id="2e3ed-110">예제의</span><span class="sxs-lookup"><span data-stu-id="2e3ed-110">EXAMPLES</span></span>

### <span data-ttu-id="2e3ed-111">예제 1:</span><span class="sxs-lookup"><span data-stu-id="2e3ed-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsInfrastructureShare
```

<span data-ttu-id="2e3ed-112">모든 파일 공유 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-112">Returns a list of all file shares.</span></span>

### <span data-ttu-id="2e3ed-113">예제 2:</span><span class="sxs-lookup"><span data-stu-id="2e3ed-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsInfrastructureShare -Name SU1_ObjStore_1
```

<span data-ttu-id="2e3ed-114">이름을 기반으로 하는 파일 공유를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-114">Returns a file share based on name.</span></span>

## <span data-ttu-id="2e3ed-115">변수</span><span class="sxs-lookup"><span data-stu-id="2e3ed-115">PARAMETERS</span></span>

### <span data-ttu-id="2e3ed-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e3ed-116">-DefaultProfile</span></span>
<span data-ttu-id="2e3ed-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2e3ed-118">-필터</span><span class="sxs-lookup"><span data-stu-id="2e3ed-118">-Filter</span></span>
<span data-ttu-id="2e3ed-119">OData 필터 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="2e3ed-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2e3ed-120">-InputObject</span></span>
<span data-ttu-id="2e3ed-121">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2e3ed-122">-위치</span><span class="sxs-lookup"><span data-stu-id="2e3ed-122">-Location</span></span>
<span data-ttu-id="2e3ed-123">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-123">Location of the resource.</span></span>

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

### <span data-ttu-id="2e3ed-124">-이름</span><span class="sxs-lookup"><span data-stu-id="2e3ed-124">-Name</span></span>
<span data-ttu-id="2e3ed-125">패브릭 파일 공유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-125">Fabric file share name.</span></span>

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

### <span data-ttu-id="2e3ed-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2e3ed-126">-PassThru</span></span>
<span data-ttu-id="2e3ed-127">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="2e3ed-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e3ed-128">-ResourceGroupName</span></span>
<span data-ttu-id="2e3ed-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="2e3ed-130">-생략</span><span class="sxs-lookup"><span data-stu-id="2e3ed-130">-Skip</span></span>
<span data-ttu-id="2e3ed-131">OData skip 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-131">OData skip parameter.</span></span>

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

### <span data-ttu-id="2e3ed-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2e3ed-132">-SubscriptionId</span></span>
<span data-ttu-id="2e3ed-133">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-133">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="2e3ed-134">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2e3ed-135">-위쪽</span><span class="sxs-lookup"><span data-stu-id="2e3ed-135">-Top</span></span>
<span data-ttu-id="2e3ed-136">OData top 매개 변수.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-136">OData top parameter.</span></span>

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

### <span data-ttu-id="2e3ed-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e3ed-137">CommonParameters</span></span>
<span data-ttu-id="2e3ed-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e3ed-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e3ed-140">입력</span><span class="sxs-lookup"><span data-stu-id="2e3ed-140">INPUTS</span></span>

### <span data-ttu-id="2e3ed-141">FabricAdmin. IFabricAdminIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="2e3ed-141">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="2e3ed-142">출력</span><span class="sxs-lookup"><span data-stu-id="2e3ed-142">OUTPUTS</span></span>

### <span data-ttu-id="2e3ed-143">FabricAdmin. Api20160501. i a PowerShell.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-143">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IFileShare</span></span>



## <span data-ttu-id="2e3ed-144">상속자</span><span class="sxs-lookup"><span data-stu-id="2e3ed-144">NOTES</span></span>

<span data-ttu-id="2e3ed-145">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-145">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2e3ed-146">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="2e3ed-147">INPUTOBJECT <IFabricAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="2e3ed-147">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2e3ed-148">`[Drive <String>]`: 저장소 드라이브의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-148">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="2e3ed-149">`[EdgeGateway <String>]`: Edge 게이트웨이의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-149">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="2e3ed-150">`[EdgeGatewayPool <String>]`: Edge 게이트웨이 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-150">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="2e3ed-151">`[FabricLocation <String>]`: 패브릭 위치.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-151">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="2e3ed-152">`[FileShare <String>]`: 패브릭 파일 공유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-152">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="2e3ed-153">`[IPPool <String>]`: IP 풀 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-153">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="2e3ed-154">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="2e3ed-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2e3ed-155">`[InfraRole <String>]`: 인프라 역할 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-155">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="2e3ed-156">`[InfraRoleInstance <String>]`: 인프라 역할 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-156">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="2e3ed-157">`[Location <String>]`: 리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-157">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="2e3ed-158">`[LogicalNetwork <String>]`: 논리 네트워크의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-158">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="2e3ed-159">`[LogicalSubnet <String>]`: 논리 서브넷의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-159">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="2e3ed-160">`[MacAddressPool <String>]`: MAC 주소 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-160">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="2e3ed-161">`[Operation <String>]`: 작업 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-161">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="2e3ed-162">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-162">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="2e3ed-163">`[ScaleUnit <String>]`: 눈금 단위 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-163">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="2e3ed-164">`[ScaleUnitNode <String>]`: 배율 단위 노드의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-164">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="2e3ed-165">`[SlbMuxInstance <String>]`: SLB MUX 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-165">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="2e3ed-166">`[StorageSubSystem <String>]`: 저장소 시스템의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-166">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="2e3ed-167">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-167">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="2e3ed-168">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-168">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="2e3ed-169">`[Volume <String>]`: 저장소 볼륨의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2e3ed-169">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="2e3ed-170">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2e3ed-170">RELATED LINKS</span></span>

