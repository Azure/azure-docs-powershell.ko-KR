---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: EC4E8CC1-C21F-4D41-818F-D0BC15AEEE1D
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmssnetworkinterfaceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 3c9e19c30d89d73a52be4defd18166f88b700889
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986944"
---
# <span data-ttu-id="286fc-101">Remove-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="286fc-101">Remove-AzVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="286fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="286fc-102">SYNOPSIS</span></span>
<span data-ttu-id="286fc-103">VMSS에서 네트워크 인터페이스 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="286fc-103">Removes a network interface configuration from a VMSS.</span></span>

## <span data-ttu-id="286fc-104">구문</span><span class="sxs-lookup"><span data-stu-id="286fc-104">SYNTAX</span></span>

### <span data-ttu-id="286fc-105">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="286fc-105">NameParameterSet</span></span>
```
Remove-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="286fc-106">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="286fc-106">IdParameterSet</span></span>
```
Remove-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="286fc-107">설명</span><span class="sxs-lookup"><span data-stu-id="286fc-107">DESCRIPTION</span></span>
<span data-ttu-id="286fc-108">**Remove-AzVmssNetworkInterfaceConfiguration** cmdlet은 VMSS(Virtual Machine Scale Set)에서 네트워크 인터페이스 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="286fc-108">The **Remove-AzVmssNetworkInterfaceConfiguration** cmdlet removes a network interface configuration from a Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="286fc-109">예제</span><span class="sxs-lookup"><span data-stu-id="286fc-109">EXAMPLES</span></span>

### <span data-ttu-id="286fc-110">예제 1: 인터페이스 구성 제거</span><span class="sxs-lookup"><span data-stu-id="286fc-110">Example 1: Remove an interface configuration</span></span>
```
PS C:\> $VMSS = Get-AzVmss -ResourceGroupName "ResourceGroup11" -VMScaleSetName "ContosoVMSS14"
PS C:\> Remove-AzVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "ContosoVmssInterface02"
```

<span data-ttu-id="286fc-111">첫 번째 명령은 Get-AzVmss cmdlet을 사용하여 VMSS를 $VMSS 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="286fc-111">The first command gets a VMSS by using the Get-AzVmss cmdlet, and then stores it in the $VMSS variable.</span></span>
<span data-ttu-id="286fc-112">두 번째 명령은 ContosoVmssInterface02라는 네트워크 인터페이스 구성을 $VMSS.</span><span class="sxs-lookup"><span data-stu-id="286fc-112">The second command removes the network interface configuration named ContosoVmssInterface02 from the set in $VMSS.</span></span>

## <span data-ttu-id="286fc-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="286fc-113">PARAMETERS</span></span>

### <span data-ttu-id="286fc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="286fc-114">-DefaultProfile</span></span>
<span data-ttu-id="286fc-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="286fc-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="286fc-116">-Id</span><span class="sxs-lookup"><span data-stu-id="286fc-116">-Id</span></span>
<span data-ttu-id="286fc-117">이 cmdlet이 제거한 네트워크 인터페이스 구성의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="286fc-117">Specifies the ID of the network interface configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="286fc-118">-Name</span><span class="sxs-lookup"><span data-stu-id="286fc-118">-Name</span></span>
<span data-ttu-id="286fc-119">이 cmdlet이 제거한 네트워크 인터페이스 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="286fc-119">Specifies the name of the network interface configuration that this cmdlet removes.</span></span>

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

### <span data-ttu-id="286fc-120">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="286fc-120">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="286fc-121">VMSS 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="286fc-121">Specifies the VMSS object.</span></span>

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

### <span data-ttu-id="286fc-122">-확인</span><span class="sxs-lookup"><span data-stu-id="286fc-122">-Confirm</span></span>
<span data-ttu-id="286fc-123">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="286fc-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="286fc-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="286fc-124">-WhatIf</span></span>
<span data-ttu-id="286fc-125">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="286fc-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="286fc-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="286fc-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="286fc-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="286fc-127">CommonParameters</span></span>
<span data-ttu-id="286fc-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="286fc-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="286fc-129">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="286fc-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="286fc-130">입력</span><span class="sxs-lookup"><span data-stu-id="286fc-130">INPUTS</span></span>

### <span data-ttu-id="286fc-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="286fc-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="286fc-132">System.String</span><span class="sxs-lookup"><span data-stu-id="286fc-132">System.String</span></span>

## <span data-ttu-id="286fc-133">출력</span><span class="sxs-lookup"><span data-stu-id="286fc-133">OUTPUTS</span></span>

### <span data-ttu-id="286fc-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="286fc-134">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="286fc-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="286fc-135">NOTES</span></span>

## <span data-ttu-id="286fc-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="286fc-136">RELATED LINKS</span></span>

[<span data-ttu-id="286fc-137">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="286fc-137">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)

[<span data-ttu-id="286fc-138">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="286fc-138">Get-AzVmss</span></span>](./Get-AzVmss.md)


