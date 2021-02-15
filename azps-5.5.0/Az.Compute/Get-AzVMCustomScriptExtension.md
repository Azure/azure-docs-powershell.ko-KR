---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 1017A74D-6420-4E51-A4A4-1AD3AD6D8122
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMCustomScriptExtension.md
ms.openlocfilehash: 1d1ccb7f8e47ce34b798124d54fdd85aa18c7d69
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177721"
---
# <span data-ttu-id="ade1a-101">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="ade1a-101">Get-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="ade1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ade1a-102">SYNOPSIS</span></span>
<span data-ttu-id="ade1a-103">사용자 지정 스크립트 확장에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ade1a-103">Gets information about a custom script extension.</span></span>

## <span data-ttu-id="ade1a-104">구문</span><span class="sxs-lookup"><span data-stu-id="ade1a-104">SYNTAX</span></span>

```
Get-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ade1a-105">설명</span><span class="sxs-lookup"><span data-stu-id="ade1a-105">DESCRIPTION</span></span>
<span data-ttu-id="ade1a-106">**Get-AzVMCustomScriptExtension** cmdlet은 가상 머신의 사용자 지정 스크립트 Virtual Machine 확장에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ade1a-106">The **Get-AzVMCustomScriptExtension** cmdlet gets information about a custom script Virtual Machine Extension on a virtual machine.</span></span>

## <span data-ttu-id="ade1a-107">예제</span><span class="sxs-lookup"><span data-stu-id="ade1a-107">EXAMPLES</span></span>

### <span data-ttu-id="ade1a-108">예제 1: 사용자 지정 스크립트 확장 사용</span><span class="sxs-lookup"><span data-stu-id="ade1a-108">Example 1: Get a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript"
```

<span data-ttu-id="ade1a-109">이 명령은 VirtualMachine07이라는 가상 머신에 대한 ContosoCustomScript라는 사용자 지정 스크립트 확장을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ade1a-109">This command gets the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

### <span data-ttu-id="ade1a-110">예제 2: 사용자 지정 스크립트 확장의 인스턴스 보기를 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ade1a-110">Example 2: Get the instance view of a custom script extension</span></span>
```
PS C:\> $VMCustomScriptExtension = Get-AzVMCustomScriptExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine07" -Name "ContosoCustomScript" -Status
```

<span data-ttu-id="ade1a-111">이 명령은 VirtualMachine07이라는 가상 머신에 대한 ContosoCustomScript라는 사용자 지정 스크립트 확장의 인스턴스 보기를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ade1a-111">This command gets the instance view of the custom script extension named ContosoCustomScript for the virtual machine named VirtualMachine07.</span></span>

## <span data-ttu-id="ade1a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ade1a-112">PARAMETERS</span></span>

### <span data-ttu-id="ade1a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ade1a-113">-DefaultProfile</span></span>
<span data-ttu-id="ade1a-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ade1a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ade1a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="ade1a-115">-Name</span></span>
<span data-ttu-id="ade1a-116">이 cmdlet에서 정보를 얻을 사용자 지정 스크립트 확장의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ade1a-116">Specifies the name of the custom script extension about which this cmdlet gets information.</span></span>

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

### <span data-ttu-id="ade1a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ade1a-117">-ResourceGroupName</span></span>
<span data-ttu-id="ade1a-118">가상 머신의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ade1a-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="ade1a-119">-Status</span><span class="sxs-lookup"><span data-stu-id="ade1a-119">-Status</span></span>
<span data-ttu-id="ade1a-120">이 cmdlet이 사용자 지정 스크립트 확장의 인스턴스 보기를 얻게 됐습니다.</span><span class="sxs-lookup"><span data-stu-id="ade1a-120">Indicates that this cmdlet gets the instance view of the custom script extension.</span></span>

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

### <span data-ttu-id="ade1a-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="ade1a-121">-VMName</span></span>
<span data-ttu-id="ade1a-122">이 cmdlet이 사용자 지정 스크립트 확장을 얻을 가상 머신의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ade1a-122">Specifies the name of a virtual machine for which this cmdlet gets the custom script extension.</span></span>

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

### <span data-ttu-id="ade1a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ade1a-123">CommonParameters</span></span>
<span data-ttu-id="ade1a-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ade1a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ade1a-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ade1a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ade1a-126">입력</span><span class="sxs-lookup"><span data-stu-id="ade1a-126">INPUTS</span></span>

### <span data-ttu-id="ade1a-127">System.String</span><span class="sxs-lookup"><span data-stu-id="ade1a-127">System.String</span></span>

### <span data-ttu-id="ade1a-128">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ade1a-128">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ade1a-129">출력</span><span class="sxs-lookup"><span data-stu-id="ade1a-129">OUTPUTS</span></span>

### <span data-ttu-id="ade1a-130">Microsoft.Azure.Commands.Compute.Models.VirtualMachineCustomScriptExtensionContext</span><span class="sxs-lookup"><span data-stu-id="ade1a-130">Microsoft.Azure.Commands.Compute.Models.VirtualMachineCustomScriptExtensionContext</span></span>

## <span data-ttu-id="ade1a-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ade1a-131">NOTES</span></span>

## <span data-ttu-id="ade1a-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ade1a-132">RELATED LINKS</span></span>

[<span data-ttu-id="ade1a-133">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="ade1a-133">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="ade1a-134">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="ade1a-134">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="ade1a-135">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="ade1a-135">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)


