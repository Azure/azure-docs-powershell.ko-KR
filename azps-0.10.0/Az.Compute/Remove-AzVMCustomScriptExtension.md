---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: A65E82D5-706B-4470-A51E-936E381DA78F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmcustomscriptextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVMCustomScriptExtension.md
ms.openlocfilehash: 8bead12111148d193e0e5dfe880ed3b28c6dcd01
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876956"
---
# <span data-ttu-id="42495-101">Remove-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="42495-101">Remove-AzVMCustomScriptExtension</span></span>

## <span data-ttu-id="42495-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42495-102">SYNOPSIS</span></span>
<span data-ttu-id="42495-103">가상 머신에서 사용자 지정 스크립트 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="42495-103">Removes a custom script extension from a virtual machine.</span></span>

## <span data-ttu-id="42495-104">구문과</span><span class="sxs-lookup"><span data-stu-id="42495-104">SYNTAX</span></span>

```
Remove-AzVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42495-105">설명은</span><span class="sxs-lookup"><span data-stu-id="42495-105">DESCRIPTION</span></span>
<span data-ttu-id="42495-106">**AzVMCustomScriptExtension** cmdlet은 가상 머신에서 사용자 지정 스크립트 가상 컴퓨터 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="42495-106">The **Remove-AzVMCustomScriptExtension** cmdlet removes a custom script Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="42495-107">예제의</span><span class="sxs-lookup"><span data-stu-id="42495-107">EXAMPLES</span></span>

## <span data-ttu-id="42495-108">변수</span><span class="sxs-lookup"><span data-stu-id="42495-108">PARAMETERS</span></span>

### <span data-ttu-id="42495-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42495-109">-DefaultProfile</span></span>
<span data-ttu-id="42495-110">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="42495-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42495-111">-Force</span><span class="sxs-lookup"><span data-stu-id="42495-111">-Force</span></span>
<span data-ttu-id="42495-112">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="42495-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42495-113">-이름</span><span class="sxs-lookup"><span data-stu-id="42495-113">-Name</span></span>
<span data-ttu-id="42495-114">이 cmdlet이 제거 하는 사용자 지정 스크립트 확장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="42495-114">Specifies the name of the custom script extension that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42495-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42495-115">-ResourceGroupName</span></span>
<span data-ttu-id="42495-116">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="42495-116">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42495-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="42495-117">-VMName</span></span>
<span data-ttu-id="42495-118">이 cmdlet이 사용자 지정 스크립트 확장을 제거 하는 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="42495-118">Specifies the name of a virtual machine from which this cmdlet removes the custom script extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42495-119">-확인</span><span class="sxs-lookup"><span data-stu-id="42495-119">-Confirm</span></span>
<span data-ttu-id="42495-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="42495-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42495-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42495-121">-WhatIf</span></span>
<span data-ttu-id="42495-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="42495-122">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="42495-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="42495-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42495-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42495-124">CommonParameters</span></span>
<span data-ttu-id="42495-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="42495-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42495-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42495-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42495-127">입력</span><span class="sxs-lookup"><span data-stu-id="42495-127">INPUTS</span></span>

### <span data-ttu-id="42495-128">않아야</span><span class="sxs-lookup"><span data-stu-id="42495-128">None</span></span>
<span data-ttu-id="42495-129">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="42495-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="42495-130">출력</span><span class="sxs-lookup"><span data-stu-id="42495-130">OUTPUTS</span></span>

### <span data-ttu-id="42495-131">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="42495-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="42495-132">상속자</span><span class="sxs-lookup"><span data-stu-id="42495-132">NOTES</span></span>

## <span data-ttu-id="42495-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="42495-133">RELATED LINKS</span></span>

[<span data-ttu-id="42495-134">Get-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="42495-134">Get-AzVMCustomScriptExtension</span></span>](./Get-AzVMCustomScriptExtension.md)

[<span data-ttu-id="42495-135">Set-AzVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="42495-135">Set-AzVMCustomScriptExtension</span></span>](./Set-AzVMCustomScriptExtension.md)
