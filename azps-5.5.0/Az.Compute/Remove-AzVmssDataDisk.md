---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
ms.openlocfilehash: 908405de847526682d8526ef2e576e6a07893c3a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181553"
---
# <span data-ttu-id="6467f-101">Remove-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="6467f-101">Remove-AzVmssDataDisk</span></span>

## <span data-ttu-id="6467f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6467f-102">SYNOPSIS</span></span>
<span data-ttu-id="6467f-103">VMSS에서 데이터 디스크를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6467f-103">Removes a data disk from the VMSS.</span></span>

## <span data-ttu-id="6467f-104">구문</span><span class="sxs-lookup"><span data-stu-id="6467f-104">SYNTAX</span></span>

### <span data-ttu-id="6467f-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6467f-105">NameParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6467f-106">LunParameterSet</span><span class="sxs-lookup"><span data-stu-id="6467f-106">LunParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6467f-107">설명</span><span class="sxs-lookup"><span data-stu-id="6467f-107">DESCRIPTION</span></span>
<span data-ttu-id="6467f-108">**Remove-AzVmssDataDisk** cmdlet은 VMSS(Virtual Machine Scale Set) 인스턴스에서 데이터 디스크를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6467f-108">The **Remove-AzVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="6467f-109">예제</span><span class="sxs-lookup"><span data-stu-id="6467f-109">EXAMPLES</span></span>

### <span data-ttu-id="6467f-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="6467f-110">Example 1</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="6467f-111">이 명령은 VMSS 개체에서 'DataDisk1'이라는 데이터 디스크를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6467f-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="6467f-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="6467f-112">Example 2</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="6467f-113">이 명령은 VMSS 개체에서 LUN 0의 데이터 디스크를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6467f-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="6467f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6467f-114">PARAMETERS</span></span>

### <span data-ttu-id="6467f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6467f-115">-DefaultProfile</span></span>
<span data-ttu-id="6467f-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6467f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6467f-117">-Lun</span><span class="sxs-lookup"><span data-stu-id="6467f-117">-Lun</span></span>
<span data-ttu-id="6467f-118">디스크의 논리 단위 번호를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6467f-118">Specifies the logical unit number of the disk.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: LunParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6467f-119">-Name</span><span class="sxs-lookup"><span data-stu-id="6467f-119">-Name</span></span>
<span data-ttu-id="6467f-120">디스크의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6467f-120">Specifies the name of the disk.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6467f-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6467f-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="6467f-122">VMSS 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6467f-122">Specify the VMSS object.</span></span>

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

### <span data-ttu-id="6467f-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6467f-123">-Confirm</span></span>
<span data-ttu-id="6467f-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6467f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6467f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6467f-125">-WhatIf</span></span>
<span data-ttu-id="6467f-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="6467f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6467f-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6467f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6467f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6467f-128">CommonParameters</span></span>
<span data-ttu-id="6467f-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6467f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6467f-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6467f-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6467f-131">입력</span><span class="sxs-lookup"><span data-stu-id="6467f-131">INPUTS</span></span>

### <span data-ttu-id="6467f-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6467f-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="6467f-133">System.String</span><span class="sxs-lookup"><span data-stu-id="6467f-133">System.String</span></span>

### <span data-ttu-id="6467f-134">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6467f-134">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="6467f-135">출력</span><span class="sxs-lookup"><span data-stu-id="6467f-135">OUTPUTS</span></span>

### <span data-ttu-id="6467f-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6467f-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="6467f-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6467f-137">NOTES</span></span>

## <span data-ttu-id="6467f-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6467f-138">RELATED LINKS</span></span>
