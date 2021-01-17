---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EE854F8A-4B6B-4831-992A-6EC318BEE234
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationScheduledRunbook.md
ms.openlocfilehash: 8080361b0dabd7d4114580777e6508fa4503fbbc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373738"
---
# <span data-ttu-id="00727-101">Get-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="00727-101">Get-AzAutomationScheduledRunbook</span></span>

## <span data-ttu-id="00727-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00727-102">SYNOPSIS</span></span>
<span data-ttu-id="00727-103">Automation Runbook 및 관련 일정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="00727-103">Gets Automation runbooks and associated schedules.</span></span>

## <span data-ttu-id="00727-104">구문</span><span class="sxs-lookup"><span data-stu-id="00727-104">SYNTAX</span></span>

### <span data-ttu-id="00727-105">ByAll(기본값)</span><span class="sxs-lookup"><span data-stu-id="00727-105">ByAll (Default)</span></span>
```
Get-AzAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00727-106">ByJobScheduleId</span><span class="sxs-lookup"><span data-stu-id="00727-106">ByJobScheduleId</span></span>
```
Get-AzAutomationScheduledRunbook -JobScheduleId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00727-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="00727-107">ByRunbookName</span></span>
```
Get-AzAutomationScheduledRunbook -RunbookName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00727-108">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="00727-108">ByRunbookNameAndScheduleName</span></span>
```
Get-AzAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="00727-109">ByScheduleName</span><span class="sxs-lookup"><span data-stu-id="00727-109">ByScheduleName</span></span>
```
Get-AzAutomationScheduledRunbook -ScheduleName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00727-110">설명</span><span class="sxs-lookup"><span data-stu-id="00727-110">DESCRIPTION</span></span>
<span data-ttu-id="00727-111">**Get-AzAutomationScheduledRunbook** cmdlet은 하나 이상의 Azure Automation Runbook 및 관련 일정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="00727-111">The **Get-AzAutomationScheduledRunbook** cmdlet gets one or more Azure Automation runbooks and associated schedules.</span></span>
<span data-ttu-id="00727-112">기본적으로 이 cmdlet은 예약된 모든 Runbook을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="00727-112">By default, this cmdlet gets all scheduled runbooks.</span></span>
<span data-ttu-id="00727-113">특정 Runbook 일정을 표시하도록 Runbook의 이름 또는 일정 또는 둘 다를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="00727-113">Specify the name of a runbook or a schedule or both to see specific runbook schedules.</span></span>

## <span data-ttu-id="00727-114">예제</span><span class="sxs-lookup"><span data-stu-id="00727-114">EXAMPLES</span></span>

### <span data-ttu-id="00727-115">예제 1: 예약된 모든 Runbook을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="00727-115">Example 1: Get all scheduled runbooks</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="00727-116">이 명령은 Contoso17이라는 Azure Automation 계정에서 예약된 모든 Runbook을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="00727-116">This command gets all scheduled runbooks in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="00727-117">예제 2: Runbook과 연결된 모든 일정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="00727-117">Example 2: Get all schedules associated with a runbook</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbk01"
```

<span data-ttu-id="00727-118">이 명령은 Contoso17이라는 Azure Automation 계정에서 Runbk01 Runbook에 대해 예약된 모든 Runbook을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="00727-118">This command gets all scheduled runbooks for the runbook Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="00727-119">예제 3: 일정과 연결된 모든 Runbook을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="00727-119">Example 3: Get all runbooks associated with a schedule</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ScheduleName "Schedule01"
```

<span data-ttu-id="00727-120">이 명령은 Contoso17이라는 Azure Automation 계정에서 Schedule01 일정에 대해 예약된 모든 Runbook을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="00727-120">This command gets all scheduled runbooks for the schedule Schedule01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="00727-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="00727-121">PARAMETERS</span></span>

### <span data-ttu-id="00727-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="00727-122">-AutomationAccountName</span></span>
<span data-ttu-id="00727-123">이 cmdlet이 작동하는 Runbook에 대한 Automation 계정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="00727-123">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="00727-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00727-124">-DefaultProfile</span></span>
<span data-ttu-id="00727-125">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="00727-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="00727-126">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="00727-126">-JobScheduleId</span></span>
<span data-ttu-id="00727-127">이 cmdlet이 얻을 예약된 작업의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="00727-127">Specifies the ID of a scheduled job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="00727-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00727-128">-ResourceGroupName</span></span>
<span data-ttu-id="00727-129">이 cmdlet에서 얻을 예약된 Runbook에 대한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="00727-129">Specifies the name of a resource group for scheduled runbooks that this cmdlet gets.</span></span>

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

### <span data-ttu-id="00727-130">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="00727-130">-RunbookName</span></span>
<span data-ttu-id="00727-131">이 cmdlet이 예약된 Runbook을 얻을 Runbook의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="00727-131">Specifies the name of a runbook for which this cmdlet gets scheduled runbooks.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookName, ByRunbookNameAndScheduleName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00727-132">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="00727-132">-ScheduleName</span></span>
<span data-ttu-id="00727-133">이 cmdlet이 예약된 Runbook을 받을 일정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="00727-133">Specifies the name of a schedule for which this cmdlet gets scheduled runbooks.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRunbookNameAndScheduleName, ByScheduleName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00727-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00727-134">CommonParameters</span></span>
<span data-ttu-id="00727-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="00727-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00727-136">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="00727-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00727-137">입력</span><span class="sxs-lookup"><span data-stu-id="00727-137">INPUTS</span></span>

### <span data-ttu-id="00727-138">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="00727-138">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="00727-139">System.String</span><span class="sxs-lookup"><span data-stu-id="00727-139">System.String</span></span>

## <span data-ttu-id="00727-140">출력</span><span class="sxs-lookup"><span data-stu-id="00727-140">OUTPUTS</span></span>

### <span data-ttu-id="00727-141">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span><span class="sxs-lookup"><span data-stu-id="00727-141">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="00727-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="00727-142">NOTES</span></span>

## <span data-ttu-id="00727-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="00727-143">RELATED LINKS</span></span>

[<span data-ttu-id="00727-144">Register-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="00727-144">Register-AzAutomationScheduledRunbook</span></span>](./Register-AzAutomationScheduledRunbook.md)

[<span data-ttu-id="00727-145">Unregister-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="00727-145">Unregister-AzAutomationScheduledRunbook</span></span>](./Unregister-AzAutomationScheduledRunbook.md)


