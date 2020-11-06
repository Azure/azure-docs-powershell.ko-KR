---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: A65E82D5-706B-4470-A51E-936E381DA78F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMCustomScriptExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmVMCustomScriptExtension.md
ms.openlocfilehash: 1e2dc6fe56cfaf182fb0614121ad9511edcfc2fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529896"
---
# <span data-ttu-id="b0b7e-101">Remove-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="b0b7e-101">Remove-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="b0b7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0b7e-102">SYNOPSIS</span></span>
<span data-ttu-id="b0b7e-103">가상 머신에서 사용자 지정 스크립트 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0b7e-103">Removes a custom script extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0b7e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b0b7e-104">SYNTAX</span></span>

```
Remove-AzureRmVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0b7e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b0b7e-105">DESCRIPTION</span></span>
<span data-ttu-id="b0b7e-106">**AzureRmVMCustomScriptExtension** cmdlet은 가상 머신에서 사용자 지정 스크립트 가상 컴퓨터 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0b7e-106">The **Remove-AzureRmVMCustomScriptExtension** cmdlet removes a custom script Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="b0b7e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b0b7e-107">EXAMPLES</span></span>

## <span data-ttu-id="b0b7e-108">변수</span><span class="sxs-lookup"><span data-stu-id="b0b7e-108">PARAMETERS</span></span>

### <span data-ttu-id="b0b7e-109">-Force</span><span class="sxs-lookup"><span data-stu-id="b0b7e-109">-Force</span></span>
<span data-ttu-id="b0b7e-110">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0b7e-110">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b0b7e-111">-이름</span><span class="sxs-lookup"><span data-stu-id="b0b7e-111">-Name</span></span>
<span data-ttu-id="b0b7e-112">이 cmdlet이 제거 하는 사용자 지정 스크립트 확장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0b7e-112">Specifies the name of the custom script extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="b0b7e-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0b7e-113">-ResourceGroupName</span></span>
<span data-ttu-id="b0b7e-114">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0b7e-114">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="b0b7e-115">-VMName</span><span class="sxs-lookup"><span data-stu-id="b0b7e-115">-VMName</span></span>
<span data-ttu-id="b0b7e-116">이 cmdlet이 사용자 지정 스크립트 확장을 제거 하는 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0b7e-116">Specifies the name of a virtual machine from which this cmdlet removes the custom script extension.</span></span>

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

### <span data-ttu-id="b0b7e-117">-확인</span><span class="sxs-lookup"><span data-stu-id="b0b7e-117">-Confirm</span></span>
<span data-ttu-id="b0b7e-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0b7e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0b7e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0b7e-119">-WhatIf</span></span>
<span data-ttu-id="b0b7e-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b0b7e-120">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="b0b7e-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b0b7e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0b7e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0b7e-122">CommonParameters</span></span>
<span data-ttu-id="b0b7e-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0b7e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0b7e-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0b7e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0b7e-125">입력</span><span class="sxs-lookup"><span data-stu-id="b0b7e-125">INPUTS</span></span>

### <span data-ttu-id="b0b7e-126">않아야</span><span class="sxs-lookup"><span data-stu-id="b0b7e-126">None</span></span>
<span data-ttu-id="b0b7e-127">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b0b7e-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b0b7e-128">출력</span><span class="sxs-lookup"><span data-stu-id="b0b7e-128">OUTPUTS</span></span>

## <span data-ttu-id="b0b7e-129">상속자</span><span class="sxs-lookup"><span data-stu-id="b0b7e-129">NOTES</span></span>

## <span data-ttu-id="b0b7e-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b0b7e-130">RELATED LINKS</span></span>

[<span data-ttu-id="b0b7e-131">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="b0b7e-131">Get-AzureRmVMCustomScriptExtension</span></span>](./Get-AzureRmVMCustomScriptExtension.md)

[<span data-ttu-id="b0b7e-132">Set-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="b0b7e-132">Set-AzureRmVMCustomScriptExtension</span></span>](./Set-AzureRmVMCustomScriptExtension.md)
