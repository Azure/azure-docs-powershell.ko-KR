---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6B26DADE-BF71-48D2-98C9-87B2F6182AC2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMNetworkInterface.md
ms.openlocfilehash: c8c7a33e3eebc5e055d6d45f6ddbf3a4e0b1f489
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355418"
---
# <span data-ttu-id="1fbd9-101">Remove-AzVMNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="1fbd9-101">Remove-AzVMNetworkInterface</span></span>

## <span data-ttu-id="1fbd9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1fbd9-102">SYNOPSIS</span></span>
<span data-ttu-id="1fbd9-103">가상 머신에서 네트워크 인터페이스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1fbd9-103">Removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="1fbd9-104">구문</span><span class="sxs-lookup"><span data-stu-id="1fbd9-104">SYNTAX</span></span>

```
Remove-AzVMNetworkInterface [-VM] <PSVirtualMachine> [[-NetworkInterfaceIDs] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fbd9-105">설명</span><span class="sxs-lookup"><span data-stu-id="1fbd9-105">DESCRIPTION</span></span>
<span data-ttu-id="1fbd9-106">**Remove-AzVMNetworkInterface** cmdlet은 가상 머신에서 네트워크 인터페이스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1fbd9-106">The **Remove-AzVMNetworkInterface** cmdlet removes a network interface from a virtual machine.</span></span>

## <span data-ttu-id="1fbd9-107">예제</span><span class="sxs-lookup"><span data-stu-id="1fbd9-107">EXAMPLES</span></span>

## <span data-ttu-id="1fbd9-108">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1fbd9-108">PARAMETERS</span></span>

### <span data-ttu-id="1fbd9-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fbd9-109">-DefaultProfile</span></span>
<span data-ttu-id="1fbd9-110">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1fbd9-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1fbd9-111">-NetworkInterfaceIDs</span><span class="sxs-lookup"><span data-stu-id="1fbd9-111">-NetworkInterfaceIDs</span></span>
<span data-ttu-id="1fbd9-112">이 cmdlet에서 제거하는 네트워크 인터페이스의 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1fbd9-112">Specifies an array of network interface IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1fbd9-113">-VM</span><span class="sxs-lookup"><span data-stu-id="1fbd9-113">-VM</span></span>
<span data-ttu-id="1fbd9-114">이 cmdlet이 네트워크 인터페이스를 제거하는 가상 머신을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1fbd9-114">Specifies the virtual machine from which this cmdlet removes a network interface.</span></span>
<span data-ttu-id="1fbd9-115">가상 머신 개체를 얻습니다. Get-AzVM cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="1fbd9-115">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="1fbd9-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1fbd9-116">-Confirm</span></span>
<span data-ttu-id="1fbd9-117">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1fbd9-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fbd9-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fbd9-118">-WhatIf</span></span>
<span data-ttu-id="1fbd9-119">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1fbd9-119">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1fbd9-120">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1fbd9-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fbd9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fbd9-121">CommonParameters</span></span>
<span data-ttu-id="1fbd9-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1fbd9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fbd9-123">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1fbd9-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fbd9-124">입력</span><span class="sxs-lookup"><span data-stu-id="1fbd9-124">INPUTS</span></span>

### <span data-ttu-id="1fbd9-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="1fbd9-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="1fbd9-126">출력</span><span class="sxs-lookup"><span data-stu-id="1fbd9-126">OUTPUTS</span></span>

### <span data-ttu-id="1fbd9-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="1fbd9-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="1fbd9-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1fbd9-128">NOTES</span></span>

## <span data-ttu-id="1fbd9-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1fbd9-129">RELATED LINKS</span></span>

[<span data-ttu-id="1fbd9-130">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="1fbd9-130">Get-AzVM</span></span>](./Get-AzVM.md)


