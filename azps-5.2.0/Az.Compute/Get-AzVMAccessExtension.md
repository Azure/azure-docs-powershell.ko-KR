---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 32CF9DA7-5607-4CF9-A2D0-D76A0C005FDA
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMAccessExtension.md
ms.openlocfilehash: c139e1bac6f910a1759e4482abdd7c67d2e7fa55
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98359283"
---
# <span data-ttu-id="858aa-101">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="858aa-101">Get-AzVMAccessExtension</span></span>

## <span data-ttu-id="858aa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="858aa-102">SYNOPSIS</span></span>
<span data-ttu-id="858aa-103">VMAccess 확장에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="858aa-103">Gets information about the VMAccess extension.</span></span>

## <span data-ttu-id="858aa-104">구문</span><span class="sxs-lookup"><span data-stu-id="858aa-104">SYNTAX</span></span>

```
Get-AzVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="858aa-105">설명</span><span class="sxs-lookup"><span data-stu-id="858aa-105">DESCRIPTION</span></span>
<span data-ttu-id="858aa-106">**Get-AzVMAccessExtension** cmdlet은 VMAccess(Virtual Machine Access) Virtual Machine 확장에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="858aa-106">The **Get-AzVMAccessExtension** cmdlet gets information about the Virtual Machine Access (VMAccess) Virtual Machine Extension.</span></span>

## <span data-ttu-id="858aa-107">예제</span><span class="sxs-lookup"><span data-stu-id="858aa-107">EXAMPLES</span></span>

### <span data-ttu-id="858aa-108">예제 1: VMAccess 확장을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="858aa-108">Example 1: Get the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest"
```

<span data-ttu-id="858aa-109">이 명령은 VirtualMachine07이라는 가상 머신에 대해 ContosoTest라는 VMAccess 확장을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="858aa-109">This command gets the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="858aa-110">예제 2: VMAccess 확장의 인스턴스 보기를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="858aa-110">Example 2: Get the instance view of the VMAccess extension</span></span>
```
PS C:\> $VMAccessExtension = Get-AzVMAccessExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoTest" -Status
```

<span data-ttu-id="858aa-111">이 명령은 VirtualMachine07이라는 가상 머신에 대해 ContosoTest라는 VMAccess 확장의 인스턴스 보기를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="858aa-111">This command gets the instance view of the VMAccess extension named ContosoTest for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="858aa-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="858aa-112">PARAMETERS</span></span>

### <span data-ttu-id="858aa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="858aa-113">-DefaultProfile</span></span>
<span data-ttu-id="858aa-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="858aa-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="858aa-115">-Name</span><span class="sxs-lookup"><span data-stu-id="858aa-115">-Name</span></span>
<span data-ttu-id="858aa-116">이 cmdlet에서 얻을 확장의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="858aa-116">Specifies the name of the extension that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="858aa-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="858aa-117">-ResourceGroupName</span></span>
<span data-ttu-id="858aa-118">가상 머신의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="858aa-118">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="858aa-119">-Status</span><span class="sxs-lookup"><span data-stu-id="858aa-119">-Status</span></span>
<span data-ttu-id="858aa-120">이 cmdlet이 확장의 인스턴스 보기만 얻게 된다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="858aa-120">Indicates that this cmdlet gets only the instance view of the extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="858aa-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="858aa-121">-VMName</span></span>
<span data-ttu-id="858aa-122">가상 머신의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="858aa-122">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="858aa-123">이 cmdlet은 이 매개 변수가 지정하는 가상 머신에 대한 VMAccess에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="858aa-123">This cmdlet gets information about VMAccess for the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="858aa-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="858aa-124">CommonParameters</span></span>
<span data-ttu-id="858aa-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="858aa-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="858aa-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="858aa-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="858aa-127">입력</span><span class="sxs-lookup"><span data-stu-id="858aa-127">INPUTS</span></span>

### <span data-ttu-id="858aa-128">System.String</span><span class="sxs-lookup"><span data-stu-id="858aa-128">System.String</span></span>

### <span data-ttu-id="858aa-129">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="858aa-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="858aa-130">출력</span><span class="sxs-lookup"><span data-stu-id="858aa-130">OUTPUTS</span></span>

### <span data-ttu-id="858aa-131">Microsoft.Azure.Commands.Compute.Models.VirtualMachineAccessExtensionContext</span><span class="sxs-lookup"><span data-stu-id="858aa-131">Microsoft.Azure.Commands.Compute.Models.VirtualMachineAccessExtensionContext</span></span>

## <span data-ttu-id="858aa-132">참고 사항</span><span class="sxs-lookup"><span data-stu-id="858aa-132">NOTES</span></span>

## <span data-ttu-id="858aa-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="858aa-133">RELATED LINKS</span></span>

[<span data-ttu-id="858aa-134">Remove-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="858aa-134">Remove-AzVMAccessExtension</span></span>](./Remove-AzVMAccessExtension.md)

[<span data-ttu-id="858aa-135">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="858aa-135">Set-AzVMAccessExtension</span></span>](./Set-AzVMAccessExtension.md)

[<span data-ttu-id="858aa-136">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="858aa-136">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)


