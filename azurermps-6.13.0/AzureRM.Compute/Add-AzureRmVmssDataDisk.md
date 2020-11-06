---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVmssDataDisk.md
ms.openlocfilehash: 0ef680f60f48451e5d5dd9bff730cbfe4ebc9aae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531414"
---
# <span data-ttu-id="24990-101">Add-AzureRmVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="24990-101">Add-AzureRmVmssDataDisk</span></span>

## <span data-ttu-id="24990-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24990-102">SYNOPSIS</span></span>
<span data-ttu-id="24990-103">VMSS에 데이터 디스크를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="24990-103">Adds a data disk to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24990-104">구문과</span><span class="sxs-lookup"><span data-stu-id="24990-104">SYNTAX</span></span>

```
Add-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Lun] <Int32>] [[-Caching] <CachingTypes>] [-WriteAccelerator] [-CreateOption <String>]
 [-DiskSizeGB <Int32>] [-StorageAccountType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24990-105">설명은</span><span class="sxs-lookup"><span data-stu-id="24990-105">DESCRIPTION</span></span>
<span data-ttu-id="24990-106">**AzureRmVmssDataDisk** cmdlet은 데이터 디스크를 Vmss (가상 컴퓨터 크기 조정 집합) 인스턴스에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="24990-106">The **Add-AzureRmVmssDataDisk** cmdlet adds a data disk to the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="24990-107">예제의</span><span class="sxs-lookup"><span data-stu-id="24990-107">EXAMPLES</span></span>

### <span data-ttu-id="24990-108">예제 1: 데이터 디스크 추가</span><span class="sxs-lookup"><span data-stu-id="24990-108">Example 1: Add a data disk</span></span>
```
PS C:\> $vmss = New-AzureRmVmssConfig -Location $Loc -SkuCapacity 2 -SkuName "Standard_A0" -UpgradePolicyMode "Automatic"
PS C:\> $vmss = Add-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1' -Lun 0 -Caching 'ReadOnly' -CreateOption Empty -DiskSizeGB 10 -StorageAccountType StandardLRS
```

<span data-ttu-id="24990-109">이 명령은 VMSS 개체에 빈 데이터 디스크를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="24990-109">This command adds an empty data disk to the VMSS object.</span></span>

## <span data-ttu-id="24990-110">변수</span><span class="sxs-lookup"><span data-stu-id="24990-110">PARAMETERS</span></span>

### <span data-ttu-id="24990-111">-캐싱</span><span class="sxs-lookup"><span data-stu-id="24990-111">-Caching</span></span>
<span data-ttu-id="24990-112">디스크의 캐싱 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24990-112">Specifies the caching type of the disk.</span></span>

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

### <span data-ttu-id="24990-113">-CreateOption</span><span class="sxs-lookup"><span data-stu-id="24990-113">-CreateOption</span></span>
<span data-ttu-id="24990-114">디스크의 만들기 옵션을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24990-114">Specifies the create option of the disk.</span></span>

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

### <span data-ttu-id="24990-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24990-115">-DefaultProfile</span></span>
<span data-ttu-id="24990-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="24990-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24990-117">-DiskSizeGB</span><span class="sxs-lookup"><span data-stu-id="24990-117">-DiskSizeGB</span></span>
<span data-ttu-id="24990-118">디스크 크기 (GB)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24990-118">Specifies the size of the disk in GB.</span></span>

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

### <span data-ttu-id="24990-119">-Lun</span><span class="sxs-lookup"><span data-stu-id="24990-119">-Lun</span></span>
<span data-ttu-id="24990-120">디스크의 논리 단위 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24990-120">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="24990-121">-이름</span><span class="sxs-lookup"><span data-stu-id="24990-121">-Name</span></span>
<span data-ttu-id="24990-122">디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24990-122">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="24990-123">-StorageAccountType</span><span class="sxs-lookup"><span data-stu-id="24990-123">-StorageAccountType</span></span>
<span data-ttu-id="24990-124">디스크의 저장소 계정 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24990-124">Specifies the storage account type of the disk.</span></span>

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

### <span data-ttu-id="24990-125">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="24990-125">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="24990-126">VMSS 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24990-126">Specify the VMSS object.</span></span>
<span data-ttu-id="24990-127">[새 AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet을 사용 하 여 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="24990-127">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="24990-128">-WriteAccelerator</span><span class="sxs-lookup"><span data-stu-id="24990-128">-WriteAccelerator</span></span>
<span data-ttu-id="24990-129">데이터 디스크에서 WriteAccelerator를 사용할지 아니면 disabled를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24990-129">Specifies whether WriteAccelerator should be enabled or disabled on the data disk.</span></span>

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

### <span data-ttu-id="24990-130">-확인</span><span class="sxs-lookup"><span data-stu-id="24990-130">-Confirm</span></span>
<span data-ttu-id="24990-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="24990-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24990-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24990-132">-WhatIf</span></span>
<span data-ttu-id="24990-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="24990-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24990-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="24990-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24990-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24990-135">CommonParameters</span></span>
<span data-ttu-id="24990-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="24990-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24990-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24990-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24990-138">입력</span><span class="sxs-lookup"><span data-stu-id="24990-138">INPUTS</span></span>

### <span data-ttu-id="24990-139">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="24990-139">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="24990-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="24990-140">System.String</span></span>

### <span data-ttu-id="24990-141">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="24990-141">System.Int32</span></span>

### <span data-ttu-id="24990-142">시스템 Null 허용 ' 1 [[21.0.0.0], [[Microsoft Azure. 31bf3856ad364e35.-Management. 관리. t e;. i =, Culture = 중립, PublicKeyToken =]]</span><span class="sxs-lookup"><span data-stu-id="24990-142">System.Nullable\`1[[Microsoft.Azure.Management.Compute.Models.CachingTypes, Microsoft.Azure.Management.Compute, Version=21.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="24990-143">출력</span><span class="sxs-lookup"><span data-stu-id="24990-143">OUTPUTS</span></span>

### <span data-ttu-id="24990-144">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="24990-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="24990-145">상속자</span><span class="sxs-lookup"><span data-stu-id="24990-145">NOTES</span></span>

## <span data-ttu-id="24990-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="24990-146">RELATED LINKS</span></span>
