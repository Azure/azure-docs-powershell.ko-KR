---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 16055879-C001-46E7-B8C3-1FE2A1A67AC4
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationRunbook.md
ms.openlocfilehash: a7dc06e4ddbeac224daf9b8a80be40d343514a18
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009888"
---
# <span data-ttu-id="7a8e0-101">Remove-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7a8e0-101">Remove-AzAutomationRunbook</span></span>

## <span data-ttu-id="7a8e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a8e0-102">SYNOPSIS</span></span>
<span data-ttu-id="7a8e0-103">Runbook을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7a8e0-103">Removes a runbook.</span></span>

## <span data-ttu-id="7a8e0-104">구문</span><span class="sxs-lookup"><span data-stu-id="7a8e0-104">SYNTAX</span></span>

```
Remove-AzAutomationRunbook [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7a8e0-105">설명</span><span class="sxs-lookup"><span data-stu-id="7a8e0-105">DESCRIPTION</span></span>
<span data-ttu-id="7a8e0-106">**Remove-AzAutomationRunbook** cmdlet은 Azure Automation에서 Runbook을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7a8e0-106">The **Remove-AzAutomationRunbook** cmdlet removes a runbook from Azure Automation.</span></span>

## <span data-ttu-id="7a8e0-107">예제</span><span class="sxs-lookup"><span data-stu-id="7a8e0-107">EXAMPLES</span></span>

### <span data-ttu-id="7a8e0-108">예제 1: Runbook 제거</span><span class="sxs-lookup"><span data-stu-id="7a8e0-108">Example 1: Remove a runbook</span></span>
```
PS C:\>Remove-AzAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook03" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="7a8e0-109">이 명령은 Contoso17이라는 Azure Automation 계정에서 Runbook03이라는 Runbook을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7a8e0-109">This command removes the runbook named Runbook03 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="7a8e0-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7a8e0-110">PARAMETERS</span></span>

### <span data-ttu-id="7a8e0-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7a8e0-111">-AutomationAccountName</span></span>
<span data-ttu-id="7a8e0-112">이 cmdlet에서 Runbook을 제거하는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7a8e0-112">Specifies the name of the Automation account in which this cmdlet removes a runbook.</span></span>

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

### <span data-ttu-id="7a8e0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a8e0-113">-DefaultProfile</span></span>
<span data-ttu-id="7a8e0-114">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7a8e0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7a8e0-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7a8e0-115">-Force</span></span>
<span data-ttu-id="7a8e0-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="7a8e0-116">ps_force</span></span>

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

### <span data-ttu-id="7a8e0-117">-Name</span><span class="sxs-lookup"><span data-stu-id="7a8e0-117">-Name</span></span>
<span data-ttu-id="7a8e0-118">이 cmdlet이 제거한 Runbook의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7a8e0-118">Specifies the name of the runbook that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7a8e0-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a8e0-119">-ResourceGroupName</span></span>
<span data-ttu-id="7a8e0-120">이 cmdlet에서 Runbook을 게시하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7a8e0-120">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="7a8e0-121">-확인</span><span class="sxs-lookup"><span data-stu-id="7a8e0-121">-Confirm</span></span>
<span data-ttu-id="7a8e0-122">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a8e0-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a8e0-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a8e0-123">-WhatIf</span></span>
<span data-ttu-id="7a8e0-124">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="7a8e0-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a8e0-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7a8e0-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a8e0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a8e0-126">CommonParameters</span></span>
<span data-ttu-id="7a8e0-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7a8e0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a8e0-128">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7a8e0-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a8e0-129">입력</span><span class="sxs-lookup"><span data-stu-id="7a8e0-129">INPUTS</span></span>

### <span data-ttu-id="7a8e0-130">System.String</span><span class="sxs-lookup"><span data-stu-id="7a8e0-130">System.String</span></span>

## <span data-ttu-id="7a8e0-131">출력</span><span class="sxs-lookup"><span data-stu-id="7a8e0-131">OUTPUTS</span></span>

### <span data-ttu-id="7a8e0-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="7a8e0-132">System.Void</span></span>

## <span data-ttu-id="7a8e0-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7a8e0-133">NOTES</span></span>

## <span data-ttu-id="7a8e0-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7a8e0-134">RELATED LINKS</span></span>

[<span data-ttu-id="7a8e0-135">Export-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7a8e0-135">Export-AzAutomationRunbook</span></span>](./Export-AzAutomationRunbook.md)

[<span data-ttu-id="7a8e0-136">Get-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7a8e0-136">Get-AzAutomationRunbook</span></span>](./Get-AzAutomationRunbook.md)

[<span data-ttu-id="7a8e0-137">Import-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7a8e0-137">Import-AzAutomationRunbook</span></span>](./Import-AzAutomationRunbook.md)

[<span data-ttu-id="7a8e0-138">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7a8e0-138">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="7a8e0-139">New-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7a8e0-139">New-AzAutomationRunbook</span></span>](./New-AzAutomationRunbook.md)

[<span data-ttu-id="7a8e0-140">Publish-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7a8e0-140">Publish-AzAutomationRunbook</span></span>](./Publish-AzAutomationRunbook.md)

[<span data-ttu-id="7a8e0-141">Set-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7a8e0-141">Set-AzAutomationRunbook</span></span>](./Set-AzAutomationRunbook.md)

[<span data-ttu-id="7a8e0-142">Start-AzAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="7a8e0-142">Start-AzAutomationRunbook</span></span>](./Start-AzAutomationRunbook.md)


