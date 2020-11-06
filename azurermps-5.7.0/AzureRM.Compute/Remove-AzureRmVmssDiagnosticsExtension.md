---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 5F135E64-9432-4D08-961F-4604410378A3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDiagnosticsExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssDiagnosticsExtension.md
ms.openlocfilehash: 07f679c714c7c8f6f65f89681e3c8df0fff133df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529935"
---
# <span data-ttu-id="1269d-101">Remove-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="1269d-101">Remove-AzureRmVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="1269d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1269d-102">SYNOPSIS</span></span>
<span data-ttu-id="1269d-103">VMSS에서 진단 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1269d-103">Removes a diagnostics extension from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1269d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1269d-104">SYNTAX</span></span>

```
Remove-AzureRmVmssDiagnosticsExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Name] <String>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1269d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1269d-105">DESCRIPTION</span></span>
<span data-ttu-id="1269d-106">**AzureRmVmssDiagnosticsExtension** CMDLET은 Vmss (가상 컴퓨터 크기 조정 집합)에서 진단 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1269d-106">The **Remove-AzureRmVmssDiagnosticsExtension** cmdlet removes a diagnostics extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="1269d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1269d-107">EXAMPLES</span></span>

### <span data-ttu-id="1269d-108">예제 1: VMSS에서 진단 확장 제거</span><span class="sxs-lookup"><span data-stu-id="1269d-108">Example 1: Remove a diagnostics extension from the VMSS</span></span>
```
PS C:\> Remove-AzureRmVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -Name $extName
```

<span data-ttu-id="1269d-109">이 명령은 VMSS에서 진단 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1269d-109">This command removes diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="1269d-110">변수</span><span class="sxs-lookup"><span data-stu-id="1269d-110">PARAMETERS</span></span>

### <span data-ttu-id="1269d-111">-이름</span><span class="sxs-lookup"><span data-stu-id="1269d-111">-Name</span></span>
<span data-ttu-id="1269d-112">이 cmdlet이 VMSS에서 제거 하는 확장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1269d-112">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1269d-113">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="1269d-113">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="1269d-114">확장을 제거할 VMSS를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1269d-114">Specifies the VMSS from which to remove the extension.</span></span>

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

### <span data-ttu-id="1269d-115">-확인</span><span class="sxs-lookup"><span data-stu-id="1269d-115">-Confirm</span></span>
<span data-ttu-id="1269d-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1269d-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1269d-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1269d-117">-WhatIf</span></span>
<span data-ttu-id="1269d-118">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1269d-118">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="1269d-119">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1269d-119">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1269d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1269d-120">CommonParameters</span></span>
<span data-ttu-id="1269d-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1269d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1269d-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1269d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1269d-123">입력</span><span class="sxs-lookup"><span data-stu-id="1269d-123">INPUTS</span></span>

### <span data-ttu-id="1269d-124">않아야</span><span class="sxs-lookup"><span data-stu-id="1269d-124">None</span></span>
<span data-ttu-id="1269d-125">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1269d-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1269d-126">출력</span><span class="sxs-lookup"><span data-stu-id="1269d-126">OUTPUTS</span></span>

###  
<span data-ttu-id="1269d-127">이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1269d-127">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="1269d-128">상속자</span><span class="sxs-lookup"><span data-stu-id="1269d-128">NOTES</span></span>

## <span data-ttu-id="1269d-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1269d-129">RELATED LINKS</span></span>

[<span data-ttu-id="1269d-130">추가-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="1269d-130">Add-AzureRmVmssDiagnosticsExtension</span></span>](./Add-AzureRmVmssDiagnosticsExtension.md)

[<span data-ttu-id="1269d-131">제거-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="1269d-131">Remove-AzureRmVMDiagnosticsExtension</span></span>](./Remove-AzureRmVMDiagnosticsExtension.md)

[<span data-ttu-id="1269d-132">제거-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="1269d-132">Remove-AzureRmVmssExtension</span></span>](./Remove-AzureRmVmssExtension.md)


