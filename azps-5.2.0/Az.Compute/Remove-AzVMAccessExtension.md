---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 22C490C2-0135-4375-897E-7224DBBE13A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMAccessExtension.md
ms.openlocfilehash: 0810ff6b9551c5ef891180397b9cf04c9f6a8b06
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363854"
---
# <span data-ttu-id="1ad52-101">Remove-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="1ad52-101">Remove-AzVMAccessExtension</span></span>

## <span data-ttu-id="1ad52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ad52-102">SYNOPSIS</span></span>
<span data-ttu-id="1ad52-103">가상 머신에서 VMAccess 확장을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1ad52-103">Removes the VMAccess extension from a virtual machine.</span></span>

## <span data-ttu-id="1ad52-104">구문</span><span class="sxs-lookup"><span data-stu-id="1ad52-104">SYNTAX</span></span>

```
Remove-AzVMAccessExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String> [-Force] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ad52-105">설명</span><span class="sxs-lookup"><span data-stu-id="1ad52-105">DESCRIPTION</span></span>
<span data-ttu-id="1ad52-106">**Remove-AzVMAccessExtension** cmdlet은 가상 머신에서 VMAccess(Virtual Machine Access) Virtual Machine 확장을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1ad52-106">The **Remove-AzVMAccessExtension** cmdlet removes the Virtual Machine Access (VMAccess) Virtual Machine Extension from a virtual machine.</span></span>

## <span data-ttu-id="1ad52-107">예제</span><span class="sxs-lookup"><span data-stu-id="1ad52-107">EXAMPLES</span></span>

### <span data-ttu-id="1ad52-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="1ad52-108">Example 1</span></span>

<span data-ttu-id="1ad52-109">가상 머신에서 VMAccess 확장을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1ad52-109">Removes the VMAccess extension from a virtual machine.</span></span> <span data-ttu-id="1ad52-110">(자동Generated)</span><span class="sxs-lookup"><span data-stu-id="1ad52-110">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Remove-AzVMAccessExtension -Name 'AgentPool01' -ResourceGroupName myresourcegroup -VMName 'VM01'
```

## <span data-ttu-id="1ad52-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1ad52-111">PARAMETERS</span></span>

### <span data-ttu-id="1ad52-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ad52-112">-DefaultProfile</span></span>
<span data-ttu-id="1ad52-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1ad52-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1ad52-114">-Force</span><span class="sxs-lookup"><span data-stu-id="1ad52-114">-Force</span></span>
<span data-ttu-id="1ad52-115">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="1ad52-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="1ad52-116">-Name</span><span class="sxs-lookup"><span data-stu-id="1ad52-116">-Name</span></span>
<span data-ttu-id="1ad52-117">이 cmdlet이 제거하는 확장의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1ad52-117">Specifies the name of the extension that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1ad52-118">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1ad52-118">-NoWait</span></span>
<span data-ttu-id="1ad52-119">작업을 시작하고 작업이 완료되기 전에 즉시 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="1ad52-119">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="1ad52-120">작업이 성공적으로 완료됐는지 확인하기 위해 다른 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1ad52-120">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="1ad52-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ad52-121">-ResourceGroupName</span></span>
<span data-ttu-id="1ad52-122">가상 머신의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1ad52-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="1ad52-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="1ad52-123">-VMName</span></span>
<span data-ttu-id="1ad52-124">가상 머신의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1ad52-124">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="1ad52-125">이 cmdlet은 이 매개 변수가 지정하는 가상 머신에 대한 VMAccess를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1ad52-125">This cmdlet removes VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="1ad52-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1ad52-126">-Confirm</span></span>
<span data-ttu-id="1ad52-127">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1ad52-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ad52-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ad52-128">-WhatIf</span></span>
<span data-ttu-id="1ad52-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1ad52-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ad52-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1ad52-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ad52-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ad52-131">CommonParameters</span></span>
<span data-ttu-id="1ad52-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1ad52-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ad52-133">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1ad52-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ad52-134">입력</span><span class="sxs-lookup"><span data-stu-id="1ad52-134">INPUTS</span></span>

### <span data-ttu-id="1ad52-135">System.String</span><span class="sxs-lookup"><span data-stu-id="1ad52-135">System.String</span></span>

## <span data-ttu-id="1ad52-136">출력</span><span class="sxs-lookup"><span data-stu-id="1ad52-136">OUTPUTS</span></span>

### <span data-ttu-id="1ad52-137">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="1ad52-137">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="1ad52-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1ad52-138">NOTES</span></span>

## <span data-ttu-id="1ad52-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1ad52-139">RELATED LINKS</span></span>

[<span data-ttu-id="1ad52-140">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="1ad52-140">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="1ad52-141">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="1ad52-141">Set-AzVMAccessExtension</span></span>](./Set-AzVMAccessExtension.md)

[<span data-ttu-id="1ad52-142">Remove-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="1ad52-142">Remove-AzVMExtension</span></span>](./Remove-AzVMExtension.md)