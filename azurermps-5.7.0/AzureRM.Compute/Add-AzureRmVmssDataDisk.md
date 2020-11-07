---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssDataDisk.md
ms.openlocfilehash: e2eca141678c5455df0e443c155693c3c1445e19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702871"
---
# <span data-ttu-id="c186e-101">Add-AzureRmVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="c186e-101">Add-AzureRmVmssDataDisk</span></span>

## <span data-ttu-id="c186e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c186e-102">SYNOPSIS</span></span>
<span data-ttu-id="c186e-103">VMSS에 데이터 디스크를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c186e-103">Adds a data disk to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c186e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c186e-104">SYNTAX</span></span>

```
Add-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Name] <String>] [[-Lun] <Int32>]
 [[-Caching] <CachingTypes>] [-CreateOption <DiskCreateOptionTypes>] [-DiskSizeGB <Int32>]
 [-StorageAccountType <StorageAccountTypes>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c186e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c186e-105">DESCRIPTION</span></span>
<span data-ttu-id="c186e-106">**AzureRmVmssDataDisk** cmdlet은 데이터 디스크를 Vmss (가상 컴퓨터 크기 조정 집합) 인스턴스에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c186e-106">The **Add-AzureRmVmssDataDisk** cmdlet adds a data disk to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="c186e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c186e-107">EXAMPLES</span></span>

### <span data-ttu-id="c186e-108">예제 1: 데이터 디스크 추가</span><span class="sxs-lookup"><span data-stu-id="c186e-108">Example 1: Add a data disk</span></span>
```
PS C:\> $vmss = New-AzureRmVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic"
PS C:\> $vmss = Add-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1' -Lun 0 -Caching 'ReadOnly' -CreateOption Empty -DiskSizeGB 10 -StorageAccountType StandardLRS
```

<span data-ttu-id="c186e-109">이 명령은 VMSS 개체에 빈 데이터 디스크를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c186e-109">This command adds an empty data disk to the VMSS object.</span></span>

## <span data-ttu-id="c186e-110">변수</span><span class="sxs-lookup"><span data-stu-id="c186e-110">PARAMETERS</span></span>

### <span data-ttu-id="c186e-111">-캐싱</span><span class="sxs-lookup"><span data-stu-id="c186e-111">-Caching</span></span>
<span data-ttu-id="c186e-112">디스크의 캐싱 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c186e-112">Specifies the caching type of the disk.</span></span>

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

### <span data-ttu-id="c186e-113">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="c186e-113">-CreateOption</span></span>
<span data-ttu-id="c186e-114">디스크의 만들기 옵션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c186e-114">Specifies the create option of the disk.</span></span>

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

### <span data-ttu-id="c186e-115">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="c186e-115">-DiskSizeGB</span></span>
<span data-ttu-id="c186e-116">디스크 크기 (GB)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c186e-116">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="c186e-117">-Lun</span><span class="sxs-lookup"><span data-stu-id="c186e-117">-Lun</span></span>
<span data-ttu-id="c186e-118">디스크의 논리 단위 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c186e-118">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="c186e-119">-이름</span><span class="sxs-lookup"><span data-stu-id="c186e-119">-Name</span></span>
<span data-ttu-id="c186e-120">디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c186e-120">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="c186e-121">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="c186e-121">-StorageAccountType</span></span>
<span data-ttu-id="c186e-122">디스크의 저장소 계정 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c186e-122">Specifies the storage account type of the disk.</span></span>

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

### <span data-ttu-id="c186e-123">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="c186e-123">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="c186e-124">VMSS 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c186e-124">Specify the VMSS object.</span></span>
<span data-ttu-id="c186e-125">[새 AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet을 사용 하 여 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c186e-125">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c186e-126">-확인</span><span class="sxs-lookup"><span data-stu-id="c186e-126">-Confirm</span></span>
<span data-ttu-id="c186e-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c186e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c186e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c186e-128">-WhatIf</span></span>
<span data-ttu-id="c186e-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c186e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c186e-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c186e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c186e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c186e-131">CommonParameters</span></span>
<span data-ttu-id="c186e-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c186e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c186e-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c186e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c186e-134">입력</span><span class="sxs-lookup"><span data-stu-id="c186e-134">INPUTS</span></span>

### <span data-ttu-id="c186e-135">VirtualMachineScaleSet를 통해 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="c186e-135">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="c186e-136">시스템. Int32 시스템. Nullable `1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable` 1 [[Microsoft. azure. 14.0.0.0 Create 형식, Microsoft Azure. 관리. compute, Version =, Culture = 중립, PublicKeyToken = 31bf3856ad364e35]] System. Nullable 1 [[Microsoft azure. i n a. i n. 관리. i n i n. i n. 관리. i n i = `1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable` 14.0.0.0, Culture = 중립, PublicKeyToken = 31bf3856ad364e35]</span><span class="sxs-lookup"><span data-stu-id="c186e-136">System.String System.Int32 System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.DiskCreateOptionTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]] System.Nullable`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]
System.Nullable`1[[Microsoft.Azure.Management.Compute.Models.StorageAccountTypes, Microsoft.Azure.Management.Compute, Version=14.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="c186e-137">출력</span><span class="sxs-lookup"><span data-stu-id="c186e-137">OUTPUTS</span></span>

### <span data-ttu-id="c186e-138">VirtualMachineScaleSet를 통해 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="c186e-138">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="c186e-139">상속자</span><span class="sxs-lookup"><span data-stu-id="c186e-139">NOTES</span></span>

## <span data-ttu-id="c186e-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c186e-140">RELATED LINKS</span></span>
