---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EAD39EE1-C66F-4092-8876-E7F9FA612481
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationSchedule.md
ms.openlocfilehash: 0c37c33b60d430bc1782254401033934552f5663
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373227"
---
# <span data-ttu-id="fa7e6-101">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="fa7e6-101">Remove-AzAutomationSchedule</span></span>

## <span data-ttu-id="fa7e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa7e6-102">SYNOPSIS</span></span>
<span data-ttu-id="fa7e6-103">Automation 일정을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="fa7e6-103">Deletes an Automation schedule.</span></span>

## <span data-ttu-id="fa7e6-104">구문</span><span class="sxs-lookup"><span data-stu-id="fa7e6-104">SYNTAX</span></span>

```
Remove-AzAutomationSchedule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fa7e6-105">설명</span><span class="sxs-lookup"><span data-stu-id="fa7e6-105">DESCRIPTION</span></span>
<span data-ttu-id="fa7e6-106">**Remove-AzAutomationSchedule** cmdlet은 Azure Automation에서 일정을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="fa7e6-106">The **Remove-AzAutomationSchedule** cmdlet deletes a schedule from Azure Automation.</span></span>

## <span data-ttu-id="fa7e6-107">예제</span><span class="sxs-lookup"><span data-stu-id="fa7e6-107">EXAMPLES</span></span>

### <span data-ttu-id="fa7e6-108">예제 1: 일정 제거</span><span class="sxs-lookup"><span data-stu-id="fa7e6-108">Example 1: Remove a schedule</span></span>
```
PS C:\>Remove-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="fa7e6-109">이 명령은 리소스 그룹 ResourceGroup01의 Automation 계정 Contoso17에서 Schedule01이라는 일정을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="fa7e6-109">This command deletes the schedule named Schedule01 in automation account Contoso17 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="fa7e6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa7e6-110">PARAMETERS</span></span>

### <span data-ttu-id="fa7e6-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="fa7e6-111">-AutomationAccountName</span></span>
<span data-ttu-id="fa7e6-112">이 cmdlet이 일정을 제거하는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fa7e6-112">Specifies the name of an Automation account for which this cmdlet removes a schedule.</span></span>

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

### <span data-ttu-id="fa7e6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa7e6-113">-DefaultProfile</span></span>
<span data-ttu-id="fa7e6-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="fa7e6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fa7e6-115">-Force</span><span class="sxs-lookup"><span data-stu-id="fa7e6-115">-Force</span></span>
<span data-ttu-id="fa7e6-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="fa7e6-116">ps_force</span></span>

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

### <span data-ttu-id="fa7e6-117">-Name</span><span class="sxs-lookup"><span data-stu-id="fa7e6-117">-Name</span></span>
<span data-ttu-id="fa7e6-118">이 cmdlet이 제거하는 일정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fa7e6-118">Specifies the name for the schedule that this cmdlet removes.</span></span>

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

### <span data-ttu-id="fa7e6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa7e6-119">-ResourceGroupName</span></span>
<span data-ttu-id="fa7e6-120">이 cmdlet이 일정을 제거하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fa7e6-120">Specifies the name of a resource group for which this cmdlet removes a schedule.</span></span>

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

### <span data-ttu-id="fa7e6-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fa7e6-121">-Confirm</span></span>
<span data-ttu-id="fa7e6-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fa7e6-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa7e6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa7e6-123">-WhatIf</span></span>
<span data-ttu-id="fa7e6-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="fa7e6-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa7e6-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fa7e6-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa7e6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa7e6-126">CommonParameters</span></span>
<span data-ttu-id="fa7e6-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fa7e6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa7e6-128">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fa7e6-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa7e6-129">입력</span><span class="sxs-lookup"><span data-stu-id="fa7e6-129">INPUTS</span></span>

### <span data-ttu-id="fa7e6-130">System.String</span><span class="sxs-lookup"><span data-stu-id="fa7e6-130">System.String</span></span>

## <span data-ttu-id="fa7e6-131">출력</span><span class="sxs-lookup"><span data-stu-id="fa7e6-131">OUTPUTS</span></span>

### <span data-ttu-id="fa7e6-132">System.Void</span><span class="sxs-lookup"><span data-stu-id="fa7e6-132">System.Void</span></span>

## <span data-ttu-id="fa7e6-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fa7e6-133">NOTES</span></span>

## <span data-ttu-id="fa7e6-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fa7e6-134">RELATED LINKS</span></span>

[<span data-ttu-id="fa7e6-135">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="fa7e6-135">Get-AzAutomationSchedule</span></span>](./Get-AzAutomationSchedule.md)

[<span data-ttu-id="fa7e6-136">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="fa7e6-136">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)

[<span data-ttu-id="fa7e6-137">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="fa7e6-137">Set-AzAutomationSchedule</span></span>](./Set-AzAutomationSchedule.md)


