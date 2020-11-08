---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/get-azsvmextension
schema: 2.0.0
ms.openlocfilehash: c2214f01b35e68ba22f9dbfc6fe9e602badb9ba9
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/24/2020
ms.locfileid: "94045372"
---
# <span data-ttu-id="0ae74-101">Get-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="0ae74-101">Get-AzsVMExtension</span></span>

## <span data-ttu-id="0ae74-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ae74-102">SYNOPSIS</span></span>
<span data-ttu-id="0ae74-103">요청 된 가상 컴퓨터 확장 이미지에 일치 하는 게시자, 형식, 버전을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ae74-103">Returns requested Virtual Machine Extension Image matching publisher, type, version.</span></span>

## <span data-ttu-id="0ae74-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0ae74-104">SYNTAX</span></span>

### <span data-ttu-id="0ae74-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="0ae74-105">List (Default)</span></span>
```
Get-AzsVMExtension [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="0ae74-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="0ae74-106">Get</span></span>
```
Get-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="0ae74-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0ae74-107">GetViaIdentity</span></span>
```
Get-AzsVMExtension -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="0ae74-108">설명은</span><span class="sxs-lookup"><span data-stu-id="0ae74-108">DESCRIPTION</span></span>
<span data-ttu-id="0ae74-109">요청 된 가상 컴퓨터 확장 이미지에 일치 하는 게시자, 형식, 버전을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ae74-109">Returns requested Virtual Machine Extension Image matching publisher, type, version.</span></span>

## <span data-ttu-id="0ae74-110">예제의</span><span class="sxs-lookup"><span data-stu-id="0ae74-110">EXAMPLES</span></span>

### <span data-ttu-id="0ae74-111">예제 1: 모든 VM 확장 가져오기</span><span class="sxs-lookup"><span data-stu-id="0ae74-111">Example 1:  Get All VM Extensions</span></span>
```powershell
PS C:\> Get-AzsVMExtension

ExtensionType            : IaaSDiagnostics
TypeHandlerVersion       : 1.11.3.12
ComputeRole              : IaaS
Id                       : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locati
                           ons/northwest/artifactTypes/VMExtension/publishers/Microsoft.Azure.Diagnostics/types/IaaSDia
                           gnostics/versions/1.11.3.12
IsSystemExtension        : False
Location                 : northwest
Name                     :
ProvisioningState        : Succeeded
Publisher                : Microsoft.Azure.Diagnostics
SourceBlobUri            :
SupportMultipleExtension : False
Type                     : Microsoft.Compute.Admin/locations/artifactTypes/publishers/types/versions
VMScaleSetEnabled        : False
VmosType                 : Windows

...
```

<span data-ttu-id="0ae74-112">모든 매개 변수를 비워 두어 모든 VMExtensions의 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0ae74-112">Get a list of all VMExtensions by leaving all parameters blank.</span></span>

## <span data-ttu-id="0ae74-113">변수</span><span class="sxs-lookup"><span data-stu-id="0ae74-113">PARAMETERS</span></span>

### <span data-ttu-id="0ae74-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ae74-114">-DefaultProfile</span></span>
<span data-ttu-id="0ae74-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0ae74-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ae74-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0ae74-116">-InputObject</span></span>
<span data-ttu-id="0ae74-117">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0ae74-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0ae74-118">-위치</span><span class="sxs-lookup"><span data-stu-id="0ae74-118">-Location</span></span>
<span data-ttu-id="0ae74-119">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="0ae74-119">Location of the resource.</span></span>

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

### <span data-ttu-id="0ae74-120">-Publisher</span><span class="sxs-lookup"><span data-stu-id="0ae74-120">-Publisher</span></span>
<span data-ttu-id="0ae74-121">게시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0ae74-121">Name of the publisher.</span></span>

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

### <span data-ttu-id="0ae74-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0ae74-122">-SubscriptionId</span></span>
<span data-ttu-id="0ae74-123">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="0ae74-123">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="0ae74-124">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ae74-124">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="0ae74-125">-Type</span><span class="sxs-lookup"><span data-stu-id="0ae74-125">-Type</span></span>
<span data-ttu-id="0ae74-126">확장명의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="0ae74-126">Type of extension.</span></span>

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

### <span data-ttu-id="0ae74-127">-버전</span><span class="sxs-lookup"><span data-stu-id="0ae74-127">-Version</span></span>
<span data-ttu-id="0ae74-128">리소스의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="0ae74-128">The version of the resource.</span></span>

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

### <span data-ttu-id="0ae74-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ae74-129">CommonParameters</span></span>
<span data-ttu-id="0ae74-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ae74-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ae74-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0ae74-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ae74-132">입력</span><span class="sxs-lookup"><span data-stu-id="0ae74-132">INPUTS</span></span>

### <span data-ttu-id="0ae74-133">IComputeAdminIdentity (Microsoft. PowerShell. t t t)</span><span class="sxs-lookup"><span data-stu-id="0ae74-133">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="0ae74-134">출력</span><span class="sxs-lookup"><span data-stu-id="0ae74-134">OUTPUTS</span></span>

### <span data-ttu-id="0ae74-135">Api20151201Preview-. a t t. t t m 확장명</span><span class="sxs-lookup"><span data-stu-id="0ae74-135">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IVMExtension</span></span>



## <span data-ttu-id="0ae74-136">상속자</span><span class="sxs-lookup"><span data-stu-id="0ae74-136">NOTES</span></span>

<span data-ttu-id="0ae74-137">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ae74-137">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0ae74-138">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="0ae74-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="0ae74-139">INPUTOBJECT <IComputeAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="0ae74-139">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0ae74-140">`[DiskId <String>]`: 디스크 guid를 id로 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ae74-140">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="0ae74-141">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="0ae74-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0ae74-142">`[Location <String>]`: 리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="0ae74-142">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="0ae74-143">`[MigrationId <String>]`: 마이그레이션 작업 guid 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0ae74-143">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="0ae74-144">`[Offer <String>]`: 제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0ae74-144">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="0ae74-145">`[Publisher <String>]`: 게시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0ae74-145">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="0ae74-146">`[QuotaName <String>]`: 할당량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0ae74-146">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="0ae74-147">`[Sku <String>]`: SKU의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0ae74-147">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="0ae74-148">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="0ae74-148">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="0ae74-149">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ae74-149">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="0ae74-150">`[Type <String>]`: 확장명의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="0ae74-150">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="0ae74-151">`[Version <String>]`: 리소스의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="0ae74-151">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="0ae74-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0ae74-152">RELATED LINKS</span></span>

