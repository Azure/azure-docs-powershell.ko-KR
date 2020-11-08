---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDataDisk.md
ms.openlocfilehash: 41728fe644148a575e92136838aaf7f120f89ab7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94049138"
---
# <span data-ttu-id="cefcc-101">Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="cefcc-101">Add-AzVmssDataDisk</span></span>

## <span data-ttu-id="cefcc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cefcc-102">SYNOPSIS</span></span>
<span data-ttu-id="cefcc-103">VMSS에 데이터 디스크를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="cefcc-103">Adds a data disk to the VMSS.</span></span>

## <span data-ttu-id="cefcc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="cefcc-104">SYNTAX</span></span>

```
Add-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>] [[-Lun] <Int32>]
 [[-Caching] <CachingTypes>] [-WriteAccelerator] [-CreateOption <String>] [-DiskSizeGB <Int32>]
 [-DiskIOPSReadWrite <Int64>] [-DiskMBpsReadWrite <Int64>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cefcc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="cefcc-105">DESCRIPTION</span></span>
<span data-ttu-id="cefcc-106">**AzVmssDataDisk** cmdlet은 데이터 디스크를 Vmss (가상 컴퓨터 크기 조정 집합) 인스턴스에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="cefcc-106">The **Add-AzVmssDataDisk** cmdlet adds a data disk to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="cefcc-107">예제의</span><span class="sxs-lookup"><span data-stu-id="cefcc-107">EXAMPLES</span></span>

### <span data-ttu-id="cefcc-108">예제 1: 데이터 디스크 추가</span><span class="sxs-lookup"><span data-stu-id="cefcc-108">Example 1: Add a data disk</span></span>
```
PS C:\> $vmss = New-AzVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic"
PS C:\> $vmss = Add-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1' -Lun 0 -Caching 'ReadOnly' -CreateOption Empty -DiskSizeGB 10 -StorageAccountType StandardLRS
```

<span data-ttu-id="cefcc-109">이 명령은 VMSS 개체에 빈 데이터 디스크를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="cefcc-109">This command adds an empty data disk to the VMSS object.</span></span>

## <span data-ttu-id="cefcc-110">변수</span><span class="sxs-lookup"><span data-stu-id="cefcc-110">PARAMETERS</span></span>

### <span data-ttu-id="cefcc-111">-캐싱</span><span class="sxs-lookup"><span data-stu-id="cefcc-111">-Caching</span></span>
<span data-ttu-id="cefcc-112">디스크의 캐싱 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cefcc-112">Specifies the caching type of the disk.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.CachingTypes]
Parameter Sets: (All)
Aliases:
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cefcc-113">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="cefcc-113">-CreateOption</span></span>
<span data-ttu-id="cefcc-114">디스크의 만들기 옵션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cefcc-114">Specifies the create option of the disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cefcc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cefcc-115">-DefaultProfile</span></span>
<span data-ttu-id="cefcc-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="cefcc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cefcc-117">-Disk. Setid</span><span class="sxs-lookup"><span data-stu-id="cefcc-117">-DiskEncryptionSetId</span></span>
<span data-ttu-id="cefcc-118">고객 관리 디스크 암호화 집합의 리소스 Id를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cefcc-118">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="cefcc-119">이는 관리 디스크에 대해서만 지정 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cefcc-119">This can only be specified for managed disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cefcc-120">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="cefcc-120">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="cefcc-121">관리 디스크에 대 한 Read-Write IOPS를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cefcc-121">Specifies the Read-Write IOPS for the managed disk.</span></span> <span data-ttu-id="cefcc-122">StorageAccountType이 UltraSSD_LRS 경우에만 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cefcc-122">Should be used only when StorageAccountType is UltraSSD_LRS.</span></span> <span data-ttu-id="cefcc-123">지정 하지 않으면 diskSizeGB를 기준으로 기본값을 할당 받습니다.</span><span class="sxs-lookup"><span data-stu-id="cefcc-123">If not specified, a default value would be assigned based on diskSizeGB.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cefcc-124">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="cefcc-124">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="cefcc-125">관리 디스크의 대역폭 (초당 MB)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cefcc-125">Specifies the bandwidth in MB per second for the managed disk.</span></span> <span data-ttu-id="cefcc-126">StorageAccountType이 UltraSSD_LRS 경우에만 사용 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="cefcc-126">Should be used only when StorageAccountType is UltraSSD_LRS.</span></span> <span data-ttu-id="cefcc-127">지정 하지 않으면 diskSizeGB를 기준으로 기본값을 할당 받습니다.</span><span class="sxs-lookup"><span data-stu-id="cefcc-127">If not specified, a default value would be assigned based on diskSizeGB.</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cefcc-128">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="cefcc-128">-DiskSizeGB</span></span>
<span data-ttu-id="cefcc-129">디스크 크기 (GB)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cefcc-129">Specifies the size of the disk in GB.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cefcc-130">-Lun</span><span class="sxs-lookup"><span data-stu-id="cefcc-130">-Lun</span></span>
<span data-ttu-id="cefcc-131">디스크의 논리 단위 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cefcc-131">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cefcc-132">-이름</span><span class="sxs-lookup"><span data-stu-id="cefcc-132">-Name</span></span>
<span data-ttu-id="cefcc-133">디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cefcc-133">Specifies the name of the disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cefcc-134">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="cefcc-134">-StorageAccountType</span></span>
<span data-ttu-id="cefcc-135">디스크의 저장소 계정 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cefcc-135">Specifies the storage account type of the disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cefcc-136">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="cefcc-136">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="cefcc-137">VMSS 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cefcc-137">Specify the VMSS object.</span></span>
<span data-ttu-id="cefcc-138">[새 AzVmssConfig](./New-AzVmssConfig.md) cmdlet을 사용 하 여 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="cefcc-138">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cefcc-139">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="cefcc-139">-WriteAccelerator</span></span>
<span data-ttu-id="cefcc-140">데이터 디스크에서 WriteAccelerator를 사용할지 아니면 disabled를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="cefcc-140">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

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

### <span data-ttu-id="cefcc-141">-확인</span><span class="sxs-lookup"><span data-stu-id="cefcc-141">-Confirm</span></span>
<span data-ttu-id="cefcc-142">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="cefcc-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cefcc-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cefcc-143">-WhatIf</span></span>
<span data-ttu-id="cefcc-144">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="cefcc-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cefcc-145">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cefcc-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cefcc-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cefcc-146">CommonParameters</span></span>
<span data-ttu-id="cefcc-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="cefcc-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cefcc-148">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="cefcc-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cefcc-149">입력</span><span class="sxs-lookup"><span data-stu-id="cefcc-149">INPUTS</span></span>

### <span data-ttu-id="cefcc-150">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="cefcc-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="cefcc-151">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="cefcc-151">System.String</span></span>

### <span data-ttu-id="cefcc-152">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="cefcc-152">System.Int32</span></span>

### <span data-ttu-id="cefcc-153">시스템 Null 허용 ' 1 [[23.0.0.0], [[Microsoft Azure. 31bf3856ad364e35.-Management. 관리. t e;. i =, Culture = 중립, PublicKeyToken =]]</span><span class="sxs-lookup"><span data-stu-id="cefcc-153">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="cefcc-154">출력</span><span class="sxs-lookup"><span data-stu-id="cefcc-154">OUTPUTS</span></span>

### <span data-ttu-id="cefcc-155">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="cefcc-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="cefcc-156">상속자</span><span class="sxs-lookup"><span data-stu-id="cefcc-156">NOTES</span></span>

## <span data-ttu-id="cefcc-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cefcc-157">RELATED LINKS</span></span>
