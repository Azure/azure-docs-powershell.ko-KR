---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 5F135E64-9432-4D08-961F-4604410378A3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmssdiagnosticsextension
schema: 2.0.0
ms.openlocfilehash: 74bb0bee84615618f464cfbfd86dcb2b7dde387b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882281"
---
# <span data-ttu-id="725f7-101">Remove-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="725f7-101">Remove-AzureRmVmssDiagnosticsExtension</span></span>

## <span data-ttu-id="725f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="725f7-102">SYNOPSIS</span></span>
<span data-ttu-id="725f7-103">VMSS에서 진단 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="725f7-103">Removes a diagnostics extension from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="725f7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="725f7-104">SYNTAX</span></span>

```
Remove-AzureRmVmssDiagnosticsExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="725f7-105">설명은</span><span class="sxs-lookup"><span data-stu-id="725f7-105">DESCRIPTION</span></span>
<span data-ttu-id="725f7-106">**AzureRmVmssDiagnosticsExtension** CMDLET은 Vmss (가상 컴퓨터 크기 조정 집합)에서 진단 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="725f7-106">The **Remove-AzureRmVmssDiagnosticsExtension** cmdlet removes a diagnostics extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="725f7-107">예제의</span><span class="sxs-lookup"><span data-stu-id="725f7-107">EXAMPLES</span></span>

### <span data-ttu-id="725f7-108">예제 1: VMSS에서 진단 확장 제거</span><span class="sxs-lookup"><span data-stu-id="725f7-108">Example 1: Remove a diagnostics extension from the VMSS</span></span>
```
PS C:\> Remove-AzureRmVmssDiagnosticsExtension -VirtualMachineScaleSet $VMSS -Name $extName
```

<span data-ttu-id="725f7-109">이 명령은 VMSS에서 진단 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="725f7-109">This command removes diagnostics extension from the VMSS.</span></span>

## <span data-ttu-id="725f7-110">변수</span><span class="sxs-lookup"><span data-stu-id="725f7-110">PARAMETERS</span></span>

### <span data-ttu-id="725f7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="725f7-111">-DefaultProfile</span></span>
<span data-ttu-id="725f7-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="725f7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="725f7-113">-이름</span><span class="sxs-lookup"><span data-stu-id="725f7-113">-Name</span></span>
<span data-ttu-id="725f7-114">이 cmdlet이 VMSS에서 제거 하는 확장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="725f7-114">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="725f7-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="725f7-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="725f7-116">확장을 제거할 VMSS를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="725f7-116">Specifies the VMSS from which to remove the extension.</span></span>

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

### <span data-ttu-id="725f7-117">-확인</span><span class="sxs-lookup"><span data-stu-id="725f7-117">-Confirm</span></span>
<span data-ttu-id="725f7-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="725f7-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="725f7-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="725f7-119">-WhatIf</span></span>
<span data-ttu-id="725f7-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="725f7-120">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="725f7-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="725f7-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="725f7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="725f7-122">CommonParameters</span></span>
<span data-ttu-id="725f7-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="725f7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="725f7-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="725f7-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="725f7-125">입력</span><span class="sxs-lookup"><span data-stu-id="725f7-125">INPUTS</span></span>

### <span data-ttu-id="725f7-126">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="725f7-126">VirtualMachineScaleSet</span></span>
<span data-ttu-id="725f7-127">' VirtualMachineScaleSet ' 매개 변수는 파이프라인에서 ' VirtualMachineScaleSet ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="725f7-127">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="725f7-128">출력</span><span class="sxs-lookup"><span data-stu-id="725f7-128">OUTPUTS</span></span>

###  
<span data-ttu-id="725f7-129">이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="725f7-129">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="725f7-130">상속자</span><span class="sxs-lookup"><span data-stu-id="725f7-130">NOTES</span></span>

## <span data-ttu-id="725f7-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="725f7-131">RELATED LINKS</span></span>

[<span data-ttu-id="725f7-132">추가-AzureRmVmssDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="725f7-132">Add-AzureRmVmssDiagnosticsExtension</span></span>](./Add-AzureRmVmssDiagnosticsExtension.md)

[<span data-ttu-id="725f7-133">제거-AzureRmVMDiagnosticsExtension</span><span class="sxs-lookup"><span data-stu-id="725f7-133">Remove-AzureRmVMDiagnosticsExtension</span></span>](./Remove-AzureRmVMDiagnosticsExtension.md)

[<span data-ttu-id="725f7-134">제거-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="725f7-134">Remove-AzureRmVmssExtension</span></span>](./Remove-AzureRmVmssExtension.md)


