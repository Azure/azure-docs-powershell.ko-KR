---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F79AFF9A-CEDA-4E57-B5DB-9D0A7CDA6D27
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/register-azautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationScheduledRunbook.md
ms.openlocfilehash: 6f53573c6eb737d280ac24182ed84158d63d132f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373395"
---
# <span data-ttu-id="4ef8f-101">Register-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="4ef8f-101">Register-AzAutomationScheduledRunbook</span></span>

## <span data-ttu-id="4ef8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ef8f-102">SYNOPSIS</span></span>
<span data-ttu-id="4ef8f-103">Runbook을 일정에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="4ef8f-103">Associates a runbook to a schedule.</span></span>

## <span data-ttu-id="4ef8f-104">구문</span><span class="sxs-lookup"><span data-stu-id="4ef8f-104">SYNTAX</span></span>

### <span data-ttu-id="4ef8f-105">ByRunbookName(기본값)</span><span class="sxs-lookup"><span data-stu-id="4ef8f-105">ByRunbookName (Default)</span></span>
```
Register-AzAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ef8f-106">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="4ef8f-106">ByRunbookNameAndScheduleName</span></span>
```
Register-AzAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-Parameters <IDictionary>]
 [-RunOn <String>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ef8f-107">설명</span><span class="sxs-lookup"><span data-stu-id="4ef8f-107">DESCRIPTION</span></span>
<span data-ttu-id="4ef8f-108">**Register-AzAutomationScheduledRunbook** cmdlet은 일정에 Azure Automation Runbook을 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="4ef8f-108">The **Register-AzAutomationScheduledRunbook** cmdlet associates an Azure Automation runbook to a schedule.</span></span>
<span data-ttu-id="4ef8f-109">*Runbook은 ScheduleName* 매개 변수를 사용하여 지정한 일정에 따라 시작됩니다.</span><span class="sxs-lookup"><span data-stu-id="4ef8f-109">The runbook starts based on the schedule you specify using the *ScheduleName* parameter.</span></span>

## <span data-ttu-id="4ef8f-110">예제</span><span class="sxs-lookup"><span data-stu-id="4ef8f-110">EXAMPLES</span></span>

### <span data-ttu-id="4ef8f-111">예제 1: 일정과 Runbook 연결</span><span class="sxs-lookup"><span data-stu-id="4ef8f-111">Example 1: Associate a runbook with a schedule</span></span>
```powershell
PS C:\>Register-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -Name "Runbk01" -ScheduleName "Sched01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="4ef8f-112">이 명령은 Runbk01이라는 Runbook을 Contoso17이라는 Azure Automation 계정의 Sched01 일정과 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="4ef8f-112">This command associates the runbook named Runbk01 with the schedule named Sched01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="4ef8f-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="4ef8f-113">Example 2</span></span>

<span data-ttu-id="4ef8f-114">Runbook을 일정에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="4ef8f-114">Associates a runbook to a schedule.</span></span> <span data-ttu-id="4ef8f-115">(자동Generated)</span><span class="sxs-lookup"><span data-stu-id="4ef8f-115">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Register-AzAutomationScheduledRunbook -AutomationAccountName 'Contoso17' -Parameters <IDictionary> -ResourceGroupName 'ResourceGroup01' -RunbookName 'Runbk01' -ScheduleName 'Sched01'
```

## <span data-ttu-id="4ef8f-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ef8f-116">PARAMETERS</span></span>

### <span data-ttu-id="4ef8f-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="4ef8f-117">-AutomationAccountName</span></span>
<span data-ttu-id="4ef8f-118">이 cmdlet이 작동하는 Runbook에 대한 Automation 계정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ef8f-118">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="4ef8f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ef8f-119">-DefaultProfile</span></span>
<span data-ttu-id="4ef8f-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4ef8f-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ef8f-121">-Parameters</span><span class="sxs-lookup"><span data-stu-id="4ef8f-121">-Parameters</span></span>
<span data-ttu-id="4ef8f-122">키/값 쌍의 해시 테이블을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ef8f-122">Specifies a hash table of key/value pairs.</span></span>
<span data-ttu-id="4ef8f-123">키는 Runbook 매개 변수 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4ef8f-123">The keys are runbook parameter names.</span></span>
<span data-ttu-id="4ef8f-124">값은 Runbook 매개 변수 값입니다.</span><span class="sxs-lookup"><span data-stu-id="4ef8f-124">The values are runbook parameter values.</span></span>
<span data-ttu-id="4ef8f-125">Runbook이 연결된 일정에 대한 응답으로 시작되면 이러한 매개 변수가 Runbook에 전달됩니다.</span><span class="sxs-lookup"><span data-stu-id="4ef8f-125">When the runbook starts in response to the associated schedule, these parameters are passed to the runbook.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: ByRunbookNameAndScheduleName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ef8f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ef8f-126">-ResourceGroupName</span></span>
<span data-ttu-id="4ef8f-127">예약된 Runbook에 대한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ef8f-127">Specifies the name of a resource group for the scheduled runbook.</span></span>

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

### <span data-ttu-id="4ef8f-128">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="4ef8f-128">-RunbookName</span></span>
<span data-ttu-id="4ef8f-129">이 cmdlet이 일정에 연결한 Runbook의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ef8f-129">Specifies the name of the runbook that this cmdlet associates to a schedule.</span></span>

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

### <span data-ttu-id="4ef8f-130">-RunOn</span><span class="sxs-lookup"><span data-stu-id="4ef8f-130">-RunOn</span></span>
<span data-ttu-id="4ef8f-131">Hybrid Runbook Worker 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4ef8f-131">The name of the hybrid runbook worker group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName
Aliases: HybridWorker

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ef8f-132">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="4ef8f-132">-ScheduleName</span></span>
<span data-ttu-id="4ef8f-133">이 cmdlet이 Runbook을 연결한 일정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4ef8f-133">Specifies the name of the schedule to which this cmdlet associates a runbook.</span></span>

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

### <span data-ttu-id="4ef8f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ef8f-134">CommonParameters</span></span>
<span data-ttu-id="4ef8f-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4ef8f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ef8f-136">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4ef8f-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ef8f-137">입력</span><span class="sxs-lookup"><span data-stu-id="4ef8f-137">INPUTS</span></span>

### <span data-ttu-id="4ef8f-138">System.String</span><span class="sxs-lookup"><span data-stu-id="4ef8f-138">System.String</span></span>

## <span data-ttu-id="4ef8f-139">출력</span><span class="sxs-lookup"><span data-stu-id="4ef8f-139">OUTPUTS</span></span>

### <span data-ttu-id="4ef8f-140">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span><span class="sxs-lookup"><span data-stu-id="4ef8f-140">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="4ef8f-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4ef8f-141">NOTES</span></span>

## <span data-ttu-id="4ef8f-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4ef8f-142">RELATED LINKS</span></span>

[<span data-ttu-id="4ef8f-143">Get-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="4ef8f-143">Get-AzAutomationScheduledRunbook</span></span>](./Get-AzAutomationScheduledRunbook.md)

[<span data-ttu-id="4ef8f-144">Unregister-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="4ef8f-144">Unregister-AzAutomationScheduledRunbook</span></span>](./Unregister-AzAutomationScheduledRunbook.md)

