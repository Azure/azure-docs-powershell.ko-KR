---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 9EE192A5-4E3F-41ED-A539-8E0A5D5EA4C9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Update-AzureRmVmss.md
ms.openlocfilehash: 4511aadaad23e47018a12365f6fb8fb346117b0e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525239"
---
# <span data-ttu-id="fe748-101">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fe748-101">Update-AzureRmVmss</span></span>

## <span data-ttu-id="fe748-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe748-102">SYNOPSIS</span></span>
<span data-ttu-id="fe748-103">VMSS의 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe748-103">Updates the state of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe748-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fe748-104">SYNTAX</span></span>

```
Update-AzureRmVmss [-ResourceGroupName] <String> -VMScaleSetName <String>
 [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe748-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fe748-105">DESCRIPTION</span></span>
<span data-ttu-id="fe748-106">**AzureRmVmss** CMDLET은 Vmss (가상 컴퓨터 크기 집합)의 상태를 로컬 vmss 개체의 상태로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe748-106">The **Update-AzureRmVmss** cmdlet updates the state of a Virtual Machine Scale Set (VMSS) to the state of a local VMSS object.</span></span>

## <span data-ttu-id="fe748-107">예제의</span><span class="sxs-lookup"><span data-stu-id="fe748-107">EXAMPLES</span></span>

### <span data-ttu-id="fe748-108">예제 1: VMSS의 상태를 로컬 VMSS 개체의 상태로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe748-108">Example 1: Update the state of a VMSS to the state of a local VMSS object.</span></span>
```
PS C:\> Update-AzureRmVmss -ResourceGroupName "Group001" -Name "VMSS001" -VirtualMachineScaleSet "LocalVMSS"
```

<span data-ttu-id="fe748-109">이 명령은 Group001 이라는 리소스 그룹에 속한 VMSS001 라는 VMSS의 상태를 LocalVMSS 라는 로컬 VMSS 개체의 상태로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe748-109">This command updates the state of the VMSS named VMSS001 that belongs to the resource group named Group001 to the state of a local VMSS object named LocalVMSS.</span></span>

## <span data-ttu-id="fe748-110">변수</span><span class="sxs-lookup"><span data-stu-id="fe748-110">PARAMETERS</span></span>

### <span data-ttu-id="fe748-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe748-111">-ResourceGroupName</span></span>
<span data-ttu-id="fe748-112">VMSS가 속한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe748-112">Specifies the name of the resource group the VMSS belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe748-113">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="fe748-113">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="fe748-114">로컬 VMSS 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe748-114">Specifies a local VMSS object.</span></span>
<span data-ttu-id="fe748-115">VMSS 개체를 가져오려면 Get-AzureRmVmss cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe748-115">To obtain a VMSS object, use the Get-AzureRmVmss cmdlet.</span></span>
<span data-ttu-id="fe748-116">이 가상 컴퓨터 개체에는 VMSS의 업데이트 상태가 포함 되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fe748-116">This virtual machine object contains the updated state for the VMSS.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fe748-117">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="fe748-117">-VMScaleSetName</span></span>
<span data-ttu-id="fe748-118">이 cmdlet이 만드는 VMSS의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe748-118">Specifies the name of the VMSS that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe748-119">-확인</span><span class="sxs-lookup"><span data-stu-id="fe748-119">-Confirm</span></span>
<span data-ttu-id="fe748-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe748-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe748-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe748-121">-WhatIf</span></span>
<span data-ttu-id="fe748-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fe748-122">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="fe748-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fe748-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe748-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe748-124">CommonParameters</span></span>
<span data-ttu-id="fe748-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe748-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe748-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe748-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe748-127">입력</span><span class="sxs-lookup"><span data-stu-id="fe748-127">INPUTS</span></span>

### <span data-ttu-id="fe748-128">않아야</span><span class="sxs-lookup"><span data-stu-id="fe748-128">None</span></span>
<span data-ttu-id="fe748-129">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fe748-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fe748-130">출력</span><span class="sxs-lookup"><span data-stu-id="fe748-130">OUTPUTS</span></span>

## <span data-ttu-id="fe748-131">상속자</span><span class="sxs-lookup"><span data-stu-id="fe748-131">NOTES</span></span>

## <span data-ttu-id="fe748-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fe748-132">RELATED LINKS</span></span>

[<span data-ttu-id="fe748-133">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fe748-133">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="fe748-134">새로운 AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fe748-134">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="fe748-135">제거-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fe748-135">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="fe748-136">다시 시작-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fe748-136">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="fe748-137">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fe748-137">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="fe748-138">시작-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fe748-138">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="fe748-139">중지-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="fe748-139">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)


