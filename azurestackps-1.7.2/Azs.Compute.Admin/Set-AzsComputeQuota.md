---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4caf955c25cd29c9cc9c09f1182454ee3a4d56df
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93874585"
---
# <span data-ttu-id="4fc1e-101">Set-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="4fc1e-101">Set-AzsComputeQuota</span></span>

## <span data-ttu-id="4fc1e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4fc1e-102">SYNOPSIS</span></span>
<span data-ttu-id="4fc1e-103">제공 된 매개 변수를 사용 하 여 기존 계산 할당량을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fc1e-103">Update an existing compute quota using the provided parameters.</span></span>

## <span data-ttu-id="4fc1e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4fc1e-104">SYNTAX</span></span>

### <span data-ttu-id="4fc1e-105">업데이트 (기본값)</span><span class="sxs-lookup"><span data-stu-id="4fc1e-105">Update (Default)</span></span>
```
Set-AzsComputeQuota -Name <String> [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>]
 [-VmScaleSetCount <Int32>] [-VirtualMachineCount <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-Location <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4fc1e-106">리소스</span><span class="sxs-lookup"><span data-stu-id="4fc1e-106">ResourceId</span></span>
```
Set-AzsComputeQuota [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>] [-VmScaleSetCount <Int32>]
 [-VirtualMachineCount <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-Location <String>] -ResourceId <String> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4fc1e-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="4fc1e-107">InputObject</span></span>
```
Set-AzsComputeQuota [-AvailabilitySetCount <Int32>] [-CoresCount <Int32>] [-VmScaleSetCount <Int32>]
 [-VirtualMachineCount <Int32>] [-StandardManagedDiskAndSnapshotSize <Int32>]
 [-PremiumManagedDiskAndSnapshotSize <Int32>] [-Location <String>] -InputObject <ComputeQuotaObject> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4fc1e-108">설명은</span><span class="sxs-lookup"><span data-stu-id="4fc1e-108">DESCRIPTION</span></span>
<span data-ttu-id="4fc1e-109">기존 계산 할당량을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fc1e-109">Update an existing compute quota.</span></span>

## <span data-ttu-id="4fc1e-110">예제의</span><span class="sxs-lookup"><span data-stu-id="4fc1e-110">EXAMPLES</span></span>

### <span data-ttu-id="4fc1e-111">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="4fc1e-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsComputeQuota -Name Quota1 -VmScaleSetCount 20
```

<span data-ttu-id="4fc1e-112">계산 할당량을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fc1e-112">Update a compute quota.</span></span>

## <span data-ttu-id="4fc1e-113">변수</span><span class="sxs-lookup"><span data-stu-id="4fc1e-113">PARAMETERS</span></span>

### <span data-ttu-id="4fc1e-114">-AvailabilitySetCount</span><span class="sxs-lookup"><span data-stu-id="4fc1e-114">-AvailabilitySetCount</span></span>
<span data-ttu-id="4fc1e-115">허용 되는 가용성 집합 수입니다.</span><span class="sxs-lookup"><span data-stu-id="4fc1e-115">Number of availability sets allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fc1e-116">-CoresCount</span><span class="sxs-lookup"><span data-stu-id="4fc1e-116">-CoresCount</span></span>
<span data-ttu-id="4fc1e-117">허용 되는 코어 수.</span><span class="sxs-lookup"><span data-stu-id="4fc1e-117">Number of cores allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: CoresLimit

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fc1e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4fc1e-118">-InputObject</span></span>
<span data-ttu-id="4fc1e-119">수정 된 계산 할당량 반환 형식 AzsComputeQuota.</span><span class="sxs-lookup"><span data-stu-id="4fc1e-119">Possibly modified compute quota returned form Get-AzsComputeQuota.</span></span>

```yaml
Type: ComputeQuotaObject
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4fc1e-120">-위치</span><span class="sxs-lookup"><span data-stu-id="4fc1e-120">-Location</span></span>
<span data-ttu-id="4fc1e-121">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="4fc1e-121">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fc1e-122">-이름</span><span class="sxs-lookup"><span data-stu-id="4fc1e-122">-Name</span></span>
<span data-ttu-id="4fc1e-123">할당량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4fc1e-123">The name of the quota.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fc1e-124">-PremiumManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="4fc1e-124">-PremiumManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="4fc1e-125">표준 관리 되는 디스크 및 스냅숏에 대 한 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="4fc1e-125">Size for standard managed disks and snapshots allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fc1e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4fc1e-126">-ResourceId</span></span>
<span data-ttu-id="4fc1e-127">ARM 계산 할당량 id입니다.</span><span class="sxs-lookup"><span data-stu-id="4fc1e-127">The ARM compute quota id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4fc1e-128">-StandardManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="4fc1e-128">-StandardManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="4fc1e-129">표준 관리 되는 디스크 및 스냅숏에 대 한 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="4fc1e-129">Size for standard managed disks and snapshots allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fc1e-130">-VirtualMachineCount</span><span class="sxs-lookup"><span data-stu-id="4fc1e-130">-VirtualMachineCount</span></span>
<span data-ttu-id="4fc1e-131">허용 되는 가상 머신 수입니다.</span><span class="sxs-lookup"><span data-stu-id="4fc1e-131">Number of virtual machines allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fc1e-132">-VmScaleSetCount</span><span class="sxs-lookup"><span data-stu-id="4fc1e-132">-VmScaleSetCount</span></span>
<span data-ttu-id="4fc1e-133">허용 되는 배율 집합 수입니다.</span><span class="sxs-lookup"><span data-stu-id="4fc1e-133">Number of scale sets allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fc1e-134">-확인</span><span class="sxs-lookup"><span data-stu-id="4fc1e-134">-Confirm</span></span>
<span data-ttu-id="4fc1e-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fc1e-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fc1e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4fc1e-136">-WhatIf</span></span>
<span data-ttu-id="4fc1e-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4fc1e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4fc1e-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4fc1e-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4fc1e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fc1e-139">CommonParameters</span></span>
<span data-ttu-id="4fc1e-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4fc1e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fc1e-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fc1e-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fc1e-142">입력</span><span class="sxs-lookup"><span data-stu-id="4fc1e-142">INPUTS</span></span>

## <span data-ttu-id="4fc1e-143">출력</span><span class="sxs-lookup"><span data-stu-id="4fc1e-143">OUTPUTS</span></span>

### <span data-ttu-id="4fc1e-144">ComputeQuotaObject</span><span class="sxs-lookup"><span data-stu-id="4fc1e-144">ComputeQuotaObject</span></span>

## <span data-ttu-id="4fc1e-145">상속자</span><span class="sxs-lookup"><span data-stu-id="4fc1e-145">NOTES</span></span>

## <span data-ttu-id="4fc1e-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4fc1e-146">RELATED LINKS</span></span>

