---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A65E82D5-706B-4470-A51E-936E381DA78F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMCustomScriptExtension.md
ms.openlocfilehash: 83041e17a930ee63c17f68d6ce8ce2797a25318c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701282"
---
# <span data-ttu-id="910dd-101">Remove-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="910dd-101">Remove-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="910dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="910dd-102">SYNOPSIS</span></span>
<span data-ttu-id="910dd-103">가상 머신에서 사용자 지정 스크립트 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="910dd-103">Removes a custom script extension from a virtual machine.</span></span>

## <span data-ttu-id="910dd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="910dd-104">SYNTAX</span></span>

```
Remove-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="910dd-105">설명은</span><span class="sxs-lookup"><span data-stu-id="910dd-105">DESCRIPTION</span></span>
<span data-ttu-id="910dd-106">**AzVMCustomScriptExtension** cmdlet은 가상 머신에서 사용자 지정 스크립트 가상 컴퓨터 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="910dd-106">The **Remove-AzVMCustomScriptExtension** cmdlet removes a custom script Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="910dd-107">예제의</span><span class="sxs-lookup"><span data-stu-id="910dd-107">EXAMPLES</span></span>

## <span data-ttu-id="910dd-108">변수</span><span class="sxs-lookup"><span data-stu-id="910dd-108">PARAMETERS</span></span>

### <span data-ttu-id="910dd-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="910dd-109">-DefaultProfile</span></span>
<span data-ttu-id="910dd-110">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="910dd-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="910dd-111">-Force</span><span class="sxs-lookup"><span data-stu-id="910dd-111">-Force</span></span>
<span data-ttu-id="910dd-112">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="910dd-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="910dd-113">-이름</span><span class="sxs-lookup"><span data-stu-id="910dd-113">-Name</span></span>
<span data-ttu-id="910dd-114">이 cmdlet이 제거 하는 사용자 지정 스크립트 확장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="910dd-114">Specifies the name of the custom script extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="910dd-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="910dd-115">-ResourceGroupName</span></span>
<span data-ttu-id="910dd-116">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="910dd-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="910dd-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="910dd-117">-VMName</span></span>
<span data-ttu-id="910dd-118">이 cmdlet이 사용자 지정 스크립트 확장을 제거 하는 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="910dd-118">Specifies the name of a virtual machine from which this cmdlet removes the custom script extension.</span></span>

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

### <span data-ttu-id="910dd-119">-확인</span><span class="sxs-lookup"><span data-stu-id="910dd-119">-Confirm</span></span>
<span data-ttu-id="910dd-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="910dd-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="910dd-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="910dd-121">-WhatIf</span></span>
<span data-ttu-id="910dd-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="910dd-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="910dd-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="910dd-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="910dd-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="910dd-124">CommonParameters</span></span>
<span data-ttu-id="910dd-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="910dd-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="910dd-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="910dd-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="910dd-127">입력</span><span class="sxs-lookup"><span data-stu-id="910dd-127">INPUTS</span></span>

### <span data-ttu-id="910dd-128">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="910dd-128">System.String</span></span>

## <span data-ttu-id="910dd-129">출력</span><span class="sxs-lookup"><span data-stu-id="910dd-129">OUTPUTS</span></span>

### <span data-ttu-id="910dd-130">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="910dd-130">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="910dd-131">상속자</span><span class="sxs-lookup"><span data-stu-id="910dd-131">NOTES</span></span>

## <span data-ttu-id="910dd-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="910dd-132">RELATED LINKS</span></span>

[<span data-ttu-id="910dd-133">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="910dd-133">Get-AzVMCustomScriptExtension</span></span>](./Get-AzVMCustomScriptExtension.md)

[<span data-ttu-id="910dd-134">Set-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="910dd-134">Set-AzVMCustomScriptExtension</span></span>](./Set-AzVMCustomScriptExtension.md)
