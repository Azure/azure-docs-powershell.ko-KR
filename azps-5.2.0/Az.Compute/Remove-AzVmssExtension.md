---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssExtension.md
ms.openlocfilehash: ceca2477d66cb6ce19564899e67a3b66d6917cfe
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355341"
---
# <span data-ttu-id="19b6c-101">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="19b6c-101">Remove-AzVmssExtension</span></span>

## <span data-ttu-id="19b6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19b6c-102">SYNOPSIS</span></span>
<span data-ttu-id="19b6c-103">VMSS에서 확장을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="19b6c-103">Removes an extension from the VMSS.</span></span>

## <span data-ttu-id="19b6c-104">구문</span><span class="sxs-lookup"><span data-stu-id="19b6c-104">SYNTAX</span></span>

### <span data-ttu-id="19b6c-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="19b6c-105">NameParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19b6c-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="19b6c-106">IdParameterSet</span></span>
```
Remove-AzVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19b6c-107">설명</span><span class="sxs-lookup"><span data-stu-id="19b6c-107">DESCRIPTION</span></span>
<span data-ttu-id="19b6c-108">**Remove-AzVmssExtension** cmdlet은 VMSS(Virtual Machine Scale Set)에서 확장을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="19b6c-108">The **Remove-AzVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="19b6c-109">예제</span><span class="sxs-lookup"><span data-stu-id="19b6c-109">EXAMPLES</span></span>

### <span data-ttu-id="19b6c-110">예제 1: VMSS 확장 제거</span><span class="sxs-lookup"><span data-stu-id="19b6c-110">Example 1: Remove a VMSS extension</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $RGName -VMScaleSetName $vmssName 
PS C:\> Remove-AzVmssExtension -VirtualMachineScaleSet $vmss -Name $vmssExtensionName
PS C:\> Update-AzVmss -ResourceGroupName $RGName -Name $vmssName -VirtualMachineScaleSet $vmss
```

<span data-ttu-id="19b6c-111">이 명령은 VMSS의 확장을 제거하고 수정 후 VMSS를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="19b6c-111">This command removes the extension of a VMSS and update the VMSS after the modification.</span></span>

### <span data-ttu-id="19b6c-112">예제 2: VMSS 내에서 인스턴스 제거</span><span class="sxs-lookup"><span data-stu-id="19b6c-112">Example 2: Remove an instance from within a VMSS</span></span>
```
PS C:\> $vmss = Get-AzVmss -ResourceGroupName $RGName -VMScaleSetName $vmssName 
PS C:\> Remove-AzVmssExtension -ResourceGroupName "Group002" -VirtualMachineScaleSet $vmss -Id $extensionId
```

<span data-ttu-id="19b6c-113">이 명령은 Group002라는 리소스 그룹에 속한 VMSS에서 확장 ID 지정을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="19b6c-113">This command removes specify extension id from the VMSS that belongs to the resource group named Group002.</span></span>

## <span data-ttu-id="19b6c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19b6c-114">PARAMETERS</span></span>

### <span data-ttu-id="19b6c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19b6c-115">-DefaultProfile</span></span>
<span data-ttu-id="19b6c-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="19b6c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19b6c-117">-Id</span><span class="sxs-lookup"><span data-stu-id="19b6c-117">-Id</span></span>
<span data-ttu-id="19b6c-118">이 cmdlet이 VMSS에서 제거하는 확장의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="19b6c-118">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19b6c-119">-Name</span><span class="sxs-lookup"><span data-stu-id="19b6c-119">-Name</span></span>
<span data-ttu-id="19b6c-120">이 cmdlet이 VMSS에서 제거하는 확장의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="19b6c-120">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="19b6c-121">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="19b6c-121">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="19b6c-122">확장을 제거할 VMSS를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="19b6c-122">Specifies the VMSS from which to remove the extension from.</span></span>

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

### <span data-ttu-id="19b6c-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="19b6c-123">-Confirm</span></span>
<span data-ttu-id="19b6c-124">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="19b6c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19b6c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19b6c-125">-WhatIf</span></span>
<span data-ttu-id="19b6c-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="19b6c-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="19b6c-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="19b6c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19b6c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19b6c-128">CommonParameters</span></span>
<span data-ttu-id="19b6c-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="19b6c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19b6c-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="19b6c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19b6c-131">입력</span><span class="sxs-lookup"><span data-stu-id="19b6c-131">INPUTS</span></span>

### <span data-ttu-id="19b6c-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="19b6c-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="19b6c-133">System.String</span><span class="sxs-lookup"><span data-stu-id="19b6c-133">System.String</span></span>

## <span data-ttu-id="19b6c-134">출력</span><span class="sxs-lookup"><span data-stu-id="19b6c-134">OUTPUTS</span></span>

### <span data-ttu-id="19b6c-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="19b6c-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="19b6c-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="19b6c-136">NOTES</span></span>

## <span data-ttu-id="19b6c-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="19b6c-137">RELATED LINKS</span></span>

[<span data-ttu-id="19b6c-138">Add-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="19b6c-138">Add-AzVmssExtension</span></span>](./Add-AzVmssExtension.md)
