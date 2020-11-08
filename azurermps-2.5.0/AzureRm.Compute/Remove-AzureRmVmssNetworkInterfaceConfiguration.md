---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: EC4E8CC1-C21F-4D41-818F-D0BC15AEEE1D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmssnetworkinterfaceconfiguration
schema: 2.0.0
ms.openlocfilehash: 46058901188b99eb30d088e2ea784fdc0df8d782
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882682"
---
# <span data-ttu-id="4d9b2-101">Remove-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="4d9b2-101">Remove-AzureRmVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="4d9b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d9b2-102">SYNOPSIS</span></span>
<span data-ttu-id="4d9b2-103">VMSS에서 네트워크 인터페이스 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d9b2-103">Removes a network interface configuration from a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d9b2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4d9b2-104">SYNTAX</span></span>

### <span data-ttu-id="4d9b2-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d9b2-105">NameParameterSet</span></span>
```
Remove-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d9b2-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d9b2-106">IdParameterSet</span></span>
```
Remove-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d9b2-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4d9b2-107">DESCRIPTION</span></span>
<span data-ttu-id="4d9b2-108">**AzureRmVmssNetworkInterfaceConfiguration** CMDLET은 Vmss (가상 컴퓨터 크기 조정 집합)에서 네트워크 인터페이스 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d9b2-108">The **Remove-AzureRmVmssNetworkInterfaceConfiguration** cmdlet removes a network interface configuration from a Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="4d9b2-109">예제의</span><span class="sxs-lookup"><span data-stu-id="4d9b2-109">EXAMPLES</span></span>

### <span data-ttu-id="4d9b2-110">예제 1: 인터페이스 구성 제거</span><span class="sxs-lookup"><span data-stu-id="4d9b2-110">Example 1: Remove an interface configuration</span></span>
```
PS C:\> $VMSS = Get-AzureRmVmss -ResourceGroupName "ResourceGroup11" -VMScaleSetName "ContosoVMSS14"
PS C:\> Remove-AzureRmVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "ContosoVmssInterface02"
```

<span data-ttu-id="4d9b2-111">첫 번째 명령은 Get-AzureRmVmss cmdlet을 사용 하 여 VMSS를 가져온 다음 $VMSS 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d9b2-111">The first command gets a VMSS by using the Get-AzureRmVmss cmdlet, and then stores it in the $VMSS variable.</span></span>

<span data-ttu-id="4d9b2-112">두 번째 명령은 $VMSS에서 설정 된 ContosoVmssInterface02 라는 네트워크 인터페이스 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d9b2-112">The second command removes the network interface configuration named ContosoVmssInterface02 from the set in $VMSS.</span></span>

## <span data-ttu-id="4d9b2-113">변수</span><span class="sxs-lookup"><span data-stu-id="4d9b2-113">PARAMETERS</span></span>

### <span data-ttu-id="4d9b2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d9b2-114">-DefaultProfile</span></span>
<span data-ttu-id="4d9b2-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4d9b2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d9b2-116">-Id</span><span class="sxs-lookup"><span data-stu-id="4d9b2-116">-Id</span></span>
<span data-ttu-id="4d9b2-117">이 cmdlet이 제거 하는 네트워크 인터페이스 구성의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d9b2-117">Specifies the ID of the network interface configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4d9b2-118">-이름</span><span class="sxs-lookup"><span data-stu-id="4d9b2-118">-Name</span></span>
<span data-ttu-id="4d9b2-119">이 cmdlet이 제거 하는 네트워크 인터페이스 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d9b2-119">Specifies the name of the network interface configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4d9b2-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4d9b2-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="4d9b2-121">VMSS 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d9b2-121">Specifies the VMSS object.</span></span>

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

### <span data-ttu-id="4d9b2-122">-확인</span><span class="sxs-lookup"><span data-stu-id="4d9b2-122">-Confirm</span></span>
<span data-ttu-id="4d9b2-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d9b2-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d9b2-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d9b2-124">-WhatIf</span></span>
<span data-ttu-id="4d9b2-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4d9b2-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4d9b2-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4d9b2-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d9b2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d9b2-127">CommonParameters</span></span>
<span data-ttu-id="4d9b2-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d9b2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d9b2-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d9b2-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d9b2-130">입력</span><span class="sxs-lookup"><span data-stu-id="4d9b2-130">INPUTS</span></span>

### <span data-ttu-id="4d9b2-131">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="4d9b2-131">VirtualMachineScaleSet</span></span>
<span data-ttu-id="4d9b2-132">' VirtualMachineScaleSet ' 매개 변수는 파이프라인에서 ' VirtualMachineScaleSet ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d9b2-132">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="4d9b2-133">출력</span><span class="sxs-lookup"><span data-stu-id="4d9b2-133">OUTPUTS</span></span>

### <span data-ttu-id="4d9b2-134">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="4d9b2-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="4d9b2-135">상속자</span><span class="sxs-lookup"><span data-stu-id="4d9b2-135">NOTES</span></span>

## <span data-ttu-id="4d9b2-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4d9b2-136">RELATED LINKS</span></span>

[<span data-ttu-id="4d9b2-137">추가-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="4d9b2-137">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="4d9b2-138">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="4d9b2-138">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

