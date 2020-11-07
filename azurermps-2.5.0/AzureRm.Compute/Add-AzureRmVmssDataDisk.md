---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmssdatadisk
schema: 2.0.0
ms.openlocfilehash: c91b9dc68bcc0cdecda9ced83a9b3c64452d6413
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881173"
---
# <span data-ttu-id="882d0-101">Add-AzureRmVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="882d0-101">Add-AzureRmVmssDataDisk</span></span>

## <span data-ttu-id="882d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="882d0-102">SYNOPSIS</span></span>
<span data-ttu-id="882d0-103">VMSS에 데이터 디스크를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="882d0-103">Adds a data disk to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="882d0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="882d0-104">SYNTAX</span></span>

```
Add-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Lun] <Int32>] [[-Caching] <CachingTypes>] [-WriteAccelerator] [-CreateOption <DiskCreateOptionTypes>]
 [-DiskSizeGB <Int32>] [-StorageAccountType <StorageAccountTypes>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="882d0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="882d0-105">DESCRIPTION</span></span>
<span data-ttu-id="882d0-106">**AzureRmVmssDataDisk** cmdlet은 데이터 디스크를 Vmss (가상 컴퓨터 크기 조정 집합) 인스턴스에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="882d0-106">The **Add-AzureRmVmssDataDisk** cmdlet adds a data disk to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="882d0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="882d0-107">EXAMPLES</span></span>

### <span data-ttu-id="882d0-108">예제 1: 데이터 디스크 추가</span><span class="sxs-lookup"><span data-stu-id="882d0-108">Example 1: Add a data disk</span></span>
```
PS C:\> $vmss = New-AzureRmVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic"
PS C:\> $vmss = Add-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1' -Lun 0 -Caching 'ReadOnly' -CreateOption Empty -DiskSizeGB 10 -StorageAccountType StandardLRS
```

<span data-ttu-id="882d0-109">이 명령은 VMSS 개체에 빈 데이터 디스크를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="882d0-109">This command adds an empty data disk to the VMSS object.</span></span>

## <span data-ttu-id="882d0-110">변수</span><span class="sxs-lookup"><span data-stu-id="882d0-110">PARAMETERS</span></span>

### <span data-ttu-id="882d0-111">-캐싱</span><span class="sxs-lookup"><span data-stu-id="882d0-111">-Caching</span></span>
<span data-ttu-id="882d0-112">디스크의 캐싱 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="882d0-112">Specifies the caching type of the disk.</span></span>

```yaml
Type: CachingTypes
Parameter Sets: (All)
Aliases: 
Accepted values: None, ReadOnly, ReadWrite

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="882d0-113">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="882d0-113">-CreateOption</span></span>
<span data-ttu-id="882d0-114">디스크의 만들기 옵션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="882d0-114">Specifies the create option of the disk.</span></span>

```yaml
Type: DiskCreateOptionTypes
Parameter Sets: (All)
Aliases: 
Accepted values: FromImage, Empty, Attach

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="882d0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="882d0-115">-DefaultProfile</span></span>
<span data-ttu-id="882d0-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="882d0-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="882d0-117">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="882d0-117">-DiskSizeGB</span></span>
<span data-ttu-id="882d0-118">디스크 크기 (GB)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="882d0-118">Specifies the size of the disk in GB.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="882d0-119">-Lun</span><span class="sxs-lookup"><span data-stu-id="882d0-119">-Lun</span></span>
<span data-ttu-id="882d0-120">디스크의 논리 단위 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="882d0-120">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="882d0-121">-이름</span><span class="sxs-lookup"><span data-stu-id="882d0-121">-Name</span></span>
<span data-ttu-id="882d0-122">디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="882d0-122">Specifies the name of the disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="882d0-123">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="882d0-123">-StorageAccountType</span></span>
<span data-ttu-id="882d0-124">디스크의 저장소 계정 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="882d0-124">Specifies the storage account type of the disk.</span></span>

```yaml
Type: StorageAccountTypes
Parameter Sets: (All)
Aliases: 
Accepted values: StandardLRS, PremiumLRS

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="882d0-125">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="882d0-125">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="882d0-126">VMSS 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="882d0-126">Specify the VMSS object.</span></span>
<span data-ttu-id="882d0-127">[새 AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet을 사용 하 여 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="882d0-127">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="882d0-128">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="882d0-128">-WriteAccelerator</span></span>
<span data-ttu-id="882d0-129">데이터 디스크에서 WriteAccelerator를 사용할지 아니면 disabled를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="882d0-129">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="882d0-130">-확인</span><span class="sxs-lookup"><span data-stu-id="882d0-130">-Confirm</span></span>
<span data-ttu-id="882d0-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="882d0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="882d0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="882d0-132">-WhatIf</span></span>
<span data-ttu-id="882d0-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="882d0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="882d0-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="882d0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="882d0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="882d0-135">CommonParameters</span></span>
<span data-ttu-id="882d0-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="882d0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="882d0-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="882d0-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="882d0-138">입력</span><span class="sxs-lookup"><span data-stu-id="882d0-138">INPUTS</span></span>

### <span data-ttu-id="882d0-139">VirtualMachineScaleSet를 통해 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="882d0-139">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="882d0-140">시스템. Int32 시스템. Nullable `1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[Microsoft. azure. 14.0.0.0 Create 형식, Microsoft Azure. 관리. compute, Version =, Culture = 중립, PublicKeyToken = 31bf3856ad364e35]] System. Nullable 1 [[Microsoft azure. i n a. i n. 관리. i n i n. i n. 관리. i n i = `1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable` 14.0.0.0, Culture = 중립, PublicKeyToken = 31bf3856ad364e35]</span><span class="sxs-lookup"><span data-stu-id="882d0-140">System.String System.Int32 System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOptionTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="882d0-141">출력</span><span class="sxs-lookup"><span data-stu-id="882d0-141">OUTPUTS</span></span>

### <span data-ttu-id="882d0-142">VirtualMachineScaleSet를 통해 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="882d0-142">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="882d0-143">상속자</span><span class="sxs-lookup"><span data-stu-id="882d0-143">NOTES</span></span>

## <span data-ttu-id="882d0-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="882d0-144">RELATED LINKS</span></span>

