---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssExtension.md
ms.openlocfilehash: 09b90d5ef1f3852f7da39efac9167a8329fba85f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529887"
---
# <span data-ttu-id="95d1d-101">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="95d1d-101">Remove-AzureRmVmssExtension</span></span>

## <span data-ttu-id="95d1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95d1d-102">SYNOPSIS</span></span>
<span data-ttu-id="95d1d-103">VMSS에서 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="95d1d-103">Removes an extension from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95d1d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="95d1d-104">SYNTAX</span></span>

### <span data-ttu-id="95d1d-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="95d1d-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-Name] <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="95d1d-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="95d1d-106">IdParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-Id] <String> [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="95d1d-107">설명은</span><span class="sxs-lookup"><span data-stu-id="95d1d-107">DESCRIPTION</span></span>
<span data-ttu-id="95d1d-108">**AzureRmVmssExtension** CMDLET은 Vmss (가상 컴퓨터 크기 조정 집합)에서 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="95d1d-108">The **Remove-AzureRmVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="95d1d-109">예제의</span><span class="sxs-lookup"><span data-stu-id="95d1d-109">EXAMPLES</span></span>

## <span data-ttu-id="95d1d-110">변수</span><span class="sxs-lookup"><span data-stu-id="95d1d-110">PARAMETERS</span></span>

### <span data-ttu-id="95d1d-111">-Id</span><span class="sxs-lookup"><span data-stu-id="95d1d-111">-Id</span></span>
<span data-ttu-id="95d1d-112">이 cmdlet이 VMSS에서 제거 하는 확장의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="95d1d-112">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="95d1d-113">-이름</span><span class="sxs-lookup"><span data-stu-id="95d1d-113">-Name</span></span>
<span data-ttu-id="95d1d-114">이 cmdlet이 VMSS에서 제거 하는 확장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="95d1d-114">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="95d1d-115">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="95d1d-115">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="95d1d-116">확장명을 제거할 VMSS를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="95d1d-116">Specifies the VMSS from which to remove the extension from.</span></span>

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

### <span data-ttu-id="95d1d-117">-확인</span><span class="sxs-lookup"><span data-stu-id="95d1d-117">-Confirm</span></span>
<span data-ttu-id="95d1d-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="95d1d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95d1d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95d1d-119">-WhatIf</span></span>
<span data-ttu-id="95d1d-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="95d1d-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="95d1d-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="95d1d-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95d1d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95d1d-122">CommonParameters</span></span>
<span data-ttu-id="95d1d-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="95d1d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95d1d-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95d1d-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95d1d-125">입력</span><span class="sxs-lookup"><span data-stu-id="95d1d-125">INPUTS</span></span>

### <span data-ttu-id="95d1d-126">않아야</span><span class="sxs-lookup"><span data-stu-id="95d1d-126">None</span></span>
<span data-ttu-id="95d1d-127">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="95d1d-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="95d1d-128">출력</span><span class="sxs-lookup"><span data-stu-id="95d1d-128">OUTPUTS</span></span>

### <span data-ttu-id="95d1d-129">이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="95d1d-129">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="95d1d-130">상속자</span><span class="sxs-lookup"><span data-stu-id="95d1d-130">NOTES</span></span>

## <span data-ttu-id="95d1d-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="95d1d-131">RELATED LINKS</span></span>

[<span data-ttu-id="95d1d-132">추가-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="95d1d-132">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)
