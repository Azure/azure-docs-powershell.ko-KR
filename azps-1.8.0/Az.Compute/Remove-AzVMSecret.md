---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSecret.md
ms.openlocfilehash: 9f9b8f28fd3b2597dede1b9fe50780b2c5e43abb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701275"
---
# <span data-ttu-id="1e678-101">Remove-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="1e678-101">Remove-AzVMSecret</span></span>

## <span data-ttu-id="1e678-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e678-102">SYNOPSIS</span></span>
<span data-ttu-id="1e678-103">가상 머신 개체에서 (a) 비밀을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e678-103">Removes (a) secret(s) from a virtual machine object</span></span>

## <span data-ttu-id="1e678-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1e678-104">SYNTAX</span></span>

```
Remove-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e678-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1e678-105">DESCRIPTION</span></span>
<span data-ttu-id="1e678-106">Remove-AzVMSecret cmdlet은 가상 컴퓨터 개체에서 (a) 비밀을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e678-106">The Remove-AzVMSecret cmdlet removes (a) secret(s) from a virtual machine object.</span></span>

## <span data-ttu-id="1e678-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1e678-107">EXAMPLES</span></span>

### <span data-ttu-id="1e678-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="1e678-108">Example 1</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "rg1" -Name "vm1" | Remove-AzVMSecret | Update-AzVM
```

<span data-ttu-id="1e678-109">리소스 그룹 "rg1"의 가상 머신 "vm1"에서 모든 비밀을 제거 하 고 VM을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e678-109">Removes all secrets from a virtual machine "vm1" in resource group "rg1" and update the VM</span></span>

## <span data-ttu-id="1e678-110">변수</span><span class="sxs-lookup"><span data-stu-id="1e678-110">PARAMETERS</span></span>

### <span data-ttu-id="1e678-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e678-111">-DefaultProfile</span></span>
<span data-ttu-id="1e678-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1e678-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e678-113">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="1e678-113">-SourceVaultId</span></span>
<span data-ttu-id="1e678-114">이 cmdlet이 제거 하는 원본 보관소 Id의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e678-114">Specifies an array of source vault IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1e678-115">-VM</span><span class="sxs-lookup"><span data-stu-id="1e678-115">-VM</span></span>
<span data-ttu-id="1e678-116">이 cmdlet가 암호 (a)를 제거 하는 가상 컴퓨터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e678-116">Specifies the virtual machine from which this cmdlet removes (a) secret(s).</span></span>
<span data-ttu-id="1e678-117">가상 컴퓨터 개체를 가져오려면 Get-AzVM cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e678-117">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="1e678-118">-확인</span><span class="sxs-lookup"><span data-stu-id="1e678-118">-Confirm</span></span>
<span data-ttu-id="1e678-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e678-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e678-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e678-120">-WhatIf</span></span>
<span data-ttu-id="1e678-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1e678-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e678-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1e678-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e678-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e678-123">CommonParameters</span></span>
<span data-ttu-id="1e678-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e678-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e678-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e678-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e678-126">입력</span><span class="sxs-lookup"><span data-stu-id="1e678-126">INPUTS</span></span>

### <span data-ttu-id="1e678-127">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e678-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="1e678-128">출력</span><span class="sxs-lookup"><span data-stu-id="1e678-128">OUTPUTS</span></span>

### <span data-ttu-id="1e678-129">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e678-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="1e678-130">상속자</span><span class="sxs-lookup"><span data-stu-id="1e678-130">NOTES</span></span>

## <span data-ttu-id="1e678-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1e678-131">RELATED LINKS</span></span>
