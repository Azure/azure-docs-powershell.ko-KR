---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSecret.md
ms.openlocfilehash: df6103cbd3ca58b5e324618c9ad2d8be5820fc96
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98355413"
---
# <span data-ttu-id="6986a-101">Remove-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="6986a-101">Remove-AzVMSecret</span></span>

## <span data-ttu-id="6986a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6986a-102">SYNOPSIS</span></span>
<span data-ttu-id="6986a-103">가상 머신 개체에서 (a) 비밀을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6986a-103">Removes (a) secret(s) from a virtual machine object</span></span>

## <span data-ttu-id="6986a-104">구문</span><span class="sxs-lookup"><span data-stu-id="6986a-104">SYNTAX</span></span>

```
Remove-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6986a-105">설명</span><span class="sxs-lookup"><span data-stu-id="6986a-105">DESCRIPTION</span></span>
<span data-ttu-id="6986a-106">이 Remove-AzVMSecret cmdlet은 가상 머신 개체에서 (a) 비밀을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="6986a-106">The Remove-AzVMSecret cmdlet removes (a) secret(s) from a virtual machine object.</span></span>

## <span data-ttu-id="6986a-107">예제</span><span class="sxs-lookup"><span data-stu-id="6986a-107">EXAMPLES</span></span>

### <span data-ttu-id="6986a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="6986a-108">Example 1</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "rg1" -Name "vm1" | Remove-AzVMSecret | Update-AzVM
```

<span data-ttu-id="6986a-109">리소스 그룹 "rg1"의 가상 머신 "vm1"에서 모든 비밀을 제거하고 VM을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6986a-109">Removes all secrets from a virtual machine "vm1" in resource group "rg1" and update the VM</span></span>

## <span data-ttu-id="6986a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6986a-110">PARAMETERS</span></span>

### <span data-ttu-id="6986a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6986a-111">-DefaultProfile</span></span>
<span data-ttu-id="6986a-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6986a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6986a-113">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="6986a-113">-SourceVaultId</span></span>
<span data-ttu-id="6986a-114">이 cmdlet에서 제거하는 원본 자격 증명 모음의 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6986a-114">Specifies an array of source vault IDs that this cmdlet removes.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: Id

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6986a-115">-VM</span><span class="sxs-lookup"><span data-stu-id="6986a-115">-VM</span></span>
<span data-ttu-id="6986a-116">이 cmdlet이 (a) 비밀을 제거하는 가상 머신을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6986a-116">Specifies the virtual machine from which this cmdlet removes (a) secret(s).</span></span>
<span data-ttu-id="6986a-117">가상 머신 개체를 얻습니다. Get-AzVM cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="6986a-117">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="6986a-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6986a-118">-Confirm</span></span>
<span data-ttu-id="6986a-119">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6986a-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6986a-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6986a-120">-WhatIf</span></span>
<span data-ttu-id="6986a-121">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="6986a-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6986a-122">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6986a-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6986a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6986a-123">CommonParameters</span></span>
<span data-ttu-id="6986a-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6986a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6986a-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6986a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6986a-126">입력</span><span class="sxs-lookup"><span data-stu-id="6986a-126">INPUTS</span></span>

### <span data-ttu-id="6986a-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="6986a-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="6986a-128">출력</span><span class="sxs-lookup"><span data-stu-id="6986a-128">OUTPUTS</span></span>

### <span data-ttu-id="6986a-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="6986a-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="6986a-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6986a-130">NOTES</span></span>

## <span data-ttu-id="6986a-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6986a-131">RELATED LINKS</span></span>
