---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: C7C193CF-4E3A-4275-8289-946C99B1C553
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/unregister-azautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationScheduledRunbook.md
ms.openlocfilehash: 53cfa3ccd708871dfe639b0053cb6ab24946bace
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338534"
---
# <span data-ttu-id="fb5b4-101">Unregister-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="fb5b4-101">Unregister-AzAutomationScheduledRunbook</span></span>

## <span data-ttu-id="fb5b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb5b4-102">SYNOPSIS</span></span>
<span data-ttu-id="fb5b4-103">Runbook과 일정 간의 연결 제거</span><span class="sxs-lookup"><span data-stu-id="fb5b4-103">Removes an association between a runbook and a schedule.</span></span>

## <span data-ttu-id="fb5b4-104">구문</span><span class="sxs-lookup"><span data-stu-id="fb5b4-104">SYNTAX</span></span>

### <span data-ttu-id="fb5b4-105">ByJobScheduleId(기본값)</span><span class="sxs-lookup"><span data-stu-id="fb5b4-105">ByJobScheduleId (Default)</span></span>
```
Unregister-AzAutomationScheduledRunbook -JobScheduleId <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fb5b4-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="fb5b4-106">ByRunbookNameAndScheduleName</span></span>
```
Unregister-AzAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-Force]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb5b4-107">설명</span><span class="sxs-lookup"><span data-stu-id="fb5b4-107">DESCRIPTION</span></span>
<span data-ttu-id="fb5b4-108">**Unregister-AzAutomationScheduledRunbook** cmdlet은 Azure Automation Runbook과 일정 간의 연관을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="fb5b4-108">The **Unregister-AzAutomationScheduledRunbook** cmdlet removes the association between an Azure Automation runbook and a schedule.</span></span>
<span data-ttu-id="fb5b4-109">일정이 더 이상 Runbook을 시작하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fb5b4-109">The schedule no longer starts the runbook.</span></span>

## <span data-ttu-id="fb5b4-110">예제</span><span class="sxs-lookup"><span data-stu-id="fb5b4-110">EXAMPLES</span></span>

### <span data-ttu-id="fb5b4-111">예제 1: Runbook과 일정 간의 연결 제거</span><span class="sxs-lookup"><span data-stu-id="fb5b4-111">Example 1: Remove the association between a runbook and a schedule</span></span>
```
PS C:\>Unregister-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ResourceGroupName "ResourceGroup01" -ScheduleName "Runbk01Sched"
```

<span data-ttu-id="fb5b4-112">이 명령은 Runbk01이라는 Runbook과 Runbk01Sched라는 일정 간의 연결은 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="fb5b4-112">This command removes the association between the runbook named Runbk01 and the schedule named Runbk01Sched.</span></span>

## <span data-ttu-id="fb5b4-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb5b4-113">PARAMETERS</span></span>

### <span data-ttu-id="fb5b4-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="fb5b4-114">-AutomationAccountName</span></span>
<span data-ttu-id="fb5b4-115">이 cmdlet이 작동하는 Runbook에 대한 Automation 계정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fb5b4-115">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="fb5b4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb5b4-116">-DefaultProfile</span></span>
<span data-ttu-id="fb5b4-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="fb5b4-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb5b4-118">-Force</span><span class="sxs-lookup"><span data-stu-id="fb5b4-118">-Force</span></span>
<span data-ttu-id="fb5b4-119">ps_force</span><span class="sxs-lookup"><span data-stu-id="fb5b4-119">ps_force</span></span>

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

### <span data-ttu-id="fb5b4-120">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="fb5b4-120">-JobScheduleId</span></span>
<span data-ttu-id="fb5b4-121">예약된 Runbook의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fb5b4-121">Specifies the ID of a scheduled runbook.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: ByJobScheduleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb5b4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb5b4-122">-ResourceGroupName</span></span>
<span data-ttu-id="fb5b4-123">예약된 Runbook에 대한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fb5b4-123">Specifies the name of a resource group for the scheduled runbook.</span></span>

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

### <span data-ttu-id="fb5b4-124">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="fb5b4-124">-RunbookName</span></span>
<span data-ttu-id="fb5b4-125">이 cmdlet이 일정에서 해리하는 Runbook의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fb5b4-125">Specifies the name of the runbook that this cmdlet dissociates from a schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb5b4-126">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="fb5b4-126">-ScheduleName</span></span>
<span data-ttu-id="fb5b4-127">이 cmdlet이 Runbook을 해리하는 일정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fb5b4-127">Specifies the name of the schedule from which this cmdlet dissociates a runbook.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb5b4-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fb5b4-128">-Confirm</span></span>
<span data-ttu-id="fb5b4-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fb5b4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb5b4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb5b4-130">-WhatIf</span></span>
<span data-ttu-id="fb5b4-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="fb5b4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fb5b4-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fb5b4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb5b4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb5b4-133">CommonParameters</span></span>
<span data-ttu-id="fb5b4-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fb5b4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb5b4-135">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fb5b4-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb5b4-136">입력</span><span class="sxs-lookup"><span data-stu-id="fb5b4-136">INPUTS</span></span>

### <span data-ttu-id="fb5b4-137">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="fb5b4-137">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="fb5b4-138">System.String</span><span class="sxs-lookup"><span data-stu-id="fb5b4-138">System.String</span></span>

## <span data-ttu-id="fb5b4-139">출력</span><span class="sxs-lookup"><span data-stu-id="fb5b4-139">OUTPUTS</span></span>

### <span data-ttu-id="fb5b4-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="fb5b4-140">System.Void</span></span>

## <span data-ttu-id="fb5b4-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fb5b4-141">NOTES</span></span>

## <span data-ttu-id="fb5b4-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fb5b4-142">RELATED LINKS</span></span>

[<span data-ttu-id="fb5b4-143">Get-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="fb5b4-143">Get-AzAutomationScheduledRunbook</span></span>](./Get-AzAutomationScheduledRunbook.md)

[<span data-ttu-id="fb5b4-144">Register-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="fb5b4-144">Register-AzAutomationScheduledRunbook</span></span>](./Register-AzAutomationScheduledRunbook.md)


