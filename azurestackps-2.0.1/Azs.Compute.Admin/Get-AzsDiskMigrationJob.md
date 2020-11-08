---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/get-azsdiskmigrationjob
schema: 2.0.0
ms.openlocfilehash: 96c14cd8d8d48b6212ed0e4c7b0d5934754912a5
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/24/2020
ms.locfileid: "94045275"
---
# <span data-ttu-id="b82bb-101">Get-AzsDiskMigrationJob</span><span class="sxs-lookup"><span data-stu-id="b82bb-101">Get-AzsDiskMigrationJob</span></span>

## <span data-ttu-id="b82bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b82bb-102">SYNOPSIS</span></span>
<span data-ttu-id="b82bb-103">요청 된 디스크 마이그레이션 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82bb-103">Returns the requested disk migration job.</span></span>

## <span data-ttu-id="b82bb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b82bb-104">SYNTAX</span></span>

### <span data-ttu-id="b82bb-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="b82bb-105">List (Default)</span></span>
```
Get-AzsDiskMigrationJob [-Location <String>] [-SubscriptionId <String[]>] [-Status <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b82bb-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="b82bb-106">Get</span></span>
```
Get-AzsDiskMigrationJob -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b82bb-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b82bb-107">GetViaIdentity</span></span>
```
Get-AzsDiskMigrationJob -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b82bb-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b82bb-108">DESCRIPTION</span></span>
<span data-ttu-id="b82bb-109">요청 된 디스크 마이그레이션 작업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82bb-109">Returns the requested disk migration job.</span></span>

## <span data-ttu-id="b82bb-110">예제의</span><span class="sxs-lookup"><span data-stu-id="b82bb-110">EXAMPLES</span></span>

### <span data-ttu-id="b82bb-111">예제 1:</span><span class="sxs-lookup"><span data-stu-id="b82bb-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsDiskMigrationJob
```

<span data-ttu-id="b82bb-112">로컬 위치에서 관리 되는 디스크 마이그레이션 작업의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82bb-112">Returns a list of managed disk migration jobs at the location local.</span></span>

### <span data-ttu-id="b82bb-113">예제 2:</span><span class="sxs-lookup"><span data-stu-id="b82bb-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsDiskMigrationJob -Name TestNewDiskMigrationJob

CreationTime : 2/26/2020 10:45:41 AM
EndTime      : 2/26/2020 10:46:32 AM
Id           : /subscriptions/627fecef-520e-4c18-94e0-8f0665ba86a7/providers/Microsoft.Compute.Admin/locations/redmond/diskmigrationjobs/TestNewDiskMigrationJob
Location     : redmond
MigrationId  : TestNewDiskMigrationJob
Name         : redmond/TestNewDiskMigrationJob
StartTime    : 2/26/2020 10:45:41 AM
Status       : Succeeded
Subtask      : {edacd0f6-760a-43f9-a188-8833751f89ce, f1ee38a4-5c27-4728-a12b-36976c565042}
TargetShare  : \\SU1FileServer.s31r1801.masd.stbtest.microsoft.com\SU1_ObjStore_1
Type         : Microsoft.Compute.Admin/locations/diskmigrationjobs
```

<span data-ttu-id="b82bb-114">특정 관리 디스크 마이그레이션 작업을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b82bb-114">Get a specific managed disk migration job.</span></span>

## <span data-ttu-id="b82bb-115">변수</span><span class="sxs-lookup"><span data-stu-id="b82bb-115">PARAMETERS</span></span>

### <span data-ttu-id="b82bb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b82bb-116">-DefaultProfile</span></span>
<span data-ttu-id="b82bb-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b82bb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b82bb-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b82bb-118">-InputObject</span></span>
<span data-ttu-id="b82bb-119">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b82bb-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b82bb-120">-위치</span><span class="sxs-lookup"><span data-stu-id="b82bb-120">-Location</span></span>
<span data-ttu-id="b82bb-121">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="b82bb-121">Location of the resource.</span></span>

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

### <span data-ttu-id="b82bb-122">-이름</span><span class="sxs-lookup"><span data-stu-id="b82bb-122">-Name</span></span>
<span data-ttu-id="b82bb-123">마이그레이션 작업 guid 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b82bb-123">The migration job guid name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: MigrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="b82bb-124">-상태</span><span class="sxs-lookup"><span data-stu-id="b82bb-124">-Status</span></span>
<span data-ttu-id="b82bb-125">디스크 마이그레이션 작업 상태의 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="b82bb-125">The parameters of disk migration job status.</span></span>

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

### <span data-ttu-id="b82bb-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b82bb-126">-SubscriptionId</span></span>
<span data-ttu-id="b82bb-127">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="b82bb-127">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b82bb-128">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82bb-128">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b82bb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b82bb-129">CommonParameters</span></span>
<span data-ttu-id="b82bb-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82bb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b82bb-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b82bb-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b82bb-132">입력</span><span class="sxs-lookup"><span data-stu-id="b82bb-132">INPUTS</span></span>

### <span data-ttu-id="b82bb-133">IComputeAdminIdentity (Microsoft. PowerShell. t t t)</span><span class="sxs-lookup"><span data-stu-id="b82bb-133">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="b82bb-134">출력</span><span class="sxs-lookup"><span data-stu-id="b82bb-134">OUTPUTS</span></span>

### <span data-ttu-id="b82bb-135">Api20180730Preview. IDiskMigrationJob에 대 한. t t t</span><span class="sxs-lookup"><span data-stu-id="b82bb-135">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180730Preview.IDiskMigrationJob</span></span>



## <span data-ttu-id="b82bb-136">상속자</span><span class="sxs-lookup"><span data-stu-id="b82bb-136">NOTES</span></span>

<span data-ttu-id="b82bb-137">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82bb-137">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b82bb-138">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="b82bb-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="b82bb-139">INPUTOBJECT <IComputeAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="b82bb-139">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b82bb-140">`[DiskId <String>]`: 디스크 guid를 id로 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82bb-140">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="b82bb-141">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="b82bb-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b82bb-142">`[Location <String>]`: 리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="b82bb-142">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="b82bb-143">`[MigrationId <String>]`: 마이그레이션 작업 guid 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b82bb-143">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="b82bb-144">`[Offer <String>]`: 제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b82bb-144">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="b82bb-145">`[Publisher <String>]`: 게시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b82bb-145">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="b82bb-146">`[QuotaName <String>]`: 할당량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b82bb-146">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="b82bb-147">`[Sku <String>]`: SKU의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b82bb-147">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="b82bb-148">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="b82bb-148">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b82bb-149">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="b82bb-149">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="b82bb-150">`[Type <String>]`: 확장명의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="b82bb-150">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="b82bb-151">`[Version <String>]`: 리소스의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="b82bb-151">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="b82bb-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b82bb-152">RELATED LINKS</span></span>

