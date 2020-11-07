---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDataDisk.md
ms.openlocfilehash: 293bb0f314b82ed2318684996f9b18c79a3b81d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702033"
---
# <span data-ttu-id="f23e5-101">Remove-AzureRmVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="f23e5-101">Remove-AzureRmVmssDataDisk</span></span>

## <span data-ttu-id="f23e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f23e5-102">SYNOPSIS</span></span>
<span data-ttu-id="f23e5-103">VMSS에서 데이터 디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f23e5-103">Removes a data disk from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f23e5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f23e5-104">SYNTAX</span></span>

### <span data-ttu-id="f23e5-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f23e5-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-Name] <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f23e5-106">LunParameterSet</span><span class="sxs-lookup"><span data-stu-id="f23e5-106">LunParameterSet</span></span>
```
Remove-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-Lun] <Int32> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f23e5-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f23e5-107">DESCRIPTION</span></span>
<span data-ttu-id="f23e5-108">**AzureRmVmssDataDisk** CMDLET은 Vmss (가상 컴퓨터 배율 집합) 인스턴스에서 데이터 디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f23e5-108">The **Remove-AzureRmVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="f23e5-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f23e5-109">EXAMPLES</span></span>

### <span data-ttu-id="f23e5-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="f23e5-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="f23e5-111">이 명령은 VMSS 개체에서 이름이 ' DataDisk1 ' 인 데이터 디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f23e5-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="f23e5-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="f23e5-112">Example 2</span></span>
```
PS C:\> Remove-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="f23e5-113">이 명령은 VMSS 개체에서 LUN 0의 데이터 디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f23e5-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="f23e5-114">변수</span><span class="sxs-lookup"><span data-stu-id="f23e5-114">PARAMETERS</span></span>

### <span data-ttu-id="f23e5-115">-Lun</span><span class="sxs-lookup"><span data-stu-id="f23e5-115">-Lun</span></span>
<span data-ttu-id="f23e5-116">디스크의 논리 단위 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f23e5-116">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: Int32
Parameter Sets: LunParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f23e5-117">-이름</span><span class="sxs-lookup"><span data-stu-id="f23e5-117">-Name</span></span>
<span data-ttu-id="f23e5-118">디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f23e5-118">Specifies the name of the disk.</span></span>

```yaml
Type: String
Parameter Sets: NameParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f23e5-119">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="f23e5-119">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="f23e5-120">VMSS 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f23e5-120">Specify the VMSS object.</span></span>

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

### <span data-ttu-id="f23e5-121">-확인</span><span class="sxs-lookup"><span data-stu-id="f23e5-121">-Confirm</span></span>
<span data-ttu-id="f23e5-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f23e5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f23e5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f23e5-123">-WhatIf</span></span>
<span data-ttu-id="f23e5-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f23e5-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f23e5-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f23e5-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f23e5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f23e5-126">CommonParameters</span></span>
<span data-ttu-id="f23e5-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f23e5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f23e5-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f23e5-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f23e5-129">입력</span><span class="sxs-lookup"><span data-stu-id="f23e5-129">INPUTS</span></span>

### <span data-ttu-id="f23e5-130">VirtualMachineScaleSet를 통해 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="f23e5-130">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="f23e5-131">System.webserver 시스템. Null 허용 ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="f23e5-131">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="f23e5-132">출력</span><span class="sxs-lookup"><span data-stu-id="f23e5-132">OUTPUTS</span></span>

### <span data-ttu-id="f23e5-133">VirtualMachineScaleSet를 통해 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="f23e5-133">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="f23e5-134">상속자</span><span class="sxs-lookup"><span data-stu-id="f23e5-134">NOTES</span></span>

## <span data-ttu-id="f23e5-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f23e5-135">RELATED LINKS</span></span>

