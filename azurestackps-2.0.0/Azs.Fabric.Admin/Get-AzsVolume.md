---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsvolume
schema: 2.0.0
ms.openlocfilehash: a423470454e77c58a8b611a47c737e5d86bfd1cf
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876060"
---
# <span data-ttu-id="e7f73-101">Get-AzsVolume</span><span class="sxs-lookup"><span data-stu-id="e7f73-101">Get-AzsVolume</span></span>

## <span data-ttu-id="e7f73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e7f73-102">SYNOPSIS</span></span>
<span data-ttu-id="e7f73-103">요청 된 저장소 볼륨을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7f73-103">Return the requested a storage volume.</span></span>

## <span data-ttu-id="e7f73-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e7f73-104">SYNTAX</span></span>

### <span data-ttu-id="e7f73-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="e7f73-105">List (Default)</span></span>
```
Get-AzsVolume -ScaleUnit <String> -StorageSubSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Filter <String>] [-Skip <String>]
 [-Top <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="e7f73-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="e7f73-106">Get</span></span>
```
Get-AzsVolume -Name <String> -ScaleUnit <String> -StorageSubSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

### <span data-ttu-id="e7f73-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e7f73-107">GetViaIdentity</span></span>
```
Get-AzsVolume -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="e7f73-108">설명은</span><span class="sxs-lookup"><span data-stu-id="e7f73-108">DESCRIPTION</span></span>
<span data-ttu-id="e7f73-109">요청 된 저장소 볼륨을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7f73-109">Return the requested a storage volume.</span></span>

## <span data-ttu-id="e7f73-110">예제의</span><span class="sxs-lookup"><span data-stu-id="e7f73-110">EXAMPLES</span></span>

### <span data-ttu-id="e7f73-111">예제 1:</span><span class="sxs-lookup"><span data-stu-id="e7f73-111">Example 1:</span></span>
```powershell
PS C:\> $scaleUnit = Get-AzsScaleUnit | select -First 1
PS C:\> $storageSubSystem = Get-AzsStorageSubSystem -ScaleUnit $scaleUnit.Name
PS C:\> Get-AzsVolume -ScaleUnit $scaleUnit.Name -StorageSubSystem $storageSubSystem.Name
```

<span data-ttu-id="e7f73-112">지정 된 위치에 있는 모든 저장소 볼륨의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e7f73-112">Get a list of all storage volumes at a given location.</span></span>

### <span data-ttu-id="e7f73-113">예제 2:</span><span class="sxs-lookup"><span data-stu-id="e7f73-113">Example 2:</span></span>
```powershell
PS C:\> $scaleUnit = Get-AzsScaleUnit | select -First 1
PS C:\> $storageSubSystem = Get-AzsStorageSubSystem -ScaleUnit $scaleUnit.Name
PS C:\> Get-AzsVolume -ScaleUnit $scaleUnit.Name -StorageSubSystem $storageSubSystem.Name -Name ee594cf5-cf54-46b4-a641-139553307195
```

<span data-ttu-id="e7f73-114">지정 된 위치에서 이름으로 저장소 볼륨을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e7f73-114">Get a storage volume by name at a given location.</span></span>

## <span data-ttu-id="e7f73-115">변수</span><span class="sxs-lookup"><span data-stu-id="e7f73-115">PARAMETERS</span></span>

### <span data-ttu-id="e7f73-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e7f73-116">-DefaultProfile</span></span>
<span data-ttu-id="e7f73-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f73-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e7f73-118">-필터</span><span class="sxs-lookup"><span data-stu-id="e7f73-118">-Filter</span></span>
<span data-ttu-id="e7f73-119">OData 필터 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f73-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="e7f73-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e7f73-120">-InputObject</span></span>
<span data-ttu-id="e7f73-121">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e7f73-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="e7f73-122">-위치</span><span class="sxs-lookup"><span data-stu-id="e7f73-122">-Location</span></span>
<span data-ttu-id="e7f73-123">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f73-123">Location of the resource.</span></span>

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

### <span data-ttu-id="e7f73-124">-이름</span><span class="sxs-lookup"><span data-stu-id="e7f73-124">-Name</span></span>
<span data-ttu-id="e7f73-125">저장소 볼륨의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f73-125">Name of the storage volume.</span></span>

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

### <span data-ttu-id="e7f73-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e7f73-126">-PassThru</span></span>
<span data-ttu-id="e7f73-127">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7f73-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="e7f73-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7f73-128">-ResourceGroupName</span></span>
<span data-ttu-id="e7f73-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f73-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="e7f73-130">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="e7f73-130">-ScaleUnit</span></span>
<span data-ttu-id="e7f73-131">눈금 단위의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f73-131">Name of the scale units.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e7f73-132">-생략</span><span class="sxs-lookup"><span data-stu-id="e7f73-132">-Skip</span></span>
<span data-ttu-id="e7f73-133">OData skip 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f73-133">OData skip parameter.</span></span>

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

### <span data-ttu-id="e7f73-134">-StorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="e7f73-134">-StorageSubSystem</span></span>
<span data-ttu-id="e7f73-135">저장소 시스템의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f73-135">Name of the storage system.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e7f73-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e7f73-136">-SubscriptionId</span></span>
<span data-ttu-id="e7f73-137">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f73-137">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e7f73-138">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7f73-138">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e7f73-139">-위쪽</span><span class="sxs-lookup"><span data-stu-id="e7f73-139">-Top</span></span>
<span data-ttu-id="e7f73-140">OData top 매개 변수.</span><span class="sxs-lookup"><span data-stu-id="e7f73-140">OData top parameter.</span></span>

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

### <span data-ttu-id="e7f73-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7f73-141">CommonParameters</span></span>
<span data-ttu-id="e7f73-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7f73-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7f73-143">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e7f73-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7f73-144">입력</span><span class="sxs-lookup"><span data-stu-id="e7f73-144">INPUTS</span></span>

### <span data-ttu-id="e7f73-145">FabricAdmin. IFabricAdminIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="e7f73-145">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="e7f73-146">출력</span><span class="sxs-lookup"><span data-stu-id="e7f73-146">OUTPUTS</span></span>

### <span data-ttu-id="e7f73-147">FabricAdmin. Api20190501. IVolume에 대 한</span><span class="sxs-lookup"><span data-stu-id="e7f73-147">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20190501.IVolume</span></span>



## <span data-ttu-id="e7f73-148">상속자</span><span class="sxs-lookup"><span data-stu-id="e7f73-148">NOTES</span></span>

<span data-ttu-id="e7f73-149">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7f73-149">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e7f73-150">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="e7f73-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="e7f73-151">INPUTOBJECT <IFabricAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="e7f73-151">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e7f73-152">`[Drive <String>]`: 저장소 드라이브의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f73-152">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="e7f73-153">`[EdgeGateway <String>]`: Edge 게이트웨이의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f73-153">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="e7f73-154">`[EdgeGatewayPool <String>]`: Edge 게이트웨이 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f73-154">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="e7f73-155">`[FabricLocation <String>]`: 패브릭 위치.</span><span class="sxs-lookup"><span data-stu-id="e7f73-155">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="e7f73-156">`[FileShare <String>]`: 패브릭 파일 공유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f73-156">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="e7f73-157">`[IPPool <String>]`: IP 풀 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f73-157">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="e7f73-158">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="e7f73-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e7f73-159">`[InfraRole <String>]`: 인프라 역할 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f73-159">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="e7f73-160">`[InfraRoleInstance <String>]`: 인프라 역할 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f73-160">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="e7f73-161">`[Location <String>]`: 리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f73-161">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="e7f73-162">`[LogicalNetwork <String>]`: 논리 네트워크의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f73-162">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="e7f73-163">`[LogicalSubnet <String>]`: 논리 서브넷의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f73-163">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="e7f73-164">`[MacAddressPool <String>]`: MAC 주소 풀의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f73-164">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="e7f73-165">`[Operation <String>]`: 작업 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f73-165">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="e7f73-166">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f73-166">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="e7f73-167">`[ScaleUnit <String>]`: 눈금 단위 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f73-167">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="e7f73-168">`[ScaleUnitNode <String>]`: 배율 단위 노드의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f73-168">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="e7f73-169">`[SlbMuxInstance <String>]`: SLB MUX 인스턴스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f73-169">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="e7f73-170">`[StorageSubSystem <String>]`: 저장소 시스템의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f73-170">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="e7f73-171">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f73-171">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="e7f73-172">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="e7f73-172">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="e7f73-173">`[Volume <String>]`: 저장소 볼륨의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e7f73-173">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="e7f73-174">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e7f73-174">RELATED LINKS</span></span>

