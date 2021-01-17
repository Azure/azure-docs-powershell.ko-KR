---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 16055879-C001-46E7-B8C3-1FE2A1A67AC4
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
ms.openlocfilehash: d6ce3a737063763d77ed408072d275c52ee5884c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373234"
---
# <span data-ttu-id="0a01f-101">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0a01f-101">Remove-AzAutomationRunbook</span></span>

## <span data-ttu-id="0a01f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a01f-102">SYNOPSIS</span></span>
<span data-ttu-id="0a01f-103">Runbook을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0a01f-103">Removes a runbook.</span></span>

## <span data-ttu-id="0a01f-104">구문</span><span class="sxs-lookup"><span data-stu-id="0a01f-104">SYNTAX</span></span>

```
Remove-AzAutomationRunbook [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0a01f-105">설명</span><span class="sxs-lookup"><span data-stu-id="0a01f-105">DESCRIPTION</span></span>
<span data-ttu-id="0a01f-106">**Remove-AzAutomationRunbook** cmdlet은 Azure Automation에서 Runbook을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0a01f-106">The **Remove-AzAutomationRunbook** cmdlet removes a runbook from Azure Automation.</span></span>

## <span data-ttu-id="0a01f-107">예제</span><span class="sxs-lookup"><span data-stu-id="0a01f-107">EXAMPLES</span></span>

### <span data-ttu-id="0a01f-108">예제 1: Runbook 제거</span><span class="sxs-lookup"><span data-stu-id="0a01f-108">Example 1: Remove a runbook</span></span>
```
PS C:\>Remove-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook03" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="0a01f-109">이 명령은 Contoso17이라는 Azure Automation 계정에서 Runbook03이라는 Runbook을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0a01f-109">This command removes the runbook named Runbook03 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="0a01f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a01f-110">PARAMETERS</span></span>

### <span data-ttu-id="0a01f-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0a01f-111">-AutomationAccountName</span></span>
<span data-ttu-id="0a01f-112">이 cmdlet이 Runbook을 제거하는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0a01f-112">Specifies the name of the Automation account in which this cmdlet removes a runbook.</span></span>

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

### <span data-ttu-id="0a01f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a01f-113">-DefaultProfile</span></span>
<span data-ttu-id="0a01f-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0a01f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0a01f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="0a01f-115">-Force</span></span>
<span data-ttu-id="0a01f-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="0a01f-116">ps_force</span></span>

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

### <span data-ttu-id="0a01f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="0a01f-117">-Name</span></span>
<span data-ttu-id="0a01f-118">이 cmdlet이 제거하는 Runbook의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0a01f-118">Specifies the name of the runbook that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a01f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a01f-119">-ResourceGroupName</span></span>
<span data-ttu-id="0a01f-120">이 cmdlet이 Runbook을 게시하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0a01f-120">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="0a01f-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0a01f-121">-Confirm</span></span>
<span data-ttu-id="0a01f-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0a01f-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a01f-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a01f-123">-WhatIf</span></span>
<span data-ttu-id="0a01f-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="0a01f-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a01f-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0a01f-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a01f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a01f-126">CommonParameters</span></span>
<span data-ttu-id="0a01f-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0a01f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a01f-128">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0a01f-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a01f-129">입력</span><span class="sxs-lookup"><span data-stu-id="0a01f-129">INPUTS</span></span>

### <span data-ttu-id="0a01f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="0a01f-130">System.String</span></span>

## <span data-ttu-id="0a01f-131">출력</span><span class="sxs-lookup"><span data-stu-id="0a01f-131">OUTPUTS</span></span>

### <span data-ttu-id="0a01f-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="0a01f-132">System.Void</span></span>

## <span data-ttu-id="0a01f-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0a01f-133">NOTES</span></span>

## <span data-ttu-id="0a01f-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0a01f-134">RELATED LINKS</span></span>

[<span data-ttu-id="0a01f-135">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0a01f-135">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="0a01f-136">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0a01f-136">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="0a01f-137">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0a01f-137">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="0a01f-138">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0a01f-138">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="0a01f-139">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0a01f-139">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="0a01f-140">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0a01f-140">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="0a01f-141">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0a01f-141">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="0a01f-142">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="0a01f-142">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


