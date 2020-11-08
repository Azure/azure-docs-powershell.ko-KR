---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 6C40A7BA-6BE2-464A-84E4-9021935A5BF6
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMExtension.md
ms.openlocfilehash: 70495ee657e511aace4babf47959c4bd6841197c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056513"
---
# <span data-ttu-id="e470b-101">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="e470b-101">Remove-AzVMExtension</span></span>

## <span data-ttu-id="e470b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e470b-102">SYNOPSIS</span></span>
<span data-ttu-id="e470b-103">가상 컴퓨터에서 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e470b-103">Removes an extension from a virtual machine.</span></span>

## <span data-ttu-id="e470b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e470b-104">SYNTAX</span></span>

```
Remove-AzVMExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e470b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e470b-105">DESCRIPTION</span></span>
<span data-ttu-id="e470b-106">**AzVMExtension** cmdlet은 가상 컴퓨터의 가상 컴퓨터 확장에서 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e470b-106">The **Remove-AzVMExtension** cmdlet removes an extension from the Virtual Machine Extensions of a virtual machine.</span></span>

## <span data-ttu-id="e470b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e470b-107">EXAMPLES</span></span>

### <span data-ttu-id="e470b-108">예제 1: 가상 머신에서 확장 제거</span><span class="sxs-lookup"><span data-stu-id="e470b-108">Example 1: Remove an extension from a virtual machine</span></span>
```
PS C:\> Remove-AzVMExtension -ResourceGroupName "ResourceGroup11" -Name "ContosoTest" -VMName "VirtualMachine22"
```

<span data-ttu-id="e470b-109">이 명령은 ResourceGroup11의 VirtualMachine22 이라는 가상 컴퓨터에서 ContosoTest 이라는 확장명을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e470b-109">This command removes the extension named ContosoTest from the virtual machine named VirtualMachine22 in ResourceGroup11.</span></span>

## <span data-ttu-id="e470b-110">변수</span><span class="sxs-lookup"><span data-stu-id="e470b-110">PARAMETERS</span></span>

### <span data-ttu-id="e470b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e470b-111">-DefaultProfile</span></span>
<span data-ttu-id="e470b-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e470b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e470b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="e470b-113">-Force</span></span>
<span data-ttu-id="e470b-114">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="e470b-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e470b-115">-이름</span><span class="sxs-lookup"><span data-stu-id="e470b-115">-Name</span></span>
<span data-ttu-id="e470b-116">이 cmdlet이 제거 하는 확장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e470b-116">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="e470b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e470b-117">-ResourceGroupName</span></span>
<span data-ttu-id="e470b-118">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e470b-118">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="e470b-119">-VMName</span><span class="sxs-lookup"><span data-stu-id="e470b-119">-VMName</span></span>
<span data-ttu-id="e470b-120">이 cmdlet이 확장을 제거 하는 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e470b-120">Specifies the name of a virtual machine from which this cmdlet removes the extension.</span></span>

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

### <span data-ttu-id="e470b-121">-확인</span><span class="sxs-lookup"><span data-stu-id="e470b-121">-Confirm</span></span>
<span data-ttu-id="e470b-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e470b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e470b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e470b-123">-WhatIf</span></span>
<span data-ttu-id="e470b-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e470b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e470b-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e470b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e470b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e470b-126">CommonParameters</span></span>
<span data-ttu-id="e470b-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e470b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e470b-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e470b-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e470b-129">입력</span><span class="sxs-lookup"><span data-stu-id="e470b-129">INPUTS</span></span>

### <span data-ttu-id="e470b-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e470b-130">System.String</span></span>

## <span data-ttu-id="e470b-131">출력</span><span class="sxs-lookup"><span data-stu-id="e470b-131">OUTPUTS</span></span>

### <span data-ttu-id="e470b-132">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="e470b-132">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="e470b-133">상속자</span><span class="sxs-lookup"><span data-stu-id="e470b-133">NOTES</span></span>

## <span data-ttu-id="e470b-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e470b-134">RELATED LINKS</span></span>

[<span data-ttu-id="e470b-135">Get-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="e470b-135">Get-AzVMExtension</span></span>](./Get-AzVMExtension.md)

[<span data-ttu-id="e470b-136">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="e470b-136">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)


