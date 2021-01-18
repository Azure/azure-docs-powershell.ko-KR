---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6C40A7BA-6BE2-464A-84E4-9021935A5BF6
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMExtension.md
ms.openlocfilehash: 70495ee657e511aace4babf47959c4bd6841197c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495972"
---
# <span data-ttu-id="7afb3-101">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="7afb3-101">Remove-AzVMExtension</span></span>

## <span data-ttu-id="7afb3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7afb3-102">SYNOPSIS</span></span>
<span data-ttu-id="7afb3-103">가상 머신에서 확장을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7afb3-103">Removes an extension from a virtual machine.</span></span>

## <span data-ttu-id="7afb3-104">구문</span><span class="sxs-lookup"><span data-stu-id="7afb3-104">SYNTAX</span></span>

```
Remove-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7afb3-105">설명</span><span class="sxs-lookup"><span data-stu-id="7afb3-105">DESCRIPTION</span></span>
<span data-ttu-id="7afb3-106">**Remove-AzVMExtension** cmdlet은 가상 머신의 Virtual Machine 확장에서 확장을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7afb3-106">The **Remove-AzVMExtension** cmdlet removes an extension from the Virtual Machine Extensions of a virtual machine.</span></span>

## <span data-ttu-id="7afb3-107">예제</span><span class="sxs-lookup"><span data-stu-id="7afb3-107">EXAMPLES</span></span>

### <span data-ttu-id="7afb3-108">예제 1: 가상 머신에서 확장 제거</span><span class="sxs-lookup"><span data-stu-id="7afb3-108">Example 1: Remove an extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMExtension -ResourceGroupName "ResourceGroup11" -Name "ContosoTest" -VMName "VirtualMachine22"
```

<span data-ttu-id="7afb3-109">이 명령은 ResourceGroup11의 VirtualMachine22라는 가상 머신에서 ContosoTest라는 확장을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7afb3-109">This command removes the extension named ContosoTest from the virtual machine named VirtualMachine22 in ResourceGroup11.</span></span>

## <span data-ttu-id="7afb3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7afb3-110">PARAMETERS</span></span>

### <span data-ttu-id="7afb3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7afb3-111">-DefaultProfile</span></span>
<span data-ttu-id="7afb3-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7afb3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7afb3-113">-Force</span><span class="sxs-lookup"><span data-stu-id="7afb3-113">-Force</span></span>
<span data-ttu-id="7afb3-114">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="7afb3-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7afb3-115">-Name</span><span class="sxs-lookup"><span data-stu-id="7afb3-115">-Name</span></span>
<span data-ttu-id="7afb3-116">이 cmdlet에서 제거하는 확장의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7afb3-116">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7afb3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7afb3-117">-ResourceGroupName</span></span>
<span data-ttu-id="7afb3-118">가상 머신의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7afb3-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="7afb3-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="7afb3-119">-VMName</span></span>
<span data-ttu-id="7afb3-120">이 cmdlet이 확장을 제거하는 가상 머신의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7afb3-120">Specifies the name of a virtual machine from which this cmdlet removes the extension.</span></span>

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

### <span data-ttu-id="7afb3-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7afb3-121">-Confirm</span></span>
<span data-ttu-id="7afb3-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7afb3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7afb3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7afb3-123">-WhatIf</span></span>
<span data-ttu-id="7afb3-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7afb3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7afb3-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7afb3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7afb3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7afb3-126">CommonParameters</span></span>
<span data-ttu-id="7afb3-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7afb3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7afb3-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7afb3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7afb3-129">입력</span><span class="sxs-lookup"><span data-stu-id="7afb3-129">INPUTS</span></span>

### <span data-ttu-id="7afb3-130">System.String</span><span class="sxs-lookup"><span data-stu-id="7afb3-130">System.String</span></span>

## <span data-ttu-id="7afb3-131">출력</span><span class="sxs-lookup"><span data-stu-id="7afb3-131">OUTPUTS</span></span>

### <span data-ttu-id="7afb3-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="7afb3-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="7afb3-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7afb3-133">NOTES</span></span>

## <span data-ttu-id="7afb3-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7afb3-134">RELATED LINKS</span></span>

[<span data-ttu-id="7afb3-135">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="7afb3-135">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="7afb3-136">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="7afb3-136">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)


