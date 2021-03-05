---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmssdatadisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDataDisk.md
ms.openlocfilehash: abdef821862976a3bffb0b39bc48a3619e17d64f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998872"
---
# <span data-ttu-id="6b914-101">Remove-AzVmssDataDisk</span><span class="sxs-lookup"><span data-stu-id="6b914-101">Remove-AzVmssDataDisk</span></span>

## <span data-ttu-id="6b914-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b914-102">SYNOPSIS</span></span>
<span data-ttu-id="6b914-103">VMSS에서 데이터 디스크를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6b914-103">Removes a data disk from the VMSS.</span></span>

## <span data-ttu-id="6b914-104">구문</span><span class="sxs-lookup"><span data-stu-id="6b914-104">SYNTAX</span></span>

### <span data-ttu-id="6b914-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b914-105">NameParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b914-106">LunParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b914-106">LunParameterSet</span></span>
```
Remove-AzVmssDataDisk [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Lun] <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b914-107">설명</span><span class="sxs-lookup"><span data-stu-id="6b914-107">DESCRIPTION</span></span>
<span data-ttu-id="6b914-108">**Remove-AzVmssDataDisk** cmdlet은 VMSS(Virtual Machine Scale Set) 인스턴스에서 데이터 디스크를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6b914-108">The **Remove-AzVmssDataDisk** cmdlet removes a data disk from the Virtual Machine Scale Set (VMSS) instance.</span></span>

## <span data-ttu-id="6b914-109">예제</span><span class="sxs-lookup"><span data-stu-id="6b914-109">EXAMPLES</span></span>

### <span data-ttu-id="6b914-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="6b914-110">Example 1</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Name 'DataDisk1'
```

<span data-ttu-id="6b914-111">이 명령은 VMSS 개체에서 'DataDisk1'이라는 데이터 디스크를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6b914-111">This command removes the data disk named 'DataDisk1' from the VMSS object.</span></span>

### <span data-ttu-id="6b914-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="6b914-112">Example 2</span></span>
```
PS C:\> Remove-AzVmssDataDisk -VirtualMachineScaleSet $vmss -Lun 0
```

<span data-ttu-id="6b914-113">이 명령은 VMSS 개체에서 LUN 0의 데이터 디스크를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6b914-113">This command removes the data disk of LUN 0 from the VMSS object.</span></span>

## <span data-ttu-id="6b914-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6b914-114">PARAMETERS</span></span>

### <span data-ttu-id="6b914-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b914-115">-DefaultProfile</span></span>
<span data-ttu-id="6b914-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6b914-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b914-117">-Lun</span><span class="sxs-lookup"><span data-stu-id="6b914-117">-Lun</span></span>
<span data-ttu-id="6b914-118">디스크의 논리 단위 번호를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6b914-118">Specifies the logical unit number of the disk.</span></span>

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

### <span data-ttu-id="6b914-119">-Name</span><span class="sxs-lookup"><span data-stu-id="6b914-119">-Name</span></span>
<span data-ttu-id="6b914-120">디스크의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6b914-120">Specifies the name of the disk.</span></span>

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

### <span data-ttu-id="6b914-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6b914-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="6b914-122">VMSS 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6b914-122">Specify the VMSS object.</span></span>

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

### <span data-ttu-id="6b914-123">-확인</span><span class="sxs-lookup"><span data-stu-id="6b914-123">-Confirm</span></span>
<span data-ttu-id="6b914-124">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6b914-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b914-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b914-125">-WhatIf</span></span>
<span data-ttu-id="6b914-126">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="6b914-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b914-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6b914-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b914-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b914-128">CommonParameters</span></span>
<span data-ttu-id="6b914-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6b914-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b914-130">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6b914-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b914-131">입력</span><span class="sxs-lookup"><span data-stu-id="6b914-131">INPUTS</span></span>

### <span data-ttu-id="6b914-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6b914-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="6b914-133">System.String</span><span class="sxs-lookup"><span data-stu-id="6b914-133">System.String</span></span>

### <span data-ttu-id="6b914-134">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6b914-134">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="6b914-135">출력</span><span class="sxs-lookup"><span data-stu-id="6b914-135">OUTPUTS</span></span>

### <span data-ttu-id="6b914-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="6b914-136">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="6b914-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6b914-137">NOTES</span></span>

## <span data-ttu-id="6b914-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6b914-138">RELATED LINKS</span></span>
