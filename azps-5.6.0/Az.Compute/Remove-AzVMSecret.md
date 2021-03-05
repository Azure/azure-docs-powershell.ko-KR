---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSecret.md
ms.openlocfilehash: 794447801789bd8923012c19914ee41e736fb945
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985245"
---
# <span data-ttu-id="4de63-101">Remove-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="4de63-101">Remove-AzVMSecret</span></span>

## <span data-ttu-id="4de63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4de63-102">SYNOPSIS</span></span>
<span data-ttu-id="4de63-103">가상 머신 개체에서 (a) 비밀 제거</span><span class="sxs-lookup"><span data-stu-id="4de63-103">Removes (a) secret(s) from a virtual machine object</span></span>

## <span data-ttu-id="4de63-104">구문</span><span class="sxs-lookup"><span data-stu-id="4de63-104">SYNTAX</span></span>

```
Remove-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4de63-105">설명</span><span class="sxs-lookup"><span data-stu-id="4de63-105">DESCRIPTION</span></span>
<span data-ttu-id="4de63-106">Remove-AzVMSecret cmdlet은 가상 머신 개체에서 (a) 비밀을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="4de63-106">The Remove-AzVMSecret cmdlet removes (a) secret(s) from a virtual machine object.</span></span>

## <span data-ttu-id="4de63-107">예제</span><span class="sxs-lookup"><span data-stu-id="4de63-107">EXAMPLES</span></span>

### <span data-ttu-id="4de63-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="4de63-108">Example 1</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "rg1" -Name "vm1" | Remove-AzVMSecret | Update-AzVM
```

<span data-ttu-id="4de63-109">리소스 그룹 "rg1"에서 가상 머신 "vm1"에서 모든 비밀을 제거하고 VM을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="4de63-109">Removes all secrets from a virtual machine "vm1" in resource group "rg1" and update the VM</span></span>

## <span data-ttu-id="4de63-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="4de63-110">PARAMETERS</span></span>

### <span data-ttu-id="4de63-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4de63-111">-DefaultProfile</span></span>
<span data-ttu-id="4de63-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4de63-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4de63-113">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="4de63-113">-SourceVaultId</span></span>
<span data-ttu-id="4de63-114">이 cmdlet이 제거한 원본 자격 증명 모음 아이디 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4de63-114">Specifies an array of source vault IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4de63-115">-VM</span><span class="sxs-lookup"><span data-stu-id="4de63-115">-VM</span></span>
<span data-ttu-id="4de63-116">이 cmdlet이 (a) 비밀을 제거하는 가상 머신을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4de63-116">Specifies the virtual machine from which this cmdlet removes (a) secret(s).</span></span>
<span data-ttu-id="4de63-117">가상 머신 개체를 얻은 경우 Get-AzVM cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="4de63-117">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="4de63-118">-확인</span><span class="sxs-lookup"><span data-stu-id="4de63-118">-Confirm</span></span>
<span data-ttu-id="4de63-119">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4de63-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4de63-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4de63-120">-WhatIf</span></span>
<span data-ttu-id="4de63-121">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="4de63-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4de63-122">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4de63-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4de63-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4de63-123">CommonParameters</span></span>
<span data-ttu-id="4de63-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4de63-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4de63-125">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4de63-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4de63-126">입력</span><span class="sxs-lookup"><span data-stu-id="4de63-126">INPUTS</span></span>

### <span data-ttu-id="4de63-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="4de63-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="4de63-128">출력</span><span class="sxs-lookup"><span data-stu-id="4de63-128">OUTPUTS</span></span>

### <span data-ttu-id="4de63-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="4de63-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="4de63-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4de63-130">NOTES</span></span>

## <span data-ttu-id="4de63-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4de63-131">RELATED LINKS</span></span>
