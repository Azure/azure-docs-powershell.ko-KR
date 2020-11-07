---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5F135E64-9432-4D08-961F-4604410378A3
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssdiagnosticsextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssDiagnosticsExtension.md
ms.openlocfilehash: 724135c1f9ed920414cdeb3c2e53724bd2e512ec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868937"
---
# <span data-ttu-id="804fc-101">Remove-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="804fc-101">Remove-AzVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="804fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="804fc-102">SYNOPSIS</span></span>
<span data-ttu-id="804fc-103">VMSS에서 진단 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="804fc-103">Removes a diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="804fc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="804fc-104">SYNTAX</span></span>

```
Remove-AzVmssDiagnosticsExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="804fc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="804fc-105">DESCRIPTION</span></span>
<span data-ttu-id="804fc-106">**AzVmssDiagnosticsExtension** CMDLET은 Vmss (가상 컴퓨터 크기 조정 집합)에서 진단 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="804fc-106">The **Remove-AzVmssDiagnosticsExtension** cmdlet removes a diagnostics extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="804fc-107">예제의</span><span class="sxs-lookup"><span data-stu-id="804fc-107">EXAMPLES</span></span>

### <span data-ttu-id="804fc-108">예제 1: VMSS에서 진단 확장 제거</span><span class="sxs-lookup"><span data-stu-id="804fc-108">Example 1: Remove a diagnostics extension from the VMSS</span></span>
```
PS C:\> Remove-AzVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -Name $extName
```

<span data-ttu-id="804fc-109">이 명령은 VMSS에서 진단 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="804fc-109">This command removes diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="804fc-110">변수</span><span class="sxs-lookup"><span data-stu-id="804fc-110">PARAMETERS</span></span>

### <span data-ttu-id="804fc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="804fc-111">-DefaultProfile</span></span>
<span data-ttu-id="804fc-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="804fc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="804fc-113">-이름</span><span class="sxs-lookup"><span data-stu-id="804fc-113">-Name</span></span>
<span data-ttu-id="804fc-114">이 cmdlet이 VMSS에서 제거 하는 확장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="804fc-114">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="804fc-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="804fc-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="804fc-116">확장을 제거할 VMSS를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="804fc-116">Specifies the VMSS from which to remove the extension.</span></span>

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

### <span data-ttu-id="804fc-117">-확인</span><span class="sxs-lookup"><span data-stu-id="804fc-117">-Confirm</span></span>
<span data-ttu-id="804fc-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="804fc-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="804fc-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="804fc-119">-WhatIf</span></span>
<span data-ttu-id="804fc-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="804fc-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="804fc-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="804fc-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="804fc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="804fc-122">CommonParameters</span></span>
<span data-ttu-id="804fc-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="804fc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="804fc-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="804fc-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="804fc-125">입력</span><span class="sxs-lookup"><span data-stu-id="804fc-125">INPUTS</span></span>

### <span data-ttu-id="804fc-126">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="804fc-126">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="804fc-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="804fc-127">System.String</span></span>

## <span data-ttu-id="804fc-128">출력</span><span class="sxs-lookup"><span data-stu-id="804fc-128">OUTPUTS</span></span>

### <span data-ttu-id="804fc-129">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="804fc-129">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="804fc-130">상속자</span><span class="sxs-lookup"><span data-stu-id="804fc-130">NOTES</span></span>

## <span data-ttu-id="804fc-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="804fc-131">RELATED LINKS</span></span>

[<span data-ttu-id="804fc-132">추가-AzVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="804fc-132">Add-AzVmssDiagnosticsExtension</span></span>](./Add-AzVmssDiagnosticsExtension.md)

[<span data-ttu-id="804fc-133">제거-AzVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="804fc-133">Remove-AzVMDiagnosticsExtension</span></span>](./Remove-AzVMDiagnosticsExtension.md)

[<span data-ttu-id="804fc-134">제거-AzVmssExtension</span><span class="sxs-lookup"><span data-stu-id="804fc-134">Remove-AzVmssExtension</span></span>](./Remove-AzVmssExtension.md)


