---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 842652D4-0F1C-4D0D-AB55-0D43D3C5D82A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtension.md
ms.openlocfilehash: 2c36408b520268acaaa6ae2fa4c4c6030fbd2111
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347721"
---
# <span data-ttu-id="619fa-101">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="619fa-101">Get-AzVMExtension</span></span>

## <span data-ttu-id="619fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="619fa-102">SYNOPSIS</span></span>
<span data-ttu-id="619fa-103">가상 머신에 설치된 Virtual Machine 확장의 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="619fa-103">Gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>

## <span data-ttu-id="619fa-104">구문</span><span class="sxs-lookup"><span data-stu-id="619fa-104">SYNTAX</span></span>

```
Get-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="619fa-105">설명</span><span class="sxs-lookup"><span data-stu-id="619fa-105">DESCRIPTION</span></span>
<span data-ttu-id="619fa-106">**Get-AzVMExtension** cmdlet은 가상 머신에 설치된 Virtual Machine 확장의 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="619fa-106">The **Get-AzVMExtension** cmdlet gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>
<span data-ttu-id="619fa-107">속성을 얻을 확장의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="619fa-107">Specify the name of an extension for which to get properties.</span></span>
<span data-ttu-id="619fa-108">확장의 인스턴스 보기만 얻습니다. 상태 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="619fa-108">To get only the instance view of an extension, specify the Status parameter.</span></span>

## <span data-ttu-id="619fa-109">예제</span><span class="sxs-lookup"><span data-stu-id="619fa-109">EXAMPLES</span></span>

### <span data-ttu-id="619fa-110">예제 1: 확장의 속성 얻기</span><span class="sxs-lookup"><span data-stu-id="619fa-110">Example 1: Get properties of an extension</span></span>
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

<span data-ttu-id="619fa-111">이 명령은 리소스 그룹 ResourceGroup11의 VirtualMachine22라는 가상 머신에서 CustomScriptExtension이라는 확장에 대한 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="619fa-111">This command gets properties for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="619fa-112">예제 2: 확장의 인스턴스 보기를 얻게</span><span class="sxs-lookup"><span data-stu-id="619fa-112">Example 2: Get instance view of an extension</span></span>
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

<span data-ttu-id="619fa-113">이 명령은 리소스 그룹 ResourceGroup11의 VirtualMachine22라는 가상 머신에서 CustomScriptExtension이라는 확장에 대한 인스턴스 보기를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="619fa-113">This command gets the instance view for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="619fa-114">예제 3: VM에 설치된 모든 확장을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="619fa-114">Example 3: Get all extensions installed on a VM</span></span>
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

<span data-ttu-id="619fa-115">이 명령은 리소스 그룹 ResourceGroup11에서 VirtualMachine22라는 가상 머신에 설치된 확장 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="619fa-115">This command gets the list of extensions installed on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="619fa-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="619fa-116">PARAMETERS</span></span>

### <span data-ttu-id="619fa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="619fa-117">-DefaultProfile</span></span>
<span data-ttu-id="619fa-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="619fa-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="619fa-119">-Name</span><span class="sxs-lookup"><span data-stu-id="619fa-119">-Name</span></span>
<span data-ttu-id="619fa-120">확장의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="619fa-120">Specifies the name of an extension.</span></span>
<span data-ttu-id="619fa-121">이 cmdlet은 이 매개 변수가 지정하는 확장에 대한 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="619fa-121">This cmdlet gets properties for the extension that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="619fa-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="619fa-122">-ResourceGroupName</span></span>
<span data-ttu-id="619fa-123">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="619fa-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="619fa-124">-Status</span><span class="sxs-lookup"><span data-stu-id="619fa-124">-Status</span></span>
<span data-ttu-id="619fa-125">이 cmdlet이 확장의 인스턴스 보기만 얻게 됐습니다.</span><span class="sxs-lookup"><span data-stu-id="619fa-125">Indicates that this cmdlet gets only the instance view of an extension.</span></span>

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

### <span data-ttu-id="619fa-126">-VMName</span><span class="sxs-lookup"><span data-stu-id="619fa-126">-VMName</span></span>
<span data-ttu-id="619fa-127">가상 머신의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="619fa-127">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="619fa-128">이 cmdlet은 이 매개 변수가 지정하는 가상 머신에서 확장의 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="619fa-128">This cmdlet gets properties of an extension from the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="619fa-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="619fa-129">CommonParameters</span></span>
<span data-ttu-id="619fa-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="619fa-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="619fa-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="619fa-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="619fa-132">입력</span><span class="sxs-lookup"><span data-stu-id="619fa-132">INPUTS</span></span>

### <span data-ttu-id="619fa-133">System.String</span><span class="sxs-lookup"><span data-stu-id="619fa-133">System.String</span></span>

### <span data-ttu-id="619fa-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="619fa-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="619fa-135">출력</span><span class="sxs-lookup"><span data-stu-id="619fa-135">OUTPUTS</span></span>

### <span data-ttu-id="619fa-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="619fa-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="619fa-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="619fa-137">NOTES</span></span>

## <span data-ttu-id="619fa-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="619fa-138">RELATED LINKS</span></span>

[<span data-ttu-id="619fa-139">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="619fa-139">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)

[<span data-ttu-id="619fa-140">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="619fa-140">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)


