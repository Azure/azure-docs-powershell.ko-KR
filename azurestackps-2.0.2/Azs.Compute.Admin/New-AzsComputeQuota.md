---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/new-azscomputequota
schema: 2.0.0
ms.openlocfilehash: efbd141d5ba41afa51c57f05df96840a81ab4fa1
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94046729"
---
# <span data-ttu-id="4343f-101">New-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="4343f-101">New-AzsComputeQuota</span></span>

## <span data-ttu-id="4343f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4343f-102">SYNOPSIS</span></span>
<span data-ttu-id="4343f-103">제공 된 할당량 매개 변수를 사용 하 여 계산 할당량을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4343f-103">Creates or Updates a Compute Quota with the provided quota parameters.</span></span>

## <span data-ttu-id="4343f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4343f-104">SYNTAX</span></span>

### <span data-ttu-id="4343f-105">CreateExpanded (기본값)</span><span class="sxs-lookup"><span data-stu-id="4343f-105">CreateExpanded (Default)</span></span>
```
New-AzsComputeQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>] [-Location1 <String>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-VirtualMachineCount <Int32>] [-VMScaleSetCount <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="4343f-106">만드는</span><span class="sxs-lookup"><span data-stu-id="4343f-106">Create</span></span>
```
New-AzsComputeQuota -Name <String> -NewQuota <IQuota> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4343f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4343f-107">DESCRIPTION</span></span>
<span data-ttu-id="4343f-108">제공 된 할당량 매개 변수를 사용 하 여 계산 할당량을 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4343f-108">Creates or Updates a Compute Quota with the provided quota parameters.</span></span>

## <span data-ttu-id="4343f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="4343f-109">EXAMPLES</span></span>

### <span data-ttu-id="4343f-110">예제 1: 기본 매개 변수를 사용 하 여 계산 할당량 만들기</span><span class="sxs-lookup"><span data-stu-id="4343f-110">Example 1: Create a Compute Quota with Default Parameters</span></span>
```powershell
PS C:\> New-AzsComputeQuota -Name ExampleComputeQuotaWithDefaultParameters

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

<span data-ttu-id="4343f-111">지정 되지 않은 매개 변수는 위와 같이 기본 매개 변수로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4343f-111">Any parameters that are not specified will be set to their default parameter, shown above.</span></span>

### <span data-ttu-id="4343f-112">예제 2: 사용자 지정 매개 변수를 사용 하 여 계산 할당량 만들기</span><span class="sxs-lookup"><span data-stu-id="4343f-112">Example 2: Create a Compute Quota with Custom Parameters</span></span>
```powershell
PS C:\>  New-AzsComputeQuota -Name ExampleComputeQuotaWithCustomParameters -Location local -AvailabilitySetCount 9 -CoresCount 99 -PremiumManagedDiskAndSnapshotSize 1024 -StandardManagedDiskAndSnapshotSize 1024 -VirtualMachineCount 99 -VMScaleSetCount 2

AvailabilitySetCount               : 9
CoresLimit                         : 99
Id                                 : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Admin/locat
                                     ions/local/quotas/ExampleComputeQuotaWithCustomParameters
