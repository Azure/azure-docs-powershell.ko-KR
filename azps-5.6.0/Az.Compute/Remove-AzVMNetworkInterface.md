---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
ms.openlocfilehash: 247a066da4d6a8a84587e451850954df40ba7be4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007051"
---
# <span data-ttu-id="7cdb3-101">Remove-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7cdb3-101">Remove-AzVMNetworkInterface</span></span>

## <span data-ttu-id="7cdb3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7cdb3-102">SYNOPSIS</span></span>
<span data-ttu-id="7cdb3-103">가상 머신에서 네트워크 인터페이스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7cdb3-103">Removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="7cdb3-104">구문</span><span class="sxs-lookup"><span data-stu-id="7cdb3-104">SYNTAX</span></span>

```
Remove-AzVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cdb3-105">설명</span><span class="sxs-lookup"><span data-stu-id="7cdb3-105">DESCRIPTION</span></span>
<span data-ttu-id="7cdb3-106">**Remove-AzVMNetworkInterface** cmdlet은 가상 머신에서 네트워크 인터페이스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7cdb3-106">The **Remove-AzVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="7cdb3-107">예제</span><span class="sxs-lookup"><span data-stu-id="7cdb3-107">EXAMPLES</span></span>

## <span data-ttu-id="7cdb3-108">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7cdb3-108">PARAMETERS</span></span>

### <span data-ttu-id="7cdb3-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cdb3-109">-DefaultProfile</span></span>
<span data-ttu-id="7cdb3-110">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7cdb3-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7cdb3-111">-NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="7cdb3-111">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="7cdb3-112">이 cmdlet이 제거한 네트워크 인터페이스 아이디 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7cdb3-112">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: Id, NicIds

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7cdb3-113">-VM</span><span class="sxs-lookup"><span data-stu-id="7cdb3-113">-VM</span></span>
<span data-ttu-id="7cdb3-114">이 cmdlet이 네트워크 인터페이스를 제거하는 가상 머신을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7cdb3-114">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="7cdb3-115">가상 머신 개체를 얻은 경우 Get-AzVM cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="7cdb3-115">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7cdb3-116">-확인</span><span class="sxs-lookup"><span data-stu-id="7cdb3-116">-Confirm</span></span>
<span data-ttu-id="7cdb3-117">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7cdb3-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cdb3-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cdb3-118">-WhatIf</span></span>
<span data-ttu-id="7cdb3-119">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="7cdb3-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7cdb3-120">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7cdb3-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cdb3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cdb3-121">CommonParameters</span></span>
<span data-ttu-id="7cdb3-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7cdb3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cdb3-123">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7cdb3-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cdb3-124">입력</span><span class="sxs-lookup"><span data-stu-id="7cdb3-124">INPUTS</span></span>

### <span data-ttu-id="7cdb3-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="7cdb3-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="7cdb3-126">출력</span><span class="sxs-lookup"><span data-stu-id="7cdb3-126">OUTPUTS</span></span>

### <span data-ttu-id="7cdb3-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="7cdb3-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="7cdb3-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7cdb3-128">NOTES</span></span>

## <span data-ttu-id="7cdb3-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7cdb3-129">RELATED LINKS</span></span>

[<span data-ttu-id="7cdb3-130">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="7cdb3-130">Get-AzVM</span></span>](./Get-AzVM.md)


