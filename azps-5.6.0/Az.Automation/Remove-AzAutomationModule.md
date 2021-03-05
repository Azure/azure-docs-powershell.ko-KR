---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 5F45A12C-BB50-4732-BE80-188491DEF8B5
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationModule.md
ms.openlocfilehash: 9fa84ffed6352dfb566ad02aa2393a7cba7f393b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009899"
---
# <span data-ttu-id="1341a-101">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="1341a-101">Remove-AzAutomationModule</span></span>

## <span data-ttu-id="1341a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1341a-102">SYNOPSIS</span></span>
<span data-ttu-id="1341a-103">Automation에서 모듈을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1341a-103">Removes a module from Automation.</span></span>

## <span data-ttu-id="1341a-104">구문</span><span class="sxs-lookup"><span data-stu-id="1341a-104">SYNTAX</span></span>

```
Remove-AzAutomationModule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1341a-105">설명</span><span class="sxs-lookup"><span data-stu-id="1341a-105">DESCRIPTION</span></span>
<span data-ttu-id="1341a-106">**Remove-AzAutomationModule** cmdlet은 Azure Automation의 Automation 계정에서 모듈을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1341a-106">The **Remove-AzAutomationModule** cmdlet removes a module from an Automation account in Azure Automation.</span></span>

## <span data-ttu-id="1341a-107">예제</span><span class="sxs-lookup"><span data-stu-id="1341a-107">EXAMPLES</span></span>

### <span data-ttu-id="1341a-108">예제 1: 모듈 제거</span><span class="sxs-lookup"><span data-stu-id="1341a-108">Example 1: Remove a module</span></span>
```
PS C:\>Remove-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="1341a-109">이 명령은 Contoso17이라는 Automation 계정에서 ContosoModule이라는 모듈을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1341a-109">This command removes a module named ContosoModule from the Automation account named Contoso17.</span></span>

## <span data-ttu-id="1341a-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="1341a-110">PARAMETERS</span></span>

### <span data-ttu-id="1341a-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1341a-111">-AutomationAccountName</span></span>
<span data-ttu-id="1341a-112">이 cmdlet에서 모듈을 제거하는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1341a-112">Specifies the name of the Automation account from which this cmdlet removes a module.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1341a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1341a-113">-DefaultProfile</span></span>
<span data-ttu-id="1341a-114">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="1341a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1341a-115">-Force</span><span class="sxs-lookup"><span data-stu-id="1341a-115">-Force</span></span>
<span data-ttu-id="1341a-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="1341a-116">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1341a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="1341a-117">-Name</span></span>
<span data-ttu-id="1341a-118">이 cmdlet이 제거한 모듈의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1341a-118">Specifies the name of the module that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1341a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1341a-119">-ResourceGroupName</span></span>
<span data-ttu-id="1341a-120">이 cmdlet에서 모듈을 제거하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1341a-120">Specifies the name of a resource group in which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="1341a-121">-확인</span><span class="sxs-lookup"><span data-stu-id="1341a-121">-Confirm</span></span>
<span data-ttu-id="1341a-122">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1341a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1341a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1341a-123">-WhatIf</span></span>
<span data-ttu-id="1341a-124">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="1341a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1341a-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1341a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1341a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1341a-126">CommonParameters</span></span>
<span data-ttu-id="1341a-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1341a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1341a-128">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1341a-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1341a-129">입력</span><span class="sxs-lookup"><span data-stu-id="1341a-129">INPUTS</span></span>

### <span data-ttu-id="1341a-130">System.String</span><span class="sxs-lookup"><span data-stu-id="1341a-130">System.String</span></span>

## <span data-ttu-id="1341a-131">출력</span><span class="sxs-lookup"><span data-stu-id="1341a-131">OUTPUTS</span></span>

### <span data-ttu-id="1341a-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="1341a-132">System.Void</span></span>

## <span data-ttu-id="1341a-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1341a-133">NOTES</span></span>

## <span data-ttu-id="1341a-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1341a-134">RELATED LINKS</span></span>

[<span data-ttu-id="1341a-135">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="1341a-135">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="1341a-136">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="1341a-136">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="1341a-137">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="1341a-137">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)


