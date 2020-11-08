---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMSecret.md
ms.openlocfilehash: df6103cbd3ca58b5e324618c9ad2d8be5820fc96
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048108"
---
# <span data-ttu-id="58aed-101">Remove-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="58aed-101">Remove-AzVMSecret</span></span>

## <span data-ttu-id="58aed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58aed-102">SYNOPSIS</span></span>
<span data-ttu-id="58aed-103">가상 머신 개체에서 (a) 비밀을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="58aed-103">Removes (a) secret(s) from a virtual machine object</span></span>

## <span data-ttu-id="58aed-104">구문과</span><span class="sxs-lookup"><span data-stu-id="58aed-104">SYNTAX</span></span>

```
Remove-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58aed-105">설명은</span><span class="sxs-lookup"><span data-stu-id="58aed-105">DESCRIPTION</span></span>
<span data-ttu-id="58aed-106">Remove-AzVMSecret cmdlet은 가상 컴퓨터 개체에서 (a) 비밀을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="58aed-106">The Remove-AzVMSecret cmdlet removes (a) secret(s) from a virtual machine object.</span></span>

## <span data-ttu-id="58aed-107">예제의</span><span class="sxs-lookup"><span data-stu-id="58aed-107">EXAMPLES</span></span>

### <span data-ttu-id="58aed-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="58aed-108">Example 1</span></span>
```
PS C:\> Get-AzVM -ResourceGroupName "rg1" -Name "vm1" | Remove-AzVMSecret | Update-AzVM
```

<span data-ttu-id="58aed-109">리소스 그룹 "rg1"의 가상 머신 "vm1"에서 모든 비밀을 제거 하 고 VM을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="58aed-109">Removes all secrets from a virtual machine "vm1" in resource group "rg1" and update the VM</span></span>

## <span data-ttu-id="58aed-110">변수</span><span class="sxs-lookup"><span data-stu-id="58aed-110">PARAMETERS</span></span>

### <span data-ttu-id="58aed-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58aed-111">-DefaultProfile</span></span>
<span data-ttu-id="58aed-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="58aed-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58aed-113">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="58aed-113">-SourceVaultId</span></span>
<span data-ttu-id="58aed-114">이 cmdlet이 제거 하는 원본 보관소 Id의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58aed-114">Specifies an array of source vault IDs that this cmdlet removes.</span></span>

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

### <span data-ttu-id="58aed-115">-VM</span><span class="sxs-lookup"><span data-stu-id="58aed-115">-VM</span></span>
<span data-ttu-id="58aed-116">이 cmdlet가 암호 (a)를 제거 하는 가상 컴퓨터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="58aed-116">Specifies the virtual machine from which this cmdlet removes (a) secret(s).</span></span>
<span data-ttu-id="58aed-117">가상 컴퓨터 개체를 가져오려면 Get-AzVM cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="58aed-117">To obtain a virtual machine object, use the Get-AzVM cmdlet.</span></span>

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

### <span data-ttu-id="58aed-118">-확인</span><span class="sxs-lookup"><span data-stu-id="58aed-118">-Confirm</span></span>
<span data-ttu-id="58aed-119">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="58aed-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58aed-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58aed-120">-WhatIf</span></span>
<span data-ttu-id="58aed-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="58aed-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58aed-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="58aed-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58aed-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58aed-123">CommonParameters</span></span>
<span data-ttu-id="58aed-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="58aed-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58aed-125">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="58aed-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58aed-126">입력</span><span class="sxs-lookup"><span data-stu-id="58aed-126">INPUTS</span></span>

### <span data-ttu-id="58aed-127">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="58aed-127">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="58aed-128">출력</span><span class="sxs-lookup"><span data-stu-id="58aed-128">OUTPUTS</span></span>

### <span data-ttu-id="58aed-129">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="58aed-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="58aed-130">상속자</span><span class="sxs-lookup"><span data-stu-id="58aed-130">NOTES</span></span>

## <span data-ttu-id="58aed-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="58aed-131">RELATED LINKS</span></span>
