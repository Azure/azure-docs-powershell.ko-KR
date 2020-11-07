---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmssdatadisk
schema: 2.0.0
ms.openlocfilehash: 411e822153c0b95bbf30829f8da915039d01ea32
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880562"
---
# <span data-ttu-id="78181-101">Remove-AzureRmVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="78181-101">Remove-AzureRmVmssDataDisk</span></span>

## <span data-ttu-id="78181-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78181-102">SYNOPSIS</span></span>
<span data-ttu-id="78181-103">VMSS에서 데이터 디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="78181-103">Removes a data disk from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78181-104">구문과</span><span class="sxs-lookup"><span data-stu-id="78181-104">SYNTAX</span></span>

### <span data-ttu-id="78181-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="78181-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78181-106">LunParameterSet</span><span class="sxs-lookup"><span data-stu-id="78181-106">LunParameterSet</span></span>
```
Remove-AzureRmVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78181-107">설명은</span><span class="sxs-lookup"><span data-stu-id="78181-107">DESCRIPTION</span></span>
<span data-ttu-id="78181-108">**AzureRmVmssDataDisk** CMDLET은 Vmss (가상 컴퓨터 배율 집합) 인스턴스에서 데이터 디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="78181-108">The **Remove-AzureRmVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="78181-109">예제의</span><span class="sxs-lookup"><span data-stu-id="78181-109">EXAMPLES</span></span>

### <span data-ttu-id="78181-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="78181-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="78181-111">이 명령은 VMSS 개체에서 이름이 ' DataDisk1 ' 인 데이터 디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="78181-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="78181-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="78181-112">Example 2</span></span>
```
PS C:\> Remove-AzureRmVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="78181-113">이 명령은 VMSS 개체에서 LUN 0의 데이터 디스크를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="78181-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="78181-114">변수</span><span class="sxs-lookup"><span data-stu-id="78181-114">PARAMETERS</span></span>

### <span data-ttu-id="78181-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78181-115">-DefaultProfile</span></span>
<span data-ttu-id="78181-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="78181-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78181-117">-Lun</span><span class="sxs-lookup"><span data-stu-id="78181-117">-Lun</span></span>
<span data-ttu-id="78181-118">디스크의 논리 단위 번호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78181-118">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="78181-119">-이름</span><span class="sxs-lookup"><span data-stu-id="78181-119">-Name</span></span>
<span data-ttu-id="78181-120">디스크의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78181-120">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="78181-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="78181-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="78181-122">VMSS 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78181-122">Specify the VMSS object.</span></span>

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

### <span data-ttu-id="78181-123">-확인</span><span class="sxs-lookup"><span data-stu-id="78181-123">-Confirm</span></span>
<span data-ttu-id="78181-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="78181-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78181-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78181-125">-WhatIf</span></span>
<span data-ttu-id="78181-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="78181-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78181-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78181-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78181-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78181-128">CommonParameters</span></span>
<span data-ttu-id="78181-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="78181-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78181-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78181-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78181-131">입력</span><span class="sxs-lookup"><span data-stu-id="78181-131">INPUTS</span></span>

### <span data-ttu-id="78181-132">VirtualMachineScaleSet를 통해 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="78181-132">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>
<span data-ttu-id="78181-133">System.webserver 시스템. Null 허용 ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="78181-133">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="78181-134">출력</span><span class="sxs-lookup"><span data-stu-id="78181-134">OUTPUTS</span></span>

### <span data-ttu-id="78181-135">VirtualMachineScaleSet를 통해 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="78181-135">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSet</span></span>

## <span data-ttu-id="78181-136">상속자</span><span class="sxs-lookup"><span data-stu-id="78181-136">NOTES</span></span>

## <span data-ttu-id="78181-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="78181-137">RELATED LINKS</span></span>