Location                           : local
Name                               : ExampleComputeQuotaWithCustomParameters
PremiumManagedDiskAndSnapshotSize  : 1024
StandardManagedDiskAndSnapshotSize : 1024
Type                               : Microsoft.Compute.Admin/quotas
VMScaleSetCount                    : 2
VirtualMachineCount                : 99
```

<span data-ttu-id="4343f-113">매개 변수를 사용 하 여 할당량을 사용자 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4343f-113">Customize Quota with parameters.</span></span> <span data-ttu-id="4343f-114">지정 되지 않은 모든 매개 변수는 default 값을 갖습니다.</span><span class="sxs-lookup"><span data-stu-id="4343f-114">Any parameters not specified will have default value.</span></span>

## <span data-ttu-id="4343f-115">변수</span><span class="sxs-lookup"><span data-stu-id="4343f-115">PARAMETERS</span></span>

### <span data-ttu-id="4343f-116">-AvailabilitySetCount</span><span class="sxs-lookup"><span data-stu-id="4343f-116">-AvailabilitySetCount</span></span>
<span data-ttu-id="4343f-117">허용 되는 최대 가용성 집합 수</span><span class="sxs-lookup"><span data-stu-id="4343f-117">Maximum number of availability sets allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 10
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4343f-118">-CoresCount</span><span class="sxs-lookup"><span data-stu-id="4343f-118">-CoresCount</span></span>
<span data-ttu-id="4343f-119">허용 되는 최대 코어 수.</span><span class="sxs-lookup"><span data-stu-id="4343f-119">Maximum number of cores allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases: CoresLimit

Required: False
Position: Named
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4343f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4343f-120">-DefaultProfile</span></span>
<span data-ttu-id="4343f-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4343f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4343f-122">-위치</span><span class="sxs-lookup"><span data-stu-id="4343f-122">-Location</span></span>
<span data-ttu-id="4343f-123">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="4343f-123">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4343f-124">-Location1</span><span class="sxs-lookup"><span data-stu-id="4343f-124">-Location1</span></span>
<span data-ttu-id="4343f-125">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="4343f-125">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4343f-126">-이름</span><span class="sxs-lookup"><span data-stu-id="4343f-126">-Name</span></span>
<span data-ttu-id="4343f-127">할당량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4343f-127">Name of the quota.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4343f-128">-새 할당량</span><span class="sxs-lookup"><span data-stu-id="4343f-128">-NewQuota</span></span>
<span data-ttu-id="4343f-129">리소스 할당을 제어 하는 데 사용 되는 계산 할당량 정보를 보유 합니다.</span><span class="sxs-lookup"><span data-stu-id="4343f-129">Holds Compute quota information used to control resource allocation.</span></span>
<span data-ttu-id="4343f-130">생성 하려면 새 할당량 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4343f-130">To construct, see NOTES section for NEWQUOTA properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="4343f-131">-PremiumManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="4343f-131">-PremiumManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="4343f-132">허용 되는 premium 유형의 최대 관리 디스크 및 스냅숏 수입니다.</span><span class="sxs-lookup"><span data-stu-id="4343f-132">Maximum number of managed disks and snapshots of type premium allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 2048
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4343f-133">-StandardManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="4343f-133">-StandardManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="4343f-134">허용 되는 표준 유형의 관리 되는 디스크와 스냅샷의 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4343f-134">Maximum number of managed disks and snapshots of type standard allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 2048
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4343f-135">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4343f-135">-SubscriptionId</span></span>
<span data-ttu-id="4343f-136">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="4343f-136">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4343f-137">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="4343f-137">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4343f-138">-VirtualMachineCount</span><span class="sxs-lookup"><span data-stu-id="4343f-138">-VirtualMachineCount</span></span>
<span data-ttu-id="4343f-139">허용 되는 최대 가상 머신 수입니다.</span><span class="sxs-lookup"><span data-stu-id="4343f-139">Maximum number of virtual machines allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4343f-140">-VMScaleSetCount</span><span class="sxs-lookup"><span data-stu-id="4343f-140">-VMScaleSetCount</span></span>
<span data-ttu-id="4343f-141">허용 되는 최대 크기 조정 집합 수입니다.</span><span class="sxs-lookup"><span data-stu-id="4343f-141">Maximum number of scale sets allowed.</span></span>

```yaml
Type: System.Int32
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4343f-142">-확인</span><span class="sxs-lookup"><span data-stu-id="4343f-142">-Confirm</span></span>
<span data-ttu-id="4343f-143">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4343f-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4343f-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4343f-144">-WhatIf</span></span>
<span data-ttu-id="4343f-145">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4343f-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4343f-146">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4343f-146">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4343f-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4343f-147">CommonParameters</span></span>
<span data-ttu-id="4343f-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4343f-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4343f-149">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4343f-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4343f-150">입력</span><span class="sxs-lookup"><span data-stu-id="4343f-150">INPUTS</span></span>

### <span data-ttu-id="4343f-151">Api20180209 (Microsoft. PowerShell. a t t.</span><span class="sxs-lookup"><span data-stu-id="4343f-151">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota</span></span>

## <span data-ttu-id="4343f-152">출력</span><span class="sxs-lookup"><span data-stu-id="4343f-152">OUTPUTS</span></span>

### <span data-ttu-id="4343f-153">Api20180209 (Microsoft. PowerShell. a t t.</span><span class="sxs-lookup"><span data-stu-id="4343f-153">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota</span></span>



## <span data-ttu-id="4343f-154">상속자</span><span class="sxs-lookup"><span data-stu-id="4343f-154">NOTES</span></span>

<span data-ttu-id="4343f-155">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="4343f-155">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4343f-156">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="4343f-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="4343f-157">새 할당량 <IQuota> : 리소스 할당을 제어 하는 데 사용 되는 계산 할당량 정보를 보유 합니다.</span><span class="sxs-lookup"><span data-stu-id="4343f-157">NEWQUOTA <IQuota>: Holds Compute quota information used to control resource allocation.</span></span>
  - <span data-ttu-id="4343f-158">`[Location <String>]`: 리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="4343f-158">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="4343f-159">`[AvailabilitySetCount <Int32?>]`: 허용 되는 최대 가용성 집합 수입니다.</span><span class="sxs-lookup"><span data-stu-id="4343f-159">`[AvailabilitySetCount <Int32?>]`: Maximum number of availability sets allowed.</span></span>
  - <span data-ttu-id="4343f-160">`[CoresLimit <Int32?>]`: 최대 코어 수를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4343f-160">`[CoresLimit <Int32?>]`: Maximum number of cores allowed.</span></span>
  - <span data-ttu-id="4343f-161">`[PremiumManagedDiskAndSnapshotSize <Int32?>]`: 관리 되는 디스크의 최대 수 및 premium 유형의 스냅숏에 허용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4343f-161">`[PremiumManagedDiskAndSnapshotSize <Int32?>]`: Maximum number of managed disks and snapshots of type premium allowed.</span></span>
  - <span data-ttu-id="4343f-162">`[StandardManagedDiskAndSnapshotSize <Int32?>]`: 관리 되는 최대 디스크 수 및 standard 유형의 스냅숏을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4343f-162">`[StandardManagedDiskAndSnapshotSize <Int32?>]`: Maximum number of managed disks and snapshots of type standard allowed.</span></span>
  - <span data-ttu-id="4343f-163">`[VMScaleSetCount <Int32?>]`: 최대 크기 조정 집합을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4343f-163">`[VMScaleSetCount <Int32?>]`: Maximum number of scale sets allowed.</span></span>
  - <span data-ttu-id="4343f-164">`[VirtualMachineCount <Int32?>]`: 허용 되는 최대 가상 머신 수입니다.</span><span class="sxs-lookup"><span data-stu-id="4343f-164">`[VirtualMachineCount <Int32?>]`: Maximum number of virtual machines allowed.</span></span>

## <span data-ttu-id="4343f-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4343f-165">RELATED LINKS</span></span>

