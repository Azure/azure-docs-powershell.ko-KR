---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 842652D4-0F1C-4D0D-AB55-0D43D3C5D82A
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtension.md
ms.openlocfilehash: 33be258858a6ace456b7aa3c5b25594a373ccfd7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013835"
---
# <span data-ttu-id="d844b-101">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="d844b-101">Get-AzVMExtension</span></span>

## <span data-ttu-id="d844b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d844b-102">SYNOPSIS</span></span>
<span data-ttu-id="d844b-103">가상 머신에 설치된 Virtual Machine 확장의 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d844b-103">Gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>

## <span data-ttu-id="d844b-104">구문</span><span class="sxs-lookup"><span data-stu-id="d844b-104">SYNTAX</span></span>

### <span data-ttu-id="d844b-105">GetExtensionParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="d844b-105">GetExtensionParameterSet (Default)</span></span>
```
Get-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d844b-106">VMParameterSet</span><span class="sxs-lookup"><span data-stu-id="d844b-106">VMParameterSet</span></span>
```
Get-AzVMExtension [-Status] [-VMObject <PSVirtualMachine>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d844b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d844b-107">ResourceIdParameterSet</span></span>
```
Get-AzVMExtension [-Status] [-ResourceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d844b-108">설명</span><span class="sxs-lookup"><span data-stu-id="d844b-108">DESCRIPTION</span></span>
<span data-ttu-id="d844b-109">**Get-AzVMExtension** cmdlet은 가상 머신에 설치된 Virtual Machine 확장의 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d844b-109">The **Get-AzVMExtension** cmdlet gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>
<span data-ttu-id="d844b-110">속성을 얻을 확장의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d844b-110">Specify the name of an extension for which to get properties.</span></span>
<span data-ttu-id="d844b-111">확장의 인스턴스 보기만 얻게 만들 경우 상태 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d844b-111">To get only the instance view of an extension, specify the Status parameter.</span></span>

## <span data-ttu-id="d844b-112">예제</span><span class="sxs-lookup"><span data-stu-id="d844b-112">EXAMPLES</span></span>

### <span data-ttu-id="d844b-113">예제 1: 확장의 속성 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d844b-113">Example 1: Get properties of an extension</span></span>
```
PS C:\> Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension"

ResourceGroupName       : ResourceGroup11
VMName                  : VirtualMachine22
Name                    : CustomScriptExtension
Location                : eastus
Etag                    : null
Publisher               : Microsoft.Azure.Extensions
ExtensionType           : CustomScript
TypeHandlerVersion      : 2.0
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11
                          /providers/Microsoft.Compute/virtualMachines/VirtualMachine22/extensions/CustomScriptExtension
PublicSettings          : {}
ProtectedSettings       :
ProvisioningState       : Succeeded
Statuses                :
SubStatuses             :
AutoUpgradeMinorVersion : True
ForceUpdateTag          :
```

<span data-ttu-id="d844b-114">이 명령은 ResourceGroup11의 VirtualMachine22라는 가상 머신에서 CustomScriptExtension이라는 확장에 대한 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d844b-114">This command gets properties for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="d844b-115">예제 2: 확장의 인스턴스 보기를 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d844b-115">Example 2: Get instance view of an extension</span></span>
```
PS C:\> Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22" -Name "CustomScriptExtension" -Status

ResourceGroupName       : ResourceGroup11
VMName                  : VirtualMachine22
Name                    : CustomScriptExtension
Location                : eastus
Etag                    : null
Publisher               : Microsoft.Azure.Extensions
ExtensionType           : CustomScript
TypeHandlerVersion      : 2.0
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11
                          /providers/Microsoft.Compute/virtualMachines/VirtualMachine22/extensions/CustomScriptExtension
PublicSettings          : {}
ProtectedSettings       :
ProvisioningState       : Succeeded
Statuses                : {Microsoft.Azure.Management.Compute.Models.InstanceViewStatus}
SubStatuses             :
AutoUpgradeMinorVersion : True
ForceUpdateTag          :
```

<span data-ttu-id="d844b-116">이 명령은 ResourceGroup11의 VirtualMachine22라는 가상 머신에서 CustomScriptExtension이라는 확장에 대한 인스턴스 보기를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d844b-116">This command gets the instance view for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="d844b-117">예제 3: VM에 설치된 모든 확장 사용</span><span class="sxs-lookup"><span data-stu-id="d844b-117">Example 3: Get all extensions installed on a VM</span></span>
```
PS C:\> Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -VMName "VirtualMachine22"

ResourceGroupName       : ResourceGroup11
VMName                  : VirtualMachine22
Name                    : CustomScriptExtension
Location                : eastus
Etag                    : null
Publisher               : Microsoft.Azure.Extensions
ExtensionType           : CustomScript
TypeHandlerVersion      : 2.0
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11
                          /providers/Microsoft.Compute/virtualMachines/VirtualMachine22/extensions/CustomScriptExtension
PublicSettings          : {}
ProtectedSettings       :
ProvisioningState       : Succeeded
Statuses                :
SubStatuses             :
AutoUpgradeMinorVersion : True
ForceUpdateTag          :
```

### <span data-ttu-id="d844b-118">예제 4: VM 매개 변수를 사용하여 확장의 속성 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d844b-118">Example 4: Get properties of an extension using the VM parameter</span></span>
```
PS C:\> $vm = Get-AzVMExtension -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine22"
PS C:\> Get-AzVMExtension -VM $vm

ResourceGroupName       : ResourceGroup11
VMName                  : VirtualMachine22
Name                    : CustomScriptExtension
Location                : eastus
Etag                    : null
Publisher               : Microsoft.Azure.Extensions
ExtensionType           : CustomScript
TypeHandlerVersion      : 2.0
Id                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/ResourceGroup11
                          /providers/Microsoft.Compute/virtualMachines/VirtualMachine22/extensions/CustomScriptExtension
PublicSettings          : {}
ProtectedSettings       :
ProvisioningState       : Succeeded
Statuses                :
SubStatuses             :
AutoUpgradeMinorVersion : True
ForceUpdateTag          :
```

<span data-ttu-id="d844b-119">이 명령은 리소스 그룹 ResourceGroup11에서 VirtualMachine22라는 가상 머신에 설치된 확장 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d844b-119">This command gets the list of extensions installed on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="d844b-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d844b-120">PARAMETERS</span></span>

### <span data-ttu-id="d844b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d844b-121">-DefaultProfile</span></span>
<span data-ttu-id="d844b-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d844b-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d844b-123">-Name</span><span class="sxs-lookup"><span data-stu-id="d844b-123">-Name</span></span>
<span data-ttu-id="d844b-124">확장의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d844b-124">Specifies the name of an extension.</span></span>
<span data-ttu-id="d844b-125">이 cmdlet은 이 매개 변수가 지정하는 확장에 대한 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d844b-125">This cmdlet gets properties for the extension that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: GetExtensionParameterSet
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d844b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d844b-126">-ResourceGroupName</span></span>
<span data-ttu-id="d844b-127">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d844b-127">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetExtensionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d844b-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d844b-128">-ResourceId</span></span>
<span data-ttu-id="d844b-129">확장이 있는 가상 머신 개체를 지정하는 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d844b-129">Resource Id specifying the virtual machine object the extension is on.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d844b-130">-Status</span><span class="sxs-lookup"><span data-stu-id="d844b-130">-Status</span></span>
<span data-ttu-id="d844b-131">이 cmdlet은 확장의 인스턴스 보기만 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d844b-131">Indicates that this cmdlet gets only the instance view of an extension.</span></span>

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

### <span data-ttu-id="d844b-132">-VMName</span><span class="sxs-lookup"><span data-stu-id="d844b-132">-VMName</span></span>
<span data-ttu-id="d844b-133">가상 머신의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d844b-133">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="d844b-134">이 cmdlet은 이 매개 변수가 지정하는 가상 머신에서 확장의 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d844b-134">This cmdlet gets properties of an extension from the virtual machine that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: GetExtensionParameterSet
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d844b-135">-VMObject</span><span class="sxs-lookup"><span data-stu-id="d844b-135">-VMObject</span></span>
<span data-ttu-id="d844b-136">확장이 있는 가상 머신 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d844b-136">Specifies the virtual machine object the extension is on.</span></span>

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

### <span data-ttu-id="d844b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d844b-137">CommonParameters</span></span>
<span data-ttu-id="d844b-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d844b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d844b-139">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d844b-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d844b-140">입력</span><span class="sxs-lookup"><span data-stu-id="d844b-140">INPUTS</span></span>

### <span data-ttu-id="d844b-141">System.String</span><span class="sxs-lookup"><span data-stu-id="d844b-141">System.String</span></span>

### <span data-ttu-id="d844b-142">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d844b-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d844b-143">출력</span><span class="sxs-lookup"><span data-stu-id="d844b-143">OUTPUTS</span></span>

### <span data-ttu-id="d844b-144">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="d844b-144">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="d844b-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d844b-145">NOTES</span></span>

## <span data-ttu-id="d844b-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d844b-146">RELATED LINKS</span></span>

[<span data-ttu-id="d844b-147">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="d844b-147">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)

[<span data-ttu-id="d844b-148">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="d844b-148">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)


