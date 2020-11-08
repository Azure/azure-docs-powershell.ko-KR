---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EC4E8CC1-C21F-4D41-818F-D0BC15AEEE1D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmssnetworkinterfaceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 1b8f9b7843cccf2475e17e1c5d8866972b5b9ee4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217511"
---
# <span data-ttu-id="776db-101">Remove-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="776db-101">Remove-AzVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="776db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="776db-102">SYNOPSIS</span></span>
<span data-ttu-id="776db-103">VMSS에서 네트워크 인터페이스 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="776db-103">Removes a network interface configuration from a VMSS.</span></span>

## <span data-ttu-id="776db-104">구문과</span><span class="sxs-lookup"><span data-stu-id="776db-104">SYNTAX</span></span>

### <span data-ttu-id="776db-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="776db-105">NameParameterSet</span></span>
```
Remove-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="776db-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="776db-106">IdParameterSet</span></span>
```
Remove-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="776db-107">설명은</span><span class="sxs-lookup"><span data-stu-id="776db-107">DESCRIPTION</span></span>
<span data-ttu-id="776db-108">**AzVmssNetworkInterfaceConfiguration** CMDLET은 Vmss (가상 컴퓨터 크기 조정 집합)에서 네트워크 인터페이스 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="776db-108">The **Remove-AzVmssNetworkInterfaceConfiguration** cmdlet removes a network interface configuration from a Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="776db-109">예제의</span><span class="sxs-lookup"><span data-stu-id="776db-109">EXAMPLES</span></span>

### <span data-ttu-id="776db-110">예제 1: 인터페이스 구성 제거</span><span class="sxs-lookup"><span data-stu-id="776db-110">Example 1: Remove an interface configuration</span></span>
```
PS C:\> $VMSS = Get-AzVmss -ResourceGroupName "ResourceGroup11" -VMScaleSetName "ContosoVMSS14"
PS C:\> Remove-AzVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "ContosoVmssInterface02"
```

<span data-ttu-id="776db-111">첫 번째 명령은 Get-AzVmss cmdlet을 사용 하 여 VMSS를 가져온 다음 $VMSS 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="776db-111">The first command gets a VMSS by using the Get-AzVmss cmdlet, and then stores it in the $VMSS variable.</span></span>
<span data-ttu-id="776db-112">두 번째 명령은 $VMSS에서 설정 된 ContosoVmssInterface02 라는 네트워크 인터페이스 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="776db-112">The second command removes the network interface configuration named ContosoVmssInterface02 from the set in $VMSS.</span></span>

## <span data-ttu-id="776db-113">변수</span><span class="sxs-lookup"><span data-stu-id="776db-113">PARAMETERS</span></span>

### <span data-ttu-id="776db-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="776db-114">-DefaultProfile</span></span>
<span data-ttu-id="776db-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="776db-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="776db-116">-Id</span><span class="sxs-lookup"><span data-stu-id="776db-116">-Id</span></span>
<span data-ttu-id="776db-117">이 cmdlet이 제거 하는 네트워크 인터페이스 구성의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="776db-117">Specifies the ID of the network interface configuration that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="776db-118">-이름</span><span class="sxs-lookup"><span data-stu-id="776db-118">-Name</span></span>
<span data-ttu-id="776db-119">이 cmdlet이 제거 하는 네트워크 인터페이스 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="776db-119">Specifies the name of the network interface configuration that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="776db-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="776db-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="776db-121">VMSS 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="776db-121">Specifies the VMSS object.</span></span>

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

### <span data-ttu-id="776db-122">-확인</span><span class="sxs-lookup"><span data-stu-id="776db-122">-Confirm</span></span>
<span data-ttu-id="776db-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="776db-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="776db-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="776db-124">-WhatIf</span></span>
<span data-ttu-id="776db-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="776db-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="776db-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="776db-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="776db-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="776db-127">CommonParameters</span></span>
<span data-ttu-id="776db-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="776db-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="776db-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="776db-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="776db-130">입력</span><span class="sxs-lookup"><span data-stu-id="776db-130">INPUTS</span></span>

### <span data-ttu-id="776db-131">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="776db-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="776db-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="776db-132">System.String</span></span>

## <span data-ttu-id="776db-133">출력</span><span class="sxs-lookup"><span data-stu-id="776db-133">OUTPUTS</span></span>

### <span data-ttu-id="776db-134">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="776db-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="776db-135">상속자</span><span class="sxs-lookup"><span data-stu-id="776db-135">NOTES</span></span>

## <span data-ttu-id="776db-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="776db-136">RELATED LINKS</span></span>

[<span data-ttu-id="776db-137">추가-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="776db-137">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="776db-138">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="776db-138">Get-AzVmss</span></span>](./Get-AzVmss.md)


