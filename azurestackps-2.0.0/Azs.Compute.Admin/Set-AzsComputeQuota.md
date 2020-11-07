---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/set-azscomputequota
schema: 2.0.0
ms.openlocfilehash: 3229a6383d7159b31bf542add7374326d0de4ac4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93877187"
---
# <span data-ttu-id="1245c-101">Set-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="1245c-101">Set-AzsComputeQuota</span></span>

## <span data-ttu-id="1245c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1245c-102">SYNOPSIS</span></span>


## <span data-ttu-id="1245c-103">구문과</span><span class="sxs-lookup"><span data-stu-id="1245c-103">SYNTAX</span></span>

### <span data-ttu-id="1245c-104">업데이트 (기본값)</span><span class="sxs-lookup"><span data-stu-id="1245c-104">Update (Default)</span></span>
```
Set-AzsComputeQuota -Name <String> -NewQuota <IQuota> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1245c-105">업데이트 (기본값)</span><span class="sxs-lookup"><span data-stu-id="1245c-105">Update (Default)</span></span>
```
Set-AzsComputeQuota -NewQuota <IQuota> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1245c-106">UpdateExpanded</span><span class="sxs-lookup"><span data-stu-id="1245c-106">UpdateExpanded</span></span>
```
Set-AzsComputeQuota -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>] [-Location1 <String>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-VirtualMachineCount <Int32>] [-VMScaleSetCount <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```
## <span data-ttu-id="1245c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="1245c-107">DESCRIPTION</span></span>
<span data-ttu-id="1245c-108">계산 할당량 업데이트</span><span class="sxs-lookup"><span data-stu-id="1245c-108">Update a Compute Quota</span></span>

## <span data-ttu-id="1245c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="1245c-109">EXAMPLES</span></span>

### <span data-ttu-id="1245c-110">예제 1: 기존 계산 할당량에 대 한 속성 설정</span><span class="sxs-lookup"><span data-stu-id="1245c-110">Example 1: Set Properties on an Existing Compute Quota</span></span>
```powershell
PS C:\> $myComputeQuota = Get-AzsComputeQuota -Name MyComputeQuota

PS C:\> $myComputeQuota.CoresLimit = 99; 

PS C:\> Set-AzsComputeQuota -NewQuota $myComputeQuota

AvailabilitySetCount               : 10
CoresLimit                         : 99
Id                                 : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locations/northwest/quotas/MyComputeQuota
Location                           : northwest
Name                               : MyComputeQuota
PremiumManagedDiskAndSnapshotSize  : 2048
StandardManagedDiskAndSnapshotSize : 2048
Type                               : Microsoft.Compute.Admin/quotas
VMScaleSetCount                    : 0
VirtualMachineCount                : 100
```

<span data-ttu-id="1245c-111">명령줄에 지정 된 매개 변수를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1245c-111">Set the parameters specified on the command line.</span></span>
<span data-ttu-id="1245c-112">설정 되지 않은 모든 매개 변수는 기본적으로 0입니다.</span><span class="sxs-lookup"><span data-stu-id="1245c-112">Any parameters not set will default to 0</span></span>

## <span data-ttu-id="1245c-113">변수</span><span class="sxs-lookup"><span data-stu-id="1245c-113">PARAMETERS</span></span>

### <span data-ttu-id="1245c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1245c-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="1245c-115">-새 할당량</span><span class="sxs-lookup"><span data-stu-id="1245c-115">-NewQuota</span></span>
<span data-ttu-id="1245c-116">생성 하려면 새 할당량 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1245c-116">To construct, see NOTES section for NEWQUOTA properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="1245c-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1245c-117">-SubscriptionId</span></span>


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

### <span data-ttu-id="1245c-118">-확인</span><span class="sxs-lookup"><span data-stu-id="1245c-118">-Confirm</span></span>
<span data-ttu-id="1245c-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1245c-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1245c-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1245c-120">-WhatIf</span></span>
<span data-ttu-id="1245c-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1245c-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1245c-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1245c-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1245c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1245c-123">CommonParameters</span></span>
<span data-ttu-id="1245c-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1245c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1245c-125">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1245c-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1245c-126">입력</span><span class="sxs-lookup"><span data-stu-id="1245c-126">INPUTS</span></span>

### <span data-ttu-id="1245c-127">Api20180209 (Microsoft. PowerShell. a t t.</span><span class="sxs-lookup"><span data-stu-id="1245c-127">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota</span></span>

## <span data-ttu-id="1245c-128">출력</span><span class="sxs-lookup"><span data-stu-id="1245c-128">OUTPUTS</span></span>

### <span data-ttu-id="1245c-129">Api20180209 (Microsoft. PowerShell. a t t.</span><span class="sxs-lookup"><span data-stu-id="1245c-129">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota</span></span>



## <span data-ttu-id="1245c-130">상속자</span><span class="sxs-lookup"><span data-stu-id="1245c-130">NOTES</span></span>

<span data-ttu-id="1245c-131">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="1245c-131">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1245c-132">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="1245c-132">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="1245c-133">새 할당량 <IQuota> :</span><span class="sxs-lookup"><span data-stu-id="1245c-133">NEWQUOTA <IQuota>:</span></span> 
  - <span data-ttu-id="1245c-134">`[Location <String>]`: 리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="1245c-134">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="1245c-135">`[AvailabilitySetCount <Int32?>]`: 허용 되는 최대 가용성 집합 수입니다.</span><span class="sxs-lookup"><span data-stu-id="1245c-135">`[AvailabilitySetCount <Int32?>]`: Maximum number of availability sets allowed.</span></span>
  - <span data-ttu-id="1245c-136">`[CoresLimit <Int32?>]`: 최대 코어 수를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1245c-136">`[CoresLimit <Int32?>]`: Maximum number of cores allowed.</span></span>
  - <span data-ttu-id="1245c-137">`[PremiumManagedDiskAndSnapshotSize <Int32?>]`: 관리 되는 디스크의 최대 수 및 premium 유형의 스냅숏에 허용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1245c-137">`[PremiumManagedDiskAndSnapshotSize <Int32?>]`: Maximum number of managed disks and snapshots of type premium allowed.</span></span>
  - <span data-ttu-id="1245c-138">`[StandardManagedDiskAndSnapshotSize <Int32?>]`: 관리 되는 최대 디스크 수 및 standard 유형의 스냅숏을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1245c-138">`[StandardManagedDiskAndSnapshotSize <Int32?>]`: Maximum number of managed disks and snapshots of type standard allowed.</span></span>
  - <span data-ttu-id="1245c-139">`[VMScaleSetCount <Int32?>]`: 최대 크기 조정 집합을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1245c-139">`[VMScaleSetCount <Int32?>]`: Maximum number of scale sets allowed.</span></span>
  - <span data-ttu-id="1245c-140">`[VirtualMachineCount <Int32?>]`: 허용 되는 최대 가상 머신 수입니다.</span><span class="sxs-lookup"><span data-stu-id="1245c-140">`[VirtualMachineCount <Int32?>]`: Maximum number of virtual machines allowed.</span></span>

## <span data-ttu-id="1245c-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1245c-141">RELATED LINKS</span></span>

