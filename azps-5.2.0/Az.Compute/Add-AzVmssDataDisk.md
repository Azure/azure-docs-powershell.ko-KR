---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssDataDisk.md
ms.openlocfilehash: 41728fe644148a575e92136838aaf7f120f89ab7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353253"
---
# <span data-ttu-id="3d197-101">Add-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="3d197-101">Add-AzVmssDataDisk</span></span>

## <span data-ttu-id="3d197-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d197-102">SYNOPSIS</span></span>
<span data-ttu-id="3d197-103">VMSS에 데이터 디스크를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="3d197-103">Adds a data disk to the VMSS.</span></span>

## <span data-ttu-id="3d197-104">구문</span><span class="sxs-lookup"><span data-stu-id="3d197-104">SYNTAX</span></span>

```
Add-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>] [[-Lun] <Int32>]
 [[-Caching] <CachingTypes>] [-WriteAccelerator] [-CreateOption <String>] [-DiskSizeGB <Int32>]
 [-DiskIOPSReadWrite <Int64>] [-DiskMBpsReadWrite <Int64>] [-StorageAccountType <String>]
 [-DiskEncryptionSetId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3d197-105">설명</span><span class="sxs-lookup"><span data-stu-id="3d197-105">DESCRIPTION</span></span>
<span data-ttu-id="3d197-106">**Add-AzVmssDataDisk** cmdlet은 VMSS(Virtual Machine Scale Set) 인스턴스에 데이터 디스크를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="3d197-106">The **Add-AzVmssDataDisk** cmdlet adds a data disk to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="3d197-107">예제</span><span class="sxs-lookup"><span data-stu-id="3d197-107">EXAMPLES</span></span>

### <span data-ttu-id="3d197-108">예제 1: 데이터 디스크 추가</span><span class="sxs-lookup"><span data-stu-id="3d197-108">Example 1: Add a data disk</span></span>
```
PS C:\> $vmss = New-AzVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic"
PS C:\> $vmss = Add-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1' -Lun 0 -Caching 'ReadOnly' -CreateOption Empty -DiskSizeGB 10 -StorageAccountType StandardLRS
```

<span data-ttu-id="3d197-109">이 명령은 VMSS 개체에 빈 데이터 디스크를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="3d197-109">This command adds an empty data disk to the VMSS object.</span></span>

## <span data-ttu-id="3d197-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3d197-110">PARAMETERS</span></span>

### <span data-ttu-id="3d197-111">-캐싱</span><span class="sxs-lookup"><span data-stu-id="3d197-111">-Caching</span></span>
<span data-ttu-id="3d197-112">디스크의 캐싱 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3d197-112">Specifies the caching type of the disk.</span></span>

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

### <span data-ttu-id="3d197-113">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="3d197-113">-CreateOption</span></span>
<span data-ttu-id="3d197-114">디스크의 만들기 옵션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3d197-114">Specifies the create option of the disk.</span></span>

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

### <span data-ttu-id="3d197-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d197-115">-DefaultProfile</span></span>
<span data-ttu-id="3d197-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3d197-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d197-117">-DiskEncryptionSetId</span><span class="sxs-lookup"><span data-stu-id="3d197-117">-DiskEncryptionSetId</span></span>
<span data-ttu-id="3d197-118">고객 관리 디스크 암호화 집합의 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3d197-118">Specifies the resource Id of customer managed disk encryption set.</span></span>  <span data-ttu-id="3d197-119">관리 디스크에만 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d197-119">This can only be specified for managed disk.</span></span>

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

### <span data-ttu-id="3d197-120">-DiskIOPSReadWrite</span><span class="sxs-lookup"><span data-stu-id="3d197-120">-DiskIOPSReadWrite</span></span>
<span data-ttu-id="3d197-121">관리 디스크에 Read-Write IOPS를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3d197-121">Specifies the Read-Write IOPS for the managed disk.</span></span> <span data-ttu-id="3d197-122">StorageAccountType이 UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="3d197-122">Should be used only when StorageAccountType is UltraSSD_LRS.</span></span> <span data-ttu-id="3d197-123">지정하지 않으면 diskSizeGB에 따라 기본값이 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d197-123">If not specified, a default value would be assigned based on diskSizeGB.</span></span>

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

### <span data-ttu-id="3d197-124">-DiskMBpsReadWrite</span><span class="sxs-lookup"><span data-stu-id="3d197-124">-DiskMBpsReadWrite</span></span>
<span data-ttu-id="3d197-125">관리 디스크의 대역폭을 초당 MB로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3d197-125">Specifies the bandwidth in MB per second for the managed disk.</span></span> <span data-ttu-id="3d197-126">StorageAccountType이 UltraSSD_LRS.</span><span class="sxs-lookup"><span data-stu-id="3d197-126">Should be used only when StorageAccountType is UltraSSD_LRS.</span></span> <span data-ttu-id="3d197-127">지정하지 않으면 diskSizeGB에 따라 기본값이 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d197-127">If not specified, a default value would be assigned based on diskSizeGB.</span></span>

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

### <span data-ttu-id="3d197-128">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="3d197-128">-DiskSizeGB</span></span>
<span data-ttu-id="3d197-129">디스크 크기를 GB로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3d197-129">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="3d197-130">-Lun</span><span class="sxs-lookup"><span data-stu-id="3d197-130">-Lun</span></span>
<span data-ttu-id="3d197-131">디스크의 논리 단위 번호를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3d197-131">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="3d197-132">-Name</span><span class="sxs-lookup"><span data-stu-id="3d197-132">-Name</span></span>
<span data-ttu-id="3d197-133">디스크의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3d197-133">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="3d197-134">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="3d197-134">-StorageAccountType</span></span>
<span data-ttu-id="3d197-135">디스크의 저장소 계정 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3d197-135">Specifies the storage account type of the disk.</span></span>

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

### <span data-ttu-id="3d197-136">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="3d197-136">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="3d197-137">VMSS 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3d197-137">Specify the VMSS object.</span></span>
<span data-ttu-id="3d197-138">[New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet을 사용하여 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d197-138">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="3d197-139">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="3d197-139">-WriteAccelerator</span></span>
<span data-ttu-id="3d197-140">데이터 디스크에서 WriteAccelerator를 사용할지 또는 사용하지 않도록 설정해야 하는지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3d197-140">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

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

### <span data-ttu-id="3d197-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3d197-141">-Confirm</span></span>
<span data-ttu-id="3d197-142">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d197-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d197-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d197-143">-WhatIf</span></span>
<span data-ttu-id="3d197-144">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="3d197-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d197-145">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3d197-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d197-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d197-146">CommonParameters</span></span>
<span data-ttu-id="3d197-147">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3d197-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d197-148">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3d197-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d197-149">입력</span><span class="sxs-lookup"><span data-stu-id="3d197-149">INPUTS</span></span>

### <span data-ttu-id="3d197-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="3d197-150">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="3d197-151">System.String</span><span class="sxs-lookup"><span data-stu-id="3d197-151">System.String</span></span>

### <span data-ttu-id="3d197-152">System.Int32</span><span class="sxs-lookup"><span data-stu-id="3d197-152">System.Int32</span></span>

### <span data-ttu-id="3d197-153">System.Nullable'1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="3d197-153">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=23.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="3d197-154">출력</span><span class="sxs-lookup"><span data-stu-id="3d197-154">OUTPUTS</span></span>

### <span data-ttu-id="3d197-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="3d197-155">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="3d197-156">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3d197-156">NOTES</span></span>

## <span data-ttu-id="3d197-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3d197-157">RELATED LINKS</span></span>
