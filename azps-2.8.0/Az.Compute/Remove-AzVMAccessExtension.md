---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 22C490C2-0135-4375-897E-7224DBBE13A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAccessExtension.md
ms.openlocfilehash: 1fececa1c7d40e8ea2667ecd6461740a6714d744
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697305"
---
# <span data-ttu-id="ea092-101">Remove-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="ea092-101">Remove-AzVMAccessExtension</span></span>

## <span data-ttu-id="ea092-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea092-102">SYNOPSIS</span></span>
<span data-ttu-id="ea092-103">가상 머신에서 VMAccess 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea092-103">Removes the VMAccess extension from a virtual machine.</span></span>

## <span data-ttu-id="ea092-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ea092-104">SYNTAX</span></span>

```
Remove-AzVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea092-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ea092-105">DESCRIPTION</span></span>
<span data-ttu-id="ea092-106">**AzVMAccessExtension** cmdlet은 가상 컴퓨터에서 vmaccess (Virtual machine Access) 가상 컴퓨터 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea092-106">The **Remove-AzVMAccessExtension** cmdlet removes the Virtual Machine Access (VMAccess) Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="ea092-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ea092-107">EXAMPLES</span></span>

## <span data-ttu-id="ea092-108">변수</span><span class="sxs-lookup"><span data-stu-id="ea092-108">PARAMETERS</span></span>

### <span data-ttu-id="ea092-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea092-109">-DefaultProfile</span></span>
<span data-ttu-id="ea092-110">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ea092-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea092-111">-Force</span><span class="sxs-lookup"><span data-stu-id="ea092-111">-Force</span></span>
<span data-ttu-id="ea092-112">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea092-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ea092-113">-이름</span><span class="sxs-lookup"><span data-stu-id="ea092-113">-Name</span></span>
<span data-ttu-id="ea092-114">이 cmdlet이 제거 하는 확장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea092-114">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ea092-115">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ea092-115">-NoWait</span></span>
<span data-ttu-id="ea092-116">작업이 완료 되기 전에 작업을 시작 하 고 즉시 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea092-116">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="ea092-117">작업이 성공적으로 완료 되었는지 확인 하려면 다른 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea092-117">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="ea092-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea092-118">-ResourceGroupName</span></span>
<span data-ttu-id="ea092-119">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea092-119">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="ea092-120">-VMName</span><span class="sxs-lookup"><span data-stu-id="ea092-120">-VMName</span></span>
<span data-ttu-id="ea092-121">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea092-121">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="ea092-122">이 cmdlet은이 매개 변수에서 지정 하는 가상 컴퓨터에 대 한 VMAccess를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea092-122">This cmdlet removes VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="ea092-123">-확인</span><span class="sxs-lookup"><span data-stu-id="ea092-123">-Confirm</span></span>
<span data-ttu-id="ea092-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea092-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea092-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea092-125">-WhatIf</span></span>
<span data-ttu-id="ea092-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ea092-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea092-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ea092-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea092-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea092-128">CommonParameters</span></span>
<span data-ttu-id="ea092-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ea092-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea092-130">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ea092-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea092-131">입력</span><span class="sxs-lookup"><span data-stu-id="ea092-131">INPUTS</span></span>

### <span data-ttu-id="ea092-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ea092-132">System.String</span></span>

## <span data-ttu-id="ea092-133">출력</span><span class="sxs-lookup"><span data-stu-id="ea092-133">OUTPUTS</span></span>

### <span data-ttu-id="ea092-134">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="ea092-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="ea092-135">상속자</span><span class="sxs-lookup"><span data-stu-id="ea092-135">NOTES</span></span>

## <span data-ttu-id="ea092-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ea092-136">RELATED LINKS</span></span>

[<span data-ttu-id="ea092-137">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="ea092-137">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="ea092-138">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="ea092-138">Set-AzVMAccessExtension</span></span>](./Set-AzVMAccessExtension.md)

[<span data-ttu-id="ea092-139">제거-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="ea092-139">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)
