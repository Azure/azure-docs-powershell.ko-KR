---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 695F224D-DA25-49F2-916E-25DA2A48A4A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdscextensionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtensionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDscExtensionStatus.md
ms.openlocfilehash: b932c7e6f920d538e501b584395f41ce2089b5de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195044"
---
# <span data-ttu-id="f9d57-101">Get-AzVMDscExtensionStatus</span><span class="sxs-lookup"><span data-stu-id="f9d57-101">Get-AzVMDscExtensionStatus</span></span>

## <span data-ttu-id="f9d57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9d57-102">SYNOPSIS</span></span>
<span data-ttu-id="f9d57-103">가상 머신에 대한 DSC 확장 처리기 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f9d57-103">Gets the status of the DSC extension handler for a virtual machine.</span></span>

## <span data-ttu-id="f9d57-104">구문</span><span class="sxs-lookup"><span data-stu-id="f9d57-104">SYNTAX</span></span>

### <span data-ttu-id="f9d57-105">GetDscExtension(기본값)</span><span class="sxs-lookup"><span data-stu-id="f9d57-105">GetDscExtension (Default)</span></span>
```
Get-AzVMDscExtensionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9d57-106">VMParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9d57-106">VMParameterSet</span></span>
```
Get-AzVMDscExtensionStatus [-VM <PSVirtualMachine>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f9d57-107">설명</span><span class="sxs-lookup"><span data-stu-id="f9d57-107">DESCRIPTION</span></span>
<span data-ttu-id="f9d57-108">**Get-AzVMDscExtensionStatus** cmdlet은 리소스 그룹의 가상 머신에 대한 DSC(Desired State Configuration) 확장 처리기 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f9d57-108">The **Get-AzVMDscExtensionStatus** cmdlet gets the status of the Desired State Configuration (DSC) extension handler for a virtual machine in a resource group.</span></span>
<span data-ttu-id="f9d57-109">구성이 적용될 때 이 cmdlet은 Start-DscConfiguration 출력을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d57-109">When a configuration is applied this cmdlet produces output consistent with the Start-DscConfiguration cmdlet.</span></span>

## <span data-ttu-id="f9d57-110">예제</span><span class="sxs-lookup"><span data-stu-id="f9d57-110">EXAMPLES</span></span>

### <span data-ttu-id="f9d57-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="f9d57-111">Example 1</span></span>

<span data-ttu-id="f9d57-112">가상 머신에 대한 DSC 확장 처리기 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f9d57-112">Gets the status of the DSC extension handler for a virtual machine.</span></span> <span data-ttu-id="f9d57-113">(자동Generated)</span><span class="sxs-lookup"><span data-stu-id="f9d57-113">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Get-AzVMDscExtensionStatus -Name 'AgentPool01' -ResourceGroupName myresourcegroup -VMName 'VM01'
```

## <span data-ttu-id="f9d57-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f9d57-114">PARAMETERS</span></span>

### <span data-ttu-id="f9d57-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9d57-115">-DefaultProfile</span></span>
<span data-ttu-id="f9d57-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f9d57-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9d57-117">-Name</span><span class="sxs-lookup"><span data-stu-id="f9d57-117">-Name</span></span>
<span data-ttu-id="f9d57-118">확장을 나타내는 Azure Resource Manager 리소스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d57-118">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="f9d57-119">이 Set-AzVMDscExtension cmdlet은 **Get-AzVMDscExtensionStatus에서** 사용하는 동일한 값인 Microsoft.Powershell.DSC로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="f9d57-119">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the same value that is used by **Get-AzVMDscExtensionStatus**.</span></span>
<span data-ttu-id="f9d57-120">Set cmdlet에서 기본 이름을 변경하거나 Resource Manager 템플릿에서 다른 리소스 이름을 사용한 경우 이 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d57-120">Specify this parameter only if you changed the default name in the Set cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDscExtension
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9d57-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9d57-121">-ResourceGroupName</span></span>
<span data-ttu-id="f9d57-122">가상 머신의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d57-122">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDscExtension
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9d57-123">-VM</span><span class="sxs-lookup"><span data-stu-id="f9d57-123">-VM</span></span>
<span data-ttu-id="f9d57-124">확장이 있는 가상 머신 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d57-124">Specifies the virtual machine object the extension is on.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: VMParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f9d57-125">-VMName</span><span class="sxs-lookup"><span data-stu-id="f9d57-125">-VMName</span></span>
<span data-ttu-id="f9d57-126">이 cmdlet이 DSC 확장 상태를 얻을 가상 머신의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d57-126">Specifies the name of a virtual machine for which this cmdlet gets the DSC extension status.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDscExtension
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9d57-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9d57-127">CommonParameters</span></span>
<span data-ttu-id="f9d57-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f9d57-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9d57-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f9d57-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9d57-130">입력</span><span class="sxs-lookup"><span data-stu-id="f9d57-130">INPUTS</span></span>

### <span data-ttu-id="f9d57-131">System.String</span><span class="sxs-lookup"><span data-stu-id="f9d57-131">System.String</span></span>

## <span data-ttu-id="f9d57-132">출력</span><span class="sxs-lookup"><span data-stu-id="f9d57-132">OUTPUTS</span></span>

### <span data-ttu-id="f9d57-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span><span class="sxs-lookup"><span data-stu-id="f9d57-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineInstanceView</span></span>

## <span data-ttu-id="f9d57-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f9d57-134">NOTES</span></span>

## <span data-ttu-id="f9d57-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f9d57-135">RELATED LINKS</span></span>

[<span data-ttu-id="f9d57-136">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="f9d57-136">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)

