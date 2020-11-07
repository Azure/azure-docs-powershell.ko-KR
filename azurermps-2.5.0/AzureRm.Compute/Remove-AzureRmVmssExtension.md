---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 8C1C12AD-5130-42E7-99BB-B13900D7A712
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmssextension
schema: 2.0.0
ms.openlocfilehash: 224b0302da76fd1c748cd77a183aa9a302dd3c9b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880561"
---
# <span data-ttu-id="3293b-101">Remove-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="3293b-101">Remove-AzureRmVmssExtension</span></span>

## <span data-ttu-id="3293b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3293b-102">SYNOPSIS</span></span>
<span data-ttu-id="3293b-103">VMSS에서 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3293b-103">Removes an extension from the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3293b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3293b-104">SYNTAX</span></span>

### <span data-ttu-id="3293b-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3293b-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3293b-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3293b-106">IdParameterSet</span></span>
```
Remove-AzureRmVmssExtension [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3293b-107">설명은</span><span class="sxs-lookup"><span data-stu-id="3293b-107">DESCRIPTION</span></span>
<span data-ttu-id="3293b-108">**AzureRmVmssExtension** CMDLET은 Vmss (가상 컴퓨터 크기 조정 집합)에서 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="3293b-108">The **Remove-AzureRmVmssExtension** cmdlet removes an extension from the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="3293b-109">예제의</span><span class="sxs-lookup"><span data-stu-id="3293b-109">EXAMPLES</span></span>

## <span data-ttu-id="3293b-110">변수</span><span class="sxs-lookup"><span data-stu-id="3293b-110">PARAMETERS</span></span>

### <span data-ttu-id="3293b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3293b-111">-DefaultProfile</span></span>
<span data-ttu-id="3293b-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3293b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3293b-113">-Id</span><span class="sxs-lookup"><span data-stu-id="3293b-113">-Id</span></span>
<span data-ttu-id="3293b-114">이 cmdlet이 VMSS에서 제거 하는 확장의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3293b-114">Specifies the ID of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="3293b-115">-이름</span><span class="sxs-lookup"><span data-stu-id="3293b-115">-Name</span></span>
<span data-ttu-id="3293b-116">이 cmdlet이 VMSS에서 제거 하는 확장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3293b-116">Specifies the name of the extension that this cmdlet removes from the VMSS.</span></span>

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

### <span data-ttu-id="3293b-117">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="3293b-117">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="3293b-118">확장명을 제거할 VMSS를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3293b-118">Specifies the VMSS from which to remove the extension from.</span></span>

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

### <span data-ttu-id="3293b-119">-확인</span><span class="sxs-lookup"><span data-stu-id="3293b-119">-Confirm</span></span>
<span data-ttu-id="3293b-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3293b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3293b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3293b-121">-WhatIf</span></span>
<span data-ttu-id="3293b-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3293b-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3293b-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3293b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3293b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3293b-124">CommonParameters</span></span>
<span data-ttu-id="3293b-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3293b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3293b-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3293b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3293b-127">입력</span><span class="sxs-lookup"><span data-stu-id="3293b-127">INPUTS</span></span>

### <span data-ttu-id="3293b-128">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="3293b-128">VirtualMachineScaleSet</span></span>
<span data-ttu-id="3293b-129">' VirtualMachineScaleSet ' 매개 변수는 파이프라인에서 ' VirtualMachineScaleSet ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3293b-129">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="3293b-130">출력</span><span class="sxs-lookup"><span data-stu-id="3293b-130">OUTPUTS</span></span>

### <span data-ttu-id="3293b-131">이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3293b-131">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="3293b-132">상속자</span><span class="sxs-lookup"><span data-stu-id="3293b-132">NOTES</span></span>

## <span data-ttu-id="3293b-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3293b-133">RELATED LINKS</span></span>

[<span data-ttu-id="3293b-134">추가-AzureRmVmssExtension</span><span class="sxs-lookup"><span data-stu-id="3293b-134">Add-AzureRmVmssExtension</span></span>](./Add-AzureRmVmssExtension.md)
