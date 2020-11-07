---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ffd2667f8c07c5b0594abe38f6cee5d40ce91a49
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93875044"
---
# <span data-ttu-id="caa28-101">New-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="caa28-101">New-AzsComputeQuota</span></span>

## <span data-ttu-id="caa28-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="caa28-102">SYNOPSIS</span></span>
<span data-ttu-id="caa28-103">계산 리소스를 제한 하는 데 사용 되는 새 계산 할당량을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="caa28-103">Create a new compute quota used to limit compute resources.</span></span>

## <span data-ttu-id="caa28-104">구문과</span><span class="sxs-lookup"><span data-stu-id="caa28-104">SYNTAX</span></span>

```
New-AzsComputeQuota [-Name] <String> [[-AvailabilitySetCount] <Int32>] [[-CoresCount] <Int32>]
 [[-VmScaleSetCount] <Int32>] [[-VirtualMachineCount] <Int32>] [[-StandardManagedDiskAndSnapshotSize] <Int32>]
 [[-PremiumManagedDiskAndSnapshotSize] <Int32>] [[-Location] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="caa28-105">설명은</span><span class="sxs-lookup"><span data-stu-id="caa28-105">DESCRIPTION</span></span>
<span data-ttu-id="caa28-106">새 계산 할당량을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="caa28-106">Create a new compute quota.</span></span>

## <span data-ttu-id="caa28-107">예제의</span><span class="sxs-lookup"><span data-stu-id="caa28-107">EXAMPLES</span></span>

### <span data-ttu-id="caa28-108">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="caa28-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
New-AzsComputeQuota -Name testQuota5 -AvailabilitySetCount 1000 -CoresCount 1000 -VmScaleSetCount 1000 -VirtualMachineCount 1000 -StandardManagedDiskAndSnapshotSize 1024 -PremiumManagedDiskAndSnapshotSize 1024
```

<span data-ttu-id="caa28-109">새 계산 할당량을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="caa28-109">Create a new compute quota.</span></span>

## <span data-ttu-id="caa28-110">변수</span><span class="sxs-lookup"><span data-stu-id="caa28-110">PARAMETERS</span></span>

### <span data-ttu-id="caa28-111">-AvailabilitySetCount</span><span class="sxs-lookup"><span data-stu-id="caa28-111">-AvailabilitySetCount</span></span>
<span data-ttu-id="caa28-112">허용 되는 가용성 집합 수입니다.</span><span class="sxs-lookup"><span data-stu-id="caa28-112">Number  of availability sets allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: 10
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caa28-113">-CoresCount</span><span class="sxs-lookup"><span data-stu-id="caa28-113">-CoresCount</span></span>
<span data-ttu-id="caa28-114">허용 되는 코어 수.</span><span class="sxs-lookup"><span data-stu-id="caa28-114">Number  of cores allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: CoresLimit

Required: False
Position: 3
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caa28-115">-위치</span><span class="sxs-lookup"><span data-stu-id="caa28-115">-Location</span></span>
<span data-ttu-id="caa28-116">리소스의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="caa28-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caa28-117">-이름</span><span class="sxs-lookup"><span data-stu-id="caa28-117">-Name</span></span>
<span data-ttu-id="caa28-118">할당량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="caa28-118">Name of the quota.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caa28-119">-PremiumManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="caa28-119">-PremiumManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="caa28-120">표준 관리 되는 디스크 및 스냅숏에 대 한 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="caa28-120">Size for standard managed disks and snapshots allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: 2048
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caa28-121">-StandardManagedDiskAndSnapshotSize</span><span class="sxs-lookup"><span data-stu-id="caa28-121">-StandardManagedDiskAndSnapshotSize</span></span>
<span data-ttu-id="caa28-122">표준 관리 되는 디스크 및 스냅숏에 대 한 크기입니다.</span><span class="sxs-lookup"><span data-stu-id="caa28-122">Size for standard managed disks and snapshots allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: 2048
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caa28-123">-VirtualMachineCount</span><span class="sxs-lookup"><span data-stu-id="caa28-123">-VirtualMachineCount</span></span>
<span data-ttu-id="caa28-124">허용 되는 가상 머신 수입니다.</span><span class="sxs-lookup"><span data-stu-id="caa28-124">Number  of virtual machines allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caa28-125">-VmScaleSetCount</span><span class="sxs-lookup"><span data-stu-id="caa28-125">-VmScaleSetCount</span></span>
<span data-ttu-id="caa28-126">허용 되는 배율 집합 수입니다.</span><span class="sxs-lookup"><span data-stu-id="caa28-126">Number  of scale sets allowed.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: 100
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caa28-127">-확인</span><span class="sxs-lookup"><span data-stu-id="caa28-127">-Confirm</span></span>
<span data-ttu-id="caa28-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="caa28-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="caa28-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="caa28-129">-WhatIf</span></span>
<span data-ttu-id="caa28-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="caa28-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="caa28-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="caa28-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="caa28-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="caa28-132">CommonParameters</span></span>
<span data-ttu-id="caa28-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="caa28-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="caa28-134">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="caa28-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="caa28-135">입력</span><span class="sxs-lookup"><span data-stu-id="caa28-135">INPUTS</span></span>

## <span data-ttu-id="caa28-136">출력</span><span class="sxs-lookup"><span data-stu-id="caa28-136">OUTPUTS</span></span>

### <span data-ttu-id="caa28-137">ComputeQuotaObject</span><span class="sxs-lookup"><span data-stu-id="caa28-137">ComputeQuotaObject</span></span>

## <span data-ttu-id="caa28-138">상속자</span><span class="sxs-lookup"><span data-stu-id="caa28-138">NOTES</span></span>

## <span data-ttu-id="caa28-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="caa28-139">RELATED LINKS</span></span>

