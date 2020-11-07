---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A65E82D5-706B-4470-A51E-936E381DA78F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmcustomscriptextension
schema: 2.0.0
ms.openlocfilehash: 70715c4bb4c3e5f805f297c8b68def0f5b3a0d6f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882282"
---
# <span data-ttu-id="d169c-101">Remove-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="d169c-101">Remove-AzureRmVMCustomScriptExtension</span></span>

## <span data-ttu-id="d169c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d169c-102">SYNOPSIS</span></span>
<span data-ttu-id="d169c-103">가상 머신에서 사용자 지정 스크립트 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d169c-103">Removes a custom script extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d169c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d169c-104">SYNTAX</span></span>

```
Remove-AzureRmVMCustomScriptExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d169c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d169c-105">DESCRIPTION</span></span>
<span data-ttu-id="d169c-106">**AzureRmVMCustomScriptExtension** cmdlet은 가상 머신에서 사용자 지정 스크립트 가상 컴퓨터 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="d169c-106">The **Remove-AzureRmVMCustomScriptExtension** cmdlet removes a custom script Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="d169c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d169c-107">EXAMPLES</span></span>

## <span data-ttu-id="d169c-108">변수</span><span class="sxs-lookup"><span data-stu-id="d169c-108">PARAMETERS</span></span>

### <span data-ttu-id="d169c-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d169c-109">-DefaultProfile</span></span>
<span data-ttu-id="d169c-110">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d169c-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d169c-111">-Force</span><span class="sxs-lookup"><span data-stu-id="d169c-111">-Force</span></span>
<span data-ttu-id="d169c-112">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d169c-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d169c-113">-이름</span><span class="sxs-lookup"><span data-stu-id="d169c-113">-Name</span></span>
<span data-ttu-id="d169c-114">이 cmdlet이 제거 하는 사용자 지정 스크립트 확장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d169c-114">Specifies the name of the custom script extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="d169c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d169c-115">-ResourceGroupName</span></span>
<span data-ttu-id="d169c-116">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d169c-116">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="d169c-117">-VMName</span><span class="sxs-lookup"><span data-stu-id="d169c-117">-VMName</span></span>
<span data-ttu-id="d169c-118">이 cmdlet이 사용자 지정 스크립트 확장을 제거 하는 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d169c-118">Specifies the name of a virtual machine from which this cmdlet removes the custom script extension.</span></span>

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

### <span data-ttu-id="d169c-119">-확인</span><span class="sxs-lookup"><span data-stu-id="d169c-119">-Confirm</span></span>
<span data-ttu-id="d169c-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d169c-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d169c-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d169c-121">-WhatIf</span></span>
<span data-ttu-id="d169c-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d169c-122">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="d169c-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d169c-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d169c-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d169c-124">CommonParameters</span></span>
<span data-ttu-id="d169c-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d169c-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d169c-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d169c-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d169c-127">입력</span><span class="sxs-lookup"><span data-stu-id="d169c-127">INPUTS</span></span>

### <span data-ttu-id="d169c-128">않아야</span><span class="sxs-lookup"><span data-stu-id="d169c-128">None</span></span>
<span data-ttu-id="d169c-129">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d169c-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d169c-130">출력</span><span class="sxs-lookup"><span data-stu-id="d169c-130">OUTPUTS</span></span>

### <span data-ttu-id="d169c-131">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="d169c-131">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="d169c-132">상속자</span><span class="sxs-lookup"><span data-stu-id="d169c-132">NOTES</span></span>

## <span data-ttu-id="d169c-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d169c-133">RELATED LINKS</span></span>

[<span data-ttu-id="d169c-134">Get-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="d169c-134">Get-AzureRmVMCustomScriptExtension</span></span>](./Get-AzureRmVMCustomScriptExtension.md)

[<span data-ttu-id="d169c-135">Set-AzureRmVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="d169c-135">Set-AzureRmVMCustomScriptExtension</span></span>](./Set-AzureRmVMCustomScriptExtension.md)
