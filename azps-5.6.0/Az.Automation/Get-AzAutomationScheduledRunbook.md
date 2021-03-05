---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: EE854F8A-4B6B-4831-992A-6EC318BEE234
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationscheduledrunbook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationScheduledRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationScheduledRunbook.md
ms.openlocfilehash: 6dfe33146ba2e35c728211f7f4b17fcfccf40ad7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014203"
---
# <span data-ttu-id="43baa-101">Get-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="43baa-101">Get-AzAutomationScheduledRunbook</span></span>

## <span data-ttu-id="43baa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43baa-102">SYNOPSIS</span></span>
<span data-ttu-id="43baa-103">Automation Runbook 및 관련 일정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="43baa-103">Gets Automation runbooks and associated schedules.</span></span>

## <span data-ttu-id="43baa-104">구문</span><span class="sxs-lookup"><span data-stu-id="43baa-104">SYNTAX</span></span>

### <span data-ttu-id="43baa-105">ByAll(기본값)</span><span class="sxs-lookup"><span data-stu-id="43baa-105">ByAll (Default)</span></span>
```
Get-AzAutomationScheduledRunbook [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43baa-106">ByJobScheduleId</span><span class="sxs-lookup"><span data-stu-id="43baa-106">ByJobScheduleId</span></span>
```
Get-AzAutomationScheduledRunbook -JobScheduleId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43baa-107">ByRunbookName</span><span class="sxs-lookup"><span data-stu-id="43baa-107">ByRunbookName</span></span>
```
Get-AzAutomationScheduledRunbook -RunbookName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43baa-108">ByRunbookNameAndScheduleName</span><span class="sxs-lookup"><span data-stu-id="43baa-108">ByRunbookNameAndScheduleName</span></span>
```
Get-AzAutomationScheduledRunbook -RunbookName <String> -ScheduleName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43baa-109">ByScheduleName</span><span class="sxs-lookup"><span data-stu-id="43baa-109">ByScheduleName</span></span>
```
Get-AzAutomationScheduledRunbook -ScheduleName <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43baa-110">설명</span><span class="sxs-lookup"><span data-stu-id="43baa-110">DESCRIPTION</span></span>
<span data-ttu-id="43baa-111">**Get-AzAutomationScheduledRunbook** cmdlet은 하나 이상의 Azure Automation Runbook 및 관련 일정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="43baa-111">The **Get-AzAutomationScheduledRunbook** cmdlet gets one or more Azure Automation runbooks and associated schedules.</span></span>
<span data-ttu-id="43baa-112">기본적으로 이 cmdlet은 예약된 모든 Runbook을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="43baa-112">By default, this cmdlet gets all scheduled runbooks.</span></span>
<span data-ttu-id="43baa-113">Runbook의 이름을 지정하거나 일정 또는 둘 다를 지정하여 특정 Runbook 일정을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="43baa-113">Specify the name of a runbook or a schedule or both to see specific runbook schedules.</span></span>

## <span data-ttu-id="43baa-114">예제</span><span class="sxs-lookup"><span data-stu-id="43baa-114">EXAMPLES</span></span>

### <span data-ttu-id="43baa-115">예제 1: 예약된 모든 Runbook을 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="43baa-115">Example 1: Get all scheduled runbooks</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="43baa-116">이 명령은 Contoso17이라는 Azure Automation 계정에서 예약된 모든 Runbook을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="43baa-116">This command gets all scheduled runbooks in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="43baa-117">예제 2: Runbook과 연결된 모든 일정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="43baa-117">Example 2: Get all schedules associated with a runbook</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -RunbookName "Runbk01"
```

<span data-ttu-id="43baa-118">이 명령은 Contoso17이라는 Azure Automation 계정에서 Runbook Runbk01에 대해 예약된 모든 Runbook을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="43baa-118">This command gets all scheduled runbooks for the runbook Runbk01 in the Azure Automation account named Contoso17.</span></span>

