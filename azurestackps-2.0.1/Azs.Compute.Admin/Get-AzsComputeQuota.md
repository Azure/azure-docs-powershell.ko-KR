---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/get-azscomputequota
schema: 2.0.0
ms.openlocfilehash: 81a7a64f1880e2ed9acb2fedd3f90df614f1619d
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/24/2020
ms.locfileid: "94045373"
---
# <span data-ttu-id="d3904-101">Get-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="d3904-101">Get-AzsComputeQuota</span></span>

## <span data-ttu-id="d3904-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3904-102">SYNOPSIS</span></span>
<span data-ttu-id="d3904-103">기존 계산 할당량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d3904-103">Get an existing Compute Quota.</span></span>

## <span data-ttu-id="d3904-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d3904-104">SYNTAX</span></span>

### <span data-ttu-id="d3904-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="d3904-105">List (Default)</span></span>
```
Get-AzsComputeQuota [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="d3904-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="d3904-106">Get</span></span>
```
Get-AzsComputeQuota -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d3904-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d3904-107">GetViaIdentity</span></span>
```
Get-AzsComputeQuota -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="d3904-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d3904-108">DESCRIPTION</span></span>
<span data-ttu-id="d3904-109">기존 계산 할당량을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d3904-109">Get an existing Compute Quota.</span></span>

## <span data-ttu-id="d3904-110">예제의</span><span class="sxs-lookup"><span data-stu-id="d3904-110">EXAMPLES</span></span>

### <span data-ttu-id="d3904-111">예제 1: 모든 계산 할당량 가져오기</span><span class="sxs-lookup"><span data-stu-id="d3904-111">Example 1: Get All Compute Quotas</span></span>
```powershell
PS C:\> Get-AzsComputeQuota

AvailabilitySetCount               : 10
CoresLimit                         : 100
Id                                 : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Ad
                                     min/locations/local/quotas/ascancompquota433
Location                           : local
Name                               : ascancompquota433
PremiumManagedDiskAndSnapshotSize  : 2048
StandardManagedDiskAndSnapshotSize : 2048
Type                               : Microsoft.Compute.Admin/quotas
VMScaleSetCount                    : 100
VirtualMachineCount                : 100
```

<span data-ttu-id="d3904-112">`Get-AzsComputeQuota`매개 변수 없이 실행 하 여 모든 계산 할당량 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d3904-112">Run `Get-AzsComputeQuota` with no parameters to get a list of all Compute Quotas.</span></span>

### <span data-ttu-id="d3904-113">예제 2: 이름별로 계산 할당량 가져오기</span><span class="sxs-lookup"><span data-stu-id="d3904-113">Example 2: Get Compute Quota by Name</span></span>
```powershell
PS C:\> Get-AzsComputeQuota -Name ExampleComputeQuotaWithDefaultParameters

AvailabilitySetCount               : 10
CoresLimit                         : 100
Id                                 : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Ad
                                     min/locations/local/quotas/ExampleComputeQuotaWithDefaultParameters
Location                           : local
Name                               : ExampleComputeQuotaWithDefaultParameters
PremiumManagedDiskAndSnapshotSize  : 2048
StandardManagedDiskAndSnapshotSize : 2048
Type                               : Microsoft.Compute.Admin/quotas
VMScaleSetCount                    : 0
VirtualMachineCount                : 100
```

<span data-ttu-id="d3904-114">명령줄에서 할당량 이름을 지정 하 여 특정 할당량을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3904-114">Specify the Quota's name on the command line to retrieve a specific quota.</span></span>

## <span data-ttu-id="d3904-115">변수</span><span class="sxs-lookup"><span data-stu-id="d3904-115">PARAMETERS</span></span>

### <span data-ttu-id="d3904-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3904-116">-DefaultProfile</span></span>
<span data-ttu-id="d3904-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d3904-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3904-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d3904-118">-InputObject</span></span>
<span data-ttu-id="d3904-119">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d3904-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="d3904-120">-위치</span><span class="sxs-lookup"><span data-stu-id="d3904-120">-Location</span></span>
<span data-ttu-id="d3904-121">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="d3904-121">Location of the resource.</span></span>

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

### <span data-ttu-id="d3904-122">-이름</span><span class="sxs-lookup"><span data-stu-id="d3904-122">-Name</span></span>
<span data-ttu-id="d3904-123">할당량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d3904-123">Name of the quota.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d3904-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d3904-124">-SubscriptionId</span></span>
<span data-ttu-id="d3904-125">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="d3904-125">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d3904-126">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3904-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d3904-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3904-127">CommonParameters</span></span>
<span data-ttu-id="d3904-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3904-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3904-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d3904-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3904-130">입력</span><span class="sxs-lookup"><span data-stu-id="d3904-130">INPUTS</span></span>

### <span data-ttu-id="d3904-131">IComputeAdminIdentity (Microsoft. PowerShell. t t t)</span><span class="sxs-lookup"><span data-stu-id="d3904-131">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="d3904-132">출력</span><span class="sxs-lookup"><span data-stu-id="d3904-132">OUTPUTS</span></span>

### <span data-ttu-id="d3904-133">Api20180209 (Microsoft. PowerShell. a t t.</span><span class="sxs-lookup"><span data-stu-id="d3904-133">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota</span></span>



## <span data-ttu-id="d3904-134">상속자</span><span class="sxs-lookup"><span data-stu-id="d3904-134">NOTES</span></span>

<span data-ttu-id="d3904-135">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3904-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d3904-136">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="d3904-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="d3904-137">INPUTOBJECT <IComputeAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="d3904-137">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d3904-138">`[DiskId <String>]`: 디스크 guid를 id로 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3904-138">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="d3904-139">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="d3904-139">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d3904-140">`[Location <String>]`: 리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="d3904-140">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="d3904-141">`[MigrationId <String>]`: 마이그레이션 작업 guid 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d3904-141">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="d3904-142">`[Offer <String>]`: 제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d3904-142">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="d3904-143">`[Publisher <String>]`: 게시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d3904-143">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="d3904-144">`[QuotaName <String>]`: 할당량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d3904-144">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="d3904-145">`[Sku <String>]`: SKU의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d3904-145">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="d3904-146">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="d3904-146">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d3904-147">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3904-147">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="d3904-148">`[Type <String>]`: 확장명의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="d3904-148">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="d3904-149">`[Version <String>]`: 리소스의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="d3904-149">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="d3904-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d3904-150">RELATED LINKS</span></span>

