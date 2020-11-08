---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A65E82D5-706B-4470-A51E-936E381DA78F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMCustomScriptExtension.md
ms.openlocfilehash: 48e2a48eab4a75634f8868b2f25e435faf3de496
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042108"
---
# <span data-ttu-id="2347d-101">Remove-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="2347d-101">Remove-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="2347d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2347d-102">SYNOPSIS</span></span>
<span data-ttu-id="2347d-103">가상 머신에서 사용자 지정 스크립트 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2347d-103">Removes a custom script extension from a virtual machine.</span></span>

## <span data-ttu-id="2347d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2347d-104">SYNTAX</span></span>

```
Remove-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2347d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2347d-105">DESCRIPTION</span></span>
<span data-ttu-id="2347d-106">**AzVMCustomScriptExtension** cmdlet은 가상 머신에서 사용자 지정 스크립트 가상 컴퓨터 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2347d-106">The **Remove-AzVMCustomScriptExtension** cmdlet removes a custom script Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="2347d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2347d-107">EXAMPLES</span></span>

## <span data-ttu-id="2347d-108">변수</span><span class="sxs-lookup"><span data-stu-id="2347d-108">PARAMETERS</span></span>

### <span data-ttu-id="2347d-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2347d-109">-DefaultProfile</span></span>
<span data-ttu-id="2347d-110">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2347d-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2347d-111">-Force</span><span class="sxs-lookup"><span data-stu-id="2347d-111">-Force</span></span>
<span data-ttu-id="2347d-112">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="2347d-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2347d-113">-이름</span><span class="sxs-lookup"><span data-stu-id="2347d-113">-Name</span></span>
<span data-ttu-id="2347d-114">이 cmdlet이 제거 하는 사용자 지정 스크립트 확장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2347d-114">Specifies the name of the custom script extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="2347d-115">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2347d-115">-NoWait</span></span>
<span data-ttu-id="2347d-116">작업이 완료 되기 전에 작업을 시작 하 고 즉시 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2347d-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="2347d-117">작업이 성공적으로 완료 되었는지 확인 하려면 다른 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2347d-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="2347d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2347d-118">-ResourceGroupName</span></span>
<span data-ttu-id="2347d-119">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2347d-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="2347d-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="2347d-120">-VMName</span></span>
<span data-ttu-id="2347d-121">이 cmdlet이 사용자 지정 스크립트 확장을 제거 하는 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2347d-121">Specifies the name of a virtual machine from which this cmdlet removes the custom script extension.</span></span>

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

### <span data-ttu-id="2347d-122">-확인</span><span class="sxs-lookup"><span data-stu-id="2347d-122">-Confirm</span></span>
<span data-ttu-id="2347d-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2347d-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2347d-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2347d-124">-WhatIf</span></span>
<span data-ttu-id="2347d-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2347d-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2347d-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2347d-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2347d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2347d-127">CommonParameters</span></span>
<span data-ttu-id="2347d-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2347d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2347d-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2347d-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2347d-130">입력</span><span class="sxs-lookup"><span data-stu-id="2347d-130">INPUTS</span></span>

### <span data-ttu-id="2347d-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2347d-131">System.String</span></span>

## <span data-ttu-id="2347d-132">출력</span><span class="sxs-lookup"><span data-stu-id="2347d-132">OUTPUTS</span></span>

### <span data-ttu-id="2347d-133">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="2347d-133">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="2347d-134">상속자</span><span class="sxs-lookup"><span data-stu-id="2347d-134">NOTES</span></span>

## <span data-ttu-id="2347d-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2347d-135">RELATED LINKS</span></span>

[<span data-ttu-id="2347d-136">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="2347d-136">Get-AzVMCustomScriptExtension</span></span>](./Get-AzVMCustomScriptExtension.md)

[<span data-ttu-id="2347d-137">Set-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="2347d-137">Set-AzVMCustomScriptExtension</span></span>](./Set-AzVMCustomScriptExtension.md)
