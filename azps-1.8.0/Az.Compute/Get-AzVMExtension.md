---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 842652D4-0F1C-4D0D-AB55-0D43D3C5D82A
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMExtension.md
ms.openlocfilehash: f861465fcc9f27f71142ffd4e49935039f3da9c0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701344"
---
# <span data-ttu-id="ca7b3-101">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="ca7b3-101">Get-AzVMExtension</span></span>

## <span data-ttu-id="ca7b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca7b3-102">SYNOPSIS</span></span>
<span data-ttu-id="ca7b3-103">가상 컴퓨터에 설치 된 가상 컴퓨터 확장의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ca7b3-103">Gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>

## <span data-ttu-id="ca7b3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ca7b3-104">SYNTAX</span></span>

```
Get-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca7b3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ca7b3-105">DESCRIPTION</span></span>
<span data-ttu-id="ca7b3-106">**AzVMExtension** cmdlet은 가상 컴퓨터에 설치 된 가상 컴퓨터 확장의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ca7b3-106">The **Get-AzVMExtension** cmdlet gets properties of Virtual Machine Extensions installed on a virtual machine.</span></span>
<span data-ttu-id="ca7b3-107">속성을 가져올 확장명의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca7b3-107">Specify the name of an extension for which to get properties.</span></span>
<span data-ttu-id="ca7b3-108">확장의 인스턴스 보기만 가져오려면 Status 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca7b3-108">To get only the instance view of an extension, specify the Status parameter.</span></span>

## <span data-ttu-id="ca7b3-109">예제의</span><span class="sxs-lookup"><span data-stu-id="ca7b3-109">EXAMPLES</span></span>

### <span data-ttu-id="ca7b3-110">예제 1: 확장의 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="ca7b3-110">Example 1: Get properties of an extension</span></span>
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

<span data-ttu-id="ca7b3-111">이 명령은 리소스 그룹 ResourceGroup11의 VirtualMachine22 이라는 가상 컴퓨터에서 CustomScriptExtension 이라는 확장명에 대 한 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ca7b3-111">This command gets properties for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="ca7b3-112">예제 2: 확장의 인스턴스 뷰 가져오기</span><span class="sxs-lookup"><span data-stu-id="ca7b3-112">Example 2: Get instance view of an extension</span></span>
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

<span data-ttu-id="ca7b3-113">이 명령은 리소스 그룹 ResourceGroup11에 있는 VirtualMachine22 이라는 가상 컴퓨터에서 CustomScriptExtension 이라는 확장명에 대 한 인스턴스 보기를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ca7b3-113">This command gets the instance view for the extension named CustomScriptExtension on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

### <span data-ttu-id="ca7b3-114">예제 3: VM에 설치 된 모든 확장 가져오기</span><span class="sxs-lookup"><span data-stu-id="ca7b3-114">Example 3: Get all extensions installed on a VM</span></span>
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

<span data-ttu-id="ca7b3-115">이 명령은 리소스 그룹 ResourceGroup11의 VirtualMachine22 이라는 가상 컴퓨터에 설치 된 확장 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ca7b3-115">This command gets the list of extensions installed on the virtual machine named VirtualMachine22 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="ca7b3-116">변수</span><span class="sxs-lookup"><span data-stu-id="ca7b3-116">PARAMETERS</span></span>

### <span data-ttu-id="ca7b3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca7b3-117">-DefaultProfile</span></span>
<span data-ttu-id="ca7b3-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ca7b3-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca7b3-119">-이름</span><span class="sxs-lookup"><span data-stu-id="ca7b3-119">-Name</span></span>
<span data-ttu-id="ca7b3-120">확장명의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca7b3-120">Specifies the name of an extension.</span></span>
<span data-ttu-id="ca7b3-121">이 cmdlet은이 매개 변수에서 지정 하는 확장에 대 한 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ca7b3-121">This cmdlet gets properties for the extension that this parameter specifies.</span></span>

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

### <span data-ttu-id="ca7b3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca7b3-122">-ResourceGroupName</span></span>
<span data-ttu-id="ca7b3-123">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca7b3-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ca7b3-124">-상태</span><span class="sxs-lookup"><span data-stu-id="ca7b3-124">-Status</span></span>
<span data-ttu-id="ca7b3-125">이 cmdlet이 확장의 인스턴스 보기만을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ca7b3-125">Indicates that this cmdlet gets only the instance view of an extension.</span></span>

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

### <span data-ttu-id="ca7b3-126">-VMName</span><span class="sxs-lookup"><span data-stu-id="ca7b3-126">-VMName</span></span>
<span data-ttu-id="ca7b3-127">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca7b3-127">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="ca7b3-128">이 cmdlet은이 매개 변수에서 지정 하는 가상 컴퓨터에서 확장의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="ca7b3-128">This cmdlet gets properties of an extension from the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="ca7b3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca7b3-129">CommonParameters</span></span>
<span data-ttu-id="ca7b3-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca7b3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca7b3-131">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ca7b3-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca7b3-132">입력</span><span class="sxs-lookup"><span data-stu-id="ca7b3-132">INPUTS</span></span>

### <span data-ttu-id="ca7b3-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ca7b3-133">System.String</span></span>

### <span data-ttu-id="ca7b3-134">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="ca7b3-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ca7b3-135">출력</span><span class="sxs-lookup"><span data-stu-id="ca7b3-135">OUTPUTS</span></span>

### <span data-ttu-id="ca7b3-136">Microsoft. a. PSVirtualMachineExtension</span><span class="sxs-lookup"><span data-stu-id="ca7b3-136">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineExtension</span></span>

## <span data-ttu-id="ca7b3-137">상속자</span><span class="sxs-lookup"><span data-stu-id="ca7b3-137">NOTES</span></span>

## <span data-ttu-id="ca7b3-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ca7b3-138">RELATED LINKS</span></span>

[<span data-ttu-id="ca7b3-139">제거-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="ca7b3-139">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)

[<span data-ttu-id="ca7b3-140">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="ca7b3-140">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)

