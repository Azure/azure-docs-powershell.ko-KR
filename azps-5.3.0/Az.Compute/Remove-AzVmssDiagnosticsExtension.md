---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5F135E64-9432-4D08-961F-4604410378A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDiagnosticsExtension.md
ms.openlocfilehash: 0bf685f9efbe47271fddcc842c1237dd86e8a298
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495962"
---
# <span data-ttu-id="354e0-101">Remove-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="354e0-101">Remove-AzVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="354e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="354e0-102">SYNOPSIS</span></span>
<span data-ttu-id="354e0-103">VMSS에서 진단 확장을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="354e0-103">Removes a diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="354e0-104">구문</span><span class="sxs-lookup"><span data-stu-id="354e0-104">SYNTAX</span></span>

```
Remove-AzVmssDiagnosticsExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="354e0-105">설명</span><span class="sxs-lookup"><span data-stu-id="354e0-105">DESCRIPTION</span></span>
<span data-ttu-id="354e0-106">**Remove-AzVmssDiagnosticsExtension** cmdlet은 VMSS(Virtual Machine Scale Set)에서 진단 확장을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="354e0-106">The **Remove-AzVmssDiagnosticsExtension** cmdlet removes a diagnostics extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="354e0-107">예제</span><span class="sxs-lookup"><span data-stu-id="354e0-107">EXAMPLES</span></span>

### <span data-ttu-id="354e0-108">예제 1: VMSS에서 진단 확장 제거</span><span class="sxs-lookup"><span data-stu-id="354e0-108">Example 1: Remove a diagnostics extension from the VMSS</span></span>
```
PS C:\> Remove-AzVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -Name $extName
```

<span data-ttu-id="354e0-109">이 명령은 VMSS에서 진단 확장을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="354e0-109">This command removes diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="354e0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="354e0-110">PARAMETERS</span></span>

### <span data-ttu-id="354e0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="354e0-111">-DefaultProfile</span></span>
<span data-ttu-id="354e0-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="354e0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="354e0-113">-Name</span><span class="sxs-lookup"><span data-stu-id="354e0-113">-Name</span></span>
<span data-ttu-id="354e0-114">이 cmdlet이 VMSS에서 제거하는 확장의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="354e0-114">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="354e0-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="354e0-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="354e0-116">확장을 제거할 VMSS를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="354e0-116">Specifies the VMSS from which to remove the extension.</span></span>

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

### <span data-ttu-id="354e0-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="354e0-117">-Confirm</span></span>
<span data-ttu-id="354e0-118">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="354e0-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="354e0-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="354e0-119">-WhatIf</span></span>
<span data-ttu-id="354e0-120">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="354e0-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="354e0-121">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="354e0-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="354e0-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="354e0-122">CommonParameters</span></span>
<span data-ttu-id="354e0-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="354e0-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="354e0-124">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="354e0-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="354e0-125">입력</span><span class="sxs-lookup"><span data-stu-id="354e0-125">INPUTS</span></span>

### <span data-ttu-id="354e0-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="354e0-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="354e0-127">System.String</span><span class="sxs-lookup"><span data-stu-id="354e0-127">System.String</span></span>

## <span data-ttu-id="354e0-128">출력</span><span class="sxs-lookup"><span data-stu-id="354e0-128">OUTPUTS</span></span>

### <span data-ttu-id="354e0-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="354e0-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="354e0-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="354e0-130">NOTES</span></span>

## <span data-ttu-id="354e0-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="354e0-131">RELATED LINKS</span></span>

[<span data-ttu-id="354e0-132">Add-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="354e0-132">Add-AzVmssDiagnosticsExtension</span></span>](./Add-AzVmssDiagnosticsExtension.md)

[<span data-ttu-id="354e0-133">Remove-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="354e0-133">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="354e0-134">Remove-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="354e0-134">Remove-AzVmssExtension</span></span>](./Remove-AzVmssExtension.md)


