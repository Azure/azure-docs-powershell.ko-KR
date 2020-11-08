---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/get-azsdisk
schema: 2.0.0
ms.openlocfilehash: 9c3c87e7c62764cff0a7d6b9d65a3dfe3df31990
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/24/2020
ms.locfileid: "94045278"
---
# <span data-ttu-id="94321-101">Get-AzsDisk</span><span class="sxs-lookup"><span data-stu-id="94321-101">Get-AzsDisk</span></span>

## <span data-ttu-id="94321-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94321-102">SYNOPSIS</span></span>
<span data-ttu-id="94321-103">디스크를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="94321-103">Returns the disk.</span></span>

## <span data-ttu-id="94321-104">구문과</span><span class="sxs-lookup"><span data-stu-id="94321-104">SYNTAX</span></span>

### <span data-ttu-id="94321-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="94321-105">List (Default)</span></span>
```
Get-AzsDisk [-Location <String>] [-SubscriptionId <String[]>] [-Count <Int32>] [-ScaleUnit <String>]
 [-SharePath <String>] [-Start <Int32>] [-Status <String>] [-UserSubscriptionId <String>]
 [-VolumeLabel <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="94321-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="94321-106">Get</span></span>
```
Get-AzsDisk -Name <String> [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="94321-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="94321-107">GetViaIdentity</span></span>
```
Get-AzsDisk -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="94321-108">설명은</span><span class="sxs-lookup"><span data-stu-id="94321-108">DESCRIPTION</span></span>
<span data-ttu-id="94321-109">디스크를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="94321-109">Returns the disk.</span></span>

## <span data-ttu-id="94321-110">예제의</span><span class="sxs-lookup"><span data-stu-id="94321-110">EXAMPLES</span></span>

### <span data-ttu-id="94321-111">예제 1: 모든 디스크 가져오기</span><span class="sxs-lookup"><span data-stu-id="94321-111">Example 1: Get All Disks</span></span> 
```powershell
PS C:\> Get-AzsDisk
```

<span data-ttu-id="94321-112">매개 변수를 사용 하지 않으면 `Get-AzsDisk` 모든 디스크가 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="94321-112">Without any parameters, `Get-AzsDisk` will list all Disks.</span></span>

### <span data-ttu-id="94321-113">예제 2: 이름으로 디스크 가져오기</span><span class="sxs-lookup"><span data-stu-id="94321-113">Example 2: Get a Disk by Name</span></span>
```powershell
PS C:\> Get-AzsDisk -Name "426b8945-8a24-42ad-acdc-c26f16202489"

ActualSizeGb    : 24
DiskId          : 426b8945-8a24-42ad-acdc-c26f16202489
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locations/north
                  west/disks/426b8945-8a24-42ad-acdc-c26f16202489
Location        : northwest
ManagedBy       :
Name            : northwest/426b8945-8a24-42ad-acdc-c26f16202489
ProvisionSizeGb : 127
SharePath       : \\SU1FileServer.azs-long02-int.selfhost.corp.microsoft.com\SU1_ObjStore_3
Status          : Unattached
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/resourceGroups/LADTEST/providers/Microsoft.Comput
                  e/Disks/TEST_OsDisk_1_426b89458a2442adacdcc26f16202489
```

<span data-ttu-id="94321-114">검색할 디스크를 지정 `Name` 합니다.</span><span class="sxs-lookup"><span data-stu-id="94321-114">Specify a disk by its `Name` to retrieve it.</span></span>

### <span data-ttu-id="94321-115">예제 3: 지정 된 수의 디스크 가져오기</span><span class="sxs-lookup"><span data-stu-id="94321-115">Example 3: Get a Specified number of Disks</span></span>
```powershell
PS C:\>  Get-AzsDisk -Count 3

ActualSizeGb    : 24
DiskId          : 20f1619e-4210-47f6-81e6-b89e3028df06
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locations/north
                  west/disks/20f1619e-4210-47f6-81e6-b89e3028df06
Location        : northwest
ManagedBy       :
Name            : northwest/20f1619e-4210-47f6-81e6-b89e3028df06
ProvisionSizeGb : 127
SharePath       : \\SU1FileServer.azs-long02-int.selfhost.corp.microsoft.com\SU1_ObjStore_4
Status          : Unattached
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/resourceGroups/RG1/providers/Microsoft.Compute/Di
                  sks/TEST_OsDisk_1_20f1619e421047f681e6b89e3028df06

ActualSizeGb    : 24
DiskId          : 38a767e4-4ceb-49fb-a53c-48de9b08aaae
DiskSku         : Standard_LRS
DiskType        : Disk
Id              : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locations/north
                  west/disks/38a767e4-4ceb-49fb-a53c-48de9b08aaae
Location        : northwest
ManagedBy       :
Name            : northwest/38a767e4-4ceb-49fb-a53c-48de9b08aaae
ProvisionSizeGb : 127
SharePath       : \\SU1FileServer.azs-long02-int.selfhost.corp.microsoft.com\SU1_ObjStore_4
Status          : Unattached
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/resourceGroups/SCTE/providers/Microsoft.Compute/D
                  isks/SCTETest_OsDisk_1_38a767e44ceb49fba53c48de9b08aaae

ActualSizeGb    : 24
DiskId          : 426b8945-8a24-42ad-acdc-c26f16202489
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locations/north
                  west/disks/426b8945-8a24-42ad-acdc-c26f16202489
Location        : northwest
ManagedBy       :
Name            : northwest/426b8945-8a24-42ad-acdc-c26f16202489
ProvisionSizeGb : 127
SharePath       : \\SU1FileServer.azs-long02-int.selfhost.corp.microsoft.com\SU1_ObjStore_3
Status          : Unattached
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/resourceGroups/LADTEST/providers/Microsoft.Comput
                  e/Disks/TEST_OsDisk_1_426b89458a2442adacdcc26f16202489
```

<span data-ttu-id="94321-116">`Count`매개 변수를 사용 하 여 특정 개수의 디스크를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="94321-116">Use the `Count` parameter to retrieve a specific number of disks.</span></span>

### <span data-ttu-id="94321-117">예제 4: 모든 디스크를 특정 위치에 가져오기</span><span class="sxs-lookup"><span data-stu-id="94321-117">Example 4: Get all disks in specific location</span></span>
```powershell
PS C:\> Get-AzsDisk -Status All -ScaleUnit s-cluster -VolumeLabel Objstore_4

ActualSizeGb    : 2
DiskId          : e4732f76-0753-40ec-80f5-8effdd0b437d
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/providers/Microsoft.Compute.Admin/locations/redmond/disks/e4732f76-0753-40ec-80f5-8effdd0b437d
Location        : redmond
ManagedBy       : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/rbactest/providers/Microsoft.Compute/virtualMachines/test1
Name            : redmond/e4732f76-0753-40ec-80f5-8effdd0b437d
ProvisionSizeGb : 30
SharePath       : \\SU1FileServer.s11r0401.masd.stbtest.microsoft.com\SU1_ObjStore_4
Status          : Reserved
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/RBACTEST/providers/Microsoft.Compute/Disks/test1_OsDisk_1_e4732f76075340ec80f58effdd0b437d

ActualSizeGb    : 1
DiskId          : 0485cbc9-1efa-43bd-86c2-0e201d79c528
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/providers/Microsoft.Compute.Admin/locations/redmond/disks/0485cbc9-1efa-43bd-86c2-0e201d79c528
Location        : redmond
ManagedBy       : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/rbactest/providers/Microsoft.Compute/virtualMachines/test1
Name            : redmond/0485cbc9-1efa-43bd-86c2-0e201d79c528
ProvisionSizeGb : 64
SharePath       : \\SU1FileServer.s11r0401.masd.stbtest.microsoft.com\SU1_ObjStore_4
Status          : Reserved
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/TESTRG1/providers/Microsoft.Compute/Disks/gpsdisk

ActualSizeGb    : 1
DiskId          : 137893db-e7ce-4907-a488-b35c5e928614
DiskSku         : Premium_LRS
DiskType        : Disk
Id              : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/providers/Microsoft.Compute.Admin/locations/redmond/disks/137893db-e7ce-4907-a488-b35c5e928614
Location        : redmond
ManagedBy       : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/rbactest/providers/Microsoft.Compute/virtualMachines/test1
Name            : redmond/137893db-e7ce-4907-a488-b35c5e928614
ProvisionSizeGb : 55
SharePath       : \\SU1FileServer.s11r0401.masd.stbtest.microsoft.com\SU1_ObjStore_4
Status          : Reserved
Type            : Microsoft.Compute.Admin/locations/disks
UserResourceId  : /subscriptions/7829c784-cd3f-464a-b195-3be83c964c9c/resourceGroups/RBACTEST/providers/Microsoft.Compute/Disks/testdd
```

<span data-ttu-id="94321-118">`ScaleUnit`Or `VolumeLabel` 매개 변수를 사용 하 여 특정 위치에 모든 디스크 나열</span><span class="sxs-lookup"><span data-stu-id="94321-118">Use the `ScaleUnit` or `VolumeLabel` parameter to list all disks in specific location</span></span>

## <span data-ttu-id="94321-119">변수</span><span class="sxs-lookup"><span data-stu-id="94321-119">PARAMETERS</span></span>

### <span data-ttu-id="94321-120">-카운트</span><span class="sxs-lookup"><span data-stu-id="94321-120">-Count</span></span>
<span data-ttu-id="94321-121">반환할 최대 디스크 수입니다.</span><span class="sxs-lookup"><span data-stu-id="94321-121">The maximum number of disks to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="94321-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94321-122">-DefaultProfile</span></span>
<span data-ttu-id="94321-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="94321-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94321-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94321-124">-InputObject</span></span>
<span data-ttu-id="94321-125">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="94321-125">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="94321-126">-위치</span><span class="sxs-lookup"><span data-stu-id="94321-126">-Location</span></span>
<span data-ttu-id="94321-127">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="94321-127">Location of the resource.</span></span>

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

### <span data-ttu-id="94321-128">-이름</span><span class="sxs-lookup"><span data-stu-id="94321-128">-Name</span></span>
<span data-ttu-id="94321-129">Id 인 디스크 guid입니다.</span><span class="sxs-lookup"><span data-stu-id="94321-129">The disk guid as identity.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DiskId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="94321-130">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="94321-130">-ScaleUnit</span></span>
<span data-ttu-id="94321-131">리소스가 속한 배율 단위입니다.</span><span class="sxs-lookup"><span data-stu-id="94321-131">The scale unit which the resource belongs to.</span></span>

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

### <span data-ttu-id="94321-132">-SharePath</span><span class="sxs-lookup"><span data-stu-id="94321-132">-SharePath</span></span>
<span data-ttu-id="94321-133">리소스가 속한 공유입니다.</span><span class="sxs-lookup"><span data-stu-id="94321-133">The share which the resource belongs to.</span></span>

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

### <span data-ttu-id="94321-134">-시작</span><span class="sxs-lookup"><span data-stu-id="94321-134">-Start</span></span>
<span data-ttu-id="94321-135">Query의 디스크 시작 인덱스입니다.</span><span class="sxs-lookup"><span data-stu-id="94321-135">The start index of disks in query.</span></span>

```yaml
Type: System.Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="94321-136">-상태</span><span class="sxs-lookup"><span data-stu-id="94321-136">-Status</span></span>
<span data-ttu-id="94321-137">디스크 상태의 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="94321-137">The parameters of disk state.</span></span>

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

### <span data-ttu-id="94321-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="94321-138">-SubscriptionId</span></span>
<span data-ttu-id="94321-139">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="94321-139">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="94321-140">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="94321-140">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="94321-141">-UserSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="94321-141">-UserSubscriptionId</span></span>
<span data-ttu-id="94321-142">자원이 속한 사용자 구독 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="94321-142">User Subscription Id which the resource belongs to.</span></span>

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

### <span data-ttu-id="94321-143">-VolumeLabel</span><span class="sxs-lookup"><span data-stu-id="94321-143">-VolumeLabel</span></span>
<span data-ttu-id="94321-144">리소스가 속한 볼륨의 볼륨 레이블입니다.</span><span class="sxs-lookup"><span data-stu-id="94321-144">The volume label of the volume which the resource belongs to.</span></span>

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

### <span data-ttu-id="94321-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94321-145">CommonParameters</span></span>
<span data-ttu-id="94321-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="94321-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94321-147">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="94321-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94321-148">입력</span><span class="sxs-lookup"><span data-stu-id="94321-148">INPUTS</span></span>

### <span data-ttu-id="94321-149">IComputeAdminIdentity (Microsoft. PowerShell. t t t)</span><span class="sxs-lookup"><span data-stu-id="94321-149">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="94321-150">출력</span><span class="sxs-lookup"><span data-stu-id="94321-150">OUTPUTS</span></span>

### <span data-ttu-id="94321-151">Api20180730Preview Eadmin. a t t t t 디스크</span><span class="sxs-lookup"><span data-stu-id="94321-151">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180730Preview.IDisk</span></span>



## <span data-ttu-id="94321-152">상속자</span><span class="sxs-lookup"><span data-stu-id="94321-152">NOTES</span></span>

<span data-ttu-id="94321-153">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="94321-153">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="94321-154">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="94321-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="94321-155">INPUTOBJECT <IComputeAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="94321-155">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="94321-156">`[DiskId <String>]`: 디스크 guid를 id로 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="94321-156">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="94321-157">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="94321-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="94321-158">`[Location <String>]`: 리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="94321-158">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="94321-159">`[MigrationId <String>]`: 마이그레이션 작업 guid 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="94321-159">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="94321-160">`[Offer <String>]`: 제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="94321-160">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="94321-161">`[Publisher <String>]`: 게시자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="94321-161">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="94321-162">`[QuotaName <String>]`: 할당량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="94321-162">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="94321-163">`[Sku <String>]`: SKU의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="94321-163">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="94321-164">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="94321-164">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="94321-165">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="94321-165">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="94321-166">`[Type <String>]`: 확장명의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="94321-166">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="94321-167">`[Version <String>]`: 리소스의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="94321-167">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="94321-168">관련 링크</span><span class="sxs-lookup"><span data-stu-id="94321-168">RELATED LINKS</span></span>

