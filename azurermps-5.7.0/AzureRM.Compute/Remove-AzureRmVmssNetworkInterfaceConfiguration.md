---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: EC4E8CC1-C21F-4D41-818F-D0BC15AEEE1D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 8f2d061fa67ed8e588ae162fbf7bd0a094ae6b1c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529886"
---
# <span data-ttu-id="5e6c7-101">Remove-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="5e6c7-101">Remove-AzureRmVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="5e6c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e6c7-102">SYNOPSIS</span></span>
<span data-ttu-id="5e6c7-103">VMSS에서 네트워크 인터페이스 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6c7-103">Removes a network interface configuration from a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e6c7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5e6c7-104">SYNTAX</span></span>

### <span data-ttu-id="5e6c7-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e6c7-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [-Name] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e6c7-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5e6c7-106">IdParameterSet</span></span>
```
Remove-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [-Id] <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e6c7-107">설명은</span><span class="sxs-lookup"><span data-stu-id="5e6c7-107">DESCRIPTION</span></span>
<span data-ttu-id="5e6c7-108">**AzureRmVmssNetworkInterfaceConfiguration** CMDLET은 Vmss (가상 컴퓨터 크기 조정 집합)에서 네트워크 인터페이스 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6c7-108">The **Remove-AzureRmVmssNetworkInterfaceConfiguration** cmdlet removes a network interface configuration from a Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="5e6c7-109">예제의</span><span class="sxs-lookup"><span data-stu-id="5e6c7-109">EXAMPLES</span></span>

### <span data-ttu-id="5e6c7-110">예제 1: 인터페이스 구성 제거</span><span class="sxs-lookup"><span data-stu-id="5e6c7-110">Example 1: Remove an interface configuration</span></span>
```
PS C:\> $VMSS = Get-AzureRmVmss -ResourceGroupName "ResourceGroup11" -VMScaleSetName "ContosoVMSS14"
PS C:\> Remove-AzureRmVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "ContosoVmssInterface02"
```

<span data-ttu-id="5e6c7-111">첫 번째 명령은 Get-AzureRmVmss cmdlet을 사용 하 여 VMSS를 가져온 다음 $VMSS 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6c7-111">The first command gets a VMSS by using the Get-AzureRmVmss cmdlet, and then stores it in the $VMSS variable.</span></span>

<span data-ttu-id="5e6c7-112">두 번째 명령은 $VMSS에서 설정 된 ContosoVmssInterface02 라는 네트워크 인터페이스 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6c7-112">The second command removes the network interface configuration named ContosoVmssInterface02 from the set in $VMSS.</span></span>

## <span data-ttu-id="5e6c7-113">변수</span><span class="sxs-lookup"><span data-stu-id="5e6c7-113">PARAMETERS</span></span>

### <span data-ttu-id="5e6c7-114">-Id</span><span class="sxs-lookup"><span data-stu-id="5e6c7-114">-Id</span></span>
<span data-ttu-id="5e6c7-115">이 cmdlet이 제거 하는 네트워크 인터페이스 구성의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6c7-115">Specifies the ID of the network interface configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5e6c7-116">-이름</span><span class="sxs-lookup"><span data-stu-id="5e6c7-116">-Name</span></span>
<span data-ttu-id="5e6c7-117">이 cmdlet이 제거 하는 네트워크 인터페이스 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6c7-117">Specifies the name of the network interface configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5e6c7-118">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="5e6c7-118">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="5e6c7-119">VMSS 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6c7-119">Specifies the VMSS object.</span></span>

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

### <span data-ttu-id="5e6c7-120">-확인</span><span class="sxs-lookup"><span data-stu-id="5e6c7-120">-Confirm</span></span>
<span data-ttu-id="5e6c7-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6c7-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e6c7-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e6c7-122">-WhatIf</span></span>
<span data-ttu-id="5e6c7-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5e6c7-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5e6c7-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6c7-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e6c7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e6c7-125">CommonParameters</span></span>
<span data-ttu-id="5e6c7-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5e6c7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e6c7-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e6c7-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e6c7-128">입력</span><span class="sxs-lookup"><span data-stu-id="5e6c7-128">INPUTS</span></span>

### <span data-ttu-id="5e6c7-129">않아야</span><span class="sxs-lookup"><span data-stu-id="5e6c7-129">None</span></span>
<span data-ttu-id="5e6c7-130">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5e6c7-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5e6c7-131">출력</span><span class="sxs-lookup"><span data-stu-id="5e6c7-131">OUTPUTS</span></span>

## <span data-ttu-id="5e6c7-132">상속자</span><span class="sxs-lookup"><span data-stu-id="5e6c7-132">NOTES</span></span>

## <span data-ttu-id="5e6c7-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5e6c7-133">RELATED LINKS</span></span>

[<span data-ttu-id="5e6c7-134">추가-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="5e6c7-134">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="5e6c7-135">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="5e6c7-135">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)