### <span data-ttu-id="43baa-119">예제 3: 일정과 연결된 모든 Runbook을 다운로드합니다.</span><span class="sxs-lookup"><span data-stu-id="43baa-119">Example 3: Get all runbooks associated with a schedule</span></span>
```
PS C:\>Get-AzAutomationScheduledRunbook -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -ScheduleName "Schedule01"
```

<span data-ttu-id="43baa-120">이 명령은 Contoso17이라는 Azure Automation 계정에서 Schedule01 일정에 대해 예약된 모든 Runbook을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="43baa-120">This command gets all scheduled runbooks for the schedule Schedule01 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="43baa-121">매개 변수</span><span class="sxs-lookup"><span data-stu-id="43baa-121">PARAMETERS</span></span>

### <span data-ttu-id="43baa-122">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="43baa-122">-AutomationAccountName</span></span>
<span data-ttu-id="43baa-123">이 cmdlet이 작동하는 Runbook에 대한 Automation 계정을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="43baa-123">Specifies an Automation account for the runbook on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="43baa-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43baa-124">-DefaultProfile</span></span>
<span data-ttu-id="43baa-125">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="43baa-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="43baa-126">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="43baa-126">-JobScheduleId</span></span>
<span data-ttu-id="43baa-127">이 cmdlet이 도착하는 예약된 작업의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="43baa-127">Specifies the ID of a scheduled job that this cmdlet gets.</span></span>

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

### <span data-ttu-id="43baa-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43baa-128">-ResourceGroupName</span></span>
<span data-ttu-id="43baa-129">이 cmdlet이 도착하는 예약된 Runbook에 대한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="43baa-129">Specifies the name of a resource group for scheduled runbooks that this cmdlet gets.</span></span>

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

### <span data-ttu-id="43baa-130">-RunbookName</span><span class="sxs-lookup"><span data-stu-id="43baa-130">-RunbookName</span></span>
<span data-ttu-id="43baa-131">이 cmdlet에서 예약된 Runbook을 받을 Runbook의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="43baa-131">Specifies the name of a runbook for which this cmdlet gets scheduled runbooks.</span></span>

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

### <span data-ttu-id="43baa-132">-ScheduleName</span><span class="sxs-lookup"><span data-stu-id="43baa-132">-ScheduleName</span></span>
<span data-ttu-id="43baa-133">이 cmdlet이 예약된 Runbook을 얻을 일정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="43baa-133">Specifies the name of a schedule for which this cmdlet gets scheduled runbooks.</span></span>

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

### <span data-ttu-id="43baa-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43baa-134">CommonParameters</span></span>
<span data-ttu-id="43baa-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="43baa-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43baa-136">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="43baa-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43baa-137">입력</span><span class="sxs-lookup"><span data-stu-id="43baa-137">INPUTS</span></span>

### <span data-ttu-id="43baa-138">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="43baa-138">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="43baa-139">System.String</span><span class="sxs-lookup"><span data-stu-id="43baa-139">System.String</span></span>

## <span data-ttu-id="43baa-140">출력</span><span class="sxs-lookup"><span data-stu-id="43baa-140">OUTPUTS</span></span>

### <span data-ttu-id="43baa-141">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span><span class="sxs-lookup"><span data-stu-id="43baa-141">Microsoft.Azure.Commands.Automation.Model.JobSchedule</span></span>

## <span data-ttu-id="43baa-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="43baa-142">NOTES</span></span>

## <span data-ttu-id="43baa-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="43baa-143">RELATED LINKS</span></span>

[<span data-ttu-id="43baa-144">Register-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="43baa-144">Register-AzAutomationScheduledRunbook</span></span>](./Register-AzAutomationScheduledRunbook.md)

[<span data-ttu-id="43baa-145">Unregister-AzAutomationScheduledRunbook</span><span class="sxs-lookup"><span data-stu-id="43baa-145">Unregister-AzAutomationScheduledRunbook</span></span>](./Unregister-AzAutomationScheduledRunbook.md)


