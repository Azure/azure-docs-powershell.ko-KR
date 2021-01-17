---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 5F45A12C-BB50-4732-BE80-188491DEF8B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationModule.md
ms.openlocfilehash: 8d7e63ed8bc24f772afa84106592ede5f9da9250
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373255"
---
# <span data-ttu-id="8c05b-101">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="8c05b-101">Remove-AzAutomationModule</span></span>

## <span data-ttu-id="8c05b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c05b-102">SYNOPSIS</span></span>
<span data-ttu-id="8c05b-103">Automation에서 모듈을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="8c05b-103">Removes a module from Automation.</span></span>

## <span data-ttu-id="8c05b-104">구문</span><span class="sxs-lookup"><span data-stu-id="8c05b-104">SYNTAX</span></span>

```
Remove-AzAutomationModule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8c05b-105">설명</span><span class="sxs-lookup"><span data-stu-id="8c05b-105">DESCRIPTION</span></span>
<span data-ttu-id="8c05b-106">**Remove-AzAutomationModule** cmdlet은 Azure Automation의 Automation 계정에서 모듈을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="8c05b-106">The **Remove-AzAutomationModule** cmdlet removes a module from an Automation account in Azure Automation.</span></span>

## <span data-ttu-id="8c05b-107">예제</span><span class="sxs-lookup"><span data-stu-id="8c05b-107">EXAMPLES</span></span>

### <span data-ttu-id="8c05b-108">예제 1: 모듈 제거</span><span class="sxs-lookup"><span data-stu-id="8c05b-108">Example 1: Remove a module</span></span>
```
PS C:\>Remove-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="8c05b-109">이 명령은 Contoso17이라는 Automation 계정에서 ContosoModule이라는 모듈을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="8c05b-109">This command removes a module named ContosoModule from the Automation account named Contoso17.</span></span>

## <span data-ttu-id="8c05b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c05b-110">PARAMETERS</span></span>

### <span data-ttu-id="8c05b-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8c05b-111">-AutomationAccountName</span></span>
<span data-ttu-id="8c05b-112">이 cmdlet이 모듈을 제거하는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8c05b-112">Specifies the name of the Automation account from which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="8c05b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c05b-113">-DefaultProfile</span></span>
<span data-ttu-id="8c05b-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8c05b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8c05b-115">-Force</span><span class="sxs-lookup"><span data-stu-id="8c05b-115">-Force</span></span>
<span data-ttu-id="8c05b-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="8c05b-116">ps_force</span></span>

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

### <span data-ttu-id="8c05b-117">-Name</span><span class="sxs-lookup"><span data-stu-id="8c05b-117">-Name</span></span>
<span data-ttu-id="8c05b-118">이 cmdlet이 제거하는 모듈의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8c05b-118">Specifies the name of the module that this cmdlet removes.</span></span>

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

### <span data-ttu-id="8c05b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c05b-119">-ResourceGroupName</span></span>
<span data-ttu-id="8c05b-120">이 cmdlet이 모듈을 제거하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8c05b-120">Specifies the name of a resource group in which this cmdlet removes a module.</span></span>

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

### <span data-ttu-id="8c05b-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8c05b-121">-Confirm</span></span>
<span data-ttu-id="8c05b-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8c05b-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c05b-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c05b-123">-WhatIf</span></span>
<span data-ttu-id="8c05b-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="8c05b-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c05b-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8c05b-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c05b-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c05b-126">CommonParameters</span></span>
<span data-ttu-id="8c05b-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8c05b-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c05b-128">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8c05b-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c05b-129">입력</span><span class="sxs-lookup"><span data-stu-id="8c05b-129">INPUTS</span></span>

### <span data-ttu-id="8c05b-130">System.String</span><span class="sxs-lookup"><span data-stu-id="8c05b-130">System.String</span></span>

## <span data-ttu-id="8c05b-131">출력</span><span class="sxs-lookup"><span data-stu-id="8c05b-131">OUTPUTS</span></span>

### <span data-ttu-id="8c05b-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="8c05b-132">System.Void</span></span>

## <span data-ttu-id="8c05b-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8c05b-133">NOTES</span></span>

## <span data-ttu-id="8c05b-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8c05b-134">RELATED LINKS</span></span>

[<span data-ttu-id="8c05b-135">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="8c05b-135">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="8c05b-136">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="8c05b-136">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="8c05b-137">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="8c05b-137">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)


