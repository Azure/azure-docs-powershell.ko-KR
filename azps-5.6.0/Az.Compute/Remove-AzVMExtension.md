---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6C40A7BA-6BE2-464A-84E4-9021935A5BF6
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMExtension.md
ms.openlocfilehash: cc813b4d6b3c5efbd1c54c25b5e198c5b0ce94e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985273"
---
# <span data-ttu-id="fe1f6-101">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="fe1f6-101">Remove-AzVMExtension</span></span>

## <span data-ttu-id="fe1f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe1f6-102">SYNOPSIS</span></span>
<span data-ttu-id="fe1f6-103">가상 머신에서 확장을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-103">Removes an extension from a virtual machine.</span></span>

## <span data-ttu-id="fe1f6-104">구문</span><span class="sxs-lookup"><span data-stu-id="fe1f6-104">SYNTAX</span></span>

```
Remove-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe1f6-105">설명</span><span class="sxs-lookup"><span data-stu-id="fe1f6-105">DESCRIPTION</span></span>
<span data-ttu-id="fe1f6-106">**Remove-AzVMExtension** cmdlet은 가상 머신의 Virtual Machine 확장에서 확장을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-106">The **Remove-AzVMExtension** cmdlet removes an extension from the Virtual Machine Extensions of a virtual machine.</span></span>

## <span data-ttu-id="fe1f6-107">예제</span><span class="sxs-lookup"><span data-stu-id="fe1f6-107">EXAMPLES</span></span>

### <span data-ttu-id="fe1f6-108">예제 1: 가상 머신에서 확장 제거</span><span class="sxs-lookup"><span data-stu-id="fe1f6-108">Example 1: Remove an extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMExtension -ResourceGroupName "ResourceGroup11" -Name "ContosoTest" -VMName "VirtualMachine22"
```

<span data-ttu-id="fe1f6-109">이 명령은 ResourceGroup11의 VirtualMachine22라는 가상 머신에서 ContosoTest라는 확장을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-109">This command removes the extension named ContosoTest from the virtual machine named VirtualMachine22 in ResourceGroup11.</span></span>

## <span data-ttu-id="fe1f6-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="fe1f6-110">PARAMETERS</span></span>

### <span data-ttu-id="fe1f6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe1f6-111">-DefaultProfile</span></span>
<span data-ttu-id="fe1f6-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fe1f6-113">-Force</span><span class="sxs-lookup"><span data-stu-id="fe1f6-113">-Force</span></span>
<span data-ttu-id="fe1f6-114">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe1f6-115">-Name</span><span class="sxs-lookup"><span data-stu-id="fe1f6-115">-Name</span></span>
<span data-ttu-id="fe1f6-116">이 cmdlet이 제거한 확장의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-116">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="fe1f6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe1f6-117">-ResourceGroupName</span></span>
<span data-ttu-id="fe1f6-118">가상 머신의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="fe1f6-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="fe1f6-119">-VMName</span></span>
<span data-ttu-id="fe1f6-120">이 cmdlet에서 확장을 제거하는 가상 머신의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-120">Specifies the name of a virtual machine from which this cmdlet removes the extension.</span></span>

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

### <span data-ttu-id="fe1f6-121">-확인</span><span class="sxs-lookup"><span data-stu-id="fe1f6-121">-Confirm</span></span>
<span data-ttu-id="fe1f6-122">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe1f6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe1f6-123">-WhatIf</span></span>
<span data-ttu-id="fe1f6-124">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe1f6-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe1f6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe1f6-126">CommonParameters</span></span>
<span data-ttu-id="fe1f6-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fe1f6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe1f6-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fe1f6-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe1f6-129">입력</span><span class="sxs-lookup"><span data-stu-id="fe1f6-129">INPUTS</span></span>

### <span data-ttu-id="fe1f6-130">System.String</span><span class="sxs-lookup"><span data-stu-id="fe1f6-130">System.String</span></span>

## <span data-ttu-id="fe1f6-131">출력</span><span class="sxs-lookup"><span data-stu-id="fe1f6-131">OUTPUTS</span></span>

### <span data-ttu-id="fe1f6-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="fe1f6-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="fe1f6-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fe1f6-133">NOTES</span></span>

## <span data-ttu-id="fe1f6-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fe1f6-134">RELATED LINKS</span></span>

[<span data-ttu-id="fe1f6-135">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="fe1f6-135">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="fe1f6-136">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="fe1f6-136">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)


