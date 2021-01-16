---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmssbootdiagnostic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssBootDiagnostic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVmssBootDiagnostic.md
ms.openlocfilehash: 31da1c621e8f3dc91c303abd6c70476f40602de4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98334197"
---
# <span data-ttu-id="db80e-101">Set-AzVmssBootDiagnostic</span><span class="sxs-lookup"><span data-stu-id="db80e-101">Set-AzVmssBootDiagnostic</span></span>

## <span data-ttu-id="db80e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db80e-102">SYNOPSIS</span></span>
<span data-ttu-id="db80e-103">가상 머신 확장 집합 부팅 진단 프로필을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="db80e-103">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="db80e-104">구문</span><span class="sxs-lookup"><span data-stu-id="db80e-104">SYNTAX</span></span>

```
Set-AzVmssBootDiagnostic [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Enabled] <Boolean>]
 [[-StorageUri] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db80e-105">설명</span><span class="sxs-lookup"><span data-stu-id="db80e-105">DESCRIPTION</span></span>
<span data-ttu-id="db80e-106">가상 머신 확장 집합 부팅 진단 프로필을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="db80e-106">Sets the virtual machine scale set boot diagnostics profile.</span></span>

## <span data-ttu-id="db80e-107">예제</span><span class="sxs-lookup"><span data-stu-id="db80e-107">EXAMPLES</span></span>

### <span data-ttu-id="db80e-108">예제 1: VMSS에 대한 부팅 진단 프로필 속성 설정</span><span class="sxs-lookup"><span data-stu-id="db80e-108">Example 1: Set the boot diagnostics profile property for a VMSS</span></span>
```
PS C:\> $vmss = New-AzVmssConfig -Location $loc -SkuCapacity 2 -SkuName 'Standard_A0'
PS C:\> Set-AzVmssBootDiagnostic -VirtualMachineScaleSet $vmss -Enabled $true -StorageUri $storageUri;
PS C:\> New-AzVmss -ResourceGroupName $rgname -Name "ContosoVMSS" -VirtualMachineScaleSet $vmss;
```

<span data-ttu-id="db80e-109">이 명령은 ContosoVMSS라는 VMSS에 대한 부팅 진단 프로필 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="db80e-109">This command sets boot diagnostics profile property for the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="db80e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="db80e-110">PARAMETERS</span></span>

### <span data-ttu-id="db80e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db80e-111">-DefaultProfile</span></span>
<span data-ttu-id="db80e-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="db80e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db80e-113">-Enabled</span><span class="sxs-lookup"><span data-stu-id="db80e-113">-Enabled</span></span>
<span data-ttu-id="db80e-114">가상 머신 확장 집합에서 부팅 진단을 사용하도록 설정해야 하는지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="db80e-114">Whether boot diagnostics should be enabled on the virtual machine scale set.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db80e-115">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="db80e-115">-StorageUri</span></span>
<span data-ttu-id="db80e-116">콘솔 출력 및 스크린샷을 배치하는 데 사용할 저장소 계정의 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="db80e-116">URI of the storage account to use for placing the console output and screenshot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db80e-117">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="db80e-117">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="db80e-118">VMSS 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="db80e-118">Specifies the VMSS object.</span></span>
<span data-ttu-id="db80e-119">New-AzVmssConfig cmdlet을 사용하여 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="db80e-119">You can use the New-AzVmssConfig cmdlet to create the object.</span></span>

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

### <span data-ttu-id="db80e-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="db80e-120">-Confirm</span></span>
<span data-ttu-id="db80e-121">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="db80e-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db80e-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db80e-122">-WhatIf</span></span>
<span data-ttu-id="db80e-123">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="db80e-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db80e-124">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="db80e-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db80e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db80e-125">CommonParameters</span></span>
<span data-ttu-id="db80e-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="db80e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db80e-127">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="db80e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db80e-128">입력</span><span class="sxs-lookup"><span data-stu-id="db80e-128">INPUTS</span></span>

### <span data-ttu-id="db80e-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="db80e-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="db80e-130">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="db80e-130">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="db80e-131">System.String</span><span class="sxs-lookup"><span data-stu-id="db80e-131">System.String</span></span>

## <span data-ttu-id="db80e-132">출력</span><span class="sxs-lookup"><span data-stu-id="db80e-132">OUTPUTS</span></span>

### <span data-ttu-id="db80e-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="db80e-133">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="db80e-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="db80e-134">NOTES</span></span>

## <span data-ttu-id="db80e-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="db80e-135">RELATED LINKS</span></span>
